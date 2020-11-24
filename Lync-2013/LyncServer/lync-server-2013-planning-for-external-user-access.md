---
title: 'Lync Server 2013: Planear acceso de usuarios externos'
description: 'Lync Server 2013: planear el acceso de usuarios externos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for external user access
ms:assetid: ea098933-eff5-461e-aba3-e7f128784dc2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399048(v=OCS.15)
ms:contentKeyID: 48185903
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8f1854791ed837b963d4c80f3467e4e89555592
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397890"
---
# <a name="planning-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="5185b-103">Planear acceso de usuarios externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5185b-103">Planning for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5185b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5185b-104">

<span> </span></span></span>

<span data-ttu-id="5185b-105">_**Última modificación del tema:** 2013-01-19_</span><span class="sxs-lookup"><span data-stu-id="5185b-105">_**Topic Last Modified:** 2013-01-19_</span></span>

<span data-ttu-id="5185b-106">Las comunicaciones en la mayoría de las organizaciones implican a servicios y usuarios que no se encuentran dentro de la red interna.</span><span class="sxs-lookup"><span data-stu-id="5185b-106">Communications in most organizations involve services and users that are not inside your internal network.</span></span> <span data-ttu-id="5185b-107">Estos servicios y usuarios incluyen empleados que están fuera del sitio temporal o permanentemente, empleados de organizaciones de clientes o socios, personas que usan servicios de mensajería instantánea pública (mi) y clientes potenciales, socios y usuarios anónimos a los que invite a reuniones y presentaciones.</span><span class="sxs-lookup"><span data-stu-id="5185b-107">These services and users include employees who are temporarily or permanently offsite, employees of customer or partner organizations, people who use public instant messaging (IM) services, and potential customers, partners and anonymous users whom you invite to meetings and presentations.</span></span> <span data-ttu-id="5185b-108">En esta documentación, estas personas se conocen colectivamente como *usuarios externos*.</span><span class="sxs-lookup"><span data-stu-id="5185b-108">In this documentation, these people are collectively referred to as *external users*.</span></span>

<span data-ttu-id="5185b-109">Con Microsoft Lync Server 2013, los usuarios de su organización pueden usar la mensajería instantánea y la presencia para comunicarse con los usuarios externos y pueden participar en conferencias de audio y vídeo (A/V) y en conferencias web con sus empleados fuera del sitio y otros tipos de usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="5185b-109">With Microsoft Lync Server 2013, users in your organization can use IM and presence to communicate with external users, and they can participate in audio/video (A/V) conferencing and web conferencing with your offsite employees and other types of external users.</span></span> <span data-ttu-id="5185b-110">También puedes admitir el acceso externo desde dispositivos móviles y con la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="5185b-110">You can also support external access from mobile devices and over Enterprise Voice.</span></span> <span data-ttu-id="5185b-111">Los usuarios externos que no son miembros de su organización pueden participar en reuniones de Lync Server 2013, lo que permite a los asistentes anónimos.</span><span class="sxs-lookup"><span data-stu-id="5185b-111">External users who are not members of your organization can participate in Lync Server 2013 meetings, allowing anonymous attendees.</span></span>

<span data-ttu-id="5185b-112">Para admitir las comunicaciones en el Firewall de la organización, debe implementar el servidor perimetral 2013 de Lync Server en la red perimetral (también conocida como DMZ, zona desmilitarizada y subred filtrada).</span><span class="sxs-lookup"><span data-stu-id="5185b-112">To support communications across your organization’s firewall, you deploy Lync Server 2013 Edge Server in your perimeter network (also known as DMZ, demilitarized zone, and screened subnet).</span></span> <span data-ttu-id="5185b-113">El servidor perimetral controla cómo los usuarios externos al firewall se pueden conectar a la implementación interna de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5185b-113">The Edge Server controls how users outside the firewall can connect to your internal Lync Server 2013 deployment.</span></span> <span data-ttu-id="5185b-114">También controla las comunicaciones con usuarios externos que se originan dentro del firewall.</span><span class="sxs-lookup"><span data-stu-id="5185b-114">It also controls communications with external users that originate within the firewall.</span></span>

<span data-ttu-id="5185b-115">En función de sus necesidades, puede implementar uno o varios servidores perimetrales en una o más ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="5185b-115">Depending on your requirements, you can deploy one or more Edge Servers in one or more locations.</span></span> <span data-ttu-id="5185b-116">En esta sección se describen escenarios para el acceso de usuarios externos en Lync Server 2013, y se explica cómo planear la topología perimetral y de proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="5185b-116">This section describes scenarios for external user access in Lync Server 2013, and it explains how to plan your edge and reverse proxy topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5185b-117">Aunque necesita un servidor perimetral para admitir la telefonía IP empresarial y el acceso de usuarios externos, esta sección se centra en la compatibilidad con la mensajería instantánea, la presencia, las conferencias A/V, la Federación, la conferencia web y Lync Mobile.</span><span class="sxs-lookup"><span data-stu-id="5185b-117">Although you need an Edge Server to support Enterprise Voice and external user access, this section focuses on support for IM, presence, A/V conferencing, federation, web conferencing, and Lync Mobile.</span></span> <span data-ttu-id="5185b-118">Para obtener más información sobre la compatibilidad de telefonía IP empresarial, consulte <A href="lync-server-2013-planning-for-enterprise-voice.md">planificación de telefonía empresarial en Lync Server 2013</A> en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="5185b-118">For details about support for Enterprise Voice, see <A href="lync-server-2013-planning-for-enterprise-voice.md">Planning for Enterprise Voice in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5185b-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5185b-119">In This Section</span></span>

  - [<span data-ttu-id="5185b-120">Cambios en Lync Server 2013 que afectan a la planificación del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="5185b-120">Changes in Lync Server 2013 that affect Edge Server planning</span></span>](lync-server-2013-changes-in-lync-server-that-affect-edge-server-planning.md)

  - [<span data-ttu-id="5185b-121">Requisitos del sistema para componentes perimetrales para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5185b-121">System requirements for external user access components for Lync Server 2013</span></span>](lync-server-2013-system-requirements-for-external-user-access-components.md)

  - [<span data-ttu-id="5185b-122">Información general sobre el acceso de usuarios externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5185b-122">Overview of external user access in Lync Server 2013</span></span>](lync-server-2013-overview-of-external-user-access.md)

  - [<span data-ttu-id="5185b-123">Descripción de la detección automática en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5185b-123">Understanding Autodiscover in Lync Server 2013</span></span>](lync-server-2013-understanding-autodiscover.md)

  - [<span data-ttu-id="5185b-124">Elección de una topología en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5185b-124">Choosing a topology in Lync Server 2013</span></span>](lync-server-2013-choosing-a-topology.md)

  - [<span data-ttu-id="5185b-125">Recopilación de datos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5185b-125">Data collection in Lync Server 2013</span></span>](lync-server-2013-data-collection.md)

  - [<span data-ttu-id="5185b-126">Determinar los requisitos DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5185b-126">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)

  - [<span data-ttu-id="5185b-127">Determinar los requisitos de los puertos y el firewall de A/V externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5185b-127">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)

  - [<span data-ttu-id="5185b-128">Plan para certificados de servidores perimetrales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5185b-128">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)

  - [<span data-ttu-id="5185b-129">Escenarios para el acceso de usuarios externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5185b-129">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)

<span data-ttu-id="5185b-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5185b-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

