---
title: 'Lync Server 2013: probar la configuración del nodo de monitor'
description: 'Lync Server 2013: probar la configuración del nodo de monitor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing watcher node configuration
ms:assetid: f9ecd85c-0ae9-4906-b786-6b002b5a77c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn751537(v=OCS.15)
ms:contentKeyID: 63969667
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1eeb141eee011d7e06f5dd49e483e026484d733
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440930"
---
# <a name="testing-watcher-node-configuration-in-lync-server-2013"></a><span data-ttu-id="09665-103">Probar la configuración del nodo de monitor en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09665-103">Testing watcher node configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09665-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09665-104">

<span> </span></span></span>

<span data-ttu-id="09665-105">_**Última modificación del tema:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="09665-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09665-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="09665-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="09665-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="09665-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09665-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="09665-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="09665-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="09665-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09665-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="09665-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="09665-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="09665-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="09665-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe asignar un rol de RBAC que tenga permiso para ejecutar el cmdlet <strong>Test-CsWatcherNodeConfiguration</strong> .</span><span class="sxs-lookup"><span data-stu-id="09665-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsWatcherNodeConfiguration</strong> cmdlet.</span></span> <span data-ttu-id="09665-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="09665-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot; Test-CsWatcherNodeConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="09665-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="09665-114">Description</span></span>

<span data-ttu-id="09665-115">Si usa Microsoft System Center Operations Manager para supervisar Lync Server 2013, tendrá la opción de configurar "nodos de monitor": equipos que ejecutan de forma periódica y automática transacciones sintéticas para comprobar que Lync Server funciona según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="09665-115">If you are using Microsoft System Center Operations Manager to monitor Lync Server 2013 then you have the option of setting up "watcher nodes": computers that periodically, and automatically, run synthetic transactions to verify that Lync Server is working as expected.</span></span> <span data-ttu-id="09665-116">Los nodos de monitor se asignan a grupos y se administran mediante los cmdlets de **CsWatcherNodeConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="09665-116">Watcher nodes are assigned to pools, and are managed by using the **CsWatcherNodeConfiguration** cmdlets.</span></span> <span data-ttu-id="09665-117">Tenga en cuenta que no necesita instalar nodos de monitor si está usando System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="09665-117">Note that you do not need to install watcher nodes if you are using System Center Operations Manager.</span></span> <span data-ttu-id="09665-118">Aún puede supervisar el sistema sin usar nodos de monitor.</span><span class="sxs-lookup"><span data-stu-id="09665-118">You can still monitor your system without using watcher nodes.</span></span> <span data-ttu-id="09665-119">La única diferencia es que cualquier transacción sintética que desee ejecutar debe invocarse manualmente en lugar de invocarse de forma automática por parte de Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="09665-119">The only difference is that any synthetic transactions that you want to run must be invoked manually instead of automatically invoked by Operations Manager.</span></span>

<span data-ttu-id="09665-120">El cmdlet **Test-CsWatcherNodeConfiguration** le permite comprobar que un nodo de monitor se ha configurado correctamente y se asigna a un grupo de servidores de Lync Server 2013 válido.</span><span class="sxs-lookup"><span data-stu-id="09665-120">The **Test-CsWatcherNodeConfiguration** cmdlet enables you to verify that a watcher node was configured correctly and is assigned to a valid Lync Server 2013 pool.</span></span> <span data-ttu-id="09665-121">Tenga en cuenta que el cmdlet **Test-CsWatcherNodeConfiguration** debe ejecutarse en el nodo de monitor en sí.</span><span class="sxs-lookup"><span data-stu-id="09665-121">Note that the **Test-CsWatcherNodeConfiguration** cmdlet must be run on the watcher node itself.</span></span> <span data-ttu-id="09665-122">El cmdlet no se puede ejecutar en equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="09665-122">The cmdlet cannot be run against remote computers.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="09665-123">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="09665-123">Running the test</span></span>

<span data-ttu-id="09665-124">El siguiente comando comprueba la configuración de cada nodo de monitor que se usa en la organización.</span><span class="sxs-lookup"><span data-stu-id="09665-124">The following command verifies the configuration settings for each watcher node that is being used in the organization.</span></span>

    Test-CsWatcherNodeConfiguration

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="09665-125">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="09665-125">Determining success or failure</span></span>

<span data-ttu-id="09665-126">La siguiente salida de ejemplo correcta muestra un sistema con cuatro servidores perimetrales.</span><span class="sxs-lookup"><span data-stu-id="09665-126">The following successful sample output shows a system with four edge servers.</span></span>

<span data-ttu-id="09665-127">Validando la atl-cs-001.litwareinc.com del grupo de destino en topología.</span><span class="sxs-lookup"><span data-stu-id="09665-127">Validating target pool atl-cs-001.litwareinc.com against topology.</span></span>

<span data-ttu-id="09665-128">Correcto: la atl-cs-001.litwareinc.com del grupo de destino existe en la topología.</span><span class="sxs-lookup"><span data-stu-id="09665-128">Success: Target pool atl-cs-001.litwareinc.com exists in topology.</span></span>

<span data-ttu-id="09665-129">Correcto: el atl-cs-001.litwareinc.com del grupo de destino tiene el rol de registrador instalado.</span><span class="sxs-lookup"><span data-stu-id="09665-129">Success: Target pool atl-cs-001.litwareinc.com has Registrar role installed.</span></span>

<span data-ttu-id="09665-130">Correcto: la versión del grupo de atl-cs-001.litwareinc.com es compatible.</span><span class="sxs-lookup"><span data-stu-id="09665-130">Success: Target pool atl-cs-001.litwareinc.com is supported version.</span></span>

<span data-ttu-id="09665-131">Éxito: el número de puerto para la atl-cs-001.litwareinc.com del grupo de destino 5061 es correcto.</span><span class="sxs-lookup"><span data-stu-id="09665-131">Success: Port number for 5061 Target pool atl-cs-001.litwareinc.com is correct.</span></span>

<span data-ttu-id="09665-132">Se ha iniciado la búsqueda de grupos que faltan en la configuración del nodo de monitor.</span><span class="sxs-lookup"><span data-stu-id="09665-132">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="09665-133">Si se detecta cualquier error, se imprimirá.</span><span class="sxs-lookup"><span data-stu-id="09665-133">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="09665-134">Se ha finalizado la búsqueda de grupos que faltan en la configuración del nodo de monitor.</span><span class="sxs-lookup"><span data-stu-id="09665-134">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="09665-135">Se ha iniciado la comprobación de las claves del registro del nodo de monitor creadas por la instalación del nodo de monitor.</span><span class="sxs-lookup"><span data-stu-id="09665-135">Checking for watcher node registry keys created by watcher node installation, is started.</span></span> <span data-ttu-id="09665-136">Si se detecta cualquier error, se imprimirá.</span><span class="sxs-lookup"><span data-stu-id="09665-136">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="09665-137">La comprobación de las claves del registro del nodo de monitor creadas por la instalación del nodo de monitor ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="09665-137">Checking for watcher node registry keys created by watcher node installation, is finished.</span></span> <span data-ttu-id="09665-138">El tipo de autenticación detectada es Negotiate.</span><span class="sxs-lookup"><span data-stu-id="09665-138">Detected authentication type is Negotiate.</span></span>

<span data-ttu-id="09665-139">La existencia del SIP de credenciales del usuario de prueba se validó correctamente: user1@ atl-cs-001.litwareinc.com en el almacén de administración de credenciales.</span><span class="sxs-lookup"><span data-stu-id="09665-139">Successfully validated existence of test user’s credential sip:user1@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="09665-140">La existencia del SIP de credenciales del usuario de prueba se validó correctamente: user2@ atl-cs-001.litwareinc.com en el almacén de administración de credenciales.</span><span class="sxs-lookup"><span data-stu-id="09665-140">Successfully validated existence of test user’s credential sip:user2@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="09665-141">Se ha iniciado la búsqueda de grupos que faltan en la configuración del nodo de monitor.</span><span class="sxs-lookup"><span data-stu-id="09665-141">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="09665-142">Si se detecta cualquier error, se imprimirá.</span><span class="sxs-lookup"><span data-stu-id="09665-142">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="09665-143">ADVERTENCIA: el atl-cs-001.litwareinc.com de grupo tiene registrador</span><span class="sxs-lookup"><span data-stu-id="09665-143">WARNING: Pool atl-cs-001.litwareinc.com has Registrar</span></span>

<span data-ttu-id="09665-144">rol instalado, pero no hay ningún usuario de prueba configurado para él.</span><span class="sxs-lookup"><span data-stu-id="09665-144">role installed, but there are no test users configured for it.</span></span>

<span data-ttu-id="09665-145">Se ha finalizado la búsqueda de grupos que faltan en la configuración del nodo de monitor.</span><span class="sxs-lookup"><span data-stu-id="09665-145">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="09665-146">La comprobación de las claves del registro del nodo de monitor creadas por la instalación del nodo de monitor es</span><span class="sxs-lookup"><span data-stu-id="09665-146">Checking for watcher node registry keys created by watcher node installation, is</span></span>

<span data-ttu-id="09665-147">Comience.</span><span class="sxs-lookup"><span data-stu-id="09665-147">started.</span></span> <span data-ttu-id="09665-148">Si se detecta cualquier error, se imprimirá.</span><span class="sxs-lookup"><span data-stu-id="09665-148">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="09665-149">Test-CsWatcherNodeConfiguration: no se puede encontrar la clave del registro de estado en</span><span class="sxs-lookup"><span data-stu-id="09665-149">Test-CsWatcherNodeConfiguration : Cannot find Health registry key in</span></span>

<span data-ttu-id="09665-150">Software \\ \\ comunicaciones en tiempo real de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09665-150">Software\\Microsoft\\Real-Time Communications.</span></span> <span data-ttu-id="09665-151">Asegúrese de que el nodo Monitor. msi está</span><span class="sxs-lookup"><span data-stu-id="09665-151">Make sure watcher node .msi is</span></span>

<span data-ttu-id="09665-152">instalado correctamente.</span><span class="sxs-lookup"><span data-stu-id="09665-152">installed properly.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="09665-153">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="09665-153">Reasons why the test might have failed</span></span>

<span data-ttu-id="09665-154">Estas son algunas de las razones comunes por las que **Test-CsWatcherNodeConfiguration** podría fallar:</span><span class="sxs-lookup"><span data-stu-id="09665-154">Here are some common reasons why **Test-CsWatcherNodeConfiguration** might fail:</span></span>

  - <span data-ttu-id="09665-155">El nodo de monitor no está correctamente instalado.</span><span class="sxs-lookup"><span data-stu-id="09665-155">Watcher node is not correctly installed.</span></span>

  - <span data-ttu-id="09665-156">No hay ningún usuario de prueba configurado.</span><span class="sxs-lookup"><span data-stu-id="09665-156">No test users are configured.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="09665-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="09665-157">See Also</span></span>


[<span data-ttu-id="09665-158">Get-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="09665-158">Get-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsWatcherNodeConfiguration)  
[<span data-ttu-id="09665-159">New-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="09665-159">New-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsWatcherNodeConfiguration)  
[<span data-ttu-id="09665-160">Remove-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="09665-160">Remove-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsWatcherNodeConfiguration)  
[<span data-ttu-id="09665-161">Set-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="09665-161">Set-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWatcherNodeConfiguration)  
  

<span data-ttu-id="09665-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09665-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

