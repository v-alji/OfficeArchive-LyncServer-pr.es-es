---
title: Modelo de usuario de conferencia de Lync Server 2013
description: Modelo de usuario de conferencia de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: The conferencing user model
ms:assetid: ba4bbba9-f2e3-4cab-8eba-b51f12133cab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205199(v=OCS.15)
ms:contentKeyID: 48185229
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 699f41303b82f4d8fd2864cbf1b29a1c601b826e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434286"
---
# <a name="the-conferencing-user-model-in-lync-server-2013"></a>El modelo de usuario de conferencias en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-22_

Una parte crítica del modelo de usuario de conferencia de Lync Server es el tamaño de la reunión. Después de recopilar datos de los diversos puntos de datos (tal y como se describe en la sección anterior), determinamos lo siguiente:

  - La mayoría de las reuniones son pequeñas reuniones de colaboración con un promedio de cuatro a seis participantes

  - Aproximadamente el 80 por ciento de las reuniones tiene menos de 20 participantes.

  - el 99,98 por ciento de las reuniones tiene menos de 100 participantes.

Además del tamaño de la reunión, el modelo de usuario de conferencia también tiene en cuenta diversos factores, como:

  - **Reuniones simultáneas**   ¿Cuántos usuarios esperan estar en las reuniones al mismo tiempo?

  - **Combinación de medios**   ¿Qué tipos de elementos multimedia están disponibles y qué pueden usar los usuarios en las reuniones?

  - **Tipos de usuario**   ¿Son los usuarios internos, los usuarios remotos, los usuarios federados o los usuarios anónimos?

  - **Tiempo de impulso de la reunión**   ¿Cuánto tiempo tardan los usuarios de una reunión en unirse a una reunión?

Para obtener más información sobre el modelo de usuario, consulte [modelos de usuario en Lync Server 2013](lync-server-2013-user-models.md).

Para determinar el número de reuniones y usuarios que se van a usar para las pruebas, hicimos lo siguiente:

  - Ha tomado el número total de usuarios de una organización (por ejemplo, 80.000 usuarios) y la ha multiplicado por la tasa de simultaneidad de la reunión (por ejemplo, el 5% de todos los usuarios) para determinar el número total de usuarios que se espera que estén en las reuniones al mismo tiempo (en este ejemplo, 4000 usuarios).

  - Dividir el número total de usuarios por el número de servidores de Lync Server 2013, front-end en la implementación (por ejemplo, 8 servidores) para determinar el número estimado de participantes de la reunión por servidor front-end (en este ejemplo, 500 usuarios por servidor front-end).

  - Divide el número de usuarios por servidor front-end por el tamaño medio de la reunión (por ejemplo, 4 usuarios) para determinar el número promedio estimado de reuniones por servidor front-end (en este ejemplo, 125 reuniones por servidor front-end).

  - Para obtener la carga por multimedia de cada servidor front-end, hemos estimado la combinación de medios. Por ejemplo, suponiendo que el 75% de las reuniones necesite algo más que compatibilidad de audio y el 50% de esas reuniones requieren compartir aplicaciones, un promedio de 47 reuniones y 188 usuarios se conectan simultáneamente a cada servidor front-end para el uso compartido de aplicaciones.

  - Se han probado diversos tamaños de reunión (basados en nuestro modelo de usuario de hasta 250 usuarios en un grupo compartido) para garantizar la escalabilidad del servidor.

</div>

<span> </span>

</div>

</div>

</div>

