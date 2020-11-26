---
title: Migración del chat de grupo de Lync Server 2010 o el chat de grupo de Office Communications Server 2007 R2 al servidor de chat persistente de Lync Server 2013
description: Migración desde Lync Server 2010, chat grupal u Office Communications Server 2007 R2 conversación grupal a Lync Server 2013, servidor de chat persistente.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446860"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a><span data-ttu-id="85c43-103">Migración del chat de grupo de Lync Server 2010 o el chat de grupo de Office Communications Server 2007 R2 al servidor de chat persistente de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85c43-103">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85c43-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85c43-104">

<span> </span></span></span>

<span data-ttu-id="85c43-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="85c43-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="85c43-106">Los temas de esta sección le guían a través del proceso de migración de Lync Server 2010, chat grupal o chat grupal de Office Communications Server 2007 R2 a Lync Server 2013, servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="85c43-106">The topics in this section guide you through the process of migrating either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="85c43-107">Si su intención es que su Lync Server 2013, la implementación del servidor de chat persistente coexista con una implementación de chat grupal de Lync Server 2010, chat grupal u Office Communications Server 2007 R2, esta guía también incluye información esencial para operar en este entorno mixto.</span><span class="sxs-lookup"><span data-stu-id="85c43-107">If you intend for your Lync Server 2013, Persistent Chat Server deployment to coexist with a Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat deployment, this guide also includes some essential information for operating in this mixed environment.</span></span> <span data-ttu-id="85c43-108">Esta guía se centra principalmente en la migración de datos para el servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="85c43-108">This guide primarily focuses on data migration for Persistent Chat Server.</span></span> <span data-ttu-id="85c43-109">Para los usuarios que migren de versiones heredadas de Lync Server a Lync Server 2013, consulte [migración de Lync server 2010 a Lync server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) y [migración de Office Communications Server 2007 R2 a Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="85c43-109">For users who are migrating from legacy versions of Lync Server to Lync Server 2013, see [Migration from Lync Server 2010 to Lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) and [Migration from Office Communications Server 2007 R2 to Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="85c43-110">En este tema se supone que ya ha instalado Lync Server 2013 en coexistencia con Lync Server 2010 u Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85c43-110">This topic assumes that you have already installed Lync Server 2013 in coexistence with Lync Server 2010 or Office Communications Server 2007 R2.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="85c43-111">En esta guía, se describen los pasos necesarios para llevar a cabo cada fase de la migración.</span><span class="sxs-lookup"><span data-stu-id="85c43-111">This guide describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="85c43-112">No se trata de todas las topologías de implementación heredadas o de todos los escenarios posibles de migración.</span><span class="sxs-lookup"><span data-stu-id="85c43-112">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="85c43-113">Por lo tanto, es posible que no tenga que realizar todos los pasos descritos o que necesite realizar pasos adicionales, en función de la implementación.</span><span class="sxs-lookup"><span data-stu-id="85c43-113">Therefore, you may not need to perform every step that is described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="85c43-114">La guía también proporciona ejemplos de pasos de verificación.</span><span class="sxs-lookup"><span data-stu-id="85c43-114">The guide also provides examples of verification steps.</span></span> <span data-ttu-id="85c43-115">Estos pasos de verificación se proporcionan para ayudarle a comprender lo que debe buscar para asegurarse de que cada fase se complete correctamente a medida que avanza en la migración.</span><span class="sxs-lookup"><span data-stu-id="85c43-115">These verification steps are provided to help you understand what you need to look for to be sure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="85c43-116">Puede modificar estos pasos de verificación en su proceso de migración específico.</span><span class="sxs-lookup"><span data-stu-id="85c43-116">You can modify these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="85c43-117">Esta guía proporciona información específica para actualizar la implementación existente.</span><span class="sxs-lookup"><span data-stu-id="85c43-117">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="85c43-118">No se explica cómo cambiar la topología existente.</span><span class="sxs-lookup"><span data-stu-id="85c43-118">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="85c43-119">Esta guía no cubre la implementación de nuevas características.</span><span class="sxs-lookup"><span data-stu-id="85c43-119">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="85c43-120">Cuando un procedimiento detallado está documentado en otra parte, esta guía le dirige a la sección documento o documento adecuada.</span><span class="sxs-lookup"><span data-stu-id="85c43-120">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="85c43-121">Este documento define los términos según se especifican en la siguiente lista.</span><span class="sxs-lookup"><span data-stu-id="85c43-121">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="85c43-122">*realizar*</span><span class="sxs-lookup"><span data-stu-id="85c43-122">*migration*</span></span>  
    <span data-ttu-id="85c43-123">El traslado de la implementación de una versión anterior del servidor de chat persistente, anteriormente conocido como servidor de chat grupal, a Lync Server 2013, servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="85c43-123">Moving your deployment from a previous version of Persistent Chat Server, formerly known as Group Chat Server, to Lync Server 2013, Persistent Chat Server.</span></span>

<!-- end list -->

  - <span data-ttu-id="85c43-124">*actualiza*</span><span class="sxs-lookup"><span data-stu-id="85c43-124">*upgrade*</span></span>  
    <span data-ttu-id="85c43-125">Instalar una versión más reciente del software en un servidor o en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="85c43-125">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="85c43-126">*coexistencia*</span><span class="sxs-lookup"><span data-stu-id="85c43-126">*coexistence*</span></span>  
    <span data-ttu-id="85c43-127">El entorno temporal que existe durante la migración, cuando se ha migrado cierta funcionalidad a Lync Server 2013, el servidor de chat persistente y otras funcionalidades siguen siendo de una versión anterior del servidor de chats grupales.</span><span class="sxs-lookup"><span data-stu-id="85c43-127">The temporary environment that exists during migration, when some functionality has been migrated to Lync Server 2013, Persistent Chat Server, and other functionality still remains on a prior version of Group Chat Server.</span></span>

<span data-ttu-id="85c43-128">El servidor de chat persistente es una extensión de la infraestructura de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="85c43-128">Persistent Chat Server is an extension of the Lync Server 2013 infrastructure.</span></span> <span data-ttu-id="85c43-129">Dependiendo de su topología, puede migrar Lync Server 2010, chat grupal u Office Communications Server 2007 R2 chat grupal a Lync Server 2013 servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="85c43-129">Depending on your topology, you can migrate Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="85c43-130">Para obtener detalles sobre las topologías disponibles y los requisitos técnicos y de software para migrar servidor de chat de grupo, consulte [planificación de servidor de chat persistente en Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) en la documentación de planificación.</span><span class="sxs-lookup"><span data-stu-id="85c43-130">For details about available topologies and the technical and software requirements for migrating Group Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

<span data-ttu-id="85c43-131">Si su organización requiere soporte de cumplimiento, ahora se instala automáticamente con cada servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="85c43-131">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="85c43-132">Ya no se necesita un servidor independiente para el cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="85c43-132">A separate server is no longer needed for compliance.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="85c43-133">El servidor de chat persistente debe instalarse en un sistema de archivos NTFS para ayudar a exigir la seguridad del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="85c43-133">Persistent Chat Server must be installed on an NTFS file system to help enforce file system security.</span></span> <span data-ttu-id="85c43-134">FAT32 no es un sistema de archivos compatible para el servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="85c43-134">FAT32 is not a supported file system for Persistent Chat Server.</span></span><BR><span data-ttu-id="85c43-135">Si su organización requiere soporte de cumplimiento, ahora se instala automáticamente con cada servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="85c43-135">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="85c43-136">Ya no se necesita un servidor independiente para el cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="85c43-136">A separate server is no longer needed for compliance.</span></span> <span data-ttu-id="85c43-137">Para obtener más detalles sobre los cambios en el servidor de chat persistente de Lync Server 2013 &nbsp; , consulte <A href="lync-server-2013-new-persistent-chat-server-features.md">nuevas características del servidor de chat persistente en lync Server 2013</A> en la documentación de introducción.</span><span class="sxs-lookup"><span data-stu-id="85c43-137">For more details about changes in Lync Server 2013&nbsp;Persistent Chat Server, see <A href="lync-server-2013-new-persistent-chat-server-features.md">New Persistent Chat Server features in Lync Server 2013</A> in the Getting Started documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="85c43-138">En esta sección</span><span class="sxs-lookup"><span data-stu-id="85c43-138">In This Section</span></span>

  - [<span data-ttu-id="85c43-139">Escenario de migración estándar - Alto nivel</span><span class="sxs-lookup"><span data-stu-id="85c43-139">Standard migration scenario - high-level</span></span>](standard-migration-scenario-high-level.md)

  - [<span data-ttu-id="85c43-140">Proceso de migración - Detalles</span><span class="sxs-lookup"><span data-stu-id="85c43-140">Migration process - details</span></span>](migration-process-details.md)

  - [<span data-ttu-id="85c43-141">Consideraciones sobre la coexistencia</span><span class="sxs-lookup"><span data-stu-id="85c43-141">Coexistence considerations</span></span>](coexistence-considerations.md)

<span data-ttu-id="85c43-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85c43-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

