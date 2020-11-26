---
title: 'Lync Server 2013: restauración de un grupo de servidores de Lync'
description: 'Lync Server 2013: restauración de un grupo de servidores de Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a Lync Server pool
ms:assetid: 6fe80fb3-38ad-4931-a07b-1763b61aa448
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202176(v=OCS.15)
ms:contentKeyID: 51541488
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02e92b4e7af9cf782d49c265425006e0118b9161
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442603"
---
# <a name="restoring-a-lync-server-pool-in-lync-server-2013"></a><span data-ttu-id="68b44-103">Restauración de un grupo de servidores de Lync en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68b44-103">Restoring a Lync Server pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68b44-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68b44-104">

<span> </span></span></span>

<span data-ttu-id="68b44-105">_**Última modificación del tema:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="68b44-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="68b44-106">La implementación de Lync Server puede incluir cualquiera de los siguientes tipos de grupos:</span><span class="sxs-lookup"><span data-stu-id="68b44-106">Your Lync Server deployment may include any of the following types of pools:</span></span>

  - <span data-ttu-id="68b44-107">Servidor front-end</span><span class="sxs-lookup"><span data-stu-id="68b44-107">Front End Server</span></span>

  - <span data-ttu-id="68b44-108">Servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="68b44-108">Mediation Server</span></span>

  - <span data-ttu-id="68b44-109">Servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="68b44-109">Persistent Chat Server</span></span>

  - <span data-ttu-id="68b44-110">Servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="68b44-110">Edge Server</span></span>

<span data-ttu-id="68b44-111">Si todo un grupo sufre una interrupción, siga estos procedimientos para cada uno de los servidores miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="68b44-111">If an entire pool experiences an outage, follow these procedures for each member server in the pool.</span></span>

  - <span data-ttu-id="68b44-112">Para un grupo de servidores front-end, restaure primero el servidor back-end y, después, restaure cada servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="68b44-112">For a Front End pool, restore the Back End Server first, and then restore each Front End Server.</span></span> <span data-ttu-id="68b44-113">Para obtener más información, consulte [restaurar un servidor de servicios de fondo de la edición empresarial en Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) y [restaurar un servidor miembro de Enterprise Edition en Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span><span class="sxs-lookup"><span data-stu-id="68b44-113">For details, see [Restoring an Enterprise Edition Back End Server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) and [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

  - <span data-ttu-id="68b44-114">Para todos los demás tipos de grupos, restaure cada servidor miembro.</span><span class="sxs-lookup"><span data-stu-id="68b44-114">For all other types of pools, restore each member server.</span></span> <span data-ttu-id="68b44-115">Para obtener más información, vea [restaurar un servidor miembro de Enterprise Edition en Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span><span class="sxs-lookup"><span data-stu-id="68b44-115">For details, see [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

<span data-ttu-id="68b44-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68b44-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

