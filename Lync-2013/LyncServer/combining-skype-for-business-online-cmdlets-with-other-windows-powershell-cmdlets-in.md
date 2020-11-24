---
title: Combinar cmdlets de Skype empresarial online con otros cmdlets de Windows PowerShell en
description: Combinar cmdlets de Skype empresarial online con otros cmdlets de Windows PowerShell en.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Combining Skype for Business Online cmdlets with other Windows PowerShell cmdlets
ms:assetid: 8bb8800a-f966-4570-8c8b-db87a91ad783
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362816(v=OCS.15)
ms:contentKeyID: 56558835
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5bd18f60891d48a54eb2f77f189ea8417e0b5e93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398874"
---
# <a name="combining-skype-for-business-online-cmdlets-with-other-windows-powershell-cmdlets-in"></a><span data-ttu-id="e0088-103">Combinar cmdlets de Skype empresarial online con otros cmdlets de Windows PowerShell en</span><span class="sxs-lookup"><span data-stu-id="e0088-103">Combining Skype for Business Online cmdlets with other Windows PowerShell cmdlets in</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e0088-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e0088-104">

<span> </span></span></span>

<span data-ttu-id="e0088-105">_**Última modificación del tema:** 2013-07-05_</span><span class="sxs-lookup"><span data-stu-id="e0088-105">_**Topic Last Modified:** 2013-07-05_</span></span>

<span data-ttu-id="e0088-106">Al conectarse a Skype empresarial online mediante Windows PowerShell, aproximadamente 40 cmdlets de Skype empresarial online estarán disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="e0088-106">When you connect to Skype for Business Online by using Windows PowerShell, approximately 40 Skype for Business Online cmdlets will available for your use.</span></span> <span data-ttu-id="e0088-107">Sin embargo, no está limitado a usar solo esos cmdlets de 40 al administrar Skype empresarial online.</span><span class="sxs-lookup"><span data-stu-id="e0088-107">However, you are not limited to using just those 40 cmdlets when managing Skype for Business Online.</span></span> <span data-ttu-id="e0088-108">Además de los cmdlets de Skype empresarial online, también puede usar otros cmdlets de Windows PowerShell que estén instalados en su equipo.</span><span class="sxs-lookup"><span data-stu-id="e0088-108">In addition to the Skype for Business Online cmdlets, you can also use any other Windows PowerShell cmdlets that are installed on your computer.</span></span> <span data-ttu-id="e0088-109">(Al instalar Windows PowerShell 3,0, también se instalan cientos de cmdlets básicos de Windows PowerShell). Sus comandos pueden combinar y asociar los cmdlets de Skype empresarial online y cualquier otro cmdlet disponible en su equipo.</span><span class="sxs-lookup"><span data-stu-id="e0088-109">(When you install Windows PowerShell 3.0, hundreds of core Windows PowerShell cmdlets are installed, as well.) Your commands can mix and match Skype for Business Online cmdlets and any other cmdlets available on your computer.</span></span>

<span data-ttu-id="e0088-110">Aunque un curso completo en Windows PowerShell 3,0 va más allá del ámbito de este artículo, aquí se muestran algunos ejemplos que muestran por qué es posible que desee combinar y asociar cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e0088-110">Although a complete course in Windows PowerShell 3.0 goes beyond the scope of this article, here are a few examples that show why you might want to mix and match cmdlets.</span></span> <span data-ttu-id="e0088-111">En primer lugar, ninguno de los cmdlets de Skype empresarial online incluye un comando imprimir, y este comando no se puede encontrar en la consola de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0088-111">First of all, none of the Skype for Business Online cmdlets include a Print command, and no such command can be found in the Windows PowerShell console, either.</span></span> <span data-ttu-id="e0088-112">¿Cómo se obtiene una copia impresa de la información que un cmdlet ha recuperado?</span><span class="sxs-lookup"><span data-stu-id="e0088-112">So how do you get a printout of the information retrieved by a cmdlet?</span></span> <span data-ttu-id="e0088-113">Una es recuperar la información y, a continuación, enviar esa información al cmdlet **out-Printer** :</span><span class="sxs-lookup"><span data-stu-id="e0088-113">One way is to retrieve the information, and then send that information to the **Out-Printer** cmdlet:</span></span>

    Get-CsTenant | Out-Printer

<span data-ttu-id="e0088-114">Como no se incluyen parámetros adicionales, toda la información devuelta por **el cmdlet out-Printer** se imprimirá en la impresora predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e0088-114">Because no additional parameters are included, all the information returned by **the Out-Printer** cmdlet will be printed to the default printer.</span></span>

<span data-ttu-id="e0088-115">Del mismo modo, ninguno de los cmdlets de Skype empresarial online incluye un parámetro que le permite guardar datos en un archivo.</span><span class="sxs-lookup"><span data-stu-id="e0088-115">Likewise, none of the Skype for Business Online cmdlets include a parameter that allows you to save data to a file.</span></span> <span data-ttu-id="e0088-116">Pero eso es correcto: este comando usa el cmdlet **out-File** para guardar la información devuelta en el archivo de texto C: \\ logs \\Tenants.txt:</span><span class="sxs-lookup"><span data-stu-id="e0088-116">But that’s OK: this command uses the **Out-File** cmdlet to save the returned information to the text file C:\\Logs\\Tenants.txt:</span></span>

    Get-Tenant | Out-File -FilePath "C:\Logs\Tenants.txt"

<span data-ttu-id="e0088-117">Y este comando usa el cmdlet **Select-Object** para limitar los datos que se devuelven y se muestran en pantalla.</span><span class="sxs-lookup"><span data-stu-id="e0088-117">And this command uses the **Select-Object** cmdlet to limit the data that is returned and displayed onscreen.</span></span> <span data-ttu-id="e0088-118">En este ejemplo, el cmdlet [Get-CsOnlineUser](https://technet.microsoft.com/library/JJ994026(v=OCS.15)) recupera información de todos los usuarios de Skype empresarial online y, a continuación, el cmdlet **Select-Object** se usa para limitar los datos mostrados al valor de identidad del usuario y a su Directiva de archivado:</span><span class="sxs-lookup"><span data-stu-id="e0088-118">In this example, the [Get-CsOnlineUser](https://technet.microsoft.com/library/JJ994026(v=OCS.15)) cmdlet retrieves information for all of your Skype for Business Online users, and then the **Select-Object** cmdlet is used to limit the displayed data to the user’s Identity value and their archiving policy:</span></span>

    Get-CsOnlineUser | Select-Object Identity, ArchivingPolicy

<span data-ttu-id="e0088-119">Como habrá cientos de cmdlets disponibles para su uso en el equipo, es posible que tenga problemas para determinar qué cmdlets son los cmdlets de Skype empresarial online y cuáles no.</span><span class="sxs-lookup"><span data-stu-id="e0088-119">Because there will be hundreds of cmdlets available for use on your computer, you might have difficulty determining which cmdlets are Skype for Business Online cmdlets and which ones are not.</span></span> <span data-ttu-id="e0088-120">Para obtener una lista de los cmdlets de Skype empresarial online (y solo de Skype empresarial online), primero debe determinar el nombre del módulo temporal de Windows PowerShell que contiene todos los cmdlets de Skype empresarial online.</span><span class="sxs-lookup"><span data-stu-id="e0088-120">To return a list of the Skype for Business Online cmdlets (and only Skype for Business Online cmdlets), you must first determine the name of the temporary Windows PowerShell module that contains all the Skype for Business Online cmdlets.</span></span> <span data-ttu-id="e0088-121">Para ello, ejecute este comando desde el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e0088-121">To do that, run this command from the Windows PowerShell prompt:</span></span>

    Get-Module

<span data-ttu-id="e0088-122">Aparecerá información similar a la siguiente en la pantalla:</span><span class="sxs-lookup"><span data-stu-id="e0088-122">Information similar to the following will appear onscreen:</span></span>

    ModuleType Name                 ExportedCommands
    ---------- ----                 ----------------
    Manifest   Microsoft.PowerS...  {Add-Computer, Add-Content, A...}
    Script     tmp_5astd3uh.m5v     {Disable-CsMeetingRoom, Enabl...}

<span data-ttu-id="e0088-123">El módulo con el script de ModuleType es el módulo que contiene los cmdlets de Skype empresarial online.</span><span class="sxs-lookup"><span data-stu-id="e0088-123">The module with the ModuleType Script is the module that contains the Skype for Business Online cmdlets.</span></span> <span data-ttu-id="e0088-124">Para obtener una lista de esos cmdlets, ejecute el cmdlet **get-command** y use el nombre del módulo de script como el nombre del módulo:</span><span class="sxs-lookup"><span data-stu-id="e0088-124">To return a list of those cmdlets, run the **Get-Command** cmdlet, using the name of the Script module as the module name:</span></span>

    Get-Command -Module tmp_5astd3uh.m5v

<span data-ttu-id="e0088-125">Es posible tener varios módulos con un valor de ModuleType igual a script.</span><span class="sxs-lookup"><span data-stu-id="e0088-125">It’s possible that you could have multiple modules with a ModuleType equal to Script.</span></span> <span data-ttu-id="e0088-126">En ese caso, puede ejecutar el comando siguiente para averiguar qué módulo incluye el cmdlet **Get-CsTenant** :</span><span class="sxs-lookup"><span data-stu-id="e0088-126">In that case, you can run the following command to find out which module includes the **Get-CsTenant** cmdlet:</span></span>

    Get-Command Get-CsTenant

<span data-ttu-id="e0088-127">El módulo devuelto para el cmdlet **Get-CsTenant** será el módulo que contiene todos los cmdlets de Skype empresarial online:</span><span class="sxs-lookup"><span data-stu-id="e0088-127">The module returned for the **Get-CsTenant** cmdlet will be the module containing all the Skype for Business Online cmdlets:</span></span>

    CommandType     Name                                               ModuleName
    -----------     ----                                               ----------
    Function        Get-CsTenant                                       tmp_5astd3uh.m5v

<div>

## <a name="see-also"></a><span data-ttu-id="e0088-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0088-128">See Also</span></span>


<span data-ttu-id="e0088-129">[Una introducción a Windows PowerShell y Skype Empresarial Online](https://technet.microsoft.com/library/Dn362785(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e0088-129">[An introduction to Windows PowerShell and Skype for Business Online](https://technet.microsoft.com/library/Dn362785(v=OCS.15))</span></span>  
  

<span data-ttu-id="e0088-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e0088-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

