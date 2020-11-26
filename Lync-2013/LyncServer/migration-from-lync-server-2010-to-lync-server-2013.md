---
title: Migrar Lync Server 2010 a Lync Server 2013
description: Migración de Lync Server 2010 a Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010 to Lync Server 2013
ms:assetid: ef99d4a9-a666-4a92-9994-4d7930f70d55
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205369(v=OCS.15)
ms:contentKeyID: 48185779
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbe1bc1b7745c5ddc89a7f8fb64295a82f52c9bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438599"
---
# <a name="migration-from-lync-server-2010-to-lync-server-2013"></a><span data-ttu-id="51fe5-103">Migrar Lync Server 2010 a Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51fe5-103">Migration from Lync Server 2010 to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="51fe5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="51fe5-104">

<span> </span></span></span>

<span data-ttu-id="51fe5-105">_**Última modificación del tema:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="51fe5-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="51fe5-106">Los temas de esta sección le guiarán a través del proceso de migración de Lync Server 2010 a Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="51fe5-106">The topics in this section guide you through the process of migrating from Lync Server 2010 to Lync Server 2013.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="51fe5-107">Este documento describe los pasos que generalmente se necesitan para realizar cada fase de la migración.</span><span class="sxs-lookup"><span data-stu-id="51fe5-107">This document describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="51fe5-108">No se trata de todas las topologías de implementación heredadas o de todos los escenarios posibles de migración.</span><span class="sxs-lookup"><span data-stu-id="51fe5-108">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="51fe5-109">Por lo tanto, es posible que no tenga que realizar cada paso descrito, o puede que tenga que realizar algunos pasos adicionales, en función de su implementación.</span><span class="sxs-lookup"><span data-stu-id="51fe5-109">Therefore, you may not need to perform every step described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="51fe5-110">Este documento también proporciona ejemplos de pasos de verificación.</span><span class="sxs-lookup"><span data-stu-id="51fe5-110">This document also provides examples of verification steps.</span></span> <span data-ttu-id="51fe5-111">Estos pasos de verificación se proporcionan para ayudarle a comprender lo que debe buscar para asegurarse de que cada fase se complete correctamente a medida que avanza en la migración.</span><span class="sxs-lookup"><span data-stu-id="51fe5-111">These verification steps are provided to help you understand what you need to look for to ensure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="51fe5-112">Adapte estos pasos de verificación a su proceso de migración específico.</span><span class="sxs-lookup"><span data-stu-id="51fe5-112">Tailor these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="51fe5-113">Esta guía proporciona información específica para actualizar la implementación existente.</span><span class="sxs-lookup"><span data-stu-id="51fe5-113">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="51fe5-114">No se explica cómo cambiar la topología existente.</span><span class="sxs-lookup"><span data-stu-id="51fe5-114">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="51fe5-115">Esta guía no cubre la implementación de nuevas características.</span><span class="sxs-lookup"><span data-stu-id="51fe5-115">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="51fe5-116">Cuando un procedimiento detallado está documentado en otra parte, esta guía le dirige a la sección documento o documento adecuada.</span><span class="sxs-lookup"><span data-stu-id="51fe5-116">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="51fe5-117">Este documento define los términos según se especifican en la siguiente lista.</span><span class="sxs-lookup"><span data-stu-id="51fe5-117">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="51fe5-118">*realizar*</span><span class="sxs-lookup"><span data-stu-id="51fe5-118">*migration*</span></span>  
    <span data-ttu-id="51fe5-119">Mover la implementación de producción de una versión anterior de Lync Server 2010 a Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="51fe5-119">Moving your production deployment from a previous version of Lync Server 2010 to Lync Server 2013.</span></span>

<!-- end list -->

  - <span data-ttu-id="51fe5-120">*actualiza*</span><span class="sxs-lookup"><span data-stu-id="51fe5-120">*upgrade*</span></span>  
    <span data-ttu-id="51fe5-121">Instalar una versión más reciente del software en un servidor o en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="51fe5-121">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="51fe5-122">*coexistencia*</span><span class="sxs-lookup"><span data-stu-id="51fe5-122">*coexistence*</span></span>  
    <span data-ttu-id="51fe5-123">El entorno temporal que existe durante la migración cuando se ha migrado cierta funcionalidad a Lync Server 2013 y otras funciones siguen en una versión anterior de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="51fe5-123">The temporary environment that exists during migration when some functionality has been migrated to Lync Server 2013 and other functionality still remains on a prior version of Lync Server 2010.</span></span>

<!-- end list -->

  - <span data-ttu-id="51fe5-124">*interoperabilidad*</span><span class="sxs-lookup"><span data-stu-id="51fe5-124">*interoperability*</span></span>  
    <span data-ttu-id="51fe5-125">La capacidad de la implementación para funcionar correctamente durante el período de coexistencia.</span><span class="sxs-lookup"><span data-stu-id="51fe5-125">The ability of your deployment to operate successfully during the period of coexistence.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="51fe5-126">En esta sección</span><span class="sxs-lookup"><span data-stu-id="51fe5-126">In This Section</span></span>

  - [<span data-ttu-id="51fe5-127">Antes de comenzar la migración</span><span class="sxs-lookup"><span data-stu-id="51fe5-127">Before you begin the migration</span></span>](before-you-begin-the-migration.md)

  - [<span data-ttu-id="51fe5-128">Fase 1: planear la migración desde Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="51fe5-128">Phase 1: Plan your migration from Lync Server 2010</span></span>](phase-1-plan-your-migration-from-lync-server-2010.md)

  - [<span data-ttu-id="51fe5-129">Fase 2: Preparación de la migración</span><span class="sxs-lookup"><span data-stu-id="51fe5-129">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

  - [<span data-ttu-id="51fe5-130">Fase 3: implementar el grupo de pruebas piloto de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51fe5-130">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="51fe5-131">Fase 4: mover los usuarios de prueba al grupo piloto</span><span class="sxs-lookup"><span data-stu-id="51fe5-131">Phase 4: Move test users to the pilot pool</span></span>](phase-4-move-test-users-to-the-pilot-pool.md)

  - [<span data-ttu-id="51fe5-132">Fase 5: agregar el servidor perimetral 2013 de Lync Server a un grupo piloto</span><span class="sxs-lookup"><span data-stu-id="51fe5-132">Phase 5: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-5-add-lync-server-2013-edge-server-to-pilot-pool.md)

  - [<span data-ttu-id="51fe5-133">Fase 6: Pasar de la implementación piloto a la producción</span><span class="sxs-lookup"><span data-stu-id="51fe5-133">Phase 6: Move from pilot deployment into production</span></span>](phase-6-move-from-pilot-deployment-into-production.md)

  - [<span data-ttu-id="51fe5-134">Fase 7: Finalización de las tareas posteriores a la migración</span><span class="sxs-lookup"><span data-stu-id="51fe5-134">Phase 7: Complete post-migration tasks</span></span>](phase-7-complete-post-migration-tasks.md)

  - [<span data-ttu-id="51fe5-135">Fase 8: Retirar los grupos de servidores heredados</span><span class="sxs-lookup"><span data-stu-id="51fe5-135">Phase 8: Decommission legacy pools</span></span>](phase-8-decommission-legacy-pools.md)

<span data-ttu-id="51fe5-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="51fe5-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

