---
title: 'Lync Server 2013: Integración de la mensajería unificada de Exchange hospedada'
description: 'Lync Server 2013: integración de mensajería unificada de Exchange hospedada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange Unified Messaging integration
ms:assetid: f4de0165-da3b-499e-98fc-28ddd0db02d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413027(v=OCS.15)
ms:contentKeyID: 48185829
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 980c0bc47258e9fae94ff623559342ca36eea145
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427533"
---
# <a name="hosted-exchange-unified-messaging-integration-in-lync-server-2013"></a><span data-ttu-id="d059d-103">Integración de la mensajería unificada de Exchange hospedada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d059d-103">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d059d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d059d-104">

<span> </span></span></span>

<span data-ttu-id="d059d-105">_**Última modificación del tema:** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="d059d-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="d059d-106">Además de la compatibilidad que las versiones anteriores de Lync Server 2013 han proporcionado para la integración con implementaciones *locales* de mensajería unificada de Exchange (UM), Lync Server 2013 incorpora compatibilidad para la integración con MU de Exchange *hospedado* .</span><span class="sxs-lookup"><span data-stu-id="d059d-106">In addition to the support that previous Lync Server 2013 releases have provided for integration with *on-premises* deployments of Exchange Unified Messaging (UM), Lync Server 2013 introduces support for integration with *hosted* Exchange UM.</span></span> <span data-ttu-id="d059d-107">La mensajería instantánea de Exchange hospedado permite que Lync Server 2013 proporcione mensajería de voz a los usuarios si se transfieren algunos o todos a un proveedor de servicios de Exchange hospedado como Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d059d-107">Hosted Exchange UM enables Lync Server 2013 to provide voice messaging to your users if you transfer some or all of them to a hosted Exchange service provider such as Microsoft Exchange Online.</span></span>

<span data-ttu-id="d059d-108">Lync Server 2013 Enterprise Voice usa la infraestructura de mensajería unificada de Exchange para proporcionar contestación de llamadas, notificaciones de llamadas, acceso por voz (incluido el correo de voz) y servicios de operador automático.</span><span class="sxs-lookup"><span data-stu-id="d059d-108">Lync Server 2013 Enterprise Voice uses the Exchange UM infrastructure to provide call answering, call notification, voice access (including voice mail), and auto attendant services.</span></span> <span data-ttu-id="d059d-109">Para obtener más información, vea [características de la mensajería unificada integrada y Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="d059d-109">For details, see [Features of integrated Unified Messaging and Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d059d-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d059d-110">In This Section</span></span>

  - [<span data-ttu-id="d059d-111">Enrutamiento y arquitectura de la mensajería unificada de Exchange hospedada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d059d-111">Hosted Exchange UM architecture and routing in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-um-architecture-and-routing.md)

  - [<span data-ttu-id="d059d-112">Directivas de correo de voz hospedado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d059d-112">Hosted voice mail policies in Lync Server 2013</span></span>](lync-server-2013-hosted-voice-mail-policies.md)

  - [<span data-ttu-id="d059d-113">Administración de usuarios de Hosted Exchange en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d059d-113">Hosted Exchange user management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-user-management.md)

  - [<span data-ttu-id="d059d-114">Administración de objetos de contactos de Hosted Exchange en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d059d-114">Hosted Exchange Contact object management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-contact-object-management.md)

  - [<span data-ttu-id="d059d-115">Proceso de implementación para la integración de la mensajería unificada de Exchange hospedada con Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d059d-115">Deployment process for integrating hosted Exchange UM with Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-hosted-exchange-um.md)

<span data-ttu-id="d059d-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d059d-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

