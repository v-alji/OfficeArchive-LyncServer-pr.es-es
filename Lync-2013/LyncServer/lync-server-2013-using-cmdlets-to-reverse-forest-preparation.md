---
title: 'Lync Server 2013: Usar cmdlets para invertir la preparación del bosque'
description: 'Lync Server 2013: usar cmdlets para invertir la preparación del bosque.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using cmdlets to reverse forest preparation
ms:assetid: f48c7eb3-ccb0-48e6-ac79-ab7c7062b9d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413024(v=OCS.15)
ms:contentKeyID: 48185822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: acac87bdaeb7e730f93401fa62ea2678a713bb8f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439642"
---
# <a name="using-cmdlets-to-reverse-forest-preparation-for-lync-server-2013"></a><span data-ttu-id="c7c23-103">Usar cmdlets para invertir la preparación del bosque para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c7c23-103">Using cmdlets to reverse forest preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c7c23-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c7c23-104">

<span> </span></span></span>

<span data-ttu-id="c7c23-105">_**Última modificación del tema:** 2013-06-19_</span><span class="sxs-lookup"><span data-stu-id="c7c23-105">_**Topic Last Modified:** 2013-06-19_</span></span>

<span data-ttu-id="c7c23-106">Use el cmdlet **Disable-CsAdForest** para invertir el paso de preparación del bosque.</span><span class="sxs-lookup"><span data-stu-id="c7c23-106">Use the **Disable-CsAdForest** cmdlet to reverse the forest preparation step.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="c7c23-107">Si ejecuta el cmdlet <STRONG>Disable-CsAdForest</STRONG> en un entorno en el que también tiene una versión anterior de Lync Server implementada, también se eliminará la configuración global de la versión anterior.</span><span class="sxs-lookup"><span data-stu-id="c7c23-107">If you run the <STRONG>Disable-CsAdForest</STRONG> cmdlet in an environment where you also have a previous version of Lync Server deployed, the global settings for the previous version will also be deleted.</span></span>



</div>

<div>

## <a name="to-use-cmdlets-to-reverse-forest-preparation"></a><span data-ttu-id="c7c23-108">Para usar cmdlets para invertir la preparación del bosque</span><span class="sxs-lookup"><span data-stu-id="c7c23-108">To use cmdlets to reverse forest preparation</span></span>

1.  <span data-ttu-id="c7c23-109">Inicie sesión en un equipo unido a un dominio como miembro del grupo administradores del dominio en el dominio raíz del bosque.</span><span class="sxs-lookup"><span data-stu-id="c7c23-109">Log on to a computer that is joined to a domain as a member of the Domain Admins group in the forest root domain.</span></span>

2.  <span data-ttu-id="c7c23-110">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="c7c23-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="c7c23-111">Ejecute:</span><span class="sxs-lookup"><span data-stu-id="c7c23-111">Run:</span></span>
    
        Disable-CsAdForest [-Force] [-GroupDomain <FQDN of the domain in which universal groups were created>]
    
    <span data-ttu-id="c7c23-112">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c7c23-112">For example:</span></span>
    
        Disable-CsAdForest -Force -GroupDomain contoso.net
    
    <span data-ttu-id="c7c23-113">El parámetro Force especifica si se debe forzar la ejecución de la tarea.</span><span class="sxs-lookup"><span data-stu-id="c7c23-113">The Force parameter specifies whether to force running the task.</span></span> <span data-ttu-id="c7c23-114">Si este parámetro no está presente, el comando no se ejecutará si aún hay un dominio del bosque preparado para Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c7c23-114">If this parameter is not present, the command will not run if even one domain in the forest is still prepared for Lync Server 2013.</span></span> <span data-ttu-id="c7c23-115">Si se especifica el parámetro Force, la acción continuará independientemente del estado de otros dominios del bosque.</span><span class="sxs-lookup"><span data-stu-id="c7c23-115">If the Force parameter is specified, the action will continue regardless of the state of other domains in the forest.</span></span>
    
    <span data-ttu-id="c7c23-116">Si no especifica el parámetro GroupDomain, el valor predeterminado es el dominio local.</span><span class="sxs-lookup"><span data-stu-id="c7c23-116">If you do not specify the GroupDomain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c7c23-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7c23-117">See Also</span></span>


[<span data-ttu-id="c7c23-118">Ejecutar la preparación del bosque para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c7c23-118">Running forest preparation for Lync Server 2013</span></span>](lync-server-2013-running-forest-preparation.md)  


[<span data-ttu-id="c7c23-119">Preparación del bosque para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c7c23-119">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
  

<span data-ttu-id="c7c23-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c7c23-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

