---
title: 'Lync Server 2013: Configurar complementos para salones'
description: 'Lync Server 2013: configurar complementos para salas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure add-ins for rooms
ms:assetid: 4eeaf19e-8369-4f6f-af65-a283cf7daa1c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204878(v=OCS.15)
ms:contentKeyID: 48184090
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 803bff81fa76bf5a7d2d408c93ba9247ead72510
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434164"
---
# <a name="configure-add-ins-for-rooms-in-lync-server-2013"></a><span data-ttu-id="85285-103">Configurar complementos para salones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85285-103">Configure add-ins for rooms in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85285-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85285-104">

<span> </span></span></span>

<span data-ttu-id="85285-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="85285-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="85285-106">En el panel de control de Lync Server 2013, puede usar la sección de **complemento** de la página de **chat persistente** para asociar direcciones URL a salas de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="85285-106">In Lync Server 2013 Control Panel, you can use the **Add-in** section of the **Persistent Chat** page to associate URLs with Persistent Chat rooms.</span></span> <span data-ttu-id="85285-107">Estas direcciones URL aparecen en el cliente de Lync 2013, en el salón de chat del panel extensibilidad de conversaciones.</span><span class="sxs-lookup"><span data-stu-id="85285-107">These URLs appear in the Lync 2013 client in the chat room in the conversation extensibility pane.</span></span> <span data-ttu-id="85285-108">Un administrador debe agregar complementos a la lista de complementos registrados y los administradores o creadores de salones de chat tienen que asociar salas a uno de los complementos registrados para que los usuarios puedan ver esta actualización en su cliente de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="85285-108">An administrator must add Add-ins to the list of registered add-ins, and chat room managers/Creators have to associate rooms with one of the registered add-ins before users can see this upgrade in their Lync 2013 client.</span></span>

<span data-ttu-id="85285-109">Los complementos sirven para ampliar la experiencia en el salón.</span><span class="sxs-lookup"><span data-stu-id="85285-109">Add-ins are used to extend the in-room experience.</span></span> <span data-ttu-id="85285-110">Un complemento típico puede incluir una dirección URL que señala a una aplicación de Silverlight que intercepta cuando un tablero de cotizaciones está publicado en un salón de chat y muestra el historial de cotizaciones en el panel extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="85285-110">A typical add-in might include a URL pointing to a Silverlight application that intercepts when a stock ticker is posted to a chat room, and shows the stock history in the extensibility pane.</span></span> <span data-ttu-id="85285-111">Otros ejemplos serían incrustar una dirección URL de OneNote 2013 en el salón de chat como un complemento para incluir contexto compartido, como "Lista de prioridades" o "Tema del día".</span><span class="sxs-lookup"><span data-stu-id="85285-111">Other examples include embedding a OneNote 2013 URL in the chat room as an add-in to include some shared context, such as "Top of mind" or "Topic of the day."</span></span>

<div>

## <a name="to-configure-add-ins-for-chat-rooms"></a><span data-ttu-id="85285-112">Para configurar complementos para salones de chat</span><span class="sxs-lookup"><span data-stu-id="85285-112">To configure Add-ins for chat rooms</span></span>

1.  <span data-ttu-id="85285-113">Desde una cuenta de usuario que se asigne al rol CsPersistentChatAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="85285-113">From a user account that is assigned to the CsPersistentChatAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="85285-114">En el menú **Inicio** , seleccione el panel de control de Lync Server o abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador.</span><span class="sxs-lookup"><span data-stu-id="85285-114">From the **Start** menu, select the Lync Server Control Panel or open a browser window, and then enter the Admin URL.</span></span> <span data-ttu-id="85285-115">Para más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="85285-115">For details about the different methods that you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="85285-116">También puede usar los cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85285-116">You can also use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="85285-117">Para obtener más información, vea <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">configuración del servidor de chat persistente mediante cmdlets de Windows PowerShell</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="85285-117">For details, see <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</A> in the Deployment documentation.</span></span>

    
    </div>

3.  <span data-ttu-id="85285-118">En la barra de navegación izquierda, haga clic en **Chat persistente** y, luego, en **Complemento**.</span><span class="sxs-lookup"><span data-stu-id="85285-118">In the left navigation bar, click **Persistent Chat**, and then click **Add-in**.</span></span>
    
    <span data-ttu-id="85285-119">Para varias implementaciones del grupo de servidores de chat persistentes, seleccione el grupo adecuado de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="85285-119">For multiple Persistent Chat Server pool deployments, select the appropriate pool from the drop-down list.</span></span>

4.  <span data-ttu-id="85285-120">En la página **Complemento**, haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="85285-120">On the **Add-in** page, click **New**.</span></span>

5.  <span data-ttu-id="85285-121">En **seleccionar un servicio**, seleccione el servicio correspondiente al grupo de servidores de chat persistente donde necesita crear el complemento.</span><span class="sxs-lookup"><span data-stu-id="85285-121">In **Select a Service**, select the service corresponding to the Persistent Chat Server pool where you need to create the Add-in.</span></span> <span data-ttu-id="85285-122">Los complementos no se pueden mover de un grupo a otro o compartirse entre diferentes grupos.</span><span class="sxs-lookup"><span data-stu-id="85285-122">Add-ins cannot be moved from one pool to another or shared between different pools.</span></span>

6.  <span data-ttu-id="85285-123">En **Complemento nuevo**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="85285-123">In **New Add-in**, do the following:</span></span>
    
      - <span data-ttu-id="85285-124">En **Nombre**, especifique un nombre para el nuevo complemento.</span><span class="sxs-lookup"><span data-stu-id="85285-124">In **Name**, specify a name for the new add-in.</span></span>
    
      - <span data-ttu-id="85285-p106">En **URL**, especifique la dirección URL que se va a asociar al complemento. Las direcciones URL se limitan a protocolos http y https.</span><span class="sxs-lookup"><span data-stu-id="85285-p106">In **URL**, specify the URL to be associated with the add-in. URLs are limited to http and https protocols.</span></span>

7.  <span data-ttu-id="85285-127">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="85285-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="85285-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="85285-128">See Also</span></span>


[<span data-ttu-id="85285-129">Abrir las herramientas administrativas de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85285-129">Open Lync Server 2013 administrative tools</span></span>](lync-server-2013-open-lync-server-administrative-tools.md)  


[<span data-ttu-id="85285-130">Configuración del servidor de chat persistente con cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="85285-130">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</span></span>](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md)  
  

<span data-ttu-id="85285-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85285-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

