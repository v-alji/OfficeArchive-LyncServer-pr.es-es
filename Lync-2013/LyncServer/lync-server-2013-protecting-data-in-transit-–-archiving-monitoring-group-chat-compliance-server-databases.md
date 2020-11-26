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
# <a name="protecting-data-in-transit--archiving-monitoring-group-chat-compliance-server-databases-in-lync-server-2013"></a><span data-ttu-id="ed629-103">Proteger los datos en tránsito: bases de datos de servidor de archivado, supervisión y cumplimiento de chat en grupo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ed629-103">Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ed629-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ed629-104">

<span> </span></span></span>

<span data-ttu-id="ed629-105">_**Última modificación del tema:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="ed629-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="ed629-106">El servidor de archivado y el servidor de supervisión de Microsoft Lync Server 2013 usan el servicio Message Queue Server (también conocido como MSMQ) para recopilar y mover mensajes de datos desde el punto de recopilación a los servidores del repositorio de forma confiable.</span><span class="sxs-lookup"><span data-stu-id="ed629-106">Microsoft Lync Server 2013 Archiving Server and Monitoring Server both use the Message Queuing (also known as MSMQ) service to collect and reliably move data messages from the collection point to the repository servers.</span></span> <span data-ttu-id="ed629-107">El servicio de cumplimiento recopila datos junto con el servidor de chat de grupo, que también usa Message Queue Server.</span><span class="sxs-lookup"><span data-stu-id="ed629-107">Compliance service collects data in conjunction with the Group Chat Server, which also uses Message Queuing.</span></span>

<span data-ttu-id="ed629-108">En Lync Server 2013, no hay protección interna para los datos en el cable; sin embargo, si hay un requisito para proteger este tráfico, el servicio de Message Queue Server puede proporcionar cifrado a un nivel de mensaje en la cola de mensajes de envío.</span><span class="sxs-lookup"><span data-stu-id="ed629-108">In Lync Server 2013, there is no internal protection for data on the wire; however, if there is a requirement to secure this traffic, the Message Queuing service can provide encryption at a message level on the sending message queue.</span></span> <span data-ttu-id="ed629-109">Esto se logra con certificados administrados por los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ed629-109">This is accomplished using certificates that are managed by the Active Directory Domain Services.</span></span> <span data-ttu-id="ed629-110">Para obtener más información, vea el Apéndice D: Message Queue Server y comunicación por Internet en Windows Server 2008, en o en el [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) Apéndice I: Message Queue Server y comunicación por Internet en Windows server 2008 R2 en Windows [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed629-110">For details, see Appendix D: Message Queuing and Internet Communication in Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) or Appendix I: Message Queuing and Internet Communication in Windows Server 2008 R2 at [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) for Windows Server 2008 R2.</span></span>

<span data-ttu-id="ed629-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ed629-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

