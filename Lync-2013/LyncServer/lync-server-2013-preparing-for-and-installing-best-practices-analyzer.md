---
title: 'Lync Server 2013: preparación para la instalación del analizador de procedimientos recomendados'
description: 'Lync Server 2013: preparación de e instalación del analizador de procedimientos recomendados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing for and installing Best Practices Analyzer
ms:assetid: 550613dd-dc08-482e-9980-a3fe187cd162
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591347(v=OCS.15)
ms:contentKeyID: 48184149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 005c5ac372a3564e74af549832830ebae899e9d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424145"
---
# <a name="preparing-for-and-installing-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="28891-103">Preparación de e instalación del analizador de procedimientos recomendados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="28891-103">Preparing for and installing Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="28891-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="28891-104">

<span> </span></span></span>

<span data-ttu-id="28891-105">_**Última modificación del tema:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="28891-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="28891-106">Para realizar las tareas que se describen en este tema, debe haber iniciado sesión como miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="28891-106">You must be logged on as a member of the Administrators group to perform the tasks that are described in this topic.</span></span>

<div>

## <a name="system-requirements-for-best-practices-analyzer-installation"></a><span data-ttu-id="28891-107">Requisitos del sistema para la instalación del analizador de procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="28891-107">System Requirements for Best Practices Analyzer Installation</span></span>

<span data-ttu-id="28891-108">Para ejecutar Lync Server 2013, analizador de procedimientos recomendados para explorar su entorno, el equipo debe ejecutar una edición de 64 bits de uno de los siguientes sistemas operativos:</span><span class="sxs-lookup"><span data-stu-id="28891-108">To run Lync Server 2013, Best Practices Analyzer to scan your environment, the computer must be running a 64-bit edition of one of the following operating systems:</span></span>

  - <span data-ttu-id="28891-109">Sistema operativo estándar Windows Server 2008 R2 con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="28891-109">Windows Server 2008 R2 with Service Pack 1 (SP1) Standard operating system</span></span>

  - <span data-ttu-id="28891-110">Sistema operativo Windows Server 2008 R2 con SP1 Enterprise</span><span class="sxs-lookup"><span data-stu-id="28891-110">Windows Server 2008 R2 with SP1 Enterprise operating system</span></span>

  - <span data-ttu-id="28891-111">Sistema operativo Windows Server 2008 R2 con SP1 Datacenter</span><span class="sxs-lookup"><span data-stu-id="28891-111">Windows Server 2008 R2 with SP1 Datacenter operating system</span></span>

  - <span data-ttu-id="28891-112">Sistema operativo Windows Server 2012 Datacenter</span><span class="sxs-lookup"><span data-stu-id="28891-112">Windows Server 2012 Datacenter operating system</span></span>

  - <span data-ttu-id="28891-113">Sistema operativo Windows Server 2012 Standard</span><span class="sxs-lookup"><span data-stu-id="28891-113">Windows Server 2012 Standard operating system</span></span>

  - <span data-ttu-id="28891-114">Sistema operativo Windows Server 2012 Enterprise</span><span class="sxs-lookup"><span data-stu-id="28891-114">Windows Server 2012 Enterprise operating system</span></span>

  - <span data-ttu-id="28891-115">Sistema operativo Windows Server 2012 R2 Datacenter</span><span class="sxs-lookup"><span data-stu-id="28891-115">Windows Server 2012 R2 Datacenter operating system</span></span>

  - <span data-ttu-id="28891-116">Sistema operativo Windows Server 2012 R2 Standard</span><span class="sxs-lookup"><span data-stu-id="28891-116">Windows Server 2012 R2 Standard operating system</span></span>

  - <span data-ttu-id="28891-117">Sistema operativo Windows Server 2012 R2 Enterprise</span><span class="sxs-lookup"><span data-stu-id="28891-117">Windows Server 2012 R2 Enterprise operating system</span></span>

  - <span data-ttu-id="28891-118">Sistema operativo Windows 8</span><span class="sxs-lookup"><span data-stu-id="28891-118">Windows 8 operating system</span></span>

  - <span data-ttu-id="28891-119">Sistema operativo Windows 7</span><span class="sxs-lookup"><span data-stu-id="28891-119">Windows 7 operating system</span></span>

<span data-ttu-id="28891-120">El equipo también debe estar ejecutando lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="28891-120">The computer must also be running the following:</span></span>

  - <span data-ttu-id="28891-121">Microsoft .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="28891-121">Microsoft .NET Framework 4.5.</span></span> <span data-ttu-id="28891-122">Para Lync Server 2013, debe instalar manualmente la edición de 64 bits de Microsoft .NET Framework 4,5 en el servidor antes de instalar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="28891-122">For Lync Server 2013, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span>

  - <span data-ttu-id="28891-123">Lync Server 2013, componentes principales.</span><span class="sxs-lookup"><span data-stu-id="28891-123">Lync Server 2013, Core Components.</span></span>

  - <span data-ttu-id="28891-124">Paquete de compatibilidad con versiones anteriores de WMI.</span><span class="sxs-lookup"><span data-stu-id="28891-124">WMI Backward Compatibility Package.</span></span> <span data-ttu-id="28891-125">Para obtener más información, consulte [instalar el paquete de compatibilidad con versiones anteriores de WMI](install-wmi-backward-compatibility-package.md) en la documentación de la migración.</span><span class="sxs-lookup"><span data-stu-id="28891-125">For details, see [Install WMI Backward Compatibility package](install-wmi-backward-compatibility-package.md) in the Migration documentation.</span></span>

  - <span data-ttu-id="28891-126">Windows PowerShell 3,0.</span><span class="sxs-lookup"><span data-stu-id="28891-126">Windows PowerShell 3.0.</span></span> <span data-ttu-id="28891-127">Para obtener más información, consulte [instalar Windows PowerShell 3,0 para Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="28891-127">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md) in the Deployment documentation.</span></span>

<span data-ttu-id="28891-128">Puede instalar Best Practices Analyzer en equipos con un sistema operativo compatible que no ejecute Lync Server 2013, los componentes básicos o el paquete de compatibilidad con versiones anteriores de WMI, pero puede usar Best Practices Analyzer en esos equipos solo para ver los informes, no para realizar análisis.</span><span class="sxs-lookup"><span data-stu-id="28891-128">You can install Best Practices Analyzer on computers with a supported operating system that are not running Lync Server 2013, Core Components or WMI Backward Compatibility Package, but you can use Best Practices Analyzer on those computers only to view reports, not to run scans.</span></span>

</div>

<div>

## <a name="choosing-a-computer-for-installation"></a><span data-ttu-id="28891-129">Elegir un equipo para la instalación</span><span class="sxs-lookup"><span data-stu-id="28891-129">Choosing a Computer for Installation</span></span>

<span data-ttu-id="28891-130">Le recomendamos que instale Lync Server 2013, Best Practices Analyzer en un equipo dedicado a la administración de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="28891-130">We recommend that you install Lync Server 2013, Best Practices Analyzer on a computer that is dedicated to Lync Server 2013 management.</span></span> <span data-ttu-id="28891-131">Puede instalar la herramienta en un servidor que ejecute Lync Server 2013 o en un equipo administrativo que ejecute herramientas administrativas 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="28891-131">You can install the tool on a server running Lync Server 2013 or an administrative computer running Lync Server 2013 administrative tools.</span></span> <span data-ttu-id="28891-132">Si instala la herramienta en un servidor que ejecuta Lync Server, le recomendamos que use la herramienta para examinar solo ese servidor.</span><span class="sxs-lookup"><span data-stu-id="28891-132">If you install the tool on a server that is running Lync Server, we recommend that you use the tool to scan only that server.</span></span>

</div>

<div>

## <a name="installing-best-practices-analyzer"></a><span data-ttu-id="28891-133">Instalación del analizador de procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="28891-133">Installing Best Practices Analyzer</span></span>

<span data-ttu-id="28891-134">Puede descargar Best Practices Analyzer para Lync Server 2013 en [https://go.microsoft.com/fwlink/p/?linkId=266539](https://go.microsoft.com/fwlink/p/?linkid=266539) .</span><span class="sxs-lookup"><span data-stu-id="28891-134">You can download the Best Practices Analyzer for Lync Server 2013 at [https://go.microsoft.com/fwlink/p/?linkId=266539](https://go.microsoft.com/fwlink/p/?linkid=266539).</span></span>

<span data-ttu-id="28891-135">Para instalar Best Practices Analyzer, inicie el archivo de Microsoft Installer RtcBPA.msi en el equipo en el que desea instalar la herramienta y, a continuación, siga las instrucciones que aparecen en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="28891-135">To install Best Practices Analyzer, start the Microsoft Installer file RtcBPA.msi on the computer where you want to install the tool, and then follow the instructions on the screen.</span></span> <span data-ttu-id="28891-136">La ubicación predeterminada para instalar los archivos de programa es \<system drive\> \\ archivos de programa de \\ Lync Server 2013 \\ BPA.</span><span class="sxs-lookup"><span data-stu-id="28891-136">The default location for installing the program files is \<system drive\>\\Program Files\\Lync Server 2013\\BPA.</span></span>

<span data-ttu-id="28891-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="28891-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

