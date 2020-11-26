---
title: 'Restaurar un servidor de servicios de fondo de la edición empresarial duplicada: reflejo'
description: Restaurar un servidor de servicios de fondo de empresa duplicada.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a mirrored Enterprise Edition Back End Server - mirror
ms:assetid: 4b3c8eae-6f1f-4377-b39b-6699e725c517
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945626(v=OCS.15)
ms:contentKeyID: 51541471
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 011c0aaa10ffed6fef7d579dbc16993fd3341070
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436240"
---
# <a name="restoring-a-mirrored-enterprise-edition-back-end-server-in-lync-server-2013---mirror"></a><span data-ttu-id="e6c0c-103">Restaurar un servidor de servicios de fondo de la edición empresarial duplicada en Lync Server 2013-Mirror</span><span class="sxs-lookup"><span data-stu-id="e6c0c-103">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e6c0c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e6c0c-104">

<span> </span></span></span>

<span data-ttu-id="e6c0c-105">_**Última modificación del tema:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="e6c0c-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="e6c0c-106">Si tiene un servidor de servicios de fondo Enterprise Edition en una configuración reflejada y solo se produce un error en el reflejo, siga los procedimientos descritos en esta sección.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-106">If you have an Enterprise Edition Back End Server in a mirrored configuration and only the mirror fails, follow the procedures in this section.</span></span> <span data-ttu-id="e6c0c-107">Si la base de datos principal y el reflejo fallan, consulte [restaurar un servidor de servicios de fondo de la edición empresarial en Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md).</span><span class="sxs-lookup"><span data-stu-id="e6c0c-107">If both the primary database and mirror fail, see [Restoring an Enterprise Edition Back End Server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md).</span></span> <span data-ttu-id="e6c0c-108">Si solo se produce un error en el principal, vea [restaurar un servidor back-end de empresa duplicada en Lync server 2013-Primary](lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md).</span><span class="sxs-lookup"><span data-stu-id="e6c0c-108">If only the primary fails, see [Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - primary](lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md).</span></span> <span data-ttu-id="e6c0c-109">Si se produce un error en la base de datos que hospeda el almacén de administración central, consulte [restaurar el servidor que hospeda el almacén de administración central en Lync server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span><span class="sxs-lookup"><span data-stu-id="e6c0c-109">If the database hosting the Central Management store fails, see [Restoring the server hosting the Central Management store in Lync Server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span></span> <span data-ttu-id="e6c0c-110">Si se produce un error en un servidor miembro de Enterprise Edition que no es el servidor back-end, consulte [restaurar un servidor miembro de Enterprise Edition en Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span><span class="sxs-lookup"><span data-stu-id="e6c0c-110">If an Enterprise Edition member server that is not the Back End Server fails, see [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

<span data-ttu-id="e6c0c-111">Le recomendamos que tome una copia de la imagen del sistema antes de comenzar la restauración.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-111">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="e6c0c-112">Puede usar esta imagen como punto de reversión, en caso de que algo falle durante la restauración.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-112">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="e6c0c-113">Es posible que desee tomar la copia de la imagen después de instalar el sistema operativo y SQL Server, y restaurar o volver a inscribir los certificados.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-113">You might want to take the image copy after you install the operating system and SQL Server, and restore or reenroll the certificates.</span></span>

<div>

## <a name="to-restore-an-enterprise-edition-back-end-server-mirror-database"></a><span data-ttu-id="e6c0c-114">Para restaurar una base de datos reflejada del servidor de servicios de fondo de la edición Enterprise</span><span class="sxs-lookup"><span data-stu-id="e6c0c-114">To restore an Enterprise Edition Back End Server Mirror Database</span></span>

1.  <span data-ttu-id="e6c0c-115">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins, inicie sesión en un servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-115">From a user account that is a member of the RTCUniversalServerAdmins group, log on to a Front End Server.</span></span>

2.  <span data-ttu-id="e6c0c-116">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e6c0c-117">Desinstalar reflejo.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-117">Uninstall mirroring.</span></span> <span data-ttu-id="e6c0c-118">En primer lugar, escriba el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e6c0c-118">First, type the following cmdlet:</span></span>
    
        Uninstall -CsMirrorDatabase -DatabaseType User -SqlServerFqdn <PrimaryServerFqdn> -SqlInstanceName <SQLInstance> -verbose
    
    <span data-ttu-id="e6c0c-119">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e6c0c-119">For example:</span></span>
    
        Uninstall -CsMirrorDatabase -DatabaseType User -SqlServerFqdn server4.contoso.com -SqlInstanceName archinst -verbose
    
    <span data-ttu-id="e6c0c-120">Haga esto para todos los tipos de base de datos en este servidor.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-120">Do this for all database types on this server.</span></span>

4.  <span data-ttu-id="e6c0c-121">Cree un servidor limpio o nuevo que tenga el mismo nombre de dominio completo (FQDN) (DB1.contoso.com) que el equipo que ha fallado, instale el sistema operativo y, a continuación, restaure o vuelva a inscribir los certificados.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-121">Create a clean or new server that has the same fully qualified domain name (FQDN) (DB1.contoso.com) as the failed computer, install the operating system, and then restore or reenroll the certificates.</span></span> <span data-ttu-id="e6c0c-122">Este servidor funcionará como el nuevo reflejo.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-122">This server will function as the new mirror.</span></span>

5.  <span data-ttu-id="e6c0c-123">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins, inicie sesión en el nuevo servidor.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-123">From a user account that is a member of the RTCUniversalServerAdmins group, log on to the new server.</span></span>

6.  <span data-ttu-id="e6c0c-124">Instale SQL Server 2012 o SQL Server 2008 R2, manteniendo los mismos nombres de instancia que antes del error.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-124">Install SQL Server 2012 or SQL Server 2008 R2, keeping the instance names the same as before the failure.</span></span>

7.  <span data-ttu-id="e6c0c-125">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins, inicie sesión en un servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-125">From a user account that is a member of the RTCUniversalServerAdmins group, log on to a Front End Server.</span></span>

8.  <span data-ttu-id="e6c0c-126">Use el generador de topología para instalar la base de datos de reflejo.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-126">Use Topology Builder to install the mirror database.</span></span> <span data-ttu-id="e6c0c-127">Realice lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e6c0c-127">Perform the following:</span></span>
    
      - <span data-ttu-id="e6c0c-128">Iniciar generador de topología: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **generador de topología de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-128">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="e6c0c-129">Haga clic con el botón secundario en el nodo de Lync Server 2013, haga clic en **topología** y, a continuación, en **instalar base de datos**.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-129">Right-click the Lync Server 2013 node, click **Topology**, and then click **Install Database**.</span></span>
    
      - <span data-ttu-id="e6c0c-130">Siga el Asistente para la **instalación de bases de datos** .</span><span class="sxs-lookup"><span data-stu-id="e6c0c-130">Follow the **Install Database** wizard.</span></span> <span data-ttu-id="e6c0c-131">En la página **crear bases de datos** , seleccione las bases de datos que desea volver a crear.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-131">On the **Create databases** page, select the databases that you want to recreate.</span></span>
    
      - <span data-ttu-id="e6c0c-132">Siga el asistente hasta que aparezca un mensaje de creación de una **base de datos de reflejo** .</span><span class="sxs-lookup"><span data-stu-id="e6c0c-132">Follow the wizard until a prompt of **Create Mirror Database** appears.</span></span> <span data-ttu-id="e6c0c-133">Seleccione la base de datos que desea instalar y complete este proceso.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-133">Select the database that you want to install and complete this process.</span></span>
        
        <div>
        

        > [!TIP]
        > <span data-ttu-id="e6c0c-134">En lugar de ejecutar el generador de topologías, puede usar el cmdlet <STRONG>install-CsMirrorDatabase</STRONG> para configurar el reflejo.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-134">Instead of running Topology Builder, you can use the <STRONG>Install-CsMirrorDatabase</STRONG> cmdlet to configure mirroring.</span></span> <span data-ttu-id="e6c0c-135">Para obtener más información, consulte la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e6c0c-135">For details, see the Lync Server Management Shell documentation.</span></span>

        
        <span data-ttu-id="e6c0c-136"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e6c0c-136"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

