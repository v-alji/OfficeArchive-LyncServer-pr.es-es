---
title: 'Lync Server 2013: Configurar opciones de servidor de chat persistentes a escala global o para grupos de servidores de chat persistentes'
description: 'Lync Server 2013: Configure las opciones del servidor de chat persistentes globalmente o para el grupo de servidores de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Persistent Chat Server options globally or for Persistent Chat Server pool
ms:assetid: 1e8d5245-cd58-4aad-9a1c-35b24189bc40
ms:mtpsurl: https://technet.microsoft.com/library/JJ204731(v=OCS.15)
ms:contentKeyID: 48183581
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0e0e26fc8719f9aa5f153a7962df70ee7237b980
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433825"
---
# <a name="configure-persistent-chat-server-options-globally-or-for-persistent-chat-server-pool-in-lync-server-2013"></a><span data-ttu-id="fffec-103">Configurar opciones de servidor de chat persistentes a escala global o para grupos de servidores de chat persistentes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fffec-103">Configure Persistent Chat Server options globally or for Persistent Chat Server pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fffec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fffec-104">

<span> </span></span></span>

<span data-ttu-id="fffec-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="fffec-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="fffec-106">En el panel de control de Lync Server 2013, puede usar la sección **configuración de chat** persistente de la página **chat persistente** para configurar las opciones de chat de forma global, donde se aplica a todos los grupos de servidores de chat persistentes o a un grupo de servidores de chat persistente específico.</span><span class="sxs-lookup"><span data-stu-id="fffec-106">In Lync Server 2013 Control Panel, you can use the **Persistent Chat Configuration** section of the **Persistent Chat** page to configure Persistent Chat settings globally where it applies to all Persistent Chat Server pools, or for a specific Persistent Chat Server pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fffec-107">Para configurar y usar el servidor de chat persistente, primero debe usar topología Builder para agregar la compatibilidad con el servidor de chat persistente a la topología y, a continuación, publicar la topología.</span><span class="sxs-lookup"><span data-stu-id="fffec-107">To configure and use Persistent Chat Server, you must first use Topology Builder to add Persistent Chat Server support to the topology, and then publish the topology.</span></span> <span data-ttu-id="fffec-108">Para obtener más información, vea <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Agregar un servidor de chat persistente a su implementación en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="fffec-108">For details, see <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adding Persistent Chat Server to your deployment in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-configure-persistent-chat-options-globally"></a><span data-ttu-id="fffec-109">Para configurar las opciones de chat persistentes de forma global</span><span class="sxs-lookup"><span data-stu-id="fffec-109">To configure Persistent Chat options globally</span></span>

1.  <span data-ttu-id="fffec-110">Desde una cuenta de usuario que se asigne al rol CsPersistentChatAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="fffec-110">From a user account that is assigned to the CsPersistentChatAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fffec-111">En el menú **Inicio** , seleccione el panel de control de Lync Server o abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador.</span><span class="sxs-lookup"><span data-stu-id="fffec-111">From the **Start** menu, select the Lync Server Control Panel or open a browser window, and then enter the Admin URL.</span></span> <span data-ttu-id="fffec-112">Para más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="fffec-112">For details about the different methods that you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="fffec-113">También puede usar los cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fffec-113">You can also use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="fffec-114">Para obtener más información, vea <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">configuración del servidor de chat persistente mediante cmdlets de Windows PowerShell</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="fffec-114">For details, see <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</A> in the Deployment documentation.</span></span>

    
    </div>

3.  <span data-ttu-id="fffec-115">En la barra de navegación izquierda, haga clic en **Chat persistente** y, luego, en **Configuración de chat persistente**.</span><span class="sxs-lookup"><span data-stu-id="fffec-115">In the left navigation bar, click **Persistent Chat**, and then click **Persistent Chat Configuration**.</span></span>

4.  <span data-ttu-id="fffec-116">En la página **configuración de chat persistente** , haga clic en **nuevo** y, a continuación, en **configuración del sitio**.</span><span class="sxs-lookup"><span data-stu-id="fffec-116">On the **Persistent Chat Configuration** page, click **New,** and then click **Site configuration**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="fffec-117">Elija esta opción si quiere que la configuración se aplique a todos los grupos de servidores de chat persistentes implementados en el sitio.</span><span class="sxs-lookup"><span data-stu-id="fffec-117">Choose this option if you want the configuration to be applied to all Persistent Chat Server pools deployed in the site.</span></span> <span data-ttu-id="fffec-118">Haga clic en <STRONG>configuración del grupo</STRONG> si quiere que la configuración se aplique a un grupo de servidores de chat persistente específico.</span><span class="sxs-lookup"><span data-stu-id="fffec-118">Click <STRONG>Pool Configuration</STRONG> if you want the configuration to be applied to a specific Persistent Chat Server pool.</span></span>

    
    </div>

5.  <span data-ttu-id="fffec-119">En **seleccionar un sitio**, seleccione el sitio que se va a configurar para la configuración del sitio del servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="fffec-119">In **Select a Site**, select the site to be configured for the Persistent Chat Server site configuration.</span></span>

6.  <span data-ttu-id="fffec-120">En **Nueva configuración de chat persistente**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fffec-120">In **New Persistent Chat Configuration**, do the following:</span></span>
    
      - <span data-ttu-id="fffec-p105">En **Nombre**, especifique un nombre para los nuevos parámetros de configuración. El nombre de sitio ya existe de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fffec-p105">In **Name**, specify a name for the new configuration settings. By default, the site name already exists.</span></span>
    
      - <span data-ttu-id="fffec-p106">En **Historial de chat predeterminado**, defina la cantidad de mensajes de chat que se va a procesar para cada salón tras la primera solicitud. La cantidad predeterminada es 30. Esta es la configuración global y los administradores pueden deshabilitar el historial de chat por categoría.</span><span class="sxs-lookup"><span data-stu-id="fffec-p106">In **Default chat history**, define the number of chat messages that will be processed for each room upon first request. By default, the number is 30. This is the global default, and administrators can disable chat history per category.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="fffec-126">El servidor de chat persistente guardará estos mensajes en la memoria caché, por lo que, si aumenta este número, se almacenarán en caché más mensajes.</span><span class="sxs-lookup"><span data-stu-id="fffec-126">Persistent Chat Server will cache these messages in memory, so if you increase this number, more messages will be cached.</span></span> <span data-ttu-id="fffec-127">El acceso al contenido del historial siempre se encuentra disponible a través de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fffec-127">You can always access historical content by search.</span></span> <span data-ttu-id="fffec-128">La cantidad predeterminada solo indica la cantidad máxima de mensajes que ve inicialmente cuando se conecta a un salón de chat.</span><span class="sxs-lookup"><span data-stu-id="fffec-128">The default number simply determines the maximum number of messages that you initially see when connecting to a chat room.</span></span>

        
        </div>
    
      - <span data-ttu-id="fffec-p108">En **Tamaño máximo de archivo (KB)**, seleccione el tamaño máximo del archivo de cada historial de chat. La cantidad predeterminada es 20 MB (20 000 KB). Este es el tamaño máximo de archivo que puede cargarse a cualquier salón de chat del sistema (en el que las cargas de archivos estén habilitadas por su correspondiente parámetro de **Categoría**).</span><span class="sxs-lookup"><span data-stu-id="fffec-p108">In **Maximum file size (KB)**, select the maximum file size of each chat history. By default, the number is 20 MB (20,000 KB). This is the maximum size for a file that can be uploaded to any chat room in the system (for which file uploads are enabled by its corresponding **Category** setting).</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="fffec-132">Esta configuración se aplica en el servidor porque las aplicaciones personalizadas o los clientes de chat de grupo anteriores que usan el servidor de chat grupal de Office Communications Server 2007 R2 &nbsp; o Lync server 2010, la conversación grupal puede publicar archivos en un salón.</span><span class="sxs-lookup"><span data-stu-id="fffec-132">This setting is enforced on the server because custom applications or previous Group Chat clients using Office Communications Server 2007 R2&nbsp;Group Chat Server or Lync Server 2010, Group Chat can post files to a room.</span></span> <span data-ttu-id="fffec-133">El cliente de Lync 2013 no tiene la funcionalidad de carga y descarga de archivos, por lo que si tiene una implementación de Lync 2013 pura o un cliente de Lync 2013, no es posible publicar archivos en un salón de chat del servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="fffec-133">The Lync 2013 client does not have file upload/download capability, so if you have a pure Lync 2013 deployment or Lync 2013 client, it is not possible to post files in a Persistent Chat Server chat room.</span></span>

        
        </div>
    
      - <span data-ttu-id="fffec-134">En **Límite de actualización de participantes**, seleccione el límite de actualizaciones de participantes.</span><span class="sxs-lookup"><span data-stu-id="fffec-134">In **Participant update limit**, select the limit for participant updates.</span></span> <span data-ttu-id="fffec-135">El servidor de chat persistente envía información de la lista (que está conectada a un salón de chat) a todos los participantes hasta que la cantidad de usuarios conectados alcance este número.</span><span class="sxs-lookup"><span data-stu-id="fffec-135">Persistent Chat Server sends roster information (who is connected to a chat room) to all participants until the number of connected users reaches this number.</span></span> <span data-ttu-id="fffec-136">La cantidad predeterminada es 75.</span><span class="sxs-lookup"><span data-stu-id="fffec-136">By default, the number is 75.</span></span> <span data-ttu-id="fffec-137">Este límite indica la cantidad máxima de participantes en una habitación determinada, más allá de la cual el servidor de chat persistente deja de enviar actualizaciones de lista a los clientes conectados sobre quién está presente en el salón.</span><span class="sxs-lookup"><span data-stu-id="fffec-137">This limit indicates the maximum number of participants in a given room beyond which Persistent Chat Server stops sending roster updates to connected clients about who is present in the room.</span></span>
    
      - <span data-ttu-id="fffec-p111">(Opcional). En **URL de administración de sala**, seleccione la dirección URL de administración de salón. Esta es la dirección URL de una administración de salones personalizada basada en la web. Si no necesita personalizar la administración de salones y, simplemente, usa la configuración predeterminada, deje esta opción en blanco. Una vez que se haya definido la dirección URL, se aplicará como la dirección URL de administración del salón tanto interna como externa.</span><span class="sxs-lookup"><span data-stu-id="fffec-p111">(Optional.) In **Room management URL**, select the room management URL. This is the URL for a web-based custom room management. If you don’t need to customize room management, and you simply use the default setting, leave this option blank. After the URL is set, it is applied as both the internal and external room management URL.</span></span>
        
        <span data-ttu-id="fffec-142">Si desea personalizar la experiencia de creación de la sala e incluir su flujo de trabajo específico, puede crear una solución de administración de salas personalizada mediante el kit de desarrollo de software (SDK) del servidor de chat persistente, hospedarlo en algún lugar y colocar la dirección URL aquí.</span><span class="sxs-lookup"><span data-stu-id="fffec-142">If you want to customize your room creation experience and include your specific business workflow, you can build a custom room management solution by using the Persistent Chat Server Software Development Kit (SDK), host it somewhere, and put the URL here.</span></span> <span data-ttu-id="fffec-143">Esta dirección URL se envía al cliente, de modo que, cuando un usuario intente ver o crear un salón, será dirigido a su solución personalizada de administración de salones.</span><span class="sxs-lookup"><span data-stu-id="fffec-143">This URL is sent down to the client, so that when a user tries to view or create a room, he or she is directed to your custom room management solution.</span></span>

7.  <span data-ttu-id="fffec-144">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="fffec-144">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-configure-persistent-chat-options-for-a-specific-persistent-chat-server-pool"></a><span data-ttu-id="fffec-145">Para configurar las opciones de chat persistente para un grupo de servidores de chat persistente específico</span><span class="sxs-lookup"><span data-stu-id="fffec-145">To configure Persistent Chat options for a specific Persistent Chat Server pool</span></span>

1.  <span data-ttu-id="fffec-146">Desde una cuenta de usuario que se asigne al rol CsPersistentChatAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="fffec-146">From a user account that is assigned to the CsPersistentChatAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fffec-147">En el menú **Inicio** , seleccione el panel de control de Lync Server, o abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador.</span><span class="sxs-lookup"><span data-stu-id="fffec-147">From the **Start** menu, select the Lync Server Control Panel, or open a browser window, and then enter the Admin URL.</span></span> <span data-ttu-id="fffec-148">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="fffec-148">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="fffec-149">También puede usar los cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fffec-149">You can also use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="fffec-150">Para obtener más información, vea <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">configuración del servidor de chat persistente mediante cmdlets de Windows PowerShell</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="fffec-150">For details, see <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</A> in the Deployment documentation.</span></span>

    
    </div>

3.  <span data-ttu-id="fffec-151">En la barra de navegación izquierda, haga clic en **Chat persistente** y, luego, en **Configuración de chat persistente**.</span><span class="sxs-lookup"><span data-stu-id="fffec-151">In the left navigation bar, click **Persistent Chat**, and then click **Persistent Chat Configuration**.</span></span>

4.  <span data-ttu-id="fffec-152">En la página **Configuración de chat persistente**, haga clic en **Nuevo** y, luego, en **Configuración del grupo de servidores**.</span><span class="sxs-lookup"><span data-stu-id="fffec-152">On the **Persistent Chat Configuration** page, click **New**, and then click **Pool configuration**.</span></span>

5.  <span data-ttu-id="fffec-153">En **seleccionar un servicio**, seleccione el servicio asociado al grupo de servidores de chat persistente que desea configurar.</span><span class="sxs-lookup"><span data-stu-id="fffec-153">In **Select a Service**, select the service associated with the Persistent Chat Server pool to be configured.</span></span>

6.  <span data-ttu-id="fffec-154">En **Nueva configuración de chat persistente**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fffec-154">In **New Persistent Chat Configuration**, do the following:</span></span>
    
      - <span data-ttu-id="fffec-p115">En **Nombre**, especifique un nombre para la nueva configuración. El nombre del grupo de servidores del sitio ya existe de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fffec-p115">In **Name**, specify a name for the new configuration settings. By default, the site pool name already exists.</span></span>
    
      - <span data-ttu-id="fffec-p116">En **Historial de chat predeterminado**, defina la cantidad de mensajes de chat que se va a procesar para cada salón tras la primera solicitud. La cantidad predeterminada es 30. Esta es la configuración global y los administradores pueden deshabilitar el historial de chat por categoría.</span><span class="sxs-lookup"><span data-stu-id="fffec-p116">In **Default chat history**, define the number of chat messages that will be processed for each room upon first request. By default, the number is 30. This is the global default, and administrators can disable chat history per category.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="fffec-160">El servidor de chat persistente guardará estos mensajes en la memoria caché, por lo que, si aumenta este número, se almacenarán en caché más mensajes.</span><span class="sxs-lookup"><span data-stu-id="fffec-160">Persistent Chat Server will cache these messages in memory, so if you increase this number, more messages will be cached.</span></span> <span data-ttu-id="fffec-161">El acceso al contenido del historial siempre se encuentra disponible a través de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fffec-161">You can always access historical content by search.</span></span> <span data-ttu-id="fffec-162">La cantidad predeterminada solo indica la cantidad máxima de mensajes que ve inicialmente cuando se conecta a un salón de chat.</span><span class="sxs-lookup"><span data-stu-id="fffec-162">The default number simply determines the maximum number of messages that you initially see when connecting to a chat room.</span></span>

        
        </div>
    
      - <span data-ttu-id="fffec-p118">En **Tamaño máximo de archivo (KB)**, seleccione el tamaño máximo del archivo de cada historial de chat. La cantidad predeterminada es 20 MB (20 000 KB). Este es el tamaño máximo de archivo que puede cargarse a cualquier salón de chat del sistema (en el que las cargas de archivos estén habilitadas por su correspondiente parámetro de **Categoría**).</span><span class="sxs-lookup"><span data-stu-id="fffec-p118">In **Maximum file size (KB)**, select the maximum file size of each chat history. By default, the number is 20 MB (20,000 KB). This is the maximum size for a file that can be uploaded to any chat room in the system (for which file uploads are enabled by its corresponding **Category** setting).</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="fffec-166">Esta configuración se aplica en el servidor porque las aplicaciones personalizadas o los clientes de chat de grupo anteriores (servidor de chat en grupo de Office Communications Server 2007 R2 &nbsp; o Lync server 2010, chat grupal) pueden publicar archivos en una sala.</span><span class="sxs-lookup"><span data-stu-id="fffec-166">This setting is enforced on the server because custom applications or previous Group Chat clients (Office Communications Server 2007 R2&nbsp;Group Chat Server or Lync Server 2010, Group Chat) can post files to a room.</span></span> <span data-ttu-id="fffec-167">El cliente de Lync 2013 no tiene la funcionalidad de carga y descarga de archivos, por lo que si tiene una implementación de Lync 2013 pura o un cliente de Lync 2013, no es posible publicar archivos en un salón de chat del servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="fffec-167">The Lync 2013 client does not have file upload/download capability, so if you have a pure Lync 2013 deployment or Lync 2013 client, it is not possible to post files in a Persistent Chat Server chat room.</span></span>

        
        </div>
    
      - <span data-ttu-id="fffec-168">En **Límite de actualización de participantes**, seleccione el límite de actualizaciones de participantes.</span><span class="sxs-lookup"><span data-stu-id="fffec-168">In **Participant update limit**, select the limit for participant updates.</span></span> <span data-ttu-id="fffec-169">El servidor de chat persistente envía información de la lista (que está conectada a un salón de chat) a todos los participantes hasta que la cantidad de usuarios conectados alcance este número.</span><span class="sxs-lookup"><span data-stu-id="fffec-169">Persistent Chat Server sends roster information (who is connected to a chat room) to all participants until the number of connected users reaches this number.</span></span> <span data-ttu-id="fffec-170">La cantidad predeterminada es 75.</span><span class="sxs-lookup"><span data-stu-id="fffec-170">By default, the number is 75.</span></span> <span data-ttu-id="fffec-171">Este límite indica la cantidad máxima de participantes en una habitación determinada, más allá de la cual el servidor de chat persistente deja de enviar actualizaciones de lista a los clientes conectados sobre quién está presente en el salón.</span><span class="sxs-lookup"><span data-stu-id="fffec-171">This limit indicates the maximum number of participants in a given room beyond which Persistent Chat Server stops sending roster updates to connected clients about who is present in the room.</span></span>
    
      - <span data-ttu-id="fffec-p121">En **URL de administración de sala**, seleccione la dirección URL de administración de salón. Se trata de la dirección URL de una implementación de administración de salones basada en web. Si no necesita personalizar la administración de salones y, simplemente, usa la configuración predeterminada, deje esta opción en blanco.</span><span class="sxs-lookup"><span data-stu-id="fffec-p121">In **Room management URL**, select the room management URL. This is the URL for a web-based room management deployment. If you don’t need to customize room management, and you simply use the default setting, leave this option blank.</span></span>
        
        <span data-ttu-id="fffec-175">Si desea personalizar la experiencia de creación de la sala e incluir su flujo de trabajo específico, puede crear una solución de administración de salas personalizada mediante el kit de desarrollo de software (SDK) del servidor de chat persistente, hospedarlo en algún lugar y colocar la dirección URL aquí.</span><span class="sxs-lookup"><span data-stu-id="fffec-175">If you want to customize your room creation experience and include your specific business workflow, you can build a custom room management solution by using the Persistent Chat Server Software Development Kit (SDK), host it somewhere, and put the URL here.</span></span> <span data-ttu-id="fffec-176">Esta dirección URL se envía al cliente, de modo que, cuando un usuario intente ver o crear un salón, será dirigido a su solución personalizada de administración de salones.</span><span class="sxs-lookup"><span data-stu-id="fffec-176">This URL is sent down to the client so that when a user tries to view/create a room, he or she is directed to your custom room management solution.</span></span>

7.  <span data-ttu-id="fffec-177">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="fffec-177">Click **Commit**.</span></span>

<span data-ttu-id="fffec-178"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fffec-178"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

