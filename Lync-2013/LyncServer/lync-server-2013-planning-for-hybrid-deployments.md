---
title: 'Lync Server 2013: Planeación de implementaciones híbridas'
description: 'Lync Server 2013: Planeación de implementaciones híbridas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424551"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a>Planeación de implementaciones híbridas de Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tema Última modificación:** 2016-05-25_

Debe tener en cuenta los siguientes requisitos para los usuarios y su infraestructura de red al planear una implementación híbrida.

<div>

## <a name="infrastructure-requirements"></a>Requisitos de infraestructura

Debe tener lo siguiente configurado en su entorno para implementar e implementar una implementación híbrida.

  - Una organización de Microsoft 365 u Office 365 con Skype Empresarial Online habilitado. Tenga en cuenta que solo puede usar un único espacio empresarial para una configuración híbrida con su implementación local.

  - Una única implementación local (infraestructura) de Skype Empresarial Server o Lync Server que se implementa en una topología compatible. Consulte Requisitos de topología.
    
    Para obtener información sobre cómo configurar la implementación de Lync Server 2013 o Lync Server 2010 para la implementación híbrida, vea Configurar implementaciones híbridas de [Lync Server 2013.](lync-server-2013-configuring-hybrid-deployments.md)

  - Herramientas administrativas de Skype Empresarial Server 2015. Si usa Lync Server 2013 o Lync Server 2010, puede usar las herramientas administrativas de Lync Server 2013.

  - Para admitir el inicio de sesión único con Microsoft 365 u Office 365 para que los usuarios puedan usar las mismas credenciales de inicio de sesión para iniciar sesión en Office de forma local, puede usar las características de sincronización de contraseña de Azure Active Directory (AAD) Connect. También puede usar los Servicios de federación de Active Directory (AD FS) para el inicio de sesión único con Microsoft 365 u Office 365.
    
    Para obtener más información, vea Integrar las identidades locales [con Azure Active Directory.](https://go.microsoft.com/fwlink/p/?linkid=619754)

  - Una solución de sincronización de directorio único para mantener sincronizados los objetos locales y en línea de Active Directory. Para obtener más información sobre la sincronización de directorios, vea [Herramientas de integración de directorios.](https://go.microsoft.com/fwlink/p/?linkid=530320)

</div>

<div>

## <a name="lync-client-support"></a>Soporte técnico de cliente de Lync

Hay algunas diferencias en las características admitidas en los clientes de Lync, así como en las características disponibles en entornos locales y en línea. Antes de decidir dónde desea hospedar usuarios de su organización, puede ver el soporte técnico del cliente para las distintas configuraciones de Lync Server. Los siguientes clientes son compatibles con Skype Empresarial Online en una implementación híbrida de Lync:

  - Lync 2010

  - Lync 2013

  - Aplicación de la Tienda Windows de Lync

  - Lync Web App

  - Lync Mobile

  - Lync para Mac 2011

  - Sistema Lync Room

  - Lync Basic 2013

Para obtener más información sobre el soporte técnico del cliente, vea los temas siguientes:

  - [Clientes para Lync Online](https://go.microsoft.com/fwlink/?linkid=281902)

  - [Tablas de comparación de clientes para Lync Server 2013](lync-server-2013-desktop-client-comparison-tables.md)

  - [Tablas de comparación de clientes móviles para Lync Server 2013](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a>Requisitos de topología

Para configurar la implementación para la implementación híbrida con Skype Empresarial Online, debe tener una de las siguientes topologías compatibles:

  - Una implementación de Skype Empresarial Server 2015 con todos los servidores que ejecutan Skype Empresarial Server 2015.

  - Una implementación de Lync Server 2013 con todos los servidores que ejecutan Lync Server 2013.

  - Una implementación de Lync Server 2010 con todos los servidores que ejecutan Lync Server 2010 con las actualizaciones acumulativas más recientes.
    
      - El servidor perimetral de federación y el servidor de salto siguiente del servidor perimetral de federación deben ejecutar Lync Server 2010 con las actualizaciones acumulativas más recientes.
    
      - Las herramientas administrativas de Skype Empresarial Server 2015 o Lync Server 2013 deben estar instaladas en al menos un servidor o estación de trabajo de administración.

  - Una implementación mixta de Lync Server 2013 y Skype Empresarial Server 2015 con los siguientes roles de servidor en al menos un sitio que ejecute Skype Empresarial Server 2015:
    
      - Al menos un grupo de servidores Enterprise o un servidor Standard Edition
    
      - El grupo de directores asociado con la federación SIP, si existe
    
      - El grupo de servidores perimetrales asociado con la federación SIP

  - Una implementación mixta de Lync Server 2010 y Skype Empresarial Server 2015 con los siguientes roles de servidores en al menos un sitio que ejecuta Skype Empresarial Server 2015:
    
      - Al menos un grupo de servidores Enterprise o un servidor Standard Edition
    
      - El grupo de directores asociado con la federación SIP, si existe
    
      - El grupo de servidores perimetrales asociado con la federación SIP para el sitio

  - Una implementación mixta de Lync Server 2010 y Lync Server 2013 con los siguientes roles de servidor en al menos un sitio que ejecute Lync Server 2013:
    
      - Al menos un grupo de servidores Enterprise o un servidor Standard Edition en el sitio
    
      - El grupo de directores asociado con la federación SIP, si existe en el sitio
    
      - El grupo de servidores perimetrales asociado con la federación SIP para el sitio

<div>


> [!IMPORTANT]  
> Toda la administración de usuarios, incluidos los movimientos de usuario entre locales y UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, debe realizarse con la última versión instalada de las herramientas administrativas. Las herramientas administrativas deben instalarse en un servidor independiente que tenga acceso a la implementación local existente y a Internet. El cmdlet <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> para mover usuarios de su implementación local a UNRESOLVED_TOKEN_VAL(skype16_online) debe ejecutarse desde las herramientas administrativas conectadas a su implementación local.



</div>

Para obtener más información sobre las topologías compatibles, vea Topologías admitidas en [Lync Server 2013](lync-server-2013-supported-topologies.md)y Topologías de referencia de [Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=398709)para implementaciones híbridas empresariales.

Para solucionar problemas de información sobre implementaciones híbridas y conectar PowerShell a Lync Online, vea [Lync Online: Lync PowerShell y Solución de problemas híbridos.](https://go.microsoft.com/fwlink/p/?linkid=306718)

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a>Requisitos para listas de federación permitidas o bloqueadas

La lista de dominios permitidos incluye los dominios que tienen configurado un nombre de dominio completo (FQDN) del perímetro de asociado. En ocasiones, se conocen como *servidores de asociado permitidos* o *asociados directos de federación*. Familiarícese con la diferencia entre las federaciones abiertas y cerradas, conocidas respectivamente como *detección de asociado* o *lista de dominios de asociado permitidos* en las implementaciones locales.

Los requisitos siguientes necesitan cumplirse para configurar correctamente una implementación híbrida:

  - La coincidencia de dominios debe configurarse igual para su implementación local y su organización de Microsoft 365 u Office 365. Si la detección de asociado está habilitada en la implementación local, configure una federación abierta para el inquilino en línea. Si, por el contrario, la detección de asociado no está habilitada, configure una federación cerrada para el inquilino en línea.

  - La lista de dominios bloqueados de la implementación local necesita coincidir exactamente con la lista de dominios bloqueados del inquilino en línea.

  - La lista de dominios permitidos de la implementación local necesita coincidir exactamente con la lista de dominios permitidos del inquilino en línea.

  - La federación debe estar habilitada para las comunicaciones externas para el inquilino en línea, que se configura mediante el Panel de control de Lync Online.

</div>

<div>

## <a name="dns-settings"></a>Configuración DNS

Al crear registros DNS para implementaciones híbridas, todos los registros DNS externos de Lync deben apuntar a la infraestructura local. Para obtener más información sobre los registros DNS necesarios, consulte Requisitos del Sistema de nombres de dominio [(DNS) para Lync Server 2013.](lync-server-2013-domain-name-system-dns-requirements.md)

Además, debe asegurarse de que la resolución DNS que se describe en la siguiente tabla funciona en su implementación local:


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Registro DNS</p></td>
<td><p>Lo puede resolver</p></td>
<td><p>Requisito de DNS</p></td>
</tr>
<tr class="even">
<td><p>Registro SRV dns para _sipfederationtls._tcp. &lt; sipdomain.com &gt; para todos los dominios SIP compatibles que se resuelven en IP externas de Access Edge</p></td>
<td><p>Servidores perimetrales</p></td>
<td><p>Habilite la comunicación federada en una configuración híbrida. El servidor perimetral tiene que saber hacia dónde redirigir el tráfico federado para el dominio SIP que se divide entre las formas local y en línea.</p></td>
</tr>
<tr class="odd">
<td><p>DNS A registros para FQDN del servicio de conferencia web perimetral, por ejemplo, webcon.contoso.com resolver en IP externas del perímetro de conferencia web</p></td>
<td><p>Equipos de usuarios conectados a la red corporativa interna</p></td>
<td><p>Permitir a los usuarios en línea presentar o ver contenido en reuniones hospedadas locales. El contenido incluye archivos de PowerPoint, pizarras, sondeos y notas compartidas.</p></td>
</tr>
</tbody>
</table>


Dependiendo de cómo esté configurado DNS en su organización, es posible que tenga que agregar estos registros a la zona DNS hospedada interna para los dominios SIP correspondientes para proporcionar una resolución dns interna a estos registros.

</div>

<div>

## <a name="firewall-considerations"></a>Consideraciones del firewall

Los equipos de la red deben poder realizar búsquedas DNS de Internet estándar. Si estos equipos pueden llegar a sitios de Internet estándar, la red cumple este requisito.

Según la ubicación del centro de datos de Microsoft Online Services, también debe configurar los dispositivos de firewall de red para que acepten conexiones basadas en nombres de dominio comodín (por ejemplo, todo el tráfico de \* .outlook.com). Si los firewalls de su organización no admiten configuraciones de nombres comodín, tendrá que determinar manualmente los intervalos de direcciones IP que le gustaría permitir y los puertos especificados.

Consulte el tema de ayuda Direcciones URL e [intervalos de direcciones IP de Office 365.](https://go.microsoft.com/fwlink/p/?linkid=252942)

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a>Requisitos de puerto y protocolo

Además de los requisitos de puerto para la comunicación interna de Lync Server 2013, también debe configurar los siguientes puertos.


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Protocolo /Puerto</th>
<th>Aplicaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TCP 443</p></td>
<td><p>Abrir entrada</p>
<ul>
<li><p>Servicios de federación de Active Directory (rol de servidor de federación)</p>
<p>Para obtener más información, vea <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Descripción de los servicios de rol de AD FS</a>.</p></li>
<li><p>Servicios de federación de Active Directory (rol de servidor proxy)</p></li>
<li><p>Microsoft Online Services Portal</p></li>
<li><p>Portal de mi empresa</p></li>
<li><p>Outlook Web App</p></li>
<li><p>Cliente de Lync (comunicación a Lync Online desde Lync Server local)</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>TCP 80 y 443</p></td>
<td><p>Abrir entrada</p>
<ul>
<li><p>Microsoft Online Services - Herramienta de sincronización de directorios</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>TCP 5061</p></td>
<td><p>Abrir entrada y salida en el servidor perimetral</p></td>
</tr>
<tr class="even">
<td><p>PSOM/TLS 443</p></td>
<td><p>Abrir entrantes y salientes para sesiones de uso compartido de datos</p></td>
</tr>
<tr class="odd">
<td><p>STUN/TCP 443</p></td>
<td><p>Abrir sesiones entrantes y salientes para audio, vídeo y uso compartido de aplicaciones</p></td>
</tr>
<tr class="even">
<td><p>STUN/UDP 3478</p></td>
<td><p>Abrir entradas y salidas para sesiones de audio y vídeo</p></td>
</tr>
<tr class="odd">
<td><p>RTP/TCP 50000-59999</p></td>
<td><p>Abrir salida para sesiones de audio y vídeo</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a>Cuentas de usuario y datos

En una implementación híbrida de Lync Server 2013, cualquier usuario que desee hospedar en Lync Online primero debe crearse en la implementación local, de modo que la cuenta de usuario se cree en Servicios de dominio de Active Directory. A continuación, puede mover el usuario a Skype Empresarial Online, que moverá la lista de contactos del usuario.

Al sincronizar cuentas de usuario entre las implementaciones de Lync local y Lync Online con AD FS y Dirsync, debe sincronizar las cuentas de AD para todos los usuarios de Lync de su organización entre sus implementaciones de Lync locales y en línea, incluso si los usuarios no se mueven a Lync Online. Si no sincroniza todos los usuarios, puede ser que la comunicación entre los usuarios locales y en línea de su organización no funcione como se podría esperar.

<div>


> [!IMPORTANT]  
> Si el usuario se crea mediante el portal en línea para el Centro de administración de Microsoft 365, la cuenta de usuario no se sincronizará con Active Directory local y el usuario no existirá en el Active Directory local. Si ya ha creado usuarios en Lync Online y desea configurar la implementación híbrida con un Lync Server local, consulte Mover usuarios de Lync Online a Lync local en <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Lync Server 2013.</A>



</div>

También debe tener en cuenta los siguientes problemas relacionados con el usuario al planear una implementación híbrida.

  - **Contactos de usuario**   El límite de contactos para los usuarios de Lync Online es 250. Los contactos que supere ese número se quitarán de la lista de contactos del usuario cuando la cuenta se mueve a Lync Online.

  - **Mensajería instantánea y presencia**   Las listas de contactos de usuario, grupos y listas de control de acceso (ACL) se migran con la cuenta de usuario.

  - **Datos de conferencia, contenido de la reunión y reuniones programadas**   Este contenido no se migra con la cuenta de usuario. Los usuarios deben reprogramar reuniones después de migrar sus cuentas a Lync Online.

</div>

<div>

## <a name="user-policies-and-features"></a>Características y directivas de usuario

  - En un entorno híbrido de Lync Server 2013, los usuarios pueden habilitarse para mensajería instantánea, voz y reuniones locales o en línea, pero no ambas simultáneamente.

  - **Cliente de Lync**    Es posible que algunos usuarios necesiten una nueva versión de cliente cuando se mueven a Lync Online. Para Office Communications Server 2007 R2, los usuarios deben moverse a un grupo de servidores de Lync Server 2013 antes de la migración a Lync Online.
    
    Para obtener más información sobre el soporte técnico del cliente, vea Clientes [para Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) y clientes de Lync compatibles y [configuraciones de puerto de red.](https://go.microsoft.com/fwlink/p/?linkid=281901)

  - **Configuración y directivas locales (no usuario)**   Las directivas locales y en línea requieren una configuración independiente. No puede establecer directivas globales que se apliquen a ambos.

</div>

</div>

<span> </span>

</div>

</div>

</div>
