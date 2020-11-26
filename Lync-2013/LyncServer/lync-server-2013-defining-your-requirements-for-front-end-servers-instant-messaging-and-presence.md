---
title: 'Lync Server 2013: Definir los requisitos de los servidores front-end, la mensajería instantánea y la presencia'
description: 'Lync Server 2013: definir los requisitos para servidores front-end, mensajería instantánea y presencia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your requirements for Front End Servers, instant messaging, and presence
ms:assetid: c21198bc-520c-4d17-8b84-7ff1475b9b0a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412956(v=OCS.15)
ms:contentKeyID: 48185319
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 923132b32d5aef80191b19a7b85c3f17276e5946
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430815"
---
# <a name="defining-your-requirements-for-front-end-servers-instant-messaging-and-presence-in-lync-server-2013"></a><span data-ttu-id="075ea-103">Definir los requisitos de los servidores front-end, la mensajería instantánea y la presencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="075ea-103">Defining your requirements for Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="075ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="075ea-104">

<span> </span></span></span>

<span data-ttu-id="075ea-105">_**Última modificación del tema:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="075ea-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="075ea-106">La tarea principal de planear la mensajería instantánea y la presencia es asegurarse de que tiene los servidores frontales suficientes para sus usuarios.</span><span class="sxs-lookup"><span data-stu-id="075ea-106">The main task of planning for instant messaging (IM) and presence is ensuring that you have enough Front End Servers for your users.</span></span>

<div>

## <a name="enabling-communication-with-external-users"></a><span data-ttu-id="075ea-107">Habilitar la comunicación con usuarios externos</span><span class="sxs-lookup"><span data-stu-id="075ea-107">Enabling Communication with External Users</span></span>

<span data-ttu-id="075ea-108">Puede aumentar enormemente los beneficios de su inversión en Lync Server al permitir que los usuarios se comuniquen con usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="075ea-108">You can greatly increase the benefits of your investment in Lync Server by enabling your users to communicate with external users.</span></span> <span data-ttu-id="075ea-109">Entre los usuarios externos se pueden incluir:</span><span class="sxs-lookup"><span data-stu-id="075ea-109">External users can include:</span></span>

  - <span data-ttu-id="075ea-110">**Usuarios remotos**   Los usuarios de su organización, cuando trabajan fuera de los firewalls y usan sus equipos portátiles u otros dispositivos de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="075ea-110">**Remote users**   Your organization’s own users, when they are working outside your firewalls and are using their laptops or other Lync Server devices.</span></span>

  - <span data-ttu-id="075ea-111">**Usuarios federados**   Usuarios de empresas con las que trabaja y que también ejecutan Lync Server.</span><span class="sxs-lookup"><span data-stu-id="075ea-111">**Federated users**   Users from companies you work with who also run Lync Server.</span></span> <span data-ttu-id="075ea-112">Si desea habilitar a sus usuarios para que se pongan en contacto fácilmente con estos otros usuarios, cree relaciones federadas con estas compañías.</span><span class="sxs-lookup"><span data-stu-id="075ea-112">To enable your users to easily contact these users, you create federated relationships with these companies.</span></span>

  - <span data-ttu-id="075ea-113">**Usuarios públicos**   Usuarios de servicios de mensajería instantánea pública, como los servicios de mensajería instantánea de Windows Live de servicios de Internet, Yahoo \! y AOL, y los usuarios de proveedores y servidores que usen el protocolo de presencia y mensajería extensible (XMPP), como Google Talk.</span><span class="sxs-lookup"><span data-stu-id="075ea-113">**Public users**   Users of public IM services, such as IM services provided by the Windows Live network of Internet services, Yahoo\!, and AOL, and users of providers and servers that use Extensible Messaging and Presence Protocol (XMPP), such as Google Talk.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="075ea-114">Tenga en cuenta que es posible que se necesite una licencia independiente para la conectividad de mensajería instantánea pública con Windows Live, AOL y Yahoo!</span><span class="sxs-lookup"><span data-stu-id="075ea-114">Note that a separate license might be required for public IM connectivity with Windows Live, AOL, and Yahoo!</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="075ea-115">A partir del 1 de septiembre de 2012, la licencia de suscripción de usuario de conectividad de mensajería instantánea pública de Microsoft Lync ("PIC USL") ya no está disponible para la compra de contratos nuevos o de renovación.</span><span class="sxs-lookup"><span data-stu-id="075ea-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="075ea-116">Los clientes con licencias activas podrán seguir federando a Yahoo!</span><span class="sxs-lookup"><span data-stu-id="075ea-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="075ea-117">Messenger hasta que se cierre la fecha del servicio.</span><span class="sxs-lookup"><span data-stu-id="075ea-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="075ea-118">Una fecha de fin de vida de junio de 2014 para AOL y Yahoo!</span><span class="sxs-lookup"><span data-stu-id="075ea-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="075ea-119">ha sido anunciado.</span><span class="sxs-lookup"><span data-stu-id="075ea-119">has been announced.</span></span> <span data-ttu-id="075ea-120">Para obtener más información, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">compatibilidad de la conectividad de mensajería instantánea pública en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="075ea-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="075ea-121">El PIC USL es una licencia por usuario por mes de suscripción que es necesaria para que Lync Server o Office Communications Server se federe con Yahoo!</span><span class="sxs-lookup"><span data-stu-id="075ea-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="075ea-122">Mensajería.</span><span class="sxs-lookup"><span data-stu-id="075ea-122">Messenger.</span></span> <span data-ttu-id="075ea-123">La capacidad de Microsoft para proporcionar este servicio está supeditada al soporte de Yahoo!, el contrato subyacente para el que se está pospuesto.</span><span class="sxs-lookup"><span data-stu-id="075ea-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="075ea-124">Más que nunca, Lync es una herramienta eficaz para la conexión entre organizaciones y con personas de todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="075ea-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="075ea-125">La Federación con Windows Live Messenger no requiere licencias adicionales para usuarios y dispositivos más allá de la CAL de Lync Standard.</span><span class="sxs-lookup"><span data-stu-id="075ea-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="075ea-126">La Federación de Skype se agrega a esta lista, lo que permite a los usuarios de Lync llegar a cientos de millones de personas con la mensajería instantánea y la voz.</span><span class="sxs-lookup"><span data-stu-id="075ea-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

    
    </div>

<span data-ttu-id="075ea-127">Para habilitar cualquiera de estos escenarios o todos ellos, debe implementar un servidor perimetral que le ayude a habilitar las comunicaciones seguras entre la implementación de Lync Server y los usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="075ea-127">To enable any or all of these scenarios, you need to deploy an Edge Server to help enable secure communications between your Lync Server deployment and external users.</span></span> <span data-ttu-id="075ea-128">Los usuarios remotos de su organización y los usuarios de las organizaciones federadas podrán ver la presencia de los demás y comunicarse por medio de la mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="075ea-128">Your organization’s remote users and users at federated organizations will be able to see each other’s presence and communicate using IM.</span></span> <span data-ttu-id="075ea-129">Para obtener más información sobre cómo habilitar la comunicación con usuarios externos, vea [planificación de acceso a usuarios externos en Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="075ea-129">For details about enabling communication with external users, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="archiving-im-content"></a><span data-ttu-id="075ea-130">Archivar contenido de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="075ea-130">Archiving IM Content</span></span>

<span data-ttu-id="075ea-131">Lync Server proporciona características que puede usar si su organización debe seguir las normas de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="075ea-131">Lync Server provides features you can use if your organization must follow compliance regulations.</span></span> <span data-ttu-id="075ea-132">Puede usar el servidor de archivado para archivar el contenido de los mensajes de MI de todos los usuarios de la organización, o solamente de algunos específicos.</span><span class="sxs-lookup"><span data-stu-id="075ea-132">You can use Archiving to archive the content of IM messages for all users in your organization or for only certain users that you specify.</span></span> <span data-ttu-id="075ea-133">Para obtener más información, vea [planificación de archivado en Lync Server 2013](lync-server-2013-planning-for-archiving.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="075ea-133">For details, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>

<span data-ttu-id="075ea-134">Si también ha implementado Microsoft Exchange Server 2013, puede integrar el archivado de datos de Exchange con el archivado de datos de Lync Server y usar una única herramienta para buscar en los dos tipos de datos archivados.</span><span class="sxs-lookup"><span data-stu-id="075ea-134">If you also have Microsoft Exchange Server 2013 deployed, you can integrate the archiving of Exchange data with the archiving of Lync Server data, and use a single tool to search both types of archived data.</span></span> <span data-ttu-id="075ea-135">Para obtener más información, vea [configurar Microsoft Lync server 2013 para usar el archivado de Microsoft Exchange server 2013](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="075ea-135">For more information, see [Configuring Microsoft Lync Server 2013 to use Microsoft Exchange Server 2013 archiving](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md).</span></span>

<span data-ttu-id="075ea-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="075ea-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

