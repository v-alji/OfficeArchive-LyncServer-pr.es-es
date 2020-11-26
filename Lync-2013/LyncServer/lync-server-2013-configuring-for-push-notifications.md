---
title: 'Lync Server 2013: Configurar las notificaciones de inserción'
description: 'Lync Server 2013: configuración de notificaciones Push.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring for push notifications
ms:assetid: d77f2c06-0fe6-45d5-8f08-808ab871b3e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690047(v=OCS.15)
ms:contentKeyID: 48185574
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24c22ff42f666add9eac4966134c88b9bf680046
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433089"
---
# <a name="configuring-for-push-notifications-in-lync-server-2013"></a><span data-ttu-id="d2bcb-103">Configurar las notificaciones de inserción en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d2bcb-103">Configuring for push notifications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d2bcb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d2bcb-104">

<span> </span></span></span>

<span data-ttu-id="d2bcb-105">_**Última modificación del tema:** 2013-02-12_</span><span class="sxs-lookup"><span data-stu-id="d2bcb-105">_**Topic Last Modified:** 2013-02-12_</span></span>

<span data-ttu-id="d2bcb-106">Las notificaciones push, en forma de insignias, iconos o alertas, se pueden enviar a un dispositivo móvil incluso cuando la aplicación móvil no está activa.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-106">Push notifications, in the form of badges, icons, or alerts, can be sent to a mobile device even when the mobile application is inactive.</span></span> <span data-ttu-id="d2bcb-107">Las notificaciones push notifican a un usuario de eventos como una invitación o un correo de voz nuevos o perdidos.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="d2bcb-108">El servicio de movilidad de Lync Server 2013 envía las notificaciones al servicio de notificaciones de inserción de Lync Server basado en la nube, que después envía las notificaciones al servicio de notificaciones push de Apple (APN) (para dispositivos Apple que ejecutan el cliente móvil de Lync 2010) o al servicio de notificaciones push 2013 2010 de Microsoft (MPNS)</span><span class="sxs-lookup"><span data-stu-id="d2bcb-108">The Lync Server 2013 Mobility Service sends the notifications to the cloud-based Lync Server Push Notification Service, which then sends the notifications to the Apple Push Notification Service (APNS) (for an Apple device running the Lync 2010 Mobile client) or the Microsoft Push Notification Service (MPNS) (for a Windows Phone device running the Lync 2010 Mobile or the Lync 2013 Mobile client).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d2bcb-109">Si usa Windows Phone con Lync 2010 Mobile o Lync 2013 Mobile Client, la notificación push es una consideración importante.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-109">If you use Windows Phone with Lync 2010 Mobile or Lync 2013 Mobile client, push notification is an important consideration.</span></span><BR><span data-ttu-id="d2bcb-110">Si usa Lync 2010 Mobile en dispositivos Apple, la notificación push es una consideración importante.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-110">If you use Lync 2010 Mobile on Apple devices, push notification is an important consideration.</span></span><BR><span data-ttu-id="d2bcb-111">Si usa Lync 2013 Mobile en dispositivos Apple, ya no necesita notificaciones Push.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-111">If you use Lync 2013 Mobile on Apple devices, you no longer need push notification.</span></span>



</div>

<span data-ttu-id="d2bcb-112">Configure su topología para que admita las notificaciones de inserción de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d2bcb-112">Configure your topology to support push notifications by doing the following:</span></span>

  - <span data-ttu-id="d2bcb-113">Si su entorno tiene un servidor perimetral de Lync Server 2010 o de Lync Server 2013, necesita agregar un nuevo proveedor de hospedaje, Microsoft Lync Online y, a continuación, configurar la Federación de proveedores de hospedaje entre su organización y Lync Online.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-113">If your environment has a Lync Server 2010 or Lync Server 2013 Edge Server, you need to add a new hosting provider, Microsoft Lync Online, and then set up hosting provider federation between your organization and Lync Online.</span></span>

  - <span data-ttu-id="d2bcb-114">Si su entorno tiene un servidor perimetral de Office Communications Server 2007 R2, necesita configurar la Federación SIP directa con push.lync.com.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-114">If your environment has a Office Communications Server 2007 R2 Edge Server, you need to set up direct SIP federation with push.lync.com.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d2bcb-115">Push.lync.com es un dominio de Microsoft Office 365 para el servicio de notificaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-115">Push.lync.com is a Microsoft Office 365 domain for Push Notification Service.</span></span>

    
    </div>

  - <span data-ttu-id="d2bcb-116">Para habilitar las notificaciones de inserción, debe ejecutar el cmdlet **set-CsPushNotificationConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="d2bcb-116">To enable push notifications, you need to run the **Set-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="d2bcb-117">De manera predeterminada, las notificaciones de inserción están desactivadas.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-117">By default, push notifications are turned off.</span></span>

  - <span data-ttu-id="d2bcb-118">Pruebe la configuración de Federación y las notificaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-118">Test the federation configuration and push notifications.</span></span>

<div>

## <a name="to-configure-for-push-notifications-with-lync-server-2013-or-lync-server-2010-edge-server"></a><span data-ttu-id="d2bcb-119">Para configurar las notificaciones de inserción con Lync Server 2013 o el servidor perimetral de Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="d2bcb-119">To configure for push notifications with Lync Server 2013 or Lync Server 2010 Edge Server</span></span>

1.  <span data-ttu-id="d2bcb-120">Inicie sesión en un equipo en el que el shell de administración de Lync Server y Ocscore estén instalados como miembro del grupo RtcUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-120">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the RtcUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="d2bcb-121">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="d2bcb-122">Agregue un proveedor de hospedaje de Lync Server online.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-122">Add a Lync Server online hosting provider.</span></span> <span data-ttu-id="d2bcb-123">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d2bcb-123">At the command line, type:</span></span>
    
        New-CsHostingProvider -Identity <unique identifier for Lync Online hosting provider> -Enabled $True -ProxyFqdn <FQDN for the Access Server used by the hosting provider> -VerificationLevel UseSourceVerification
    
    <span data-ttu-id="d2bcb-124">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d2bcb-124">For example:</span></span>
    
        New-CsHostingProvider -Identity "LyncOnline" -Enabled $True -ProxyFqdn "sipfed.online.lync.com" -VerificationLevel UseSourceVerification
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d2bcb-125">No puede tener más de una relación de Federación con un solo proveedor de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-125">You cannot have more than one federation relationship with a single hosting provider.</span></span> <span data-ttu-id="d2bcb-126">Es decir, si ya ha configurado un proveedor de hospedaje que tiene una relación de Federación con sipfed.online.lync.com, no agregue otro proveedor de hospedaje para él, incluso si la identidad del proveedor de hospedaje es distinta de LyncOnline.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-126">That is, if you have already set up a hosting provider that has a federation relationship with sipfed.online.lync.com, do not add another hosting provider for it, even if the identity of the hosting provider is something other than LyncOnline.</span></span>

    
    </div>

4.  <span data-ttu-id="d2bcb-127">Configure la Federación de proveedores de hospedaje entre su organización y el servicio de notificaciones de inserción en Lync Online.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-127">Set up hosting provider federation between your organization and the Push Notification Service at Lync Online.</span></span> <span data-ttu-id="d2bcb-128">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="d2bcb-128">At the command line, type:</span></span>
    
        New-CsAllowedDomain -Identity "push.lync.com"

</div>

<div>

## <a name="to-configure-for-push-notifications-with-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="d2bcb-129">Para configurar las notificaciones de inserción con el servidor perimetral de Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d2bcb-129">To configure for push notifications with Office Communications Server 2007 R2 Edge Server</span></span>

1.  <span data-ttu-id="d2bcb-130">Inicie sesión en el servidor perimetral como miembro del grupo RtcUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-130">Log on to the Edge Server as a member of the RtcUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="d2bcb-131">Haga clic en **Inicio**, en **todos los programas**, en **herramientas administrativas** y, por último, en **Administración de equipos**.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-131">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Computer Management**.</span></span>

3.  <span data-ttu-id="d2bcb-132">En el árbol de consola, expanda **servicios y aplicaciones**, haga clic con el botón secundario en **Microsoft Office Communications Server 2007 R2** y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-132">In the console tree, expand **Services and Applications**, right-click **Microsoft Office Communications Server 2007 R2**, and then click **Properties**.</span></span>

4.  <span data-ttu-id="d2bcb-133">En la pestaña **permitir** , haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-133">On the **Allow** tab, click **Add**.</span></span>

5.  <span data-ttu-id="d2bcb-134">En el cuadro de diálogo **Agregar socio federado** , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d2bcb-134">In the **Add Federated Partner** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="d2bcb-135">En **nombre de dominio del socio federado**, escriba **Push.Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-135">In **Federated partner domain name**, type **push.lync.com**.</span></span>
    
      - <span data-ttu-id="d2bcb-136">En el **servidor perimetral de acceso del socio federado**, escriba **sipfed.online.Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-136">In **Federated partner Access Edge Server**, type **sipfed.online.lync.com**.</span></span>
    
      - <span data-ttu-id="d2bcb-137">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-137">Click **OK**.</span></span>

</div>

<div>

## <a name="to-enable-push-notifications"></a><span data-ttu-id="d2bcb-138">Para habilitar las notificaciones de inserción</span><span class="sxs-lookup"><span data-stu-id="d2bcb-138">To enable push notifications</span></span>

1.  <span data-ttu-id="d2bcb-139">Inicie sesión en un equipo en el que el shell de administración de Lync Server y Ocscore estén instalados como miembro del rol CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-139">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="d2bcb-140">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-140">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="d2bcb-141">Habilitar las notificaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-141">Enable push notifications.</span></span> <span data-ttu-id="d2bcb-142">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="d2bcb-142">At the command line, type:</span></span>
    
        Set-CsPushNotificationConfiguration -EnableApplePushNotificationService $True -EnableMicrosoftPushNotificationService $True

4.  <span data-ttu-id="d2bcb-143">Habilitar la Federación.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-143">Enable federation.</span></span> <span data-ttu-id="d2bcb-144">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="d2bcb-144">At the command line, type:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

</div>

<div>

## <a name="to-test-federation-and-push-notifications"></a><span data-ttu-id="d2bcb-145">Para probar la Federación y las notificaciones de inserción</span><span class="sxs-lookup"><span data-stu-id="d2bcb-145">To test federation and push notifications</span></span>

1.  <span data-ttu-id="d2bcb-146">Inicie sesión en un equipo en el que el shell de administración de Lync Server y Ocscore estén instalados como miembro del rol CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-146">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="d2bcb-147">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="d2bcb-148">Pruebe la configuración de Federación.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-148">Test the federation configuration.</span></span> <span data-ttu-id="d2bcb-149">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d2bcb-149">At the command line, type:</span></span>
    
        Test-CsFederatedPartner -TargetFqdn <FQDN of Access Edge server used for federated SIP traffic> -Domain <FQDN of federated domain> -ProxyFqdn <FQDN of the Access Edge server used by the federated organization>
    
    <span data-ttu-id="d2bcb-150">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d2bcb-150">For example:</span></span>
    
        Test-CsFederatedPartner -TargetFqdn accessproxy.contoso.com -Domain push.lync.com -ProxyFqdn sipfed.online.lync.com

4.  <span data-ttu-id="d2bcb-151">Probar las notificaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="d2bcb-151">Test push notifications.</span></span> <span data-ttu-id="d2bcb-152">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d2bcb-152">At the command line, type:</span></span>
    
        Test-CsMcxPushNotification -AccessEdgeFqdn <Access Edge service FQDN>
    
    <span data-ttu-id="d2bcb-153">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d2bcb-153">For example:</span></span>
    
        Test-CsMcxPushNotification -AccessEdgeFqdn accessproxy.contoso.com

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d2bcb-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2bcb-154">See Also</span></span>


[<span data-ttu-id="d2bcb-155">Prueba-CsFederatedPartner</span><span class="sxs-lookup"><span data-stu-id="d2bcb-155">Test-CsFederatedPartner</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner)  
[<span data-ttu-id="d2bcb-156">Test-CsMcxPushNotification</span><span class="sxs-lookup"><span data-stu-id="d2bcb-156">Test-CsMcxPushNotification</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification)  
  

<span data-ttu-id="d2bcb-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d2bcb-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

