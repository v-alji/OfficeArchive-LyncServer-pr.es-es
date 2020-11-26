---
title: 'Lync Server 2013: Tabla FileTransfers'
description: 'Lync Server 2013: tabla FileTransfers.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers table
ms:assetid: 5368e67c-d8a9-43a1-9472-a839950dedb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398353(v=OCS.15)
ms:contentKeyID: 48184118
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ccde45fa3743a809499273676d567846ef292ecc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428170"
---
# <a name="filetransfers-table-in-lync-server-2013"></a><span data-ttu-id="e79e7-103">Tabla FileTransfers en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e79e7-103">FileTransfers table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e79e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e79e7-104">

<span> </span></span></span>

<span data-ttu-id="e79e7-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="e79e7-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="e79e7-106">Cada registro representa una sesión de transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="e79e7-106">Each record represents one file transfer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e79e7-107">Columna</span><span class="sxs-lookup"><span data-stu-id="e79e7-107">Column</span></span></th>
<th><span data-ttu-id="e79e7-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e79e7-108">Data Type</span></span></th>
<th><span data-ttu-id="e79e7-109">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="e79e7-109">Key/Index</span></span></th>
<th><span data-ttu-id="e79e7-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="e79e7-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e79e7-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="e79e7-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e79e7-112">datetime</span><span class="sxs-lookup"><span data-stu-id="e79e7-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="e79e7-113">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="e79e7-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="e79e7-114">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="e79e7-114">Time of session request.</span></span> <span data-ttu-id="e79e7-115">Se usa en conjunción con <strong>SessionIdSeq</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="e79e7-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="e79e7-116">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e79e7-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e79e7-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e79e7-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e79e7-118">int</span><span class="sxs-lookup"><span data-stu-id="e79e7-118">int</span></span></p></td>
<td><p><span data-ttu-id="e79e7-119">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="e79e7-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="e79e7-120">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="e79e7-120">ID number to identify the session.</span></span> <span data-ttu-id="e79e7-121">Se usa en conjunción con <strong>SessionIdTime</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="e79e7-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="e79e7-122">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e79e7-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e79e7-123"><strong>Nombre de archivo</strong></span><span class="sxs-lookup"><span data-stu-id="e79e7-123"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="e79e7-124">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e79e7-124">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e79e7-125">Nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="e79e7-125">Name of the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e79e7-126"><strong>FileIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="e79e7-126"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="e79e7-127">identificador</span><span class="sxs-lookup"><span data-stu-id="e79e7-127">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e79e7-128">Identificador único para distinguir entre transferencias de archivos que impliquen el mismo nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="e79e7-128">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e79e7-129"><strong>Ésta</strong></span><span class="sxs-lookup"><span data-stu-id="e79e7-129"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="e79e7-130">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="e79e7-130">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="e79e7-131">Primary</span><span class="sxs-lookup"><span data-stu-id="e79e7-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="e79e7-132">Se usa para identificar cada mensaje de seguimiento como asociado con este.</span><span class="sxs-lookup"><span data-stu-id="e79e7-132">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e79e7-133"><strong>Aceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e79e7-133"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="e79e7-134">bit</span><span class="sxs-lookup"><span data-stu-id="e79e7-134">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e79e7-135">Puede ser TRUE o NULL.</span><span class="sxs-lookup"><span data-stu-id="e79e7-135">Can be TRUE or NULL.</span></span> <span data-ttu-id="e79e7-136">Si es verdadero, rechazar y cancelar será nulo.</span><span class="sxs-lookup"><span data-stu-id="e79e7-136">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e79e7-137"><strong>Rechace</strong></span><span class="sxs-lookup"><span data-stu-id="e79e7-137"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="e79e7-138">bit</span><span class="sxs-lookup"><span data-stu-id="e79e7-138">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e79e7-139">Puede ser TRUE o NULL.</span><span class="sxs-lookup"><span data-stu-id="e79e7-139">Can be TRUE or NULL.</span></span> <span data-ttu-id="e79e7-140">Si es verdadero, aceptar y cancelar será nulo.</span><span class="sxs-lookup"><span data-stu-id="e79e7-140">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e79e7-141"><strong>Cancelar.</strong></span><span class="sxs-lookup"><span data-stu-id="e79e7-141"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="e79e7-142">bit</span><span class="sxs-lookup"><span data-stu-id="e79e7-142">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e79e7-143">Puede ser TRUE o NULL.</span><span class="sxs-lookup"><span data-stu-id="e79e7-143">Can be TRUE or NULL.</span></span> <span data-ttu-id="e79e7-144">Si es verdadero, aceptar y rechazar serán NULOs.</span><span class="sxs-lookup"><span data-stu-id="e79e7-144">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e79e7-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e79e7-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

