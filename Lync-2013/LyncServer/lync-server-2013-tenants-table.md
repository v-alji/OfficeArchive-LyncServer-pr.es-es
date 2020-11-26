---
title: 'Lync Server 2013: Tabla Tenants'
description: 'Lync Server 2013: tabla de inquilinos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Tenants table
ms:assetid: c1b070c1-2c59-4ca9-910b-43f673f97fda
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412950(v=OCS.15)
ms:contentKeyID: 48185309
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96025dfd9fb42a6083f7f3daca98e243f01a8516
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441287"
---
# <a name="tenants-table-in-lync-server-2013"></a><span data-ttu-id="418e8-103">Tabla Tenants en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418e8-103">Tenants table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="418e8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="418e8-104">

<span> </span></span></span>

<span data-ttu-id="418e8-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="418e8-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="418e8-106">La tabla de inquilinos es una tabla de soporte que almacena una lista de los distintos inquilinos.</span><span class="sxs-lookup"><span data-stu-id="418e8-106">The Tenants table is a supporting table that stores a list of the various tenants.</span></span> <span data-ttu-id="418e8-107">Cada registro de la tabla representa un inquilino.</span><span class="sxs-lookup"><span data-stu-id="418e8-107">Each record in the table represents one tenant.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="418e8-108">En la implementación local, CDR usa el identificador de inquilino de la compilación para indicar un tipo de autenticación diferente, como la conectividad de mensajería instantánea pública, federada y anónima.</span><span class="sxs-lookup"><span data-stu-id="418e8-108">In on-premises deployment, CDR uses the build-in Tenant ID to indicate different authentication type, such as public IM connectivity, Federated and Anonymous.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="418e8-109">Columna</span><span class="sxs-lookup"><span data-stu-id="418e8-109">Column</span></span></th>
<th><span data-ttu-id="418e8-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="418e8-110">Data Type</span></span></th>
<th><span data-ttu-id="418e8-111">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="418e8-111">Key/Index</span></span></th>
<th><span data-ttu-id="418e8-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="418e8-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="418e8-113"><strong>TenantId</strong></span><span class="sxs-lookup"><span data-stu-id="418e8-113"><strong>TenantId</strong></span></span></p></td>
<td><p><span data-ttu-id="418e8-114">int</span><span class="sxs-lookup"><span data-stu-id="418e8-114">int</span></span></p></td>
<td><p><span data-ttu-id="418e8-115">Primary</span><span class="sxs-lookup"><span data-stu-id="418e8-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="418e8-116">Número único que identifica este ID de inquilino.</span><span class="sxs-lookup"><span data-stu-id="418e8-116">Unique number identifying this Tenant ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e8-117"><strong>TenantKey</strong></span><span class="sxs-lookup"><span data-stu-id="418e8-117"><strong>TenantKey</strong></span></span></p></td>
<td><p><span data-ttu-id="418e8-118">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="418e8-118">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="418e8-119">Valores permitidos:</span><span class="sxs-lookup"><span data-stu-id="418e8-119">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="418e8-120">00000000-0000-0000-0000-000000000000-Enterprise</span><span class="sxs-lookup"><span data-stu-id="418e8-120">00000000-0000-0000-0000-000000000000 – Enterprise</span></span></p></li>
<li><p><span data-ttu-id="418e8-121">00000000-0000-0000-0000-000000000001: federado</span><span class="sxs-lookup"><span data-stu-id="418e8-121">00000000-0000-0000-0000-000000000001 – Federated</span></span></p></li>
<li><p><span data-ttu-id="418e8-122">00000000-0000-0000-0000-000000000002: anónimo</span><span class="sxs-lookup"><span data-stu-id="418e8-122">00000000-0000-0000-0000-000000000002 – Anonymous</span></span></p></li>
<li><p><span data-ttu-id="418e8-123">00000000-0000-0000-0000-000000000003: conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="418e8-123">00000000-0000-0000-0000-000000000003 – Public IM connectivity</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="418e8-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="418e8-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

