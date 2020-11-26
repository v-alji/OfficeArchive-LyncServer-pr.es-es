---
title: 'Lync Server 2013: configuración de la directiva global para archivar'
description: 'Lync Server 2013: configuración de la directiva global para el archivado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the global policy for Archiving
ms:assetid: 58341d6b-c3ff-4dd9-b1c7-0048f33861ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204906(v=OCS.15)
ms:contentKeyID: 48184192
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8f8125f458c4269626e0b1c929f2acb1a8de0b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432572"
---
# <a name="configuring-the-global-policy-for-archiving-in-lync-server-2013"></a><span data-ttu-id="28616-103">Configuración de la directiva global para archivar en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="28616-103">Configuring the global policy for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="28616-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="28616-104">

<span> </span></span></span>

<span data-ttu-id="28616-105">_**Última modificación del tema:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="28616-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="28616-106">Al implementar los servidores front-end, Lync Server crea una directiva global para el archivado.</span><span class="sxs-lookup"><span data-stu-id="28616-106">When you deploy your Front End Servers, Lync Server creates a global policy for Archiving.</span></span> <span data-ttu-id="28616-107">De forma predeterminada, el archivado está deshabilitado en la directiva global.</span><span class="sxs-lookup"><span data-stu-id="28616-107">By default, Archiving is disabled in the global policy.</span></span> <span data-ttu-id="28616-108">La directiva global controla si el archivado está habilitado para las comunicaciones internas y externas para toda la implementación, a no ser que Configure directivas de usuario o de sitio, que invaliden la directiva global, o si usa la integración de Microsoft Exchange para algunos o todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="28616-108">The global policy controls whether archiving is enabled for internal and external communications for your entire deployment, unless you set up site or user policies, which override the global policy, or if you use Microsoft Exchange integration for some or all of your users.</span></span> <span data-ttu-id="28616-109">Si usa la integración de Microsoft Exchange, la directiva global no se aplica a los usuarios alojados en Exchange 2013 y tienen los buzones puestos en espera In-Place.</span><span class="sxs-lookup"><span data-stu-id="28616-109">If you use Microsoft Exchange integration, the global policy does not apply to any users who are homed on Exchange 2013 and have the mailboxes put on In-Place Hold.</span></span>

<span data-ttu-id="28616-110">Para obtener detalles sobre cómo funcionan las directivas de archivado, incluida la jerarquía para las directivas globales, de sitio y de usuario, consulte [Cómo funciona el archivado en](lync-server-2013-how-archiving-works.md) la documentación de planeamiento, la documentación de implementación o la documentación de operaciones de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="28616-110">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="28616-111">Si habilita la integración de Microsoft Exchange para su implementación, las directivas de retención de Exchange In-Place controlan si el archivado está habilitado para los usuarios alojados en Exchange 2013 y si sus buzones se colocan en In-Place espera.</span><span class="sxs-lookup"><span data-stu-id="28616-111">If you enable Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="28616-112">Para obtener más información, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configurar directivas para archivar en Lync Server 2013 al usar la integración de Exchange Server</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="28616-112">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="28616-113">Debe especificar todas las opciones apropiadas en las configuraciones de archivado antes de habilitar el archivado.</span><span class="sxs-lookup"><span data-stu-id="28616-113">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="28616-114">Para obtener información detallada, vea <A href="lync-server-2013-configuring-archiving-options.md">configuración de las opciones de archivado en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="28616-114">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-configure-the-global-policy-for-archiving-when-using-lync-server-archiving-databases"></a><span data-ttu-id="28616-115">Para configurar la directiva global para archivar al usar las bases de datos de archivado de Lync Server</span><span class="sxs-lookup"><span data-stu-id="28616-115">To configure the global policy for archiving when using Lync Server Archiving databases</span></span>

1.  <span data-ttu-id="28616-116">Desde una cuenta de usuario que se asigne al rol CsArchivingAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="28616-116">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="28616-117">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="28616-117">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="28616-118">Para más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server 2013, consulte [abrir las herramientas administrativas de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="28616-118">For details about the different methods you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="28616-119">En la barra de navegación izquierda, haga clic en **Supervisión y archivado** y, después, en **Directiva de archivado**.</span><span class="sxs-lookup"><span data-stu-id="28616-119">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="28616-120">En la página **Directiva de archivado**, haga clic en **Global**, **Editar** y, luego, en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="28616-120">On the **Archiving Policy** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="28616-121">En **Editar directiva de archivado: global**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="28616-121">In **Edit Archiving Policy - Global**, do the following:</span></span>
    
      - <span data-ttu-id="28616-122">En **Nombre**, si no desea usar el nombre predeterminado "global", especifique un nombre nuevo para la directiva global.</span><span class="sxs-lookup"><span data-stu-id="28616-122">In **Name**, if you do not want to use the default name of Global, specify a new name for the global policy.</span></span>
    
      - <span data-ttu-id="28616-123">En **Descripción**, proporcione información sobre la directiva (por ejemplo, directiva global para *divisionName*).</span><span class="sxs-lookup"><span data-stu-id="28616-123">In **Description**, provide information about what the policy is (for example, Global policy for *divisionName*).</span></span>
    
      - <span data-ttu-id="28616-124">Para controlar el archivado de las comunicaciones internas de todos los usuarios y sitios que no se controlan específicamente por medio de una directiva de sitio o de usuario, active o desactive la casilla **Archivar comunicaciones internas**.</span><span class="sxs-lookup"><span data-stu-id="28616-124">To control archiving of internal communications for all sites and users not specifically controlled through a site policy or user policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="28616-125">Para controlar el archivado de las comunicaciones externas de todos los usuarios y sitios que no se controlan específicamente por medio de una directiva de sitio o de usuario, active o desactive la casilla **Archivar comunicaciones externas**.</span><span class="sxs-lookup"><span data-stu-id="28616-125">To control archiving of external communications for all sites and users not specifically controlled through a site policy or user policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="28616-126">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="28616-126">Click **Commit**.</span></span>

<span data-ttu-id="28616-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="28616-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

