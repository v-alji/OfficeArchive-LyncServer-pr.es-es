---
title: 'Lync Server 2013: Tabla User'
description: 'Lync Server 2013: tabla de usuario.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User table
ms:assetid: 6b52047e-286d-47ab-b7bc-a9b266f62d82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398505(v=OCS.15)
ms:contentKeyID: 48184437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15d1ac08a229f4afea35a2727ef1105a5f24b826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444171"
---
# <a name="user-table-in-lync-server-2013"></a><span data-ttu-id="5d847-103">Tabla User en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d847-103">User table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d847-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d847-104">

<span> </span></span></span>

<span data-ttu-id="5d847-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="5d847-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="5d847-106">La tabla de usuario es una tabla de soporte que almacena una lista de los distintos usuarios que participaron en sesiones registradas en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5d847-106">The User table is a supporting table that stores a list of the various users who have participated in sessions recorded in the database.</span></span> <span data-ttu-id="5d847-107">Cada registro de la tabla representa un usuario.</span><span class="sxs-lookup"><span data-stu-id="5d847-107">Each record in the table represents one user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5d847-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="5d847-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="5d847-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="5d847-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="5d847-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="5d847-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="5d847-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="5d847-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d847-112"><strong>UserKey</strong></span><span class="sxs-lookup"><span data-stu-id="5d847-112"><strong>UserKey</strong></span></span></p></td>
<td><p><span data-ttu-id="5d847-113">int</span><span class="sxs-lookup"><span data-stu-id="5d847-113">int</span></span></p></td>
<td><p><span data-ttu-id="5d847-114">Primary</span><span class="sxs-lookup"><span data-stu-id="5d847-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="5d847-115">Número único que identifica a este usuario.</span><span class="sxs-lookup"><span data-stu-id="5d847-115">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d847-116"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="5d847-116"><strong>URI</strong></span></span></p></td>
<td><p><span data-ttu-id="5d847-117">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5d847-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5d847-118">Solo</span><span class="sxs-lookup"><span data-stu-id="5d847-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="5d847-119">Cadena URI.</span><span class="sxs-lookup"><span data-stu-id="5d847-119">URI string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d847-120"><strong>URIType</strong></span><span class="sxs-lookup"><span data-stu-id="5d847-120"><strong>URIType</strong></span></span></p></td>
<td><p><span data-ttu-id="5d847-121">int</span><span class="sxs-lookup"><span data-stu-id="5d847-121">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5d847-122">1 es un tipo de URI desconocido.</span><span class="sxs-lookup"><span data-stu-id="5d847-122">1 is unknown URI type.</span></span></p>
<p><span data-ttu-id="5d847-123">2 es el URI del usuario.</span><span class="sxs-lookup"><span data-stu-id="5d847-123">2 is user URI.</span></span></p>
<p><span data-ttu-id="5d847-124">4 es el URI de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="5d847-124">4 is conference URI.</span></span></p>
<p><span data-ttu-id="5d847-125">8 es el URI del teléfono.</span><span class="sxs-lookup"><span data-stu-id="5d847-125">8 is phone URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d847-126"><strong>TenantKey</strong></span><span class="sxs-lookup"><span data-stu-id="5d847-126"><strong>TenantKey</strong></span></span></p></td>
<td><p><span data-ttu-id="5d847-127">int</span><span class="sxs-lookup"><span data-stu-id="5d847-127">int</span></span></p></td>
<td><p><span data-ttu-id="5d847-128">Extranjero</span><span class="sxs-lookup"><span data-stu-id="5d847-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5d847-129">Espacio empresarial del usuario al que se hace referencia desde la tabla de inquilinos.</span><span class="sxs-lookup"><span data-stu-id="5d847-129">Tenant of the user, referenced from tenant table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d847-130"><strong>LastPoorCallTime</strong></span><span class="sxs-lookup"><span data-stu-id="5d847-130"><strong>LastPoorCallTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5d847-131">datetime</span><span class="sxs-lookup"><span data-stu-id="5d847-131">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5d847-132">Última marca de tiempo cuando el usuario tenía una mala llamada de audio.</span><span class="sxs-lookup"><span data-stu-id="5d847-132">Latest time stamp when the user had a poor audio call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d847-133"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="5d847-133"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="5d847-134">datetime</span><span class="sxs-lookup"><span data-stu-id="5d847-134">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5d847-135">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="5d847-135">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5d847-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d847-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

