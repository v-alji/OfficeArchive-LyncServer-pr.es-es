---
title: 'Lync Server 2013: vista de registro'
description: 'Lync Server 2013: vista de registro.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration view
ms:assetid: 8a42bc7d-3d4f-43c1-9e15-89b2ee419ade
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688120(v=OCS.15)
ms:contentKeyID: 49733718
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be169cafc324f89cacedda154ca49a8ff1ff39aa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398730"
---
# <a name="registration-view-in-lync-server-2013"></a><span data-ttu-id="b61a2-103">Vista de registro en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b61a2-103">Registration view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b61a2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b61a2-104">

<span> </span></span></span>

<span data-ttu-id="b61a2-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="b61a2-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="b61a2-106">La vista de registro almacena información sobre el registro de usuarios.</span><span class="sxs-lookup"><span data-stu-id="b61a2-106">The Registration view stores information about user registration.</span></span> <span data-ttu-id="b61a2-107">Esta vista se presentó en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b61a2-107">This view was introduced in Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b61a2-108">Columna</span><span class="sxs-lookup"><span data-stu-id="b61a2-108">Column</span></span></th>
<th><span data-ttu-id="b61a2-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b61a2-109">Data Type</span></span></th>
<th><span data-ttu-id="b61a2-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="b61a2-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-112">datetime</span><span class="sxs-lookup"><span data-stu-id="b61a2-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="b61a2-113">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="b61a2-113">Time of session request.</span></span> <span data-ttu-id="b61a2-114">Se usa en conjunción con SessionIdSeq para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="b61a2-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="b61a2-115">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b61a2-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-117">int</span><span class="sxs-lookup"><span data-stu-id="b61a2-117">int</span></span></p></td>
<td><p><span data-ttu-id="b61a2-118">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="b61a2-118">ID number to identify the session.</span></span> <span data-ttu-id="b61a2-119">Se usa en conjunción con SessionIdTime para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="b61a2-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="b61a2-120">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b61a2-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-121"><strong>RegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-121"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-122">datetime</span><span class="sxs-lookup"><span data-stu-id="b61a2-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="b61a2-123">Hora en la que se realizó el registro.</span><span class="sxs-lookup"><span data-stu-id="b61a2-123">Time at which registration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-124"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-124"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="b61a2-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-126">Identificador URI del usuario que se registró.</span><span class="sxs-lookup"><span data-stu-id="b61a2-126">URI of the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-127"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-127"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b61a2-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-129">Tipo de URI del usuario que se registró.</span><span class="sxs-lookup"><span data-stu-id="b61a2-129">Type of URI of the user who registered.</span></span> <span data-ttu-id="b61a2-130">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b61a2-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-131"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-131"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b61a2-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-133">Inquilino del usuario que se registró.</span><span class="sxs-lookup"><span data-stu-id="b61a2-133">Tenant of the user who registered.</span></span> <span data-ttu-id="b61a2-134">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b61a2-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-135"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-135"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-136">identificador</span><span class="sxs-lookup"><span data-stu-id="b61a2-136">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="b61a2-137">Identificador único del extremo del usuario registrado con.</span><span class="sxs-lookup"><span data-stu-id="b61a2-137">Unique identifier of the endpoint of the user registered with.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-138"><strong>EndpointEra</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-138"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-139">identificador</span><span class="sxs-lookup"><span data-stu-id="b61a2-139">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="b61a2-140">Identificador único que se usa para diferenciar los registros que implican al mismo usuario y al mismo punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="b61a2-140">Unique identifier used to differentiate registrations that involve the same user and the same endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-141"><strong>DeRegisterType</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-141"><strong>DeRegisterType</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-142">datetime</span><span class="sxs-lookup"><span data-stu-id="b61a2-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="b61a2-143">Hora en la que se produjo la anulación de inscripción.</span><span class="sxs-lookup"><span data-stu-id="b61a2-143">Time at which deregistration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-144"><strong>DeRegisterReason</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-144"><strong>DeRegisterReason</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b61a2-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-146">Motivo de la anulación del registro.</span><span class="sxs-lookup"><span data-stu-id="b61a2-146">Reason for deregistration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-147"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-147"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-148">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b61a2-148">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-149">Versión del cliente que usó el usuario que se registró.</span><span class="sxs-lookup"><span data-stu-id="b61a2-149">Version of client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-150"><strong>Tipocliente</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-150"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-151">int</span><span class="sxs-lookup"><span data-stu-id="b61a2-151">int</span></span></p></td>
<td><p><span data-ttu-id="b61a2-152">Cliente usado por el usuario que registró.</span><span class="sxs-lookup"><span data-stu-id="b61a2-152">Client used by the user who registered.</span></span> <span data-ttu-id="b61a2-153">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table.md">tabla UserAgentDef en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b61a2-153">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-154"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-154"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-155">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="b61a2-155">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-156">Categoría del cliente que ha usado el usuario que registró.</span><span class="sxs-lookup"><span data-stu-id="b61a2-156">Category of the client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-157"><strong>Dirección IP</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-157"><strong>IpAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-158">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b61a2-158">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-159">Dirección IP con la que el usuario se registró.</span><span class="sxs-lookup"><span data-stu-id="b61a2-159">IP Address the user registered with.</span></span> <span data-ttu-id="b61a2-160">Puede ser una dirección IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="b61a2-160">This may be an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-161"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-161"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-162">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="b61a2-162">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-163">IDENTIFICACIÓN del cuadro de diálogo SIP.</span><span class="sxs-lookup"><span data-stu-id="b61a2-163">SIP dialog ID.</span></span> <span data-ttu-id="b61a2-164">El formato de es:</span><span class="sxs-lookup"><span data-stu-id="b61a2-164">The format of the is:</span></span></p>
<p><span data-ttu-id="b61a2-165">cuadro de diálogo; desde: etiqueta; to-Tag</span><span class="sxs-lookup"><span data-stu-id="b61a2-165">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-166"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-166"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-167">int</span><span class="sxs-lookup"><span data-stu-id="b61a2-167">int</span></span></p></td>
<td><p><span data-ttu-id="b61a2-168">Código de respuesta SIP a la invitación de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b61a2-168">SIP response code to the session invitation.</span></span> <span data-ttu-id="b61a2-169">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b61a2-169">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="b61a2-170">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="b61a2-170">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-171"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-171"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-172">int</span><span class="sxs-lookup"><span data-stu-id="b61a2-172">int</span></span></p></td>
<td><p><span data-ttu-id="b61a2-173">IDENTIFICACIÓN de diagnóstico capturada del encabezado de SIP.</span><span class="sxs-lookup"><span data-stu-id="b61a2-173">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-174"><strong>Registrador</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-174"><strong>Registrar</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b61a2-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-176">FQDN del registrador.</span><span class="sxs-lookup"><span data-stu-id="b61a2-176">FQDN of the Registrar.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-177"><strong>Grupo</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-177"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b61a2-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-179">FQDN del grupo de servidores que ha capturado los datos de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b61a2-179">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-180"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-180"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b61a2-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-182">FQDN del servidor perimetral usado por el usuario que registró.</span><span class="sxs-lookup"><span data-stu-id="b61a2-182">FQDN of the Edge Server used by the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-183"><strong>IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-183"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-184">bit</span><span class="sxs-lookup"><span data-stu-id="b61a2-184">bit</span></span></p></td>
<td><p><span data-ttu-id="b61a2-185">Indica si el usuario ha iniciado sesión en la red interna.</span><span class="sxs-lookup"><span data-stu-id="b61a2-185">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-186"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-186"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-187">bit</span><span class="sxs-lookup"><span data-stu-id="b61a2-187">bit</span></span></p></td>
<td><p><span data-ttu-id="b61a2-188">Indica si el UserService estaba disponible en el momento del registro.</span><span class="sxs-lookup"><span data-stu-id="b61a2-188">Indicates whether the UserService was available at registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-189"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-189"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-190">bit</span><span class="sxs-lookup"><span data-stu-id="b61a2-190">bit</span></span></p></td>
<td><p><span data-ttu-id="b61a2-191">Indica si el registro se realizó con el registrador principal.</span><span class="sxs-lookup"><span data-stu-id="b61a2-191">Indicates whether registration was with the primary Registrar.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-192"><strong>DeviceMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-192"><strong>DeviceMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-193">BIGINT</span><span class="sxs-lookup"><span data-stu-id="b61a2-193">bigint</span></span></p></td>
<td><p><span data-ttu-id="b61a2-194">Dirección MAC del dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="b61a2-194">MAC Address of device registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b61a2-195"><strong>DeviceManufacturer</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-195"><strong>DeviceManufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b61a2-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-197">Fabricante del dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="b61a2-197">Manufacturer of the device registered.</span></span> <span data-ttu-id="b61a2-198">Para obtener más información, consulte la <a href="lync-server-2013-manufacturers-table.md">tabla de fabricantes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b61a2-198">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b61a2-199"><strong>DeviceHardwareVersion</strong></span><span class="sxs-lookup"><span data-stu-id="b61a2-199"><strong>DeviceHardwareVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="b61a2-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b61a2-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b61a2-201">Versión de hardware del dispositivo registrada.</span><span class="sxs-lookup"><span data-stu-id="b61a2-201">Hardware version of the device registered.</span></span> <span data-ttu-id="b61a2-202">Para obtener más información, consulte la <a href="lync-server-2013-hardwareversions-table.md">tabla HardwareVersions en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b61a2-202">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b61a2-203">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b61a2-203">


</div>

<span> </span>

</div>

</div>

</span></span></div>

