---
title: 'Lync Server 2013: Administrar directivas de correo de voz hospedado'
description: 'Lync Server 2013: Administrar directivas de correo de voz hospedado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage hosted voice mail policies
ms:assetid: 50ff22e3-9c8b-4a33-a72f-d149892acf53
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398332(v=OCS.15)
ms:contentKeyID: 48184139
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fcb5e98884d37540d5e75cc8cb6b1b419e4e75e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426098"
---
# <a name="manage-hosted-voice-mail-policies-in-lync-server-2013"></a><span data-ttu-id="dbb77-103">Administrar directivas de correo de voz hospedado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbb77-103">Manage hosted voice mail policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dbb77-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dbb77-104">

<span> </span></span></span>

<span data-ttu-id="dbb77-105">_**Última modificación del tema:** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="dbb77-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="dbb77-106">Una *Directiva de correo de voz hospedada* proporciona información a la aplicación de enrutamiento de 2013 ExUM de Lync Server acerca de dónde enrutar las llamadas de los usuarios cuyos buzones se encuentran en un servicio de Exchange hospedado.</span><span class="sxs-lookup"><span data-stu-id="dbb77-106">A *hosted voice mail policy* provides information to the Lync Server 2013 ExUM Routing application about where to route calls for users whose mailboxes are located on a hosted Exchange service.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="dbb77-107">Por lo general, solo se necesita una directiva de correo de voz hospedado.</span><span class="sxs-lookup"><span data-stu-id="dbb77-107">Typically, only one hosted voice mail policy is required.</span></span> <span data-ttu-id="dbb77-108">En muchos casos, puede modificar la directiva global para satisfacer todas sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="dbb77-108">In many cases, you can modify the global policy to meet all your needs.</span></span> <span data-ttu-id="dbb77-109">Si crea una directiva con el ámbito del sitio, se asignará automáticamente a todos los usuarios alojados en el sitio especificado.</span><span class="sxs-lookup"><span data-stu-id="dbb77-109">If you create a policy with site scope, it is assigned automatically to all users homed at the specified site.</span></span> <span data-ttu-id="dbb77-110">Si crea una directiva con ámbito por usuario, debe asignarla explícitamente a los usuarios, grupos y objetos de contacto.</span><span class="sxs-lookup"><span data-stu-id="dbb77-110">If you create a policy with per-user scope, you must explicitly assign it to users, groups, and contact objects.</span></span> <span data-ttu-id="dbb77-111">Es posible implementar varias directivas de correo de voz hospedado, pero, en ese caso, las directivas deben asignarse para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="dbb77-111">It is possible to deploy multiple hosted voice mail policies, but in that case the policies must be assigned on a per-user basis.</span></span>



</div>

<span data-ttu-id="dbb77-112">Para obtener más información sobre cómo planear directivas de correo de voz hospedado, consulte [directivas de correo de voz hospedado en Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="dbb77-112">For details about planning hosted voice mail policies, see [Hosted voice mail policies in Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="dbb77-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="dbb77-113">In This Section</span></span>

  - [<span data-ttu-id="dbb77-114">Modificar la Directiva de correo de voz hospedado global en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbb77-114">Modify the global hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-modify-the-global-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="dbb77-115">Crear una directiva de correo de voz hospedado en el nivel de sitio en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbb77-115">Create a site-level hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-create-a-site-level-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="dbb77-116">Crear una directiva de correo de voz hospedada por usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbb77-116">Create a per-user hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-create-a-per-user-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="dbb77-117">Asignar una directiva de correo de voz hospedado por usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbb77-117">Assign a per-user hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md)

<span data-ttu-id="dbb77-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dbb77-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

