---
title: 'Lync Server 2013: vista ConferenceMessageCount'
description: 'Lync Server 2013: vista ConferenceMessageCount.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount view
ms:assetid: 8ee3ee95-fb78-4d4e-bcdd-6ce5a0a23b44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688129(v=OCS.15)
ms:contentKeyID: 49733727
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 212d6e1a346253809fb70806424350cc7fc0dfe2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434434"
---
# <a name="conferencemessagecount-view-in-lync-server-2013"></a><span data-ttu-id="858ee-103">Vista ConferenceMessageCount en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="858ee-103">ConferenceMessageCount view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="858ee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="858ee-104">

<span> </span></span></span>

<span data-ttu-id="858ee-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="858ee-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="858ee-106">La vista ConferenceMessageCount almacena información acerca de cuántos mensajes envió un usuario a una conferencia.</span><span class="sxs-lookup"><span data-stu-id="858ee-106">The ConferenceMessageCount view stores information about how many messages were sent by a user to a conference.</span></span> <span data-ttu-id="858ee-107">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="858ee-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="858ee-108">La vista ConferenceMessageCount contiene todas las columnas de la <A href="lync-server-2013-conferencesessiondetails-view.md">vista ConferenceSessionDetails de Lync Server 2013</A> , además de las columnas que figuran a continuación.</span><span class="sxs-lookup"><span data-stu-id="858ee-108">The ConferenceMessageCount view contains all of the columns in the <A href="lync-server-2013-conferencesessiondetails-view.md">ConferenceSessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="858ee-109">Columna</span><span class="sxs-lookup"><span data-stu-id="858ee-109">Column</span></span></th>
<th><span data-ttu-id="858ee-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="858ee-110">Data Type</span></span></th>
<th><span data-ttu-id="858ee-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="858ee-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="858ee-112"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="858ee-112"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="858ee-113">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="858ee-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="858ee-114">Identificador URI del usuario que envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="858ee-114">URI of the user who sent the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="858ee-115"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="858ee-115"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="858ee-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="858ee-116">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="858ee-117">Tipo de URI del usuario que envió los mensajes.</span><span class="sxs-lookup"><span data-stu-id="858ee-117">Type of URI of the user who sent the messages.</span></span> <span data-ttu-id="858ee-118">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="858ee-118">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="858ee-119"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="858ee-119"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="858ee-120">identificador</span><span class="sxs-lookup"><span data-stu-id="858ee-120">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="858ee-121">Espacio empresarial del usuario que envió los mensajes.</span><span class="sxs-lookup"><span data-stu-id="858ee-121">Tenant of user who sent the messages.</span></span> <span data-ttu-id="858ee-122">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="858ee-122">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="858ee-123"><strong>UserMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="858ee-123"><strong>UserMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="858ee-124">smallint</span><span class="sxs-lookup"><span data-stu-id="858ee-124">smallint</span></span></p></td>
<td><p><span data-ttu-id="858ee-125">Número de mensajes enviados por el usuario durante la sesión de conferencia.</span><span class="sxs-lookup"><span data-stu-id="858ee-125">Number of messages sent by the user during the conference session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="858ee-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="858ee-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

