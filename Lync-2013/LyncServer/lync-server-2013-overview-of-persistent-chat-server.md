---
title: 'Lync Server 2013: Información general del servidor de chat en grupo'
description: 'Lync Server 2013: información general sobre el servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Persistent Chat Server
ms:assetid: 23f7c886-304d-495a-ae70-3cbb44241acd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425717(v=OCS.15)
ms:contentKeyID: 48183622
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bbcb396522611aca52bd2093f2fd49f376341356
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424761"
---
# <a name="overview-of-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="48ae8-103">Información general del servidor de chat en grupo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="48ae8-103">Overview of Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48ae8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48ae8-104">

<span> </span></span></span>

<span data-ttu-id="48ae8-105">_**Última modificación del tema:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="48ae8-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="48ae8-106">Lync Server 2013, el servidor de chat persistente permite a los usuarios participar en conversaciones de varias partes y basadas en temas que persisten a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="48ae8-106">Lync Server 2013, Persistent Chat Server enables users to participate in multiparty, topic-based conversations that persist over time.</span></span> <span data-ttu-id="48ae8-107">El servidor de chat persistente puede ayudar a su organización a hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="48ae8-107">Persistent Chat Server can help your organization do the following:</span></span>

  - <span data-ttu-id="48ae8-108">Mejorar la comunicación entre equipos geográficamente dispersos y con varias funciones.</span><span class="sxs-lookup"><span data-stu-id="48ae8-108">Improve communication between geographically dispersed and cross-functional teams.</span></span> <span data-ttu-id="48ae8-109">Al usar el chat persistente, los equipos pueden compartir de forma eficaz información, ideas y decisiones entre sí.</span><span class="sxs-lookup"><span data-stu-id="48ae8-109">By using Persistent Chat, teams can efficiently share information, ideas, and decisions with one another.</span></span> <span data-ttu-id="48ae8-110">Los mensajes publicados en los salones de chat (foros de discusión) pueden persistir (es decir, pueden estar disponibles a lo largo del tiempo), de modo que puedan participar las personas de diferentes ubicaciones y departamentos, incluso cuando no estén conectados de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="48ae8-110">The messages posted to chat rooms (discussion forums) can persist (that is, can be available over time), so that people from different locations and departments can participate, even when they are not simultaneously online.</span></span> <span data-ttu-id="48ae8-111">Cuando un usuario se conecta a un salón de chat, el chat de postales (un número configurable de mensajes del historial de conversaciones) se carga automáticamente en el salón de chat para darle al usuario un contexto para la conversación.</span><span class="sxs-lookup"><span data-stu-id="48ae8-111">When a user connects to a chat room, backchat (a configurable number of chat-history messages) is automatically loaded in the chat room to give the user a context for the conversation.</span></span>

  - <span data-ttu-id="48ae8-112">Mejorar el conocimiento de la información.</span><span class="sxs-lookup"><span data-stu-id="48ae8-112">Improve information awareness.</span></span> <span data-ttu-id="48ae8-113">Al usar filtros de cliente, los usuarios pueden definir condiciones, como palabras clave en el contenido del mensaje o el valor del campo "de" en un mensaje, para recibir una notificación cuando estas condiciones se cumplan en mensajes instantáneos de chat persistente o en mensajes de salones de chat.</span><span class="sxs-lookup"><span data-stu-id="48ae8-113">By using client-side filters, users can define conditions—such as keywords in message content, or the value of the "from" field in a message—to receive notification when those conditions are met in Persistent Chat instant messages or chat room messages.</span></span> <span data-ttu-id="48ae8-114">De esta manera, los usuarios pueden mantenerse al día con el contenido que más les interesa.</span><span class="sxs-lookup"><span data-stu-id="48ae8-114">This way, users can stay up-to-date with the content that interests them most.</span></span>

  - <span data-ttu-id="48ae8-115">Mejorar la comunicación con su organización extendida.</span><span class="sxs-lookup"><span data-stu-id="48ae8-115">Improve communication with their extended organization.</span></span> <span data-ttu-id="48ae8-116">Al facilitar la colaboración en temas de larga ejecución con otras personas de la organización y proporcionando un lugar persistente para compartir información, el chat persistente ayuda a mejorar la comunicación.</span><span class="sxs-lookup"><span data-stu-id="48ae8-116">By making it easy to collaborate over long-running topics with others in the organization, and by providing a persistent place to share information, Persistent Chat helps improve communication.</span></span>

  - <span data-ttu-id="48ae8-117">Reduzca la sobrecarga de información.</span><span class="sxs-lookup"><span data-stu-id="48ae8-117">Reduce information overload.</span></span> <span data-ttu-id="48ae8-118">Los usuarios pueden seguir las salas de chats y los mensajes de mayor interés mediante filtros de cliente, y pueden agregar salones de chat que deseen seguir a su lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="48ae8-118">Users can follow chat rooms and messages of most interest by using client-side filters, and can add chat rooms they want to follow to their contact list.</span></span>

  - <span data-ttu-id="48ae8-119">Aumente la dispersión de información importante y conocimientos.</span><span class="sxs-lookup"><span data-stu-id="48ae8-119">Increase dispersion of important knowledge and information.</span></span> <span data-ttu-id="48ae8-120">Los documentos y vínculos se pueden incluir en las conversaciones para que todo el equipo pueda acceder a ellos.</span><span class="sxs-lookup"><span data-stu-id="48ae8-120">Documents and links can be included within conversations for access by all the team.</span></span> <span data-ttu-id="48ae8-121">Al publicar preguntas en un equipo más amplio, los usuarios pueden beneficiarse de las respuestas de expertos en la materia.</span><span class="sxs-lookup"><span data-stu-id="48ae8-121">By posting questions to a broader team, users can benefit from responses by subject matter experts.</span></span> <span data-ttu-id="48ae8-122">La integración con otros sistemas de información permite comunicar fácilmente datos organizativos importantes a grupos grandes.</span><span class="sxs-lookup"><span data-stu-id="48ae8-122">Integration with other information systems enables important organizational data to be easily communicated to large groups.</span></span>

<span data-ttu-id="48ae8-123">Para habilitar los salones de chat en Lync Server 2013, implemente Lync Server 2013 chat persistente.</span><span class="sxs-lookup"><span data-stu-id="48ae8-123">To enable chat rooms in Lync Server 2013, deploy Lync Server 2013 Persistent Chat.</span></span> <span data-ttu-id="48ae8-124">Para obtener información sobre cómo habilitar salones de chat, consulte la ayuda de chat persistente en <https://go.microsoft.com/fwlink/p/?linkid=270945> .</span><span class="sxs-lookup"><span data-stu-id="48ae8-124">For information about enabling chat rooms, see the Persistent Chat Help at <https://go.microsoft.com/fwlink/p/?linkid=270945>.</span></span> <span data-ttu-id="48ae8-125">Si los usuarios están habilitados para Lync Server y la compatibilidad con Lync Server está implementada, los usuarios pueden instalar y usar Lync 2013 chat persistente para proporcionar compatibilidad con el salón de chat.</span><span class="sxs-lookup"><span data-stu-id="48ae8-125">If users are enabled for Lync Server, and Lync Server support is deployed, users can install and use Lync 2013 Persistent Chat to provide chat room support.</span></span>

<span data-ttu-id="48ae8-126">Si es necesario que su organización siga las normas de cumplimiento, puede implementar el servicio de cumplimiento de chat persistente de manera opcional.</span><span class="sxs-lookup"><span data-stu-id="48ae8-126">If your organization is required to follow compliance regulations, you can optionally deploy Persistent Chat Compliance service.</span></span>

<span data-ttu-id="48ae8-127"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48ae8-127"></div>

<span> </span>

</div>

</div>

</span></span></div>

