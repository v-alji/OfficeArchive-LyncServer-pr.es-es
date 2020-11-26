---
title: 'Lync Server 2013: Instalar la herramienta de planeación'
description: 'Lync Server 2013: instalación de la herramienta de planeación.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Planning Tool
ms:assetid: ebdc9e26-4b22-4b02-85b9-7462bcfe7c93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615046(v=OCS.15)
ms:contentKeyID: 51541525
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11836e2c86cb01d6f911670a9eeafef0c31c0af4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426910"
---
# <a name="installing-the-planning-tool-in-lync-server-2013"></a><span data-ttu-id="95244-103">Instalar la herramienta de planeación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="95244-103">Installing the Planning Tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="95244-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="95244-104">

<span> </span></span></span>

<span data-ttu-id="95244-105">_**Última modificación del tema:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="95244-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="95244-106">Antes de empezar a diseñar y planear la infraestructura de Lync Server 2013 con Microsoft Lync Server 2013, la herramienta de planeación, primero debe instalar la herramienta de planeación.</span><span class="sxs-lookup"><span data-stu-id="95244-106">Before you begin designing and planning your Lync Server 2013 infrastructure by using the Microsoft Lync Server 2013, Planning Tool, you must first install the Planning Tool.</span></span> <span data-ttu-id="95244-107">No es necesario implementar la herramienta de planeación en una estación de trabajo o servidor que forme parte del dominio o de la infraestructura donde se va a instalar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="95244-107">The Planning Tool does not need to be deployed to a workstation or server that is part of the domain or infrastructure where you plan to install Lync Server 2013.</span></span> <span data-ttu-id="95244-108">El archivo Léame que acompaña a la herramienta de planificación detalla información importante sobre la instalación y el uso de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="95244-108">The Readme file that accompanies the Planning Tool details important information about installing and using the tool.</span></span> <span data-ttu-id="95244-109">Se ha duplicado aquí una parte de la información del archivo Léame para mayor claridad.</span><span class="sxs-lookup"><span data-stu-id="95244-109">Some of the information in the Readme file is duplicated here for clarity.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="95244-110">La herramienta de Planeación requiere la instalación de un usuario con derechos y permisos de administrador en el equipo en el que se va a instalar la herramienta.</span><span class="sxs-lookup"><span data-stu-id="95244-110">The Planning Tool requires installation by a user with administrator rights and permissions on the computer on which the tool is to be installed.</span></span>



</div>

<span data-ttu-id="95244-111">Los sistemas operativos compatibles para la instalación y el funcionamiento de la herramienta de planificación son:</span><span class="sxs-lookup"><span data-stu-id="95244-111">The supported operating systems for installation and operation of the Planning Tool are:</span></span>

  - <span data-ttu-id="95244-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="95244-112">Windows 8</span></span>

  - <span data-ttu-id="95244-113">Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="95244-113">Windows 8.1</span></span>

  - <span data-ttu-id="95244-114">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="95244-114">Windows Server 2012</span></span>

  - <span data-ttu-id="95244-115">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="95244-115">Windows Server 2012 R2</span></span>

  - <span data-ttu-id="95244-116">Edición de 32 bits de Windows 7</span><span class="sxs-lookup"><span data-stu-id="95244-116">Windows 7, 32-bit edition</span></span>

  - <span data-ttu-id="95244-117">Edición de 64 bits de Windows 7 usando Windows en Win32 (WOW)</span><span class="sxs-lookup"><span data-stu-id="95244-117">Windows 7, 64-bit edition using Windows on Win32 (WOW)</span></span>

  - <span data-ttu-id="95244-118">Windows Server 2008 R2 usando WOW</span><span class="sxs-lookup"><span data-stu-id="95244-118">Windows Server 2008 R2, using WOW</span></span>

<span data-ttu-id="95244-119">Además, la herramienta de Planeación requiere Microsoft .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="95244-119">Additionally, the Planning Tool requires Microsoft .NET Framework 4.5.</span></span>

<span data-ttu-id="95244-120">Después de que se cumplan los requisitos de preinstalación, puede instalar la herramienta de planeación.</span><span class="sxs-lookup"><span data-stu-id="95244-120">After the preinstallation requirements are met, you can then install the Planning Tool.</span></span>

<div>

## <a name="to-install-the-planning-tool"></a><span data-ttu-id="95244-121">Para instalar la Herramienta de planeación</span><span class="sxs-lookup"><span data-stu-id="95244-121">To install the Planning Tool</span></span>

1.  <span data-ttu-id="95244-122">Inicie sesión en el equipo local como miembro del grupo Administradores.</span><span class="sxs-lookup"><span data-stu-id="95244-122">Log on to the local computer as a member of the Administrators group.</span></span>

2.  <span data-ttu-id="95244-123">Con el explorador de Windows o una ventana de comandos, busque el directorio en el que ha descargado los archivos de instalación de la herramienta de planeación.</span><span class="sxs-lookup"><span data-stu-id="95244-123">Using Windows Explorer or a command window, locate the directory where you downloaded the Planning Tool installation files.</span></span>

3.  <span data-ttu-id="95244-124">Busque el LyncPlanningTool.msi.</span><span class="sxs-lookup"><span data-stu-id="95244-124">Locate the LyncPlanningTool.msi.</span></span> <span data-ttu-id="95244-125">En el Explorador de Windows, haga doble clic en el archivo.</span><span class="sxs-lookup"><span data-stu-id="95244-125">In Windows Explorer, double-click the file.</span></span> <span data-ttu-id="95244-126">En la ventana de línea de comandos, escriba el nombre del archivo y presione **Entrar** para ejecutarlo.</span><span class="sxs-lookup"><span data-stu-id="95244-126">In the command window, type the name of the file, and then press **Enter** to run the file.</span></span>

4.  <span data-ttu-id="95244-127">En la Página principal de **Microsoft Lync Server 2013, Asistente para la instalación de la herramienta de planeación**, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="95244-127">On the Welcome page of the **Microsoft Lync Server 2013, Planning Tool Setup Wizard**, click **Next**.</span></span>

5.  <span data-ttu-id="95244-128">Lea el **Contrato de licencia para el usuario final**, seleccione **Acepto los términos del contrato de licencia**, si quiere aceptar los términos de uso del contrato de licencia, y haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="95244-128">Review the **End-User License Agreement**, select **I accept the terms in the License Agreement** if you choose to accept the terms of use in the license agreement, and then click **Next**.</span></span>

6.  <span data-ttu-id="95244-129">Elija dónde instalar los archivos de la herramienta de planeación.</span><span class="sxs-lookup"><span data-stu-id="95244-129">Choose where to install the Planning Tool files.</span></span> <span data-ttu-id="95244-130">La ubicación predeterminada es C: \\ archivos de programa (x86) \\ Microsoft Lync Server 2013 \\ herramienta de planeación.</span><span class="sxs-lookup"><span data-stu-id="95244-130">The default location is C:\\Program Files (x86)\\Microsoft Lync Server 2013\\Planning Tool.</span></span> <span data-ttu-id="95244-131">Si desea cambiar la ubicación de instalación, haga clic en **cambiar**.</span><span class="sxs-lookup"><span data-stu-id="95244-131">If you want to change the installation location, click **Change**.</span></span> <span data-ttu-id="95244-132">En **cambiar carpeta de destino**, examine o escriba la ubicación para instalar los archivos, haga clic en **Aceptar** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="95244-132">On **Change destination folder**, browse or type the location to install the files, click **OK**, and then click **Next**.</span></span>

7.  <span data-ttu-id="95244-133">El instalador ya está listo para instalar la herramienta de planeación.</span><span class="sxs-lookup"><span data-stu-id="95244-133">The installer is now ready to install the Planning Tool.</span></span> <span data-ttu-id="95244-134">Haga clic en **Instalar** para comenzar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="95244-134">Click **Install** to begin the installation process.</span></span>

8.  <span data-ttu-id="95244-135">La instalación se iniciará y se mostrará el progreso de la misma.</span><span class="sxs-lookup"><span data-stu-id="95244-135">The installation will start, and the progress will be displayed.</span></span> <span data-ttu-id="95244-136">Una vez completado el proceso de instalación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="95244-136">After the installation is successfully completed, click **Finish**.</span></span>

9.  <span data-ttu-id="95244-137">La herramienta de planeación está lista para usarse.</span><span class="sxs-lookup"><span data-stu-id="95244-137">The Planning Tool is ready for use.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="95244-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="95244-138">See Also</span></span>


[<span data-ttu-id="95244-139">Instalar software opcional en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="95244-139">Installing optional software in Lync Server 2013</span></span>](lync-server-2013-installing-optional-software.md)  
  

<span data-ttu-id="95244-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="95244-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

