---
title: 'Lync Server 2013: Requisitos previos del componente de VDI de Lync'
description: 'Lync Server 2013: requisitos previos del complemento de Lync VDI.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync VDI plug-in prerequisites
ms:assetid: da25a976-7624-4dfc-b332-9c4db4ee78da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205304(v=OCS.15)
ms:contentKeyID: 48185552
ms.date: 03/07/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4389f776747426d07442e29418ab97e9609de7ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426245"
---
# <a name="lync-vdi-plug-in-prerequisites-in-lync-server-2013"></a><span data-ttu-id="abc2a-103">Requisitos previos del componente de VDI de Lync en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abc2a-103">Lync VDI plug-in prerequisites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abc2a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abc2a-104">

<span> </span></span></span>

<span data-ttu-id="abc2a-105">_**Última modificación del tema:** 2017-03-07_</span><span class="sxs-lookup"><span data-stu-id="abc2a-105">_**Topic Last Modified:** 2017-03-07_</span></span>

<span data-ttu-id="abc2a-106">En un entorno de infraestructura de escritorio virtual (VDI), las máquinas virtuales y el equipo local del usuario deben cumplir los requisitos descritos en esta sección.</span><span class="sxs-lookup"><span data-stu-id="abc2a-106">In a virtual desktop infrastructure (VDI) environment, the virtual machines and the user’s local computer must meet the requirements outlined in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="abc2a-107">Para obtener más información sobre cómo instalar e implementar el entorno virtualizado, consulte su proveedor de soluciones de virtualización.</span><span class="sxs-lookup"><span data-stu-id="abc2a-107">Refer to your virtualization solution provider for details about how to install and deploy the virtualized environment.</span></span> <span data-ttu-id="abc2a-108">Para obtener información sobre cómo implementar un entorno virtualizado basado en Hyper-V y servicios de escritorio remoto, consulte los artículos siguientes en la biblioteca de Microsoft TechNet:</span><span class="sxs-lookup"><span data-stu-id="abc2a-108">For information about deploying a virtualized environment based on Hyper-V and Remote Desktop Services, see the following articles in the Microsoft TechNet Library:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="abc2a-109">Hyper-V en <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247514">https://go.microsoft.com/fwlink/p/?linkid=247514</A></span><span class="sxs-lookup"><span data-stu-id="abc2a-109">Hyper-V at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247514">https://go.microsoft.com/fwlink/p/?linkid=247514</A></span></span></P>
> <LI>
> <P><span data-ttu-id="abc2a-110">Servicios de escritorio remoto en Windows Server &nbsp; 2008 &nbsp; R2 en <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247513">https://go.microsoft.com/fwlink/p/?linkid=247513</A></span><span class="sxs-lookup"><span data-stu-id="abc2a-110">Remote Desktop Services in Windows Server&nbsp;2008&nbsp;R2 at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247513">https://go.microsoft.com/fwlink/p/?linkid=247513</A></span></span></P></LI></UL>



</div>

<span data-ttu-id="abc2a-111">A continuación se indican los requisitos para las máquinas virtuales que se ejecutan en el equipo del centro de datos:</span><span class="sxs-lookup"><span data-stu-id="abc2a-111">The following are requirements for the virtual machines running on the data center computer:</span></span>

  - <span data-ttu-id="abc2a-112">Las máquinas virtuales deben configurarse con Windows 10, Windows 8,1, Windows 8, Windows 7 o Windows Server 2008 R2 con los Service Packs más recientes.</span><span class="sxs-lookup"><span data-stu-id="abc2a-112">Virtual machines must be configured with Windows 10, Windows 8.1, Windows 8, Windows 7, or Windows Server 2008 R2 with the latest service packs.</span></span>

<span data-ttu-id="abc2a-113">A continuación se indican los requisitos para el usuario y el equipo local del usuario:</span><span class="sxs-lookup"><span data-stu-id="abc2a-113">The following are requirements for the user and the user’s local computer:</span></span>

  - <span data-ttu-id="abc2a-114">El usuario debe estar alojado en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="abc2a-114">The user must be homed on Lync Server 2013.</span></span>

  - <span data-ttu-id="abc2a-115">El equipo local debe estar ejecutando Windows Embedded Standard 7 con SP1, Windows 7 con SP1, Windows 8, Windows 8,1 Embedded o Windows 8,1 (no incrustado).</span><span class="sxs-lookup"><span data-stu-id="abc2a-115">The local computer must be running Windows Embedded Standard 7 with SP1, Windows 7 with SP1, Windows 8, Windows 8.1 Embedded, or Windows 8.1 (not embedded).</span></span>

  - <span data-ttu-id="abc2a-116">Si está usando servicios de escritorio remoto, el bits del complemento VDI de Lync (es decir, si la aplicación es de 32 bits o 64 bits) debe coincidir con los bits del sistema operativo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="abc2a-116">If you are using Remote Desktop Services, the Lync VDI plug-in bitness (that is, whether the application is 32-bit or 64-bit) must match the local computer’s operating system bitness.</span></span> <span data-ttu-id="abc2a-117">No es necesario que los bits del sistema operativo en el equipo local y en el sistema operativo de la máquina virtual coincidan.</span><span class="sxs-lookup"><span data-stu-id="abc2a-117">The bitness of the operating system on the local computer and the operating system on the virtual machine do not need to match.</span></span> <span data-ttu-id="abc2a-118">Si está usando otra solución de virtualización o plataforma, consulte la guía de su proveedor de soluciones de virtualización sobre los requisitos de bits.</span><span class="sxs-lookup"><span data-stu-id="abc2a-118">If you are using another virtualization solution or platform, refer to guidance from your virtualization solution provider about bitness requirements.</span></span>

  - <span data-ttu-id="abc2a-119">El equipo local debe estar ejecutando la última versión del cliente de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="abc2a-119">The local computer must be running the latest version of the remote desktop client.</span></span> <span data-ttu-id="abc2a-120">Instale las últimas actualizaciones del cliente de los Servicios de Escritorio remoto de Microsoft o el último software de cliente de escritorio remoto del proveedor de soluciones de virtualización.</span><span class="sxs-lookup"><span data-stu-id="abc2a-120">Install the latest updates of Remote Desktop Services client from Microsoft or the latest remote desktop client software from your virtualization solution provider.</span></span> <span data-ttu-id="abc2a-121">Para obtener las actualizaciones más recientes de servicios de escritorio remoto, consulte [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032) .</span><span class="sxs-lookup"><span data-stu-id="abc2a-121">For the latest Remote Desktop Services updates, see [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032).</span></span>

  - <span data-ttu-id="abc2a-122">En el equipo local, configure el cliente de escritorio remoto para que el audio se reproduzca en el equipo local y la grabación remota esté deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="abc2a-122">On the local computer, the remote desktop client settings must be configured so that audio plays on the local computer and remote recording is disabled.</span></span> <span data-ttu-id="abc2a-123">Para configurar estas opciones de conexión a escritorio remoto en Windows, consulte la sección siguiente, "para configurar las opciones de conexión a escritorio remoto".</span><span class="sxs-lookup"><span data-stu-id="abc2a-123">To configure these settings for Remote Desktop Connection in Windows, see the next section, "To configure Remote Desktop Connection settings."</span></span>

<div>

## <a name="to-configure-remote-desktop-connection-settings"></a><span data-ttu-id="abc2a-124">Para configurar las opciones de conexión a escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="abc2a-124">To configure Remote Desktop Connection settings</span></span>

<span data-ttu-id="abc2a-125">Para preparar conexión a escritorio remoto en Windows para el complemento VDI de Lync, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="abc2a-125">To prepare Remote Desktop Connection in Windows for the Lync VDI plug-in, follow these steps.</span></span>

1.  <span data-ttu-id="abc2a-126">Si el equipo local está ejecutando Windows 8, omita este paso.</span><span class="sxs-lookup"><span data-stu-id="abc2a-126">If the local computer is running Windows 8, skip this step.</span></span> <span data-ttu-id="abc2a-127">Si el equipo local ejecuta Windows 7 con SP1, instale la versión más reciente de Windows 8 del cliente de servicios de escritorio remoto, disponible en [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032) .</span><span class="sxs-lookup"><span data-stu-id="abc2a-127">If the local computer is running Windows 7 with SP1, install the latest Windows 8 version of the Remote Desktop Services client, available at [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032).</span></span>

2.  <span data-ttu-id="abc2a-128">Inicie el cliente de Servicios de Escritorio remoto haciendo clic en **Iniciar** y después en **Conexión a Escritorio remoto**.</span><span class="sxs-lookup"><span data-stu-id="abc2a-128">Start the Remote Desktop Services client by clicking **Start**, and then clicking **Remote Desktop Connection**.</span></span>

3.  <span data-ttu-id="abc2a-129">Haga clic en **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="abc2a-129">Click **Options**.</span></span>

4.  <span data-ttu-id="abc2a-130">Haga clic en la pestaña **Recursos locales**. En **Audio remoto**, haga clic en **Configuración** y haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="abc2a-130">Click the **Local Resources** tab. Under **Remote audio**, click **Settings**, and then do the following:</span></span>
    
      - <span data-ttu-id="abc2a-131">En **Reproducción de audio remoto**, seleccione **Reproducir en este equipo**.</span><span class="sxs-lookup"><span data-stu-id="abc2a-131">Under **Remote audio playback**, select **Play on this computer**.</span></span>
    
      - <span data-ttu-id="abc2a-132">En **Grabación de audio remoto**, seleccione **No grabar**.</span><span class="sxs-lookup"><span data-stu-id="abc2a-132">Under **Remote audio recording**, select **Do not record**.</span></span>
    
      - <span data-ttu-id="abc2a-133">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="abc2a-133">Click **OK**.</span></span>

5.  <span data-ttu-id="abc2a-134">Haga clic en la pestaña **Experiencia**. En **Rendimiento**, desactive la casilla **Almacenamiento en caché persistente de mapas de bits**.</span><span class="sxs-lookup"><span data-stu-id="abc2a-134">Click the **Experience** tab. Under **Performance**, clear the **Persistent bitmap caching** check box.</span></span>

6.  <span data-ttu-id="abc2a-135">Haga clic en la pestaña **General** . En **equipo**, escriba el nombre de la máquina virtual y, a continuación, haga clic en **conectar**.</span><span class="sxs-lookup"><span data-stu-id="abc2a-135">Click the **General** tab. In **Computer**, type the name of the virtual machine, and then click **Connect**.</span></span>

<span data-ttu-id="abc2a-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abc2a-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

