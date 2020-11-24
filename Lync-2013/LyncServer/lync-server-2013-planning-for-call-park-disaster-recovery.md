---
title: 'Lync Server 2013: Planear la recuperación ante desastres del estacionamiento de llamadas'
description: 'Lync Server 2013: planificación de recuperación ante desastres de estacionamiento de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Call Park disaster recovery
ms:assetid: f7cf3958-177b-4340-a864-35a6f44d6d88
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205395(v=OCS.15)
ms:contentKeyID: 48185867
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1d05503f1d8c30f4dd4446a995442d5e2500dbc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397895"
---
# <a name="planning-for-call-park-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="f752c-103">Planear la recuperación ante desastres del estacionamiento de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f752c-103">Planning for Call Park disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f752c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f752c-104">

<span> </span></span></span>

<span data-ttu-id="f752c-105">_**Última modificación del tema:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="f752c-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="f752c-106">En esta sección se describen algunas formas de preparar la aplicación de estacionamiento de llamadas para la recuperación ante desastres y algunas consideraciones para el proceso de recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="f752c-106">This section describes some ways to prepare the Call Park application for disaster recovery and some considerations for the disaster recovery process.</span></span>

<div>

## <a name="preparing-for-call-park-disaster-recovery"></a><span data-ttu-id="f752c-107">Preparación de la recuperación ante desastres de estacionamiento de llamadas</span><span class="sxs-lookup"><span data-stu-id="f752c-107">Preparing for Call Park Disaster Recovery</span></span>

<span data-ttu-id="f752c-108">Tenga en cuenta lo siguiente cuando prepare y lleve a cabo procedimientos de recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="f752c-108">Keep the following in mind when preparing for and carrying out disaster recovery procedures.</span></span>

  - <span data-ttu-id="f752c-109">Planee la recuperación de desastres cuando realice su plan de capacidad.</span><span class="sxs-lookup"><span data-stu-id="f752c-109">Plan for disaster recovery when you do your capacity planning.</span></span> <span data-ttu-id="f752c-110">Para la capacidad de recuperación ante desastres, cada grupo de un grupo emparejado debe poder administrar las cargas de trabajo de los servicios de estacionamiento de llamadas en ambos grupos.</span><span class="sxs-lookup"><span data-stu-id="f752c-110">For disaster recovery capacity, each pool in a paired pool should be able to handle the workloads of the Call Park services in both pools.</span></span> <span data-ttu-id="f752c-111">Para obtener más información sobre la planeación de la capacidad de estacionamiento de llamadas, consulte [planificación de la capacidad de estacionamiento de llamadas en Lync Server 2013](lync-server-2013-capacity-planning-for-call-park.md).</span><span class="sxs-lookup"><span data-stu-id="f752c-111">For details about Call Park capacity planning, see [Capacity planning for Call Park in Lync Server 2013](lync-server-2013-capacity-planning-for-call-park.md).</span></span>

  - <span data-ttu-id="f752c-112">Durante la recuperación de desastres, los usuarios que se han redirigido al grupo de copia de seguridad como parte del proceso de conmutación por error usan el servicio de estacionamiento de llamadas que se ejecuta en el grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f752c-112">During disaster recovery, users who have been redirected to the backup pool as part of the failover process use the Call Park service running in the backup pool.</span></span> <span data-ttu-id="f752c-113">Por lo tanto, la compatibilidad con el parque de llamadas durante la recuperación de desastres requiere que la aplicación de estacionamiento de llamadas se implemente y se habilite en el grupo primario y en el grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f752c-113">Therefore, support for Call Park during disaster recovery requires the Call Park application to be deployed and enabled in both the primary pool and the backup pool.</span></span>

  - <span data-ttu-id="f752c-114">Cada grupo debe tener un intervalo válido de números de órbita para los usuarios que estén alojados en ese grupo para usarlos en las llamadas de aparcamiento.</span><span class="sxs-lookup"><span data-stu-id="f752c-114">Each pool must have a valid range of orbit numbers for users who are homed in that pool to use for parking calls.</span></span>

  - <span data-ttu-id="f752c-115">Mantenga siempre una copia de seguridad separada de cualquier música personalizada en espera que se haya cargado para el parque de llamadas.</span><span class="sxs-lookup"><span data-stu-id="f752c-115">Always keep a separate backup copy of any customized music on hold that has been uploaded for Call Park.</span></span> <span data-ttu-id="f752c-116">No se realiza una copia de seguridad de estos archivos como parte del proceso de recuperación de desastres de Lync Server 2013 y se perderán si los archivos cargados en el grupo están dañados, están dañados o se hayan borrado.</span><span class="sxs-lookup"><span data-stu-id="f752c-116">These files are not backed up as part of the Lync Server 2013 disaster recovery process and will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span>

</div>

<div>

## <a name="call-park-disaster-recovery-considerations"></a><span data-ttu-id="f752c-117">Consideraciones de recuperación ante desastres de estacionamiento de llamadas</span><span class="sxs-lookup"><span data-stu-id="f752c-117">Call Park Disaster Recovery Considerations</span></span>

<span data-ttu-id="f752c-118">Solo puede definir un conjunto de parámetros de configuración de la aplicación de estacionamiento de llamadas y un archivo de audio de música en espera personalizado por grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="f752c-118">You can define only one set of Call Park application configuration settings and one customized music-on-hold audio file per pool.</span></span> <span data-ttu-id="f752c-119">Esta configuración incluye el umbral de tiempo de espera, la música en espera, los intentos de recogida máxima de llamadas y el URI de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="f752c-119">These settings include the timeout threshold, music on hold, maximum call pickup attempts, and timeout URI.</span></span> <span data-ttu-id="f752c-120">Para ver estas opciones de configuración, ejecute el cmdlet **Get-CsCpsConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f752c-120">To view these configuration settings, run the **Get-CsCpsConfiguration** cmdlet.</span></span> <span data-ttu-id="f752c-121">Para obtener más información sobre el cmdlet **Get-CsCpsConfiguration** , vea [Get-CsCpsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCpsConfiguration).</span><span class="sxs-lookup"><span data-stu-id="f752c-121">For details about the **Get-CsCpsConfiguration** cmdlet, see [Get-CsCpsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCpsConfiguration).</span></span>

<span data-ttu-id="f752c-122">Durante la recuperación de desastres, el parque de llamadas usa la aplicación de estacionamiento de llamadas del grupo de copia de seguridad, por lo que no se realiza una copia de seguridad de la configuración del grupo principal.</span><span class="sxs-lookup"><span data-stu-id="f752c-122">During disaster recovery, Call Park uses the Call Park application in the backup pool, so settings in the primary pool are not backed up.</span></span> <span data-ttu-id="f752c-123">Si el repositorio principal no se puede recuperar e implementa un nuevo grupo para reemplazar el grupo primario, se perderán las opciones de configuración del grupo principal y tendrá que volver a configurar la configuración de la suspensión de llamada y los archivos de audio de música activada en el nuevo grupo.</span><span class="sxs-lookup"><span data-stu-id="f752c-123">If the primary pool can't be recovered and you deploy a new pool to replace the primary pool, the settings from the primary pool are lost, and you need to reconfigure the Call Park settings and any customized music-on-hold audio files in the new pool.</span></span>

<span data-ttu-id="f752c-124">Si implementa un nuevo grupo de servidores con un nombre de dominio completo (FQDN) diferente para reemplazar el grupo primario, tendrá que reasignar todos los intervalos de órbita del parque de llamadas asociados con el grupo primario al FQDN del nuevo grupo.</span><span class="sxs-lookup"><span data-stu-id="f752c-124">If you deploy a new pool with a different fully qualified domain name (FQDN) to replace the primary pool, you need to reassign all the Call Park orbit ranges that were associated with the primary pool to the FQDN of the new pool.</span></span> <span data-ttu-id="f752c-125">Para reasignar intervalos orbitales al nuevo grupo, puede usar el panel de control de Lync Server o el cmdlet **set-CsCallParkOrbit** .</span><span class="sxs-lookup"><span data-stu-id="f752c-125">To reassign orbit ranges to the new pool, you can use either Lync Server Control Panel or the **Set-CsCallParkOrbit** cmdlet.</span></span> <span data-ttu-id="f752c-126">Para obtener más información sobre el cmdlet **set-CsCallParkOrbit** , consulte [set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span><span class="sxs-lookup"><span data-stu-id="f752c-126">For details about the **Set-CsCallParkOrbit** cmdlet, see [Set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span></span>

<span data-ttu-id="f752c-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f752c-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

