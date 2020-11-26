---
title: 'Lync Server 2013: Tiempo de recuperación para la conmutación por error y por recuperación del grupo de servidores'
description: Lync Server 2013 tiempo de recuperación para la conmutación por error del grupo y la conmutación por recuperación.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Recovery time for pool failover and pool failback
ms:assetid: 902c658f-8442-4d0d-b3ad-bf795ecd550d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205079(v=OCS.15)
ms:contentKeyID: 48184786
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1bb09c32ac4d062358a511464dc21aa7346ee034
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436681"
---
# <a name="recovery-time-for-pool-failover-and-pool-failback-in-lync-server-2013"></a><span data-ttu-id="8f7f0-103">Tiempo de recuperación para la conmutación por error y por recuperación del grupo de servidores en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f7f0-103">Recovery time for pool failover and pool failback in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f7f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f7f0-104">

<span> </span></span></span>

<span data-ttu-id="8f7f0-105">_**Última modificación del tema:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="8f7f0-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="8f7f0-106">Para la conmutación por error de grupo y la conmutación por recuperación del grupo, el objetivo de ingeniería del objetivo de tiempo de recuperación (RTO) es de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="8f7f0-106">For pool failover and pool failback, the engineering target for recovery time objective (RTO) is 30 minutes.</span></span> <span data-ttu-id="8f7f0-107">Este es el tiempo necesario para que se produzca el failover, después de que los administradores hayan determinado que se ha producido un desastre y se hayan iniciado los procedimientos de conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="8f7f0-107">This is the time required for the failover to happen, after administrators have determined there was a disaster and initiated the failover procedures.</span></span> <span data-ttu-id="8f7f0-108">No incluye el tiempo necesario para que los administradores evalúen la situación y tomen una decisión, como tampoco el tiempo necesario para que los usuarios vuelvan a iniciar sesión una vez que finalice la conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="8f7f0-108">It does not include the time for administrators to assess the situation and make a decision, nor does it include the time for users to sign in again after failover is complete.</span></span>

<span data-ttu-id="8f7f0-109">Para la conmutación por error de grupo y la conmutación por recuperación de grupos, el objetivo de ingeniería para objetivo de punto de recuperación (RPO) es de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="8f7f0-109">For pool failover and pool failback, the engineering target for recovery point objective (RPO) is 30 minutes.</span></span> <span data-ttu-id="8f7f0-110">Esto representa la medida de tiempo de los datos que se podrían perder debido al desastre, debido a la latencia de replicación del servicio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8f7f0-110">This represents the time measure of data that could be lost due to the disaster, due to replication latency of the Backup Service.</span></span> <span data-ttu-id="8f7f0-111">Por ejemplo, si un grupo se desconecta a las 10:00 A.M. y el RPO es de 30 minutos, los datos escritos en el grupo van de la 9:30 A.M.</span><span class="sxs-lookup"><span data-stu-id="8f7f0-111">For example, if a pool goes down at 10:00 A.M., and the RPO is 30 minutes, data written to the pool between 9:30 A.M.</span></span> <span data-ttu-id="8f7f0-112">y 10:00 a. M es posible que no se haya replicado en el grupo de copia de seguridad y se perdería.</span><span class="sxs-lookup"><span data-stu-id="8f7f0-112">and 10:00 A.M.might not have replicated to the backup pool, and would be lost.</span></span>

<span data-ttu-id="8f7f0-113">Para todas las cantidades de RTO y RPO de este documento se asume que los dos centros de datos se encuentran en la misma región del mundo con un transporte de alta velocidad y baja latencia entre los dos sitios.</span><span class="sxs-lookup"><span data-stu-id="8f7f0-113">All RTO and RPO numbers in this document assume that the two data centers are located within the same world region with high-speed, low-latency transport between the two sites.</span></span> <span data-ttu-id="8f7f0-114">Estas cantidades se miden para un grupo de 40 000 usuarios activos simultáneamente y 200 000 usuarios habilitados para Lync con respecto a un modelo de usuario predefinido en el que no hay trabajo pendiente en la replicación de datos.</span><span class="sxs-lookup"><span data-stu-id="8f7f0-114">These numbers are measured for a pool with 40,000 concurrently active users and 200,000 users enabled for Lync with respect to a pre-defined user model where there is no backlog in data replication.</span></span> <span data-ttu-id="8f7f0-115">Están sujetas a cambios a partir de las pruebas de rendimiento y validación.</span><span class="sxs-lookup"><span data-stu-id="8f7f0-115">They are subject to change based on performance testing and validation.</span></span>

<span data-ttu-id="8f7f0-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f7f0-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

