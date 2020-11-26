---
title: 'Lync Server 2013: tabla SIPResponseMetaData'
description: 'Lync Server 2013: tabla SIPResponseMetaData.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SIPResponseMetaData table
ms:assetid: cf723737-4a75-4352-829b-f4954aa59716
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205294(v=OCS.15)
ms:contentKeyID: 48185510
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 402cff331f81a9b46028d76de69deeaace8d5ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444626"
---
# <a name="sipresponsemetadata-table-in-lync-server-2013"></a><span data-ttu-id="21993-103">Tabla SIPResponseMetaData en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21993-103">SIPResponseMetaData table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="21993-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="21993-104">

<span> </span></span></span>

<span data-ttu-id="21993-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="21993-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="21993-106">El SIPResponseMetaDataTable contiene una lista de códigos de respuesta SIP, así como la clasificación y la definición de cada uno de esos códigos.</span><span class="sxs-lookup"><span data-stu-id="21993-106">The SIPResponseMetaDataTable contains a list of SIP response codes and the classification and definition of each of those codes.</span></span> <span data-ttu-id="21993-107">Estos códigos se generan en respuesta a los eventos que afectan a los dispositivos SIP y a las sesiones de comunicación SIP; por ejemplo, el código de respuesta 403 se genera cuando un dispositivo SIP realiza una solicitud, pero el servidor no acepta la solicitud.</span><span class="sxs-lookup"><span data-stu-id="21993-107">These codes are generated in response to events affecting SIP devices and SIP communication sessions; for example, the response code 403 is generated when a SIP device makes a request, but the server declines to honor that request.</span></span>

<span data-ttu-id="21993-108">Esta tabla se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="21993-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21993-109">Columna</span><span class="sxs-lookup"><span data-stu-id="21993-109">Column</span></span></th>
<th><span data-ttu-id="21993-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="21993-110">Data Type</span></span></th>
<th><span data-ttu-id="21993-111">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="21993-111">Key/Index</span></span></th>
<th><span data-ttu-id="21993-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="21993-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21993-113"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="21993-113"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="21993-114">int</span><span class="sxs-lookup"><span data-stu-id="21993-114">int</span></span></p></td>
<td><p><span data-ttu-id="21993-115">Primary</span><span class="sxs-lookup"><span data-stu-id="21993-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="21993-116">Valor numérico que representa el código de respuesta SIP.</span><span class="sxs-lookup"><span data-stu-id="21993-116">Numeric value that represents the SIP response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21993-117"><strong>Las</strong></span><span class="sxs-lookup"><span data-stu-id="21993-117"><strong>Class</strong></span></span></p></td>
<td><p><span data-ttu-id="21993-118">int</span><span class="sxs-lookup"><span data-stu-id="21993-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="21993-119">Clasificación general para el código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="21993-119">General classification for the response code.</span></span> <span data-ttu-id="21993-120">Las clasificaciones incluyen:</span><span class="sxs-lookup"><span data-stu-id="21993-120">Classifications include:</span></span></p>
<ul>
<li><p><span data-ttu-id="21993-121">1: respuestas informativas</span><span class="sxs-lookup"><span data-stu-id="21993-121">1 – Informational Responses</span></span></p></li>
<li><p><span data-ttu-id="21993-122">2: respuestas correctas</span><span class="sxs-lookup"><span data-stu-id="21993-122">2 – Successful Responses</span></span></p></li>
<li><p><span data-ttu-id="21993-123">3: respuestas de redireccionamiento</span><span class="sxs-lookup"><span data-stu-id="21993-123">3 – Redirection Responses</span></span></p></li>
<li><p><span data-ttu-id="21993-124">4-respuestas de error del cliente</span><span class="sxs-lookup"><span data-stu-id="21993-124">4 – Client Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="21993-125">5--respuestas de error de servidor</span><span class="sxs-lookup"><span data-stu-id="21993-125">5 -- Server Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="21993-126">6: respuesta de error global</span><span class="sxs-lookup"><span data-stu-id="21993-126">6 – Global Failure Response</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21993-127"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="21993-127"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="21993-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="21993-128">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="21993-129">Descripción del código de respuesta SIP.</span><span class="sxs-lookup"><span data-stu-id="21993-129">Description of the SIP response code.</span></span> <span data-ttu-id="21993-130">Por ejemplo, el código de respuesta 181 tiene la siguiente descripción:</span><span class="sxs-lookup"><span data-stu-id="21993-130">For example, response code 181 has the following description:</span></span></p>
<p><span data-ttu-id="21993-131">La llamada se está reenviando</span><span class="sxs-lookup"><span data-stu-id="21993-131">Call Is Being Forwarded</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="21993-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="21993-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

