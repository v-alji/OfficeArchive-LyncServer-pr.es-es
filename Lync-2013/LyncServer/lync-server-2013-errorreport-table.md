---
title: 'Lync Server 2013: Tabla ErrorReport'
description: 'Lync Server 2013: tabla ErrorReport.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport table
ms:assetid: ae0287b4-e8ca-4f8c-84ef-502897dcaa2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412826(v=OCS.15)
ms:contentKeyID: 48185129
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c1cc65c396c16dc137255438f7ef7c32b2d0b78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428520"
---
# <a name="errorreport-table-in-lync-server-2013"></a><span data-ttu-id="e450e-103">Tabla ErrorReport en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e450e-103">ErrorReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e450e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e450e-104">

<span> </span></span></span>

<span data-ttu-id="e450e-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="e450e-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="e450e-106">La tabla ErrorReport almacena información sobre los errores que se han producido.</span><span class="sxs-lookup"><span data-stu-id="e450e-106">The ErrorReport table stores information about errors that have occurred.</span></span> <span data-ttu-id="e450e-107">Cada registro es una aparición de error.</span><span class="sxs-lookup"><span data-stu-id="e450e-107">Each record is one error occurrence.</span></span> <span data-ttu-id="e450e-108">Los errores se capturan mediante el agente CDR que se ejecuta en el servidor front-end o se envían desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="e450e-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e450e-109">Columna</span><span class="sxs-lookup"><span data-stu-id="e450e-109">Column</span></span></th>
<th><span data-ttu-id="e450e-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e450e-110">Data Type</span></span></th>
<th><span data-ttu-id="e450e-111">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="e450e-111">Key/Index</span></span></th>
<th><span data-ttu-id="e450e-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="e450e-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e450e-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-114">datetime</span><span class="sxs-lookup"><span data-stu-id="e450e-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="e450e-115">Primary</span><span class="sxs-lookup"><span data-stu-id="e450e-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="e450e-116">Fecha y hora en que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="e450e-116">Date and time the error occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e450e-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-118">int</span><span class="sxs-lookup"><span data-stu-id="e450e-118">int</span></span></p></td>
<td><p><span data-ttu-id="e450e-119">Primary</span><span class="sxs-lookup"><span data-stu-id="e450e-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="e450e-120">Número de identificación para identificar el informe de errores.</span><span class="sxs-lookup"><span data-stu-id="e450e-120">ID number to identify the error report.</span></span> <span data-ttu-id="e450e-121">Se usa en conjunción con <strong>ErrorTime</strong> para identificar de manera exclusiva un informe de errores.</span><span class="sxs-lookup"><span data-stu-id="e450e-121">Used in conjunction with <strong>ErrorTime</strong> to uniquely identify an error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e450e-122"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-122"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-123">int</span><span class="sxs-lookup"><span data-stu-id="e450e-123">int</span></span></p></td>
<td><p><span data-ttu-id="e450e-124">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e450e-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e450e-125">IDENTIFICADOR único del tipo de error.</span><span class="sxs-lookup"><span data-stu-id="e450e-125">Unique ID of the error type.</span></span> <span data-ttu-id="e450e-126">Para obtener más información, consulte la <a href="lync-server-2013-errordef-table.md">tabla ErrorDef en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e450e-126">See the <a href="lync-server-2013-errordef-table.md">ErrorDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e450e-127"><strong>FromUserId</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-127"><strong>FromUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-128">int</span><span class="sxs-lookup"><span data-stu-id="e450e-128">int</span></span></p></td>
<td><p><span data-ttu-id="e450e-129">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e450e-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e450e-130">Usuario que originó la solicitud que causó el error.</span><span class="sxs-lookup"><span data-stu-id="e450e-130">User who originated the request that caused the error.</span></span> <span data-ttu-id="e450e-131">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e450e-131">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e450e-132"><strong>ToUserId</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-132"><strong>ToUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-133">int</span><span class="sxs-lookup"><span data-stu-id="e450e-133">int</span></span></p></td>
<td><p><span data-ttu-id="e450e-134">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e450e-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e450e-135">Usuario de destino de la solicitud que causó el error.</span><span class="sxs-lookup"><span data-stu-id="e450e-135">Destination user for the request that caused the error.</span></span> <span data-ttu-id="e450e-136">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e450e-136">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e450e-137"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-137"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-138">int</span><span class="sxs-lookup"><span data-stu-id="e450e-138">int</span></span></p></td>
<td><p><span data-ttu-id="e450e-139">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e450e-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e450e-140">URI de conferencia relacionado con el error.</span><span class="sxs-lookup"><span data-stu-id="e450e-140">Conference URI related to the error.</span></span> <span data-ttu-id="e450e-141">Para obtener más información, consulte la <a href="lync-server-2013-conferenceuris-table.md">tabla ConferenceUris en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e450e-141">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="e450e-142">Normalmente, si ConferenceUriId no es null, FromUserId o ToUserId será null.</span><span class="sxs-lookup"><span data-stu-id="e450e-142">Typically, if ConferenceUriId is not null, then either FromUserId or ToUserId will be null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e450e-143"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-143"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-144">datetime</span><span class="sxs-lookup"><span data-stu-id="e450e-144">datetime</span></span></p></td>
<td><p><span data-ttu-id="e450e-145">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e450e-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e450e-146">Se usa en conjunción con <strong>SessionIdSeq</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="e450e-146">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="e450e-147">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e450e-147">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e450e-148"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-148"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-149">int</span><span class="sxs-lookup"><span data-stu-id="e450e-149">int</span></span></p></td>
<td><p><span data-ttu-id="e450e-150">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e450e-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e450e-151">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="e450e-151">ID number to identify the session.</span></span> <span data-ttu-id="e450e-152">Se usa en conjunción con <strong>SessionIdTime</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="e450e-152">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="e450e-153">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e450e-153">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e450e-154"><strong>SourceId</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-154"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-155">int</span><span class="sxs-lookup"><span data-stu-id="e450e-155">int</span></span></p></td>
<td><p><span data-ttu-id="e450e-156">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e450e-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e450e-157">Servidor que ha enviado el informe de errores (si el informe se está enviando desde un componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="e450e-157">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="e450e-158">Para obtener más información, consulte la <a href="lync-server-2013-servers-table.md">tabla servidores en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e450e-158">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="e450e-159">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e450e-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e450e-160"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-160"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-161">int</span><span class="sxs-lookup"><span data-stu-id="e450e-161">int</span></span></p></td>
<td><p><span data-ttu-id="e450e-162">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e450e-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e450e-163">Servidor que ha enviado el informe de errores (si el informe se está enviando desde un componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="e450e-163">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="e450e-164">Para obtener más información, consulte la <a href="lync-server-2013-application-table.md">tabla de aplicaciones en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e450e-164">See the <a href="lync-server-2013-application-table.md">Application table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="e450e-165">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e450e-165">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e450e-166"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-166"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-167">imagen</span><span class="sxs-lookup"><span data-stu-id="e450e-167">image</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e450e-168">Más información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="e450e-168">More information about the error.</span></span></p>
<p><span data-ttu-id="e450e-169">Estos datos se pueden convertir a formato de texto con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="e450e-169">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(Detail as varbinary(max)) as varchar(max)) </code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e450e-170"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-170"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-171">int</span><span class="sxs-lookup"><span data-stu-id="e450e-171">int</span></span></p></td>
<td><p><span data-ttu-id="e450e-172">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e450e-172">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e450e-173">La versión de cliente del extremo que envía el informe de errores.</span><span class="sxs-lookup"><span data-stu-id="e450e-173">The client version of endpoint that sends the error report.</span></span> <span data-ttu-id="e450e-174">Para obtener más información, consulte la <a href="lync-server-2013-clientversions-table.md">tabla ClientVersions en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e450e-174">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e450e-175"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-175"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-176">bit</span><span class="sxs-lookup"><span data-stu-id="e450e-176">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e450e-177">Es el informe de errores capturado por el agente CDR que se ejecuta en el servidor front-end o enviado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="e450e-177">Is the error report captured by the CDR agent running on the front-end server, or sent by the client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e450e-178"><strong>Fdisableautoindexingonschemaupdate</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-178"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-179">smallint</span><span class="sxs-lookup"><span data-stu-id="e450e-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e450e-180">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e450e-180">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e450e-181"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-181"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-182">Identificador</span><span class="sxs-lookup"><span data-stu-id="e450e-182">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e450e-183">Identificador único que correlaciona información de tiempo de Unión para los distintos componentes implicados en una conferencia.</span><span class="sxs-lookup"><span data-stu-id="e450e-183">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="e450e-184">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e450e-184">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e450e-185"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-185"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-186">int</span><span class="sxs-lookup"><span data-stu-id="e450e-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e450e-187">Tiempo (en milisegundos) necesario para que un componente específico se una a una conferencia.</span><span class="sxs-lookup"><span data-stu-id="e450e-187">Time (in milliseconds) required for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="e450e-188">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e450e-188">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e450e-189"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-189"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-190">int</span><span class="sxs-lookup"><span data-stu-id="e450e-190">int</span></span></p></td>
<td><p><span data-ttu-id="e450e-191">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e450e-191">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e450e-192">Representa el nombre de dominio completo del servidor que ha generado el informe de errores.</span><span class="sxs-lookup"><span data-stu-id="e450e-192">Represents the fully qualified domain name of the server that generated the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e450e-193"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="e450e-193"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="e450e-194">int</span><span class="sxs-lookup"><span data-stu-id="e450e-194">int</span></span></p></td>
<td><p><span data-ttu-id="e450e-195">Extranjero</span><span class="sxs-lookup"><span data-stu-id="e450e-195">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e450e-196">Representa el nombre de dominio completo del grupo en el que se generó el informe de errores.</span><span class="sxs-lookup"><span data-stu-id="e450e-196">Represents the fully qualified domain name of the pool where the error report was generated.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e450e-197">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e450e-197">


</div>

<span> </span>

</div>

</div>

</span></span></div>

