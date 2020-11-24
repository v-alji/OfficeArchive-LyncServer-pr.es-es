---
title: Usar los paquetes de administración de Lync Server 2010 en un escenario de coexistencia
description: Usar los paquetes de administración de Lync Server 2010 en un escenario de coexistencia.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Lync Server 2010 management packs in a coexistence scenario
ms:assetid: 8b792503-bd88-47fe-9d97-b071e8d429a5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205078(v=OCS.15)
ms:contentKeyID: 48184772
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5f6e76f49b74badd0f40d115101abb38aa35172
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400128"
---
# <a name="using-the-lync-server-2010-management-packs-in-a-coexistence-scenario"></a><span data-ttu-id="d02ab-103">Usar los paquetes de administración de Lync Server 2010 en un escenario de coexistencia</span><span class="sxs-lookup"><span data-stu-id="d02ab-103">Using the Lync Server 2010 management packs in a coexistence scenario</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d02ab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d02ab-104">

<span> </span></span></span>

<span data-ttu-id="d02ab-105">_**Última modificación del tema:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="d02ab-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="d02ab-106">Muchos clientes adoptan un programa de implementación dentro de sus empresas en el que los usuarios se migran progresivamente desde Microsoft Lync Server 2010 a Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d02ab-106">Many customers adopt a rollout program inside of their enterprises in which users are progressively migrated from Microsoft Lync Server 2010 to Lync Server 2013.</span></span> <span data-ttu-id="d02ab-107">Los administradores de estas empresas se interesan en la supervisión de ambas versiones de Lync Server para garantizar que todos los usuarios finales obtengan la mejor experiencia de comunicación posible.</span><span class="sxs-lookup"><span data-stu-id="d02ab-107">The administrators at these companies will care about monitoring both versions of Lync Server to help ensure that all of their end users are getting the best possible communication experience.</span></span> <span data-ttu-id="d02ab-108">Para este escenario, el paquete de administración de Lync Server 2013 admite una ruta de migración en paralelo con el módulo de administración de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d02ab-108">For this scenario, the Lync Server 2013 Management Pack supports a side-by-side migration path with the Lync Server 2010 Management Pack.</span></span>

<span data-ttu-id="d02ab-109">En Lync Server 2010, los equipos de Lync Server se detectaron a través del documento de topología almacenado con el almacén central de administración.</span><span class="sxs-lookup"><span data-stu-id="d02ab-109">In the Lync Server 2010, Lync Server computers were discovered through the topology document stored with the Central Management store.</span></span> <span data-ttu-id="d02ab-110">En esta configuración, un único equipo notificaría la existencia de todos los demás equipos de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d02ab-110">In this configuration, a single computer would report the existence of all the other Lync Server computers.</span></span>

<span data-ttu-id="d02ab-111">Los módulos de administración para Lync Server 2013 ahora usan la detección a nivel de equipo en lugar del mecanismo de detección central que se usó en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d02ab-111">The management packs for Lync Server 2013 now use machine-level discovery instead of the central discovery mechanism that was used in Lync Server 2010.</span></span> <span data-ttu-id="d02ab-112">Esto significa que cada agente de System Center se descubre por sí mismo e informa de su existencia en System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="d02ab-112">This means that each System Center agent essentially discovers itself and reports its existence to System Center Operations Manager.</span></span> <span data-ttu-id="d02ab-113">El uso de detección en el nivel de equipo simplifica la administración de la infraestructura de System Center y también permite que las distintas versiones de los paquetes de administración de Lync Server (por ejemplo, los módulos de administración de Lync Server 2010 y los paquetes de administración de Lync Server 2013) puedan coexistir más fácilmente.</span><span class="sxs-lookup"><span data-stu-id="d02ab-113">Using machine-level discovery simplifies administration of your System Center infrastructure and also enables different versions of the Lync Server management packs (for example, management packs for Lync Server 2010 and management packs for Lync Server 2013) to coexist more easily.</span></span>

<span data-ttu-id="d02ab-114">Para admitir esta migración, primero deberá actualizar la supervisión de Lync Server 2010 existente para evitar lagunas en la cobertura.</span><span class="sxs-lookup"><span data-stu-id="d02ab-114">To support this migration, you will first need to upgrade your existing Lync Server 2010 monitoring to avoid gaps in coverage.</span></span> <span data-ttu-id="d02ab-115">Para ello, elija un equipo de Lync Server 2010 existente para que sea servicio del script de detección central de Lync Server 2010 antes de actualizar su almacén de administración central a Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d02ab-115">To do this, elect an existing Lync Server 2010 computer to service the Central Discovery script for the Lync Server 2010 before upgrading your Central Management store to Lync Server 2013.</span></span> <span data-ttu-id="d02ab-116">Este es un proceso de cuatro pasos:</span><span class="sxs-lookup"><span data-stu-id="d02ab-116">This is a four-step process:</span></span>

1.  <span data-ttu-id="d02ab-117">Actualice los paquetes de administración de Lync Server 2010 a la actualización acumulativa 7.</span><span class="sxs-lookup"><span data-stu-id="d02ab-117">Upgrade the Lync Server 2010 Management Packs to Cumulative Update 7.</span></span>

2.  <span data-ttu-id="d02ab-118">Indique a un equipo de Lync Server 2010 que ejecute el script de detección central.</span><span class="sxs-lookup"><span data-stu-id="d02ab-118">Instruct a Lync Server 2010 computer to run the Central Discovery script.</span></span>

3.  <span data-ttu-id="d02ab-119">Invalide el candidato de detección central en el módulo de administración de Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d02ab-119">Override the Central Discovery Candidate in the Microsoft Lync Server 2010 Management Pack.</span></span>

4.  <span data-ttu-id="d02ab-120">Compruebe que se ha descubierto el nuevo candidato de detección central.</span><span class="sxs-lookup"><span data-stu-id="d02ab-120">Verify that the new Central Discovery Candidate has been discovered.</span></span>

<div>

## <a name="instructing-a-lync-server-2010-computer-to-run-the-central-discovery-script"></a><span data-ttu-id="d02ab-121">Instrucciones para que un equipo de Lync Server 2010 ejecute el script de detección central</span><span class="sxs-lookup"><span data-stu-id="d02ab-121">Instructing a Lync Server 2010 Computer to Run the Central Discovery script</span></span>

<span data-ttu-id="d02ab-122">Para designar un equipo de almacenamiento de administración no central (por ejemplo, un servidor front-end de Lync Server) para controlar la detección centralizada, tendrá que crear la siguiente clave de registro en el servidor de almacenamiento de administración no central:</span><span class="sxs-lookup"><span data-stu-id="d02ab-122">To nominate a non-Central Management store computer (for example, a Lync Server Front End) server to handle central discovery, you will need to create the following registry key on the non-Central Management store server:</span></span>

<span data-ttu-id="d02ab-123">\\Software HKLM \\ \\ CentralDiscoveryCandidate de salud de las comunicaciones en tiempo real de Microsoft \\ \\</span><span class="sxs-lookup"><span data-stu-id="d02ab-123">HKLM\\Software\\Microsoft\\Real-Time Communications\\Health\\CentralDiscoveryCandidate</span></span>

<span data-ttu-id="d02ab-124">Puede crear esta clave del registro completando el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="d02ab-124">You can create this registry key by completing the following procedure:</span></span>

1.  <span data-ttu-id="d02ab-125">Haga clic en **Inicio** y, después, en **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-125">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="d02ab-126">En el cuadro de diálogo **Ejecutar** , escriba **regedit** y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="d02ab-126">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="d02ab-127">En el editor del registro, expanda el **\_ \_ equipo local HKEY**, expanda **software**, expanda **Microsoft** y, a continuación, expanda **comunicaciones en tiempo real**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-127">In Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SOFTWARE**, expand **Microsoft**, and then expand **Real-Time Communications**.</span></span>

4.  <span data-ttu-id="d02ab-128">Haga clic con el botón derecho en **mantenimiento**, seleccione **nuevo** y, a continuación, haga clic en **clave**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-128">Right-click **Health**, click **New**, and then click **Key**.</span></span> <span data-ttu-id="d02ab-129">Si la clave de **Estado** no existe, haga clic con el botón secundario en **comunicaciones en tiempo real**, seleccione **nuevo** y, a continuación, haga clic en **clave**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-129">If the **Health** key does not exist, then right-click **Real-Time Communications**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="d02ab-130">Cuando se cree la nueva clave, escriba Health y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="d02ab-130">When the new key is created, type Health, and then press ENTER.</span></span>
    
    <span data-ttu-id="d02ab-131">Una vez creada la nueva clave, escriba **CentralDiscoveryCandidate** y, a continuación, presione Entrar para cambiar el nombre de la clave.</span><span class="sxs-lookup"><span data-stu-id="d02ab-131">After the new key has been created, type **CentralDiscoveryCandidate** and then press ENTER to rename the key.</span></span>

<span data-ttu-id="d02ab-132">Es posible que tarde el equipo varias horas en detectar este cambio.</span><span class="sxs-lookup"><span data-stu-id="d02ab-132">It may take the computer several hours to pick up this change.</span></span> <span data-ttu-id="d02ab-133">Para que el cambio surta efecto inmediatamente, detenga y reinicie el servicio de agente de estado.</span><span class="sxs-lookup"><span data-stu-id="d02ab-133">To make the change take effect immediately, stop and then restart the Health Agent service.</span></span> <span data-ttu-id="d02ab-134">Para reiniciar el servicio agente de estado, complete el procedimiento siguiente en el equipo con Lync Server 2010:</span><span class="sxs-lookup"><span data-stu-id="d02ab-134">To restart the Health Agent service, complete the following procedure on the Lync Server 2010 computer:</span></span>

1.  <span data-ttu-id="d02ab-135">Haga clic en **Inicio**, seleccione **todos los programas**, **accesorios**, haga clic con el botón derecho en **símbolo del sistema** y, a continuación, haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-135">Click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="d02ab-136">En la ventana de consola, escriba el siguiente comando y, a continuación, presione ENTRAR:</span><span class="sxs-lookup"><span data-stu-id="d02ab-136">In the console window, type the following command and then press ENTER:</span></span>
    
        Net stop HealthService

3.  <span data-ttu-id="d02ab-137">Verá un mensaje que indica "el servicio de administración de System Center se está deteniendo" seguido de un segundo mensaje que le indica que el servicio se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="d02ab-137">You will see a message that states "The System Center Management service is stopping," followed by a second message that tells you that the service has been stopped.</span></span> <span data-ttu-id="d02ab-138">Una vez que el servicio se haya detenido, puede reiniciarlo escribiendo el siguiente comando y presionando entrar:</span><span class="sxs-lookup"><span data-stu-id="d02ab-138">After the service has stopped, you can restart it by typing the following command and pressing ENTER:</span></span>
    
        Net start HealthService

</div>

<div>

## <a name="overriding-the-central-discovery-candidate-in-the-lync-server-2010-management-pack"></a><span data-ttu-id="d02ab-139">Reemplazar el candidato de detección central en el módulo de administración de Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="d02ab-139">Overriding the Central Discovery Candidate in the Lync Server 2010 Management Pack</span></span>

<span data-ttu-id="d02ab-140">Después de indicar a un equipo de Lync Server 2010 que informe sobre los equipos de Lync Server 2010, tendrá que informar también al módulo de administración de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d02ab-140">After instructing a Lync Server 2010 computer to report on Lync Server 2010 computers, you will need to inform the Lync Server 2010 Management Pack about this change as well.</span></span> <span data-ttu-id="d02ab-141">Para ello, tendrá que crear un reemplazo en el módulo de administración.</span><span class="sxs-lookup"><span data-stu-id="d02ab-141">To do this, you will need to create an override in the Management Pack.</span></span> <span data-ttu-id="d02ab-142">Esto se puede realizar mediante el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="d02ab-142">That can be done by completing the following procedure:</span></span>

1.  <span data-ttu-id="d02ab-143">En la consola de Operations Manager, haga clic en **creación**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-143">In the Operations Manager console, click **Authoring**.</span></span>

2.  <span data-ttu-id="d02ab-144">En la pestaña creación, expanda **objetos del módulo de administración**, haga clic en **descubrimientos de objetos** y, a continuación, haga clic en **ámbito**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-144">On the Authoring tab, expand **Management Pack Objects**, click **Object Discoveries**, and then click **Scope**.</span></span>

3.  <span data-ttu-id="d02ab-145">En el cuadro de diálogo **objetos del módulo de administración del ámbito** , seleccione el elemento con el candidato de detección de **LS** de destino y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-145">In the **Scope Management Pack Objects** dialog box, select the item with the Target **LS Discovery Candidate** and then click **OK**.</span></span> <span data-ttu-id="d02ab-146">Tenga en cuenta que el candidato de detección de LS solo aparecerá si ha instalado el módulo de administración de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d02ab-146">Note that LS Discovery Candidate will appear only if you have installed the Lync Server 2010 Management Pack.</span></span>

4.  <span data-ttu-id="d02ab-147">En la consola de Operations Manager, haga clic con el botón secundario del mouse en la **detección de LS**, **Seleccione reemplazos, seleccione** **invalidar la detección de objetos** y, a continuación, haga clic en **para todos los objetos de clase: candidato de detección de LS**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-147">In the Operations Manager console, right-click **LS Discovery Candidate**, point to **Overrides**, point to **Override the Object Discovery**, and then click **For all objects of class: LS Discovery Candidate**.</span></span>

5.  <span data-ttu-id="d02ab-148">En el cuadro de diálogo **reemplazar propiedades** , seleccione la casilla **invalidar** situada junto al parámetro de **descubrimiento central WatcherNode FQDN**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-148">In the **Override Properties** dialog box, select the **Override** check box next to the parameter **Central Discovery WatcherNode Fqdn**.</span></span> <span data-ttu-id="d02ab-149">Escriba el nombre de dominio completo del equipo de Lync Server 2010 en los cuadros **valor de reemplazo** y **valor efectivo** .</span><span class="sxs-lookup"><span data-stu-id="d02ab-149">Type the fully qualified domain name of the Lync Server 2010 computer in the **Override Value** and **Effective Value** boxes.</span></span> <span data-ttu-id="d02ab-150">Seleccione la casilla **exigido** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-150">Select the **Enforced** check box and click **OK**.</span></span>

<span data-ttu-id="d02ab-151">Una vez que haya creado el reemplazo, debe reiniciar el servicio de mantenimiento en el servidor de administración raíz.</span><span class="sxs-lookup"><span data-stu-id="d02ab-151">After you have created the override, you need to restart the health service on the Root Management Server.</span></span> <span data-ttu-id="d02ab-152">Para reiniciar el servicio de mantenimiento, complete el procedimiento siguiente en el servidor de administración raíz:</span><span class="sxs-lookup"><span data-stu-id="d02ab-152">To restart the health service, complete the following procedure on the Root Management Server:</span></span>

1.  <span data-ttu-id="d02ab-153">Haga clic en **Inicio**, seleccione **todos los programas**, **accesorios**, haga clic con el botón derecho en **símbolo del sistema** y, a continuación, haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-153">Click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="d02ab-154">En la ventana de consola, escriba el siguiente comando y, a continuación, presione ENTRAR:</span><span class="sxs-lookup"><span data-stu-id="d02ab-154">In the console window, type the following command, and then press ENTER:</span></span>
    
        Net stop HealthService

3.  <span data-ttu-id="d02ab-155">Verá un mensaje en el que se indica que "el servicio de administración de System Center se está deteniendo" seguido de un segundo mensaje que le indica que el servicio se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="d02ab-155">You will see a message stating that "The System Center Management service is stopping," followed by a second message that tells you that the service has been stopped.</span></span> <span data-ttu-id="d02ab-156">Después de que el servicio se haya detenido, puede reiniciarlo escribiendo el siguiente comando y presionando entrar:</span><span class="sxs-lookup"><span data-stu-id="d02ab-156">After the service has stopped, you can then restart it by typing the following command and pressing ENTER:</span></span>
    
        Net start HealthService

</div>

<div>

## <a name="verifying-that-the-new-central-discovery-candidate-was-discovered"></a><span data-ttu-id="d02ab-157">Comprobar que se detectó el nuevo candidato de detección central</span><span class="sxs-lookup"><span data-stu-id="d02ab-157">Verifying that the New Central Discovery Candidate Was Discovered</span></span>

<span data-ttu-id="d02ab-158">El paso final antes de actualizar el almacén de administración central es asegurarse de que el nuevo candidato de detección central fue descubierto por el módulo de administración de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d02ab-158">The final step before upgrading Central Management store is to make sure that the new central discovery candidate was discovered by the Lync Server 2010 Management Pack.</span></span> <span data-ttu-id="d02ab-159">Para ello, abra la consola de Operations Manager y, a continuación, haga clic en supervisión.</span><span class="sxs-lookup"><span data-stu-id="d02ab-159">To do this, open the Operations Manager console and then click Monitoring.</span></span> <span data-ttu-id="d02ab-160">En la pestaña supervisión, expanda **estado 2010 de Microsoft Lync Server**, expanda **descubrimiento de topología** y, a continuación, haga clic en **vista estado de detección**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-160">On the Monitoring tab, expand **Microsoft Lync Server 2010 Health**, expand **Topology Discovery**, and then click **Discovery State View**.</span></span> <span data-ttu-id="d02ab-161">Compruebe que una fila de la pantalla tiene una **ruta de acceso** que indica el nombre de dominio completo del candidato de detección central.</span><span class="sxs-lookup"><span data-stu-id="d02ab-161">Verify that a row in the display has a **Path** that lists the fully qualified domain name of the central discovery candidate.</span></span> <span data-ttu-id="d02ab-162">También debe verificar que el estado del equipo sea **correcto**.</span><span class="sxs-lookup"><span data-stu-id="d02ab-162">You should also verify that the computer state is reported as **Healthy**.</span></span>

<span data-ttu-id="d02ab-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d02ab-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

