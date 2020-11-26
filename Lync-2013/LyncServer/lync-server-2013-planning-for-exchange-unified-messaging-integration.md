---
title: 'Lync Server 2013: Planear la integración de la mensajería unificada de Exchange'
description: 'Lync Server 2013: planeamiento de la integración de mensajería unificada de Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Exchange Unified Messaging integration
ms:assetid: e7c63a71-2d99-4aa9-b649-36c1a431bdf1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399031(v=OCS.15)
ms:contentKeyID: 48185880
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31296444d21a86a7837da3e29fc2152f3ca96ccc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443002"
---
# <a name="planning-for-exchange-unified-messaging-integration-in-lync-server-2013"></a><span data-ttu-id="5d20d-103">Planear la integración de la mensajería unificada de Exchange en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d20d-103">Planning for Exchange Unified Messaging integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d20d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d20d-104">

<span> </span></span></span>

<span data-ttu-id="5d20d-105">_**Última modificación del tema:** 2012-10-13_</span><span class="sxs-lookup"><span data-stu-id="5d20d-105">_**Topic Last Modified:** 2012-10-13_</span></span>

<span data-ttu-id="5d20d-106">Lync Server 2013 admite la integración con mensajería unificada de Exchange (UM) para combinar la mensajería de voz y la mensajería de correo electrónico en una sola infraestructura de mensajería.</span><span class="sxs-lookup"><span data-stu-id="5d20d-106">Lync Server 2013 supports integration with Exchange Unified Messaging (UM) for combining voice messaging and email messaging into a single messaging infrastructure.</span></span> <span data-ttu-id="5d20d-107">En Microsoft Exchange Server 2007 Service Pack 1 (SP1) y Microsoft Exchange Server 2010, la mensajería unificada de Exchange (UM) es una de las diversas funciones de Exchange Server que puede instalar y configurar.</span><span class="sxs-lookup"><span data-stu-id="5d20d-107">In Microsoft Exchange Server 2007 Service Pack 1 (SP1) and Microsoft Exchange Server 2010, Exchange Unified Messaging (UM) is one of several Exchange server roles that you can install and configure.</span></span>

<span data-ttu-id="5d20d-108">En Microsoft Exchange Server 2013, la mensajería unificada de Exchange se ejecuta como un servicio en un servidor de buzones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d20d-108">In Microsoft Exchange Server 2013, Exchange UM runs as a service on an Exchange Mailbox server.</span></span> <span data-ttu-id="5d20d-109">Para implementaciones de Lync Server 2013 Enterprise Voice, la mensajería unificada combina la mensajería de voz y la mensajería de correo electrónico en un único almacén que está disponible desde un teléfono (Outlook Voice Access) o un equipo.</span><span class="sxs-lookup"><span data-stu-id="5d20d-109">For Lync Server 2013 Enterprise Voice deployments, Unified Messaging combines voice messaging and email messaging into a single store that is available from a telephone (Outlook Voice Access) or a computer.</span></span> <span data-ttu-id="5d20d-110">Mensajería unificada y Lync Server 2013 trabajan de manera conjunta para proporcionar respuesta de llamadas, Outlook Voice Access y los servicios de operador automático a los usuarios de telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="5d20d-110">Unified Messaging and Lync Server 2013 work together to provide call answering, Outlook Voice Access, and auto-attendant services to users of Enterprise Voice.</span></span>

<span data-ttu-id="5d20d-111">Para obtener más información sobre los cambios de arquitectura de Microsoft Exchange Server 2013, consulte "Voice Architecture Changes" en la documentación de Microsoft Exchange Server 2013 en [https://go.microsoft.com/fwlink/p/?LinkId=266730](https://go.microsoft.com/fwlink/p/?linkid=266730) .</span><span class="sxs-lookup"><span data-stu-id="5d20d-111">For more information about the architecture changes in Microsoft Exchange Server 2013, see “Voice Architecture Changes” in the Microsoft Exchange Server 2013 documentation at [https://go.microsoft.com/fwlink/p/?LinkId=266730](https://go.microsoft.com/fwlink/p/?linkid=266730).</span></span>

<span data-ttu-id="5d20d-112">Para que estas características se admitan en una implementación de mensajería unificada de Exchange local, debe estar ejecutando una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="5d20d-112">For these features to be supported in an on-premises Exchange UM deployment, you must be running one of the following:</span></span>

  - <span data-ttu-id="5d20d-113">Microsoft Exchange Server 2007 Service Pack 1 (SP1) o el Service Pack más reciente</span><span class="sxs-lookup"><span data-stu-id="5d20d-113">Microsoft Exchange Server 2007 Service Pack 1 (SP1) or latest service pack</span></span>

  - <span data-ttu-id="5d20d-114">Microsoft Exchange Server 2010 o Service Pack más reciente</span><span class="sxs-lookup"><span data-stu-id="5d20d-114">Microsoft Exchange Server 2010 or latest service pack</span></span>

  - <span data-ttu-id="5d20d-115">Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d20d-115">Microsoft Exchange Server 2013</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5d20d-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5d20d-116">In This Section</span></span>

  - [<span data-ttu-id="5d20d-117">Características de la mensajería unificada integrada y Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d20d-117">Features of integrated Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-features-of-integrated-unified-messaging.md)

  - [<span data-ttu-id="5d20d-118">Componentes y topologías para mensajería unificada local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d20d-118">Components and topologies for on-premises Unified Messaging in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-on-premises-unified-messaging.md)

  - [<span data-ttu-id="5d20d-119">Instrucciones para integrar mensajería unificada local y Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d20d-119">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md)

  - [<span data-ttu-id="5d20d-120">Proceso de implementación de la integración de la mensajería unificada local y Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d20d-120">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="5d20d-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d20d-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

