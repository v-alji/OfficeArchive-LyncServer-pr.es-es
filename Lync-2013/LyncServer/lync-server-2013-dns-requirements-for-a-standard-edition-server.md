---
title: 'Lync Server 2013: Requisitos DNS para un servidor Standard Edition'
description: 'Lync Server 2013: requisitos DNS para un servidor Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for a Standard Edition server
ms:assetid: 5d1daf54-6e60-4ce0-9254-7d57a0835fa4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204936(v=OCS.15)
ms:contentKeyID: 48184259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea0c7219563d62a9d99bd85655b3d3fcb0c551f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399750"
---
# <a name="dns-requirements-for-a-standard-edition-server-in-lync-server-2013"></a>Requisitos DNS para un servidor Standard Edition en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tema última modificación:** 22-02-2013_

En esta sección se describen los registros del sistema de nombres de dominio (DNS) necesarios para la implementación de servidores Standard Edition.

<div>

## <a name="dns-records-for-standard-edition-servers"></a>Registros de DNS para servidores Standard Edition

La tabla siguiente especifica los requisitos DNS para la implementación del servidor Lync Server 2013 Standard Edition.


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Escenario de implementación</th>
<th>Requisito de DNS</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Servidor Standard Edition</p></td>
<td><p>Un registro A interno que resuelve el nombre de dominio completo (FQDN) del servidor en su dirección IP.</p></td>
</tr>
<tr class="even">
<td><p>Inicio de sesión de clientes automático</p></td>
<td><p>Para cada dominio SIP compatible, un registro SRV para _sipinternaltls._tcp. &lt; dominio &gt; a través del puerto 5061 que se asigna al FQDN del servidor Standard Edition que autentica y redirige las solicitudes del cliente para el inicio de sesión. Para obtener más información, consulte los requisitos DNS para el inicio de sesión <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">automático de clientes en Lync Server 2013.</a></p></td>
</tr>
<tr class="odd">
<td><p>Detección del servicio web de actualización de dispositivos por los dispositivos de comunicaciones unificadas (UC)</p></td>
<td><p>Un registro A interno con el nombre ucupdates-r2. &lt; Dominio SIP que se resuelve en la dirección IP del servidor Standard Edition que hospeda el servicio web &gt; de actualización de dispositivos. En una situación en la que un dispositivo de comunicaciones unificadas esté activado, pero en el que nunca un usuario inició sesión, el registro A permite al dispositivo detectar el servidor que hospeda el servicio web de actualización de dispositivos y obtener actualizaciones. De lo contrario, los dispositivos obtienen la información del servidor a través del aprovisionamiento en banda la primera vez que un usuario inicia sesión. Para obtener más información, consulte el servicio Web de actualización <a href="lync-server-2013-device-update-web-service.md">de dispositivos de Lync Server 2013</a> en la documentación de Operaciones.</p></td>
</tr>
<tr class="even">
<td><p>Un proxy inverso compatible con el tráfico HTTP</p></td>
<td><p>Un registro A externo que resuelve el FQDN externo de la granja de servidores web en la dirección IP externa del proxy inverso. Los clientes y los dispositivos de UC usan este registro para conectarse al proxy inverso. Para obtener más información, <a href="lync-server-2013-determine-dns-requirements.md">consulte Determinar los requisitos DNS para Lync Server 2013</a> en la documentación de planeamiento.</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a>Vea también


[Requisitos DNS para el inicio de sesión automático de clientes en Lync Server 2013](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)  
[Determinar los requisitos DNS para Lync Server 2013](lync-server-2013-determine-dns-requirements.md)  


[Servicio web de actualización de dispositivos en Lync Server 2013](lync-server-2013-device-update-web-service.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

