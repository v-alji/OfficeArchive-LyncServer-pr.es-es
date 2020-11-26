---
title: 'Lync Server 2013: Tabla ConferenceMessageCount'
description: 'Lync Server 2013: tabla ConferenceMessageCount.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount table
ms:assetid: 78569dbf-5217-42fa-ba1a-4380f56e2a3d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398590(v=OCS.15)
ms:contentKeyID: 48184570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 271b654c09ab1aef194eb613e660de208aea1534
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434455"
---
# <a name="conferencemessagecount-table-in-lync-server-2013"></a><span data-ttu-id="2db6c-103">Tabla ConferenceMessageCount en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2db6c-103">ConferenceMessageCount table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2db6c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2db6c-104">

<span> </span></span></span>

<span data-ttu-id="2db6c-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="2db6c-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="2db6c-106">Cada registro de esta tabla representa un usuario en una conferencia de mensajería instantánea e incluye el número de mensajes enviados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2db6c-106">Each record in this table represents one user in one IM conference and includes the number of messages sent by that user.</span></span> <span data-ttu-id="2db6c-107">Cada conferencia está representada por varios registros en esta tabla; un registro para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="2db6c-107">Each conference is represented by multiple records in this table; one record for each user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2db6c-108">Columna</span><span class="sxs-lookup"><span data-stu-id="2db6c-108">Column</span></span></th>
<th><span data-ttu-id="2db6c-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2db6c-109">Data Type</span></span></th>
<th><span data-ttu-id="2db6c-110">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="2db6c-110">Key/Index</span></span></th>
<th><span data-ttu-id="2db6c-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="2db6c-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2db6c-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="2db6c-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2db6c-113">datetime</span><span class="sxs-lookup"><span data-stu-id="2db6c-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="2db6c-114">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="2db6c-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="2db6c-115">Hora de la instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="2db6c-115">Time of conference instance.</span></span> <span data-ttu-id="2db6c-116">Se usa junto con <strong>SessionIdSeq</strong> para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="2db6c-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="2db6c-117">Para obtener más información, vea la <a href="lync-server-2013-conferences-table.md">tabla conferencias en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="2db6c-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2db6c-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="2db6c-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="2db6c-119">int</span><span class="sxs-lookup"><span data-stu-id="2db6c-119">int</span></span></p></td>
<td><p><span data-ttu-id="2db6c-120">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="2db6c-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="2db6c-121">Número de identificación para identificar la instancia de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="2db6c-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="2db6c-122">Se usa junto con <strong>SessionIdTime</strong> para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="2db6c-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="2db6c-123">Para obtener más información, vea la <a href="lync-server-2013-conferences-table.md">tabla conferencias en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="2db6c-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2db6c-124"><strong>Iddeusuario</strong></span><span class="sxs-lookup"><span data-stu-id="2db6c-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="2db6c-125">int</span><span class="sxs-lookup"><span data-stu-id="2db6c-125">int</span></span></p></td>
<td><p><span data-ttu-id="2db6c-126">Extranjero</span><span class="sxs-lookup"><span data-stu-id="2db6c-126">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2db6c-127">Número único que identifica a este usuario, al que se hace referencia en la <a href="lync-server-2013-users-table.md">tabla usuarios de Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="2db6c-127">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2db6c-128"><strong>MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="2db6c-128"><strong>MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="2db6c-129">smallint</span><span class="sxs-lookup"><span data-stu-id="2db6c-129">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="2db6c-130">El número de mensajes enviados por este usuario durante esta conferencia.</span><span class="sxs-lookup"><span data-stu-id="2db6c-130">The number of messages sent by this user during this conference.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2db6c-131">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2db6c-131">


</div>

<span> </span>

</div>

</div>

</span></span></div>

