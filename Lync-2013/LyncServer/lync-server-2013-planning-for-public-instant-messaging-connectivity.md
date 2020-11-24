---
title: 'Lync Server 2013: planeamiento de la conectividad de mensajería instantánea pública'
description: 'Lync Server 2013: planeamiento de la conectividad de mensajería instantánea pública.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for public instant messaging connectivity
ms:assetid: e75e8884-05c7-414a-8014-bc9aa8126fb7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205349(v=OCS.15)
ms:contentKeyID: 48185698
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9a020a291a39d78aea9271926c99b508a8cd9827
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400217"
---
# <a name="planning-for-public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="3fe7d-103">Planeamiento de la conectividad de mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fe7d-103">Planning for public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3fe7d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3fe7d-104">

<span> </span></span></span>

<span data-ttu-id="3fe7d-105">_**Última modificación del tema:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="3fe7d-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="3fe7d-106">La conectividad de mensajería instantánea pública es una clase de Federación y está configurada para permitir a los usuarios internos y externos de Lync Server 2013 agregar contactos de cualquiera de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="3fe7d-106">Public Instant Messaging Connectivity is a class of federation, and is configured to allow your internal and external Lync Server 2013 users to add contacts from any of the following:</span></span>

  - <span data-ttu-id="3fe7d-107">Contactos de Messenger</span><span class="sxs-lookup"><span data-stu-id="3fe7d-107">Messenger contacts</span></span>

  - <span data-ttu-id="3fe7d-108">Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="3fe7d-108">Yahoo\!</span></span> <span data-ttu-id="3fe7d-109">contactos</span><span class="sxs-lookup"><span data-stu-id="3fe7d-109">contacts</span></span>

  - <span data-ttu-id="3fe7d-110">Contactos de America Online (AOL)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-110">America Online (AOL) contacts</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="3fe7d-111">A partir del 1 de septiembre de 2012, la licencia de suscripción de usuario de la conectividad de mensajería instantánea pública de Microsoft Lync (PIC USL) ya no está disponible para la compra de contratos nuevos o de renovación.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-111">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="3fe7d-112">Los clientes con licencias activas podrán seguir federando a Yahoo!</span><span class="sxs-lookup"><span data-stu-id="3fe7d-112">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="3fe7d-113">Messenger hasta la fecha de cierre del servicio.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-113">Messenger until the service shutdown date.</span></span> <span data-ttu-id="3fe7d-114">Una fecha de fin de vida de junio de 2014 para AOL y Yahoo!</span><span class="sxs-lookup"><span data-stu-id="3fe7d-114">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="3fe7d-115">ha sido anunciado.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-115">has been announced.</span></span> <span data-ttu-id="3fe7d-116">Para obtener más información, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">compatibilidad de la conectividad de mensajería instantánea pública en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-116">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="3fe7d-117">El PIC USL es una licencia por usuario y por mes de suscripción que es necesaria para que Lync Server o Office Communications Server se federe con Yahoo!</span><span class="sxs-lookup"><span data-stu-id="3fe7d-117">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="3fe7d-118">Mensajería.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-118">Messenger.</span></span> <span data-ttu-id="3fe7d-119">La capacidad de Microsoft para proporcionar este servicio está supeditada al soporte de Yahoo!, el contrato subyacente para el cual no se renovará.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-119">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="3fe7d-120">Más que nunca, Lync es una herramienta eficaz para la conexión entre organizaciones y con personas de todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-120">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="3fe7d-121">La Federación con Windows Live Messenger no requiere licencias adicionales para usuarios y dispositivos más allá de la CAL de Lync Standard.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-121">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="3fe7d-122">La Federación de Skype se agrega a esta lista, lo que permite a los usuarios de Lync llegar a cientos de millones de personas a través de la mensajería instantánea y la voz.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-122">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="3fe7d-123">Esta clase de Federación requiere las siguientes consideraciones de planeación:</span><span class="sxs-lookup"><span data-stu-id="3fe7d-123">This class of federation requires the following planning considerations:</span></span>

  - <span data-ttu-id="3fe7d-124">Los usuarios de Windows Live Messenger pueden tener una comunicación visual o de audio de punto a punto con los usuarios de Lync Server 2013, además de la mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-124">Windows Live Messenger users can have peer-to-peer audio/visual communication with Lync Server 2013 users, in addition to instant messaging.</span></span> <span data-ttu-id="3fe7d-125">Los servidores perimetrales deben cumplir con requisitos de puerto y protocolo específicos.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-125">Your Edge Servers must meet specific port and protocol requirements.</span></span> <span data-ttu-id="3fe7d-126">Para obtener más información, consulte [determinar el firewall externo a/V y los requisitos de puerto para Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3fe7d-126">For details, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

  - <span data-ttu-id="3fe7d-127">La mensajería instantánea de Yahoo no tiene requisitos únicos, excepto los que normalmente se usan en la planificación y la implementación del servidor perimetral típico que proporciona la Federación.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-127">Yahoo instant messaging has no unique requirements, other than those typically used in the planning and deployment of the typical Edge Server that is providing federation.</span></span>

  - <span data-ttu-id="3fe7d-128">America Online requiere que el certificado del servidor perimetral asignado al servicio perimetral de acceso tenga un uso mejorado de clave (EKU) de cliente.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-128">America Online requires that your Edge Server certificate assigned to the Access Edge service has a client enhanced key usage (EKU).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3fe7d-129">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3fe7d-129">In This Section</span></span>

  - [<span data-ttu-id="3fe7d-130">Resumen del certificado: conectividad de mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fe7d-130">Certificate summary - Public instant messaging connectivity in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-public-instant-messaging-connectivity.md)

  - [<span data-ttu-id="3fe7d-131">Resumen de puertos: conectividad de mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fe7d-131">Port summary - Public instant messaging connectivity in Lync Server 2013</span></span>](lync-server-2013-port-summary-public-instant-messaging-connectivity.md)

  - <span data-ttu-id="3fe7d-132">[Resumen de DNS: conectividad de mensajería instantánea pública en Lync Server 2013](https://technet.microsoft.com/library/jj618375\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3fe7d-132">[DNS summary - Public instant messaging connectivity in Lync Server 2013](https://technet.microsoft.com/library/jj618375\(v=ocs.15\))</span></span>

<span data-ttu-id="3fe7d-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3fe7d-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

