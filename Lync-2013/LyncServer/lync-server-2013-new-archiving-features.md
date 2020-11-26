---
title: 'Lync Server 2013: Nuevas características de archivado'
description: 'Lync Server 2013: nuevas características de archivado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Archiving features
ms:assetid: c002e367-41ad-498d-9d23-8b117ac435b2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205225(v=OCS.15)
ms:contentKeyID: 48185288
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5b69c90e62914284f178ae328375c6e350f5b3e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425167"
---
# <a name="new-archiving-features-in-lync-server-2013"></a><span data-ttu-id="74646-103">Nuevas características de archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74646-103">New Archiving features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="74646-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="74646-104">

<span> </span></span></span>

<span data-ttu-id="74646-105">_**Última modificación del tema:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="74646-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="74646-106">El archivado en Lync Server 2013 puede archivar los siguientes tipos de contenido:</span><span class="sxs-lookup"><span data-stu-id="74646-106">Archiving in Lync Server 2013 can archive the following types of content:</span></span>

  - <span data-ttu-id="74646-107">Mensajes instantáneos de punto a punto</span><span class="sxs-lookup"><span data-stu-id="74646-107">Peer-to-peer instant messages</span></span>

  - <span data-ttu-id="74646-108">Conferencias (reuniones) que son mensajes instantáneos de varios participantes</span><span class="sxs-lookup"><span data-stu-id="74646-108">Conferences (meetings) that are multi-party instant messages</span></span>

  - <span data-ttu-id="74646-109">Contenido de conferencias, como contenido que se carga (por ejemplo, documentos de la reunión) y contenido relacionado con el evento (por ejemplo, los usuarios que se unen o abandonan el evento, la carga de recursos compartidos y los cambios en la visibilidad)</span><span class="sxs-lookup"><span data-stu-id="74646-109">Conference content, including uploaded content (for example, handouts) and event-related content (for example, joining, leaving, uploading sharing, and changes in visibility)</span></span>

<span data-ttu-id="74646-110">Además, el archivado en Lync Server 2013 ofrece nuevas características que mejoran la implementación y la eficacia de las operaciones.</span><span class="sxs-lookup"><span data-stu-id="74646-110">Additionally, Archiving in Lync Server 2013 provides new features that improve deployment and operations efficiency.</span></span> <span data-ttu-id="74646-111">Estas nuevas características constan de:</span><span class="sxs-lookup"><span data-stu-id="74646-111">These new features consist of:</span></span>

  - <span data-ttu-id="74646-112">**Collocation de archivo en los servidores frontales.**</span><span class="sxs-lookup"><span data-stu-id="74646-112">**Collocation of Archiving on Front End Servers.**</span></span>   <span data-ttu-id="74646-113">Lync Server 2013 no tiene un rol de servidor de archivado independiente.</span><span class="sxs-lookup"><span data-stu-id="74646-113">Lync Server 2013 does not have a separate Archiving Server role.</span></span> <span data-ttu-id="74646-114">El archivado es una característica opcional disponible en todos los servidores front-end de una implementación de Enterprise Edition, y en servidores Standard Edition, que se puede implementar en un grupo o sitio.</span><span class="sxs-lookup"><span data-stu-id="74646-114">Archiving is an optional feature available on all Front End Servers in an Enterprise Edition deployment, and on Standard Edition servers, that can be implemented configured for a pool or a site.</span></span>

  - <span data-ttu-id="74646-115">**Integración con Microsoft Exchange.**</span><span class="sxs-lookup"><span data-stu-id="74646-115">**Microsoft Exchange integration.**</span></span>   <span data-ttu-id="74646-116">Al implementar el archivado, puede integrar el almacenamiento de datos para archivar con el almacenamiento de Exchange 2013 existente para todos los usuarios que estén alojados en Exchange 2013 y que sus buzones se pongan en espera In-Place, por lo que no es necesario implementar bases de datos de SQL Server independientes para archivar datos de Lync.</span><span class="sxs-lookup"><span data-stu-id="74646-116">When you deploy Archiving, you can integrate data storage for Archiving with your existing Exchange 2013 storage for all users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold, so you don’t need to deploy separate SQL Server databases to archive Lync data.</span></span> <span data-ttu-id="74646-117">Si no tiene una implementación de Exchange 2013, o si prefiere no integrarlo, o si tiene usuarios de Lync 2013 que no están alojados en Exchange 2013 con sus buzones puestos en In-Place, puede implementar bases de datos de archivado independientes mediante SQL Server para almacenar datos archivados de las comunicaciones de Lync.</span><span class="sxs-lookup"><span data-stu-id="74646-117">If you do not have an Exchange 2013 deployment, or if you prefer not to integrate with it, or if you have any Lync 2013 users who are not homed on Exchange 2013 with their mailboxes put on In-Place Hold, you can deploy separate Archiving databases by using SQL Server to store archived data from Lync communications.</span></span> <span data-ttu-id="74646-118">Puede usar las bases de datos de integración de Microsoft Exchange y de archivo de Lync Server 2013 si desea usar la integración de Microsoft Exchange para algunos, pero no todos los usuarios de su implementación.</span><span class="sxs-lookup"><span data-stu-id="74646-118">You can use both Microsoft Exchange integration and Lync Server 2013 Archiving databases if you want to use Microsoft Exchange integration for some but not all users in your deployment.</span></span> <span data-ttu-id="74646-119">Para obtener más información sobre la suspensión de In-Place, vea "conservación local" en [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500) .</span><span class="sxs-lookup"><span data-stu-id="74646-119">For details about In-Place Hold, see “In-Place Hold” at [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500).</span></span>

  - <span data-ttu-id="74646-120">**Reflejo de la tienda SQL.**</span><span class="sxs-lookup"><span data-stu-id="74646-120">**SQL Store Mirroring.**</span></span>   <span data-ttu-id="74646-121">Al implementar el archivado, puede habilitar la creación de reflejo de la base de datos de SQL Server para la base de datos de archivado.</span><span class="sxs-lookup"><span data-stu-id="74646-121">When you deploy Archiving, you can enable SQL Server database mirroring for your Archiving database.</span></span>

  - <span data-ttu-id="74646-122">**Archivo de pizarras y sondeos.**</span><span class="sxs-lookup"><span data-stu-id="74646-122">**Archiving of Whiteboards and Polls.**</span></span>   <span data-ttu-id="74646-123">El contenido de conferencia archivado ahora incluye pizarras y sondeos compartidos durante la reunión.</span><span class="sxs-lookup"><span data-stu-id="74646-123">Archived conference content now includes whiteboards and polls that are shared during the meeting.</span></span>

<span data-ttu-id="74646-124">Los siguientes tipos de contenido no se archivan:</span><span class="sxs-lookup"><span data-stu-id="74646-124">The following types of content are not archived:</span></span>

  - <span data-ttu-id="74646-125">Transferencias de archivos de punto a punto</span><span class="sxs-lookup"><span data-stu-id="74646-125">Peer-to-peer file transfers</span></span>

  - <span data-ttu-id="74646-126">Audio o vídeo para conferencias y mensajes instantáneos de punto a punto</span><span class="sxs-lookup"><span data-stu-id="74646-126">Audio/video for peer-to-peer instant messages and conferences</span></span>

  - <span data-ttu-id="74646-127">Uso compartido de aplicaciones para conferencias y mensajes instantáneos de punto a punto</span><span class="sxs-lookup"><span data-stu-id="74646-127">Application sharing for peer-to-peer instant messages and conferences</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="74646-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="74646-128">See Also</span></span>


[<span data-ttu-id="74646-129">Planificar el archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74646-129">Planning for Archiving in Lync Server 2013</span></span>](lync-server-2013-planning-for-archiving.md)  
  

<span data-ttu-id="74646-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="74646-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

