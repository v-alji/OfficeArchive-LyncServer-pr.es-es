---
title: 'Lync Server 2013: tblFileToken'
description: 'Lync Server 2013: tblFileToken'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblFileToken
ms:assetid: 49e7dd79-1607-443c-818a-88c160e4ed06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558646(v=OCS.15)
ms:contentKeyID: 48184073
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c0a0465bd769cff5c23c00a98f79e2346232175
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423536"
---
# <a name="tblfiletoken-in-lync-server-2013"></a><span data-ttu-id="b3576-103">tblFileToken en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3576-103">tblFileToken in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3576-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3576-104">

<span> </span></span></span>

<span data-ttu-id="b3576-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="b3576-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="b3576-106">tblFileToken contiene tokens temporales para la transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="b3576-106">tblFileToken contains temporary tokens for file transfer purposes.</span></span>

### <a name="columns"></a><span data-ttu-id="b3576-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="b3576-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3576-108">Columna</span><span class="sxs-lookup"><span data-stu-id="b3576-108">Column</span></span></th>
<th><span data-ttu-id="b3576-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3576-109">Type</span></span></th>
<th><span data-ttu-id="b3576-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3576-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3576-111">fileToken</span><span class="sxs-lookup"><span data-stu-id="b3576-111">fileToken</span></span></p></td>
<td><p><span data-ttu-id="b3576-112">nvarchar (50), not null</span><span class="sxs-lookup"><span data-stu-id="b3576-112">nvarchar (50), not null</span></span></p></td>
<td><p><span data-ttu-id="b3576-113">Identificador exclusivo (un GUID).</span><span class="sxs-lookup"><span data-stu-id="b3576-113">Unique token (a GUID).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3576-114">fileTokenUserID</span><span class="sxs-lookup"><span data-stu-id="b3576-114">fileTokenUserID</span></span></p></td>
<td><p><span data-ttu-id="b3576-115">int, not null</span><span class="sxs-lookup"><span data-stu-id="b3576-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="b3576-116">IDENTIFICADOR de la entidad de identidad que está transfiriendo el archivo.</span><span class="sxs-lookup"><span data-stu-id="b3576-116">ID of the principal that is transferring the file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3576-117">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="b3576-117">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="b3576-118">GUID, not null</span><span class="sxs-lookup"><span data-stu-id="b3576-118">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="b3576-119">GUID del nodo del salón de chat.</span><span class="sxs-lookup"><span data-stu-id="b3576-119">GUID of the chat room node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3576-120">fileTokenExpireDate</span><span class="sxs-lookup"><span data-stu-id="b3576-120">fileTokenExpireDate</span></span></p></td>
<td><p><span data-ttu-id="b3576-121">DateTime, not null</span><span class="sxs-lookup"><span data-stu-id="b3576-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="b3576-122">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="b3576-122">Expiration time.</span></span> <span data-ttu-id="b3576-123">(Los tokens vencen después de 30 minutos, a menos que se hayan anclado (vea las siguientes descripciones en esta columna).</span><span class="sxs-lookup"><span data-stu-id="b3576-123">(Tokens expire after 30 minutes, unless pinned (see the following descriptions in this column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3576-124">fileTokenComplianceFileUrl</span><span class="sxs-lookup"><span data-stu-id="b3576-124">fileTokenComplianceFileUrl</span></span></p></td>
<td><p><span data-ttu-id="b3576-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b3576-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b3576-126">Dirección URL del archivo transferido (para el uso del servicio de cumplimiento).</span><span class="sxs-lookup"><span data-stu-id="b3576-126">URL of the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3576-127">fileTokenComplianceThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="b3576-127">fileTokenComplianceThumbnailUrl</span></span></p></td>
<td><p><span data-ttu-id="b3576-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b3576-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b3576-129">Dirección URL de la miniatura del archivo transferido (para el uso del servicio de cumplimiento).</span><span class="sxs-lookup"><span data-stu-id="b3576-129">URL of the thumbnail for the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3576-130">fileTokenComplianceTime</span><span class="sxs-lookup"><span data-stu-id="b3576-130">fileTokenComplianceTime</span></span></p></td>
<td><p><span data-ttu-id="b3576-131">datetime2</span><span class="sxs-lookup"><span data-stu-id="b3576-131">datetime2</span></span></p></td>
<td><p><span data-ttu-id="b3576-132">Marca de hora para la operación de transferencia de archivos real (para el uso del servicio de cumplimiento).</span><span class="sxs-lookup"><span data-stu-id="b3576-132">Timestamp for the actual file transfer operation (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3576-133">fileTokenComplianceIsUpload</span><span class="sxs-lookup"><span data-stu-id="b3576-133">fileTokenComplianceIsUpload</span></span></p></td>
<td><p><span data-ttu-id="b3576-134">bit</span><span class="sxs-lookup"><span data-stu-id="b3576-134">bit</span></span></p></td>
<td><p><span data-ttu-id="b3576-135">Es verdadero si se carga; Falso si descargar (para uso del servicio de cumplimiento).</span><span class="sxs-lookup"><span data-stu-id="b3576-135">True if upload; False if download (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3576-136">fileTokenCompliancePinned</span><span class="sxs-lookup"><span data-stu-id="b3576-136">fileTokenCompliancePinned</span></span></p></td>
<td><p><span data-ttu-id="b3576-137">bit, not null</span><span class="sxs-lookup"><span data-stu-id="b3576-137">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="b3576-138">True si el símbolo está anclado.</span><span class="sxs-lookup"><span data-stu-id="b3576-138">True if token is pinned.</span></span> <span data-ttu-id="b3576-139">Se usa para mantener el token en la tabla hasta que el servicio de cumplimiento tiene la posibilidad de recuperar los campos correspondientes de él.</span><span class="sxs-lookup"><span data-stu-id="b3576-139">It’s used to keep the token in the table until Compliance service has a chance to retrieve the relevant fields from it.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="b3576-140">Sus</span><span class="sxs-lookup"><span data-stu-id="b3576-140">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3576-141">Columna</span><span class="sxs-lookup"><span data-stu-id="b3576-141">Column</span></span></th>
<th><span data-ttu-id="b3576-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3576-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3576-143">fileToken</span><span class="sxs-lookup"><span data-stu-id="b3576-143">fileToken</span></span></p></td>
<td><p><span data-ttu-id="b3576-144">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="b3576-144">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3576-145">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="b3576-145">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="b3576-146">Clave externa con la búsqueda en la tabla tblNode. nodeGuid.</span><span class="sxs-lookup"><span data-stu-id="b3576-146">Foreign key with lookup in tblNode.nodeGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b3576-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3576-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

