---
title: 'Lync Server 2013: Configuración de federación de Lync'
description: 'Lync Server 2013: Configurar la federación de Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399810"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a>Configuración de federación de Lync en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tema Última modificación:** 2014-03-27_

Si ya ha implementado servidores o servidores perimetrales, agregar las características de escenarios federados es un paso adelante. Si no ha configurado servidores perimetrales, primero debe hacerlo. Para obtener más información, vea: Planear el acceso de usuarios externos en [Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) en la documentación de planeamiento e implementar el acceso de usuario externo en [Lync Server 2013](lync-server-2013-deploying-external-user-access.md) en la documentación de implementación.

<div>


> [!NOTE]  
> Si tiene la intención de configurar cualquier combinación de federación XMPP, federación de Lync o conectividad de mensajería instantánea pública, puede implementarlas simultáneamente o de una en una. Si configura las opciones mediante el Generador de topologías y el shell de administración de Lync Server, ejecute el Asistente para la implementación en el servidor perimetral después de configurar las opciones para uno, dos o los tres tipos de federación, puede reducir el número de pasos necesarios.



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a>Configurar la federación de Lync en el Generador de topologías y el Asistente para la implementación

1.  En un servidor front-end, abra generador de topologías. Expanda Grupos perimetrales y, a continuación, haga clic con el botón derecho en el servidor perimetral o en el grupo de servidores perimetrales. Seleccione Editar propiedades.

2.  En Editar propiedades en General, seleccione Habilitar federación para este grupo de servidores perimetrales (Puerto 5061). Haga clic en Aceptar.

3.  Haga clic en Acción, seleccione Topología y publicar. Cuando se le solicite en Publicar la topología, haga clic en Siguiente. Cuando finalice la publicación, haga clic en Finalizar.

4.  En el servidor perimetral, abra el Asistente para la implementación de Lync Server. Haga clic en Instalar o actualizar Lync Server System y, a continuación, haga clic en Configurar o quitar componentes de Lync Server. Haga clic en Ejecutar de nuevo.

5.  En Configurar componentes de Lync Server, haga clic en Siguiente. La pantalla de resumen mostrará las acciones a medida que se ejecuten. Una vez que haya terminado la implementación, haga clic en Ver registro para ver los archivos de registro disponibles. Haga clic en Finalizar para completar la implementación.
    
    <div>
    

    > [!IMPORTANT]  
    > Puede seleccionar esta opción, pero solo un grupo perimetral o un servidor perimetral de su organización se pueden publicar externamente para la federación. Todos los accesos de usuarios federados, incluidos los usuarios de mensajería instantánea pública (MI), pasan por el mismo grupo perimetral o un único servidor perimetral. Por ejemplo, si la implementación incluye un grupo perimetral o un único servidor perimetral implementado en Nueva York y uno implementado en Londres y habilita el soporte de federación en el grupo perimetral de Nueva York o en un único servidor perimetral, el tráfico de señales para los usuarios federados pasará por el grupo perimetral de Nueva York o un único servidor perimetral. Esto es así incluso para las comunicaciones con usuarios de Londres, aunque un usuario interno de Londres que llame a un usuario federado de Londres usa el grupo de servidores o el servidor perimetral de Londres para el tráfico A/V.

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a>Configurar la federación con partners

1.  Para configurar una federación correcta con otro Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 u Office Communicator 2007, seleccione el tipo de federación de la tabla siguiente y defina registros SRV dns, host DNS (A o AAAA para IPv6) y configure directivas aplicables al tipo de federación:
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Tipo de federación</th>
    <th>Registros DNS</th>
    <th>Definición de directiva</th>
    <th>Notas</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Dominio de partner detectado</p></td>
    <td><p>Configure el registro SRV del formato _sipfederationtls._tcp. &lt; Nombre de dominio externo Donde el valor de puerto para el registro SRV es &gt; TCP 5061 y el <strong>host</strong> que ofrece este servicio se define como sip. &lt;nombre de dominio &gt; externo: el FQDN de su servicio perimetral de Access. Consulte <a href="lync-server-2013-configure-dns-for-edge-support.md">Configurar DNS para soporte técnico perimetral en Lync Server 2013</a> para obtener más información sobre cómo crear el registro SRV</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Habilitar o deshabilitar la detección de socios de federación en Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Las versiones anteriores hacían referencia a este tipo de federación como <strong>Federación mejorada abierta.</strong> La creación del registro SRV es necesaria para este tipo de federación y es para permitir que otros partners descubran su federación.</p></td>
    </tr>
    <tr class="even">
    <td><p>Dominio de partner permitido</p></td>
    <td><p>Configure el registro SRV del formato _sipfederationtls._tcp. &lt; Nombre de dominio externo Donde el valor de puerto para el registro SRV es &gt; TCP 5061 y el <strong>host</strong> que ofrece este servicio se define como sip. &lt;nombre de dominio &gt; externo: el FQDN de su servicio perimetral de Access. Consulte <a href="lync-server-2013-configure-dns-for-edge-support.md">Configurar DNS para soporte técnico perimetral en Lync Server 2013</a> para obtener más información sobre cómo crear el registro SRV</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Las versiones anteriores hacían referencia a este tipo de federación como <strong>Federación mejorada.</strong> La creación del registro SRV es opcional para este tipo de federación y permite que otros partners descubran su federación. Por supuesto, se trata de una federación <strong>mejorada abierta</strong>o un dominio de <strong>partner detectado</strong></p></td>
    </tr>
    <tr class="odd">
    <td><p>Servidor asociado permitido</p></td>
    <td><p>Configurar el nombre de dominio SIP y el FQDN del servidor perimetral asociado como partner de federación en Directivas</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configurar la compatibilidad con dominios externos permitidos en Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configurar la compatibilidad con dominios externos bloqueados en Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Este tipo de federación es la definición de una relación uno a uno y no permite la detección de otros partners de federación. Cada partner de federación se configura explícitamente. En versiones anteriores, esto se conocía como <strong>Federación directa</strong></p></td>
    </tr>
    <tr class="even">
    <td><p>Proveedor de hospedaje y proveedor público de mensajería instantánea</p></td>
    <td><p>No se definen requisitos DNS específicos para este tipo de federación</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Crear o editar proveedores federados de SIP públicos en Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Crear o editar proveedores federados de SIP hospedados en Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Este tipo de federación define los servicios y los proveedores de hospedaje que desea configurar para los usuarios. Los usos típicos incluyen la configuración para proveedores de mensajería instantánea públicos como Windows Live Messenger, Yahoo! y AOL, así como proveedores de hospedaje como Lync Online y Microsoft 365</p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P>A partir del 1 de septiembre de 2012, la licencia de suscripción de usuario de conectividad de mensajería instantánea pública de Microsoft Lync ("PIC USL") ya no está disponible para la compra de contratos nuevos o de renovación. Los clientes con licencias activas podrán seguir federados con Yahoo! Messenger hasta la fecha de cierre del servicio. Una fecha de fin de vida de junio de 2014 para AOL y Yahoo! se ha anunciado. Para obtener más información, vea <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Soporte para la conectividad de mensajería instantánea pública en Lync Server 2013.</A></P>
    > <LI>
    > <P>PIC USL es una licencia de suscripción por usuario y mes que se requiere para que Lync Server u Office Communications Server puedan federar con Yahoo! Messenger. La capacidad de Microsoft para proporcionar este servicio depende del soporte técnico de Yahoo!, cuyo contrato subyacente se está acabando.</P>
    > <LI>
    > <P>Más que nunca, Lync es una herramienta eficaz para conectarse entre organizaciones y con personas de todo el mundo. La federación con Windows Live Messenger no requiere licencias de usuario o dispositivo adicionales más allá de la CAL estándar de Lync. La federación de Skype se agregará a esta lista, lo que permitirá a los usuarios de Lync llegar a cientos de millones de personas con mensajería instantánea y voz.</P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  Definir y configurar cualquier host DNS necesario (A o AAAA para IPv6) y registros SRV DNS

3.  Defina y configure las directivas con el Panel de control de Lync Server o con el Shell de administración de Lync Server y los cmdlets adecuados. Para obtener más información sobre los cmdlets del Shell de administración de Lync Server, vea Cmdlets de federación y acceso [externo en Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)
    
    <div>
    

    > [!NOTE]  
    > Lync Room System (LRS) no muestra el botón unirse a las reuniones enviadas por los organizadores en partners federados de Lync. Para que un vínculo de unirse a una reunión aparezca en LRS, la organización de envío debe habilitar TNEF mediante el siguiente cmdlet:<BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR>Tenga en cuenta que esto no es específico de LRS. Outlook y Lync tampoco mostrarían vínculos de combinación en este caso, ya que las propiedades MAPI no se transportan, pero en el caso de Outlook, el usuario puede abrir la invitación a la reunión y hacer clic en la dirección URL de la reunión. Cuando TNEFEnabled se establece en true Exchange 2013 no quita las propiedades MAPI, incluido OnlineMeetingExternalLink y el botón Unirse se mostrará en el aviso.

    
    </div>

</div>

<div>

## <a name="see-also"></a>Vea también


[Planeación de sip, federación XMPP y mensajería instantánea pública en Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[Administración de la federación y el acceso externo a Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

