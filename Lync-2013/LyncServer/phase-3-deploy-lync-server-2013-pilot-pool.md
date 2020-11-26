---
title: 'Fase 3: implementar el grupo de pruebas piloto de Lync Server 2013'
description: 'Fase 3: implementar el grupo de pruebas piloto de Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Phase 3: Deploy Lync Server 2013 pilot pool'
ms:assetid: f12b1517-fb56-4ded-8323-57aa9fc9ea48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205367(v=OCS.15)
ms:contentKeyID: 48185778
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f72f0cdd2e7d3b9e29891a4adc0ab0551539f465
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438459"
---
# <a name="phase-3-deploy-lync-server-2013-pilot-pool"></a><span data-ttu-id="ae229-103">Fase 3: implementar el grupo de pruebas piloto de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae229-103">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae229-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae229-104">

<span> </span></span></span>

<span data-ttu-id="ae229-105">_**Última modificación del tema:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="ae229-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="ae229-106">En esta sección se describen los pasos necesarios para implementar un grupo piloto de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ae229-106">This section covers the steps required to deploy a pilot pool of Lync Server 2013.</span></span> <span data-ttu-id="ae229-107">La implementación de Lync Server 2013 requiere el uso de generador de topología para definir la topología y los componentes que desea implementar, preparar su entorno para la implementación de los componentes de Lync Server 2013, publicar el diseño de topología en el primer servidor front-end y, a continuación, instalar y configurar el software de Lync Server 2013 para los componentes de su implementación.</span><span class="sxs-lookup"><span data-stu-id="ae229-107">The deployment of Lync Server 2013 requires using Topology Builder to define your topology and the components you want to deploy, preparing your environment for deployment of the Lync Server 2013 components, publishing your topology design on the first Front End Server, and then installing and configuring Lync Server 2013 software for the components for your deployment.</span></span> <span data-ttu-id="ae229-108">Cuando se complete, la implementación del grupo piloto de Lync Server 2013 coexistirá con un grupo de servidores de Lync Server 2010 existente.</span><span class="sxs-lookup"><span data-stu-id="ae229-108">When completed, your Lync Server 2013 pilot pool deployment will coexist with an existing Lync Server 2010 pool.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ae229-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ae229-109">In This Section</span></span>

  - [<span data-ttu-id="ae229-110">Preparar Active Directory para Lync Server</span><span class="sxs-lookup"><span data-stu-id="ae229-110">Prepare Active Directory for Lync Server</span></span>](prepare-active-directory-for-lync-server.md)

  - [<span data-ttu-id="ae229-111">Descargar una topología desde una implementación existente</span><span class="sxs-lookup"><span data-stu-id="ae229-111">Download topology from existing deployment</span></span>](download-topology-from-existing-deployment.md)

  - [<span data-ttu-id="ae229-112">Implementar el grupo de pruebas piloto de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae229-112">Deploy Lync Server 2013 pilot pool</span></span>](deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="ae229-113">Comprobar la coexistencia del grupo de servidores piloto con el grupo de servidores heredado</span><span class="sxs-lookup"><span data-stu-id="ae229-113">Verify pilot pool coexistence with legacy pool</span></span>](verify-pilot-pool-coexistence-with-legacy-pool.md)

  - [<span data-ttu-id="ae229-114">Conecte el grupo de servidores piloto a los servidores perimetrales heredados</span><span class="sxs-lookup"><span data-stu-id="ae229-114">Connect pilot pool to legacy Edge Servers</span></span>](connect-pilot-pool-to-legacy-edge-servers.md)

  - [<span data-ttu-id="ae229-115">Configurar certificados y directivas de acceso por puerta de enlace XMPP</span><span class="sxs-lookup"><span data-stu-id="ae229-115">Configure XMPP gateway access policies and certificates</span></span>](configure-xmpp-gateway-access-policies-and-certificates.md)

<span data-ttu-id="ae229-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae229-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

