---
title: 'Lync Server 2013: Detalles de tablas CDR'
description: 'Lync Server 2013: detalles de la tabla de CDR.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CDR table details
ms:assetid: 896198f5-672b-48ea-852f-0211c0c90857
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398693(v=OCS.15)
ms:contentKeyID: 48184730
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 331a3dfd4ffccac2ac4a442eeb9ad9171defb41c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435484"
---
# <a name="cdr-table-details-in-lync-server-2013"></a><span data-ttu-id="73cd1-103">Detalles de tablas CDR en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-103">CDR table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="73cd1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="73cd1-104">

<span> </span></span></span>

<span data-ttu-id="73cd1-105">_**Última modificación del tema:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="73cd1-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="73cd1-106">En los temas siguientes se detallan las columnas de cada una de las tablas de esquema de la base de datos Records Records Records (CDR).</span><span class="sxs-lookup"><span data-stu-id="73cd1-106">The following topics detail the columns in each of the call detail records (CDR) database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="73cd1-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="73cd1-107">In This Section</span></span>

  - [<span data-ttu-id="73cd1-108">Tabla Application en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-108">Application table in Lync Server 2013</span></span>](lync-server-2013-application-table.md)

  - [<span data-ttu-id="73cd1-109">Tabla CallPriorities en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-109">CallPriorities table in Lync Server 2013</span></span>](lync-server-2013-callpriorities-table.md)

  - [<span data-ttu-id="73cd1-110">Tabla CallType en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-110">CallType table in Lync Server 2013</span></span>](lync-server-2013-calltype-table.md)

  - [<span data-ttu-id="73cd1-111">Tabla ClientVersions en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-111">ClientVersions table in Lync Server 2013</span></span>](lync-server-2013-clientversions-table.md)

  - [<span data-ttu-id="73cd1-112">Tabla ConferenceJoinTimeThresholds en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-112">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>](lync-server-2013-conferencejointimethresholds-table.md)

  - [<span data-ttu-id="73cd1-113">Tabla ConferenceMessageCount en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-113">ConferenceMessageCount table in Lync Server 2013</span></span>](lync-server-2013-conferencemessagecount-table.md)

  - [<span data-ttu-id="73cd1-114">Tabla Conferences en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-114">Conferences table in Lync Server 2013</span></span>](lync-server-2013-conferences-table.md)

  - [<span data-ttu-id="73cd1-115">Tabla ConferenceSessionDetails en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-115">ConferenceSessionDetails table in Lync Server 2013</span></span>](lync-server-2013-conferencesessiondetails-table.md)

  - [<span data-ttu-id="73cd1-116">Tabla ConferenceUris en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-116">ConferenceUris table in Lync Server 2013</span></span>](lync-server-2013-conferenceuris-table.md)

  - [<span data-ttu-id="73cd1-117">Tabla ContentTypes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-117">ContentTypes table in Lync Server 2013</span></span>](lync-server-2013-contenttypes-table.md)

  - [<span data-ttu-id="73cd1-118">Tabla DeRegisterType en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-118">DeRegisterType table in Lync Server 2013</span></span>](lync-server-2013-deregistertype-table.md)

  - [<span data-ttu-id="73cd1-119">Tabla Devices en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-119">Devices table in Lync Server 2013</span></span>](lync-server-2013-devices-table.md)

  - [<span data-ttu-id="73cd1-120">Tabla Dialogs en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-120">Dialogs table in Lync Server 2013</span></span>](lync-server-2013-dialogs-table.md)

  - [<span data-ttu-id="73cd1-121">Tabla EdgeServers en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-121">EdgeServers table in Lync Server 2013</span></span>](lync-server-2013-edgeservers-table.md)

  - [<span data-ttu-id="73cd1-122">Tabla ErrorCategory en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-122">ErrorCategory table in Lync Server 2013</span></span>](lync-server-2013-errorcategory-table.md)

  - [<span data-ttu-id="73cd1-123">Tabla ErrorDef en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-123">ErrorDef table in Lync Server 2013</span></span>](lync-server-2013-errordef-table.md)

  - [<span data-ttu-id="73cd1-124">Tabla ErrorReport en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-124">ErrorReport table in Lync Server 2013</span></span>](lync-server-2013-errorreport-table.md)

  - [<span data-ttu-id="73cd1-125">Tabla FileTransfers en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-125">FileTransfers table in Lync Server 2013</span></span>](lync-server-2013-filetransfers-table.md)

  - [<span data-ttu-id="73cd1-126">Tabla FocusJoinsAndLeaves en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-126">FocusJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-focusjoinsandleaves-table.md)

  - [<span data-ttu-id="73cd1-127">Tabla de FrontEnd en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-127">FrontEnd table in Lync Server 2013</span></span>](lync-server-2013-frontend-table.md)

  - [<span data-ttu-id="73cd1-128">Tabla Gateways en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-128">Gateways table in Lync Server 2013</span></span>](lync-server-2013-gateways-table.md)

  - [<span data-ttu-id="73cd1-129">Tabla HardwareVersions en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-129">HardwareVersions table in Lync Server 2013</span></span>](lync-server-2013-hardwareversions-table.md)

  - [<span data-ttu-id="73cd1-130">Tabla IMReportSummary en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-130">IMReportSummary table in Lync Server 2013</span></span>](lync-server-2013-imreportsummary-table.md)

  - [<span data-ttu-id="73cd1-131">Tabla Locations en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-131">Locations table in Lync Server 2013</span></span>](lync-server-2013-locations-table.md)

  - [<span data-ttu-id="73cd1-132">Tabla Manufacturers en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-132">Manufacturers table in Lync Server 2013</span></span>](lync-server-2013-manufacturers-table.md)

  - [<span data-ttu-id="73cd1-133">Tabla McuJoinsAndLeaves en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-133">McuJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-mcujoinsandleaves-table.md)

  - [<span data-ttu-id="73cd1-134">Tabla Mcus en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-134">Mcus table in Lync Server 2013</span></span>](lync-server-2013-mcus-table.md)

  - [<span data-ttu-id="73cd1-135">Tabla Media en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-135">Media table in Lync Server 2013</span></span>](lync-server-2013-media-table.md)

  - [<span data-ttu-id="73cd1-136">Tabla MediaList en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-136">MediaList table in Lync Server 2013</span></span>](lync-server-2013-medialist-table.md)

  - [<span data-ttu-id="73cd1-137">Tabla MediationServers en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-137">MediationServers table in Lync Server 2013</span></span>](lync-server-2013-mediationservers-table.md)

  - [<span data-ttu-id="73cd1-138">Tabla MSMQProcessing en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-138">MSMQProcessing table in Lync Server 2013</span></span>](lync-server-2013-msmqprocessing-table.md)

  - [<span data-ttu-id="73cd1-139">Tabla Phones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-139">Phones table in Lync Server 2013</span></span>](lync-server-2013-phones-table.md)

  - [<span data-ttu-id="73cd1-140">Tabla Pools en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-140">Pools table in Lync Server 2013</span></span>](lync-server-2013-pools-table.md)

  - [<span data-ttu-id="73cd1-141">Tabla ProgressReport en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-141">ProgressReport table in Lync Server 2013</span></span>](lync-server-2013-progressreport-table.md)

  - [<span data-ttu-id="73cd1-142">Tabla PurgeSettings en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-142">PurgeSettings table in Lync Server 2013</span></span>](lync-server-2013-purgesettings-table.md)

  - [<span data-ttu-id="73cd1-143">Tabla Registration en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-143">Registration table in Lync Server 2013</span></span>](lync-server-2013-registration-table.md)

  - [<span data-ttu-id="73cd1-144">Tabla Roles en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-144">Roles table in Lync Server 2013</span></span>](lync-server-2013-roles-table.md)

  - [<span data-ttu-id="73cd1-145">Tabla Servers en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-145">Servers table in Lync Server 2013</span></span>](lync-server-2013-servers-table.md)

  - [<span data-ttu-id="73cd1-146">Tabla SessionDetails en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-146">SessionDetails table in Lync Server 2013</span></span>](lync-server-2013-sessiondetails-table.md)

  - [<span data-ttu-id="73cd1-147">Tabla SIPResponseMetaData en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-147">SIPResponseMetaData table in Lync Server 2013</span></span>](lync-server-2013-sipresponsemetadata-table.md)

  - [<span data-ttu-id="73cd1-148">Tabla de sindicaciones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-148">Syndicators table in Lync Server 2013</span></span>](lync-server-2013-syndicators-table.md)

  - [<span data-ttu-id="73cd1-149">Tabla SyndicatorsTenantMap en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-149">SyndicatorsTenantMap table in Lync Server 2013</span></span>](lync-server-2013-syndicatorstenantmap-table.md)

  - [<span data-ttu-id="73cd1-150">Tabla de tareas de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-150">Task table in Lync Server 2013</span></span>](lync-server-2013-task-table.md)

  - [<span data-ttu-id="73cd1-151">Tabla Tenants en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-151">Tenants table in Lync Server 2013</span></span>](lync-server-2013-tenants-table.md)

  - [<span data-ttu-id="73cd1-152">Tabla UriTypes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-152">UriTypes table in Lync Server 2013</span></span>](lync-server-2013-uritypes-table.md)

  - [<span data-ttu-id="73cd1-153">Tabla Users en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-153">Users table in Lync Server 2013</span></span>](lync-server-2013-users-table.md)

  - [<span data-ttu-id="73cd1-154">Tabla UserAgentDef en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-154">UserAgentDef table in Lync Server 2013</span></span>](lync-server-2013-useragentdef-table.md)

  - [<span data-ttu-id="73cd1-155">Tabla UserStatistics en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-155">UserStatistics table in Lync Server 2013</span></span>](lync-server-2013-userstatistics-table.md)

  - [<span data-ttu-id="73cd1-156">Tabla VoipDetails en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73cd1-156">VoipDetails table in Lync Server 2013</span></span>](lync-server-2013-voipdetails-table.md)

<span data-ttu-id="73cd1-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="73cd1-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

