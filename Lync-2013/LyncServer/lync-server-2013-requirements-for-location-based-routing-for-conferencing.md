---
title: 'Lync Server 2013: requisitos para el enrutamiento de Location-Based para conferencias'
description: 'Lync Server 2013: requisitos para el enrutamiento de Location-Based para conferencias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements for Location-Based Routing for conferencing
ms:assetid: 766d9286-2c34-4faf-bb3e-f0ca478a70cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362806(v=OCS.15)
ms:contentKeyID: 56335085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbaa1af2690c3148d2ecfb173b13be288a21d80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442666"
---
# <a name="requirements-for-location-based-routing-for-conferencing-in-lync-server-2013"></a>Requisitos para Location-Based el enrutamiento de conferencias en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-07-19_

A continuación se indican los requisitos necesarios para la instalación y configuración de la aplicación de conferencia de enrutamiento de Location-Based:

  - La actualización acumulativa 2 de Lync Server 2013 debe implementarse en todos los servidores o grupos de servidores de su topología.

<div>


> [!NOTE]  
> Si un servidor de Lync o un grupo de servidores de su topología no tienen instalado la actualización acumulativa 2 o posterior de Lync Server 2013, no se puede garantizar la aplicación de Location-Based el enrutamiento de las reuniones de Lync.



</div>

  - Lync Server 2013 Location-Based el enrutamiento es un requisito previo para Location-Based aplicación de conferencia de enrutamiento. Para obtener más información sobre cómo configurar Lync Server 2013 Location-Based enrutamiento, consulte [configuring Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).

  - Los requisitos de Location-Based aplicación de conferencia de enrutamiento son los mismos que se incluyen en el enrutamiento de Lync Server 2013 Location-Based. Para obtener más información, consulte [planeamiento de Location-Based enrutamiento](lync-server-2013-planning-for-location-based-routing.md).

<div>

## <a name="supported-servers"></a>Servidores compatibles

La aplicación de conferencia de Location-Based enrutamiento requiere que la actualización acumulativa 2 de Lync Server 2013 se implemente en todos los grupos de Front-End y servidores Standard Edition de su topología. Si la actualización acumulativa 2 de Lync Server 2013 no está instalada en algunos servidores de Lync de su topología, Location-Based restricciones de enrutamiento no se pueden aplicar completamente en las reuniones de Lync ni en las transferencias de llamadas Consultiva.

En la siguiente tabla se identifica la combinación de las versiones y los roles de servidor que admiten Location-Based enrutamiento.


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Versión del grupo de servidores front-end</p></td>
<td><p>Versión del servidor de mediación</p></td>
<td><p>Compatible</p></td>
</tr>
<tr class="even">
<td><p>Actualización acumulativa 2 de Lync Server 2013</p></td>
<td><p>Actualización acumulativa 2 de Lync Server 2013</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Actualización acumulativa 2 de Lync Server 2013</p></td>
<td><p>Actualización acumulativa 1 de Lync Server 2013</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Actualización acumulativa 2 de Lync Server 2013</p></td>
<td><p>Lync Server 2010</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Actualización acumulativa 2 de Lync Server 2013</p></td>
<td><p>Office Communications Server 2007 R2</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Actualización acumulativa 1 de Lync Server 2013</p></td>
<td><p>Cualquiera</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Lync Server 2010</p></td>
<td><p>Cualquiera</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Office Communications Server 2007 R2</p></td>
<td><p>Cualquiera</p></td>
<td><p>No</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients"></a>Clientes compatibles

Los clientes de Lync que admiten el enrutamiento Location-Based de reuniones de Lync son los mismos clientes que admiten el enrutamiento de Lync Server 2013 Location-Based. Para obtener más información, consulte [compatibilidad de servidor y cliente para Location-Based enrutamiento](lync-server-2013-client-and-server-support-for-location-based-routing.md).

</div>

<div>

## <a name="mediation-server-requirements-for-consultative-call-transfers"></a>Requisitos del servidor de mediación para las transferencias de llamadas Consultiva

La aplicación de conferencia de Location-Based enrutamiento requiere la implementación de servidores de mediación independientes para exigir Location-Based restricciones de enrutamiento en las transferencias de llamadas Consultiva.

Para exigir Location-Based el enrutamiento de las transferencias de llamadas Consultiva, el servidor de mediación debe estar asociado solo con un servidor de mediación del mismo nivel (por ejemplo, PBX, puerta de enlace SIP, etc.) en las regiones de red en las que se requiere Location-Based enrutamiento. Si se implementan pares de servidores de mediación adicionales en la misma región de red, el servidor de mediación del mismo nivel debe estar asociado a un servidor de mediación diferente. Este requisito se detalla de la siguiente manera:

  - Servidor de mediación único para los interlocutores de varios servidores de mediación cuando una transferencia de llamada Consultiva se dirige a un servidor de mediación del mismo nivel a través de un servidor de mediación que está configurado con varios troncos SIP para varios interlocutores (es decir, PBX y puertas de enlace), la transferencia de llamadas Consultiva está bloqueada a través de otros troncos SIP.
    
    Por ejemplo, en el caso de un único servidor de mediación que atienda un servidor de mediación de puerta de enlace RTC y un servidor de mediación de PBX, se observará el siguiente comportamiento:
    
      - Cuando un usuario de Lync de un sitio determinado (por ejemplo, el sitio 1) intenta transferir una llamada con un punto final de la RTC a un usuario de Lync desde un sitio diferente (por ejemplo, el sitio 2) a través de una transferencia Consultiva, la llamada no se permitirá para evitar la omisión de llamadas RTC.
    
      - Cuando un usuario de Lync de un sitio determinado (por ejemplo, el sitio 1) intenta transferir una llamada con un extremo de PBX en el mismo sitio (sitio 1) a un usuario de Lync desde un sitio diferente (por ejemplo, el sitio 2) a través de una transferencia Consultiva, la llamada no se permitirá incluso si no se produce ninguna incumplimiento en la posible omisión de llamadas RTC.

  - Servidores de mediación independientes por servidor de mediación del mismo nivel
    
    Cuando una transferencia Consultiva se dirige a un interlocutor de servidor de mediación, la transferencia Consultiva se evaluará en relación con el servidor de mediación que atendida el servidor de mediación. La llamada no se permitirá o se autorizará en función de su potencial de incurrir en una omisión de peaje de RTC, independientemente del resto de los servidores de mediación del sitio que sean atendidas por servidores de mediación independientes.
    
    Por ejemplo, en el caso de un servidor de mediación independiente que está atendiendo a un servidor de mediación de puerta de enlace RTC y un servidor de mediación de PBX, se observará el siguiente comportamiento:
    
      - Cuando un usuario de Lync de un sitio determinado (por ejemplo, el sitio 1) intenta transferir una llamada con un punto final de la RTC a un usuario de Lync desde un sitio diferente (por ejemplo, el sitio 2) a través de una transferencia Consultiva, la llamada no se permitirá para evitar la omisión de llamadas RTC.
    
      - Cuando un usuario de Lync de un sitio determinado (es decir, el sitio 1) intenta transferir una llamada con un extremo de PBX en el mismo sitio (sitio 1) a un usuario de Lync desde un sitio diferente (por ejemplo, el sitio 2) a través de la transferencia Consultiva, la llamada se permitirá porque no se produce en la posible omisión de llamadas RTC.

</div>

<div>

## <a name="capabilities-not-supported-by-the-location-based-routing-conferencing-application"></a>Funciones no compatibles con la aplicación de conferencia de enrutamiento de Location-Based

Las siguientes características no son compatibles con la aplicación Location-Based de conferencia de enrutamiento:

  - Conferencias de acceso telefónico local. No se puede aplicar el enrutamiento Location-Based para las conferencias de acceso telefónico local. Las solicitudes de acceso telefónico a una conferencia determinada no estarán limitadas por el enrutamiento del Location-Based incluso si el organizador de la Conferencia es un usuario de Lync habilitado para Location-Based el enrutamiento.

  - Se recomienda no suministrar números de acceso a la Conferencia en regiones donde sea necesario exigir Location-Based restricciones de enrutamiento.

</div>

</div>

<span> </span>

</div>

</div>

</div>

