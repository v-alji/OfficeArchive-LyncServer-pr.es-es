---
title: 'Lync Server 2013: Habilitar la directiva de servidor de chat persistente'
description: 'Lync Server 2013: habilitar la Directiva del servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Persistent Chat Server policy
ms:assetid: 87063d6c-2e38-4970-b76d-2aa15f0de29e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205056(v=OCS.15)
ms:contentKeyID: 48184718
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58da577679795f00492af72b43ca72106d40f4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428842"
---
# <a name="enable-persistent-chat-server-policy-in-lync-server-2013"></a><span data-ttu-id="a3e6f-103">Habilitar la directiva de servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3e6f-103">Enable Persistent Chat Server policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3e6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3e6f-104">

<span> </span></span></span>

<span data-ttu-id="a3e6f-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="a3e6f-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="a3e6f-106">En el panel de control de Lync Server 2013, puede usar la página de la **Directiva de chat** persistente del grupo **chat persistente** para administrar directivas a nivel global, de grupo, de sitio o de usuario, incluida la configuración de la directiva global predeterminada y la creación de una o más directivas de usuario y de sitio adicionales para su implementación.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-106">In the Lync Server 2013 Control Panel, you can use the **Persistent Chat Policy** page of the **Persistent Chat** group to manage policies at a global, pool, site, or user level, including configuring the default global policy and creating one or more additional user and site policies for your deployment.</span></span> <span data-ttu-id="a3e6f-107">Si un usuario está habilitado para el servidor de chat persistente por directiva, el entorno del servidor de chat persistente aparece en el cliente de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-107">If a user is enabled for Persistent Chat Server by policy, then the Persistent Chat Server environment appears in their Lync 2013 client.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a3e6f-108">En la topología, se aplican globalmente las directivas del sitio servidor de chat persistentes, por grupo de usuarios o por sitio o por usuario.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-108">In the topology, Persistent Chat Server site policies apply globally, per user’s pool, or per user’s site, or per user.</span></span>



</div>

<span data-ttu-id="a3e6f-109">La directiva global se crea automáticamente al implementar un servidor de chat persistente, y puede configurarse, pero no eliminarse.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-109">The global policy is created automatically when you deploy Persistent Chat Server, and it can be configured, but not deleted.</span></span> <span data-ttu-id="a3e6f-110">Debido a que la política global se aplica a todos los usuarios, no hay que configurarla para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-110">Because the global policy applies to all users, it doesn’t have to be set per user.</span></span>

<span data-ttu-id="a3e6f-111">Puede crear y configurar varias directivas de sitio y de usuario que, junto con la directiva global, permitan a los usuarios usar el servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-111">You can create and configure multiple site and user policies which, together with the global policy, enable users for Persistent Chat Server.</span></span> <span data-ttu-id="a3e6f-112">Las directivas del servidor de chat persistente del sitio y del grupo invalidan la Directiva del servidor de chat persistente global, pero solo para los usuarios de ese sitio.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-112">Pool and site Persistent Chat Server policies override the global Persistent Chat Server policy, but only for users of that site.</span></span> <span data-ttu-id="a3e6f-113">Las directivas de usuario reemplazan a las directivas globales, de grupo y de sitio para los usuarios que tengan asignada esa directiva de usuario.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-113">User policies override both global, pool, and site policies for the users to whom the user policy is assigned.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a3e6f-114">Para configurar y usar el servidor de chat persistente, primero debe usar topología Builder para agregar la compatibilidad con el servidor de chat persistente a la topología y, a continuación, publicar la topología.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-114">To configure and use Persistent Chat Server, you must first use Topology Builder to add Persistent Chat Server support to the topology, and then publish the topology.</span></span> <span data-ttu-id="a3e6f-115">Para obtener más información, vea <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Agregar un servidor de chat persistente a su implementación en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-115">For details, see <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adding Persistent Chat Server to your deployment in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a3e6f-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a3e6f-116">In This Section</span></span>

  - [<span data-ttu-id="a3e6f-117">Configurar la directiva global para chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3e6f-117">Configure the global policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-configure-the-global-policy-for-persistent-chat.md)

  - [<span data-ttu-id="a3e6f-118">Crear una directiva de sitio para chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3e6f-118">Create a site policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-create-a-site-policy-for-persistent-chat.md)

  - [<span data-ttu-id="a3e6f-119">Crear una directiva de usuario para chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3e6f-119">Create a user policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-create-a-user-policy-for-persistent-chat.md)

  - [<span data-ttu-id="a3e6f-120">Aplicar una directiva de chat persistente a un usuario o grupo de usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3e6f-120">Apply a Persistent Chat policy to a user or user group in Lync Server 2013</span></span>](lync-server-2013-apply-a-persistent-chat-policy-to-a-user-or-user-group.md)

<span data-ttu-id="a3e6f-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3e6f-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

