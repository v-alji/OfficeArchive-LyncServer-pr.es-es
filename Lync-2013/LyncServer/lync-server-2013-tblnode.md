---
title: 'Lync Server 2013: tblNode'
description: 'Lync Server 2013: tblNode'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblNode
ms:assetid: a31d2961-aa83-4286-a12e-15d279c95f19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615024(v=OCS.15)
ms:contentKeyID: 48184960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0a5d630621c32cbc54501249c7a679bf4023c60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423522"
---
# <a name="tblnode-in-lync-server-2013"></a><span data-ttu-id="1d9a2-103">tblNode en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d9a2-103">tblNode in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1d9a2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1d9a2-104">

<span> </span></span></span>

<span data-ttu-id="1d9a2-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="1d9a2-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="1d9a2-106">tblNode contiene el árbol de objetos (con nodos de categoría o de salón de chat) tal como se administra en el panel de control y los cmdlets administrativos de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-106">tblNode contains the object tree (with category or chat room nodes) as managed in the Lync Server 2013 Control Panel and administrative cmdlets.</span></span>

### <a name="columns"></a><span data-ttu-id="1d9a2-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="1d9a2-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1d9a2-108">Columna</span><span class="sxs-lookup"><span data-stu-id="1d9a2-108">Column</span></span></th>
<th><span data-ttu-id="1d9a2-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d9a2-109">Type</span></span></th>
<th><span data-ttu-id="1d9a2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d9a2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-111">nodeID</span><span class="sxs-lookup"><span data-stu-id="1d9a2-111">nodeID</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-112">int, not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-113">IDENTIFICADOR de nodo (número único).</span><span class="sxs-lookup"><span data-stu-id="1d9a2-113">Node ID (unique number).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9a2-114">nodeGuid</span><span class="sxs-lookup"><span data-stu-id="1d9a2-114">nodeGuid</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-115">GUID, not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-116">GUID de nodo.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-116">Node GUID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-117">parentID</span><span class="sxs-lookup"><span data-stu-id="1d9a2-117">parentID</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-118">int</span><span class="sxs-lookup"><span data-stu-id="1d9a2-118">int</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-119">IDENTIFICADOR de nodo del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-119">Node ID of parent.</span></span> <span data-ttu-id="1d9a2-120">El nodo raíz (con identificador 1) también se incluye como principal.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-120">The root node (with ID 1) includes itself as parent as well.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9a2-121">Nodo</span><span class="sxs-lookup"><span data-stu-id="1d9a2-121">nodeType</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-122">bit, not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-122">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-123">True si el nodo es una categoría.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-123">True if the node is a category.</span></span></p>
<p><span data-ttu-id="1d9a2-124">Falso si el nodo es un salón de chat.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-124">False if the node is a chat room.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-125">nombreDeNodo</span><span class="sxs-lookup"><span data-stu-id="1d9a2-125">nodeName</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-126">nvarchar (256), not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-126">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-127">Nombre del nodo.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-127">Node name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9a2-128">nodeDesc</span><span class="sxs-lookup"><span data-stu-id="1d9a2-128">nodeDesc</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-129">nvarchar (256), not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-129">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-130">Descripción del nodo.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-130">Node description.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-131">recibir</span><span class="sxs-lookup"><span data-stu-id="1d9a2-131">invite</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-132">bit</span><span class="sxs-lookup"><span data-stu-id="1d9a2-132">bit</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-133">Para las categorías:</span><span class="sxs-lookup"><span data-stu-id="1d9a2-133">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="1d9a2-134">True si los invitados están activados.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-134">True if invites are on.</span></span></p></li>
<li><p><span data-ttu-id="1d9a2-135">False si los invitados están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-135">False if invites are off.</span></span></p></li>
</ul>
<p><span data-ttu-id="1d9a2-136">Para salas:</span><span class="sxs-lookup"><span data-stu-id="1d9a2-136">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="1d9a2-137">False si los invitados están deshabilitados (reemplaza la categoría principal).</span><span class="sxs-lookup"><span data-stu-id="1d9a2-137">False if invites are off (overrides the parent category).</span></span></p></li>
<li><p><span data-ttu-id="1d9a2-138">NULL si la configuración de invitados se hereda de la categoría principal.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-138">Null if the invites setting is inherited from the parent category.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9a2-139">conectarse</span><span class="sxs-lookup"><span data-stu-id="1d9a2-139">logged</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-140">bit</span><span class="sxs-lookup"><span data-stu-id="1d9a2-140">bit</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-141">Para las categorías:</span><span class="sxs-lookup"><span data-stu-id="1d9a2-141">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="1d9a2-142">True si el historial de chat está activado.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-142">True if chat history is on.</span></span></p></li>
<li><p><span data-ttu-id="1d9a2-143">Falso si el historial de conversaciones está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-143">False if chat history is off.</span></span></p></li>
</ul>
<p><span data-ttu-id="1d9a2-144">Para salas:</span><span class="sxs-lookup"><span data-stu-id="1d9a2-144">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="1d9a2-145">Valor.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-145">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-146">filePost</span><span class="sxs-lookup"><span data-stu-id="1d9a2-146">filePost</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-147">bit</span><span class="sxs-lookup"><span data-stu-id="1d9a2-147">bit</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-148">Para las categorías:</span><span class="sxs-lookup"><span data-stu-id="1d9a2-148">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="1d9a2-149">True si se permiten las cargas de archivos.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-149">True if file uploads are allowed.</span></span></p></li>
<li><p><span data-ttu-id="1d9a2-150">False si no se permiten las cargas de archivos.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-150">False if file uploads are disallowed.</span></span></p></li>
</ul>
<p><span data-ttu-id="1d9a2-151">Para salas:</span><span class="sxs-lookup"><span data-stu-id="1d9a2-151">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="1d9a2-152">Valor.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-152">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9a2-153">habilitar</span><span class="sxs-lookup"><span data-stu-id="1d9a2-153">disabled</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-154">bit, not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-154">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-155">True si el salón de chat está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-155">True if the chat room is disabled.</span></span> <span data-ttu-id="1d9a2-156">Solo se aplica a salones de chat.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-156">Applies only to chat rooms.</span></span> <span data-ttu-id="1d9a2-157">(Falso para categorías).</span><span class="sxs-lookup"><span data-stu-id="1d9a2-157">(False for categories.)</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9a2-158">problema</span><span class="sxs-lookup"><span data-stu-id="1d9a2-158">behavior</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-159">smallint, not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-159">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-160">Comportamiento (que se busca en la tabla EnumValue):</span><span class="sxs-lookup"><span data-stu-id="1d9a2-160">Behavior (looked up in EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="1d9a2-161">4: normal (salones de chat normales).</span><span class="sxs-lookup"><span data-stu-id="1d9a2-161">4: Normal (normal chat rooms).</span></span></p></li>
<li><p><span data-ttu-id="1d9a2-162">5: auditorio (salones de chat de Auditorio; solo los moderadores pueden contribuir).</span><span class="sxs-lookup"><span data-stu-id="1d9a2-162">5: Auditorium (auditorium chat rooms, only presenters can contribute).</span></span></p></li>
</ul>
<p><span data-ttu-id="1d9a2-163">Solo se aplica a salones de chat.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-163">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-164">visión</span><span class="sxs-lookup"><span data-stu-id="1d9a2-164">visibility</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-165">smallint, not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-165">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-166">Visibilidad (en la tabla EnumValue):</span><span class="sxs-lookup"><span data-stu-id="1d9a2-166">Visibility (looked up on EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="1d9a2-167">2: privado</span><span class="sxs-lookup"><span data-stu-id="1d9a2-167">2: Private</span></span></p></li>
<li><p><span data-ttu-id="1d9a2-168">3: ámbito</span><span class="sxs-lookup"><span data-stu-id="1d9a2-168">3: Scoped</span></span></p></li>
<li><p><span data-ttu-id="1d9a2-169">6: abrir</span><span class="sxs-lookup"><span data-stu-id="1d9a2-169">6: Open</span></span></p></li>
</ul>
<p><span data-ttu-id="1d9a2-170">Solo se aplica a salones de chat.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-170">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9a2-171">siopID</span><span class="sxs-lookup"><span data-stu-id="1d9a2-171">siopID</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-172">Identificador único global</span><span class="sxs-lookup"><span data-stu-id="1d9a2-172">GUID</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-173">Add-In GUID si un complemento está asociado con este salón de chat.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-173">Add-In GUID if an add-in is associated with this chat room.</span></span> <span data-ttu-id="1d9a2-174">(Las categorías no tienen complementos).</span><span class="sxs-lookup"><span data-stu-id="1d9a2-174">(Categories do not have add-ins.)</span></span></p>
<p><span data-ttu-id="1d9a2-175">La información del complemento se busca en la tabla SiopWhiteList.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-175">The add-in information is looked up in SiopWhiteList table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-176">nodeAddedBy</span><span class="sxs-lookup"><span data-stu-id="1d9a2-176">nodeAddedBy</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-177">int, not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-177">int, not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-178">IDENTIFICADOR de la entidad de identidad que creó este nodo.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-178">ID of the principal that created this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9a2-179">nodeAddedOn</span><span class="sxs-lookup"><span data-stu-id="1d9a2-179">nodeAddedOn</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-180">BIGINT, not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-180">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-181">Marca de tiempo de la creación del nodo.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-181">Time stamp of the node creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-182">nodeUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="1d9a2-182">nodeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-183">int, not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-183">int, not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-184">IDENTIFICADOR de la entidad de identidad que realizó la última actualización de este nodo.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-184">ID of the principal that did the latest update of this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9a2-185">nodeUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="1d9a2-185">nodeUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-186">BIGINT, not null</span><span class="sxs-lookup"><span data-stu-id="1d9a2-186">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-187">Marca de tiempo de la última actualización de este nodo.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-187">Time stamp of the latest update of this node.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-188">purgedOn</span><span class="sxs-lookup"><span data-stu-id="1d9a2-188">purgedOn</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-189">datetime</span><span class="sxs-lookup"><span data-stu-id="1d9a2-189">datetime</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-190">Hora de la última operación de purga (eliminación de ámbitos de la tabla tblScopedPrincipal y roles de la tabla tblPrincipalRole) que afectó a este nodo.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-190">Time of the latest purge operation (removal of scopes from tblScopedPrincipal table and roles from tblPrincipalRole table) that affected this node.</span></span> <span data-ttu-id="1d9a2-191">Lo usa el mecanismo de actualización de la caché interna del servicio de chat.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-191">This is used by the Chat service’s internal cache update mechanism.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="1d9a2-192">Sus</span><span class="sxs-lookup"><span data-stu-id="1d9a2-192">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1d9a2-193">Columna</span><span class="sxs-lookup"><span data-stu-id="1d9a2-193">Column</span></span></th>
<th><span data-ttu-id="1d9a2-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d9a2-194">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-195">nodeID</span><span class="sxs-lookup"><span data-stu-id="1d9a2-195">nodeID</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-196">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-196">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9a2-197">problema</span><span class="sxs-lookup"><span data-stu-id="1d9a2-197">behavior</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-198">Clave externa con la búsqueda en la tabla tblEnumValue. valueID.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-198">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-199">visión</span><span class="sxs-lookup"><span data-stu-id="1d9a2-199">visibility</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-200">Clave externa con la búsqueda en la tabla tblEnumValue. valueID.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-200">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9a2-201">parentID</span><span class="sxs-lookup"><span data-stu-id="1d9a2-201">parentID</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-202">Clave externa con la búsqueda en la tabla tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-202">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d9a2-203">siopID</span><span class="sxs-lookup"><span data-stu-id="1d9a2-203">siopID</span></span></p></td>
<td><p><span data-ttu-id="1d9a2-204">Clave externa con la búsqueda en la tabla tblSiopWhiteList. siopId.</span><span class="sxs-lookup"><span data-stu-id="1d9a2-204">Foreign key with lookup in tblSiopWhiteList.siopId table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1d9a2-205">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1d9a2-205">


</div>

<span> </span>

</div>

</div>

</span></span></div>

