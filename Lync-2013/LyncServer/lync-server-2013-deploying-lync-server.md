---
title: 'Lync Server 2013: Implementar Lync Server'
description: 'Lync Server 2013: implementación de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync Server 2013
ms:assetid: b76795a4-4e71-4c70-a5c0-d1197fa8028c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412892(v=OCS.15)
ms:contentKeyID: 48185197
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 569b1e8b07954f04ee7e4f73de51494ece27157e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429933"
---
# <a name="deploying-lync-server-2013"></a><span data-ttu-id="0ee14-103">Implementar Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ee14-103">Deploying Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ee14-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ee14-104">

<span> </span></span></span>

<span data-ttu-id="0ee14-105">_**Última modificación del tema:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="0ee14-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="0ee14-106">El proceso de implementación de Lync Server 2013 viene determinado por la topología y los componentes de Lync Server que decida instalar, incluso si desea implementar un grupo de servidores front-end o un servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="0ee14-106">Your deployment process for Lync Server 2013 is determined by the Lync Server topology and components you decide to install, including whether you want to deploy a Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="0ee14-107">Los temas de esta sección le ayudan a determinar qué entorno desea implementar y le guiará a través del proceso de implementación.</span><span class="sxs-lookup"><span data-stu-id="0ee14-107">The topics in this section help you determine what environment you want to deploy and guide you through the deployment process.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0ee14-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="0ee14-108">In This Section</span></span>

  - [<span data-ttu-id="0ee14-109">Introducción general a la implementación para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ee14-109">Deployment overview for Lync Server 2013</span></span>](lync-server-2013-deployment-overview.md)

  - [<span data-ttu-id="0ee14-110">Requisitos del sistema para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ee14-110">System requirements for Lync Server 2013</span></span>](lync-server-2013-system-requirements.md)

  - [<span data-ttu-id="0ee14-111">Preparación de la infraestructura y los sistemas para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ee14-111">Preparing the infrastructure and systems for Lync Server 2013</span></span>](lync-server-2013-preparing-the-infrastructure-and-systems.md)

  - [<span data-ttu-id="0ee14-112">Definición y configuración de la topología en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ee14-112">Defining and configuring the topology in Lync Server 2013</span></span>](lync-server-2013-defining-and-configuring-the-topology.md)

  - [<span data-ttu-id="0ee14-113">Finalización e implementación del diseño de la topología en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ee14-113">Finalizing and implementing the topology design in Lync Server 2013</span></span>](lync-server-2013-finalizing-and-implementing-the-topology-design.md)

  - [<span data-ttu-id="0ee14-114">Configurar servidores front-end y grupos de servidores front-end para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ee14-114">Setting up Front End Servers and Front End pools for Lync Server 2013</span></span>](lync-server-2013-setting-up-front-end-servers-and-front-end-pools.md)

  - [<span data-ttu-id="0ee14-115">Implementación de Lync Server 2013 Standard Edition en un Lync Server 2013 Enterprise existente</span><span class="sxs-lookup"><span data-stu-id="0ee14-115">Deploying Lync Server 2013 Standard Edition into an existing Lync Server 2013 Enterprise</span></span>](lync-server-2013-deploying-lync-server-2013-standard-edition-into-an-existing-lync-server-2013-enterprise.md)

  - [<span data-ttu-id="0ee14-116">Agregar roles de servidor en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ee14-116">Adding server roles in Lync Server 2013</span></span>](lync-server-2013-adding-server-roles.md)

  - [<span data-ttu-id="0ee14-117">Configurar la autenticación Kerberos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ee14-117">Setting up Kerberos authentication in Lync Server 2013</span></span>](lync-server-2013-setting-up-kerberos-authentication.md)

<span data-ttu-id="0ee14-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ee14-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

