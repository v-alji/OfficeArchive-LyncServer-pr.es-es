---
title: 'Lync Server 2013: Tabla Conference'
description: 'Lync Server 2013: tabla de conferencia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference table
ms:assetid: 2a2c327c-4719-42dc-a3bb-6dbc0864d9af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425762(v=OCS.15)
ms:contentKeyID: 48183700
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 565725b527399cb3be55c649dfd74d8bcb5f13a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434469"
---
# <a name="conference-table-in-lync-server-2013"></a><span data-ttu-id="d21c9-103">Tabla Conference en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d21c9-103">Conference table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d21c9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d21c9-104">

<span> </span></span></span>

<span data-ttu-id="d21c9-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="d21c9-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="d21c9-106">La tabla de conferencia es una tabla de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="d21c9-106">The Conference table is a supporting table.</span></span> <span data-ttu-id="d21c9-107">Cada registro representa una sesión de conferencia o de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="d21c9-107">Each record represents one conference or peer-to-peer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d21c9-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="d21c9-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="d21c9-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="d21c9-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="d21c9-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="d21c9-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="d21c9-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="d21c9-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d21c9-112"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="d21c9-112"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="d21c9-113">int</span><span class="sxs-lookup"><span data-stu-id="d21c9-113">int</span></span></p></td>
<td><p><span data-ttu-id="d21c9-114">Primary</span><span class="sxs-lookup"><span data-stu-id="d21c9-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="d21c9-115">Número único que identifica este registro de conferencia.</span><span class="sxs-lookup"><span data-stu-id="d21c9-115">Unique number identifying this conference record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d21c9-116"><strong>ConfURI</strong></span><span class="sxs-lookup"><span data-stu-id="d21c9-116"><strong>ConfURI</strong></span></span></p></td>
<td><p><span data-ttu-id="d21c9-117">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d21c9-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d21c9-118">solo</span><span class="sxs-lookup"><span data-stu-id="d21c9-118">unique</span></span></p></td>
<td><p><span data-ttu-id="d21c9-119">URI de conferencia si se trata de una conferencia o DialogID si se trata de una sesión de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="d21c9-119">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d21c9-120"><strong>Comprobación</strong></span><span class="sxs-lookup"><span data-stu-id="d21c9-120"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="d21c9-121">int</span><span class="sxs-lookup"><span data-stu-id="d21c9-121">int</span></span></p></td>
<td><p><span data-ttu-id="d21c9-122">clasificación</span><span class="sxs-lookup"><span data-stu-id="d21c9-122">index</span></span></p></td>
<td><p><span data-ttu-id="d21c9-123">Suma de comprobación del URI de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="d21c9-123">Checksum of the conference URI.</span></span> <span data-ttu-id="d21c9-124">Esto se usa internamente.</span><span class="sxs-lookup"><span data-stu-id="d21c9-124">This is used internally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d21c9-125"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="d21c9-125"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="d21c9-126">datetime</span><span class="sxs-lookup"><span data-stu-id="d21c9-126">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d21c9-127">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="d21c9-127">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d21c9-128">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d21c9-128">


</div>

<span> </span>

</div>

</div>

</span></span></div>

