---
title: Configurar servidores de chat persistente para la alta disponibilidad y la recuperación ante desastres
description: Configuración del servidor de chat persistente para una alta disponibilidad y recuperación ante desastres.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Persistent Chat Server for high availability and disaster recovery
ms:assetid: eebc581c-e3a0-4b69-8a43-80b607b4d8f2
ms:mtpsurl: https://technet.microsoft.com/library/JJ205364(v=OCS.15)
ms:contentKeyID: 48185760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 13935f2ec690deb7f896c13d185680ce1122a892
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432789"
---
# <a name="configuring-persistent-chat-server-for-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="5ac73-103">Configurar servidores de chat persistente para la alta disponibilidad y la recuperación ante desastres en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ac73-103">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5ac73-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5ac73-104">

<span> </span></span></span>

<span data-ttu-id="5ac73-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="5ac73-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="5ac73-106">Los servicios Lync Server 2013, servidor de chat persistente usan una configuración de *agrupación extendida* para la recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="5ac73-106">The Lync Server 2013, Persistent Chat Server services use a *stretched pool* configuration for disaster recovery.</span></span> <span data-ttu-id="5ac73-107">Una agrupación extendida es una agrupación que tiene equipos que se distribuyen entre dos centros de datos físicos, pero que se encuentran dentro de un único sitio lógico de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5ac73-107">A stretched pool is a pool that has computers that are distributed between two physical data centers, but are within a single logical Lync Server site.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5ac73-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5ac73-108">In This Section</span></span>

  - [<span data-ttu-id="5ac73-109">Recursos requeridos para el servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ac73-109">Required resources for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-required-resources-for-persistent-chat-server.md)

  - [<span data-ttu-id="5ac73-110">Usar Topology Builder para configurar la alta disponibilidad y la recuperación ante desastres en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ac73-110">Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-topology-builder-to-configure-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="5ac73-111">Usar un grupo de servidores de chat persistente estirado para la recuperación ante desastres en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ac73-111">Using a stretched Persistent Chat Server pool for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-a-stretched-persistent-chat-server-pool-for-disaster-recovery.md)

  - [<span data-ttu-id="5ac73-112">Crear un reflejo de SQL Server en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ac73-112">SQL Server mirroring in Lync Server 2013</span></span>](lync-server-2013-sql-server-mirroring.md)

  - [<span data-ttu-id="5ac73-113">Configurar registro de transacciones de SQL Server para base de datos principal del servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ac73-113">Setting up SQL Server Log Shipping in Lync Server 2013 for the Persistent Chat Server primary database</span></span>](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md)

  - [<span data-ttu-id="5ac73-114">Configuración del envío de registro de SQL Server entre el reflejo principal y la base de datos secundaria de envío de registro en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ac73-114">Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013</span></span>](lync-server-2013-set-up-log-shipping-secondary-database.md)

<span data-ttu-id="5ac73-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5ac73-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

