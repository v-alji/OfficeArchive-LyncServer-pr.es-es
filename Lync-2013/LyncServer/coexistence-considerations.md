---
title: Consideraciones sobre la coexistencia
description: Consideraciones de coexistencia.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Coexistence considerations
ms:assetid: 9d1a3c0f-492a-4e37-bc2f-63509e328785
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205131(v=OCS.15)
ms:contentKeyID: 48184990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd1f9525b37bdee3249e0e47352fdea1bc7f012f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399180"
---
# <a name="coexistence-considerations"></a><span data-ttu-id="07820-103">Consideraciones sobre la coexistencia</span><span class="sxs-lookup"><span data-stu-id="07820-103">Coexistence considerations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07820-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07820-104">

<span> </span></span></span>

<span data-ttu-id="07820-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="07820-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="07820-106">Después de la migración, solo existirá un servidor Lync Server 2013, el grupo de servidores de chat persistente y podrá dar de baja la implementación heredada.</span><span class="sxs-lookup"><span data-stu-id="07820-106">After migration, only a Lync Server 2013, Persistent Chat Server pool will exist, and you can decommission your legacy deployment.</span></span>

<span data-ttu-id="07820-107">Antes de que se complete la migración y antes de haber desactivado la implementación del servidor de chat de grupo actual, es posible que tenga alguna de las siguientes implementaciones:</span><span class="sxs-lookup"><span data-stu-id="07820-107">Before migration completes and before you have decommissioned your current Group Chat Server deployment completely, you may have any of the following deployments:</span></span>

  - <span data-ttu-id="07820-108">Lync Server 2013, grupo de servidores de chat persistente, que debe estar alojado en un grupo de servidores de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="07820-108">Lync Server 2013, Persistent Chat Server pool, which must be homed on a Lync Server 2013 pool.</span></span>

  - <span data-ttu-id="07820-109">Lync Server 2010, grupo de chats grupales, que se debe alojar en un grupo de servidores de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="07820-109">Lync Server 2010, Group Chat pool, which must be homed on a Lync Server 2010 pool.</span></span>

  - <span data-ttu-id="07820-110">Grupo de chats grupales de Office Communications Server 2007 R2, que debe estar alojado en un grupo de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="07820-110">Office Communications Server 2007 R2 Group Chat pool, which must be homed on an Office Communications Server 2007 R2 pool.</span></span>

<span data-ttu-id="07820-111">Estas implementaciones pueden existir en paralelo.</span><span class="sxs-lookup"><span data-stu-id="07820-111">These deployments can exist side by side.</span></span> <span data-ttu-id="07820-112">Sin embargo, las categorías, salas y complementos de una implementación no interactúan con los de la implementación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="07820-112">However the categories, rooms, and add-ins in one deployment do not interact with those in the accompanying deployment.</span></span>

<span data-ttu-id="07820-113">Con la configuración manual, un cliente heredado (cliente de chat grupal) puede conectarse a un grupo a la vez para Office Communications Server 2007 R2, Lync Server 2010, chat grupal o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="07820-113">Using manual configuration, a legacy client (Group Chat client) can connect to one pool at a time for Office Communications Server 2007 R2, Lync Server 2010, Group Chat, or Lync Server 2013.</span></span>

<span data-ttu-id="07820-114">Lync 2013 (cliente) solo puede interactuar con Lync Server 2013, grupo de servidores de chat persistente y no con grupos de servidores de chat heredados.</span><span class="sxs-lookup"><span data-stu-id="07820-114">The Lync 2013 (client) can interact only with the Lync Server 2013, Persistent Chat Server pool, not with legacy Group Chat Server pools.</span></span> <span data-ttu-id="07820-115">Para usar el chat persistente en una 2013 (cliente) de Lync, el usuario debe estar alojado en Lync 2013 y habilitado por directiva.</span><span class="sxs-lookup"><span data-stu-id="07820-115">To use Persistent Chat in a Lync 2013 (client), the user must be homed on Lync 2013 and enabled by policy.</span></span>

<span data-ttu-id="07820-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07820-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

