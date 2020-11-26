---
title: 'Lync Server 2013: tareas diarias'
description: 'Lync Server 2013: tareas diarias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Daily tasks
ms:assetid: f7a5f99e-5d2b-445d-9ba1-cbfcfeff16ae
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720351(v=OCS.15)
ms:contentKeyID: 63969666
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9e2d62eb29db2bafa23565637bb655ba932c7b6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431319"
---
# <a name="daily-tasks-in-lync-server-2013"></a><span data-ttu-id="109be-103">Tareas diarias en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="109be-103">Daily tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="109be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="109be-104">

<span> </span></span></span>

<span data-ttu-id="109be-105">_**Última modificación del tema:** 2015-01-26_</span><span class="sxs-lookup"><span data-stu-id="109be-105">_**Topic Last Modified:** 2015-01-26_</span></span>

<span data-ttu-id="109be-106">Para garantizar la disponibilidad y la confiabilidad de la implementación de Lync Server 2013, debe formar parte de los elementos de prueba y de supervisión diaria que son muy importantes para el funcionamiento del sistema, lo que incluye la plataforma física, el sistema operativo y todos los servicios importantes de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="109be-106">To help ensure the availability and reliability of the Lync Server 2013 deployment, you should as part of daily routine monitor and test elements that are very important to the functioning of the system, which includes the physical platform, the operating system, and all important Lync Server 2013 services.</span></span> <span data-ttu-id="109be-107">El mantenimiento preventivo y la supervisión proactiva le ayudarán a identificar posibles errores y problemas que puedan afectar negativamente a la implementación de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="109be-107">Preventive maintenance and proactive monitoring will help you identify potential errors and issues that may adversely affect the Lync Server 2013 deployment.</span></span>

<span data-ttu-id="109be-108">La supervisión de la implementación de Lync Server 2013 implica comprobar si hay problemas con las conexiones, los servicios, los recursos del servidor y los recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="109be-108">Monitoring the Lync Server 2013 deployment involves checking for issues with connections, services, server resources, and system resources.</span></span> <span data-ttu-id="109be-109">Los sistemas operativos de Windows Server, junto con System Center Operations Manager, y Lync Server le ofrecen muchas herramientas y servicios de supervisión para ayudarle a garantizar que la organización de Lync Server funcione sin problemas.</span><span class="sxs-lookup"><span data-stu-id="109be-109">Windows Server operating systems, together with System Center Operations Manager, and Lync Server give you many monitoring tools and services to help ensure that the Lync Server organization is running smoothly.</span></span> <span data-ttu-id="109be-110">Cuando estas tecnologías se implementan juntas, los administradores pueden recibir alertas antes de que se produzca una incidencia.</span><span class="sxs-lookup"><span data-stu-id="109be-110">When these technologies are implemented together, administrators will be able to receive alerts when or before issues occur.</span></span>

<span data-ttu-id="109be-111">Las ventajas principales de la supervisión diaria son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="109be-111">The key advantages to daily monitoring are as follows:</span></span>

  - <span data-ttu-id="109be-112">Cumplimiento de los requisitos de rendimiento y disponibilidad de los contratos de nivel de servicio definidos.</span><span class="sxs-lookup"><span data-stu-id="109be-112">Meeting the performance and availability requirements of defined SLAs.</span></span>

  - <span data-ttu-id="109be-113">Correcta realización de tareas administrativas específicas, como las tareas diarias de copia de seguridad y la comprobación del estado de los servidores.</span><span class="sxs-lookup"><span data-stu-id="109be-113">Successfully completing specific administrative tasks, such as daily backup operations, and checking server health.</span></span>

  - <span data-ttu-id="109be-114">Detección y resolución de incidencias tales como cuellos de botella en el rendimiento del servidor, o determinación de la necesidad de contar con recursos adicionales antes de que la productividad se vea afectada.</span><span class="sxs-lookup"><span data-stu-id="109be-114">Detecting and addressing issues, such as bottlenecks in the server performance, or need for additional resources before they affect productivity.</span></span>

<span data-ttu-id="109be-115">Las tareas de mantenimiento diarias ayudan al equipo de administración a definir o establecer unos criterios o bases para la operación normal de los sistemas dentro de la organización, y a detectar cualquier actividad anormal.</span><span class="sxs-lookup"><span data-stu-id="109be-115">Daily maintenance tasks help the administrative team to define or establish a criteria or baseline for normal systems operations within the organization, and to detect any abnormal activity.</span></span> <span data-ttu-id="109be-116">Es importante implementar estas tareas de mantenimiento diario para que el equipo administrativo pueda capturar y mantener datos sobre la infraestructura de Lync Server 2013, por ejemplo, los niveles de uso, los posibles cuellos de botella de rendimiento y los cambios administrativos.</span><span class="sxs-lookup"><span data-stu-id="109be-116">It is important to implement these daily maintenance tasks so that the administrative team can capture and maintain data about the Lync Server 2013 infrastructure, such as usage levels, possible performance bottlenecks, and administrative changes.</span></span>

<span data-ttu-id="109be-117">Para organizar más fácilmente las tareas de rendimiento diarias, use la [lista de comprobación de tareas diarias](lync-server-2013-operations-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="109be-117">To help organize the performance of daily tasks, use the [Daily task checklist](lync-server-2013-operations-checklists.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="109be-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="109be-118">See Also</span></span>


[<span data-ttu-id="109be-119">Lista de comprobación de tareas diarias</span><span class="sxs-lookup"><span data-stu-id="109be-119">Daily task checklist</span></span>](lync-server-2013-operations-checklists.md)  
  

<span data-ttu-id="109be-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="109be-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

