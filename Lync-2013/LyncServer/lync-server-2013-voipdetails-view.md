---
title: 'Lync Server 2013: vista VoIPDetails'
description: 'Lync Server 2013: vista VoIPDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoIPDetails view
ms:assetid: 14c44736-71ba-4fc5-82c7-1df65bf6261c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687973(v=OCS.15)
ms:contentKeyID: 49733561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ecd34be0c8568eef29d773f088e8503a8065743
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446187"
---
# <a name="voipdetails-view-in-lync-server-2013"></a><span data-ttu-id="3480f-103">Vista VoIPDetails en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3480f-103">VoIPDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3480f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3480f-104">

<span> </span></span></span>

<span data-ttu-id="3480f-105">_**Última modificación del tema:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="3480f-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="3480f-106">La vista VoIPDetails almacena información sobre sesiones de punto a punto, donde al menos un usuario es un usuario de VoIP.</span><span class="sxs-lookup"><span data-stu-id="3480f-106">The VoIPDetails view stores information about peer-to-peer sessions, where at least one user is a VoIP user.</span></span> <span data-ttu-id="3480f-107">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3480f-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3480f-108">La vista VoIPDetails contiene todas las columnas de la <A href="lync-server-2013-sessiondetails-view.md">vista SessionDetails de Lync Server 2013</A> , además de las columnas que figuran a continuación.</span><span class="sxs-lookup"><span data-stu-id="3480f-108">The VoIPDetails view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3480f-109">Columna</span><span class="sxs-lookup"><span data-stu-id="3480f-109">Column</span></span></th>
<th><span data-ttu-id="3480f-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3480f-110">Data Type</span></span></th>
<th><span data-ttu-id="3480f-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="3480f-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3480f-112"><strong>FromPhone</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-112"><strong>FromPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="3480f-113">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="3480f-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="3480f-114">URI de teléfono del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="3480f-114">Phone URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3480f-115"><strong>Teléfono</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-115"><strong>ToPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="3480f-116">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="3480f-116">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="3480f-117">URI de teléfono del usuario que se unió a la sesión.</span><span class="sxs-lookup"><span data-stu-id="3480f-117">Phone URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3480f-118"><strong>DisconnectedByUri</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-118"><strong>DisconnectedByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="3480f-119">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="3480f-119">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="3480f-120">URI del usuario que desconectó la sesión.</span><span class="sxs-lookup"><span data-stu-id="3480f-120">URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3480f-121"><strong>DisconnectedByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-121"><strong>DisconnectedByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="3480f-122">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="3480f-122">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="3480f-123">Tipo de URI del usuario que ha desconectado la sesión.</span><span class="sxs-lookup"><span data-stu-id="3480f-123">Type of URI of the user who disconnected the session.</span></span> <span data-ttu-id="3480f-124">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3480f-124">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3480f-125"><strong>DisconnectedByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-125"><strong>DisconnectedByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="3480f-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="3480f-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="3480f-127">Espacio empresarial del usuario que desconectó la sesión.</span><span class="sxs-lookup"><span data-stu-id="3480f-127">Tenant of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3480f-128"><strong>DisconnectedByPhone</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-128"><strong>DisconnectedByPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="3480f-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="3480f-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="3480f-130">URI de teléfono del usuario que desconectó la sesión.</span><span class="sxs-lookup"><span data-stu-id="3480f-130">Phone URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3480f-131"><strong>FromMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-131"><strong>FromMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="3480f-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="3480f-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="3480f-133">Servidor de mediación usado por el usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="3480f-133">Mediation Server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3480f-134"><strong>ToMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-134"><strong>ToMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="3480f-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="3480f-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="3480f-136">Servidor de mediación usado por el usuario que se unió a la sesión.</span><span class="sxs-lookup"><span data-stu-id="3480f-136">Mediation Server used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3480f-137"><strong>FromGateway</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-137"><strong>FromGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="3480f-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="3480f-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="3480f-139">Puerta de enlace usada por el usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="3480f-139">Gateway used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3480f-140"><strong>ToGateway</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-140"><strong>ToGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="3480f-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="3480f-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="3480f-142">Puerta de enlace usada por el usuario que se unió a la sesión.</span><span class="sxs-lookup"><span data-stu-id="3480f-142">Gateway used by the user who joined the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3480f-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3480f-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

