---
title: 'Lync Server 2013: vista FileTransfers'
description: 'Lync Server 2013: vista FileTransfers.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers view
ms:assetid: e52c3ad0-152e-4a18-af1c-1aff0d205151
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721914(v=OCS.15)
ms:contentKeyID: 49733848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd2b084274a4d5daa093f2269617214f703ac03e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428156"
---
# <a name="filetransfers-view-in-lync-server-2013"></a><span data-ttu-id="28880-103">Vista FileTransfers en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="28880-103">FileTransfers view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="28880-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="28880-104">

<span> </span></span></span>

<span data-ttu-id="28880-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="28880-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="28880-106">La vista FileTransfer almacena información sobre las sesiones de transferencia de archivos de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="28880-106">The FileTransfer view stores information about peer-to-peer file transfer sessions.</span></span> <span data-ttu-id="28880-107">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="28880-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="28880-108">La vista FileTransfers contiene todas las columnas de la <A href="lync-server-2013-sessiondetails-view.md">vista SessionDetails de Lync Server 2013</A> , además de las columnas que figuran a continuación.</span><span class="sxs-lookup"><span data-stu-id="28880-108">The FileTransfers view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28880-109">Columna</span><span class="sxs-lookup"><span data-stu-id="28880-109">Column</span></span></th>
<th><span data-ttu-id="28880-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="28880-110">Data Type</span></span></th>
<th><span data-ttu-id="28880-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="28880-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28880-112"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="28880-112"><strong>FileName</strong></span></span></p></td>
<td><p><span data-ttu-id="28880-113">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="28880-113">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="28880-114">Nombre del archivo transferido.</span><span class="sxs-lookup"><span data-stu-id="28880-114">Name of the file transferred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28880-115"><strong>Ésta</strong></span><span class="sxs-lookup"><span data-stu-id="28880-115"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="28880-116">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="28880-116">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="28880-117">Se usa para identificar cada mensaje de seguimiento como asociado con este.</span><span class="sxs-lookup"><span data-stu-id="28880-117">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28880-118"><strong>FileIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="28880-118"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="28880-119">identificador</span><span class="sxs-lookup"><span data-stu-id="28880-119">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="28880-120">Identificador único para distinguir entre transferencias de archivos que impliquen el mismo nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="28880-120">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28880-121"><strong>Aceptable</strong></span><span class="sxs-lookup"><span data-stu-id="28880-121"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="28880-122">bit</span><span class="sxs-lookup"><span data-stu-id="28880-122">bit</span></span></p></td>
<td><p><span data-ttu-id="28880-123">Puede ser TRUE o NULL.</span><span class="sxs-lookup"><span data-stu-id="28880-123">Can be TRUE or NULL.</span></span> <span data-ttu-id="28880-124">Si es verdadero, rechazar y cancelar será nulo.</span><span class="sxs-lookup"><span data-stu-id="28880-124">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28880-125"><strong>Rechace</strong></span><span class="sxs-lookup"><span data-stu-id="28880-125"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="28880-126">bit</span><span class="sxs-lookup"><span data-stu-id="28880-126">bit</span></span></p></td>
<td><p><span data-ttu-id="28880-127">Puede ser TRUE o NULL.</span><span class="sxs-lookup"><span data-stu-id="28880-127">Can be TRUE or NULL.</span></span> <span data-ttu-id="28880-128">Si es verdadero, aceptar y cancelar será nulo.</span><span class="sxs-lookup"><span data-stu-id="28880-128">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28880-129"><strong>Cancelar.</strong></span><span class="sxs-lookup"><span data-stu-id="28880-129"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="28880-130">bit</span><span class="sxs-lookup"><span data-stu-id="28880-130">bit</span></span></p></td>
<td><p><span data-ttu-id="28880-131">Puede ser TRUE o NULL.</span><span class="sxs-lookup"><span data-stu-id="28880-131">Can be TRUE or NULL.</span></span> <span data-ttu-id="28880-132">Si es verdadero, aceptar y rechazar serán NULOs.</span><span class="sxs-lookup"><span data-stu-id="28880-132">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="28880-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="28880-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

