---
title: Quitar un grupo de servidores front-end o servidor Standard Edition
description: Quitar el grupo de servidores front-end o el servidor Standard Edition.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove Front End pool or Standard Edition server
ms:assetid: 83c39a36-49a1-4ac6-9cc5-b0e441b1fdec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688115(v=OCS.15)
ms:contentKeyID: 49733713
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c878d56b073558f4f4b50f31b6742fd581c80241
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440279"
---
# <a name="remove-front-end-pool-or-standard-edition-server"></a><span data-ttu-id="481e6-103">Quitar un grupo de servidores front-end o servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="481e6-103">Remove Front End pool or Standard Edition server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="481e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="481e6-104">

<span> </span></span></span>

<span data-ttu-id="481e6-105">_**Última modificación del tema:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="481e6-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="481e6-106">Este tema le guiará a través del proceso de eliminación de un grupo de servidores front-end o de un servidor front-end Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="481e6-106">This topic guides you through the process of removing a Front End pool or a Standard Edition Front End Server.</span></span> <span data-ttu-id="481e6-107">Al quitar un grupo de servidores front-end, se quita cada servidor front-end que pertenece al grupo como parte del proceso de eliminación de la agrupación.</span><span class="sxs-lookup"><span data-stu-id="481e6-107">When you remove a Front End pool, you remove each Front End Server that belongs to the pool as a part of the pool removal process.</span></span> <span data-ttu-id="481e6-108">Al quitar un servidor front-end Standard Edition, debe quitar la definición de la tienda SQL del generador de topología.</span><span class="sxs-lookup"><span data-stu-id="481e6-108">When you remove a Standard Edition Front End Server, you must remove the SQL Store definition from Topology Builder.</span></span>

<div>

## <a name="to-remove-a-front-end-server-pool"></a><span data-ttu-id="481e6-109">Para quitar un grupo de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="481e6-109">To remove a Front End Server pool</span></span>

1.  <span data-ttu-id="481e6-110">Abra el generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="481e6-110">Open Topology Builder.</span></span>

2.  <span data-ttu-id="481e6-111">Vaya al nodo de 2010 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="481e6-111">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="481e6-112">Expanda agrupaciones **front end de Enterprise Edition**, expanda el grupo de servidores front-end, haga clic con el botón secundario en el grupo de servidores front-end que desee quitar y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="481e6-112">Expand **Enterprise Edition Front End pools**, expand the Front End pool, right-click the Front End pool that you want to remove, and then click **Delete**.</span></span>

4.  <span data-ttu-id="481e6-113">Publique la topología, compruebe el estado de replicación y, a continuación, ejecute el Asistente para la implementación de Lync Server según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="481e6-113">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

</div>

<div>

## <a name="to-remove-a-standard-edition-front-end-server"></a><span data-ttu-id="481e6-114">Para quitar un servidor front-end Standard Edition</span><span class="sxs-lookup"><span data-stu-id="481e6-114">To remove a Standard Edition Front End server</span></span>

1.  <span data-ttu-id="481e6-115">Abra el generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="481e6-115">Open Topology Builder.</span></span>

2.  <span data-ttu-id="481e6-116">Vaya al nodo de 2010 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="481e6-116">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="481e6-117">Expanda **servidores front-end Standard Edition**, haga clic con el botón secundario en el servidor front-end que desee quitar y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="481e6-117">Expand **Standard Edition Front End servers**, right-click the Front End Server that you want to remove, and then click **Delete**.</span></span>

4.  <span data-ttu-id="481e6-118">Expanda **almacenes SQL**, haga clic con el botón secundario en la base de datos de SQL Server asociada al servidor front-end Standard Edition y, después, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="481e6-118">Expand **SQL stores**, right-click the SQL Server database that is associated with the Standard Edition Front End Server, and then click **Delete**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="481e6-119">Debe quitar la definición de las bases de datos de SQL Server en el servidor front-end Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="481e6-119">You must remove the definition of the collocated SQL Server databases from the Standard Edition Front End Server.</span></span>

    
    </div>

5.  <span data-ttu-id="481e6-120">Publique la topología, compruebe el estado de replicación y, a continuación, ejecute el Asistente para la implementación de Lync Server según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="481e6-120">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

<span data-ttu-id="481e6-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="481e6-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

