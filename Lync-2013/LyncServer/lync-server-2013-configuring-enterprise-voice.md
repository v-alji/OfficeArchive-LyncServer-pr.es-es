---
title: 'Lync Server 2013: configuración de telefonía IP empresarial'
description: 'Lync Server 2013: configuración de telefonía IP empresarial.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise Voice
ms:assetid: 7df179fa-d3a2-4b23-a433-b750aedf980b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994041(v=OCS.15)
ms:contentKeyID: 51803952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49a231b92bf7b04aa3466927a79258f0cbad4e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433125"
---
# <a name="configuring-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="2f93e-103">Configurar la telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f93e-103">Configuring Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2f93e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2f93e-104">

<span> </span></span></span>

<span data-ttu-id="2f93e-105">_**Última modificación del tema:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="2f93e-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="2f93e-106">Para implementar la telefonía IP empresarial, tendrá que configurar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2f93e-106">To deploy Enterprise Voice, you’ll need to configure the following:</span></span>

  - <span data-ttu-id="2f93e-107">Crear un tronco</span><span class="sxs-lookup"><span data-stu-id="2f93e-107">Create a Trunk</span></span>

  - <span data-ttu-id="2f93e-108">Definir una directiva de voz</span><span class="sxs-lookup"><span data-stu-id="2f93e-108">Define a Voice Policy</span></span>

  - <span data-ttu-id="2f93e-109">Definir una ruta de voz</span><span class="sxs-lookup"><span data-stu-id="2f93e-109">Define a Voice Route</span></span>

  - <span data-ttu-id="2f93e-110">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="2f93e-110">Enable Users for Enterprise Voice</span></span>

<div>

## <a name="create-a-trunk"></a><span data-ttu-id="2f93e-111">Crear un tronco</span><span class="sxs-lookup"><span data-stu-id="2f93e-111">Create a Trunk</span></span>

<span data-ttu-id="2f93e-112">Debe definir los troncos en su implementación de telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="2f93e-112">You must define trunks in your Enterprise Voice deployment.</span></span> <span data-ttu-id="2f93e-113">Para Location-Based el enrutamiento, debe crear una configuración troncal por tronco.</span><span class="sxs-lookup"><span data-stu-id="2f93e-113">For Location-Based Routing, you must create a trunk configuration per trunk.</span></span> <span data-ttu-id="2f93e-114">Use el generador de topología de Lync Server para definir sus troncos y use el comando de Windows PowerShell de Lync Server, New-CsTrunkConfiguration o el panel de control de Lync Server para definir las configuraciones de troncal correspondientes.</span><span class="sxs-lookup"><span data-stu-id="2f93e-114">Use the Lync Server Topology Builder to define your trunks, and use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, or the Lync Server Control Panel to define the corresponding trunk configurations.</span></span> <span data-ttu-id="2f93e-115">Puede encontrar más información sobre cómo habilitar el enrutamiento de Location-Based en las configuraciones troncales en la sección, habilitar el enrutamiento de Location-Based a los troncos, en el tema sobre [Cómo habilitar el enrutamiento de Location-Based en Lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="2f93e-115">More information on how to enable Location-Based Routing on trunk configurations can be found in the section, Enable Location-Based Routing to Trunks, in the topic, [Enabling Location-Based Routing in Lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span></span> <span data-ttu-id="2f93e-116">En este ejemplo, la tabla siguiente muestra las troncos que se usan en este escenario.</span><span class="sxs-lookup"><span data-stu-id="2f93e-116">For this example, the following table illustrates the trunks used in this scenario.</span></span>

<span data-ttu-id="2f93e-117">Para obtener más información, vea [definir más troncos en el generador de topología en Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span><span class="sxs-lookup"><span data-stu-id="2f93e-117">For more information, see [Define additional trunks in Topology Builder in Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span></span>


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
<th><span data-ttu-id="2f93e-118">Nombre del tronco</span><span class="sxs-lookup"><span data-stu-id="2f93e-118">Trunk name</span></span></th>
<th><span data-ttu-id="2f93e-119">Tipo de sistema</span><span class="sxs-lookup"><span data-stu-id="2f93e-119">System type</span></span></th>
<th><span data-ttu-id="2f93e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2f93e-120">Name</span></span></th>
<th><span data-ttu-id="2f93e-121">Ubicación</span><span class="sxs-lookup"><span data-stu-id="2f93e-121">Location</span></span></th>
<th><span data-ttu-id="2f93e-122">Servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="2f93e-122">Mediation Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f93e-123">Tronco 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="2f93e-123">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="2f93e-124">Puerta de enlace RTC</span><span class="sxs-lookup"><span data-stu-id="2f93e-124">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="2f93e-125">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="2f93e-125">DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="2f93e-126">Delhi</span><span class="sxs-lookup"><span data-stu-id="2f93e-126">Delhi</span></span></p></td>
<td><p><span data-ttu-id="2f93e-127">MS1</span><span class="sxs-lookup"><span data-stu-id="2f93e-127">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f93e-128">Troncal 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="2f93e-128">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="2f93e-129">Puerta de enlace RTC</span><span class="sxs-lookup"><span data-stu-id="2f93e-129">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="2f93e-130">HYD-GW</span><span class="sxs-lookup"><span data-stu-id="2f93e-130">HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="2f93e-131">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="2f93e-131">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="2f93e-132">MS1</span><span class="sxs-lookup"><span data-stu-id="2f93e-132">MS1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f93e-133">Troncal 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-133">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="2f93e-134">PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="2f93e-135">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-135">DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="2f93e-136">Delhi</span><span class="sxs-lookup"><span data-stu-id="2f93e-136">Delhi</span></span></p></td>
<td><p><span data-ttu-id="2f93e-137">MS1</span><span class="sxs-lookup"><span data-stu-id="2f93e-137">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f93e-138">Troncal 4 HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-138">Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="2f93e-139">PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-139">PBX</span></span></p></td>
<td><p><span data-ttu-id="2f93e-140">HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-140">HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="2f93e-141">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="2f93e-141">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="2f93e-142">MS1</span><span class="sxs-lookup"><span data-stu-id="2f93e-142">MS1</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="defines-voice-policies"></a><span data-ttu-id="2f93e-143">Define directivas de voz</span><span class="sxs-lookup"><span data-stu-id="2f93e-143">Defines Voice Policies</span></span>

<span data-ttu-id="2f93e-144">Debe definir directivas de voz para su implementación de telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="2f93e-144">You must define voice policies for your Enterprise Voice deployment.</span></span> <span data-ttu-id="2f93e-145">Definir una directiva de voz para exigir Location-Based restricciones de enrutamiento a un subconjunto de usuarios si solo se requiere un subconjunto de ellas para usar Location-Based enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="2f93e-145">Define a Voice Policy to enforce Location-Based Routing restrictions to a subset of users if only a subset of them is required to use Location-Based Routing.</span></span> <span data-ttu-id="2f93e-146">En este ejemplo, la tabla siguiente muestra las directivas de voz que se usan en este escenario.</span><span class="sxs-lookup"><span data-stu-id="2f93e-146">For this example, the following table illustrates the voice policies used in this scenario.</span></span> <span data-ttu-id="2f93e-147">En la tabla solo se incluyen los valores específicos de Location-Based enrutamiento, con fines de ilustración.</span><span class="sxs-lookup"><span data-stu-id="2f93e-147">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="2f93e-148">Para obtener más información, vea [configuración de directivas de voz y registros de uso de RTC para autorizar llamadas y características de Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="2f93e-148">For more information, see [Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2f93e-149">Política de voz 1</span><span class="sxs-lookup"><span data-stu-id="2f93e-149">Voice policy 1</span></span></th>
<th><span data-ttu-id="2f93e-150">Política de voz 2</span><span class="sxs-lookup"><span data-stu-id="2f93e-150">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f93e-151">IDENTIFICADOR de la Directiva de voz</span><span class="sxs-lookup"><span data-stu-id="2f93e-151">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="2f93e-152">Directiva de voz de Delhi</span><span class="sxs-lookup"><span data-stu-id="2f93e-152">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="2f93e-153">Política de voz de Hyderabad</span><span class="sxs-lookup"><span data-stu-id="2f93e-153">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f93e-154">Usos de RTC</span><span class="sxs-lookup"><span data-stu-id="2f93e-154">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="2f93e-155">Uso de la Delhi, PBX del uso, uso de HYD de PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-155">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="2f93e-156">Uso de Hyderabad, uso de HYD de PBX, PBX del uso</span><span class="sxs-lookup"><span data-stu-id="2f93e-156">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f93e-157">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="2f93e-157">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="2f93e-158">Falso</span><span class="sxs-lookup"><span data-stu-id="2f93e-158">False</span></span></p></td>
<td><p><span data-ttu-id="2f93e-159">Falso</span><span class="sxs-lookup"><span data-stu-id="2f93e-159">False</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-voice-routes"></a><span data-ttu-id="2f93e-160">Definir rutas de voz</span><span class="sxs-lookup"><span data-stu-id="2f93e-160">Define Voice Routes</span></span>

<span data-ttu-id="2f93e-161">Debe definir rutas de voz para su implementación de telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="2f93e-161">You must define voice routes for your Enterprise Voice deployment.</span></span> <span data-ttu-id="2f93e-162">En este ejemplo, la tabla siguiente muestra las rutas de voz usadas en este escenario.</span><span class="sxs-lookup"><span data-stu-id="2f93e-162">For this example, the following table illustrates the voice routes used in this scenario.</span></span> <span data-ttu-id="2f93e-163">En la tabla solo se incluyen los valores específicos de Location-Based enrutamiento, con fines de ilustración.</span><span class="sxs-lookup"><span data-stu-id="2f93e-163">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="2f93e-164">Para obtener más información, consulte [configuración de rutas de voz para llamadas salientes en Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span><span class="sxs-lookup"><span data-stu-id="2f93e-164">For more information, see [Configuring voice routes for outbound calls in Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span></span>


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
<th></th>
<th><span data-ttu-id="2f93e-165">Ruta de voz 1</span><span class="sxs-lookup"><span data-stu-id="2f93e-165">Voice route 1</span></span></th>
<th><span data-ttu-id="2f93e-166">Ruta de voz 2</span><span class="sxs-lookup"><span data-stu-id="2f93e-166">Voice route 2</span></span></th>
<th><span data-ttu-id="2f93e-167">Ruta de voz 3</span><span class="sxs-lookup"><span data-stu-id="2f93e-167">Voice route 3</span></span></th>
<th><span data-ttu-id="2f93e-168">Ruta de voz 4</span><span class="sxs-lookup"><span data-stu-id="2f93e-168">Voice route 4</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f93e-169">Nombre</span><span class="sxs-lookup"><span data-stu-id="2f93e-169">Name</span></span></p></td>
<td><p><span data-ttu-id="2f93e-170">Ruta de Delhi</span><span class="sxs-lookup"><span data-stu-id="2f93e-170">Delhi route</span></span></p></td>
<td><p><span data-ttu-id="2f93e-171">Ruta de Hyderabad</span><span class="sxs-lookup"><span data-stu-id="2f93e-171">Hyderabad route</span></span></p></td>
<td><p><span data-ttu-id="2f93e-172">PBX del camino</span><span class="sxs-lookup"><span data-stu-id="2f93e-172">PBX Del route</span></span></p></td>
<td><p><span data-ttu-id="2f93e-173">Ruta de HYD PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-173">PBX Hyd route</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f93e-174">Usos de RTC</span><span class="sxs-lookup"><span data-stu-id="2f93e-174">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="2f93e-175">Uso de Delhi</span><span class="sxs-lookup"><span data-stu-id="2f93e-175">Delhi usage</span></span></p></td>
<td><p><span data-ttu-id="2f93e-176">Uso de Hyderabad</span><span class="sxs-lookup"><span data-stu-id="2f93e-176">Hyderabad usage</span></span></p></td>
<td><p><span data-ttu-id="2f93e-177">Uso de PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-177">PBX Del usage</span></span></p></td>
<td><p><span data-ttu-id="2f93e-178">Uso de HYD de PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-178">PBX Hyd usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f93e-179">Tronco</span><span class="sxs-lookup"><span data-stu-id="2f93e-179">Trunk</span></span></p></td>
<td><p><span data-ttu-id="2f93e-180">Tronco 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="2f93e-180">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="2f93e-181">Troncal 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="2f93e-181">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="2f93e-182">Troncal 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-182">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="2f93e-183">Troncal 4 HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="2f93e-183">Trunk 4 HYD-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-users-for-enterprise-voice"></a><span data-ttu-id="2f93e-184">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="2f93e-184">Enable Users for Enterprise Voice</span></span>

<span data-ttu-id="2f93e-185">Habilitar a los usuarios para la telefonía IP empresarial y asignarles una directiva de voz que haya definido previamente.</span><span class="sxs-lookup"><span data-stu-id="2f93e-185">Enable users for Enterprise Voice and assign them a voice policy you’ve previously defined.</span></span> <span data-ttu-id="2f93e-186">En este ejemplo, la tabla siguiente muestra la asignación que se usa en este escenario.</span><span class="sxs-lookup"><span data-stu-id="2f93e-186">For this example, the following table illustrates the assignment used in this scenario.</span></span> <span data-ttu-id="2f93e-187">En la tabla solo se incluyen los valores específicos de Location-Based enrutamiento, con fines de ilustración.</span><span class="sxs-lookup"><span data-stu-id="2f93e-187">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="2f93e-188">Para obtener más información, consulte [Habilitar usuarios para telefonía IP empresarial en Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span><span class="sxs-lookup"><span data-stu-id="2f93e-188">For more information, see [Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2f93e-189">Usuarios ubicados en Delhi</span><span class="sxs-lookup"><span data-stu-id="2f93e-189">Users located in Delhi</span></span></th>
<th><span data-ttu-id="2f93e-190">Usuarios que se encuentran en Hyderabad</span><span class="sxs-lookup"><span data-stu-id="2f93e-190">Users located in Hyderabad</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f93e-191">Directiva de voz asociada</span><span class="sxs-lookup"><span data-stu-id="2f93e-191">Associated voice policy</span></span></p></td>
<td><p><span data-ttu-id="2f93e-192">Directiva de voz de Delhi</span><span class="sxs-lookup"><span data-stu-id="2f93e-192">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="2f93e-193">Política de voz de Hyderabad</span><span class="sxs-lookup"><span data-stu-id="2f93e-193">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f93e-194">Usuarios de muestra</span><span class="sxs-lookup"><span data-stu-id="2f93e-194">Sample users</span></span></p></td>
<td><p><span data-ttu-id="2f93e-195">DE-LYNC-1, DE-LYNC-2, DE-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="2f93e-195">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
<td><p><span data-ttu-id="2f93e-196">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="2f93e-196">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2f93e-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f93e-197">See Also</span></span>


[<span data-ttu-id="2f93e-198">Configurar el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f93e-198">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="2f93e-199"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2f93e-199"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

