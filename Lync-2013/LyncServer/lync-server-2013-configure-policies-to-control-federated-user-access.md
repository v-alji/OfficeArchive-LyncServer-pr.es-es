---
title: 'Lync Server 2013: Configurar directivas para controlar el acceso de usuarios federados'
description: 'Lync Server 2013: configurar directivas para controlar el acceso de usuarios federados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure policies to control federated user access
ms:assetid: 5485e208-81e4-4e59-9aeb-1232c11dd8a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398359(v=OCS.15)
ms:contentKeyID: 48184180
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d69f35baa16086b0c4e93a2a015474f87e08b736
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398507"
---
# <a name="configure-policies-to-control-federated-user-access-in-lync-server-2013"></a><span data-ttu-id="2e319-103">Configurar directivas para controlar el acceso de usuarios federados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e319-103">Configure policies to control federated user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2e319-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2e319-104">

<span> </span></span></span>

<span data-ttu-id="2e319-105">_**Última modificación del tema:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="2e319-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="2e319-106">Al configurar directivas para admitir las comunicaciones con socios federados, las directivas se aplican a los usuarios de dominios federados.</span><span class="sxs-lookup"><span data-stu-id="2e319-106">When you configure policies to support communications with federated partners, the policies apply to users of federated domains.</span></span> <span data-ttu-id="2e319-107">Puede configurar una o más directivas de acceso de usuarios externos para controlar si los usuarios de dominios federados pueden colaborar con los usuarios de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2e319-107">You can configure one or more external user access policies to control whether users of federated domains can collaborate with your Lync Server 2013 users.</span></span> <span data-ttu-id="2e319-108">Para controlar el acceso de usuarios federados, puede configurar directivas en el nivel global, de sitio y de usuario.</span><span class="sxs-lookup"><span data-stu-id="2e319-108">To control federated user access, you can configure policies at the global, site, and user level.</span></span> <span data-ttu-id="2e319-109">La configuración de directiva de Lync Server que se aplica a un nivel de Directiva puede invalidar la configuración que se aplica a otro nivel de directiva.</span><span class="sxs-lookup"><span data-stu-id="2e319-109">Lync Server policy settings that are applied at one policy level can override settings that are applied at another policy level.</span></span> <span data-ttu-id="2e319-110">La prioridad de la Directiva de Lync Server es: la Directiva de usuario (más influencia) reemplaza a una directiva de sitio y, después, una directiva de sitio invalida una directiva global (menor influencia).</span><span class="sxs-lookup"><span data-stu-id="2e319-110">Lync Server policy precedence is: User policy (most influence) overrides a Site policy, and then a Site policy overrides a Global policy (least influence).</span></span> <span data-ttu-id="2e319-111">Esto significa que, cuanto más cercana es la configuración de directiva al objeto al que la directiva afecta, mayor es la influencia que ejerce sobre el objeto.</span><span class="sxs-lookup"><span data-stu-id="2e319-111">This means that the closer the policy setting is to the object that the policy is affecting, the more influence it has on the object.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2e319-112">Puede configurar directivas para controlar el acceso de usuarios federados, incluso si no ha habilitado la Federación de su organización.</span><span class="sxs-lookup"><span data-stu-id="2e319-112">You can configure policies to control federated user access, even if you have not enabled federation for your organization.</span></span> <span data-ttu-id="2e319-113">Sin embargo, las directivas que configure solo estarán vigentes cuando tenga habilitada la Federación de su organización.</span><span class="sxs-lookup"><span data-stu-id="2e319-113">However, the policies that you configure are in effect only when you have federation enabled for your organization.</span></span> <span data-ttu-id="2e319-114">Para obtener más información sobre cómo habilitar la Federación, vea <A href="lync-server-2013-enable-or-disable-remote-user-access.md">habilitar o deshabilitar el acceso de usuarios remotos en Lync Server 2013</A> en la documentación de implementación o en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="2e319-114">For details about enabling federation, see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A> in the Deployment documentation or the Operations documentation.</span></span> <span data-ttu-id="2e319-115">Además, si especifica una directiva de usuario para controlar el acceso de usuarios federados, la Directiva solo se aplica a los usuarios que están habilitados para Lync Server 2013 y están configurados para usar la Directiva.</span><span class="sxs-lookup"><span data-stu-id="2e319-115">Additionally, if you specify a user policy to control federated user access, the policy applies only to users that are enabled for Lync Server 2013 and configured to use the policy.</span></span>



</div>

<div>

## <a name="to-configure-a-policy-to-support-access-by-users-of-federated-domains"></a><span data-ttu-id="2e319-116">Para configurar una directiva para admitir el acceso de usuarios de dominios federados</span><span class="sxs-lookup"><span data-stu-id="2e319-116">To configure a policy to support access by users of federated domains</span></span>

1.  <span data-ttu-id="2e319-117">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="2e319-117">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="2e319-118">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2e319-118">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2e319-119">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2e319-119">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="2e319-120">En la barra de navegación izquierda, haga clic en **acceso de usuarios externos** y, después, en **Directiva de acceso externo**.</span><span class="sxs-lookup"><span data-stu-id="2e319-120">In the left navigation bar, click **External User Access**, and then click **External Access Policy**.</span></span>

4.  <span data-ttu-id="2e319-121">En la página **Directiva de acceso externo** , realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="2e319-121">On the **External Access Policy** page, do one of the following:</span></span>
    
      - <span data-ttu-id="2e319-122">Para configurar la directiva global para admitir el acceso de usuarios federados, haga clic en la directiva global, haga clic en **Editar** y, a continuación, haga clic en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="2e319-122">To configure the global policy to support federated user access, click the global policy, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="2e319-123">Para crear una nueva Directiva de sitio, haga clic en **nueva** y, a continuación, haga clic en **Directiva del sitio**.</span><span class="sxs-lookup"><span data-stu-id="2e319-123">To create a new site policy, click **New**, and then click **Site policy**.</span></span> <span data-ttu-id="2e319-124">En **seleccionar un sitio**, haga clic en el sitio adecuado de la lista y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="2e319-124">In **Select a Site**, click the appropriate site from the list and then click **OK**.</span></span>
    
      - <span data-ttu-id="2e319-125">Para crear una nueva Directiva de usuario, haga clic en **nueva** y, a continuación, haga clic en **Directiva de usuario**.</span><span class="sxs-lookup"><span data-stu-id="2e319-125">To create a new user policy, click **New**, and then click **User policy**.</span></span> <span data-ttu-id="2e319-126">En **nueva Directiva de acceso externo**, cree un nombre único en el campo **nombre** que indique lo que cubre la Directiva de usuario (por ejemplo, **EnableFederatedUsers** para una directiva de usuario que permita las comunicaciones de usuarios de dominios federados).</span><span class="sxs-lookup"><span data-stu-id="2e319-126">In **New External Access Policy**, create a unique name in the **Name** field that indicates what the user policy covers (for example, **EnableFederatedUsers** for a user policy that enables communications for federated domain users).</span></span>
    
      - <span data-ttu-id="2e319-127">Para cambiar una directiva existente, haga clic en la directiva correspondiente que aparece en la tabla, haga clic en **Editar** y, a continuación, haga clic en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="2e319-127">To change an existing policy, click the appropriate policy listed in the table, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="2e319-128">Faculta Si desea agregar o editar una descripción, especifique la información de la Directiva en **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="2e319-128">(Optional) If you want to add or edit a description, specify the information for the policy in **Description**.</span></span>

6.  <span data-ttu-id="2e319-129">Realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="2e319-129">Do one of the following:</span></span>
    
      - <span data-ttu-id="2e319-130">Para habilitar el acceso de usuarios federados para la Directiva, active la casilla **Habilitar comunicaciones con usuarios federados** .</span><span class="sxs-lookup"><span data-stu-id="2e319-130">To enable federated user access for the policy, select the **Enable communications with federated users** check box.</span></span>
    
      - <span data-ttu-id="2e319-131">Para deshabilitar el acceso de usuarios federados para la Directiva, desactive la casilla **Habilitar comunicaciones con usuarios federados** .</span><span class="sxs-lookup"><span data-stu-id="2e319-131">To disable federated user access for the policy, clear the **Enable communications with federated users** check box.</span></span>

7.  <span data-ttu-id="2e319-132">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="2e319-132">Click **Commit**.</span></span>

<span data-ttu-id="2e319-133">Para habilitar el acceso de usuarios federados, también debe habilitar la compatibilidad con la Federación de su organización.</span><span class="sxs-lookup"><span data-stu-id="2e319-133">To enable federated user access, you must also enable support for federation in your organization.</span></span> <span data-ttu-id="2e319-134">Para obtener más información, vea [habilitar o deshabilitar la Federación y la conectividad de mensajería instantánea pública en Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md).</span><span class="sxs-lookup"><span data-stu-id="2e319-134">For details, see [Enable or disable federation and public IM connectivity in Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md).</span></span>

<span data-ttu-id="2e319-135">Si se trata de una directiva de usuario, también debe aplicar la Directiva a los usuarios que desee que puedan colaborar con los usuarios federados.</span><span class="sxs-lookup"><span data-stu-id="2e319-135">If this is a user policy, you must also apply the policy to users that you want to be able to collaborate with federated users.</span></span> <span data-ttu-id="2e319-136">Para obtener más información, consulte [asignar una directiva de acceso de usuarios externos a un usuario habilitado de Lync en Lync Server 2013](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md).</span><span class="sxs-lookup"><span data-stu-id="2e319-136">For details, see [Assign an external user access policy to a Lync enabled user in Lync Server 2013](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md).</span></span>

</div>

<div>

## <a name="to-configure-an-existing-policy-using-windows-powershell-to-support-access-by-users-of-federated-domains"></a><span data-ttu-id="2e319-137">Para configurar una directiva existente mediante Windows PowerShell para admitir el acceso de usuarios de dominios federados</span><span class="sxs-lookup"><span data-stu-id="2e319-137">To configure an existing policy using Windows PowerShell to support access by users of federated domains</span></span>

1.  <span data-ttu-id="2e319-138">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="2e319-138">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="2e319-139">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="2e319-139">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="2e319-140">Escriba lo siguiente en el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="2e319-140">Type the following in the Lync Server Management Shell:</span></span>
    
        Set-CsExternalAccessPolicy -Identity <name of global, site or user policy - policy must exist when using Set-CsExternalAccessPolicy > -Description <descriptive name for policy> -EnableFederationAccess <$true, $false> -EnableXmppAccess <$true, $false> -EnablePublicCloudAccess <$true, $false> -EnablePublicCloudAudioVideoAccess <$true, $false> -EnableOutsideAccess <$true, $false>
    
    <span data-ttu-id="2e319-141">Un comando de ejemplo que establecerá la directiva global de acceso de usuarios federados en habilitado, acceso de dominio XMPP a acceso de usuarios remotos habilitado a acceso de usuarios remotos a habilitado, acceso de proveedor público a habilitado y concesión de la posibilidad de usar audio y vídeo para los proveedores públicos que lo admitan:</span><span class="sxs-lookup"><span data-stu-id="2e319-141">An example command that will set the global policy for Federated user access to enabled, XMPP domain access to enabled, Remote user access to enabled, Public provider access to enabled, and grant the ability to use audio and video for public providers that support it:</span></span>
    
        Set-CsExternalAccessPolicy -Identity global -EnableFederationAccess $true -EnableXmppAccess $true -EnableOutsideAccess $true -EnablePublicCloudAccess $true -EnablePublicCloudAudioVideoAccess $true
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="2e319-142">El parámetro "EnablePublicCloudAudioVideoAccess" no tiene una selección correspondiente en el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2e319-142">The parameter “EnablePublicCloudAudioVideoAccess” does not have a corresponding selection in the Lync Server Control Panel</span></span>

    
    </div>

</div>

<div>

## <a name="to-create-a-new-policy-using-windows-powershell-to-support-access-by-users-of-federated-domains"></a><span data-ttu-id="2e319-143">Para crear una nueva directiva con Windows PowerShell para admitir el acceso de usuarios de dominios federados</span><span class="sxs-lookup"><span data-stu-id="2e319-143">To create a new policy using Windows PowerShell to support access by users of federated domains</span></span>

1.  <span data-ttu-id="2e319-144">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="2e319-144">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="2e319-145">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="2e319-145">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="2e319-146">Escriba lo siguiente en el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="2e319-146">Type the following in the Lync Server Management Shell:</span></span>
    
        New-CsExtenalAccessPolicy -Identity <name of site or user policy - you cannot create a new global policy using New-CsExternalAccessPolicy > -Description <descriptive name for policy> -EnableFederationAccess <$true, $false> -EnableXmppAccess <$true, $false> -EnablePublicCloudAccess <$true, $false> -EnablePublicCloudAudioVideoAccess <$true, $false> -EnableOutsideAccess <$true, $false>
    
    <span data-ttu-id="2e319-147">Un ejemplo de creación de una nueva Directiva de sitio:</span><span class="sxs-lookup"><span data-stu-id="2e319-147">An example of creating a new site policy:</span></span>
    
        New-CsExternalAccessPolicy -Identity site:Redmond -EnableFederationAccess $true -EnableXmppAccess $true -EnableOutsideAccess $true -EnablePublicCloudAccess $true -EnablePublicCloudAudioVideoAccess $true

</div>

<div>

## <a name="to-delete-or-reset-a-policy-using-windows-powershell-to-support-access-by-users-of-federated-domains"></a><span data-ttu-id="2e319-148">Para eliminar o restablecer una directiva con Windows PowerShell para admitir el acceso de usuarios de dominios federados</span><span class="sxs-lookup"><span data-stu-id="2e319-148">To delete or reset a policy using Windows PowerShell to support access by users of federated domains</span></span>

1.  <span data-ttu-id="2e319-149">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="2e319-149">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="2e319-150">Escriba lo siguiente en el shell de administración de Lync Server</span><span class="sxs-lookup"><span data-stu-id="2e319-150">Type the following in the Lync Server Management Shell</span></span>
    
        Remove-CsExternalAccessPolicy -Identity <name of global, site or user policy> 
    
    <span data-ttu-id="2e319-151">Un ejemplo de restablecimiento de la directiva global (la directiva global solo puede tener su configuración desinstalada).</span><span class="sxs-lookup"><span data-stu-id="2e319-151">An example of resetting the global policy (The global policy can only have its setting removed.</span></span> <span data-ttu-id="2e319-152">No se puede eliminar la Directiva):</span><span class="sxs-lookup"><span data-stu-id="2e319-152">The policy cannot be deleted):</span></span>
    
        Remove-CsExternalAccessPolicy -Identity global 
    
    <span data-ttu-id="2e319-153">Para quitar una directiva de sitio, escriba:</span><span class="sxs-lookup"><span data-stu-id="2e319-153">To remove a site policy, type:</span></span>
    
        Remove-CsExternalAccessPolicy -Identity site:Redmond 
    
    <span data-ttu-id="2e319-154">Elimina la Directiva de sitio de Redmond.</span><span class="sxs-lookup"><span data-stu-id="2e319-154">Deletes the site policy Redmond.</span></span> <span data-ttu-id="2e319-155">Para eliminar una directiva de usuario denominada UserEAPPolicy, escriba:</span><span class="sxs-lookup"><span data-stu-id="2e319-155">To delete a user policy named UserEAPPolicy, type:</span></span>
    
        Remove-CsExternalAccessPolicy -Identity UserEAPPolicy

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2e319-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e319-156">See Also</span></span>


[<span data-ttu-id="2e319-157">Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e319-157">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)  
[<span data-ttu-id="2e319-158">Asignar una directiva de acceso de usuario externo a un usuario habilitado para Lync en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e319-158">Assign an external user access policy to a Lync enabled user in Lync Server 2013</span></span>](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)  


[<span data-ttu-id="2e319-159">Administrar dominios federados SIP para la organización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e319-159">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)  
[<span data-ttu-id="2e319-160">Administrar proveedores federados SIP para la organización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e319-160">Manage SIP federated providers for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-providers-for-your-organization.md)  
[<span data-ttu-id="2e319-161">Set-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2e319-161">Set-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsExternalAccessPolicy)  
[<span data-ttu-id="2e319-162">Nuevo: CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2e319-162">New-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsExternalAccessPolicy)  
[<span data-ttu-id="2e319-163">Get-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2e319-163">Get-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsExternalAccessPolicy)  
[<span data-ttu-id="2e319-164">Remove-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2e319-164">Remove-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsExternalAccessPolicy)  
[<span data-ttu-id="2e319-165">Grant-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2e319-165">Grant-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsExternalAccessPolicy)  
  

<span data-ttu-id="2e319-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2e319-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

