---
title: 'Lync Server 2013: configuración de Lync Server en un entorno entre entornos'
description: 'Lync Server 2013: configuración de Lync Server en un entorno entre entornos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Microsoft Lync Server 2013 in a cross-premises environment
ms:assetid: 700639ec-5264-4449-a8a6-d7386fad8719
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204990(v=OCS.15)
ms:contentKeyID: 48184449
ms.date: 02/21/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1ec978cd8e0e34c01c1d5cabb5bba42debd16fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433020"
---
# <a name="configuring-microsoft-lync-server-2013-in-a-cross-premises-environment"></a><span data-ttu-id="6a860-103">Configuración de Microsoft Lync Server 2013 en un entorno entre entornos</span><span class="sxs-lookup"><span data-stu-id="6a860-103">Configuring Microsoft Lync Server 2013 in a cross-premises environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6a860-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6a860-104">

<span> </span></span></span>

<span data-ttu-id="6a860-105">_**Última modificación del tema:** 2017-02-21_</span><span class="sxs-lookup"><span data-stu-id="6a860-105">_**Topic Last Modified:** 2017-02-21_</span></span>

<span data-ttu-id="6a860-106">En una configuración entre locales, algunos de los usuarios están alojados en una instalación local de Microsoft Lync Server 2013 mientras que otros usuarios se encuentran en la versión Microsoft 365 u Office 365 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6a860-106">In a cross-premise configuration, some of your users are homed on an on-premises installation of Microsoft Lync Server 2013 while other users are homed on the Microsoft 365 or Office 365 version of Lync Server.</span></span> <span data-ttu-id="6a860-107">Para configurar la autenticación de servidor a servidor en un entorno entre locales, primero debe configurar la instalación local de Lync Server 2013 para que confíe en el servidor de autorización Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6a860-107">In order to configure server-to-server authentication in a cross-premises environment, you must first configure your on-premises installation of Lync Server 2013 to trust the Microsoft 365 Authorization server.</span></span> <span data-ttu-id="6a860-108">El paso inicial de este proceso se puede llevar a cabo ejecutando la siguiente secuencia de comandos del shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="6a860-108">The initial step in this process can be carried out by running the following Lync Server Management Shell script:</span></span>

    $TenantID = (Get-CsTenant -Filter {DisplayName -eq "Fabrikam.com"}).TenantId
    
    $sts = Get-CsOAuthServer microsoft.sts -ErrorAction SilentlyContinue
            
       if ($sts -eq $null)
          {
             New-CsOAuthServer microsoft.sts -MetadataUrl "https://accounts.accesscontrol.windows.net/$TenantId/metadata/json/1"
          }
       else
          {
             if ($sts.MetadataUrl -ne  "https://accounts.accesscontrol.windows.net/$TenantId/metadata/json/1")
                {
                   Remove-CsOAuthServer microsoft.sts
                   New-CsOAuthServer microsoft.sts -MetadataUrl "https://accounts.accesscontrol.windows.net/$TenantId/metadata/json/1"
                }
            }
    
    $exch = Get-CsPartnerApplication microsoft.exchange -ErrorAction SilentlyContinue
            
    if ($exch -eq $null)
       {
          New-CsPartnerApplication -Identity microsoft.exchange -ApplicationIdentifier 00000002-0000-0ff1-ce00-000000000000 -ApplicationTrustLevel Full -UseOAuthServer
        }
    else
        {
           if ($exch.ApplicationIdentifier -ne "00000002-0000-0ff1-ce00-000000000000")
              {
                 Remove-CsPartnerApplication microsoft.exchange
                 New-CsPartnerApplication -Identity microsoft.exchange -ApplicationIdentifier 00000002-0000-0ff1-ce00-000000000000 -ApplicationTrustLevel Full -UseOAuthServer 
              }
           else
              {
                 Set-CsPartnerApplication -Identity microsoft.exchange -ApplicationTrustLevel Full -UseOAuthServer
              }
       }
    
    Set-CsOAuthConfiguration -ServiceName 00000004-0000-0ff1-ce00-000000000000

<span data-ttu-id="6a860-p102">Tenga en cuenta que el nombre de dominio kerberos de un inquilino normalmente es diferente al nombre de la organización; de hecho, el nombre de dominio kerberos casi siempre es igual al identificador del inquilino. Por tanto, la primera línea del script se usa para devolver el valor de la propiedad TenantId del inquilino especificado (en este caso, fabrikam.com) y para asignar después dicho nombre a la variable $TenantId:</span><span class="sxs-lookup"><span data-stu-id="6a860-p102">Keep in mind that the realm name for a tenant is typically different than the organization name; in fact, the realm name is almost always the same as the tenant ID. Because of that, the first line in the script is used to return the value of the TenantId property for the specified tenant (in this case, fabrikam.com) and then assign that name to the variable $TenantId:</span></span>

    $TenantID = (Get-CsTenant -DisplayName "Fabrikam.com").TenantId

<span data-ttu-id="6a860-111">Una vez completada la secuencia de comandos, debe configurar una relación de confianza entre Lync Server 2013 y el servidor de autorización, y una segunda relación de confianza entre Exchange 2013 y el servidor de autorización.</span><span class="sxs-lookup"><span data-stu-id="6a860-111">After the script completes you must then configure a trust relationship between Lync Server 2013 and the authorization server, and a second trust relationship between Exchange 2013 and the authorization server.</span></span> <span data-ttu-id="6a860-112">Solo podrá hacer esto usando los cmdlets de Microsoft Online Services.</span><span class="sxs-lookup"><span data-stu-id="6a860-112">This can only be done by using the Microsoft Online Services cmdlets.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6a860-113">Si no ha instalado los cmdlets de Microsoft Online Services, tendrá que realizar dos acciones antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="6a860-113">If you have not installed the Microsoft Online Services cmdlets you will need to do two things before proceeding.</span></span> <span data-ttu-id="6a860-114">En primer lugar, descargue e instale la versión de 64 bits de Microsoft Online Services - Ayudante para el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="6a860-114">First, download and install the 64-bit version of the Microsoft Online Services Sign-in Assistant.</span></span> <span data-ttu-id="6a860-115">Una vez completada la instalación, descargue e instale la versión de 64 del módulo Microsoft Online Services para Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a860-115">After installation is complete, download and install the 64-bit version of the Microsoft Online Services Module for Windows PowerShell.</span></span> <span data-ttu-id="6a860-116">Puede encontrar información detallada para instalar y usar el módulo Microsoft Online Services en el sitio web de Microsoft 365 u Office 365.</span><span class="sxs-lookup"><span data-stu-id="6a860-116">Detailed information for installing and using the Microsoft Online Services Module can be found on the Microsoft 365 or Office 365 web site.</span></span> <span data-ttu-id="6a860-117">Estas instrucciones también le indicarán cómo configurar el inicio de sesión único, la Federación y la sincronización entre Microsoft 365 u Office 36 y Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6a860-117">These instructions will also tell you how to configure single sign-on, federation, and synchronization between Microsoft 365 or Office 36 and Active Directory.</span></span><BR><span data-ttu-id="6a860-118">Si no ha instalado estos cmdlets, el script dará un error porque el cmdlet Get-CsTenant no estará disponible.</span><span class="sxs-lookup"><span data-stu-id="6a860-118">If you have not installed these cmdlets your script will fail because the Get-CsTenant cmdlet will not be available.</span></span>



</div>

<span data-ttu-id="6a860-119">Una vez que haya configurado Microsoft 365 y después de haber creado las entidades de servicio de Microsoft 365 u Office 365 para Lync Server 2013 y Exchange 2013, tendrá que registrar sus credenciales con estas entidades de servicio.</span><span class="sxs-lookup"><span data-stu-id="6a860-119">After you have configured Microsoft 365, and after you have created Microsoft 365 or Office 365 service principals for Lync Server 2013 and Exchange 2013, you will then need to register your credentials with these service principals.</span></span> <span data-ttu-id="6a860-120">Para ello, primero debe obtener una X. 509 Base64 guardada como un. Archivo CER.</span><span class="sxs-lookup"><span data-stu-id="6a860-120">In order to do this, you must first obtain an X.509 Base64 saved as a .CER file.</span></span> <span data-ttu-id="6a860-121">Este certificado se aplicará a las entidades de servicio de Microsoft 365 u Office 365.</span><span class="sxs-lookup"><span data-stu-id="6a860-121">This certificate will then be applied to the Microsoft 365 or Office 365 service principals.</span></span>

<span data-ttu-id="6a860-122">Cuando haya obtenido el certificado X. 509, inicie el módulo Microsoft Online Services (haga clic en **Inicio**, haga clic en **todos los programas**, haga clic en **Microsoft Online Services** y, a continuación, haga clic en **Microsoft Online Services Module para Windows PowerShell**).</span><span class="sxs-lookup"><span data-stu-id="6a860-122">When you have obtained the X.509 certificate, start the Microsoft Online Services Module (click **Start**, click **All Programs**, click **Microsoft Online Services**, and then click **Microsoft Online Services Module for Windows PowerShell**).</span></span> <span data-ttu-id="6a860-123">Después de que se abra el módulo servicios, escriba lo siguiente para importar el módulo Microsoft online Windows PowerShell que contiene los cmdlets que se pueden usar para administrar entidades de servicio:</span><span class="sxs-lookup"><span data-stu-id="6a860-123">After the Services Module opens, type the following to import the Microsoft Online Windows PowerShell module containing the cmdlets that can be used to manage service principals:</span></span>

    Import-Module MSOnlineExtended

<span data-ttu-id="6a860-124">Cuando se haya importado el módulo, escriba el siguiente comando y, a continuación, presione Entrar para conectarse a Microsoft 365:</span><span class="sxs-lookup"><span data-stu-id="6a860-124">When the module has been imported, type the following command and then press ENTER in order to connect to Microsoft 365:</span></span>

    Connect-MsolService

<span data-ttu-id="6a860-125">Tras presionar ENTRAR, aparecerá un cuadro de diálogo de credenciales.</span><span class="sxs-lookup"><span data-stu-id="6a860-125">After you press ENTER, a credentials dialog box will appear.</span></span> <span data-ttu-id="6a860-126">Escriba su nombre de usuario y contraseña de Microsoft 365 u Office 365 en el cuadro de diálogo y, a continuación, haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="6a860-126">Enter your Microsoft 365 or Office 365 user name and password in the dialog box, and then click OK.</span></span>

<span data-ttu-id="6a860-127">En cuanto esté conectado a Microsoft 365, puede ejecutar el comando siguiente para obtener información sobre las entidades de servicio:</span><span class="sxs-lookup"><span data-stu-id="6a860-127">As soon as you are connected to Microsoft 365 you can then run the following command in order to return information about your service principals:</span></span>

    Get-MsolServicePrincipal

<span data-ttu-id="6a860-128">La información relativa a todas las entidades de servicio que aparecerá será similar a esta:</span><span class="sxs-lookup"><span data-stu-id="6a860-128">You should get back information similar to this for all your service principals:</span></span>

    ExtensionData        : System.Runtime.Serialization.ExtensionDataObject
    AccountEnabled       : True
    Addresses            : {}
    AppPrincipalId       : 00000004-0000-0ff1-ce00-000000000000
    DisplayName          : Microsoft Lync Server
    ObjectId             : aada5fbd-c0ae-442a-8c0b-36fec40602e2
    ServicePrincipalName : LyncServer/litwareinc.com
    TrustedForDelegation : True

<span data-ttu-id="6a860-129">El paso siguiente es importar, codificar y asignar el certificado X.509.</span><span class="sxs-lookup"><span data-stu-id="6a860-129">The next step is to import, encode, and assign the X.509 certificate.</span></span> <span data-ttu-id="6a860-130">Para importar y codificar el certificado, use los siguientes comandos de Windows PowerShell y asegúrese de especificar la ruta de acceso completa del archivo a su. CER al llamar al método Import:</span><span class="sxs-lookup"><span data-stu-id="6a860-130">To import and encode the certificate, use the following Windows PowerShell commands, being sure to specify the complete file path to your .CER file when you call the Import method:</span></span>

    $certificate = New-Object System.Security.Cryptography.X509Certificates.X509Certificate
    $certificate.Import("C:\Certificates\Office365.cer")
    $binaryValue = $certificate.GetRawCertData()
    $credentialsValue = [System.Convert]::ToBase64String($binaryValue)

<span data-ttu-id="6a860-131">Una vez que el certificado se ha importado y codificado, puede asignar el certificado a las entidades de servicio de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6a860-131">After the certificate has been imported and encoded, you can then assign the certificate to your Microsoft 365 service principals.</span></span> <span data-ttu-id="6a860-132">Para ello, en primer lugar use el Get-MsolServicePrincipal para recuperar el valor de la propiedad AppPrincipalId para las entidades de servicio Lync Server y Microsoft Exchange. el valor de la propiedad AppPrincipalId se usará para identificar la entidad de servicio a la que se asigna el certificado.</span><span class="sxs-lookup"><span data-stu-id="6a860-132">To do that, first use the Get-MsolServicePrincipal to retrieve the value of the AppPrincipalId property for both the Lync Server and the Microsoft Exchange service principals; the value of the AppPrincipalId property will be used to identify the service principal being assigned the certificate.</span></span> <span data-ttu-id="6a860-133">Con el valor de la propiedad AppPrincipalId para Lync Server 2013, use el siguiente comando para asignar el certificado a la versión de Microsoft 365 de Lync Server (las propiedades StartDate y EndDate deben corresponderse con el período de validez del certificado):</span><span class="sxs-lookup"><span data-stu-id="6a860-133">With the AppPrincipalId property value for Lync Server 2013 in hand, use the following command to assign the certificate to the Microsoft 365 version of Lync Server (the StartDate and EndDate properties should correspond to the validity period for the certificate):</span></span>

    New-MsolServicePrincipalCredential -AppPrincipalId 00000004-0000-0ff1-ce00-000000000000 -Type Asymmetric -Usage Verify -Value $credentialsValue -StartDate 6/1/2012 -EndDate 5/31/2013

<span data-ttu-id="6a860-134">Después, debe repetir el comando, esta vez usando el valor de la propiedad AppPrincipalId para Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="6a860-134">You should then repeat the command, this time using the AppPrincipalId property value for Exchange 2013.</span></span>

<span data-ttu-id="6a860-135">Si más tarde necesita eliminar el certificado, primero recupere el KeyId del certificado con:</span><span class="sxs-lookup"><span data-stu-id="6a860-135">If you later need to delete that certificate, you can do so by first retrieving the KeyId for the certificate:</span></span>

    Get-MsolServicePrincipalCredential -AppPrincipalId 00000004-0000-0ff1-ce00-000000000000

<span data-ttu-id="6a860-136">El comando devolverá datos similares a estos:</span><span class="sxs-lookup"><span data-stu-id="6a860-136">That command will return data like this one:</span></span>

    Type      : Asymmetric
    Value     : 
    KeyId     : bc2795f3-2387-4543-a95d-f92c85c7a1b0
    StartDate : 6/1/2012 8:00:00 AM
    EndDate   : 5/31/2013 8:00:00 AM
    Usage     : Verify

<span data-ttu-id="6a860-137">Entonces podrá eliminar el certificado usando un comando como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="6a860-137">You can then delete the certificate by using a command similar to this:</span></span>

    Remove-MsolServicePrincipalCredential -AppPrincipalId 00000004-0000-0ff1-ce00-000000000000 -KeyId bc2795f3-2387-4543-a95d-f92c85c7a1b0

<span data-ttu-id="6a860-138">Además de asignar un certificado, también debe configurar la entidad de servicio de Microsoft 365 para Exchange Online agregando el nombre principal de servidor de la versión local de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6a860-138">In addition to assigning a certificate you must also configure the Microsoft 365 Service Principal for Exchange Online by adding the Server Principal Name for your on-premise version of Lync Server 2013.</span></span> <span data-ttu-id="6a860-139">Esto puede hacerse ejecutando las cuatro líneas siguientes en una sesión de Microsoft Online Services PowerShell:</span><span class="sxs-lookup"><span data-stu-id="6a860-139">This can be done by running the following four lines in a Microsoft Online Services PowerShell session:</span></span>

    Set-MSOLServicePrincipal -AppPrincipalID 00000002-0000-0ff1-ce00-000000000000 -AccountEnabled $true
    
    $lyncSP = Get-MSOLServicePrincipal -AppPrincipalID 00000004-0000-0ff1-ce00-000000000000
    $lyncSP.ServicePrincipalNames.Add("00000004-0000-0ff1-ce00-000000000000/lync.contoso.com")
    Set-MSOLServicePrincipal -AppPrincipalID 00000004-0000-0ff1-ce00-000000000000 -ServicePrincipalNames $lyncSP.ServicePrincipalNames

<span data-ttu-id="6a860-140"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6a860-140"></div>

<span> </span>

</div>

</div>

</span></span></div>

