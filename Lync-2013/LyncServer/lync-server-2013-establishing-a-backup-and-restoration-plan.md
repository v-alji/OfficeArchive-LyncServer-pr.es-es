---
title: 'Lync Server 2013: establecimiento de un plan de copia de seguridad y restauración'
description: 'Lync Server 2013: establecimiento de un plan de copia de seguridad y restauración.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Establishing a backup and restoration plan
ms:assetid: 9f562ef1-3804-41e2-b3e4-d45b2e8c63c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202183(v=OCS.15)
ms:contentKeyID: 51541499
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06d93c713364bf6b5f230b255b68a2c1dfe1d04a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428464"
---
# <a name="establishing-a-backup-and-restoration-plan-for-lync-server-2013"></a><span data-ttu-id="5d843-103">Establecer un plan de copia de seguridad y restauración para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d843-103">Establishing a backup and restoration plan for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d843-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d843-104">

<span> </span></span></span>

<span data-ttu-id="5d843-105">_**Última modificación del tema:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="5d843-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="5d843-106">Para crear un plan de copia de seguridad y restauración, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="5d843-106">Creating a backup and restoration plan involves the following steps:</span></span>

  - <span data-ttu-id="5d843-107">Desarrollar el plan.</span><span class="sxs-lookup"><span data-stu-id="5d843-107">Developing the plan.</span></span>

  - <span data-ttu-id="5d843-108">Implementar el plan.</span><span class="sxs-lookup"><span data-stu-id="5d843-108">Implementing the plan.</span></span>

  - <span data-ttu-id="5d843-109">Mantenimiento del plan.</span><span class="sxs-lookup"><span data-stu-id="5d843-109">Maintaining the plan.</span></span>

<div>

## <a name="developing-a-backup-and-restoration-plan"></a><span data-ttu-id="5d843-110">Desarrollar un plan de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="5d843-110">Developing a Backup and Restoration Plan</span></span>

<span data-ttu-id="5d843-111">Después de desarrollar la estrategia de copia de seguridad y restauración de Lync Server, Úsela para documentar un plan detallado de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="5d843-111">After you develop your backup and restoration strategy for Lync Server, use it to document a detailed backup and restoration plan.</span></span> <span data-ttu-id="5d843-112">Su plan debe transmitir claramente las prioridades y los requisitos para realizar copias de seguridad de los datos y la configuración.</span><span class="sxs-lookup"><span data-stu-id="5d843-112">Your plan should clearly convey the priorities and requirements for backing up data and settings.</span></span> <span data-ttu-id="5d843-113">Puede usar la información contenida en [establecer una estrategia de copia de seguridad y restauración para Lync server 2013](lync-server-2013-establishing-a-backup-and-restoration-strategy.md) y las hojas de cálculo de [copia de seguridad y restauración de Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md) para facilitar la documentación de su estrategia.</span><span class="sxs-lookup"><span data-stu-id="5d843-113">You can use the information in [Establishing a backup and restoration strategy for Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-strategy.md) and the worksheets in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md) to facilitate the documentation of your strategy.</span></span> <span data-ttu-id="5d843-114">Su plan debe contener también criterios para decidir cuándo y cómo restaurar el servicio.</span><span class="sxs-lookup"><span data-stu-id="5d843-114">Your plan should also contain criteria for deciding when and how to restore service.</span></span>

<span data-ttu-id="5d843-115">A medida que desarrolla su plan, debe tener en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5d843-115">As you develop your plan, you need to consider, and account for, the following:</span></span>

  - <span data-ttu-id="5d843-116">Cómo se recuperan los servidores en el nuevo hardware.</span><span class="sxs-lookup"><span data-stu-id="5d843-116">How you will recover servers on new hardware.</span></span>

  - <span data-ttu-id="5d843-117">Cómo se recuperan los servicios que requieren una acción en la parte de varias áreas o departamentos empresariales.</span><span class="sxs-lookup"><span data-stu-id="5d843-117">How you will recover services that require action on the part of multiple business areas or departments.</span></span>

  - <span data-ttu-id="5d843-118">Cómo puede adquirir servidores de repuesto rápidamente.</span><span class="sxs-lookup"><span data-stu-id="5d843-118">How you can acquire spare servers quickly.</span></span>

  - <span data-ttu-id="5d843-119">El tiempo que se tarda en recuperarse con su estrategia.</span><span class="sxs-lookup"><span data-stu-id="5d843-119">The time it takes to recover by using your strategy.</span></span> <span data-ttu-id="5d843-120">Considere los requisitos de la organización para el objetivo de tiempo de recuperación (RTO).</span><span class="sxs-lookup"><span data-stu-id="5d843-120">Consider your organization’s requirements for recovery time objective (RTO).</span></span>

<span data-ttu-id="5d843-121">Modifique los procedimientos de copia de seguridad y restauración de este tema, agregando y eliminando procedimientos según corresponda, para reflejar los servidores y componentes de su implementación.</span><span class="sxs-lookup"><span data-stu-id="5d843-121">Modify the backup and restoration procedures in this topic, adding and deleting procedures as appropriate, to reflect the servers and components in your deployment.</span></span> <span data-ttu-id="5d843-122">También puede agregar detalles apropiados, como la programación de la copia de seguridad, a los procedimientos apropiados para asegurarse de que la información no se ha descargado.</span><span class="sxs-lookup"><span data-stu-id="5d843-122">You can also add appropriate details, such as the backup schedule, to the appropriate procedures to make sure that the information is not overlooked.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5d843-123">Es recomendable crear scripts para tantos pasos como sea posible para garantizar la calidad y la reproducibilidad de los procedimientos.</span><span class="sxs-lookup"><span data-stu-id="5d843-123">It is good practice to create scripts for as many steps as possible, to help ensure the quality and reproducibility of procedures.</span></span>



</div>

<span data-ttu-id="5d843-124">En su plan, especifique quién es el responsable de revisar el plan, quién es el responsable de probar y validar los nuevos procedimientos o herramientas, y quién debe aprobar los cambios en el plan y los procedimientos relacionados.</span><span class="sxs-lookup"><span data-stu-id="5d843-124">In your plan, specify who is responsible for reviewing the plan, who is responsible for testing and validating any new procedures or tools, and who must approve any changes to the plan and related procedures.</span></span>

<span data-ttu-id="5d843-125">Para asegurarse de que el plan de copia de seguridad y restauración cumple todos los objetivos y las prioridades establecidos, obtenga la aprobación de los responsables de la toma de decisiones empresariales y los responsables de las decisiones técnicas correspondientes de la organización antes de implementar el plan.</span><span class="sxs-lookup"><span data-stu-id="5d843-125">To make sure that your backup and restoration plan fully meets all established goals and priorities, get the approval of the appropriate business decision makers and technical decision makers in your organization before you implement the plan.</span></span>

</div>

<div>

## <a name="implementing-the-backup-and-restoration-plan"></a><span data-ttu-id="5d843-126">Implementación del plan de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="5d843-126">Implementing the Backup and Restoration Plan</span></span>

<span data-ttu-id="5d843-127">Para implementar un plan de copia de seguridad y restauración, debe seguir estos pasos:</span><span class="sxs-lookup"><span data-stu-id="5d843-127">Implementing a backup and restoration plan requires the following steps:</span></span>

  - <span data-ttu-id="5d843-128">Probar y validar el plan.</span><span class="sxs-lookup"><span data-stu-id="5d843-128">Testing and validating the plan.</span></span>

  - <span data-ttu-id="5d843-129">Comunicar el plan.</span><span class="sxs-lookup"><span data-stu-id="5d843-129">Communicating the plan.</span></span>

  - <span data-ttu-id="5d843-130">Validación de las operaciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="5d843-130">Validating backup and restoration operations.</span></span>

<div>

## <a name="testing-and-validating-the-plan"></a><span data-ttu-id="5d843-131">Probar y validar el plan</span><span class="sxs-lookup"><span data-stu-id="5d843-131">Testing and Validating the Plan</span></span>

<span data-ttu-id="5d843-132">Los procedimientos descritos aquí se han probado y validado en un entorno de laboratorio.</span><span class="sxs-lookup"><span data-stu-id="5d843-132">The procedures described here have been tested and validated in a lab environment.</span></span> <span data-ttu-id="5d843-133">Para asegurarse de que estos u otros procedimientos funcionan en su entorno, debe probar y validar cada procedimiento que desee implementar.</span><span class="sxs-lookup"><span data-stu-id="5d843-133">To make sure that these or any other procedures work in your environment, you should test and validate each procedure you intend to implement.</span></span> <span data-ttu-id="5d843-134">Complete las pruebas y la validación antes de enviar su plan para la aprobación final.</span><span class="sxs-lookup"><span data-stu-id="5d843-134">Complete the testing and the validation before you submit your plan for final approval.</span></span>

</div>

<div>

## <a name="communicating-the-plan"></a><span data-ttu-id="5d843-135">Comunicar el plan</span><span class="sxs-lookup"><span data-stu-id="5d843-135">Communicating the Plan</span></span>

<span data-ttu-id="5d843-136">El plan de copia de seguridad y restauración debería describir claramente quién implementa procedimientos e instrucciones paso a paso para llevar a cabo los procedimientos.</span><span class="sxs-lookup"><span data-stu-id="5d843-136">Your backup and restoration plan should clearly describe who implements procedures and step-by-step instructions for carrying out the procedures.</span></span> <span data-ttu-id="5d843-137">Debe asegurarse de que todos los responsables de cualquier aspecto de la copia de seguridad y restauración entienden el plan, cómo se va a implementar y cuál es su función.</span><span class="sxs-lookup"><span data-stu-id="5d843-137">You should make sure that everyone responsible for any aspect of backup and restoration understands the plan, how it is to be implemented, and what their role is.</span></span> <span data-ttu-id="5d843-138">Esto incluye todos los requisitos de implementación para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5d843-138">This includes all implementation requirements for the following:</span></span>

  - <span data-ttu-id="5d843-139">Copia de seguridad del servidor y del grupo.</span><span class="sxs-lookup"><span data-stu-id="5d843-139">Pool and server backup.</span></span>

  - <span data-ttu-id="5d843-140">Restauración de servicio.</span><span class="sxs-lookup"><span data-stu-id="5d843-140">Restoration of service.</span></span>

<span data-ttu-id="5d843-141">**Copia de seguridad del servidor y del grupo**</span><span class="sxs-lookup"><span data-stu-id="5d843-141">**Pool and server backup**</span></span>

<span data-ttu-id="5d843-142">El plan de copia de seguridad y restauración debe incluir toda la información necesaria para completar procedimientos de copia de seguridad de manera continua.</span><span class="sxs-lookup"><span data-stu-id="5d843-142">The backup and restoration plan should include all information required to complete backup procedures on an ongoing basis.</span></span> <span data-ttu-id="5d843-143">La información principal que se debe transmitir a los miembros del equipo responsable incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5d843-143">The primary information to be communicated to responsible team members includes the following:</span></span>

  - <span data-ttu-id="5d843-144">Equipo o persona (especificada como una persona o rol) responsable de realizar la copia de seguridad de cada servidor.</span><span class="sxs-lookup"><span data-stu-id="5d843-144">Team or person (specified as an individual or role) responsible for backing up each server.</span></span>

  - <span data-ttu-id="5d843-145">Programaciones específicas para realizar copias de seguridad de cada servidor.</span><span class="sxs-lookup"><span data-stu-id="5d843-145">Specific schedules for backing up each server.</span></span>

  - <span data-ttu-id="5d843-146">Ubicaciones de copia de seguridad para cada tipo de datos (configuración, base de datos y recursos compartidos de archivos).</span><span class="sxs-lookup"><span data-stu-id="5d843-146">Backup locations for each type of data (settings, database, and file shares).</span></span>

  - <span data-ttu-id="5d843-147">Procedimientos de copia de seguridad que se deben usar, incluidas las herramientas necesarias para completar cada procedimiento.</span><span class="sxs-lookup"><span data-stu-id="5d843-147">Backup procedures to be used, including the tools required to complete each procedure.</span></span>

  - <span data-ttu-id="5d843-148">Información necesaria para completar las copias de seguridad, como se explica en las [hojas de cálculo de copia de seguridad y restauración de Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span><span class="sxs-lookup"><span data-stu-id="5d843-148">Information required to complete backups, as covered in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

  - <span data-ttu-id="5d843-149">Métodos de validación que se van a usar para ayudar a garantizar que se realicen copias de seguridad de los datos y la configuración correctamente y que estén disponibles para la restauración, que pueden incluir auditorías periódicas y restauraciones de prueba.</span><span class="sxs-lookup"><span data-stu-id="5d843-149">Validation methods to be used to help ensure that data and settings are appropriately backed up and available for restoration, which can include periodic audits and test restorations.</span></span>

<span data-ttu-id="5d843-150">**Restauración del servicio**</span><span class="sxs-lookup"><span data-stu-id="5d843-150">**Restoration of service**</span></span>

<span data-ttu-id="5d843-151">El plan de copia de seguridad y restauración debe incluir toda la información necesaria para restaurar el servicio, en caso de que uno o varios servidores experimenten una pérdida que hace que el servicio no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="5d843-151">The backup and restoration plan should include all information required to restore service, in case one or more servers experience a loss that makes service unavailable.</span></span> <span data-ttu-id="5d843-152">La información principal que se debe transmitir a los miembros del equipo responsable incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5d843-152">The primary information to be communicated to responsible team members includes the following:</span></span>

  - <span data-ttu-id="5d843-153">El equipo o la persona (especificados como una persona o un rol) que sea responsable de determinar cuándo se necesita la restauración del servicio y los procedimientos que se deben usar para restaurar el servicio, así como el equipo o la persona responsable de implementar procedimientos para cada escenario de restauración.</span><span class="sxs-lookup"><span data-stu-id="5d843-153">Team or person (specified as an individual or a role) that is responsible for determining when restoration of service is required and the procedures to be used to restore service, and also the team or person responsible for implementing procedures for each restoration scenario.</span></span>

  - <span data-ttu-id="5d843-154">Criterios para determinar qué procedimientos de restauración son los más adecuados para una situación específica.</span><span class="sxs-lookup"><span data-stu-id="5d843-154">Criteria for determining which restoration procedures are most appropriate for a specific situation.</span></span>

  - <span data-ttu-id="5d843-155">Tiempo estimado para la restauración del objetivo de servicio y tiempo de recuperación (RTO) en cada escenario de restauración.</span><span class="sxs-lookup"><span data-stu-id="5d843-155">Time estimates for restoration of service and recovery time objective (RTO) in each restoration scenario.</span></span>

  - <span data-ttu-id="5d843-156">Procedimientos de restauración que se deben usar, incluidas las herramientas necesarias para completar cada procedimiento.</span><span class="sxs-lookup"><span data-stu-id="5d843-156">Restoration procedures to be used, including the tools required to complete each procedure.</span></span>

  - <span data-ttu-id="5d843-157">Información necesaria para restaurar los datos y la configuración.</span><span class="sxs-lookup"><span data-stu-id="5d843-157">Information required to restore data and settings.</span></span> <span data-ttu-id="5d843-158">Las hojas de cálculo se proporcionan en las [hojas de cálculo de copia de seguridad y restauración de Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span><span class="sxs-lookup"><span data-stu-id="5d843-158">Worksheets are provided in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

</div>

<div>

## <a name="validating-backup-and-restoration-operations"></a><span data-ttu-id="5d843-159">Validación de las operaciones de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="5d843-159">Validating Backup and Restoration Operations</span></span>

<span data-ttu-id="5d843-160">Después de completar los esfuerzos de copia de seguridad inicial en el entorno de producción y en intervalos especificados (según se cubre en el plan de copia de seguridad y restauración), debe comprobar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5d843-160">After completing initial backup efforts in your production environment and at specified intervals (as covered in your backup and restoration plan), you should verify the following:</span></span>

  - <span data-ttu-id="5d843-161">Las copias de seguridad se producen según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="5d843-161">Backups are occurring as required.</span></span>

  - <span data-ttu-id="5d843-162">Los datos y la configuración de la copia de seguridad son accesibles.</span><span class="sxs-lookup"><span data-stu-id="5d843-162">Backed-up data and settings are accessible.</span></span>

  - <span data-ttu-id="5d843-163">Los procedimientos de restauración se pueden realizar en las horas de objetivo de tiempo de recuperación (RTO) especificadas en el plan de copia de seguridad y restauración, y los resultados cumplen todos los requisitos empresariales.</span><span class="sxs-lookup"><span data-stu-id="5d843-163">Restoration procedures can be performed within the recovery time objective (RTO) times specified in the backup and restoration plan, and the results meet all business requirements.</span></span>

  - <span data-ttu-id="5d843-164">Las hojas de cálculo de copia de seguridad se han completado y verificado, y se almacenan en un lugar seguro.</span><span class="sxs-lookup"><span data-stu-id="5d843-164">Backup worksheets have been completed and verified, and they are stored in a secure location.</span></span> <span data-ttu-id="5d843-165">Estas hojas de cálculo se proporcionan en las [hojas de cálculo de copia de seguridad y restauración de Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span><span class="sxs-lookup"><span data-stu-id="5d843-165">These worksheets are provided in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

  - <span data-ttu-id="5d843-166">Los procedimientos de restauración han sido probados y verificados para funcionar según lo esperado, según lo especificado en el plan de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="5d843-166">Restoration procedures have been tested and verified to work as expected, as specified in your backup and restoration plan.</span></span>

</div>

</div>

<div>

## <a name="maintaining-the-backup-and-restoration-plan"></a><span data-ttu-id="5d843-167">Mantenimiento del plan de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="5d843-167">Maintaining the Backup and Restoration Plan</span></span>

<span data-ttu-id="5d843-168">Una topología de Lync Server es un entorno dinámico que cambia con su organización.</span><span class="sxs-lookup"><span data-stu-id="5d843-168">A Lync Server topology is a dynamic environment that changes with your organization.</span></span> <span data-ttu-id="5d843-169">Reevalúe el plan de copia de seguridad y restauración a medida que su organización cambie y revise periódicamente para asegurarse de que continúa satisfaciendo las necesidades de su empresa.</span><span class="sxs-lookup"><span data-stu-id="5d843-169">Reassess your backup and restoration plan as your organization changes, and review it periodically to make sure that it continues to meet the needs of your business.</span></span>

<span data-ttu-id="5d843-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d843-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

