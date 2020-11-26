---
title: 'Lync Server 2013: configuración de un nodo de monitor para usar la autenticación de credenciales'
description: 'Lync Server 2013: configuración de un nodo de monitor para usar la autenticación de credenciales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to use credential authentication
ms:assetid: 032e33f3-9483-42e6-a33c-347eb6779597
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204632(v=OCS.15)
ms:contentKeyID: 48183255
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b65d4e3f90b27aac69b8569472ac9896766e093e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433447"
---
# <a name="configuring-a-watcher-node-to-use-credential-authentication-in-lync-server-2013"></a><span data-ttu-id="18925-103">Configuración de un nodo de monitor para usar la autenticación de credenciales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="18925-103">Configuring a watcher node to use credential authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="18925-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="18925-104">

<span> </span></span></span>

<span data-ttu-id="18925-105">_**Última modificación del tema:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="18925-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="18925-106">Si el equipo del nodo de observador se encuentra fuera de la red perimetral, debe seguir un procedimiento ligeramente diferente para configurar ese nodo de observador de forma que se ejecuten las transacciones sintéticas.</span><span class="sxs-lookup"><span data-stu-id="18925-106">If your watcher node computer lies outside the perimeter network, then you must follow a slightly different procedure in order to configure that watcher node to run synthetic transactions.</span></span> <span data-ttu-id="18925-107">En concreto, no debe crear un grupo de aplicaciones de confianza ni una aplicación de confianza, y debe instalar un certificado que permita al nodo de monitor enviar alertas a un equipo dentro de la red perimetral.</span><span class="sxs-lookup"><span data-stu-id="18925-107">Specifically, you should not create a trusted application pool and a trusted application, and you must install a certificate that enables the watcher node to send alerts to a computer inside the perimeter network.</span></span> <span data-ttu-id="18925-108">Esto significa que tendrá que completar dos tareas independientes:</span><span class="sxs-lookup"><span data-stu-id="18925-108">This means that you will need to complete two separate tasks:</span></span>

  - <span data-ttu-id="18925-109">Actualizar la pertenencia al grupo administradores de RTC locales de solo lectura del equipo</span><span class="sxs-lookup"><span data-stu-id="18925-109">Update the membership in the computer's RTC Local Read-only Administrators Group</span></span>

  - <span data-ttu-id="18925-110">Instalar los archivos de configuración del nodo de monitor</span><span class="sxs-lookup"><span data-stu-id="18925-110">Install the watcher node configuration files</span></span>

<div>

## <a name="updating-membership-in-the-rtc-local-read-only-administrators-group"></a><span data-ttu-id="18925-111">Actualización de la pertenencia al grupo RTC local Read-Only administradores</span><span class="sxs-lookup"><span data-stu-id="18925-111">Updating Membership in the RTC Local Read-Only Administrators Group</span></span>

<span data-ttu-id="18925-112">Si el nodo de monitor se encuentra fuera de la red perimetral, debe agregar la cuenta de servicio de red al grupo de administradores RTC local de solo lectura en el equipo del nodo de supervisor.</span><span class="sxs-lookup"><span data-stu-id="18925-112">If your watcher node lies outside the perimeter network, you must add the Network Service account to the RTC Local Read-only Administrators group on the watcher node computer.</span></span> <span data-ttu-id="18925-113">Para ello, complete el siguiente procedimiento en el nodo Watcher (monitor):</span><span class="sxs-lookup"><span data-stu-id="18925-113">To do this, complete the following procedure on the watcher node:</span></span>

1.  <span data-ttu-id="18925-114">Haga clic en **Inicio**, haga clic con el botón secundario en **equipo** y, a continuación, haga clic en **administrar**.</span><span class="sxs-lookup"><span data-stu-id="18925-114">Click **Start**, right-click **Computer**, and then click **Manage**.</span></span>

2.  <span data-ttu-id="18925-115">En Administrador del servidor, expanda **configuración**, expanda **usuarios locales y grupos** y, a continuación, haga clic en **grupos**.</span><span class="sxs-lookup"><span data-stu-id="18925-115">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="18925-116">En el panel grupos, haga doble clic en **RTC local-Only Administrators**.</span><span class="sxs-lookup"><span data-stu-id="18925-116">In the Groups pane, double-click **RTC Local Read-only Administrators**.</span></span>

4.  <span data-ttu-id="18925-117">En el cuadro de diálogo **propiedades de administrador de solo lectura local de RTC** , haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="18925-117">In the **RTC Local Read-only Administrators Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="18925-118">En el cuadro de diálogo **Seleccionar usuarios, equipos, cuentas de servicio o grupos** , haga clic en **ubicaciones**.</span><span class="sxs-lookup"><span data-stu-id="18925-118">In the **Select Users, Computers, Service Accounts, or Groups** dialog box, click **Locations**.</span></span>

6.  <span data-ttu-id="18925-119">En el cuadro de diálogo **ubicaciones** , seleccione el nombre del equipo del nodo de monitor y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="18925-119">In the **Locations** dialog box, select the name of the watcher node computer, and then click **OK**.</span></span>

7.  <span data-ttu-id="18925-120">En el cuadro **Escriba los nombres de objeto que desea seleccionar** , escriba **servicio de red** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="18925-120">In the **Enter object names to select** box, type **Network Service**, and then click **OK**.</span></span>

8.  <span data-ttu-id="18925-121">En el cuadro de diálogo **propiedades de administradores locales de solo lectura** , haga clic en **Aceptar** y, a continuación, cierre el **Administrador del servidor**.</span><span class="sxs-lookup"><span data-stu-id="18925-121">In the **RTC Local Read-only Administrators Properties** dialog box, click **OK**, and then close **Server Manager**.</span></span>

<span data-ttu-id="18925-122">Reinicie el equipo del nodo de observador.</span><span class="sxs-lookup"><span data-stu-id="18925-122">Restart the watcher node computer.</span></span>

</div>

<div>

## <a name="installing-the-watcher-node-configuration-files"></a><span data-ttu-id="18925-123">Instalar los archivos de configuración del nodo de monitor</span><span class="sxs-lookup"><span data-stu-id="18925-123">Installing the Watcher Node Configuration Files</span></span>

<span data-ttu-id="18925-124">Una vez que se haya reiniciado el nodo de supervisor, el siguiente paso es ejecutar el archivo Watchernode.msi.</span><span class="sxs-lookup"><span data-stu-id="18925-124">After the watcher node computer has restarted, your next step is to run the file Watchernode.msi.</span></span> <span data-ttu-id="18925-125">Para ejecutar este archivo, abra el shell de administración de Lync Server 2013 haciendo clic en **Inicio**, haga clic en **todos los programas**, en **Lync Server 2013** y, por último, en el **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="18925-125">To run this file, open the Lync Server 2013 Management Shell by clicking **Start**, clicking **All Programs**, clicking **Lync Server 2013**, and then clicking **Lync Server Management Shell**.</span></span> <span data-ttu-id="18925-126">En el shell de administración de Lync Server, escriba el siguiente comando y, a continuación, presione Entrar (Asegúrese de especificar la ruta de acceso real a su copia de Watchernode.msi):</span><span class="sxs-lookup"><span data-stu-id="18925-126">In the Lync Server Management Shell, type the following command and then press ENTER (be sure and specify the actual path to your copy of Watchernode.msi):</span></span>

    C:\Tools\Watchernode.msi Authentication=Negotiate

<div>


> [!NOTE]  
> <span data-ttu-id="18925-127">Como se indicó anteriormente, Watchernode.msi también se puede ejecutar desde una ventana de comandos.</span><span class="sxs-lookup"><span data-stu-id="18925-127">As noted previously, Watchernode.msi can also be run from a command window.</span></span> <span data-ttu-id="18925-128">Para abrir una ventana Comandos, haga clic en <STRONG>Inicio</STRONG>, haga clic con el botón secundario en <STRONG>Símbolo del sistema</STRONG> y, a continuación, haga clic en <STRONG>Ejecutar como administrador</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="18925-128">To open a command window, click <STRONG>Start</STRONG>, right-click <STRONG>Command Prompt</STRONG>, and then click <STRONG>Run as administrator</STRONG>.</span></span> <span data-ttu-id="18925-129">Cuando se abra la ventana de comandos, escriba el mismo comando que se mostró anteriormente.</span><span class="sxs-lookup"><span data-stu-id="18925-129">When the command window opens, type the same command as shown earlier.</span></span>



</div>

<span data-ttu-id="18925-p105">El modo Negotiate se usa en cualquier momento que el nodo de monitor no se puede configurar como un grupo de servidores de aplicaciones de confianza. En este modo, los administradores tendrán que administrar contraseñas de usuario de prueba en el nodo de monitor.</span><span class="sxs-lookup"><span data-stu-id="18925-p105">The Negotiate mode is used any time the watcher node cannot be set up as a trusted application pool. In this mode, administrators will need to manage test user passwords on the watcher node.</span></span>

<span data-ttu-id="18925-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="18925-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

