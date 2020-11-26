---
title: Instalar los archivos básicos de Lync Server 2013 y la base de datos de RTCLocal
description: Instalar los archivos básicos de Lync Server 2013 y la base de datos de RTCLocal.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Server 2013 core files and the RTCLocal database
ms:assetid: 206f0c1d-40f7-45b6-aa62-88aaef6cf7f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204734(v=OCS.15)
ms:contentKeyID: 48183591
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 68964f8b80f6377afd859d113783d61e33afbebd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427001"
---
# <a name="installing-the-lync-server-2013-core-files-and-the-rtclocal-database"></a><span data-ttu-id="58d2e-103">Instalar los archivos básicos de Lync Server 2013 y la base de datos de RTCLocal</span><span class="sxs-lookup"><span data-stu-id="58d2e-103">Installing the Lync Server 2013 core files and the RTCLocal database</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58d2e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58d2e-104">

<span> </span></span></span>

<span data-ttu-id="58d2e-105">_**Última modificación del tema:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="58d2e-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="58d2e-106">Para instalar los archivos principales de Lync Server 2013 en un equipo, complete el siguiente procedimiento.</span><span class="sxs-lookup"><span data-stu-id="58d2e-106">To install the Lync Server 2013 core files on a computer, complete the following procedure.</span></span> <span data-ttu-id="58d2e-107">La base de datos de RTCLocal se instala automáticamente al instalar los archivos principales.</span><span class="sxs-lookup"><span data-stu-id="58d2e-107">The RTCLocal database is automatically installed when you install the core files.</span></span> <span data-ttu-id="58d2e-108">Tenga en cuenta que no es necesario instalar SQL Server en los nodos de los monitores.</span><span class="sxs-lookup"><span data-stu-id="58d2e-108">Note that you do not need to install SQL Server on the watcher nodes.</span></span> <span data-ttu-id="58d2e-109">En su lugar, SQL Server Express se instala automáticamente.</span><span class="sxs-lookup"><span data-stu-id="58d2e-109">Instead, SQL Server Express is automatically installed for you.</span></span>

<span data-ttu-id="58d2e-110">Para instalar los archivos principales de Lync Server 2013 y la base de datos RTCLocal:</span><span class="sxs-lookup"><span data-stu-id="58d2e-110">To install the Lync Server 2013 core files and the RTCLocal database:</span></span>

1.  <span data-ttu-id="58d2e-111">En el equipo del nodo de monitor, haga clic en **Inicio**, haga clic en **todos los programas**, en **accesorios**, en **símbolo del sistema** y luego en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="58d2e-111">On the watcher node computer, click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="58d2e-112">En la ventana de consola, escriba el siguiente comando y, a continuación, presione entrar, usando la ruta de acceso adecuada a los archivos de instalación de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="58d2e-112">In the console window, type the following command and then press ENTER, using the appropriate path to your Lync Server setup files:</span></span>
    
        D:\Setup.exe /BootstrapLocalMgmt

<span data-ttu-id="58d2e-113">Para comprobar que los componentes principales de Lync Server se instalaron correctamente, haga clic en **Inicio**, haga clic en **todos los programas**, **Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="58d2e-113">To verify that the core Lync Server components were successfully installed, click **Start**, click **All Programs**, click **Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span> <span data-ttu-id="58d2e-114">En el shell de administración de Lync Server 2013, escriba el siguiente comando de Windows PowerShell y, a continuación, presione ENTRAR:</span><span class="sxs-lookup"><span data-stu-id="58d2e-114">In the Lync Server 2013 Management Shell, type the following Windows PowerShell command, and then press ENTER:</span></span>

    Get-CsWatcherNodeConfiguration

<span data-ttu-id="58d2e-115">La primera vez que ejecute este comando, no se devolverá ningún dato porque aún no ha configurado ningún equipo de nodo de monitor.</span><span class="sxs-lookup"><span data-stu-id="58d2e-115">The first time you run this command, you no data is returned because you have not configured any watcher node computers yet.</span></span> <span data-ttu-id="58d2e-116">Siempre y cuando el comando se ejecute sin devolver un error, puede suponer que la configuración de Lync Server se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="58d2e-116">As long as the command runs without returning an error, you can assume that the Lync Server setup completed successfully.</span></span>

<span data-ttu-id="58d2e-117">Si el equipo del nodo de observador está ubicado dentro de la red perimetral, puede ejecutar el siguiente comando para comprobar la instalación de Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="58d2e-117">If your watcher node computer is located inside your perimeter network, you can run the following command to verify the installation of Lync Server 2013:</span></span>

    Get-CsPinPolicy

<span data-ttu-id="58d2e-118">Recibirá información similar a la siguiente, según el número de directivas de números de identificación personal (PIN) configuradas para su uso en su organización:</span><span class="sxs-lookup"><span data-stu-id="58d2e-118">You will receive information similar to the following, depending on the number of personal identification number (PIN) policies configured for use in your organization:</span></span>

    Identity             : Global
    Description          :
    MinPasswordLength    : 5
    PINHistoryCount      : 0
    AllowCommonPatterns  : False
    PINLifetime          : 0
    MaximumLogonAttempts :

<span data-ttu-id="58d2e-119">Si ve información sobre las directivas de PIN, significa que ha instalado correctamente los componentes principales.</span><span class="sxs-lookup"><span data-stu-id="58d2e-119">If you see information about your PIN policies, it means that you have successfully installed the core components.</span></span>

<span data-ttu-id="58d2e-120"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58d2e-120"></div>

<span> </span>

</div>

</div>

</span></span></div>

