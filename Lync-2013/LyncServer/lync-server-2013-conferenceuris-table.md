---
title: 'Lync Server 2013: Tabla ConferenceUris'
description: 'Lync Server 2013: tabla ConferenceUris.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceUris table
ms:assetid: b1721d52-3c65-45ea-8997-06af8fef93fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412854(v=OCS.15)
ms:contentKeyID: 48185160
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a142aa9ad1fe4d3ae92aa3e21aa9eee505457cbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434392"
---
# <a name="conferenceuris-table-in-lync-server-2013"></a><span data-ttu-id="e1402-103">Tabla ConferenceUris en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1402-103">ConferenceUris table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e1402-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e1402-104">

<span> </span></span></span>

<span data-ttu-id="e1402-105">_**Última modificación del tema:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="e1402-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="e1402-106">La tabla ConfereneUris es una tabla de soporte que almacena una lista de los distintos URI de conferencia que participaron en sesiones de conferencia registradas en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e1402-106">The ConfereneUris table is a supporting table that stores a list of the various conference URIs that have participated in conference sessions recorded in the database.</span></span> <span data-ttu-id="e1402-107">Cada registro de la tabla representa un URI de conferencia.</span><span class="sxs-lookup"><span data-stu-id="e1402-107">Each record in the table represents one conference URI.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1402-108">Columna</span><span class="sxs-lookup"><span data-stu-id="e1402-108">Column</span></span></th>
<th><span data-ttu-id="e1402-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e1402-109">Data Type</span></span></th>
<th><span data-ttu-id="e1402-110">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="e1402-110">Key/Index</span></span></th>
<th><span data-ttu-id="e1402-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="e1402-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1402-112"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="e1402-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="e1402-113">datetime</span><span class="sxs-lookup"><span data-stu-id="e1402-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="e1402-114">Primary</span><span class="sxs-lookup"><span data-stu-id="e1402-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="e1402-115">Marca de tiempo, usada internamente.</span><span class="sxs-lookup"><span data-stu-id="e1402-115">Time stamp, Internal used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1402-116"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="e1402-116"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="e1402-117">int</span><span class="sxs-lookup"><span data-stu-id="e1402-117">int</span></span></p></td>
<td><p><span data-ttu-id="e1402-118">Primary</span><span class="sxs-lookup"><span data-stu-id="e1402-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="e1402-119">Número único que identifica este URI de conferencia.</span><span class="sxs-lookup"><span data-stu-id="e1402-119">Unique number identifying this conference URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1402-120"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="e1402-120"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="e1402-121">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="e1402-121">nvarchar(450)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e1402-122">URI de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="e1402-122">Conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1402-123"><strong>Comprobación</strong></span><span class="sxs-lookup"><span data-stu-id="e1402-123"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="e1402-124">int</span><span class="sxs-lookup"><span data-stu-id="e1402-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e1402-125">Suma de comprobación de ConferenceUri.</span><span class="sxs-lookup"><span data-stu-id="e1402-125">Checksum of ConferenceUri.</span></span> <span data-ttu-id="e1402-126">Se usa para aumentar la velocidad de las búsquedas de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="e1402-126">Used to increases the speed of database searches.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1402-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="e1402-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="e1402-128">int</span><span class="sxs-lookup"><span data-stu-id="e1402-128">int</span></span></p></td>
<td><p><span data-ttu-id="e1402-129">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e1402-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e1402-130">Tipo de URI, como conf: chat para conferencias de mensajería instantánea o conf: audio-video para conferencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="e1402-130">URI type, such as conf:chat for IM conference, or conf:audio-video for audio/video conference.</span></span> <span data-ttu-id="e1402-131">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en la tabla de 2013 de Lync Server</a> .</span><span class="sxs-lookup"><span data-stu-id="e1402-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> table for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e1402-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e1402-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

