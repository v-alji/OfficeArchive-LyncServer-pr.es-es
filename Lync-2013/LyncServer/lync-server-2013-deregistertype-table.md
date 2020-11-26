---
title: 'Lync Server 2013: Tabla DeRegisterType'
description: 'Lync Server 2013: tabla DeRegisterType.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DeRegisterType table
ms:assetid: 09148118-6209-4fd7-a494-99118689a245
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398142(v=OCS.15)
ms:contentKeyID: 48183346
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: afad63c2abeba3e91565e07dac75d0ac6c96ca3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429562"
---
# <a name="deregistertype-table-in-lync-server-2013"></a><span data-ttu-id="07869-103">Tabla DeRegisterType en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07869-103">DeRegisterType table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07869-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07869-104">

<span> </span></span></span>

<span data-ttu-id="07869-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="07869-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="07869-106">La tabla DeRegisterType es una tabla estática que almacena la lista de posibles tipos de registros de usuario, como ' cliente iniciado ', ' registro expirado ' o ' cliente ha dejado de responder '.</span><span class="sxs-lookup"><span data-stu-id="07869-106">The DeRegisterType table is a static table that stores the list of possible user de-registers types, such as ‘client initiated’, ‘registration expired’, or ‘client stopped responding.’</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07869-107">Columna</span><span class="sxs-lookup"><span data-stu-id="07869-107">Column</span></span></th>
<th><span data-ttu-id="07869-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="07869-108">Data Type</span></span></th>
<th><span data-ttu-id="07869-109">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="07869-109">Key/Index</span></span></th>
<th><span data-ttu-id="07869-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="07869-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07869-111"><strong>DeRegisterTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="07869-111"><strong>DeRegisterTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="07869-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="07869-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="07869-113">Primary</span><span class="sxs-lookup"><span data-stu-id="07869-113">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07869-114"><strong>DeRegisterReason</strong></span><span class="sxs-lookup"><span data-stu-id="07869-114"><strong>DeRegisterReason</strong></span></span></p></td>
<td><p><span data-ttu-id="07869-115">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="07869-115">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="07869-116">Valores permitidos:</span><span class="sxs-lookup"><span data-stu-id="07869-116">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="07869-117">0--desconocido</span><span class="sxs-lookup"><span data-stu-id="07869-117">0 -- Unknown</span></span></p></li>
<li><p><span data-ttu-id="07869-118">1: deregistro Iniciado por el cliente</span><span class="sxs-lookup"><span data-stu-id="07869-118">1 -- Client Initiated Deregistration</span></span></p></li>
<li><p><span data-ttu-id="07869-119">2--registro expirado</span><span class="sxs-lookup"><span data-stu-id="07869-119">2 -- Registration Expired</span></span></p></li>
<li><p><span data-ttu-id="07869-120">3: cliente bloqueado</span><span class="sxs-lookup"><span data-stu-id="07869-120">3 – Client crashed</span></span></p></li>
<li><p><span data-ttu-id="07869-121">4: atributos de usuario modificados</span><span class="sxs-lookup"><span data-stu-id="07869-121">4 -- User Attributes Changed</span></span></p></li>
<li><p><span data-ttu-id="07869-122">5: se cambió la entidad de registro preferida</span><span class="sxs-lookup"><span data-stu-id="07869-122">5 – Preferred Registrar Changed</span></span></p></li>
<li><p><span data-ttu-id="07869-123">6--cliente heredado en modo de supervivencia</span><span class="sxs-lookup"><span data-stu-id="07869-123">6 -- Legacy Client In Survival Mode</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="07869-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07869-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

