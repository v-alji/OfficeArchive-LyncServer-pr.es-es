---
title: 'Lync Server 2013: Modificación de certificados para movilidad'
description: 'Lync Server 2013: modificar certificados para la movilidad.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modifying certificates for mobility
ms:assetid: 4e9107af-20f4-4c2a-8c98-ca35b39a4e2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690015(v=OCS.15)
ms:contentKeyID: 48184120
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 099122b1773c3f15d8ae0034ee5fa404225cdfd2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445697"
---
# <a name="modifying-certificates-for-mobility-in-lync-server-2013"></a><span data-ttu-id="9a990-103">Modificación de certificados para movilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a990-103">Modifying certificates for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a990-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a990-104">

<span> </span></span></span>

<span data-ttu-id="9a990-105">_**Última modificación del tema:** 2014-06-20_</span><span class="sxs-lookup"><span data-stu-id="9a990-105">_**Topic Last Modified:** 2014-06-20_</span></span>

<span data-ttu-id="9a990-106">Para admitir conexiones seguras entre su entorno de Lync y sus clientes móviles, los certificados de nivel de socket seguro (SSL) para el grupo de directores, el grupo front-end y el proxy inverso deben actualizarse con algunas entradas de nombre alternativo de asunto (SAN) adicionales.</span><span class="sxs-lookup"><span data-stu-id="9a990-106">To support secure connections between your Lync environment and your mobile clients, the Secure Socket Layer (SSL) certificates for your Director pool, Front End pool, and reverse proxy are going to need to be updated with some additional subject alternative name (SAN) entries.</span></span> <span data-ttu-id="9a990-107">Si necesita consultar más detalles sobre los requisitos de certificados para la movilidad, consulte la sección requisitos técnicos de la [movilidad en Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md), pero básicamente tendrá que obtener nuevos certificados de la entidad emisora de certificados con las entradas de San adicionales incluidas y, después, agregar esos certificados siguiendo los pasos de este artículo.</span><span class="sxs-lookup"><span data-stu-id="9a990-107">If you need to check out more details about the certificate requirements for mobility, see the Certificate Requirements section in [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md), but basically you’ll need to get new certificates from the Certificate Authority with the additional SAN entries included, and then add those certificates using this article’s steps.</span></span>

<span data-ttu-id="9a990-108">Por supuesto que antes de empezar, suele ser una buena idea saber qué nombres alternativos de sujeto ya tienen los certificados.</span><span class="sxs-lookup"><span data-stu-id="9a990-108">Of course before you begin, it’s usually a good idea to know what subject alternative names your certificates already have.</span></span> <span data-ttu-id="9a990-109">Si no está seguro de lo que ya está configurado, hay muchas formas de averiguarlo. Si bien la opción está allí para ejecutar **Get-CsCertificate** y otros comandos de PowerShell para ver esta información, (que trataremos a continuación) de forma predeterminada, se truncarán los datos, por lo que es posible que no vea todas las propiedades que necesita.</span><span class="sxs-lookup"><span data-stu-id="9a990-109">If you’re not sure what’s already been configured, there are a lot of ways to find out. While the option’s there to run the **Get-CsCertificate** and other PowerShell commands to view this information, (which we walk through below) by default that data will be truncated, so you may not get to see all the properties you need.</span></span> <span data-ttu-id="9a990-110">Para obtener un buen aspecto del certificado y de todas sus propiedades, puede ir a Microsoft Management Console (MMC) y cargar el complemento certificados (que también trataremos a continuación), o bien, puede simplemente comprobar el Asistente para la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9a990-110">In order to get a good look at the certificate and all its properties, you can go to the Microsoft Management Console (MMC) and load the Certificates snap-in (which we also walk through below), or you can just check in the Lync Server Deployment Wizard.</span></span>

<span data-ttu-id="9a990-111">Como se mencionó anteriormente, los pasos siguientes le guiarán en la actualización de certificados mediante el shell de administración de Lync Server y MMC.</span><span class="sxs-lookup"><span data-stu-id="9a990-111">As noted above, the following steps will walk you through updating the certificates using the Lync Server Management Shell and the MMC.</span></span> <span data-ttu-id="9a990-112">Si está interesado en usar el Asistente para certificados en el Asistente para la implementación de Lync Server, en su lugar, puede comprobar la [configuración de certificados para el director de Lync server 2013](lync-server-2013-configure-certificates-for-the-director.md) para el grupo de directores o directores, si ha configurado uno (es posible que no lo tenga).</span><span class="sxs-lookup"><span data-stu-id="9a990-112">If you’re interested in using the Certificate Wizard in the Lync Server Deployment Wizard for this instead, you can check [Configure certificates for the Director in Lync Server 2013](lync-server-2013-configure-certificates-for-the-director.md) out for the Director or Director pool, if you configured one (you may not have).</span></span> <span data-ttu-id="9a990-113">Para el servidor front-end o el grupo front-end, querrá ver [configurar certificados para servidores en Lync Server 2013](lync-server-2013-configure-certificates-for-servers.md).</span><span class="sxs-lookup"><span data-stu-id="9a990-113">For the Front End Server or Front End pool, you’ll want to see [Configure certificates for servers in Lync Server 2013](lync-server-2013-configure-certificates-for-servers.md).</span></span>

<span data-ttu-id="9a990-114">Un último aspecto que se debe tener en cuenta es que puede tener un único certificado predeterminado en el entorno de Lync Server 2013, o puede que tenga certificados separados de forma predeterminada (que es todo menos los servicios web), WebServicesExternal y WebServicesInternal.</span><span class="sxs-lookup"><span data-stu-id="9a990-114">One last thing to keep in mind is that you may have a single Default certificate in your Lync Server 2013 environment, or you may have separate certificates for Default (which is everything but the web services), WebServicesExternal and WebServicesInternal.</span></span> <span data-ttu-id="9a990-115">Independientemente de la configuración, estos pasos le ayudarán.</span><span class="sxs-lookup"><span data-stu-id="9a990-115">Whatever your configuration, these steps should help you out.</span></span>

<div>

## <a name="to-update-certificates-with-new-subject-alternative-names-using-the-lync-server-management-shell"></a><span data-ttu-id="9a990-116">Para actualizar certificados con nombres alternativos de asunto nuevos mediante el shell de administración de Lync Server</span><span class="sxs-lookup"><span data-stu-id="9a990-116">To update certificates with new subject alternative names using the Lync Server Management Shell</span></span>

1.  <span data-ttu-id="9a990-117">Debe iniciar sesión en su servidor de Lync Server 2013 con una cuenta que tenga derechos y permisos de administrador local.</span><span class="sxs-lookup"><span data-stu-id="9a990-117">You need to log on to your Lync Server 2013 server using an account that has local administrator rights and permissions.</span></span> <span data-ttu-id="9a990-118">Además, si está ejecutando el CsCertificate de **solicitud** de PowerShell en los pasos 12 y posteriores, la cuenta debe tener derechos para la entidad emisora de certificados especificada (CA).</span><span class="sxs-lookup"><span data-stu-id="9a990-118">Additionally, if you’re running the PowerShell **Request-CsCertificate** in Steps 12 and beyond, the account needs to have rights to the specified Certificate Authority (CA).</span></span>

2.  <span data-ttu-id="9a990-119">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="9a990-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="9a990-120">Antes de poder asignar un certificado actualizado, tendrá que averiguar qué certificados se han asignado al servidor y para qué tipo de uso.</span><span class="sxs-lookup"><span data-stu-id="9a990-120">Before you can assign an updated certificate, you’ll need to find out what certificates have been assigned to the server and for which type of use.</span></span> <span data-ttu-id="9a990-121">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="9a990-121">At the command line, type:</span></span>
    
        Get-CsCertificate

4.  <span data-ttu-id="9a990-122">Revise la salida del paso anterior para ver si se ha asignado un certificado para varios usos, o si se ha asignado un certificado diferente para cada uso.</span><span class="sxs-lookup"><span data-stu-id="9a990-122">Review the output from the previous step to see whether a single certificate has been assigned for multiple uses, or whether a different certificate is assigned for each use.</span></span> <span data-ttu-id="9a990-123">Busque el parámetro use para saber cómo se usa un certificado.</span><span class="sxs-lookup"><span data-stu-id="9a990-123">Look in the Use parameter to find out how a certificate’s being used.</span></span> <span data-ttu-id="9a990-124">Compare el parámetro de la huella digital de los certificados mostrados para ver si el mismo certificado tiene varios usos.</span><span class="sxs-lookup"><span data-stu-id="9a990-124">Compare the Thumbprint parameter for the displayed certificates to see if the same certificate has multiple uses.</span></span> <span data-ttu-id="9a990-125">Mantén el ojo del parámetro de la huella digital.</span><span class="sxs-lookup"><span data-stu-id="9a990-125">Keep your eye on the Thumbprint parameter.</span></span>

5.  <span data-ttu-id="9a990-126">Actualice el certificado.</span><span class="sxs-lookup"><span data-stu-id="9a990-126">Update the certificate.</span></span> <span data-ttu-id="9a990-127">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="9a990-127">At the command line, type:</span></span>
    
        Set-CsCertificate -Type <type of certificate as displayed in the Use parameter> -Thumbprint <unique identifier>
    
    <span data-ttu-id="9a990-128">Por ejemplo, si el cmdlet **Get-CsCertificate** muestra un certificado con el uso predeterminado, otro con el uso de WebServicesInternal y otro con el uso de WebServicesExternal, y todos tenían el mismo valor de huella digital, en la línea de comandos, debe escribir:</span><span class="sxs-lookup"><span data-stu-id="9a990-128">For example, if the **Get-CsCertificate** cmdlet displayed a certificate with Use of Default, another with a Use of WebServicesInternal, and another with a Use of WebServicesExternal, and they all had the same Thumbprint value, at the command line, you should type:</span></span>
    
        Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
    
    <span data-ttu-id="9a990-129">**Importante:**</span><span class="sxs-lookup"><span data-stu-id="9a990-129">**Important:**</span></span>
    
    <span data-ttu-id="9a990-130">Si se asigna un certificado independiente para cada uso (por lo que el valor de la huella digital que ha activado anteriormente es diferente para cada certificado), es fundamental que **no** ejecute el cmdlet **set-CsCertificate** con varios tipos, como en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="9a990-130">If a separate certificate is assigned for each use (so the Thumbprint value you checked above is different for each certificate), it’s vital that you **don’t** run the **Set-CsCertificate** cmdlet with multiple types, as in the example above.</span></span> <span data-ttu-id="9a990-131">En este caso, ejecute el cmdlet **set-CsCertificate** por separado para cada uso.</span><span class="sxs-lookup"><span data-stu-id="9a990-131">In this case, run the **Set-CsCertificate** cmdlet separately for each use.</span></span> <span data-ttu-id="9a990-132">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9a990-132">For example:</span></span>
    
        Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>

6.  <span data-ttu-id="9a990-133">Para ver el certificado (o certificados), haga clic en **Inicio**, haga clic en **Ejecutar...**.</span><span class="sxs-lookup"><span data-stu-id="9a990-133">To view the certificate (or certificates), click **Start**, click **Run…**.</span></span> <span data-ttu-id="9a990-134">Escriba MMC para abrir la consola de administración de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9a990-134">Type MMC to open the Microsoft Management Console.</span></span>

7.  <span data-ttu-id="9a990-135">En el menú MMC, seleccione **archivo**, seleccione **Agregar o quitar complemento...**, seleccione certificados.</span><span class="sxs-lookup"><span data-stu-id="9a990-135">From the MMC menu, select **File**, select **Add/Remove snap-in…**, select Certificates.</span></span> <span data-ttu-id="9a990-136">Haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="9a990-136">Click **Add**.</span></span> <span data-ttu-id="9a990-137">Cuando se le solicite, seleccione **cuenta de equipo** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9a990-137">When prompted, select **Computer account**, then click **Next**.</span></span>

8.  <span data-ttu-id="9a990-138">Si este es el servidor donde se encuentra el certificado, seleccione **equipo local**.</span><span class="sxs-lookup"><span data-stu-id="9a990-138">If this is the server where the certificate’s located, select **Local computer**.</span></span> <span data-ttu-id="9a990-139">Si el certificado se encuentra en otro equipo, debe seleccionar **otro equipo** y, a continuación, puede escribir el nombre de dominio completo del equipo o hacer clic en **examinar** , escriba el nombre de **objeto que desea seleccionar** y escriba el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="9a990-139">If the certificate’s located on another computer, you should select **Another computer**, and then you can either type in the fully qualified domain name of the computer, or click **Browse** in **Enter the object name to select**, and type the name of the computer.</span></span> <span data-ttu-id="9a990-140">Haga clic en **Comprobar nombres**.</span><span class="sxs-lookup"><span data-stu-id="9a990-140">Click **Check Names**.</span></span> <span data-ttu-id="9a990-141">Cuando se resuelva el nombre del equipo, aparecerá subrayado.</span><span class="sxs-lookup"><span data-stu-id="9a990-141">When the name of the computer resolves, it’ll be underlined.</span></span> <span data-ttu-id="9a990-142">Haga clic en **Aceptar** y, después, en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="9a990-142">Click **OK**, then click **Finish**.</span></span> <span data-ttu-id="9a990-143">Haga clic en **Aceptar** para confirmar la selección y cerrar el cuadro de diálogo **Agregar o quitar complementos** .</span><span class="sxs-lookup"><span data-stu-id="9a990-143">Click **OK** to commit the selection and close the **Add or Remove Snap-ins** dialog.</span></span>

9.  <span data-ttu-id="9a990-144">Para ver las propiedades del certificado, expanda **certificados**, expanda **personal** y seleccione **certificados**.</span><span class="sxs-lookup"><span data-stu-id="9a990-144">To view the properties of the certificate, expand **Certificates**, expand **Personal**, and select **Certificates**.</span></span> <span data-ttu-id="9a990-145">Seleccione el certificado que desea ver, haga clic con el botón derecho en el certificado y seleccione **abrir**.</span><span class="sxs-lookup"><span data-stu-id="9a990-145">Select the certificate to view, right-click on the certificate and select **Open**.</span></span>

10. <span data-ttu-id="9a990-146">En la vista del **certificado** , seleccione **detalles**.</span><span class="sxs-lookup"><span data-stu-id="9a990-146">In the **Certificate** view, select **Details**.</span></span> <span data-ttu-id="9a990-147">Desde aquí, puede seleccionar el nombre del sujeto del certificado seleccionando **asunto** y se muestran el nombre del asunto asignado y las propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="9a990-147">From here, you can select the certificate subject name by selecting **Subject** and the assigned subject name and associated properties are displayed.</span></span>

11. <span data-ttu-id="9a990-148">Para ver los nombres alternativos del asunto asignados, seleccione **nombre alternativo del asunto**.</span><span class="sxs-lookup"><span data-stu-id="9a990-148">To view the assigned subject alternative names, select **Subject Alternative Name**.</span></span> <span data-ttu-id="9a990-149">Aquí se muestran todos los nombres alternativos del asunto asignados.</span><span class="sxs-lookup"><span data-stu-id="9a990-149">All assigned subject alternative names are displayed here.</span></span> <span data-ttu-id="9a990-150">Los nombres alternativos de asunto que se encuentran aquí son de tipo **DNS** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9a990-150">The subject alternative names found here are of type **DNS Name** by default.</span></span> <span data-ttu-id="9a990-151">Debería ver los siguientes miembros (que deben ser nombres de dominio totalmente cualificados, como se representa en host DNS (si es IPv6 AAAA) los registros:</span><span class="sxs-lookup"><span data-stu-id="9a990-151">You should see the following members (all of which should be fully qualified domain names as represented in DNS host (A or, if IPv6 AAAA) records:</span></span>
    
      - <span data-ttu-id="9a990-152">Nombre de grupo para este grupo o el nombre de servidor único si no se trata de un grupo</span><span class="sxs-lookup"><span data-stu-id="9a990-152">Pool name for this pool, or the single server name if this isn’t a pool</span></span>
    
      - <span data-ttu-id="9a990-153">Nombre del servidor al que está asignado el certificado</span><span class="sxs-lookup"><span data-stu-id="9a990-153">Server name that the certificate is assigned to</span></span>
    
      - <span data-ttu-id="9a990-154">Registros de dirección URL simples, que suelen reunirse y marcar</span><span class="sxs-lookup"><span data-stu-id="9a990-154">Simple URL records, typically meet and dialin</span></span>
    
      - <span data-ttu-id="9a990-155">Nombres externos de servicios web y internos de servicios web (por ejemplo, webpool01.contoso.net, webpool01.contoso.com), en función de las opciones seleccionadas en las selecciones del generador de topología y de los servicios web reemplazados.</span><span class="sxs-lookup"><span data-stu-id="9a990-155">Web services internal and Web services external names (for example, webpool01.contoso.net, webpool01.contoso.com), based on choices made in Topology Builder and over-ridden web services selections.</span></span>
    
      - <span data-ttu-id="9a990-156">Si ya está asignado, la lyncdiscover.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="9a990-156">If already assigned, the lyncdiscover.\<sipdomain\></span></span> <span data-ttu-id="9a990-157">y lyncdiscoverinternal.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="9a990-157">and lyncdiscoverinternal.\<sipdomain\></span></span> <span data-ttu-id="9a990-158">PTR.</span><span class="sxs-lookup"><span data-stu-id="9a990-158">records.</span></span>
    
    <span data-ttu-id="9a990-159">El último elemento es lo que te interesa más interesado: si hay una lyncdiscover y lyncdiscoverinternal de SAN.</span><span class="sxs-lookup"><span data-stu-id="9a990-159">The last item is what you’re most interested in – if there’s a lyncdiscover and lyncdiscoverinternal SAN entry.</span></span>
    
    <span data-ttu-id="9a990-160">Repita estos pasos si tiene varios certificados para comprobar.</span><span class="sxs-lookup"><span data-stu-id="9a990-160">Repeat these steps if you have multiple certificates to check.</span></span> <span data-ttu-id="9a990-161">Una vez que tenga esta información, puede cerrar la vista certificado y MMC.</span><span class="sxs-lookup"><span data-stu-id="9a990-161">Once you have this information, you can close the certificate view and the MMC.</span></span>

12. <span data-ttu-id="9a990-162">Si falta un nombre alternativo de asunto del servicio de detección automática y está usando un único certificado predeterminado para los tipos predeterminados, WebServicesInternal y WebServiceExternal, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9a990-162">If an Autodiscover Service subject alternative name is missing, and you are using a single Default certificate for the Default, WebServicesInternal and WebServiceExternal types, do the following:</span></span>
    
      - <span data-ttu-id="9a990-163">En el símbolo del sistema del shell de administración de Lync Server, escriba:</span><span class="sxs-lookup"><span data-stu-id="9a990-163">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="9a990-164">Si tiene muchos dominios SIP, no puede usar el nuevo parámetro AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="9a990-164">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="9a990-165">En su lugar, debe usar el parámetro DomainName.</span><span class="sxs-lookup"><span data-stu-id="9a990-165">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="9a990-166">Cuando use el parámetro DomainName, tendrá que definir el FQDN para los registros lyncdiscoverinternal y lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="9a990-166">When you use the DomainName parameter, you’ve got to define the FQDN for the lyncdiscoverinternal and lyncdiscover records.</span></span> <span data-ttu-id="9a990-167">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9a990-167">For example:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="9a990-168">Para asignar el certificado, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9a990-168">To assign the certificate, type the following:</span></span>
        
            Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="9a990-169">Donde "huella digital" es la huella digital que se muestra para el certificado recién emitido.</span><span class="sxs-lookup"><span data-stu-id="9a990-169">Where “Thumbprint” is the thumbprint displayed for the newly issued certificate.</span></span>

13. <span data-ttu-id="9a990-170">Para una SAN interna de detección automática que falta al usar certificados independientes para default, WebServicesInternal y WebServicesExternal, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9a990-170">For a missing internal Autodiscover SAN when using separate certificates for Default, WebServicesInternal, and WebServicesExternal, do the following:</span></span>
    
      - <span data-ttu-id="9a990-171">En el símbolo del sistema del shell de administración de Lync Server, escriba:</span><span class="sxs-lookup"><span data-stu-id="9a990-171">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="9a990-172">Si tiene muchos dominios SIP, no puede usar el nuevo parámetro AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="9a990-172">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="9a990-173">En su lugar, debe usar el parámetro DomainName.</span><span class="sxs-lookup"><span data-stu-id="9a990-173">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="9a990-174">Cuando use el parámetro DomainName, tendrá que usar un prefijo adecuado para el FQDN del dominio SIP.</span><span class="sxs-lookup"><span data-stu-id="9a990-174">When you use the DomainName parameter, you’ve got to use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="9a990-175">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9a990-175">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="9a990-176">Para un nombre alternativo externo de asunto de detección automática, en la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="9a990-176">For a missing external Autodiscover subject alternative name, at the command line, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="9a990-177">Si tiene muchos dominios SIP, no puede usar el nuevo parámetro AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="9a990-177">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="9a990-178">En su lugar, debe usar el parámetro DomainName.</span><span class="sxs-lookup"><span data-stu-id="9a990-178">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="9a990-179">Cuando use el parámetro DomainName, tendrá que usar un prefijo adecuado para el FQDN del dominio SIP.</span><span class="sxs-lookup"><span data-stu-id="9a990-179">When you use the DomainName parameter, you’ve got to use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="9a990-180">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9a990-180">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -DomainName "Lyncdiscover.contoso.com, Lyncdiscover.contoso.net" -verbose
    
      - <span data-ttu-id="9a990-181">Para asignar los tipos de certificado individuales, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9a990-181">To assign the individual certificate types, type the following:</span></span>
        
            Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="9a990-182">Donde "huella digital" es la huella digital que se muestra para los certificados individuales recién emitidos.</span><span class="sxs-lookup"><span data-stu-id="9a990-182">Where “Thumbprint” is the thumbprint displayed for the newly issued individual certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9a990-183">Solo para tener en cuenta, los pasos 12 y 13 solo se deben ejecutar si la cuenta que los ejecuta tiene acceso a la entidad emisora de certificados con los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="9a990-183">Just to note, Steps 12 and 13 should be run only if the account running them has access to the Certificate Authority with appropriate permissions.</span></span> <span data-ttu-id="9a990-184">Si no puede iniciar sesión con una cuenta que tiene esos permisos, o si usa una entidad emisora de certificados pública o remota para sus certificados, necesitará solicitarlos mediante el Asistente para la implementación de Lync Server, que se ha tocado en la parte superior del artículo.</span><span class="sxs-lookup"><span data-stu-id="9a990-184">If you are unable to log in with an account that’s got those permissions, or if you’re using a public or remote Certificate Authority for your certificates, you would need to request them through the Lync Server Deployment Wizard, which was touched on at the top of the article.</span></span>

    
    <span data-ttu-id="9a990-185"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a990-185"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

