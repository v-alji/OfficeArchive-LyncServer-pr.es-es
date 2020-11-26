---
title: 'Lync Server 2013: vista McuJoinsAndLeaves'
description: 'Lync Server 2013: vista McuJoinsAndLeaves.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves view
ms:assetid: 6f00b8e7-b8b6-4657-ac5e-d8a571806ae2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688088(v=OCS.15)
ms:contentKeyID: 49733687
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7f2f51c340d5bd4824a6e8eff1a0da172a758c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425734"
---
# <a name="mcujoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="748e3-103">Vista McuJoinsAndLeaves en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="748e3-103">McuJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="748e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="748e3-104">

<span> </span></span></span>

<span data-ttu-id="748e3-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="748e3-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="748e3-106">La vista McuJoinsAndLeaves almacena información sobre los usuarios que se unen y salen de la información de un servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="748e3-106">The McuJoinsAndLeaves view stores information about users join and leave information for one conference server.</span></span> <span data-ttu-id="748e3-107">Cada registro de esta vista contiene detalles de la llamada sobre una combinación de una Unión de usuario o el servidor abandonar y Conferencia.</span><span class="sxs-lookup"><span data-stu-id="748e3-107">Each record in this view contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="748e3-108">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="748e3-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="748e3-109">Columna</span><span class="sxs-lookup"><span data-stu-id="748e3-109">Column</span></span></th>
<th><span data-ttu-id="748e3-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="748e3-110">Data Type</span></span></th>
<th><span data-ttu-id="748e3-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="748e3-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="748e3-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-113">datetime</span><span class="sxs-lookup"><span data-stu-id="748e3-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="748e3-114">Hora de la instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="748e3-114">Time of conference instance.</span></span> <span data-ttu-id="748e3-115">Se usa junto con SessionIdSeq para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="748e3-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="748e3-116">Para obtener más información, vea la <a href="lync-server-2013-conferences-table.md">tabla conferencias en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="748e3-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748e3-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-118">int</span><span class="sxs-lookup"><span data-stu-id="748e3-118">int</span></span></p></td>
<td><p><span data-ttu-id="748e3-119">Número de identificación para identificar la instancia de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="748e3-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="748e3-120">Se usa junto con SessionIdTime para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="748e3-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="748e3-121">Para obtener más información, vea la <a href="lync-server-2013-conferences-table.md">tabla conferencias en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="748e3-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748e3-122"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-122"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-123">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="748e3-123">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="748e3-124">El URI del servidor de conferencia al que se conectó el usuario.</span><span class="sxs-lookup"><span data-stu-id="748e3-124">The URI of the conferencing server that the user connected to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748e3-125"><strong>McuUriType</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-125"><strong>McuUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="748e3-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="748e3-127">El URI del servidor de conferencia al que se conectó el usuario.</span><span class="sxs-lookup"><span data-stu-id="748e3-127">The URI of the conferencing server that the user connected to.</span></span> <span data-ttu-id="748e3-128">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="748e3-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748e3-129"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-129"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-130">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="748e3-130">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="748e3-131">El URI del usuario en el que se ha capturado la información de Unión/salida del servidor de conferencias.</span><span class="sxs-lookup"><span data-stu-id="748e3-131">The URI of the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748e3-132"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-132"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="748e3-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="748e3-134">El tipo de URI del usuario en el que se capturó la información de Unión/salida del servidor de conferencias.</span><span class="sxs-lookup"><span data-stu-id="748e3-134">The type of URI of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="748e3-135">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="748e3-135">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748e3-136"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-136"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="748e3-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="748e3-138">El inquilino del usuario en el que se ha capturado la información de Unión/salida del servidor de conferencias.</span><span class="sxs-lookup"><span data-stu-id="748e3-138">The tenant of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="748e3-139">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="748e3-139">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748e3-140"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-140"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="748e3-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="748e3-142">La versión de cliente utilizada por el usuario en el que se capturó la información de Unión/salida del servidor de conferencias.</span><span class="sxs-lookup"><span data-stu-id="748e3-142">The version of client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748e3-143"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-143"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-144">int</span><span class="sxs-lookup"><span data-stu-id="748e3-144">int</span></span></p></td>
<td><p><span data-ttu-id="748e3-145">El cliente usado por el usuario en el que se capturó la información de Unión/salida del servidor de conferencias.</span><span class="sxs-lookup"><span data-stu-id="748e3-145">The client used by the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="748e3-146">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table.md">tabla UserAgentDef en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="748e3-146">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748e3-147"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-147"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-148">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="748e3-148">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="748e3-149">El nombre de la categoría del cliente usada por el usuario en el que se capturó la información de Unión/salida del servidor de conferencias.</span><span class="sxs-lookup"><span data-stu-id="748e3-149">The name of the category of the client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748e3-150"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-150"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-151">int</span><span class="sxs-lookup"><span data-stu-id="748e3-151">int</span></span></p></td>
<td><p><span data-ttu-id="748e3-152">Identifica de forma única la combinación de usuarios y dispositivos para los usuarios que tienen iniciada sesión simultáneamente en varios dispositivos.</span><span class="sxs-lookup"><span data-stu-id="748e3-152">Uniquely identifies the user/device combination for users simultaneously logged on to multiple devices.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748e3-153"><strong>IsUserFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-153"><strong>IsUserFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-154">bit</span><span class="sxs-lookup"><span data-stu-id="748e3-154">bit</span></span></p></td>
<td><p><span data-ttu-id="748e3-155">Bit que representa si el usuario es un usuario interno o no.</span><span class="sxs-lookup"><span data-stu-id="748e3-155">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748e3-156"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-156"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-157">datetime</span><span class="sxs-lookup"><span data-stu-id="748e3-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="748e3-158">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="748e3-158">Time of session request.</span></span> <span data-ttu-id="748e3-159">Se usa en conjunción con SessionIdSeq para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="748e3-159">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="748e3-160">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="748e3-160">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748e3-161"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-161"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-162">int</span><span class="sxs-lookup"><span data-stu-id="748e3-162">int</span></span></p></td>
<td><p><span data-ttu-id="748e3-163">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="748e3-163">ID number to identify the session.</span></span> <span data-ttu-id="748e3-164">Se usa en conjunción con SessionIdTime para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="748e3-164">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="748e3-165">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="748e3-165">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748e3-166"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-166"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-167">VARCHAR (775)</span><span class="sxs-lookup"><span data-stu-id="748e3-167">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="748e3-168">IDENTIFICACIÓN del cuadro de diálogo SIP de la sesión.</span><span class="sxs-lookup"><span data-stu-id="748e3-168">SIP dialog ID of the session.</span></span> <span data-ttu-id="748e3-169">El formato es: diálogo; de-etiqueta; to-TAG.</span><span class="sxs-lookup"><span data-stu-id="748e3-169">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748e3-170"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-170"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-171">datetime</span><span class="sxs-lookup"><span data-stu-id="748e3-171">datetime</span></span></p></td>
<td><p><span data-ttu-id="748e3-172">Momento en que el usuario se unió al servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="748e3-172">Time the user joined the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748e3-173"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="748e3-173"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="748e3-174">datetime</span><span class="sxs-lookup"><span data-stu-id="748e3-174">datetime</span></span></p></td>
<td><p><span data-ttu-id="748e3-175">El momento en que el usuario abandonó el servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="748e3-175">Time the user left the conferencing server.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="748e3-176">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="748e3-176">


</div>

<span> </span>

</div>

</div>

</span></span></div>

