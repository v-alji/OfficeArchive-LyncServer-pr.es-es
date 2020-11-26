---
title: 'Lync Server 2013: Características y funcionalidad de movilidad'
description: 'Lync Server 2013: capacidades y características de movilidad.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobility features and capabilities
ms:assetid: 12517a88-2531-44a5-bea5-d8884aff53eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh689983(v=OCS.15)
ms:contentKeyID: 48183457
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20713145c18260f22d9635c34af291e9a7c5ea9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445956"
---
# <a name="mobility-features-and-capabilities-in-lync-server-2013"></a><span data-ttu-id="e8de3-103">Características y funcionalidad de movilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8de3-103">Mobility features and capabilities in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8de3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8de3-104">

<span> </span></span></span>

<span data-ttu-id="e8de3-105">_**Última modificación del tema:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="e8de3-105">_**Topic Last Modified:** 2013-02-19_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="e8de3-106">La característica de movilidad introducida en las actualizaciones acumulativas para Lync Server 2013: el 2013 de febrero admite Lync 2010 para móviles y la funcionalidad de clientes móviles de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e8de3-106">The mobility feature introduced in the Cumulative Updates for Lync Server 2013: February 2013 supports Lync 2010 Mobile and Lync 2013 Mobile clients functionality.</span></span> <span data-ttu-id="e8de3-107">Al implementar el servicio de movilidad de Lync Server 2013, los usuarios pueden usar Apple iOS, Android y Windows Phone compatibles, o dispositivos móviles Nokia Symbian para realizar actividades como enviar y recibir mensajes instantáneos, ver contactos y ver presencia.</span><span class="sxs-lookup"><span data-stu-id="e8de3-107">When you deploy the Lync Server 2013 Mobility Service, users can use supported Apple iOS, Android, and Windows Phone, or Nokia Symbian mobile devices to perform activities such as sending and receiving instant messages, viewing contacts, and viewing presence.</span></span> <span data-ttu-id="e8de3-108">Además, los dispositivos móviles admiten algunas características de Enterprise Voice, como hacer clic para unirse a una conferencia, llamar a través del trabajo, acceso a un número único, correo de voz y llamadas perdidas.</span><span class="sxs-lookup"><span data-stu-id="e8de3-108">In addition, mobile devices support some Enterprise Voice features, such as click to join a conference, Call via Work, single number reach, voice mail, and missed calls.</span></span> <span data-ttu-id="e8de3-109">Las nuevas características introducidas en las actualizaciones acumulativas para Lync Server 2013: febrero de 2013 incluyen capacidad de voz sobre IP (VoIP) y vídeo (H. 264) para el Asistente de la reunión.</span><span class="sxs-lookup"><span data-stu-id="e8de3-109">New features introduced in the Cumulative Updates for Lync Server 2013: February 2013 include Voice over IP (VoIP) capability and video (H.264) for meeting attendee.</span></span>

<span data-ttu-id="e8de3-110">La característica de movilidad introducida en las actualizaciones acumulativas para Lync Server 2013: el 2013 de febrero es compatible con la funcionalidad de cliente móvil de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e8de3-110">The mobility feature introduced in the Cumulative Updates for Lync Server 2013: February 2013 supports Lync 2013 Mobile client functionality.</span></span> <span data-ttu-id="e8de3-111">Las actualizaciones acumulativas para Lync Server 2013: febrero 2013 Instale la API Web de comunicaciones unificadas, o UCWA.</span><span class="sxs-lookup"><span data-stu-id="e8de3-111">The Cumulative Updates for Lync Server 2013: February 2013 install Unified Communications Web API, or UCWA.</span></span> <span data-ttu-id="e8de3-112">UCWA es el componente que se usa para clientes móviles de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e8de3-112">UCWA is the component used for Lync 2013 Mobile clients.</span></span> <span data-ttu-id="e8de3-113">En Lync Server 2013, MCX se usa para clientes móviles de Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="e8de3-113">In Lync Server 2013, Mcx is used for Lync 2010 Mobile clients.</span></span> <span data-ttu-id="e8de3-114">Actualizaciones acumulativas para Lync Server 2013: febrero de 2013 introduce UCWA como el nuevo punto de entrada para los servicios de movilidad.</span><span class="sxs-lookup"><span data-stu-id="e8de3-114">Cumulative Updates for Lync Server 2013: February 2013 introduce UCWA as the new entry point for mobility services.</span></span> <span data-ttu-id="e8de3-115">Lync Server 2013 implementa de forma simultánea el servicio de movilidad (MCX), presentado en las actualizaciones acumulativas para Lync Server 2010:2011 de noviembre, y proporciona soporte técnico para Lync 2010 Mobile.</span><span class="sxs-lookup"><span data-stu-id="e8de3-115">Lync Server 2013 concurrently implements the Mobility Service (Mcx), introduced in the Cumulative Updates for Lync Server 2010: November 2011, and provides support for Lync 2010 Mobile.</span></span> <span data-ttu-id="e8de3-116">Al implementar las actualizaciones acumulativas para Lync Server 2013: febrero de 2013, los usuarios pueden usar dispositivos móviles compatibles con Apple iOS, Android y Windows Phone para realizar estas actividades, como:</span><span class="sxs-lookup"><span data-stu-id="e8de3-116">When you deploy the Cumulative Updates for Lync Server 2013: February 2013, users can use supported Apple iOS, Android, and Windows Phone mobile devices to perform such activities as:</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e8de3-117">Características compatibles con el servicio de movilidad de las actualizaciones acumulativas para Lync Server 2010: el 2011 de noviembre se indica con (MCX).</span><span class="sxs-lookup"><span data-stu-id="e8de3-117">Features supported by the Mobility Service from the Cumulative Updates for Lync Server 2010: November 2011 are noted with (Mcx).</span></span> <span data-ttu-id="e8de3-118">UCWA admite todas las características de la lista, que se incluyen en las actualizaciones acumulativas para Lync Server 2013: febrero de 2013.</span><span class="sxs-lookup"><span data-stu-id="e8de3-118">All listed features are supported by the UCWA, introduced in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

  - <span data-ttu-id="e8de3-119">Enviar y recibir mensajes instantáneos (MCX)</span><span class="sxs-lookup"><span data-stu-id="e8de3-119">Send and receive instant messages (Mcx)</span></span>

  - <span data-ttu-id="e8de3-120">Ver presencia (MCX)</span><span class="sxs-lookup"><span data-stu-id="e8de3-120">View presence (Mcx)</span></span>

  - <span data-ttu-id="e8de3-121">Ver contactos (MCX)</span><span class="sxs-lookup"><span data-stu-id="e8de3-121">View contacts (Mcx)</span></span>

  - <span data-ttu-id="e8de3-122">Haga clic para unirse a una conferencia (MCX)</span><span class="sxs-lookup"><span data-stu-id="e8de3-122">Click to join a conference (Mcx)</span></span>

  - <span data-ttu-id="e8de3-123">Llamar a través del trabajo (MCX)</span><span class="sxs-lookup"><span data-stu-id="e8de3-123">Call via work (Mcx)</span></span>

  - <span data-ttu-id="e8de3-124">Alcance de un solo número (MCX)</span><span class="sxs-lookup"><span data-stu-id="e8de3-124">Single number reach (Mcx)</span></span>

  - <span data-ttu-id="e8de3-125">Correo de voz (MCX)</span><span class="sxs-lookup"><span data-stu-id="e8de3-125">Voice mail (Mcx)</span></span>

  - <span data-ttu-id="e8de3-126">Notificación de llamada perdida (MCX)</span><span class="sxs-lookup"><span data-stu-id="e8de3-126">Missed call notification (Mcx)</span></span>

  - <span data-ttu-id="e8de3-127">Voz sobre IP (VoIP)</span><span class="sxs-lookup"><span data-stu-id="e8de3-127">Voice over IP (VoIP)</span></span>

  - <span data-ttu-id="e8de3-128">Vídeo para asistentes (H.264)</span><span class="sxs-lookup"><span data-stu-id="e8de3-128">Attendee video (H.264)</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e8de3-129">Lync 2010 Mobile proporcionó un cliente para dispositivos Nokia Symbian.</span><span class="sxs-lookup"><span data-stu-id="e8de3-129">Lync 2010 Mobile provided a client for Nokia Symbian devices.</span></span> <span data-ttu-id="e8de3-130">Lync 2013 Mobile no tendrá un cliente para dispositivos basados en Nokia Symbian.</span><span class="sxs-lookup"><span data-stu-id="e8de3-130">Lync 2013 Mobile will not have a client for Nokia Symbian-based devices.</span></span>



</div>

<span data-ttu-id="e8de3-131">Los usuarios de Apple iPad tendrán acceso a capacidades mejoradas.</span><span class="sxs-lookup"><span data-stu-id="e8de3-131">Apple iPad users will have access to enhanced capabilities.</span></span> <span data-ttu-id="e8de3-132">Después de unirse a una reunión con la devolución de llamada de audio, un usuario de iPad podrá ver las presentaciones cargadas de Microsoft PowerPoint en una reunión, compartir aplicaciones y escritorios, ver la lista de participantes de la reunión y recibir notificaciones de otros tipos de contenido que se comparten en la reunión.</span><span class="sxs-lookup"><span data-stu-id="e8de3-132">After joining a meeting by using audio call back, an iPad user will be able to view uploaded Microsoft PowerPoint presentations within a meeting, share applications and desktops, view the meeting participant list, and receive notifications of other content types that are being shared within the meeting.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="e8de3-133">Con un único número, un usuario recibe llamadas en un teléfono móvil que se marcaron en el número del trabajo.</span><span class="sxs-lookup"><span data-stu-id="e8de3-133">With single number reach, a user receives calls on a mobile phone that were dialed to the work number.</span></span> <span data-ttu-id="e8de3-134">Con la llamada a través del trabajo, el usuario realiza una llamada saliente desde el cliente móvil de Lync usando un número de teléfono del trabajo en lugar del número de teléfono móvil.</span><span class="sxs-lookup"><span data-stu-id="e8de3-134">With Call via Work, the user places an outbound call from the Lync Mobile client by using a work phone number instead of the mobile phone number.</span></span> <span data-ttu-id="e8de3-135">Con el marcado, el cliente envía una solicitud a MCX o UCWA (en función de la versión de Lync Mobile) para hacer la llamada.</span><span class="sxs-lookup"><span data-stu-id="e8de3-135">With dial-out, the client sends a request to Mcx or UCWA (based on the Lync Mobile version) to make the call for them.</span></span> <span data-ttu-id="e8de3-136">El servidor inicia la llamada y, a continuación, vuelve a llamar al usuario en el teléfono móvil.</span><span class="sxs-lookup"><span data-stu-id="e8de3-136">The server initiates the call and then calls the user back on the mobile phone.</span></span> <span data-ttu-id="e8de3-137">Cuando el usuario responde, el servidor completa la llamada marcando a la otra parte.</span><span class="sxs-lookup"><span data-stu-id="e8de3-137">When the user answers, the server completes the call by dialing the other party.</span></span> <span data-ttu-id="e8de3-138">Al usar las llamadas a través del trabajo, los usuarios pueden mantener su identidad de trabajo durante una llamada, lo que significa que el destinatario de la llamada no verá el número de teléfono móvil de la persona que llama, y la persona que llama evitará los cargos de llamadas salientes.</span><span class="sxs-lookup"><span data-stu-id="e8de3-138">By using Call via Work, users can maintain their work identity during a call, which means that the call recipient does not see the caller's mobile number, and the caller avoids incurring outbound calling charges.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="e8de3-139">No todas las características funcionan exactamente igual en todos los dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="e8de3-139">Not all features work exactly the same on all mobile devices.</span></span> <span data-ttu-id="e8de3-140">Para obtener más información sobre las características compatibles con dispositivos móviles, vea las tablas de comparación de clientes móviles en <A href="https://go.microsoft.com/fwlink/p/?linkid=234777">https://go.microsoft.com/fwlink/p/?LinkId=234777</A> .</span><span class="sxs-lookup"><span data-stu-id="e8de3-140">For details about features supported on mobile devices, see the Mobile Client Comparison Tables at <A href="https://go.microsoft.com/fwlink/p/?linkid=234777">https://go.microsoft.com/fwlink/p/?LinkId=234777</A>.</span></span> <span data-ttu-id="e8de3-141">Para obtener más información sobre los dispositivos y sistemas operativos compatibles, consulte los temas de requisitos en <A href="lync-server-2013-planning-for-mobile-clients.md">planificación de clientes móviles en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="e8de3-141">For details about supported devices and operating systems, see the requirements topics under <A href="lync-server-2013-planning-for-mobile-clients.md">Planning for mobile clients in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="e8de3-142">Cuando usa la característica de detección automática de Lync Server 2013, las aplicaciones móviles pueden ubicar automáticamente los servicios Web de Lync Server 2013 sin que los usuarios tengan que introducir manualmente las direcciones URL en la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8de3-142">When you use the Lync Server 2013 Autodiscover feature, mobile applications can automatically locate Lync Server 2013 Web Services without requiring users to manually enter the URLs in their device settings.</span></span> <span data-ttu-id="e8de3-143">También se admite la especificación manual de direcciones URL en la configuración de dispositivos móviles, principalmente para propósitos de solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="e8de3-143">Manually entering URLs in mobile device settings is also supported, primarily for troubleshooting purposes.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e8de3-144">MCX y UCWA son servicios complementarios y ambos se implementan para admitir clientes móviles de Lync 2010 Mobile y Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e8de3-144">The Mcx and UCWA are complimentary services and both are deployed to support Lync 2010 Mobile and Lync 2013 Mobile clients.</span></span> <span data-ttu-id="e8de3-145">Lync 2013 Mobile no podrá iniciar sesión en implementaciones de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="e8de3-145">Lync 2013 Mobile will not be able to sign in to Lync Server 2010 deployments.</span></span> <span data-ttu-id="e8de3-146">Lync 2010 Mobile y Lync 2013 Mobile podrán usar una implementación de Lync Server 2013 con las actualizaciones acumulativas para Lync Server 2013:2013 de febrero aplicado.</span><span class="sxs-lookup"><span data-stu-id="e8de3-146">Lync 2010 Mobile and Lync 2013 Mobile will be able to use a Lync Server 2013 deployment with the Cumulative Updates for Lync Server 2013: February 2013 applied.</span></span>



</div>

<span data-ttu-id="e8de3-147">La característica de movilidad también admite las *notificaciones de inserción* en los dispositivos móviles que no son compatibles con las aplicaciones que se ejecutan en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e8de3-147">The mobility feature also supports *push notifications* for mobile devices that do not support applications running in the background.</span></span> <span data-ttu-id="e8de3-148">Las notificaciones de inserción son notificaciones que se envían a dispositivos móviles sobre un evento que se produce mientras una aplicación móvil está inactiva.</span><span class="sxs-lookup"><span data-stu-id="e8de3-148">A push notification is a notification that is sent to a mobile device about an event that occurs while a mobile application is inactive.</span></span> <span data-ttu-id="e8de3-149">Por ejemplo, una invitación de mensajería instantánea (mi) perdida puede dar lugar a una notificación push.</span><span class="sxs-lookup"><span data-stu-id="e8de3-149">For example, a missed instant messaging (IM) invitation can result in a push notification.</span></span>

<span data-ttu-id="e8de3-150">MCX, UCWA, el servicio Detección automática y la compatibilidad con las notificaciones push se proporcionan en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e8de3-150">Mcx, UCWA, Autodiscover Service, and support for push notifications are provided in Lync Server 2013.</span></span> <span data-ttu-id="e8de3-151">Las características de cliente actualizadas, las capacidades y el uso de UCWA como punto de entrada de movilidad se incluyen en las actualizaciones acumulativas para Lync Server 2013:2013 de febrero.</span><span class="sxs-lookup"><span data-stu-id="e8de3-151">Updated client features, capabilities, and the use of UCWA as the mobility entry point are introduced in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>

<span data-ttu-id="e8de3-152"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8de3-152"></div>

<span> </span>

</div>

</div>

</span></span></div>

