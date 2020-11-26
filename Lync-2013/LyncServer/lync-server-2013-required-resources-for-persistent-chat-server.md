---
title: 'Lync Server 2013: Recursos requeridos para el servidor de chat persistente'
description: 'Lync Server 2013: recursos necesarios para el servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Required resources
ms:assetid: bce50b95-f3c8-407e-963a-d8896ee77fbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205211(v=OCS.15)
ms:contentKeyID: 48185255
ms.date: 02/05/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18c81f0017428e4305e46fbcf5580a83af38accf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442707"
---
# <a name="required-resources-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="55d77-103">Recursos requeridos para el servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="55d77-103">Required resources for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="55d77-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="55d77-104">

<span> </span></span></span>

<span data-ttu-id="55d77-105">_**Última modificación del tema:** 2016-02-05_</span><span class="sxs-lookup"><span data-stu-id="55d77-105">_**Topic Last Modified:** 2016-02-05_</span></span>

<span data-ttu-id="55d77-106">La alta disponibilidad y la recuperación ante desastres para el servidor de chat persistente requieren recursos adicionales más allá de lo que normalmente se necesita para una completa operación.</span><span class="sxs-lookup"><span data-stu-id="55d77-106">High availability and disaster recovery for Persistent Chat Server requires additional resources beyond what is typically needed for full operation.</span></span> <span data-ttu-id="55d77-107">Antes de configurar el servidor de chat persistente para una alta disponibilidad y recuperación ante desastres, asegúrese de disponer de los recursos siguientes, además de lo que se requiere para el funcionamiento del servidor de chat persistente estándar.</span><span class="sxs-lookup"><span data-stu-id="55d77-107">Before configuring Persistent Chat Server for high availability and disaster recovery, ensure that you have the following resources in addition to what is required for standard Persistent Chat Server operation.</span></span> <span data-ttu-id="55d77-108">Para obtener información de configuración adicional, consulte [configuración de un servidor de chat persistente en Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="55d77-108">For additional configuration information, see [Configuring Persistent Chat Server in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md).</span></span>

  - <span data-ttu-id="55d77-109">Una instancia de base de datos dedicada ubicada en el mismo centro de datos físico en el que se encuentra el front-end del servicio del servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="55d77-109">One dedicated database instance located in the same physical data center in which the home front end of the Persistent Chat Server service is located.</span></span> <span data-ttu-id="55d77-110">Esta base de datos servirá de SQL Server Mirror para la base de datos de chat persistente principal.</span><span class="sxs-lookup"><span data-stu-id="55d77-110">This database will serve as the SQL Server mirror for the primary Persistent Chat database.</span></span> <span data-ttu-id="55d77-111">De manera opcional, designe un servidor SQL Server adicional para que sirva como testigo de creación de reflejos si desea una conmutación automática para la base de datos reflejada.</span><span class="sxs-lookup"><span data-stu-id="55d77-111">Optionally, designate an additional SQL Server to serve as the mirroring witness if you want an automated failover to the mirror database.</span></span>

  - <span data-ttu-id="55d77-112">Una instancia de base de datos dedicada ubicada en el otro centro de datos físico.</span><span class="sxs-lookup"><span data-stu-id="55d77-112">One dedicated database instance located in the other physical data center.</span></span> <span data-ttu-id="55d77-113">Esta base de datos servirá como la base de datos secundaria de trasvase de registros de SQL Server para la base de datos en el centro de datos principal.</span><span class="sxs-lookup"><span data-stu-id="55d77-113">This database will serve as the SQL Server Log Shipping secondary database for the database in the primary data center.</span></span>

  - <span data-ttu-id="55d77-114">Una instancia de base de datos dedicada que servirá como reflejo de SQL Server para la base de datos secundaria.</span><span class="sxs-lookup"><span data-stu-id="55d77-114">One dedicated database instance to serve as the SQL Server mirror for the secondary database.</span></span> <span data-ttu-id="55d77-115">De manera opcional, designe un servidor SQL Server adicional como testigo de creación de reflejos.</span><span class="sxs-lookup"><span data-stu-id="55d77-115">Optionally, designate an additional SQL Server to server as the mirroring witness.</span></span> <span data-ttu-id="55d77-116">Es preciso que ambos estén ubicados en el mismo centro de datos físico que la base de datos secundaria.</span><span class="sxs-lookup"><span data-stu-id="55d77-116">Both of these must be located in the same physical data center as the secondary database.</span></span>

  - <span data-ttu-id="55d77-117">Si el cumplimiento del servidor de chat persistente está habilitado, se necesitan tres instancias de base de datos dedicadas adicionales.</span><span class="sxs-lookup"><span data-stu-id="55d77-117">If Persistent Chat Server compliance is enabled, an additional three dedicated database instances are required.</span></span> <span data-ttu-id="55d77-118">Su distribución es la misma que la de la base de datos de chat persistente anterior.</span><span class="sxs-lookup"><span data-stu-id="55d77-118">Their distribution is the same as those previously outlined for the Persistent Chat database.</span></span> <span data-ttu-id="55d77-119">Aunque es posible que la base de datos de cumplimiento comparta la misma instancia de SQL Server que la base de datos de chat persistente, recomendamos instancias independientes para la alta disponibilidad y la recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="55d77-119">While it is possible for the compliance database to share the same SQL Server instance as the Persistent Chat database, we recommend standalone instances for high availability and disaster recovery.</span></span>

  - <span data-ttu-id="55d77-120">Es necesario crear y designar un recurso compartido de archivos para los registros de transacciones de trasvase de registros de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="55d77-120">A file share must be created and designated for the SQL Server Log Shipping transaction logs.</span></span> <span data-ttu-id="55d77-121">Todos los servidores SQL de ambos centros de datos que ejecutan bases de datos de chat persistentes deben tener acceso de lectura y escritura a este recurso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="55d77-121">All SQL Servers in both data centers that run Persistent Chat databases must have read/write access to this file share.</span></span> <span data-ttu-id="55d77-122">Este recurso compartido no está designado como parte del rol FileStore.</span><span class="sxs-lookup"><span data-stu-id="55d77-122">This share is not defined as part of a FileStore role.</span></span>

  - <span data-ttu-id="55d77-123">Un recurso compartido de archivos en el servidor de la base de datos secundaria para que sirva como carpeta de destino para los registros de transacciones de SQL Server que se copian desde el recurso compartido de archivos del servidor principal.</span><span class="sxs-lookup"><span data-stu-id="55d77-123">A file share on the secondary database server to serve as the destination folder for the SQL Server transaction logs that are copied from the primary server file share.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="55d77-124">Los servidores de chat persistente activos en un grupo de servidores de chat persistente deben residir en la misma zona horaria que el grupo de Lync del próximo salto definido en la topología.</span><span class="sxs-lookup"><span data-stu-id="55d77-124">Active Persistent Chat servers in a Persistent Chat Server pool MUST reside in the same time zone as the next hop Lync Pool defined in the topology.</span></span>



</div>

<span data-ttu-id="55d77-125">Las figuras siguientes proporcionan ejemplos acerca de cómo se puede configurar todo el grupo de servidores de chat persistente en las dos topologías de grupo extendidas diferentes:</span><span class="sxs-lookup"><span data-stu-id="55d77-125">The following figures provide examples about how the entire Persistent Chat Server pool can be configured in the two different stretched pool topologies:</span></span>

  - <span data-ttu-id="55d77-126">Grupo de servidores de chat persistente estirado cuando los centros de datos se encuentran en un gran ancho de banda y baja latencia.</span><span class="sxs-lookup"><span data-stu-id="55d77-126">Stretched Persistent Chat Server pool when data centers are geo-located with high bandwidth/low latency.</span></span>

  - <span data-ttu-id="55d77-127">Grupo de servidores de chat persistente estirado cuando los centros de datos se encuentran en una ubicación geográfica con un ancho de banda bajo y una latencia alta.</span><span class="sxs-lookup"><span data-stu-id="55d77-127">Stretched Persistent Chat Server pool when data centers are geo-located with low bandwidth/high latency.</span></span>

<span data-ttu-id="55d77-128">La siguiente ilustración muestra una topología de grupo de servidores de chat persistente superpuesto en la que los centros de datos se encuentran en una ubicación geográfica con un alto ancho de banda y baja latencia.</span><span class="sxs-lookup"><span data-stu-id="55d77-128">The following figure shows a stretched Persistent Chat Server pool topology where data centers are geo-located with high bandwidth/low latency.</span></span>

<span data-ttu-id="55d77-129">**Grupo de servidores de chat persistente estirado cuando los centros de datos se encuentran en un gran ancho de banda y baja latencia.**</span><span class="sxs-lookup"><span data-stu-id="55d77-129">**Stretched Persistent Chat Server pool when data centers are geo-located with high bandwidth/low latency.**</span></span>

<span data-ttu-id="55d77-130">![Examen de configuración HBW del grupo de servidores de chat persistente](images/JJ205211.55d10910-c824-41e6-bed2-08d13a2abd65(OCS.15).jpg "Examen de configuración HBW del grupo de servidores de chat persistente")</span><span class="sxs-lookup"><span data-stu-id="55d77-130">![Persistent Chat Server pool HBW configuration exam](images/JJ205211.55d10910-c824-41e6-bed2-08d13a2abd65(OCS.15).jpg "Persistent Chat Server pool HBW configuration exam")</span></span>

<span data-ttu-id="55d77-131">La siguiente ilustración muestra una topología de grupo de servidores de chat persistente superpuesto en la que los centros de datos se encuentran en una ubicación geográfica con un ancho de banda bajo y una latencia elevada.</span><span class="sxs-lookup"><span data-stu-id="55d77-131">The following figure shows a stretched Persistent Chat Server pool topology where data centers are geo-located with low bandwidth/high latency.</span></span>

<span data-ttu-id="55d77-132">**Grupo de servidores de chat persistente estirado cuando los centros de datos se encuentran en una ubicación geográfica con un ancho de banda bajo y una latencia alta.**</span><span class="sxs-lookup"><span data-stu-id="55d77-132">**Stretched Persistent Chat Server pool when data centers are geo-located with low bandwidth/high latency.**</span></span>

<span data-ttu-id="55d77-133">![Examen de configuración LBW del grupo de servidores de chat persistente](images/JJ205211.586b0a3a-3767-4991-944f-ee54389512aa(OCS.15).jpg "Examen de configuración LBW del grupo de servidores de chat persistente")</span><span class="sxs-lookup"><span data-stu-id="55d77-133">![Persistent Chat Server pool LBW configuration exam](images/JJ205211.586b0a3a-3767-4991-944f-ee54389512aa(OCS.15).jpg "Persistent Chat Server pool LBW configuration exam")</span></span>

<span data-ttu-id="55d77-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="55d77-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

