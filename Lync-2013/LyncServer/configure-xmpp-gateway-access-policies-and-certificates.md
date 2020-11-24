---
title: Configurar certificados y directivas de acceso por puerta de enlace XMPP
description: Configure certificados y directivas de acceso de puerta de enlace XMPP.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure XMPP gateway access policies and certificates
ms:assetid: fac02f4e-d14d-4be3-b53c-74c82436fd93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721945(v=OCS.15)
ms:contentKeyID: 49733882
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e958100501ad9ca87d1ab970162f4be8c7692a99
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398357"
---
# <a name="configure-xmpp-gateway-access-policies-and-certificates"></a>Configurar certificados y directivas de acceso por puerta de enlace XMPP

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-15_

La Federación XMPP define una implementación externa basada en el protocolo de presencia y mensajería extensible (XMPP). Una configuración XMPP permite a los usuarios de Lync acceder a los usuarios del dominio XMPP de la siguiente manera:

  - Mensajería instantánea y presencia: solo para personas

  - Creación de los contactos de XMPP federados en el cliente de Lync

Al configurar directivas para la compatibilidad de los socios federados protocolo de presencia y mensajería extensible (XMPP), las directivas se aplican a los usuarios de XMPP Federated Domains, pero no a los usuarios de proveedores de servicios de mensajería instantánea (mi) o de protocolo de inicio de sesión (por ejemplo, Windows Live) ni a los dominios federados de SIP. Configure un socio de XMPP federado para cada dominio de XMPP federado que desee permitir a los usuarios que añadan contactos y se comuniquen con ellos. Una vez que las directivas estén en vigor, tendrá que configurar los certificados de la puerta de enlace XMPP.

<div>


> [!NOTE]  
> Para comenzar la migración de la puerta de enlace XMPP, debe implementar la puerta de enlace 2013 XMPP de Lync Server y configurar directivas de acceso para habilitar usuarios para la puerta de enlace XMPP de Lync Server 2013. Debe mover todos los usuarios a la implementación de Lync Server 2013 antes de realizar estos pasos. Para obtener más información, consulte <A href="configure-xmpp-gateway-on-lync-server-2013.md">configurar la puerta de enlace XMPP en Lync Server 2013</A>.



</div>

<div>

## <a name="configure-an-external-access-policy-to-enable-users-for-lync-server-2013-xmpp-gateway"></a>Configurar una directiva de acceso externo para habilitar usuarios en la puerta de enlace de Lync Server 2013 XMPP

1.  Abra el Panel de control de Lync Server.

2.  En la barra de navegación izquierda, haga clic en **Federación y acceso externo** y, después, haga clic en **Directiva de acceso externo**.

3.  Haga clic en **nuevo** y, a continuación, en **Directiva de usuario**.

4.  Escriba un nombre para la Directiva de usuario de acceso externo.

5.  Proporcione una descripción para la Directiva de usuario de acceso externo.

6.  Seleccione **Habilitar comunicaciones con usuarios federados**.

7.  Seleccione **Habilitar comunicaciones con usuarios federados de XMPP**.

8.  Haga clic en **confirmar** para guardar los cambios en el sitio o en la Directiva de usuario.

</div>

</div>

<span> </span>

</div>

</div>

</div>

