---
title: 'Lync Server 2013: configuración del enrutamiento basado en ubicación para conferencias'
description: 'Lync Server 2013: configuración de Location-Based enrutamiento para conferencias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399948"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="d87b9-103">Configuración del enrutamiento basado en ubicación para conferencias de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d87b9-103">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d87b9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d87b9-104">

<span> </span></span></span>

<span data-ttu-id="d87b9-105">_**Última modificación del tema:** 2013-09-11_</span><span class="sxs-lookup"><span data-stu-id="d87b9-105">_**Topic Last Modified:** 2013-09-11_</span></span>

<span data-ttu-id="d87b9-106">La aplicación de conferencia de Location-Based enrutamiento depende de la configuración del enrutamiento de Location-Based de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d87b9-106">The Location-Based Routing Conferencing application relies on the configuration of Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="d87b9-107">Las siguientes son las opciones de configuración principales:</span><span class="sxs-lookup"><span data-stu-id="d87b9-107">The main configurations are the following:</span></span>

  - <span data-ttu-id="d87b9-108">La ubicación de los participantes que se unen a una reunión se determina a partir de su sitio de red.</span><span class="sxs-lookup"><span data-stu-id="d87b9-108">The location of participants joining a meeting is determined based on their network site.</span></span> <span data-ttu-id="d87b9-109">Para exigir Location-Based enrutamiento, debe definirse un sitio de red y sus subredes de red asociadas en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d87b9-109">A network site and its associated network subnets must be defined in Lync Server in order to enforce Location-Based Routing.</span></span>

  - <span data-ttu-id="d87b9-110">Para exigir Location-Based el enrutamiento de reuniones, los participantes de Lync deben estar habilitados para Location-Based el enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="d87b9-110">To enforce Location-Based Routing of meetings, Lync participants must be enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="d87b9-111">Para exigir Location-Based enrutamiento de puntos de conexión RTC que se unen a las reuniones, el troncal SIP usado para conectar los puntos de conexión RTC debe configurarse para el enrutamiento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="d87b9-111">To enforce Location-Based Routing of PSTN endpoints joining meetings, the SIP trunk used to connect the PSTN endpoints must be configured for Location-Based Routing.</span></span>

<span data-ttu-id="d87b9-112">Para obtener más información sobre cómo implementar y configurar Lync Server 2013 Location-Based enrutamiento, consulte Configuración del [enrutamiento basado en la ubicación](lync-server-2013-configuring-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="d87b9-112">For additional information on deploying and configuring Lync Server 2013 Location-Based Routing, please refer Configuring [Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a><span data-ttu-id="d87b9-113">Habilitar la aplicación Location-Based de conferencia de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="d87b9-113">Enabling the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="d87b9-114">La aplicación Location-Based de conferencia de enrutamiento está deshabilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d87b9-114">The Location-Based Routing Conferencing application is disabled by default.</span></span> <span data-ttu-id="d87b9-115">Antes de habilitar esta aplicación, tienes que determinar la prioridad adecuada para asignar a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d87b9-115">Before enabling this application, you need to determine the right priority to assign for the application.</span></span> <span data-ttu-id="d87b9-116">Para determinar esta prioridad, ejecute el siguiente cmdlet en el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="d87b9-116">To determine this priority, run the following cmdlet in Lync Server Management Shell:</span></span>

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

<span data-ttu-id="d87b9-117">En este cmdlet, \<Pool FQDN\> se encuentra el grupo en el que se habilitará la aplicación de conferencia de enrutamiento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="d87b9-117">In this cmdlet, \<Pool FQDN\> is the pool in which the Location-Based Routing Conferencing application is to be enabled.</span></span>

<span data-ttu-id="d87b9-118">Este cmdlet devolverá la lista de las aplicaciones hospedadas por Lync Server y el valor de prioridad de cada una de ellas.</span><span class="sxs-lookup"><span data-stu-id="d87b9-118">This cmdlet will return the list of the applications hosted by Lync Server and the priority value for each of them.</span></span> <span data-ttu-id="d87b9-119">La aplicación de conferencia de Location-Based enrutamiento debe tener asignado un valor de prioridad mayor que el de la aplicación "UdcAgent" y menor que las aplicaciones "DefaultRouting", "ExumRouting" y "OutboundRouting".</span><span class="sxs-lookup"><span data-stu-id="d87b9-119">The Location-Based Routing Conferencing application needs to be assigned a priority value larger than the “UdcAgent” application and smaller than the “DefaultRouting”, “ExumRouting” and “OutboundRouting” applications.</span></span> <span data-ttu-id="d87b9-120">Le recomendamos que asigne el Location-Based aplicación de conferencia de enrutamiento un valor de prioridad que sea un punto superior al valor de prioridad de la aplicación "UdcAgent".</span><span class="sxs-lookup"><span data-stu-id="d87b9-120">We recommend that you assign the Location-Based Routing Conferencing application a priority value that is one point higher than the priority value of the “UdcAgent” application.</span></span>

<span data-ttu-id="d87b9-121">Por ejemplo, si la aplicación "UdcAgent" tiene un valor de prioridad de "2", la aplicación "DefaultRouting" tiene un valor de prioridad de "8", la aplicación "ExumRouting" tiene un valor de prioridad de "9" y la aplicación "OutboundRouting" tiene un valor de prioridad de "10", debe asignar la Location-Based aplicación de conferencia de enrutamiento como valor de prioridad</span><span class="sxs-lookup"><span data-stu-id="d87b9-121">For example, if the “UdcAgent” application has a priority value of “2”, the “DefaultRouting” application has a priority value of “8”, the “ExumRouting” application has a priority value of “9” and the “OutboundRouting” application has a priority value of “10” then you should assign the Location-Based Routing Conferencing application a priority value of “3”.</span></span> <span data-ttu-id="d87b9-122">Al hacerlo, la prioridad de las aplicaciones quedará ordenada así: otras aplicaciones (prioridades: de 0 a 1), “UdcAgent” (prioridad: 2), aplicación de conferencias con enrutamiento basado en ubicación (prioridad: 3), otras aplicaciones (prioridades: de 4 a 8), “DefaultRouting” (prioridad: 9), “ExumRouting” (prioridad: 10) y “OutboundRouting” (prioridad: 11).</span><span class="sxs-lookup"><span data-stu-id="d87b9-122">Doing so would place the priority of the applications in the following order: Other applications (Priorities: 0 to 1), “UdcAgent” (Priority: 2), Location-Based Routing Conferencing application (Priority: 3), other applications (Priorities: 4 to 8), “DefaultRouting” (Priority: 9), “ExumRouting” (Priority: 10) and “OutboundRouting” (Priority: 11).</span></span>

<span data-ttu-id="d87b9-123">Después de encontrar el valor de prioridad correcto para la aplicación de conferencia de enrutamiento de Location-Based, escriba el siguiente cmdlet para cada Front-End servidor Standard Edition o grupo de servidores que aloje usuarios habilitados para Location-Based enrutamiento:</span><span class="sxs-lookup"><span data-stu-id="d87b9-123">After you find the correct priority value for the Location-Based Routing Conferencing application, type the following cmdlet for each Front-End pool or Standard Edition Server that homes users enabled for Location-Based Routing:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="d87b9-124">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d87b9-124">For example:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="d87b9-125">Después de usar este cmdlet, reinicie todos los servidores front-end del grupo o los servidores Standard Edition donde se haya habilitado la aplicación de conferencia de enrutamiento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="d87b9-125">After using this cmdlet, restart all Front End servers in the pool or the Standard Edition Servers where the Location-Based Routing Conferencing application has been enabled.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d87b9-126">Location-Based la aplicación de enrutamiento a las conferencias o a las transferencias de asesoría no se aplicará hasta que se reinicien todos los servidores front-end de los servidores Standard Edition o Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d87b9-126">Location-Based Routing enforcements to conferences or consultative transfers won’t be enforced until all the Front End Servers in the applicable pools or the Standard Edition Servers are restarted.</span></span>



</div>

<span data-ttu-id="d87b9-127">Una vez que la aplicación de conferencia de enrutamiento de Location-Based se haya habilitado correctamente y se hayan reiniciado todos los servidores de Lync aplicables, se supervisarán todas las conferencias organizadas por usuarios de Lync habilitados para Location-Based enrutamiento para evitar el bypass de llamadas RTC.</span><span class="sxs-lookup"><span data-stu-id="d87b9-127">Once the Location-Based Routing Conferencing application has been successfully enabled and all applicable Lync servers have been restarted, all conferences organized by Lync users enabled for Location-Based Routing will be monitored to prevent PSTN toll bypass</span></span>

<span data-ttu-id="d87b9-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d87b9-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

