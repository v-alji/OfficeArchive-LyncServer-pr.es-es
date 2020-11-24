---
title: 'Lync Server 2013: Consideraciones sobre coexistencia y migración para IPv6'
description: 'Lync Server 2013: consideraciones de migración y coexistencia para IPv6.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration and coexistence considerations for IPv6
ms:assetid: 8c769c4f-c8a9-4cbf-9080-beee3be9848a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205068(v=OCS.15)
ms:contentKeyID: 48184751
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e8618cc14ff3c2467ea41df34e39f5094d1206dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399689"
---
# <a name="migration-and-coexistence-considerations-for-ipv6-in-lync-server-2013"></a><span data-ttu-id="17181-103">Consideraciones sobre coexistencia y migración para IPv6 en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17181-103">Migration and coexistence considerations for IPv6 in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="17181-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="17181-104">

<span> </span></span></span>

<span data-ttu-id="17181-105">_**Última modificación del tema:** 2012-06-14_</span><span class="sxs-lookup"><span data-stu-id="17181-105">_**Topic Last Modified:** 2012-06-14_</span></span>

<span data-ttu-id="17181-106">La versión 6 de IP (IPv6) no es compatible con Lync Server 2010 o con Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="17181-106">IP version 6 (IPv6) is not supported on Lync Server 2010 or Office Communications Server.</span></span> <span data-ttu-id="17181-107">Para fines piloto, puede probar Lync Server 2010 y Lync Server 2013, coexistencia de pila doble.</span><span class="sxs-lookup"><span data-stu-id="17181-107">For piloting purposes, you can test Lync Server 2010 and Lync Server 2013 dual-stack coexistence.</span></span> <span data-ttu-id="17181-108">Le recomendamos que todos los grupos de un sitio central determinado se actualicen a Lync Server 2013 antes de habilitar IPv6 (red de pila doble) para cualquiera de los grupos.</span><span class="sxs-lookup"><span data-stu-id="17181-108">We recommend that all pools for a given central site are upgraded to Lync Server 2013 before you enable IPv6 (dual-stack network) for any of the pools.</span></span> <span data-ttu-id="17181-109">Si necesita configurar un grupo solo para IPv6, recomendamos configurar un grupo de servidores solo IPv6 en su entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="17181-109">If you need to configure a pool for IPv6 only, we recommend that you set up an IPv6-only pool in your lab environment for testing.</span></span>

<span data-ttu-id="17181-110">Se admiten los siguientes escenarios durante la migración y coexistencia:</span><span class="sxs-lookup"><span data-stu-id="17181-110">The following scenarios are supported during migration and coexistence:</span></span>

  - <span data-ttu-id="17181-111">Lync Server 2013, Lync Server 2010 y los grupos de Office Communications Server 2007 R2 en modo IPv4, coexistencia con Lync Server 2013 en modo Dual Stack.</span><span class="sxs-lookup"><span data-stu-id="17181-111">Lync Server 2013, Lync Server 2010, and Office Communications Server 2007 R2 pools in IPv4 mode, coexisting with Lync Server 2013 in dual-stack mode.</span></span>

  - <span data-ttu-id="17181-112">Grupo de servidores de Lync Server 2013 en modo de solo IPv6, si el grupo de solo IPv6 está en silos.</span><span class="sxs-lookup"><span data-stu-id="17181-112">Lync Server 2013 pool in IPv6-only mode, if the IPv6-only pool is siloed.</span></span>

<span data-ttu-id="17181-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="17181-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

