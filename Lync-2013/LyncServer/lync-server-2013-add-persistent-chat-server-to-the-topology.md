---
title: 'Lync Server 2013: Agregar un servidor de chat persistente a la topología'
description: 'Lync Server 2013: agregar un servidor de chat persistente a la topología.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add Persistent Chat Server to the topology
ms:assetid: 8389b307-8c17-4e45-b3b5-5dc9fcfc2ffb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205049(v=OCS.15)
ms:contentKeyID: 48184682
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0321978ce4a0c7381cf2915030267645931f572b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439271"
---
# <a name="add-persistent-chat-server-to-the-topology-in-lync-server-2013"></a><span data-ttu-id="e6f4d-103">Agregar un servidor de chat persistente a la topología en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e6f4d-103">Add Persistent Chat Server to the topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e6f4d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e6f4d-104">

<span> </span></span></span>

<span data-ttu-id="e6f4d-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="e6f4d-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="e6f4d-106">Debe incorporar Lync Server 2013, la compatibilidad con el servidor de chat persistente en su topología antes de configurar su implementación para que admita el servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-106">You must incorporate Lync Server 2013, Persistent Chat Server support in your topology before you can configure your deployment to support Persistent Chat Server.</span></span> <span data-ttu-id="e6f4d-107">La información de este tema describe cómo usar el generador de topologías para agregar la compatibilidad con el servidor de chat persistente a su topología existente.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-107">The information in this topic describes how to use Topology Builder to add Persistent Chat Server support to your existing topology.</span></span>

<div>

## <a name="to-add-persistent-chat-server-to-a-topology"></a><span data-ttu-id="e6f4d-108">Para agregar un servidor de chat persistente a una topología</span><span class="sxs-lookup"><span data-stu-id="e6f4d-108">To add Persistent Chat Server to a topology</span></span>

<span data-ttu-id="e6f4d-109">Siga estos pasos para instalar un único grupo de servidores de chat persistente sin una configuración de recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-109">Perform the following steps for installing a single Persistent Chat Server pool without a disaster recovery configuration.</span></span> <span data-ttu-id="e6f4d-110">Para configurar un grupo de servidores de chat persistente ampliado para una alta disponibilidad y recuperación ante desastres, vea [configurar el servidor de chat persistente para una alta disponibilidad y recuperación ante desastres en Lync Server 2013](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-110">For configuring a stretched Persistent Chat Server pool for high availability and disaster recovery, see [Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) in the Deployment documentation.</span></span>

<span data-ttu-id="e6f4d-111">Para implementar varios grupos de servidores de chat persistentes, repita el mismo proceso para cada grupo.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-111">To deploy multiple Persistent Chat Server pools, repeat the same process for each pool.</span></span>

1.  <span data-ttu-id="e6f4d-112">En un equipo que ejecute Lync Server 2013 o en el que estén instaladas las herramientas administrativas de Lync Server, inicie sesión con una cuenta que sea miembro del grupo usuarios locales (o una cuenta con derechos de usuario equivalentes).</span><span class="sxs-lookup"><span data-stu-id="e6f4d-112">On a computer that is running Lync Server 2013 or on which the Lync Server administrative tools are installed, log on using an account that is a member of the local Users group (or an account with equivalent user rights).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e6f4d-113">Puede definir una topología con una cuenta que sea miembro del grupo usuarios locales, pero para publicar una topología, que es necesaria para instalar un servidor de Lync Server 2013, debe usar una cuenta que sea miembro del grupo de <STRONG>administradores de dominio</STRONG> y el grupo <STRONG>RTCUniversalServerAdmins</STRONG> , y que tenga permisos de control total (es decir, leer, escribir y modificar) en el almacén de archivos que va a usar para el almacén de archivos del servidor de chat persistente (es decir, para que el generador de topología pueda configurar las DACL obligatorias) o una cuenta con derechos equivalentes.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-113">You can define a topology by using an account that is a member of the local Users group, but to publish a topology, which is required to install a Lync Server 2013 server, you must use an account that is a member of the <STRONG>Domain Admins</STRONG> group and the <STRONG>RTCUniversalServerAdmins</STRONG> group, and that has full control permissions (that is, read, write, and modify) on the file store that you are going to use for the Persistent Chat Server file store (that is, so that Topology Builder can configure the required DACLs), or an account with equivalent rights.</span></span>

    
    </div>

2.  <span data-ttu-id="e6f4d-114">Iniciar el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-114">Start Topology Builder.</span></span>

3.  <span data-ttu-id="e6f4d-115">En el árbol de consola, vaya al nodo **grupos de chats persistentes** y expándalo para seleccionar un grupo de servidores de chat persistente, o haga clic con el botón derecho en el nodo y seleccione **nuevo grupo de chats persistentes**.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-115">In the console tree, navigate to the **Persistent Chat Pools** node and expand it to select a Persistent Chat Server pool, or right-click the node and select **New Persistent Chat Pool**.</span></span> <span data-ttu-id="e6f4d-116">You must define the pool’s fully qualified domain name (FQDN), and indicate whether the pool will be a single-server pool or multiple-server pool deployment.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-116">You must define the pool’s fully qualified domain name (FQDN), and indicate whether the pool will be a single-server pool or multiple-server pool deployment.</span></span>
    
    <span data-ttu-id="e6f4d-117">Puede elegir un **Grupo de varios equipos** o **Grupo de un solo equipo**.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-117">You can choose a **Multiple Computer Pool** or a **Single Computer Pool**.</span></span> <span data-ttu-id="e6f4d-118">Elija el primero si está planeando tener más de un servidor de usuario de chat persistente en el grupo de servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-118">Choose the former if you are planning to have more than one Persistent Chat Server Front End Server in your Persistent Chat Server pool.</span></span> <span data-ttu-id="e6f4d-119">Realice esta elección ahora, porque después de crear un grupo de un solo equipo no le podrá agregar servidores adicionales más adelante.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-119">Make this choice now, or at a later point, because after you create a single computer pool, you cannot add additional servers to it later.</span></span> <span data-ttu-id="e6f4d-120">Si elige un grupo de varios equipos, escriba los nombres de los servidores de cliente de la conversación persistente que forman el grupo.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-120">If you choose a multiple computer pool, enter the names of the individual Persistent Chat Server Front End Servers that comprise the pool.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e6f4d-121">Si el rol de servidor de chat persistente se instala en un servidor de Lync Server 2013 &nbsp; Standard Edition, el FQDN debe coincidir con el FQDN del servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-121">If the Persistent Chat Server role is being installed on a Lync Server 2013&nbsp;Standard Edition server, the FQDN needs to match the FQDN of the Standard Edition server.</span></span>

    
    </div>

4.  <span data-ttu-id="e6f4d-122">Defina un **nombre para mostrar** simple para el grupo de servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-122">Define a simple **Display Name** for the Persistent Chat Server pool.</span></span> <span data-ttu-id="e6f4d-123">El nombre para mostrar puede ser usado por clientes personalizados, especialmente cuando hay varios grupos de servidores de chat persistentes, para diferenciar las habitaciones.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-123">The display name can be used by custom clients, particularly when there are multiple Persistent Chat Server pools, to differentiate rooms.</span></span>

5.  <span data-ttu-id="e6f4d-124">Defina el puerto que usa el servidor de chat persistente para comunicarse con los servidores front-end de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-124">Define the port used by the Persistent Chat Server to communicate with Lync Server Front End Servers.</span></span> <span data-ttu-id="e6f4d-125">El puerto predeterminado es 5041.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-125">The default port is 5041.</span></span>

6.  <span data-ttu-id="e6f4d-126">Si su organización requiere compatibilidad con el cumplimiento, seleccione la casilla **Habilitar cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-126">If your organization requires compliance support, select the **Enable compliance** check box.</span></span> <span data-ttu-id="e6f4d-127">Si se elige, el servicio de cumplimiento de servidor de chat persistente se instala en el mismo equipo que el servidor de front-end del servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-127">If chosen, the Persistent Chat Server Compliance service is installed on the same computer as the Persistent Chat Server Front End Server.</span></span> <span data-ttu-id="e6f4d-128">Se le pedirá que seleccione un servidor Back End SQL Server para el cumplimiento del servidor de chat persistente más adelante.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-128">You are prompted to select a SQL Server Back End Server for Persistent Chat Server Compliance later.</span></span>

7.  <span data-ttu-id="e6f4d-129">Asigne afinidad de sitio para el grupo de servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-129">Assign site affinity for the Persistent Chat Server pool.</span></span> <span data-ttu-id="e6f4d-130">Active la casilla **usar este grupo como predeterminado para \<SiteName\> el sitio** o **use este grupo como predeterminado para que todos los sitios** designen este grupo de servidores de chat persistente como el grupo predeterminado para el sitio actual o todos los sitios.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-130">Select the **Use this pool as default for site \<SiteName\>** check box or **Use this pool as default for all sites** to designate this Persistent Chat Server pool as the default pool for the current site or all sites.</span></span> <span data-ttu-id="e6f4d-131">Cuando se usa el cliente de Lync 2013 para crear y administrar salas, la experiencia de creación y administración de la sala usa el grupo predeterminado asociado al sitio del usuario para que pueda dirigir las operaciones de administración y creación de salas a ese grupo.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-131">When the Lync 2013 client is used to create and manage rooms, the default pool associated with the user’s site is used by the room creation and management experience so that it can route room creation and management operations to that pool.</span></span> <span data-ttu-id="e6f4d-132">Esto solo se aplica cuando se han implementado varios grupos de servidores de chat persistentes y desea usar las características de creación y administración de la sala de un servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-132">This only applies when you have multiple Persistent Chat Server pools deployed, and want to use the room creation and management features of Persistent Chat Server.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e6f4d-133">Puede personalizar las características de creación y administración de la sala con el kit de desarrollo de software (SDK) del servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-133">You can customize the room creation and management features using the Persistent Chat Server Software Development Kit (SDK).</span></span><BR><span data-ttu-id="e6f4d-134">Para obtener más información sobre cómo configurar las bases de datos de copia de seguridad de SQL Server para la recuperación ante desastres, vea <A href="lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md">configurar el servidor de chat persistente para una alta disponibilidad y recuperación ante desastres en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-134">For details about how to configure SQL Server backup databases for disaster recovery, see <A href="lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    </div>

8.  <span data-ttu-id="e6f4d-135">Defina el **almacén SQL para el back-end del servidor de chat persistente (donde se almacena el contenido del salón de chat)** mediante uno de los siguientes procedimientos:</span><span class="sxs-lookup"><span data-stu-id="e6f4d-135">Define the **SQL store for the Persistent Chat Server Back End (where chat room content is stored)** by doing one of the following:</span></span>
    
      - <span data-ttu-id="e6f4d-136">Para usar una base de datos de SQL Server existente, en la lista desplegable, haga clic en el nombre de la base de datos de SQL Server que desea usar.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-136">To use an existing SQL Server database, in the drop-down list, click the name of the SQL Server database that you want to use.</span></span>
    
      - <span data-ttu-id="e6f4d-137">Para especificar una nueva base de datos de SQL Server, haga clic en **nuevo** y, en **definir nueva tienda SQL**, realice lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e6f4d-137">To specify a new SQL Server database, click **New**, and in **Define New SQL Store**, perform the following:</span></span>
    
    <!-- end list -->
    
      - <span data-ttu-id="e6f4d-138">En **FQDN de SQL Server**, especifique el nombre completo del servidor SQL Server en el que desea crear la nueva base de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-138">In **SQL Server FQDN**, specify the FQDN of the SQL Server on which you want to create the new SQL Server database.</span></span>
    
      - <span data-ttu-id="e6f4d-139">Puede seleccionar **Instancia predeterminada** para utilizar la instancia predeterminada, o bien, para especificar una instancia diferente, seleccione **Instancia con nombre** y, luego, especifique la instancia que desee utilizar.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-139">Either select **Default Instance** to use the default instance or, to specify a different instance, select **Named Instance**, and specify the instance that you want to use.</span></span>

9.  <span data-ttu-id="e6f4d-140">Defina la base de datos de cumplimiento de SQL Server si ha habilitado la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-140">Define the SQL Server compliance database if you enabled Compliance.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e6f4d-141">Para obtener más información sobre cómo configurar espejos de SQL Server para una alta disponibilidad de la base de datos del servidor de chat persistente y la base de datos de cumplimiento del servidor de chat persistente, vea <A href="lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md">configurar el servidor de chat persistente para una alta disponibilidad y recuperación ante desastres en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-141">For details about how to configure SQL Server mirrors for high availability for the Persistent Chat Server database and the Persistent Chat Server compliance database, see <A href="lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    </div>

10. <span data-ttu-id="e6f4d-142">Defina el almacén de archivos.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-142">Define the file store.</span></span> <span data-ttu-id="e6f4d-143">Un almacén de archivos es una carpeta en la que se almacena una copia de cualquier archivo cargado al repositorio de archivos (por ejemplo, el almacenamiento de datos adjuntos de archivos publicados en un salón de chat).</span><span class="sxs-lookup"><span data-stu-id="e6f4d-143">A file store is a folder where a copy of any file uploaded to the file repository is stored (for example, storing file attachments posted to a chat room).</span></span> <span data-ttu-id="e6f4d-144">En el caso de una topología de servidor de chat persistente de varios servidores, debe ser una ruta de acceso UNC (Convención de nomenclatura universal); para una topología de servidor de chat persistente de un solo servidor, puede ser una ruta de acceso de archivo local.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-144">In the case of a multiple-server Persistent Chat Server topology, this must be a Universal Naming Convention (UNC) path; and for a single-server Persistent Chat Server topology, it can be a local file path.</span></span>
    
    <span data-ttu-id="e6f4d-145">Para utilizar un almacén de archivos existente, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e6f4d-145">To use an existing file store, perform the following steps:</span></span>
    
      - <span data-ttu-id="e6f4d-146">En **FQDN del servidor de archivos**, especifique el FQDN del almacén de archivos en el que desea crear el nuevo almacén de archivos.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-146">In **File Server FQDN**, specify the FQDN of the file store on which you want to create the new file store.</span></span>
    
      - <span data-ttu-id="e6f4d-147">En **Recurso compartido de archivos**, especifique el almacén de archivos que desee utilizar.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-147">In **File Share**, specify the file store that you want to use.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e6f4d-148">Puede definir el almacén de archivos en el generador de topología antes de crear el almacén de archivos, pero debe crear el almacén de archivos en la ubicación definida que defina antes de publicar la topología.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-148">You can define the file store in Topology Builder before you create the file store, but you must create the file store in the defined location you define before you publish the topology.</span></span>

    
    </div>

11. <span data-ttu-id="e6f4d-149">Seleccione el grupo de servidores front-end que se usará como próximo salto para este grupo de servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-149">Select the Front End Server pool to be used as a next hop for this Persistent Chat Server pool.</span></span> <span data-ttu-id="e6f4d-150">Este es el grupo de servidores front-end que podrá enrutar solicitudes de servidor de chat persistentes a este grupo.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-150">This is the Front End Server pool that will be able to route Persistent Chat Server requests to this pool.</span></span>

12. <span data-ttu-id="e6f4d-151">Para guardar la configuración, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-151">To save the configuration, click **Finish**.</span></span> <span data-ttu-id="e6f4d-152">El grupo de servidores de chat persistente aparece en el generador de topología junto con la configuración específica de la agrupación.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-152">The Persistent Chat Server pool appears in Topology Builder accompanied by your specific pool settings.</span></span>
    
    <span data-ttu-id="e6f4d-153">Para publicar su topología actualizada a la que tiene el servidor de chat persistente, vea [publicar la topología actualizada en Lync server 2013](lync-server-2013-publish-the-updated-topology.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-153">To now publish your updated topology to which you’ve Persistent Chat Server, see [Publish the updated topology in Lync Server 2013](lync-server-2013-publish-the-updated-topology.md) in the Deployment documentation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e6f4d-154">Con el generador de topología ya abierto, puede continuar con el paso 3 en <A href="lync-server-2013-publish-the-updated-topology.md">publicar la topología actualizada en Lync Server 2013</A> para empezar a publicar su topología actualizada.</span><span class="sxs-lookup"><span data-stu-id="e6f4d-154">With Topology Builder already open, you can proceed to step 3 in <A href="lync-server-2013-publish-the-updated-topology.md">Publish the updated topology in Lync Server 2013</A> to begin publishing your updated topology.</span></span>

    
    <span data-ttu-id="e6f4d-155"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e6f4d-155"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

