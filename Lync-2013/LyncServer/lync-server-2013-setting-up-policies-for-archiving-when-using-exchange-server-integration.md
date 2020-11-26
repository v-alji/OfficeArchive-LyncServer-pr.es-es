---
title: Configurar directivas para archivar al usar la integración de Exchange Server
description: Configurar directivas para archivar al utilizar la integración de Exchange Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up policies for Archiving when using Exchange Server integration
ms:assetid: 8b9b2bad-a4b3-42e1-85a7-04022e9442ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205063(v=OCS.15)
ms:contentKeyID: 48184742
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8281d27101c049b1029a2005ed062a934438afc5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444724"
---
# <a name="setting-up-policies-for-archiving-in-lync-server-2013-when-using-exchange-server-integration"></a><span data-ttu-id="573f0-103">Configurar directivas para archivar en Lync Server 2013 al usar la integración de Exchange Server</span><span class="sxs-lookup"><span data-stu-id="573f0-103">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="573f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="573f0-104">

<span> </span></span></span>

<span data-ttu-id="573f0-105">_**Última modificación del tema:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="573f0-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="573f0-106">Si los usuarios alojados en Exchange 2013 tienen sus buzones en espera In-Place, Exchange In-Place mantener directivas controlan el archivado de esos usuarios.</span><span class="sxs-lookup"><span data-stu-id="573f0-106">If users homed on Exchange 2013 have their mailboxes put on In-Place Hold, Exchange In-Place Hold policies control archiving for those users.</span></span> <span data-ttu-id="573f0-107">Si usa la integración de Microsoft Exchange para su implementación, las directivas de Exchange 2013 invalidan las directivas de archivado de Lync Server para los usuarios que están alojados en los 2013 de Exchange.</span><span class="sxs-lookup"><span data-stu-id="573f0-107">If you use Microsoft Exchange integration for your deployment, Exchange 2013 policies override Lync Server Archiving policies for users who are homed on Exchange 2013.</span></span> <span data-ttu-id="573f0-108">Para obtener más información sobre cómo configurar las directivas de archivado de Exchange, consulte la documentación de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="573f0-108">For information about configuring Exchange Archiving policies, see the Exchange 2013 documentation.</span></span> <span data-ttu-id="573f0-109">Para obtener detalles sobre cómo configurar directivas de usuario para usuarios alojados en Lync Server 2013, vea [configurar directivas de usuario para archivar en Lync server 2013](lync-server-2013-setting-up-user-policies-for-archiving-in-lync-server.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="573f0-109">For details about setting up user policies for users homed on Lync Server 2013, see [Setting up user policies for Archiving in Lync Server 2013](lync-server-2013-setting-up-user-policies-for-archiving-in-lync-server.md) in the Deployment documentation.</span></span> <span data-ttu-id="573f0-110">Para obtener más información sobre cómo funcionan las directivas, consulte [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, documentación de implementación u operaciones.</span><span class="sxs-lookup"><span data-stu-id="573f0-110">For details about how policies work, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="573f0-111">Si implementa Exchange 2013 y Lync Server 2013 en el mismo bosque, las directivas de Exchange 2013 In-Place retener controlan el archivado.</span><span class="sxs-lookup"><span data-stu-id="573f0-111">If you deploy Exchange 2013 and Lync Server 2013 in the same forest, your Exchange 2013 In-Place Hold policies control archiving.</span></span> <span data-ttu-id="573f0-112">Si implementa Exchange 2013 y Lync Server 2013 en bosques independientes, consulte "implementar Lync Server y Microsoft Exchange en bosques diferentes" en la <A href="lync-server-2013-deployment-checklist-for-archiving.md">lista de comprobación de la implementación para archivar en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="573f0-112">If you deploy Exchange 2013 and Lync Server 2013 in separate forests, see “Deploying Lync Server and Microsoft Exchange in Different Forests” in <A href="lync-server-2013-deployment-checklist-for-archiving.md">Deployment checklist for Archiving in Lync Server 2013</A>.</span></span>



<span data-ttu-id="573f0-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="573f0-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

