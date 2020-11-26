---
title: 'Lync Server 2013: configurar la omisión de medios para omitir siempre el servidor de mediación'
description: 'Lync Server 2013: configurar la omisión de elementos multimedia para omitir siempre el servidor de mediación.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure media bypass to always bypass the Mediation Server
ms:assetid: 370c4f54-e520-4d77-96a3-84c5e84a9996
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425846(v=OCS.15)
ms:contentKeyID: 48183819
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b4981c7b12700d2f0bbf0bf05c8a51623bb8ba9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433916"
---
# <a name="configure-media-bypass-in-lync-server-2013-to-always-bypass-the-mediation-server"></a><span data-ttu-id="4a187-103">Configure media bypass in Lync Server 2013 to always bypass the Mediation Server</span><span class="sxs-lookup"><span data-stu-id="4a187-103">Configure media bypass in Lync Server 2013 to always bypass the Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4a187-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4a187-104">

<span> </span></span></span>

<span data-ttu-id="4a187-105">_**Última modificación del tema:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="4a187-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4a187-106">En este tema se supone que ya ha configurado la omisión de medios para cualquier conexión troncal a un interlocutor (una puerta de enlace de red de telefonía pública conmutada (RTC), un IP-PBX o un controlador de borde de sesión (SBC) en un proveedor de servicios de telefonía (ITSP) de Internet</span><span class="sxs-lookup"><span data-stu-id="4a187-106">This topic assumes that you have already configured media bypass for any trunk connections to a peer (a public switched telephone network (PSTN) gateway, an IP-PBX, or a Session Border Controller (SBC) at an Internet Telephony Service Provider (ITSP)) for a specific site or service for which you want media to bypass the Mediation Server.</span></span><BR><span data-ttu-id="4a187-107">No puede configurar los medios para omitir siempre el servidor de mediación y también habilitar el control de admisión de llamadas.</span><span class="sxs-lookup"><span data-stu-id="4a187-107">You cannot configure media to always bypass the Mediation Server while also enabling call admission control.</span></span> <span data-ttu-id="4a187-108">Esta configuración es incompatible y, por lo tanto, es mutuamente excluyente en la interfaz de usuario del panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4a187-108">These settings are incompatible and are therefore mutually exclusive settings in the Lync Server Control Panel user interface.</span></span>



</div>

<span data-ttu-id="4a187-109">Además de habilitar la omisión de medios para conexiones troncales individuales asociadas con un servidor de mediación, también debe establecer la configuración global para la omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="4a187-109">In addition to enabling media bypass for individual trunk connections associated with a peer to the Mediation Server, you must also configure global settings for media bypass.</span></span> <span data-ttu-id="4a187-110">Si usa los pasos de este tema para establecer la configuración global de omisión de elementos multimedia, se supone que tiene una buena conectividad entre los puntos de conexión de Lync y cualquier elemento del mismo nivel para el que haya configurado el bypass de medios en la conexión troncal.</span><span class="sxs-lookup"><span data-stu-id="4a187-110">If you use the steps in this topic to configure global settings for media bypass, the assumption is that you have good connectivity between Lync endpoints and any peer for which you configured media bypass on the trunk connection.</span></span>

<span data-ttu-id="4a187-111">Si no tiene buena conectividad entre los puntos de conexión de Lync Server y todos los elementos del servidor de media cuyas conexiones troncales se han habilitado para la omisión de medios, debe configurar la configuración de omisión de multimedia global para usar la información del sitio y de la región cuando emplee la omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="4a187-111">If you do not have good connectivity between Lync Server endpoints and all peers to the Mediation Server whose respective trunk connections have been enabled for media bypass, you must configure global media bypass settings to use site and region information when employing media bypass.</span></span> <span data-ttu-id="4a187-112">Esto permite un mayor control para determinar cuándo el contenido multimedia pasa por alto el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="4a187-112">This allows for more control in determining when media bypasses the Mediation Server.</span></span> <span data-ttu-id="4a187-113">Para ello, siga los pasos de [configurar la configuración global de omisión de medios en Lync server 2013 para usar la información del sitio y de la región](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md) y [asociar una subred con un sitio de red en Lync Server 2013 en](lync-server-2013-associate-a-subnet-with-a-network-site.md) su lugar.</span><span class="sxs-lookup"><span data-stu-id="4a187-113">To do this, use the steps in [Configure media bypass global settings in Lync Server 2013 to use site and region information](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md) and [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md) instead.</span></span>

<div>

## <a name="to-enable-media-bypass-globally-to-always-bypass-the-mediation-server"></a><span data-ttu-id="4a187-114">Para habilitar globalmente el desvío de medios para que omita siempre el servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="4a187-114">To Enable Media Bypass Globally to Always Bypass the Mediation Server</span></span>

1.  <span data-ttu-id="4a187-115">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4a187-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4a187-116">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4a187-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="4a187-117">En la barra de navegación izquierda, haga clic en **Configuración de red**.</span><span class="sxs-lookup"><span data-stu-id="4a187-117">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="4a187-118">Haga doble clic en la configuración **Global** de la lista.</span><span class="sxs-lookup"><span data-stu-id="4a187-118">Double-click the **Global** configuration in the list.</span></span>

4.  <span data-ttu-id="4a187-119">En la página **Editar configuración global**, seleccione la casilla **Habilitar omisión de medios**.</span><span class="sxs-lookup"><span data-stu-id="4a187-119">On the **Edit Global Setting** page, select the **Enable media bypass** check box.</span></span>

5.  <span data-ttu-id="4a187-120">Haga clic en **Omitir siempre**.</span><span class="sxs-lookup"><span data-stu-id="4a187-120">Click **Always bypass**.</span></span>

6.  <span data-ttu-id="4a187-121">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="4a187-121">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4a187-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a187-122">See Also</span></span>


[<span data-ttu-id="4a187-123">Configurar la omisión de medios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a187-123">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)  
[<span data-ttu-id="4a187-124">Opciones de omisión de multimedia global en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a187-124">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  
[<span data-ttu-id="4a187-125">Omisión de medios y servidor de mediación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a187-125">Media bypass and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-mediation-server.md)  


[<span data-ttu-id="4a187-126">Planificar la omisión de medios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a187-126">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="4a187-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4a187-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

