---
title: Implementar una aplicación o servidor de sucursal con funciones de supervivencia - Tarea en el sitio de sucursal
description: Implementar una tarea de equipo de sucursal o de sitio de rama de servidor.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy a Survivable Branch Appliance or Server - branch site task
ms:assetid: 7989ba29-0419-46dd-892c-4ad3238afd56
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398599(v=OCS.15)
ms:contentKeyID: 48184586
ms.date: 10/29/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b84f603f185bd507111d4767a22e9009fc0e8b3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430255"
---
# <a name="deploy-a-survivable-branch-appliance-or-server-with-lync-server-2013---branch-site-task"></a><span data-ttu-id="e3821-103">Implementar una aplicación o servidor de sucursal con funciones de supervivencia con Lync Server 2013 - Tarea en el sitio de sucursal</span><span class="sxs-lookup"><span data-stu-id="e3821-103">Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e3821-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e3821-104">

<span> </span></span></span>

<span data-ttu-id="e3821-105">_**Última modificación del tema:** 2014-10-28_</span><span class="sxs-lookup"><span data-stu-id="e3821-105">_**Topic Last Modified:** 2014-10-28_</span></span>

<span data-ttu-id="e3821-106">Realice uno de los dos procedimientos descritos en este tema en el sitio de la sucursal, después de completar correctamente las tareas de [implementación de un equipo o servidor de sucursal con las tareas más Revivientes de Lync Server 2013-tareas del sitio central](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="e3821-106">Perform one of the two procedures described in this topic at the branch site, after successfully completing the tasks in [Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md).</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="e3821-107">Para llevar a cabo este procedimiento, debe ser miembro del grupo RTCUniversalSBATechnicians.</span><span class="sxs-lookup"><span data-stu-id="e3821-107">To perform this procedure, you must be a member of the RTCUniversalSBATechnicians group.</span></span>



</div>

<div>

## <a name="to-deploy-the-survivable-branch-appliance"></a><span data-ttu-id="e3821-108">Para implementar la aplicación de rama superviviente</span><span class="sxs-lookup"><span data-stu-id="e3821-108">To deploy the Survivable Branch Appliance</span></span>

  - <span data-ttu-id="e3821-109">El proveedor de equipos de sucursales con la que se ha habilitado la implementación de equipos con la supervivencia</span><span class="sxs-lookup"><span data-stu-id="e3821-109">Survivable Branch Appliance deployment is enabled by the Survivable Branch Appliance vendor through a web user interface (UI).</span></span> <span data-ttu-id="e3821-110">Para obtener información sobre la implementación de la aplicación de sucursales con la que es más reviviente, consulte la documentación del fabricante de su equipo.</span><span class="sxs-lookup"><span data-stu-id="e3821-110">For information about deploying the Survivable Branch Appliance, see your Survivable Branch Appliance vendor documentation.</span></span>

</div>

<div>

## <a name="to-deploy-the-survivable-branch-server"></a><span data-ttu-id="e3821-111">Para implementar el servidor de sucursal con la supervivencia</span><span class="sxs-lookup"><span data-stu-id="e3821-111">To deploy the Survivable Branch Server</span></span>

  - <span data-ttu-id="e3821-112">Instale Lync Server 2013 en un equipo con Windows Server 2008 R2, Windows Server 2012 o Windows Server 2012 R2, de la misma manera en que se instala cualquier otro rol de servidor de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e3821-112">Install Lync Server 2013 on a computer running Windows Server 2008 R2, Windows Server 2012, or Windows Server 2012 R2, just as you would install any other Lync Server 2013 server role.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="e3821-113">Para obtener información acerca de la instalación de Lync Server, consulte <A href="lync-server-2013-deploying-lync-server.md">implementar Lync server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="e3821-113">For information about installing Lync Server, see <A href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    </div>

<span data-ttu-id="e3821-114">**Siguiente paso**: [configuración de usuarios para la resistencia de sitios de sucursal en Lync Server 2013](lync-server-2013-configuring-users-for-branch-site-resiliency.md)</span><span class="sxs-lookup"><span data-stu-id="e3821-114">**Next step**: [Configuring users for branch site resiliency in Lync Server 2013](lync-server-2013-configuring-users-for-branch-site-resiliency.md)</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e3821-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3821-115">See Also</span></span>


[<span data-ttu-id="e3821-116">Apéndice A: Usar cmdlets para implementar una aplicación de sucursal con funciones de supervivencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e3821-116">Appendix A: Using cmdlets to deploy a Survivable Branch Appliance in Lync Server 2013</span></span>](lync-server-2013-appendix-a-using-cmdlets-to-deploy-a-survivable-branch-appliance.md)  
  

<span data-ttu-id="e3821-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e3821-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

