---
title: Actualizar registros SRV de DNS
description: Actualizar registros SRV de DNS.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Update DNS SRV records
ms:assetid: 9542b91a-108c-4980-89ec-634905cbbf26
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688139(v=OCS.15)
ms:contentKeyID: 49733739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24161074e8f3bcf7e296a957588eeb59d5f2ad1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446552"
---
# <a name="update-dns-srv-records"></a>Actualizar registros SRV de DNS

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-09-29_

Para completar correctamente este procedimiento, debe haber iniciado sesión en el servidor o dominio como miembro del grupo administradores de dominio o miembro del grupo DnsAdmins.

En este tema se describe cómo actualizar los registros del sistema de nombres de dominio (DNS) después de migrar a Lync Server 2013. Después de que todos los usuarios se hayan movido a Lync Server 2013, pero antes de que se haya retirado el grupo o el director heredado de Lync Server 2010, debe actualizar los registros SRV de DNS en el DNS interno para cada dominio SIP. En este procedimiento se supone que su DNS interno tiene zonas para sus dominios de usuario SIP.

**Para configurar un registro SRV de DNS**

1.  En el servidor DNS, haga clic en **Inicio**, haga clic en **herramientas administrativas** y, a continuación, haga clic en **DNS**.

2.  En el árbol de consola de su dominio SIP, expanda **zonas de búsqueda directa**, expanda el dominio SIP en el que está instalado Lync Server 2013 y vaya a la configuración de **\_ TCP** .

3.  En el panel derecho, haga clic con el botón derecho en **\_ sipinternaltls** y seleccione **propiedades**.

4.  En el **hospedaje que ofrece este servicio**, actualice el FQDN del host para que apunte al grupo de servidores de Lync Server 2013.

5.  Haga clic en **Aceptar**.

**Para comprobar que se puede resolver el FQDN del grupo de servidores front-end o del servidor Standard Edition**

1.  Inicie sesión en un equipo cliente del dominio.

2.  Haga clic en  **Inicio** y en  **Ejecutar**.

3.  En el cuadro **abrir** , escriba **cmd** y haga clic en **Aceptar**.

4.  En el símbolo del sistema, escriba **nslookup** \<FQDN of the Front End pool\> o \<FQDN of the Standard Edition server\> , y, a continuación, presione Entrar.

5.  Compruebe que recibe una respuesta que se resuelve en la dirección IP adecuada para el nombre de dominio completo (FQDN).

</div>

<span> </span>

</div>

</div>

</div>

