---
title: 'Lync Server 2013: detalles de la vista de QoE'
description: 'Lync Server 2013: detalles de la vista de QoE.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE view details
ms:assetid: 6a658318-a317-4546-a44c-a9c473d8e86a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688081(v=OCS.15)
ms:contentKeyID: 49733677
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b20eb083295a5f3d3ecb5be7a8c96d9c4b7cfab2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398993"
---
# <a name="qoe-view-details-in-lync-server-2013"></a><span data-ttu-id="88ed4-103">Información general de la vista de calidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88ed4-103">QoE view details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88ed4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88ed4-104">

<span> </span></span></span>

<span data-ttu-id="88ed4-105">_**Última modificación del tema:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="88ed4-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="88ed4-106">Las vistas cubren los escenarios más comunes para devolver datos desde la base de datos SQL de calidad.</span><span class="sxs-lookup"><span data-stu-id="88ed4-106">Views cover the most common scenarios for returning data from the QoE SQL database.</span></span> <span data-ttu-id="88ed4-107">Se recomienda usar vistas para crear informes personalizados en lugar de obtener acceso directamente a las tablas de la base de datos; Esto se debe a que las vistas tienen más probabilidades de mantener la compatibilidad con versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="88ed4-107">It is recommended views used for building custom reports instead of directly accessing the database tables; that’s because views are more likely to maintain backwards compatibility with future releases.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88ed4-108">Nombre de la vista</span><span class="sxs-lookup"><span data-stu-id="88ed4-108">View Name</span></span></th>
<th><span data-ttu-id="88ed4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="88ed4-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88ed4-110"><a href="lync-server-2013-audiostreamdetail-view.md">Vista AudioStreamDetail en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="88ed4-110"><a href="lync-server-2013-audiostreamdetail-view.md">AudioStreamDetail view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="88ed4-111">Almacena información sobre cada secuencia de audio de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="88ed4-111">Stores information about each audio stream in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88ed4-112"><a href="lync-server-2013-medialine-view.md">Vista MediaLine en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="88ed4-112"><a href="lync-server-2013-medialine-view.md">MediaLine view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="88ed4-113">Almacena información sobre cada línea de medios de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="88ed4-113">Stores information about each media line in the database.</span></span> <span data-ttu-id="88ed4-114">Una sesión de audio normalmente contiene una línea multimedia de audio.</span><span class="sxs-lookup"><span data-stu-id="88ed4-114">One audio session typically contains one audio media line.</span></span> <span data-ttu-id="88ed4-115">Una sesión de audio y vídeo (A/V) normalmente contiene una línea de medio de audio y una línea de medio de vídeo; sin embargo, la sesión podría contener dos líneas multimedia de vídeo si se usa un dispositivo de conferencia o si se usa la vista de galería.</span><span class="sxs-lookup"><span data-stu-id="88ed4-115">One audio and video (A/V) session typically contains one audio media line and one video media line; however, the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88ed4-116"><a href="lync-server-2013-networkconfigurationsettings-view.md">Vista NetworkConfigurationSettings en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="88ed4-116"><a href="lync-server-2013-networkconfigurationsettings-view.md">NetworkConfigurationSettings view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="88ed4-117">Almacena información sobre la configuración de red.</span><span class="sxs-lookup"><span data-stu-id="88ed4-117">Stores information about the network configuration.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88ed4-118"><a href="lync-server-2013-session-view.md">Vista de sesión de Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="88ed4-118"><a href="lync-server-2013-session-view.md">Session view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="88ed4-119">Almacena información sobre las sesiones que tienen registros en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="88ed4-119">Stores information about sessions that have records in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88ed4-120"><a href="lync-server-2013-useragent-view.md">Vista UserAgent en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="88ed4-120"><a href="lync-server-2013-useragent-view.md">UserAgent view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="88ed4-121">Almacena información sobre los agentes de usuario implicados en las sesiones que tienen registros en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="88ed4-121">Stores information about the user agents that have been involved in sessions that have records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88ed4-122"><a href="lync-server-2013-videostreamdetail-view.md">Vista VideoStreamDetail en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="88ed4-122"><a href="lync-server-2013-videostreamdetail-view.md">VideoStreamDetail view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="88ed4-123">Almacena información sobre cada secuencia de vídeo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="88ed4-123">Stores information about each video stream in the database.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="88ed4-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88ed4-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

