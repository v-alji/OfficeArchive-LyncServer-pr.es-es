---
title: 'Lync Server 2013: Implementación de grupos front-end emparejados para recuperación ante desastres'
description: 'Lync Server 2013: implementar grupos front-end emparejados para recuperación ante desastres.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying paired Front End pools for disaster recovery
ms:assetid: 2f12467c-8b90-43e6-831b-a0b096427f17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204773(v=OCS.15)
ms:contentKeyID: 48183727
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4846121f301d2bc7be1af9b58f0a0fef3f88e6d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429825"
---
# <a name="deploying-paired-front-end-pools-for-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="d2531-103">Implementación de grupos front-end emparejados para recuperación ante desastres en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d2531-103">Deploying paired Front End pools for disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d2531-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d2531-104">

<span> </span></span></span>

<span data-ttu-id="d2531-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="d2531-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="d2531-106">Puede implementar fácilmente la topología de recuperación ante desastres de las agrupaciones de front-end emparejadas con el generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="d2531-106">You can easily deploy the disaster recovery topology of paired Front End pools using Topology Builder.</span></span>

<div>

## <a name="to-deploy-a-pair-of-front-end-pools"></a><span data-ttu-id="d2531-107">Para implementar un par de grupos de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="d2531-107">To deploy a pair of Front End pools</span></span>

1.  <span data-ttu-id="d2531-108">Si los grupos son nuevos y aún no se han definido, use el generador de topología para crear los grupos.</span><span class="sxs-lookup"><span data-stu-id="d2531-108">If the pools are new and not yet defined, use Topology Builder to create the pools.</span></span>

2.  <span data-ttu-id="d2531-109">En el generador de topología, haga clic con el botón secundario en uno de los dos grupos y, a continuación, haga clic en **Editar propiedades**.</span><span class="sxs-lookup"><span data-stu-id="d2531-109">In Topology Builder, right-click one of the two pools, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="d2531-110">Haga clic en **Resistencia** en el panel izquierdo y, a continuación, seleccione **Grupo de servidores de copia de seguridad asociado** en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="d2531-110">Click **Resiliency** in the left pane, and then select **Associated Backup Pool** in the right pane.</span></span>

4.  <span data-ttu-id="d2531-p101">En el cuadro de debajo de **Grupo de servidores de copia de seguridad asociado**, seleccione el grupo que desea emparejar con este grupo. Solo los grupos existentes que aún no están emparejados con otro grupo estarán disponibles para su selección.</span><span class="sxs-lookup"><span data-stu-id="d2531-p101">In the box below **Associated Backup Pool**, select the pool that you want to pair with this pool. Only existing pools that are not already paired with another pool will be available to select from.</span></span>
    
    <span data-ttu-id="d2531-113">![36080581-db76-497d-bf9e-f02b39574d0e](images/JJ204773.36080581-db76-497d-bf9e-f02b39574d0e(OCS.15).png "36080581-db76-497d-bf9e-f02b39574d0e")</span><span class="sxs-lookup"><span data-stu-id="d2531-113">![36080581-db76-497d-bf9e-f02b39574d0e](images/JJ204773.36080581-db76-497d-bf9e-f02b39574d0e(OCS.15).png "36080581-db76-497d-bf9e-f02b39574d0e")</span></span>  

5.  <span data-ttu-id="d2531-114">Seleccione **Conmutación por error y conmutación por recuperación automática para voz** y después haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d2531-114">Select **Automatic failover and failback for Voice**, and then click **OK**.</span></span>
    
    <span data-ttu-id="d2531-115">Cuando vea los detalles de este grupo, el grupo asociado aparecerá en el panel derecho debajo de **Resistencia**. </span><span class="sxs-lookup"><span data-stu-id="d2531-115">When you view the details about this pool, the associated pool now appears in the right pane under **Resiliency**.</span></span>

6.  <span data-ttu-id="d2531-116">Use el generador de topología para publicar la topología.</span><span class="sxs-lookup"><span data-stu-id="d2531-116">Use Topology Builder to publish the topology.</span></span>

7.  <span data-ttu-id="d2531-p102">Si los dos grupos aún no se han implementado, impleméntelos ahora y se completará la configuración. Puede omitir los dos últimos pasos de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="d2531-p102">If the two pools were not yet deployed, deploy them now and the configuration will be complete. You can skip the final two steps in this procedure.</span></span>
    
    <span data-ttu-id="d2531-119">Sin embargo, si ya se implementaron los grupos antes de definir la relación emparejada, debe completar los dos pasos finales siguientes.</span><span class="sxs-lookup"><span data-stu-id="d2531-119">However, if the pools were already deployed before you defined the paired relationship, you must complete the following two final steps.</span></span>

8.  <span data-ttu-id="d2531-120">En cada servidor front-end de ambos grupos, ejecute lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d2531-120">On every Front End Server in both pools, run the following:</span></span>
    ```console
    <system drive>\Program Files\Microsoft Lync Server 2013\Deployment\Bootstrapper.exe 
    ```
    <span data-ttu-id="d2531-121">Esto configura otros servicios necesarios para que el emparejamiento de copia de seguridad funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="d2531-121">This configures other services required for backup pairing to work correctly.</span></span>

9.  <span data-ttu-id="d2531-122">Desde un símbolo del sistema del shell de administración de Lync Server, ejecute lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d2531-122">From a Lync Server Management Shell command prompt, run the following:</span></span>
    ```powershell
    Start-CsWindowsService -Name LYNCBACKUP
    ```
10. <span data-ttu-id="d2531-123">Haga que los datos de conferencia y usuarios de ambos grupos de servidores se sincronicen entre sí, con los siguientes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d2531-123">Force the user and conference data of both pools to be synchronized with each other, with the following cmdlets:</span></span>
    
       ```powershell
        Invoke-CsBackupServiceSync -PoolFqdn <Pool1 FQDN>
       ```
    
       ```powershell
        Invoke-CsBackupServiceSync -PoolFqdn <Pool2 FQDN>
       ```
    
    <span data-ttu-id="d2531-p103">La sincronización de datos podría llevar unos minutos. Puede utilizar los siguientes cmdlets para ver el estado. Asegúrese de que el estado de ambas direcciones sea parejo</span><span class="sxs-lookup"><span data-stu-id="d2531-p103">Synchronizing the data may take some time. You can use the following cmdlets to check the status. Make sure that the status in both directions is in steady state.</span></span>
    
       ```powershell
        Get-CsBackupServiceStatus -PoolFqdn <Pool1 FQDN>
       ```
    
       ```powershell
        Get-CsBackupServiceStatus -PoolFqdn <Pool2 FQDN>
       ```

<div class="">


> [!NOTE]  
> <span data-ttu-id="d2531-127">El <STRONG>failover automático y el failback para la opción de voz</STRONG> y los intervalos de tiempo asociados en el generador de topología se aplican solo a las características de resistencia de voz que se introdujeron en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d2531-127">The <STRONG>Automatic failover and failback for Voice</STRONG> option and the associated time intervals in Topology Builder apply only to the voice resiliency features that were introduced in Lync Server 2010.</span></span> <span data-ttu-id="d2531-128">La selección de esta opción no implica que la conmutación por error de grupos de servidores tratada en este documento sea automática.</span><span class="sxs-lookup"><span data-stu-id="d2531-128">Selecting this option does not imply that the pool failover discussed in this document is automatic.</span></span> <span data-ttu-id="d2531-129">La conmutación por error y la conmutación por recuperación de los grupos de servidores siempre requieren que un administrador invoque manualmente los cmdlets de conmutación por error y de conmutación por recuperación, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d2531-129">Pool failover and failback always require an administrator to manually invoke the failover and failback cmdlets, respectively.</span></span>



<span data-ttu-id="d2531-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d2531-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

