---
title: 'Lync Server 2013: vista ClientVersions'
description: 'Lync Server 2013: vista ClientVersions.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ClientVersions view
ms:assetid: caf7678f-83a0-46c8-83cc-fee4c3991f52
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721891(v=OCS.15)
ms:contentKeyID: 49733825
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42ede7107a59db3162ac7f5344e47e81a80d57df
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434735"
---
# <a name="clientversions-view-in-lync-server-2013"></a><span data-ttu-id="47132-103">Vista ClientVersions en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47132-103">ClientVersions view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47132-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47132-104">

<span> </span></span></span>

<span data-ttu-id="47132-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="47132-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="47132-106">La vista ClientVersions almacena información sobre los diversos tipos y versiones de los clientes que participaron en sesiones registradas en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="47132-106">The ClientVersions view stores information about the various client types and versions that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="47132-107">Cada registro de la vista representa una versión de cliente.</span><span class="sxs-lookup"><span data-stu-id="47132-107">Each record in the view represents one client version.</span></span> <span data-ttu-id="47132-108">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="47132-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="47132-109">Es posible que haya varios registros para determinadas columnas.</span><span class="sxs-lookup"><span data-stu-id="47132-109">There may be multiple records for certain columns.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47132-110">Columna</span><span class="sxs-lookup"><span data-stu-id="47132-110">Column</span></span></th>
<th><span data-ttu-id="47132-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="47132-111">Data Type</span></span></th>
<th><span data-ttu-id="47132-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="47132-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47132-113"><strong>VersionId</strong></span><span class="sxs-lookup"><span data-stu-id="47132-113"><strong>VersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="47132-114">int</span><span class="sxs-lookup"><span data-stu-id="47132-114">int</span></span></p></td>
<td><p><span data-ttu-id="47132-115">Número único que identifica este tipo de cliente y versión.</span><span class="sxs-lookup"><span data-stu-id="47132-115">Unique number identifying this client type and version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47132-116"><strong>Versión</strong></span><span class="sxs-lookup"><span data-stu-id="47132-116"><strong>Version</strong></span></span></p></td>
<td><p><span data-ttu-id="47132-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="47132-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="47132-118">Representa el agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="47132-118">Represents the user agent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47132-119"><strong>Tipocliente</strong></span><span class="sxs-lookup"><span data-stu-id="47132-119"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="47132-120">int</span><span class="sxs-lookup"><span data-stu-id="47132-120">int</span></span></p></td>
<td><p><span data-ttu-id="47132-121">Tipo de cliente.</span><span class="sxs-lookup"><span data-stu-id="47132-121">Type of client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47132-122"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="47132-122"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="47132-123">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="47132-123">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="47132-124">Categoría a la que pertenece el cliente.</span><span class="sxs-lookup"><span data-stu-id="47132-124">Category that the client belongs to.</span></span> <span data-ttu-id="47132-125">Por ejemplo, el cliente Conferencing_Attendant_1.0 pertenece a la CAA de ClientCategory.</span><span class="sxs-lookup"><span data-stu-id="47132-125">For example, the client Conferencing_Attendant_1.0 belongs to the ClientCategory CAA.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="47132-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47132-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

