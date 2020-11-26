---
title: 'Lync Server 2013: tblConfig'
description: 'Lync Server 2013: tblConfig'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblConfig
ms:assetid: 7445e7db-c574-46fa-b964-8640d77047a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558663(v=OCS.15)
ms:contentKeyID: 48184515
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8990e0b2c8724a5e90c36e706b92f9985f288772
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444465"
---
# <a name="tblconfig-in-lync-server-2013"></a><span data-ttu-id="cdecc-103">tblConfig en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cdecc-103">tblConfig in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cdecc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cdecc-104">

<span> </span></span></span>

<span data-ttu-id="cdecc-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="cdecc-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="cdecc-106">tblConfig contiene la configuración no admitida de un servidor de chat persistente, en una fila.</span><span class="sxs-lookup"><span data-stu-id="cdecc-106">tblConfig contains some Persistent Chat Server unsupported configuration, in one row.</span></span>

### <a name="columns"></a><span data-ttu-id="cdecc-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="cdecc-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cdecc-108">Columna</span><span class="sxs-lookup"><span data-stu-id="cdecc-108">Column</span></span></th>
<th><span data-ttu-id="cdecc-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="cdecc-109">Type</span></span></th>
<th><span data-ttu-id="cdecc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdecc-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdecc-111">configLabel</span><span class="sxs-lookup"><span data-stu-id="cdecc-111">configLabel</span></span></p></td>
<td><p><span data-ttu-id="cdecc-112">nvarchar (255), not null</span><span class="sxs-lookup"><span data-stu-id="cdecc-112">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="cdecc-113">Contiene el &quot; grupo.&quot;</span><span class="sxs-lookup"><span data-stu-id="cdecc-113">Contains &quot;pool.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdecc-114">configContent</span><span class="sxs-lookup"><span data-stu-id="cdecc-114">configContent</span></span></p></td>
<td><p><span data-ttu-id="cdecc-115">nvarchar (Max)</span><span class="sxs-lookup"><span data-stu-id="cdecc-115">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="cdecc-116">Contenido de configuración.</span><span class="sxs-lookup"><span data-stu-id="cdecc-116">Configuration content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdecc-117">configPoolID</span><span class="sxs-lookup"><span data-stu-id="cdecc-117">configPoolID</span></span></p></td>
<td><p><span data-ttu-id="cdecc-118">GUID, not null</span><span class="sxs-lookup"><span data-stu-id="cdecc-118">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="cdecc-119">IDENTIFICADOR único de la instancia de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdecc-119">Unique ID of the database instance.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="cdecc-120">Clave</span><span class="sxs-lookup"><span data-stu-id="cdecc-120">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cdecc-121">Columna</span><span class="sxs-lookup"><span data-stu-id="cdecc-121">Column</span></span></th>
<th><span data-ttu-id="cdecc-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdecc-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdecc-123">configLabel</span><span class="sxs-lookup"><span data-stu-id="cdecc-123">configLabel</span></span></p></td>
<td><p><span data-ttu-id="cdecc-124">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="cdecc-124">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cdecc-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cdecc-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

