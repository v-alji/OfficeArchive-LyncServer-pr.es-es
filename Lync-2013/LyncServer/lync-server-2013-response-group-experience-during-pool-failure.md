---
title: 'Lync Server 2013: Experiencia de grupo de respuesta durante errores del grupo de servidores'
description: Experiencia de grupo de respuesta de Lync Server 2013 durante un error de grupo.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group experience during pool failure
ms:assetid: 4e00fb38-64b1-4fd9-903d-7639177bc303
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204886(v=OCS.15)
ms:contentKeyID: 48184116
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d8d5904bc6934d4c330202bafa66d6dd8a16ff5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436247"
---
# <a name="response-group-experience-in-lync-server-2013-during-pool-failure"></a><span data-ttu-id="49459-103">Experiencia de grupo de respuesta durante errores del grupo de servidores en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49459-103">Response group experience in Lync Server 2013 during pool failure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="49459-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="49459-104">

<span> </span></span></span>

<span data-ttu-id="49459-105">_**Última modificación del tema:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="49459-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="49459-106">En esta sección se describe detalladamente cómo afecta la actividad de grupos de respuesta en las siguientes etapas:</span><span class="sxs-lookup"><span data-stu-id="49459-106">This section describes in detail how response group activity is affected in the following stages:</span></span>

  - <span data-ttu-id="49459-107">Se produce una interrupción en el grupo principal, pero aún no se ha iniciado la conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="49459-107">An outage occurs in the primary pool, but failover is not yet initiated.</span></span>

  - <span data-ttu-id="49459-108">El servicio se conmuta por error al grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="49459-108">Service is failed over to the backup pool.</span></span>

  - <span data-ttu-id="49459-109">El servicio no puede recuperarse en el grupo primario.</span><span class="sxs-lookup"><span data-stu-id="49459-109">Service is failed back to the primary pool.</span></span>

<div>

## <a name="user-experience-when-outage-occurs"></a><span data-ttu-id="49459-110">Experiencia de usuario cuando se produce una interrupción</span><span class="sxs-lookup"><span data-stu-id="49459-110">User Experience When Outage Occurs</span></span>

<span data-ttu-id="49459-111">Cuando se produce una interrupción en un grupo o sitio, pero el administrador aún no ha iniciado la conmutación por error, la actividad del grupo de respuesta se controla como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="49459-111">When a pool or site outage occurs, but the administrator has not yet initiated failover, response group activity is handled as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="49459-112">Durante la recuperación de desastres, las llamadas se comportan de forma diferente en función de si los grupos de respuesta del grupo principal se importaron al grupo de copia de seguridad durante la recuperación.</span><span class="sxs-lookup"><span data-stu-id="49459-112">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="49459-113">En la tabla siguiente, las referencias a grupos de respuesta importados significan que los grupos de respuesta del grupo principal se importaron al grupo de copia de seguridad durante el modo de recuperación de desastres.</span><span class="sxs-lookup"><span data-stu-id="49459-113">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="outage-occurs"></a><span data-ttu-id="49459-114">Se produce una interrupción</span><span class="sxs-lookup"><span data-stu-id="49459-114">Outage Occurs</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49459-115">Tipo de acción de usuario o llamada</span><span class="sxs-lookup"><span data-stu-id="49459-115">Type of call or user action</span></span></th>
<th><span data-ttu-id="49459-116">Durante la interrupción</span><span class="sxs-lookup"><span data-stu-id="49459-116">During outage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49459-117">Llamadas conectadas a un agente</span><span class="sxs-lookup"><span data-stu-id="49459-117">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-118">Las llamadas regulares permanecen conectadas.</span><span class="sxs-lookup"><span data-stu-id="49459-118">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="49459-119">Las llamadas anónimas se desconectan.</span><span class="sxs-lookup"><span data-stu-id="49459-119">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49459-120">Llamadas en curso que aún no están conectadas a un agente</span><span class="sxs-lookup"><span data-stu-id="49459-120">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="49459-121">Las llamadas se desconectan.</span><span class="sxs-lookup"><span data-stu-id="49459-121">Calls are disconnected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49459-122">Llamadas nuevas</span><span class="sxs-lookup"><span data-stu-id="49459-122">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-123">Las llamadas se desconectan.</span><span class="sxs-lookup"><span data-stu-id="49459-123">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="49459-124">Si se importaron grupos de respuesta, las llamadas se conectan al grupo de copia de seguridad, pero no se pueden alcanzar los agentes alojados en el bloque principal.</span><span class="sxs-lookup"><span data-stu-id="49459-124">If response groups were imported, calls connect to backup pool, but agents homed in primary pool are unreachable.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49459-125">Llamadas del agente en nombre del grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="49459-125">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="49459-126">La característica está deshabilitada durante este paso.</span><span class="sxs-lookup"><span data-stu-id="49459-126">Feature is disabled during this stage.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49459-127">Inicio de sesión del agente e información del agente</span><span class="sxs-lookup"><span data-stu-id="49459-127">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-128">Los grupos de agentes que pertenecen al repositorio principal pueden verse en la consola del agente, pero los agentes no pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-128">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="49459-129">Los grupos de agentes que pertenecen al grupo de copia de seguridad pueden verse en la consola del agente y los agentes pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-129">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="49459-130">Los grupos de agentes importados no se muestran en la consola del agente.</span><span class="sxs-lookup"><span data-stu-id="49459-130">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49459-131">Configuración del grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="49459-131">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-132">Los grupos de respuesta que pertenecen al grupo primario se pueden ver, en función de la disponibilidad de la base de datos back-end del grupo principal, pero no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="49459-132">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="49459-133">Los grupos de respuesta que pertenecen al grupo de copias de seguridad se pueden ver y modificar.</span><span class="sxs-lookup"><span data-stu-id="49459-133">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="49459-134">Los grupos de respuesta importados no se pueden ver con el panel de control de Lync Server o la herramienta de configuración de grupo de respuesta, pero se pueden configurar mediante los cmdlets del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="49459-134">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failover"></a><span data-ttu-id="49459-135">Experiencia del usuario durante la conmutación por error</span><span class="sxs-lookup"><span data-stu-id="49459-135">User Experience During Failover</span></span>

<span data-ttu-id="49459-136">Cuando un administrador invoca la conmutación por error a un grupo de copia de seguridad, la actividad del grupo de respuesta se controla durante y después de la conmutación por error, tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="49459-136">When an administrator invokes failover to a backup pool, response group activity is handled during and after the failover as described in the following table.</span></span> <span data-ttu-id="49459-137">En la primera columna se describe el tipo de actividad que se puede llevar a cabo.</span><span class="sxs-lookup"><span data-stu-id="49459-137">The first column describes the type of activity that might be taking place.</span></span> <span data-ttu-id="49459-138">La columna central describe cómo se administra cada actividad durante el breve tiempo que se tarda en conmutar por error al grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="49459-138">The middle column describes how each activity is handled during the brief time that it takes to fail over to the backup pool.</span></span> <span data-ttu-id="49459-139">La última columna describe cómo se controla la actividad durante la duración, una vez completada la conmutación por error y en la que se encuentra el grupo de copia de seguridad para el grupo primario.</span><span class="sxs-lookup"><span data-stu-id="49459-139">The last column describes how the activity is handled for the duration, after the failover process is complete and the backup pool is standing in for the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="49459-140">Durante la recuperación de desastres, las llamadas se comportan de forma diferente en función de si los grupos de respuesta del grupo principal se importaron al grupo de copia de seguridad durante la recuperación.</span><span class="sxs-lookup"><span data-stu-id="49459-140">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="49459-141">En la tabla siguiente, las referencias a grupos de respuesta importados significan que los grupos de respuesta del grupo principal se importaron al grupo de copia de seguridad durante el modo de recuperación de desastres.</span><span class="sxs-lookup"><span data-stu-id="49459-141">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="failover-is-initiated"></a><span data-ttu-id="49459-142">Se inicia la conmutación por error</span><span class="sxs-lookup"><span data-stu-id="49459-142">Failover Is Initiated</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49459-143">Tipo de acción de usuario o llamada</span><span class="sxs-lookup"><span data-stu-id="49459-143">Type of call or user action</span></span></th>
<th><span data-ttu-id="49459-144">Durante la conmutación por error</span><span class="sxs-lookup"><span data-stu-id="49459-144">During Failover</span></span></th>
<th><span data-ttu-id="49459-145">Después de que se complete la conmutación por error</span><span class="sxs-lookup"><span data-stu-id="49459-145">After Failover Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49459-146">Llamadas conectadas a un agente</span><span class="sxs-lookup"><span data-stu-id="49459-146">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-147">Las llamadas regulares permanecen conectadas.</span><span class="sxs-lookup"><span data-stu-id="49459-147">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="49459-148">Las llamadas anónimas se desconectan.</span><span class="sxs-lookup"><span data-stu-id="49459-148">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="49459-149">Las llamadas regulares permanecen conectadas.</span><span class="sxs-lookup"><span data-stu-id="49459-149">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="49459-150">Para los grupos de respuesta importados, las llamadas anónimas que hayan llegado al grupo de backup seguirán estando conectadas.</span><span class="sxs-lookup"><span data-stu-id="49459-150">For imported response groups, anonymous calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49459-151">Llamadas en curso que aún no están conectadas a un agente</span><span class="sxs-lookup"><span data-stu-id="49459-151">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="49459-152">Las llamadas se desconectan.</span><span class="sxs-lookup"><span data-stu-id="49459-152">Calls are disconnected.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-153">Si los grupos de respuesta no se importaron, no hay llamadas en este estado.</span><span class="sxs-lookup"><span data-stu-id="49459-153">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="49459-154">Para los grupos de respuesta importados, las llamadas que hayan llegado al grupo de copia de seguridad seguirán estando conectadas.</span><span class="sxs-lookup"><span data-stu-id="49459-154">For imported response groups, calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49459-155">Llamadas nuevas</span><span class="sxs-lookup"><span data-stu-id="49459-155">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-156">Las llamadas se desconectan.</span><span class="sxs-lookup"><span data-stu-id="49459-156">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="49459-157">Para los grupos de respuesta importados, las llamadas se conectan al grupo de copia de seguridad, pero los agentes alojados en el grupo primario son inaccesibles.</span><span class="sxs-lookup"><span data-stu-id="49459-157">For imported response groups, calls connect to the backup pool, but agents homed in the primary pool are unreachable.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="49459-158">Si los grupos de respuesta no se importaron, las llamadas se desconectarán.</span><span class="sxs-lookup"><span data-stu-id="49459-158">If response groups were not imported, calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="49459-159">Para los grupos de respuesta importados, las llamadas se conectan al grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="49459-159">For imported response groups, calls connect to the backup pool.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49459-160">Llamadas del agente en nombre del grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="49459-160">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="49459-161">La característica está deshabilitada durante esta fase</span><span class="sxs-lookup"><span data-stu-id="49459-161">Feature is disabled during this stage</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-162">Si los grupos de respuesta no se importaron, no se pueden realizar llamadas.</span><span class="sxs-lookup"><span data-stu-id="49459-162">If response groups were not imported, calls fail.</span></span></p></li>
<li><p><span data-ttu-id="49459-163">Para grupos de respuesta importados, las llamadas se realizarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="49459-163">For imported response groups, calls succeed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49459-164">Inicio de sesión del agente e información del agente</span><span class="sxs-lookup"><span data-stu-id="49459-164">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-165">Los grupos de agentes que pertenecen al repositorio principal pueden verse en la consola del agente, pero los agentes no pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-165">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="49459-166">Los grupos de agentes que pertenecen al grupo de copia de seguridad pueden verse en la consola del agente y los agentes pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-166">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="49459-167">Los grupos de agentes importados se muestran en la consola del agente y los agentes pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-167">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="49459-168">Los grupos de agentes que pertenecen al repositorio principal pueden verse en la consola del agente, pero los agentes no pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-168">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="49459-169">Los grupos de agentes que pertenecen al grupo de copia de seguridad pueden verse en la consola del agente y los agentes pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-169">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="49459-170">Los grupos de agentes importados se muestran en la consola del agente y los agentes pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-170">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49459-171">Configuración del grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="49459-171">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-172">Los grupos de respuesta que pertenecen al grupo primario se pueden ver, en función de la disponibilidad de la base de datos back-end del grupo principal, pero no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="49459-172">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="49459-173">Los grupos de respuesta que pertenecen al grupo de copias de seguridad se pueden ver y modificar.</span><span class="sxs-lookup"><span data-stu-id="49459-173">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="49459-174">Los grupos de respuesta importados no se pueden ver con el panel de control de Lync Server o la herramienta de configuración de grupo de respuesta, pero se pueden configurar mediante los cmdlets del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="49459-174">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="49459-175">Los grupos de respuesta que pertenecen al grupo primario se pueden ver, dependiendo de la disponibilidad de la base de datos back-end, pero no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="49459-175">Response groups owned by the primary pool can be viewed, depending on the availability of the back end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="49459-176">Los grupos de respuesta que pertenecen al grupo de copias de seguridad se pueden ver y modificar.</span><span class="sxs-lookup"><span data-stu-id="49459-176">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="49459-177">Los grupos de respuesta importados no se pueden ver con el panel de control de Lync Server o la herramienta de configuración de grupo de respuesta, pero se pueden configurar mediante los cmdlets del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="49459-177">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failback"></a><span data-ttu-id="49459-178">Experiencia de usuario durante la conmutación por recuperación</span><span class="sxs-lookup"><span data-stu-id="49459-178">User Experience During Failback</span></span>

<span data-ttu-id="49459-179">Cuando un administrador invoca la conmutación por recuperación al grupo principal, la actividad del grupo de respuesta se controla durante y después de la conmutación por recuperación, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="49459-179">When an administrator invokes failback to the primary pool, response group activity is handled during and after the failback as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="49459-180">Durante la recuperación de desastres, las llamadas se comportan de forma diferente en función de si los grupos de respuesta del grupo principal se importaron al grupo de copia de seguridad durante la recuperación.</span><span class="sxs-lookup"><span data-stu-id="49459-180">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="49459-181">En la tabla siguiente, las referencias a grupos de respuesta importados significan que los grupos de respuesta del grupo principal se importaron al grupo de copia de seguridad durante el modo de recuperación de desastres.</span><span class="sxs-lookup"><span data-stu-id="49459-181">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="call-handling-in-failback"></a><span data-ttu-id="49459-182">Control de llamadas en failback</span><span class="sxs-lookup"><span data-stu-id="49459-182">Call Handling in Failback</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49459-183">Tipo de acción de usuario o llamada</span><span class="sxs-lookup"><span data-stu-id="49459-183">Type of call or user action</span></span></th>
<th><span data-ttu-id="49459-184">Durante la conmutación por recuperación</span><span class="sxs-lookup"><span data-stu-id="49459-184">During Failback</span></span></th>
<th><span data-ttu-id="49459-185">Tras completar la conmutación por recuperación</span><span class="sxs-lookup"><span data-stu-id="49459-185">After Failback Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49459-186">Llamadas conectadas a un agente</span><span class="sxs-lookup"><span data-stu-id="49459-186">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-187">Las llamadas regulares permanecen conectadas.</span><span class="sxs-lookup"><span data-stu-id="49459-187">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="49459-188">Si los grupos de respuesta no se importaron, no hay llamadas anónimas en este estado.</span><span class="sxs-lookup"><span data-stu-id="49459-188">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="49459-189">Para los grupos de respuesta importados, las llamadas anónimas permanecen conectadas.</span><span class="sxs-lookup"><span data-stu-id="49459-189">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="49459-190">Las llamadas regulares permanecen conectadas.</span><span class="sxs-lookup"><span data-stu-id="49459-190">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="49459-191">Si los grupos de respuesta no se importaron, no hay llamadas anónimas en este estado.</span><span class="sxs-lookup"><span data-stu-id="49459-191">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="49459-192">Para los grupos de respuesta importados, las llamadas anónimas permanecen conectadas.</span><span class="sxs-lookup"><span data-stu-id="49459-192">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49459-193">Llamadas en curso que aún no están conectadas a un agente</span><span class="sxs-lookup"><span data-stu-id="49459-193">In progress calls not yet connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-194">Si los grupos de respuesta no se importaron, no hay llamadas en este estado.</span><span class="sxs-lookup"><span data-stu-id="49459-194">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="49459-195">Para los grupos de respuesta importados, las llamadas se desconectarán.</span><span class="sxs-lookup"><span data-stu-id="49459-195">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="49459-196">Si los grupos de respuesta no se importaron, no hay llamadas en este estado.</span><span class="sxs-lookup"><span data-stu-id="49459-196">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="49459-197">Para los grupos de respuesta importados, las llamadas se desconectarán.</span><span class="sxs-lookup"><span data-stu-id="49459-197">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49459-198">Llamadas nuevas</span><span class="sxs-lookup"><span data-stu-id="49459-198">New calls</span></span></p></td>
<td><p><span data-ttu-id="49459-199">Las llamadas se conectan al grupo de servidores principal, pero los agentes alojados en el grupo primario no son accesibles.</span><span class="sxs-lookup"><span data-stu-id="49459-199">Calls connect to the primary pool, but agents homed in the primary pool are unreachable.</span></span></p></td>
<td><p><span data-ttu-id="49459-200">Las llamadas se conectan al grupo primario.</span><span class="sxs-lookup"><span data-stu-id="49459-200">Calls connect to the primary pool.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49459-201">Llamadas del agente en nombre del grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="49459-201">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="49459-202">La característica está deshabilitada durante este paso.</span><span class="sxs-lookup"><span data-stu-id="49459-202">Feature is disabled during this stage.</span></span></p></td>
<td><p><span data-ttu-id="49459-203">Las llamadas se realizaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="49459-203">Calls succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49459-204">Inicio de sesión del agente e información del agente</span><span class="sxs-lookup"><span data-stu-id="49459-204">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-205">Los grupos de agentes que pertenecen al repositorio principal pueden verse en la consola del agente, pero los agentes no pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-205">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="49459-206">Los grupos de agentes que pertenecen al grupo de copia de seguridad pueden verse en la consola del agente y los agentes pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-206">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="49459-207">Los grupos de agentes importados se muestran en la consola del agente y los agentes pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-207">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="49459-208">Los grupos de agentes que pertenecen al repositorio principal pueden verse en la consola del agente y los agentes pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-208">Agent groups owned by the primary pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="49459-209">Los grupos de agentes que pertenecen al grupo de copia de seguridad pueden verse en la consola del agente y los agentes pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="49459-209">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="49459-210">Los grupos de agentes importados no se muestran en la consola del agente.</span><span class="sxs-lookup"><span data-stu-id="49459-210">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49459-211">Configuración del grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="49459-211">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="49459-212">Los grupos de respuesta que pertenecen al grupo primario se pueden ver, en función de la disponibilidad de la base de datos back-end del grupo principal, pero no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="49459-212">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="49459-213">Los grupos de respuesta que pertenecen al grupo de copias de seguridad se pueden ver y modificar.</span><span class="sxs-lookup"><span data-stu-id="49459-213">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="49459-214">Los grupos de respuesta importados no se pueden ver con el panel de control de Lync Server o la herramienta de configuración de grupo de respuesta, pero se pueden configurar mediante los cmdlets del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="49459-214">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="49459-215">Los grupos de respuesta que pertenecen al grupo principal se pueden ver y modificar.</span><span class="sxs-lookup"><span data-stu-id="49459-215">Response groups owned by the primary pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="49459-216">Los grupos de respuesta que pertenecen al grupo de copias de seguridad se pueden ver y modificar.</span><span class="sxs-lookup"><span data-stu-id="49459-216">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="49459-217">Los grupos de respuesta importados no se pueden ver con el panel de control de Lync Server o la herramienta de configuración de grupo de respuesta, pero se pueden configurar mediante los cmdlets del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="49459-217">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="49459-218">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="49459-218">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

