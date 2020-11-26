---
title: Migración del chat de grupo de Lync Server 2010 o el chat de grupo de Office Communications Server 2007 R2 al servidor de chat persistente de Lync Server 2013
description: Migración desde Lync Server 2010, chat grupal u Office Communications Server 2007 R2 conversación grupal a Lync Server 2013, servidor de chat persistente.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446860"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a>Migración del chat de grupo de Lync Server 2010 o el chat de grupo de Office Communications Server 2007 R2 al servidor de chat persistente de Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-06_

Los temas de esta sección le guían a través del proceso de migración de Lync Server 2010, chat grupal o chat grupal de Office Communications Server 2007 R2 a Lync Server 2013, servidor de chat persistente. Si su intención es que su Lync Server 2013, la implementación del servidor de chat persistente coexista con una implementación de chat grupal de Lync Server 2010, chat grupal u Office Communications Server 2007 R2, esta guía también incluye información esencial para operar en este entorno mixto. Esta guía se centra principalmente en la migración de datos para el servidor de chat persistente. Para los usuarios que migren de versiones heredadas de Lync Server a Lync Server 2013, consulte [migración de Lync server 2010 a Lync server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) y [migración de Office Communications Server 2007 R2 a Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).

<div>


> [!IMPORTANT]  
> En este tema se supone que ya ha instalado Lync Server 2013 en coexistencia con Lync Server 2010 u Office Communications Server 2007 R2.



</div>

<div>


> [!IMPORTANT]  
> En esta guía, se describen los pasos necesarios para llevar a cabo cada fase de la migración. No se trata de todas las topologías de implementación heredadas o de todos los escenarios posibles de migración. Por lo tanto, es posible que no tenga que realizar todos los pasos descritos o que necesite realizar pasos adicionales, en función de la implementación. La guía también proporciona ejemplos de pasos de verificación. Estos pasos de verificación se proporcionan para ayudarle a comprender lo que debe buscar para asegurarse de que cada fase se complete correctamente a medida que avanza en la migración. Puede modificar estos pasos de verificación en su proceso de migración específico.



</div>

Esta guía proporciona información específica para actualizar la implementación existente. No se explica cómo cambiar la topología existente. Esta guía no cubre la implementación de nuevas características. Cuando un procedimiento detallado está documentado en otra parte, esta guía le dirige a la sección documento o documento adecuada.

Este documento define los términos según se especifican en la siguiente lista.

  - *realizar*  
    El traslado de la implementación de una versión anterior del servidor de chat persistente, anteriormente conocido como servidor de chat grupal, a Lync Server 2013, servidor de chat persistente.

<!-- end list -->

  - *actualiza*  
    Instalar una versión más reciente del software en un servidor o en un equipo cliente.

<!-- end list -->

  - *coexistencia*  
    El entorno temporal que existe durante la migración, cuando se ha migrado cierta funcionalidad a Lync Server 2013, el servidor de chat persistente y otras funcionalidades siguen siendo de una versión anterior del servidor de chats grupales.

El servidor de chat persistente es una extensión de la infraestructura de Lync Server 2013. Dependiendo de su topología, puede migrar Lync Server 2010, chat grupal u Office Communications Server 2007 R2 chat grupal a Lync Server 2013 servidor de chat persistente. Para obtener detalles sobre las topologías disponibles y los requisitos técnicos y de software para migrar servidor de chat de grupo, consulte [planificación de servidor de chat persistente en Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) en la documentación de planificación.

Si su organización requiere soporte de cumplimiento, ahora se instala automáticamente con cada servidor de chat persistente. Ya no se necesita un servidor independiente para el cumplimiento.

<div>


> [!IMPORTANT]  
> El servidor de chat persistente debe instalarse en un sistema de archivos NTFS para ayudar a exigir la seguridad del sistema de archivos. FAT32 no es un sistema de archivos compatible para el servidor de chat persistente.<BR>Si su organización requiere soporte de cumplimiento, ahora se instala automáticamente con cada servidor de chat persistente. Ya no se necesita un servidor independiente para el cumplimiento. Para obtener más detalles sobre los cambios en el servidor de chat persistente de Lync Server 2013 &nbsp; , consulte <A href="lync-server-2013-new-persistent-chat-server-features.md">nuevas características del servidor de chat persistente en lync Server 2013</A> en la documentación de introducción.



</div>

<div>

## <a name="in-this-section"></a>En esta sección

  - [Escenario de migración estándar - Alto nivel](standard-migration-scenario-high-level.md)

  - [Proceso de migración - Detalles](migration-process-details.md)

  - [Consideraciones sobre la coexistencia](coexistence-considerations.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

