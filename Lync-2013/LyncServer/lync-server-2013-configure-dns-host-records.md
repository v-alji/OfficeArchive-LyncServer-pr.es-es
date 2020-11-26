---
title: 'Lync Server 2013: Configurar registros de host DNS'
description: 'Lync Server 2013: configurar registros de host DNS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS Host records
ms:assetid: 78a1afcf-41c8-4da5-8740-c6570c19078c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398593(v=OCS.15)
ms:contentKeyID: 48184577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7fd403402d0d2f089d7fc92a62296a56df0cf2e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434042"
---
# <a name="configure-dns-host-records-for-lync-server-2013"></a><span data-ttu-id="a8d7e-103">Configurar registros de host DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8d7e-103">Configure DNS Host records for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8d7e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8d7e-104">

<span> </span></span></span>

<span data-ttu-id="a8d7e-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="a8d7e-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="a8d7e-106">Para completar correctamente este procedimiento, debe haber iniciado sesión en el servidor o dominio como mínimo como miembro del grupo administradores de dominio o miembro del grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-106">To successfully complete this procedure, you should be logged on to the server or domain at minimum as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<div>

## <a name="to-configure-dns-host-a-records"></a><span data-ttu-id="a8d7e-107">Para configurar registros A de host DNS</span><span class="sxs-lookup"><span data-stu-id="a8d7e-107">To configure DNS Host A records</span></span>

1.  <span data-ttu-id="a8d7e-108">En el servidor del sistema de nombres de dominio (DNS), haga clic en **Inicio**, en **herramientas administrativas** y, por último, en **DNS**.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-108">On the Domain Name System (DNS) server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="a8d7e-109">En el árbol de consola de su dominio, expanda **zonas de búsqueda directa** y haga clic con el botón secundario en el dominio en el que se instalará Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-109">In the console tree for your domain, expand **Forward Lookup Zones**, and then right-click the domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="a8d7e-110">Haga clic en **nuevo host (A o aaaa)**.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-110">Click **New Host (A or AAAA)**.</span></span>

4.  <span data-ttu-id="a8d7e-111">Haga clic en **nombre**, escriba el nombre de host del grupo (el nombre de dominio se supone de la zona en la que está definido el registro y no tiene que especificarse como parte del registro A).</span><span class="sxs-lookup"><span data-stu-id="a8d7e-111">Click **Name**, type the host name for the pool (the domain name is assumed from the zone that the record is defined in and does not need to be entered as part of the A record).</span></span>

5.  <span data-ttu-id="a8d7e-112">Haga clic en **dirección IP**, escriba la IP virtual (VIP) del equilibrador de carga para el grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-112">Click **IP Address**, type the virtual IP (VIP) of the load balancer for the Front End pool.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="a8d7e-113">En las implementaciones que usan un grupo de directores, los registros de host (A) para las direcciones URL simples deben señalar a la dirección VIP del equilibrador de carga de director.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-113">In deployments that use a Director pool, the host (A) records for the simple URLs should point to the VIP of the Director load balancer.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a8d7e-114">Si implementa solo un servidor Enterprise Edition o director que está conectado a la topología sin un equilibrador de carga, o si implementa un servidor Standard Edition, escriba la dirección IP del servidor Enterprise Edition, servidor Standard Edition o director.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-114">If you deploy only one Enterprise Edition server or Director that is connected to the topology without a load balancer, or if you deploy a Standard Edition server, type the IP address of the Enterprise Edition server, Standard Edition server, or Director.</span></span> <span data-ttu-id="a8d7e-115">Es necesario un equilibrador de carga si implementa más de un servidor Enterprise Edition o Director en un grupo.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-115">A load balancer is required if you deploy more than one Enterprise Edition server or Director in a pool.</span></span> <span data-ttu-id="a8d7e-116">Los equilibradores de carga no se usan con servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-116">Load balancers are not used with Standard Edition servers.</span></span>

    
    </div>

6.  <span data-ttu-id="a8d7e-117">Haga clic en **Agregar host** y, a continuación, en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-117">Click **Add Host**, and then click **OK**.</span></span>

7.  <span data-ttu-id="a8d7e-118">Para crear un registro A adicional, repita los pasos 4 y 5.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-118">To create an additional A record, repeat steps 4 and 5.</span></span>

8.  <span data-ttu-id="a8d7e-119">Cuando haya terminado de crear todos los registros A que necesita, haga clic en **listo**.</span><span class="sxs-lookup"><span data-stu-id="a8d7e-119">When you are finished creating all the A records that you need, click **Done**.</span></span>

<span data-ttu-id="a8d7e-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8d7e-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

