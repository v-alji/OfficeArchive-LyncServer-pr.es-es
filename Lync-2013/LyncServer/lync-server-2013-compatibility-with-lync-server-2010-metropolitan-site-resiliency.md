---
title: Compatibilidad de Lync Server 2013 con la resistencia de sitios de metropolitana de Lync Server 2010
description: Lync Server 2013 compatibilidad con la resistencia de sitios metropolitana de Lync Server 2010.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2010 metropolitan site resiliency
ms:assetid: 18673ff6-b664-4a57-a89b-cbda8b129e6a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204715(v=OCS.15)
ms:contentKeyID: 48183526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec72f261ac593b24bad13dcd400f495ba7ba0722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434609"
---
# <a name="lync-server-2010-metropolitan-site-resiliency"></a><span data-ttu-id="58b54-103">Resistencia de sitios de metropolitana de Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="58b54-103">Lync Server 2010 metropolitan site resiliency</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58b54-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58b54-104">

<span> </span></span></span>

<span data-ttu-id="58b54-105">_**Última modificación del tema:** 2014-03-19_</span><span class="sxs-lookup"><span data-stu-id="58b54-105">_**Topic Last Modified:** 2014-03-19_</span></span>

<span data-ttu-id="58b54-106">La solución metropolitana de resiliencia de sitios admitida para Lync Server 2010 no es compatible con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="58b54-106">The metropolitan site resiliency solution supported for Lync Server 2010 is not supported for Lync Server 2013.</span></span> <span data-ttu-id="58b54-107">Esta solución implicaba la expansión de un único Pool front end en dos centros de datos en el mismo área metropolitana.</span><span class="sxs-lookup"><span data-stu-id="58b54-107">This solution involved spanning a single Front End pool across two data centers in the same metropolitan area.</span></span>

<span data-ttu-id="58b54-108">La solución de resistencia de sitios metropolitana se ha diseñado para recuperarse de la pérdida de un centro de recursos completo.</span><span class="sxs-lookup"><span data-stu-id="58b54-108">The metropolitan site resiliency solution was designed to recover from the loss of a full datacenter.</span></span> <span data-ttu-id="58b54-109">Cuando el grupo se extiende por dos centros de recursos, normalmente se coloca la mitad de los extremos en un centro de recursos y la otra mitad en el segundo centro de recursos.</span><span class="sxs-lookup"><span data-stu-id="58b54-109">When you span your pool across two datacenters, you typically put half of your front ends in one datacenter and the other half in the second datacenter.</span></span> <span data-ttu-id="58b54-110">Si pierde un centro de información completo, habrá perdido la mitad de los servidores de aplicaciones para el usuario.</span><span class="sxs-lookup"><span data-stu-id="58b54-110">If you lose an entire datacenter, you have lost half of your Front End Servers.</span></span> <span data-ttu-id="58b54-111">Esto puede ocasionar problemas con el nuevo modelo de sistema distribuido para los grupos de servidores front-end en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="58b54-111">This can cause issues with the new distributed system model for Front End Pools in Lync Server 2013.</span></span> <span data-ttu-id="58b54-112">Para obtener más información, vea [topologías y componentes para servidores front-end, mensajería instantánea y presencia en Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span><span class="sxs-lookup"><span data-stu-id="58b54-112">For more information, see [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span></span>

<span data-ttu-id="58b54-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58b54-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

