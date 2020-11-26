---
title: 'Lync Server 2013: Shell de administración de Lync Server'
description: 'Lync Server 2013: Shell de administración de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server Management Shell
ms:assetid: 674b523b-c0b7-4ed6-9e67-afa6e8ac7e12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398474(v=OCS.15)
ms:contentKeyID: 48184386
ms.date: 09/20/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45727c42899defcf20ce36e2a27a9268a52ecd71
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426268"
---
# <a name="lync-server-2013-management-shell"></a><span data-ttu-id="a9065-103">Shell de administración de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9065-103">Lync Server 2013 Management Shell</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a9065-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a9065-104">

<span> </span></span></span>

<span data-ttu-id="a9065-105">_**Última modificación del tema:** 2017-09-20_</span><span class="sxs-lookup"><span data-stu-id="a9065-105">_**Topic Last Modified:** 2017-09-20_</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a9065-106">La referencia del cmdlet de Skype empresarial se ha movido a docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a9065-106">Skype for Business cmdlet reference has moved to docs.microsoft.com.</span></span> <span data-ttu-id="a9065-107">Al hacer clic en los vínculos siguientes te llevará a la nueva página de docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a9065-107">Clicking on the links below will take you to the new docs.microsoft.com page.</span></span> <span data-ttu-id="a9065-108">El contenido ahora está abierto y disponible para las contribuciones de la comunidad a través de GitHub.</span><span class="sxs-lookup"><span data-stu-id="a9065-108">The content is now open sourced and available for community contributions through GitHub.</span></span> <span data-ttu-id="a9065-109">¿Está interesado en colaborar?</span><span class="sxs-lookup"><span data-stu-id="a9065-109">Interested in contributing?</span></span> <span data-ttu-id="a9065-110">Consulte el archivo Léame en el repositorio aquí: <A href="https://github.com/microsoftdocs/office-docs-powershell">https://github.com/MicrosoftDocs/office-docs-powershell</A></span><span class="sxs-lookup"><span data-stu-id="a9065-110">Check out the README in the repo here: <A href="https://github.com/microsoftdocs/office-docs-powershell">https://github.com/MicrosoftDocs/office-docs-powershell</A></span></span>



</div>

<span data-ttu-id="a9065-111">Microsoft Lync Server 2010 presentó un gran conjunto de características nuevas y mejoradas en comparación con lo que estaba disponible en Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="a9065-111">Microsoft Lync Server 2010 introduced a large set of new and improved features compared to what was available in Microsoft Office Communications Server 2007 R2.</span></span> <span data-ttu-id="a9065-112">Una mejora es la manera en la que administra su implementación.</span><span class="sxs-lookup"><span data-stu-id="a9065-112">One improvement is the way in which you manage your implementation.</span></span> <span data-ttu-id="a9065-113">Por ejemplo, hay una nueva interfaz de usuario, llamada panel de control de Lync Server, que representa un gran turno desde donde se usan la mayoría de los usuarios con Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="a9065-113">For example, there’s a new user interface, called the Lync Server Control Panel, which represents a big shift from what most people are used to with the Microsoft Management Console.</span></span> <span data-ttu-id="a9065-114">La otra mejora importante de la capacidad de administración es la inclusión de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a9065-114">The other major improvement to manageability is the inclusion of Windows PowerShell.</span></span>

<span data-ttu-id="a9065-115">Windows PowerShell le permite administrar aplicaciones de Microsoft desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a9065-115">Windows PowerShell allows you to manage Microsoft applications from the command line.</span></span> <span data-ttu-id="a9065-116">Incluye un entorno de línea de comandos, comandos específicos del producto y un lenguaje de scripting completo.</span><span class="sxs-lookup"><span data-stu-id="a9065-116">It includes a command-line environment, product-specific commands, and a full scripting language.</span></span> <span data-ttu-id="a9065-117">Windows PowerShell se presentó por primera vez como una versión descargable para el sistema operativo Windows en 2006, y se incorporó como la interfaz de línea de comandos para la capacidad de administración de Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="a9065-117">Windows PowerShell was first introduced as a downloadable release for the Windows operating system late in 2006, and was incorporated as the command-line interface for manageability of Microsoft Exchange Server 2007.</span></span> <span data-ttu-id="a9065-118">A partir de ese punto, continuará creciendo y se ha incorporado a la mayoría de los productos de servidor de Microsoft, el más reciente de ellos es Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a9065-118">From that point it continued to grow, and it has been incorporated into most of the Microsoft Server products, the most recent of these being Microsoft Lync Server 2013.</span></span> <span data-ttu-id="a9065-119">Lync Server 2010 ha introducido cmdlets específicos de producto de 550 que puede usar para administrar todos los aspectos de su implementación.</span><span class="sxs-lookup"><span data-stu-id="a9065-119">Lync Server 2010 introduced close to 550 product-specific cmdlets that you can use to manage every aspect of your deployment.</span></span>

<span data-ttu-id="a9065-120">Las secciones siguientes contienen una lista de los cmdlets y sus descripciones.</span><span class="sxs-lookup"><span data-stu-id="a9065-120">The following sections contain a list of cmdlets and their descriptions.</span></span> <span data-ttu-id="a9065-121">Esta información también se encuentra disponible directamente en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a9065-121">This information is also available directly from the command line.</span></span> <span data-ttu-id="a9065-122">Simplemente escriba lo siguiente en el símbolo del sistema del shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="a9065-122">Simply type the following at the Lync Server Management Shell command prompt:</span></span>

    Get-Help <cmdlet name> -Full

<span data-ttu-id="a9065-123">Por ejemplo, para obtener ayuda en el símbolo del sistema sobre el cmdlet **New-CsVoicePolicy**, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a9065-123">For example, to retrieve help from the command prompt on the **New-CsVoicePolicy** cmdlet, type the following:</span></span>

    Get-Help New-CsVoicePolicy -Full

<span data-ttu-id="a9065-124">Cosas que debe saber sobre Windows PowerShell en Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="a9065-124">Things to know about Windows PowerShell in Lync Server 2013:</span></span>

  - <span data-ttu-id="a9065-125">Para ejecutar los cmdlets de Lync Server, abra el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a9065-125">To run the Lync Server cmdlets, open the Lync Server Management Shell.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="a9065-126">Si abre una ventana de Windows PowerShell en lugar del shell de administración de Lync Server, de forma predeterminada, no podrá ejecutar los cmdlets de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a9065-126">If you open a Windows PowerShell window rather than the Lync Server Management Shell, by default you will not be able to run the Lync Server cmdlets.</span></span> <span data-ttu-id="a9065-127">Para ejecutar los cmdlets de Lync Server desde Windows PowerShell, en primer lugar escriba lo siguiente en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a9065-127">To run the Lync Server cmdlets from within Windows PowerShell, first type the following at the Windows PowerShell command prompt:</span></span><BR><span data-ttu-id="a9065-128">Import-Module Lync</span><span class="sxs-lookup"><span data-stu-id="a9065-128">Import-Module Lync</span></span>

    
    </div>

  - <span data-ttu-id="a9065-129">El shell de administración de Lync Server se instala automáticamente en todos los servidores front-end de Lync Server Enterprise Edition o en el servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a9065-129">Lync Server Management Shell is automatically installed on every Lync Server Enterprise Edition Front End Server or Standard Edition server.</span></span>

  - <span data-ttu-id="a9065-130">La información nueva y actualizada, los scripts de ejemplo y la ayuda para comenzar y aprender más acerca de los cmdlets de Windows PowerShell y Microsoft Lync Server 2013 está disponible en el blog de Windows PowerShell de Lync Server [https://go.microsoft.com/fwlink/p/?linkId=203150](https://go.microsoft.com/fwlink/p/?linkid=203150) .</span><span class="sxs-lookup"><span data-stu-id="a9065-130">New and updated information, sample scripts, and help for getting started and learning more about Windows PowerShell and Microsoft Lync Server 2013 cmdlets is available at the Lync Server Windows PowerShell Blog [https://go.microsoft.com/fwlink/p/?linkId=203150](https://go.microsoft.com/fwlink/p/?linkid=203150).</span></span>

<span data-ttu-id="a9065-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a9065-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

