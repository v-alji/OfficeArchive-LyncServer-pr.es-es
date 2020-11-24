---
title: 'Lync Server 2013: Compatibilidad de mensajería instantánea pública'
description: 'Lync Server 2013: compatibilidad con mensajería instantánea pública.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Public instant messaging support
ms:assetid: 1f45163b-52c6-4a78-b9c8-dfe3abe4e5eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204732(v=OCS.15)
ms:contentKeyID: 48183582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e071e8b79be82d865a85a9488e48dd0a4264c7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399078"
---
# <a name="public-instant-messaging-support-in-lync-server-2013"></a><span data-ttu-id="d7256-103">Compatibilidad de mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7256-103">Public instant messaging support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d7256-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d7256-104">

<span> </span></span></span>

<span data-ttu-id="d7256-105">_**Última modificación del tema:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="d7256-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="d7256-106">Lync Server 2013 admite el uso de proveedores de conectividad de mensajería instantánea pública con licencia (mi), así como el uso de protocolo de presencia y mensajería extensible (XMPP) con el fin de implementar un tipo especial de Federación que permita a un Lync Server acceder a los socios del dominio XMPP configurado mediante el cliente de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="d7256-106">Lync Server 2013 supports the use of licensed public instant messaging (IM) connectivity providers, as well as the use of eXtensible Messaging and Presence Protocol (XMPP) to implement a special type of federation that enables a Lync Server to access configured XMPP domain partners by using the Lync 2013 client.</span></span>

<div>

## <a name="public-im-connectivity-provider-support"></a><span data-ttu-id="d7256-107">Compatibilidad con el proveedor de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="d7256-107">Public IM Connectivity Provider Support</span></span>

<span data-ttu-id="d7256-108">Los partners de conectividad de mensajería instantánea actualmente compatibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d7256-108">The currently supported public instant messaging connectivity partners are:</span></span>

  - <span data-ttu-id="d7256-109">America Online</span><span class="sxs-lookup"><span data-stu-id="d7256-109">America Online</span></span>

  - <span data-ttu-id="d7256-110">Windows Live</span><span class="sxs-lookup"><span data-stu-id="d7256-110">Windows Live</span></span>

  - <span data-ttu-id="d7256-111">Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="d7256-111">Yahoo\!</span></span>

<span data-ttu-id="d7256-112">Para las comunicaciones con usuarios de Windows Live, Lync Server 2013 admite la mensajería instantánea de punto a punto y las llamadas de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7256-112">For communications with Windows Live users, Lync Server 2013 supports peer-to-peer IM and audio and video calls.</span></span> <span data-ttu-id="d7256-113">Para las comunicaciones con AOL y Yahoo \! , Lync Server 2013 admite la mensajería instantánea de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="d7256-113">For communications with AOL and Yahoo\!, Lync Server 2013 supports peer-to-peer IM.</span></span> <span data-ttu-id="d7256-114">Es posible que se necesite una licencia por separado.</span><span class="sxs-lookup"><span data-stu-id="d7256-114">A separate license may be required.</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="d7256-115">A partir del 1 de septiembre de 2012, la licencia de suscripción de usuario de conectividad de mensajería instantánea pública de Microsoft Lync ("PIC USL") ya no está disponible para la compra de contratos nuevos o de renovación.</span><span class="sxs-lookup"><span data-stu-id="d7256-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="d7256-116">Los clientes con licencias activas podrán seguir federando a Yahoo!</span><span class="sxs-lookup"><span data-stu-id="d7256-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="d7256-117">Messenger hasta que se cierre la fecha del servicio.</span><span class="sxs-lookup"><span data-stu-id="d7256-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="d7256-118">Una fecha de fin de vida de junio de 2014 para AOL y Yahoo!</span><span class="sxs-lookup"><span data-stu-id="d7256-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="d7256-119">ha sido anunciado.</span><span class="sxs-lookup"><span data-stu-id="d7256-119">has been announced.</span></span> <span data-ttu-id="d7256-120">Para obtener más información, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">compatibilidad de la conectividad de mensajería instantánea pública en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d7256-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="d7256-121">El PIC USL es una licencia por usuario por mes de suscripción que es necesaria para que Lync Server o Office Communications Server se federe con Yahoo!</span><span class="sxs-lookup"><span data-stu-id="d7256-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="d7256-122">Mensajería.</span><span class="sxs-lookup"><span data-stu-id="d7256-122">Messenger.</span></span> <span data-ttu-id="d7256-123">La capacidad de Microsoft para proporcionar este servicio está supeditada al soporte de Yahoo!, el contrato subyacente para el que se está pospuesto.</span><span class="sxs-lookup"><span data-stu-id="d7256-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="d7256-124">Más que nunca, Lync es una herramienta eficaz para la conexión entre organizaciones y con personas de todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="d7256-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="d7256-125">La Federación con Windows Live Messenger no requiere licencias adicionales para usuarios y dispositivos más allá de la CAL de Lync Standard.</span><span class="sxs-lookup"><span data-stu-id="d7256-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="d7256-126">La Federación de Skype se agrega a esta lista, lo que permite a los usuarios de Lync llegar a cientos de millones de personas con la mensajería instantánea y la voz.</span><span class="sxs-lookup"><span data-stu-id="d7256-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

</div>

<div>

## <a name="xmpp-federation-support"></a><span data-ttu-id="d7256-127">Compatibilidad con la Federación de XMPP</span><span class="sxs-lookup"><span data-stu-id="d7256-127">XMPP Federation Support</span></span>

<span data-ttu-id="d7256-128">La Federación XMPP admite la comunicación entre usuarios de Lync con usuarios del dominio XMPP configurados que usan un proveedor público, como GTalk.</span><span class="sxs-lookup"><span data-stu-id="d7256-128">XMPP federation supports Lync users communication with configured XMPP domain users who use a public provider, such as GTalk.</span></span> <span data-ttu-id="d7256-129">Las comunicaciones con estos usuarios pueden incluir lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d7256-129">Communications with these users can include the following:</span></span>

  - <span data-ttu-id="d7256-130">Mensajería instantánea y presencia de punto a punto</span><span class="sxs-lookup"><span data-stu-id="d7256-130">Peer-to-peer IM and presence</span></span>

  - <span data-ttu-id="d7256-131">Creación de los contactos de XMPP federados en el cliente de Lync</span><span class="sxs-lookup"><span data-stu-id="d7256-131">Creation of XMPP federated contacts in the Lync client</span></span>

<span data-ttu-id="d7256-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d7256-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

