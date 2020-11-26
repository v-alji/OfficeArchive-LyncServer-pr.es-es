---
title: 'Lync Server 2013: vista FocusJoinsAndLeaves'
description: 'Lync Server 2013: vista FocusJoinsAndLeaves.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves view
ms:assetid: 226460ef-766f-4d61-80cb-f332b65a210d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687992(v=OCS.15)
ms:contentKeyID: 49733582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c6f68c44461e378e9ebedce1305ee6b384a7a8a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428114"
---
# <a name="focusjoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="0b05a-103">Vista FocusJoinsAndLeaves en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b05a-103">FocusJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b05a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b05a-104">

<span> </span></span></span>

<span data-ttu-id="0b05a-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="0b05a-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="0b05a-106">La vista FocusJoinsAndLeaves almacena información acerca de la Unión y la información de salida de una conferencia.</span><span class="sxs-lookup"><span data-stu-id="0b05a-106">The FocusJoinsAndLeaves view stores information about join and leave information for one conference.</span></span> <span data-ttu-id="0b05a-107">Cada conferencia se representa en esta vista por un registro que se escribe cada vez que un usuario se une y sale de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="0b05a-107">Each conference is represented in this view by a record written each time a user joins and leaves the conference.</span></span> <span data-ttu-id="0b05a-108">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0b05a-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b05a-109">Columna</span><span class="sxs-lookup"><span data-stu-id="0b05a-109">Column</span></span></th>
<th><span data-ttu-id="0b05a-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0b05a-110">Data Type</span></span></th>
<th><span data-ttu-id="0b05a-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="0b05a-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b05a-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-113">datetime</span><span class="sxs-lookup"><span data-stu-id="0b05a-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="0b05a-114">Hora de la instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="0b05a-114">Time of conference instance.</span></span> <span data-ttu-id="0b05a-115">Se usa junto con SessionIdSeq para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="0b05a-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="0b05a-116">Para obtener más información, vea la <a href="lync-server-2013-conferences-table.md">tabla conferencias en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0b05a-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b05a-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-118">int</span><span class="sxs-lookup"><span data-stu-id="0b05a-118">int</span></span></p></td>
<td><p><span data-ttu-id="0b05a-119">Número de identificación para identificar la instancia de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="0b05a-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="0b05a-120">Se usa junto con SessionIdTime para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="0b05a-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="0b05a-121">Para obtener más información, vea la <a href="lync-server-2013-conferences-table.md">tabla conferencias en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0b05a-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b05a-122"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-122"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-123">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="0b05a-123">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="0b05a-124">URI del usuario en el que se capturó la información de unión o salida de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="0b05a-124">URI of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b05a-125"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-125"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0b05a-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0b05a-127">Tipo de URI del usuario cuya información de unión o salida de conferencia se capturó.</span><span class="sxs-lookup"><span data-stu-id="0b05a-127">Type of URI of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="0b05a-128">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0b05a-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b05a-129"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-129"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-130">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0b05a-130">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0b05a-131">Espacio empresarial del usuario cuya información de unión o salida de conferencia fue capturada.</span><span class="sxs-lookup"><span data-stu-id="0b05a-131">Tenant of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="0b05a-132">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0b05a-132">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b05a-133"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-133"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-134">identificador</span><span class="sxs-lookup"><span data-stu-id="0b05a-134">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="0b05a-135">Identificador único del usuario cuya información de unión o salida de conferencia se capturó.</span><span class="sxs-lookup"><span data-stu-id="0b05a-135">Unique identifier of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b05a-136"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-136"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0b05a-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0b05a-138">Versión del cliente usada por el usuario cuya información de unión o salida de conferencia ha sido capturada.</span><span class="sxs-lookup"><span data-stu-id="0b05a-138">Version of client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b05a-139"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-139"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-140">int</span><span class="sxs-lookup"><span data-stu-id="0b05a-140">int</span></span></p></td>
<td><p><span data-ttu-id="0b05a-141">Cliente usado por el usuario cuya información de unión o salida de conferencia fue capturada.</span><span class="sxs-lookup"><span data-stu-id="0b05a-141">Client used by the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="0b05a-142">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table.md">tabla UserAgentDef en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0b05a-142">See <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b05a-143"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-143"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-144">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="0b05a-144">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="0b05a-145">Nombre de la categoría del cliente usada por el usuario cuya información de unión o salida de conferencia fue capturada.</span><span class="sxs-lookup"><span data-stu-id="0b05a-145">Name of the category of the client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b05a-146"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-146"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-147">int</span><span class="sxs-lookup"><span data-stu-id="0b05a-147">int</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b05a-148"><strong>IsuserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-148"><strong>IsuserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-149">bit</span><span class="sxs-lookup"><span data-stu-id="0b05a-149">bit</span></span></p></td>
<td><p><span data-ttu-id="0b05a-150">Bit que representa si el usuario es un usuario interno o no.</span><span class="sxs-lookup"><span data-stu-id="0b05a-150">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b05a-151"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-151"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-152">datetime</span><span class="sxs-lookup"><span data-stu-id="0b05a-152">datetime</span></span></p></td>
<td><p><span data-ttu-id="0b05a-153">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="0b05a-153">Time of session request.</span></span> <span data-ttu-id="0b05a-154">Se usa en conjunción con SessionIdSeq para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="0b05a-154">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="0b05a-155">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0b05a-155">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b05a-156"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-156"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-157">int</span><span class="sxs-lookup"><span data-stu-id="0b05a-157">int</span></span></p></td>
<td><p><span data-ttu-id="0b05a-158">Si un usuario ha iniciado sesión en varios equipos o dispositivos al mismo tiempo, UserInstance se usa para identificar de forma inequívoca la combinación de usuario y dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b05a-158">If a user is logged on at multiple computers or devices at the same time, UserInstance is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b05a-159"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-159"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-160">VARCHAR (775)</span><span class="sxs-lookup"><span data-stu-id="0b05a-160">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="0b05a-161">IDENTIFICACIÓN del cuadro de diálogo SIP de la sesión.</span><span class="sxs-lookup"><span data-stu-id="0b05a-161">SIP dialog ID of the session.</span></span> <span data-ttu-id="0b05a-162">El formato es: diálogo; de-etiqueta; to-TAG.</span><span class="sxs-lookup"><span data-stu-id="0b05a-162">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b05a-163"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-163"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-164">datetime</span><span class="sxs-lookup"><span data-stu-id="0b05a-164">datetime</span></span></p></td>
<td><p><span data-ttu-id="0b05a-165">El momento en que el usuario se unió a la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="0b05a-165">Time that the user joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b05a-166"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-166"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-167">datetime</span><span class="sxs-lookup"><span data-stu-id="0b05a-167">datetime</span></span></p></td>
<td><p><span data-ttu-id="0b05a-168">Tiempo que el usuario abandonó la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="0b05a-168">Time that the user left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b05a-169"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="0b05a-169"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="0b05a-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0b05a-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0b05a-171">Función del usuario en la Conferencia, como moderador o asistente.</span><span class="sxs-lookup"><span data-stu-id="0b05a-171">User’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0b05a-172">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b05a-172">


</div>

<span> </span>

</div>

</div>

</span></span></div>

