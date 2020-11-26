---
title: 'Lync Server 2013: tblLastChatId'
description: 'Lync Server 2013: tblLastChatId'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblLastChatId
ms:assetid: 17a4ffbe-cca9-4ec5-ae46-38a15274889a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558616(v=OCS.15)
ms:contentKeyID: 48183513
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69e80a735e70c8a03441038f5e58eb93e0af1f82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444430"
---
# <a name="tbllastchatid-in-lync-server-2013"></a><span data-ttu-id="42632-103">tblLastChatId en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42632-103">tblLastChatId in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42632-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42632-104">

<span> </span></span></span>

<span data-ttu-id="42632-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="42632-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="42632-106">tblLastChatId contiene el último identificador de chat generado (y usado en la tabla tblChat) para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="42632-106">tblLastChatId contains the last chat ID that was generated (and used in the tblChat table) for each user.</span></span>

### <a name="columns"></a><span data-ttu-id="42632-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="42632-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="42632-108">Columna</span><span class="sxs-lookup"><span data-stu-id="42632-108">Column</span></span></th>
<th><span data-ttu-id="42632-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="42632-109">Type</span></span></th>
<th><span data-ttu-id="42632-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="42632-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42632-111">nodeID</span><span class="sxs-lookup"><span data-stu-id="42632-111">nodeID</span></span></p></td>
<td><p><span data-ttu-id="42632-112">int, not null</span><span class="sxs-lookup"><span data-stu-id="42632-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="42632-113">IDENTIFICADOR de nodo (solo tipo salón de chat).</span><span class="sxs-lookup"><span data-stu-id="42632-113">Node ID (chat room-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42632-114">lastChatID</span><span class="sxs-lookup"><span data-stu-id="42632-114">lastChatID</span></span></p></td>
<td><p><span data-ttu-id="42632-115">BIGINT, not null</span><span class="sxs-lookup"><span data-stu-id="42632-115">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="42632-116">Último ID de chat usado.</span><span class="sxs-lookup"><span data-stu-id="42632-116">Last used chat ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="42632-117">Sus</span><span class="sxs-lookup"><span data-stu-id="42632-117">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="42632-118">Columna</span><span class="sxs-lookup"><span data-stu-id="42632-118">Column</span></span></th>
<th><span data-ttu-id="42632-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="42632-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42632-120">&lt;nodeID, lastChatID&gt;</span><span class="sxs-lookup"><span data-stu-id="42632-120">&lt;nodeID, lastChatID&gt;</span></span></p></td>
<td><p><span data-ttu-id="42632-121">Clave principal (solo nodeID es suficiente para procesar).</span><span class="sxs-lookup"><span data-stu-id="42632-121">Primary key (just nodeID is sufficient for processing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42632-122">nodeID</span><span class="sxs-lookup"><span data-stu-id="42632-122">nodeID</span></span></p></td>
<td><p><span data-ttu-id="42632-123">Clave externa con la búsqueda en la tabla tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="42632-123">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="42632-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="42632-124">See Also</span></span>


[<span data-ttu-id="42632-125">tblChat en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42632-125">tblChat in Lync Server 2013</span></span>](lync-server-2013-tblchat.md)  
  

<span data-ttu-id="42632-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42632-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

