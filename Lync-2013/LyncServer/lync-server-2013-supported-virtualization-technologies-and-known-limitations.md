---
title: 'Lync Server 2013: Tecnologías de virtualización admitidas y limitaciones comunes'
description: 'Lync Server 2013: tecnologías de virtualización compatibles y limitaciones conocidas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported virtualization technologies and known limitations
ms:assetid: 6d3d749d-e840-4c05-afae-d6e69e7616aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204982(v=OCS.15)
ms:contentKeyID: 48184428
ms.date: 02/07/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 745fa535462d29342f4c0a58674ee6487db42a6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423564"
---
# <a name="supported-virtualization-technologies-and-known-limitations-in-lync-server-2013"></a><span data-ttu-id="0300c-103">Tecnologías de virtualización admitidas y limitaciones comunes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0300c-103">Supported virtualization technologies and known limitations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0300c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0300c-104">

<span> </span></span></span>

<span data-ttu-id="0300c-105">_**Última modificación del tema:** 2017-02-06_</span><span class="sxs-lookup"><span data-stu-id="0300c-105">_**Topic Last Modified:** 2017-02-06_</span></span>

<span data-ttu-id="0300c-106">El complemento VDI para Lync permite llamadas de audio y vídeo para tecnologías de virtualización compatibles.</span><span class="sxs-lookup"><span data-stu-id="0300c-106">The Lync VDI plug-in allows audio and video calling for supported virtualization technologies.</span></span> <span data-ttu-id="0300c-107">Esto extiende la funcionalidad descrita para Microsoft Lync Server 2010 en las notas del producto [de virtualización de cliente en Microsoft lync 2010](https://go.microsoft.com/fwlink/?linkid=330447) .</span><span class="sxs-lookup"><span data-stu-id="0300c-107">This extends the functionality outlined for Microsoft Lync Server 2010 in the [Client Virtualization in Microsoft Lync 2010](https://go.microsoft.com/fwlink/?linkid=330447) white paper.</span></span> <span data-ttu-id="0300c-108">Conforme a las normativas estándar para teléfonos, también se incluye compatibilidad con E911.</span><span class="sxs-lookup"><span data-stu-id="0300c-108">In compliance with standard telephone regulations, support for E911 is also included.</span></span> <span data-ttu-id="0300c-109">En las siguientes secciones se describen las tecnologías de virtualización admitidas por el complemento VDI de Lync y las limitaciones de las características conocidas.</span><span class="sxs-lookup"><span data-stu-id="0300c-109">The following sections describe the virtualization technologies that are supported by the Lync VDI plug-in and the known feature limitations.</span></span>

<div>

## <a name="support-for-virtualization-technologies"></a><span data-ttu-id="0300c-110">Soporte de tecnologías de virtualización</span><span class="sxs-lookup"><span data-stu-id="0300c-110">Support for Virtualization Technologies</span></span>

<span data-ttu-id="0300c-111">El complemento de VDI para Lync es compatible con el entorno remoto de escritorio completo en el escenario de escritorio virtual personal, pero no en el escenario de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="0300c-111">The Lync VDI plug-in supports full desktop remoting in the personal virtual desktop scenario, but not in the remote desktop session scenario.</span></span> <span data-ttu-id="0300c-112">Estos entornos pueden describirse así:</span><span class="sxs-lookup"><span data-stu-id="0300c-112">These scenarios can be described as follows:</span></span>

  - <span data-ttu-id="0300c-113">**Admitido: escritorios virtuales personalizados o infraestructura de escritorio virtual (VDI).**</span><span class="sxs-lookup"><span data-stu-id="0300c-113">**Supported: Personalized Virtual Desktops or Virtual Desktop Infrastructure (VDI).**</span></span>   <span data-ttu-id="0300c-114">En esta situación, cada usuario inicia sesión en un escritorio virtual personalizable y puede guardar archivos en el escritorio, que se conservan entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="0300c-114">In this scenario, each user logs on to a customizable virtual desktop and is able to save files on the desktop that persist across sessions.</span></span> <span data-ttu-id="0300c-115">Los servicios de escritorio remoto de Microsoft, la vista de horizonte de VMware y Citrix XenDesktop son implementaciones probadas para su uso con Lync.</span><span class="sxs-lookup"><span data-stu-id="0300c-115">Microsoft Remote Desktop Services, VMware Horizon View, and Citrix XenDesktop are implementations that have been tested for use with Lync.</span></span> <span data-ttu-id="0300c-116">Para obtener información sobre los entornos de VDI específicos del proveedor y el hardware de cliente que Microsoft ha probado, consulte [infraestructura cualificada para Microsoft Lync](https://go.microsoft.com/fwlink/?linkid=313435).</span><span class="sxs-lookup"><span data-stu-id="0300c-116">For information about vendor-specific VDI environments and client hardware that have been tested by Microsoft, see [Infrastructure qualified for Microsoft Lync](https://go.microsoft.com/fwlink/?linkid=313435).</span></span>

  - <span data-ttu-id="0300c-117">**No admitidos: sesiones de escritorio remoto.**</span><span class="sxs-lookup"><span data-stu-id="0300c-117">**Not supported: Remote Desktop Sessions.**</span></span>   <span data-ttu-id="0300c-118">En este entorno, cada usuario inicia sesión en una sesión de escritorio virtual genérica que no puede personalizarse.</span><span class="sxs-lookup"><span data-stu-id="0300c-118">In this scenario, each user logs on to a generic virtual desktop session that cannot be customized.</span></span> <span data-ttu-id="0300c-119">Algunos ejemplos de implementaciones son las sesiones de escritorio remoto de Microsoft (RDSH) y Citrix XenApp combinadas con Citrix Receiver.</span><span class="sxs-lookup"><span data-stu-id="0300c-119">Example implementations include Microsoft Remote Desktop Sessions (RDSH) and Citrix XenApp combined with Citrix Receiver.</span></span>

<span data-ttu-id="0300c-120">El complemento de VDI para Lync no admite otras tecnologías de virtualización, como la virtualización de aplicaciones, que permite el uso de una aplicación sin requerir la instalación de la aplicación completa de forma local.</span><span class="sxs-lookup"><span data-stu-id="0300c-120">The Lync VDI plug-in does not support other virtualization technologies, such as application virtualization, which allows the use of an application without requiring installation of the full application locally.</span></span> <span data-ttu-id="0300c-121">Algunos ejemplos de implementaciones son Citrix XenApp y Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="0300c-121">Example implementations include Citrix XenApp and Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="0300c-122">El streaming de aplicaciones, la comunicación remota de aplicaciones y los modos mixtos de virtualización (por ejemplo, la comunicación remota de aplicaciones en la comunicación remota de escritorio completa) no se admiten.</span><span class="sxs-lookup"><span data-stu-id="0300c-122">Application streaming, application remoting, and mixed virtualization modes (for example, application remoting in full desktop remoting) are not supported.</span></span>

<span data-ttu-id="0300c-123">Para permitir la extensibilidad, el complemento de VDI para Lync se diseñó para usar las API independientes de la plataforma denominadas canales virtuales dinámicos (DVCs).</span><span class="sxs-lookup"><span data-stu-id="0300c-123">To allow extensibility, the Lync VDI plug-in was designed to use platform-independent APIs called Dynamic Virtual Channels (DVCs).</span></span> <span data-ttu-id="0300c-124">Para escenarios que no son explícitamente compatibles con Lync, consulte declaraciones de soporte técnico del proveedor de soluciones de VDI.</span><span class="sxs-lookup"><span data-stu-id="0300c-124">For scenarios that are not explicitly supported by Lync, refer to support statements from the VDI solution provider.</span></span>

</div>

<div>

## <a name="known-feature-limitations"></a><span data-ttu-id="0300c-125">Limitaciones comunes de la funciones</span><span class="sxs-lookup"><span data-stu-id="0300c-125">Known Feature Limitations</span></span>

<span data-ttu-id="0300c-126">A continuación se muestran algunas limitaciones conocidas al usar Lync 2013 en un entorno de VDI:</span><span class="sxs-lookup"><span data-stu-id="0300c-126">The following are known limitations when you use Lync 2013 in a VDI environment:</span></span>

  - <span data-ttu-id="0300c-127">La delegación de llamadas y las características de anonymization de grupo de respuesta son limitadas.</span><span class="sxs-lookup"><span data-stu-id="0300c-127">There is limited support for Call Delegation and Response Group Agent Anonymization features.</span></span>

  - <span data-ttu-id="0300c-128">No se admiten estas características:</span><span class="sxs-lookup"><span data-stu-id="0300c-128">There is no support for the following features:</span></span>
    
      - <span data-ttu-id="0300c-129">Las páginas de ajuste del dispositivo de audio y de vídeo integrados.</span><span class="sxs-lookup"><span data-stu-id="0300c-129">Integrated Audio Device and Video Device tuning pages.</span></span>
    
      - <span data-ttu-id="0300c-130">El vídeo de múltiples vistas.</span><span class="sxs-lookup"><span data-stu-id="0300c-130">Multiple-view video.</span></span>
    
      - <span data-ttu-id="0300c-131">La grabación de las conversaciones.</span><span class="sxs-lookup"><span data-stu-id="0300c-131">Recording of conversations.</span></span>
    
      - <span data-ttu-id="0300c-132">Servicios de escritorio remoto (RDS).</span><span class="sxs-lookup"><span data-stu-id="0300c-132">Remote Desktop Services (RDS).</span></span>
    
      - <span data-ttu-id="0300c-133">Unirse a reuniones de forma anónima (es decir, unirse a reuniones de Lync hospedadas por una organización que no se federan con su organización).</span><span class="sxs-lookup"><span data-stu-id="0300c-133">Joining meetings anonymously (that is, joining Lync meetings hosted by an organization that does not federate with your organization).</span></span>
    
      - <span data-ttu-id="0300c-134">Usar el complemento VDI de Lync junto con un dispositivo de Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="0300c-134">Using the Lync VDI plug-in along with a Lync Phone Edition device.</span></span>
    
      - <span data-ttu-id="0300c-135">La continuación de llamadas en caso de una interrupción de la red.</span><span class="sxs-lookup"><span data-stu-id="0300c-135">Call continuity in case of a network outage.</span></span>
    
      - <span data-ttu-id="0300c-136">Las características de tonos de llamada personalizados y de música en espera.</span><span class="sxs-lookup"><span data-stu-id="0300c-136">Customized ringtones and music-on-hold features.</span></span>

  - <span data-ttu-id="0300c-137">El complemento de VDI para Lync no es compatible con un entorno de Microsoft 365 o de Office 365.</span><span class="sxs-lookup"><span data-stu-id="0300c-137">The Lync VDI plug-in is not supported in a Microsoft 365 or Office 365 environment.</span></span>

<span data-ttu-id="0300c-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0300c-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

