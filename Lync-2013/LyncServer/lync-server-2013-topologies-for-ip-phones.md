---
title: 'Lync Server 2013: topologías para teléfonos IP'
description: 'Lync Server 2013: topologías para teléfonos IP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topologies for IP phones
ms:assetid: 26ebffcf-43ff-4e70-847d-0fbc90e94e57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425740(v=OCS.15)
ms:contentKeyID: 48183662
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7a151a83a69e1f7e14dcbed8d8ab1038157fa839
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439669"
---
# <a name="topologies-for-ip-phones-in-lync-server-2013"></a><span data-ttu-id="46714-103">Topologías para teléfonos IP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46714-103">Topologies for IP phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="46714-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="46714-104">

<span> </span></span></span>

<span data-ttu-id="46714-105">_**Última modificación del tema:** 2012-06-21_</span><span class="sxs-lookup"><span data-stu-id="46714-105">_**Topic Last Modified:** 2012-06-21_</span></span>

<span data-ttu-id="46714-106">Esta sección proporciona una descripción general del proceso de conectividad y explica las diferencias entre el modo en que un teléfono IP se conecta en una red interna y externa.</span><span class="sxs-lookup"><span data-stu-id="46714-106">This section provides an overview of the connectivity process and explains the differences between how an IP phone connects in an internal and external network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="46714-107">Lync Server proporciona soporte técnico para los siguientes teléfonos IP: el Aastra 6721ip de área común, Aastra teléfono de escritorio 6725ip, teléfono IP HP 4110 (teléfono de área común), teléfono IP HP 4120 (teléfono de escritorio), teléfono de escritorio IP Polycom CX600, teléfono IP de escritorio Polycom CX700, teléfono Polycom CX500 IP y teléfono de conferencia Polycom CX3000 de IP.</span><span class="sxs-lookup"><span data-stu-id="46714-107">Lync Server provides support for the following IP phones: the Aastra 6721ip common area phone, Aastra 6725ip desk phone, HP 4110 IP Phone (common area phone), HP 4120 IP Phone (desk phone), Polycom CX600 IP desk phone, Polycom CX700 IP desk phone, Polycom CX500 IP common area phone, and Polycom CX3000 IP conference phone.</span></span> <span data-ttu-id="46714-108">De esos teléfonos, todos excepto el Polycom CX700 pueden ejecutar Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="46714-108">Of those phones, all but the Polycom CX700 can run Lync Phone Edition.</span></span>



</div>

<span data-ttu-id="46714-109">El siguiente diagrama describe todos los componentes implicados en la conectividad de dispositivos dentro del entorno corporativo.</span><span class="sxs-lookup"><span data-stu-id="46714-109">The following diagram describes all the components involved in device connectivity within the corporate environment.</span></span>

<span data-ttu-id="46714-110">**Topología interna**</span><span class="sxs-lookup"><span data-stu-id="46714-110">**Internal Topology**</span></span>

<span data-ttu-id="46714-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span><span class="sxs-lookup"><span data-stu-id="46714-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="46714-112">La figura anterior es una representación lógica, no una visión general física.</span><span class="sxs-lookup"><span data-stu-id="46714-112">The previous figure is a logical representation, not a physical overview.</span></span> <span data-ttu-id="46714-113">Por ejemplo, los servicios de dominio de Active Directory (AD DS) rara vez se encuentran en el mismo equipo que cualquier componente de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="46714-113">For example, Active Directory Domain Services (AD DS) is rarely located on the same machine as any Lync Server components.</span></span> <span data-ttu-id="46714-114">El almacén de usuario puede encontrarse en el servidor back-end o en los servidores de archivado y supervisión.</span><span class="sxs-lookup"><span data-stu-id="46714-114">The user store can be located on the Back End Server or on the Archiving and Monitoring Servers.</span></span> <span data-ttu-id="46714-115">El shell de administración de Lync Server, el servidor Web y los servicios de actualización forman parte de la función de servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="46714-115">The Lync Server Management Shell, web server, and update services are all part of the Front End Server role.</span></span>



</div>

<span data-ttu-id="46714-116">En el siguiente diagrama se ofrece información general sobre los componentes que se utilizan cuando el dispositivo se encuentra fuera de la red corporativa.</span><span class="sxs-lookup"><span data-stu-id="46714-116">The following diagram provides an overview of the components involved when the device is located outside the corporate network.</span></span>

<span data-ttu-id="46714-117">**Topología externa**</span><span class="sxs-lookup"><span data-stu-id="46714-117">**External Topology**</span></span>

<span data-ttu-id="46714-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span><span class="sxs-lookup"><span data-stu-id="46714-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="46714-119">El servicio Web de actualización de dispositivos proporciona un sitio web externo e interno, pero solo se muestra el externo.</span><span class="sxs-lookup"><span data-stu-id="46714-119">The Device Update Web service provides an external and internal website, but only the external one is shown here.</span></span><BR><span data-ttu-id="46714-120">La ubicación del registrador y la dirección URL del servicio Web de actualización de dispositivos para la organización se deben publicar en DNS si se va a habilitar el acceso externo.</span><span class="sxs-lookup"><span data-stu-id="46714-120">The location of the Registrar and the URL of the Device Update Web service for the organization must be published in DNS if external access is to be enabled.</span></span> <span data-ttu-id="46714-121">Además, el servidor perimetral debe implementarse y configurarse correctamente para permitir las comunicaciones externas desde el dispositivo al entorno corporativo y viceversa.</span><span class="sxs-lookup"><span data-stu-id="46714-121">Additionally, the Edge Server must be deployed and correctly configured to allow external communications from the device to the corporate environment and back.</span></span> <span data-ttu-id="46714-122">Esto se omite del diagrama anterior porque la implementación perimetral no es específica de la Conectividad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46714-122">This is omitted from the previous diagram because Edge deployment is not specific to device connectivity.</span></span>



<span data-ttu-id="46714-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="46714-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

