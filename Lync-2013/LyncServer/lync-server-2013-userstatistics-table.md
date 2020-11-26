---
title: 'Lync Server 2013: tabla UserStatistics'
description: 'Lync Server 2013: tabla UserStatistics.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserStatistics table
ms:assetid: cfaf803b-1679-4169-92d3-533fad3e56ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721893(v=OCS.15)
ms:contentKeyID: 49733827
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 75b34fa3c34af4cc9cf2cacc6ae7feb4d217114c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436100"
---
# <a name="userstatistics-table-in-lync-server-2013"></a><span data-ttu-id="5be1b-103">Tabla UserStatistics en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5be1b-103">UserStatistics table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5be1b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5be1b-104">

<span> </span></span></span>

<span data-ttu-id="5be1b-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="5be1b-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="5be1b-106">La tabla UserStatistics es una tabla de soporte.</span><span class="sxs-lookup"><span data-stu-id="5be1b-106">The UserStatistics table is a supporting table.</span></span> <span data-ttu-id="5be1b-107">Cada registro de la tabla almacena información sobre el uso del sistema por un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="5be1b-107">Each record in the table stores information about an individual user’s usage of the system.</span></span> <span data-ttu-id="5be1b-108">Esta tabla se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5be1b-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5be1b-109">Columna</span><span class="sxs-lookup"><span data-stu-id="5be1b-109">Column</span></span></th>
<th><span data-ttu-id="5be1b-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5be1b-110">Data Type</span></span></th>
<th><span data-ttu-id="5be1b-111">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="5be1b-111">Key/Index</span></span></th>
<th><span data-ttu-id="5be1b-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="5be1b-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5be1b-113"><strong>Iddeusuario</strong></span><span class="sxs-lookup"><span data-stu-id="5be1b-113"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="5be1b-114">int</span><span class="sxs-lookup"><span data-stu-id="5be1b-114">int</span></span></p></td>
<td><p><span data-ttu-id="5be1b-115">Primary</span><span class="sxs-lookup"><span data-stu-id="5be1b-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="5be1b-116">Número único que identifica a este usuario.</span><span class="sxs-lookup"><span data-stu-id="5be1b-116">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5be1b-117"><strong>LastLogInTime</strong></span><span class="sxs-lookup"><span data-stu-id="5be1b-117"><strong>LastLogInTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5be1b-118">datetime</span><span class="sxs-lookup"><span data-stu-id="5be1b-118">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5be1b-119">La última vez que el usuario inició sesión.</span><span class="sxs-lookup"><span data-stu-id="5be1b-119">Last time the user logged in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5be1b-120"><strong>LastConfOrganizedTime</strong></span><span class="sxs-lookup"><span data-stu-id="5be1b-120"><strong>LastConfOrganizedTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5be1b-121">datetime</span><span class="sxs-lookup"><span data-stu-id="5be1b-121">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5be1b-122">La última vez que el usuario organizó una conferencia.</span><span class="sxs-lookup"><span data-stu-id="5be1b-122">Last time the user organized a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5be1b-123"><strong>LastCallOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="5be1b-123"><strong>LastCallOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5be1b-124">datetime</span><span class="sxs-lookup"><span data-stu-id="5be1b-124">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5be1b-125">La última vez que el usuario experimentó un error de llamada.</span><span class="sxs-lookup"><span data-stu-id="5be1b-125">Last time the user experienced a call failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5be1b-126"><strong>LastConfOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="5be1b-126"><strong>LastConfOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5be1b-127">datetime</span><span class="sxs-lookup"><span data-stu-id="5be1b-127">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5be1b-128">La última vez que el usuario experimentó un error de llamada como organizador de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="5be1b-128">Last time the user experienced a call failure as a conference organizer.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5be1b-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5be1b-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

