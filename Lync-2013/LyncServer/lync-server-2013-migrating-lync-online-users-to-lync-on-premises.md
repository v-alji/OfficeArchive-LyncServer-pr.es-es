---
title: 'Lync Server 2013: migración de usuarios de Lync Online a Lync local'
description: 'Lync Server 2013: migración de usuarios de Lync Online a Lync local.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migrating Lync Online users to Lync on-premises
ms:assetid: 0e29605b-db2d-4cbf-b6a9-15db6b9fdabc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689115(v=OCS.15)
ms:contentKeyID: 62258120
ms.date: 11/13/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 620bc07def8e3c1f6b761c6398b452b4dbcd3b04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445984"
---
# <a name="migrating-lync-online-users-to-lync-on-premises-in-lync-server-2013"></a><span data-ttu-id="230a8-103">Migrar usuarios de Lync Online a Lync local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="230a8-103">Migrating Lync Online users to Lync on-premises in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="230a8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="230a8-104">

<span> </span></span></span>

<span data-ttu-id="230a8-105">_**Última modificación del tema:** 2015-11-13_</span><span class="sxs-lookup"><span data-stu-id="230a8-105">_**Topic Last Modified:** 2015-11-13_</span></span>

<div class="">


> [!IMPORTANT]  
> <span data-ttu-id="230a8-106">Estos pasos solo son necesarios para migrar cuentas de usuario que se han habilitado originalmente para Lync en Lync Online, antes de implementar Lync local.</span><span class="sxs-lookup"><span data-stu-id="230a8-106">These steps are necessary only for migrating user accounts that were originally enabled for Lync in Lync Online, before you deployed Lync on-premises.</span></span> <span data-ttu-id="230a8-107">Para mover los usuarios que se habilitaron originalmente para Lync local y, después, se movieron a Lync Online, vea <A href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">administrar usuarios en una implementación híbrida de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="230a8-107">To move users who were originally enabled for Lync on-premises, then later moved to Lync Online, see <A href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Administering users in a hybrid Lync Server 2013 deployment</A>.</span></span><BR><span data-ttu-id="230a8-108">Además, todos los usuarios que se muevan necesitarán tener cuentas en Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="230a8-108">Additionally, all users being moved must have accounts in the on-premises Active Directory.</span></span>



</div>

<div>

## <a name="migrating-user-accounts-originally-enabled-in-lync-online-to-lync-on-premises"></a><span data-ttu-id="230a8-109">Migrar cuentas de usuario originalmente habilitadas en Lync Online a Lync local</span><span class="sxs-lookup"><span data-stu-id="230a8-109">Migrating User Accounts Originally Enabled in Lync Online to Lync On-Premises</span></span>

1.  <span data-ttu-id="230a8-110">En primer lugar, asegúrese de que su organización está configurada para una implementación híbrida.</span><span class="sxs-lookup"><span data-stu-id="230a8-110">First, make sure that your organization is configured for hybrid.</span></span>
    
      - <span data-ttu-id="230a8-111">Instale la herramienta de sincronización de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="230a8-111">Install the Azure Active Directory Sync Tool.</span></span> <span data-ttu-id="230a8-112">Para obtener más información, consulte <https://social.technet.microsoft.com/wiki/contents/articles/19098.howto-install-the-windows-azure-active-directory-sync-tool.aspx>.</span><span class="sxs-lookup"><span data-stu-id="230a8-112">For more information, see <https://social.technet.microsoft.com/wiki/contents/articles/19098.howto-install-the-windows-azure-active-directory-sync-tool.aspx>.</span></span>
    
      - <span data-ttu-id="230a8-113">Para permitir a los usuarios usar el inicio de sesión único en Lync Online, instale los servicios de Federación de Active Directory <https://social.technet.microsoft.com/wiki/contents/articles/1011.active-directory-federation-services-ad-fs-overview.aspx> .</span><span class="sxs-lookup"><span data-stu-id="230a8-113">To enable your users to use single sign-on for Lync Online, install Active Directory Federation Services <https://social.technet.microsoft.com/wiki/contents/articles/1011.active-directory-federation-services-ad-fs-overview.aspx>.</span></span>
    
      - <span data-ttu-id="230a8-114">En la implementación local, en el shell de administración de Lync Server, escriba los siguientes cmdlets para crear el proveedor de hospedaje para Lync Online:</span><span class="sxs-lookup"><span data-stu-id="230a8-114">On your on-premises deployment, in Lync Server Management Shell, type the following cmdlets to create the hosting provider for Lync Online:</span></span>
        
           ```PowerShell
           Set-CsAccessEdgeConfiguration -AllowOutsideUsers 1 -AllowFederatedUsers 1 -UseDnsSrvRouting -EnablePartnerDiscovery $true
           ```
        
           ```PowerShell
            New-CsHostingProvider -Identity LyncOnline -ProxyFqdn "sipfed.online.lync.com" -Enabled $true -EnabledSharedAddressSpace $true -HostsOCSUsers $true -VerificationLevel UseSourceVerification -IsLocal $false -AutodiscoverUrl https://webdir.online.lync.com/Autodiscover/AutodiscoverService.svc/root
           ```

2.  <span data-ttu-id="230a8-115">Confirme que, en los servidores perimetrales locales, tiene la cadena de certificados que habilita la conexión a Lync Online, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="230a8-115">Confirm that, on your on-premises Edge Servers, you have the certificate chain that enables connection to Lync Online, as shown in the following table.</span></span> <span data-ttu-id="230a8-116">Puede descargar esta cadena aquí: https://support.office.com/article/office-365-certificate-chains-0c03e6b3-e73f-4316-9e2b-bf4091ae96bb</span><span class="sxs-lookup"><span data-stu-id="230a8-116">You can download this chain here: https://support.office.com/article/office-365-certificate-chains-0c03e6b3-e73f-4316-9e2b-bf4091ae96bb</span></span>


    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="230a8-117">Certificado</span><span class="sxs-lookup"><span data-stu-id="230a8-117">Certificate</span></span></th>
    <th><span data-ttu-id="230a8-118">Almacén de certificado</span><span class="sxs-lookup"><span data-stu-id="230a8-118">Certificate Store</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="230a8-119">Baltimore CyberTrust Root</span><span class="sxs-lookup"><span data-stu-id="230a8-119">Baltimore CyberTrust Root</span></span></p></td>
    <td><p><span data-ttu-id="230a8-120">CA raíz de confianza</span><span class="sxs-lookup"><span data-stu-id="230a8-120">Trusted Root CA</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="230a8-121">Microsoft Internet Authority (nuevo certificado CA)</span><span class="sxs-lookup"><span data-stu-id="230a8-121">Microsoft Internet Authority (New CA certificate)</span></span></p></td>
    <td><p><span data-ttu-id="230a8-122">CA intermedia</span><span class="sxs-lookup"><span data-stu-id="230a8-122">Intermediate CA</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="230a8-123">MSIT Machine Auth CA2 (nueva CA2 de emisión)</span><span class="sxs-lookup"><span data-stu-id="230a8-123">MSIT Machine Auth CA2 (New Issuing CA2)</span></span></p></td>
    <td><p><span data-ttu-id="230a8-124">CA intermedia</span><span class="sxs-lookup"><span data-stu-id="230a8-124">Intermediate CA</span></span></p></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="230a8-125">En su Active Directory local, habilite las cuentas de usuario afectadas para Lync local.</span><span class="sxs-lookup"><span data-stu-id="230a8-125">In your on-premises Active Directory, enable the affected user accounts for Lync on-premises.</span></span> <span data-ttu-id="230a8-126">Para hacerlo para un usuario individual, escriba el cmdlet siguiente:</span><span class="sxs-lookup"><span data-stu-id="230a8-126">You can do this for an individual user by typing the following cmdlet:</span></span>
    
        Enable-CsUser
        -Identity "username" 
        -SipAddress "sip: username@contoso.com"
        -HostingProviderProxyFqdn "sipfed.online.lync.com"
    
    <span data-ttu-id="230a8-127">También puede crear un script que lea los nombres de usuario de un archivo y los indique como entrada al cmdlet Enable-CsUser cmdlet:</span><span class="sxs-lookup"><span data-stu-id="230a8-127">Or you can create a script that reads user names from a file and provides them as input to the Enable-CsUser cmdlet:</span></span>
    
        Enable-CsUser
        -Identity $Identity 
        -SipAddress $SipAddress 
        -HostingProviderProxyFqdn "sipfed.online.lync.com"

4.  <span data-ttu-id="230a8-128">Ejecute DirSync para sincronizar los usuarios de Lync Online con los usuarios de Lync local actualizados.</span><span class="sxs-lookup"><span data-stu-id="230a8-128">Run DirSync to sync the Lync Online users with the updated Lync on-premises users.</span></span>

5.  <span data-ttu-id="230a8-129">Actualice algunos registros DNS para dirigir todo el tráfico SIP a Lync local:</span><span class="sxs-lookup"><span data-stu-id="230a8-129">Update some DNS records to direct all SIP traffic to Lync on-premises:</span></span>
    
      - <span data-ttu-id="230a8-130">Actualice el registro A **lyncdiscover.contoso.com** para que apunte al FQDN del servidor proxy inverso local.</span><span class="sxs-lookup"><span data-stu-id="230a8-130">Update the **lyncdiscover.contoso.com** A record to point to the FQDN of the on-premises reverse proxy server.</span></span>
    
      - <span data-ttu-id="230a8-131">Actualice el **_\_ SIP_. \_** registro SRV de TLS.contoso.com para resolver la dirección IP pública o VIP del servicio perimetral de acceso de Lync local.</span><span class="sxs-lookup"><span data-stu-id="230a8-131">Update the **_\_sip_.\_tls.contoso.com** SRV record to resolve to the public IP or VIP address of the Access Edge service of Lync on-premises.</span></span>
    
      - <span data-ttu-id="230a8-132">Actualice el **_\_ sipfederationtls_. \_** registro SRV de TCP.contoso.com para resolver la dirección IP pública o VIP del servicio perimetral de acceso de Lync local.</span><span class="sxs-lookup"><span data-stu-id="230a8-132">Update the **_\_sipfederationtls_.\_tcp.contoso.com** SRV record to resolve to the public IP or VIP address of the Access Edge service of Lync on-premises.</span></span>
    
      - <span data-ttu-id="230a8-133">Si su organización usa DNS dividido (a veces denominado “DNS de horizonte dividido”), asegúrese de que los usuarios que están convirtiendo nombres por medio de la zona de DNS interna se dirigen al conjunto front-end.</span><span class="sxs-lookup"><span data-stu-id="230a8-133">If your organization uses split DNS (sometimes called “split-brain DNS”), make sure that users resolving names through the internal DNS zone are directed to the Front End Pool.</span></span>

6.  <span data-ttu-id="230a8-134">Escriba el `Get-CsUser` cmdlet para comprobar algunas propiedades sobre los usuarios que va a mover.</span><span class="sxs-lookup"><span data-stu-id="230a8-134">Type the `Get-CsUser` cmdlet to check some properties about the users you’ll be moving.</span></span> <span data-ttu-id="230a8-135">Desea asegurarse de que el HostingProviderProxyFQDN esté establecido en y de `"sipfed.online.lync.com"` que las direcciones SIP se hayan establecido correctamente.</span><span class="sxs-lookup"><span data-stu-id="230a8-135">You want to make sure that the HostingProviderProxyFQDN is set to `"sipfed.online.lync.com"` and that the SIP addresses are set correctly.</span></span>

7.  <span data-ttu-id="230a8-136">Mueva los usuarios de Lync Online a Lync local.</span><span class="sxs-lookup"><span data-stu-id="230a8-136">Move Lync Online users to Lync on-premises.</span></span>
    
    <span data-ttu-id="230a8-137">Para mover un solo usuario, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="230a8-137">To move a single user, type this:</span></span>
    
       ```PowerShell
       $cred = Get-Credential
       ```
    
       ```PowerShell
       Move-CsUser -Identity <username>@contoso.com -Target "<fe-pool>.contoso.com" -Credential $cred -HostedMigrationOverrideURL <URL>
       ```
    
    <span data-ttu-id="230a8-138">Para mover varios usuarios, use el cmdlet **Get-CsUSer** con el parámetro –Filter para seleccionar a los usuarios con una propiedad concreta.</span><span class="sxs-lookup"><span data-stu-id="230a8-138">You can move multiple users by using the **Get-CsUSer** cmdlet with the –Filter parameter to select the users with a specific property.</span></span> <span data-ttu-id="230a8-139">Por ejemplo, puede seleccionar todos los usuarios de Lync Online filtrando por {proveedor de hospedaje – EQ "sipfed.online.lync.om"}.</span><span class="sxs-lookup"><span data-stu-id="230a8-139">For example, you could select all Lync Online users by filtering for {Hosting Provider –eq “sipfed.online.lync.om”}.</span></span> <span data-ttu-id="230a8-140">Luego, puede transferir los usuarios devueltos al cmdlet **Move-CsUSer**, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="230a8-140">You can then pipe the returned users to the **Move-CsUSer** cmdlet, as shown below.</span></span>
    
        Get-CsUser -Filter {Hosting Provider -eq "sipfed.online.lync.com"} | Move-CsUser -Target "<fe-pool>.contoso.com" -Credential $creds -HostedMigrationOverrideURL <URL>
    
    <span data-ttu-id="230a8-141">El formato de la dirección URL especificada para el parámetro **HostedMigrationOverrideUrl** debe ser la dirección URL del grupo en el que se está ejecutando el servicio de migración hospedada, en el siguiente formato: *https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.SVC*.</span><span class="sxs-lookup"><span data-stu-id="230a8-141">The format of the URL specified for the **HostedMigrationOverrideUrl** parameter must be the URL to the pool where the Hosted Migration service is running, in the following format: *Https://\<Pool FQDN\>/HostedMigration/hostedmigrationService.svc*.</span></span>
    
    <span data-ttu-id="230a8-142">Para determinar la dirección URL del servicio de migración hospedada, consulte la URL del panel de control de Lync Online de la cuenta de la organización de Microsoft 365 u Office 365.</span><span class="sxs-lookup"><span data-stu-id="230a8-142">You can determine the URL to the Hosted Migration Service by viewing the URL for the Lync Online Control Panel for your Microsoft 365 or Office 365 organization account.</span></span>
    
    <div>
    
    ## <a name="to-determine-the-hosted-migration-service-url-for-your-organizaton"></a><span data-ttu-id="230a8-143">Para determinar la dirección URL del servicio de migración hospedada de su organización</span><span class="sxs-lookup"><span data-stu-id="230a8-143">To determine the Hosted Migration Service URL for your organizaton</span></span>
    
    1.  <span data-ttu-id="230a8-144">Inicie sesión en su organización de Microsoft 365 u Office 365 como administrador.</span><span class="sxs-lookup"><span data-stu-id="230a8-144">Log in to your Microsoft 365 or Office 365 organization as an administrator.</span></span>
    
    2.  <span data-ttu-id="230a8-145">Abra el **centro de administración de Lync**.</span><span class="sxs-lookup"><span data-stu-id="230a8-145">Open the **Lync admin center**.</span></span>
    
    3.  <span data-ttu-id="230a8-146">Con el **centro de administración de Lync** mostrado, seleccione y copie la dirección URL en la barra de direcciones hasta **Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="230a8-146">With the **Lync admin center** displayed, select and copy the URL in the address bar up to **lync.com**.</span></span> <span data-ttu-id="230a8-147">Una dirección URL de ejemplo es muy similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="230a8-147">An example URL looks similar to the following:</span></span>
        
        `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`
    
    4.  <span data-ttu-id="230a8-148">Sustituya **webdir** en la dirección URL por **admin**. Quedará como a continuación:</span><span class="sxs-lookup"><span data-stu-id="230a8-148">Replace **webdir** in the URL with **admin**, resulting in the following:</span></span>
        
        `https://admin0a.online.lync.com`
    
    5.  <span data-ttu-id="230a8-149">Anexe la cadena siguiente a la URL: **/MigraciónHospedada/ServicioDeMigraciónHospedada.svc**.</span><span class="sxs-lookup"><span data-stu-id="230a8-149">Append the following string to the URL: **/HostedMigration/hostedmigrationservice.svc**.</span></span>
        
        <span data-ttu-id="230a8-150">La dirección URL resultante, que es el valor de **HostedMigrationOverrideUrl**, necesita ser como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="230a8-150">The resulting URL, which is the value of the **HostedMigrationOverrideUrl**, should look like the following:</span></span>
        
        `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`
    
    </div>
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="230a8-151">El tamaño máximo por defecto de los archivos de registro de la transacción de la base de datos rtcxds es de 16 GB.</span><span class="sxs-lookup"><span data-stu-id="230a8-151">The default maximum size for transaction log files of the rtcxds database is 16 GB.</span></span> <span data-ttu-id="230a8-152">Puede que no sea lo suficiente grande para mover un gran número de usuarios a la vez, especialmente si la creación de reflejos está habilitada.</span><span class="sxs-lookup"><span data-stu-id="230a8-152">This might not be big enough if you’re moving a large number of users at once, especially if you have mirroring enabled.</span></span> <span data-ttu-id="230a8-153">Para solucionarlo, puede aumentar el tamaño del archivo o hacer regularmente una copia de seguridad de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="230a8-153">To get around this you can increase the file size or back up the log files regularly.</span></span> <span data-ttu-id="230a8-154">Para obtener más información, consulte <A class=uri href="https://support.microsoft.com/kb/2756725">https://support.microsoft.com/kb/2756725</A>.</span><span class="sxs-lookup"><span data-stu-id="230a8-154">For more information, see <A class=uri href="https://support.microsoft.com/kb/2756725">https://support.microsoft.com/kb/2756725</A>.</span></span>

    
    </div>

8.  <span data-ttu-id="230a8-155">Este paso es opcional.</span><span class="sxs-lookup"><span data-stu-id="230a8-155">This is an optional step.</span></span> <span data-ttu-id="230a8-156">Si tiene que llevar a cabo la integración con Exchange 2013 Online, tendrá que usar un proveedor de hospedaje adicional.</span><span class="sxs-lookup"><span data-stu-id="230a8-156">If you need to integrate with Exchange 2013 Online, you need to use an additional hosting provider.</span></span> <span data-ttu-id="230a8-157">Para obtener información detallada, consulte [configuración de la integración de Lync Server 2013 con Exchange Online](lync-server-2013-configuring-on-premises-lync-server-integration-with-exchange-online.md).</span><span class="sxs-lookup"><span data-stu-id="230a8-157">For details, see [Configuring on-premises Lync Server 2013 integration with Exchange Online](lync-server-2013-configuring-on-premises-lync-server-integration-with-exchange-online.md).</span></span>

9.  <span data-ttu-id="230a8-p110">Ahora se han movido los usuarios. Para comprobar si un usuario tiene valores correctos para los atributos que se muestran en la tabla siguiente, escriba este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="230a8-p110">The users are now moved. To check that a user has correct values for the attributes shown in the following table, type this cmdlet:</span></span>
    
        Get-CsUser | fl DisplayName,HostingProvider,SipAddress,Enabled
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="230a8-160">Atributo de Active Directory</span><span class="sxs-lookup"><span data-stu-id="230a8-160">Active Directory attribute</span></span></th>
    <th><span data-ttu-id="230a8-161">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="230a8-161">Attribute name</span></span></th>
    <th><span data-ttu-id="230a8-162">Valor correcto para el usuario de Lync Online</span><span class="sxs-lookup"><span data-stu-id="230a8-162">Correct value for Lync Online user</span></span></th>
    <th><span data-ttu-id="230a8-163">Valor correcto para usuarios locales de Lync</span><span class="sxs-lookup"><span data-stu-id="230a8-163">Correct value for Lync on–premises users</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="230a8-164">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="230a8-164">msRTCSIP-DeploymentLocator</span></span></p></td>
    <td><p><span data-ttu-id="230a8-165">Proveedor de hospedaje</span><span class="sxs-lookup"><span data-stu-id="230a8-165">HostingProvider</span></span></p></td>
    <td><p><span data-ttu-id="230a8-166">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="230a8-166">sipfed.online.lync.com</span></span></p></td>
    <td><p><span data-ttu-id="230a8-167">SRV:</span><span class="sxs-lookup"><span data-stu-id="230a8-167">SRV:</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="230a8-168">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="230a8-168">msRTCSIP-PrimaryUserAddress</span></span></p></td>
    <td><p><span data-ttu-id="230a8-169">Dirección SIP</span><span class="sxs-lookup"><span data-stu-id="230a8-169">SIPAddress</span></span></p></td>
    <td><p><span data-ttu-id="230a8-170">sip:userName@contoso.com</span><span class="sxs-lookup"><span data-stu-id="230a8-170">sip:userName@contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="230a8-171">sip:userName@contoso.com</span><span class="sxs-lookup"><span data-stu-id="230a8-171">sip:userName@contoso.com</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="230a8-172">msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="230a8-172">msRTCSIP-UserEnabled</span></span></p></td>
    <td><p><span data-ttu-id="230a8-173">Habilitado</span><span class="sxs-lookup"><span data-stu-id="230a8-173">Enabled</span></span></p></td>
    <td><p><span data-ttu-id="230a8-174">True</span><span class="sxs-lookup"><span data-stu-id="230a8-174">True</span></span></p></td>
    <td><p><span data-ttu-id="230a8-175">True</span><span class="sxs-lookup"><span data-stu-id="230a8-175">True</span></span></p></td>
    </tr>
    </tbody>
    </table>


10. <span data-ttu-id="230a8-176">Cada usuario que se haya movido necesitará cerrar sesión en Lync y, a continuación, volver a iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="230a8-176">Each user who has been moved will need to log out of Lync, then log back in.</span></span> <span data-ttu-id="230a8-177">Al hacerlo, tendrán que verificar sus listas de contactos y agregar contactos si es necesario.</span><span class="sxs-lookup"><span data-stu-id="230a8-177">When they log in they should verify their contact lists, and add contacts if needed.</span></span>
    
    <span data-ttu-id="230a8-178">Tenga en cuenta que las reuniones programadas no se migran de Lync Online a Lync local.</span><span class="sxs-lookup"><span data-stu-id="230a8-178">Note that scheduled meetings are not migrated from Lync Online to Lync on-premises.</span></span> <span data-ttu-id="230a8-179">Los usuarios tendrán que volver a programar las reuniones una vez movidos.</span><span class="sxs-lookup"><span data-stu-id="230a8-179">Users will need to reschedule these meetings after being moved.</span></span>
    
    <span data-ttu-id="230a8-180">Después de que se actualicen los registros DNS y de que todos los usuarios se dirijan a local, el atributo Hostingprovider manda indica al usuario de Lync que use registros SRV o los dirija al proveedor en línea "sipfed.online.lync.com".</span><span class="sxs-lookup"><span data-stu-id="230a8-180">After the DNS records are updated and all users are directed to On premise, the HostingProvider attribute directs the Lync user to either use SRV records or direct them to the Online provider “sipfed.online.lync.com.”</span></span>

<span data-ttu-id="230a8-181"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="230a8-181"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

