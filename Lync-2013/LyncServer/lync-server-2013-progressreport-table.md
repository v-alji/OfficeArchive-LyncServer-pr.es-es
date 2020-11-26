---
title: 'Lync Server 2013: Tabla ProgressReport'
description: 'Lync Server 2013: tabla ProgressReport.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport table
ms:assetid: 38e5f060-5e9b-4185-87b2-7ef61c4bb75f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425864(v=OCS.15)
ms:contentKeyID: 48183847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d36ee2ab75410ea2462da4b647ef5b45afefb1bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436870"
---
# <a name="progressreport-table-in-lync-server-2013"></a><span data-ttu-id="9d3fb-103">Tabla ProgressReport en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9d3fb-103">ProgressReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d3fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d3fb-104">

<span> </span></span></span>

<span data-ttu-id="9d3fb-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="9d3fb-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="9d3fb-106">Los informes de progreso se basan en los datos cargados por el cliente en la base de datos después de completarse una llamada o sesión.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-106">Progress reports are based on data uploaded by the client to the database after a call or session is completed.</span></span> <span data-ttu-id="9d3fb-107">Los informes de progreso solo se escribirán para las llamadas y las sesiones que la 2013 determina Lync Server puede resultar útil para propósitos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span>

<span data-ttu-id="9d3fb-108">Los campos ErrorTime, ErrorReportSeq y ProgressReportSeq no hacen referencia a errores sino a mensajes que indican el estado de las llamadas o los mensajes.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-108">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d3fb-109">Columna</span><span class="sxs-lookup"><span data-stu-id="9d3fb-109">Column</span></span></th>
<th><span data-ttu-id="9d3fb-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9d3fb-110">Data Type</span></span></th>
<th><span data-ttu-id="9d3fb-111">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="9d3fb-111">Key/Index</span></span></th>
<th><span data-ttu-id="9d3fb-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="9d3fb-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d3fb-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="9d3fb-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9d3fb-114">datetime</span><span class="sxs-lookup"><span data-stu-id="9d3fb-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="9d3fb-115">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="9d3fb-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d3fb-116">Fecha y hora del informe de errores de progreso que contiene este informe de progreso.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-116">Date and time of the progress error report that contains this progress report.</span></span> <span data-ttu-id="9d3fb-117">Para obtener más información, consulte la <a href="lync-server-2013-errorreport-table.md">tabla errorreport en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9d3fb-117">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d3fb-118"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="9d3fb-118"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d3fb-119">int</span><span class="sxs-lookup"><span data-stu-id="9d3fb-119">int</span></span></p></td>
<td><p><span data-ttu-id="9d3fb-120">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="9d3fb-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d3fb-121">Número de identificación usado en conjunción con ErrorTime, ProgressReportSeq para identificar de manera exclusiva un informe de progreso.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-121">ID number used in conjunction with ErrorTime, ProgressReportSeq to uniquely identify a progress report.</span></span> <span data-ttu-id="9d3fb-122">Para obtener más información, consulte la <a href="lync-server-2013-errorreport-table.md">tabla errorreport en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9d3fb-122">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d3fb-123"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9d3fb-123"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9d3fb-124">int</span><span class="sxs-lookup"><span data-stu-id="9d3fb-124">int</span></span></p></td>
<td><p><span data-ttu-id="9d3fb-125">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="9d3fb-125">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d3fb-126">Número de identificación que identifica el informe de errores.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-126">ID number that identifies the error report.</span></span> <span data-ttu-id="9d3fb-127">ErrorReporSeq se usa junto con ErrorTime para identificar de forma exclusiva un informe de errores.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-127">ErrorReporSeq is used in conjunction with ErrorTime to uniquely identify an error report.</span></span> <span data-ttu-id="9d3fb-128">Para obtener más información, consulte la <a href="lync-server-2013-errorreport-table.md">tabla errorreport en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="9d3fb-128">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information</span></span></p>
<p><span data-ttu-id="9d3fb-129">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-129">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d3fb-130"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9d3fb-130"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9d3fb-131">int</span><span class="sxs-lookup"><span data-stu-id="9d3fb-131">int</span></span></p></td>
<td><p><span data-ttu-id="9d3fb-132">Primary</span><span class="sxs-lookup"><span data-stu-id="9d3fb-132">Primary</span></span></p></td>
<td><p><span data-ttu-id="9d3fb-133">Número de identificación para identificar el informe de progreso.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-133">ID number to identify the progress report.</span></span> <span data-ttu-id="9d3fb-134">Se usa junto con ErrorTime y ErrorReportSeq para identificar de manera única un informe de progreso.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-134">Used in conjunction with ErrorTime and ErrorReportSeq to uniquely identify a progress report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d3fb-135"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="9d3fb-135"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d3fb-136">int</span><span class="sxs-lookup"><span data-stu-id="9d3fb-136">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d3fb-137">IDENTIFICADOR de diagnóstico del informe de progreso.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-137">Diagnostic ID of the progress report.</span></span></p>
<p><span data-ttu-id="9d3fb-138">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-138">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d3fb-139"><strong>SourceId</strong></span><span class="sxs-lookup"><span data-stu-id="9d3fb-139"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d3fb-140">int</span><span class="sxs-lookup"><span data-stu-id="9d3fb-140">int</span></span></p></td>
<td><p><span data-ttu-id="9d3fb-141">Extranjero</span><span class="sxs-lookup"><span data-stu-id="9d3fb-141">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d3fb-142">Servidor que ha enviado el informe de errores (si el informe se envió desde un componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="9d3fb-142">Server that sent the error report (if the report was sent from a server component).</span></span> <span data-ttu-id="9d3fb-143">Para obtener más información, consulte la <a href="lync-server-2013-servers-table.md">tabla servidores en Lync Server 2013</a> . Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-143">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d3fb-144"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="9d3fb-144"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d3fb-145">int</span><span class="sxs-lookup"><span data-stu-id="9d3fb-145">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d3fb-146">El proceso de Lync Server sobre el que se encuentra el informe.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-146">The Lync Server process that the report is about.</span></span> <span data-ttu-id="9d3fb-147">Para obtener más información, consulte la tabla de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-147">See the Application Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d3fb-148"><strong>Detalle</strong></span><span class="sxs-lookup"><span data-stu-id="9d3fb-148"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="9d3fb-149">imagen</span><span class="sxs-lookup"><span data-stu-id="9d3fb-149">image</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d3fb-150">Detalles del informe de progreso, almacenado en formato binario, para ahorrar espacio. Estos datos se pueden convertir a formato de texto con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="9d3fb-150">Progress report details, stored in binary format to save space.This data can be converted to text format using this syntax:</span></span></p>
<p><span data-ttu-id="9d3fb-151">CAST (detallar como varbinary (Max)) como varchar (Max))</span><span class="sxs-lookup"><span data-stu-id="9d3fb-151">cast(cast(Detail as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d3fb-152"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="9d3fb-152"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d3fb-153">Identificador</span><span class="sxs-lookup"><span data-stu-id="9d3fb-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d3fb-154">Identificador único que correlaciona la información de tiempo de Unión para los distintos componentes implicados en una conferencia.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-154">Unique identifier that correlates join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="9d3fb-155">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d3fb-156"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="9d3fb-156"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9d3fb-157">int</span><span class="sxs-lookup"><span data-stu-id="9d3fb-157">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d3fb-158">Tiempo (en milisegundos) para que un componente específico se una a una conferencia.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-158">Time (in milliseconds) for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="9d3fb-159">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d3fb-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9d3fb-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d3fb-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

