---
title: 'Lync Server 2013: agregar o quitar un servidor front-end'
description: 'Lync Server 2013: agregar o quitar un servidor front-end.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add or remove a Front End Server
ms:assetid: ab748733-6bad-4c93-8dda-db8d5271653d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205153(v=OCS.15)
ms:contentKeyID: 48185050
ms.date: 01/21/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 297bbf42dbba3d4f9926fd5ab9e0d7ed79349dc4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439278"
---
# <a name="add-or-remove-a-front-end-server-in-lync-server-2013"></a><span data-ttu-id="3d32f-103">Add or remove a Front End Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3d32f-103">Add or remove a Front End Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d32f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d32f-104">

<span> </span></span></span>

<span data-ttu-id="3d32f-105">_**Última modificación del tema:** 2016-01-21_</span><span class="sxs-lookup"><span data-stu-id="3d32f-105">_**Topic Last Modified:** 2016-01-21_</span></span>

<span data-ttu-id="3d32f-106">Al agregar un servidor front-end a un grupo o quitar un servidor front-end de un grupo, debe reiniciar el grupo.</span><span class="sxs-lookup"><span data-stu-id="3d32f-106">When you add a Front End Server to a pool, or remove a Front End Server from a pool, you then need to restart the pool.</span></span> <span data-ttu-id="3d32f-107">Para evitar que se interrumpa el servicio para los usuarios, use el siguiente procedimiento al agregar o quitar un servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="3d32f-107">To prevent any interruption of service to users, use the following procedure when adding or removing a Front End Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3d32f-108">Si agrega nuevos servidores al grupo, actualice los nuevos servidores del grupo para que estén en el mismo nivel de actualización acumulativa que los servidores existentes del grupo.</span><span class="sxs-lookup"><span data-stu-id="3d32f-108">If you're adding new servers to the pool, update your new pool servers to be at the same Cumulative Update level as the existing servers in the Pool.</span></span>



</div>

<div>

## <a name="to-add-or-remove-front-end-servers"></a><span data-ttu-id="3d32f-109">Para agregar o quitar servidores front-end</span><span class="sxs-lookup"><span data-stu-id="3d32f-109">To add or remove Front End servers</span></span>

1.  <span data-ttu-id="3d32f-110">Si va a quitar los servidores front-end, primero detenga las conexiones nuevas a esos servidores.</span><span class="sxs-lookup"><span data-stu-id="3d32f-110">If you are removing any Front End Servers, first stop new connections to those servers.</span></span> <span data-ttu-id="3d32f-111">Para ello, puede usar el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3d32f-111">To do so, you can use the following cmdlet:</span></span>
    
        Stop-CsWindowsServices -Graceful

2.  <span data-ttu-id="3d32f-112">Cuando los servidores que se van a quitar no tengan sesiones actuales, detenga los servicios de Lync Server en ellos.</span><span class="sxs-lookup"><span data-stu-id="3d32f-112">When the servers being removed have no current sessions, stop Lync Server services on them.</span></span>

3.  <span data-ttu-id="3d32f-113">Abra el generador de topologías y agregue o quite los servidores necesarios.</span><span class="sxs-lookup"><span data-stu-id="3d32f-113">Open Topology Builder, and add or remove the necessary servers.</span></span>

4.  <span data-ttu-id="3d32f-114">Publique la topología.</span><span class="sxs-lookup"><span data-stu-id="3d32f-114">Publish the topology.</span></span>

5.  <span data-ttu-id="3d32f-115">Si el grupo ha desaparecido de dos servidores front-end a más de dos o ha ido de más de dos servidores a dos exactamente, debe escribir el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3d32f-115">If the pool has gone from having two Front End Servers to more than two, or gone from more than two servers to exactly two, you need to type the following cmdlet:</span></span>
    
        Reset-CsPoolRegistrarState-ResetType FullReset -PoolFqdn <PoolFqdn>
    
    <span data-ttu-id="3d32f-116">Si el grupo tiene tres o más servidores, al menos tres de esos servidores deben estar ejecutándose al escribir este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d32f-116">If the pool has three or more servers, then at least three of those servers must be running when you type this cmdlet.</span></span>

6.  <span data-ttu-id="3d32f-117">Reinicie todos los servidores front-end del grupo, uno por uno.</span><span class="sxs-lookup"><span data-stu-id="3d32f-117">Restart all Front End Servers in the pool, one at a time.</span></span>

<span data-ttu-id="3d32f-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d32f-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

