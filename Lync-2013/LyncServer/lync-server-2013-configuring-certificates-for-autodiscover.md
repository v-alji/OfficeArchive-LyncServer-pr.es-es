---
title: 'Lync Server 2013: configuración de certificados para la detección automática'
description: 'Lync Server 2013: configuración de certificados para la detección automática.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring certificates for Autodiscover
ms:assetid: 1842191d-df9a-41e0-9286-08c25f9b5dca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945617(v=OCS.15)
ms:contentKeyID: 51541453
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98ab9eca92685eef8bccc500dc4a91efa891dec6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397955"
---
# <a name="configuring-certificates-for-autodiscover-in-lync-server-2013"></a><span data-ttu-id="282c0-103">Configuración de certificados para la detección automática en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="282c0-103">Configuring certificates for Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="282c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="282c0-104">

<span> </span></span></span>

<span data-ttu-id="282c0-105">_**Última modificación del tema:** 2012-12-12_</span><span class="sxs-lookup"><span data-stu-id="282c0-105">_**Topic Last Modified:** 2012-12-12_</span></span>

<span data-ttu-id="282c0-106">Los certificados para el grupo de directores, el grupo front-end y el proxy inverso requieren entradas de nombre alternativo adicionales para admitir conexiones seguras con clientes de Lync.</span><span class="sxs-lookup"><span data-stu-id="282c0-106">The certificates for your Director pool, Front End pool, and reverse proxy require additional subject alternative name entries to support secure connections with Lync clients.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="282c0-107">Puede usar el cmdlet <STRONG>Get-CsCertificate</STRONG> para ver información sobre los certificados asignados actualmente.</span><span class="sxs-lookup"><span data-stu-id="282c0-107">You can use the <STRONG>Get-CsCertificate</STRONG> cmdlet to view information about the currently assigned certificates.</span></span> <span data-ttu-id="282c0-108">Sin embargo, la vista predeterminada trunca las propiedades del certificado y no muestra todos los valores de la propiedad SubjectAlternativeNames.</span><span class="sxs-lookup"><span data-stu-id="282c0-108">However, the default view truncates the properties of the certificate and does not display all values in the SubjectAlternativeNames property.</span></span> <span data-ttu-id="282c0-109">Puede usar los cmdlets <STRONG>Get-CsCertificate</STRONG> , <STRONG>request-</STRONG>CsCertificate y <STRONG>set-CsCertificate</STRONG> para ver cierta información y para solicitar y asignar certificados.</span><span class="sxs-lookup"><span data-stu-id="282c0-109">You can use the <STRONG>Get-CsCertificate</STRONG> , <STRONG>Request-</STRONG>CsCertificate and the <STRONG>Set-CsCertificate</STRONG> cmdlets to view some information and to request and assign certificates.</span></span> <span data-ttu-id="282c0-110">Sin embargo, no es el mejor método de uso si no está seguro de las propiedades de los nombres alternativos de asunto (SAN) en el certificado actual.</span><span class="sxs-lookup"><span data-stu-id="282c0-110">However, it’s not the best method to use if you are unsure of the properties of the subject alternative names (SAN) on the current certificate.</span></span> <span data-ttu-id="282c0-111">Para ver el certificado y todos los miembros de la propiedad, se recomienda usar el complemento certificados en <EM>Microsoft Management Console (MMC)</EM> o usar el Asistente para la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="282c0-111">To view the certificate and all property members, it is suggested to use the Certificates snap-in the <EM>Microsoft Management Console (MMC)</EM> or to use the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="282c0-112">En el Asistente para la implementación de Lync Server, puede usar el Asistente para la implementación de certificados para ver las propiedades del certificado.</span><span class="sxs-lookup"><span data-stu-id="282c0-112">In the Lync Server Deployment Wizard, you can use the Certificate Wizard to view the certificate properties.</span></span> <span data-ttu-id="282c0-113">Los procedimientos para ver, solicitar y asignar un certificado mediante el shell de administración de Lync Server y <EM>Microsoft Management Console (MMC)</EM> se detallan en los procedimientos siguientes.</span><span class="sxs-lookup"><span data-stu-id="282c0-113">The procedures for viewing, requesting and assigning a certificate using the Lync Server Management Shell and the <EM>Microsoft Management Console (MMC)</EM> are detailed in the following procedures.</span></span> <span data-ttu-id="282c0-114">Para usar el Asistente para la implementación de Lync Server, vea detalles aquí si ha implementado el grupo opcional de directores o directores: <A href="lync-server-2013-configure-certificates-for-the-director.md">configurar certificados para el Director en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="282c0-114">To use the Lync Server Deployment Wizard, see details here if you have deployed the optional Director or Director pool: <A href="lync-server-2013-configure-certificates-for-the-director.md">Configure certificates for the Director in Lync Server 2013</A>.</span></span> <span data-ttu-id="282c0-115">Para el servidor front-end o el grupo front-end, consulte los detalles aquí: <A href="lync-server-2013-configure-certificates-for-servers.md">configurar certificados para servidores en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="282c0-115">For the Front End Server or Front End pool, see the details here: <A href="lync-server-2013-configure-certificates-for-servers.md">Configure certificates for servers in Lync Server 2013</A>.</span></span><BR><span data-ttu-id="282c0-116">Los pasos iniciales de este procedimiento son pasos de preparación para orientarse en cuanto a la función de reproducción de los certificados actuales.</span><span class="sxs-lookup"><span data-stu-id="282c0-116">The initial steps in this procedure are preparation steps, to orient you as to what role the current certificates play.</span></span> <span data-ttu-id="282c0-117">De forma predeterminada, los certificados no tendrán un lyncdiscover. &lt; sipdomain &gt; o lyncdiscoverinternal. &lt; nombre de dominio interno &gt; , a menos que haya instalado previamente servicios de movilidad o haya preparado los certificados con antelación.</span><span class="sxs-lookup"><span data-stu-id="282c0-117">By default, the certificates will not have a lyncdiscover.&lt;sipdomain&gt; or lyncdiscoverinternal.&lt;internal domain name&gt; entry unless you have previously installed Mobility Services or have prepared your certificates in advance.</span></span> <span data-ttu-id="282c0-118">Este procedimiento usa el ejemplo de nombre de dominio SIP ' contoso.com ' y el nombre de dominio interno ' contoso.net ' de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="282c0-118">This procedure uses the example SIP domain name ‘contoso.com’ and the example internal domain name ‘contoso.net’.</span></span><BR><span data-ttu-id="282c0-119">La configuración de certificado predeterminada para Lync Server 2013 y Lync Server 2010 es usar un único certificado (denominado ' predeterminado ') con los propósitos predeterminados (para todos los propósitos excepto los servicios web), WebServicesExternal y WebServicesInternal.</span><span class="sxs-lookup"><span data-stu-id="282c0-119">The default certificate configuration for Lync Server 2013 and Lync Server 2010 is to use a single certificate (named ‘Default’) with the purposes Default (for all purposes except for the web services), WebServicesExternal and WebServicesInternal.</span></span> <span data-ttu-id="282c0-120">Una configuración opcional es usar certificados independientes para cada propósito.</span><span class="sxs-lookup"><span data-stu-id="282c0-120">An optional configuration is to use separate certificates for each purpose.</span></span> <span data-ttu-id="282c0-121">Los certificados se pueden administrar mediante el shell de administración de Lync Server y los cmdlets de Windows PowerShell, o bien mediante el Asistente para certificados del Asistente para la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="282c0-121">Certificates can be managed by using the Lync Server Management Shell and Windows PowerShell cmdlets, or by using the Certificate Wizard in the Lync Server Deployment Wizard.</span></span>



</div>

<div>

## <a name="to-update-certificates-with-new-subject-alternative-names-using-the-lync-server-management-shell"></a><span data-ttu-id="282c0-122">Para actualizar certificados con nombres alternativos de asunto nuevos mediante el shell de administración de Lync Server</span><span class="sxs-lookup"><span data-stu-id="282c0-122">To update certificates with new subject alternative names using the Lync Server Management Shell</span></span>

1.  <span data-ttu-id="282c0-123">Inicie sesión en el equipo con una cuenta que tenga derechos y permisos de administrador local.</span><span class="sxs-lookup"><span data-stu-id="282c0-123">Log on to the computer using an account that has local administrator rights and permissions.</span></span>

2.  <span data-ttu-id="282c0-124">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="282c0-124">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="282c0-125">Averigüe qué certificados se han asignado al servidor y para qué tipo de uso.</span><span class="sxs-lookup"><span data-stu-id="282c0-125">Find out what certificates have been assigned to the server and for which type of use.</span></span> <span data-ttu-id="282c0-126">Necesitas esta información en el siguiente paso para asignar el certificado actualizado.</span><span class="sxs-lookup"><span data-stu-id="282c0-126">You need this information in the next step to assign the updated certificate.</span></span> <span data-ttu-id="282c0-127">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="282c0-127">At the command line, type:</span></span>
    
        Get-CsCertificate

4.  <span data-ttu-id="282c0-128">Mire la salida del paso anterior para ver si se asigna un único certificado para varios usos o si se asigna un certificado diferente para cada uso.</span><span class="sxs-lookup"><span data-stu-id="282c0-128">Look in the output from the previous step to see whether a single certificate is assigned for multiple uses or whether a different certificate is assigned for each use.</span></span> <span data-ttu-id="282c0-129">Busque el parámetro use para saber cómo se usa un certificado.</span><span class="sxs-lookup"><span data-stu-id="282c0-129">Look in the Use parameter to find out how a certificate is used.</span></span> <span data-ttu-id="282c0-130">Compare el parámetro de la huella digital de los certificados mostrados para ver si el mismo certificado tiene varios usos.</span><span class="sxs-lookup"><span data-stu-id="282c0-130">Compare the Thumbprint parameter for the displayed certificates to see if the same certificate has multiple uses.</span></span>

5.  <span data-ttu-id="282c0-131">Actualice el certificado.</span><span class="sxs-lookup"><span data-stu-id="282c0-131">Update the certificate.</span></span> <span data-ttu-id="282c0-132">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="282c0-132">At the command line, type:</span></span>
    
        Set-CsCertificate -Type <type of certificate as displayed in the Use parameter> -Thumbprint <unique identifier>
    
    <span data-ttu-id="282c0-133">Por ejemplo, si el cmdlet **Get-CsCertificate** muestra un certificado con el uso predeterminado, otro con el uso de WebServicesInternal y otro con el uso de WebServicesExternal, y todos tenían el mismo valor de huella digital, en la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="282c0-133">For example, if the **Get-CsCertificate** cmdlet displayed a certificate with Use of Default, another with a Use of WebServicesInternal, and another with a Use of WebServicesExternal, and they all had the same Thumbprint value, at the command line, type:</span></span>
    
        Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
    
    <span data-ttu-id="282c0-134">**Importante:**</span><span class="sxs-lookup"><span data-stu-id="282c0-134">**Important:**</span></span>
    
    <span data-ttu-id="282c0-135">Si se asigna un certificado independiente para cada uso (el valor de la huella digital es diferente para cada certificado), es importante que no ejecute el cmdlet **set-CsCertificate** con varios tipos.</span><span class="sxs-lookup"><span data-stu-id="282c0-135">If a separate certificate is assigned for each use (the Thumbprint value is different for each certificate), it is important that you do not run the **Set-CsCertificate** cmdlet with multiple types.</span></span> <span data-ttu-id="282c0-136">En este caso, ejecute el cmdlet **set-CsCertificate** por separado para cada uso.</span><span class="sxs-lookup"><span data-stu-id="282c0-136">In this case, run the **Set-CsCertificate** cmdlet separately for each use.</span></span> <span data-ttu-id="282c0-137">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="282c0-137">For example:</span></span>
    
        Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>

6.  <span data-ttu-id="282c0-138">Para ver el certificado, haga clic en **Inicio**, haga clic en **Ejecutar...**.</span><span class="sxs-lookup"><span data-stu-id="282c0-138">To view the certificate, click **Start**, click **Run…**.</span></span> <span data-ttu-id="282c0-139">Escriba MMC para abrir la consola de administración de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="282c0-139">Type MMC to open the Microsoft Management Console.</span></span>

7.  <span data-ttu-id="282c0-140">En el menú MMC, seleccione **archivo**, seleccione **Agregar o quitar complemento...**, seleccione certificados.</span><span class="sxs-lookup"><span data-stu-id="282c0-140">From the MMC menu, select **File**, select **Add/Remove snap-in…**, select Certificates.</span></span> <span data-ttu-id="282c0-141">Haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="282c0-141">Click **Add**.</span></span> <span data-ttu-id="282c0-142">Cuando se le solicite, seleccione **cuenta de equipo** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="282c0-142">When prompted, select **Computer account**, then click **Next**.</span></span>

8.  <span data-ttu-id="282c0-143">Si el certificado se encuentra en este equipo, seleccione **equipo local**.</span><span class="sxs-lookup"><span data-stu-id="282c0-143">If the certificate is located on this computer, select **Local computer**.</span></span> <span data-ttu-id="282c0-144">Si el certificado se encuentra en otro equipo, seleccione **otro equipo**, escriba el nombre de dominio completo del equipo o haga clic en **examinar** en **Escriba el nombre de objeto para seleccionar**, escriba el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="282c0-144">If the certificate is located on another computer, select **Another computer**, type in the fully qualified domain name of the computer or click **Browse** In **Enter the object name to select**, type the name of the computer.</span></span> <span data-ttu-id="282c0-145">Haga clic en **Comprobar nombres**.</span><span class="sxs-lookup"><span data-stu-id="282c0-145">Click **Check Names**.</span></span> <span data-ttu-id="282c0-146">Cuando el nombre del equipo se resuelva, estará subrayado.</span><span class="sxs-lookup"><span data-stu-id="282c0-146">When the name of the computer is resolved, it will be underlined.</span></span> <span data-ttu-id="282c0-147">Haga clic en **Aceptar** y, después, en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="282c0-147">Click **OK**, then click **Finish**.</span></span> <span data-ttu-id="282c0-148">Haga clic en **Aceptar** para confirmar la selección y cerrar el cuadro de diálogo **Agregar o quitar complementos** .</span><span class="sxs-lookup"><span data-stu-id="282c0-148">Click **OK** to commit the selection and close the **Add or Remove Snap-ins** dialog.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="282c0-149">Si el certificado no se muestra en la consola, asegúrese de que no ha seleccionado el usuario o el servicio.</span><span class="sxs-lookup"><span data-stu-id="282c0-149">If the certificate does not show up in the console, ensure that you have not selected User or Service.</span></span> <span data-ttu-id="282c0-150">Debes seleccionar equipo o no podrás encontrar el certificado de probper.</span><span class="sxs-lookup"><span data-stu-id="282c0-150">You must select Computer, or you will not be able to locate the probper certificate.</span></span>

    
    </div>

9.  <span data-ttu-id="282c0-151">Para ver las propiedades del certificado, expanda **certificados**, expanda **personal** y seleccione **certificados**.</span><span class="sxs-lookup"><span data-stu-id="282c0-151">To view the properties of the certificate, expand **Certificates**, expand **Personal**, and select **Certificates**.</span></span> <span data-ttu-id="282c0-152">Seleccione el certificado que desea ver, haga clic con el botón derecho en el certificado y seleccione **abrir**.</span><span class="sxs-lookup"><span data-stu-id="282c0-152">Select the certificate to view, right-click on the certificate and select **Open**.</span></span>

10. <span data-ttu-id="282c0-153">En la vista del **certificado** , seleccione **detalles**.</span><span class="sxs-lookup"><span data-stu-id="282c0-153">In the **Certificate** view, select **Details**.</span></span> <span data-ttu-id="282c0-154">Desde aquí, puede seleccionar el nombre del sujeto del certificado seleccionando **asunto** y se muestran el nombre del asunto asignado y las propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="282c0-154">From here, you can select the certificate subject name by selecting **Subject** and the assigned subject name and associated properties are displayed.</span></span>

11. <span data-ttu-id="282c0-155">Para ver los nombres alternativos del asunto asignados, seleccione **nombre alternativo del asunto**.</span><span class="sxs-lookup"><span data-stu-id="282c0-155">To view the assigned subject alternative names, select **Subject Alternative Name**.</span></span> <span data-ttu-id="282c0-156">Se muestran todos los nombres alternativos del asunto asignados.</span><span class="sxs-lookup"><span data-stu-id="282c0-156">All assigned subject alternative names are displayed.</span></span> <span data-ttu-id="282c0-157">De forma predeterminada, los nombres alternativos de asunto que se encuentran en la propiedad son de tipo **DNS** .</span><span class="sxs-lookup"><span data-stu-id="282c0-157">The subject alternative names that are found in the property are of type **DNS Name** by default.</span></span> <span data-ttu-id="282c0-158">Debería ver los siguientes miembros (que deben ser nombres de dominio totalmente cualificados, como se representa en host DNS (si es IPv6 AAAA) los registros:</span><span class="sxs-lookup"><span data-stu-id="282c0-158">You should see the following members (all of which should be fully qualified domain names as represented in DNS host (A or, if IPv6 AAAA) records:</span></span>
    
      - <span data-ttu-id="282c0-159">Nombre de grupo para este grupo o el nombre de un servidor si no es un grupo</span><span class="sxs-lookup"><span data-stu-id="282c0-159">Pool name for this pool, or the single server name if this is not a pool</span></span>
    
      - <span data-ttu-id="282c0-160">Nombre del servidor al que está asignado el certificado</span><span class="sxs-lookup"><span data-stu-id="282c0-160">Server name that the certificate is assigned to</span></span>
    
      - <span data-ttu-id="282c0-161">Registros de dirección URL simples, que suelen reunirse y marcar</span><span class="sxs-lookup"><span data-stu-id="282c0-161">Simple URL records, typically meet and dialin</span></span>
    
      - <span data-ttu-id="282c0-162">Nombres externos de servicios web y internos de servicios web (por ejemplo, webpool01.contoso.net, webpool01.contoso.com), en función de las opciones seleccionadas en las selecciones del generador de topología y de los servicios web reemplazados.</span><span class="sxs-lookup"><span data-stu-id="282c0-162">Web services internal and Web services external names (for example, webpool01.contoso.net, webpool01.contoso.com), based on choices made in Topology Builder and over-ridden web services selections.</span></span>
    
      - <span data-ttu-id="282c0-163">Si ya está asignado, la lyncdiscover.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="282c0-163">If already assigned, the lyncdiscover.\<sipdomain\></span></span> <span data-ttu-id="282c0-164">y lyncdiscoverinternal.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="282c0-164">and lyncdiscoverinternal.\<sipdomain\></span></span> <span data-ttu-id="282c0-165">PTR.</span><span class="sxs-lookup"><span data-stu-id="282c0-165">records.</span></span>
    
    <span data-ttu-id="282c0-166">El último elemento es lo que más le interesa: si existe una lyncdiscover y lyncdiscoverinternal de SAN.</span><span class="sxs-lookup"><span data-stu-id="282c0-166">The last item is what you are most interested in – if there is a lyncdiscover and lyncdiscoverinternal SAN entry.</span></span>
    
    <span data-ttu-id="282c0-167">Una vez que tenga esta información, puede cerrar la vista certificado y MMC.</span><span class="sxs-lookup"><span data-stu-id="282c0-167">Once you have this information, you can close the certificate view and the MMC.</span></span>

12. <span data-ttu-id="282c0-168">Si es un servicio de detección automática, es decir, el lyncdiscover. \> nombre \> de dominio y lyncdiscoverinternal.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="282c0-168">If an Autodiscover Service, meaning the lyncdiscover.\>domain name\> and lyncdiscoverinternal.\<domain name\></span></span> <span data-ttu-id="282c0-169">(según se trata de un certificado interno o externo) no se encuentra el nombre alternativo de asunto y está usando un único certificado predeterminado para los tipos predeterminados, WebServicesInternal y WebServiceExternal, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="282c0-169">(based on if this is an external or internal certificate) subject alternative name is missing, and you are using a single Default certificate for the Default, WebServicesInternal and WebServiceExternal types, do the following:</span></span>
    
      - <span data-ttu-id="282c0-170">En el símbolo del sistema del shell de administración de Lync Server, escriba:</span><span class="sxs-lookup"><span data-stu-id="282c0-170">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="282c0-171">Si tiene muchos dominios SIP, no puede usar el nuevo parámetro AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="282c0-171">If you have many SIP domains, you cannot use the new AllSipDomain parameter.</span></span> <span data-ttu-id="282c0-172">En su lugar, debe usar el parámetro DomainName.</span><span class="sxs-lookup"><span data-stu-id="282c0-172">Instead, you must use DomainName parameter.</span></span> <span data-ttu-id="282c0-173">Al usar el parámetro DomainName, debe definir el FQDN para los registros lyncdiscoverinternal y lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="282c0-173">When you use the DomainName parameter, you must define the FQDN for the lyncdiscoverinternal and lyncdiscover records.</span></span> <span data-ttu-id="282c0-174">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="282c0-174">For example:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="282c0-175">Para asignar el certificado, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="282c0-175">To assign the certificate, type the following:</span></span>
        
            Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="282c0-176">Donde "huella digital" es la huella digital que se muestra para el certificado recién emitido.</span><span class="sxs-lookup"><span data-stu-id="282c0-176">Where “Thumbprint” is the thumbprint displayed for the newly issued certificate.</span></span>

13. <span data-ttu-id="282c0-177">En el caso de que falten nombres alternativos de sujeto de detección automática internos al usar certificados independientes para default, WebServicesInternal y WebServicesExternal, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="282c0-177">For a missing internal Autodiscover subject alternative names when using separate certificates for Default, WebServicesInternal, and WebServicesExternal, do the following:</span></span>
    
      - <span data-ttu-id="282c0-178">En el símbolo del sistema del shell de administración de Lync Server, escriba:</span><span class="sxs-lookup"><span data-stu-id="282c0-178">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="282c0-179">Si tiene muchos dominios SIP, no puede usar el nuevo parámetro AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="282c0-179">If you have many SIP domains, you cannot use the new AllSipDomain parameter.</span></span> <span data-ttu-id="282c0-180">En su lugar, debe usar el parámetro DomainName.</span><span class="sxs-lookup"><span data-stu-id="282c0-180">Instead, you must use DomainName parameter.</span></span> <span data-ttu-id="282c0-181">Al usar el parámetro DomainName, debe usar un prefijo adecuado para el FQDN del dominio SIP.</span><span class="sxs-lookup"><span data-stu-id="282c0-181">When you use the DomainName parameter, you must use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="282c0-182">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="282c0-182">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="282c0-183">Para un nombre alternativo externo de asunto de detección automática, en la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="282c0-183">For a missing external Autodiscover subject alternative name, at the command line, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="282c0-184">Si tiene muchos dominios SIP, no puede usar el nuevo parámetro AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="282c0-184">If you have many SIP domains, you cannot use the new AllSipDomain parameter.</span></span> <span data-ttu-id="282c0-185">En su lugar, debe usar el parámetro DomainName.</span><span class="sxs-lookup"><span data-stu-id="282c0-185">Instead, you must use DomainName parameter.</span></span> <span data-ttu-id="282c0-186">Al usar el parámetro DomainName, debe usar un prefijo adecuado para el FQDN del dominio SIP.</span><span class="sxs-lookup"><span data-stu-id="282c0-186">When you use the DomainName parameter, you must use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="282c0-187">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="282c0-187">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -DomainName "Lyncdiscover.contoso.com, Lyncdiscover.contoso.net" -verbose
    
      - <span data-ttu-id="282c0-188">Para asignar los tipos de certificado individuales, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="282c0-188">To assign the individual certificate types, type the following:</span></span>
        
            Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="282c0-189">Donde "huella digital" es la huella digital que se muestra para los certificados individuales recién emitidos.</span><span class="sxs-lookup"><span data-stu-id="282c0-189">Where “Thumbprint” is the thumbprint displayed for the newly issued individual certificates.</span></span>

<span data-ttu-id="282c0-190"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="282c0-190"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

