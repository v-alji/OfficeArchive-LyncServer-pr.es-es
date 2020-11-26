---
title: 'Lync Server 2013: Crear registros DNS para servidores de proxy inverso'
description: 'Lync Server 2013: crear registros DNS para servidores proxy inversos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create DNS records for reverse proxy servers
ms:assetid: b3513339-e49b-4665-80f1-b5a1c81a0e2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429719(v=OCS.15)
ms:contentKeyID: 48185181
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef785ebbd7160274b631a2d2b6b1f1dcc866e5fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431949"
---
# <a name="create-dns-records-for-reverse-proxy-servers-in-lync-server-2013"></a>Crear registros DNS para servidores de proxy inverso en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-03-29_

Crear registros DNS A externos que apunten a la interfaz externa pública de Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1, Forefront Threat Management Gateway 2010 Server o solicitud enrutamiento de Internet Information Server, como se describe en [configurar la compatibilidad con DNS para Edge en Lync Server 2013](lync-server-2013-configure-dns-for-edge-support.md). Necesita registros DNS para los FQDN de servicio Web externo para cada grupo, el director (o grupo de directores) y cada dirección URL simple.

Los registros DNS mínimos para la resolución del cliente en el proxy inverso, se deben crear los siguientes registros:

  - Registros de host (A) que definen los servicios web externos publicados para los grupos de directores y directores (por ejemplo, **webdirext.contoso.com**)

  - Registros de host (A) que definen los servicios web externos publicados para servicios web externos hospedados en cualquier grupo de servidores front-end y roles de servidor Standard Edition (por ejemplo, **webext.contoso.com**)

  - Registros de host (A) para las direcciones URL simples (por ejemplo, **Dialin.contoso.com** y **meet.contoso.com**)

  - Registro host (A) para el registro externo Discover de Lync y también proporciona un puntero a Autodiscover para todas las aplicaciones Web, incluidos Lync Web App, programador y movilidad (por ejemplo, **lyncdiscover.contoso.com**)

  - Registros de host (A) para la dirección URL de Office Web Apps Server (por ejemplo, **officewebapp01.contoso.com**)

Para obtener más información, consulte [Resumen de DNS-proxy inverso en Lync Server 2013](lync-server-2013-dns-summary-reverse-proxy.md).

</div>

<span> </span>

</div>

</div>

</div>

