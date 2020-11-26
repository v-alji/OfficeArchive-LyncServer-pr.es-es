---
title: 'Lync Server 2013: Control de admisión de llamadas en un enlace troncal SIP'
description: 'Lync Server 2013: control de admisión de llamadas en un tronco de SIP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call admission control on a SIP trunk
ms:assetid: 7eada098-3d47-4be2-839f-8f87d582efe8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398632(v=OCS.15)
ms:contentKeyID: 48184623
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3667ef4608b221a1607b6bbe0d89d390cb1dd402
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435859"
---
# <a name="call-admission-control-on-a-sip-trunk-in-lync-server-2013"></a><span data-ttu-id="adae1-103">Control de admisión de llamadas en un enlace troncal SIP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="adae1-103">Call admission control on a SIP trunk in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="adae1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="adae1-104">

<span> </span></span></span>

<span data-ttu-id="adae1-105">_**Última modificación del tema:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="adae1-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="adae1-p101">Para implementar el servicio de control de admisión de llamadas (CAC) en un tronco SIP necesitas crear un sitio de red para representar al proveedor de servicios de telefonía por Internet (ITSP). Para aplicar valores de directivas de ancho de banda al tronco SIP necesitas crear una directiva entre el sitio de red de tu empresa y el sitio de red que crees para representar al ITSP.</span><span class="sxs-lookup"><span data-stu-id="adae1-p101">To deploy call admission control (CAC) on a SIP trunk, you create a network site to represent the Internet telephony service provider (ITSP). To apply bandwidth policy values on the SIP trunk, you create an inter-site policy between the network site in your enterprise and the network site that you create to represent the ITSP.</span></span>

<span data-ttu-id="adae1-108">La siguiente figura muestra un ejemplo de implementación de CAC en un tronco SIP.</span><span class="sxs-lookup"><span data-stu-id="adae1-108">The following figure shows an example CAC deployment on a SIP trunk.</span></span>

<span data-ttu-id="adae1-109">**Configuración de CAC en un tronco SIP**</span><span class="sxs-lookup"><span data-stu-id="adae1-109">**CAC configuration on a SIP trunk**</span></span>

<span data-ttu-id="adae1-110">![Diagrama de enlace troncal SIP del control de admisión de llamadas](images/Gg398632.276c0d8f-1dd5-4883-8499-c202399ddbe9(OCS.15).jpg "Diagrama de enlace troncal SIP del control de admisión de llamadas")</span><span class="sxs-lookup"><span data-stu-id="adae1-110">![Call Admission Control SIP Trunking diagram](images/Gg398632.276c0d8f-1dd5-4883-8499-c202399ddbe9(OCS.15).jpg "Call Admission Control SIP Trunking diagram")</span></span>

<span data-ttu-id="adae1-111">Para configurar el CAC en un tronco SIP necesitarás realizar las siguientes tareas durante la implementación de CAC:</span><span class="sxs-lookup"><span data-stu-id="adae1-111">To configure CAC on a SIP trunk, you will have to perform the following tasks during CAC deployment:</span></span>

1.  <span data-ttu-id="adae1-112">Crea un sitio de red para representar al ITSP.</span><span class="sxs-lookup"><span data-stu-id="adae1-112">Create a network site to represent the ITSP.</span></span> <span data-ttu-id="adae1-113">Asocia el sitio de red a una región de red adecuada y asigna un ancho de banda de cero para el audio y el vídeo para este sitio de red.</span><span class="sxs-lookup"><span data-stu-id="adae1-113">Associate the network site to an appropriate network region, and allocate bandwidth of zero for audio and video for this network site.</span></span> <span data-ttu-id="adae1-114">Para obtener más información, vea [configurar sitios de red para CAC en Lync Server 2013](lync-server-2013-configure-network-sites-for-cac.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="adae1-114">For details, see [Configure network sites for CAC in Lync Server 2013](lync-server-2013-configure-network-sites-for-cac.md) in the Deployment documentation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="adae1-115">Para el ITSP, no funciona esta configuración de sitio de red.</span><span class="sxs-lookup"><span data-stu-id="adae1-115">For the ITSP, this network site configuration is not functional.</span></span> <span data-ttu-id="adae1-116">Los valores de la directiva de ancho de banda se aplican, en realidad, en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="adae1-116">Bandwidth policy values are actually applied in step 2.</span></span>

    
    </div>

2.  <span data-ttu-id="adae1-117">Crea un vínculo entre sitios para el tronco SIP, usando los valores de los parámetros correspondientes al sitio que creaste en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="adae1-117">Create an inter-site link for the SIP trunk using the relevant parameter values for the site you created in step 1.</span></span> <span data-ttu-id="adae1-118">Por ejemplo, usa el nombre del sitio de red de tu empresa como el valor del parámetro NetworkSiteID1 y el sitio de red de ITSP como el valor del parámetro NetworkSiteID2.</span><span class="sxs-lookup"><span data-stu-id="adae1-118">For example, use the name of the network site in your enterprise as the value of the NetworkSiteID1 parameter, and the ITSP network site as the value of the NetworkSiteID2 parameter.</span></span> <span data-ttu-id="adae1-119">Para obtener más información, vea [crear directivas de intersitio de red en Lync Server 2013](lync-server-2013-create-network-intersite-policies.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="adae1-119">For details, see [Create network intersite policies in Lync Server 2013](lync-server-2013-create-network-intersite-policies.md) in the Deployment documentation.</span></span> <span data-ttu-id="adae1-120">Consulte también la documentación del shell de administración de Lync Server para el cmdlet New-CsNetworkInterSitePolicy.</span><span class="sxs-lookup"><span data-stu-id="adae1-120">Also see the Lync Server Management Shell documentation for the New-CsNetworkInterSitePolicy cmdlet.</span></span>

3.  <span data-ttu-id="adae1-121">Consulta a tu ITSP la dirección IP del punto de terminación de medios del controlador de borde de sesión (SBC).</span><span class="sxs-lookup"><span data-stu-id="adae1-121">Get the IP address of the Session Border Controller’s (SCB) Media Termination Point from your ITSP.</span></span> <span data-ttu-id="adae1-122">Agrega esa dirección IP con una máscara de subred de 32 al sitio de red que representa al ITSP.</span><span class="sxs-lookup"><span data-stu-id="adae1-122">Add that IP address with a subnet mask of 32 to the network site that represents the ITSP.</span></span> <span data-ttu-id="adae1-123">Para obtener más información, consulte [asociar una subred con un sitio de red en Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span><span class="sxs-lookup"><span data-stu-id="adae1-123">For details, see [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span></span>

<span data-ttu-id="adae1-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="adae1-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

