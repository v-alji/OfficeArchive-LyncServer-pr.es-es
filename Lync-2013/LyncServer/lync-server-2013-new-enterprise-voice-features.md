---
title: 'Lync Server 2013: Nuevas características de la telefonía IP empresarial'
description: 'Lync Server 2013: nuevas características de telefonía IP empresarial.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Enterprise Voice features
ms:assetid: db0ad7b9-e469-4c29-89d9-52fed018ef08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398964(v=OCS.15)
ms:contentKeyID: 48185591
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1fc0c0970fe22fb6a56eaf0d950f1d49d210826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445424"
---
# <a name="new-enterprise-voice-features-in-lync-server-2013"></a><span data-ttu-id="b5958-103">Nuevas características de la telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b5958-103">New Enterprise Voice features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b5958-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b5958-104">

<span> </span></span></span>

<span data-ttu-id="b5958-105">_**Última modificación del tema:** 2013-05-01_</span><span class="sxs-lookup"><span data-stu-id="b5958-105">_**Topic Last Modified:** 2013-05-01_</span></span>

<span data-ttu-id="b5958-106">Lync Server 2013 presenta varias características nuevas de administración de llamadas y enrutamiento que mejoran la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="b5958-106">Lync Server 2013 introduces several new routing and call management features that enhance Enterprise Voice.</span></span>

<span data-ttu-id="b5958-107">Lync Server 2013 admite varios troncos entre servidores de mediación y puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="b5958-107">Lync Server 2013 supports multiple trunks between Mediation Servers and gateways.</span></span> <span data-ttu-id="b5958-108">Un *tronco* es una asociación lógica entre un número de puerto y un servidor de mediación con un número de puerto y una puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="b5958-108">A *trunk* is a logical association between a port number and Mediation Server with a port number and gateway.</span></span> <span data-ttu-id="b5958-109">Esto significa que un servidor de mediación puede tener varios troncos en diferentes puertas de enlace y un Gateway puede tener varios troncos en diferentes servidores de mediación.</span><span class="sxs-lookup"><span data-stu-id="b5958-109">This means that a Mediation Server can have multiple trunks to different gateways, and a gateway can have multiple trunks to different Mediation Servers.</span></span> <span data-ttu-id="b5958-110">El enrutamiento de interconexión permite que Lync Server 2013 pueda interconectar un IP-PBX con una puerta de enlace de red telefónica conmutada (RTC) o para interconectar varios sistemas IP-PBX.</span><span class="sxs-lookup"><span data-stu-id="b5958-110">Intertrunk routing makes it possible for Lync Server 2013 to interconnect an IP-PBX to a public switched telephone network (PSTN) gateway or to interconnect multiple IP-PBX systems.</span></span> <span data-ttu-id="b5958-111">Lync Server 2013 actúa como el pegamento (es decir, la interconexión) entre diferentes sistemas de telefonía.</span><span class="sxs-lookup"><span data-stu-id="b5958-111">Lync Server 2013 serves as the glue (that is, the interconnection) between different telephony systems.</span></span>

<span data-ttu-id="b5958-112">Microsoft Lync Server 2013 realiza mejoras en las áreas de desvío de llamadas, llamadas simultáneas, administración de correo de voz y presentación de identificación de llamadas.</span><span class="sxs-lookup"><span data-stu-id="b5958-112">Microsoft Lync Server 2013 makes improvements in the areas of call forwarding, simultaneous ringing, voice mail handling, and caller ID presentation.</span></span> <span data-ttu-id="b5958-113">Estas características enriquecen la experiencia de llamada de voz empresarial.</span><span class="sxs-lookup"><span data-stu-id="b5958-113">These features enrich the Enterprise Voice call experience.</span></span>

<span data-ttu-id="b5958-114">Lync Server 2013 incorpora las siguientes mejoras nuevas para telefonía IP empresarial:</span><span class="sxs-lookup"><span data-stu-id="b5958-114">Lync Server 2013 introduces the following new enhancements to Enterprise Voice:</span></span>

  - [<span data-ttu-id="b5958-115">Nuevas características de llamada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b5958-115">New call features in Lync Server 2013</span></span>](lync-server-2013-new-call-features.md)

  - [<span data-ttu-id="b5958-116">Nueva característica Id. de autor de llamada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b5958-116">New caller ID feature in Lync Server 2013</span></span>](lync-server-2013-new-caller-id-feature.md)

  - [<span data-ttu-id="b5958-117">Característica nueva de correo de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b5958-117">New voice mail feature in Lync Server 2013</span></span>](lync-server-2013-new-voice-mail-feature.md)

  - [<span data-ttu-id="b5958-118">Nueva característica de tronco en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b5958-118">New trunk feature in Lync Server 2013</span></span>](lync-server-2013-new-trunk-feature.md)

  - [<span data-ttu-id="b5958-119">Nueva característica de troncos cruzados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b5958-119">New intertrunk feature in Lync Server 2013</span></span>](lync-server-2013-new-intertrunk-feature.md)

  - [<span data-ttu-id="b5958-120">Nuevas características de administración de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b5958-120">New call management features in Lync Server 2013</span></span>](lync-server-2013-new-call-management-features.md)

<span data-ttu-id="b5958-121"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b5958-121"></div>

<span> </span>

</div>

</div>

</span></span></div>

