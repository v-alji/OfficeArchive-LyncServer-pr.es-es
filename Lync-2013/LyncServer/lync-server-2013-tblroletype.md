---
title: 'Lync Server 2013: tblRoleType'
description: 'Lync Server 2013: tblRoleType'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblRoleType
ms:assetid: 1eac3a54-656a-40ac-b771-edfc64d6e34b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558623(v=OCS.15)
ms:contentKeyID: 48183577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f458259acaee7821d5f6a7339b993c70fe65f595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398076"
---
# <a name="tblroletype-in-lync-server-2013"></a><span data-ttu-id="78872-103">tblRoleType en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78872-103">tblRoleType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78872-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78872-104">

<span> </span></span></span>

<span data-ttu-id="78872-105">_**Última modificación del tema:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="78872-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="78872-106">tblRoleType es una tabla de búsqueda estática con tipos de roles y sus conjuntos de permisos asociados.</span><span class="sxs-lookup"><span data-stu-id="78872-106">tblRoleType is a static lookup table with role types and their associated permission sets.</span></span>

### <a name="columns"></a><span data-ttu-id="78872-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="78872-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78872-108">Columna</span><span class="sxs-lookup"><span data-stu-id="78872-108">Column</span></span></th>
<th><span data-ttu-id="78872-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="78872-109">Type</span></span></th>
<th><span data-ttu-id="78872-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="78872-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78872-111">rtypeID</span><span class="sxs-lookup"><span data-stu-id="78872-111">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="78872-112">int, not null</span><span class="sxs-lookup"><span data-stu-id="78872-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="78872-113">IDENTIFICADOR de tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="78872-113">Role type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78872-114">rtypeDesc</span><span class="sxs-lookup"><span data-stu-id="78872-114">rtypeDesc</span></span></p></td>
<td><p><span data-ttu-id="78872-115">nvarchar (256), not null</span><span class="sxs-lookup"><span data-stu-id="78872-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="78872-116">Descripción de tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="78872-116">Role type description.</span></span> <span data-ttu-id="78872-117">Hay cuatro roles disponibles:</span><span class="sxs-lookup"><span data-stu-id="78872-117">There are four available roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="78872-118">Miembro: miembro del salón de chat</span><span class="sxs-lookup"><span data-stu-id="78872-118">Member: Chat room member</span></span></p></li>
<li><p><span data-ttu-id="78872-119">Administrador: administrador del salón de chat</span><span class="sxs-lookup"><span data-stu-id="78872-119">Manager: Chat room manager</span></span></p></li>
<li><p><span data-ttu-id="78872-120">Voz: moderador de un salón de chat de Auditorio</span><span class="sxs-lookup"><span data-stu-id="78872-120">Voiced: Presenter for an auditorium chat room</span></span></p></li>
<li><p><span data-ttu-id="78872-121">Creador: puede crear salones de chat</span><span class="sxs-lookup"><span data-stu-id="78872-121">Creator: Can create chat rooms</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78872-122">rtypeAllowedPermSet</span><span class="sxs-lookup"><span data-stu-id="78872-122">rtypeAllowedPermSet</span></span></p></td>
<td><p><span data-ttu-id="78872-123">BIGINT, not null</span><span class="sxs-lookup"><span data-stu-id="78872-123">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="78872-124">Conjunto de permisos para el rol.</span><span class="sxs-lookup"><span data-stu-id="78872-124">Permission set for the role.</span></span> <span data-ttu-id="78872-125">Los bits utilizados son:</span><span class="sxs-lookup"><span data-stu-id="78872-125">The used bits are:</span></span></p>
<ul>
<li><p><span data-ttu-id="78872-126">2: verdadero si el rol puede administrar nodos.</span><span class="sxs-lookup"><span data-stu-id="78872-126">2: True if the role can manage nodes.</span></span></p></li>
<li><p><span data-ttu-id="78872-127">4: true si el rol puede crear nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="78872-127">4: True if the role can create children nodes.</span></span></p></li>
<li><p><span data-ttu-id="78872-128">7: verdadero si el rol puede unirse a un salón de chat (o a salones de chat de niños de una categoría).</span><span class="sxs-lookup"><span data-stu-id="78872-128">7: True if the role can join a chat room (or children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="78872-129">8: verdadero si el rol puede chatear en un salón de chat (o en los salones de chat de los niños de una categoría).</span><span class="sxs-lookup"><span data-stu-id="78872-129">8: True if the role can chat in a chat room (or in children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="78872-130">10: verdadero si el rol puede leer el historial de chats incluso cuando no está unido a un salón de chat.</span><span class="sxs-lookup"><span data-stu-id="78872-130">10: True if the role can read chat history even when not joined to a chat room.</span></span></p></li>
<li><p><span data-ttu-id="78872-131">11: verdadero si el rol puede ver el salón de chat.</span><span class="sxs-lookup"><span data-stu-id="78872-131">11: True if the role can see the chat room.</span></span> <span data-ttu-id="78872-132">(Esto se ha refinado con factores como el alcance y la visibilidad).</span><span class="sxs-lookup"><span data-stu-id="78872-132">(This is further refined by factors such as scope and visibility.)</span></span></p></li>
<li><p><span data-ttu-id="78872-133">12: verdadero si el rol puede chatear en un salón de chat de Auditorio.</span><span class="sxs-lookup"><span data-stu-id="78872-133">12: True if the role can chat in an auditorium chat room.</span></span></p></li>
<li><p><span data-ttu-id="78872-134">13: verdadero si el rol puede omitir las reglas de visibilidad al ver los nodos.</span><span class="sxs-lookup"><span data-stu-id="78872-134">13: True if the role can bypass visibility rules when viewing nodes.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="78872-135">Clave</span><span class="sxs-lookup"><span data-stu-id="78872-135">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78872-136">Columna</span><span class="sxs-lookup"><span data-stu-id="78872-136">Column</span></span></th>
<th><span data-ttu-id="78872-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="78872-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78872-138">rtypeID</span><span class="sxs-lookup"><span data-stu-id="78872-138">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="78872-139">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="78872-139">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="78872-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78872-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

