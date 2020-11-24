---
title: 'Lync Server 2013: requisitos del sistema de nombres de dominio (DNS)'
description: 'Lync Server 2013: requisitos del sistema de nombres de dominio (DNS).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Domain Name System (DNS) requirements
ms:assetid: 586cf18e-0080-4eb1-aee5-56843277fdfc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398386(v=OCS.15)
ms:contentKeyID: 48184194
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f84868d4929cc410cddbb6c9ad2019a12841e80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397931"
---
# <a name="domain-name-system-dns-requirements-for-lync-server-2013"></a><span data-ttu-id="8e3a1-103">Requisitos del sistema de nombres de dominio (DNS) para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3a1-103">Domain Name System (DNS) requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e3a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e3a1-104">

<span> </span></span></span>

<span data-ttu-id="8e3a1-105">_**Última modificación del tema:** 2012-06-18_</span><span class="sxs-lookup"><span data-stu-id="8e3a1-105">_**Topic Last Modified:** 2012-06-18_</span></span>

<span data-ttu-id="8e3a1-106">Para implementar Lync Server, debe crear registros de sistema de nombres de dominio (DNS) que permitan el descubrimiento de clientes y servidores y, opcionalmente, soporte técnico para el inicio de sesión automático de cliente si su organización quiere admitirlo.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-106">To deploy Lync Server, you must create Domain Name System (DNS) records that enable the discovery of clients and servers, and, optionally, support for automatic client sign-in if your organization wants to support it.</span></span>

<span data-ttu-id="8e3a1-107">Lync Server usa DNS de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="8e3a1-107">Lync Server uses DNS in the following ways:</span></span>

  - <span data-ttu-id="8e3a1-108">Para detectar los servidores o grupos de servidores internos para las comunicaciones de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-108">To discover internal servers or pools for server-to-server communications.</span></span>

  - <span data-ttu-id="8e3a1-109">Para permitir que los clientes descubran el grupo de servidores front-end o el servidor Standard Edition usado para varias transacciones SIP.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-109">To allow clients to discover the Front End pool or Standard Edition server used for various SIP transactions.</span></span>

  - <span data-ttu-id="8e3a1-110">Para permitir los dispositivos de comunicaciones unificadas (UC) que no han iniciado sesión para descubrir el grupo de servidores front-end o el servidor Standard Edition que ejecuta el servicio Web de actualización de dispositivos, obtener actualizaciones y enviar registros.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-110">To allow unified communications (UC) devices that are not logged on to discover the Front End pool or Standard Edition server running Device Update Web Service, obtain updates, and send logs.</span></span>

  - <span data-ttu-id="8e3a1-111">Para permitir que los servidores y clientes externos se conecten a servidores perimetrales o al proxy inverso HTTP para mensajería instantánea (mi) o conferencias.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-111">To allow external servers and clients to connect to Edge Servers or the HTTP reverse proxy for instant messaging (IM) or conferencing.</span></span>

  - <span data-ttu-id="8e3a1-112">Para permitir que los dispositivos de comunicaciones unificadas externos se conecten al servicio Web de actualización de dispositivos a través de servidores perimetrales o el proxy inverso HTTP y obtener actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-112">To allow external UC devices to connect to Device Update Web service through Edge Servers or the HTTP reverse proxy and obtain updates.</span></span>

  - <span data-ttu-id="8e3a1-113">Para permitir que los clientes móviles detecten automáticamente recursos de servicios web sin que los usuarios tengan que escribir manualmente las direcciones URL en la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-113">To allow mobile clients to automatically discover Web Services resources without requiring users to manually enter URLs in device settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8e3a1-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8e3a1-114">In This Section</span></span>

  - [<span data-ttu-id="8e3a1-115">Determinar los requisitos DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3a1-115">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)

  - [<span data-ttu-id="8e3a1-116">Requisitos de DNS para las agrupaciones front-end en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3a1-116">DNS requirements for Front End pools in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-front-end-pools.md)

  - [<span data-ttu-id="8e3a1-117">Requisitos de DNS para servidores Standard Edition en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3a1-117">DNS requirements for Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-standard-edition-servers.md)

  - [<span data-ttu-id="8e3a1-118">Requisitos de DNS para direcciones URL simples en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3a1-118">DNS requirements for simple URLs in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-simple-urls.md)

  - [<span data-ttu-id="8e3a1-119">Requisitos de DNS para el inicio de sesión automático de cliente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3a1-119">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)

  - [<span data-ttu-id="8e3a1-120">Requisitos de DNS para movilidad con Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3a1-120">DNS requirements for mobility with Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-mobility.md)

  - [<span data-ttu-id="8e3a1-121">Equilibrio de carga de DNS en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3a1-121">DNS load balancing in Lync Server 2013</span></span>](lync-server-2013-dns-load-balancing.md)

<span data-ttu-id="8e3a1-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e3a1-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

