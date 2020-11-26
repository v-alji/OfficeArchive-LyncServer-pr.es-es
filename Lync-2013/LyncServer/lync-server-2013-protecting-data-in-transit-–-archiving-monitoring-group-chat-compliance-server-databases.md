---
title: 'Lync Server 2013: Proteger los datos en tránsito: bases de datos de servidor de archivado, supervisión y cumplimiento de chat en grupo'
description: 'Lync Server 2013: protección de datos en tránsito: archivar, supervisar, agrupar las bases de datos del servidor de cumplimiento de las conversaciones.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013
ms:assetid: ea219705-1015-43a7-890b-e7e67b451e7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518336(v=OCS.15)
ms:contentKeyID: 62625494
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: d4d4127bb0404bca376da450d0b0c58cf3b76560
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436849"
---
# <a name="protecting-data-in-transit--archiving-monitoring-group-chat-compliance-server-databases-in-lync-server-2013"></a>Proteger los datos en tránsito: bases de datos de servidor de archivado, supervisión y cumplimiento de chat en grupo en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-12-05_

El servidor de archivado y el servidor de supervisión de Microsoft Lync Server 2013 usan el servicio Message Queue Server (también conocido como MSMQ) para recopilar y mover mensajes de datos desde el punto de recopilación a los servidores del repositorio de forma confiable. El servicio de cumplimiento recopila datos junto con el servidor de chat de grupo, que también usa Message Queue Server.

En Lync Server 2013, no hay protección interna para los datos en el cable; sin embargo, si hay un requisito para proteger este tráfico, el servicio de Message Queue Server puede proporcionar cifrado a un nivel de mensaje en la cola de mensajes de envío. Esto se logra con certificados administrados por los servicios de dominio de Active Directory. Para obtener más información, vea el Apéndice D: Message Queue Server y comunicación por Internet en Windows Server 2008, en o en el [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) Apéndice I: Message Queue Server y comunicación por Internet en Windows server 2008 R2 en Windows [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) Server 2008 R2.

</div>

<span> </span>

</div>

</div>

</div>

