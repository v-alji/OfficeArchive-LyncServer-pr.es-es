---
title: 'Lync Server 2013: Compatibilidad con software de base de datos'
description: Soporte de software de base de datos de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Database software support
ms:assetid: e05d0032-bbea-4e61-987d-d07b1c045fd5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398990(v=OCS.15)
ms:contentKeyID: 48185517
ms.date: 12/02/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c5d7b44e5febc4123dbcdf7072b98fcfd004609
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431228"
---
# <a name="database-software-support-in-lync-server-2013"></a><span data-ttu-id="a22b3-103">Compatibilidad con software de base de datos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a22b3-103">Database software support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a22b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a22b3-104">

<span> </span></span></span>

<span data-ttu-id="a22b3-105">_**Última modificación del tema:** 2014-12-01_</span><span class="sxs-lookup"><span data-stu-id="a22b3-105">_**Topic Last Modified:** 2014-12-01_</span></span>

<span data-ttu-id="a22b3-106">Lync Server 2013 admite los siguientes sistemas de administración de bases de datos:</span><span class="sxs-lookup"><span data-stu-id="a22b3-106">Lync Server 2013 supports the following database management systems:</span></span>

  - <span data-ttu-id="a22b3-107">**Base de datos back-end de un grupo de servidores front-end, una base de datos de archivado, una base de datos de supervisión, una base de datos de chat persistente y una base de datos para el cumplimiento de chat persistente**</span><span class="sxs-lookup"><span data-stu-id="a22b3-107">**Back-end database of a Front End pool, Archiving database, Monitoring database, persistent chat database, and persistent chat compliance database**</span></span>
    
      - <span data-ttu-id="a22b3-p101">Software de base de datos Microsoft SQL Server 2008 R2 Enterprise (edición de 64 bits) o el último service pack (recomendado)</span><span class="sxs-lookup"><span data-stu-id="a22b3-p101">Microsoft SQL Server 2008 R2 Enterprise database software (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="a22b3-p102">Microsoft SQL Server 2008 R2 Standard (edición de 64 bits) o el último service pack (recomendado)</span><span class="sxs-lookup"><span data-stu-id="a22b3-p102">Microsoft SQL Server 2008 R2 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="a22b3-p103">Microsoft SQL Server 2012 Enterprise (edición de 64 bits) o el último service pack (recomendado)</span><span class="sxs-lookup"><span data-stu-id="a22b3-p103">Microsoft SQL Server 2012 Enterprise (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="a22b3-p104">Microsoft SQL Server 2012 Standard (edición de 64 bits) o el último service pack (recomendado)</span><span class="sxs-lookup"><span data-stu-id="a22b3-p104">Microsoft SQL Server 2012 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>

  - <span data-ttu-id="a22b3-116">**Bases de datos del servidor Standard Edition y del servidor front-end**</span><span class="sxs-lookup"><span data-stu-id="a22b3-116">**Standard Edition server database and Front End Server databases**</span></span>
    
      - <span data-ttu-id="a22b3-117">Microsoft SQL Server 2012 Express (edición de 64 bits).</span><span class="sxs-lookup"><span data-stu-id="a22b3-117">Microsoft SQL Server 2012 Express (64-bit edition).</span></span> <span data-ttu-id="a22b3-118">Se recomienda ejecutar además el último Service Pack.</span><span class="sxs-lookup"><span data-stu-id="a22b3-118">Additionally running the latest service pack is recommended.</span></span>
        
        <span data-ttu-id="a22b3-119">Admitimos la revisión y actualización de Microsoft SQL Server en servidores front-end y servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a22b3-119">We support the patching and upgrade of Microsoft SQL Server on Front End Servers and Standard Edition servers.</span></span> <span data-ttu-id="a22b3-120">Sin embargo, cuando realiza cualquier tipo de actualización o revisión en servidores de aplicaciones para el usuario, debe tener en cuenta los requisitos de quórum.</span><span class="sxs-lookup"><span data-stu-id="a22b3-120">However, when you make any kind of upgrade or patch on Front End Servers, you must account for quorum requirements.</span></span> <span data-ttu-id="a22b3-121">Para obtener más información, consulte [Upgrade or update Front End Servers in Lync Server 2013](lync-server-2013-upgrade-or-update-front-end-servers.md) y [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span><span class="sxs-lookup"><span data-stu-id="a22b3-121">For more information, see [Upgrade or update Front End Servers in Lync Server 2013](lync-server-2013-upgrade-or-update-front-end-servers.md) and [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a22b3-122">Lync Server 2013 instala automáticamente Microsoft SQL Server 2012 Express (64-bit Edition) en cada servidor Standard Edition y cada servidor de servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="a22b3-122">Microsoft SQL Server 2012 Express (64-bit edition) is automatically installed by Lync Server 2013 on each Standard Edition server and each Front End Server server.</span></span>

    
    </div>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="a22b3-123">Lync Server 2013 no es compatible con la edición de 32 bits de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a22b3-123">Lync Server 2013 does not support the 32-bit edition of SQL Server.</span></span> <span data-ttu-id="a22b3-124">Emplee la edición de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a22b3-124">You must use the 64-bit edition.</span></span></P>
> <LI>
> <P><span data-ttu-id="a22b3-125">SQL Server Web Edition y SQL Server Workgroup Edition no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="a22b3-125">SQL Server Web edition and SQL Server Workgroup edition are not supported.</span></span> <span data-ttu-id="a22b3-126">No puede usarlos con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a22b3-126">You cannot use them with Lync Server 2013.</span></span></P>
> <LI>
> <P><span data-ttu-id="a22b3-127">Lync Server 2013 admite el reflejo de base de datos nativa.</span><span class="sxs-lookup"><span data-stu-id="a22b3-127">Lync Server 2013 does support native database mirroring.</span></span></P>
> <LI>
> <P><span data-ttu-id="a22b3-128">Para usar el rol de servidor supervisión, debe instalar SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="a22b3-128">To use the Monitoring Server role, you should install SQL Server Reporting Services.</span></span></P></LI></UL>



</div>

<span data-ttu-id="a22b3-129">En un grupo de servidores front-end, la base de datos back-end puede ser un único equipo SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a22b3-129">In a Front End pool, the back-end database can be a single SQL Server computer.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a22b3-130">Si Collocate bases de datos de Lync Server con otras bases de datos, recomendamos encarecidamente evaluar todos los factores que pueden afectar a la disponibilidad y el rendimiento, así como garantizar que, si se produce un error en un nodo, el nodo restante puede controlar la carga.</span><span class="sxs-lookup"><span data-stu-id="a22b3-130">If you collocate Lync Server databases with other databases, we highly recommend assessing all factors that might affect availability and performance, as well as ensuring that, if one node fails, the remaining node can handle the load.</span></span> <span data-ttu-id="a22b3-131">Para comprobar las capacidades de conmutación por error, se recomienda probar todos los escenarios de conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="a22b3-131">To verify failover capabilities, we recommend testing all failover scenarios.</span></span>



</div>

<div>

## <a name="using-sql-mirroring-and-sql-clustering"></a><span data-ttu-id="a22b3-132">Información de uso sobre la creación de espejos y la agrupación en clústeres de SQL</span><span class="sxs-lookup"><span data-stu-id="a22b3-132">Using SQL Mirroring and SQL Clustering</span></span>

<span data-ttu-id="a22b3-133">Lync Server 2013 admite el uso de la creación de reflejos SQL o SQL clustering en cada base de datos de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a22b3-133">Lync Server 2013 supports the use of either SQL mirroring or SQL clustering for each Lync Server database.</span></span> <span data-ttu-id="a22b3-134">Puede configurar el reflejo de SQL fácilmente con la herramienta topología del compilador de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a22b3-134">You can easily set up SQL mirroring with the Topology Builder tool in Lync Server 2013.</span></span> <span data-ttu-id="a22b3-135">Los clústeres de conmutación por error de SQL deben configurarse desde SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a22b3-135">For SQL failover clustering, you must use SQL Server for setup.</span></span>

<span data-ttu-id="a22b3-136">Lync Server 2013 admite el reflejo SQL y las topologías de clúster SQL para todas las implementaciones, incluidas las implementaciones y organizaciones de Greenfield que han actualizado de versiones anteriores de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a22b3-136">Lync Server 2013 supports both SQL mirroring and SQL clustering topologies for all deployments, including greenfield deployments and organizations that have upgraded from previous versions of Lync Server.</span></span>

<span data-ttu-id="a22b3-p111">La agrupación en clústeres de SQL es compatible con la configuración activa/pasiva. Por motivos de rendimiento, el nodo pasivo no debe compartirse con otras instancias de SQL.</span><span class="sxs-lookup"><span data-stu-id="a22b3-p111">SQL Clustering support is for an active/passive configuration. For performance reasons, the passive node should not be shared by any other SQL instance.</span></span>

<span data-ttu-id="a22b3-139">Se ofrecen los supuestos de compatibilidad siguientes:</span><span class="sxs-lookup"><span data-stu-id="a22b3-139">The following support is included:</span></span>

  - <span data-ttu-id="a22b3-140">Clústeres de conmutación por error de dos nodos para:</span><span class="sxs-lookup"><span data-stu-id="a22b3-140">Two-node failover clustering for the following:</span></span>
    
      - <span data-ttu-id="a22b3-p112">Microsoft SQL Server 2012 Standard (edición de 64 bits) o el último service pack (recomendado)</span><span class="sxs-lookup"><span data-stu-id="a22b3-p112">Microsoft SQL Server 2012 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="a22b3-p113">Microsoft SQL Server 2008 R2 Standard (edición de 64 bits) o el último service pack (recomendado)</span><span class="sxs-lookup"><span data-stu-id="a22b3-p113">Microsoft SQL Server 2008 R2 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>

  - <span data-ttu-id="a22b3-145">Clústeres de conmutación por error de hasta dieciséis nodos para:</span><span class="sxs-lookup"><span data-stu-id="a22b3-145">Up to sixteen-node failover clustering for the following:</span></span>
    
      - <span data-ttu-id="a22b3-p114">Microsoft SQL Server 2012 Enterprise (edición de 64 bits) o el último service pack (recomendado)</span><span class="sxs-lookup"><span data-stu-id="a22b3-p114">Microsoft SQL Server 2012 Enterprise (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="a22b3-p115">Software de base de datos Microsoft SQL Server 2008 R2 Enterprise (edición de 64 bits) o el último service pack (recomendado)</span><span class="sxs-lookup"><span data-stu-id="a22b3-p115">Microsoft SQL Server 2008 R2 Enterprise database software (64-bit edition). Additionally running the latest service pack is recommended.</span></span>

<span data-ttu-id="a22b3-150">Para obtener más información sobre la creación de reflejos de SQL, vea la [alta disponibilidad del servidor de back-end en Lync server 2013](lync-server-2013-back-end-server-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="a22b3-150">For more information about SQL mirroring, see [Back End Server high availability in Lync Server 2013](lync-server-2013-back-end-server-high-availability.md).</span></span> <span data-ttu-id="a22b3-151">Para obtener más información sobre cómo implementar clústeres SQL, consulte [configurar clústeres de SQL Server para Lync Server 2013](lync-server-2013-configure-sql-server-clustering.md).</span><span class="sxs-lookup"><span data-stu-id="a22b3-151">For details on how to deploy SQL clustering, see [Configure SQL Server clustering for Lync Server 2013](lync-server-2013-configure-sql-server-clustering.md).</span></span>

<span data-ttu-id="a22b3-152">Para obtener más información y procedimientos recomendados para el clúster de conmutación por error en SQL Server 2012, consulte <https://technet.microsoft.com/library/hh231721.aspx> .</span><span class="sxs-lookup"><span data-stu-id="a22b3-152">For more information and best practices for failover clustering in SQL Server 2012, see <https://technet.microsoft.com/library/hh231721.aspx>.</span></span> <span data-ttu-id="a22b3-153">Para el clúster de conmutación por error en SQL Server 2008, consulte <https://technet.microsoft.com/library/ms189134(v=sql.105).aspx> .</span><span class="sxs-lookup"><span data-stu-id="a22b3-153">For failover clustering in SQL Server 2008, see <https://technet.microsoft.com/library/ms189134(v=sql.105).aspx>.</span></span>

<span data-ttu-id="a22b3-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a22b3-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

