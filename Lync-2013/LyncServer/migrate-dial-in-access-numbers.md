---
title: Migrar los números de acceso telefónico
description: Migrar números de acceso telefónico local.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate dial-in access numbers
ms:assetid: e0dfaed2-64c7-45cb-aaa9-d6117a26625d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721909(v=OCS.15)
ms:contentKeyID: 49733843
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2c8bd34a30bc4b3f8999144cd84a1eee62e2ab1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446895"
---
# <a name="migrate-dial-in-access-numbers"></a><span data-ttu-id="69ab9-103">Migrar los números de acceso telefónico</span><span class="sxs-lookup"><span data-stu-id="69ab9-103">Migrate dial-in access numbers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69ab9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69ab9-104">

<span> </span></span></span>

<span data-ttu-id="69ab9-105">_**Última modificación del tema:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="69ab9-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="69ab9-106">La migración de números de acceso telefónico local de Lync Server 2010 a Lync Server 2013 requiere que se ejecute el cmdlet **Move-CsApplicationEndpoint** para migrar los objetos de contacto.</span><span class="sxs-lookup"><span data-stu-id="69ab9-106">Migrating dial-in access numbers from Lync Server 2010 to Lync Server 2013 requires running the **Move-CsApplicationEndpoint** cmdlet to migrate the contact objects.</span></span> <span data-ttu-id="69ab9-107">Durante el período de coexistencia de Lync Server 2010 y Lync Server 2013, los números de acceso telefónico local creados en Lync Server 2013 se comportan de forma similar a los números de acceso telefónico local que se crean en Lync Server 2010, tal y como se describe en esta sección.</span><span class="sxs-lookup"><span data-stu-id="69ab9-107">During the Lync Server 2010 and Lync Server 2013 coexistence period, dial-in access numbers that you created in Lync Server 2013 behave similarly to the dial-in access numbers that you create in Lync Server 2010, as described in this section.</span></span>

<span data-ttu-id="69ab9-108">Los números de acceso telefónico local que ha creado en Lync Server 2010, pero que se han movido a Lync Server 2013 o que ha creado en Lync Server 2013 antes, durante o después de la migración tienen las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="69ab9-108">Dial-in access numbers that you created in Lync Server 2010 but moved to Lync Server 2013 or that you created in Lync Server 2013 before, during or after migration have the following characteristics:</span></span>

  - <span data-ttu-id="69ab9-109">No aparecen en las invitaciones a reuniones de Office Communications Server 2007 R2 y la página de número de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="69ab9-109">Do not appear on Office Communications Server 2007 R2 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="69ab9-110">Aparece en las invitaciones a reuniones de Lync Server 2010 y la página de número de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="69ab9-110">Appear on Lync Server 2010 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="69ab9-111">Aparece en las invitaciones a reuniones de Lync Server 2013 y la página de número de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="69ab9-111">Appear on Lync Server 2013 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="69ab9-112">No se puede ver ni modificar en la herramienta administrativa de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="69ab9-112">Cannot be viewed or modified in the Office Communications Server 2007 R2 administrative tool.</span></span>

  - <span data-ttu-id="69ab9-113">Se puede ver y modificar en el panel de control de Lync Server 2010 y en el shell de administración de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="69ab9-113">Can be viewed and modified in the Lync Server 2010 Control Panel and in Lync Server 2010 Management Shell.</span></span>

  - <span data-ttu-id="69ab9-114">Se puede ver y modificar en el panel de control de Lync Server 2013 y en el shell de administración de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="69ab9-114">Can be viewed and modified in the Lync Server 2013 Control Panel and in Lync Server 2013 Management Shell.</span></span>

  - <span data-ttu-id="69ab9-115">Se puede volver a secuenciar dentro de la región mediante el cmdlet Set-CsDialinConferencingAccessNumber con el parámetro Priority.</span><span class="sxs-lookup"><span data-stu-id="69ab9-115">Can be re-sequenced within the region by using the Set-CsDialinConferencingAccessNumber cmdlet with the Priority parameter.</span></span>

<span data-ttu-id="69ab9-116">Debe finalizar la migración de los números de acceso telefónico local que apunten a un grupo de 2010 de Lync Server antes de retirar el grupo de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="69ab9-116">You must finish migrating dial-in access numbers that point to a Lync Server 2010 pool before you decommission the Lync Server 2010 pool.</span></span> <span data-ttu-id="69ab9-117">Si no completa la migración de números de acceso telefónico, como se describe en el siguiente procedimiento, se producirán errores en las llamadas entrantes a los números de acceso.</span><span class="sxs-lookup"><span data-stu-id="69ab9-117">If you do not complete dial-in access number migration as described in the following procedure, incoming calls to the access numbers will fail.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="69ab9-118">Debe realizar este procedimiento antes de dar de baja al grupo de servidores de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="69ab9-118">You must perform this procedure prior to decommissioning the Lync Server 2010 pool.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="69ab9-119">Le recomendamos que mueva los números de acceso telefónico cuando el uso de la red sea bajo, en caso de que haya un breve período de tiempo de servicio.</span><span class="sxs-lookup"><span data-stu-id="69ab9-119">We recommend that you move dial-in access numbers when network usage is low, in case there is a short period of service outage.</span></span>



</div>

<span data-ttu-id="69ab9-120">**Para identificar y mover los números de acceso telefónico local**</span><span class="sxs-lookup"><span data-stu-id="69ab9-120">**To identify and move dial-in access numbers**</span></span>

1.  <span data-ttu-id="69ab9-121">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="69ab9-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="69ab9-122">Para mover cada número de acceso de acceso telefónico local a un grupo alojado en Lync Server 2013, en la línea de comandos ejecute:</span><span class="sxs-lookup"><span data-stu-id="69ab9-122">To move each dial-in access number to a pool hosted on Lync Server 2013, from the command line run:</span></span>
    
        Move-CsApplicationEndpoint -Identity <SIP URI of the access number to be moved> -Target <FQDN of the pool to which the access number is moving>

3.  <span data-ttu-id="69ab9-123">Abra el Panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69ab9-123">Open Lync Server Control Panel.</span></span>

4.  <span data-ttu-id="69ab9-124">En la barra de navegación izquierda, haga clic en **Conferencia**.</span><span class="sxs-lookup"><span data-stu-id="69ab9-124">In the left navigation bar, click **Conferencing**.</span></span>

5.  <span data-ttu-id="69ab9-125">Haga clic en la pestaña **número de acceso telefónico local** .</span><span class="sxs-lookup"><span data-stu-id="69ab9-125">Click the **Dial-in Access Number** tab.</span></span>

6.  <span data-ttu-id="69ab9-126">Compruebe que no quedan números de acceso telefónico local para el grupo de servidores de Lync Server 2010 desde el que está migrando.</span><span class="sxs-lookup"><span data-stu-id="69ab9-126">Verify that no dial-in access numbers remain for the Lync Server 2010 pool from which you are migrating.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="69ab9-127">Cuando todos los números de acceso telefónico local señalan al grupo de servidores de Lync Server 2013, puede retirar el grupo de servidores de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="69ab9-127">When all dial-in access numbers point to the Lync Server 2013 pool, you can then decommission the Lync Server 2010 pool.</span></span>

    
    </div>

<span data-ttu-id="69ab9-128">**Comprobar la migración de números de acceso telefónico local con el panel de control de Lync Server**</span><span class="sxs-lookup"><span data-stu-id="69ab9-128">**Verify the dial-in access number migration using Lync Server Control Panel**</span></span>

1.  <span data-ttu-id="69ab9-129">Desde una cuenta de usuario que tenga asignada la función **CsUserAdministrator** o el rol **CsAdministrator** , inicie sesión en cualquier equipo de su implementación interna.</span><span class="sxs-lookup"><span data-stu-id="69ab9-129">From a user account that is assigned to the **CsUserAdministrator** role or the **CsAdministrator** role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="69ab9-130">Abra el Panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69ab9-130">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="69ab9-131">En la barra de navegación izquierda, haga clic en **Conferencia**.</span><span class="sxs-lookup"><span data-stu-id="69ab9-131">In the left navigation bar, click **Conferencing**.</span></span>

4.  <span data-ttu-id="69ab9-132">Haga clic en la pestaña **número de acceso telefónico local** .</span><span class="sxs-lookup"><span data-stu-id="69ab9-132">Click the **Dial-in Access Number** tab.</span></span>

5.  <span data-ttu-id="69ab9-133">Compruebe que todo el número de acceso telefónico local se ha migrado al grupo hospedado en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="69ab9-133">Verify all the dial-in access number are migrated to the pool hosted on Lync Server 2013.</span></span>

<span data-ttu-id="69ab9-134">**Comprobar la migración de números de acceso telefónico local con el shell de administración de Lync Server**</span><span class="sxs-lookup"><span data-stu-id="69ab9-134">**Verify the dial-in access number migration using Lync Server Management Shell**</span></span>

1.  <span data-ttu-id="69ab9-135">Abra el Shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69ab9-135">Open Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="69ab9-136">Para devolver todos los números de acceso de la Conferencia de acceso telefónico local migrados, desde la línea de comandos ejecute:</span><span class="sxs-lookup"><span data-stu-id="69ab9-136">To return all the dial-in conferencing access numbers migrated, from the command line run:</span></span>
    
        Get-CsDialInConferencingAccessNumber -Filter {Pool -eq "<FQDN of the pool to which the access number is moved>"}

3.  <span data-ttu-id="69ab9-137">Compruebe que todos los números de acceso telefónico local se migran al grupo hospedado en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="69ab9-137">Verify all the dial-in access numbers are migrated to the pool hosted on Lync Server 2013.</span></span>

<span data-ttu-id="69ab9-138"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69ab9-138"></div>

<span> </span>

</div>

</div>

</span></span></div>

