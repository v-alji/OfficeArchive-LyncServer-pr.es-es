---
title: 'Lync Server 2013: Compatibilidad con reuniones grandes'
description: Soporte técnico de Lync Server 2013 para reuniones grandes.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for large meetings
ms:assetid: 8f0446d5-1ed9-4ea0-bb97-6c062a98a1eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205090(v=OCS.15)
ms:contentKeyID: 48184820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb37cbfb95e36b9a07604eb4fbbc548e4d7ce9a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423669"
---
# <a name="support-for-large-meetings-in-lync-server-2013"></a><span data-ttu-id="68827-103">Compatibilidad con reuniones grandes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68827-103">Support for large meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68827-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68827-104">

<span> </span></span></span>

<span data-ttu-id="68827-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="68827-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="68827-106">Lync Server 2013 puede admitir reuniones con hasta 1000 participantes que usan conferencias de audio y vídeo (A/V), incluidas las presentaciones de PowerPoint en uso compartido.</span><span class="sxs-lookup"><span data-stu-id="68827-106">Lync Server 2013 can support meetings with up to 1000 participants using audio/video (A/V) conferencing, including sharing PowerPoint presentations.</span></span> <span data-ttu-id="68827-107">Esta compatibilidad requiere un grupo dedicado configurado para admitir reuniones grandes y administrado de manera que garantice que solo hospedará una reunión grande al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="68827-107">This support requires a dedicated pool configured to support large meetings and managed in a way that ensures hosting of only a single large meeting at a time.</span></span>

<span data-ttu-id="68827-108">En esta sección se describe cómo admitir reuniones grandes con un grupo de servidores de Lync Server 2013 dedicado.</span><span class="sxs-lookup"><span data-stu-id="68827-108">This section describes how to support large meetings using a dedicated Lync Server 2013 pool.</span></span> <span data-ttu-id="68827-109">Describe las consideraciones de escalabilidad y los requisitos de implementación de un grupo dedicado, incluidos los requisitos de topología, hardware, software y configuración.</span><span class="sxs-lookup"><span data-stu-id="68827-109">It describes scalability considerations and the implementation requirements for a dedicated pool, including topology, hardware, software, and configuration requirements.</span></span> <span data-ttu-id="68827-110">También proporciona un conjunto de recomendaciones de procedimientos recomendados para admitir reuniones grandes, un resumen de los métodos de prueba y los resultados de las pruebas de escalabilidad de servidores realizados por el equipo de ingeniería de Lync Server y las respuestas a las preguntas más frecuentes sobre soporte técnico para reuniones de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="68827-110">It also provides a set of best practice recommendations for supporting large meetings, a summary of the test methods and results of server scalability testing conducted by the Lync Server engineering team, and the answers to frequently asked questions about support for large meetings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="68827-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="68827-111">In This Section</span></span>

  - [<span data-ttu-id="68827-112">Información general sobre la escalabilidad de conferencias en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68827-112">Overview of conferencing scalability in Lync Server 2013</span></span>](lync-server-2013-conferencing-scalability-overview.md)

  - [<span data-ttu-id="68827-113">Compatibilidad con reuniones grandes con Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68827-113">Supporting large meetings using Lync Server 2013</span></span>](lync-server-2013-supporting-large-meetings.md)

  - [<span data-ttu-id="68827-114">Preguntas más frecuentes sobre la compatibilidad con reuniones grandes para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68827-114">Large meeting support FAQ for Lync Server 2013</span></span>](lync-server-2013-large-meeting-support-faq.md)

<span data-ttu-id="68827-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68827-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

