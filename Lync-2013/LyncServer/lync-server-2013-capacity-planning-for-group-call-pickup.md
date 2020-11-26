---
title: 'Lync Server 2013: Planeación de capacidad para la recogida de llamadas grupales'
description: 'Lync Server 2013: Planeación de capacidad para la recogida de llamadas grupales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Group Call Pickup
ms:assetid: 0d654a19-6cf0-4118-903d-ec2c4e519253
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ984297(v=OCS.15)
ms:contentKeyID: 51476680
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12648c57d1036a0ed27c60ef6399bf570c5dcd3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435575"
---
# <a name="capacity-planning-for-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="3defd-103">Planificación de la capacidad para la recopilación de llamadas grupales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3defd-103">Capacity planning for Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3defd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3defd-104">

<span> </span></span></span>

<span data-ttu-id="3defd-105">_**Última modificación del tema:** 2013-02-12_</span><span class="sxs-lookup"><span data-stu-id="3defd-105">_**Topic Last Modified:** 2013-02-12_</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="3defd-106">En la siguiente tabla se describe el modelo de usuario de recogida de llamadas grupales que puede usar como base para los requisitos de planes de capacidad.</span><span class="sxs-lookup"><span data-stu-id="3defd-106">The following table describes the Group Call Pickup user model that you can use as the basis for capacity planning requirements.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3defd-107">La recogida de llamadas grupales se basa en la aplicación de estacionamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="3defd-107">Group Call Pickup is based on the Call Park application.</span></span> <span data-ttu-id="3defd-108">Tenga en cuenta que, para la planeación de la capacidad de recuperación ante desastres, cada grupo de un grupo emparejado debería poder controlar las cargas de trabajo de los servicios de estacionamiento de llamadas, incluida la recogida de llamadas grupales, en ambos grupos.</span><span class="sxs-lookup"><span data-stu-id="3defd-108">Keep in mind that, for disaster recovery capacity planning, each pool of a paired pool should be able to handle the workloads for Call Park services, including Group Call Pickup, in both pools.</span></span>



</div>

### <a name="group-call-pickup-user-model"></a><span data-ttu-id="3defd-109">Modelo de usuario de llamada grupal</span><span class="sxs-lookup"><span data-stu-id="3defd-109">Group Call Pickup User Model</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3defd-110">Métrica</span><span class="sxs-lookup"><span data-stu-id="3defd-110">Metric</span></span></th>
<th><span data-ttu-id="3defd-111">Por grupo front-end (con 8 servidores frontales)</span><span class="sxs-lookup"><span data-stu-id="3defd-111">Per Front End pool (with 8 Front End Servers)</span></span></th>
<th><span data-ttu-id="3defd-112">Por servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="3defd-112">Per Standard Edition server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3defd-113">Cantidad recomendada de usuarios por grupo</span><span class="sxs-lookup"><span data-stu-id="3defd-113">Recommended number of users per group</span></span></p></td>
<td><p><span data-ttu-id="3defd-114">50</span><span class="sxs-lookup"><span data-stu-id="3defd-114">50</span></span></p></td>
<td><p><span data-ttu-id="3defd-115">50</span><span class="sxs-lookup"><span data-stu-id="3defd-115">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3defd-116">Cantidad recomendada de grupos</span><span class="sxs-lookup"><span data-stu-id="3defd-116">Recommended number of groups</span></span></p></td>
<td><p><span data-ttu-id="3defd-117">500</span><span class="sxs-lookup"><span data-stu-id="3defd-117">500</span></span></p></td>
<td><p><span data-ttu-id="3defd-118">60</span><span class="sxs-lookup"><span data-stu-id="3defd-118">60</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3defd-119">Cantidad máxima de usuarios por grupo habilitados para la atención de llamadas grupales</span><span class="sxs-lookup"><span data-stu-id="3defd-119">Maximum number of users per pool enabled for Group Call Pickup</span></span></p></td>
<td><p><span data-ttu-id="3defd-120">25 000</span><span class="sxs-lookup"><span data-stu-id="3defd-120">25,000</span></span></p></td>
<td><p><span data-ttu-id="3defd-121">3 000</span><span class="sxs-lookup"><span data-stu-id="3defd-121">3,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3defd-122">Tasa máxima de llamadas entrantes al total de usuarios habilitados para la atención de llamadas grupales por grupo, por minuto</span><span class="sxs-lookup"><span data-stu-id="3defd-122">Maximum rate of incoming calls to total users enabled for Group Call Pickup per pool per minute</span></span></p></td>
<td><p><span data-ttu-id="3defd-123">500</span><span class="sxs-lookup"><span data-stu-id="3defd-123">500</span></span></p></td>
<td><p><span data-ttu-id="3defd-124">60</span><span class="sxs-lookup"><span data-stu-id="3defd-124">60</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3defd-125">Tasa máxima de llamadas recuperadas por los usuarios con la atención de llamadas grupales por grupo, por minuto</span><span class="sxs-lookup"><span data-stu-id="3defd-125">Maximum rate of calls retrieved by users with Group Call Pickup per pool per minute</span></span></p></td>
<td><p><span data-ttu-id="3defd-126">200</span><span class="sxs-lookup"><span data-stu-id="3defd-126">200</span></span></p></td>
<td><p><span data-ttu-id="3defd-127">veinticinco</span><span class="sxs-lookup"><span data-stu-id="3defd-127">25</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <UL>
> <LI>
> <P><span data-ttu-id="3defd-128">Para los grupos de servidores front-end que tienen menos de ocho servidores front-end, calcule las métricas linealmente.</span><span class="sxs-lookup"><span data-stu-id="3defd-128">For Front End pools that have fewer than eight Front End Servers, calculate the metrics linearly.</span></span> <span data-ttu-id="3defd-129">Por ejemplo, si el grupo de servidores front-end tiene un servidor front-end, calcule la carga máxima como 1/8 de los valores que se muestran en la tabla.</span><span class="sxs-lookup"><span data-stu-id="3defd-129">For example, if your Front End pool has one Front End Server, calculate the maximum load as 1/8 of the values shown in the table.</span></span></P>
> <LI>
> <P><span data-ttu-id="3defd-130">Puedes aumentar o disminuir la cantidad recomendada de usuarios por grupo y la cantidad de grupos siempre y cuando no supere la cantidad máxima de usuarios por grupo.</span><span class="sxs-lookup"><span data-stu-id="3defd-130">You can increase or decrease the recommended number of users per group and number of groups as long as you do not exceed the maximum number of users per pool.</span></span> <span data-ttu-id="3defd-131">Por ejemplo, su servidor Standard Edition puede tener 120 grupos con 25 usuarios por grupo, porque la cantidad de usuarios habilitada para la recogida de llamadas grupales todavía está dentro del modelo de usuario máximo (es decir, 120 grupos de 25 usuarios es 3.000 usuarios habilitados para la recogida de llamadas grupales).</span><span class="sxs-lookup"><span data-stu-id="3defd-131">For example, your Standard Edition server can have 120 groups with 25 users per group because the number of users enabled for Group Call Pickup is still within the user model maximum (that is, 120 groups times 25 users is 3,000 users enabled for Group Call Pickup).</span></span></P></LI></UL><span data-ttu-id="3defd-132">



</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3defd-132">



</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

