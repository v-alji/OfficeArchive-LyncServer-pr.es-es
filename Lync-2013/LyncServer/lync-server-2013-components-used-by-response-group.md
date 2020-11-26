---
title: 'Lync Server 2013: Componentes usados por el grupo de respuesta'
description: 'Lync Server 2013: componentes usados por el grupo de respuesta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Response Group
ms:assetid: 2b058785-47ca-43b7-b3de-6928a60dc685
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425768(v=OCS.15)
ms:contentKeyID: 48183693
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a1e916d9e4bf986bf0337a6f1f1dd918ff2772e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434560"
---
# <a name="components-used-by-response-group-in-lync-server-2013"></a><span data-ttu-id="1273b-103">Componentes usados por el grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1273b-103">Components used by Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1273b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1273b-104">

<span> </span></span></span>

<span data-ttu-id="1273b-105">_**Última modificación del tema:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="1273b-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="1273b-106">La aplicación de grupo de respuesta se habilita automáticamente al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="1273b-106">The Response Group application is automatically enabled when you deploy Enterprise Voice.</span></span> <span data-ttu-id="1273b-107">En esta sección se describen los componentes que admiten la aplicación de grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1273b-107">This section describes the components that support the Response Group application.</span></span>

<div>

## <a name="response-group-components"></a><span data-ttu-id="1273b-108">Componentes de grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="1273b-108">Response Group Components</span></span>

<span data-ttu-id="1273b-109">Los siguientes componentes de Microsoft Lync Server 2013 son compatibles con la aplicación de grupo de respuesta:</span><span class="sxs-lookup"><span data-stu-id="1273b-109">The following Microsoft Lync Server 2013 components support the Response Group application:</span></span>

  - <span data-ttu-id="1273b-110">**Servicio de aplicación**   El servicio de aplicación proporciona una plataforma para implementar, hospedar y administrar aplicaciones de comunicaciones unificadas, como el grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1273b-110">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as Response Group.</span></span> <span data-ttu-id="1273b-111">El servicio de aplicación se instala automáticamente en todos los servidores front-end de un grupo de servidores front-end y en todos los servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="1273b-111">The Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="1273b-112">**Aplicación de grupo de respuesta**   La aplicación de grupo de respuesta es una de las aplicaciones de comunicaciones unificadas que se hospedan en el servicio de aplicación.</span><span class="sxs-lookup"><span data-stu-id="1273b-112">**Response Group application**   The Response Group application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="1273b-113">Se incluye automáticamente al implementar el grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1273b-113">It is included automatically when you deploy Response Group.</span></span> <span data-ttu-id="1273b-114">La aplicación de grupo de respuesta enruta y pone en cola las llamadas entrantes a grupos de agentes.</span><span class="sxs-lookup"><span data-stu-id="1273b-114">The Response Group application routes and queues incoming calls to groups of agents.</span></span>

  - <span data-ttu-id="1273b-115">**Paquete de idioma**   Se necesita un paquete de idioma para admitir texto a voz y reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="1273b-115">**Language pack**   A language pack is required to support text-to-speech and speech recognition.</span></span> <span data-ttu-id="1273b-116">Estas tecnologías de voz se usan al configurar mensajes, como el mensaje de bienvenida y otras solicitudes de respuesta de voz interactiva (IVR) y las respuestas.</span><span class="sxs-lookup"><span data-stu-id="1273b-116">These speech technologies are used when you configure messages, such as the welcome message and other prompts, and interactive voice response (IVR) questions and answers.</span></span> <span data-ttu-id="1273b-117">De forma predeterminada, los 26 paquetes de idioma admitidos se instalan al implementar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1273b-117">By default, the 26 supported language packs are installed when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="1273b-118">**Archivos de audio**   Los archivos de audio se usan para mensajes y música en espera.</span><span class="sxs-lookup"><span data-stu-id="1273b-118">**Audio files**   Audio files are used for messages and on-hold music.</span></span>

  - <span data-ttu-id="1273b-119">**Almacén de archivos**   El grupo de respuesta usa el almacén de archivos para almacenar archivos de audio.</span><span class="sxs-lookup"><span data-stu-id="1273b-119">**File Store**   Response Group uses File store to store audio files.</span></span> <span data-ttu-id="1273b-120">Varios grupos de grupos de respuesta pueden usar la misma instancia del almacén de archivos.</span><span class="sxs-lookup"><span data-stu-id="1273b-120">Multiple Response Group pools can use the same instance of File store.</span></span>

  - <span data-ttu-id="1273b-121">**Herramienta de configuración de grupo de respuesta**   La herramienta de configuración de grupos de respuesta es una herramienta basada en Web que se usa para crear y configurar grupos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1273b-121">**Response Group Configuration Tool**   The Response Group Configuration Tool is a web-based tool that is used to create and configure response groups.</span></span> <span data-ttu-id="1273b-122">La herramienta de configuración de grupos de respuesta se incluye al instalar servicios Web.</span><span class="sxs-lookup"><span data-stu-id="1273b-122">The Response Group Configuration Tool is included when you install Web Services.</span></span>

  - <span data-ttu-id="1273b-123">**Panel de control de Microsoft Lync Server 2013**   Puede usar el panel de control de Lync Server para configurar y configurar colas y grupos de agentes para grupos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1273b-123">**Microsoft Lync Server 2013 Control Panel**   You can use Lync Server Control Panel to setup and configure agent groups and queues for response groups.</span></span>

  - <span data-ttu-id="1273b-124">**Shell de administración de Lync Server**   Todas las opciones de configuración del grupo de respuesta se pueden configurar mediante los cmdlets del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1273b-124">**Lync Server Management Shell**   All Response Group settings can be configured by using Lync Server Management Shell cmdlets.</span></span>

  - <span data-ttu-id="1273b-125">**Microsoft Lync 2013**   Agentes formales (agentes que deben iniciar sesión en el grupo antes de que puedan aceptar llamadas para el grupo) usar Lync 2013 para iniciar y cerrar sesión en el grupo.</span><span class="sxs-lookup"><span data-stu-id="1273b-125">**Microsoft Lync 2013**   Formal agents (agents who are required to sign in to the group before they can accept calls for the group) use Lync 2013 to sign in to and sign out from the group.</span></span> <span data-ttu-id="1273b-126">Si un grupo de agentes está configurado para agentes formales, los agentes deben hacer clic en un elemento de menú de Lync 2013 para abrir Internet Explorer y mostrar una consola de página web para iniciar y cerrar sesión en el grupo.</span><span class="sxs-lookup"><span data-stu-id="1273b-126">If an agent group is configured for formal agents, the agents click a menu item in Lync 2013 to open Internet Explorer and display a webpage console for signing in and out of the group.</span></span>

  - <span data-ttu-id="1273b-127">**Servicios web**   Los servicios web son necesarios para la herramienta de configuración de grupos de respuesta, la consola de inicio de sesión y de inicio de sesión de los agentes, el panel de control de Lync Server y el servicio Web de cliente de grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1273b-127">**Web Services**   Web Services is required for Response Group Configuration Tool, the agents’ sign-in and sign-out console, Lync Server Control Panel, and Response Group client web service.</span></span>

  - <span data-ttu-id="1273b-128">**Servicio Web de cliente de grupo de respuesta**   Aplicación de grupo de respuesta proporciona un servicio Web de cliente, que puede ser usado por aplicaciones de terceros para recuperar información sobre agentes, pertenencia a grupos de agentes, estado de inicio de sesión de agentes, estado de llamadas para grupos y los grupos que admiten llamadas anónimas.</span><span class="sxs-lookup"><span data-stu-id="1273b-128">**Response Group Client Web Service**   Response Group application provides a client web service, which can be used by third-party applications to retrieve information about agents, agent group membership, agent sign-in status, call status for groups, and the groups that support anonymous calls.</span></span> <span data-ttu-id="1273b-129">El operador de Lync 2013 y Lync 2010 use el servicio Web de cliente de grupo de respuesta para recuperar la lista de grupos de respuesta que los agentes pueden usar para realizar llamadas anónimas.</span><span class="sxs-lookup"><span data-stu-id="1273b-129">Lync 2013 and Lync 2010 Attendant use Response Group Client Web service to retrieve the list of response groups that agents can use to make anonymous calls.</span></span> <span data-ttu-id="1273b-130">El servicio Web de cliente se incluye cuando se instalan los servicios Web.</span><span class="sxs-lookup"><span data-stu-id="1273b-130">The client web service is included when you install Web Services.</span></span>

<span data-ttu-id="1273b-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1273b-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

