---
title: 'Lync Server 2013: implementar regiones, sitios y subredes de la red'
description: 'Lync Server 2013: implementar regiones, sitios y subredes de la red.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying network regions, sites, and subnets
ms:assetid: c4b75601-3538-4d07-8d23-1ad90459ae48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994067(v=OCS.15)
ms:contentKeyID: 51803978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1c4c08cd9b78b1439000cdb4a7bbe3ffc2f99d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429849"
---
# <a name="deploying-network-regions-sites-and-subnets-in-lync-server-2013"></a><span data-ttu-id="462a6-103">Implementar regiones, sitios y subredes de la red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="462a6-103">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="462a6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="462a6-104">

<span> </span></span></span>

<span data-ttu-id="462a6-105">_**Última modificación del tema:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="462a6-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="462a6-106">Una vez implementada la voz de la empresa, debe configurar:</span><span class="sxs-lookup"><span data-stu-id="462a6-106">Once Enterprise Voice is deployed, you need to configure:</span></span>

  - <span data-ttu-id="462a6-107">Regiones de red</span><span class="sxs-lookup"><span data-stu-id="462a6-107">Network regions</span></span>

  - <span data-ttu-id="462a6-108">Sitios de red</span><span class="sxs-lookup"><span data-stu-id="462a6-108">Network sites</span></span>

  - <span data-ttu-id="462a6-109">Subredes de red</span><span class="sxs-lookup"><span data-stu-id="462a6-109">Network subnets</span></span>

<div>

## <a name="define-network-regions"></a><span data-ttu-id="462a6-110">Definir regiones de red</span><span class="sxs-lookup"><span data-stu-id="462a6-110">Define Network Regions</span></span>

<span data-ttu-id="462a6-111">Use el comando de Windows PowerShell de Lync Server, New-CsNetworkRegion o panel de control de Lync Server para definir las regiones de red.</span><span class="sxs-lookup"><span data-stu-id="462a6-111">Use the Lync Server Windows PowerShell command, New-CsNetworkRegion, or Lync Server Control Panel to define network regions.</span></span>

    New-CsNetworkRegion -NetworkRegionID <region ID> -CentralSite <site ID>

<span data-ttu-id="462a6-112">Para obtener más información, vea [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span><span class="sxs-lookup"><span data-stu-id="462a6-112">For more information, see [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span></span>

<span data-ttu-id="462a6-113">En este ejemplo, el siguiente comando de Windows PowerShell muestra la región de red, región 1 (India), definida en este escenario.</span><span class="sxs-lookup"><span data-stu-id="462a6-113">For this example, the following Windows PowerShell command illustrates the network region, region 1 (India), defined in this scenario.</span></span>

    New-CsNetworkRegion -NetworkRegionID "India" -CentralSite "India Central Site"

<div>


</div>

</div>

<div>

## <a name="define-network-sites"></a><span data-ttu-id="462a6-114">Definir sitios de red</span><span class="sxs-lookup"><span data-stu-id="462a6-114">Define Network Sites</span></span>

<span data-ttu-id="462a6-115">Use el comando de Windows PowerShell de Lync Server, New-CsNetworkSite o el panel de control de Lync Server para definir sitios de red.</span><span class="sxs-lookup"><span data-stu-id="462a6-115">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, or the Lync Server Control Panel to define network sites.</span></span>

    New-CsNetworkSite -NetworkSiteID <site ID> -NetworkRegionID <region ID>

<span data-ttu-id="462a6-116">Para obtener más información, vea [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span><span class="sxs-lookup"><span data-stu-id="462a6-116">For more information, see [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span></span>

<span data-ttu-id="462a6-117">En este ejemplo, la siguiente tabla y el comando de Windows PowerShell de Lync Server muestran los sitios de red definidos en este escenario.</span><span class="sxs-lookup"><span data-stu-id="462a6-117">For this example, the following table and Lync Server Windows PowerShell command illustrate the network sites defined in this scenario.</span></span> <span data-ttu-id="462a6-118">En la tabla solo se incluyen los valores específicos de Location-Based enrutamiento, con fines de ilustración.</span><span class="sxs-lookup"><span data-stu-id="462a6-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSite -NetworkSiteID "Delhi" -NetworkRegionID "India"
    New-CsNetworkSite -NetworkSiteID "Hyderabad" -NetworkRegionID "India"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="462a6-119">Sitio 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="462a6-119">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="462a6-120">Sitio 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="462a6-120">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="462a6-121">IDENTIFICADOR de sitio</span><span class="sxs-lookup"><span data-stu-id="462a6-121">Site ID</span></span></p></td>
<td><p><span data-ttu-id="462a6-122">Sitio 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="462a6-122">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="462a6-123">Sitio 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="462a6-123">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462a6-124">IDENTIFICADOR de región</span><span class="sxs-lookup"><span data-stu-id="462a6-124">Region ID</span></span></p></td>
<td><p><span data-ttu-id="462a6-125">Región 1 (India)</span><span class="sxs-lookup"><span data-stu-id="462a6-125">Region 1 (India)</span></span></p></td>
<td><p><span data-ttu-id="462a6-126">Región 1 (India)</span><span class="sxs-lookup"><span data-stu-id="462a6-126">Region 1 (India)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-network-subnets"></a><span data-ttu-id="462a6-127">Definir subredes de red</span><span class="sxs-lookup"><span data-stu-id="462a6-127">Define Network Subnets</span></span>

<span data-ttu-id="462a6-128">Use el comando de Windows PowerShell de Lync Server, New-CsNetworkSubnet o el panel de control de Lync Server para definir subredes de red y asignarlas a sitios de red.</span><span class="sxs-lookup"><span data-stu-id="462a6-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSubnet, or the Lync Server Control Panel to define network subnets and assign them to network sites.</span></span>

    New-CsNetworkSubnet -SubnetID <Subnet IP address> -MaskBits <Subnet bitmask> -NetworkSiteID <site ID>

<span data-ttu-id="462a6-129">Para obtener más información, vea [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="462a6-129">For more information, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<span data-ttu-id="462a6-130">En este ejemplo, los siguientes comandos de tabla y Windows PowerShell ilustran la asignación de subredes de red a los sitios de red, Delhi y Hyderabad, definidas en este escenario.</span><span class="sxs-lookup"><span data-stu-id="462a6-130">For this example, the following table and Windows PowerShell commands illustrate the assignment of network subnets to the network sites, Delhi and Hyderabad, defined in this scenario.</span></span> <span data-ttu-id="462a6-131">En la tabla solo se incluyen los valores específicos de Location-Based enrutamiento, con fines de ilustración.</span><span class="sxs-lookup"><span data-stu-id="462a6-131">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSubnet -SubnetID "192.168.0.0" -MaskBits "24" -NetworkSiteID "Delhi"
    New-CsNetworkSubnet -SubnetID "192.168.1.0" -MaskBits "24" -NetworkSiteID "Hyderabad"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="462a6-132">Sitio 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="462a6-132">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="462a6-133">Sitio 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="462a6-133">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="462a6-134">IDENTIFICADOR de subred</span><span class="sxs-lookup"><span data-stu-id="462a6-134">Subnet ID</span></span></p></td>
<td><p><span data-ttu-id="462a6-135">192.168.0.0</span><span class="sxs-lookup"><span data-stu-id="462a6-135">192.168.0.0</span></span></p></td>
<td><p><span data-ttu-id="462a6-136">192.168.1.0</span><span class="sxs-lookup"><span data-stu-id="462a6-136">192.168.1.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462a6-137">Sin</span><span class="sxs-lookup"><span data-stu-id="462a6-137">Mask</span></span></p></td>
<td><p><span data-ttu-id="462a6-138">veinticuatro</span><span class="sxs-lookup"><span data-stu-id="462a6-138">24</span></span></p></td>
<td><p><span data-ttu-id="462a6-139">veinticuatro</span><span class="sxs-lookup"><span data-stu-id="462a6-139">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462a6-140">IDENTIFICADOR de sitio</span><span class="sxs-lookup"><span data-stu-id="462a6-140">Site ID</span></span></p></td>
<td><p><span data-ttu-id="462a6-141">Sitio 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="462a6-141">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="462a6-142">Sitio 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="462a6-142">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="462a6-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="462a6-143">See Also</span></span>


[<span data-ttu-id="462a6-144">Configurar el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="462a6-144">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="462a6-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="462a6-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

