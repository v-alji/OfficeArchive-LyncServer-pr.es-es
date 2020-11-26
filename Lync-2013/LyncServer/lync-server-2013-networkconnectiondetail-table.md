---
title: 'Lync Server 2013: tabla NetworkConnectionDetail'
description: 'Lync Server 2013: tabla NetworkConnectionDetail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: NetworkConnectionDetail table
ms:assetid: b48cc9a6-5232-48b5-bd20-53b68229336b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205185(v=OCS.15)
ms:contentKeyID: 48185170
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dcd0f429999b6629826a9f9369d154afe3c1af2f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445494"
---
# <a name="networkconnectiondetail-table-in-lync-server-2013"></a><span data-ttu-id="d06cf-103">Tabla NetworkConnectionDetail en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d06cf-103">NetworkConnectionDetail table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d06cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d06cf-104">

<span> </span></span></span>

<span data-ttu-id="d06cf-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="d06cf-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="d06cf-106">La tabla NetworkConnectionDetail se asigna a los identificadores de conexión de red que se usan en otras partes de la base de datos de la calidad de la experiencia.</span><span class="sxs-lookup"><span data-stu-id="d06cf-106">The NetworkConnectionDetail table maps network connection types to the network connection identifiers used elsewhere in the Quality of Experience database.</span></span> <span data-ttu-id="d06cf-107">Esta tabla se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d06cf-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d06cf-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="d06cf-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="d06cf-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="d06cf-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="d06cf-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="d06cf-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="d06cf-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="d06cf-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d06cf-112"><strong>NetworkConnectionDetailKey</strong></span><span class="sxs-lookup"><span data-stu-id="d06cf-112"><strong>NetworkConnectionDetailKey</strong></span></span></p></td>
<td><p><span data-ttu-id="d06cf-113">tinyint</span><span class="sxs-lookup"><span data-stu-id="d06cf-113">tinyint</span></span></p></td>
<td><p><span data-ttu-id="d06cf-114">Primary</span><span class="sxs-lookup"><span data-stu-id="d06cf-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="d06cf-115">Identificador único del tipo de conexión de red.</span><span class="sxs-lookup"><span data-stu-id="d06cf-115">Unique identifier for the network connection type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06cf-116"><strong>NetworkConnectionDetail</strong></span><span class="sxs-lookup"><span data-stu-id="d06cf-116"><strong>NetworkConnectionDetail</strong></span></span></p></td>
<td><p><span data-ttu-id="d06cf-117">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="d06cf-117">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d06cf-118">Solo</span><span class="sxs-lookup"><span data-stu-id="d06cf-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="d06cf-119">Tipo de conexión de red que corresponde a la NetworkConnectionDetailKey.</span><span class="sxs-lookup"><span data-stu-id="d06cf-119">Network connection type that corresponds to the NetworkConnectionDetailKey.</span></span> <span data-ttu-id="d06cf-120">Los valores permitidos son:</span><span class="sxs-lookup"><span data-stu-id="d06cf-120">Allowed values are:</span></span></p>
<ol>
<li><p><span data-ttu-id="d06cf-121">0: conectado</span><span class="sxs-lookup"><span data-stu-id="d06cf-121">0 -- Wired</span></span></p></li>
<li><p><span data-ttu-id="d06cf-122">1--WiFi</span><span class="sxs-lookup"><span data-stu-id="d06cf-122">1 -- WiFi</span></span></p></li>
<li><p><span data-ttu-id="d06cf-123">2--Ethernet</span><span class="sxs-lookup"><span data-stu-id="d06cf-123">2 -- Ethernet</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table><span data-ttu-id="d06cf-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d06cf-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

