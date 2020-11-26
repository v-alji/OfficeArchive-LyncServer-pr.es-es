---
title: Migrar servidores de archivado y supervisión
description: Migrar los servidores de archivado y supervisión.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating Archiving and Monitoring servers
ms:assetid: 77831579-df45-4697-b8c5-207b74a07a40
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205015(v=OCS.15)
ms:contentKeyID: 48184550
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2dabd16fd38dbf463a4bc608fe77368e781571fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443751"
---
# <a name="migrating-archiving-and-monitoring-servers"></a><span data-ttu-id="b3900-103">Migrar servidores de archivado y supervisión</span><span class="sxs-lookup"><span data-stu-id="b3900-103">Migrating Archiving and Monitoring servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3900-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3900-104">

<span> </span></span></span>

<span data-ttu-id="b3900-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="b3900-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="b3900-106">Si ha implementado el servidor de archivado y el servidor de supervisión en el entorno de Lync Server 2010, puede implementar estos servidores en el entorno de Lync Server 2013 después de migrar los grupos de aplicaciones para el usuario.</span><span class="sxs-lookup"><span data-stu-id="b3900-106">If you deployed Archiving Server and Monitoring Server in your Lync Server 2010 environment, you can deploy these servers in your Lync Server 2013 environment after you migrate your Front End pools.</span></span> <span data-ttu-id="b3900-107">Sin embargo, si la funcionalidad de archivado y supervisión es crítica para su organización, debe agregar el archivado y la supervisión al grupo de pruebas piloto de Lync Server 2013 antes de la migración para que la funcionalidad esté disponible durante el proceso de migración.</span><span class="sxs-lookup"><span data-stu-id="b3900-107">If archiving and monitoring functionality are critical to your organization, however, you should add archiving and monitoring to your Lync Server 2013 pilot pool before you migrate so that the functionality is available during the migration process.</span></span>

<span data-ttu-id="b3900-108">Si desea mantener la funcionalidad de archivado y supervisión durante el proceso de migración, tenga en cuenta las siguientes consideraciones:</span><span class="sxs-lookup"><span data-stu-id="b3900-108">If you want archiving and monitoring functionality during the migration process, keep the following considerations in mind:</span></span>

  - <span data-ttu-id="b3900-109">Los datos de archivado y supervisión no se mueven a la implementación de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b3900-109">Archiving data and monitoring data are not moved to the Lync Server 2013 deployment.</span></span> <span data-ttu-id="b3900-110">Los datos de los que haya hecho una copia de seguridad antes de retirar el entorno heredado serán el historial de actividad en el entorno de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b3900-110">The data you back up prior to decommissioning the legacy environment will be your history of activity in the Lync Server 2010 environment.</span></span>

  - <span data-ttu-id="b3900-111">La versión de Lync Server 2010 del servidor de archivado y del servidor de supervisión solo se puede asociar con un grupo front-end de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b3900-111">The Lync Server 2010 version of Archiving Server and Monitoring Server can be associated only with a Lync Server 2010 Front End pool.</span></span> <span data-ttu-id="b3900-112">En Lync Server 2013, el archivado y la supervisión ya no tienen roles de servidor, pero los servicios integrados en el grupo front-end de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b3900-112">In Lync Server 2013, Archiving and Monitoring are no longer server roles, but services integrated into the Lync Server 2013 Front End pool.</span></span>

  - <span data-ttu-id="b3900-113">Durante el tiempo que coexistan las implementaciones heredadas de Lync Server 2013, la versión de Lync Server 2010 del servidor de archivado y el servidor de supervisión recopilan datos para los usuarios alojados en los grupos de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b3900-113">During the time that your legacy and Lync Server 2013 deployments coexist, the Lync Server 2010 version of Archiving Server and Monitoring Server gather data for users homed on Lync Server 2010 pools.</span></span> <span data-ttu-id="b3900-114">Archivado y supervisión en Lync Server 2013 recopilar datos para los usuarios alojados en los grupos de servidores de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b3900-114">Archiving and Monitoring in Lync Server 2013 gather data for users homed on Lync Server 2013 pools.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b3900-115">Durante la fase de migración, cuando aún está usando su servidor perimetral heredado con el nuevo grupo piloto de Lync Server 2013, la versión de Lync Server 2010 del servidor de archivado continúa recopilando datos para los usuarios alojados en los grupos de Lync Server 2010 y el archivado en Lync Server 2013 reúne datos para los usuarios alojados en los grupos de servidores de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b3900-115">During the phase of migration when you are still using your legacy Edge server with the new Lync Server 2013 pilot pool, the Lync Server 2010 version of Archiving Server continues to gather data for users homed on Lync Server 2010 pools and Archiving in Lync Server 2013 gathers data for users homed on Lync Server 2013 pools.</span></span>

    
    </div>

  - <span data-ttu-id="b3900-116">Si usa una solución de archivado y supervisión de terceros junto con el archivado y la supervisión en Lync Server 2013, consulte con su proveedor sobre cuándo y cómo necesita integrar la solución de terceros con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b3900-116">If you use a third-party archiving and monitoring solution in conjunction with Archiving and Monitoring in Lync Server 2013, consult with your vendor about when and how you need to integrate the third-party solution with Lync Server 2013.</span></span>

<span data-ttu-id="b3900-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3900-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

