---
title: 'Lync Server 2013: Tabla Server'
description: 'Lync Server 2013: tabla de servidor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server table
ms:assetid: 9af89d08-d35a-48e8-b56d-6df292f973cc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398801(v=OCS.15)
ms:contentKeyID: 48184890
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 00990a91aec64063480d96a16380171990913ad4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441854"
---
# <a name="server-table-in-lync-server-2013"></a><span data-ttu-id="0875f-103">Tabla Server en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0875f-103">Server table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0875f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0875f-104">

<span> </span></span></span>

<span data-ttu-id="0875f-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="0875f-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="0875f-106">La tabla del servidor es una tabla de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="0875f-106">The Server table is a supporting table.</span></span> <span data-ttu-id="0875f-107">Cada registro representa un servidor.</span><span class="sxs-lookup"><span data-stu-id="0875f-107">Each record represents one server.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0875f-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="0875f-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="0875f-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="0875f-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="0875f-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="0875f-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="0875f-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="0875f-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0875f-112"><strong>ServerKey</strong></span><span class="sxs-lookup"><span data-stu-id="0875f-112"><strong>ServerKey</strong></span></span></p></td>
<td><p><span data-ttu-id="0875f-113">int</span><span class="sxs-lookup"><span data-stu-id="0875f-113">int</span></span></p></td>
<td><p><span data-ttu-id="0875f-114">Primary</span><span class="sxs-lookup"><span data-stu-id="0875f-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="0875f-115">Número único que identifica el servidor.</span><span class="sxs-lookup"><span data-stu-id="0875f-115">Unique number identifying the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0875f-116"><strong>FQDNOrIP</strong></span><span class="sxs-lookup"><span data-stu-id="0875f-116"><strong>FQDNOrIP</strong></span></span></p></td>
<td><p><span data-ttu-id="0875f-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0875f-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0875f-118">clasificación</span><span class="sxs-lookup"><span data-stu-id="0875f-118">index</span></span></p></td>
<td><p><span data-ttu-id="0875f-119">Cadena de dirección MAC.</span><span class="sxs-lookup"><span data-stu-id="0875f-119">MAC address string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0875f-120"><strong>ServerType</strong></span><span class="sxs-lookup"><span data-stu-id="0875f-120"><strong>ServerType</strong></span></span></p></td>
<td><p><span data-ttu-id="0875f-121">int</span><span class="sxs-lookup"><span data-stu-id="0875f-121">int</span></span></p></td>
<td><p><span data-ttu-id="0875f-122">Extranjero</span><span class="sxs-lookup"><span data-stu-id="0875f-122">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0875f-123">1: servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="0875f-123">1: Mediation Server</span></span></p>
<p><span data-ttu-id="0875f-124">2: Server16394 de conferencia a/V: service32769 Edge: Gateway</span><span class="sxs-lookup"><span data-stu-id="0875f-124">2: A/V Conferencing Server16394: A/V Edge service32769: Gateway</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0875f-125"><strong>Nombredegrupo</strong></span><span class="sxs-lookup"><span data-stu-id="0875f-125"><strong>PoolName</strong></span></span></p></td>
<td><p><span data-ttu-id="0875f-126">nvarchar (512)</span><span class="sxs-lookup"><span data-stu-id="0875f-126">nvarchar(512)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0875f-127">Grupo al que pertenece el servidor.</span><span class="sxs-lookup"><span data-stu-id="0875f-127">Pool the server belongs to.</span></span> <span data-ttu-id="0875f-128">Solo es aplicable para el servidor de conferencia A/V.</span><span class="sxs-lookup"><span data-stu-id="0875f-128">Only applicable for the A/V Conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0875f-129"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="0875f-129"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="0875f-130">datetime</span><span class="sxs-lookup"><span data-stu-id="0875f-130">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0875f-131">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="0875f-131">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0875f-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0875f-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

