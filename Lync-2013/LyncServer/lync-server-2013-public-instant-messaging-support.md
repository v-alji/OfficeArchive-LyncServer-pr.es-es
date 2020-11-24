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
# <a name="public-instant-messaging-support-in-lync-server-2013"></a>Compatibilidad de mensajería instantánea pública en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-10-07_

Lync Server 2013 admite el uso de proveedores de conectividad de mensajería instantánea pública con licencia (mi), así como el uso de protocolo de presencia y mensajería extensible (XMPP) con el fin de implementar un tipo especial de Federación que permita a un Lync Server acceder a los socios del dominio XMPP configurado mediante el cliente de Lync 2013.

<div>

## <a name="public-im-connectivity-provider-support"></a>Compatibilidad con el proveedor de conectividad de mensajería instantánea pública

Los partners de conectividad de mensajería instantánea actualmente compatibles son los siguientes:

  - America Online

  - Windows Live

  - Yahoo\!

Para las comunicaciones con usuarios de Windows Live, Lync Server 2013 admite la mensajería instantánea de punto a punto y las llamadas de audio y vídeo. Para las comunicaciones con AOL y Yahoo \! , Lync Server 2013 admite la mensajería instantánea de punto a punto. Es posible que se necesite una licencia por separado.

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P>A partir del 1 de septiembre de 2012, la licencia de suscripción de usuario de conectividad de mensajería instantánea pública de Microsoft Lync ("PIC USL") ya no está disponible para la compra de contratos nuevos o de renovación. Los clientes con licencias activas podrán seguir federando a Yahoo! Messenger hasta que se cierre la fecha del servicio. Una fecha de fin de vida de junio de 2014 para AOL y Yahoo! ha sido anunciado. Para obtener más información, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">compatibilidad de la conectividad de mensajería instantánea pública en Lync Server 2013</A>.</P>
> <LI>
> <P>El PIC USL es una licencia por usuario por mes de suscripción que es necesaria para que Lync Server o Office Communications Server se federe con Yahoo! Mensajería. La capacidad de Microsoft para proporcionar este servicio está supeditada al soporte de Yahoo!, el contrato subyacente para el que se está pospuesto.</P>
> <LI>
> <P>Más que nunca, Lync es una herramienta eficaz para la conexión entre organizaciones y con personas de todo el mundo. La Federación con Windows Live Messenger no requiere licencias adicionales para usuarios y dispositivos más allá de la CAL de Lync Standard. La Federación de Skype se agrega a esta lista, lo que permite a los usuarios de Lync llegar a cientos de millones de personas con la mensajería instantánea y la voz.</P></LI></UL>



</div>

</div>

<div>

## <a name="xmpp-federation-support"></a>Compatibilidad con la Federación de XMPP

La Federación XMPP admite la comunicación entre usuarios de Lync con usuarios del dominio XMPP configurados que usan un proveedor público, como GTalk. Las comunicaciones con estos usuarios pueden incluir lo siguiente:

  - Mensajería instantánea y presencia de punto a punto

  - Creación de los contactos de XMPP federados en el cliente de Lync

</div>

</div>

<span> </span>

</div>

</div>

</div>

