---
title: 'Lync Server 2013: consideraciones de migración para reuniones'
description: 'Lync Server 2013: consideraciones de migración para reuniones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration considerations for meetings
ms:assetid: a9807d58-99a3-4cff-b4c6-74950d106a2b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412800(v=OCS.15)
ms:contentKeyID: 61097556
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e238405acf7bc2a96fd2efd4cca761c1f1f258fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425587"
---
# <a name="migration-considerations-for-meetings-in-lync-server-2013"></a><span data-ttu-id="7bbdb-103">Consideraciones de migración para las reuniones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7bbdb-103">Migration considerations for meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7bbdb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7bbdb-104">

<span> </span></span></span>

<span data-ttu-id="7bbdb-105">_**Última modificación del tema:** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="7bbdb-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="7bbdb-106">En esta sección se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="7bbdb-106">The following topics are discussed in this section:</span></span>

  - <span data-ttu-id="7bbdb-107">Cambios en las reuniones de Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7bbdb-107">Changes to meetings in Microsoft Lync Server 2013</span></span>

  - <span data-ttu-id="7bbdb-108">Migrar usuarios en función de sus necesidades de conferencia</span><span class="sxs-lookup"><span data-stu-id="7bbdb-108">Migrating users based on their conferencing needs</span></span>

  - <span data-ttu-id="7bbdb-109">Migrar reuniones y contenido de reuniones existentes</span><span class="sxs-lookup"><span data-stu-id="7bbdb-109">Migrating existing meetings and meeting content</span></span>

  - <span data-ttu-id="7bbdb-110">Experiencia del usuario durante la migración de Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="7bbdb-110">User experience during Lync Server 2010 migration</span></span>

  - <span data-ttu-id="7bbdb-111">Experiencia del usuario durante la migración de Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7bbdb-111">User Experience during Office Communications Server 2007 R2 migration</span></span>

  - <span data-ttu-id="7bbdb-112">Compatibilidad de Microsoft Lync 2013 con reuniones en versiones anteriores de un servidor</span><span class="sxs-lookup"><span data-stu-id="7bbdb-112">Microsoft Lync 2013 compatibility with meetings on earlier server versions</span></span>

<div>

## <a name="changes-to-meetings-in-lync-server-2013"></a><span data-ttu-id="7bbdb-113">Cambios en las reuniones de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7bbdb-113">Changes to Meetings in Lync Server 2013</span></span>

<span data-ttu-id="7bbdb-114">**Características de Lync Server 2013.**</span><span class="sxs-lookup"><span data-stu-id="7bbdb-114">**Lync Server 2013 features.**</span></span>   <span data-ttu-id="7bbdb-115">Lync Server 2013 proporciona nuevas características de conferencia que estarán disponibles para los usuarios después de que sus cuentas se muevan a Lync Server 2013 y que inicien sesión con el cliente de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-115">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="7bbdb-116">Las nuevas características se describen en [las nuevas características de conferencia de Lync server 2013](lync-server-2013-new-conferencing-features.md) y las novedades [de los clientes en Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="7bbdb-116">New features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="7bbdb-117">**Dirección URL de la reunión.**</span><span class="sxs-lookup"><span data-stu-id="7bbdb-117">**Meeting URL.**</span></span>   <span data-ttu-id="7bbdb-118">Al igual que en Lync Server 2010, todas las reuniones recién programadas en Lync Server 2013 tienen un prefijo de dirección URL de https://y las reuniones existentes se migran con las cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-118">As in Lync Server 2010, all newly scheduled meetings in Lync Server 2013 have a URL prefix of https:// and existing meetings migrate along with user accounts.</span></span> <span data-ttu-id="7bbdb-119">Sin embargo, Lync Server 2013 no admite la llamada de conferencia de Office Communications Server 2007 R2 (Prefijo de URL de conf://) o la conferencia web (Prefijo de dirección URL de meet://).</span><span class="sxs-lookup"><span data-stu-id="7bbdb-119">However, Lync Server 2013 does not support the Office Communications Server 2007 R2 conference call (conf:// URL prefix) or web conference (meet:// URL prefix).</span></span> <span data-ttu-id="7bbdb-120">Para obtener más información, vea "migrar reuniones de Office Communications Server 2007 R2" más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-120">See “Migrating Meetings from Office Communications Server 2007 R2” later in this topic for more information.</span></span>

<span data-ttu-id="7bbdb-121">**Compatibilidad con clientes.**</span><span class="sxs-lookup"><span data-stu-id="7bbdb-121">**Client support.**</span></span>   <span data-ttu-id="7bbdb-122">A diferencia de Lync Server 2010, Lync Server 2013 no es compatible con los clientes de Office Communicator para conferencias.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-122">Unlike Lync Server 2010, Lync Server 2013 does not support Office Communicator clients for conferencing.</span></span> <span data-ttu-id="7bbdb-123">No puede usar los siguientes clientes para unirse a reuniones programadas a través del complemento de reuniones en línea para Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="7bbdb-123">You cannot use the following clients to join meetings scheduled through the Online Meeting Add-in for Lync 2013:</span></span>

  - <span data-ttu-id="7bbdb-124">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7bbdb-124">Office Communicator 2007 R2</span></span>

  - <span data-ttu-id="7bbdb-125">Operador de Microsoft Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7bbdb-125">Microsoft Office Communications Server 2007 R2 Attendant</span></span>

  - <span data-ttu-id="7bbdb-126">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="7bbdb-126">Office Communicator 2007</span></span>

  - <span data-ttu-id="7bbdb-127">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="7bbdb-127">Office Live Meeting 2007</span></span>

<span data-ttu-id="7bbdb-128">Durante la migración, los usuarios de Office Communicator 2007 R2 deben usar Lync Web App 2013 para unirse a las reuniones de Lync Server 2013 hasta que sus clientes se actualicen.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-128">During migration, Office Communicator 2007 R2 users should use Lync Web App 2013 to join Lync Server 2013 meetings until their clients are upgraded.</span></span> <span data-ttu-id="7bbdb-129">Tenga en cuenta que los usuarios de Office Communicator 2007 R2 pueden continuar usando su cliente existente en Lync Server 2013 para las características de presencia y mensajería instantánea, pero no son compatibles con las características de conferencia.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-129">Note that Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

<div>


</div>

</div>

<div>

## <a name="migrating-users-based-on-their-conferencing-needs"></a><span data-ttu-id="7bbdb-130">Migrar usuarios en función de sus necesidades de conferencia</span><span class="sxs-lookup"><span data-stu-id="7bbdb-130">Migrating Users Based on Their Conferencing Needs</span></span>

<span data-ttu-id="7bbdb-131">**Organizadores de reuniones frecuentes.**</span><span class="sxs-lookup"><span data-stu-id="7bbdb-131">**Frequent meeting organizers.**</span></span>   <span data-ttu-id="7bbdb-132">Considere migrar con frecuencia los organizadores de reuniones al principio del proceso para poder aprovechar las nuevas características de Lync Server 2013 y Lync 2013 descritas en [las nuevas características de conferencia de Lync server 2013](lync-server-2013-new-conferencing-features.md) y las novedades [de los clientes en Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="7bbdb-132">Consider migrating frequent meeting organizers early in the process so that they can take advantage of the new Lync Server 2013 and Lync 2013 features outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="7bbdb-133">**Usuarios de Live Meeting.**</span><span class="sxs-lookup"><span data-stu-id="7bbdb-133">**Live Meeting users.**</span></span>   <span data-ttu-id="7bbdb-134">Si va a migrar desde Office Communications Server 2007 R2 y tiene usuarios que necesitan características de conferencias web específicas de Live Meeting, especialmente en el caso de reuniones y salas de despiece de gran tamaño, tiene las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="7bbdb-134">If you are migrating from Office Communications Server 2007 R2 and you have users who need web conferencing features specific to Live Meeting—particularly support for large meetings and break-out rooms—you have the following options:</span></span>

  - <span data-ttu-id="7bbdb-135">Aconseje a los organizadores que usen el servicio de Live Meeting, si está disponible en su organización.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-135">Advise organizers to use the Live Meeting service, if available in your organization.</span></span>

  - <span data-ttu-id="7bbdb-136">Deje los organizadores alojados en la versión anterior de Office Communications Server para que puedan continuar con la programación de conferencias web de Live Meeting basadas en servidor.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-136">Leave the organizers homed on the earlier version of Office Communications Server, so they can continue to schedule server-based Live Meeting web conferences.</span></span>

</div>

<div>

## <a name="migrating-existing-meetings-and-meeting-content"></a><span data-ttu-id="7bbdb-137">Migrar reuniones y contenido de reuniones existentes</span><span class="sxs-lookup"><span data-stu-id="7bbdb-137">Migrating Existing Meetings and Meeting Content</span></span>

<div>

## <a name="migrating-meetings-from-lync-server-2010"></a><span data-ttu-id="7bbdb-138">Migrar reuniones desde Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="7bbdb-138">Migrating Meetings from Lync Server 2010</span></span>

<span data-ttu-id="7bbdb-139">Al mover un usuario de Lync Server 2010 a Lync Server 2013, la siguiente información se mueve con la cuenta del usuario:</span><span class="sxs-lookup"><span data-stu-id="7bbdb-139">When you move a user from Lync Server 2010 to Lync Server 2013, the following information moves with the user’s account:</span></span>

  - <span data-ttu-id="7bbdb-140">Reuniones ya programadas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-140">Meetings already scheduled by the user.</span></span> <span data-ttu-id="7bbdb-141">Esto incluye los directorios de conferencias y los datos de conferencia.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-141">This includes conferencing directories and conferencing data.</span></span>

  - <span data-ttu-id="7bbdb-142">Número de identificación personal (PIN) del usuario.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-142">The user’s personal identification number (PIN).</span></span> <span data-ttu-id="7bbdb-143">El PIN actual del usuario sigue funcionando hasta que venza o cuando el usuario solicite un nuevo PIN.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-143">The user’s current PIN continues to work until it expires or the user requests a new PIN.</span></span>

<span data-ttu-id="7bbdb-144">Sin embargo, la siguiente información de la cuenta de usuario no se mueve al nuevo servidor:</span><span class="sxs-lookup"><span data-stu-id="7bbdb-144">However, the following user account information does not move to the new server:</span></span>

  - <span data-ttu-id="7bbdb-145">Contenido de la reunión, por ejemplo, presentaciones de PowerPoint, contenido de pizarra y datos de sondeos</span><span class="sxs-lookup"><span data-stu-id="7bbdb-145">Meeting content, for example PowerPoint presentations, whiteboard content, and poll data</span></span>

<span data-ttu-id="7bbdb-146">Para mover el contenido que se ha compartido en las reuniones, use el parámetro MoveMeetingContent del cmdlet Move-CsUser.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-146">To move the content that has been shared in meetings, use the MoveMeetingContent parameter of the Move-CsUser cmdlet.</span></span> <span data-ttu-id="7bbdb-147">Para obtener más información sobre el uso de este cmdlet, consulte [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) en la documentación de cmdlets de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-147">For details about using this cmdlet, see [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) in the Lync Server 2013 cmdlets documentation.</span></span>

</div>

<div>

## <a name="migrating-meetings-from-office-communications-server-2007-r2"></a><span data-ttu-id="7bbdb-148">Migrar reuniones desde Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7bbdb-148">Migrating Meetings from Office Communications Server 2007 R2</span></span>

<span data-ttu-id="7bbdb-149">Las reuniones de Office Communications Server 2007 R2 son llamadas en conferencia (prefijos de dirección URL conf://) o conferencias web (prefijo meet://URL).</span><span class="sxs-lookup"><span data-stu-id="7bbdb-149">Office Communications Server 2007 R2 meetings are either conference calls (conf:// URL prefix) or web conferences (meet:// URL prefix).</span></span> <span data-ttu-id="7bbdb-150">Lync Server 2013 no admite estas conferencias de conf://y meet://anteriores, y no se migran junto con la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-150">Lync Server 2013 does not support these earlier conf:// and meet:// conferences, and they are not migrated along with the user account.</span></span> <span data-ttu-id="7bbdb-151">Después de la migración, debe indicar a los usuarios que actualicen los vínculos de las reuniones en línea que hayan programado.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-151">After migration, you should instruct users to update the links for any online meetings they have scheduled.</span></span> <span data-ttu-id="7bbdb-152">Pueden hacerlo después de instalar el cliente de Lync 2013 abriendo una invitación de reunión programada (que actualiza la dirección URL de la reunión) y reenviando la invitación a los participantes.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-152">They can do this after installing the Lync 2013 client by opening a scheduled meeting invitation—which updates the meeting URL—and resending the invitation to participants.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-lync-server-2010-migration"></a><span data-ttu-id="7bbdb-153">Experiencia del usuario durante la migración de Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="7bbdb-153">User Experience during Lync Server 2010 Migration</span></span>

<span data-ttu-id="7bbdb-154">Esta sección proporciona un resumen de la experiencia de conferencia de los usuarios al migrar desde Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-154">This section provides a summary of users’ conferencing experience when migrating from Lync 2010.</span></span> <span data-ttu-id="7bbdb-155">Para obtener más información sobre cómo pueden coexistir los clientes de Lync Server 2013 e interactuar con versiones de cliente y servidor anteriores, consulte [interoperabilidad de cliente en Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span><span class="sxs-lookup"><span data-stu-id="7bbdb-155">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="joining-lync-server-2010-meetings-with-a-lync-2013-client"></a><span data-ttu-id="7bbdb-156">Unirse a reuniones de Lync Server 2010 con un cliente de Lync 2013</span><span class="sxs-lookup"><span data-stu-id="7bbdb-156">Joining Lync Server 2010 Meetings with a Lync 2013 Client</span></span>

<span data-ttu-id="7bbdb-157">Durante la migración desde Lync Server 2010, es posible que haya un período de coexistencia cuando los usuarios se unan a reuniones de Lync Server 2010 con un cliente de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-157">During migration from Lync Server 2010, there may be a period of coexistence when users join Lync Server 2010 meetings with a Lync 2013 client.</span></span> <span data-ttu-id="7bbdb-158">Estos usuarios tienen acceso a las características de cliente de Lync 2013 con las siguientes excepciones:</span><span class="sxs-lookup"><span data-stu-id="7bbdb-158">These users have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="7bbdb-159">En las opciones de administración de **participantes** , a las que se puede acceder seleccionando el icono de personas en la ventana de la reunión, la opción **sin mensajería instantánea** no funciona.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-159">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="7bbdb-160">La vista de Galería no funciona en las videoconferencias.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-160">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="7bbdb-161">El usuario solo ve el orador activo en lugar de todos los altavoces.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-161">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="7bbdb-162">En la lista de opciones de **diseño** , la **vista de Galería** no está disponible</span><span class="sxs-lookup"><span data-stu-id="7bbdb-162">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="7bbdb-163">La lista de participantes se muestra de forma predeterminada en las videoconferencias.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-163">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="7bbdb-164">Al hacer clic con el botón derecho en un usuario de la lista participantes, las opciones **bloquear las imágenes destacadas** y **anclar a la Galería** no estarán disponibles.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-164">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-office-communications-server-2007-r2-migration"></a><span data-ttu-id="7bbdb-165">Experiencia del usuario durante la migración de Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7bbdb-165">User Experience during Office Communications Server 2007 R2 Migration</span></span>

<span data-ttu-id="7bbdb-166">Esta sección proporciona un resumen de la experiencia de conferencia de los usuarios al migrar desde Office Communications Server 2007 R2, tanto antes como después de instalar Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-166">This section provides a summary of users’ conferencing experience when migrating from Office Communications Server 2007 R2, both before and after Lync 2013 is installed.</span></span> <span data-ttu-id="7bbdb-167">Para obtener más información sobre cómo pueden coexistir los clientes de Lync Server 2013 e interactuar con versiones de cliente y servidor anteriores, consulte [interoperabilidad de cliente en Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span><span class="sxs-lookup"><span data-stu-id="7bbdb-167">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="after-user-account-is-migrated-before-lync-2013-is-installed"></a><span data-ttu-id="7bbdb-168">Después de migrar la cuenta de usuario, antes de instalar Lync 2013</span><span class="sxs-lookup"><span data-stu-id="7bbdb-168">After User Account is Migrated, Before Lync 2013 Is Installed</span></span>

<span data-ttu-id="7bbdb-169">Después de que un usuario se migra al servidor de Lync Server 2013, pero antes de que se instalen nuevos clientes, los usuarios de Office Communicator 2007 R2 pueden continuar usando su cliente existente en Lync Server 2013 para las características de presencia y mensajería instantánea, pero no se admiten las características de conferencia.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-169">After a user is migrated to the Lync Server 2013 server, but before new clients are installed, Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

</div>

<div>

## <a name="after-user-account-is-migrated-after-lync-2013-is-installed"></a><span data-ttu-id="7bbdb-170">Después de migrar la cuenta de usuario, después de instalar Lync 2013</span><span class="sxs-lookup"><span data-stu-id="7bbdb-170">After User Account is Migrated, After Lync 2013 Is Installed</span></span>

<span data-ttu-id="7bbdb-171">Cuando un usuario migrado instala Lync 2013, también se instala el complemento de reunión en línea para Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-171">When a migrated user installs Lync 2013, the Online Meeting Add-in for Lync 2013 is installed too.</span></span> <span data-ttu-id="7bbdb-172">Esto tiene los siguientes efectos:</span><span class="sxs-lookup"><span data-stu-id="7bbdb-172">This has the following effects:</span></span>

  - <span data-ttu-id="7bbdb-173">Todas las reuniones programadas posteriormente usan el nuevo formato de reunión, que usa una dirección de https://en lugar de la dirección heredada de meet://Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-173">All subsequently scheduled meetings use the new meeting format, which uses an https:// address instead of the legacy meet:// Live Meeting address.</span></span>

  - <span data-ttu-id="7bbdb-174">En una implementación administrada por ti de Lync 2013, el administrador tiene la opción de desinstalar el complemento de conferencias para Microsoft Office Outlook, que se usa para programar Live Meeting Server y las reuniones basadas en servicios.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-174">In an IT-managed deployment of Lync 2013, the administrator has the option of uninstalling the Conferencing Add-in for Microsoft Office Outlook, which is used to schedule Live Meeting server and service-based meetings.</span></span> <span data-ttu-id="7bbdb-175">Sin embargo, es posible que tenga usuarios que necesiten continuar programando reuniones de servicio de Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-175">However, you may have users who need to continue to schedule Live Meeting service meetings.</span></span> <span data-ttu-id="7bbdb-176">En este caso, puede permitir que ambos complementos coexistan.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-176">In this case, you can allow both add-ins to coexist.</span></span>

</div>

<div>

## <a name="meetings-with-federated-organizations-that-use-previous-clients"></a><span data-ttu-id="7bbdb-177">Reuniones con organizaciones federadas que usan clientes anteriores</span><span class="sxs-lookup"><span data-stu-id="7bbdb-177">Meetings with Federated Organizations that Use Previous Clients</span></span>

<span data-ttu-id="7bbdb-178">Los usuarios de organizaciones federadas que usan Microsoft Office Communicator 2007 no pueden unirse a reuniones de Lync Server 2013 de su organización si dichas reuniones están bloqueadas por el organizador.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-178">Users in federated organizations who are using Microsoft Office Communicator 2007 cannot join Lync Server 2013 meetings in your organization if those meetings are locked by the organizer.</span></span> <span data-ttu-id="7bbdb-179">Debe reprogramar estas reuniones en Lync Server 2013 de modo que cuando los participantes federados se unan a la reunión con la nueva dirección URL de la reunión de https://, pueden usar Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="7bbdb-179">You have to reschedule these meetings in Lync Server 2013 so when federated participants join the meeting by using the new https:// meeting URL, they can use Lync Web App.</span></span>

<span data-ttu-id="7bbdb-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7bbdb-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

