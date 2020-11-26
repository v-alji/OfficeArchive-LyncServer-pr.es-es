---
title: 'Lync Server 2013: vista ErrorReport'
description: 'Lync Server 2013: vista ErrorReport.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport view
ms:assetid: ca873f7e-b18b-4eaf-8db0-5f9d5a9b60a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721887(v=OCS.15)
ms:contentKeyID: 49733821
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50fb0a362c71d8dfb5873157e7b1ed3d3eb680ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428527"
---
# <a name="errorreport-view-in-lync-server-2013"></a><span data-ttu-id="7bd13-103">Vista ErrorReport en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7bd13-103">ErrorReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7bd13-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7bd13-104">

<span> </span></span></span>

<span data-ttu-id="7bd13-105">_**Última modificación del tema:** 2013-01-22_</span><span class="sxs-lookup"><span data-stu-id="7bd13-105">_**Topic Last Modified:** 2013-01-22_</span></span>

<span data-ttu-id="7bd13-106">La vista ErrorReport almacena información sobre los errores notificados.</span><span class="sxs-lookup"><span data-stu-id="7bd13-106">The ErrorReport view stores information about errors reported.</span></span> <span data-ttu-id="7bd13-107">Cada registro es una aparición de error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-107">Each record is one error occurrence.</span></span> <span data-ttu-id="7bd13-108">Los errores se capturan mediante el agente CDR que se ejecuta en el servidor front-end o se envían desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="7bd13-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span> <span data-ttu-id="7bd13-109">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7bd13-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7bd13-110">Columna</span><span class="sxs-lookup"><span data-stu-id="7bd13-110">Column</span></span></th>
<th><span data-ttu-id="7bd13-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7bd13-111">Data Type</span></span></th>
<th><span data-ttu-id="7bd13-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="7bd13-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-114">datetime</span><span class="sxs-lookup"><span data-stu-id="7bd13-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="7bd13-115">Hora de error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-115">Time of error occurred.</span></span> <span data-ttu-id="7bd13-116">Se usa junto con ErrorReportSeq para identificar de forma única un error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-118">int</span><span class="sxs-lookup"><span data-stu-id="7bd13-118">int</span></span></p></td>
<td><p><span data-ttu-id="7bd13-119">Número de identificación para identificar el error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-119">ID number to identify the error.</span></span> <span data-ttu-id="7bd13-120">Se usa junto con ErrorTime para identificar de forma única un error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-121"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-121"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-122">int</span><span class="sxs-lookup"><span data-stu-id="7bd13-122">int</span></span></p></td>
<td><p><span data-ttu-id="7bd13-123">IDENTIFICADOR de diagnóstico del informe de errores.</span><span class="sxs-lookup"><span data-stu-id="7bd13-123">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-124"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-124"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="7bd13-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-126">Identificador URI del usuario que originó el error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-126">URI of the user who originated the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-127"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-127"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bd13-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-129">Tipo de URI del usuario que originó el error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-129">Type of URI of the user who originated the error.</span></span> <span data-ttu-id="7bd13-130">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7bd13-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-131"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-131"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bd13-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-133">Espacio empresarial del usuario que originó el error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-133">Tenant of the user who originated the error.</span></span> <span data-ttu-id="7bd13-134">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7bd13-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-135"><strong>ToUr</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-135"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-136">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="7bd13-136">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-137">Identificador URI del usuario que era el destino del informe de errores.</span><span class="sxs-lookup"><span data-stu-id="7bd13-137">URI of the user who was the target of the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bd13-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-140">Tipo de URI del usuario que se dirige al informe de errores.</span><span class="sxs-lookup"><span data-stu-id="7bd13-140">Type of URI of the user who target of the error report.</span></span> <span data-ttu-id="7bd13-141">Para obtener más información, consulte la tabla UriTypes.</span><span class="sxs-lookup"><span data-stu-id="7bd13-141">See the UriTypes Table for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-142"><strong>ToTenant</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-142"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-143">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bd13-143">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-144">Espacio empresarial del usuario que se dirige al informe de errores.</span><span class="sxs-lookup"><span data-stu-id="7bd13-144">Tenant of the user who target of the error report.</span></span> <span data-ttu-id="7bd13-145">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7bd13-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-146"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-146"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="7bd13-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-148">URI de la Conferencia que era el destino del informe de errores.</span><span class="sxs-lookup"><span data-stu-id="7bd13-148">URI of the conference that was the target of the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-149"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-149"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bd13-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-151">Tipo de URI de la Conferencia que era el destino del informe de errores.</span><span class="sxs-lookup"><span data-stu-id="7bd13-151">URI type of the conference that was the target of the error report.</span></span> <span data-ttu-id="7bd13-152">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7bd13-152">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-153"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-153"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-154">datetime</span><span class="sxs-lookup"><span data-stu-id="7bd13-154">datetime</span></span></p></td>
<td><p><span data-ttu-id="7bd13-155">Hora de la solicitud de sesión que originó el informe de errores.</span><span class="sxs-lookup"><span data-stu-id="7bd13-155">Time of session request that originated the error report.</span></span> <span data-ttu-id="7bd13-156">Se usa en conjunción con SessionIdSeq para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="7bd13-156">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="7bd13-157">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7bd13-157">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-158"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-158"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-159">int</span><span class="sxs-lookup"><span data-stu-id="7bd13-159">int</span></span></p></td>
<td><p><span data-ttu-id="7bd13-160">Número de identificación para identificar la solicitud de sesión que originó el informe de errores.</span><span class="sxs-lookup"><span data-stu-id="7bd13-160">ID number to identify the session request that originated the error report.</span></span> <span data-ttu-id="7bd13-161">Se usa en conjunción con SessionIdTime para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="7bd13-161">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="7bd13-162">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7bd13-162">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-163"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-163"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-164">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="7bd13-164">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-165">IDENTIFICADOR del cuadro de diálogo SIP de la sesión que originó el error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-165">SIP dialog ID of session that originated the error.</span></span> <span data-ttu-id="7bd13-166">El formato es:</span><span class="sxs-lookup"><span data-stu-id="7bd13-166">The format is:</span></span></p>
<p><span data-ttu-id="7bd13-167">cuadro de diálogo; desde: etiqueta; to-Tag</span><span class="sxs-lookup"><span data-stu-id="7bd13-167">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="7bd13-168">Estos datos se pueden convertir a formato de texto con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="7bd13-168">This data can be converted to text format by using this syntax:</span></span></p>
<p><span data-ttu-id="7bd13-169">CAST (Cast) (ExternalId as varbinary (Max)) as VARCHAR (Max))</span><span class="sxs-lookup"><span data-stu-id="7bd13-169">cast(cast(ExternalId as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-170"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-170"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-171">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bd13-171">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-172">Versión del cliente utilizada por el usuario que originó el error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-172">Version of client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-173"><strong>Tipocliente</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-173"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-174">int</span><span class="sxs-lookup"><span data-stu-id="7bd13-174">int</span></span></p></td>
<td><p><span data-ttu-id="7bd13-175">Cliente usado por el usuario que originó el error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-175">Client used by the user who originated the error.</span></span> <span data-ttu-id="7bd13-176">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table.md">tabla UserAgentDef en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7bd13-176">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-177"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-177"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-178">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="7bd13-178">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-179">Nombre de la categoría del cliente que ha usado el usuario que originó el error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-179">Name of the category of the client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-180"><strong>Origen</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-180"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bd13-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-182">Nombre del servidor que originó el error (si el informe fue enviado desde un componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="7bd13-182">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-183"><strong>Aplicación</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-183"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-184">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bd13-184">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-185">Nombre de la aplicación que originó el error (si el informe fue enviado desde un componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="7bd13-185">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-186"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-186"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-187">int</span><span class="sxs-lookup"><span data-stu-id="7bd13-187">int</span></span></p></td>
<td><p><span data-ttu-id="7bd13-188">Código de respuesta SIP a la sesión del mensaje SIP que contiene el informe de errores.</span><span class="sxs-lookup"><span data-stu-id="7bd13-188">SIP response code to the session of the SIP message containing the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-189"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-189"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-190">VARCHAR (Max)</span><span class="sxs-lookup"><span data-stu-id="7bd13-190">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-191">Tipo de solicitud en la que se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-191">Type of request that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-192"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-192"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-193">VARCHAR (Max)</span><span class="sxs-lookup"><span data-stu-id="7bd13-193">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-194">Tipo de contenido de la solicitud en la que se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-194">Content type of the request that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-195"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-195"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bd13-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-197">Tipo de sesión.</span><span class="sxs-lookup"><span data-stu-id="7bd13-197">Type of session.</span></span> <span data-ttu-id="7bd13-198">Para obtener más información, consulte la <a href="lync-server-2013-calltype-table.md">tabla CallType en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7bd13-198">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-199"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-199"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-200">identificador</span><span class="sxs-lookup"><span data-stu-id="7bd13-200">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="7bd13-201">Identificador único que correlaciona información de tiempo de Unión para los distintos componentes implicados en una conferencia.</span><span class="sxs-lookup"><span data-stu-id="7bd13-201">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-202"><strong>SetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-202"><strong>SetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-203">int</span><span class="sxs-lookup"><span data-stu-id="7bd13-203">int</span></span></p></td>
<td><p><span data-ttu-id="7bd13-204">Tiempo (en milisegundos) necesario para que un componente específico se una a una conferencia.</span><span class="sxs-lookup"><span data-stu-id="7bd13-204">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-205"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-205"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-206">bit</span><span class="sxs-lookup"><span data-stu-id="7bd13-206">bit</span></span></p></td>
<td><p><span data-ttu-id="7bd13-207">Indica si el informe de errores fue capturado por el agente CDR que se ejecuta en el servidor front-end o enviado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="7bd13-207">Indicates whether the error report was captured by the CDR agent running on the Front End server, or sent by the client.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-208"><strong>Fdisableautoindexingonschemaupdate</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-208"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-209">smallint</span><span class="sxs-lookup"><span data-stu-id="7bd13-209">smallint</span></span></p></td>
<td><p><span data-ttu-id="7bd13-210">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="7bd13-210">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-211"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-211"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-212">VARCHAR (Max)</span><span class="sxs-lookup"><span data-stu-id="7bd13-212">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="7bd13-213">Información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="7bd13-213">Additional information about the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd13-214"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-214"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-215">nvarchar</span><span class="sxs-lookup"><span data-stu-id="7bd13-215">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="7bd13-216">Nombre de dominio completo del servidor front-end que ha enviado el informe.</span><span class="sxs-lookup"><span data-stu-id="7bd13-216">Fully qualified domain name of the Front End server that submitted the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd13-217"><strong>Grupo</strong></span><span class="sxs-lookup"><span data-stu-id="7bd13-217"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd13-218">nvarchar</span><span class="sxs-lookup"><span data-stu-id="7bd13-218">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="7bd13-219">Nombre de dominio completo del grupo que contiene el servidor front-end que ha enviado el informe.</span><span class="sxs-lookup"><span data-stu-id="7bd13-219">Fully qualified domain name of the pool containing the Front End server that submitted the report.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7bd13-220">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7bd13-220">


</div>

<span> </span>

</div>

</div>

</span></span></div>

