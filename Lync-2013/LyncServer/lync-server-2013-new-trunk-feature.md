---
title: 'Lync Server 2013: Nueva característica de tronco'
description: 'Lync Server 2013: nueva característica de troncal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New trunk feature
ms:assetid: 9b398bc8-2760-4218-b1a4-89b9694b1171
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688152(v=OCS.15)
ms:contentKeyID: 49733755
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d8f923ceada899608cc350bd1343345c12d0996b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445340"
---
# <a name="new-trunk-feature-in-lync-server-2013"></a>Nueva característica de tronco en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-09-21_

En Microsoft Lync Server 2013, se pueden definir varios troncos entre un servidor de mediación y una puerta de enlace. Microsoft Lync Server 2010 solo se permite para un único tronco entre un servidor de mediación y una puerta de enlace RTC. Esta característica proporciona la flexibilidad de definir troncos adicionales. Un tronco es una asociación lógica entre un FQDN de servidor de mediación y un puerto de escucha y una puerta de enlace de RTC y un puerto de escucha. Esta nueva capacidad permite una definición de troncal sencilla para obtener resistencia (donde se pueden usar varios servidores de mediación para enrutar llamadas a la misma puerta de enlace PSTN). para la interoperabilidad de PBX, en la que se pueden usar varios troncos con diferentes directivas relacionadas y IP-PBX y un servidor de mediación, y para configuraciones de troncal de SIP, donde los servidores de mediación en diferentes sitios tienen troncos SIP a la portadora a la que hace referencia el mismo FQDN de portadora.

<div>

## <a name="see-also"></a>Vea también


[Nuevas características de la telefonía IP empresarial en Lync Server 2013](lync-server-2013-new-enterprise-voice-features.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

