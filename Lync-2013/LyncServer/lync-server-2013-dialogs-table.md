---
title: 'Lync Server 2013: Tabla Dialogs'
description: 'Lync Server 2013: tabla de cuadros de diálogo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialogs table
ms:assetid: 487a430b-af66-4ea6-b28e-4e33cfdb7f9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425954(v=OCS.15)
ms:contentKeyID: 48184001
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c2c9cf9ec59fc48f7f5ffc6232980e3f8aa68c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429185"
---
# <a name="dialogs-table-in-lync-server-2013"></a><span data-ttu-id="b0bbd-103">Tabla Dialogs en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0bbd-103">Dialogs table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0bbd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0bbd-104">

<span> </span></span></span>

<span data-ttu-id="b0bbd-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="b0bbd-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="b0bbd-106">La tabla de cuadros de diálogo es una tabla de soporte que almacena la información sobre DialogIDs para las sesiones de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-106">The Dialogs table is a supporting table that stores the information about DialogIDs for peer-to-peer sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0bbd-107">Columna</span><span class="sxs-lookup"><span data-stu-id="b0bbd-107">Column</span></span></th>
<th><span data-ttu-id="b0bbd-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b0bbd-108">Data Type</span></span></th>
<th><span data-ttu-id="b0bbd-109">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="b0bbd-109">Key/Index</span></span></th>
<th><span data-ttu-id="b0bbd-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="b0bbd-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0bbd-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="b0bbd-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b0bbd-112">datetime</span><span class="sxs-lookup"><span data-stu-id="b0bbd-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="b0bbd-113">Primary</span><span class="sxs-lookup"><span data-stu-id="b0bbd-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="b0bbd-114">Hora de la solicitud de sesión; se usa en conjunción con SessionIDSeq para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-114">Time of session request; used in conjunction with SessionIDSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0bbd-115"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b0bbd-115"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b0bbd-116">int</span><span class="sxs-lookup"><span data-stu-id="b0bbd-116">int</span></span></p></td>
<td><p><span data-ttu-id="b0bbd-117">Primary</span><span class="sxs-lookup"><span data-stu-id="b0bbd-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="b0bbd-118">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-118">ID number to identify the session.</span></span> <span data-ttu-id="b0bbd-119">Se usa en conjunción con SessionIDTime para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-119">Used in conjunction with SessionIDTime to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0bbd-120"><strong>ExternalChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="b0bbd-120"><strong>ExternalChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="b0bbd-121">int</span><span class="sxs-lookup"><span data-stu-id="b0bbd-121">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b0bbd-122">Suma de comprobación de la ExternalID.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-122">Checksum of the ExternalID.</span></span> <span data-ttu-id="b0bbd-123">Este campo se usa para aumentar la velocidad de las búsquedas en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-123">This field is used to increase the speed of database searches.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0bbd-124"><strong>ExternalId</strong></span><span class="sxs-lookup"><span data-stu-id="b0bbd-124"><strong>ExternalId</strong></span></span></p></td>
<td><p><span data-ttu-id="b0bbd-125">varbinary (775)</span><span class="sxs-lookup"><span data-stu-id="b0bbd-125">varbinary(775)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b0bbd-126">IDENTIFICADOR del cuadro de diálogo SIP, almacenado como binario.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-126">SIP dialog ID, stored as a binary.</span></span> <span data-ttu-id="b0bbd-127">El formato del binario es:</span><span class="sxs-lookup"><span data-stu-id="b0bbd-127">The format of the binary is:</span></span></p>
<p><span data-ttu-id="b0bbd-128">cuadro de diálogo; desde: etiqueta; to-Tag</span><span class="sxs-lookup"><span data-stu-id="b0bbd-128">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="b0bbd-129">Estos datos se pueden convertir a formato de texto con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="b0bbd-129">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(ExternalId as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b0bbd-130">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0bbd-130">


</div>

<span> </span>

</div>

</div>

</span></span></div>

