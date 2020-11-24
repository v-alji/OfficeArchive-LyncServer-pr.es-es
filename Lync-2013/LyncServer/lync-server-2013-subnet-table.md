---
title: 'Lync Server 2013: Tabla Subnet'
description: 'Lync Server 2013: tabla de subredes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Subnet table
ms:assetid: 76f5c995-96c8-4aa3-bc30-1d74991d7c42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398582(v=OCS.15)
ms:contentKeyID: 48184544
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30c04ddf897e0a62551709b30211ba724a75cbf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398124"
---
# <a name="subnet-table-in-lync-server-2013"></a><span data-ttu-id="cdf29-103">Tabla Subnet en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cdf29-103">Subnet table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cdf29-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cdf29-104">

<span> </span></span></span>

<span data-ttu-id="cdf29-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="cdf29-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="cdf29-106">La tabla de subred es una tabla de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="cdf29-106">The Subnet table is a supporting table.</span></span> <span data-ttu-id="cdf29-107">Cada registro representa una subred definida en la opción de configuración de red.</span><span class="sxs-lookup"><span data-stu-id="cdf29-107">Each record represents one subnet defined in network configuration setting.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cdf29-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="cdf29-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="cdf29-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="cdf29-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="cdf29-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="cdf29-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="cdf29-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="cdf29-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf29-112"><strong>SubnetIP</strong></span><span class="sxs-lookup"><span data-stu-id="cdf29-112"><strong>SubnetIP</strong></span></span></p></td>
<td><p><span data-ttu-id="cdf29-113">int</span><span class="sxs-lookup"><span data-stu-id="cdf29-113">int</span></span></p></td>
<td><p><span data-ttu-id="cdf29-114">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="cdf29-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="cdf29-115">Representación de enteros de la IP de subred.</span><span class="sxs-lookup"><span data-stu-id="cdf29-115">Integer representation for the subnet IP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf29-116"><strong>Máscaradesubred</strong></span><span class="sxs-lookup"><span data-stu-id="cdf29-116"><strong>SubnetMask</strong></span></span></p></td>
<td><p><span data-ttu-id="cdf29-117">int</span><span class="sxs-lookup"><span data-stu-id="cdf29-117">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cdf29-118">Máscara de la subred.</span><span class="sxs-lookup"><span data-stu-id="cdf29-118">Subnet mask.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf29-119"><strong>UserSiteKey</strong></span><span class="sxs-lookup"><span data-stu-id="cdf29-119"><strong>UserSiteKey</strong></span></span></p></td>
<td><p><span data-ttu-id="cdf29-120">int</span><span class="sxs-lookup"><span data-stu-id="cdf29-120">int</span></span></p></td>
<td><p><span data-ttu-id="cdf29-121">Extranjero</span><span class="sxs-lookup"><span data-stu-id="cdf29-121">Foreign</span></span></p></td>
<td><p><span data-ttu-id="cdf29-122">Se hace referencia a ellos desde la <a href="lync-server-2013-usersite-table.md">tabla UserSite en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="cdf29-122">Referenced from the <a href="lync-server-2013-usersite-table.md">UserSite table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf29-123"><strong>SubnetDescription</strong></span><span class="sxs-lookup"><span data-stu-id="cdf29-123"><strong>SubnetDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="cdf29-124">nvarchar (512)</span><span class="sxs-lookup"><span data-stu-id="cdf29-124">nvarchar(512)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cdf29-125">La descripción de la subred.</span><span class="sxs-lookup"><span data-stu-id="cdf29-125">The description for the subnet.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cdf29-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cdf29-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

