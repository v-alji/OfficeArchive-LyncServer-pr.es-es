---
title: 'Lync Server 2013: Información general sobre el director'
description: 'Lync Server 2013: información general del director.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Director
ms:assetid: cf9919b3-e16b-47c5-be1d-2c4bc64f44ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398879(v=OCS.15)
ms:contentKeyID: 48185393
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6686534e22bab5b02a2663789298e4cf7ea582c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424712"
---
# <a name="overview-of-the-director-in-lync-server-2013"></a><span data-ttu-id="c2f33-103">Información general sobre el director en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2f33-103">Overview of the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c2f33-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c2f33-104">

<span> </span></span></span>

<span data-ttu-id="c2f33-105">_**Última modificación del tema:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="c2f33-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="c2f33-106">Un director es un servidor que ejecuta Lync Server 2013 que autentica solicitudes de usuario, pero no aloja cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="c2f33-106">A Director is a server running Lync Server 2013 that authenticates user requests, but does not home any user accounts.</span></span> <span data-ttu-id="c2f33-107">De manera opcional, puede implementar un director en los dos escenarios siguientes:</span><span class="sxs-lookup"><span data-stu-id="c2f33-107">You optionally can deploy a Director in the following two scenarios:</span></span>

  - <span data-ttu-id="c2f33-108">Si habilita el acceso de usuarios externos mediante la implementación de servidores perimetrales, también debe implementar un director.</span><span class="sxs-lookup"><span data-stu-id="c2f33-108">If you enable access by external users by deploying Edge Servers, you should also deploy a Director.</span></span> <span data-ttu-id="c2f33-109">En este escenario, el director autentica a los usuarios externos y, a continuación, pasa su tráfico a los servidores internos.</span><span class="sxs-lookup"><span data-stu-id="c2f33-109">In this scenario, the Director authenticates the external users, and then passes their traffic on to internal servers.</span></span> <span data-ttu-id="c2f33-110">Cuando se usa un director para autenticar usuarios externos, libera servidores de grupo de servidores front-end de la sobrecarga de realizar la autenticación de estos usuarios.</span><span class="sxs-lookup"><span data-stu-id="c2f33-110">When a Director is used to authenticate external users, it relieves Front End pool servers from the overhead of performing authentication of these users.</span></span> <span data-ttu-id="c2f33-111">También ayuda a aislar grupos internos de aplicaciones para el usuario contra tráfico malintencionado, como ataques de denegación de servicio.</span><span class="sxs-lookup"><span data-stu-id="c2f33-111">It also helps insulate internal Front End pools from malicious traffic such as denial-of-service attacks.</span></span> <span data-ttu-id="c2f33-112">Si la red se inunda con tráfico externo no válido en tal ataque, este tráfico finaliza en el director.</span><span class="sxs-lookup"><span data-stu-id="c2f33-112">If the network is flooded with invalid external traffic in such an attack, this traffic ends at the Director.</span></span>

  - <span data-ttu-id="c2f33-113">Si implementa varios grupos front-end en un sitio central agregando un director a ese sitio, podrá optimizar las solicitudes de autenticación y mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c2f33-113">If you deploy multiple Front End pools at a central site, by adding a Director to that site you can streamline authentication requests and improve performance.</span></span> <span data-ttu-id="c2f33-114">En este escenario, todas las solicitudes se dirigen al Director, que a su vez las enruta al grupo de servidores front-end correcto.</span><span class="sxs-lookup"><span data-stu-id="c2f33-114">In this scenario, all requests go first to the Director, which then routes them to the correct Front End pool.</span></span>

<span data-ttu-id="c2f33-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c2f33-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

