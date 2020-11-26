---
title: 'Lync Server 2013: Llamadas entrantes'
description: 'Lync Server 2013: llamadas entrantes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Incoming calls
ms:assetid: 65b9c1b4-6af7-4527-8c33-22c4442bd209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994038(v=OCS.15)
ms:contentKeyID: 51803948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a72c7fc378240f9751eae8e6c24e9cc601b08d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427302"
---
# <a name="incoming-calls-in-lync-server-2013"></a>Llamadas entrantes en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-03-09_

El enrutamiento de llamadas entrantes a los usuarios habilitados para el enrutamiento de Location-Based depende de la ubicación del extremo del usuario. El enrutamiento de llamadas entrantes se ve afectado de la siguiente manera. Si un usuario tiene una llamada entrante a un extremo ubicado en un sitio de red habilitado para enrutamiento de Location-Based y el punto final se encuentra en el mismo sitio de red que la puerta de enlace RTC, la llamada se redirigirá. Si un usuario tiene una llamada entrante a un extremo ubicado en un sitio de red habilitado para enrutamiento de Location-Based y el punto final se encuentra en un sitio de red diferente de la puerta de enlace PSTN, la llamada no se redirigirá. Cuando un usuario no tenga extremos ubicados en el mismo sitio de red que la puerta de enlace RTC desde la que se origina la llamada entrante, la llamada entrante se redirigirá directamente al correo de voz del usuario y se enviará una notificación de llamada perdida a la persona a la que se está llamando.

La configuración del desvío de llamadas de un usuario habilitado para Location-Based el enrutamiento continuará aplicándose; sin embargo, las llamadas desviadas estarán sujetas a Location-Based restricciones de enrutamiento del usuario.

En la tabla siguiente se muestra cómo el enrutamiento de Location-Based afecta al enrutamiento de las llamadas entrantes en función de la ubicación del punto final de la llamada. El sitio de red de la puerta de enlace RTC está habilitado para Location-Based enrutamiento y Location-Based enrutamiento solo permite el enrutamiento de llamadas RTC a extremos dentro del mismo sitio de red.

### <a name="callee-receiving-an-inbound-call-from-the-pstn"></a>El destinatario recibe una llamada entrante desde la RTC

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>El extremo del destinatario se encuentra en el mismo sitio de red que la puerta de enlace RTC</th>
<th>El extremo del destinatario no se encuentra en el mismo sitio de red que la puerta de enlace RTC</th>
<th>El extremo del destinatario se encuentra en un sitio de red desconocido o no habilitado para el enrutamiento basado en ubicación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Enrutamiento de una llamada RTC entrante</p></td>
<td><p>La llamada entrante se redirige a los extremos del destinatario</p></td>
<td><p>La llamada entrante no se redirige a los extremos del destinatario</p></td>
<td><p>La llamada entrante no se redirige a los extremos del destinatario</p></td>
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

