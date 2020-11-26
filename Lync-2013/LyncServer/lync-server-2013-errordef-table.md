---
title: 'Lync Server 2013: Tabla ErrorDef'
description: 'Lync Server 2013: tabla ErrorDef.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorDef table
ms:assetid: 6acf3b86-da61-4923-9812-300db6f66dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398503(v=OCS.15)
ms:contentKeyID: 48184403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58980a671b54007012bbbf6780e24c162aebe00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428541"
---
# <a name="errordef-table-in-lync-server-2013"></a><span data-ttu-id="247cd-103">Tabla ErrorDef en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="247cd-103">ErrorDef table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="247cd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="247cd-104">

<span> </span></span></span>

<span data-ttu-id="247cd-105">_**Última modificación del tema:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="247cd-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="247cd-106">La tabla ErrorDef almacena información acerca de cada tipo de error que puede ocurrir.</span><span class="sxs-lookup"><span data-stu-id="247cd-106">The ErrorDef table stores information about each type of error that may occur.</span></span> <span data-ttu-id="247cd-107">Cada registro es un tipo de error.</span><span class="sxs-lookup"><span data-stu-id="247cd-107">Each record is one type of error.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="247cd-108">Columna</span><span class="sxs-lookup"><span data-stu-id="247cd-108">Column</span></span></th>
<th><span data-ttu-id="247cd-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="247cd-109">Data Type</span></span></th>
<th><span data-ttu-id="247cd-110">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="247cd-110">Key/Index</span></span></th>
<th><span data-ttu-id="247cd-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="247cd-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="247cd-112"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="247cd-112"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="247cd-113">int</span><span class="sxs-lookup"><span data-stu-id="247cd-113">int</span></span></p></td>
<td><p><span data-ttu-id="247cd-114">Primary</span><span class="sxs-lookup"><span data-stu-id="247cd-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="247cd-115">Número de identificación único que identifica este tipo de error.</span><span class="sxs-lookup"><span data-stu-id="247cd-115">Unique ID number identifying this type of error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247cd-116"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="247cd-116"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="247cd-117">int</span><span class="sxs-lookup"><span data-stu-id="247cd-117">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="247cd-118">Código de respuesta SIP estándar asociado a este error.</span><span class="sxs-lookup"><span data-stu-id="247cd-118">Standard SIP response code associated with this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="247cd-119"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="247cd-119"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="247cd-120">int</span><span class="sxs-lookup"><span data-stu-id="247cd-120">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="247cd-121">IDENTIFICADOR de diagnóstico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="247cd-121">Microsoft Diagnostic ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247cd-122"><strong>CallTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="247cd-122"><strong>CallTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="247cd-123">ENT</span><span class="sxs-lookup"><span data-stu-id="247cd-123">Int</span></span></p></td>
<td><p><span data-ttu-id="247cd-124">Extranjero</span><span class="sxs-lookup"><span data-stu-id="247cd-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="247cd-125">Tipo de la llamada.</span><span class="sxs-lookup"><span data-stu-id="247cd-125">Type of the call.</span></span> <span data-ttu-id="247cd-126">Para obtener más información, consulte la <a href="lync-server-2013-calltype-table.md">tabla CallType en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="247cd-126">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="247cd-127"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="247cd-127"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="247cd-128">varbinary (33)</span><span class="sxs-lookup"><span data-stu-id="247cd-128">varbinary(33)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="247cd-129">Tipo de solicitud en la que se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="247cd-129">Type of request that failed.</span></span></p>
<p><span data-ttu-id="247cd-130">Estos datos se pueden convertir a formato de texto con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="247cd-130">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(RequestType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247cd-131"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="247cd-131"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="247cd-132">varbinary (257)</span><span class="sxs-lookup"><span data-stu-id="247cd-132">varbinary(257)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="247cd-133">Tipo de contenido de la solicitud en la que se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="247cd-133">Content type of the request that failed.</span></span></p>
<p><span data-ttu-id="247cd-134">Estos datos se pueden convertir a formato de texto con este sintaxis:</span><span class="sxs-lookup"><span data-stu-id="247cd-134">This data can be converted to text format by using this syntaxt:</span></span></p>
<p><code>cast(cast(ContentType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="247cd-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="247cd-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

