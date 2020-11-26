---
title: 'Lync Server 2013: Implementar la movilidad'
description: 'Lync Server 2013: implementación de movilidad.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying mobility
ms:assetid: f41e6b25-d2cd-43fd-a17b-22cfda8bcd4f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690055(v=OCS.15)
ms:contentKeyID: 48185805
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cf927b950f8b94884fb91224a87e196fc815fca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429877"
---
# <a name="deploying-mobility-in-lync-server-2013"></a><span data-ttu-id="a6a07-103">Implementar la movilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6a07-103">Deploying mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6a07-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6a07-104">

<span> </span></span></span>

<span data-ttu-id="a6a07-105">_**Última modificación del tema:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="a6a07-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="a6a07-106">Al implementar la característica de movilidad de Lync Server 2013, los usuarios móviles pueden usar dispositivos móviles compatibles para las características de Lync, como la mensajería instantánea (mi), la presencia y los contactos.</span><span class="sxs-lookup"><span data-stu-id="a6a07-106">When you deploy the Lync Server 2013 mobility feature, mobile users can use supported mobile devices for Lync functionality such as instant messaging (IM), presence, and contacts.</span></span>

<span data-ttu-id="a6a07-107">Para obtener más información sobre los requisitos para implementar la característica de movilidad, consulte [planificación de movilidad en Lync Server 2013](lync-server-2013-planning-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="a6a07-107">For details about requirements for deploying the mobility feature, see [Planning for mobility in Lync Server 2013](lync-server-2013-planning-for-mobility.md).</span></span>

<span data-ttu-id="a6a07-108">Esta sección le guiará a través de los pasos para implementar y comprobar las características de movilidad y detección automática.</span><span class="sxs-lookup"><span data-stu-id="a6a07-108">This section guides you through the steps for deploying and verifying the mobility and automatic discovery features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a6a07-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a6a07-109">In This Section</span></span>

  - [<span data-ttu-id="a6a07-110">Creación de registros DNS para el servicio Detección automática en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6a07-110">Creating DNS records for the Autodiscover Service in Lync Server 2013</span></span>](lync-server-2013-creating-dns-records-for-the-autodiscover-service.md)

  - [<span data-ttu-id="a6a07-111">Modificación de certificados para movilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6a07-111">Modifying certificates for mobility in Lync Server 2013</span></span>](lync-server-2013-modifying-certificates-for-mobility.md)

  - [<span data-ttu-id="a6a07-112">Configuración del proxy inverso para movilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6a07-112">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)

  - [<span data-ttu-id="a6a07-113">Configurar la detección automática para movilidad con implementaciones híbridas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6a07-113">Configuring Autodiscover in Lync Server 2013 for mobility with hybrid deployments</span></span>](lync-server-2013-configuring-autodiscover-for-mobility-with-hybrid-deployments.md)

  - [<span data-ttu-id="a6a07-114">Comprobar la implementación de la movilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6a07-114">Verifying your mobility deployment in Lync Server 2013</span></span>](lync-server-2013-verifying-your-mobility-deployment.md)

  - [<span data-ttu-id="a6a07-115">Configurar las notificaciones de inserción en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6a07-115">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)

  - [<span data-ttu-id="a6a07-116">Configuración de la directiva de movilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6a07-116">Configuring mobility policy in Lync Server 2013</span></span>](lync-server-2013-configuring-mobility-policy.md)

<span data-ttu-id="a6a07-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6a07-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

