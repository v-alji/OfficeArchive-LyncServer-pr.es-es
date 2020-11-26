---
title: 'Lync Server 2013: Procedimientos recomendados para el servicio de control de admisión de llamadas'
description: 'Lync Server 2013: procedimientos recomendados para el control de admisión de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for call admission control
ms:assetid: 97173cca-8175-4ae2-a247-eb7ef809da93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398770(v=OCS.15)
ms:contentKeyID: 48184913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17c32af904dc7fb48a1a5d1903bd6ed1f81f4cb3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436072"
---
# <a name="best-practices-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="4b9cd-103">Procedimientos recomendados para el servicio de control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4b9cd-103">Best practices for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b9cd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b9cd-104">

<span> </span></span></span>

<span data-ttu-id="4b9cd-105">_**Última modificación del tema:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="4b9cd-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="4b9cd-106">Para mejorar el rendimiento y facilitar la implementación, sigue los procedimientos recomendados descritos a continuación a la hora de implementar el servicio de control de admisión de llamadas:</span><span class="sxs-lookup"><span data-stu-id="4b9cd-106">To enhance performance and facilitate deployment, apply the following best practices when you deploy call admission control:</span></span>

  - <span data-ttu-id="4b9cd-107">Comprueba que las redes WAN estén correctamente aprovisionadas para el tráfico de medios actual y previsto.</span><span class="sxs-lookup"><span data-stu-id="4b9cd-107">Ensure that WANs are adequately provisioned for current and anticipated media traffic.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4b9cd-p101">Recomendamos tener en cuenta un búfer además de los límites de ancho de banda. Existen escenarios, como condiciones de carrera, que afectan al ancho de banda total usado y pueden dar lugar a situaciones en que se supera el límite de ancho de banda. Por ejemplo, si se intentan iniciar dos llamadas cuando el tráfico de medios está alcanzando un límite de ancho de banda, es posible que una de ellas sea denegada porque la otra intentó iniciarse primero.</span><span class="sxs-lookup"><span data-stu-id="4b9cd-p101">We recommend that you factor in a buffer to your bandwidth limits. There are scenarios such as race conditions that affect the total bandwidth used and can result in situations where the bandwidth limit is exceeded. For example, if two calls try to start while media traffic is approaching a bandwidth limit, one of them may be denied because the other managed to start first.</span></span>

    
    </div>

  - <span data-ttu-id="4b9cd-111">Supervisa el uso de red y los registros de detalles de llamadas para que puedas elegir una configuración óptima de CAC y actualizarla conforme el uso de la red va cambiando.</span><span class="sxs-lookup"><span data-stu-id="4b9cd-111">Monitor network usage and call detail records so that you can choose optimal CAC settings and update CAC settings as network usage changes.</span></span>

  - <span data-ttu-id="4b9cd-112">Usa directivas de ancho de banda de CAC para complementar la configuración de QoS.</span><span class="sxs-lookup"><span data-stu-id="4b9cd-112">Use CAC bandwidth policies to complement QoS settings.</span></span>

  - <span data-ttu-id="4b9cd-113">Si deseas volver a redirigir llamadas bloqueadas a la RTC, comprueba la capacidad y las funciones de la RTC.</span><span class="sxs-lookup"><span data-stu-id="4b9cd-113">If you want to re-route blocked calls onto the PSTN, verify PSTN functionality and capacity.</span></span> <span data-ttu-id="4b9cd-114">Para obtener más información, consulte [planear el enrutamiento de voz saliente en Lync Server 2013](lync-server-2013-planning-outbound-voice-routing.md).</span><span class="sxs-lookup"><span data-stu-id="4b9cd-114">For details, see [Planning outbound voice routing in Lync Server 2013](lync-server-2013-planning-outbound-voice-routing.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4b9cd-115">La capacidad hace referencia a la cantidad de puertos que necesitas abrir para admitir un nuevo posible enrutamiento de la RTC.</span><span class="sxs-lookup"><span data-stu-id="4b9cd-115">Capacity refers to the number of ports you need to open to support potential PSTN re-routing.</span></span>

    
    <span data-ttu-id="4b9cd-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b9cd-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

