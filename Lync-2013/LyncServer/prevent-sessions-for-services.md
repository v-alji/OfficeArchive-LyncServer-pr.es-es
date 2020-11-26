---
title: Impedir sesiones para servicios
description: Evitar las sesiones de servicios.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 4b541c72-cdc1-4f86-a5a8-c43c24f41d8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688049(v=OCS.15)
ms:contentKeyID: 49733642
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a452f8091716daa0a15967e2a278e82c5bc8c4f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438466"
---
# <a name="prevent-sessions-for-services"></a><span data-ttu-id="314e8-103">Impedir sesiones para servicios</span><span class="sxs-lookup"><span data-stu-id="314e8-103">Prevent sessions for services</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="314e8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="314e8-104">

<span> </span></span></span>

<span data-ttu-id="314e8-105">_**Última modificación del tema:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="314e8-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="314e8-106">Puede usar el panel de control de Microsoft Lync Server 2010 para evitar nuevas sesiones para todos los servicios de Lync Server 2010 que se ejecutan en un equipo específico o para evitar nuevas sesiones para un servicio específico de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="314e8-106">You can use Microsoft Lync Server 2010 Control Panel to prevent new sessions for all the Lync Server 2010 services running on a specific computer or to prevent new sessions for a specific Lync Server 2010 service.</span></span>

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a><span data-ttu-id="314e8-107">Para evitar nuevas sesiones para todos los servicios de Lync Server en un equipo</span><span class="sxs-lookup"><span data-stu-id="314e8-107">To prevent new sessions for all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="314e8-108">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o asignada al rol CsServerAdministrator o CsAdministrator, inicie sesión en cualquier equipo de la red en el que haya implementado Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="314e8-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="314e8-109">Abra el Panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="314e8-109">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="314e8-110">En la barra de navegación izquierda, haga clic en **topología** y, a continuación, en **Estado**.</span><span class="sxs-lookup"><span data-stu-id="314e8-110">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="314e8-111">En la página **Estado** , ordene o busque en la lista según sea necesario para buscar el equipo que ejecuta los servicios para los que desea evitar nuevas sesiones y, a continuación, haga clic en ella.</span><span class="sxs-lookup"><span data-stu-id="314e8-111">On the **Status** page, sort or search through the list as needed to find the computer that is running the services for which you want to prevent new sessions, and then click it.</span></span>

5.  <span data-ttu-id="314e8-112">Haga clic en **acción**.</span><span class="sxs-lookup"><span data-stu-id="314e8-112">Click **Action**.</span></span>

6.  <span data-ttu-id="314e8-113">Haga clic en **evitar nuevas sesiones para todos los servicios**.</span><span class="sxs-lookup"><span data-stu-id="314e8-113">Click **Prevent new sessions for all services**.</span></span>

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a><span data-ttu-id="314e8-114">Para evitar nuevas sesiones para un servicio específico</span><span class="sxs-lookup"><span data-stu-id="314e8-114">To prevent new sessions for a specific service</span></span>

1.  <span data-ttu-id="314e8-115">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o asignada al rol CsServerAdministrator o CsAdministrator, inicie sesión en cualquier equipo de la red en el que haya implementado Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="314e8-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="314e8-116">Abra el Panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="314e8-116">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="314e8-117">En la barra de navegación izquierda, haga clic en **topología** y, a continuación, en **Estado**.</span><span class="sxs-lookup"><span data-stu-id="314e8-117">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="314e8-118">En la página **Estado** , ordene o busque en la lista según sea necesario para buscar el equipo que está ejecutando el servicio que desea iniciar o detener y, a continuación, haga clic en él.</span><span class="sxs-lookup"><span data-stu-id="314e8-118">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="314e8-119">Haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="314e8-119">Click **Properties**.</span></span>

6.  <span data-ttu-id="314e8-120">Si es necesario, ordene la lista de servicios y haga clic en el servicio para el que desea evitar nuevas sesiones.</span><span class="sxs-lookup"><span data-stu-id="314e8-120">Sort the list of services, if necessary, and click the service for which you want to prevent new sessions.</span></span>

7.  <span data-ttu-id="314e8-121">Haga clic en **acción**.</span><span class="sxs-lookup"><span data-stu-id="314e8-121">Click **Action**.</span></span>

8.  <span data-ttu-id="314e8-122">Haga clic en **evitar nuevas sesiones para el servicio**.</span><span class="sxs-lookup"><span data-stu-id="314e8-122">Click **Prevent new sessions for service**.</span></span>

9.  <span data-ttu-id="314e8-123">Haga clic en **Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="314e8-123">Click **Close**.</span></span>

<span data-ttu-id="314e8-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="314e8-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

