---
title: 'Lync Server 2013: Definir la topología perimetral'
description: 'Lync Server 2013: defina su topología perimetral.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define your edge topology
ms:assetid: 787b23f1-8fa0-4c37-abf2-c516c5dd66f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398591(v=OCS.15)
ms:contentKeyID: 48184562
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd4aa16ca23d24f0edd92189216030ef926fc841
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431039"
---
# <a name="define-your-edge-topology-in-lync-server-2013"></a><span data-ttu-id="9ee90-103">Definir la topología perimetral en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9ee90-103">Define your edge topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9ee90-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9ee90-104">

<span> </span></span></span>

<span data-ttu-id="9ee90-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="9ee90-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="9ee90-106">Debe usar topología Builder para crear su topología y debe configurar al menos un grupo de servidores front-end interno o un servidor Standard Edition para poder implementar el servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-106">You must use Topology Builder to build your topology and you must set up at least one internal Front End pool or Standard Edition server before you can deploy your Edge Server.</span></span> <span data-ttu-id="9ee90-107">Use el siguiente procedimiento para definir la topología de borde para un único servidor perimetral y, a continuación, use los procedimientos de [publicar su topología en Lync Server 2013](lync-server-2013-publish-your-topology.md) y [exportar su topología de Lync Server 2013 y copiarla en medios externos para la instalación perimetral](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) para publicar la topología y ponerla a disposición de su servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-107">Use the following procedure to define the edge topology for a single Edge Server, and then use the procedures in [Publish your topology in Lync Server 2013](lync-server-2013-publish-your-topology.md) and [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) to publish the topology and make it available to your Edge Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9ee90-p102">La interfaz perimetral interna y la interfaz perimetral externa necesitan usar el mismo tipo de equilibrio de carga. No puede usar equilibrio de carga de DNS en una interfaz perimetral y equilibrio de carga de hardware en la otra interfaz perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-p102">The internal Edge interface and external Edge interface must use the same type of load balancing. You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span>



</div>

<span data-ttu-id="9ee90-110">Para publicar, habilitar o deshabilitar correctamente una topología al agregar o quitar un rol de servidor, debe haber iniciado sesión como un usuario que sea miembro de los grupos administradores de dominio y RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="9ee90-110">To successfully publish, enable, or disable a topology when adding or removing a server role, you must be logged in as a user who is a member of the RTCUniversalServerAdmins and Domain Admins groups.</span></span> <span data-ttu-id="9ee90-111">También puede conceder derechos y permisos de administrador necesarios para agregar roles de servidor a una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="9ee90-111">You can also grant the administrator rights and permissions required for adding server roles to a user account.</span></span> <span data-ttu-id="9ee90-112">Para obtener más información, consulte [permisos de configuración de delegación en Lync Server 2013](lync-server-2013-delegate-setup-permissions.md) en la documentación de implementación de servidor Standard Edition o Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="9ee90-112">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md) in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="9ee90-113">Para otros cambios de configuración, solo es necesario pertenecer al grupo RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="9ee90-113">For other configuration changes, only membership in the RTCUniversalServerAdmins group is required.</span></span>

<span data-ttu-id="9ee90-114">Si definió la topología de borde cuando definió y publicó su topología interna, y no se necesitan cambios en la topología perimetral que definió anteriormente, no es necesario que la defina y la publique de nuevo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-114">If you defined your edge topology when you defined and published your internal topology, and no changes are required to the edge topology that you previously defined, you do not need to do define it and publish it again.</span></span> <span data-ttu-id="9ee90-115">Use el siguiente procedimiento solo si necesita realizar cambios en la topología de borde.</span><span class="sxs-lookup"><span data-stu-id="9ee90-115">Use the following procedure only if you need to make changes to your edge topology.</span></span> <span data-ttu-id="9ee90-116">Debe hacer que la topología previamente definida y publicada esté disponible para los servidores perimetrales, que puede hacer con el procedimiento de [exportar su topología de Lync Server 2013 y copiarla en medios externos para la instalación perimetral](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span><span class="sxs-lookup"><span data-stu-id="9ee90-116">You must make the previously defined and published topology available to your Edge Servers, which you do by using the procedure in [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="9ee90-117">No se puede ejecutar el generador de topologías desde un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-117">You cannot run Topology Builder from an Edge Server.</span></span> <span data-ttu-id="9ee90-118">Debe ejecutarla desde el servidor front-end o los servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="9ee90-118">You must run it from your Front End Server or Standard Edition servers.</span></span>



</div>

<span data-ttu-id="9ee90-119">El proceso para definir la topología del servidor perimetral se realiza en el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="9ee90-119">The process to define your Edge Server topology is done in Topology Builder.</span></span> <span data-ttu-id="9ee90-120">A continuación, se muestran los tres tipos principales de topologías de servidores perimetrales que se planean y se configuran:</span><span class="sxs-lookup"><span data-stu-id="9ee90-120">The three primary types of Edge Server topologies that you plan and configure are listed below:</span></span>

  - <span data-ttu-id="9ee90-121">Para definir la topología de un único servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="9ee90-121">To define the Topology for a Single Edge Server</span></span>

  - <span data-ttu-id="9ee90-122">Para definir la topología de un grupo de servidores perimetrales de carga equilibrada</span><span class="sxs-lookup"><span data-stu-id="9ee90-122">To define the Topology for a Load Balanced Edge Server Pool</span></span>

  - <span data-ttu-id="9ee90-123">Para definir la topología de un grupo de servidores perimetrales con equilibrio de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="9ee90-123">To define the Topology for a Hardware Load Balanced Edge Pool</span></span>

<div>

## <a name="to-define-the-topology-for-a-single-edge-server"></a><span data-ttu-id="9ee90-124">Para definir la topología de un único servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="9ee90-124">To define the topology for a single Edge Server</span></span>

1.  <span data-ttu-id="9ee90-125">Iniciar generador de topología: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **generador de topología de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-125">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="9ee90-126">En el árbol de consola, expanda el sitio en el que desea implementar un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-126">In the console tree, expand the site in which you want to deploy an Edge Server.</span></span>

3.  <span data-ttu-id="9ee90-127">Haga clic con el botón secundario en **agrupaciones perimetrales** y luego haga clic en **nuevo borde**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-127">Right-click **Edge pools**, and then click **New Edge Pool**.</span></span>

4.  <span data-ttu-id="9ee90-128">En **definir el nuevo grupo de límites**, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-128">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="9ee90-129">En **definir el FQDN del grupo perimetral**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-129">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-130">En **FQDN del grupo**, escriba el nombre de dominio completo (FQDN) de la interfaz interna para el servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-130">In **Pool FQDN**, type the fully qualified domain name (FQDN) of the internal interface for the Edge Server.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="9ee90-131">El nombre que especifique debe ser idéntico al nombre de equipo configurado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="9ee90-131">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="9ee90-132">De forma predeterminada, el nombre de equipo de un equipo que no está unido a un dominio es un nombre corto, no un FQDN.</span><span class="sxs-lookup"><span data-stu-id="9ee90-132">By default the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="9ee90-133">El Generador de topologías usa nombres de dominio completos, no nombres cortos.</span><span class="sxs-lookup"><span data-stu-id="9ee90-133">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="9ee90-134">Por lo tanto, debe configurar un sufijo DNS en el nombre del equipo para implementarse como servidor perimetral que no está unido a un dominio.</span><span class="sxs-lookup"><span data-stu-id="9ee90-134">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="9ee90-135">Utilice únicamente caracteres estándar (incluyendo A–Z, a–z, 0–9 y guiones) a la hora de asignar FQDN de sus Lync Server, servidores perimetrales y grupos.</span><span class="sxs-lookup"><span data-stu-id="9ee90-135">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="9ee90-136">No utilice caracteres Unicode ni de subrayado.</span><span class="sxs-lookup"><span data-stu-id="9ee90-136">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="9ee90-137">A menudo, los caracteres no estándar de un FQDN no son compatibles con las entidades de certificación públicas y DNS externas (cuando se debe asignar el FQDN al SN en el certificado).</span><span class="sxs-lookup"><span data-stu-id="9ee90-137">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="9ee90-138">Para más información sobre cómo agregar un sufijo DNS al nombre de un equipo, consulte <A href="lync-server-2013-configure-dns-for-edge-support.md">configurar DNS para la compatibilidad con Edge en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9ee90-138">For details about adding a DNS suffix to a computer name, see <A href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</A>.</span></span>

        
        </div>
    
      - <span data-ttu-id="9ee90-139">Haga clic en **grupo de equipos únicos** y, a continuación, en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-139">Click **Single computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="9ee90-140">En **seleccionar características**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-140">In **Select features**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-141">Si planea usar un único FQDN e dirección IP para el servicio de acceso SIP, el servicio de conferencias web de Lync Server 2013 y los servicios perimetrales A/V, active la casilla **usar un único FQDN e dirección IP** .</span><span class="sxs-lookup"><span data-stu-id="9ee90-141">If you plan to use a single FQDN and IP address for the SIP Access service, Lync Server 2013 Web Conferencing service, and A/V Edge services, select the **Use a single FQDN and IP Address** check box.</span></span>
    
      - <span data-ttu-id="9ee90-142">Si planea habilitar la Federación, active la casilla **Habilitar la Federación para este grupo perimetral (puerto 5061)** .</span><span class="sxs-lookup"><span data-stu-id="9ee90-142">If you plan to enable federation select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9ee90-143">Puede seleccionar esta opción, pero solo se puede publicar externamente un grupo perimetral o un servidor perimetral en su organización para la Federación.</span><span class="sxs-lookup"><span data-stu-id="9ee90-143">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="9ee90-144">Todo el acceso de usuarios federados, incluidos los usuarios de mensajería instantánea (mi) pública, con el mismo grupo perimetral o servidor de borde único.</span><span class="sxs-lookup"><span data-stu-id="9ee90-144">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="9ee90-145">Por ejemplo, si su implementación incluye un grupo perimetral o un solo servidor perimetral implementado en Nueva York y uno implementado en Londres y habilita la compatibilidad con la Federación en el grupo de servidores perimetrales de Nueva York o en el único servidor perimetral, el tráfico de señales para usuarios federados pasará por el grupo de servidores perimetrales de Nueva York o el servidor perimetral único.</span><span class="sxs-lookup"><span data-stu-id="9ee90-145">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="9ee90-146">Esto es así incluso para las comunicaciones con usuarios de Londres, aunque un usuario interno de Londres que llame a un usuario federado de Londres usa el grupo de servidores o el servidor perimetral de Londres para el tráfico A/V.</span><span class="sxs-lookup"><span data-stu-id="9ee90-146">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="9ee90-147">Si tiene previsto admitir el protocolo de presencia y mensajería extensible (XMPP) para su implementación, active la casilla de verificación **Habilitar Federación XMPP (puerto 5269)**</span><span class="sxs-lookup"><span data-stu-id="9ee90-147">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="9ee90-148">En **seleccionar opciones de IP**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-148">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-149">**Habilitar IPv4 en la interfaz interna**: Active la casilla si desea aplicar una dirección IPv4 al servidor perimetral o a la interfaz interna de grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-149">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="9ee90-150">**Habilitar IPv6 en la interfaz interna**: Active la casilla si desea aplicar una dirección IPv6 al servidor perimetral o a la interfaz interna de la agrupación perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-150">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="9ee90-151">**Habilitar IPv4 en la interfaz externa**: Active la casilla si desea aplicar una dirección IPv4 al servidor perimetral o a la interfaz externa del grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-151">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="9ee90-152">**Habilitar IPv6 en la interfaz externa**: Active la casilla si desea aplicar una dirección IPv6 al servidor perimetral o a la interfaz externa del grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-152">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <span data-ttu-id="9ee90-153">También puede configurar el servidor perimetral o el grupo Edge para usar una dirección de traducción de direcciones de red para las direcciones IP externas.</span><span class="sxs-lookup"><span data-stu-id="9ee90-153">You can also configure the Edge Server or Edge pool to use a network address translation address for the external IP addresses.</span></span> <span data-ttu-id="9ee90-154">Para ello, active la casilla **la dirección IP externa de este grupo de límites la traduce nat**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-154">You do this by selecting the check box **The external IP address of this Edge pool is translated by NAT**.</span></span>

8.  <span data-ttu-id="9ee90-155">En los **FQDN externos**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-155">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-156">Si en **seleccionar características** ha elegido usar un único FQDN e dirección IP para el acceso SIP, el servicio de conferencias web y el servicio perimetral a/V, escriba el FQDN externo en el **acceso SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-156">If in **Select features** you chose to use a single FQDN and IP address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9ee90-157">Si elige esta opción, debe especificar un número de puerto diferente para cada uno de los servicios perimetrales (configuración de Puerto recomendado: 5061 para el servicio perimetral de Access, 444 para el servicio perimetral de conferencias web y 443 para el servicio perimetral de a/V).</span><span class="sxs-lookup"><span data-stu-id="9ee90-157">If you choose this option, you must specify a different port number for each of the edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="9ee90-158">Seleccionar esta opción puede ayudar a evitar posibles problemas de conectividad y simplificar la configuración, ya que puede usar el mismo número de puerto (por ejemplo, 443) para los tres servicios.</span><span class="sxs-lookup"><span data-stu-id="9ee90-158">Selecting this option can help prevent potential connectivity issues, and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="9ee90-159">Si en **seleccionar características** no ha elegido usar un FQDN y una dirección IP únicos, escriba los FQDN externos para el **acceso SIP**, las **conferencias web** y el **audio video**, manteniendo los puertos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="9ee90-159">If in **Select features** you did not chose to use a single FQDN and IP Address, type the External FQDNs for **SIP Access**, **Web Conferencing** and **Audio Video**, keeping the default ports.</span></span>

9.  <span data-ttu-id="9ee90-160">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-160">Click **Next**.</span></span>

10. <span data-ttu-id="9ee90-161">En **definir la dirección IP interna**, escriba la dirección IP de su servidor perimetral en la **dirección IPv4 interna** y la **dirección IPv6 interna** , según corresponda a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="9ee90-161">In **Define the Internal IP address**, type the IP address of your Edge Server in **Internal IPv4 address** and **Internal IPv6 address** as is appropriate for your requirements.</span></span> <span data-ttu-id="9ee90-162">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-162">Click **Next**.</span></span>

11. <span data-ttu-id="9ee90-163">En **definir la dirección IP externa**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-163">In **Define the External IP address**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-164">Si decide usar un FQDN y una dirección IP únicos para el acceso SIP, el servicio de conferencias web y el servicio perimetral A/V, escriba la dirección IPv4 externa del servidor perimetral en **acceso SIP** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-164">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 address of the Edge Server in **SIP Access**, and then, click **Next**.</span></span>
    
      - <span data-ttu-id="9ee90-165">Si decide usar direcciones IPv6, escriba la dirección IPv6 externa del servidor perimetral en **acceso SIP** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-165">If you chose to use IPv6 addresses, type the external IPv6 address of the Edge Server in **SIP Access**, and then, click **Next**.</span></span>
    
      - <span data-ttu-id="9ee90-166">Si no ha elegido usar un FQDN y una dirección IP únicos para el acceso SIP, el servicio de conferencias web y el servicio perimetral A/V, escriba las direcciones IPv4 externas del servidor perimetral en **acceso SIP**, **conferencia web** y **Conferencia a/v** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-166">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 addresses of the Edge Server in **SIP Access**, **Web Conferencing**, and **A/V Conferencing**, and then click **Next**.</span></span>
    
      - <span data-ttu-id="9ee90-167">Si decide usar direcciones IPv6 y no ha elegido usar un FQDN y una dirección IP únicos para el acceso SIP, el servicio de conferencias web y el servicio perimetral a/V, escriba las direcciones IPv6 externas del servidor perimetral en **acceso SIP**, **conferencias web** y **conferencias a/v** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-167">If you chose to use IPv6 addresses and did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 addresses of the Edge Server in **SIP Access**, **Web Conferencing**, and **A/V Conferencing**, and then click **Next**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9ee90-168">Si no ha elegido habilitar ni asignar direcciones IPv6, no podrá ver este cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-168">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

        
        </div>

12. <span data-ttu-id="9ee90-169">Si decide usar NAT, aparecerá un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-169">If you chose to use NAT, a dialog box appears.</span></span> <span data-ttu-id="9ee90-170">En **dirección IPv4 pública para el servicio a/V Edge**, escriba la dirección IPv4 pública que quiere que traduzca NAT y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-170">In **Public IPv4 address for the A/V Edge service**, type the public IPv4 address to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-171">Debe ser la dirección IP externa del servicio perimetral A/V.</span><span class="sxs-lookup"><span data-stu-id="9ee90-171">This should be the external IP address of the A/V Edge service.</span></span>

    
    </div>

13. <span data-ttu-id="9ee90-172">Si decide usar direcciones NAT e IPv6, aparecerá un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-172">If you chose to use NAT and IPv6 addresses, a dialog box appears.</span></span> <span data-ttu-id="9ee90-173">En **dirección IPv6 pública para el servicio a/V Edge**, escriba la dirección IPv6 pública que quiere que traduzca NAT y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-173">In **Public IPv6 address for the A/V Edge service**, type the public IPv6 address to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-174">Debe ser la dirección IP externa del servicio perimetral A/V.</span><span class="sxs-lookup"><span data-stu-id="9ee90-174">This should be the external IP address of the A/V Edge service.</span></span>

    
    </div>

14. <span data-ttu-id="9ee90-175">En **definir el próximo salto**, en **grupo de próximo salto**, seleccione el nombre del grupo interno, que puede ser un grupo de servidores front-end o un grupo de servidores Standard.</span><span class="sxs-lookup"><span data-stu-id="9ee90-175">In **Define the next hop**, in **Next hop pool**, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="9ee90-176">O bien, si su implementación incluye un director, seleccione el director.</span><span class="sxs-lookup"><span data-stu-id="9ee90-176">Or, if your deployment includes a Director, select the Director.</span></span> <span data-ttu-id="9ee90-177">A continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-177">Then, click **Next**.</span></span>

15. <span data-ttu-id="9ee90-178">En la opción **asociar grupos front end**, especifique uno o varios grupos internos, que pueden incluir grupos de aplicaciones para el usuario y servidores Standard Edition, para que se asocien a este servidor perimetral; para ello, seleccione los nombres de los grupos internos que usarán este servidor perimetral para la comunicación con los usuarios externos admitidos.</span><span class="sxs-lookup"><span data-stu-id="9ee90-178">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pools that are to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-179">Solo se puede asociar un grupo perimetral de carga equilibrada o un único servidor perimetral con cada grupo interno para tráfico de A/V.</span><span class="sxs-lookup"><span data-stu-id="9ee90-179">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="9ee90-180">Si ya tiene un grupo interno asociado con un grupo perimetral o un servidor perimetral, aparece una advertencia que indica que el grupo interno ya está asociado a un grupo perimetral o a un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-180">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="9ee90-181">Si selecciona un grupo que ya está asociado a otro servidor perimetral, este cambiará la asociación.</span><span class="sxs-lookup"><span data-stu-id="9ee90-181">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

16. <span data-ttu-id="9ee90-182">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-182">Click **Finish**.</span></span>

17. <span data-ttu-id="9ee90-183">Publique su topología.</span><span class="sxs-lookup"><span data-stu-id="9ee90-183">Publish your topology.</span></span>

</div>

<div>

## <a name="to-define-the-topology-for-a-dns-load-balanced-edge-server-pool"></a><span data-ttu-id="9ee90-184">Para definir la topología de un grupo de servidores perimetrales de carga equilibrada de DNS</span><span class="sxs-lookup"><span data-stu-id="9ee90-184">To define the topology for a DNS load balanced Edge Server pool</span></span>

1.  <span data-ttu-id="9ee90-185">Iniciar generador de topología: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **generador de topología de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-185">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="9ee90-186">En el árbol de consola, expanda el sitio en el que desea implementar servidores perimetrales.</span><span class="sxs-lookup"><span data-stu-id="9ee90-186">In the console tree, expand the site in which you want to deploy Edge Servers.</span></span>

3.  <span data-ttu-id="9ee90-187">Haga clic con el botón secundario en **agrupaciones perimetrales** y luego haga clic en **nuevo borde**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-187">Right-click **Edge Pools**, and then click **New Edge Pool**.</span></span>

4.  <span data-ttu-id="9ee90-188">En **definir el nuevo grupo de límites**, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-188">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="9ee90-189">En **definir el FQDN del grupo perimetral**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-189">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-190">En **FQDN del grupo**, escriba el nombre de dominio completo (FQDN) para la conexión interna del grupo Edge.</span><span class="sxs-lookup"><span data-stu-id="9ee90-190">In **Pool FQDN**, type the fully qualified domain name (FQDN) for the internal connection of the Edge pool.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="9ee90-191">El nombre que especifique para el grupo debe ser el nombre del grupo de bordes interno.</span><span class="sxs-lookup"><span data-stu-id="9ee90-191">The name you specify for the pool must be the internal edge pool name.</span></span> <span data-ttu-id="9ee90-192">Debe definirse como un FQDN.</span><span class="sxs-lookup"><span data-stu-id="9ee90-192">This must be defined as a FQDN.</span></span> <span data-ttu-id="9ee90-193">El Generador de topologías usa nombres de dominio completos, no nombres cortos.</span><span class="sxs-lookup"><span data-stu-id="9ee90-193">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="9ee90-194">Utilice únicamente caracteres estándar (incluyendo A–Z, a–z, 0–9 y guiones) a la hora de asignar FQDN de sus Lync Server, servidores perimetrales y grupos.</span><span class="sxs-lookup"><span data-stu-id="9ee90-194">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="9ee90-195">No utilice caracteres Unicode ni de subrayado.</span><span class="sxs-lookup"><span data-stu-id="9ee90-195">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="9ee90-196">A menudo, los caracteres no estándar de un FQDN no son compatibles con las entidades de certificación públicas y DNS externas (cuando se debe asignar el FQDN al SN en el certificado).</span><span class="sxs-lookup"><span data-stu-id="9ee90-196">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span>

        
        </div>
    
      - <span data-ttu-id="9ee90-197">Haga clic en **grupo de varios equipos** y, a continuación, en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-197">Click **Multiple computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="9ee90-198">En **seleccionar características**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-198">In **Select features**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-199">Si tiene pensado usar un FQDN y una dirección IP únicos para el acceso SIP, el servicio de conferencias web de Lync Server 2013 y los servicios perimetrales A/V, active la casilla **usar un único FQDN e dirección IP** .</span><span class="sxs-lookup"><span data-stu-id="9ee90-199">If you plan to use a single FQDN and IP address for the SIP access, Lync Server 2013 Web Conferencing service and A/V Edge services, select the **Use a single FQDN and IP Address** check box.</span></span>
    
      - <span data-ttu-id="9ee90-200">Si tiene previsto habilitar la Federación, active la casilla **Habilitar la Federación para este grupo perimetral (puerto 5061)** .</span><span class="sxs-lookup"><span data-stu-id="9ee90-200">If you plan to enable federation, select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span> <span data-ttu-id="9ee90-201">Haga clic en **siguiente**</span><span class="sxs-lookup"><span data-stu-id="9ee90-201">Click **Next**</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9ee90-202">Puede seleccionar esta opción, pero solo se puede publicar externamente un grupo perimetral o un servidor perimetral en su organización para la Federación.</span><span class="sxs-lookup"><span data-stu-id="9ee90-202">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="9ee90-203">Todo el acceso de usuarios federados, incluidos los usuarios de mensajería instantánea (mi) pública, con el mismo grupo perimetral o servidor de borde único.</span><span class="sxs-lookup"><span data-stu-id="9ee90-203">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="9ee90-204">Por ejemplo, si la implementación incluye la implementación en Nueva York de un grupo de servidores perimetrales o un servidor perimetral único y la implementación de uno en Londres y habilita la compatibilidad de federación en el grupo de servidores perimetrales o el servidor perimetral único de Nueva York, el tráfico de señales de los usuarios federales pasará por el grupo de servidores perimetrales o el servidor perimetral único de Nueva York.</span><span class="sxs-lookup"><span data-stu-id="9ee90-204">For instance, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="9ee90-205">Esto es así incluso para las comunicaciones con usuarios de Londres, aunque un usuario interno de Londres que llame a un usuario federado de Londres usa el grupo de servidores o el servidor perimetral de Londres para el tráfico A/V.</span><span class="sxs-lookup"><span data-stu-id="9ee90-205">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="9ee90-206">Si tiene previsto admitir el protocolo de presencia y mensajería extensible (XMPP) para su implementación, active la casilla de verificación **Habilitar Federación XMPP (puerto 5269)**</span><span class="sxs-lookup"><span data-stu-id="9ee90-206">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="9ee90-207">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-207">Click **Next**.</span></span>

8.  <span data-ttu-id="9ee90-208">En **seleccionar opciones de IP**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-208">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-209">**Habilitar IPv4 en la interfaz interna**: Active la casilla si desea aplicar una dirección IPv4 al servidor perimetral o a la interfaz interna de grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-209">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="9ee90-210">**Habilitar IPv6 en la interfaz interna**: Active la casilla si desea aplicar una dirección IPv6 al servidor perimetral o a la interfaz interna de la agrupación perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-210">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="9ee90-211">**Habilitar IPv4 en la interfaz externa**: Active la casilla si desea aplicar una dirección IPv4 al servidor perimetral o a la interfaz externa del grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-211">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="9ee90-212">**Habilitar IPv6 en la interfaz externa**: Active la casilla si desea aplicar una dirección IPv6 al servidor perimetral o a la interfaz externa del grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-212">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <span data-ttu-id="9ee90-213">También puede configurar el servidor perimetral o el grupo Edge para usar una dirección de traducción de direcciones de red para las direcciones IP externas.</span><span class="sxs-lookup"><span data-stu-id="9ee90-213">You can also configure the Edge Server or Edge pool to use a network address translation address for the external IP addresses.</span></span> <span data-ttu-id="9ee90-214">Para ello, active la casilla **la dirección IP externa de este grupo de límites la traduce nat**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-214">You do this by selecting the check box **The external IP address of this Edge pool is translated by NAT**.</span></span>

9.  <span data-ttu-id="9ee90-215">En los **FQDN externos**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-215">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-216">Si en **seleccionar características** ha elegido usar un único FQDN e dirección IP para el acceso SIP, el servicio de conferencias web y el servicio perimetral a/V, escriba el FQDN externo en el **acceso SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-216">If in **Select features** you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9ee90-217">Si elige esta opción, debe especificar un número de puerto diferente para cada uno de los servicios perimetrales (configuración de Puerto recomendado: 5061 para el servicio perimetral de Access, 444 para el servicio perimetral de conferencias web y 443 para el servicio perimetral de a/V).</span><span class="sxs-lookup"><span data-stu-id="9ee90-217">If you choose this option, you must specify a different port number for each of the Edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="9ee90-218">Al seleccionar esta opción, puede ayudar a evitar posibles problemas de conectividad y simplificar la configuración porque puede usar el mismo número de puerto (por ejemplo, 443) para los tres servicios.</span><span class="sxs-lookup"><span data-stu-id="9ee90-218">By selecting this option, you can help prevent potential connectivity issues and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="9ee90-219">Si en **seleccionar características** no ha elegido usar un FQDN y una dirección IP únicos, escriba el FQDN que ha elegido para el lado público al que está enfrentada el grupo perimetral para el **acceso por SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-219">If in **Select features** you did not chose to use a single FQDN and IP Address, type the FQDN that you have chosen for your public facing side of the edge pool for in **SIP Access**.</span></span> <span data-ttu-id="9ee90-220">En **conferencias web**, escriba el FQDN que ha elegido para el lado público al que está enfrentada el grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-220">In **Web Conferencing**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="9ee90-221">En **audio o vídeo**, escriba el nombre de dominio completo que haya elegido para el lado al que se enfrentará el grupo del borde.</span><span class="sxs-lookup"><span data-stu-id="9ee90-221">In **Audio/Video**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="9ee90-222">Use los puertos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="9ee90-222">Use the default ports.</span></span>

10. <span data-ttu-id="9ee90-223">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-223">Click **Next**.</span></span>

11. <span data-ttu-id="9ee90-224">En **definir los equipos de este grupo**, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-224">In **Define the computers in this pool**, click **Add**.</span></span>

12. <span data-ttu-id="9ee90-225">En **nombre completo y dirección IP internos**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-225">In **Internal FQDN and IP address**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-226">En **dirección IPv4 interna**, escriba la dirección IPv4 y la **dirección IPv6 interna** , según corresponda a sus requisitos para el primer servidor perimetral que desea crear en este grupo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-226">In **Internal IPv4 address**, type the IPv4 address and **Internal IPv6 address** as is appropriate for your requirements for the first Edge Server that you want to create in this pool.</span></span>
    
      - <span data-ttu-id="9ee90-227">En **nombre de dominio interno**, escriba el FQDN del primer servidor perimetral que desea crear en este grupo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-227">In **Internal FQDN**, type the FQDN of the first Edge Server that you want to create in this pool.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9ee90-228">El nombre que especifique necesita ser idéntico al nombre del equipo configurado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="9ee90-228">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="9ee90-229">Un equipo no incorporado a un dominio tiene un nombre corto de forma predeterminada, no un nombre de dominio completo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-229">By default, the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="9ee90-230">El Generador de topologías usa nombres de dominio completos, no nombres cortos.</span><span class="sxs-lookup"><span data-stu-id="9ee90-230">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="9ee90-231">Por lo tanto, debe configurar un sufijo DNS en el nombre del equipo para implementarse como servidor perimetral que no está unido a un dominio.</span><span class="sxs-lookup"><span data-stu-id="9ee90-231">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="9ee90-232">Use solo caracteres estándar (incluidos A-Z, a-z, 0-9 y guiones) al asignar FQDN de sus servidores de Lync, servidores perimetrales, grupos y matrices.</span><span class="sxs-lookup"><span data-stu-id="9ee90-232">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, pools, and arrays.</span></span> <span data-ttu-id="9ee90-233">No utilice caracteres Unicode ni de subrayado.</span><span class="sxs-lookup"><span data-stu-id="9ee90-233">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="9ee90-234">A menudo, los caracteres no estándar de un FQDN no son compatibles con las entidades de certificación públicas y DNS externas (cuando se debe asignar el FQDN al SN en el certificado).</span><span class="sxs-lookup"><span data-stu-id="9ee90-234">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="9ee90-235">Para más información sobre cómo agregar un sufijo DNS al nombre de un equipo, consulte <A href="lync-server-2013-configure-dns-for-edge-support.md">configurar DNS para la compatibilidad con Edge en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9ee90-235">For details about adding a DNS suffix to a computer name, see <A href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</A>.</span></span>

        
        </div>

13. <span data-ttu-id="9ee90-236">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-236">Click **Next**.</span></span>

14. <span data-ttu-id="9ee90-237">En **definir las direcciones IP externas**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-237">In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-238">Si decide usar un FQDN y una dirección IP únicos para el acceso SIP, el servicio de conferencias web y el servicio perimetral A/V, escriba la dirección IP externa del servidor perimetral en **acceso de SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-238">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IP address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="9ee90-239">Si no ha elegido usar un FQDN y una dirección IP únicos para el servicio de conferencia de acceso por SIP, servicio de conferencias por Internet y a/V, escriba la dirección IP que haya elegido para el lado de cara pública de este servidor de grupo de bordes para el **acceso de SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-239">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IP address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="9ee90-240">En **conferencias web**, escriba la dirección IP que ha elegido para el lado de la dirección pública de este servidor de la agrupación perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-240">In **Web Conferencing**, type the IP address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="9ee90-241">En **conferencia A/V**, escriba la dirección IP que ha elegido para el lado al que va dirigida la pública de este servidor de la agrupación perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-241">In **A/V Conferencing**, type the IP address you have chosen for your public facing side of this Edge pool server.</span></span>

15. <span data-ttu-id="9ee90-242">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-242">Click **Next**.</span></span>

16. <span data-ttu-id="9ee90-243">Si decide habilitar las direcciones IPv6, en **definir las direcciones IP externas**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-243">If you chose to enable IPv6 addresses, In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-244">Si decide usar un FQDN y una dirección IP únicos para el acceso SIP, el servicio de conferencias web y el servicio perimetral A/V, escriba la dirección IPv6 externa del servidor perimetral en **acceso de SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-244">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="9ee90-245">Si no ha elegido usar un FQDN y una dirección IP únicos para el servicio de conferencia de acceso por SIP, servicio de conferencias por Internet y a/V, escriba la dirección IPv6 que haya elegido para el lado de cara pública de este servidor de grupo de bordes para el **acceso de SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-245">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IPv6 address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="9ee90-246">En **conferencias web**, escriba la dirección IPv6 que haya elegido para el lado al que va dirigida la pública de este servidor de grupo de bordes.</span><span class="sxs-lookup"><span data-stu-id="9ee90-246">In **Web Conferencing**, type the IPv6 address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="9ee90-247">En **conferencias A/V**, escriba la dirección IPv6 que ha elegido para el lado al que se enfrenta su público en este servidor de la agrupación perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-247">In **A/V Conferencing**, type the IPv6 address you have chosen for your public facing side of this Edge pool server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-248">Si no ha elegido habilitar ni asignar direcciones IPv6, no podrá ver este cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-248">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

    
    </div>

17. <span data-ttu-id="9ee90-249">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-249">Click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-250">Ahora verá el primer servidor perimetral que creó en su grupo en el cuadro de diálogo <STRONG>definir los equipos de este grupo</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="9ee90-250">You will now see the first Edge Server you created in your pool in the <STRONG>Define the computers in this pool</STRONG> dialog box.</span></span>

    
    </div>

18. <span data-ttu-id="9ee90-251">En **definir los equipos de este grupo**, haga clic en **Agregar** y, a continuación, repita los pasos 11 a 14 para el segundo servidor perimetral que desea agregar al grupo de bordes.</span><span class="sxs-lookup"><span data-stu-id="9ee90-251">In **Define the computers in this pool**, click **Add**, and then repeat steps 11 through 14 for the second Edge Server that you want to add to you Edge pool.</span></span>

19. <span data-ttu-id="9ee90-252">Después de repetir los pasos 11 a 14, haga clic en **siguiente** en **definir los equipos de este grupo**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-252">After you repeat steps 11 through 14, click **Next** in **Define the computers in this pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-253">En este momento, puede ver ambos servidores perimetrales en su grupo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-253">At this point, you can see both of the Edge Servers in your pool.</span></span>

    
    </div>

20. <span data-ttu-id="9ee90-254">Si decide usar NAT, aparecerá un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-254">If you chose to use NAT, a dialog box appears.</span></span> <span data-ttu-id="9ee90-255">En **dirección IP pública**, escriba las direcciones IPv4 e IPv6 públicas (según corresponda) que NAT va a traducir y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-255">In **Public IP address**, type the public IPv4 and IPv6 (as appropriate) addresses to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-256">Debe ser la dirección IP externa del borde A/V.</span><span class="sxs-lookup"><span data-stu-id="9ee90-256">This should be the external IP Address of the A/V Edge.</span></span>

    
    </div>

21. <span data-ttu-id="9ee90-257">En **definir el próximo salto**, en la lista **siguiente grupo de saltos** , seleccione el nombre del grupo interno, que puede ser un grupo de servidores front-end o un grupo Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="9ee90-257">In **Define the next hop**, in the **Next hop pool** list, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="9ee90-258">O bien, si su implementación incluye un director, seleccione el nombre del director.</span><span class="sxs-lookup"><span data-stu-id="9ee90-258">Or, if your deployment includes a Director, select the name of the Director.</span></span> <span data-ttu-id="9ee90-259">A continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-259">Then, click **Next**.</span></span>

22. <span data-ttu-id="9ee90-260">En las **agrupaciones front end de Associate**, especifique uno o varios grupos internos, que pueden incluir grupos front-end y servidores Standard Edition, que se asociarán con este servidor perimetral seleccionando los nombres de los pools internos que usarán este servidor perimetral para la comunicación con los usuarios externos admitidos.</span><span class="sxs-lookup"><span data-stu-id="9ee90-260">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pool(s) that is to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-261">Solo se puede asociar un grupo perimetral de carga equilibrada o un único servidor perimetral con cada grupo interno para tráfico de A/V.</span><span class="sxs-lookup"><span data-stu-id="9ee90-261">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="9ee90-262">Si ya tiene un grupo interno asociado con un grupo perimetral o un servidor perimetral, aparece una advertencia que indica que el grupo interno ya está asociado a un grupo perimetral o a un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-262">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="9ee90-263">Si selecciona un grupo que ya está asociado a otro servidor perimetral, este cambiará la asociación.</span><span class="sxs-lookup"><span data-stu-id="9ee90-263">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

23. <span data-ttu-id="9ee90-264">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-264">Click **Finish**.</span></span>

24. <span data-ttu-id="9ee90-265">Publique su topología.</span><span class="sxs-lookup"><span data-stu-id="9ee90-265">Publish your topology.</span></span>

</div>

<div>

## <a name="to-define-the-topology-for-a-hardware-load-balanced-edge-server-pool"></a><span data-ttu-id="9ee90-266">Para definir la topología de un grupo de servidores perimetrales con equilibrio de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="9ee90-266">To define the topology for a hardware load balanced Edge Server pool</span></span>

1.  <span data-ttu-id="9ee90-267">Iniciar generador de topología: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **generador de topología de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-267">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="9ee90-268">En el árbol de consola, expanda el sitio en el que desea implementar servidores perimetrales.</span><span class="sxs-lookup"><span data-stu-id="9ee90-268">In the console tree, expand the site in which you want to deploy Edge Servers.</span></span>

3.  <span data-ttu-id="9ee90-269">Haga clic con el botón secundario en **agrupaciones perimetrales** y seleccione **nuevo grupo perimetral**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-269">Right-click **Edge Pools**, and then select **New Edge Pool**.</span></span>

4.  <span data-ttu-id="9ee90-270">En **definir el nuevo grupo de límites**, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-270">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="9ee90-271">En **definir el FQDN del grupo perimetral**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-271">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-272">En **FQDN**, escriba el nombre de dominio completo (FQDN) que ha elegido para el lado interno del grupo Edge.</span><span class="sxs-lookup"><span data-stu-id="9ee90-272">In **FQDN**, type the fully qualified domain name (FQDN) you have chosen for the internal side of the Edge pool.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="9ee90-273">El nombre que especifique para el grupo debe ser el nombre del grupo de bordes interno.</span><span class="sxs-lookup"><span data-stu-id="9ee90-273">The name you specify for the pool must be the internal edge pool name.</span></span> <span data-ttu-id="9ee90-274">Debe definirse como un FQDN.</span><span class="sxs-lookup"><span data-stu-id="9ee90-274">This must be defined as a FQDN.</span></span> <span data-ttu-id="9ee90-275">El Generador de topologías usa nombres de dominio completos, no nombres cortos.</span><span class="sxs-lookup"><span data-stu-id="9ee90-275">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="9ee90-276">Utilice únicamente caracteres estándar (incluyendo A–Z, a–z, 0–9 y guiones) a la hora de asignar FQDN de sus Lync Server, servidores perimetrales y grupos.</span><span class="sxs-lookup"><span data-stu-id="9ee90-276">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="9ee90-277">No utilice caracteres Unicode ni de subrayado.</span><span class="sxs-lookup"><span data-stu-id="9ee90-277">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="9ee90-278">A menudo, los caracteres no estándar de un FQDN no son compatibles con las entidades de certificación públicas y DNS externas (cuando se debe asignar el FQDN al SN en el certificado).</span><span class="sxs-lookup"><span data-stu-id="9ee90-278">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span>

        
        </div>
    
    <!-- end list -->
    
      - <span data-ttu-id="9ee90-279">Haga clic en **varios grupos de equipos** y luego en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-279">Click **Multiple computer pool**, and then **Next**.</span></span>

6.  <span data-ttu-id="9ee90-280">En **seleccionar características** , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-280">In **Select features** do the following:</span></span>
    
      - <span data-ttu-id="9ee90-281">Si tiene pensado usar un FQDN y una dirección IP únicos para el servicio de acceso SIP, el servicio de conferencias web de Lync Server y el servicio perimetral A/V, active la casilla **usar un solo FQDN & dirección IP** .</span><span class="sxs-lookup"><span data-stu-id="9ee90-281">If you plan to use a single FQDN and IP address for the SIP access service, Lync Server Web Conferencing service, and A/V Edge service, select the **Use a single FQDN & IP Address** check box.</span></span>
    
      - <span data-ttu-id="9ee90-282">Si tiene previsto habilitar la Federación, active la casilla **Habilitar la Federación para este grupo perimetral (puerto 5061)** .</span><span class="sxs-lookup"><span data-stu-id="9ee90-282">If you plan to enable federation, select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9ee90-283">Puede seleccionar esta opción, pero solo se puede publicar externamente un grupo perimetral o un servidor perimetral en su organización para la Federación.</span><span class="sxs-lookup"><span data-stu-id="9ee90-283">You can select this option, but only one Edge pool or Edge Server in your organization may be published externally for federation.</span></span> <span data-ttu-id="9ee90-284">Todo el acceso de usuarios federados, incluidos los usuarios de mensajería instantánea (mi) pública, con el mismo grupo perimetral o servidor de borde único.</span><span class="sxs-lookup"><span data-stu-id="9ee90-284">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="9ee90-285">Por ejemplo, si la implementación incluye la implementación en Nueva York de un grupo de servidores perimetrales o un servidor perimetral único y la implementación de uno en Londres y habilita la compatibilidad de federación en el grupo de servidores perimetrales o el servidor perimetral único de Nueva York, el tráfico de señales de los usuarios federales pasará por el grupo de servidores perimetrales o el servidor perimetral único de Nueva York.</span><span class="sxs-lookup"><span data-stu-id="9ee90-285">For instance, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="9ee90-286">Esto es así incluso para las comunicaciones con usuarios de Londres, aunque un usuario interno de Londres que llame a un usuario federado de Londres usa el grupo de servidores o el servidor perimetral de Londres para el tráfico A/V.</span><span class="sxs-lookup"><span data-stu-id="9ee90-286">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="9ee90-287">Si tiene previsto admitir el protocolo de presencia y mensajería extensible (XMPP) para su implementación, active la casilla de verificación **Habilitar Federación XMPP (puerto 5269)**</span><span class="sxs-lookup"><span data-stu-id="9ee90-287">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="9ee90-288">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-288">Click **Next**.</span></span>

8.  <span data-ttu-id="9ee90-289">En **seleccionar opciones de IP**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-289">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-290">**Habilitar IPv4 en la interfaz interna**: Active la casilla si desea aplicar una dirección IPv4 al servidor perimetral o a la interfaz interna de grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-290">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="9ee90-291">**Habilitar IPv6 en la interfaz interna**: Active la casilla si desea aplicar una dirección IPv6 al servidor perimetral o a la interfaz interna de la agrupación perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-291">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="9ee90-292">**Habilitar IPv4 en la interfaz externa**: Active la casilla si desea aplicar una dirección IPv4 al servidor perimetral o a la interfaz externa del grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-292">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="9ee90-293">**Habilitar IPv6 en la interfaz externa**: Active la casilla si desea aplicar una dirección IPv6 al servidor perimetral o a la interfaz externa del grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-293">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9ee90-294"><STRONG>No</STRONG> seleccione la casilla de verificación <STRONG>la dirección IP externa del grupo de servidores perimetrales está traducida por NAT</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="9ee90-294"><STRONG>Do Not</STRONG> select the <STRONG>The external IP address of the Edge pool is translated by NAT</STRONG> check box.</span></span> <span data-ttu-id="9ee90-295">La traducción de direcciones de red (NAT) no es compatible cuando se usa el equilibrio de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="9ee90-295">Network address translation (NAT) is not supported when you are using hardware load balancing.</span></span>

    
    </div>

9.  <span data-ttu-id="9ee90-296">En los **FQDN externos**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-296">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-297">Si en **seleccionar características** ha elegido usar un único FQDN e dirección IP para el acceso SIP, el servicio de conferencias web y el servicio perimetral a/V, escriba el FQDN externo en el **acceso SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-297">If in **Select features** you chose to use a single FQDN and IP address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9ee90-298">Si elige esta opción, debe especificar un número de puerto diferente para cada uno de los servicios perimetrales (configuración de Puerto recomendado: 5061 para el servicio perimetral de Access, 444 para el servicio perimetral de conferencias web y 443 para el servicio perimetral a/V).</span><span class="sxs-lookup"><span data-stu-id="9ee90-298">If you choose to select this option, you must specify a different port number for each of the Edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="9ee90-299">Al seleccionar esta opción, puede ayudar a evitar posibles problemas de conectividad y simplificar la configuración porque puede usar el mismo número de puerto (por ejemplo, 443) para los tres servicios.</span><span class="sxs-lookup"><span data-stu-id="9ee90-299">By selecting this option, you can help prevent potential connectivity issues and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="9ee90-300">Si en **seleccionar características** no ha elegido usar un FQDN y una dirección IP únicos, escriba el FQDN que ha elegido para el lado público al que está enfrentada el grupo perimetral para el **acceso por SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-300">If in **Select features** you did not chose to use a single FQDN and IP address, type the FQDN that you have chosen for your public facing side of the edge pool for in **SIP Access**.</span></span> <span data-ttu-id="9ee90-301">En **conferencias web**, escriba el FQDN que ha elegido para el lado público al que está enfrentada el grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-301">In **Web Conferencing**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="9ee90-302">En **audio o vídeo**, escriba el nombre de dominio completo que haya elegido para el lado al que se enfrentará el grupo del borde.</span><span class="sxs-lookup"><span data-stu-id="9ee90-302">In **Audio/Video**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="9ee90-303">Use los puertos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="9ee90-303">Use the default ports.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="9ee90-304">Estos serán los FQDN de IP virtual (VIP) de orientación pública para el grupo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-304">These will be the publicly facing virtual IP (VIP) FQDNs for the pool.</span></span>

        
        </div>

10. <span data-ttu-id="9ee90-305">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-305">Click **Next**.</span></span>

11. <span data-ttu-id="9ee90-306">En **definir los equipos de este grupo**, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-306">In **Define the computers in this pool**, click **Add**.</span></span>

12. <span data-ttu-id="9ee90-307">En **definir las direcciones IP externas**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-307">In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-308">Si decide usar un FQDN y una dirección IP únicos para el acceso SIP, el servicio de conferencias web y el servicio perimetral de A/V, escriba la dirección IPv4 externa del servidor perimetral en el **acceso por SIP**. dirección IP externa del servidor perimetral en **acceso de SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-308">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 address of the Edge Server in **SIP Access**.external IP address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="9ee90-309">Si no ha elegido usar un FQDN y una dirección IP únicos para el servicio de conferencia de acceso por SIP, servicio de conferencias por Internet y a/V, escriba la dirección IP que haya elegido para el lado de cara pública de este servidor de grupo de bordes para el **acceso de SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-309">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IP address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="9ee90-310">En **conferencias web**, escriba la dirección IP que ha elegido para el lado de la dirección pública de este servidor de la agrupación perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-310">In **Web Conferencing**, type the IP address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="9ee90-311">En **conferencia A/V**, escriba la dirección IP que ha elegido para el lado al que va dirigida la pública de este servidor de la agrupación perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-311">In **A/V Conferencing**, type the IP address you have chosen for your public facing side of this Edge pool server.</span></span>

13. <span data-ttu-id="9ee90-312">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-312">Click **Next**.</span></span>

14. <span data-ttu-id="9ee90-313">Si decide habilitar las direcciones IPv6, en **definir las direcciones IP externas**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee90-313">If you chose to enable IPv6 addresses, In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="9ee90-314">Si decide usar un FQDN y una dirección IP únicos para el acceso SIP, el servicio de conferencias web y el servicio perimetral A/V, escriba la dirección IPv6 externa del servidor perimetral en **acceso de SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-314">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="9ee90-315">Si no ha elegido usar un FQDN y una dirección IP únicos para el servicio de conferencia de acceso por SIP, servicio de conferencias por Internet y a/V, escriba la dirección IPv6 que haya elegido para el lado de cara pública de este servidor de grupo de bordes para el **acceso de SIP**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-315">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IPv6 address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="9ee90-316">En **conferencias web**, escriba la dirección IPv6 que haya elegido para el lado al que va dirigida la pública de este servidor de grupo de bordes.</span><span class="sxs-lookup"><span data-stu-id="9ee90-316">In **Web Conferencing**, type the IPv6 address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="9ee90-317">En **conferencias A/V**, escriba la dirección IPv6 que ha elegido para el lado al que se enfrenta su público en este servidor de la agrupación perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-317">In **A/V Conferencing**, type the IPv6 address you have chosen for your public facing side of this Edge pool server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-318">Si no ha elegido habilitar ni asignar direcciones IPv6, no podrá ver este cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-318">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

    
    </div>

15. <span data-ttu-id="9ee90-319">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-319">Click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-320">Ahora verá el primer servidor perimetral que creó en su grupo en el cuadro de diálogo <STRONG>definir los equipos de este grupo</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="9ee90-320">You will now see the first Edge Server you created in your pool in the <STRONG>Define the computers in this pool</STRONG> dialog box.</span></span>

    
    </div>

16. <span data-ttu-id="9ee90-321">En **definir los equipos de este grupo**, haga clic en **Agregar** y, a continuación, repita los pasos 11 a 14 para el segundo servidor perimetral que desea agregar al grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-321">In **Define the computers in this pool**, click **Add**, and then repeat steps 11 through 14 for the second Edge Server that you want to add to your Edge pool.</span></span>

17. <span data-ttu-id="9ee90-322">Después de repetir los pasos 11 a 14, haga clic en **siguiente** en **definir los equipos de este grupo**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-322">After you repeat steps 11 through 14, click **Next** in **Define the computers in this pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-323">En este momento, puede ver ambos servidores perimetrales en su grupo.</span><span class="sxs-lookup"><span data-stu-id="9ee90-323">At this point, you can see both of the Edge Servers in your pool.</span></span>

    
    </div>

18. <span data-ttu-id="9ee90-324">En **definir el próximo salto**, en la lista **siguiente grupo de saltos** , seleccione el nombre del grupo interno, que puede ser un grupo de servidores front-end o un grupo Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="9ee90-324">In **Define the next hop**, in the **Next hop pool** list, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="9ee90-325">O bien, si su implementación incluye un director, seleccione el nombre del director.</span><span class="sxs-lookup"><span data-stu-id="9ee90-325">Or, if your deployment includes a Director, select the name of the Director.</span></span> <span data-ttu-id="9ee90-326">A continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-326">Then, click **Next**.</span></span>

19. <span data-ttu-id="9ee90-327">En las **agrupaciones front end de Associate**, especifique uno o varios grupos internos, que pueden incluir grupos front-end y servidores Standard Edition, que se asociarán con este servidor perimetral seleccionando los nombres de los pools internos que usarán este servidor perimetral para la comunicación con los usuarios externos admitidos.</span><span class="sxs-lookup"><span data-stu-id="9ee90-327">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pool(s) that is to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9ee90-328">Solo se puede asociar un grupo perimetral de carga equilibrada o un único servidor perimetral con cada grupo interno para tráfico de A/V.</span><span class="sxs-lookup"><span data-stu-id="9ee90-328">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="9ee90-329">Si ya tiene un grupo interno asociado con un grupo perimetral o un servidor perimetral, aparece una advertencia que indica que el grupo interno ya está asociado a un grupo perimetral o a un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="9ee90-329">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="9ee90-330">Si selecciona un grupo que ya está asociado a otro servidor perimetral, este cambiará la asociación.</span><span class="sxs-lookup"><span data-stu-id="9ee90-330">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

20. <span data-ttu-id="9ee90-331">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="9ee90-331">Click **Finish**.</span></span>

21. <span data-ttu-id="9ee90-332">Publique su topología.</span><span class="sxs-lookup"><span data-stu-id="9ee90-332">Publish your topology.</span></span>

<span data-ttu-id="9ee90-333"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9ee90-333"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

