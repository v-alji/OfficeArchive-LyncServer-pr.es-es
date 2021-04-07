---
title: 'Lync Server 2013: requisitos DNS para grupos de servidores front-end'
description: 'Lync Server 2013: requisitos DNS para grupos de servidores front-end.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429073"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a>Requisitos DNS para grupos front-end en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tema Última modificación:** 2012-11-07_

En esta sección se describen los registros del Sistema de nombres de dominio (DNS) necesarios para implementar grupos de servidores front-end.

<div>

## <a name="dns-records-for-front-end-pools"></a>Registros de DNS para grupos de servidores front-end

En la tabla siguiente se especifican los requisitos DNS para una implementación de grupo front-end de Lync Server 2013.

### <a name="dns-requirements-for-a-front-end-pool"></a>Requisitos de DNS para un grupo de servidores front-end

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
<td><p>Grupo de servidores front-end con varios servidores front-end y un equilibrador de carga de hardware (independientemente de si el equilibrio de carga de DNS también está implementado en este grupo)</p></td>
<td><p>Al usar el equilibrio de carga DNS y un equilibrador de carga de hardware, debe hospedar (A) registros. Cree un registro A interno que resuelva el nombre de dominio completo (FQDN) del grupo front-end para el equilibrio de carga DNS. Cree un registro de host interno (A) para los servicios web internos en la dirección IP virtual (VIP) del equilibrador de carga. Debe usar el nombre de los servicios web internos tal como se define en generador de topologías.</p>
<p>Por ejemplo, si usa el equilibrio de carga DNS y el equilibrio de carga de hardware, tendría un registro A para cada servidor front-end en un grupo de servidores para el equilibrio de carga DNS y un registro A para los servicios web internos que apunten a la IP virtual del equilibrador de carga de hardware:</p>
<ul>
<li><p>Equilibrio de carga de DNS: Pool01.contoso.net Dirección IP del grupo 10.10.10.5</p>
<div>

> [!WARNING]  
> Cada servidor front-end también tendrá un registro A distinto:


</div>
<ol>
<li><p>FE01.contoso.net 10.10.10.1</p></li>
<li><p>FE02.contoso.net 10.10.10.2</p></li>
<li><p>FE03.contoso.net 10.10.10.3</p></li>
<li><p>FE04.contoso.net 10.10.10.4</p></li>
</ol></li>
<li><p>Equilibrio de carga de hardware: WebInternal.contoso.net Dirección IP de HLB VIP 192.168.10.5</p></li>
</ul>
<p>Todo el tráfico, excepto el tráfico HTTP/HTTPS, usará el registro Pool01.contoso.net. El tráfico HTTP/HTTPS utilizará la dirección definida de los servicios web internos, 192.168.10.5.</p></td>
</tr>
<tr class="even">
<td><p>Grupo de servidores front-end con equilibrio de carga de DNS implementado</p></td>
<td><p>Un conjunto de registros A internos que resuelven el FQDN del grupo para la dirección IP de cada uno de los servidores del grupo. Tiene que haber un registro A para cada servidor del grupo.</p></td>
</tr>
<tr class="odd">
<td><p>Grupo de servidores front-end con equilibrio de carga de DNS implementado</p></td>
<td><p>Un conjunto de registros A internos que resuelven el FQDN de cada servidor del grupo en la dirección IP de ese servidor. Para obtener más información, <a href="lync-server-2013-dns-load-balancing.md">vea Equilibrio de carga DNS en Lync Server 2013</a> en la documentación de planeamiento.</p></td>
</tr>
<tr class="even">
<td><p>Un grupo de servidores front-end con un solo servidor front-end y una base de datos back-end dedicada sin equilibrador de carga</p></td>
<td><p>Un registro A interno que resuelve el FQDN del grupo de servidores front-end para la dirección IP del único servidor front-end Enterprise Edition.</p></td>
</tr>
<tr class="odd">
<td><p>Inicio de sesión de clientes automático</p></td>
<td><p>Para cada dominio SIP compatible, un registro SRV para _sipinternaltls._tcp. &lt; dominio &gt; a través del puerto 5061 que se asigna al FQDN del grupo front-end que autentica y redirige las solicitudes de cliente para el inicio de sesión. Para obtener más información, vea Requisitos DNS para el inicio de sesión automático del cliente <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">en Lync Server 2013.</a></p></td>
</tr>
<tr class="even">
<td><p>Detección del servicio web de actualización de dispositivos por los dispositivos de comunicaciones unificadas (UC)</p></td>
<td><p>Un registro A interno con el nombre ucupdates-r2. &lt; Dominio SIP que se resuelve en la dirección IP del grupo &gt; front-end que hospeda el servicio web de actualización de dispositivos. En caso de que se active un dispositivo de UC en el que nunca ningún usuario inició sesión, el registro A permite al dispositivo detectar el grupo de servidores front-end que hospeda el servicio web de actualización de dispositivos y obtener actualizaciones. De lo contrario, los dispositivos obtienen esta información a través del aprovisionamiento en banda la primera vez que un usuario inicia sesión.</p>
<div>

> [!IMPORTANT]  
> Si tiene una implementación existente del servicio web de actualización de dispositivos en Lync Server 2010, ya ha creado un registro A interno con el nombre ucupdates. &lt; Dominio SIP &gt; . Para Microsoft Office Communications Server 2007 R2, debe crear un registro DNS A adicional con el nombre ucupdates-r2. &lt; Dominio SIP &gt; .


</div></td>
</tr>
<tr class="odd">
<td><p>Un proxy inverso compatible con el tráfico HTTP</p></td>
<td><p>Un registro A externo que resuelve el FQDN externo de la granja de servidores web en la dirección IP externa del proxy inverso. Los clientes y los dispositivos de UC usan este registro para conectarse al proxy inverso. Para obtener más información, vea <a href="lync-server-2013-determine-dns-requirements.md">Determinar los requisitos DNS para Lync Server 2013</a> en la documentación de planeamiento.</p></td>
</tr>
</tbody>
</table>


La tabla siguiente muestra un ejemplo de los registros de DNS necesarios para el FQDN interno de la granja de servidores web.

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a>Ejemplo de los registros de DNS para el FQDN interno de la granja de servidores web

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>FQDN interno de la granja de servidores web</th>
<th>FQDN del grupo de servidores</th>
<th>Registro(s) A de DNS</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>webcon.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>Registro A de DNS para ee-pool.contoso.com que se resuelve en la dirección VIP del equilibrador de carga que usan los servidores front-end.</p>
<p>Registro A de DNS para webcon.contoso.com que se resuelve en la dirección VIP del equilibrador de carga que usan los servidores front-end.</p></td>
</tr>
<tr class="even">
<td><p>ee-pool.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>Registro A de DNS para ee-pool.contoso.com que se resuelve en la dirección IP virtual (VIP) del equilibrador de carga que usan los servidores front-end Enterprise Edition en el grupo de servidores front-end.</p>
<p>Tenga en cuenta que si usa el equilibrio de carga de DNS en este grupo, su grupo de servidores front-end y la granja de servidores web internos no podrán tener el mismo FQDN.</p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

