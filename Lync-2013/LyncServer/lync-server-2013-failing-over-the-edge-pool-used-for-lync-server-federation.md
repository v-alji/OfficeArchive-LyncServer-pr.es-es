---
title: 'Lync Server 2013: Conmutación por error para el grupo de servidores perimetrales usado para la federación Lync Server'
description: 'Lync Server 2013: error en el grupo perimetral usado para la Federación de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over the Edge pool used for Lync Server federation
ms:assetid: 5c9da0f2-7429-40bb-bb3c-5cc4ecb5a13d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688071(v=OCS.15)
ms:contentKeyID: 49733665
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1e7e13ccd35a653d38174f55ace9dc6637ded04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398471"
---
# <a name="failing-over-the-edge-pool-used-for-lync-server-federation-in-lync-server-2013"></a><span data-ttu-id="6f3cd-103">Conmutación por error para el grupo de servidores perimetrales usado para la federación Lync Server en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f3cd-103">Failing over the Edge pool used for Lync Server federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f3cd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f3cd-104">

<span> </span></span></span>

<span data-ttu-id="6f3cd-105">_**Última modificación del tema:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="6f3cd-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="6f3cd-106">Si el grupo perimetral donde tiene la Federación de Lync Server configurada, debe cambiar la Federación para usar un grupo de borde diferente para que la Federación funcione.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-106">If the Edge pool where you have Lync Server federation configured goes down, you must change federation to use a different Edge pool for federation to work.</span></span>

<div>

## <a name="failing-over-the-edge-pool-used-for-lync-server-federation"></a><span data-ttu-id="6f3cd-107">Conmutación por error del grupo perimetral usado para la Federación de Lync Server</span><span class="sxs-lookup"><span data-stu-id="6f3cd-107">Failing Over the Edge Pool Used for Lync Server Federation</span></span>

1.  <span data-ttu-id="6f3cd-108">En un servidor front-end, abra Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-108">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="6f3cd-109">Expanda **agrupaciones perimetrales** y haga clic con el botón secundario en el servidor perimetral o en el grupo de servidores perimetrales actualmente configurados para la Federación.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-109">Expand **Edge pools**, then right click the Edge server or Edge server pool that is currently configured for Federation.</span></span> <span data-ttu-id="6f3cd-110">Seleccione **Editar propiedades**.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-110">Select **Edit properties**.</span></span>

2.  <span data-ttu-id="6f3cd-111">En **Editar propiedades** , en **General**, desactive **Habilitar Federación para este grupo perimetral (puerto 5061)**.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-111">In **Edit Properties** under **General**, clear **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="6f3cd-112">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-112">Click **OK**.</span></span>

3.  <span data-ttu-id="6f3cd-113">Expanda **agrupaciones perimetrales** y haga clic con el botón secundario en el grupo de servidores perimetrales o perimetrales que desea usar para la Federación.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-113">Expand **Edge pools**, then right click the Edge server or Edge server pool that you now want to use for Federation.</span></span> <span data-ttu-id="6f3cd-114">Seleccione **Editar propiedades**.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-114">Select **Edit properties**.</span></span>

4.  <span data-ttu-id="6f3cd-115">En **propiedades de edición** , en **General**, seleccione **Habilitar Federación para este grupo perimetral (puerto 5061)**.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-115">In **Edit Properties** under **General**, select **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="6f3cd-116">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-116">Click **OK**.</span></span>

5.  <span data-ttu-id="6f3cd-117">Haga clic en **acción**, seleccione **topología**, seleccione **publicar**.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-117">Click **Action**, select **Topology**, select **Publish**.</span></span> <span data-ttu-id="6f3cd-118">Cuando se le solicite al **publicar la topología**, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-118">When prompted on **Publish the topology**, click **Next**.</span></span> <span data-ttu-id="6f3cd-119">Una vez finalizada la publicación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-119">When the Publish is finished, click **Finish**.</span></span>

6.  <span data-ttu-id="6f3cd-120">En el servidor perimetral, abra el Asistente para la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="6f3cd-121">Haga clic en **instalar o actualizar el sistema Lync Server** y, a continuación, haga clic en **configurar o quitar los componentes de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-121">Click **Install or Update Lync Server System**, then click **Setup or Remove Lync Server Components**.</span></span> <span data-ttu-id="6f3cd-122">**Vuelva a** hacer clic en ejecutar.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-122">Click **Run Again**.</span></span>

7.  <span data-ttu-id="6f3cd-123">En instalación de los componentes de Lync Server, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-123">At Setup Lync Server components, click **Next**.</span></span> <span data-ttu-id="6f3cd-124">La pantalla resumen mostrará las acciones a medida que se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="6f3cd-125">Una vez que haya finalizado la implementación, haga clic en **Ver registro** para ver los archivos de registro disponibles.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-125">Once the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="6f3cd-126">Haga clic en **Finalizar** para completar la implementación.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-126">Click **Finish** to complete the deployment.</span></span>
    
    <span data-ttu-id="6f3cd-127">Si el sitio que contiene el grupo perimetral con error contiene servidores front-end que aún se están ejecutando, debe actualizar el servicio de conferencias web y el servicio de conferencia A/V en estos grupos front-end para usar un grupo perimetral en un sitio remoto que aún se esté ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6f3cd-127">If the site containing the failed Edge pool contains Front End Servers that are still running, you must update the Web Conferencing Service and A/V Conferencing Service on these Front End pools to use an Edge pool in a remote site that is still running.</span></span> <span data-ttu-id="6f3cd-128">Para obtener más información, vea [cambiar el grupo perimetral asociado a un grupo de servidores front-end en Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span><span class="sxs-lookup"><span data-stu-id="6f3cd-128">For more information, see [Changing the Edge pool associated with a Front End pool in Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6f3cd-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f3cd-129">See Also</span></span>


[<span data-ttu-id="6f3cd-130">Conmutación por error para el grupo de servidores perimetrales para la federación XMPP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f3cd-130">Failing over the Edge pool used for XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md)  
[<span data-ttu-id="6f3cd-131">Conmutación por recuperación para el grupo de servidores perimetrales que se usa para la federación Lync Server o la federación XMPP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f3cd-131">Failing back the Edge pool used for Lync Server federation or XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-back-the-edge-pool-used-for-lync-server-federation-or-xmpp-federation.md)  


[<span data-ttu-id="6f3cd-132">Recuperación ante desastres del servidor perimetral en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f3cd-132">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)  
  

<span data-ttu-id="6f3cd-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f3cd-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

