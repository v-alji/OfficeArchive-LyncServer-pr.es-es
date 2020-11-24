---
title: Configurar registros DNS para una implementación de grupo de servidores piloto
description: Configure los registros DNS para la implementación del grupo piloto.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS records for pilot pool deployment
ms:assetid: eb421bad-4bf1-4837-a077-7795094692d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721921(v=OCS.15)
ms:contentKeyID: 49733855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e41e163432ba910f6d083cc508e8ad8c9f2006d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398873"
---
# <a name="configure-dns-records-for-pilot-pool-deployment"></a>Configurar registros DNS para una implementación de grupo de servidores piloto

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-09-29_

Antes de implementar el grupo piloto de Lync Server 2013, debe actualizar las entradas de host DNS A para la agrupación piloto. Para completar correctamente este procedimiento, debe haber iniciado sesión en el servidor o dominio como miembro del grupo administradores de dominio o miembro del grupo DnsAdmins.

**Para configurar registros A de host DNS**

1.  En el servidor del sistema de nombres de dominio (DNS), haga clic en **Inicio**, en **herramientas administrativas** y, por último, en **DNS**.

2.  En el árbol de consola de su dominio, expanda **zonas de búsqueda directa** y haga clic con el botón secundario en el dominio en el que se instalará Lync Server 2013.

3.  Haga clic en **nuevo host (A o aaaa)**.

4.  Haga clic en **nombre**, escriba el nombre de host para el grupo de servidores de Lync Server 2013 (el nombre de dominio se supone de la zona en la que está definido el registro y no tiene que especificarse como parte del registro A).

5.  Haga clic en **dirección IP** y escriba la dirección IP del grupo de servidores front-end.

6.  Haga clic en **Agregar host** y, a continuación, en **Aceptar**.

7.  Cuando haya terminado, haga clic en **listo**.

</div>

<span> </span>

</div>

</div>

</div>

