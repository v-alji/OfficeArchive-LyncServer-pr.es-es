---
title: 'Lync Server 2013: Ubicación del usuario'
description: 'Lync Server 2013: Ubicación del usuario.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User's location
ms:assetid: ce57941d-086b-448e-8ada-c7d636a2a1c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994073(v=OCS.15)
ms:contentKeyID: 51803984
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a92ec780809cdb3e1ee582ce6c348c884bbb5890
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439173"
---
# <a name="users-location-in-lync-server-2013"></a>Ubicación del usuario en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-03-09_

El enrutamiento de Location-Based aprovecha las mismas regiones, sitios y subredes de la red que se definen en Lync Server usado por E9-1-1, CAC y media bypass para aplicar restricciones de enrutamiento de llamadas para evitar la omisión de llamadas RTC. La ubicación de un usuario viene determinada por la subred IP de los puntos de conexión de Lync del usuario. Cada subred IP está asociada a un sitio de red, y los sitios de red se agrupan en regiones de red definidas por el administrador. El enrutamiento basado en ubicación se aplica en función del sitio de red del usuario.

Location-Based las reglas de enrutamiento se aplican por sitio de red, lo que significa que se aplicará a todos los puntos de conexión habilitados para Location-Based enrutamiento que se encuentren en el mismo sitio de red. Los administradores pueden aplicar el enrutamiento basado en ubicación a los sitios de red que lo necesiten.

Se pueden definir directivas de enrutamiento de voz en cada sitio de red, para que todos los usuarios ubicados en el sitio de red utilicen una puerta de enlace RTC concreta para llamar a números de teléfono de RTC. Dichas directivas de enrutamiento de voz tendrán prioridad sobre el enrutamiento definido por la Directiva de voz del usuario cuando el usuario se encuentre en un sitio de red habilitado para Location-Based enrutamiento y evitará el enrutamiento de llamadas a través de puertas de enlace RTC habilitadas para Location-Based enrutamiento. Cuando un usuario de Lync realiza una llamada RTC, la Directiva de voz del usuario determina si el usuario puede tener autorización para realizar la llamada. Si la Directiva de voz del usuario permite al usuario realizar la llamada, el enrutamiento de Location-Based determina qué puerta de enlace RTC debe salir de la llamada. Location-Based enrutamiento realiza esta determinación en función de la ubicación del usuario.

La ubicación de un usuario se puede clasificar de las siguientes maneras:

  - El usuario se encuentra en un sitio de red conocido habilitado para Location-Based enrutamiento y su número de realizado (marcado directo) termina en una puerta de enlace RTC situada en el mismo sitio de red (es decir, Office). El enrutamiento de las llamadas salientes se realizará a través de la directiva de enrutamiento de voz del sitio de red en el que está ubicado el usuario. Las llamadas de RTC entrantes que reciba el usuario se redirigirán a los extremos ubicados en el mismo sitio de red que la puerta de enlace RTC.

  - El usuario está ubicado en un sitio de red conocido y diferente del sitio de red donde se encuentra la puerta de enlace RTC (es decir, el usuario viajó a otra oficina de la compañía). El enrutamiento de las llamadas salientes utilizará la directiva de enrutamiento de voz del sitio de red en el que está ubicado el usuario. Las llamadas de RTC entrantes que reciba el usuario no se redirigirán a los extremos ubicados en sitios diferentes del de la puerta de enlace RTC, para evitar que se omitan los números de pago de RTC.

  - Cuando un usuario se encuentra en un sitio de red desconocido para la implementación de Lync Server, el enrutamiento de las llamadas salientes se basará en la Directiva de voz asignada al usuario a las puertas de enlace RTC no enlazadas a las restricciones de enrutamiento de Location-Based. Las llamadas de RTC entrantes no se redirigirán a los extremos ubicados en sitios de red desconocidos, para evitar que se omitan los números de pago de RTC.

<div>

## <a name="see-also"></a>Vea también


[Instrucciones para el enrutamiento basado en ubicación en Lync Server 2013](lync-server-2013-guidance-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

