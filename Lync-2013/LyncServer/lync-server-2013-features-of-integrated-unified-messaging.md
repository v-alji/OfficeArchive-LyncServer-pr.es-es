---
title: 'Lync Server 2013: Características de la mensajería unificada integrada'
description: 'Lync Server 2013: características de la mensajería unificada integrada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Features of integrated Unified Messaging and Lync Server
ms:assetid: 094f549d-fccc-43ab-9f39-6ddd18130915
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398144(v=OCS.15)
ms:contentKeyID: 48183353
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8e2caa75504c0468293ced8f20946500fad7cf54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428205"
---
# <a name="features-of-integrated-unified-messaging-and-lync-server-2013"></a><span data-ttu-id="1ae7b-103">Características de la mensajería unificada integrada y Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1ae7b-103">Features of integrated Unified Messaging and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1ae7b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1ae7b-104">

<span> </span></span></span>

<span data-ttu-id="1ae7b-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="1ae7b-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="1ae7b-106">Lync Server 2013, Enterprise Voice usa la infraestructura de mensajería unificada (UM) de Exchange para proporcionar contestación de llamadas, notificaciones de llamadas, acceso por voz (incluido el correo de voz) y servicios de operador automático.</span><span class="sxs-lookup"><span data-stu-id="1ae7b-106">Lync Server 2013, Enterprise Voice uses the Exchange Unified Messaging (UM) infrastructure to provide call answering, call notification, voice access (including voice mail), and auto-attendant services.</span></span>

<div>

## <a name="call-answering"></a><span data-ttu-id="1ae7b-107">Respuesta de llamada</span><span class="sxs-lookup"><span data-stu-id="1ae7b-107">Call Answering</span></span>

<span data-ttu-id="1ae7b-108">El contestador automático es la recepción de mensajes de voz en nombre de los usuarios cuyas llamadas no están respondidas o están ocupadas.</span><span class="sxs-lookup"><span data-stu-id="1ae7b-108">Call answering is the receiving of voice messages on behalf of users whose calls are not answered or are busy.</span></span> <span data-ttu-id="1ae7b-109">Incluye la reproducción de un saludo personal, la grabación de un mensaje y el envío del mensaje que se va a poner en la cola para su entrega al buzón del usuario, que se almacena en el servidor de buzones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1ae7b-109">It includes playing a personal greeting, recording a message, and submitting the message to be queued for delivery to the user's mailbox, which is stored on the Exchange mailbox server.</span></span>

<span data-ttu-id="1ae7b-p102">Si el autor de la llamada deja un mensaje, el mensaje se trasfiere a la bandeja de entrada del usuario. Si decide no dejar un mensaje, se almacena una notificación de llamada perdida en el buzón del usuario. Los usuarios pueden acceder a sus bandejas de entrada mediante el cliente de mensajería y colaboración de Microsoft Outlook, Outlook Web Access, la tecnología Exchange ActiveSync o Outlook Voice Access. Se pueden mostrar el asunto y la prioridad de las llamadas de manera similar al correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1ae7b-p102">If a caller leaves a message, the message is routed to the user's Inbox. If a caller chooses not to leave a message, a missed call notification is stored in the user's mailbox. Users can then access their Inbox by using the Microsoft Outlook messaging and collaboration client, Outlook Web Access, the Exchange ActiveSync technology, or Outlook Voice Access. The subject and priority of calls can be displayed in a way similar to that of email.</span></span>

</div>

<div>

## <a name="outlook-voice-access"></a><span data-ttu-id="1ae7b-114">Outlook Voice Access</span><span class="sxs-lookup"><span data-stu-id="1ae7b-114">Outlook Voice Access</span></span>

<span data-ttu-id="1ae7b-115">Outlook Voice Access permite a un usuario de telefonía IP obtener acceso no solo al correo de voz, sino también a la bandeja de entrada de Exchange, que incluye el correo electrónico, el calendario y los contactos de una interfaz de telefonía.</span><span class="sxs-lookup"><span data-stu-id="1ae7b-115">Outlook Voice Access enables an Enterprise Voice user to access not just voice mail, but also the Exchange inbox, including email, calendar, and contacts from a telephony interface.</span></span> <span data-ttu-id="1ae7b-116">El número de acceso de suscriptor es asignado por un administrador de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1ae7b-116">The subscriber access number is assigned by an Exchange UM administrator.</span></span>

</div>

<div>

## <a name="auto-attendant"></a><span data-ttu-id="1ae7b-117">Operador automático</span><span class="sxs-lookup"><span data-stu-id="1ae7b-117">Auto Attendant</span></span>

<span data-ttu-id="1ae7b-118">El operador automático es una característica de mensajería unificada de Exchange que se puede usar para configurar un número de teléfono que no pertenezca a los usuarios para que puedan comunicarse con los representantes de la empresa.</span><span class="sxs-lookup"><span data-stu-id="1ae7b-118">Auto attendant is an Exchange UM feature that can be used to configure a phone number that outside users can dial to reach company representatives.</span></span> <span data-ttu-id="1ae7b-119">En particular, proporciona una serie de mensajes de voz que ayudan a una persona que llama externa a navegar por un sistema de menús.</span><span class="sxs-lookup"><span data-stu-id="1ae7b-119">In particular, it provides a series of voice prompts that assist an external caller in navigating a menu system.</span></span> <span data-ttu-id="1ae7b-120">La lista de opciones disponibles está configurada en el servidor de mensajería unificada de Exchange por el administrador de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1ae7b-120">The list of available options is configured on the Exchange UM server by the Exchange UM administrator.</span></span>

</div>

<div>

## <a name="fax-services"></a><span data-ttu-id="1ae7b-121">Servicios de fax</span><span class="sxs-lookup"><span data-stu-id="1ae7b-121">Fax Services</span></span>

<span data-ttu-id="1ae7b-122">La mensajería unificada de Exchange incluye características de fax, que permiten a los usuarios recibir faxes entrantes en sus buzones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1ae7b-122">Exchange UM includes fax features, which enable users to receive incoming faxes in their Exchange mailboxes.</span></span> <span data-ttu-id="1ae7b-123">Para obtener más información, consulte "mensajería unificada" en la documentación de Microsoft Exchange Server en [https://go.microsoft.com/fwlink/p/?linkId=135652](https://go.microsoft.com/fwlink/p/?linkid=135652) .</span><span class="sxs-lookup"><span data-stu-id="1ae7b-123">For details, see "Unified Messaging" in the Microsoft Exchange Server documentation at [https://go.microsoft.com/fwlink/p/?linkId=135652](https://go.microsoft.com/fwlink/p/?linkid=135652).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1ae7b-124">Los servicios de fax proporcionados por el servidor de mensajería unificada de Exchange no están disponibles en las implementaciones de Lync Server que se integran con Microsoft Exchange Server 2010, Exchange 2010 con el Service Pack más reciente o Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="1ae7b-124">Fax services provided by the Exchange UM server are not available in Lync Server deployments that are integrated with Microsoft Exchange Server 2010, Exchange 2010 with the latest service pack, or Exchange 2013.</span></span>



<span data-ttu-id="1ae7b-125"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1ae7b-125"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

