---
title: 'Lync Server 2013: instalación de los módulos de administración de Lync Server 2013'
description: 'Lync Server 2013: instalación de los módulos de administración de Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: nstalling the Lync Server 2013 management packs
ms:assetid: b800d4ab-fdc8-4c72-a76a-b78932779fe3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205202(v=OCS.15)
ms:contentKeyID: 48185233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cbb50146474211c12dbd95801ed2b20f6bbfd8c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426931"
---
# <a name="installing-the-lync-server-2013-management-packs"></a><span data-ttu-id="df3f4-103">Instalar los módulos de administración de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df3f4-103">Installing the Lync Server 2013 management packs</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="df3f4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="df3f4-104">

<span> </span></span></span>

<span data-ttu-id="df3f4-105">_**Última modificación del tema:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="df3f4-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="df3f4-106">Por sí solo, System Center Operations Manager tiene la capacidad de supervisar solo una pequeña parte del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="df3f4-106">By itself, System Center Operations Manager has the ability to monitor only a small portion of the Windows operating system.</span></span> <span data-ttu-id="df3f4-107">Sin embargo, puede ampliar las capacidades de System Center Operations Manager mediante la instalación de paquetes de administración, software que determina los elementos que System Center Operations Manager puede supervisar, incluido cómo se deben supervisar esos elementos y cómo se deberían desencadenar y notificar las alertas.</span><span class="sxs-lookup"><span data-stu-id="df3f4-107">However, you can extend the capabilities of System Center Operations Manager by installing management packs, software that dictates which items System Center Operations Manager can monitor, including how those items should be monitored and how alerts should be triggered and reported.</span></span> <span data-ttu-id="df3f4-108">Microsoft Lync Server 2013 incluye dos módulos de administración de System Center Operations Manager que proporcionan las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="df3f4-108">Microsoft Lync Server 2013 includes two System Center Operations Manager management packs that provide the following capabilities:</span></span>

  - <span data-ttu-id="df3f4-109">El módulo de administración de componentes y usuarios (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) realiza un seguimiento de los problemas de Lync Server registrados en registros de eventos, registrados por contadores de rendimiento o registrados en las bases de datos de registros de detalles de llamadas (CDR) o de la calidad de la experiencia (QoE).</span><span class="sxs-lookup"><span data-stu-id="df3f4-109">The Component and User Management Pack (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) tracks Lync Server issues recorded in event logs, registered by performance counters, or logged in the call detail records (CDR) or the Quality of Experience (QoE) databases.</span></span> <span data-ttu-id="df3f4-110">En el caso de problemas críticos, System Center Operations Manager se puede configurar para que notifiquen inmediatamente a los administradores a través de mensajes de correo electrónico, mensajes instantáneos o mensajes SMS.</span><span class="sxs-lookup"><span data-stu-id="df3f4-110">For critical problems, System Center Operations Manager can be configured to immediately notify administrators via email, instant message, or Short Message Service (SMS) messaging.</span></span> <span data-ttu-id="df3f4-111">SMS es la tecnología que se usa para enviar mensajes de texto desde un dispositivo móvil a otro.</span><span class="sxs-lookup"><span data-stu-id="df3f4-111">SMS is the technology used to send text messages from one mobile device to another.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="df3f4-112">Para obtener más información sobre la configuración de notificaciones de Operations Manager, vea Configurar notificaciones en la biblioteca de TechNet en <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?linkid=268785</A> .</span><span class="sxs-lookup"><span data-stu-id="df3f4-112">For more information on configuring Operations Manager notification, see Configuring Notification in the TechNet Library at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?linkid=268785</A>.</span></span>

    
    </div>

  - <span data-ttu-id="df3f4-113">El paquete de supervisión activa (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) prueba de forma proactiva componentes de Lync Server clave como iniciar sesión en el sistema, intercambiar mensajes instantáneos o hacer llamadas a un teléfono que se encuentra en la red de telefonía pública conmutada (RTC).</span><span class="sxs-lookup"><span data-stu-id="df3f4-113">The Active Monitoring Pack (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) proactively tests key Lync Server components such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="df3f4-114">Estas pruebas se realizan mediante los cmdlets de transacciones sintéticas de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="df3f4-114">These tests are conducted using the Lync Server synthetic transaction cmdlets.</span></span> <span data-ttu-id="df3f4-115">Por ejemplo, el cmdlet **Test-CsIM** se usa para simular una conversación de mensajería instantánea entre dos usuarios de prueba.</span><span class="sxs-lookup"><span data-stu-id="df3f4-115">For example, the **Test-CsIM** cmdlet is used to simulate an instant messaging conversation between a pair of test users.</span></span> <span data-ttu-id="df3f4-116">Si se produce un error en esta conversación de mensajería simulada, se generará una alerta.</span><span class="sxs-lookup"><span data-stu-id="df3f4-116">If this simulated messaging conversation fails an alert will be generated.</span></span>

<span data-ttu-id="df3f4-117">Los dos módulos de administración incluidos en Lync Server 2013 incluyen un gran número de mejoras en los paquetes de administración que se usan con Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="df3f4-117">The two management packs included with Lync Server 2013 include a large number of enhancements over the management packs used with Microsoft Lync Server 2010.</span></span> <span data-ttu-id="df3f4-118">Por ejemplo, el módulo de administración de componentes de Lync Server 2013 no se limita a supervisar el servidor de Lync en sí.</span><span class="sxs-lookup"><span data-stu-id="df3f4-118">For example, the Lync Server 2013 Component Management Pack is not limited to monitoring Lync Server itself.</span></span> <span data-ttu-id="df3f4-119">Además de supervisar los registros de eventos y los contadores de rendimiento de Lync Server, el módulo de administración de componentes también puede realizar un seguimiento del rendimiento de elementos esenciales, como por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="df3f4-119">In addition to monitoring event logs and performance counters for Lync Server, the Component Management pack can also track the performance of, and issue alerts for, crucial items such as:</span></span>

  - <span data-ttu-id="df3f4-120">**Servicios de Internet Information Server (IIS)**   Las alertas se emitirán si Internet Information Services se desconecta.</span><span class="sxs-lookup"><span data-stu-id="df3f4-120">**Internet Information Services (IIS)**   Alerts will be issued if Internet Information Services goes offline.</span></span> <span data-ttu-id="df3f4-121">Esto es importante porque los servicios Web de Lync Server dependen de IIS.</span><span class="sxs-lookup"><span data-stu-id="df3f4-121">This is important, because the Lync Server web services rely on IIS.</span></span>

  - <span data-ttu-id="df3f4-122">**Uso del proceso**   Las alertas se emitirán si los recursos del sistema (como la memoria disponible) comienzan a agotarse.</span><span class="sxs-lookup"><span data-stu-id="df3f4-122">**Process usage**   Alerts will be issued if system resources (such as available memory) begin to run low.</span></span> <span data-ttu-id="df3f4-123">Estas alertas se emitirán incluso si Lync Server no es responsable del uso elevado del sistema.</span><span class="sxs-lookup"><span data-stu-id="df3f4-123">These alerts will be issued even if Lync Server is not responsible for the high system usage.</span></span>

  - <span data-ttu-id="df3f4-124">**Eventos de error de equipo**   Las alertas se emitirán en caso de un problema de hardware o software que amenace la viabilidad de un servidor.</span><span class="sxs-lookup"><span data-stu-id="df3f4-124">**Computer failure events**   Alerts will be issued in case of a hardware or software issue that threatens the viability of a server.</span></span> <span data-ttu-id="df3f4-125">Por ejemplo, los administradores de Lync Server recibirán una notificación si un servidor parece estar en peligro de experimentar un error en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="df3f4-125">For example, Lync Server administrators will be notified if a server appears to be in danger of experiencing a hard disk failure.</span></span>

<span data-ttu-id="df3f4-126">Los nuevos paquetes de administración también ofrecen informes mejorados.</span><span class="sxs-lookup"><span data-stu-id="df3f4-126">The new management packs also feature enhanced reporting.</span></span> <span data-ttu-id="df3f4-127">Los nuevos informes para Lync Server 2013 incluyen:</span><span class="sxs-lookup"><span data-stu-id="df3f4-127">New reports for Lync Server 2013 include:</span></span>

  - <span data-ttu-id="df3f4-128">**Informe de disponibilidad de escenario de principio a fin**   Este informe detalla la disponibilidad y el tiempo de actividad de los servicios clave de Lync Server, como el registro o la presencia.</span><span class="sxs-lookup"><span data-stu-id="df3f4-128">**End to End Scenario Availability Report**   This report details the availability/uptime for key Lync Server services such as registration or presence.</span></span>

  - <span data-ttu-id="df3f4-129">**Informe de capacidad**   Con la información de contador de rendimiento, este informe muestra tendencias de componentes del sistema, como la disponibilidad de memoria y el uso del procesador.</span><span class="sxs-lookup"><span data-stu-id="df3f4-129">**Capacity Report**   Using performance counter information, this report shows trends for system components such as memory availability and processor usage.</span></span>

  - <span data-ttu-id="df3f4-130">**Informe de componente**   Este informe muestra los principales generadores de alertas agrupados por el componente Lync Server.</span><span class="sxs-lookup"><span data-stu-id="df3f4-130">**Component Report**   This report lists the top alert generators grouped by Lync Server component.</span></span>

<span data-ttu-id="df3f4-131">Además de estos informes prediseñados, los módulos de administración para Lync Server 2013 automáticamente notifican las alertas de confiabilidad de llamadas (métricas medidas por la grabación de detalles de llamadas) y los Estados de QoE (métricas medidas según la calidad de la experiencia).</span><span class="sxs-lookup"><span data-stu-id="df3f4-131">In addition to these predesigned reports, the management packs for Lync Server 2013 automatically report alerts for both Call Reliability (metrics measured by Call Detail Recording) and QoE states (metrics measured by Quality of Experience).</span></span> <span data-ttu-id="df3f4-132">Si ha habilitado la grabación de detalles de llamadas, puede revisar las alertas de confiabilidad de llamadas completando el siguiente procedimiento de la consola de System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="df3f4-132">If you have enabled Call Detail Recording, you can review Call Reliability alerts by completing the following procedure from the System Center Operations Manager console:</span></span>

  - <span data-ttu-id="df3f4-133">Expanda **supervisión**, expanda **Estado 2013 de Microsoft Lync Server**, expanda **fiabilidad y calidad multimedia** y, después, haga clic en confiabilidad de la **llamada**.</span><span class="sxs-lookup"><span data-stu-id="df3f4-133">Expand **Monitoring**, expand **Microsoft Lync Server 2013 Health**, expand **Call Reliability and Media Quality**, and then click **Call Reliability**.</span></span>

<span data-ttu-id="df3f4-134">Para ver las alertas de calidad de la experiencia, complete este procedimiento desde la consola de System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="df3f4-134">To view Quality of Experience alerts, complete this procedure from the System Center Operations Manager console:</span></span>

  - <span data-ttu-id="df3f4-135">Expanda **supervisión**, expanda **Estado de Microsoft Lync Server 2013**, expanda **fiabilidad y calidad multimedia** y, después, expanda **calidad de multimedia**.</span><span class="sxs-lookup"><span data-stu-id="df3f4-135">Expand **Monitoring**, expand **Microsoft Lync Server 2013 Health**, expand **Call Reliability and Media Quality**, and then expand **Media Quality**.</span></span>

<span data-ttu-id="df3f4-136">Los módulos de administración para Lync Server 2013 ahora usan la detección a nivel de equipo en lugar del mecanismo de detección central usado en Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="df3f4-136">The management packs for Lync Server 2013 now use machine-level discovery instead of the central discovery mechanism used in Microsoft Lync Server 2010.</span></span> <span data-ttu-id="df3f4-137">Esto significa que cada agente de System Center se descubre por sí mismo e informa de su existencia en el servidor de administración central.</span><span class="sxs-lookup"><span data-stu-id="df3f4-137">This means that each System Center agent essentially discovers itself and reports its existence to the Central Management Server.</span></span> <span data-ttu-id="df3f4-138">El uso de detección en el nivel de equipo simplifica la administración de la infraestructura de System Center y permite la coexistencia de los paquetes de administración de Lync Server (por ejemplo, paquetes de administración para Lync Server 2010 y paquetes de administración de Lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="df3f4-138">Using machine-level discovery simplifies administration of your System Center infrastructure and also allows different versions of the Lync Server management packs (for example, management packs for Lync Server 2010 and management packs for Lync Server 2013) to coexist.</span></span>

<span data-ttu-id="df3f4-139"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="df3f4-139"></div>

<span> </span>

</div>

</div>

</span></span></div>

