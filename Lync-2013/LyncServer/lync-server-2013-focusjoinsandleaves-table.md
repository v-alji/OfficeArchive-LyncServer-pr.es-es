---
title: 'Lync Server 2013: Tabla FocusJoinsAndLeaves'
description: 'Lync Server 2013: tabla FocusJoinsAndLeaves.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves table
ms:assetid: e6f0212c-67e9-4061-8720-d0296e855991
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399026(v=OCS.15)
ms:contentKeyID: 48185690
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5796de16ed204ce4f33935d937cbaa425d63a67f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428113"
---
# <a name="focusjoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="da62b-103">Tabla FocusJoinsAndLeaves en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da62b-103">FocusJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="da62b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="da62b-104">

<span> </span></span></span>

<span data-ttu-id="da62b-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="da62b-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="da62b-106">Cada registro de esta tabla contiene la información de CDR de la combinación de un usuario y la deja la información para una conferencia.</span><span class="sxs-lookup"><span data-stu-id="da62b-106">Each record in this table contains the CDR information about one user’s join and leave information for one conference.</span></span> <span data-ttu-id="da62b-107">Cada conferencia está representada en esta tabla un registro para cada vez que un usuario se une y sale de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="da62b-107">Each conference is represented in this table by one record for each time a user joins and leaves the conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da62b-108">Columna</span><span class="sxs-lookup"><span data-stu-id="da62b-108">Column</span></span></th>
<th><span data-ttu-id="da62b-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="da62b-109">Data Type</span></span></th>
<th><span data-ttu-id="da62b-110">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="da62b-110">Key/Index</span></span></th>
<th><span data-ttu-id="da62b-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="da62b-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da62b-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-113">datetime</span><span class="sxs-lookup"><span data-stu-id="da62b-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="da62b-114">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="da62b-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="da62b-115">Hora de la instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="da62b-115">Time of conference instance.</span></span> <span data-ttu-id="da62b-116">Se usa junto con <strong>SessionIdSeq</strong> para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="da62b-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="da62b-117">Para obtener más información, vea la <a href="lync-server-2013-conferences-table.md">tabla conferencias en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="da62b-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da62b-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-119">int</span><span class="sxs-lookup"><span data-stu-id="da62b-119">int</span></span></p></td>
<td><p><span data-ttu-id="da62b-120">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="da62b-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="da62b-121">Número de identificación para identificar la instancia de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="da62b-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="da62b-122">Se usa junto con <strong>SessionIdTime</strong> para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="da62b-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="da62b-123">Para obtener más información, vea la <a href="lync-server-2013-conferences-table.md">tabla conferencias en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="da62b-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da62b-124"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-124"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-125">datetime</span><span class="sxs-lookup"><span data-stu-id="da62b-125">datetime</span></span></p></td>
<td><p><span data-ttu-id="da62b-126">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="da62b-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="da62b-127">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="da62b-127">Time of session request.</span></span> <span data-ttu-id="da62b-128">Se usa en conjunción con <strong>SessionIdSeq</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="da62b-128">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="da62b-129">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="da62b-129">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da62b-130"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-130"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-131">int</span><span class="sxs-lookup"><span data-stu-id="da62b-131">int</span></span></p></td>
<td><p><span data-ttu-id="da62b-132">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="da62b-132">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="da62b-133">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="da62b-133">ID number to identify the session.</span></span> <span data-ttu-id="da62b-134">Se usa en conjunción con <strong>SessionIdTime</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="da62b-134">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="da62b-135">para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="da62b-135">see the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da62b-136"><strong>Iddeusuario</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-136"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-137">int</span><span class="sxs-lookup"><span data-stu-id="da62b-137">int</span></span></p></td>
<td><p><span data-ttu-id="da62b-138">Extranjero</span><span class="sxs-lookup"><span data-stu-id="da62b-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="da62b-139">Número único que identifica a este usuario, al que se hace referencia en la <a href="lync-server-2013-users-table.md">tabla usuarios de Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="da62b-139">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da62b-140"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-140"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-141">int</span><span class="sxs-lookup"><span data-stu-id="da62b-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="da62b-142">Si un usuario ha iniciado sesión en varios equipos o dispositivos al mismo tiempo, <strong>UserInstance</strong> se usa para identificar de forma inequívoca la combinación de usuario y dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da62b-142">If a user is logged on at multiple computers or devices at the same time, <strong>UserInstance</strong> is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da62b-143"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-143"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-144">bit</span><span class="sxs-lookup"><span data-stu-id="da62b-144">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="da62b-145">Si el usuario ha iniciado sesión en forma interna o no.</span><span class="sxs-lookup"><span data-stu-id="da62b-145">Whether the user logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da62b-146"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-146"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-147">int</span><span class="sxs-lookup"><span data-stu-id="da62b-147">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="da62b-148">El rol de este usuario en la Conferencia, como moderador o asistente.</span><span class="sxs-lookup"><span data-stu-id="da62b-148">This user’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da62b-149"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-149"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-150">datetime</span><span class="sxs-lookup"><span data-stu-id="da62b-150">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="da62b-151">El momento en que este usuario se une a la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="da62b-151">The time this user joins the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da62b-152"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-152"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-153">datetime</span><span class="sxs-lookup"><span data-stu-id="da62b-153">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="da62b-154">Hora en que este usuario abandona la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="da62b-154">The time this user leaves the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da62b-155"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-155"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-156">int</span><span class="sxs-lookup"><span data-stu-id="da62b-156">int</span></span></p></td>
<td><p><span data-ttu-id="da62b-157">Extranjero</span><span class="sxs-lookup"><span data-stu-id="da62b-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="da62b-158">Versión del software de cliente del usuario, al que se hace referencia en la <a href="lync-server-2013-clientversions-table.md">tabla ClientVersions en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="da62b-158">Version of the user’s client software, referenced to the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da62b-159"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="da62b-159"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="da62b-160">Identificador</span><span class="sxs-lookup"><span data-stu-id="da62b-160">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="da62b-161">Identificador único global (GUID) del extremo que se usa en la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="da62b-161">Globally unique identifier (GUID) of the endpoint used in the conference.</span></span></p>
<p><span data-ttu-id="da62b-162">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da62b-162">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="da62b-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="da62b-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

