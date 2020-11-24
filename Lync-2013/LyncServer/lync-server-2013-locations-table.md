---
title: 'Lync Server 2013: Tabla Locations'
description: 'Lync Server 2013: tabla de ubicaciones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Locations table
ms:assetid: 78dc1b14-5394-4f8e-89d3-4ba593272a04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398596(v=OCS.15)
ms:contentKeyID: 48184579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d07b6d3d3820f4efb3310adf0734a7e10c53e6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399833"
---
# <a name="locations-table-in-lync-server-2013"></a><span data-ttu-id="70ff2-103">Tabla Locations en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="70ff2-103">Locations table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70ff2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70ff2-104">

<span> </span></span></span>

<span data-ttu-id="70ff2-105">_**Última modificación del tema:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="70ff2-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="70ff2-106">Cada registro representa una referencia de una ubicación en una llamada de emergencia, como una llamada de E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="70ff2-106">Each record represents one location reference in an emergency call, like an E9-1-1 call.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70ff2-107">Columna</span><span class="sxs-lookup"><span data-stu-id="70ff2-107">Column</span></span></th>
<th><span data-ttu-id="70ff2-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="70ff2-108">Data Type</span></span></th>
<th><span data-ttu-id="70ff2-109">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="70ff2-109">Key/Index</span></span></th>
<th><span data-ttu-id="70ff2-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="70ff2-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70ff2-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="70ff2-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="70ff2-112">datetime</span><span class="sxs-lookup"><span data-stu-id="70ff2-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="70ff2-113">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="70ff2-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="70ff2-114">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="70ff2-114">Time of session request.</span></span> <span data-ttu-id="70ff2-115">Se usa en conjunción con <strong>SessionIdSeq</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="70ff2-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="70ff2-116">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="70ff2-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70ff2-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="70ff2-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="70ff2-118">int</span><span class="sxs-lookup"><span data-stu-id="70ff2-118">int</span></span></p></td>
<td><p><span data-ttu-id="70ff2-119">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="70ff2-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="70ff2-120">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="70ff2-120">ID number to identify the session.</span></span> <span data-ttu-id="70ff2-121">Se usa en conjunción con <strong>SessionIdTime</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="70ff2-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="70ff2-122">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="70ff2-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70ff2-123"><strong>Ubicación</strong></span><span class="sxs-lookup"><span data-stu-id="70ff2-123"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="70ff2-124">nvarchar (Max)</span><span class="sxs-lookup"><span data-stu-id="70ff2-124">nvarchar(max)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="70ff2-125">Ubicación de la llamada de emergencia.</span><span class="sxs-lookup"><span data-stu-id="70ff2-125">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="70ff2-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70ff2-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

