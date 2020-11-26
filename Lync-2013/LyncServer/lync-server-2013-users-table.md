---
title: 'Lync Server 2013: Tabla Users'
description: 'Lync Server 2013: tabla usuarios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Users table
ms:assetid: a8d71373-4b57-4245-9f02-f7fc0d9fcd3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412791(v=OCS.15)
ms:contentKeyID: 48185032
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b1418e162a04e46ee0dfeca082aa66b0665fc77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436184"
---
# <a name="users-table-in-lync-server-2013"></a><span data-ttu-id="09e45-103">Tabla Users en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09e45-103">Users table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09e45-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09e45-104">

<span> </span></span></span>

<span data-ttu-id="09e45-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="09e45-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="09e45-106">La tabla usuarios es una tabla de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="09e45-106">The Users table is a supporting table.</span></span> <span data-ttu-id="09e45-107">Cada registro de la tabla almacena información acerca de un usuario implicado en llamadas o sesiones que tienen registros en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="09e45-107">Each record in the table stores information about one user involved in calls or sessions that have records in the database.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09e45-108">Columna</span><span class="sxs-lookup"><span data-stu-id="09e45-108">Column</span></span></th>
<th><span data-ttu-id="09e45-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="09e45-109">Data Type</span></span></th>
<th><span data-ttu-id="09e45-110">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="09e45-110">Key/Index</span></span></th>
<th><span data-ttu-id="09e45-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="09e45-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09e45-112"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="09e45-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="09e45-113">datetime</span><span class="sxs-lookup"><span data-stu-id="09e45-113">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="09e45-114">Marca de tiempo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="09e45-114">Time stamp for internal use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09e45-115"><strong>Iddeusuario</strong></span><span class="sxs-lookup"><span data-stu-id="09e45-115"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="09e45-116">int</span><span class="sxs-lookup"><span data-stu-id="09e45-116">int</span></span></p></td>
<td><p><span data-ttu-id="09e45-117">Primary</span><span class="sxs-lookup"><span data-stu-id="09e45-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="09e45-118">Número único que identifica a este usuario.</span><span class="sxs-lookup"><span data-stu-id="09e45-118">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09e45-119"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="09e45-119"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="09e45-120">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="09e45-120">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="09e45-121">URI de usuario.</span><span class="sxs-lookup"><span data-stu-id="09e45-121">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09e45-122"><strong>TenantId</strong></span><span class="sxs-lookup"><span data-stu-id="09e45-122"><strong>TenantId</strong></span></span></p></td>
<td><p><span data-ttu-id="09e45-123">int</span><span class="sxs-lookup"><span data-stu-id="09e45-123">int</span></span></p></td>
<td><p><span data-ttu-id="09e45-124">Extranjero</span><span class="sxs-lookup"><span data-stu-id="09e45-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="09e45-125">El identificador de inquilino de este usuario.</span><span class="sxs-lookup"><span data-stu-id="09e45-125">This user’s Tenant ID.</span></span> <span data-ttu-id="09e45-126">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="09e45-126">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09e45-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="09e45-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="09e45-128">int</span><span class="sxs-lookup"><span data-stu-id="09e45-128">int</span></span></p></td>
<td><p><span data-ttu-id="09e45-129">Extranjero</span><span class="sxs-lookup"><span data-stu-id="09e45-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="09e45-130">Tipo de URI de este usuario.</span><span class="sxs-lookup"><span data-stu-id="09e45-130">This user’s URI type.</span></span> <span data-ttu-id="09e45-131">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="09e45-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="09e45-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09e45-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

