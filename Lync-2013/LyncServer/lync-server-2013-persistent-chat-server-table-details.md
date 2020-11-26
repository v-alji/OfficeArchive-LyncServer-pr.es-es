---
title: 'Lync Server 2013: Detalles de la tabla del servidor de chat persistente'
description: 'Lync Server 2013: detalles de la tabla del servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server table details
ms:assetid: c22d4a76-da50-49de-9038-e0ed7b8e1b58
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615034(v=OCS.15)
ms:contentKeyID: 48185323
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a27feaaccf861d537127f06920cf903be5ae000
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443086"
---
# <a name="persistent-chat-server-table-details-in-lync-server-2013"></a><span data-ttu-id="bf023-103">Detalles de la tabla del servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-103">Persistent Chat Server table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf023-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf023-104">

<span> </span></span></span>

<span data-ttu-id="bf023-105">_**Última modificación del tema:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="bf023-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="bf023-106">En los temas siguientes se detallan las columnas de cada una de las tablas de esquema de base de datos de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="bf023-106">The following topics detail the columns in each of the Persistent Chat database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bf023-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bf023-107">In This Section</span></span>

  - [<span data-ttu-id="bf023-108">tblADCookie en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-108">tblADCookie in Lync Server 2013</span></span>](lync-server-2013-tbladcookie.md)

  - [<span data-ttu-id="bf023-109">tblPrincipalMemberDifference en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-109">tblPrincipalMemberDifference in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmemberdifference.md)

  - [<span data-ttu-id="bf023-110">tblADUpdates en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-110">tblADUpdates in Lync Server 2013</span></span>](lync-server-2013-tbladupdates.md)

  - [<span data-ttu-id="bf023-111">tblPrincipalMembers en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-111">tblPrincipalMembers in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmembers.md)

  - [<span data-ttu-id="bf023-112">tblPrincipalMeta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-112">tblPrincipalMeta in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmeta.md)

  - [<span data-ttu-id="bf023-113">tblSkippedAffiliations en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-113">tblSkippedAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblskippedaffiliations.md)

  - [<span data-ttu-id="bf023-114">tblPrincipalType en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-114">tblPrincipalType in Lync Server 2013</span></span>](lync-server-2013-tblprincipaltype.md)

  - [<span data-ttu-id="bf023-115">tblPrincipal enn Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-115">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)

  - [<span data-ttu-id="bf023-116">tblPrincipalAffiliations en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-116">tblPrincipalAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblprincipalaffiliations.md)

  - [<span data-ttu-id="bf023-117">tblNode en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-117">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)

  - [<span data-ttu-id="bf023-118">tblRoleType en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-118">tblRoleType in Lync Server 2013</span></span>](lync-server-2013-tblroletype.md)

  - [<span data-ttu-id="bf023-119">tblScopePrincipal en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-119">tblScopePrincipal in Lync Server 2013</span></span>](lync-server-2013-tblscopeprincipal.md)

  - [<span data-ttu-id="bf023-120">tblPrincipalRole en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-120">tblPrincipalRole in Lync Server 2013</span></span>](lync-server-2013-tblprincipalrole.md)

  - [<span data-ttu-id="bf023-121">tblSiopWhiteList en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-121">tblSiopWhiteList in Lync Server 2013</span></span>](lync-server-2013-tblsiopwhitelist.md)

  - [<span data-ttu-id="bf023-122">tblEnumAttribute en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-122">tblEnumAttribute in Lync Server 2013</span></span>](lync-server-2013-tblenumattribute.md)

  - [<span data-ttu-id="bf023-123">tblEnumValue en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-123">tblEnumValue in Lync Server 2013</span></span>](lync-server-2013-tblenumvalue.md)

  - [<span data-ttu-id="bf023-124">tblPrincipalInvites en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-124">tblPrincipalInvites in Lync Server 2013</span></span>](lync-server-2013-tblprincipalinvites.md)

  - [<span data-ttu-id="bf023-125">tblChat en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-125">tblChat in Lync Server 2013</span></span>](lync-server-2013-tblchat.md)

  - [<span data-ttu-id="bf023-126">tblLastInviteId en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-126">tblLastInviteId in Lync Server 2013</span></span>](lync-server-2013-tbllastinviteid.md)

  - [<span data-ttu-id="bf023-127">tblLastChatId en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-127">tblLastChatId in Lync Server 2013</span></span>](lync-server-2013-tbllastchatid.md)

  - [<span data-ttu-id="bf023-128">tblPreference en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-128">tblPreference in Lync Server 2013</span></span>](lync-server-2013-tblpreference.md)

  - [<span data-ttu-id="bf023-129">tblFileToken en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-129">tblFileToken in Lync Server 2013</span></span>](lync-server-2013-tblfiletoken.md)

  - [<span data-ttu-id="bf023-130">tblServerIdentity en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-130">tblServerIdentity in Lync Server 2013</span></span>](lync-server-2013-tblserveridentity.md)

  - [<span data-ttu-id="bf023-131">tblAdminLock en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-131">tblAdminLock in Lync Server 2013</span></span>](lync-server-2013-tbladminlock.md)

  - [<span data-ttu-id="bf023-132">tblSystemRevision en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-132">tblSystemRevision in Lync Server 2013</span></span>](lync-server-2013-tblsystemrevision.md)

  - [<span data-ttu-id="bf023-133">tblActivePeers en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-133">tblActivePeers in Lync Server 2013</span></span>](lync-server-2013-tblactivepeers.md)

  - [<span data-ttu-id="bf023-134">tblConfig en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-134">tblConfig in Lync Server 2013</span></span>](lync-server-2013-tblconfig.md)

  - [<span data-ttu-id="bf023-135">tblComplianceData en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-135">tblComplianceData in Lync Server 2013</span></span>](lync-server-2013-tblcompliancedata.md)

  - [<span data-ttu-id="bf023-136">tblComplianceFanout en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-136">tblComplianceFanout in Lync Server 2013</span></span>](lync-server-2013-tblcompliancefanout.md)

  - [<span data-ttu-id="bf023-137">tblComplianceParticipant en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-137">tblComplianceParticipant in Lync Server 2013</span></span>](lync-server-2013-tblcomplianceparticipant.md)

  - [<span data-ttu-id="bf023-138">tblComplianceState en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf023-138">tblComplianceState in Lync Server 2013</span></span>](lync-server-2013-tblcompliancestate.md)

<span data-ttu-id="bf023-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf023-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

