---
title: 'Lync Server 2013: Conmutación por error del almacén de administración central'
description: La conmutación por error del almacén central de administración de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Central Management store failover
ms:assetid: f464d715-68a4-462c-9584-00f41ab10db0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205376(v=OCS.15)
ms:contentKeyID: 48185809
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2960a55d6bdc49e00bf22997bc53946d4770fde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435470"
---
# <a name="central-management-store-failover-in-lync-server-2013"></a><span data-ttu-id="c6159-103">Conmutación por error del almacén de administración central en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c6159-103">Central Management store failover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c6159-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c6159-104">

<span> </span></span></span>

<span data-ttu-id="c6159-105">_**Última modificación del tema:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="c6159-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="c6159-106">El almacén central de administración contiene datos de configuración sobre servidores y servicios de la implementación de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="c6159-106">The Central Management store contains configuration data about servers and services in your Lync 2013 deployment.</span></span> <span data-ttu-id="c6159-107">Proporciona un almacenamiento schematized sólido de los datos necesarios para definir, configurar, mantener, administrar, describir y usar una implementación de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="c6159-107">It provides a robust, schematized storage of the data needed to define, set up, maintain, administer, describe, and operate a Lync 2013 deployment.</span></span> <span data-ttu-id="c6159-108">También comprueba los datos para asegurarse de que la configuración es coherente.</span><span class="sxs-lookup"><span data-stu-id="c6159-108">It also validates the data to ensure configuration consistency.</span></span>

<span data-ttu-id="c6159-109">Cada implementación de Lync incluye un almacén de administración central, que se hospeda en el servidor back-end de un grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="c6159-109">Each Lync deployment includes one Central Management store, which is hosted by the Back End Server of one Front End pool.</span></span>

<span data-ttu-id="c6159-110">Al establecer un emparejamiento de grupo que incluye el grupo que hospeda el almacén central de administración, se configura una base de datos de almacenamiento central de administración de copia de seguridad en el grupo de copias de seguridad y los servicios del almacén central de administración se instalan en ambos grupos.</span><span class="sxs-lookup"><span data-stu-id="c6159-110">When you establish a pool pairing that includes the pool hosting the Central Management store, a backup Central Management store database is set up in the backup pool, and Central Management store services are installed in both pools.</span></span> <span data-ttu-id="c6159-111">En cualquier momento, una de las dos bases de datos del almacén de administración central es la principal activa y la otra es una en espera.</span><span class="sxs-lookup"><span data-stu-id="c6159-111">At any point in time, one of the two Central Management store databases is the active master, and the other is a standby.</span></span> <span data-ttu-id="c6159-112">El servicio de copia de seguridad Replica el contenido desde el maestro activo al modo de espera.</span><span class="sxs-lookup"><span data-stu-id="c6159-112">The content is replicated by the Backup Service from the active master to the standby.</span></span>

<span data-ttu-id="c6159-113">Durante la conmutación por error de un grupo de servidores que implica a los grupos que hospedan el almacén de administración central, el administrador debe realizar la conmutación por error del almacén central de administración antes de realizar la conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="c6159-113">During a pool failover that involves the pools hosting the Central Management store, the administrator must fail over the Central Management store before failing over the Front End pool.</span></span>

<span data-ttu-id="c6159-114">Después de que se repara el desastre, no es necesario llevar a cabo la conmutación por recuperación del almacén de administración central.</span><span class="sxs-lookup"><span data-stu-id="c6159-114">After the disaster is repaired, it is not necessary to fail back the Central Management store.</span></span> <span data-ttu-id="c6159-115">Después de la reparación, el almacén de administración central del grupo de copia de seguridad original puede permanecer como maestro activo.</span><span class="sxs-lookup"><span data-stu-id="c6159-115">After repair, the Central Management store in the original backup pool can remain as the active master.</span></span>

<span data-ttu-id="c6159-116">Los objetivos de ingeniería para la conmutación por error del almacén de administración central son 5 minutos para el de tiempo de recuperación (RTO) y 5 minutos para el de punto de recuperación (RPO).</span><span class="sxs-lookup"><span data-stu-id="c6159-116">The engineering targets for Central Management store failover are 5 minutes for recovery time objective (RTO) and 5 minutes for recovery point objective (RPO).</span></span>

<span data-ttu-id="c6159-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c6159-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

