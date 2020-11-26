---
title: Crear y configurar directivas de usuario para archivar en Lync Server
description: Crear y configurar directivas de usuario para archivar en Lync Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating and configuring user policies for Archiving in Lync Server
ms:assetid: 5af0e605-3563-4d6f-a3c6-511d204a3165
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204923(v=OCS.15)
ms:contentKeyID: 48184234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dad260910f01e10c71dbbde67af98ea9a207e33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431543"
---
# <a name="creating-and-configuring-user-policies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="bf3c4-103">Crear y configurar directivas de usuario para archivar en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf3c4-103">Creating and configuring user policies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf3c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf3c4-104">

<span> </span></span></span>

<span data-ttu-id="bf3c4-105">_**Última modificación del tema:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="bf3c4-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="bf3c4-106">Para habilitar o deshabilitar el archivado de usuarios específicos alojados en Lync Server, primero debe crear una directiva de usuario y, a continuación, aplicar la Directiva a uno o más usuarios o grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-106">To enable or disable Archiving for specific users homed on Lync Server, you must first create a user policy and then apply the policy to one or more users or user groups.</span></span> <span data-ttu-id="bf3c4-107">Para obtener detalles sobre cómo aplicar directivas de usuario a usuarios específicos y grupos de usuarios, vea [aplicar una directiva de archivado de Lync Server a un usuario en Lync server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-107">For details about applying user policies to specific users and user groups, see [Applying a Lync Server Archiving policy to a user in Lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) in the Deployment documentation.</span></span>

<span data-ttu-id="bf3c4-108">Para obtener más información sobre cómo funcionan las directivas de archivado, incluida la jerarquía para las directivas globales, de sitio y de usuario, consulte [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, en la documentación de implementación o en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-108">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, in the Deployment documentation, or in the Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="bf3c4-109">Si habilitó la integración de Microsoft Exchange para su implementación, las directivas de retención de Exchange In-Place controlan si el archivado está habilitado para los usuarios alojados en Exchange 2013 y si sus buzones se colocan en In-Place espera.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-109">If you enabled Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="bf3c4-110">Para obtener más información, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configurar directivas para archivar en Lync Server 2013 al usar la integración de Exchange Server</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-110">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="bf3c4-111">Debe especificar todas las opciones apropiadas en las configuraciones de archivado antes de habilitar el archivado.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-111">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="bf3c4-112">Para obtener información detallada, vea <A href="lync-server-2013-configuring-archiving-options.md">configuración de las opciones de archivado en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-112">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-configure-an-archiving-policy-for-users-homed-on-lync-server"></a><span data-ttu-id="bf3c4-113">Para configurar una directiva de archivado para usuarios alojados en Lync Server</span><span class="sxs-lookup"><span data-stu-id="bf3c4-113">To configure an archiving policy for users homed on Lync Server</span></span>

1.  <span data-ttu-id="bf3c4-114">Desde una cuenta de usuario que se asigne al rol CsArchivingAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-114">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="bf3c4-115">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-115">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="bf3c4-116">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server 2013, consulte [abrir las herramientas administrativas de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bf3c4-116">For details about the different methods that you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="bf3c4-117">En la barra de navegación izquierda, haga clic en **Supervisión y archivado** y, después, en **Directiva de archivado**.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-117">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="bf3c4-118">Haga clic en **Nuevo** y, luego, en **Directiva de usuario**.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-118">Click **New**, and then click **User policy**.</span></span>

5.  <span data-ttu-id="bf3c4-119">En **Directiva de archivado nueva**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bf3c4-119">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="bf3c4-120">En **Nombre**, escriba el nombre de la directiva de usuario.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-120">In **Name**, specify the name for the user policy.</span></span>
    
      - <span data-ttu-id="bf3c4-121">En **Descripción**, proporcione información sobre la directiva de usuario (por ejemplo, directiva de usuario para el departamento legal).</span><span class="sxs-lookup"><span data-stu-id="bf3c4-121">In **Description**, provide information about what the user policy is (for example, user policy for legal department).</span></span>
    
      - <span data-ttu-id="bf3c4-122">Para controlar el archivado de las comunicaciones internas para la directiva de usuario, active o desactive la casilla **Archivar comunicaciones internas**.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-122">To control archiving of internal communications for the user policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="bf3c4-123">Para controlar el archivado de las comunicaciones externas para la directiva de usuario, active o desactive la casilla **Archivar comunicaciones externas**.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-123">To control archiving of external communications for the user policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="bf3c4-124">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-124">Click **Commit**.</span></span>

<span data-ttu-id="bf3c4-125">Una directiva de usuario solo se aplica a los usuarios a los que asigne la directiva.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-125">A user policy applies only to users to whom you assign the policy.</span></span> <span data-ttu-id="bf3c4-126">Para obtener más información sobre cómo aplicar una directiva de usuario a usuarios específicos, consulte [aplicar una directiva de archivado de Lync Server a un usuario en Lync server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="bf3c4-126">For details about applying a user policy to specific users, see [Applying a Lync Server Archiving policy to a user in Lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) in the Deployment documentation.</span></span>

<span data-ttu-id="bf3c4-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf3c4-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

