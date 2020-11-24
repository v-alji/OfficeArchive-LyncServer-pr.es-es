---
title: Conecte el grupo de servidores piloto a los servidores perimetrales heredados
description: Conectar el grupo piloto a servidores perimetrales heredados.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Connect pilot pool to legacy Edge Servers
ms:assetid: c3b67220-5705-47f6-852e-415204f3626c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721875(v=OCS.15)
ms:contentKeyID: 49733808
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ede2256efabf561be6b3f99543437087cb5c3890
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398831"
---
# <a name="connect-pilot-pool-to-legacy-edge-servers"></a><span data-ttu-id="f5ace-103">Conecte el grupo de servidores piloto a los servidores perimetrales heredados</span><span class="sxs-lookup"><span data-stu-id="f5ace-103">Connect pilot pool to legacy Edge Servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f5ace-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f5ace-104">

<span> </span></span></span>

<span data-ttu-id="f5ace-105">_**Última modificación del tema:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="f5ace-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="f5ace-106">Después de implementar Lync Server 2013, debe configurar una ruta de Federación para el sitio.</span><span class="sxs-lookup"><span data-stu-id="f5ace-106">After deploying Lync Server 2013, you need to configure a federation route for your site.</span></span> <span data-ttu-id="f5ace-107">Para poder usar la ruta federada que está usando Lync Server 2010, Lync Server 2013 debe estar configurado para usar esta ruta.</span><span class="sxs-lookup"><span data-stu-id="f5ace-107">In order to use the federated route that is being used by Lync Server 2010, Lync Server 2013 must be configured to use this route.</span></span>

<span data-ttu-id="f5ace-108">Para habilitar el sitio de 2013 de Lync Server para que use el director y el servidor perimetral de la implementación de Lync Server 2010, use el generador de topología para asociar el grupo perimetral heredado.</span><span class="sxs-lookup"><span data-stu-id="f5ace-108">To enable the Lync Server 2013 site to use the Director and Edge Server of the Lync Server 2010 deployment, use Topology Builder to associate the legacy Edge pool.</span></span>

<div>

## <a name="to-associate-the-legacy-edge-pool-by-using-topology-builder"></a><span data-ttu-id="f5ace-109">Para asociar el grupo perimetral heredado mediante el generador de topología</span><span class="sxs-lookup"><span data-stu-id="f5ace-109">To associate the legacy Edge pool by using Topology Builder</span></span>

1.  <span data-ttu-id="f5ace-110">Abra el **generador de topologías**.</span><span class="sxs-lookup"><span data-stu-id="f5ace-110">Open **Topology Builder**.</span></span>

2.  <span data-ttu-id="f5ace-111">Seleccione su sitio, que se encuentra directamente debajo del nodo de **Lync Server** .</span><span class="sxs-lookup"><span data-stu-id="f5ace-111">Select your site, which is directly below the **Lync Server** node.</span></span>

3.  <span data-ttu-id="f5ace-112">En el menú **acciones** , haga clic en **Editar propiedades**.</span><span class="sxs-lookup"><span data-stu-id="f5ace-112">On the **Actions** menu, click **Edit Properties**.</span></span>

4.  <span data-ttu-id="f5ace-113">En el panel de la izquierda, seleccione **ruta de Federación**.</span><span class="sxs-lookup"><span data-stu-id="f5ace-113">In the left pane, select **Federation route**.</span></span>

5.  <span data-ttu-id="f5ace-114">En **asignación** de la ruta de Federación de sitios, seleccione **Habilitar Federación SIP** y, a continuación, seleccione el Director de Lync Server 2010 o el servidor perimetral de Lync Server 2010 si no se muestra ningún director.</span><span class="sxs-lookup"><span data-stu-id="f5ace-114">Under **Site federation route assignment**, select **Enable SIP federation**, and then select the Lync Server 2010 Director, or the Lync Server 2010 Edge Server if no Director is listed.</span></span>
    
    <span data-ttu-id="f5ace-115">![Editar propiedades, página de ruta de Federación](images/JJ721875.5f1d04c3-c724-426d-b27d-3fe89c6c5cfb(OCS.15).jpg "Editar propiedades, página de ruta de Federación")</span><span class="sxs-lookup"><span data-stu-id="f5ace-115">![Edit Properties, Federation route page](images/JJ721875.5f1d04c3-c724-426d-b27d-3fe89c6c5cfb(OCS.15).jpg "Edit Properties, Federation route page")</span></span>  

6.  <span data-ttu-id="f5ace-116">Haga clic en **Aceptar** para cerrar la página **Editar propiedades** .</span><span class="sxs-lookup"><span data-stu-id="f5ace-116">Click **OK** to close the **Edit Properties** page.</span></span>

7.  <span data-ttu-id="f5ace-117">En el generador de topologías, en el nodo de 2013 de Lync Server, vaya a los grupos de servidores **Standard Edition** o **Enterprise Edition**, haga clic con el botón secundario en el grupo y, a continuación, haga clic en **Editar propiedades**.</span><span class="sxs-lookup"><span data-stu-id="f5ace-117">In Topology Builder, under the Lync Server 2013 node, navigate to the **Standard Edition server** or **Enterprise Edition Front End pools**, right-click the pool, and then click **Edit Properties**.</span></span>

8.  <span data-ttu-id="f5ace-118">En **asociaciones**, active la casilla situada junto a **asociar grupo perimetral (para componentes multimedia)**.</span><span class="sxs-lookup"><span data-stu-id="f5ace-118">Under **Associations**, select the check box next to **Associate Edge pool (for media components)**.</span></span>

9.  <span data-ttu-id="f5ace-119">En la lista, seleccione el servidor perimetral heredado.</span><span class="sxs-lookup"><span data-stu-id="f5ace-119">From the list, select the legacy Edge Server.</span></span>
    
    <span data-ttu-id="f5ace-120">![Cuadro de diálogo Editar propiedades, selección del borde heredado](images/JJ721875.feae8156-540e-4804-bb0a-2b5736ec2900(OCS.15).jpg "Cuadro de diálogo Editar propiedades, selección del borde heredado")</span><span class="sxs-lookup"><span data-stu-id="f5ace-120">![Edit Properties dialog, selecting the legacy Edge](images/JJ721875.feae8156-540e-4804-bb0a-2b5736ec2900(OCS.15).jpg "Edit Properties dialog, selecting the legacy Edge")</span></span>  

10. <span data-ttu-id="f5ace-121">Haga clic en **Aceptar** para cerrar la página **Editar propiedades** .</span><span class="sxs-lookup"><span data-stu-id="f5ace-121">Click **OK** to close the **Edit Properties** page.</span></span>

11. <span data-ttu-id="f5ace-122">En el **generador de topologías**, seleccione el nodo de nivel superior, **Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="f5ace-122">In **Topology Builder**, select the top-most node, **Lync Server**.</span></span>

12. <span data-ttu-id="f5ace-123">En el menú **acción** , haga clic en **publicar topología** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f5ace-123">From the **Action** menu, click **Publish Topology**, and then click **Next**.</span></span>

13. <span data-ttu-id="f5ace-124">Cuando finalice el **Asistente para la publicación** , haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="f5ace-124">When the **Publishing wizard** completes, click **Finish**.</span></span>

<span data-ttu-id="f5ace-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f5ace-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

