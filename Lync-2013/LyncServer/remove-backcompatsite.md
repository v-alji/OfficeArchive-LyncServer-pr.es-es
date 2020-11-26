---
title: Quitar BackCompatSite
description: Quitar BackCompatSite.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove BackCompatSite
ms:assetid: 039650e3-541b-45c2-a682-c4fa08423118
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204637(v=OCS.15)
ms:contentKeyID: 48183265
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 809324320ec1869ac0c9d324b8fc270a3cf8f174
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440304"
---
# <a name="remove-backcompatsite"></a><span data-ttu-id="eec13-103">Quitar BackCompatSite</span><span class="sxs-lookup"><span data-stu-id="eec13-103">Remove BackCompatSite</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eec13-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eec13-104">

<span> </span></span></span>

<span data-ttu-id="eec13-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="eec13-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="eec13-106">Una vez desactivados todos los grupos y todos los servidores perimetrales se han desinstalado, ejecute el Asistente para combinar el generador de topología para quitar el **BackCompatSite**.</span><span class="sxs-lookup"><span data-stu-id="eec13-106">After all pools are deactivated and all Edge Servers have been uninstalled, run the Topology Builder Merge wizard to remove the **BackCompatSite**.</span></span>

<div>

## <a name="to-remove-backcompat-site-from-topology-builder"></a><span data-ttu-id="eec13-107">Para quitar el sitio de BackCompat del generador de topología</span><span class="sxs-lookup"><span data-stu-id="eec13-107">To remove BackCompat site from Topology Builder</span></span>

1.  <span data-ttu-id="eec13-108">Abra una implementación existente desde el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="eec13-108">Open an existing deployment from Topology Builder.</span></span>

2.  <span data-ttu-id="eec13-109">En el menú **acción** , haga clic en **fusionar topología R2 de 2007**.</span><span class="sxs-lookup"><span data-stu-id="eec13-109">In the **Action** menu, click **Merge 2007 R2 Topology**.</span></span>

3.  <span data-ttu-id="eec13-110">Haga clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="eec13-110">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="eec13-111">En la página **especificar borde heredado** , asegúrese de que la lista de servidores perimetrales esté vacía.</span><span class="sxs-lookup"><span data-stu-id="eec13-111">On the **Specify Legacy Edge** page, ensure that list of Edge Servers is empty.</span></span> <span data-ttu-id="eec13-112">Si la lista no está vacía, use el botón **quitar** para quitar todos los servidores perimetrales heredados y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="eec13-112">If the list is not empty, use the **Remove** button to remove all the legacy Edge Servers, and then click **Next**.</span></span>
    
    <span data-ttu-id="eec13-113">![Asistente para combinar topología, especificar página de configuración de Edge](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Asistente para combinar topología, especificar página de configuración de Edge")</span><span class="sxs-lookup"><span data-stu-id="eec13-113">![Merge Topology Wizard, Specify Edge Setup page](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Merge Topology Wizard, Specify Edge Setup page")</span></span>  

5.  <span data-ttu-id="eec13-114">En la página **especificar la configuración interna del puerto SIP** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="eec13-114">On the **Specify Internal SIP port setting** page, click **Next**.</span></span>

6.  <span data-ttu-id="eec13-115">En la página **Resumen** , haga clic en **siguiente** para empezar a combinar las topologías para quitar el sitio heredado.</span><span class="sxs-lookup"><span data-stu-id="eec13-115">On the **Summary** page, click **Next** to begin merging the topologies to remove the legacy site.</span></span>

7.  <span data-ttu-id="eec13-116">En la columna **Estado** , compruebe que el valor es **correcto** y, a continuación, haga clic en **Finalizar** para cerrar el asistente.</span><span class="sxs-lookup"><span data-stu-id="eec13-116">In the **Status** column, verify that the value is **Success** and then click **Finish** to close the wizard.</span></span>

8.  <span data-ttu-id="eec13-117">En el panel izquierdo del generador de topologías, expanda el BackCompatSite y asegúrese de que no hay servidores en la lista.</span><span class="sxs-lookup"><span data-stu-id="eec13-117">In the left pane of Topology Builder, expand the BackCompatSite and ensure no servers are listed.</span></span>

9.  <span data-ttu-id="eec13-118">Haga clic con el botón secundario en el **BackCompatSite** y luego haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="eec13-118">Right-click the **BackCompatSite**, and then click **Delete**.</span></span>

10. <span data-ttu-id="eec13-119">En el **generador de topologías**, seleccione el nodo de nivel superior de **Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="eec13-119">In **Topology Builder**, select the top-most node **Lync Server**.</span></span>

11. <span data-ttu-id="eec13-120">En el menú **acción** , seleccione **publicar topología** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="eec13-120">From the **Action** menu, select **Publish Topology** and then click **Next**.</span></span>

12. <span data-ttu-id="eec13-121">Cuando finalice el Asistente para la **publicación** , haga clic en **Finalizar** para cerrar el asistente.</span><span class="sxs-lookup"><span data-stu-id="eec13-121">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

<span data-ttu-id="eec13-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eec13-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

