---
title: 'Lync Server 2013: Tabla UserAgent'
description: 'Tabla Lync Server 2013: UserAgent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgent table
ms:assetid: d6bda1c0-b053-457a-9ffa-2ae859788775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398939(v=OCS.15)
ms:contentKeyID: 48185582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b701d8384313d0267dd566e0c32242f6cc077472
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439131"
---
# <a name="useragent-table-in-lync-server-2013"></a><span data-ttu-id="8e903-103">Tabla UserAgent en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e903-103">UserAgent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e903-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e903-104">

<span> </span></span></span>

<span data-ttu-id="8e903-105">_**Última modificación del tema:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="8e903-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="8e903-106">La tabla UserAgent es una tabla de soporte que almacena una lista de los diversos agentes de usuario que participaron en sesiones registradas en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8e903-106">The UserAgent table is a supporting table that stores a list of the various user agents that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="8e903-107">Cada registro de la tabla representa un agente de usuario</span><span class="sxs-lookup"><span data-stu-id="8e903-107">Each record in the table represents one user agent</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e903-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="8e903-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="8e903-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="8e903-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="8e903-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="8e903-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="8e903-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="8e903-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e903-112"><strong>UserAgentKey</strong></span><span class="sxs-lookup"><span data-stu-id="8e903-112"><strong>UserAgentKey</strong></span></span></p></td>
<td><p><span data-ttu-id="8e903-113">int</span><span class="sxs-lookup"><span data-stu-id="8e903-113">int</span></span></p></td>
<td><p><span data-ttu-id="8e903-114">Primary</span><span class="sxs-lookup"><span data-stu-id="8e903-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="8e903-115">Número único que identifica a este agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="8e903-115">Unique number identifying this user agent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e903-116"><strong>UserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="8e903-116"><strong>UserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="8e903-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="8e903-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8e903-118">Solo</span><span class="sxs-lookup"><span data-stu-id="8e903-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="8e903-119">Cadena de agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="8e903-119">User Agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e903-120"><strong>UAType</strong></span><span class="sxs-lookup"><span data-stu-id="8e903-120"><strong>UAType</strong></span></span></p></td>
<td><p><span data-ttu-id="8e903-121">smallint</span><span class="sxs-lookup"><span data-stu-id="8e903-121">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8e903-122">1 es el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="8e903-122">1 is Mediation Server.</span></span></p>
<p><span data-ttu-id="8e903-123">2 es un servidor de conferencia A/V.</span><span class="sxs-lookup"><span data-stu-id="8e903-123">2 is A/V Conferencing Server.</span></span></p>
<p><span data-ttu-id="8e903-124">4 es Lync.</span><span class="sxs-lookup"><span data-stu-id="8e903-124">4 is Lync.</span></span></p>
<p><span data-ttu-id="8e903-125">8 es teléfono IP.</span><span class="sxs-lookup"><span data-stu-id="8e903-125">8 is IP Phone.</span></span></p>
<p><span data-ttu-id="8e903-126">16 es la consola de Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="8e903-126">16 is Live Meeting Console.</span></span></p>
<p><span data-ttu-id="8e903-127">32 es la herramienta de validación de implementación (DVT).</span><span class="sxs-lookup"><span data-stu-id="8e903-127">32 is Deployment Validation Tool (DVT).</span></span></p>
<p><span data-ttu-id="8e903-128">64 son Lync en equipos Macintosh.</span><span class="sxs-lookup"><span data-stu-id="8e903-128">64 is Lync on Macintosh computers.</span></span></p>
<p><span data-ttu-id="8e903-129">128 es el operador R2 de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="8e903-129">128 is Office Communications Server 2007 R2 Attendant.</span></span></p>
<p><span data-ttu-id="8e903-130">256 es el servicio de anuncios de conferencia.</span><span class="sxs-lookup"><span data-stu-id="8e903-130">256 is Conferencing Announcement service.</span></span></p>
<p><span data-ttu-id="8e903-131">512 es operador automático de conferencia.</span><span class="sxs-lookup"><span data-stu-id="8e903-131">512 is Conferencing Auto Attendant.</span></span></p>
<p><span data-ttu-id="8e903-132">1024 es una aplicación de grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e903-132">1024 is Response Group application.</span></span></p>
<p><span data-ttu-id="8e903-133">2048 está fuera del control de voz.</span><span class="sxs-lookup"><span data-stu-id="8e903-133">2048 is Outside Voice Control.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8e903-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e903-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

