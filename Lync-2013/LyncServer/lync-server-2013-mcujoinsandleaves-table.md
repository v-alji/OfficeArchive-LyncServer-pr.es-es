---
title: 'Lync Server 2013: Tabla McuJoinsAndLeaves'
description: 'Lync Server 2013: tabla McuJoinsAndLeaves.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves table
ms:assetid: 4e073366-0b5d-45b4-a3f6-d63dd5fd9f25
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398316(v=OCS.15)
ms:contentKeyID: 48184115
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee7d9473892ac357dcefd80b0d52382c5dd7d930
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425755"
---
# <a name="mcujoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="dffec-103">Tabla McuJoinsAndLeaves en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dffec-103">McuJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dffec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dffec-104">

<span> </span></span></span>

<span data-ttu-id="dffec-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="dffec-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="dffec-106">Cada registro de esta tabla contiene detalles de la llamada acerca de una combinación de una Unión de usuario o de un servidor de conferencia y un servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="dffec-106">Each record in this table contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="dffec-107">Por ejemplo, si un usuario se une a una conferencia que incluye conferencias web y elementos de audio/vídeo, se creará un registro para la combinación de conferencias por Internet de ese usuario y otro para la combinación de audio y videoconferencias del usuario.</span><span class="sxs-lookup"><span data-stu-id="dffec-107">For example, if a user joins a conference that includes web conferencing and audio/video elements, one record would be created for that user’s web conferencing join, and another record would be created for the user’s audio/video conferencing join.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dffec-108">Columna</span><span class="sxs-lookup"><span data-stu-id="dffec-108">Column</span></span></th>
<th><span data-ttu-id="dffec-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="dffec-109">Data Type</span></span></th>
<th><span data-ttu-id="dffec-110">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="dffec-110">Key/Index</span></span></th>
<th><span data-ttu-id="dffec-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="dffec-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dffec-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="dffec-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="dffec-113">datetime</span><span class="sxs-lookup"><span data-stu-id="dffec-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="dffec-114">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="dffec-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="dffec-115">Hora de la instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="dffec-115">Time of conference instance.</span></span> <span data-ttu-id="dffec-116">Se usa junto con <strong>SessionIdSeq</strong> para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="dffec-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="dffec-117">Para obtener más información, vea la <a href="lync-server-2013-conferences-table.md">tabla conferencias en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="dffec-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dffec-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="dffec-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="dffec-119">int</span><span class="sxs-lookup"><span data-stu-id="dffec-119">int</span></span></p></td>
<td><p><span data-ttu-id="dffec-120">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="dffec-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="dffec-121">Número de identificación para identificar la instancia de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="dffec-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="dffec-122">Se usa junto con <strong>SessionIdTime</strong> para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="dffec-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="dffec-123">Para obtener más información, vea la <a href="lync-server-2013-conferences-table.md">tabla conferencias en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="dffec-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dffec-124"><strong>Iddeusuario</strong></span><span class="sxs-lookup"><span data-stu-id="dffec-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="dffec-125">int</span><span class="sxs-lookup"><span data-stu-id="dffec-125">int</span></span></p></td>
<td><p><span data-ttu-id="dffec-126">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="dffec-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="dffec-127">Número único que identifica a este usuario.</span><span class="sxs-lookup"><span data-stu-id="dffec-127">Unique number identifying this user.</span></span> <span data-ttu-id="dffec-128">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="dffec-128">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dffec-129"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="dffec-129"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="dffec-130">int</span><span class="sxs-lookup"><span data-stu-id="dffec-130">int</span></span></p></td>
<td><p><span data-ttu-id="dffec-131">Primary</span><span class="sxs-lookup"><span data-stu-id="dffec-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="dffec-132">Si un usuario ha iniciado sesión en varios equipos o dispositivos a la vez, McuUserInstancerá de forma exclusiva la combinación de usuario y dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dffec-132">If a user is logged on at multiple computers or devices at once, McuUserInstance uniquely identifies the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dffec-133"><strong>IsFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="dffec-133"><strong>IsFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="dffec-134">bit</span><span class="sxs-lookup"><span data-stu-id="dffec-134">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="dffec-135">Si el usuario se une desde una RTC o no.</span><span class="sxs-lookup"><span data-stu-id="dffec-135">Whether the user is joining from a PSTN or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dffec-136"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="dffec-136"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="dffec-137">int</span><span class="sxs-lookup"><span data-stu-id="dffec-137">int</span></span></p></td>
<td><p><span data-ttu-id="dffec-138">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="dffec-138">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="dffec-139">Número único que identifica este servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="dffec-139">Unique number identifying this conferencing server.</span></span> <span data-ttu-id="dffec-140">Para obtener más información, consulte la <a href="lync-server-2013-mcus-table.md">tabla MCU en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="dffec-140">See the <a href="lync-server-2013-mcus-table.md">Mcus table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dffec-141"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="dffec-141"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="dffec-142">datetime</span><span class="sxs-lookup"><span data-stu-id="dffec-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="dffec-143">Extranjero</span><span class="sxs-lookup"><span data-stu-id="dffec-143">Foreign</span></span></p></td>
<td><p><span data-ttu-id="dffec-144">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="dffec-144">Time of session request.</span></span> <span data-ttu-id="dffec-145">Se usa en conjunción con <strong>SessionIdSeq</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="dffec-145">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="dffec-146">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="dffec-146">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dffec-147"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="dffec-147"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="dffec-148">int</span><span class="sxs-lookup"><span data-stu-id="dffec-148">int</span></span></p></td>
<td><p><span data-ttu-id="dffec-149">Extranjero</span><span class="sxs-lookup"><span data-stu-id="dffec-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="dffec-150">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="dffec-150">ID number to identify the session.</span></span> <span data-ttu-id="dffec-151">Se usa en conjunción con <strong>SessionIdTime</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="dffec-151">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="dffec-152">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="dffec-152">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dffec-153"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="dffec-153"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="dffec-154">datetime</span><span class="sxs-lookup"><span data-stu-id="dffec-154">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="dffec-155">El momento en que este usuario se une a este servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="dffec-155">The time this user joins this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dffec-156"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="dffec-156"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="dffec-157">datetime</span><span class="sxs-lookup"><span data-stu-id="dffec-157">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="dffec-158">Hora en que este usuario abandona este servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="dffec-158">The time this user leaves this conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dffec-159"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="dffec-159"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="dffec-160">int</span><span class="sxs-lookup"><span data-stu-id="dffec-160">int</span></span></p></td>
<td><p><span data-ttu-id="dffec-161">Extranjero</span><span class="sxs-lookup"><span data-stu-id="dffec-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="dffec-162">Identificador que especifica el número de versión del uso de software de cliente en la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="dffec-162">Identifier that specifies the version number of the client software use in the conference.</span></span> <span data-ttu-id="dffec-163">Para obtener más información, consulte la <a href="lync-server-2013-clientversions-table.md">tabla ClientVersions en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="dffec-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="dffec-164">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dffec-164">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="dffec-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dffec-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

