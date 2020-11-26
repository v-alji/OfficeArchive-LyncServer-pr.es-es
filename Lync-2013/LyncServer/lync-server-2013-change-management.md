---
title: 'Lync Server 2013: administración de cambios'
description: 'Lync Server 2013: administración de cambios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Change management
ms:assetid: 73c774f5-c12f-4c72-be73-e07dc745b994
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720336(v=OCS.15)
ms:contentKeyID: 63969618
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69ea019f6366528c40b60a39ca8b646b49b336b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435129"
---
# <a name="change-management-in-lync-server-2013"></a><span data-ttu-id="0857f-103">Administración de cambios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0857f-103">Change management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0857f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0857f-104">

<span> </span></span></span>

<span data-ttu-id="0857f-105">_**Última modificación del tema:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="0857f-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="0857f-106">Los cambios en el entorno de TI son inevitables.</span><span class="sxs-lookup"><span data-stu-id="0857f-106">Changes to the IT environment are unavoidable.</span></span> <span data-ttu-id="0857f-107">Los cambios incluyen nuevas tecnologías, sistemas, aplicaciones, hardware, herramientas, procesos y cambios en roles y responsabilidades.</span><span class="sxs-lookup"><span data-stu-id="0857f-107">Changes include new technologies, systems, applications, hardware, tools, processes, and changes in roles and responsibilities.</span></span> <span data-ttu-id="0857f-108">Un sistema de administración de cambios eficaz le permite introducir cambios en el entorno de ti rápidamente y con interrupciones mínimas en el servicio.</span><span class="sxs-lookup"><span data-stu-id="0857f-108">An effective change management system lets you introduce changes to the IT environment quickly and with minimal service disruption.</span></span> <span data-ttu-id="0857f-109">Un sistema de administración de cambios reúne los equipos implicados en el cambio de sistema.</span><span class="sxs-lookup"><span data-stu-id="0857f-109">A change management system brings together the teams involved in changing a system.</span></span> <span data-ttu-id="0857f-110">Por ejemplo, decidir sacar partido de Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="0857f-110">For example, deciding to take advantage of the Office Web Apps.</span></span> <span data-ttu-id="0857f-111">Esta es una aplicación de servicio de Lync integrada que permite a los usuarios leer y editar documentos en un explorador.</span><span class="sxs-lookup"><span data-stu-id="0857f-111">This is an integrated Lync Service application that enables users to read and edit documents in a browser.</span></span> <span data-ttu-id="0857f-112">La implementación de este servicio, después de haber ido a producción, requiere la participación de varios equipos:</span><span class="sxs-lookup"><span data-stu-id="0857f-112">The implementation of this service, after you have gone into production, requires the involvement of several teams:</span></span>

  - <span data-ttu-id="0857f-113">**Equipo de pruebas**   Esta carga de equipo prueba las aplicaciones Web de Office en un servidor de prueba, en el proceso que proporciona información sobre los patrones de uso esperados y el rendimiento esperado de los servidores de producción.</span><span class="sxs-lookup"><span data-stu-id="0857f-113">**Test Team**   This team load-tests the Office Web Apps on a test server, in the process providing information about the expected usage patterns and expected performance of the production servers.</span></span>

  - <span data-ttu-id="0857f-114">**Administradores de Lync**   Este equipo determina la estrategia de implementación y las secuencias de comandos de la instalación donde fue posible.</span><span class="sxs-lookup"><span data-stu-id="0857f-114">**Lync Administrators**   This team determines the deployment strategy and scripts the installation where it was possible.</span></span> <span data-ttu-id="0857f-115">El equipo es responsable de asegurarse de que el cambio se implementa en el entorno de producción, y es responsable de la administración más adelante.</span><span class="sxs-lookup"><span data-stu-id="0857f-115">The team is responsible for making sure that the change is deployed on the production environment, and it is responsible for administration afterward.</span></span> <span data-ttu-id="0857f-116">El equipo debe comprender el efecto de los cambios e incorporarlos en procedimientos antes de que los cambios se pongan en producción.</span><span class="sxs-lookup"><span data-stu-id="0857f-116">The team must understand the effect of the changes and incorporate them in procedures before the changes are put into production</span></span>

  - <span data-ttu-id="0857f-117">**Equipo de red**   Este equipo es responsable de los cambios en las reglas del firewall que permiten el acceso desde Internet a los servidores internos del grupo de servidores de Lync.</span><span class="sxs-lookup"><span data-stu-id="0857f-117">**Network Team**   This team is responsible for changes to firewall rules that allow access from the Internet to the internal Lync pool servers.</span></span> <span data-ttu-id="0857f-118">El equipo también es responsable de trabajar con los administradores de Lync para asegurarse de que el ancho de banda disponible puede admitir la carga adicional.</span><span class="sxs-lookup"><span data-stu-id="0857f-118">The team is also responsible in working with the Lync administrators for making sure that the available bandwidth can support the additional load.</span></span>

  - <span data-ttu-id="0857f-119">**Equipo de seguridad**   Este equipo evalúa la seguridad y minimiza los riesgos.</span><span class="sxs-lookup"><span data-stu-id="0857f-119">**Security Team**   This team assesses security and minimizes risks.</span></span> <span data-ttu-id="0857f-120">El equipo de seguridad debe revisar las vulnerabilidades conocidas y ayudar a garantizar que se minimicen los riesgos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0857f-120">The security team must review known vulnerabilities and help ensure that security risks are minimized.</span></span>

  - <span data-ttu-id="0857f-121">**Equipo de aceptación de usuario**   Este equipo está compuesto de usuarios que están dispuestos a probar el sistema y ofrecer comentarios para mejoras.</span><span class="sxs-lookup"><span data-stu-id="0857f-121">**User Acceptance Team**   This team is composed of users who are willing to test the system and offer feedback for improvements.</span></span>

<span data-ttu-id="0857f-122">El proceso de administración de cambios define las responsabilidades de cada equipo y programa el trabajo que se va a realizar, con la incorporación de comprobaciones y pruebas cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="0857f-122">The change management process defines the responsibilities of each team and schedules the work to be performed, incorporating checks and tests where they are required.</span></span> <span data-ttu-id="0857f-123">Los controles de cambio variarán en función de la complejidad y del efecto esperado de un cambio.</span><span class="sxs-lookup"><span data-stu-id="0857f-123">Change controls will vary depending on the complexity and expected effect of a change.</span></span> <span data-ttu-id="0857f-124">Pueden variar desde la aprobación automática de cambios menores, para cambiar las reuniones de revisión, a revisiones de nivel de proyecto completas.</span><span class="sxs-lookup"><span data-stu-id="0857f-124">They can vary from automatic approval of minor changes, to change review meetings, to full project-level reviews.</span></span> <span data-ttu-id="0857f-125">Para explicar esto mejor, los grupos de cambios se tratan en esta sección.</span><span class="sxs-lookup"><span data-stu-id="0857f-125">To explain this better, the groups of changes are discussed in this section.</span></span>

  - <span data-ttu-id="0857f-126">**Cambios principales**   Los cambios importantes tienen un efecto global en el sistema y pueden requerir la intervención de varios equipos.</span><span class="sxs-lookup"><span data-stu-id="0857f-126">**Major Changes**   Major changes have a global effect on the system and may require input from various teams.</span></span> <span data-ttu-id="0857f-127">Un ejemplo de esto es la actualización a Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0857f-127">An example of this is upgrading to Lync Server 2013.</span></span> <span data-ttu-id="0857f-128">Los cambios importantes afectan a muchos equipos y quizás a diferentes sistemas.</span><span class="sxs-lookup"><span data-stu-id="0857f-128">Major changes affect many teams and perhaps different systems.</span></span> <span data-ttu-id="0857f-129">El proceso de administración de cambios probablemente incluirá una o varias reuniones de revisión de cambios para informar a los equipos que participarán en el cambio o que se verán afectados por el cambio.</span><span class="sxs-lookup"><span data-stu-id="0857f-129">The change management process will probably include one or more change review meetings to inform the teams that will be involved in the change or be affected by the change.</span></span>

  - <span data-ttu-id="0857f-130">**Cambios importantes**   Los cambios significativos requieren recursos importantes para planear, crear e implementar.</span><span class="sxs-lookup"><span data-stu-id="0857f-130">**Significant Changes**   Significant changes require significant resources to plan, build, and implement.</span></span> <span data-ttu-id="0857f-131">Deben introducirse controles de cambio apropiados para ayudar a garantizar que el efecto del cambio se entienda, los procedimientos de implementación se prueban y los planes de reversión y de contingencia están listos.</span><span class="sxs-lookup"><span data-stu-id="0857f-131">Appropriate change controls should be introduced to help make ensure that the effect of the change is understood, deployment procedures are tested, and the rollback and contingency plans are ready.</span></span> <span data-ttu-id="0857f-132">Un ejemplo de un cambio significativo es implementar una nueva actualización acumulativa.</span><span class="sxs-lookup"><span data-stu-id="0857f-132">An example of a significant change is deploying a new cumulative update.</span></span>

  - <span data-ttu-id="0857f-133">**Cambios menores**   Los cambios menores no afectan significativamente al entorno de ti, por ejemplo, el cambio de determinadas directivas de Lync a través del panel de control de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0857f-133">**Minor Changes**   Minor changes do not significantly affect the IT environment, for example, changing certain Lync policies via the Microsoft Lync Server 2013 Control Panel.</span></span>

  - <span data-ttu-id="0857f-134">**Cambios estándar**   Los cambios estándar se realizan de forma periódica y se han entendido y documentado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0857f-134">**Standard Changes**   Standard changes are performed regularly and are well understood and documented.</span></span> <span data-ttu-id="0857f-135">El proceso de administración de cambios debe revisar todos los cambios realizados en los procedimientos.</span><span class="sxs-lookup"><span data-stu-id="0857f-135">The change management process should review all changes to the procedures.</span></span> <span data-ttu-id="0857f-136">No debería ser necesario para cambios rutinarios como la creación de una base de datos de contenido o la adición de un usuario.</span><span class="sxs-lookup"><span data-stu-id="0857f-136">It should not be needed for routine changes like creating a content database or adding a user.</span></span>

<span data-ttu-id="0857f-137">El siguiente ejemplo de administración de cambios examina cómo interactúan diferentes equipos y las acciones que se realizan cuando se implementa un nuevo Service Pack.</span><span class="sxs-lookup"><span data-stu-id="0857f-137">The following example of change management examines how different teams interact and the actions that are performed when a new service pack is deployed.</span></span> <span data-ttu-id="0857f-138">Estas acciones están organizadas y administradas por el proceso de administración de cambios.</span><span class="sxs-lookup"><span data-stu-id="0857f-138">These actions are organized and managed by the change management process.</span></span>

  - <span data-ttu-id="0857f-139">**Generar una solicitud de cambio**   El equipo de seguridad ha evaluado el último Service Pack y confirmado que resuelve una posible vulnerabilidad en el sistema de producción.</span><span class="sxs-lookup"><span data-stu-id="0857f-139">**Raise a change request**   The security team has assessed the latest service pack and confirmed that it resolves a possible vulnerability in the production system.</span></span> <span data-ttu-id="0857f-140">El equipo genera una solicitud de cambio para que la nueva actualización acumulativa se aplique a todos los servidores que ejecutan Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0857f-140">The team raises a change request to have the new cumulative update applied to all servers that are running Lync Server.</span></span>

  - <span data-ttu-id="0857f-141">**Revisión de notas de la versión de Service Pack**   El equipo de administrador de Lync revisa las notas de la versión de Service Pack para identificar el efecto en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0857f-141">**Service pack release notes review**   The Lync administrator team reviews the service pack release notes to identify the effect on the system.</span></span>

  - <span data-ttu-id="0857f-142">**Se realiza una serie de pruebas de laboratorio**   El equipo de administrador de Lync debe realizar actualizaciones de prueba en un servidor en un entorno de prueba para decidir si el Service Pack se puede aplicar correctamente sin afectar a ninguna de las aplicaciones y los sistemas de servidor instalados.</span><span class="sxs-lookup"><span data-stu-id="0857f-142">**A series of lab tests is performed**   The Lync administrator team must perform test updates on a server in a test environment to decide whether the service pack can be applied successfully without affecting any of the installed applications and server systems.</span></span> <span data-ttu-id="0857f-143">Si hay aplicaciones de terceros o creadas internamente con la interfaz de Lync Server en un entorno de producción, también se deben probar.</span><span class="sxs-lookup"><span data-stu-id="0857f-143">If there are third-party or internally created applications that interface with Lync Server in a production environment, these should be also tested.</span></span> <span data-ttu-id="0857f-144">Estas pruebas también se pueden usar para estimar el tiempo necesario para realizar las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="0857f-144">These tests can also be used to estimate the time that is required to perform the upgrades.</span></span>

  - <span data-ttu-id="0857f-145">**A los usuarios se les informa de la interrupción**   El equipo de administrador de Lync, el equipo de comunicaciones o el servicio de asistencia al usuario informa a todos los usuarios afectados sobre el ciclo de mantenimiento planeado y el tiempo durante el cual el servicio no estará disponible.</span><span class="sxs-lookup"><span data-stu-id="0857f-145">**Users are informed of the outage**   The Lync administrator team, communications team, or user help desk informs all affected users about the planned maintenance cycle and how long the service will be unavailable.</span></span>

  - <span data-ttu-id="0857f-146">**Se realiza una copia de seguridad completa de Lync antes de la actualización**   .   El equipo de administrador de Lync debe comprobar que hay una copia de seguridad válida que se puede usar para volver al estado del sistema original si se produce un error en la instalación del Service Pack.</span><span class="sxs-lookup"><span data-stu-id="0857f-146">**A full backup of Lync is performed before the upgrade**   The Lync administrator team must verify that there is a valid backup that can be used to revert to the original system state if the service pack installation fails.</span></span> <span data-ttu-id="0857f-147">Le recomendamos que se restaure la copia de seguridad en un servidor de reserva para que este sistema esté disponible si hay problemas.</span><span class="sxs-lookup"><span data-stu-id="0857f-147">We recommend that the backup be restored to a standby server to have this system readily available if there are issues.</span></span>

  - <span data-ttu-id="0857f-148">**Se implementa la actualización acumulativa**   El equipo de administrador de Lync realiza la instalación durante el ciclo de mantenimiento planeado.</span><span class="sxs-lookup"><span data-stu-id="0857f-148">**The cumulative update is deployed**   The Lync administrator team does the installation during the planned maintenance cycle.</span></span>

<div>

## <a name="managing-the-timing-of-changes"></a><span data-ttu-id="0857f-149">Administrar los intervalos de cambios</span><span class="sxs-lookup"><span data-stu-id="0857f-149">Managing the timing of changes</span></span>

<span data-ttu-id="0857f-150">Le recomendamos que implemente un procedimiento de programación de cambios para evitar interrupciones en secciones superpuestas de su trabajo.</span><span class="sxs-lookup"><span data-stu-id="0857f-150">We recommend that you implement a procedure for scheduling changes to avoid disruptions in overlapping sections of your work.</span></span> <span data-ttu-id="0857f-151">Por ejemplo, dos equipos pueden estar planeando un cambio menor en un sistema.</span><span class="sxs-lookup"><span data-stu-id="0857f-151">For example, two teams may both be planning a minor change to a system.</span></span> <span data-ttu-id="0857f-152">Un equipo puede estar aplicando una actualización acumulativa en un grupo mientras otro equipo está migrando usuarios heredados a ese grupo.</span><span class="sxs-lookup"><span data-stu-id="0857f-152">One team may be applying a cumulative update on a pool while another team is migrating legacy users into that pool.</span></span> <span data-ttu-id="0857f-153">Ningún equipo se ve afectado por los cambios que el otro equipo está planeando, y es posible que cada equipo no sepa necesariamente los cambios que el otro equipo está planeando.</span><span class="sxs-lookup"><span data-stu-id="0857f-153">Neither team is affected by the changes that the other team is planning, and each team may not necessarily know about changes that the other team is planning.</span></span> <span data-ttu-id="0857f-154">Si los dos cambios se produjeron al mismo tiempo, es posible que haya problemas para implementar los cambios.</span><span class="sxs-lookup"><span data-stu-id="0857f-154">If both changes occurred at the same time, there might be issues implementing the changes.</span></span> <span data-ttu-id="0857f-155">Además, si hay problemas después de la aplicación de los cambios, por ejemplo, si se produce un error en la migración de usuario, puede ser difícil decidir qué cambio se debe revertir.</span><span class="sxs-lookup"><span data-stu-id="0857f-155">Also, if there are issues after the changes were applied, for example, if the user migration fails, it may be difficult to decide which change should be rolled back.</span></span> <span data-ttu-id="0857f-156">Deben configurarse períodos de mantenimiento regulares entre ti y la administración para probar los cambios y aceptarlos.</span><span class="sxs-lookup"><span data-stu-id="0857f-156">There should be regular maintenance periods set up between IT and management to test the changes and accept them.</span></span>

<span data-ttu-id="0857f-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0857f-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

