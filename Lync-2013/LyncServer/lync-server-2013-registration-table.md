---
title: 'Lync Server 2013: Tabla Registration'
description: 'Lync Server 2013: tabla de registro.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration table
ms:assetid: 05ff9dd3-1aaa-4af0-bd69-8789fb8eaeb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398114(v=OCS.15)
ms:contentKeyID: 48183298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 806e1a4e944c9bc04ebdd167c41c80a57fde3f29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436569"
---
# <a name="registration-table-in-lync-server-2013"></a><span data-ttu-id="5ea67-103">Tabla Registration en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ea67-103">Registration table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5ea67-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5ea67-104">

<span> </span></span></span>

<span data-ttu-id="5ea67-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="5ea67-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="5ea67-106">Cada registro representa un evento de registro de usuario.</span><span class="sxs-lookup"><span data-stu-id="5ea67-106">Each record represents one user registration event.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ea67-107">Columna</span><span class="sxs-lookup"><span data-stu-id="5ea67-107">Column</span></span></th>
<th><span data-ttu-id="5ea67-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5ea67-108">Data Type</span></span></th>
<th><span data-ttu-id="5ea67-109">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="5ea67-109">Key/Index</span></span></th>
<th><span data-ttu-id="5ea67-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="5ea67-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ea67-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-112">datetime</span><span class="sxs-lookup"><span data-stu-id="5ea67-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="5ea67-113">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="5ea67-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="5ea67-114">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="5ea67-114">Time of session request.</span></span> <span data-ttu-id="5ea67-115">Se usa en conjunción con <strong>SessionIdSeq</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="5ea67-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="5ea67-116">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ea67-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea67-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-118">int</span><span class="sxs-lookup"><span data-stu-id="5ea67-118">int</span></span></p></td>
<td><p><span data-ttu-id="5ea67-119">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="5ea67-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="5ea67-120">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="5ea67-120">ID number to identify the session.</span></span> <span data-ttu-id="5ea67-121">Se usa en conjunción con <strong>SessionIdTime</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="5ea67-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="5ea67-122">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ea67-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea67-123"><strong>Iddeusuario</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-123"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-124">int</span><span class="sxs-lookup"><span data-stu-id="5ea67-124">int</span></span></p></td>
<td><p><span data-ttu-id="5ea67-125">Extranjero</span><span class="sxs-lookup"><span data-stu-id="5ea67-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5ea67-126">El identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="5ea67-126">The user ID.</span></span> <span data-ttu-id="5ea67-127">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ea67-127">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea67-128"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-128"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-129">identificador</span><span class="sxs-lookup"><span data-stu-id="5ea67-129">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5ea67-130">Un GUID para identificar un extremo de registro.</span><span class="sxs-lookup"><span data-stu-id="5ea67-130">A GUID to identify a registration endpoint.</span></span> <span data-ttu-id="5ea67-131">Normalmente, el evento Register del mismo equipo del mismo usuario tendrá el mismo identificador de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="5ea67-131">Usually the register event from the same computer of the same user will have the same endpoint ID.</span></span> <span data-ttu-id="5ea67-132">Diferentes equipos tienen un identificador de extremo diferente.</span><span class="sxs-lookup"><span data-stu-id="5ea67-132">Different machines have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea67-133"><strong>EndpointEra</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-133"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-134">Identificador</span><span class="sxs-lookup"><span data-stu-id="5ea67-134">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5ea67-135">IDENTIFICADOR usado para diferenciar los registros que implican el mismo usuario y el mismo punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="5ea67-135">ID used to differentiate registrations that involve the same user and the same endpoint.</span></span></p>
<p><span data-ttu-id="5ea67-136">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5ea67-136">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea67-137"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-137"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-138">int</span><span class="sxs-lookup"><span data-stu-id="5ea67-138">int</span></span></p></td>
<td><p><span data-ttu-id="5ea67-139">Extranjero</span><span class="sxs-lookup"><span data-stu-id="5ea67-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5ea67-140">Versión de cliente del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="5ea67-140">Client version of current user.</span></span> <span data-ttu-id="5ea67-141">Para obtener más información, consulte la <a href="lync-server-2013-clientversions-table.md">tabla ClientVersions en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ea67-141">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea67-142"><strong>RegistrarId</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-142"><strong>RegistrarId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-143">int</span><span class="sxs-lookup"><span data-stu-id="5ea67-143">int</span></span></p></td>
<td><p><span data-ttu-id="5ea67-144">Extranjero</span><span class="sxs-lookup"><span data-stu-id="5ea67-144">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5ea67-145">IDENTIFICADOR del servidor del registrador usado para el registro.</span><span class="sxs-lookup"><span data-stu-id="5ea67-145">ID of the Registrar Server used for registration.</span></span> <span data-ttu-id="5ea67-146">Para obtener más información, consulte la <a href="lync-server-2013-servers-table.md">tabla servidores en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ea67-146">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea67-147"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-147"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-148">int</span><span class="sxs-lookup"><span data-stu-id="5ea67-148">int</span></span></p></td>
<td><p><span data-ttu-id="5ea67-149">Extranjero</span><span class="sxs-lookup"><span data-stu-id="5ea67-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5ea67-150">IDENTIFICADOR del grupo en el que se capturó la sesión.</span><span class="sxs-lookup"><span data-stu-id="5ea67-150">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="5ea67-151">Para obtener más información, consulte la <a href="lync-server-2013-pools-table.md">tabla de grupos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ea67-151">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea67-152"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-152"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-153">int</span><span class="sxs-lookup"><span data-stu-id="5ea67-153">int</span></span></p></td>
<td><p><span data-ttu-id="5ea67-154">Extranjero</span><span class="sxs-lookup"><span data-stu-id="5ea67-154">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5ea67-155">Servidor perimetral en el que se está realizando la inscripción.</span><span class="sxs-lookup"><span data-stu-id="5ea67-155">Edge Server the registration is going through.</span></span> <span data-ttu-id="5ea67-156">Para obtener más información, consulte la <a href="lync-server-2013-edgeservers-table.md">tabla EdgeServers en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ea67-156">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea67-157"><strong>IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-157"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-158">Algo</span><span class="sxs-lookup"><span data-stu-id="5ea67-158">Bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5ea67-159">Si el usuario ha iniciado sesión desde dentro o no.</span><span class="sxs-lookup"><span data-stu-id="5ea67-159">Whether the user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea67-160"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-160"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-161">bit</span><span class="sxs-lookup"><span data-stu-id="5ea67-161">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5ea67-162">Si el UserService está disponible o no.</span><span class="sxs-lookup"><span data-stu-id="5ea67-162">Whether the UserService is available or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea67-163"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-163"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-164">bit</span><span class="sxs-lookup"><span data-stu-id="5ea67-164">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5ea67-165">Si se registra en el registrador principal o no.</span><span class="sxs-lookup"><span data-stu-id="5ea67-165">Whether register to the primary Registrar or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea67-166"><strong>IsPrimaryRegistrarCentral</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-166"><strong>IsPrimaryRegistrarCentral</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-167">bit</span><span class="sxs-lookup"><span data-stu-id="5ea67-167">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5ea67-168">Indica si el usuario está registrado o no en un equipo de sucursal con la supervivencia.</span><span class="sxs-lookup"><span data-stu-id="5ea67-168">Indicates whether or not the user is registered with a survivable branch appliance.</span></span></p>
<p><span data-ttu-id="5ea67-169">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5ea67-169">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea67-170"><strong>RegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-170"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-171">datetime</span><span class="sxs-lookup"><span data-stu-id="5ea67-171">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5ea67-172">Hora de registro.</span><span class="sxs-lookup"><span data-stu-id="5ea67-172">Registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea67-173"><strong>DeRegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-173"><strong>DeRegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-174">datetime</span><span class="sxs-lookup"><span data-stu-id="5ea67-174">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5ea67-175">De-Registration momento.</span><span class="sxs-lookup"><span data-stu-id="5ea67-175">De-Registration time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea67-176"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-176"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-177">int</span><span class="sxs-lookup"><span data-stu-id="5ea67-177">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5ea67-178">Código de respuesta de la solicitud de registro.</span><span class="sxs-lookup"><span data-stu-id="5ea67-178">Response code of the register request.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea67-179"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-179"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-180">int</span><span class="sxs-lookup"><span data-stu-id="5ea67-180">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5ea67-181">IDENTIFICADOR de diagnóstico de la solicitud de registro.</span><span class="sxs-lookup"><span data-stu-id="5ea67-181">Diagnostic ID of the register request.</span></span> <span data-ttu-id="5ea67-182">Indica que el tipo de información de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="5ea67-182">This indicates that diagnostic information type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea67-183"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-183"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-184">int</span><span class="sxs-lookup"><span data-stu-id="5ea67-184">int</span></span></p></td>
<td><p><span data-ttu-id="5ea67-185">Extranjero</span><span class="sxs-lookup"><span data-stu-id="5ea67-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5ea67-186">El dispositivo del que procede la solicitud de registro.</span><span class="sxs-lookup"><span data-stu-id="5ea67-186">The device that the register request is coming from.</span></span> <span data-ttu-id="5ea67-187">Para obtener más información, consulte la <a href="lync-server-2013-devices-table.md">tabla dispositivos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ea67-187">See the <a href="lync-server-2013-devices-table.md">Devices table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea67-188"><strong>DeRegisterTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-188"><strong>DeRegisterTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="5ea67-189">tinyint</span></span></p></td>
<td><p><span data-ttu-id="5ea67-190">Extranjero</span><span class="sxs-lookup"><span data-stu-id="5ea67-190">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5ea67-191">El motivo de la anulación del registro, como "Iniciado por el usuario", "registro expirado", "error del cliente" y más.</span><span class="sxs-lookup"><span data-stu-id="5ea67-191">The reason of de-register, such as ‘user initiated’, ‘registration expired’, ‘client fail’, and more.</span></span> <span data-ttu-id="5ea67-192">Para obtener más información, consulte la <a href="lync-server-2013-deregistertype-table.md">tabla DeRegisterType en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ea67-192">See the <a href="lync-server-2013-deregistertype-table.md">DeRegisterType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea67-193"><strong>IPAddress</strong></span><span class="sxs-lookup"><span data-stu-id="5ea67-193"><strong>IPAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="5ea67-194">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ea67-194">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5ea67-195">Dirección IP del extremo con el que el usuario registró el registro.</span><span class="sxs-lookup"><span data-stu-id="5ea67-195">IP address of the endpoint the user registered with.</span></span> <span data-ttu-id="5ea67-196">Puede ser una dirección IPv4 o una dirección IPv6.</span><span class="sxs-lookup"><span data-stu-id="5ea67-196">This can be an IPv4 address or an IPv6 address.</span></span></p>
<p><span data-ttu-id="5ea67-197">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5ea67-197">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5ea67-198">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5ea67-198">


</div>

<span> </span>

</div>

</div>

</span></span></div>

