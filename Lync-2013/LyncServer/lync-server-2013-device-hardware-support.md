---
title: 'Lync Server 2013: Compatibilidad con hardware de dispositivos'
description: Compatibilidad con hardware del dispositivo de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device hardware support
ms:assetid: ba07ca91-32b4-49cf-801c-47a2d1d96e18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412908(v=OCS.15)
ms:contentKeyID: 48185222
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cd03936d35fbc3a639a3ba4596a4357e8e379719
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429457"
---
# <a name="device-hardware-support-in-lync-server-2013"></a><span data-ttu-id="c212a-103">Compatibilidad con hardware de dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c212a-103">Device hardware support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c212a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c212a-104">

<span> </span></span></span>

<span data-ttu-id="c212a-105">_**Última modificación del tema:** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="c212a-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="c212a-106">Las configuraciones de hardware específicas deben estar vigentes antes de implementar los teléfonos IP y los dispositivos analógicos.</span><span class="sxs-lookup"><span data-stu-id="c212a-106">Specific hardware configurations must be in place before you deploy IP phones and analog devices.</span></span>

<span data-ttu-id="c212a-107">Los teléfonos IP que ejecutan Lync Phone Edition admiten el descubrimiento de nivel de vínculo Protocol-Media detección de extremos (LLDP-MED) y Power over Ethernet (PoE).</span><span class="sxs-lookup"><span data-stu-id="c212a-107">IP phones running Lync Phone Edition support Link Layer Discovery Protocol-Media Endpoint Discovery (LLDP-MED) and Power over Ethernet (PoE).</span></span> <span data-ttu-id="c212a-108">Para aprovechar LLDP-MED, el switch debe ser compatible con IEEE 802.1 AB y ANSI/and-1057.</span><span class="sxs-lookup"><span data-stu-id="c212a-108">To take advantage of LLDP-MED, the switch must support IEEE802.1AB and ANSI/TIA-1057.</span></span> <span data-ttu-id="c212a-109">Para aprovechar las ventajas de PoE, el conmutador debe ser compatible con PoE 802.3 AF o 802.3 en.</span><span class="sxs-lookup"><span data-stu-id="c212a-109">To take advantage of PoE, the switch must support PoE802.3AF or 802.3at.</span></span>

<span data-ttu-id="c212a-110">Para habilitar LLDP-MED, el administrador debe habilitar LLDP mediante la ventana cambiar consola y configurar la Directiva de red LLDP-MED con la identificación de voz VLAN correcta.</span><span class="sxs-lookup"><span data-stu-id="c212a-110">To enable LLDP-MED, the administrator must enable LLDP by using the switch console window and set the LLDP-MED network policy with the correct voice VLAN ID.</span></span>

<span data-ttu-id="c212a-111">Además, si su implementación incluye dispositivos analógicos, debe configurar la puerta de enlace analógica para usar Lync Server, y la puerta de enlace debe ser una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="c212a-111">In addition, if your deployment includes analog devices, you must configure the analog gateway to use Lync Server, and the gateway must be one of the following:</span></span>

  - <span data-ttu-id="c212a-112">Un adaptador de teléfono analógico (ATA)</span><span class="sxs-lookup"><span data-stu-id="c212a-112">An analog telephone adapter (ATA)</span></span>

  - <span data-ttu-id="c212a-113">Una puerta de enlace analógica RTC</span><span class="sxs-lookup"><span data-stu-id="c212a-113">A PSTN analog gateway</span></span>

  - <span data-ttu-id="c212a-114">Un dispositivo de sucursal con la que se incluye una puerta de enlace analógica RTC</span><span class="sxs-lookup"><span data-stu-id="c212a-114">A Survivable Branch Appliance that includes a PSTN analog gateway</span></span>

  - <span data-ttu-id="c212a-115">Un dispositivo de sucursal con la que se incluye una puerta de enlace RTC que se comunica con un ATA</span><span class="sxs-lookup"><span data-stu-id="c212a-115">A Survivable Branch Appliance that includes a PSTN gateway that communicates with an ATA</span></span>

<span data-ttu-id="c212a-116">Para obtener información sobre cómo configurar una puerta de enlace analógica, consulte "planear la implementación de dispositivos analógicos" en [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) la biblioteca de TechNet de 2010 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c212a-116">To learn how to configure an analog gateway, see "Planning to Deploy Analog Devices" at [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) in the Lync Server 2010 TechNet Library.</span></span> <span data-ttu-id="c212a-117">(Los dispositivos analógicos funcionan de la misma manera en Lync Server 2013 que en Lync Server 2010).</span><span class="sxs-lookup"><span data-stu-id="c212a-117">(Analog devices work the same way in Lync Server 2013 as they do in Lync Server 2010.)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c212a-118">Puede configurar el modificador para una 9-1-1 mejorada (E9-1-1), si el modificador lo admite.</span><span class="sxs-lookup"><span data-stu-id="c212a-118">You can configure the switch for Enhanced 9-1-1 (E9-1-1), if the switch supports this.</span></span>



<span data-ttu-id="c212a-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c212a-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

