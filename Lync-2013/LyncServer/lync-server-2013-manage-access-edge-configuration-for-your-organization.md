---
title: 'Lync Server 2013: Administrar la configuración perimetral de acceso para su organización'
description: 'Lync Server 2013: administrar la configuración perimetral de acceso de su organización.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage Access Edge Configuration for your organization
ms:assetid: 0145eb08-984f-4ecd-bf9c-364817619c2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552443(v=OCS.15)
ms:contentKeyID: 48679555
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2161385f9c03f025bcf6f5e599b7e0276f6d592c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426140"
---
# <a name="manage-access-edge-configuration-for-your-organization-in-lync-server-2013"></a>Administrar la configuración perimetral de acceso para su organización en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-11-01_

Esta documentación es preliminar y está sujeta a cambios. Los temas en blanco que se incluyen actúan como marcadores de posición.

Después de implementar uno o varios servidores perimetrales, debe habilitar el acceso de los tipos de dominios externos o proveedores, el acceso de usuarios remotos y el acceso de usuarios anónimos a las conferencias a través de los servidores perimetrales que serán compatibles con su organización.

Estas opciones incluyen los siguientes tipos de acceso que se pueden configurar a través de la página **configuración de Edge de Access** :

  - **Habilitar la Federación y la conectividad de mensajería instantánea pública**   Habilite esta opción si desea admitir el acceso de los usuarios a dominios federados. Esta configuración se aplica a la Federación de SIP y a la Federación de XMPP que están configuradas para los ámbitos globales, de sitio o de usuario en la página de la **Directiva de acceso externo** . Para que se aplique la configuración de Federación, debe configurar la compatibilidad de Federación en ambas páginas.
    
    Existen dos opciones opcionales para conocer el modo en que se descubren los socios federados y si archivar descargos de responsabilidad (la notificación a los contactos federados con los que se comunica la implementación tiene habilitado el archivado y se enviarán los detalles de las comunicaciones) a los contactos
    
      - **Habilitar detección de dominios del socio**   Al seleccionar esta opción, se habilita la detección automática de dominios con los que se puede federar. Lync Server 2013 usa registros del sistema de nombres de dominio (DNS) para intentar descubrir dominios no incluidos en la lista de dominios permitidos, evaluar automáticamente el tráfico entrante de socios federados descubiertos y limitar o bloquear ese tráfico en función del nivel de confianza, la cantidad de tráfico y la configuración del administrador. Si no selecciona esta opción, acceso de usuarios federados solo se habilitará para los usuarios de los dominios que incluya en la lista de dominios permitidos. Independientemente de si selecciona esta opción, puede especificar que los dominios individuales se bloqueen o se permitan, incluido el acceso restringido a servidores específicos que ejecuten el servicio perimetral de acceso en el dominio federado. Para obtener más información, vea [configurar la compatibilidad de dominios externos permitidos en Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).
    
      - **Enviar renuncia de archivado a socios federados**   Al seleccionar esta opción, el envío de un mensaje de renuncia de archivado a los socios federados le informa de que se registran los detalles de la comunicación. Si archiva comunicaciones externas con dominios federados de socios federados, debe habilitar la notificación de renuncia de archivado para avisar a los socios de que su implementación ha archivado sus mensajes y sus detalles de comunicaciones. Para obtener más información sobre el archivado, vea [definir los requisitos para el archivado en Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md).

  - **Habilitar el acceso de usuarios remotos**   Habilite esta opción si quiere que los usuarios de su organización que estén fuera del firewall, como teletrabajadores y usuarios que viajan, puedan conectarse a Lync Server. Para obtener más información, vea [habilitar o deshabilitar el acceso de usuarios remotos en Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).

  - **Permitir que los usuarios anónimos tengan acceso a conferencias**   Habilite esta opción si desea que los usuarios internos inviten a usuarios anónimos externos a conferencias que organizan. Habilitar esta opción solo permite usuarios anónimos en conferencias. Para configurar la experiencia de conferencia y las opciones que definen cómo y qué pueden hacer los usuarios con las conferencias y para la inclusión de usuarios anónimos, vea detalles en [crear o modificar la experiencia de usuario de conferencias para un sitio o una](https://technet.microsoft.com/library/gg429715\(v=ocs.15\)) [referencia de configuración de directiva de usuarios y conferencias para Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).

<div>


> [!NOTE]  
> Además de habilitar la compatibilidad con el acceso de usuarios externos, también puede configurar directivas para controlar el uso del acceso de usuarios remotos de su organización antes de que los usuarios puedan tener acceso a cualquier tipo de acceso de usuario externo. Para obtener más información sobre cómo crear, configurar y aplicar directivas para el acceso de usuarios externos, vea <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">administrar la Directiva de acceso externo en Lync Server 2013</A>.



</div>

**Ver la información de configuración perimetral de acceso mediante cmdlets de Windows PowerShell**

  - La información de configuración perimetral de acceso se puede ver con Windows PowerShell y el cmdlet **Get-CsAccessEdgeConfiguration** . Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell. Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .
    
    Para ver información sobre todas las opciones de configuración de los límites de acceso, escriba el siguiente comando en el shell de administración de Lync Server y, a continuación, presione ENTRAR:
    
        Get-CsAccessEdgeConfiguration
    
    Devolverá información similar a la siguiente:
    
        Identity                               : Global
        AllowAnonymousUsers                    : False
        AllowFederatedUsers                    : False
        AllowOutsideUsers                      : True
        BeClearingHouse                        : False
        EnablePartnerDiscovery                 : False
        EnableArchivingDisclaimer              : False
        EnableUserReplicator                   : True
        KeepCrlsUpToDateForPeers               : True
        MarkSourceVerifiableOnOutgoingMessages : True
        OutgoingTlsCountForFederatedPartners   : 4
        DiscoveredPartnerStandardRate          : 20
        EnableDiscoveredPartnerContactsLimit   : True
        MaxContactsPerDiscoveredPartner        : 1000
        DiscoveredPartnerReportPeriodMinutes   : 60
        MaxAcceptedCertificatesStored          : 1000
        MaxRejectedCertificatesStored          : 500
        CertificatesDeletedPercentage          : 20
        RoutingMethod                          : UseDnsSrvRouting

<div>

## <a name="in-this-section"></a>En esta sección

  - [Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)

  - [Habilitar o deshabilitar la detección de socios de federación en Lync Server 2013](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md)

  - [Habilitar o deshabilitar el envío de una renuncia de archivado a socios federados en Lync Server 2013](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md)

  - [Habilitar y deshabilitar el acceso de usuarios remotos en Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md)

  - [Habilitar y deshabilitar el acceso anónimo de usuarios en Lync Server 2013](lync-server-2013-enable-or-disable-anonymous-user-access.md)

  - [Asignar directivas de conferencia para admitir usuarios anónimos en Lync Server 2013](lync-server-2013-assign-conferencing-policies-to-support-anonymous-users.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

