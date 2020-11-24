---
title: Configurar la supervisión SCOM
description: Configurar la supervisión de SCOM.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure SCOM monitoring
ms:assetid: 4003d225-2a33-448c-abd9-571750661140
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688033(v=OCS.15)
ms:contentKeyID: 49733624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c93e10c705a1a1e08972d7534e00a33c472d23a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398370"
---
# <a name="configure-scom-monitoring"></a><span data-ttu-id="96805-103">Configurar la supervisión SCOM</span><span class="sxs-lookup"><span data-stu-id="96805-103">Configure SCOM monitoring</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96805-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96805-104">

<span> </span></span></span>

<span data-ttu-id="96805-105">_**Última modificación del tema:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="96805-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="96805-106">Después de migrar a Microsoft Lync Server 2013, debe completar algunas tareas para configurar Lync Server 2013 para que funcione con System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="96805-106">After migrating to Microsoft Lync Server 2013, you must complete a few tasks to configure Lync Server 2013 to work with System Center Operations Manager.</span></span>

  - <span data-ttu-id="96805-107">Aplique actualizaciones de Lync Server 2010 a un servidor elegido para administrar la lógica de descubrimiento central.</span><span class="sxs-lookup"><span data-stu-id="96805-107">Apply Lync Server 2010 updates to a server elected to manage the central discovery logic.</span></span>

  - <span data-ttu-id="96805-108">Actualice la clave del registro del candidato de detección central.</span><span class="sxs-lookup"><span data-stu-id="96805-108">Update the central discovery candidate server registry key.</span></span>

  - <span data-ttu-id="96805-109">Configure el servidor de administración principal de System Center Operations Manager para que invalide el nodo de detección central candidato.</span><span class="sxs-lookup"><span data-stu-id="96805-109">Configure your primary System Center Operations Manager management server to override the candidate central discovery node.</span></span>

<span data-ttu-id="96805-110">A continuación se proporcionan instrucciones para llevar a cabo estas tareas.</span><span class="sxs-lookup"><span data-stu-id="96805-110">Instructions for carrying out each of these tasks are provided below.</span></span>

<span data-ttu-id="96805-111">**Aplique actualizaciones de Lync Server 2010 a un servidor elegido para administrar la lógica de descubrimiento central.**</span><span class="sxs-lookup"><span data-stu-id="96805-111">**Apply Lync Server 2010 updates to a server elected to manage the central discovery logic.**</span></span>

1.  <span data-ttu-id="96805-112">Elija un servidor que tenga instalados los archivos del agente System Center Operations Manager y esté configurado como un nodo de detección candidato.</span><span class="sxs-lookup"><span data-stu-id="96805-112">Elect a server that has the System Center Operations Manager agent files installed and is configured as a candidate discovery node.</span></span>

2.  <span data-ttu-id="96805-113">Aplique las actualizaciones de Lync Server 2010 a este servidor.</span><span class="sxs-lookup"><span data-stu-id="96805-113">Apply Lync Server 2010 updates to this server.</span></span> <span data-ttu-id="96805-114">Vea el tema sobre cómo [aplicar actualizaciones de Lync Server 2010](apply-lync-server-2010-updates.md).</span><span class="sxs-lookup"><span data-stu-id="96805-114">See the topic [Apply Lync Server 2010 updates](apply-lync-server-2010-updates.md).</span></span>

<span data-ttu-id="96805-115">**Actualice la clave del registro del candidato de detección central.**</span><span class="sxs-lookup"><span data-stu-id="96805-115">**Update the central discovery candidate server registry key.**</span></span>

1.  <span data-ttu-id="96805-116">En el servidor elegido para administrar la lógica de detección central, abra una ventana de comandos de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="96805-116">On the server elected to manage the central discovery logic, open a Windows PowerShell command window.</span></span>

2.  <span data-ttu-id="96805-117">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="96805-117">At the command line, type the following:</span></span>
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health"
       ```
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health\CentralDiscoveryCandidate"
       ```
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="96805-118">Siempre que edite el registro, es posible que se produzca un error en el comando si la clave del registro ya existe.</span><span class="sxs-lookup"><span data-stu-id="96805-118">Whenever you edit the registry, you may experience an error that the command failed if the registry key already exists.</span></span> <span data-ttu-id="96805-119">Si tiene esto, puede ignorar el error sin riesgos.</span><span class="sxs-lookup"><span data-stu-id="96805-119">If you experience this, you can safely ignore the error.</span></span>

    
    </div>

<span data-ttu-id="96805-120">**Configure su servidor de administración principal de System Center Operations Manager para invalidar el nodo de supervisor de detección central candidato.**</span><span class="sxs-lookup"><span data-stu-id="96805-120">**Configure your primary System Center Operations Manager management server to override the candidate central discovery watcher node.**</span></span>

1.  <span data-ttu-id="96805-121">En un equipo en el que se haya instalado la consola de System Center Operations Manager, expanda los **objetos del módulo de administración** y seleccione **descubrimientos de objetos**.</span><span class="sxs-lookup"><span data-stu-id="96805-121">On a computer where the System Center Operations Manager console has been installed, expand **Management Pack Objects** and then select **Object Discoveries**.</span></span>

2.  <span data-ttu-id="96805-122">Haga clic en **cambiar ámbito...**</span><span class="sxs-lookup"><span data-stu-id="96805-122">Click **Change Scope...**</span></span>

3.  <span data-ttu-id="96805-123">En la página **objetos del módulo de administración del ámbito** , seleccione candidato de detección de **LS**.</span><span class="sxs-lookup"><span data-stu-id="96805-123">From the **Scope Management Pack Objects** page, select **LS Discovery Candidate**.</span></span>

4.  <span data-ttu-id="96805-124">Invalide el **valor efectivo candidato** a la detección de LS al nombre del servidor candidato elegido en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="96805-124">Override the **LS Discovery Candidate Effective Value** to the name of the candidate server elected in the earlier procedure.</span></span>

<span data-ttu-id="96805-125">Por último, para finalizar los cambios, reinicie el servicio de mantenimiento en el servidor de administración de raíz de System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="96805-125">Lastly, to finalize your changes, restart the health service on the System Center Operations Manager Root Management Server.</span></span>

<span data-ttu-id="96805-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96805-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

