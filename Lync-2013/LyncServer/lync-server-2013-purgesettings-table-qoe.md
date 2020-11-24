---
title: 'Lync Server 2013: tabla PurgeSettings (QoE)'
description: 'Lync Server 2013: tabla PurgeSettings (QoE).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PurgeSettings table (QoE)
ms:assetid: 31b85d1c-3f32-4f67-94bf-9389cdd282c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204788(v=OCS.15)
ms:contentKeyID: 48183777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d515d799a7cc442dc6d34f2ece1a968de51cdad6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399017"
---
# <a name="purgesettings-table-qoe-in-lync-server-2013"></a><span data-ttu-id="f3681-103">Tabla PurgeSettings (QoE) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3681-103">PurgeSettings table (QoE) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3681-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3681-104">

<span> </span></span></span>

<span data-ttu-id="f3681-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="f3681-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="f3681-106">La tabla PurgeSettings contiene información que especifica si (y cuándo) la calidad de los registros de experiencia se eliminará automáticamente de la base de datos de QoE.</span><span class="sxs-lookup"><span data-stu-id="f3681-106">The PurgeSettings table contains information that specifies if (and when) outdated Quality of Experience records will automatically be deleted from the QoE database.</span></span> <span data-ttu-id="f3681-107">Tenga en cuenta que la información relacionada con la purga también puede obtenerse en el shell de administración de Microsoft Lync Server 2013 ejecutando el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="f3681-107">Note that purging-related information can also be obtained from within the Microsoft Lync Server 2013 Management Shell by running the following command:</span></span>

    Get-CsQoEConfiguration

<span data-ttu-id="f3681-108">Esta tabla se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f3681-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3681-109"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="f3681-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="f3681-110"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="f3681-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="f3681-111"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="f3681-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="f3681-112"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="f3681-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3681-113"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="f3681-113"><strong>ID</strong></span></span></p></td>
<td><p><span data-ttu-id="f3681-114">int</span><span class="sxs-lookup"><span data-stu-id="f3681-114">int</span></span></p></td>
<td><p><span data-ttu-id="f3681-115">Primary</span><span class="sxs-lookup"><span data-stu-id="f3681-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="f3681-116">Identificador único para la recopilación de configuración de purga de QoE.</span><span class="sxs-lookup"><span data-stu-id="f3681-116">Unique identifier for the collection of QoE purge settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3681-117"><strong>EnablePurge</strong></span><span class="sxs-lookup"><span data-stu-id="f3681-117"><strong>EnablePurge</strong></span></span></p></td>
<td><p><span data-ttu-id="f3681-118">bit</span><span class="sxs-lookup"><span data-stu-id="f3681-118">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f3681-119">Cuando se establece en true (1), Microsoft Lync Server 2013 purgará periódicamente los registros obsoletos de la base de datos de calidad.</span><span class="sxs-lookup"><span data-stu-id="f3681-119">When set to True (1) Microsoft Lync Server 2013 will periodically purge outdated records from the QoE database.</span></span> <span data-ttu-id="f3681-120">La purga se realizará cada día a la tomé especificada por el valor PurgeHour.</span><span class="sxs-lookup"><span data-stu-id="f3681-120">Purging will take place each day at the tome specified by the PurgeHour setting.</span></span> <span data-ttu-id="f3681-121">Si se establece en false (0), los registros no se purgarán automáticamente de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f3681-121">If set to False (0) then records will not be automatically purged from the database.</span></span> <span data-ttu-id="f3681-122">El valor predeterminado es True.</span><span class="sxs-lookup"><span data-stu-id="f3681-122">The default value is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3681-123"><strong>KeepQoEDataForDays</strong></span><span class="sxs-lookup"><span data-stu-id="f3681-123"><strong>KeepQoEDataForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="f3681-124">int</span><span class="sxs-lookup"><span data-stu-id="f3681-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f3681-125">Especifica los registros de edad de calidad (en días) que se purgarán de la base de datos: Si la purga está habilitada, los registros de QoE anteriores a este valor se eliminarán de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f3681-125">Specifies the age of QoE records (in days) that will be purged from the database: if purging is enabled, QoE records older than this value will be removed from the database.</span></span> <span data-ttu-id="f3681-126">El valor predeterminado es 60 días.</span><span class="sxs-lookup"><span data-stu-id="f3681-126">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3681-127"><strong>PurgeHour</strong></span><span class="sxs-lookup"><span data-stu-id="f3681-127"><strong>PurgeHour</strong></span></span></p></td>
<td><p><span data-ttu-id="f3681-128">int</span><span class="sxs-lookup"><span data-stu-id="f3681-128">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f3681-129">Especifica la hora local del día en la que tendrá lugar la depuración de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f3681-129">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="f3681-130">La hora del día se especifica con el formato de 24 horas, donde 0 representa la media noche (12:00 AM) y 23 representa las 11:00 PM.</span><span class="sxs-lookup"><span data-stu-id="f3681-130">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="f3681-131">Tenga en cuenta que solo se puede especificar la hora del día: un valor de 10 (indicando 10:00 A.M.), pero no se permite un valor de 10:30 de 10,5 (que indica 10:30 A.M.).</span><span class="sxs-lookup"><span data-stu-id="f3681-131">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="f3681-132">El valor predeterminado es 1 (1:00 A.M.).</span><span class="sxs-lookup"><span data-stu-id="f3681-132">The default value is 1 (1:00 AM).</span></span> <span data-ttu-id="f3681-133">Especifica la hora local del día en la que tendrá lugar la depuración de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f3681-133">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="f3681-134">La hora del día se especifica con el formato de 24 horas, donde 0 representa la media noche (12:00 AM) y 23 representa las 11:00 PM.</span><span class="sxs-lookup"><span data-stu-id="f3681-134">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="f3681-135">Tenga en cuenta que solo se puede especificar la hora del día: un valor de 10 (indicando 10:00 A.M.), pero no se permite un valor de 10:30 de 10,5 (que indica 10:30 A.M.).</span><span class="sxs-lookup"><span data-stu-id="f3681-135">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="f3681-136">El valor predeterminado es 1 (1:00 A.M.).</span><span class="sxs-lookup"><span data-stu-id="f3681-136">The default value is 1 (1:00 AM).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f3681-137">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3681-137">


</div>

<span> </span>

</div>

</div>

</span></span></div>

