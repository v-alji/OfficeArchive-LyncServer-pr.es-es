---
title: 'Lync Server 2013: Novedades para clientes'
description: 'Lync Server 2013: novedades para los clientes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: What's new for clients
ms:assetid: 5c144677-4d58-4fc3-8445-74b76c9fcf07
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204933(v=OCS.15)
ms:contentKeyID: 48184253
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90c1b93666b556c7ce7c4f3d94bea583dbf9b1a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398927"
---
# <a name="whats-new-for-clients-in-lync-server-2013"></a><span data-ttu-id="347f9-103">Novedades para clientes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="347f9-103">What's new for clients in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="347f9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="347f9-104">

<span> </span></span></span>

<span data-ttu-id="347f9-105">_**Última modificación del tema:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="347f9-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="347f9-106">Microsoft Lync 2013 tiene una interfaz de usuario rediseñada y características nuevas importantes.</span><span class="sxs-lookup"><span data-stu-id="347f9-106">Microsoft Lync 2013 has a redesigned user interface and important new features.</span></span> <span data-ttu-id="347f9-107">Para los administradores, el cliente está ahora incluido con el programa de instalación de Office, lo que proporciona un método más simplificado para implementar Office y personalizar clientes de su organización.</span><span class="sxs-lookup"><span data-stu-id="347f9-107">For administrators, the client is now included with the Office setup program, providing a more streamlined approach to deploying Office and customizing clients in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="347f9-108">Para ver una vista ilustrada de actualizaciones de la interfaz de usuario de Lync 2013, vea "Novedades de Lync 2013" en <A href="https://go.microsoft.com/fwlink/?linkid=273885">https://go.microsoft.com/fwlink/?LinkId=273885</A> .</span><span class="sxs-lookup"><span data-stu-id="347f9-108">For an illustrated view of Lync 2013 user interface updates, see “What’s New in Lync 2013” at <A href="https://go.microsoft.com/fwlink/?linkid=273885">https://go.microsoft.com/fwlink/?LinkId=273885</A>.</span></span>



</div>

<div>

## <a name="integration-with-office-setup"></a><span data-ttu-id="347f9-109">Integración con la configuración de Office</span><span class="sxs-lookup"><span data-stu-id="347f9-109">Integration with Office Setup</span></span>

<span data-ttu-id="347f9-110">El cliente de Lync 2013 y el complemento de reunión en línea para Lync 2013 (que admite la administración de reuniones desde el cliente de mensajería y colaboración de Outlook) ya están incluidos en el programa de instalación de Office 2013.</span><span class="sxs-lookup"><span data-stu-id="347f9-110">The Lync 2013 client and the Online Meeting Add-in for Lync 2013—which supports meeting management from within the Outlook messaging and collaboration client—are now both included with the Office 2013 Setup program.</span></span>

<span data-ttu-id="347f9-111">En versiones anteriores de Lync y Office Communicator, se pueden usar las propiedades de Windows Installer para personalizar y controlar la instalación de Office.</span><span class="sxs-lookup"><span data-stu-id="347f9-111">In previous versions of Lync and Office Communicator, you could use Windows Installer properties to customize and control the Office installation.</span></span> <span data-ttu-id="347f9-112">Puesto que Lync 2013 está integrado con el programa de instalación de Office, puede usar los siguientes métodos para personalizar la configuración de Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="347f9-112">Because Lync 2013 is integrated with Office setup, you can use the following methods to customize Lync 2013 setup:</span></span>

  - <span data-ttu-id="347f9-113">Usar la Herramienta de personalización de Office (OCT)</span><span class="sxs-lookup"><span data-stu-id="347f9-113">Use the Office Customization Tool (OCT)</span></span>

  - <span data-ttu-id="347f9-114">Usar el Config.xml para realizar tareas de instalación</span><span class="sxs-lookup"><span data-stu-id="347f9-114">Use the Config.xml to perform installation tasks</span></span>

  - <span data-ttu-id="347f9-115">Usar opciones de Command-Line de configuración</span><span class="sxs-lookup"><span data-stu-id="347f9-115">Use Setup Command-Line Options</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="347f9-116">El programa de instalación de Lync 2013 no desinstala versiones anteriores de Lync u Office Communicator.</span><span class="sxs-lookup"><span data-stu-id="347f9-116">The Lync 2013 setup program does not uninstall previous versions of Lync or Office Communicator.</span></span> <span data-ttu-id="347f9-117">El cliente de Lync 2013 se instala en paralelo con otros clientes de Lync u Office Communicator</span><span class="sxs-lookup"><span data-stu-id="347f9-117">The Lync 2013 client installs side-by-side with other Lync or Office Communicator clients</span></span>



</div>

<span data-ttu-id="347f9-118">Para obtener más información, vea [implementación de clientes de Lync en Lync Server 2013](lync-server-2013-deploying-lync-clients.md).</span><span class="sxs-lookup"><span data-stu-id="347f9-118">For details, see [Deploying Lync clients in Lync Server 2013](lync-server-2013-deploying-lync-clients.md).</span></span>

</div>

<div>

## <a name="group-policy-deployment"></a><span data-ttu-id="347f9-119">Implementación de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="347f9-119">Group Policy Deployment</span></span>

<span data-ttu-id="347f9-120">Puesto que Lync 2013 ahora está incluido en el programa de instalación de Office, el método para implementar la configuración de la Directiva de grupo de Lync ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="347f9-120">Because Lync 2013 is now included in Office setup, the method for deploying Lync Group Policy settings has changed.</span></span> <span data-ttu-id="347f9-121">En las versiones anteriores de Lync y Office Communicator, se puede usar Communicator. ADM para definir la configuración de directiva de grupo, mientras que en Lync 2013 ahora puede usar las plantillas administrativas de ADMX y ADML de Lync que se proporcionan junto con las plantillas administrativas de la Directiva de grupo de Office.</span><span class="sxs-lookup"><span data-stu-id="347f9-121">In previous versions of Lync and Office Communicator, you could use the Communicator.adm to define Group Policy settings, whereas in Lync 2013 you can now use the Lync ADMX and ADML administrative templates that are provided along with the Office Group Policy Administrative Templates.</span></span>

<span data-ttu-id="347f9-122">Para obtener más información, consulte [configuración de directiva de grupo para Lync 2013](lync-server-2013-group-policy-settings-for-lync-2013.md).</span><span class="sxs-lookup"><span data-stu-id="347f9-122">For details, see [Group Policy settings for Lync 2013](lync-server-2013-group-policy-settings-for-lync-2013.md).</span></span>

</div>

<div>

## <a name="outlook-scheduling-add-in-updates"></a><span data-ttu-id="347f9-123">Actualizaciones de complementos de programación de Outlook</span><span class="sxs-lookup"><span data-stu-id="347f9-123">Outlook Scheduling Add-in Updates</span></span>

<span data-ttu-id="347f9-124">El complemento de reunión en línea para Lync 2013 incluye personalización de invitaciones de reuniones y nuevas opciones de reunión.</span><span class="sxs-lookup"><span data-stu-id="347f9-124">The Online Meeting Add-in for Lync 2013 includes meeting invite customization and new meeting options.</span></span>

  - <span data-ttu-id="347f9-125">Los administradores pueden personalizar las invitaciones a reuniones de la organización agregando un logotipo personalizado, una dirección URL de soporte técnico, una dirección URL de renuncia legal o texto de pie de página personalizado.</span><span class="sxs-lookup"><span data-stu-id="347f9-125">Administrators can customize the organization’s meeting invitations by adding a custom logo, a support URL, a legal disclaimer URL, or custom footer text.</span></span> <span data-ttu-id="347f9-126">Para obtener más información, consulte [personalizar el complemento de reunión en línea en Lync Server 2013](lync-server-2013-customizing-the-online-meeting-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="347f9-126">For details, see [Customizing the Online Meeting Add-in in Lync Server 2013](lync-server-2013-customizing-the-online-meeting-add-in.md).</span></span>

  - <span data-ttu-id="347f9-127">Los controles de silencio de nuevo asistente permiten a los organizadores de reuniones programar conferencias en las que el asistente está silenciado de audio y vídeo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="347f9-127">New attendee mute controls allow meeting organizers to schedule conferences that have attendee audio and video muted by default.</span></span>

</div>

<div>

## <a name="virtual-desktop-infrastructure-plug-in"></a><span data-ttu-id="347f9-128">Complemento de infraestructura de escritorio virtual</span><span class="sxs-lookup"><span data-stu-id="347f9-128">Virtual Desktop Infrastructure Plug-in</span></span>

<span data-ttu-id="347f9-129">El cliente de Lync 2013 ahora admite audio y vídeo en un entorno de infraestructura de escritorio virtual (VDI).</span><span class="sxs-lookup"><span data-stu-id="347f9-129">The Lync 2013 client now supports audio and video in a Virtual Desktop Infrastructure (VDI) environment.</span></span> <span data-ttu-id="347f9-130">Un usuario puede conectar un dispositivo de audio o vídeo (por ejemplo, unos auriculares con micrófono o una cámara) al equipo local (por ejemplo, un equipo de cliente ligero o un equipo con un propósito).</span><span class="sxs-lookup"><span data-stu-id="347f9-130">A user can connect an audio or video device (for example, a headset or a camera) to the local computer (for example, a thin client or repurposed computer).</span></span> <span data-ttu-id="347f9-131">El usuario puede conectarse a la máquina virtual, inicie sesión en el cliente de Lync 2013 que se ejecuta en la máquina virtual y participe en la comunicación de audio y vídeo en tiempo real como si el cliente se ejecuta de forma local.</span><span class="sxs-lookup"><span data-stu-id="347f9-131">The user can connect to the virtual machine, sign in to the Lync 2013 client that is running on the virtual machine, and participate in real-time audio and video communication as though the client is running locally.</span></span> <span data-ttu-id="347f9-132">Las siguientes características son compatibles con un entorno de escritorio virtual:</span><span class="sxs-lookup"><span data-stu-id="347f9-132">The following features are supported in a virtual desktop environment:</span></span>

  - <span data-ttu-id="347f9-133">Integración de dispositivos para audio y vídeo, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="347f9-133">Device integration for audio and video, including the following:</span></span>
    
      - <span data-ttu-id="347f9-134">Llamar a controles desde el dispositivo</span><span class="sxs-lookup"><span data-stu-id="347f9-134">Call controls from the device</span></span>
    
      - <span data-ttu-id="347f9-135">Integración de presencia en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="347f9-135">Presence integration on the device</span></span>
    
      - <span data-ttu-id="347f9-136">Compatibilidad con varios HID (dispositivo de interfaz humana)</span><span class="sxs-lookup"><span data-stu-id="347f9-136">Multiple HID (human interface device) support</span></span>

  - <span data-ttu-id="347f9-137">Soporte de servicios de emergencia y ubicación.</span><span class="sxs-lookup"><span data-stu-id="347f9-137">Location and emergency services support.</span></span>

  - <span data-ttu-id="347f9-138">Compatibilidad con todas las modalidades de Lync, como la mensajería instantánea, el audio, el vídeo, el uso compartido de aplicaciones, el uso compartido de PowerPoint, la pizarra y la transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="347f9-138">Support for all Lync modalities, including IM, audio, video, application sharing, desktop sharing, PowerPoint sharing, whiteboard, and file transfer.</span></span>

  - <span data-ttu-id="347f9-139">Compatibilidad de audio y vídeo en llamadas entre usuarios y llamadas en conferencia.</span><span class="sxs-lookup"><span data-stu-id="347f9-139">Audio and video support in person-to-person calls and conference calls.</span></span>

<span data-ttu-id="347f9-140">Para obtener información sobre cómo implementar el complemento VDI, consulte [implementar el complemento de VDI para Lync en Lync Server 2013](lync-server-2013-deploying-the-lync-vdi-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="347f9-140">For information about deploying the VDI plug-in, see [Deploying the Lync VDI plug-in in Lync Server 2013](lync-server-2013-deploying-the-lync-vdi-plug-in.md).</span></span>

</div>

<div>

## <a name="video-enhancements"></a><span data-ttu-id="347f9-141">Mejoras de video</span><span class="sxs-lookup"><span data-stu-id="347f9-141">Video Enhancements</span></span>

<span data-ttu-id="347f9-142">Varias características nuevas mejoran significativamente la experiencia de vídeo para los participantes de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="347f9-142">Several new features significantly enhance the video experience for conference participants.</span></span>

  - <span data-ttu-id="347f9-143">El video se ha mejorado con la detección de rostro y las tramas inteligentes, de modo que el video de un participante se mueve para ayudarle a mantenerlos centrados en el marco.</span><span class="sxs-lookup"><span data-stu-id="347f9-143">Video is enhanced with face detection and smart framing, so that a participant’s video moves to help keep them centered in the frame.</span></span>

  - <span data-ttu-id="347f9-144">Ahora se admite el video de alta definición en las llamadas de dos participantes y en las conferencias de varias partes.</span><span class="sxs-lookup"><span data-stu-id="347f9-144">High-definition video is now supported in two-party calls and multiparty conferences.</span></span> <span data-ttu-id="347f9-145">Los usuarios pueden tener resoluciones de hasta HD 1080P.</span><span class="sxs-lookup"><span data-stu-id="347f9-145">Users can experience resolutions up to HD 1080P.</span></span>

  - <span data-ttu-id="347f9-146">Los participantes pueden seleccionar entre diferentes diseños de reunión: la vista de Galería muestra las imágenes o los vídeos de todos los participantes; Vista de orador muestra el contenido de la reunión y solo el vídeo o la imagen del orador; La vista de presentación muestra solo el contenido de la reunión; La vista compacta muestra solo los controles de la reunión.</span><span class="sxs-lookup"><span data-stu-id="347f9-146">Participants can select from different meeting layouts: Gallery View shows all participants’ pictures or videos; Speaker View shows the meeting content and only the current speaker’s video or picture; Presentation View shows meeting content only; Compact View shows just the meeting controls.</span></span>

  - <span data-ttu-id="347f9-147">Con la nueva característica de galería, los participantes pueden ver varias fuentes de video al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="347f9-147">With the new Gallery feature, participants can see multiple video feeds at the same time.</span></span> <span data-ttu-id="347f9-148">Si la Conferencia tiene más de cinco participantes, las fuentes de vídeo de los participantes más activos aparecerán en la fila superior y las imágenes aparecerán para los demás participantes.</span><span class="sxs-lookup"><span data-stu-id="347f9-148">If the conference has more than five participants, video feeds of only the most active participants appear in the top row, and pictures appear for the other participants.</span></span>

  - <span data-ttu-id="347f9-149">Los participantes pueden usar el anclaje de video para seleccionar una o varias de las fuentes de video disponibles para que sean visibles en todo momento.</span><span class="sxs-lookup"><span data-stu-id="347f9-149">Participants can use video pinning to select one or more of the available video feeds to be visible at all times.</span></span>

  - <span data-ttu-id="347f9-150">Los moderadores pueden usar la característica noticias destacadas de vídeo para seleccionar una fuente de vídeo de una persona para que todos los participantes de la reunión puedan ver únicamente a ese participante.</span><span class="sxs-lookup"><span data-stu-id="347f9-150">Presenters can use the Video Spotlight feature to select one person’s video feed so that every participant in the meeting sees that participant only.</span></span>

</div>

<div>

## <a name="chat-room-integration"></a><span data-ttu-id="347f9-151">Integración del salón de chat</span><span class="sxs-lookup"><span data-stu-id="347f9-151">Chat Room Integration</span></span>

<span data-ttu-id="347f9-152">Lync 2013 ahora integra las características proporcionadas previamente por la conversación grupal de Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="347f9-152">Lync 2013 now integrates the features previously provided by Lync 2010 Group Chat.</span></span> <span data-ttu-id="347f9-153">Ya no se necesita un cliente de conversación grupal independiente.</span><span class="sxs-lookup"><span data-stu-id="347f9-153">A separate group chat client is no longer required.</span></span>

  - <span data-ttu-id="347f9-154">Desde dentro de Lync 2013, los usuarios pueden buscar salas de chats, agregar salones de chat a sus contactos, supervisar la actividad de los salones de chat y leer y publicar mensajes.</span><span class="sxs-lookup"><span data-stu-id="347f9-154">From within Lync 2013, users can search for chat rooms, add chat rooms to their contacts, monitor chat room activity, and read and post messages.</span></span>

  - <span data-ttu-id="347f9-155">Los usuarios pueden crear fuentes de temas para que reciban una notificación si alguien de uno de sus salones de chat agrega una publicación que contiene palabras clave específicas.</span><span class="sxs-lookup"><span data-stu-id="347f9-155">Users can create topic feeds so that they’ll be notified if someone in one of their chat rooms adds a post containing specific keywords.</span></span>

  - <span data-ttu-id="347f9-156">Con la página nuevas opciones de **chat persistente** , los usuarios pueden configurar alertas y sonidos de notificación que se aplican cuando los usuarios publican mensajes en sus salones de chat.</span><span class="sxs-lookup"><span data-stu-id="347f9-156">With the new **Persistent Chat** options page, users can set notification alerts and sounds that apply when people post messages to their chat rooms.</span></span>

</div>

<div>

## <a name="lync-web-app-updates"></a><span data-ttu-id="347f9-157">Actualizaciones de Lync Web App</span><span class="sxs-lookup"><span data-stu-id="347f9-157">Lync Web App Updates</span></span>

<span data-ttu-id="347f9-158">Lync Web App es el cliente de conferencia basado en web para reuniones de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="347f9-158">Lync Web App is the web-based conferencing client for Lync Server 2013 meetings.</span></span> <span data-ttu-id="347f9-159">En esta versión, la adición de audio y vídeo de PC a Lync Web App proporciona una experiencia de reunión completa para cualquier persona que no tenga un cliente Lync instalado de forma local.</span><span class="sxs-lookup"><span data-stu-id="347f9-159">In this release, the addition of computer audio and video to Lync Web App provides a complete in-meeting experience for anyone who doesn’t have a Lync client installed locally.</span></span> <span data-ttu-id="347f9-160">Los participantes de las reuniones obtienen acceso a todas las características de uso compartido y colaboración, y a todos los controles de la reunión del moderador.</span><span class="sxs-lookup"><span data-stu-id="347f9-160">Meeting participants have access to all collaboration and sharing features and presenter meeting controls.</span></span>

<span data-ttu-id="347f9-161">Cuando un usuario intenta unirse a una reunión pero no tiene un cliente instalado localmente, se abre Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="347f9-161">When a user tries to join a meeting but doesn’t have a locally installed client, Lync Web App opens.</span></span> <span data-ttu-id="347f9-162">Si desea permitir opciones adicionales para unirse a la reunión, puede configurar la página de la combinación de reuniones; consulte [configurar la página de la combinación de reuniones en Lync Server 2013](lync-server-2013-configuring-the-meeting-join-page.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="347f9-162">If you want to allow additional options for joining the meeting, you can configure the Meeting Join page; see [Configuring the meeting join page in Lync Server 2013](lync-server-2013-configuring-the-meeting-join-page.md) in the Deployment documentation.</span></span>

<span data-ttu-id="347f9-163">Debido a las mejoras de Lync Web App, no está disponible una versión actualizada del Asistente para Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="347f9-163">Because of the enhancements to Lync Web App, an updated version of Attendee isn’t available for Lync Server 2013.</span></span> <span data-ttu-id="347f9-164">Lync Web App es el cliente que elige para los participantes fuera de su organización.</span><span class="sxs-lookup"><span data-stu-id="347f9-164">Lync Web App is the client of choice for participants outside your organization.</span></span> <span data-ttu-id="347f9-165">No se requiere instalación de cliente local, aunque las características de audio, vídeo y uso compartido requieren que se instale un complemento al utilizar por primera vez.</span><span class="sxs-lookup"><span data-stu-id="347f9-165">No local client installation is required, although audio, video, and sharing features require a plug-in to be installed at first use.</span></span>

</div>

<div>

## <a name="lync-2013-for-mobile-clients-updates"></a><span data-ttu-id="347f9-166">Lync 2013 para actualizaciones de clientes móviles</span><span class="sxs-lookup"><span data-stu-id="347f9-166">Lync 2013 for Mobile Clients Updates</span></span>

<span data-ttu-id="347f9-167">Además de las capacidades mejoradas de presencia, contactos y mensajería instantánea, los clientes móviles de Lync 2013 ahora proporcionan llamadas y videollamadas a través de Internet y de las conexiones de datos móviles.</span><span class="sxs-lookup"><span data-stu-id="347f9-167">In addition to enhanced presence, contacts, and IM capabilities, Lync 2013 mobile clients now provide voice and video calling over the Internet and cellular data connections.</span></span> <span data-ttu-id="347f9-168">Con un solo toque en el vínculo de la reunión en un elemento de calendario, los usuarios móviles pueden unirse a reuniones de Lync y de vídeo.</span><span class="sxs-lookup"><span data-stu-id="347f9-168">With a single tap of the meeting link in a calendar item, mobile users can join Lync voice and video meetings.</span></span> <span data-ttu-id="347f9-169">Para obtener más información sobre los clientes móviles de Lync 2013, consulte [planificación de clientes móviles en Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span><span class="sxs-lookup"><span data-stu-id="347f9-169">For more information about Lync 2013 mobile clients, see [Planning for mobile clients in Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span></span>

</div>

<div>

## <a name="lync-2013-user-interface-updates"></a><span data-ttu-id="347f9-170">Actualizaciones de la interfaz de usuario de Lync 2013</span><span class="sxs-lookup"><span data-stu-id="347f9-170">Lync 2013 User Interface Updates</span></span>

<div>

## <a name="accessibility-updates"></a><span data-ttu-id="347f9-171">Actualizaciones de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="347f9-171">Accessibility Updates</span></span>

<span data-ttu-id="347f9-172">Lync 2013 incorpora varias nuevas características de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="347f9-172">Lync 2013 incorporates several new accessibility features.</span></span>

  - <span data-ttu-id="347f9-173">Lync 2013 admite una resolución alta de PPP, lo que permite a los usuarios ajustar el texto y los gráficos de 125% y 150 puntos por pulgada.</span><span class="sxs-lookup"><span data-stu-id="347f9-173">Lync 2013 supports high DPI resolution, enabling users to scale text and graphics for 125% and 150% dots per inch.</span></span>

  - <span data-ttu-id="347f9-174">Lync proporciona compatibilidad de contraste alto para que la interfaz de usuario siga funcionando completamente cuando se usa con los temas de contraste alto de Windows.</span><span class="sxs-lookup"><span data-stu-id="347f9-174">Lync provides high-contrast support so that the user interface remains fully functional when used with high contrast themes in Windows.</span></span>

  - <span data-ttu-id="347f9-175">Lync ofrece más de 100 métodos abreviados de teclado para que los usuarios puedan obtener acceso a funciones importantes sin un mouse.</span><span class="sxs-lookup"><span data-stu-id="347f9-175">Lync offers more than 100 keyboard shortcuts so that users can access important functions without a mouse.</span></span> <span data-ttu-id="347f9-176">Por ejemplo, los usuarios pueden presionar ALT + C para aceptar una llamada o Alt + I para ignorarla, sin tener que utilizar la tecla TAB o establecer el foco.</span><span class="sxs-lookup"><span data-stu-id="347f9-176">For example, users can press Alt+C to accept a call, or Alt + I to ignore it, without having to tab or set the focus.</span></span> <span data-ttu-id="347f9-177">Si pulsa (Alt + Q) finaliza una llamada, (Ctrl + N) inicia OneNote y (Alt + T) se abre el menú herramientas.</span><span class="sxs-lookup"><span data-stu-id="347f9-177">Pressing (Alt+Q) ends a call, (Ctrl+N) starts OneNote, and (Alt+T) opens the Tools menu.</span></span>

  - <span data-ttu-id="347f9-178">La compatibilidad con un lector de pantalla extensivo en Lync 2013 garantiza que todas las notificaciones, las solicitudes entrantes y los mensajes instantáneos se lean en voz alta cuando se habilita un lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="347f9-178">Extensive screen reader support in Lync 2013 ensures that all notifications, incoming requests, and instant messages are read aloud when a screen reader is enabled.</span></span>

</div>

<div>

## <a name="presence-while-sharing"></a><span data-ttu-id="347f9-179">Presencia al compartir</span><span class="sxs-lookup"><span data-stu-id="347f9-179">Presence While Sharing</span></span>

<span data-ttu-id="347f9-180">Cuando Lync detecta que un usuario está compartiendo, Lync asigna automáticamente un estado de presencia para el usuario.</span><span class="sxs-lookup"><span data-stu-id="347f9-180">When Lync detects that a user is sharing, Lync automatically assigns the user a Presenting presence status.</span></span> <span data-ttu-id="347f9-181">Este estado bloquea todas las comunicaciones entrantes a menos que el remitente tenga asignada la relación de privacidad grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="347f9-181">This status blocks all incoming communications unless the sender is assigned the Workgroup privacy relationship.</span></span> <span data-ttu-id="347f9-182">Si el usuario usa la característica de uso compartido por completo en un monitor secundario, Lync no asigna un estado de presencia de presentación.</span><span class="sxs-lookup"><span data-stu-id="347f9-182">If the user is using the sharing feature entirely on a secondary monitor, Lync does not assign a Presenting presence status.</span></span>

</div>

<div>

## <a name="conversation-window-updates"></a><span data-ttu-id="347f9-183">Actualizaciones de la ventana de conversación</span><span class="sxs-lookup"><span data-stu-id="347f9-183">Conversation Window Updates</span></span>

<span data-ttu-id="347f9-184">La ventana de conversación rediseñada ofrece un acceso más rápido a las características importantes.</span><span class="sxs-lookup"><span data-stu-id="347f9-184">The redesigned Conversation window provides quicker access to important features.</span></span>

  - <span data-ttu-id="347f9-185">Con la nueva característica de conversaciones en pestañas, los usuarios pueden conservar todos los mensajes instantáneos y salones de chat en una ventana de conversación.</span><span class="sxs-lookup"><span data-stu-id="347f9-185">With the new tabbed conversations feature, users can now keep all their IMs and chat rooms in one Conversation window.</span></span> <span data-ttu-id="347f9-186">Las pestañas de la parte izquierda de la ventana de conversación permiten a los usuarios desplazarse fácilmente entre todas las conversaciones activas.</span><span class="sxs-lookup"><span data-stu-id="347f9-186">The tabs along the left side of the Conversation window let users navigate easily among all active conversations.</span></span>

  - <span data-ttu-id="347f9-187">Los usuarios pueden mostrar una conversación individual en una ventana independiente y, a continuación, cambiar el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="347f9-187">Users can pop out an individual conversation into a separate window, and then resize the window.</span></span> <span data-ttu-id="347f9-188">También pueden volver a mostrar la ventana en la ventana de conversación principal.</span><span class="sxs-lookup"><span data-stu-id="347f9-188">They can also pop the window back into the main Conversation window.</span></span>

  - <span data-ttu-id="347f9-189">Lync 2013 vuelve a abrir las conversaciones de un usuario cuando el usuario cierra sesión e inicia sesión en Lync.</span><span class="sxs-lookup"><span data-stu-id="347f9-189">Lync 2013 reopens a user’s conversations when the user signs out and signs back in to Lync.</span></span>

  - <span data-ttu-id="347f9-190">Los usuarios pueden agregar rápidamente mensajería instantánea, vídeo, uso compartido de programas, uso compartido de escritorio o herramientas de conferencia web (pizarra, notas de reunión, blocs de notas compartidos y datos adjuntos) a cualquier conversación.</span><span class="sxs-lookup"><span data-stu-id="347f9-190">Users can quickly add IM, video, program sharing, desktop sharing, or web conferencing tools (whiteboard, meeting notes, shared notebooks, and attachments) to any conversation.</span></span>

  - <span data-ttu-id="347f9-191">En una reunión en la que el vídeo o contenido se comparte, los usuarios pueden mostrar el vídeo de la reunión o el contenido compartido y, a continuación, cambiar el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="347f9-191">In a meeting where video or content is being shared, users can pop out the meeting video or shared content, and then resize the window.</span></span>

</div>

<div>

## <a name="lync-main-window-updates"></a><span data-ttu-id="347f9-192">Actualizaciones de la ventana principal de Lync</span><span class="sxs-lookup"><span data-stu-id="347f9-192">Lync Main Window Updates</span></span>

<span data-ttu-id="347f9-193">El nuevo aspecto simplificado conserva características conocidas, como el campo **¿Qué está sucediendo?** , el selector de estado y el selector **de ubicación** .</span><span class="sxs-lookup"><span data-stu-id="347f9-193">The new streamlined look retains familiar features such as the **What’s happening today?** note field, the status selector, and the **Set Your Location** selector.</span></span>

  - <span data-ttu-id="347f9-194">Cuando los salones de chat estén habilitados, los usuarios verán un nuevo icono de **salones de chat** en la Página principal de Lync.</span><span class="sxs-lookup"><span data-stu-id="347f9-194">When chat rooms are enabled, users see a new **Chat Rooms** icon on the main Lync page.</span></span> <span data-ttu-id="347f9-195">Con el icono de los **salones de chat** , los usuarios pueden acceder rápidamente a sus salones de chat y filtros.</span><span class="sxs-lookup"><span data-stu-id="347f9-195">With the **Chat Rooms** icon, users can quickly access their chat rooms and filters.</span></span>

  - <span data-ttu-id="347f9-196">Los usuarios pueden hacer clic en Ver iconos para cambiar a la vista **contactos** , a la vista de **salones de chat** , a la vista **conversaciones** o a la vista de **teléfono** .</span><span class="sxs-lookup"><span data-stu-id="347f9-196">Users can click the view icons to switch to the **Contacts** view, **Chat Rooms** view, **Conversations** view, or **Phone** view.</span></span>

  - <span data-ttu-id="347f9-197">Si los usuarios han migrado a Exchange 2013, pueden cargar una imagen de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="347f9-197">If users have been migrated to Exchange 2013, they can upload a high resolution picture.</span></span>

</div>

<div>

## <a name="contacts-view-and-contact-card-updates"></a><span data-ttu-id="347f9-198">Vista contactos y actualizaciones de tarjetas de contacto</span><span class="sxs-lookup"><span data-stu-id="347f9-198">Contacts View and Contact Card Updates</span></span>

<span data-ttu-id="347f9-199">Lync 2013 ofrece a los usuarios distintas formas de ver los contactos y grupos en su vista **contactos** .</span><span class="sxs-lookup"><span data-stu-id="347f9-199">Lync 2013 gives users different ways to view contacts and groups in their **Contacts** view.</span></span>

  - <span data-ttu-id="347f9-200">Con el nuevo almacén de contactos unificado, después de migrar los contactos de Lync de los usuarios a Exchange 2013, los usuarios pueden tener acceso y administrar sus contactos desde Lync 2013, Outlook o Outlook Web App, y sus favoritos permanecen sincronizados.</span><span class="sxs-lookup"><span data-stu-id="347f9-200">With the new unified contact store, after users' Lync contacts are migrated to Exchange 2013, the users can access and manage their contacts from Lync 2013, Outlook, or Outlook Web App, and their Favorites stay synchronized.</span></span> <span data-ttu-id="347f9-201">Por ejemplo, si un usuario agrega un contacto a favoritos en Outlook, el contacto aparece en el grupo favoritos de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="347f9-201">For example, if a user adds a contact to Favorites in Outlook, the contact appears in the Favorites group in Lync 2013.</span></span>

  - <span data-ttu-id="347f9-202">Si ha agregado y configurado el proxy XMPP y la puerta de enlace XMPP, los usuarios pueden agregar contactos de socios basados en XMPP para la mensajería instantánea y la presencia.</span><span class="sxs-lookup"><span data-stu-id="347f9-202">If you have added and configured the XMPP proxy and XMPP gateway, users can add contacts from XMPP-based partners for instant messaging and presence.</span></span>

  - <span data-ttu-id="347f9-203">Una nueva característica **Agregar un contacto que no está en mi organización** ofrece a los usuarios una forma fácil de agregar personas externas a la organización.</span><span class="sxs-lookup"><span data-stu-id="347f9-203">A new **Add a Contact That’s Not in My Organization** feature gives users an easy way to add people who are external to the organization.</span></span>

  - <span data-ttu-id="347f9-204">Un nuevo grupo de **Favoritos** permite a los usuarios crear una lista de personas con las que los usuarios se comunican con mayor frecuencia para obtener acceso más rápido.</span><span class="sxs-lookup"><span data-stu-id="347f9-204">A new **Favorites** group lets users build a list of people users contact most often for quicker access.</span></span>

  - <span data-ttu-id="347f9-205">Los usuarios pueden usar la página de opciones de la nueva **lista de contactos** para elegir cómo desean ordenar y mostrar los contactos.</span><span class="sxs-lookup"><span data-stu-id="347f9-205">Users can use the new **Contacts List** options page to choose how users want to sort and display contacts.</span></span> <span data-ttu-id="347f9-206">Los usuarios pueden seleccionar una vista expandida de dos líneas en la que se muestran las imágenes de los contactos o una vista de una línea comprimida.</span><span class="sxs-lookup"><span data-stu-id="347f9-206">Users can select an expanded, two-line view that shows contacts’ pictures, or a condensed one-line view.</span></span> <span data-ttu-id="347f9-207">Los usuarios también pueden ordenar los contactos por orden alfabético o por disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="347f9-207">Users can also sort contacts alphabetically or by availability.</span></span>

</div>

<div>

## <a name="conferencing-updates"></a><span data-ttu-id="347f9-208">Actualizaciones de conferencias</span><span class="sxs-lookup"><span data-stu-id="347f9-208">Conferencing Updates</span></span>

<span data-ttu-id="347f9-209">Lync 2013 ofrece varias mejoras para las características de conferencia.</span><span class="sxs-lookup"><span data-stu-id="347f9-209">Lync 2013 offers several enhancements to conferencing features.</span></span>

  - <span data-ttu-id="347f9-210">En función del tipo de reunión, los usuarios pueden silenciar la audiencia y permitir o bloquear el uso compartido de vídeo al programar la reunión.</span><span class="sxs-lookup"><span data-stu-id="347f9-210">Depending on the type of meeting, users can now mute the audience and allow or block video sharing when scheduling the meeting.</span></span> <span data-ttu-id="347f9-211">Estas opciones están disponibles en la página Opciones de la **reunión** y se recomiendan para reuniones grandes con más de 20 participantes.</span><span class="sxs-lookup"><span data-stu-id="347f9-211">These options are available on the **Meeting Options** page and are recommended for large meetings with more than 20 participants.</span></span>

  - <span data-ttu-id="347f9-212">Los controles de audio fáciles de usar en la sala de reuniones permiten que el usuario controle las opciones de audio, como silenciar, reactivar el audio, cambiar el dispositivo, etc.</span><span class="sxs-lookup"><span data-stu-id="347f9-212">Easy to use audio controls in the meeting room allow the user to control audio options, such as mute, unmute, change device, and so on.</span></span>

  - <span data-ttu-id="347f9-213">Al compartir programas, los usuarios pueden seleccionar varios programas para compartirlos si necesitan trabajar con más de un programa.</span><span class="sxs-lookup"><span data-stu-id="347f9-213">When sharing programs, users can select multiple programs to share if they need to work with more than one program.</span></span>

  - <span data-ttu-id="347f9-214">Ahora los usuarios pueden cargar presentaciones que contienen clips de vídeo cargando el archivo de PowerPoint y haciendo clic con el mouse sobre la diapositiva para mostrar los controles de vídeo, como los controles de reproducción, pausa y audio.</span><span class="sxs-lookup"><span data-stu-id="347f9-214">Users can now upload presentations that contain video clips by uploading the PowerPoint file, and pointing the mouse over the slide to display video controls, such as play, pause, and audio controls.</span></span>

  - <span data-ttu-id="347f9-215">Durante una reunión, los usuarios pueden combinar otra conversación abierta en la reunión mediante la **combinación de esta llamada** en el menú **más opciones** (**...**).</span><span class="sxs-lookup"><span data-stu-id="347f9-215">While in a meeting, users can merge another open conversation into the meeting by using **Merge This Call Into** on the **More Options** (**…**) menu.</span></span>

  - <span data-ttu-id="347f9-216">Para ver los nombres de los participantes, los usuarios pueden situar el mouse sobre el botón **Ver participantes** o hacer clic en **Mostrar lista de participantes** para acoplar el panel en la reunión.</span><span class="sxs-lookup"><span data-stu-id="347f9-216">To see the participants’ names, users can hover the mouse over the **View Participants** button, or click **Show Participant List** to dock the panel in the meeting.</span></span>

  - <span data-ttu-id="347f9-217">Según el tipo de reunión, los usuarios pueden seleccionar entre varias vistas de contenido y participantes diferentes.</span><span class="sxs-lookup"><span data-stu-id="347f9-217">Depending on the meeting type, users can select from several different content and participant views.</span></span>

  - <span data-ttu-id="347f9-218">Las grabaciones de reuniones se guardan automáticamente en un formato que se reproduce en el reproductor de Windows Media (MP4).</span><span class="sxs-lookup"><span data-stu-id="347f9-218">Meeting recordings are automatically saved in a format that plays in Windows Media Player (MP4).</span></span> <span data-ttu-id="347f9-219">Los usuarios pueden compartir fácilmente el archivo con cualquier persona o usar la característica **publicar** en el administrador de grabaciones para publicar la grabación en una ubicación compartida.</span><span class="sxs-lookup"><span data-stu-id="347f9-219">Users can easily share the file with anyone, or use the **Publish** feature in recording manager to post the recording on a shared location.</span></span>

  - <span data-ttu-id="347f9-220">OneNote habilita nuevas maneras de colaborar en una reunión.</span><span class="sxs-lookup"><span data-stu-id="347f9-220">OneNote enables new ways to collaborate in a meeting.</span></span> <span data-ttu-id="347f9-221">Durante una reunión, los usuarios pueden tomar notas con OneNote para su uso personal después de la reunión, o usar blocs de notas compartidos y coautoría en la reunión en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="347f9-221">During a meeting, users can take notes with OneNote for personal use after the meeting, or use shared notebooks and co-edit with meeting participants in real time.</span></span> <span data-ttu-id="347f9-222">Todos los miembros del equipo pueden acceder a las notas compartidas para colaborar en la información, recopilar ideas o usar las páginas de los blocs de notas como una pizarra virtual.</span><span class="sxs-lookup"><span data-stu-id="347f9-222">All team members can access the shared notes to contribute information, brainstorm ideas, or use the notebook pages as a virtual whiteboard.</span></span> <span data-ttu-id="347f9-223">Las personas y el contenido compartido en la reunión se agregan automáticamente a las notas.</span><span class="sxs-lookup"><span data-stu-id="347f9-223">People and content shared in the meeting are automatically added to the Notes.</span></span>

  - <span data-ttu-id="347f9-224">Los usuarios pueden cambiar de un tipo de contenido a otro usando **compartir contenido y coordinar actividades** de la reunión en la parte inferior de la sala de reuniones.</span><span class="sxs-lookup"><span data-stu-id="347f9-224">Users can switch between content types using **Share content and lead meeting activities** at the bottom of the meeting room.</span></span> <span data-ttu-id="347f9-225">Los usuarios también pueden usar el menú **administrar contenido** presentable para elegir el contenido que desean compartir.</span><span class="sxs-lookup"><span data-stu-id="347f9-225">Users can also use the **Manage Presentable Content** menu to choose which content they want to share.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="347f9-226">Vea también</span><span class="sxs-lookup"><span data-stu-id="347f9-226">See Also</span></span>


[<span data-ttu-id="347f9-227">Planificación de clientes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="347f9-227">Planning for clients in Lync Server 2013</span></span>](lync-server-2013-planning-for-clients.md)  
  

<span data-ttu-id="347f9-228"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="347f9-228"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

