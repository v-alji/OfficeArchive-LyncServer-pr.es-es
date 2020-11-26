---
title: 'Lync Server 2013: Lista de tablas de CDR'
description: 'Lync Server 2013: lista de tablas de CDR.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of CDR tables
ms:assetid: 031843fd-c7ff-4534-9b02-8847aad70807
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398084(v=OCS.15)
ms:contentKeyID: 48183254
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 21d0f683ffeb0f5f1cbba5db4c45d248aa14e8e4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426616"
---
# <a name="list-of-cdr-tables-in-lync-server-2013"></a><span data-ttu-id="799fa-103">Lista de tablas de CDR en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="799fa-103">List of CDR tables in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="799fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="799fa-104">

<span> </span></span></span>

<span data-ttu-id="799fa-105">_**Última modificación del tema:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="799fa-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="799fa-106">El esquema de la base de datos de grabación de detalles de llamadas (CDR) consta de las siguientes tablas.</span><span class="sxs-lookup"><span data-stu-id="799fa-106">The call detail recording (CDR) database schema consists of the following tables.</span></span>

<div>

## <a name="static-tables"></a><span data-ttu-id="799fa-107">Tablas estáticas</span><span class="sxs-lookup"><span data-stu-id="799fa-107">Static Tables</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="799fa-108">Tabla</span><span class="sxs-lookup"><span data-stu-id="799fa-108">Table</span></span></th>
<th><span data-ttu-id="799fa-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="799fa-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="799fa-110"><a href="lync-server-2013-callpriorities-table.md">Tabla CallPriorities en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-110"><a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-111">Almacena la lista de posibles prioridades de llamadas, como emergencia, urgente, normal, no urgentes, etc.</span><span class="sxs-lookup"><span data-stu-id="799fa-111">Stores the list of possible call priorities, such as emergency, urgent, normal, non-urgent, and more.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-112"><a href="lync-server-2013-conferencejointimethresholds-table.md">Tabla ConferenceJoinTimeThresholds en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-112"><a href="lync-server-2013-conferencejointimethresholds-table.md">ConferenceJoinTimeThresholds table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-113">Almacena los límites de clasificación usados por el informe de Resumen de tiempo de combinación de conferencia.</span><span class="sxs-lookup"><span data-stu-id="799fa-113">Stores the classification boundaries used by the Conference Join Time Summary Report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-114"><a href="lync-server-2013-deregistertype-table.md">Tabla DeRegisterType en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-114"><a href="lync-server-2013-deregistertype-table.md">DeRegisterType table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-115">Almacena la lista de posibles razones de anulación del registro de usuarios, como el &quot; cliente iniciado, el &quot; &quot; registro expirado, el &quot; &quot; bloqueo del cliente &quot; y mucho más.</span><span class="sxs-lookup"><span data-stu-id="799fa-115">Stores the list of possible user de-register reasons, such as &quot;client initiated,&quot; &quot;registration expired,&quot; &quot;client crash,&quot; and more.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-116"><a href="lync-server-2013-medialist-table.md">Tabla MediaList en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-116"><a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-117">Almacena la lista de tipos de medios que pueden generar entradas en la base de datos (por ejemplo, mensajería instantánea, audio, vídeo y transferencia de archivos).</span><span class="sxs-lookup"><span data-stu-id="799fa-117">Stores the list of media types that can generate entries in the database (for example, IM, audio, video, and file transfer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-118"><a href="lync-server-2013-purgesettings-table.md">Tabla PurgeSettings en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-118"><a href="lync-server-2013-purgesettings-table.md">PurgeSettings table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-119">Almacena información que especifica si (y cuándo) los registros de detalles de llamadas obsoletas se eliminarán automáticamente de la base de datos de CDR.</span><span class="sxs-lookup"><span data-stu-id="799fa-119">Stores information that specifies if (and when) outdated call detail records will automatically be deleted from the CDR database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-120"><a href="lync-server-2013-roles-table.md">Tabla Roles en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-120"><a href="lync-server-2013-roles-table.md">Roles table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-121">Almacena la lista de posibles roles de conferencia (por ejemplo, asistente y moderador).</span><span class="sxs-lookup"><span data-stu-id="799fa-121">Stores the list of possible conference roles (for example, attendee and presenter).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-122"><a href="lync-server-2013-sipresponsemetadata-table.md">Tabla SIPResponseMetaData en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-122"><a href="lync-server-2013-sipresponsemetadata-table.md">SIPResponseMetaData table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-123">Almacena una lista de códigos de respuesta SIP, así como la clasificación y definición de cada uno de esos códigos.</span><span class="sxs-lookup"><span data-stu-id="799fa-123">Stores a list of SIP response codes and the classification and definition of each of those codes.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supporting-tables"></a><span data-ttu-id="799fa-124">Tablas de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="799fa-124">Supporting Tables</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="799fa-125">Tabla</span><span class="sxs-lookup"><span data-stu-id="799fa-125">Table</span></span></th>
<th><span data-ttu-id="799fa-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="799fa-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="799fa-127"><a href="lync-server-2013-clientversions-table.md">Tabla ClientVersions en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-127"><a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-128">Almacena los clientes (tanto el tipo de cliente como el número de versión) de cada cliente implicado en una llamada con información capturada en esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="799fa-128">Stores the clients (both client type and version number) of each client involved in a call with information captured in this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-129"><a href="lync-server-2013-conferenceuris-table.md">Tabla ConferenceUris en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-129"><a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-130">Almacena una lista de ConferenceURIs que se usan en llamadas relacionadas con la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="799fa-130">Stores a list of ConferenceURIs that are used in conference related calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-131"><a href="lync-server-2013-contenttypes-table.md">Tabla ContentTypes en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-131"><a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-132">Almacena una lista de tipos de contenido de protocolo de inicio de sesión (SIP) que se usan en las llamadas de punto a punto y en las llamadas en conferencia.</span><span class="sxs-lookup"><span data-stu-id="799fa-132">Stores a list of Session Initiation Protocol (SIP) content types that are used in both peer-to-peer calls and conference calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-133"><a href="lync-server-2013-devices-table.md">Tabla Devices en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-133"><a href="lync-server-2013-devices-table.md">Devices table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-134">Almacena una lista de dispositivos, incluidos el fabricante, la versión de hardware y la dirección MAC.</span><span class="sxs-lookup"><span data-stu-id="799fa-134">Stores a list of devices, including their manufacturer, hardware version, and MAC address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-135"><a href="lync-server-2013-dialogs-table.md">Tabla Dialogs en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-135"><a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-136">Almacena información sobre el identificador de cuadro de diálogo para cada sesión de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="799fa-136">Stores information about the Dialog ID for each session in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-137"><a href="lync-server-2013-edgeservers-table.md">Tabla EdgeServers en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-137"><a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-138">Almacena una lista de servidores perimetrales que se usan para llamadas externas.</span><span class="sxs-lookup"><span data-stu-id="799fa-138">Stores a list of Edge Servers that are used for external calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-139"><a href="lync-server-2013-gateways-table.md">Tabla Gateways en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-139"><a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-140">Almacena una lista de puertas de enlace que se usan para llamadas de protocolo de voz a través de Internet (VoIP).</span><span class="sxs-lookup"><span data-stu-id="799fa-140">Stores a list of Gateways that are used for Voice over Internet Protocol (VoIP) calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-141"><a href="lync-server-2013-hardwareversions-table.md">Tabla HardwareVersions en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-141"><a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-142">Almacena una lista de versiones de hardware de los dispositivos (teléfono de escritorio).</span><span class="sxs-lookup"><span data-stu-id="799fa-142">Stores a list of hardware versions of devices (desk phone).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-143"><a href="lync-server-2013-manufacturers-table.md">Tabla Manufacturers en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-143"><a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-144">Almacena una lista de fabricantes de dispositivos (teléfono de escritorio).</span><span class="sxs-lookup"><span data-stu-id="799fa-144">Stores a list of manufacturers of devices (desk phone).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-145"><a href="lync-server-2013-mcus-table.md">Tabla Mcus en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-145"><a href="lync-server-2013-mcus-table.md">Mcus table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-146">Almacena información acerca de los diversos servidores de conferencia A/V y sus URI.</span><span class="sxs-lookup"><span data-stu-id="799fa-146">Stores information about the various A/V Conferencing Servers and their URIs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-147"><a href="lync-server-2013-mediationservers-table.md">Tabla MediationServers en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-147"><a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-148">Almacena una lista de servidores de mediación que se usan para llamadas de VoIP.</span><span class="sxs-lookup"><span data-stu-id="799fa-148">Stores a list of Mediation Servers that are used for VoIP calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-149"><a href="lync-server-2013-phones-table.md">Tabla Phones en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-149"><a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-150">Almacena todos los números de teléfono usados en llamadas VoIP que fueron archivados o cuyos detalles de llamadas fueron grabados.</span><span class="sxs-lookup"><span data-stu-id="799fa-150">Stores all the phone numbers used in VoIP calls that were archived or whose call details were recorded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-151"><a href="lync-server-2013-pools-table.md">Tabla Pools en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-151"><a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-152">Almacena los nombres del grupo en el que se capturan los mensajes INSTANTÁNEos.</span><span class="sxs-lookup"><span data-stu-id="799fa-152">Stores the names of the pool on which IM messages are captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-153"><a href="lync-server-2013-servers-table.md">Tabla Servers en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-153"><a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-154">Almacena el nombre de los servidores implicados en las llamadas.</span><span class="sxs-lookup"><span data-stu-id="799fa-154">Stores the name of servers involved in calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-155"><a href="lync-server-2013-tenants-table.md">Tabla Tenants en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-155"><a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-156">Almacena los espacios empresariales admitidos por la implementación actual.</span><span class="sxs-lookup"><span data-stu-id="799fa-156">Stores the tenants supported by current deployment.</span></span> <span data-ttu-id="799fa-157">Hay algunos inquilinos de compilación para usuarios de empresa, usuarios federados, usuarios de la conectividad de mensajería instantánea pública y usuarios anónimos.</span><span class="sxs-lookup"><span data-stu-id="799fa-157">There some build-in tenants for Enterprise user, Federated User, public IM connectivity user, and Anonymous users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-158"><a href="lync-server-2013-useragentdef-table.md">Tabla UserAgentDef en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-158"><a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-159">Asigna identificadores de agente de usuario a los nombres descriptivos del agente.</span><span class="sxs-lookup"><span data-stu-id="799fa-159">Maps user agent identifiers to the agent’s descriptive names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-160"><a href="lync-server-2013-users-table.md">Tabla Users en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-160"><a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-161">Almacena los URI de usuario de los usuarios que participaron en sesiones grabadas o archivadas en esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="799fa-161">Stores the user URIs of users who have participated in sessions recorded or archived in this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-162"><a href="lync-server-2013-userstatistics-table.md">Tabla UserStatistics en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-162"><a href="lync-server-2013-userstatistics-table.md">UserStatistics table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-163">Almacena información sobre el uso del sistema por un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="799fa-163">Stores information about an individual user’s usage of the system.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-specific-to-conference-cdr-records"></a><span data-ttu-id="799fa-164">Tablas específicas de registros de CDR de conferencia</span><span class="sxs-lookup"><span data-stu-id="799fa-164">Tables Specific to Conference CDR Records</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="799fa-165">Tabla</span><span class="sxs-lookup"><span data-stu-id="799fa-165">Table</span></span></th>
<th><span data-ttu-id="799fa-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="799fa-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="799fa-167"><a href="lync-server-2013-conferences-table.md">Tabla Conferences en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-167"><a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-168">Almacena información sobre todas las conferencias que se archivaron o cuyos detalles se grabaron, incluyendo ConferenceURI, y la hora de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="799fa-168">Stores information about all conferences that were archived or whose details were recorded, including ConferenceURI, and start and end time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-169"><a href="lync-server-2013-conferencesessiondetails-table.md">Tabla ConferenceSessionDetails en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-169"><a href="lync-server-2013-conferencesessiondetails-table.md">ConferenceSessionDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-170">Almacena información sobre todas las sesiones de conferencia basadas en SIP, como la hora de inicio y finalización, el identificador de usuario, el código de respuesta y el identificador de diagnóstico de cada sesión.</span><span class="sxs-lookup"><span data-stu-id="799fa-170">Stores information about every SIP-based conference session, including start and end time, user ID, response code, and diagnostic ID for each session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-171"><a href="lync-server-2013-focusjoinsandleaves-table.md">Tabla FocusJoinsAndLeaves en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-171"><a href="lync-server-2013-focusjoinsandleaves-table.md">FocusJoinsAndLeaves table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-172">Almacena información acerca de las uniones y las hojas de reuniones, incluidos el rol de los usuarios y la versión del cliente.</span><span class="sxs-lookup"><span data-stu-id="799fa-172">Stores information about conference joins and leaves, including users’ role and client version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-173"><a href="lync-server-2013-mcujoinsandleaves-table.md">Tabla McuJoinsAndLeaves en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-173"><a href="lync-server-2013-mcujoinsandleaves-table.md">McuJoinsAndLeaves table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-174">Almacena información sobre los servidores de conferencia A/V implicados en una conferencia y la combinación de usuarios y horas de salida.</span><span class="sxs-lookup"><span data-stu-id="799fa-174">Stores information about the A/V Conferencing Servers that are involved in a conference and the user join and leave times.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-messages-in-im-conferences"></a><span data-ttu-id="799fa-175">Tablas de mensajes en conferencias de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="799fa-175">Tables for Messages in IM Conferences</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="799fa-176">Tabla</span><span class="sxs-lookup"><span data-stu-id="799fa-176">Table</span></span></th>
<th><span data-ttu-id="799fa-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="799fa-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="799fa-178"><a href="lync-server-2013-conferencemessagecount-table.md">Tabla ConferenceMessageCount en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-178"><a href="lync-server-2013-conferencemessagecount-table.md">ConferenceMessageCount table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-179">Para cada Conferencia de mensajería instantánea, almacena el número de mensajes que envió cada usuario.</span><span class="sxs-lookup"><span data-stu-id="799fa-179">For each IM conference, stores the number of messages that were sent by each user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-180"><a href="lync-server-2013-imreportsummary-table.md">Tabla IMReportSummary en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-180"><a href="lync-server-2013-imreportsummary-table.md">IMReportSummary table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-181">Proporciona un informe general sobre las sesiones de mensajería instantánea mantenidas en una organización.</span><span class="sxs-lookup"><span data-stu-id="799fa-181">Provides an overall report on the instant messaging sessions held in an organization.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-peer-to-peer-sessions"></a><span data-ttu-id="799fa-182">Tablas para sesiones de punto a punto</span><span class="sxs-lookup"><span data-stu-id="799fa-182">Tables for Peer-to-Peer Sessions</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="799fa-183">Tabla</span><span class="sxs-lookup"><span data-stu-id="799fa-183">Table</span></span></th>
<th><span data-ttu-id="799fa-184">Descripción</span><span class="sxs-lookup"><span data-stu-id="799fa-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="799fa-185"><a href="lync-server-2013-sessiondetails-table.md">Tabla SessionDetails en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-185"><a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-186">Almacena información sobre cada sesión de punto a punto, incluyendo la hora de inicio y finalización, el identificador de usuario, el código de respuesta y el recuento de mensajes de cada usuario.</span><span class="sxs-lookup"><span data-stu-id="799fa-186">Stores information about every peer-to-peer session, including start and end time, user ID, response code, and message count for each user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-187"><a href="lync-server-2013-filetransfers-table.md">Tabla FileTransfers en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-187"><a href="lync-server-2013-filetransfers-table.md">FileTransfers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-188">Almacena información sobre las sesiones de transferencia de archivos, incluidos el nombre de archivo y el resultado (aceptada, rechazada o cancelada).</span><span class="sxs-lookup"><span data-stu-id="799fa-188">Stores information about file transfer sessions, including file name and result (accepted, rejected, or canceled).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-189"><a href="lync-server-2013-media-table.md">Tabla Media en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-189"><a href="lync-server-2013-media-table.md">Media table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-190">Almacena información sobre los diferentes tipos de medios implicados en sesiones de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="799fa-190">Stores information about the different media types involved in peer-to-peer sessions.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="table-for-voip-call-details"></a><span data-ttu-id="799fa-191">Tabla de detalles de llamadas VoIP</span><span class="sxs-lookup"><span data-stu-id="799fa-191">Table for VoIP Call Details</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="799fa-192">Tabla</span><span class="sxs-lookup"><span data-stu-id="799fa-192">Table</span></span></th>
<th><span data-ttu-id="799fa-193">Descripción</span><span class="sxs-lookup"><span data-stu-id="799fa-193">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="799fa-194"><a href="lync-server-2013-voipdetails-table.md">Tabla VoipDetails en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-194"><a href="lync-server-2013-voipdetails-table.md">VoipDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-195">Para cada llamada de VoIP/RTC de dos partes, almacena información sobre la llamada, como el identificador de teléfono del teléfono VoIP, la puerta de enlace usada y qué parte se desconectó.</span><span class="sxs-lookup"><span data-stu-id="799fa-195">For each two-party VoIP/PSTN call, stores information about the call, such as the phone ID of VoIP phone, gateway used, and which party disconnected.</span></span> <span data-ttu-id="799fa-196">Hace referencia a la <a href="lync-server-2013-sessiondetails-table.md">tabla SessionDetails en Lync Server 2013</a> para las horas de inicio y finalización de la llamada y el código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="799fa-196">Refers to the <a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a> for call start/end times and response code.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="799fa-197">Si una de las partes de una llamada es un usuario de VoIP o si un servidor de mediación participó en la llamada, se creará un registro en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="799fa-197">If one party on a call is a VoIP user or if a Mediation Server was involved in the call, a record will be created in this table.</span></span> <span data-ttu-id="799fa-198">La información sobre las llamadas de VoIP o VoIP que no implica un teléfono de red telefónica conmutada (RTC) se captura en la <A href="lync-server-2013-sessiondetails-table.md">tabla SessionDetails en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="799fa-198">Information about VoIP/VoIP calls not involving a public switched telephone network (PSTN) phone is captured in the <A href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</A>.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="table-for-e9-1-1-call-auditing"></a><span data-ttu-id="799fa-199">Tabla de auditorías de llamadas de E9-1-1</span><span class="sxs-lookup"><span data-stu-id="799fa-199">Table for E9-1-1 Call Auditing</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="799fa-200">Tabla</span><span class="sxs-lookup"><span data-stu-id="799fa-200">Table</span></span></th>
<th><span data-ttu-id="799fa-201">Descripción</span><span class="sxs-lookup"><span data-stu-id="799fa-201">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="799fa-202"><a href="lync-server-2013-locations-table.md">Tabla Locations en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-202"><a href="lync-server-2013-locations-table.md">Locations table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-203">Para cada llamada de emergencia, como una llamada mejorada de 9-1-1 (E9-1-1), almacena información sobre la ubicación de la llamada.</span><span class="sxs-lookup"><span data-stu-id="799fa-203">For each emergency call, such as an Enhanced 9-1-1 (E9-1-1) call, stores location information about the call.</span></span> <span data-ttu-id="799fa-204">Hace referencia a la <a href="lync-server-2013-sessiondetails-table.md">tabla SessionDetails en Lync Server 2013</a> para las horas de inicio y finalización de la llamada y el código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="799fa-204">Refers to the <a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a> for call start/end times and response code.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="799fa-205">Esta tabla solo contiene el BLOB de ubicación para la llamada de E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="799fa-205">This table only contains the location blob for the E9-1-1 call.</span></span> <span data-ttu-id="799fa-206">Hace referencia a la tabla SessionDetails para obtener información detallada sobre la llamada.</span><span class="sxs-lookup"><span data-stu-id="799fa-206">Refers to the SessionDetails table for other detailed information about the call.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-troubleshooting"></a><span data-ttu-id="799fa-207">Tablas para la solución de problemas</span><span class="sxs-lookup"><span data-stu-id="799fa-207">Tables for Troubleshooting</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="799fa-208">Tabla</span><span class="sxs-lookup"><span data-stu-id="799fa-208">Table</span></span></th>
<th><span data-ttu-id="799fa-209">Descripción</span><span class="sxs-lookup"><span data-stu-id="799fa-209">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="799fa-210"><a href="lync-server-2013-application-table.md">Tabla Application en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-210"><a href="lync-server-2013-application-table.md">Application table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-211">Almacena información acerca de los distintos procesos de Lync Server 2013 que participan en el enrutamiento y en las conexiones.</span><span class="sxs-lookup"><span data-stu-id="799fa-211">Stores information about various processes within Lync Server 2013 that are involved in routing and connections.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-212"><a href="lync-server-2013-calltype-table.md">Tabla CallType en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-212"><a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-213">Almacena información sobre los tipos de la llamada, como "audio", "mensajería instantánea", "audio y vídeo" y "uso compartido de aplicaciones".</span><span class="sxs-lookup"><span data-stu-id="799fa-213">Stores information about types of the call, such as, “audio”, “Instant Messaging”, “audio and video” and “application sharing”.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-214"><a href="lync-server-2013-errorcategory-table.md">Tabla ErrorCategory en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-214"><a href="lync-server-2013-errorcategory-table.md">ErrorCategory table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-215">Almacena el nombre descriptivo de cada clasificación de diagnóstico de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="799fa-215">Stores the friendly name for each Microsoft Lync Server 2013 diagnostic classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-216"><a href="lync-server-2013-errordef-table.md">Tabla ErrorDef en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-216"><a href="lync-server-2013-errordef-table.md">ErrorDef table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-217">Almacena información sobre los tipos de errores y sus definiciones.</span><span class="sxs-lookup"><span data-stu-id="799fa-217">Stores information about types of errors and their definitions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-218"><a href="lync-server-2013-errorreport-table.md">Tabla ErrorReport en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-218"><a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-219">Almacena información sobre los errores que se han producido.</span><span class="sxs-lookup"><span data-stu-id="799fa-219">Stores information about errors that have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-220"><a href="lync-server-2013-progressreport-table.md">Tabla ProgressReport en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="799fa-220"><a href="lync-server-2013-progressreport-table.md">ProgressReport table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="799fa-221">Almacena información sobre los informes de progreso de varios pasos implicados en los procesos de 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="799fa-221">Stores information about the progress reports of various steps involved in Lync Server 2013 processes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="799fa-222">Las tablas de la siguiente lista son utilizadas internamente por Lync Server.</span><span class="sxs-lookup"><span data-stu-id="799fa-222">The tables in the following list are used internally by Lync Server.</span></span> <span data-ttu-id="799fa-223">Los detalles no se describen en este documento.</span><span class="sxs-lookup"><span data-stu-id="799fa-223">Their details are not described in this document.</span></span>

</div>

<div>

## <a name="tables-for-internal-use-by-lync-server"></a><span data-ttu-id="799fa-224">Tablas para uso interno de Lync Server</span><span class="sxs-lookup"><span data-stu-id="799fa-224">Tables for Internal Use by Lync Server</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="799fa-225">Tabla</span><span class="sxs-lookup"><span data-stu-id="799fa-225">Table</span></span></th>
<th><span data-ttu-id="799fa-226">Descripción</span><span class="sxs-lookup"><span data-stu-id="799fa-226">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="799fa-227"><strong>DbConfigDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-227"><strong>DbConfigDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-228">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-228">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-229"><strong>DbConfigInt</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-229"><strong>DbConfigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-230">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-230">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-231"><strong>DbErrorMessage</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-231"><strong>DbErrorMessage</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-232">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-232">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-233"><strong>Tabla de FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-233"><strong>FrontEnd Table</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-234">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-234">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-235"><strong>Tabla MSMQProcessing</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-235"><strong>MSMQProcessing Table</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-236">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-236">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-237"><strong>SummaryTableConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-237"><strong>SummaryTableConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-238">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-238">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-239"><strong>Tabla de sindicación</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-239"><strong>Syndicators Table</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-240">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-240">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-241"><strong>Tabla SyndicatorsTenantMap</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-241"><strong>SyndicatorsTenantMap Table</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-242">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-242">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-243"><strong>Tabla de tareas</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-243"><strong>Task Table</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-244">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-244">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-245"><strong>UserStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-245"><strong>UserStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-246">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-246">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-247"><strong>UsageSummary_UQ</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-247"><strong>UsageSummary_UQ</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-248">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-248">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-249"><strong>UsageSummary</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-249"><strong>UsageSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-250">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-250">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-251"><strong>DaylightSavingYears</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-251"><strong>DaylightSavingYears</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-252">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-252">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-253"><strong>TimeZoneConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-253"><strong>TimeZoneConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-254">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-254">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-255"><strong>TimeZones</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-255"><strong>TimeZones</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-256">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-256">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-257"><strong>FailureSummary_UQ</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-257"><strong>FailureSummary_UQ</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-258">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-258">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-259"><strong>FailureSummary</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-259"><strong>FailureSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-260">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-260">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="799fa-261"><strong>ServerSummary</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-261"><strong>ServerSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-262">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-262">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="799fa-263"><strong>MsDiagMetaData</strong></span><span class="sxs-lookup"><span data-stu-id="799fa-263"><strong>MsDiagMetaData</strong></span></span></p></td>
<td><p><span data-ttu-id="799fa-264">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="799fa-264">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="799fa-265">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="799fa-265">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

