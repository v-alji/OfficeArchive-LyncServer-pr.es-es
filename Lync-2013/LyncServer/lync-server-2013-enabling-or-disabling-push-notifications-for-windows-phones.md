---
title: 'Lync Server 2013: habilitar o deshabilitar las notificaciones push para Windows Phone'
description: 'Lync Server 2013: habilitar o deshabilitar las notificaciones push para Windows Phone.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling or disabling push notifications for Windows Phones
ms:assetid: a34f0c5c-4228-40e3-9d93-bc0b5df4895d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688162(v=OCS.15)
ms:contentKeyID: 49733767
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba3748c56291b8c6eb236edaac7e23a9e00e5e98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428772"
---
# <a name="enabling-or-disabling-push-notifications-for-windows-phones-in-lync-server-2013"></a><span data-ttu-id="f3a95-103">Habilitar o deshabilitar las notificaciones push para teléfonos Windows en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3a95-103">Enabling or disabling push notifications for Windows Phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3a95-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3a95-104">

<span> </span></span></span>

<span data-ttu-id="f3a95-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="f3a95-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="f3a95-106">Las notificaciones push, en forma de insignias, iconos o alertas, se pueden enviar a un Windows Phone incluso cuando la aplicación móvil no está activa.</span><span class="sxs-lookup"><span data-stu-id="f3a95-106">Push notifications, in the form of badges, icons, or alerts, can be sent to a Windows Phone even when the mobile application is inactive.</span></span> <span data-ttu-id="f3a95-107">Las notificaciones push notifican a un usuario de eventos como una invitación o un correo de voz nuevos o perdidos.</span><span class="sxs-lookup"><span data-stu-id="f3a95-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="f3a95-108">Puede habilitar o deshabilitar las notificaciones push para dispositivos Windows Phone mediante el panel de control de Lync Server 2013 o el shell de administración de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f3a95-108">You can enable or disable push notifications for Windows Phone devices by using either Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-enable-push-notifications-for-windows-phone-by-using-lync-server-control-panel"></a><span data-ttu-id="f3a95-109">Para habilitar las notificaciones push para Windows Phone mediante el panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="f3a95-109">To enable push notifications for Windows Phone by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="f3a95-110">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="f3a95-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f3a95-111">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f3a95-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f3a95-112">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f3a95-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f3a95-113">En la barra de navegación izquierda, haga clic en **clientes** y, a continuación, haga clic en el botón de navegación de **configuración de notificaciones push** .</span><span class="sxs-lookup"><span data-stu-id="f3a95-113">In the left navigation bar, click **Clients**, and then click the **Push Notification Configuration** navigation button.</span></span>

4.  <span data-ttu-id="f3a95-114">En la página **configuración de notificaciones push** , haga clic en el sitio que desea editar, haga clic en el menú **Editar** y, a continuación, haga clic en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="f3a95-114">On the **Push Notification Configuration** page, click the site you want to edit, click the **Edit** menu, and then click **Show details**.</span></span>

5.  <span data-ttu-id="f3a95-115">Haga clic en la casilla de verificación **habilitar notificaciones de inserción de Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="f3a95-115">Click the **Enable Microsoft push notifications** checkbox.</span></span>

6.  <span data-ttu-id="f3a95-116">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="f3a95-116">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-disable-push-notifications-for-windows-phone-by-using-lync-server-control-panel"></a><span data-ttu-id="f3a95-117">Para deshabilitar las notificaciones push para Windows Phone mediante el panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="f3a95-117">To disable push notifications for Windows Phone by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="f3a95-118">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="f3a95-118">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f3a95-119">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f3a95-119">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f3a95-120">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f3a95-120">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f3a95-121">En la barra de navegación izquierda, haga clic en **clientes** y, a continuación, haga clic en el botón de navegación de **configuración de notificaciones push** .</span><span class="sxs-lookup"><span data-stu-id="f3a95-121">In the left navigation bar, click **Clients**, and then click the **Push Notification Configuration** navigation button.</span></span>

4.  <span data-ttu-id="f3a95-122">En la página **configuración de notificaciones push** , haga clic en el sitio que desea editar, haga clic en el menú **Editar** y, a continuación, haga clic en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="f3a95-122">On the **Push Notification Configuration** page, click the site you want to edit, click the **Edit** menu, and then click **Show details**.</span></span>

5.  <span data-ttu-id="f3a95-123">Desactive la casilla **habilitar notificaciones de inserción de Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="f3a95-123">Clear the **Enable Microsoft push notifications** checkbox.</span></span>

6.  <span data-ttu-id="f3a95-124">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="f3a95-124">Click **Commit**.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-push-notifications-for-windows-phone-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="f3a95-125">Habilitar o deshabilitar las notificaciones push para Windows Phone mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3a95-125">Enabling or Disabling Push Notifications for Windows Phone by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="f3a95-126">Puede habilitar o deshabilitar las notificaciones push para Windows Phone mediante el cmdlet **set-CsPushNotificationConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f3a95-126">You can enable or disable push notifications for Windows Phone by using the **Set-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="f3a95-127">Puede ejecutar este cmdlet desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3a95-127">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="f3a95-128">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="f3a95-128">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-push-notifications-for-windows-phone"></a><span data-ttu-id="f3a95-129">Para habilitar las notificaciones push para Windows Phone</span><span class="sxs-lookup"><span data-stu-id="f3a95-129">To enable push notifications for Windows Phone</span></span>

  - <span data-ttu-id="f3a95-130">Para habilitar las notificaciones de inserción para Windows Phone, establezca el valor de la propiedad EnableMicrosoftPushNotificationService en true ($True).</span><span class="sxs-lookup"><span data-stu-id="f3a95-130">To enable push notifications for Windows Phone set the value of the EnableMicrosoftPushNotificationService property to True ($True).</span></span> <span data-ttu-id="f3a95-131">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f3a95-131">For example:</span></span>
    
        Set-CsPushNotificationConfiguration -Identity "site:Redmond" -EnableMicrosoftPushNotificationService $True

</div>

<div>

## <a name="to-disable-push-notifications-for-windows-phone"></a><span data-ttu-id="f3a95-132">Para deshabilitar las notificaciones push para Windows Phone</span><span class="sxs-lookup"><span data-stu-id="f3a95-132">To disable push notifications for Windows Phone</span></span>

  - <span data-ttu-id="f3a95-133">Para deshabilitar las notificaciones de inserción para Windows Phone, establezca el valor de la propiedad EnableMicrosoftPushNotificationService en false ($False).</span><span class="sxs-lookup"><span data-stu-id="f3a95-133">To disable push notifications for Windows Phone set the value of the EnableMicrosoftPushNotificationService property to False ($False).</span></span> <span data-ttu-id="f3a95-134">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f3a95-134">For example:</span></span>
    
        Set-CsPushNotificationConfiguration -Identity "site:Redmond" -EnableMicrosoftPushNotificationService $False

</div>

<span data-ttu-id="f3a95-135">Para obtener más información, consulte el tema de ayuda para el cmdlet [set-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPushNotificationConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="f3a95-135">For more information, see the help topic for the [Set-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPushNotificationConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f3a95-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3a95-136">See Also</span></span>


[<span data-ttu-id="f3a95-137">Configurar las notificaciones de inserción en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3a95-137">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)  
  

<span data-ttu-id="f3a95-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3a95-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

