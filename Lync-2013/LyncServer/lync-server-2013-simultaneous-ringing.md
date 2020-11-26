---
title: 'Lync Server 2013: Tono de llamada simultáneo'
description: 'Lync Server 2013: llamadas simultáneas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Simultaneous ringing
ms:assetid: df02f919-4d50-4832-9300-6c51f8b4fc56
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994079(v=OCS.15)
ms:contentKeyID: 51803990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 595c8c1d4ce105e2189002f18733ffae92cff8bf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423823"
---
# <a name="simultaneous-ringing-in-lync-server-2013"></a>Tono de llamada simultáneo en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-03-09_

Cuando la persona llamada tiene habilitado el timbre simultáneo, Location-Based el enrutamiento analiza la ubicación de la persona que llama y los puntos finales de las partes a las que se llama para determinar si se debe distribuir la llamada.

En la siguiente tabla se muestra un usuario con la configuración de llamadas simultáneas habilitada y el destino de llamadas simultáneas es un usuario en el mismo sitio de red, en un sitio de red diferente o en un sitio de red desconocido.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Llamada RTC entrante para</th>
<th>Ubicado en el mismo sitio de red que el destinatario</th>
<th>Ubicado en un sitio de red distinto del sitio del destinatario</th>
<th>Se encuentra en un sitio de red desconocido o no está habilitado para Location-Based enrutamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Usuario de Lync</p></td>
<td><p>Llamadas simultáneas permitidas</p></td>
<td><p>Llamadas simultáneas no permitidas</p></td>
<td><p>Llamadas simultáneas no permitidas</p></td>
</tr>
</tbody>
</table>

  
En la tabla siguiente se muestra una llamada de un usuario de Lync (es decir, el autor de la llamada de Lync) en el mismo sitio de red, en un sitio de red diferente o desde un sitio de red desconocido. El destinatario de la llamada tiene un punto final de la RTC (por ejemplo, teléfono móvil) configurado como un objetivo de llamada simultánea. En este caso, el enrutamiento de Location-Based determinará si la llamada debe dirigirse al destino simultáneo (por ejemplo, teléfono móvil) del destinatario de la llamada.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Destino de llamadas simultáneas</th>
<th>Ubicado en el mismo sitio de red que el destinatario</th>
<th>Ubicado en un sitio de red distinto del sitio del destinatario</th>
<th>Se encuentra en un sitio de red desconocido o no está habilitado para Location-Based enrutamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Extremo de RTC</p></td>
<td><p>Llamadas simultáneas permitidas a través de la directiva del enrutamiento de voz del sitio del autor de la llamada</p></td>
<td><p>Llamadas simultáneas permitidas a través de la directiva del enrutamiento de voz del sitio del autor de la llamada</p></td>
<td><p>Llamadas simultáneas permitidas a través de la directiva del enrutamiento de voz del autor de la llamada para troncos no habilitados para el enrutamiento basado en ubicación</p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a>Vea también


[Escenarios para el enrutamiento basado en ubicación en Lync Server 2013](lync-server-2013-scenarios-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

