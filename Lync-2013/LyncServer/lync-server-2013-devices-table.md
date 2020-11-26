---
title: 'Lync Server 2013: Tabla Devices'
description: 'Lync Server 2013: tabla de dispositivos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Devices table
ms:assetid: 532e2280-4bbc-4a6c-93da-45d9f80a30a0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398351(v=OCS.15)
ms:contentKeyID: 48184169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 763e1788e2874f9f9831c089ffe8fa077621b030
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429342"
---
# <a name="devices-table-in-lync-server-2013"></a><span data-ttu-id="c105b-103">Tabla Devices en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c105b-103">Devices table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c105b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c105b-104">

<span> </span></span></span>

<span data-ttu-id="c105b-105">_**Última modificación del tema:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="c105b-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="c105b-106">La tabla dispositivos es una tabla de soporte.</span><span class="sxs-lookup"><span data-stu-id="c105b-106">The Devices table is a supporting table.</span></span> <span data-ttu-id="c105b-107">Cada registro almacena información acerca de un dispositivo (teléfono de escritorio).</span><span class="sxs-lookup"><span data-stu-id="c105b-107">Each record stores information about one device (desk phone).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c105b-108">Columna</span><span class="sxs-lookup"><span data-stu-id="c105b-108">Column</span></span></th>
<th><span data-ttu-id="c105b-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c105b-109">Data Type</span></span></th>
<th><span data-ttu-id="c105b-110">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="c105b-110">Key/Index</span></span></th>
<th><span data-ttu-id="c105b-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="c105b-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c105b-112"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="c105b-112"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="c105b-113">int</span><span class="sxs-lookup"><span data-stu-id="c105b-113">int</span></span></p></td>
<td><p><span data-ttu-id="c105b-114">Primary</span><span class="sxs-lookup"><span data-stu-id="c105b-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="c105b-115">Número único que identifica esta versión de hardware.</span><span class="sxs-lookup"><span data-stu-id="c105b-115">Unique number identifying this hardware version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c105b-116"><strong>ManufacturerId</strong></span><span class="sxs-lookup"><span data-stu-id="c105b-116"><strong>ManufacturerId</strong></span></span></p></td>
<td><p><span data-ttu-id="c105b-117">int</span><span class="sxs-lookup"><span data-stu-id="c105b-117">int</span></span></p></td>
<td><p><span data-ttu-id="c105b-118">Extranjero</span><span class="sxs-lookup"><span data-stu-id="c105b-118">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c105b-119">Fabricante de este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c105b-119">Manufacturer of this device.</span></span> <span data-ttu-id="c105b-120">Para obtener más información, consulte la <a href="lync-server-2013-manufacturers-table.md">tabla de fabricantes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c105b-120">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c105b-121"><strong>HardwareVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="c105b-121"><strong>HardwareVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="c105b-122">int</span><span class="sxs-lookup"><span data-stu-id="c105b-122">int</span></span></p></td>
<td><p><span data-ttu-id="c105b-123">Extranjero</span><span class="sxs-lookup"><span data-stu-id="c105b-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c105b-124">Versión de hardware de este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c105b-124">Hardware version of this device.</span></span> <span data-ttu-id="c105b-125">Para obtener más información, consulte la <a href="lync-server-2013-hardwareversions-table.md">tabla HardwareVersions en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c105b-125">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c105b-126"><strong>MacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="c105b-126"><strong>MacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="c105b-127">BIGINT</span><span class="sxs-lookup"><span data-stu-id="c105b-127">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c105b-128">Dirección MAC</span><span class="sxs-lookup"><span data-stu-id="c105b-128">MAC Address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c105b-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c105b-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

