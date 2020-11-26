---
title: 'Lync Server 2013: Tabla Dialog'
description: 'Lync Server 2013: tabla de cuadros de diálogo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialog table
ms:assetid: 4d93424f-9072-43f5-83c2-3d539e3e9ca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398313(v=OCS.15)
ms:contentKeyID: 48184068
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ae93b8ca9f1146b7dc164803f27cbeeadc66777
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429206"
---
# <a name="dialog-table-in-lync-server-2013"></a><span data-ttu-id="78320-103">Tabla Dialog en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78320-103">Dialog table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78320-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78320-104">

<span> </span></span></span>

<span data-ttu-id="78320-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="78320-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="78320-106">La tabla de diálogo es una tabla de soporte técnico; cada registro representa un cuadro de diálogo protocolo de inicio de sesión (SIP).</span><span class="sxs-lookup"><span data-stu-id="78320-106">The Dialog table is a supporting table; each record represents one Session Initiation Protocol (SIP) dialog.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78320-107"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="78320-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="78320-108"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="78320-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="78320-109"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="78320-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="78320-110"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="78320-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78320-111"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="78320-111"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="78320-112">datetime</span><span class="sxs-lookup"><span data-stu-id="78320-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="78320-113">Primary</span><span class="sxs-lookup"><span data-stu-id="78320-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="78320-114">Hora en que el agente de calidad de excelencia (QoE) recibe el primer informe de quien llama o de quien llama.</span><span class="sxs-lookup"><span data-stu-id="78320-114">Time when the Quality of Excellence (QoE) agent receives the first report from either caller or callee.</span></span> <span data-ttu-id="78320-115">Se usa en conjunción con SessionSeq para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="78320-115">Used in conjunction with SessionSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78320-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="78320-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="78320-117">int</span><span class="sxs-lookup"><span data-stu-id="78320-117">int</span></span></p></td>
<td><p><span data-ttu-id="78320-118">Primary</span><span class="sxs-lookup"><span data-stu-id="78320-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="78320-119">Número de secuencia para diferenciar las sesiones cuando tienen el mismo ConferenceDateTime.</span><span class="sxs-lookup"><span data-stu-id="78320-119">Sequence number to differentiate sessions when they have the same ConferenceDateTime.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78320-120"><strong>DialogID</strong></span><span class="sxs-lookup"><span data-stu-id="78320-120"><strong>DialogID</strong></span></span></p></td>
<td><p><span data-ttu-id="78320-121">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="78320-121">varchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78320-122">IDENTIFICADOR de cuadro de diálogo único de forma global.</span><span class="sxs-lookup"><span data-stu-id="78320-122">Dialog ID which is globally unique.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78320-123"><strong>DialogIDChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="78320-123"><strong>DialogIDChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="78320-124">int</span><span class="sxs-lookup"><span data-stu-id="78320-124">int</span></span></p></td>
<td><p><span data-ttu-id="78320-125">clasificación</span><span class="sxs-lookup"><span data-stu-id="78320-125">index</span></span></p></td>
<td><p><span data-ttu-id="78320-126">Suma de comprobación del identificador de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="78320-126">Checksum of the Dialog ID.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="78320-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78320-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

