---
title: 'Lync Server 2013: detalles de programación de reuniones'
description: 'Lync Server 2013: información sobre la programación de reuniones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scheduling details
ms:assetid: 39ca6fff-2c15-4347-9f1f-6c8687a39a49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204823(v=OCS.15)
ms:contentKeyID: 48183910
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef7a6907aedbc880731b3fb474c9294c1c111b80
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442019"
---
# <a name="scheduling-details-for-meetings-in-lync-server-2013"></a><span data-ttu-id="4ed57-103">Detalles de programación de reuniones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4ed57-103">Scheduling details for meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4ed57-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4ed57-104">

<span> </span></span></span>

<span data-ttu-id="4ed57-105">_**Última modificación del tema:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="4ed57-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="4ed57-106">Tras comprobar para asegurarse de que no hay ninguna otra reunión programada a la hora solicitada, el personal de soporte técnico de la gran reunión que administra la solicitud programa la reunión en el grupo de servidores de reuniones grandes.</span><span class="sxs-lookup"><span data-stu-id="4ed57-106">After checking to ensure that no other meeting is scheduled at the requested time, the large meeting support staff that handles the request schedules the meeting on the large-meeting pool.</span></span> <span data-ttu-id="4ed57-107">Use el complemento de reunión en línea para Lync que se instala con el cliente de Lync Server 2013 para realizar esta tarea, usando las credenciales de un usuario habilitado para Lync Server en el grupo de reuniones de gran tamaño dedicado.</span><span class="sxs-lookup"><span data-stu-id="4ed57-107">Use the Online Meeting Add-in for Lync that is installed with the Lync Server 2013 client to perform this task, using the credentials of a user enabled for Lync Server in the dedicated large-meeting pool.</span></span>

<span data-ttu-id="4ed57-108">Para garantizar la mejor experiencia de usuario, es importante programar la reunión grande con los niveles de acceso adecuados y los valores de reunión que sean adecuados para las necesidades del organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="4ed57-108">To ensure the best user experience, it is important to schedule the large meeting with the right access levels and meeting settings that are appropriate to the meeting organizer’s needs.</span></span> <span data-ttu-id="4ed57-109">Recomendamos las siguientes opciones de programación configuradas en las opciones de reunión de Lync:</span><span class="sxs-lookup"><span data-stu-id="4ed57-109">We recommend the following scheduling settings configured in Lync Meeting options:</span></span>

  - <span data-ttu-id="4ed57-110">Use un nuevo espacio de reunión para cada reunión grande en lugar de volver a usar el espacio de reunión dedicado.</span><span class="sxs-lookup"><span data-stu-id="4ed57-110">Use a new meeting space for each large meeting instead of reusing the dedicated meeting space.</span></span>

  - <span data-ttu-id="4ed57-111">Especifique el nivel de acceso de reunión de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="4ed57-111">Specify the meeting access level as follows:</span></span>
    
      - <span data-ttu-id="4ed57-112">Si al menos una de las invitaciones es externa a la organización, establezca el tipo de acceso de la reunión en **cualquiera (sin restricciones**.</span><span class="sxs-lookup"><span data-stu-id="4ed57-112">If at least one invitee is external to the organization, set the meeting access type to **Anyone (no restrictions**.</span></span> <span data-ttu-id="4ed57-113">Esto le habilita para evitar tener que administrar una sala de espera potencialmente grande cuando la reunión está en curso.</span><span class="sxs-lookup"><span data-stu-id="4ed57-113">This enables you to avoid having to manage a potentially large lobby when the meeting is in progress.</span></span>
    
      - <span data-ttu-id="4ed57-114">Si la reunión es solo interna, establezca el tipo de acceso de reunión en **Cualquiera de mi organización**.</span><span class="sxs-lookup"><span data-stu-id="4ed57-114">If the meeting is an internal-only meeting, set the meeting access type to **Anyone from my organization**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="4ed57-115">Evite establecer el tipo de acceso de reunión en <STRONG>Personas de mi compañía a quien invito</STRONG> porque cuando usa esta configuración, los organizadores necesitan agregar todas las direcciones de correo electrónico de usuario a la lista de invitados y no puede invitar a un grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="4ed57-115">Avoid setting the meeting access type to <STRONG>People I invite from my company</STRONG> because when you use this setting, organizers must add all user email addresses to the invitee list and you cannot invite a distribution group.</span></span><BR><span data-ttu-id="4ed57-116">Evite establecer el tipo de acceso de reunión en <STRONG>Solo yo, el organizador de la reunión</STRONG> porque esta configuración requiere que todos los participantes de la reunión, incluidos los moderadores, tengan que colocarse en la sala de espera en el tiempo de ejecución de la reunión.</span><span class="sxs-lookup"><span data-stu-id="4ed57-116">Avoid setting the meeting access type to <STRONG>Only me, the meeting organizer</STRONG> because this setting requires that every meeting participant, including presenters, must be put in the lobby at meeting run time.</span></span> <span data-ttu-id="4ed57-117">La persona responsable de la ejecución de la reunión grande necesita supervisar entonces constantemente la lista de la sala de espera y admitir a nuevos usuarios que estén en la sala de espera.</span><span class="sxs-lookup"><span data-stu-id="4ed57-117">The person responsible for running the large meeting must then constantly monitor the lobby roster and admit new users who are in the lobby.</span></span>

        
        </div>

  - <span data-ttu-id="4ed57-118">Permita a los usuarios que marquen desde teléfonos para entrar en la reunión automáticamente activando la configuración **Los autores de llamada entran directamente**.</span><span class="sxs-lookup"><span data-stu-id="4ed57-118">Allow users who dial-in from phones to enter the meeting automatically by checking the **Callers get in directly** setting.</span></span>

  - <span data-ttu-id="4ed57-119">Invitar de manera explícita a los siguientes usuarios:</span><span class="sxs-lookup"><span data-stu-id="4ed57-119">Explicitly invite the following users:</span></span>
    
      - <span data-ttu-id="4ed57-120">Delegado y organizador de reunión (solicitante)</span><span class="sxs-lookup"><span data-stu-id="4ed57-120">Meeting organizer and delegate (requester)</span></span>
    
      - <span data-ttu-id="4ed57-121">La lista de moderadores proporcionada por un solicitante de reunión</span><span class="sxs-lookup"><span data-stu-id="4ed57-121">The list of presenters provided by a meeting requester</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4ed57-122">Si el tipo de acceso de reunión se establece en <STRONG>Las personas que yo elija</STRONG>, tiene que agregar de manera explícita a cada participante de una reunión grande como invitado de la reunión.</span><span class="sxs-lookup"><span data-stu-id="4ed57-122">If the meeting access type is set to <STRONG>People I choose</STRONG>, you need to explicitly add each participant of a large meeting as an invitee of the meeting.</span></span>

    
    </div>

  - <span data-ttu-id="4ed57-p105">Administrar de manera explícita moderadores, en lugar de establecer la opción de moderador a uno de los valores de promoción automática. Asegúrese de agregar los siguientes usuarios como moderadores:</span><span class="sxs-lookup"><span data-stu-id="4ed57-p105">Explicitly manage presenters, instead of setting the presenter option to one of the auto-promote values. Be sure to add the following users as presenters:</span></span>
    
      - <span data-ttu-id="4ed57-125">Delegado y organizador de reunión (solicitante)</span><span class="sxs-lookup"><span data-stu-id="4ed57-125">Meeting organizer and delegate (requester)</span></span>
    
      - <span data-ttu-id="4ed57-126">La lista de moderadores proporcionada por solicitantes de grandes reuniones</span><span class="sxs-lookup"><span data-stu-id="4ed57-126">The list of presenters provided by large meeting requesters</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4ed57-127">Al administrar los moderadores de forma explícita, puede controlar el número de moderadores, de modo que puede limitar los moderadores a un número tan pequeño para que sea posible tener una reunión de gran tamaño eficaz.</span><span class="sxs-lookup"><span data-stu-id="4ed57-127">By explicitly managing presenters, you can control the number of presenters, so that you can limit presenters to a small enough number to make it possible to have an effective large meeting.</span></span> <span data-ttu-id="4ed57-128">Si la mayoría de los participantes de la reunión tienen el rol de asistente, ayuda a reducir la posibilidad de que las personas tomen el control de la presentación, eliminen una presentación de PowerPoint, pongan o quiten el silencio de los moderadores de manera accidental, y otras interrupciones de la reunión.</span><span class="sxs-lookup"><span data-stu-id="4ed57-128">If the majority of meeting participants have the attendee role, it helps reduce the chance of people accidentally taking control of the presentation, deleting a PowerPoint presentation, muting/unmuting presenters, and other disruptions to the meeting.</span></span>

    
    </div>

  - <span data-ttu-id="4ed57-129">Active la configuración **Silenciar a todos los asistentes** para asegurarse de que solo los moderadores pueden difundir audio a la reunión.</span><span class="sxs-lookup"><span data-stu-id="4ed57-129">Check the **Mute all attendees** setting to make sure that only presenters can broadcast audio into the meeting.</span></span>

  - <span data-ttu-id="4ed57-130">Active la configuración **Bloquear el vídeo de los asistentes** para asegurarse de que solo los moderadores pueden difundir vídeo a la reunión.</span><span class="sxs-lookup"><span data-stu-id="4ed57-130">Check the **Block attendees’ video** setting to make sure only presenters can broadcast video into the meeting.</span></span>

<span data-ttu-id="4ed57-131">La siguiente ilustración muestra la configuración recomendada para el complemento de reunión en línea para Lync.</span><span class="sxs-lookup"><span data-stu-id="4ed57-131">The following figure shows the recommended settings for the Online Meeting Add-in for Lync.</span></span>

<span data-ttu-id="4ed57-132">![54e4e70d-06b0-45cd-8d94-bab649cd5dc0](images/JJ204823.54e4e70d-06b0-45cd-8d94-bab649cd5dc0(OCS.15).jpg "54e4e70d-06b0-45cd-8d94-bab649cd5dc0")</span><span class="sxs-lookup"><span data-stu-id="4ed57-132">![54e4e70d-06b0-45cd-8d94-bab649cd5dc0](images/JJ204823.54e4e70d-06b0-45cd-8d94-bab649cd5dc0(OCS.15).jpg "54e4e70d-06b0-45cd-8d94-bab649cd5dc0")</span></span>

<span data-ttu-id="4ed57-133"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ed57-133"></div>

<span> </span>

</div>

</div>

</span></span></div>

