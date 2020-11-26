---
title: 'Lync Server 2013: Tabla Media'
description: 'Lync Server 2013: tabla de medios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media table
ms:assetid: 1e1b427f-59b5-4564-bde5-1002a80439ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398268(v=OCS.15)
ms:contentKeyID: 48183568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31e30d1f91c59b8e3aa7915fc0d513618d0f709f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425678"
---
# <a name="media-table-in-lync-server-2013"></a><span data-ttu-id="96e0b-103">Tabla Media en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96e0b-103">Media table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96e0b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96e0b-104">

<span> </span></span></span>

<span data-ttu-id="96e0b-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="96e0b-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="96e0b-106">Cada registro representa un tipo de medio usado en una sesión de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="96e0b-106">Each record represents one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="96e0b-107">Una sesión estaría representada por varios registros de la tabla, si se usa más de un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="96e0b-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="96e0b-108">La tabla de medios no se debe usar para calcular la duración multimedia de una sesión.</span><span class="sxs-lookup"><span data-stu-id="96e0b-108">The Media table should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="96e0b-109">Esta tabla contiene los detalles de señalización de intercambio de medios en una sesión.</span><span class="sxs-lookup"><span data-stu-id="96e0b-109">This table contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="96e0b-110">El intercambio de medios se realiza mediante la solicitud INVITE y StartTime indica el momento en que se envió la invitación. La hora de la invitación no significa necesariamente la hora de inicio del medio, porque los elementos multimedia solo se inician después de que la sesión acepte la sesión.</span><span class="sxs-lookup"><span data-stu-id="96e0b-110">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the sessionee accepts the session.</span></span> <span data-ttu-id="96e0b-111">La EndTime normalmente significa la hora de finalización de esta sesión.</span><span class="sxs-lookup"><span data-stu-id="96e0b-111">The EndTime usually means the end time of this session.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96e0b-112">Columna</span><span class="sxs-lookup"><span data-stu-id="96e0b-112">Column</span></span></th>
<th><span data-ttu-id="96e0b-113">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="96e0b-113">Data Type</span></span></th>
<th><span data-ttu-id="96e0b-114">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="96e0b-114">Key/Index</span></span></th>
<th><span data-ttu-id="96e0b-115">Detalles</span><span class="sxs-lookup"><span data-stu-id="96e0b-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96e0b-116"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="96e0b-116"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="96e0b-117">datetime</span><span class="sxs-lookup"><span data-stu-id="96e0b-117">datetime</span></span></p></td>
<td><p><span data-ttu-id="96e0b-118">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="96e0b-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="96e0b-119">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="96e0b-119">Time of session request.</span></span> <span data-ttu-id="96e0b-120">Se usa en conjunción con <strong>SessionIdSeq</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="96e0b-120">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="96e0b-121">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="96e0b-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96e0b-122"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="96e0b-122"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="96e0b-123">int</span><span class="sxs-lookup"><span data-stu-id="96e0b-123">int</span></span></p></td>
<td><p><span data-ttu-id="96e0b-124">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="96e0b-124">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="96e0b-125">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="96e0b-125">ID number to identify the session.</span></span> <span data-ttu-id="96e0b-126">Se usa en conjunción con <strong>SessionIdTime</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="96e0b-126">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="96e0b-127">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="96e0b-127">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96e0b-128"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="96e0b-128"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="96e0b-129">tinyint</span><span class="sxs-lookup"><span data-stu-id="96e0b-129">tinyint</span></span></p></td>
<td><p><span data-ttu-id="96e0b-130">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="96e0b-130">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="96e0b-131">Número único que identifica este tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="96e0b-131">Unique number identifying this media type.</span></span> <span data-ttu-id="96e0b-132">Para obtener más información, consulte la <a href="lync-server-2013-medialist-table.md">tabla medial en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="96e0b-132">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96e0b-133"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="96e0b-133"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="96e0b-134">datetime</span><span class="sxs-lookup"><span data-stu-id="96e0b-134">datetime</span></span></p></td>
<td><p><span data-ttu-id="96e0b-135">Primary</span><span class="sxs-lookup"><span data-stu-id="96e0b-135">Primary</span></span></p></td>
<td><p><span data-ttu-id="96e0b-136">Este es el tiempo que se envió una solicitud de medios, no la hora real de inicio de medios.</span><span class="sxs-lookup"><span data-stu-id="96e0b-136">This is the time that a media request was sent out, not the real media start time.</span></span> <span data-ttu-id="96e0b-137"><strong>StartTime</strong> incluye la hora de configuración de la sesión.</span><span class="sxs-lookup"><span data-stu-id="96e0b-137"><strong>StartTime</strong> includes the session setup time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96e0b-138"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="96e0b-138"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="96e0b-139">datetime</span><span class="sxs-lookup"><span data-stu-id="96e0b-139">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="96e0b-140">Esta es la hora de finalización de la sesión.</span><span class="sxs-lookup"><span data-stu-id="96e0b-140">This is the end time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="96e0b-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96e0b-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

