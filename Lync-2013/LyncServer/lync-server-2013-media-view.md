---
title: 'Lync Server 2013: vista multimedia'
description: 'Lync Server 2013: vista de elementos multimedia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media view
ms:assetid: 1a7b2e59-082e-4188-98ae-48ae9bd3494a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687981(v=OCS.15)
ms:contentKeyID: 49733570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74643986b12a30b1055a46a37febf90eeb70c514
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446040"
---
# <a name="media-view-in-lync-server-2013"></a><span data-ttu-id="b8e4c-103">Vista de elementos multimedia de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8e4c-103">Media view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8e4c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8e4c-104">

<span> </span></span></span>

<span data-ttu-id="b8e4c-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="b8e4c-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="b8e4c-106">La vista multimedia almacena información sobre un tipo de medio usado en una sesión de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="b8e4c-106">The Media view stores information about one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="b8e4c-107">Una sesión estaría representada por varios registros de la tabla, si se usa más de un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b8e4c-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span> <span data-ttu-id="b8e4c-108">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b8e4c-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b8e4c-109">La vista de elementos multimedia no debe usarse para calcular la duración multimedia de una sesión.</span><span class="sxs-lookup"><span data-stu-id="b8e4c-109">The Media view should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="b8e4c-110">Esta vista contiene los detalles de señalización de intercambio de medios en una sesión.</span><span class="sxs-lookup"><span data-stu-id="b8e4c-110">This view contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="b8e4c-111">El intercambio de medios se realiza mediante la solicitud INVITE y StartTime indica el momento en que se envió la invitación. La hora de la invitación no significa necesariamente la hora de inicio del medio, porque los medios solo se inician una vez que se acepta la sesión.</span><span class="sxs-lookup"><span data-stu-id="b8e4c-111">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the session is accepted.</span></span>



</div>

<span data-ttu-id="b8e4c-112">La vista contenido multimedia contiene todas las columnas de la [vista SessionDetails de Lync Server 2013](lync-server-2013-sessiondetails-view.md) , además de las que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="b8e4c-112">The Media view contains all of the columns in the [SessionDetails view in Lync Server 2013](lync-server-2013-sessiondetails-view.md) in addition the ones listed below.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e4c-113">Columna</span><span class="sxs-lookup"><span data-stu-id="b8e4c-113">Column</span></span></th>
<th><span data-ttu-id="b8e4c-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b8e4c-114">Data Type</span></span></th>
<th><span data-ttu-id="b8e4c-115">Detalles</span><span class="sxs-lookup"><span data-stu-id="b8e4c-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8e4c-116"><strong>Media</strong></span><span class="sxs-lookup"><span data-stu-id="b8e4c-116"><strong>Media</strong></span></span></p></td>
<td><p><span data-ttu-id="b8e4c-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b8e4c-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b8e4c-118">Tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b8e4c-118">Media type.</span></span> <span data-ttu-id="b8e4c-119">Para obtener más información, consulte la <a href="lync-server-2013-medialist-table.md">tabla medial en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b8e4c-119">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8e4c-120"><strong>MediaStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="b8e4c-120"><strong>MediaStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b8e4c-121">datetime</span><span class="sxs-lookup"><span data-stu-id="b8e4c-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="b8e4c-122">Hora en que se envió una solicitud de medios.</span><span class="sxs-lookup"><span data-stu-id="b8e4c-122">Time that a media request was sent out.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8e4c-123"><strong>MediaEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="b8e4c-123"><strong>MediaEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b8e4c-124">datetime</span><span class="sxs-lookup"><span data-stu-id="b8e4c-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="b8e4c-125">Hora de finalización de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b8e4c-125">End time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b8e4c-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8e4c-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

