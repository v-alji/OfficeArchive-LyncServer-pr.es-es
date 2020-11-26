---
title: 'Lync Server 2013: vista ProgressReport'
description: 'Lync Server 2013: vista ProgressReport.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport view
ms:assetid: b49f3fc7-0e2f-498f-8505-aaaf54e435f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721857(v=OCS.15)
ms:contentKeyID: 49733790
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b95086012f254499644e778e43cafdf70ffc8f9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436856"
---
# <a name="progressreport-view-in-lync-server-2013"></a><span data-ttu-id="3db0d-103">Vista ProgressReport en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3db0d-103">ProgressReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3db0d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3db0d-104">

<span> </span></span></span>

<span data-ttu-id="3db0d-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="3db0d-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="3db0d-106">La vista ProgressReport almacena información sobre las sesiones completadas.</span><span class="sxs-lookup"><span data-stu-id="3db0d-106">The ProgressReport view stores information about completed sessions.</span></span> <span data-ttu-id="3db0d-107">Los informes de progreso solo se escribirán para las llamadas y las sesiones que la 2013 determina Lync Server puede resultar útil para propósitos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="3db0d-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span> <span data-ttu-id="3db0d-108">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3db0d-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3db0d-109">Los campos ErrorTime, ErrorReportSeq y ProgressReportSeq no hacen referencia a errores sino a mensajes que indican el estado de las llamadas o los mensajes.</span><span class="sxs-lookup"><span data-stu-id="3db0d-109">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3db0d-110">Columna</span><span class="sxs-lookup"><span data-stu-id="3db0d-110">Column</span></span></th>
<th><span data-ttu-id="3db0d-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3db0d-111">Data Type</span></span></th>
<th><span data-ttu-id="3db0d-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="3db0d-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3db0d-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="3db0d-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3db0d-114">datetime</span><span class="sxs-lookup"><span data-stu-id="3db0d-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="3db0d-115">Hora de error.</span><span class="sxs-lookup"><span data-stu-id="3db0d-115">Time of error occurred.</span></span> <span data-ttu-id="3db0d-116">Se usa junto con ErrorReportSeq para identificar de forma única un error.</span><span class="sxs-lookup"><span data-stu-id="3db0d-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db0d-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="3db0d-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="3db0d-118">int</span><span class="sxs-lookup"><span data-stu-id="3db0d-118">int</span></span></p></td>
<td><p><span data-ttu-id="3db0d-119">Número de identificación para identificar el error.</span><span class="sxs-lookup"><span data-stu-id="3db0d-119">ID number to identify the error.</span></span> <span data-ttu-id="3db0d-120">Se usa junto con ErrorTime para identificar de forma única un error.</span><span class="sxs-lookup"><span data-stu-id="3db0d-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db0d-121"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="3db0d-121"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="3db0d-122">int</span><span class="sxs-lookup"><span data-stu-id="3db0d-122">int</span></span></p></td>
<td><p><span data-ttu-id="3db0d-123">IDENTIFICADOR para identificar el informe de progreso.</span><span class="sxs-lookup"><span data-stu-id="3db0d-123">ID to identify the progress report.</span></span> <span data-ttu-id="3db0d-124">Se usa para distinguir los informes de progreso del mismo informe de errores.</span><span class="sxs-lookup"><span data-stu-id="3db0d-124">Used to distinguish progress reports of the same error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db0d-125"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="3db0d-125"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="3db0d-126">int</span><span class="sxs-lookup"><span data-stu-id="3db0d-126">int</span></span></p></td>
<td><p><span data-ttu-id="3db0d-127">IDENTIFICADOR de diagnóstico del informe de errores.</span><span class="sxs-lookup"><span data-stu-id="3db0d-127">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db0d-128"><strong>Origen</strong></span><span class="sxs-lookup"><span data-stu-id="3db0d-128"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="3db0d-129">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="3db0d-129">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="3db0d-130">Nombre del servidor que originó el error (si el informe fue enviado desde un componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="3db0d-130">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db0d-131"><strong>Aplicación</strong></span><span class="sxs-lookup"><span data-stu-id="3db0d-131"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="3db0d-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="3db0d-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="3db0d-133">Nombre de la aplicación que originó el error (si el informe fue enviado desde un componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="3db0d-133">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db0d-134"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="3db0d-134"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="3db0d-135">identificador</span><span class="sxs-lookup"><span data-stu-id="3db0d-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="3db0d-136">Identificador único que correlaciona información de tiempo de Unión para los distintos componentes implicados en una conferencia.</span><span class="sxs-lookup"><span data-stu-id="3db0d-136">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db0d-137"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="3db0d-137"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3db0d-138">int</span><span class="sxs-lookup"><span data-stu-id="3db0d-138">int</span></span></p></td>
<td><p><span data-ttu-id="3db0d-139">Tiempo (en milisegundos) necesario para que un componente específico se una a una conferencia.</span><span class="sxs-lookup"><span data-stu-id="3db0d-139">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db0d-140"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="3db0d-140"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="3db0d-141">VARCHAR (Max)</span><span class="sxs-lookup"><span data-stu-id="3db0d-141">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="3db0d-142">Información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="3db0d-142">Additional error information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3db0d-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3db0d-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

