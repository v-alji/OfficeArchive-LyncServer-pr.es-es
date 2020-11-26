---
title: 'Lync Server 2013: ejecutar Lync Server en servidores virtuales'
description: 'Lync Server 2013: ejecutar Lync Server en servidores virtuales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running Lync Server on virtual servers
ms:assetid: e83c0f7f-88ec-434f-b35e-adedec3c318a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399035(v=OCS.15)
ms:contentKeyID: 49733856
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 377c481ac149f556fc950a29a0c5054097f3b0e2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442204"
---
# <a name="running-lync-server-2013-on-virtual-servers"></a><span data-ttu-id="c58c2-103">Ejecutar Lync Server 2013 en servidores virtuales</span><span class="sxs-lookup"><span data-stu-id="c58c2-103">Running Lync Server 2013 on virtual servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c58c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c58c2-104">

<span> </span></span></span>

<span data-ttu-id="c58c2-105">_**Última modificación del tema:** 2014-03-13_</span><span class="sxs-lookup"><span data-stu-id="c58c2-105">_**Topic Last Modified:** 2014-03-13_</span></span>

<span data-ttu-id="c58c2-106">Lync Server 2013 admite topologías de virtualización que admiten todas las cargas de trabajo de Lync Server, incluidas la mensajería instantánea (mi) y la presencia, Conferencia, voz empresarial, supervisión, archivado y chat persistente.</span><span class="sxs-lookup"><span data-stu-id="c58c2-106">Lync Server 2013 supports virtualization topologies that support all Lync Server workloads, including instant messaging (IM) and presence, conferencing, Enterprise Voice, Monitoring, Archiving, and Persistent Chat.</span></span> <span data-ttu-id="c58c2-107">Tenga en cuenta que el rendimiento de Lync Server en topologías virtuales puede variar en gran medida según las cargas de trabajo que se usan, el número de usuarios y el hardware del host.</span><span class="sxs-lookup"><span data-stu-id="c58c2-107">Note that Lync Server performance on virtual topologies can vary greatly depending on the workloads being used, the number of users, and the host hardware.</span></span> <span data-ttu-id="c58c2-108">Para obtener instrucciones detalladas sobre cómo ejecutar Lync Server 2013 en servidores virtuales, consulte las notas del producto [planear una implementación de Lync server 2013 en servidores virtuales](https://www.microsoft.com/download/details.aspx?id=41936).</span><span class="sxs-lookup"><span data-stu-id="c58c2-108">For detailed guidance about running Lync Server 2013 on virtual servers, see the white paper [Planning a Lync Server 2013 Deployment on Virtual Servers](https://www.microsoft.com/download/details.aspx?id=41936).</span></span>

<span data-ttu-id="c58c2-109">Lync Server 2013 es compatible con la plataforma Hyper-V y en cualquier plataforma de virtualización que sea compatible con el programa de validación de virtualización de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c58c2-109">Lync Server 2013 is supported on the Hyper-V platform, and on any virtualization platform that is supported under the Windows Server Virtualization Validation Program.</span></span> <span data-ttu-id="c58c2-110">Para obtener más información sobre este programa, consulte <http://www.windowsservercatalog.com/svvp.aspx> .</span><span class="sxs-lookup"><span data-stu-id="c58c2-110">For information on this program, see <http://www.windowsservercatalog.com/svvp.aspx>.</span></span>

<div id="sectionSection0" class="section">

</div><span data-ttu-id="c58c2-111">

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c58c2-111">

</div>

<span> </span>

</div>

</div>

</span></span></div>

