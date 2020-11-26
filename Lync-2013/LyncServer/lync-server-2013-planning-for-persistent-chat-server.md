---
title: 'Lync Server 2013: Planeación del servidor de chat persistente'
description: 'Lync Server 2013: planificación de servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Persistent Chat Server
ms:assetid: 57b2f574-234e-4a5a-bb78-8823369ba79e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398381(v=OCS.15)
ms:contentKeyID: 48184190
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6944437492a1eee718a614369201c3548c95864a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424455"
---
# <a name="planning-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="f9dc3-103">Planeación del servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9dc3-103">Planning for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9dc3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9dc3-104">

<span> </span></span></span>

<span data-ttu-id="f9dc3-105">_**Última modificación del tema:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="f9dc3-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="f9dc3-106">Puede usar Lync Server 2013, servidor de chat persistente para permitir que varios usuarios participen en las conversaciones en las que publican y tienen acceso al contenido sobre temas específicos, como texto, vínculos y archivos.</span><span class="sxs-lookup"><span data-stu-id="f9dc3-106">You can use Lync Server 2013, Persistent Chat Server to enable multiple users to participate in conversations in which they post and access content about specific topics, including text, links, and files.</span></span> <span data-ttu-id="f9dc3-107">Aunque los usuarios se pueden comunicar en tiempo real durante una sesión, el contenido de cada sesión es persistente, lo que significa que sigue disponible después de que finaliza la sesión.</span><span class="sxs-lookup"><span data-stu-id="f9dc3-107">Although users can communicate in real time during a session, the content of each session is persistent, which means it continues to be available after a session ends.</span></span>

<span data-ttu-id="f9dc3-108">Esta sección describe las consideraciones de planeación en un servidor de Lync 2013, una implementación de servidor de chat persistente, lo que incluye la definición de requisitos, la identificación de componentes y las topologías admitidas, y recomendaciones de implementación.</span><span class="sxs-lookup"><span data-stu-id="f9dc3-108">This section describes planning considerations in a Lync Server 2013, Persistent Chat Server deployment, including defining requirements, identifying components and supported topologies, and deployment recommendations.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f9dc3-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f9dc3-109">In This Section</span></span>

  - [<span data-ttu-id="f9dc3-110">Información general del servidor de chat en grupo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9dc3-110">Overview of Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-overview-of-persistent-chat-server.md)

  - [<span data-ttu-id="f9dc3-111">Cómo funciona el servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9dc3-111">How Persistent Chat Server works in Lync Server 2013</span></span>](lync-server-2013-how-persistent-chat-server-works.md)

  - [<span data-ttu-id="f9dc3-112">Definición de los requisitos de la organización para el servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9dc3-112">Defining your organization's requirements for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="f9dc3-113">Componentes y topologías para el servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9dc3-113">Components and topologies for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-persistent-chat-server.md)

  - [<span data-ttu-id="f9dc3-114">Requisitos técnicos para el servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9dc3-114">Technical requirements for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="f9dc3-115">Configurar los sistemas y la infraestructura para servidores de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9dc3-115">Setting up systems and infrastructure for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-setting-up-systems-and-infrastructure-for-persistent-chat-server.md)

  - [<span data-ttu-id="f9dc3-116">Lista de comprobación para la implementación de servidores de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9dc3-116">Deployment checklist for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-persistent-chat-server.md)

<span data-ttu-id="f9dc3-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9dc3-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

