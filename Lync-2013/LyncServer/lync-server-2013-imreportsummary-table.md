---
title: 'Lync Server 2013: tabla IMReportSummary'
description: 'Lync Server 2013: tabla IMReportSummary.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IMReportSummary table
ms:assetid: 27ff9453-53f2-4fae-b637-70a086c9df96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204753(v=OCS.15)
ms:contentKeyID: 48183673
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dfafa81d1605845b29a3627321fcbc0f72ca7ac7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427316"
---
# <a name="imreportsummary-table-in-lync-server-2013"></a><span data-ttu-id="68d7d-103">Tabla IMReportSummary en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68d7d-103">IMReportSummary table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68d7d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68d7d-104">

<span> </span></span></span>

<span data-ttu-id="68d7d-105">_**Última modificación del tema:** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="68d7d-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="68d7d-106">El IMReportSummaryTable ofrece un informe general sobre las sesiones de mensajería instantánea que se mantienen en una organización.</span><span class="sxs-lookup"><span data-stu-id="68d7d-106">The IMReportSummaryTable provides an overall report on the instant messaging sessions held in an organization.</span></span> <span data-ttu-id="68d7d-107">Esta tabla se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="68d7d-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68d7d-108">Columna</span><span class="sxs-lookup"><span data-stu-id="68d7d-108">Column</span></span></th>
<th><span data-ttu-id="68d7d-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="68d7d-109">Data Type</span></span></th>
<th><span data-ttu-id="68d7d-110">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="68d7d-110">Key/Index</span></span></th>
<th><span data-ttu-id="68d7d-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="68d7d-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68d7d-112"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="68d7d-112"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="68d7d-113">datetime</span><span class="sxs-lookup"><span data-stu-id="68d7d-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="68d7d-114">Primary</span><span class="sxs-lookup"><span data-stu-id="68d7d-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="68d7d-115">Fecha y hora en que comenzó la sesión de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="68d7d-115">Date and time that the instant messaging session began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68d7d-116"><strong>TimePeriod</strong></span><span class="sxs-lookup"><span data-stu-id="68d7d-116"><strong>TimePeriod</strong></span></span></p></td>
<td><p><span data-ttu-id="68d7d-117">Char (1)</span><span class="sxs-lookup"><span data-stu-id="68d7d-117">char(1)</span></span></p></td>
<td><p><span data-ttu-id="68d7d-118">Primary</span><span class="sxs-lookup"><span data-stu-id="68d7d-118">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68d7d-119"><strong>PoolFQDN</strong></span><span class="sxs-lookup"><span data-stu-id="68d7d-119"><strong>PoolFQDN</strong></span></span></p></td>
<td><p><span data-ttu-id="68d7d-120">nvarchar (257)</span><span class="sxs-lookup"><span data-stu-id="68d7d-120">nvarchar(257)</span></span></p></td>
<td><p><span data-ttu-id="68d7d-121">Primary</span><span class="sxs-lookup"><span data-stu-id="68d7d-121">Primary</span></span></p></td>
<td><p><span data-ttu-id="68d7d-122">Nombre de dominio completo del grupo que hospeda la sesión.</span><span class="sxs-lookup"><span data-stu-id="68d7d-122">Fully qualified domain name of the pool hosting the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68d7d-123"><strong>AuthType</strong></span><span class="sxs-lookup"><span data-stu-id="68d7d-123"><strong>AuthType</strong></span></span></p></td>
<td><p><span data-ttu-id="68d7d-124">int</span><span class="sxs-lookup"><span data-stu-id="68d7d-124">int</span></span></p></td>
<td><p><span data-ttu-id="68d7d-125">Primary</span><span class="sxs-lookup"><span data-stu-id="68d7d-125">Primary</span></span></p></td>
<td><p><span data-ttu-id="68d7d-126">Prioridad (por ejemplo, urgente o no urgente) de la llamada.</span><span class="sxs-lookup"><span data-stu-id="68d7d-126">Priority (for example, urgent or non-urgent) of the call.</span></span> <span data-ttu-id="68d7d-127">La información de prioridad se almacena en la <a href="lync-server-2013-callpriorities-table.md">tabla CallPriorities en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="68d7d-127">Priority information is stored in the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68d7d-128"><strong>SessionCount</strong></span><span class="sxs-lookup"><span data-stu-id="68d7d-128"><strong>SessionCount</strong></span></span></p></td>
<td><p><span data-ttu-id="68d7d-129">BIGINT</span><span class="sxs-lookup"><span data-stu-id="68d7d-129">bigint</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68d7d-130"><strong>MsgCount</strong></span><span class="sxs-lookup"><span data-stu-id="68d7d-130"><strong>MsgCount</strong></span></span></p></td>
<td><p><span data-ttu-id="68d7d-131">BIGINT</span><span class="sxs-lookup"><span data-stu-id="68d7d-131">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="68d7d-132">Número total de mensajes instantáneos intercambiados durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="68d7d-132">Total number of instant messages exchanged during the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="68d7d-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68d7d-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

