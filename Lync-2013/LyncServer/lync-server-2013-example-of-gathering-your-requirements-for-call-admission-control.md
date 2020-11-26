---
title: Ejemplo de recopilación de los requisitos para el control de admisión de llamadas
description: Ejemplo de recopilación de los requisitos para el control de admisión de llamadas.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Example of gathering your requirements for call admission control
ms:assetid: 3363ac53-b7c4-4a59-aea1-b2f3ee016ae1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425827(v=OCS.15)
ms:contentKeyID: 48183820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 25c0b450070bda62c2610d98cfff8c8cd16ad2af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428506"
---
# <a name="example-gathering-your-requirements-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="eb243-103">Ejemplo: recopilar los requisitos para el control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb243-103">Example: Gathering your requirements for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb243-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb243-104">

<span> </span></span></span>

<span data-ttu-id="eb243-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="eb243-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="eb243-p101">Este ejemplo muestra cómo planificar e implementar el servicio de control de admisión de llamadas (CAC). De forma general, esto consta de las siguientes actividades:</span><span class="sxs-lookup"><span data-stu-id="eb243-p101">This example shows you how to plan for and implement call admission control (CAC). At a high level, this consists of the following activities:</span></span>

1.  <span data-ttu-id="eb243-108">Identifica todos los concentradores de red y redes troncales (llamados *regiones de red*).</span><span class="sxs-lookup"><span data-stu-id="eb243-108">Identify all of your network hubs and backbones (known as *network regions*).</span></span>

2.  <span data-ttu-id="eb243-109">Identifique el sitio central de Lync Server que administrará CAC para cada región de la red.</span><span class="sxs-lookup"><span data-stu-id="eb243-109">Identify the Lync Server central site that will manage CAC for each network region.</span></span>

3.  <span data-ttu-id="eb243-110">Identifica y define los *sitios de red* que están conectados a cada región de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-110">Identify and define the *network sites* that are connected to each network region.</span></span>

4.  <span data-ttu-id="eb243-111">Para cada sitio de red cuya conexión a la WAN se limite al ancho de banda, describa la capacidad de ancho de banda de la conexión WAN y los límites de ancho de banda que se han establecido para el tráfico multimedia de Lync Server, si procede.</span><span class="sxs-lookup"><span data-stu-id="eb243-111">For each network site whose connection to the WAN is bandwidth-constrained, describe the bandwidth capacity of the WAN connection and the bandwidth limits that to the network administrator has set for Lync Server media traffic, if applicable.</span></span> <span data-ttu-id="eb243-112">No necesitas incluir sitios cuya conexión a la red WAN no tiene ancho de banda restringido.</span><span class="sxs-lookup"><span data-stu-id="eb243-112">You do not need to include sites whose connection to the WAN is not bandwidth-constrained.</span></span>

5.  <span data-ttu-id="eb243-113">Asocia cada subred de la red a un sitio de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-113">Associate each subnet in your network with a network site.</span></span>

6.  <span data-ttu-id="eb243-114">Asigna los vínculos entre las regiones de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-114">Map the links between the network regions.</span></span> <span data-ttu-id="eb243-115">Para cada vínculo, describa su capacidad de ancho de banda y los límites que el administrador de la red haya colocado en el tráfico multimedia de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="eb243-115">For each link, describe its bandwidth capacity and any limits that the network administrator has placed on Lync Server media traffic.</span></span>

7.  <span data-ttu-id="eb243-116">Define una ruta entre cada par de regiones de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-116">Define a route between every pair of network regions.</span></span>

<div>

## <a name="gather-the-required-information"></a><span data-ttu-id="eb243-117">Recopilar la información necesaria</span><span class="sxs-lookup"><span data-stu-id="eb243-117">Gather the Required Information</span></span>

<span data-ttu-id="eb243-118">Para preparar el servicio de control de admisión de llamadas, recopila la información descrita en los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="eb243-118">To prepare for call admission control, gather the information described in the following steps:</span></span>

1.  <span data-ttu-id="eb243-p104">Identifica las regiones de red. Una región de red representa una red troncal de red o un concentrador de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-p104">Identify your network regions. A network region represents a network backbone or a network hub.</span></span>
    
    <span data-ttu-id="eb243-p105">Una red troncal de red o un concentrador de red forma parte de una infraestructura de red informática que interconecta diversas partes de red, que proporciona una ruta de acceso para el intercambio de información entre distintas redes LAN o subredes. Una red troncal puede asociar diversas redes, desde una ubicación pequeña a una amplia zona geográfica. La capacidad de la red troncal suele ser mayor que la de las redes conectadas a ella.</span><span class="sxs-lookup"><span data-stu-id="eb243-p105">A network backbone or a network hub is a part of computer network infrastructure that interconnects various pieces of network, providing a path for the exchange of information between different LANs or subnets. A backbone can tie together diverse networks, from a small location to a wide geographic area. The backbone's capacity is typically greater than that of the networks connected to it.</span></span>
    
    <span data-ttu-id="eb243-p106">Nuestra topología de ejemplo tiene tres regiones de red: Norteamérica, EMEA y APAC. Una región de red incluye una colección de sitios de red. Trabaja con el administrador de la red para definir las regiones de red de tu empresa.</span><span class="sxs-lookup"><span data-stu-id="eb243-p106">Our example topology has three network regions: North America, EMEA, and APAC. A network region contains a collection of network sites. Work with your network administrator to define the network regions for your enterprise.</span></span>

2.  <span data-ttu-id="eb243-127">Identifica cada sitio central asociado a la región de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-127">Identify each network region’s associated central site.</span></span> <span data-ttu-id="eb243-128">Un sitio central contiene al menos un servidor front-end y es la implementación de Lync Server que administrará CAC para todo el tráfico multimedia que pasa por la conexión WAN de la región de la red.</span><span class="sxs-lookup"><span data-stu-id="eb243-128">A central site contains at least one Front End Server and is the Lync Server deployment that will manage CAC for all media traffic that passes through the network region’s WAN connection.</span></span>
    
    <span data-ttu-id="eb243-129">**Una red de empresa de ejemplo dividida en tres regiones de red**</span><span class="sxs-lookup"><span data-stu-id="eb243-129">**An example enterprise network divided into three network regions**</span></span>
    
    <span data-ttu-id="eb243-130">![Ejemplo de topología de red con 3 regiones de red](images/Gg425827.08937347-250f-488f-ba5f-c256e6afcd8b(OCS.15).jpg "Ejemplo de topología de red con 3 regiones de red")</span><span class="sxs-lookup"><span data-stu-id="eb243-130">![Network Topology Example with 3 Network Regions](images/Gg425827.08937347-250f-488f-ba5f-c256e6afcd8b(OCS.15).jpg "Network Topology Example with 3 Network Regions")</span></span>  
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="eb243-131">Una red de conmutación de etiquetas multiprotocolo (MPLS) necesita representarse como una región de red en la que cada ubicación geográfica tiene un sitio de red correspondiente.</span><span class="sxs-lookup"><span data-stu-id="eb243-131">A Multiprotocol Label Switching (MPLS) network should be represented as a network region in which each geographic location has a corresponding network site.</span></span> <span data-ttu-id="eb243-132">Para obtener más información, consulte el tema "<A href="lync-server-2013-call-admission-control-on-an-mpls-network.md">control de admisión de llamadas en una red MPLS con Lync Server 2013</A>" en la documentación de planificación.</span><span class="sxs-lookup"><span data-stu-id="eb243-132">For details, see the “<A href="lync-server-2013-call-admission-control-on-an-mpls-network.md">Call admission control on an MPLS network with Lync Server 2013</A>” topic in the Planning documentation.</span></span>

    
    </div>
    
    <span data-ttu-id="eb243-133">En el ejemplo anterior, hay tres regiones de red, cada una con un sitio central de Lync Server que administra CAC.</span><span class="sxs-lookup"><span data-stu-id="eb243-133">In the preceding example network topology, there are three network regions, each with a Lync Server central site that manages CAC.</span></span> <span data-ttu-id="eb243-134">El sitio central adecuado para una región de red se elige por la proximidad geográfica.</span><span class="sxs-lookup"><span data-stu-id="eb243-134">The appropriate central site for a network region is chosen by the geographic vicinity.</span></span> <span data-ttu-id="eb243-135">Como el tráfico de medios será mayor dentro de las regiones de red, la propiedad por proximidad geográfica lo hace independiente y seguirá siendo funcional aunque otros sitios centrales dejen de estar disponibles.</span><span class="sxs-lookup"><span data-stu-id="eb243-135">Because media traffic will be heaviest within network regions, the ownership by geographic vicinity makes it self-contained and will continue to be functional even if other central sites become unavailable.</span></span>
    
    <span data-ttu-id="eb243-136">En este ejemplo, una implementación de Lync Server llamada Chicago es el sitio central de la región de Norteamérica.</span><span class="sxs-lookup"><span data-stu-id="eb243-136">In this example, a Lync Server deployment named Chicago is the central site for the North America region.</span></span>
    
    <span data-ttu-id="eb243-137">Todos los usuarios de Lync de América del norte están alojados en servidores de la implementación de Chicago.</span><span class="sxs-lookup"><span data-stu-id="eb243-137">All Lync users in North America are homed on servers in the Chicago deployment.</span></span> <span data-ttu-id="eb243-138">En la tabla siguiente se muestran los sitios centrales de las tres regiones de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-138">The following table shows central sites for all three network regions.</span></span>
    
    ### <a name="network-regions-and-their-associated-central-sites"></a><span data-ttu-id="eb243-139">Regiones de red y sus sitios centrales asociados</span><span class="sxs-lookup"><span data-stu-id="eb243-139">Network Regions and their Associated Central Sites</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="eb243-140">Región de red</span><span class="sxs-lookup"><span data-stu-id="eb243-140">Network Region</span></span></th>
    <th><span data-ttu-id="eb243-141">Sitio central</span><span class="sxs-lookup"><span data-stu-id="eb243-141">Central Site</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-142">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-142">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-143">Chicago</span><span class="sxs-lookup"><span data-stu-id="eb243-143">Chicago</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="eb243-144">EMEA</span><span class="sxs-lookup"><span data-stu-id="eb243-144">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="eb243-145">Londres</span><span class="sxs-lookup"><span data-stu-id="eb243-145">London</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-146">APAC</span><span class="sxs-lookup"><span data-stu-id="eb243-146">APAC</span></span></p></td>
    <td><p><span data-ttu-id="eb243-147">Pekín</span><span class="sxs-lookup"><span data-stu-id="eb243-147">Beijing</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="eb243-148">Dependiendo de su topología de Lync Server, se puede asignar el mismo sitio central a varias regiones de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-148">Depending on your Lync Server topology, the same central site can be assigned to multiple network regions.</span></span>

    
    </div>

3.  <span data-ttu-id="eb243-p111">En cada región de red, identifica todos los sitios de red (oficinas o ubicaciones) cuyas conexiones WAN no tienen ancho de banda restringido. Como estos sitios no tienen ancho de banda restringido, no necesitas aplicarles directivas de ancho de banda de CAC.</span><span class="sxs-lookup"><span data-stu-id="eb243-p111">For each network region, identify all of the network sites (offices or locations) whose WAN connections are not bandwidth-constrained. Because these sites are not bandwidth constrained, you do not need to apply CAC bandwidth policies to them.</span></span>
    
    <span data-ttu-id="eb243-151">En el ejemplo que se muestra en la siguiente tabla, tres sitios de red no tienen vínculos WAN de ancho de banda restringido: Nueva York, Chicago y Detroit.</span><span class="sxs-lookup"><span data-stu-id="eb243-151">In the example shown in the following table, three network sites do not have bandwidth-constrained WAN links: New York, Chicago, and Detroit.</span></span>
    
    ### <a name="network-sites-not-constrained-by-wan-bandwidth"></a><span data-ttu-id="eb243-152">Sitios de red no restringidos por el ancho de banda de WAN</span><span class="sxs-lookup"><span data-stu-id="eb243-152">Network Sites not Constrained by WAN Bandwidth</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="eb243-153">Sitio de red</span><span class="sxs-lookup"><span data-stu-id="eb243-153">Network Site</span></span></th>
    <th><span data-ttu-id="eb243-154">Región de red</span><span class="sxs-lookup"><span data-stu-id="eb243-154">Network Region</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-155">Nueva York</span><span class="sxs-lookup"><span data-stu-id="eb243-155">New York</span></span></p></td>
    <td><p><span data-ttu-id="eb243-156">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-156">North America</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="eb243-157">Chicago</span><span class="sxs-lookup"><span data-stu-id="eb243-157">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="eb243-158">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-158">North America</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-159">Detroit</span><span class="sxs-lookup"><span data-stu-id="eb243-159">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="eb243-160">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-160">North America</span></span></p></td>
    </tr>
    </tbody>
    </table>


4.  <span data-ttu-id="eb243-161">En cada región de red, identifica todos los sitios de red que se conectan a la región de red a través de vínculos WAN de ancho de banda restringido.</span><span class="sxs-lookup"><span data-stu-id="eb243-161">For each network region, identify all of the network sites that connect to the network region through bandwidth-constrained WAN links.</span></span>
    
    <span data-ttu-id="eb243-162">Para asegurar la calidad de audio y vídeo, recomendamos que estos sitios de red de ancho de banda restringido tengan las redes WAN supervisadas y directivas de ancho de banda del CAC que limiten el flujo del tráfico de medios (voz o vídeo) hacia la región de red y desde ella.</span><span class="sxs-lookup"><span data-stu-id="eb243-162">To help ensure audio and video quality, we recommend that these bandwidth-constrained network sites have their WANs monitored and CAC bandwidth policies that limit media (voice or video) traffic flow to and from the network region.</span></span>
    
    <span data-ttu-id="eb243-163">En el ejemplo que se muestra en la siguiente tabla, hay tres sitios de red que están restringidos por el ancho de banda de WAN: Portland, Reno y Albuquerque.</span><span class="sxs-lookup"><span data-stu-id="eb243-163">In the example shown in the following table, there are three network sites that are constrained by WAN bandwidth: Portland, Reno and Albuquerque.</span></span>
    
    ### <a name="network-sites-constrained-by-wan-bandwidth"></a><span data-ttu-id="eb243-164">Sitios de red restringidos por el ancho de banda de WAN</span><span class="sxs-lookup"><span data-stu-id="eb243-164">Network Sites Constrained by WAN Bandwidth</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="eb243-165">Sitio de red</span><span class="sxs-lookup"><span data-stu-id="eb243-165">Network Site</span></span></th>
    <th><span data-ttu-id="eb243-166">Región de red</span><span class="sxs-lookup"><span data-stu-id="eb243-166">Network Region</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-167">Albuquerque</span><span class="sxs-lookup"><span data-stu-id="eb243-167">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="eb243-168">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-168">North America</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="eb243-169">Reno</span><span class="sxs-lookup"><span data-stu-id="eb243-169">Reno</span></span></p></td>
    <td><p><span data-ttu-id="eb243-170">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-170">North America</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-171">Portland</span><span class="sxs-lookup"><span data-stu-id="eb243-171">Portland</span></span></p></td>
    <td><p><span data-ttu-id="eb243-172">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-172">North America</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="eb243-173">**Región de red para CAC Norteamérica con tres sitios de red que no están restringidos por el ancho de banda (Chicago, Nueva York y Detroit) y tres sitios de red que están restringidos por el ancho de banda de WAN (Portland, Reno y Albuquerque)**</span><span class="sxs-lookup"><span data-stu-id="eb243-173">**CAC network region North America with three network sites that are unconstrained by bandwidth (Chicago, New York, and Detroit) and three network sites that are constrained by WAN bandwidth (Portland, Reno, and Albuquerque)**</span></span>
    
    <span data-ttu-id="eb243-174">![Ejemplo de sitios de la red restringidos por el ancho de banda de la WAN](images/Gg425827.d9d1f231-db4d-4dd7-8fbc-eb0b6d1e705d(OCS.15).jpg "Ejemplo de sitios de la red restringidos por el ancho de banda de la WAN")</span><span class="sxs-lookup"><span data-stu-id="eb243-174">![Example network sites constrained by WAN bandwidth](images/Gg425827.d9d1f231-db4d-4dd7-8fbc-eb0b6d1e705d(OCS.15).jpg "Example network sites constrained by WAN bandwidth")</span></span>  

5.  <span data-ttu-id="eb243-175">Para cada vínculo WAN de ancho de banda restringido, determina lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="eb243-175">For each bandwidth-constrained WAN link, determine the following:</span></span>
    
      - <span data-ttu-id="eb243-176">Límite general de ancho de banda que deseas establecer para todas las sesiones simultáneas de audio.</span><span class="sxs-lookup"><span data-stu-id="eb243-176">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="eb243-177">Si una nueva sesión de audio hace que se supere este límite, Lync Server no permite que se inicie la sesión.</span><span class="sxs-lookup"><span data-stu-id="eb243-177">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="eb243-p113">Límite de ancho de banda que deseas establecer para cada sesión individual de audio. El límite predeterminado de ancho de banda para CAC es de 175 kbps, pero el administrador puede modificarlo.</span><span class="sxs-lookup"><span data-stu-id="eb243-p113">Bandwidth limit that you want to set for each individual audio session. The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="eb243-180">Límite general de ancho de banda que deseas establecer para todas las sesiones simultáneas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="eb243-180">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="eb243-181">Si una nueva sesión de video hace que se supere este límite, Lync Server no permite que se inicie la sesión.</span><span class="sxs-lookup"><span data-stu-id="eb243-181">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="eb243-p115">Límite de ancho de banda que deseas establecer para cada sesión individual de vídeo. El límite predeterminado de ancho de banda para CAC es de 700 kbps, pero el administrador puede modificarlo.</span><span class="sxs-lookup"><span data-stu-id="eb243-p115">Bandwidth limit that you want to set for each individual video session. The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    ### <a name="network-sites-with-wan-bandwidth-constraint-information-bandwidth-in-kbps"></a><span data-ttu-id="eb243-184">Sitios de red con información de restricción de ancho de banda de WAN (ancho de banda en kbps)</span><span class="sxs-lookup"><span data-stu-id="eb243-184">Network Sites with WAN Bandwidth Constraint Information (Bandwidth in kbps)</span></span>
    
    <table style="width:100%;">
    <colgroup>
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="eb243-185">Sitio de red</span><span class="sxs-lookup"><span data-stu-id="eb243-185">Network Site</span></span></th>
    <th><span data-ttu-id="eb243-186">Región de red</span><span class="sxs-lookup"><span data-stu-id="eb243-186">Network Region</span></span></th>
    <th><span data-ttu-id="eb243-187">Límite de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="eb243-187">BW Limit</span></span></th>
    <th><span data-ttu-id="eb243-188">Límite de audio</span><span class="sxs-lookup"><span data-stu-id="eb243-188">Audio Limit</span></span></th>
    <th><span data-ttu-id="eb243-189">Límite de sesión de audio</span><span class="sxs-lookup"><span data-stu-id="eb243-189">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="eb243-190">Límite de vídeo</span><span class="sxs-lookup"><span data-stu-id="eb243-190">Video Limit</span></span></th>
    <th><span data-ttu-id="eb243-191">Límite de sesión de vídeo</span><span class="sxs-lookup"><span data-stu-id="eb243-191">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-192">Albuquerque</span><span class="sxs-lookup"><span data-stu-id="eb243-192">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="eb243-193">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-193">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-194">5 000</span><span class="sxs-lookup"><span data-stu-id="eb243-194">5,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-195">2.000</span><span class="sxs-lookup"><span data-stu-id="eb243-195">2,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-196">175</span><span class="sxs-lookup"><span data-stu-id="eb243-196">175</span></span></p></td>
    <td><p><span data-ttu-id="eb243-197">1.400</span><span class="sxs-lookup"><span data-stu-id="eb243-197">1,400</span></span></p></td>
    <td><p><span data-ttu-id="eb243-198">700</span><span class="sxs-lookup"><span data-stu-id="eb243-198">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="eb243-199">Reno</span><span class="sxs-lookup"><span data-stu-id="eb243-199">Reno</span></span></p></td>
    <td><p><span data-ttu-id="eb243-200">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-200">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-201">10 000</span><span class="sxs-lookup"><span data-stu-id="eb243-201">10,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-202">4.000</span><span class="sxs-lookup"><span data-stu-id="eb243-202">4,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-203">175</span><span class="sxs-lookup"><span data-stu-id="eb243-203">175</span></span></p></td>
    <td><p><span data-ttu-id="eb243-204">2.800</span><span class="sxs-lookup"><span data-stu-id="eb243-204">2,800</span></span></p></td>
    <td><p><span data-ttu-id="eb243-205">700</span><span class="sxs-lookup"><span data-stu-id="eb243-205">700</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-206">Portland</span><span class="sxs-lookup"><span data-stu-id="eb243-206">Portland</span></span></p></td>
    <td><p><span data-ttu-id="eb243-207">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-207">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-208">5 000</span><span class="sxs-lookup"><span data-stu-id="eb243-208">5,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-209">4.000</span><span class="sxs-lookup"><span data-stu-id="eb243-209">4,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-210">175</span><span class="sxs-lookup"><span data-stu-id="eb243-210">175</span></span></p></td>
    <td><p><span data-ttu-id="eb243-211">2.800</span><span class="sxs-lookup"><span data-stu-id="eb243-211">2,800</span></span></p></td>
    <td><p><span data-ttu-id="eb243-212">700</span><span class="sxs-lookup"><span data-stu-id="eb243-212">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="eb243-213">Nueva York</span><span class="sxs-lookup"><span data-stu-id="eb243-213">New York</span></span></p></td>
    <td><p><span data-ttu-id="eb243-214">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-214">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-215">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-215">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-216">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-216">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-217">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-217">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-218">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-218">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-219">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-219">(no limit)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-220">Chicago</span><span class="sxs-lookup"><span data-stu-id="eb243-220">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="eb243-221">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-221">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-222">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-222">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-223">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-223">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-224">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-224">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-225">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-225">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-226">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-226">(no limit)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="eb243-227">Detroit</span><span class="sxs-lookup"><span data-stu-id="eb243-227">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="eb243-228">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-228">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-229">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-229">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-230">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-230">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-231">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-231">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-232">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-232">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-233">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-233">(no limit)</span></span></p></td>
    </tr>
    </tbody>
    </table>


6.  <span data-ttu-id="eb243-234">Para cada subred de la red, especifica el sitio de red asociado.</span><span class="sxs-lookup"><span data-stu-id="eb243-234">For every subnet in your network, specify its associated network site.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="eb243-p116">Cada subred de la red necesita estar asociada a un sitio de red, aunque el sitio de red no esté restringido por el ancho de banda. Esto es porque el servicio de control de admisión de llamadas usa la información de la subred para determinar el sitio de red en que está situado un extremo. Cuando se determinan las ubicaciones de ambas partes de la sesión, el servicio de control de admisión de llamadas puede determinar si existe suficiente ancho de banda para establecer una llamada. Cuando se establece una sesión a través de un vínculo que no tiene límites de ancho de banda, se genera una alerta.</span><span class="sxs-lookup"><span data-stu-id="eb243-p116">Every subnet in your network must be associated with a network site, even if the network site is not bandwidth constrained. This is because call admission control uses subnet information to determine at which network site an endpoint is located. When the locations of both parties in the session are determined, call admission control can determine if there is sufficient bandwidth to establish a call. When a session is established over a link that has no bandwidth limits, an alert is generated.</span></span><BR><span data-ttu-id="eb243-239">Si implementas servidores perimetrales de audio o vídeo, las direcciones IP públicas de cada servidor perimetral necesitan estar asociadas al sitio de red en el que se implementa el servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="eb243-239">If you deploy Audio/Video Edge Servers, the public IP addresses of each Edge Server must be associated with the network site where the Edge Server is deployed.</span></span> <span data-ttu-id="eb243-240">Cada dirección IP pública del servidor perimetral A/V necesita agregarse a las opciones de configuración de la red como subred con una máscara de subred de 32.</span><span class="sxs-lookup"><span data-stu-id="eb243-240">Each public IP address of the A/V Edge Server must be added to your network configuration settings as a subnet with a subnet mask of 32.</span></span> <span data-ttu-id="eb243-241">Por ejemplo, si implementas servidores perimetrales A/V en Chicago, para cada dirección IP externa de los servidores, crea una subred con una máscara de subred de 32 y asocia el sitio de red Chicago a dichas subredes.</span><span class="sxs-lookup"><span data-stu-id="eb243-241">For example, if you deploy A/V Edge Servers in Chicago, then for each external IP address of those servers create a subnet with a subnet mask of 32 and associate network site Chicago with those subnets.</span></span> <span data-ttu-id="eb243-242">Para obtener detalles sobre las direcciones IP públicas, consulte <A href="lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md">determinar el firewall externo a/V y los requisitos de puerto para Lync Server 2013</A> en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="eb243-242">For details about public IP addresses, see <A href="lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md">Determine external A/V firewall and port requirements for Lync Server 2013</A> in the Planning documentation.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="eb243-p118">Aparecerá una alerta de indicador de estado clave (KHI), que especifica una lista de direcciones IP que están incluidas en la red, pero que no están asociadas a una subred; o bien, la subred que incluye las direcciones IP no está asociada a un sitio de red. Esta alerta no aparecerá más que una vez en un período de 8 horas. A continuación se ofrece la información sobre las alertas relevante y un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="eb243-p118">A Key Health Indicator (KHI) alert is raised, specifying a list of IP addresses that are present in your network but are either not associated with a subnet, or the subnet that includes the IP addresses is not associated with a network site. This alert will not be raised more than once within an 8 hour period. The relevant alert information and an example are as follows:</span></span><BR><span data-ttu-id="eb243-246"><STRONG>Fuente:</STRONG> Servicio de directivas de ancho de banda CS (núcleo)</span><span class="sxs-lookup"><span data-stu-id="eb243-246"><STRONG>Source:</STRONG> CS Bandwidth Policy Service (Core)</span></span><BR><span data-ttu-id="eb243-247"><STRONG>Número de evento:</STRONG> 36034</span><span class="sxs-lookup"><span data-stu-id="eb243-247"><STRONG>Event number:</STRONG> 36034</span></span><BR><span data-ttu-id="eb243-248"><STRONG>Nivel:</STRONG> 2</span><span class="sxs-lookup"><span data-stu-id="eb243-248"><STRONG>Level:</STRONG> 2</span></span><BR><span data-ttu-id="eb243-249"><STRONG>Descripción:</STRONG> Las subredes de las siguientes direcciones IP: &lt; la lista de direcciones IP &gt; no está configurada o las subredes no están asociadas a un sitio de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-249"><STRONG>Description:</STRONG> The subnets for the following IP Addresses: &lt;List of IP Addresses&gt; are either not configured or the subnets are not associated to a network site.</span></span><BR><span data-ttu-id="eb243-250"><STRONG>Causa:</STRONG> Las subredes de las direcciones IP correspondientes no se encuentran en la configuración de red o las subredes no están asociadas a un sitio de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-250"><STRONG>Cause:</STRONG> The subnets for the corresponding IP addresses are missing from the network configuration settings or the subnets are not associated to a network site.</span></span><BR><span data-ttu-id="eb243-251"><STRONG>Solución:</STRONG> Agregue subredes que correspondan a la lista anterior de direcciones IP en la configuración de red y asocie cada subred a un sitio de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-251"><STRONG>Resolution:</STRONG> Add subnets corresponding to the preceding list of IP addresses into the network configuration settings and associate every subnet to a network site.</span></span><BR><span data-ttu-id="eb243-p119">Por ejemplo, si la lista de direcciones IP de la alerta especifica 10.121.248.226 y 10.121.249.20, estas direcciones IP no están asociadas a una subred o la subred a la que están asociadas no pertenece a un sitio de red. Si 10.121.248.0/24 y 10.121.249.0/24 son las subredes correspondientes a estas direcciones, este problema se puede resolver de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="eb243-p119">For example, if the IP address list in the alert specifies 10.121.248.226 and 10.121.249.20, either these IP addresses are not associated with a subnet, or the subnet that they are associated with does not belong to a network site. If 10.121.248.0/24 and 10.121.249.0/24 are the corresponding subnets for these addresses, you can resolve this issue as follows:</span></span> 
    > <OL>
    > <LI>
    > <P><span data-ttu-id="eb243-254">Asegúrate de que la dirección IP 10.121.248.226 esté asociada a la subred 10.121.248.0/24 y la dirección IP 10.121.249.20 esté asociada a la subred 10.121.249.0/24.</span><span class="sxs-lookup"><span data-stu-id="eb243-254">Be sure that IP address 10.121.248.226 is associated with the 10.121.248.0/24 subnet and IP address 10.121.249.20 is associated with the 10.121.249.0/24 subnet.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="eb243-255">Asegúrate de que cada una de las subredes 10.121.248.0/24 y 10.121.249.0/24 esté asociada a un sitio de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-255">Be sure that the 10.121.248.0/24 and 10.121.249.0/24 subnets are each associated with a network site.</span></span></P></LI></OL>

    
    </div>
    
    ### <a name="network-sites-and-associated-subnets-bandwidth-in-kbps"></a><span data-ttu-id="eb243-256">Sitios de red y subredes asociadas (ancho de banda en kbps)</span><span class="sxs-lookup"><span data-stu-id="eb243-256">Network Sites and Associated Subnets (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="eb243-257">Sitio de red</span><span class="sxs-lookup"><span data-stu-id="eb243-257">Network Site</span></span></th>
    <th><span data-ttu-id="eb243-258">Región de red</span><span class="sxs-lookup"><span data-stu-id="eb243-258">Network Region</span></span></th>
    <th><span data-ttu-id="eb243-259">Límite de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="eb243-259">BW Limit</span></span></th>
    <th><span data-ttu-id="eb243-260">Límite de audio</span><span class="sxs-lookup"><span data-stu-id="eb243-260">Audio Limit</span></span></th>
    <th><span data-ttu-id="eb243-261">Límite de sesión de audio</span><span class="sxs-lookup"><span data-stu-id="eb243-261">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="eb243-262">Límite de vídeo</span><span class="sxs-lookup"><span data-stu-id="eb243-262">Video Limit</span></span></th>
    <th><span data-ttu-id="eb243-263">Límite de sesión de vídeo</span><span class="sxs-lookup"><span data-stu-id="eb243-263">Video Session Limit</span></span></th>
    <th><span data-ttu-id="eb243-264">Subredes</span><span class="sxs-lookup"><span data-stu-id="eb243-264">Subnets</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-265">Albuquerque</span><span class="sxs-lookup"><span data-stu-id="eb243-265">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="eb243-266">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-266">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-267">5 000</span><span class="sxs-lookup"><span data-stu-id="eb243-267">5,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-268">2.000</span><span class="sxs-lookup"><span data-stu-id="eb243-268">2,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-269">175</span><span class="sxs-lookup"><span data-stu-id="eb243-269">175</span></span></p></td>
    <td><p><span data-ttu-id="eb243-270">1.400</span><span class="sxs-lookup"><span data-stu-id="eb243-270">1,400</span></span></p></td>
    <td><p><span data-ttu-id="eb243-271">700</span><span class="sxs-lookup"><span data-stu-id="eb243-271">700</span></span></p></td>
    <td><p><span data-ttu-id="eb243-272">172.29.79.0/23, 157.57.215.0/25, 172.29.90.0/23, 172.29.80.0/24</span><span class="sxs-lookup"><span data-stu-id="eb243-272">172.29.79.0/23, 157.57.215.0/25, 172.29.90.0/23, 172.29.80.0/24</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="eb243-273">Reno</span><span class="sxs-lookup"><span data-stu-id="eb243-273">Reno</span></span></p></td>
    <td><p><span data-ttu-id="eb243-274">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-274">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-275">10 000</span><span class="sxs-lookup"><span data-stu-id="eb243-275">10,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-276">4.000</span><span class="sxs-lookup"><span data-stu-id="eb243-276">4,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-277">175</span><span class="sxs-lookup"><span data-stu-id="eb243-277">175</span></span></p></td>
    <td><p><span data-ttu-id="eb243-278">2.800</span><span class="sxs-lookup"><span data-stu-id="eb243-278">2,800</span></span></p></td>
    <td><p><span data-ttu-id="eb243-279">700</span><span class="sxs-lookup"><span data-stu-id="eb243-279">700</span></span></p></td>
    <td><p><span data-ttu-id="eb243-280">157.57.210.0/23, 172.28.151.128/25</span><span class="sxs-lookup"><span data-stu-id="eb243-280">157.57.210.0/23, 172.28.151.128/25</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-281">Portland</span><span class="sxs-lookup"><span data-stu-id="eb243-281">Portland</span></span></p></td>
    <td><p><span data-ttu-id="eb243-282">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-282">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-283">5 000</span><span class="sxs-lookup"><span data-stu-id="eb243-283">5,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-284">4.000</span><span class="sxs-lookup"><span data-stu-id="eb243-284">4,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-285">175</span><span class="sxs-lookup"><span data-stu-id="eb243-285">175</span></span></p></td>
    <td><p><span data-ttu-id="eb243-286">2.800</span><span class="sxs-lookup"><span data-stu-id="eb243-286">2,800</span></span></p></td>
    <td><p><span data-ttu-id="eb243-287">700</span><span class="sxs-lookup"><span data-stu-id="eb243-287">700</span></span></p></td>
    <td><p><span data-ttu-id="eb243-288">172.29.77.0/24 10.71.108.0/24, 157.57.208.0/23</span><span class="sxs-lookup"><span data-stu-id="eb243-288">172.29.77.0/24 10.71.108.0/24, 157.57.208.0/23</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="eb243-289">Nueva York</span><span class="sxs-lookup"><span data-stu-id="eb243-289">New York</span></span></p></td>
    <td><p><span data-ttu-id="eb243-290">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-290">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-291">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-291">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-292">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-292">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-293">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-293">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-294">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-294">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-295">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-295">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-296">172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24</span><span class="sxs-lookup"><span data-stu-id="eb243-296">172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-297">Chicago</span><span class="sxs-lookup"><span data-stu-id="eb243-297">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="eb243-298">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-298">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-299">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-299">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-300">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-300">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-301">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-301">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-302">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-302">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-303">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-303">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-304">157.57.211.0/23, 172.28.152.128/25</span><span class="sxs-lookup"><span data-stu-id="eb243-304">157.57.211.0/23, 172.28.152.128/25</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="eb243-305">Detroit</span><span class="sxs-lookup"><span data-stu-id="eb243-305">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="eb243-306">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-306">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-307">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-307">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-308">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-308">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-309">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-309">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-310">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-310">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-311">(sin límite)</span><span class="sxs-lookup"><span data-stu-id="eb243-311">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="eb243-312">172.29.78.0/24 10.71.109.0/24, 157.57.209.0/23</span><span class="sxs-lookup"><span data-stu-id="eb243-312">172.29.78.0/24 10.71.109.0/24, 157.57.209.0/23</span></span></p></td>
    </tr>
    </tbody>
    </table>


7.  <span data-ttu-id="eb243-313">En el control de admisión de las llamadas de Lync Server, las conexiones entre regiones de red se denominan *vínculos de región*.</span><span class="sxs-lookup"><span data-stu-id="eb243-313">In Lync Server call admission control, the connections between network regions are called *region links*.</span></span> <span data-ttu-id="eb243-314">Para cada vínculo de región, determina lo siguiente, tal como has hecho para los sitios de red:</span><span class="sxs-lookup"><span data-stu-id="eb243-314">For each region link, determine the following, just as you did for the network sites:</span></span>
    
      - <span data-ttu-id="eb243-315">Límite general de ancho de banda que deseas establecer para todas las sesiones simultáneas de audio.</span><span class="sxs-lookup"><span data-stu-id="eb243-315">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="eb243-316">Si una nueva sesión de audio hace que se supere este límite, Lync Server no permite que se inicie la sesión.</span><span class="sxs-lookup"><span data-stu-id="eb243-316">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="eb243-p122">Límite de ancho de banda que deseas establecer para cada sesión individual de audio. El límite predeterminado de ancho de banda para CAC es de 175 kbps, pero el administrador puede modificarlo.</span><span class="sxs-lookup"><span data-stu-id="eb243-p122">Bandwidth limit that you want to set for each individual audio session. The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="eb243-319">Límite general de ancho de banda que deseas establecer para todas las sesiones simultáneas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="eb243-319">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="eb243-320">Si una nueva sesión de video hace que se supere este límite, Lync Server no permite que se inicie la sesión.</span><span class="sxs-lookup"><span data-stu-id="eb243-320">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="eb243-p124">Límite de ancho de banda que deseas establecer para cada sesión individual de vídeo. El límite predeterminado de ancho de banda para CAC es de 700 kbps, pero el administrador puede modificarlo.</span><span class="sxs-lookup"><span data-stu-id="eb243-p124">Bandwidth limit that you want to set for each individual video session. The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    <span data-ttu-id="eb243-323">**Vínculos de región de red con límites de ancho de banda asociados**</span><span class="sxs-lookup"><span data-stu-id="eb243-323">**Network Region links with associated bandwidth limits**</span></span>
    
    <span data-ttu-id="eb243-324">![Ejemplo de limitaciones entre 3 regiones](images/Gg425827.25259afa-ee7c-4d26-bc41-92ba9cb56dec(OCS.15).jpg "Ejemplo de limitaciones entre 3 regiones")</span><span class="sxs-lookup"><span data-stu-id="eb243-324">![Example of Limitations between 3 Regions](images/Gg425827.25259afa-ee7c-4d26-bc41-92ba9cb56dec(OCS.15).jpg "Example of Limitations between 3 Regions")</span></span>  
    
    ### <a name="region-link-bandwidth-information-bandwidth-in-kbps"></a><span data-ttu-id="eb243-325">Información de ancho de banda de vínculos de región (ancho de banda en kbps)</span><span class="sxs-lookup"><span data-stu-id="eb243-325">Region Link Bandwidth Information (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="eb243-326">Nombre del vínculo de región</span><span class="sxs-lookup"><span data-stu-id="eb243-326">Region Link Name</span></span></th>
    <th><span data-ttu-id="eb243-327">Primera región</span><span class="sxs-lookup"><span data-stu-id="eb243-327">First Region</span></span></th>
    <th><span data-ttu-id="eb243-328">Segunda región</span><span class="sxs-lookup"><span data-stu-id="eb243-328">Second Region</span></span></th>
    <th><span data-ttu-id="eb243-329">Límite de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="eb243-329">BW Limit</span></span></th>
    <th><span data-ttu-id="eb243-330">Límite de audio</span><span class="sxs-lookup"><span data-stu-id="eb243-330">Audio Limit</span></span></th>
    <th><span data-ttu-id="eb243-331">Límite de sesión de audio</span><span class="sxs-lookup"><span data-stu-id="eb243-331">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="eb243-332">Límite de vídeo</span><span class="sxs-lookup"><span data-stu-id="eb243-332">Video Limit</span></span></th>
    <th><span data-ttu-id="eb243-333">Límite de sesión de vídeo</span><span class="sxs-lookup"><span data-stu-id="eb243-333">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-334">NA-EMEA-LINK</span><span class="sxs-lookup"><span data-stu-id="eb243-334">NA-EMEA-LINK</span></span></p></td>
    <td><p><span data-ttu-id="eb243-335">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-335">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-336">EMEA</span><span class="sxs-lookup"><span data-stu-id="eb243-336">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="eb243-337">50 000</span><span class="sxs-lookup"><span data-stu-id="eb243-337">50,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-338">20 000</span><span class="sxs-lookup"><span data-stu-id="eb243-338">20,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-339">175</span><span class="sxs-lookup"><span data-stu-id="eb243-339">175</span></span></p></td>
    <td><p><span data-ttu-id="eb243-340">14 000</span><span class="sxs-lookup"><span data-stu-id="eb243-340">14,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-341">700</span><span class="sxs-lookup"><span data-stu-id="eb243-341">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="eb243-342">EMEA-APAC-LINK</span><span class="sxs-lookup"><span data-stu-id="eb243-342">EMEA-APAC-LINK</span></span></p></td>
    <td><p><span data-ttu-id="eb243-343">EMEA</span><span class="sxs-lookup"><span data-stu-id="eb243-343">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="eb243-344">APAC</span><span class="sxs-lookup"><span data-stu-id="eb243-344">APAC</span></span></p></td>
    <td><p><span data-ttu-id="eb243-345">25 000</span><span class="sxs-lookup"><span data-stu-id="eb243-345">25,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-346">10 000</span><span class="sxs-lookup"><span data-stu-id="eb243-346">10,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-347">175</span><span class="sxs-lookup"><span data-stu-id="eb243-347">175</span></span></p></td>
    <td><p><span data-ttu-id="eb243-348">7.000</span><span class="sxs-lookup"><span data-stu-id="eb243-348">7,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-349">700</span><span class="sxs-lookup"><span data-stu-id="eb243-349">700</span></span></p></td>
    </tr>
    </tbody>
    </table>


8.  <span data-ttu-id="eb243-350">Define una ruta entre cada par de regiones de red.</span><span class="sxs-lookup"><span data-stu-id="eb243-350">Define a route between every pair of network regions.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="eb243-351">Se requieren dos vínculos para la ruta entre las regiones Norteamérica y APAC porque no existe ningún vínculo de región que las conecte directamente.</span><span class="sxs-lookup"><span data-stu-id="eb243-351">Two links are required for the route between the North America and APAC regions because there is no region link that directly connects them.</span></span>

    
    </div>
    
    ### <a name="region-routes"></a><span data-ttu-id="eb243-352">Rutas de región</span><span class="sxs-lookup"><span data-stu-id="eb243-352">Region Routes</span></span>
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="eb243-353">Nombre de la ruta de región</span><span class="sxs-lookup"><span data-stu-id="eb243-353">Region Route Name</span></span></th>
    <th><span data-ttu-id="eb243-354">Primera región</span><span class="sxs-lookup"><span data-stu-id="eb243-354">First Region</span></span></th>
    <th><span data-ttu-id="eb243-355">Segunda región</span><span class="sxs-lookup"><span data-stu-id="eb243-355">Second Region</span></span></th>
    <th><span data-ttu-id="eb243-356">Vínculos de región</span><span class="sxs-lookup"><span data-stu-id="eb243-356">Region Links</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-357">NA-EMEA-ROUTE</span><span class="sxs-lookup"><span data-stu-id="eb243-357">NA-EMEA-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="eb243-358">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-358">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-359">EMEA</span><span class="sxs-lookup"><span data-stu-id="eb243-359">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="eb243-360">NA-EMEA-LINK</span><span class="sxs-lookup"><span data-stu-id="eb243-360">NA-EMEA-LINK</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="eb243-361">EMEA-APAC-ROUTE</span><span class="sxs-lookup"><span data-stu-id="eb243-361">EMEA-APAC-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="eb243-362">EMEA</span><span class="sxs-lookup"><span data-stu-id="eb243-362">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="eb243-363">APAC</span><span class="sxs-lookup"><span data-stu-id="eb243-363">APAC</span></span></p></td>
    <td><p><span data-ttu-id="eb243-364">EMEA-APAC-LINK</span><span class="sxs-lookup"><span data-stu-id="eb243-364">EMEA-APAC-LINK</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-365">NA-APAC-ROUTE</span><span class="sxs-lookup"><span data-stu-id="eb243-365">NA-APAC-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="eb243-366">Norteamérica</span><span class="sxs-lookup"><span data-stu-id="eb243-366">North America</span></span></p></td>
    <td><p><span data-ttu-id="eb243-367">APAC</span><span class="sxs-lookup"><span data-stu-id="eb243-367">APAC</span></span></p></td>
    <td><p><span data-ttu-id="eb243-368">NA-EMEA-LINK, EMEA-APAC-LINK</span><span class="sxs-lookup"><span data-stu-id="eb243-368">NA-EMEA-LINK, EMEA-APAC-LINK</span></span></p></td>
    </tr>
    </tbody>
    </table>


9.  <span data-ttu-id="eb243-369">Para cada par de sitios de red que estén conectados directamente por un solo vínculo (denominado vínculo *entre sitios*), determina lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="eb243-369">For every pair of network sites that are directly connected by a single link (called an *inter-site* link), determine the following:</span></span>
    
      - <span data-ttu-id="eb243-370">Límite general de ancho de banda que deseas establecer para todas las sesiones simultáneas de audio.</span><span class="sxs-lookup"><span data-stu-id="eb243-370">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="eb243-371">Si una nueva sesión de audio hace que se supere este límite, Lync Server no permite que se inicie la sesión.</span><span class="sxs-lookup"><span data-stu-id="eb243-371">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="eb243-p126">Límite de ancho de banda que deseas establecer para cada sesión individual de audio. El límite predeterminado de ancho de banda para CAC es de 175 kbps, pero el administrador puede modificarlo.</span><span class="sxs-lookup"><span data-stu-id="eb243-p126">Bandwidth limit that you want to set for each individual audio session. The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="eb243-374">Límite general de ancho de banda que deseas establecer para todas las sesiones simultáneas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="eb243-374">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="eb243-375">Si una nueva sesión de video hace que se supere este límite, Lync Server no permite que se inicie la sesión.</span><span class="sxs-lookup"><span data-stu-id="eb243-375">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="eb243-p128">Límite de ancho de banda que deseas establecer para cada sesión individual de vídeo. El límite predeterminado de ancho de banda para CAC es de 700 kbps, pero el administrador puede modificarlo.</span><span class="sxs-lookup"><span data-stu-id="eb243-p128">Bandwidth limit that you want to set for each individual video session. The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    <span data-ttu-id="eb243-378">**Región de red para CAC Norteamérica con indicación de las capacidades de ancho de banda y los límites de ancho de banda del vínculo entre sitios entre Reno y Albuquerque**</span><span class="sxs-lookup"><span data-stu-id="eb243-378">**CAC network region North America showing the bandwidth capacities and bandwidth limits for the inter-site link between Reno and Albuquerque**</span></span>
    
    <span data-ttu-id="eb243-379">![Ejemplo de sitios de la red restringidos por el ancho de banda de la WAN](images/Gg425827.063e5e1d-b6c8-4e8c-98db-c227c78f671d(OCS.15).jpg "Ejemplo de sitios de la red restringidos por el ancho de banda de la WAN")</span><span class="sxs-lookup"><span data-stu-id="eb243-379">![Network Sites Constrained by WAN Bandwidth example](images/Gg425827.063e5e1d-b6c8-4e8c-98db-c227c78f671d(OCS.15).jpg "Network Sites Constrained by WAN Bandwidth example")</span></span>  
    
    ### <a name="bandwidth-information-for-an-inter-site-link-between-two-network-sites-bandwidth-in-kbps"></a><span data-ttu-id="eb243-380">Información de ancho de banda de un vínculo entre sitios entre dos sitios de red (ancho de banda en kbps)</span><span class="sxs-lookup"><span data-stu-id="eb243-380">Bandwidth Information for an Inter-Site Link between Two Network Sites (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="eb243-381">Nombre del vínculo entre sitios</span><span class="sxs-lookup"><span data-stu-id="eb243-381">Inter-Site Link Name</span></span></th>
    <th><span data-ttu-id="eb243-382">Primer sitio</span><span class="sxs-lookup"><span data-stu-id="eb243-382">First Site</span></span></th>
    <th><span data-ttu-id="eb243-383">Segundo sitio</span><span class="sxs-lookup"><span data-stu-id="eb243-383">Second Site</span></span></th>
    <th><span data-ttu-id="eb243-384">Límite de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="eb243-384">BW Limit</span></span></th>
    <th><span data-ttu-id="eb243-385">Límite de audio</span><span class="sxs-lookup"><span data-stu-id="eb243-385">Audio Limit</span></span></th>
    <th><span data-ttu-id="eb243-386">Límite de sesión de audio</span><span class="sxs-lookup"><span data-stu-id="eb243-386">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="eb243-387">Límite de vídeo</span><span class="sxs-lookup"><span data-stu-id="eb243-387">Video Limit</span></span></th>
    <th><span data-ttu-id="eb243-388">Límite de sesión de vídeo</span><span class="sxs-lookup"><span data-stu-id="eb243-388">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="eb243-389">Reno-Albu-Intersite-Link</span><span class="sxs-lookup"><span data-stu-id="eb243-389">Reno-Albu-Intersite-Link</span></span></p></td>
    <td><p><span data-ttu-id="eb243-390">Reno</span><span class="sxs-lookup"><span data-stu-id="eb243-390">Reno</span></span></p></td>
    <td><p><span data-ttu-id="eb243-391">Albuquerque</span><span class="sxs-lookup"><span data-stu-id="eb243-391">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="eb243-392">20 000</span><span class="sxs-lookup"><span data-stu-id="eb243-392">20,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-393">12 000</span><span class="sxs-lookup"><span data-stu-id="eb243-393">12,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-394">175</span><span class="sxs-lookup"><span data-stu-id="eb243-394">175</span></span></p></td>
    <td><p><span data-ttu-id="eb243-395">5 000</span><span class="sxs-lookup"><span data-stu-id="eb243-395">5,000</span></span></p></td>
    <td><p><span data-ttu-id="eb243-396">700</span><span class="sxs-lookup"><span data-stu-id="eb243-396">700</span></span></p></td>
    </tr>
    </tbody>
    </table>


<div>

## <a name="next-steps"></a><span data-ttu-id="eb243-397">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="eb243-397">Next Steps</span></span>

<span data-ttu-id="eb243-398">Una vez recopilada la información necesaria, puede realizar la implementación de CAC mediante el shell de administración de Lync Server o el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="eb243-398">After you have gathered the required information, you can perform CAC deployment either by using the Lync Server Management Shell or Lync Server Control Panel.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="eb243-399">Aunque puede realizar la mayoría de las tareas de configuración de red con el panel de control de Lync Server, para crear subredes y vínculos entre sitios, debe usar el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="eb243-399">Although you can perform most network configuration tasks by using Lync Server Control Panel, to create subnets and intersite links, you must use Lync Server Management Shell.</span></span> <span data-ttu-id="eb243-400">Para obtener más información, vea la documentación del shell de administración de Lync Server para el cmdlet <STRONG>New-CsNetworkSubnet</STRONG> y el cmdlet <STRONG>New-CsNetworkIntersitePolicy</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="eb243-400">For details, see the Lync Server Management Shell documentation for the <STRONG>New-CsNetworkSubnet</STRONG> cmdlet and the <STRONG>New-CsNetworkIntersitePolicy</STRONG> cmdlet.</span></span>



<span data-ttu-id="eb243-401"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb243-401"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

