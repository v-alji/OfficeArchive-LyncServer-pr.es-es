---
title: La comprobación de la replicación de usuarios ha finalizado
description: Comprobar que la replicación de usuario ha finalizado.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify user replication has completed
ms:assetid: 119e9896-45e5-4f8b-af43-7b09360ada0b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204680(v=OCS.15)
ms:contentKeyID: 48183441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 60bca44fcce811c29b1633bd4d3a39f832851885
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446075"
---
# <a name="verify-user-replication-has-completed"></a><span data-ttu-id="e3f29-103">La comprobación de la replicación de usuarios ha finalizado</span><span class="sxs-lookup"><span data-stu-id="e3f29-103">Verify user replication has completed</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e3f29-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e3f29-104">

<span> </span></span></span>

<span data-ttu-id="e3f29-105">_**Última modificación del tema:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="e3f29-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="e3f29-106">Al ejecutar el cmdlet **Move-CsUser** , puede experimentar un error porque la información del usuario entre los servicios de dominio de Active Directory (AD DS) y las bases de datos de Lync Server 2013 no está sincronizada porque la replicación inicial está incompleta.</span><span class="sxs-lookup"><span data-stu-id="e3f29-106">When running the **Move-CsUser** cmdlet, you may experience a failure because user information between Active Directory Domain Services (AD DS) and the Lync Server 2013 databases are out of sync because the initial replication is incomplete.</span></span> <span data-ttu-id="e3f29-107">El tiempo que tarda la finalización satisfactoria de la sincronización inicial del servicio duplicador de usuarios de Lync Server 2013 depende del número de controladores de dominio que se hospeden en el bosque de Active Directory que hospeda el grupo de servidores de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e3f29-107">The time it takes for the successful completion of the Lync Server 2013 User Replicator service's initial synchronization depends on the number of domain controllers that are hosted in the Active Directory forest that hosts the Lync Server 2013 pool.</span></span> <span data-ttu-id="e3f29-108">El proceso de sincronización inicial del servicio replicador de usuarios de Lync Server 2013 se produce cuando el servidor front-end de Lync Server 2013 se inicia por primera vez.</span><span class="sxs-lookup"><span data-stu-id="e3f29-108">The Lync Server 2013 User Replicator service initial synchronization process occurs when the Lync Server 2013 Front End Server is started for the first time.</span></span> <span data-ttu-id="e3f29-109">Después, la sincronización se basa en el intervalo del replicador de usuarios.</span><span class="sxs-lookup"><span data-stu-id="e3f29-109">After that, the synchronization is then based on the User Replicator interval.</span></span> <span data-ttu-id="e3f29-110">Complete los pasos siguientes para comprobar que la replicación de usuario se ha completado antes de ejecutar el cmdlet **Move-CsUser** .</span><span class="sxs-lookup"><span data-stu-id="e3f29-110">Complete the following steps to verify user replication has completed before running the **Move-CsUser** cmdlet.</span></span>

<div>

## <a name="to-verify-user-replication-has-completed"></a><span data-ttu-id="e3f29-111">Para comprobar que la replicación de usuario se ha completado</span><span class="sxs-lookup"><span data-stu-id="e3f29-111">To verify user replication has completed</span></span>

1.  <span data-ttu-id="e3f29-112">Inicie sesión en el equipo donde se encuentre instalado el Generador de topologías como miembro del grupo Administradores del dominio y el grupo RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="e3f29-112">Log on to the computer where Topology Builder is installed as a member of the Domain Admins group and the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="e3f29-113">Haga clic en el menú **Inicio** y, a continuación, en **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="e3f29-113">Click the **Start** menu, and then click **Run**.</span></span>

3.  <span data-ttu-id="e3f29-114">Escriba **eventvwr.exe** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e3f29-114">Enter **eventvwr.exe** and then click **OK**.</span></span>

4.  <span data-ttu-id="e3f29-115">En el visor de eventos, haga clic en **registros de aplicaciones y servicios** para expandirlo y, a continuación, seleccione Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e3f29-115">In Event Viewer, click **Applications and Services logs** to expand it, and then select Lync Server.</span></span>

5.  <span data-ttu-id="e3f29-116">En el panel **acciones** , haga clic en **filtrar registro actual**.</span><span class="sxs-lookup"><span data-stu-id="e3f29-116">In the **Actions** pane click **Filter Current Log**.</span></span>

6.  <span data-ttu-id="e3f29-117">En la lista **orígenes de eventos** , haga clic en **replicador de usuarios de LS**.</span><span class="sxs-lookup"><span data-stu-id="e3f29-117">From the **Event sources** list, click **LS User Replicator**.</span></span>

7.  <span data-ttu-id="e3f29-118">En **\<All Event IDs\>** escriba **30024** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e3f29-118">In **\<All Event IDs\>** enter **30024** and then click **OK**.</span></span>

8.  <span data-ttu-id="e3f29-119">En la lista eventos filtrados, en la pestaña **General** , busque una entrada que indique que la replicación de usuarios se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e3f29-119">In the filtered events list, on the **General** tab, look for an entry that states user replication has completed successfully.</span></span>

<span data-ttu-id="e3f29-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e3f29-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

