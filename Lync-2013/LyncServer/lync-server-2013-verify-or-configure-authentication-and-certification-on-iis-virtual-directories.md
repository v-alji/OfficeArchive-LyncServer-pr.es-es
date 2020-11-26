---
title: 'Lync Server 2013: Comprobar o configurar la autenticación y la certificación en directorios virtuales IIS'
description: 'Lync Server 2013: comprobar o configurar la autenticación y la certificación en los directorios virtuales de IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify or configure authentication and certification on IIS virtual directories
ms:assetid: 3ca90be0-1d64-447c-807a-3a2ee3bf625e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429702(v=OCS.15)
ms:contentKeyID: 48183883
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e4d583eda7f0c7fb32b51dd5df6eb48af9b20d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438947"
---
# <a name="verify-or-configure-authentication-and-certification-on-iis-virtual-directories-in-lync-server-2013"></a><span data-ttu-id="821d9-103">Comprobar o configurar la autenticación y la certificación en directorios virtuales IIS en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="821d9-103">Verify or configure authentication and certification on IIS virtual directories in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="821d9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="821d9-104">

<span> </span></span></span>

<span data-ttu-id="821d9-105">_**Última modificación del tema:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="821d9-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="821d9-106">Use el procedimiento siguiente para configurar el certificado en los directorios virtuales de servicios de Internet Information Server (IIS) o comprobar que el certificado está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="821d9-106">Use the following procedure to configure the certificate on your Internet Information Services (IIS) virtual directories or verify that the certificate is configured correctly.</span></span> <span data-ttu-id="821d9-107">Realice el siguiente procedimiento en cada servidor que ejecute IIS en el grupo de servidores de Lync interno y en el director opcional. o servidores de grupo de directores.</span><span class="sxs-lookup"><span data-stu-id="821d9-107">Perform the following procedure on each server running IIS in your internal Lync Server pool and the optional Director.or Director pool servers.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="821d9-108">El procedimiento siguiente define un procedimiento para solicitar un certificado combinado que se usa para todos los propósitos de Lync Server, sitio Web interno y sitio web externo en IIS.</span><span class="sxs-lookup"><span data-stu-id="821d9-108">The following procedure defines a procedure to request a combined certificate that is used for all purposes Lync Server, Internal Web Site and External Web Site in IIS.</span></span> <span data-ttu-id="821d9-109">Lync Server 2010 presentó un conjunto de cmdlets de Windows PowerShell de Shell de administración de Lync Server &nbsp; para la administración de solicitudes de certificados, importaciones y asignaciones.</span><span class="sxs-lookup"><span data-stu-id="821d9-109">Lync Server 2010 introduced a set of Lync Server Management Shell&nbsp;Windows PowerShell cmdlets for the express purpose of managing certificate request, import, and assignment.</span></span> <span data-ttu-id="821d9-110">En el procedimiento se supone que hay una entidad de certificación (CA) implementada internamente que puede procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="821d9-110">The procedure assumes that there is an internally deployed certification authority (CA) that can process the request.</span></span> <span data-ttu-id="821d9-111">Si usa certificados públicos para sus propósitos de Lync Server, o si su CA requiere una solicitud sin conexión, consulte la sintaxis detallada de este tema para obtener información sobre el parámetro-output.</span><span class="sxs-lookup"><span data-stu-id="821d9-111">If you use public certificates for your Lync Server purposes, or your CA requires an offline request, see the detailed syntax in this topic for information on the –Output parameter.</span></span> <span data-ttu-id="821d9-112"><A href="https://docs.microsoft.com/powershell/module/skype/Request-CsCertificate">Solicitud-CsCertificate</A></span><span class="sxs-lookup"><span data-stu-id="821d9-112"><A href="https://docs.microsoft.com/powershell/module/skype/Request-CsCertificate">Request-CsCertificate</A></span></span>



</div>

<div>

## <a name="to-configure-authentication-and-certificates-on-iis-virtual-directories"></a><span data-ttu-id="821d9-113">Para configurar la autenticación y los certificados en directorios virtuales de IIS</span><span class="sxs-lookup"><span data-stu-id="821d9-113">To configure authentication and certificates on IIS virtual directories</span></span>

1.  <span data-ttu-id="821d9-114">Para completar correctamente lo siguiente, debe haber iniciado sesión en el equipo (servidor front-end o director) donde están instalados los servicios web y ser administradores locales.</span><span class="sxs-lookup"><span data-stu-id="821d9-114">To successfully complete the following, you must be logged on to the computer (Front End Server or Director) where the web services are installed and be a local administrator.</span></span> <span data-ttu-id="821d9-115">Debe tener permisos de **lectura** e **inscripción** en la entidad de certificación de la que va a solicitar certificados, si la entidad emisora de certificados es la entidad de certificación de su organización.</span><span class="sxs-lookup"><span data-stu-id="821d9-115">You must have the **read** and **enroll** permissions on the certification authority that you will be requesting certificates from, if the certification authority is your organization’s certification authority.</span></span> <span data-ttu-id="821d9-116">No necesita permisos para la entidad emisora de certificados si va a configurar y enviar una solicitud de certificado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="821d9-116">You do not need permissions to the certification authority if you will configure and send an offline certificate request.</span></span>

2.  <span data-ttu-id="821d9-117">Haga clic en **Inicio**, seleccione **todos los programas**, **herramientas administrativas** y, a continuación, haga clic en **Administrador de Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="821d9-117">Click **Start**, select **All Programs**, select **Administrative Tools**, and then click **Internet Information Services (IIS) Manager**.</span></span>

3.  <span data-ttu-id="821d9-118">En el **Administrador de Internet Information Services (IIS)**, seleccione **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="821d9-118">In **Internet Information Services (IIS) Manager**, select **ServerName**.</span></span> <span data-ttu-id="821d9-119">En la **vista características**, seleccione **certificados de servidor**, haga clic con el botón derecho y seleccione **abrir característica**.</span><span class="sxs-lookup"><span data-stu-id="821d9-119">In **Features View**, select **Server Certificates**, right-click and select **Open Feature**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="821d9-120">En la vista características de certificados de servidor, si hay certificados asignados al servidor, aparecerán aquí.</span><span class="sxs-lookup"><span data-stu-id="821d9-120">In the Server Certificates Feature View, if there are certificates assigned to the server, they will appear here.</span></span> <span data-ttu-id="821d9-121">Si hay un certificado que cumpla los requisitos para el sitio web externo en IIS, puede volver a usarlo.</span><span class="sxs-lookup"><span data-stu-id="821d9-121">If there is a certificate that matches the requirements for the External Web Site in IIS, you can re-use that certificate.</span></span> <span data-ttu-id="821d9-122">Para ver un certificado, haga clic con el botón derecho en el certificado y seleccione <STRONG>ver...</STRONG></span><span class="sxs-lookup"><span data-stu-id="821d9-122">To view a certificate, right-click the certificate and select <STRONG>View…</STRONG></span></span>

    
    </div>

4.  <span data-ttu-id="821d9-123">En el servidor front-end o director para el que va a solicitar el certificado, haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="821d9-123">On the Front End Server or Director that you are requesting the certificate for, click **Start**, select **All Programs**, select **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

5.  <span data-ttu-id="821d9-124">En el shell de administración de Lync Server, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="821d9-124">In the Lync Server Management Shell, type the following:</span></span>
    
        Get-CsCertificate
    
    <span data-ttu-id="821d9-125">El resultado es una lista de los certificados que se encuentran actualmente en el servidor del almacén de certificados personal del equipo.</span><span class="sxs-lookup"><span data-stu-id="821d9-125">The output is a list of the certificates that are currently on the server in the Computer Personal certificate store.</span></span> <span data-ttu-id="821d9-126">Tenga en cuenta que en el certificado combinado (es decir, cuando el valor predeterminado, servicios Web internos y servicios web externos estén usando el mismo certificado) verá que la propiedad use se rellenará con default, WebServicesInternal y WebServicesExternal.</span><span class="sxs-lookup"><span data-stu-id="821d9-126">Note that in the combined certificate (that is, where the default, web services internal and web services external are using the same certificate) you will see that the Use property will be populated with Default, WebServicesInternal and WebServicesExternal.</span></span> <span data-ttu-id="821d9-127">Además, la propiedad Thumbprint será la misma para cada uno de los tipos de uso.</span><span class="sxs-lookup"><span data-stu-id="821d9-127">Also, the Thumbprint property will be the same for each of the Use types.</span></span> <span data-ttu-id="821d9-128">En este ejemplo se muestra un ejemplo de salida de Get-CsCertificate:</span><span class="sxs-lookup"><span data-stu-id="821d9-128">An example output of Get-CsCertificate is shown in this example:</span></span>
    
    <span data-ttu-id="821d9-129">![Get-CsCertificate información sobre el estado actual de scert](images/Gg429702.664f6326-6cd5-48e2-8235-fc3950ea43b4(OCS.15).jpg "Get-CsCertificate información sobre el estado actual de scert")</span><span class="sxs-lookup"><span data-stu-id="821d9-129">![Get-CsCertificate info on current scert status](images/Gg429702.664f6326-6cd5-48e2-8235-fc3950ea43b4(OCS.15).jpg "Get-CsCertificate info on current scert status")</span></span>

6.  <span data-ttu-id="821d9-130">En el shell de administración de Lync Server, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="821d9-130">In the Lync Server Management Shell, type the following:</span></span>
    
        Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -CA <CA Server FQDN\CA Instance> -Verbose -DomainName "<FQDN entries to be added to the Subject Alternative Name>"
    
    <span data-ttu-id="821d9-131">Donde el comando completo tendría el siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="821d9-131">Where the full command would appear like following example:</span></span>
    
        Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -CA dc01.contoso.net\contoso-DC01-CA -Verbose -DomainName "LyncdiscoverInternal.Contoso.com,Lyncdiscover.Contoso.com"
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="821d9-132">De forma predeterminada, Request-CsCertificate rellenará el nombre del asunto con el nombre del servidor o grupo de servidores y rellenará las entradas en el nombre de asunto alternativo con el FQDN del servidor, el FQDN del grupo, FQDN de dirección URL simple y los FQDN de los servicios Web internos y externos.</span><span class="sxs-lookup"><span data-stu-id="821d9-132">By default, Request-CsCertificate will populate the subject name with the server or pool name and populate entries in the subject alternative name with the server FQDN, pool FQDN, Simple URL FQDNs, and internal and external web services FQDNs.</span></span> <span data-ttu-id="821d9-133">Para ello, hace referencia al documento de topología de su implementación.</span><span class="sxs-lookup"><span data-stu-id="821d9-133">It does this by referencing to the topology document in your deployment.</span></span> <span data-ttu-id="821d9-134">Si falta un valor y ha especificado el parámetro – verbose, se le notificará que los valores calculados y reales de los nombres alternativos son diferentes, pero no le informan los valores que faltan.</span><span class="sxs-lookup"><span data-stu-id="821d9-134">If there is a missing value and you have specified the –Verbose parameter, you will be notified that the computed and actual values for alternative names are different, but it does not inform you which values are missing.</span></span> <span data-ttu-id="821d9-135">Le proporciona el valor calculado completo al que hace referencia el cmdlet.</span><span class="sxs-lookup"><span data-stu-id="821d9-135">It does supply you with the entire computed value that the cmdlet references.</span></span> <span data-ttu-id="821d9-136">Use la cadena de nombres alternativos calculados en la salida para volver a solicitar un nuevo certificado que incluirá todos los valores.</span><span class="sxs-lookup"><span data-stu-id="821d9-136">Use the computed alternative names string in the output to re-request a new certificate that will include all values.</span></span>

    
    </div>
    
    <span data-ttu-id="821d9-137">![Resultado de la solicitud del certificado mediante la solicitud-CsCertifica](images/Gg429702.9e59a657-fa75-4454-8fd3-57c81e829f7b(OCS.15).jpg "Resultado de una solicitud de certificado con Request-CsCertifica")</span><span class="sxs-lookup"><span data-stu-id="821d9-137">![Output from cert request using Request-CsCertifica](images/Gg429702.9e59a657-fa75-4454-8fd3-57c81e829f7b(OCS.15).jpg "Output from cert request using Request-CsCertifica")</span></span>

7.  <span data-ttu-id="821d9-138">En el shell de administración de Lync Server, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="821d9-138">In the Lync Server Management Shell, type the following:</span></span>
    
        Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Thumbprint of certificate to use>
    
    <span data-ttu-id="821d9-139">Donde el comando completo tendría el siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="821d9-139">Where the full command would appear like following example:</span></span>
    
        Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint 466D9BB0E8B928B65AF38FA2D9F41E1B301ECE9D
    
    <span data-ttu-id="821d9-140">El resultado del cmdlet Set-CsCertificate mostrará que el mismo certificado (identificado por la huella digital del certificado) se asigna al uso predeterminado, WebServicesExternal y WebServicesInternal.</span><span class="sxs-lookup"><span data-stu-id="821d9-140">The output from the Set-CsCertificate cmdlet will show that the same certificate (identified by the thumbprint of the certificate) is assigned for the Default, WebServicesExternal and WebServicesInternal usage.</span></span>
    
    <span data-ttu-id="821d9-141">![Resultado de Set-CsCertificate en IIS WebExt](images/Gg429702.dd451c9d-7b49-4408-8071-c868cb1e678c(OCS.15).jpg "Resultado de Set-CsCertificate en IIS WebExt")</span><span class="sxs-lookup"><span data-stu-id="821d9-141">![Output from Set-CsCertificate on IIS WebExt](images/Gg429702.dd451c9d-7b49-4408-8071-c868cb1e678c(OCS.15).jpg "Output from Set-CsCertificate on IIS WebExt")</span></span>

</div>

<div>

## <a name="to-verify-or-configure-authentication-and-certificates-on-iis-virtual-directories"></a><span data-ttu-id="821d9-142">Para comprobar o configurar la autenticación y los certificados en los directorios virtuales de IIS</span><span class="sxs-lookup"><span data-stu-id="821d9-142">To verify or configure authentication and certificates on IIS virtual directories</span></span>

1.  <span data-ttu-id="821d9-143">Haga clic en **Inicio**, seleccione **todos los programas**, **herramientas administrativas** y, a continuación, haga clic en **Administrador de Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="821d9-143">Click **Start**, select **All Programs**, select **Administrative Tools**, and then click **Internet Information Services (IIS) Manager**.</span></span>

2.  <span data-ttu-id="821d9-144">En el **Administrador de Internet Information Services (IIS)**, expanda **ServerName** y, a continuación, expanda **sites**.</span><span class="sxs-lookup"><span data-stu-id="821d9-144">In **Internet Information Services (IIS) Manager**, expand **ServerName**, and then expand **Sites**.</span></span>

3.  <span data-ttu-id="821d9-145">Haga clic con el botón secundario en **sitio web externo de Lync Server** y, a continuación, haga clic en **Editar enlaces**</span><span class="sxs-lookup"><span data-stu-id="821d9-145">Right-click **Lync Server External Web Site**, and then click **Edit Bindings**</span></span>

4.  <span data-ttu-id="821d9-146">Compruebe que https está asociado con el puerto 4443 y, a continuación, haga clic en **https**.</span><span class="sxs-lookup"><span data-stu-id="821d9-146">Verify that https is associated with port 4443, and then click **https**.</span></span>

5.  <span data-ttu-id="821d9-147">Seleccione la entrada HTTPS, haga clic en **Editar** y, a continuación, compruebe que Lync Server WebServicesExternalCertificate está enlazado a este protocolo.</span><span class="sxs-lookup"><span data-stu-id="821d9-147">Select the HTTPS entry, click **Edit**, and then verify that Lync Server WebServicesExternalCertificate is bound to this protocol.</span></span> <span data-ttu-id="821d9-148">Compare la huella digital del cmdlet Set-CsCertificate para asegurarse de que el certificado esperado esté correctamente asociado con el enlace HTTPS.</span><span class="sxs-lookup"><span data-stu-id="821d9-148">Compare the thumbprint from the Set-CsCertificate cmdlet to ensure that the expected certificate is correctly associated with the HTTPS binding.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="821d9-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="821d9-149">See Also</span></span>


[<span data-ttu-id="821d9-150">Get-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="821d9-150">Get-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCertificate)  
[<span data-ttu-id="821d9-151">Set-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="821d9-151">Set-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  
  

<span data-ttu-id="821d9-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="821d9-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

