---
title: 'Lync Server 2013: Realizar la migración de usuarios a almacén de contactos unificados'
description: 'Lync Server 2013: migración de usuarios a almacenamiento de contactos unificado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migrate users to unified contact store
ms:assetid: 215a8ec1-d63e-4fdf-b73d-75aeb9dddb43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204737(v=OCS.15)
ms:contentKeyID: 48183600
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e9ee9850cc723ae132f15d7c0c6b3769e1240ba
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425594"
---
# <a name="migrate-users-to-unified-contact-store-in-lync-server-2013"></a>Realizar la migración de usuarios a almacén de contactos unificados en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-15_

Los contactos de un usuario se migran automáticamente al servidor de Exchange 2013 cuando el usuario:

  - Tiene asignado una directiva de servicios de usuario que tiene UcsAllowed configurado en True.

  - Se aprovisionó con un buzón de Exchange 2013 y ha iniciado sesión en el buzón al menos una vez.

  - Inicia sesión con un cliente enriquecido de Lync 2013.

Si el usuario inicia sesión con un cliente de Lync 2010 o una versión anterior, o si el usuario no está conectado a un servidor de Exchange 2013, se ignora la Directiva de servicios de usuario y los contactos del usuario permanecen en Lync Server.

Puede determinar si se han migrado los contactos de un usuario usando uno de los métodos siguientes:

  - Compruebe la siguiente clave del registro en el equipo cliente:
    
    HKEY \_ Current \_ User \\ software \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ \<SIP URL\> \\ UCS
    
    Si los contactos del usuario se almacenan en Exchange 2013, esta clave contiene un valor de InUCSMode con un valor de 2165.

  - Ejecute el cmdlet **Test-CsUnifiedContactStore**. En la línea de comandos del shell de administración de Lync Server, escriba:
    
        Test-CsUnifiedContactStore -UserSipAddress "sip:kenmyer@litwareinc.com" -TargetFqdn "atl-cs-001.litwareinc.com"
    
    Si el cmdlet **Test-CsUnifiedContactStore** se lleva a cabo con éxito, quiere decir que los contactos del usuario se han migrado al almacén de contactos unificado.

</div>

<span> </span>

</div>

</div>

</div>

