---
title: 'Lync Server 2013: Requisitos de la infraestructura de certificados'
description: Requisitos de la infraestructura de certificados de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate infrastructure requirements
ms:assetid: 0051aa23-0bbe-4e72-9f29-e01c6bcc6190
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398066(v=OCS.15)
ms:contentKeyID: 48183219
ms.date: 06/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02c7e69f272c29f0ba9386f403db326b4d39bbff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435414"
---
# <a name="certificate-infrastructure-requirements-for-lync-server-2013"></a>Requisitos de la infraestructura de certificados para Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2016-06-23_

Lync Server 2013 requiere una infraestructura de clave pública (PKI) para que sea compatible con las conexiones TLS y Mutual TLS (MTLS).

Lync Server usa certificados para los siguientes fines:

  - Conexiones TLS entre el cliente y el servidor

  - Conexiones MTLS entre servidores

  - Federación mediante la detección automática de asociados de DNS

  - Acceso de usuarios remotos a la mensajería instantánea (MI)

  - Acceso de usuarios externos a sesiones de audio/vídeo (A/V), uso compartido de aplicaciones y conferencias

  - Solicitudes de teléfono móvil con el descubrimiento automático de servicios Web

Para Lync Server, se aplican los siguientes requisitos comunes:

  - Todos los certificados de servidor deben admitir la autorización de servidor (EKU de servidor).

  - Todos los certificados de servidor deben contener un punto de distribución CRL (CDP).

  - Todos los certificados deben estar firmados mediante un algoritmo de firma compatible con el sistema operativo. Lync Server 2013 admite el conjunto de tamaños de compendio SHA-1 y SHA-2 (224, 256, 384 y 512 bits), y cumple o supera los requisitos del sistema operativo. Para obtener asistencia sobre el sistema operativo, consulte [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002) .
    
    <div>
    

    > [!NOTE]  
    > No está permitido usar el algoritmo de firma RSASSA-PSS, ya que podría dar lugar a errores en problemas relacionados con el inicio de sesión y el desvío de llamadas, entre otros. 

    
    </div>

  - La inscripción automática es compatible con los servidores internos que ejecutan Lync Server.

  - La inscripción automática no es compatible con los servidores perimetrales de Lync Server.

  - Al enviar una solicitud de certificado basada en Web a una CA de Windows Server 2003, debe enviarla desde un equipo con Windows Server 2003 con SP2 o Windows XP.
    
    Tenga en cuenta que, aunque KB922706 ofrece compatibilidad para resolver problemas con la inscripción de certificados Web en una inscripción Web de servicios de Certificate Server de Windows Server 2003, no permite usar Windows Server 2008, Windows Vista o Windows 7 para solicitar un certificado a una CA de Windows Server 2003.

  - Se admiten longitudes de clave de cifrado de 1024, 2048 y 4096. Se recomienda usar longitudes de clave de 2048 y superiores.

  - El algoritmo de firma hash o implícito predeterminado es RSA. \_ \_ \_ También se admiten los algoritmos P256, ECDH P384 y P521 ECDH. 

<div>

## <a name="in-this-section"></a>En esta sección

  - [Requisitos de certificado para Servidores internos en Lync Server 2013](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [Requisitos de certificado para el acceso de usuarios externos en Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [Requisitos de certificados para el servidor de chat persistente en Lync Server 2013](lync-server-2013-certificate-requirements-for-persistent-chat-server.md)

  - [Requisitos de certificado para movilidad en Lync Server 2013](lync-server-2013-certificate-requirements-for-mobility.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

