---
title: Configurar registros DNS para una implementación de grupo de servidores piloto
description: Configure los registros DNS para la implementación del grupo piloto.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS records for pilot pool deployment
ms:assetid: eb421bad-4bf1-4837-a077-7795094692d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721921(v=OCS.15)
ms:contentKeyID: 49733855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e41e163432ba910f6d083cc508e8ad8c9f2006d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398873"
---
# <a name="configure-dns-records-for-pilot-pool-deployment"></a><span data-ttu-id="dfa50-103">Configurar registros DNS para una implementación de grupo de servidores piloto</span><span class="sxs-lookup"><span data-stu-id="dfa50-103">Configure DNS records for pilot pool deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dfa50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dfa50-104">

<span> </span></span></span>

<span data-ttu-id="dfa50-105">_**Última modificación del tema:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="dfa50-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="dfa50-106">Antes de implementar el grupo piloto de Lync Server 2013, debe actualizar las entradas de host DNS A para la agrupación piloto.</span><span class="sxs-lookup"><span data-stu-id="dfa50-106">Prior to deploying the Lync Server 2013 pilot pool, you must update the DNS Host A entries for the pilot pool.</span></span> <span data-ttu-id="dfa50-107">Para completar correctamente este procedimiento, debe haber iniciado sesión en el servidor o dominio como miembro del grupo administradores de dominio o miembro del grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="dfa50-107">To successfully complete this procedure, you should be logged on to the server or domain as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="dfa50-108">**Para configurar registros A de host DNS**</span><span class="sxs-lookup"><span data-stu-id="dfa50-108">**To configure DNS Host A records**</span></span>

1.  <span data-ttu-id="dfa50-109">En el servidor del sistema de nombres de dominio (DNS), haga clic en **Inicio**, en **herramientas administrativas** y, por último, en **DNS**.</span><span class="sxs-lookup"><span data-stu-id="dfa50-109">On the Domain Name System (DNS) server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="dfa50-110">En el árbol de consola de su dominio, expanda **zonas de búsqueda directa** y haga clic con el botón secundario en el dominio en el que se instalará Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dfa50-110">In the console tree for your domain, expand **Forward Lookup Zones**, and then right-click the domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="dfa50-111">Haga clic en **nuevo host (A o aaaa)**.</span><span class="sxs-lookup"><span data-stu-id="dfa50-111">Click **New Host (A or AAAA)**.</span></span>

4.  <span data-ttu-id="dfa50-112">Haga clic en **nombre**, escriba el nombre de host para el grupo de servidores de Lync Server 2013 (el nombre de dominio se supone de la zona en la que está definido el registro y no tiene que especificarse como parte del registro A).</span><span class="sxs-lookup"><span data-stu-id="dfa50-112">Click **Name**, type the host name for the Lync Server 2013 pool (the domain name is assumed from the zone that the record is defined in and does not need to be entered as part of the A record).</span></span>

5.  <span data-ttu-id="dfa50-113">Haga clic en **dirección IP** y escriba la dirección IP del grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="dfa50-113">Click **IP Address**, type the IP address for the Front End pool.</span></span>

6.  <span data-ttu-id="dfa50-114">Haga clic en **Agregar host** y, a continuación, en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="dfa50-114">Click **Add Host**, and then click **OK**.</span></span>

7.  <span data-ttu-id="dfa50-115">Cuando haya terminado, haga clic en **listo**.</span><span class="sxs-lookup"><span data-stu-id="dfa50-115">When you are finished, click **Done**.</span></span>

<span data-ttu-id="dfa50-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dfa50-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

