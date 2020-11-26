---
title: 'Lync Server 2013: Configurar una ruta de conmutación por error'
description: 'Lync Server 2013: configuración de una ruta de conmutación por error.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a failover route
ms:assetid: 76e48df4-3b78-4fb7-b1f7-c1e604b81bad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398581(v=OCS.15)
ms:contentKeyID: 48184542
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7cfc45276931685a2d42103b1b7f1d5015dcd7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433524"
---
# <a name="configuring-a-failover-route-in-lync-server-2013"></a><span data-ttu-id="a4f39-103">Configurar una ruta de conmutación por error en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4f39-103">Configuring a failover route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a4f39-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a4f39-104">

<span> </span></span></span>

<span data-ttu-id="a4f39-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="a4f39-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="a4f39-106">En el ejemplo siguiente se muestra cómo un administrador puede definir una ruta de conmutación por error para su uso si la GW1 de Dallas está desactivada para su mantenimiento o no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a4f39-106">The following example shows how an administrator can define a failover route for use if the Dallas-GW1 is down for maintenance or is otherwise unavailable.</span></span> <span data-ttu-id="a4f39-107">En las siguientes tablas se muestra el cambio de configuración requerido.</span><span class="sxs-lookup"><span data-stu-id="a4f39-107">The following tables illustrate the required configuration change.</span></span>

### <a name="table-1-user-policy"></a><span data-ttu-id="a4f39-108">Tabla 1.</span><span class="sxs-lookup"><span data-stu-id="a4f39-108">Table 1.</span></span> <span data-ttu-id="a4f39-109">Directiva de usuario</span><span class="sxs-lookup"><span data-stu-id="a4f39-109">User Policy</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4f39-110">Directiva de usuario</span><span class="sxs-lookup"><span data-stu-id="a4f39-110">User policy</span></span></th>
<th><span data-ttu-id="a4f39-111">Uso del teléfono</span><span class="sxs-lookup"><span data-stu-id="a4f39-111">Phone usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4f39-112">Directiva de llamadas predeterminada</span><span class="sxs-lookup"><span data-stu-id="a4f39-112">Default Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="a4f39-113">Local</span><span class="sxs-lookup"><span data-stu-id="a4f39-113">Local</span></span></p>
<p><span data-ttu-id="a4f39-114">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="a4f39-114">GlobalPSTNHopoff</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4f39-115">Directiva local de Redmond</span><span class="sxs-lookup"><span data-stu-id="a4f39-115">Redmond Local Policy</span></span></p></td>
<td><p><span data-ttu-id="a4f39-116">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="a4f39-116">RedmondLocal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4f39-117">Política de llamadas de Dallas</span><span class="sxs-lookup"><span data-stu-id="a4f39-117">Dallas Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="a4f39-118">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="a4f39-118">DallasUsers</span></span></p>
<p><span data-ttu-id="a4f39-119">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="a4f39-119">GlobalPSTNHopoff</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-2-routes"></a><span data-ttu-id="a4f39-120">Tabla 2.</span><span class="sxs-lookup"><span data-stu-id="a4f39-120">Table 2.</span></span> <span data-ttu-id="a4f39-121">Redirige</span><span class="sxs-lookup"><span data-stu-id="a4f39-121">Routes</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4f39-122">Nombre de la ruta</span><span class="sxs-lookup"><span data-stu-id="a4f39-122">Route name</span></span></th>
<th><span data-ttu-id="a4f39-123">Patrón de números</span><span class="sxs-lookup"><span data-stu-id="a4f39-123">Number pattern</span></span></th>
<th><span data-ttu-id="a4f39-124">Uso del teléfono</span><span class="sxs-lookup"><span data-stu-id="a4f39-124">Phone usage</span></span></th>
<th><span data-ttu-id="a4f39-125">Tronco</span><span class="sxs-lookup"><span data-stu-id="a4f39-125">Trunk</span></span></th>
<th><span data-ttu-id="a4f39-126">Puerta</span><span class="sxs-lookup"><span data-stu-id="a4f39-126">Gateway</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4f39-127">Camino local de Redmond</span><span class="sxs-lookup"><span data-stu-id="a4f39-127">Redmond Local Route</span></span></p></td>
<td><p><span data-ttu-id="a4f39-128">^\+1 (425 | 206 | 253) (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="a4f39-128">^\+1(425|206|253)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="a4f39-129">Local</span><span class="sxs-lookup"><span data-stu-id="a4f39-129">Local</span></span></p>
<p><span data-ttu-id="a4f39-130">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="a4f39-130">RedmondLocal</span></span></p></td>
<td><p><span data-ttu-id="a4f39-131">Trunk1</span><span class="sxs-lookup"><span data-stu-id="a4f39-131">Trunk1</span></span></p>
<p><span data-ttu-id="a4f39-132">Trunk2</span><span class="sxs-lookup"><span data-stu-id="a4f39-132">Trunk2</span></span></p></td>
<td><p><span data-ttu-id="a4f39-133">Rojo: GW1</span><span class="sxs-lookup"><span data-stu-id="a4f39-133">Red-GW1</span></span></p>
<p><span data-ttu-id="a4f39-134">Rojo: GW2</span><span class="sxs-lookup"><span data-stu-id="a4f39-134">Red-GW2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4f39-135">Ruta local de Dallas</span><span class="sxs-lookup"><span data-stu-id="a4f39-135">Dallas Local Route</span></span></p></td>
<td><p><span data-ttu-id="a4f39-136">^\+1 (972 | 214 | 469) (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="a4f39-136">^\+1(972|214|469)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="a4f39-137">Local</span><span class="sxs-lookup"><span data-stu-id="a4f39-137">Local</span></span></p></td>
<td><p><span data-ttu-id="a4f39-138">Trunk3</span><span class="sxs-lookup"><span data-stu-id="a4f39-138">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="a4f39-139">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="a4f39-139">Dallas-GW1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4f39-140">Ruta universal</span><span class="sxs-lookup"><span data-stu-id="a4f39-140">Universal Route</span></span></p></td>
<td><p><span data-ttu-id="a4f39-141">^\+? (\d \*) $</span><span class="sxs-lookup"><span data-stu-id="a4f39-141">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="a4f39-142">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="a4f39-142">GlobalPSTNHopoff</span></span></p></td>
<td><p><span data-ttu-id="a4f39-143">Trunk1</span><span class="sxs-lookup"><span data-stu-id="a4f39-143">Trunk1</span></span></p>
<p><span data-ttu-id="a4f39-144">Trunk2</span><span class="sxs-lookup"><span data-stu-id="a4f39-144">Trunk2</span></span></p>
<p><span data-ttu-id="a4f39-145">Trunk3</span><span class="sxs-lookup"><span data-stu-id="a4f39-145">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="a4f39-146">Rojo: GW1</span><span class="sxs-lookup"><span data-stu-id="a4f39-146">Red-GW1</span></span></p>
<p><span data-ttu-id="a4f39-147">Rojo: GW2</span><span class="sxs-lookup"><span data-stu-id="a4f39-147">Red-GW2</span></span></p>
<p><span data-ttu-id="a4f39-148">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="a4f39-148">Dallas-GW1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4f39-149">Ruta de usuarios de Dallas</span><span class="sxs-lookup"><span data-stu-id="a4f39-149">Dallas Users Route</span></span></p></td>
<td><p><span data-ttu-id="a4f39-150">^\+? (\d \*) $</span><span class="sxs-lookup"><span data-stu-id="a4f39-150">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="a4f39-151">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="a4f39-151">DallasUsers</span></span></p></td>
<td><p><span data-ttu-id="a4f39-152">Trunk3</span><span class="sxs-lookup"><span data-stu-id="a4f39-152">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="a4f39-153">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="a4f39-153">Dallas-GW1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a4f39-154">En la tabla 1, se agrega un uso de teléfono de GlobalPSTNHopoff después del uso del teléfono DallasUsers en la política de llamadas de Dallas.</span><span class="sxs-lookup"><span data-stu-id="a4f39-154">In Table 1, a phone usage of GlobalPSTNHopoff is added after the DallasUsers phone usage in the Dallas Calling Policy.</span></span> <span data-ttu-id="a4f39-155">Esto permite que las llamadas con la Directiva de llamadas de Dallas usen rutas configuradas para el uso del teléfono GlobalPSTNHopoff si una ruta para el uso del teléfono DallasUsers no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a4f39-155">This enables calls with the Dallas Calling policy to use routes that are configured for the GlobalPSTNHopoff phone usage if a route for the DallasUsers phone usage is unavailable.</span></span>

<span data-ttu-id="a4f39-156"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a4f39-156"></div>

<span> </span>

</div>

</div>

</span></span></div>

