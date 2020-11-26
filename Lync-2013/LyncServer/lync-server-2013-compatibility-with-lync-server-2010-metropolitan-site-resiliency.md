---
title: Compatibilidad de Lync Server 2013 con la resistencia de sitios de metropolitana de Lync Server 2010
description: Lync Server 2013 compatibilidad con la resistencia de sitios metropolitana de Lync Server 2010.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2010 metropolitan site resiliency
ms:assetid: 18673ff6-b664-4a57-a89b-cbda8b129e6a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204715(v=OCS.15)
ms:contentKeyID: 48183526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec72f261ac593b24bad13dcd400f495ba7ba0722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434609"
---
# <a name="lync-server-2010-metropolitan-site-resiliency"></a>Resistencia de sitios de metropolitana de Lync Server 2010

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2014-03-19_

La solución metropolitana de resiliencia de sitios admitida para Lync Server 2010 no es compatible con Lync Server 2013. Esta solución implicaba la expansión de un único Pool front end en dos centros de datos en el mismo área metropolitana.

La solución de resistencia de sitios metropolitana se ha diseñado para recuperarse de la pérdida de un centro de recursos completo. Cuando el grupo se extiende por dos centros de recursos, normalmente se coloca la mitad de los extremos en un centro de recursos y la otra mitad en el segundo centro de recursos. Si pierde un centro de información completo, habrá perdido la mitad de los servidores de aplicaciones para el usuario. Esto puede ocasionar problemas con el nuevo modelo de sistema distribuido para los grupos de servidores front-end en Lync Server 2013. Para obtener más información, vea [topologías y componentes para servidores front-end, mensajería instantánea y presencia en Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).

</div>

<span> </span>

</div>

</div>

</div>

