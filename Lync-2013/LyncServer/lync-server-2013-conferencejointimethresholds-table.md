---
title: 'Lync Server 2013: tabla ConferenceJoinTimeThresholds'
description: 'Lync Server 2013: tabla ConferenceJoinTimeThresholds.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceJoinTimeThresholds table
ms:assetid: 3944d724-bdd8-4d1c-a2af-933ee8141529
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204809(v=OCS.15)
ms:contentKeyID: 48183855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e38c8b99f444e16309882b6a8885d166fdceb9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434462"
---
# <a name="conferencejointimethresholds-table-in-lync-server-2013"></a><span data-ttu-id="e13d0-103">Tabla ConferenceJoinTimeThresholds en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e13d0-103">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e13d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e13d0-104">

<span> </span></span></span>

<span data-ttu-id="e13d0-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="e13d0-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="e13d0-106">La tabla ConferenceJoinTimeThresholds contiene los límites de clasificación usados por el informe Resumen de tiempo de combinación de conferencia.</span><span class="sxs-lookup"><span data-stu-id="e13d0-106">The ConferenceJoinTimeThresholds table contains the classification boundaries used by the Conference Join Time Summary Report.</span></span> <span data-ttu-id="e13d0-107">En el informe Resumen de tiempo de combinación de conferencia se resume la cantidad de tiempo necesario para que los usuarios se unan correctamente a una conferencia; Estos valores de hora se notifican como promedio y en una de las siguientes categorías:</span><span class="sxs-lookup"><span data-stu-id="e13d0-107">The Conference Join Time Summary Report summarizes the amount time required for users to successfully join a conference; these time values are reported both as an average and in one of the following categories:</span></span>

  - <span data-ttu-id="e13d0-108">Menos de 2 segundos.</span><span class="sxs-lookup"><span data-stu-id="e13d0-108">Less than 2 seconds.</span></span>

  - <span data-ttu-id="e13d0-109">Entre 2 y 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="e13d0-109">Between 2 second and 5 seconds.</span></span>

  - <span data-ttu-id="e13d0-110">Entre 5 segundos y 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="e13d0-110">Between 5 seconds and 10 seconds.</span></span>

  - <span data-ttu-id="e13d0-111">Más de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="e13d0-111">More than 10 seconds.</span></span>

<span data-ttu-id="e13d0-112">La tabla ConferenceJoinTimeThresholds contiene los valores de clasificación de 2 segundos, 5 segundos y 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="e13d0-112">The ConferenceJoinTimeThresholds table contains the classification values 2 seconds, 5 seconds, and 10 seconds.</span></span>

<span data-ttu-id="e13d0-113">Esta tabla se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e13d0-113">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e13d0-114">Columna</span><span class="sxs-lookup"><span data-stu-id="e13d0-114">Column</span></span></th>
<th><span data-ttu-id="e13d0-115">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e13d0-115">Data Type</span></span></th>
<th><span data-ttu-id="e13d0-116">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="e13d0-116">Key/Index</span></span></th>
<th><span data-ttu-id="e13d0-117">Detalles</span><span class="sxs-lookup"><span data-stu-id="e13d0-117">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e13d0-118"><strong>ThresholdId</strong></span><span class="sxs-lookup"><span data-stu-id="e13d0-118"><strong>ThresholdId</strong></span></span></p></td>
<td><p><span data-ttu-id="e13d0-119">int</span><span class="sxs-lookup"><span data-stu-id="e13d0-119">int</span></span></p></td>
<td><p><span data-ttu-id="e13d0-120">Primary</span><span class="sxs-lookup"><span data-stu-id="e13d0-120">Primary</span></span></p></td>
<td><p><span data-ttu-id="e13d0-121">Identificador único de la clasificación.</span><span class="sxs-lookup"><span data-stu-id="e13d0-121">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13d0-122"><strong>ThresholdValue</strong></span><span class="sxs-lookup"><span data-stu-id="e13d0-122"><strong>ThresholdValue</strong></span></span></p></td>
<td><p><span data-ttu-id="e13d0-123">int</span><span class="sxs-lookup"><span data-stu-id="e13d0-123">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e13d0-124">Límite superior de la clasificación.</span><span class="sxs-lookup"><span data-stu-id="e13d0-124">Upper limit for the classification.</span></span> <span data-ttu-id="e13d0-125">Los valores permitidos son:</span><span class="sxs-lookup"><span data-stu-id="e13d0-125">Allowed values are:</span></span></p>
<ol>
<li><p><span data-ttu-id="e13d0-126">2</span><span class="sxs-lookup"><span data-stu-id="e13d0-126">2</span></span></p></li>
<li><p><span data-ttu-id="e13d0-127">5</span><span class="sxs-lookup"><span data-stu-id="e13d0-127">5</span></span></p></li>
<li><p><span data-ttu-id="e13d0-128">base10</span><span class="sxs-lookup"><span data-stu-id="e13d0-128">10</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table><span data-ttu-id="e13d0-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e13d0-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

