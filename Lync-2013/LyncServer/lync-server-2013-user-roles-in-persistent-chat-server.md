---
title: 'Lync Server 2013: roles de usuario en el servidor de chat persistente'
description: 'Lync Server 2013: roles de usuario en el servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User roles in Persistent Chat Server
ms:assetid: 343a0563-9ca5-4ad0-b4f3-a72f1d7f1a81
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ676774(v=OCS.15)
ms:contentKeyID: 49361095
ms.date: 03/19/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aed64aaa9129e6667cd138bc4365acfb2a64d52c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439165"
---
# <a name="user-roles-in-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="7859e-103">Roles de usuario en el servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7859e-103">User roles in Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7859e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7859e-104">

<span> </span></span></span>

<span data-ttu-id="7859e-105">_**Última modificación del tema:** 2015-03-19_</span><span class="sxs-lookup"><span data-stu-id="7859e-105">_**Topic Last Modified:** 2015-03-19_</span></span>

<span data-ttu-id="7859e-106">El servidor de chat persistente proporciona el concepto de miembros permitidos o denegados, que se aplica a categorías de chat persistentes y controles que pueden acceder a salas en una determinada categoría.</span><span class="sxs-lookup"><span data-stu-id="7859e-106">Persistent Chat Server provides the concept of Allowed/Denied members, which applies to Persistent Chat categories and controls who can access rooms in a particular category.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="7859e-107">Los miembros permitidos o denegados de una categoría no son iguales a los de un rol de <STRONG>miembro</STRONG> , que se aplica a un salón de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="7859e-107">Allowed/Denied members in a Category is not the same as a <STRONG>Member</STRONG> role, which applies to a Persistent Chat room.</span></span><BR><span data-ttu-id="7859e-108">Las búsquedas muestran todos los salones de chat abiertos y cerrados en los que el usuario que realiza la búsqueda se encuentra en la lista de miembros permitido o denegado.</span><span class="sxs-lookup"><span data-stu-id="7859e-108">Searches display all open and closed chat rooms for which the user performing the search is in the Allowed/Denied member list.</span></span> <span data-ttu-id="7859e-109">Los salones secretos no se muestran a menos que el usuario que efectúa la búsqueda sea miembro del salón secreto.</span><span class="sxs-lookup"><span data-stu-id="7859e-109">Secret rooms are not displayed unless the user who performs the search is a member of the secret room.</span></span> <span data-ttu-id="7859e-110">De este modo, el usuario solo puede buscar salones de los que sea miembro o aquellos a los que pueda solicitar ser miembro.</span><span class="sxs-lookup"><span data-stu-id="7859e-110">The user can search only for rooms that he or she is already a member of, or those for which they can request membership.</span></span>



</div>

<span data-ttu-id="7859e-111">El fundamento principal para el concepto de miembros permitidos o rechazados son las paredes éticas.</span><span class="sxs-lookup"><span data-stu-id="7859e-111">The primary rationale for the concept of Allowed/Denied Members is ethical walls.</span></span> <span data-ttu-id="7859e-112">Por ejemplo, en las instituciones financieras y bancarias, es muy común disponer de límites de protección que impidan a los comerciantes y analistas compartir comunicaciones al implementar directivas y convenciones.</span><span class="sxs-lookup"><span data-stu-id="7859e-112">For example, it is common in banking and financial institutions to have ethical boundaries that prevent traders and analysts from sharing communications while implementing policies and conventions.</span></span> <span data-ttu-id="7859e-113">Para abordar este requisito, el administrador puede crear categorías de manera que una categoría admita la creación y el uso de salones por parte de los comerciantes, mientras que la otra admita la creación y el uso de salones por parte de los analistas.</span><span class="sxs-lookup"><span data-stu-id="7859e-113">To address this requirement, an administrator can create categories so that one category allows rooms to be created and used by traders, and another category allows rooms to be created and used by analysts.</span></span> <span data-ttu-id="7859e-114">Con esta restricción está diseñada en el sistema, prohíbe agregar un usuario como miembro del salón si la categoría principal lo impide.</span><span class="sxs-lookup"><span data-stu-id="7859e-114">With this constraint is designed into the system prohibits adding a user as a member of the room if the parent category prevents it.</span></span>

<span data-ttu-id="7859e-115">A continuación se muestran los cuatro roles de usuario servidor de chat persistente:</span><span class="sxs-lookup"><span data-stu-id="7859e-115">Following are the four user roles Persistent Chat Server:</span></span>

  - <span data-ttu-id="7859e-116">**Creador:** Usuarios que tienen permisos para crear salones de chat.</span><span class="sxs-lookup"><span data-stu-id="7859e-116">**Creator:** Users who have permissions to create chat rooms.</span></span> <span data-ttu-id="7859e-117">Estos usuarios figuran en la lista de autores de determinadas categorías: pueden crear salones de chat en sus categorías, asignar miembros en función de la categoría y asignar administradores del salón de chat.</span><span class="sxs-lookup"><span data-stu-id="7859e-117">These users are in the Creators list of certain categories: they can create chat rooms in that category, and they can also assign membership according to the category, and assign managers to manage the chat room.</span></span> <span data-ttu-id="7859e-118">El usuario que cree un salón de chat se agregará automáticamente como administrador del salón.</span><span class="sxs-lookup"><span data-stu-id="7859e-118">The user who creates a chat room is automatically added as a manager of the room.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7859e-p104">Los autores solo están autorizados a crear salones de chat. La promoción automática al rol de Administrador es la que permite al Autor delimitar las pertenencias a grupos, etc., en los servicios de chat creados.</span><span class="sxs-lookup"><span data-stu-id="7859e-p104">Being a Creator simply provides rights for creating chat rooms. It is the automatic promotion to Manager that enables the Creator to further refine memberships, managers, and so on, on the created chat services.</span></span>

    
    </div>
    
    <span data-ttu-id="7859e-121">Este rol ofrece la opción de controlar quién crea salones de chat en su organización, lo cual resulta de especial utilidad si desea administrar de forma centralizada creación de salones de chat para garantizar el cumplimiento de directivas y convenciones, con la consiguiente delegación de la administración de la sala de chat a los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="7859e-121">This role exists to give you the option of controlling who creates chat rooms in your organization, particularly if you want to centrally manage creating chat rooms to enforce policies and conventions, and subsequently delegate the chat room management to other users in the organization.</span></span>

  - <span data-ttu-id="7859e-122">**Administrador:** Usuarios que administran las propiedades de un salón de chat.</span><span class="sxs-lookup"><span data-stu-id="7859e-122">**Manager:** Users who manage properties of a chat room.</span></span> <span data-ttu-id="7859e-123">Los administradores de salones de chat pueden modificar la lista de miembros (agregar o quitar miembros), así como la lista de administradores de la sala de chat (agregar y quitar administradores).</span><span class="sxs-lookup"><span data-stu-id="7859e-123">Chat room managers can modify the member list (add and remove members), and modify the chat room managers list (add and remove managers).</span></span> <span data-ttu-id="7859e-124">Los administradores de los salones de chat pueden agregarse a sí mismos a la lista de miembros o de moderadores (en salones de auditorio) para participar en el salón de chat.</span><span class="sxs-lookup"><span data-stu-id="7859e-124">Chat room managers can add themselves to the members or presenters list (for auditorium rooms) so they can participate in the chat room.</span></span> <span data-ttu-id="7859e-125">También pueden deshabilitar salones de chat (los administradores pueden consultar los salones de chat deshabilitados para eliminarlos de forma permanente).</span><span class="sxs-lookup"><span data-stu-id="7859e-125">Chat room managers can also disable chat rooms (administrators can query for disabled chat rooms and can permanently delete them).</span></span> <span data-ttu-id="7859e-126">Los administradores pueden cambiar todas las propiedades de los salones de chat, excepto la categoría del salón de chat.</span><span class="sxs-lookup"><span data-stu-id="7859e-126">Managers can change all the properties of a chat room, except the category of the chat room.</span></span> <span data-ttu-id="7859e-127">Solo el administrador de chat persistente puede cambiar la categoría después de que se haya creado el salón de chat.</span><span class="sxs-lookup"><span data-stu-id="7859e-127">Only the Persistent Chat Administrator can change the category after the chat room has been created.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="7859e-128">En caso de que el administrador también sea autor en otra categoría, estará autorizado a cambiar la categoría a otra en la que esté autorizado a crear salones de chat.</span><span class="sxs-lookup"><span data-stu-id="7859e-128">If the manager is also a Creator in another category, he or she can change the category to one where they are authorized to create rooms.</span></span>

    
    </div>

  - <span data-ttu-id="7859e-129">**Miembro:** Usuarios que son miembros de un salón de chat.</span><span class="sxs-lookup"><span data-stu-id="7859e-129">**Member:** Users who are members of a chat room.</span></span> <span data-ttu-id="7859e-130">Estos usuarios pueden ver los salones de chat en el directorio (incluso si el salón de chat es secreto), así como suscribirte al salón de chat (incluidas las opciones de metadatos como, por ejemplo, los mensajes no leídos, los filtros de ego y los filtros de palabras clave) y participar en el salón de chat (pueden publicar, a menos que el salón sea un salón de Auditorio</span><span class="sxs-lookup"><span data-stu-id="7859e-130">These users can see the chat rooms in the directory (even if the chat room is secret), as well as subscribe to the chat room (including metadata options such as unread messages, ego filters, and keyword filters), and participate in the chat room (can post, unless the room is an auditorium room where only presenters can post, get content, and search).</span></span> <span data-ttu-id="7859e-131">Los usuarios que no son miembros del salón de chat pueden buscar el salón de chat si están en la lista de miembros permitidos de la categoría, pero necesitan solicitar acceso para que se unan a estos salones de chat y tengan acceso al contenido.</span><span class="sxs-lookup"><span data-stu-id="7859e-131">Users who aren’t members of the chat room can search for the chat room if they are in the Allowed Members list of the category, but need to request access to join these chat rooms to access content.</span></span> <span data-ttu-id="7859e-132">(No hay acceso ni aprobaciones de solicitudes integradas en el sistema; estas se realizan externamente por correo electrónico, teléfono u otras formas de contacto).</span><span class="sxs-lookup"><span data-stu-id="7859e-132">(There is no request access or approvals built into the system; these are done externally by email, phone, or other forms of contact.)</span></span>

  - <span data-ttu-id="7859e-133">**Moderador:** Usuarios que pueden publicar en una sala de Auditorio.</span><span class="sxs-lookup"><span data-stu-id="7859e-133">**Presenter:** Users who can post to an auditorium room.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7859e-134">El servidor de chat persistente permite a los usuarios crear y administrar el salón de chat para un sitio específico.</span><span class="sxs-lookup"><span data-stu-id="7859e-134">Persistent Chat Server lets users create and manage chat room for a specific site.</span></span> <span data-ttu-id="7859e-135">Sin embargo, los usuarios no pueden crear ni administrar salones de chat en otros sitios dentro de la misma topología.</span><span class="sxs-lookup"><span data-stu-id="7859e-135">Users cannot, however, create or manage chat rooms on other sites within the same topology.</span></span> <span data-ttu-id="7859e-136">Asegúrese de especificar los creadores y administradores del salón de chat de todos los sitios de su organización.</span><span class="sxs-lookup"><span data-stu-id="7859e-136">Be sure to specify chat room Creators and Managers for all the sites in your organization.</span></span>



</div>

<span data-ttu-id="7859e-137">Los roles siguientes son roles de administrador para el servidor de chat persistente:</span><span class="sxs-lookup"><span data-stu-id="7859e-137">The following roles are administrator roles for Persistent Chat Server:</span></span>

  - <span data-ttu-id="7859e-138">**Administrador de chat persistente (CsPersistentChatAdministrator):** Este es un nuevo rol de control de acceso de Role-Based (RBAC) para administrar y administrar el servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="7859e-138">**Persistent Chat Administrator (CsPersistentChatAdministrator):** This is a new Role-Based Access Control (RBAC) role to administer and manage Persistent Chat Server.</span></span> <span data-ttu-id="7859e-139">Los usuarios o grupos de seguridad designados como CsPersistentChatAdministrator pueden administrar el servidor de chat persistente mediante cmdlets de Windows PowerShell de forma remota (es decir, desde un equipo que no sea el servidor de chat persistente).</span><span class="sxs-lookup"><span data-stu-id="7859e-139">Users or security groups designated as CsPersistentChatAdministrator are able administer Persistent Chat Server by using Windows PowerShell cmdlets remotely (that is, from a computer other than the Persistent Chat Server).</span></span> <span data-ttu-id="7859e-140">El servidor de chat persistente comprueba que el administrador de chat persistente sea miembro del grupo local RTC local Administrators en el servidor front-end del servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="7859e-140">Persistent Chat Server checks that the Persistent Chat Administrator is member of the RTC Local administrator local group on the Persistent Chat Server Front End Server.</span></span>
    
    <span data-ttu-id="7859e-141">El rol CsPersistentChatAdministrator puede administrar salones de chat (modificar todas las propiedades, como la pertenencia, los jefes, las categorías, marcar salas como deshabilitadas), así como crear y administrar categorías de salones de chat que definan quién puede crear y acceder a salones de chat.</span><span class="sxs-lookup"><span data-stu-id="7859e-141">The CsPersistentChatAdministrator role can manage chat rooms (modify all properties including membership, managers, categories, mark rooms as disabled), as well as create and manage chat room categories that define who can create and access chat rooms.</span></span> <span data-ttu-id="7859e-142">Administrators can also mark chat rooms as disabled and clean up chat rooms that are no longer active.</span><span class="sxs-lookup"><span data-stu-id="7859e-142">Administrators can also mark chat rooms as disabled and clean up chat rooms that are no longer active.</span></span> <span data-ttu-id="7859e-143">Administrators are not subject to the Creators or Allowed Members restrictions.</span><span class="sxs-lookup"><span data-stu-id="7859e-143">Administrators are not subject to the Creators or Allowed Members restrictions.</span></span> <span data-ttu-id="7859e-144">Administrators can create any kind of chat room and add themselves as a member to any chat room.</span><span class="sxs-lookup"><span data-stu-id="7859e-144">Administrators can create any kind of chat room and add themselves as a member to any chat room.</span></span> <span data-ttu-id="7859e-145">Los administradores también pueden modificar y administrar la configuración de los chats persistentes (propiedades de grupo, configuración global y configuración de cumplimiento) y también pueden planear e implementar la migración desde una versión anterior de la implementación del servidor de chat a Lync Server 2013 servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="7859e-145">Administrators can also modify and manage Persistent Chat configuration (pool properties, global settings, and compliance configuration) and can also plan and implement migration from an older Group Chat Server deployment to Lync Server 2013 Persistent Chat Server.</span></span>

  - <span data-ttu-id="7859e-146">**Administrador de Lync:** Administrador corporativo general de Lync Server 2013 responsable de la implementación.</span><span class="sxs-lookup"><span data-stu-id="7859e-146">**Lync Administrator:** Overall enterprise administrator for Lync Server 2013 responsible for deployment.</span></span>

  - <span data-ttu-id="7859e-147">**Operations Manager:** Usuario responsable de administrar las operaciones diarias.</span><span class="sxs-lookup"><span data-stu-id="7859e-147">**Operations Manager:** User responsible for managing day-to-day operations.</span></span>

  - <span data-ttu-id="7859e-148">**Desarrolladores y socios de terceros:** Los programadores de terceros amplían el sistema, en especial proporcionando una solución de pared ética para las conversaciones grupales, soporte técnico y herramientas de cumplimiento, clientes web/móviles y un marco para el desarrollo de bot.</span><span class="sxs-lookup"><span data-stu-id="7859e-148">**Third-party developers and partners:** Third-party developers extend the system, in particular providing an ethical wall solution for group conversations, compliance support and tools, web/mobile clients, and a framework for Bot development.</span></span>

<span data-ttu-id="7859e-149"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7859e-149"></div>

<span> </span>

</div>

</div>

</span></span></div>

