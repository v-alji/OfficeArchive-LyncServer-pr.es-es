---
title: 'Lync Server 2013: Características y funcionalidades de los servidores front-end, la mensajería instantánea y la presencia'
description: 'Lync Server 2013: características y funcionalidad de los servidores front-end, la mensajería instantánea y la presencia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Features and functionality of Front End Servers, instant messaging, and presence
ms:assetid: 05b29536-dcd7-49b5-934a-2ebf20ddc45c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398109(v=OCS.15)
ms:contentKeyID: 48183294
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5c8bc3db255228da3366eb5aa142cd5adc233d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398177"
---
# <a name="features-and-functionality-of-front-end-servers-instant-messaging-and-presence-in-lync-server-2013"></a><span data-ttu-id="1523b-103">Características y funcionalidades de los servidores front-end, la mensajería instantánea y la presencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1523b-103">Features and functionality of Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1523b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1523b-104">

<span> </span></span></span>

<span data-ttu-id="1523b-105">_**Última modificación del tema:** 2013-03-17_</span><span class="sxs-lookup"><span data-stu-id="1523b-105">_**Topic Last Modified:** 2013-03-17_</span></span>

<span data-ttu-id="1523b-106">Los servidores front-end proporcionan la mayor parte de la funcionalidad de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1523b-106">Front End Servers provide most Lync Server functionality.</span></span> <span data-ttu-id="1523b-107">Hay dos ediciones disponibles: Lync Server Enterprise Edition, que está diseñado principalmente para organizaciones de mayor tamaño, y Lync Server Standard Edition, que está diseñado principalmente para organizaciones pequeñas que desean una Investement de hardware más pequeña y no requieren una alta disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="1523b-107">There are two editions available: Lync Server Enterprise Edition, which is designed primarily for larger organizations, and Lync Server Standard Edition, which is designed primarily for smaller organizations which want a smaller hardware investement and do not require high availability.</span></span> <span data-ttu-id="1523b-108">Ambas ediciones admiten todas las cargas de trabajo de Lync Server, incluidas la mensajería instantánea, presencia, Conferencia y telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="1523b-108">Both editions support all Lync Server workloads including IM, presence, conferencing, and Enterprise Voice.</span></span>

<span data-ttu-id="1523b-109">La mensajería instantánea (MI) permite a los usuarios comunicarse entre sí en tiempo real desde sus equipos y por medio de mensajes basados en texto.</span><span class="sxs-lookup"><span data-stu-id="1523b-109">Instant messaging (IM) enables your users to communicate with each other in real time on their computers using text-based messages.</span></span> <span data-ttu-id="1523b-110">Se admiten sesiones de mensajería instantánea con dos participantes y con varios participantes.</span><span class="sxs-lookup"><span data-stu-id="1523b-110">Both two-party and multiparty IM sessions are supported.</span></span> <span data-ttu-id="1523b-111">Un participante de una conversación de mensajería instantánea entre dos participantes puede agregar a la conversación a un tercer participante en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="1523b-111">A participant in a two-party IM conversation can add a third participant to the conversation at any time.</span></span> <span data-ttu-id="1523b-112">Cuando esto ocurre, la ventana Conversación cambia para admitir características de conferencia.</span><span class="sxs-lookup"><span data-stu-id="1523b-112">When this happens, the Conversation window changes to support conferencing features.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="1523b-113">Los clientes de Lync y Communicator, cuando participan en una sola comunicación, se suelen denominar de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="1523b-113">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="1523b-114">Técnicamente, los dos clientes se comunican en una conversación de una en una, con la unidad de control multipunto de mensajería instantánea (IMMCU) en el medio.</span><span class="sxs-lookup"><span data-stu-id="1523b-114">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="1523b-115">El IMMCU es un componente de servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="1523b-115">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="1523b-116">La colocación de IMMCU en el flujo de trabajo de comunicaciones requerido permite la grabación de detalles de llamadas y otras características que permite el servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="1523b-116">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="1523b-117">La comunicación es de un puerto de origen dinámico en el cliente al puerto del servidor front-end TLS/TCP/5061 (asumiendo el uso de la seguridad de la capa de transporte recomendada).</span><span class="sxs-lookup"><span data-stu-id="1523b-117">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="1523b-118">Por diseño, la comunicación de punto a punto (así como la de mensajería instantánea de varios participantes) solo es posible cuando Lync Server y IMMCU está activo y disponible.</span><span class="sxs-lookup"><span data-stu-id="1523b-118">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<span data-ttu-id="1523b-119">*Presencia* proporciona información a los usuarios sobre el estado de otros en la red.</span><span class="sxs-lookup"><span data-stu-id="1523b-119">*Presence* provides information to users about the status of other on the network.</span></span> <span data-ttu-id="1523b-120">El estado de presencia de un usuario brinda información que ayuda a los demás usuarios a decidir si pueden intentar ponerse en contacto con él y si hacerlo con la mensajería instantánea, el teléfono o el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1523b-120">A user’s presence status provides information to help others decide whether they should try to contact the user and whether to use instant messaging, phone, or email.</span></span> <span data-ttu-id="1523b-121">El estado de presencia fomenta la comunicación instantánea cada vez que sea posible, pero también proporciona información sobre si un usuario está en una reunión o fuera de la oficina, indicando que la comunicación instantánea no es posible.</span><span class="sxs-lookup"><span data-stu-id="1523b-121">Presence encourages instant communication when possible, but it also provides information about whether a user is in a meeting or out of the office, indicating that instant communication is not possible.</span></span> <span data-ttu-id="1523b-122">Este estado de presencia se muestra como un icono de presencia en Lync y en otras aplicaciones de presencia, incluidos el cliente de mensajería y colaboración Microsoft Outlook, las tecnologías de Microsoft SharePoint, Microsoft Word y el software de hoja de cálculo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1523b-122">This presence status is displayed as a presence icon in Lync and other presence-aware applications, including the Microsoft Outlook messaging and collaboration client, Microsoft SharePoint technologies, Microsoft Word, and Microsoft Excel spreadsheet software.</span></span> <span data-ttu-id="1523b-123">El icono del estado de presencia representa la disponibilidad y la disposición de comunicación actual del usuario.</span><span class="sxs-lookup"><span data-stu-id="1523b-123">The presence icon represents the user’s current availability and willingness to communicate.</span></span>

<span data-ttu-id="1523b-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1523b-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

