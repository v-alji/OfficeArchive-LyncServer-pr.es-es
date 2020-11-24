---
title: 'Lync Server 2013: Configurar directivas para controlar el acceso de usuarios federados de XMPP'
description: 'Lync Server 2013: configurar directivas para controlar el acceso de usuarios de XMPP federado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure policies to control XMPP federated user access
ms:assetid: 0fe0ff75-e52a-4e3e-923a-64f6412ac4e4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552446(v=OCS.15)
ms:contentKeyID: 48679557
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cdb2b7a3da6c00aa7725ecbb69856756f229ed97
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399365"
---
# <a name="configure-policies-to-control-xmpp-federated-user-access-in-lync-server-2013"></a><span data-ttu-id="e4407-103">Configurar directivas para controlar el acceso de usuarios federados de XMPP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4407-103">Configure policies to control XMPP federated user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e4407-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e4407-104">

<span> </span></span></span>

<span data-ttu-id="e4407-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="e4407-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="e4407-106">Esta documentación es preliminar y está sujeta a cambios.</span><span class="sxs-lookup"><span data-stu-id="e4407-106">This is preliminary documentation and is subject to change.</span></span> <span data-ttu-id="e4407-107">Los temas en blanco que se incluyen actúan como marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="e4407-107">Blank topics are included as placeholders.</span></span>

<span data-ttu-id="e4407-108">Al configurar directivas para la compatibilidad de los socios federados protocolo de presencia y mensajería extensible (XMPP), las directivas se aplican a los usuarios de XMPP Federated Domains, pero no a los usuarios de proveedores de servicios de mensajería instantánea (mi) o de protocolo de inicio de sesión (por ejemplo, Windows Live) ni a los dominios federados de SIP.</span><span class="sxs-lookup"><span data-stu-id="e4407-108">When you configure policies for support of extensible messaging and presence protocol (XMPP) federated partners, the policies apply to users of XMPP federated domains, but not to users of session initiation protocol (SIP) instant messaging (IM) service providers (for example, Windows Live), or SIP federated domains.</span></span> <span data-ttu-id="e4407-109">Configure un **socio de XMPP federado** para cada dominio de XMPP federado que desee permitir a los usuarios que añadan contactos y se comuniquen con ellos.</span><span class="sxs-lookup"><span data-stu-id="e4407-109">You configure an **XMPP Federated Partner** for each XMPP federated domain that you want to allow your users to add contacts and communicate with.</span></span> <span data-ttu-id="e4407-110">Las directivas de socios de XMPP federados solo están disponibles en un solo ámbito, aunque no se define como una directiva global, actúa como una directiva global.</span><span class="sxs-lookup"><span data-stu-id="e4407-110">XMPP federated partners policies are only available in a single scope, though it is not defined as a global policy, acts as a global policy.</span></span> <span data-ttu-id="e4407-111">Para definir una directiva global, de sitio o de usuario para los asociados de Federación de XMPP, debe configurar el ámbito de la Directiva creando y configurando en primer lugar la Directiva de acceso externo para el ámbito que necesite.</span><span class="sxs-lookup"><span data-stu-id="e4407-111">To define a global, site or user policy for XMPP Federation Partners, you configure the policy scope by first creating and configuring the External Access Policy for the scope you require.</span></span> <span data-ttu-id="e4407-112">Para obtener más información sobre los tipos de directivas que puede configurar para el acceso externo y la Federación, consulte [administrar la Federación y el acceso externo a Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md) en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="e4407-112">For details about the types of policies that you can configure for external access and federation, see [Managing federation and external access to Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md) in the Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e4407-113">Todas las directivas de <STRONG>Federación y acceso externo</STRONG> se aplican mediante aprovisionamiento en banda.</span><span class="sxs-lookup"><span data-stu-id="e4407-113">All <STRONG>Federation and External Access</STRONG> policies are applied through in-band provisioning.</span></span> <span data-ttu-id="e4407-114">Las directivas que se aplican al usuario, pertenecen a un sitio o que se encuentran en ámbito global se comunican al cliente durante el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e4407-114">The policies that apply to the user, belong to a site, or are global in scope are communicated to the client during login.</span></span> <span data-ttu-id="e4407-115">Puede configurar directivas para controlar el acceso al socio XMPP federado, incluso si no ha habilitado la Federación de XMPP para su organización.</span><span class="sxs-lookup"><span data-stu-id="e4407-115">You can configure policies to control XMPP federated partner access, even if you have not enabled XMPP federation for your organization.</span></span> <span data-ttu-id="e4407-116">Sin embargo, las directivas que configure se aplicarán solamente cuando tenga la Federación XMPP Partner implementada, habilitada y configurada para su organización.</span><span class="sxs-lookup"><span data-stu-id="e4407-116">However, the policies that you configure take effect only when you have XMPP partner federation deployed, enabled and configured for your organization.</span></span> <span data-ttu-id="e4407-117">Para obtener más información sobre cómo implementar y configurar la Federación de socios XMPP, vea <A href="lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md">configurar la Federación SIP, la Federación XMPP y la mensajería instantánea pública en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="e4407-117">For details about deploying and configuring XMPP partner federation, see <A href="lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md">Configuring SIP federation, XMPP federation and public instant messaging in Lync Server 2013</A> in the Deployment documentation.</span></span> <span data-ttu-id="e4407-118">Además, si especifica una directiva de usuario en la Directiva de acceso externo para controlar los socios federados de XMPP, la Directiva solo se aplica a los usuarios que están habilitados para Lync Server 2013 y se han configurado para usar la Directiva.</span><span class="sxs-lookup"><span data-stu-id="e4407-118">Additionally, if you specify a user policy in External Access Policy to control XMPP federated partners, the policy applies only to users that are enabled for Lync Server 2013 and configured to use the policy.</span></span>



</div>

<div>

## <a name="to-edit-a-global-policy-for-xmpp-federated-partners"></a><span data-ttu-id="e4407-119">Para editar una directiva global para los socios de XMPP federados</span><span class="sxs-lookup"><span data-stu-id="e4407-119">To edit a global policy for XMPP federated partners</span></span>

1.  <span data-ttu-id="e4407-120">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="e4407-120">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e4407-121">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e4407-121">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e4407-122">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e4407-122">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e4407-123">En la barra de navegación izquierda, haga clic en **acceso de usuarios externos** y, después, en **Directiva de acceso externo**.</span><span class="sxs-lookup"><span data-stu-id="e4407-123">In the left navigation bar, click **External User Access**, and then click **External Access Policy**.</span></span>

4.  <span data-ttu-id="e4407-124">En la página **Directiva de acceso externo** , haga lo siguiente para la directiva global:</span><span class="sxs-lookup"><span data-stu-id="e4407-124">On the **External Access Policy** page, do the following for the global policy:</span></span>

5.  <span data-ttu-id="e4407-125">Haga clic en la directiva global, haga clic en **Editar** y, a continuación, haga clic en Mostrar detalles.</span><span class="sxs-lookup"><span data-stu-id="e4407-125">Click the global policy, click **Edit**, and then click Show details.</span></span>

6.  <span data-ttu-id="e4407-126">Proporcione una descripción para la directiva global (opcional).</span><span class="sxs-lookup"><span data-stu-id="e4407-126">Provide a description for the Global policy (optional).</span></span>

7.  <span data-ttu-id="e4407-127">Seleccione **Habilitar comunicaciones con usuarios federados**.</span><span class="sxs-lookup"><span data-stu-id="e4407-127">Select **Enable communications with federated users**.</span></span>

8.  <span data-ttu-id="e4407-128">Seleccione **Habilitar comunicaciones con usuarios federados de XMPP**.</span><span class="sxs-lookup"><span data-stu-id="e4407-128">Select **Enable communications with XMPP federated users**.</span></span>

9.  <span data-ttu-id="e4407-129">Haga clic en **confirmar** para guardar los cambios en la directiva global.</span><span class="sxs-lookup"><span data-stu-id="e4407-129">Click **Commit** to save your changes to the Global policy.</span></span>

</div>

<div>

## <a name="to-create-a-site-or-user-policy-for-xmpp-federated-partners"></a><span data-ttu-id="e4407-130">Para crear un sitio o una directiva de usuario para socios de XMPP federados</span><span class="sxs-lookup"><span data-stu-id="e4407-130">To create a site or user policy for XMPP federated partners</span></span>

1.  <span data-ttu-id="e4407-131">Haga clic en **nuevo** y, a continuación, en **Directiva del sitio** o **Directiva de usuario**.</span><span class="sxs-lookup"><span data-stu-id="e4407-131">Click **New**, and then click **Site policy** or **User policy**.</span></span> <span data-ttu-id="e4407-132">En **seleccionar un sitio**, haga clic en el sitio adecuado de la lista y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e4407-132">In **Select a Site**, click the appropriate site from the list and then click **OK**.</span></span>

2.  <span data-ttu-id="e4407-133">Proporcione una descripción para la Directiva de sitio (opcional).</span><span class="sxs-lookup"><span data-stu-id="e4407-133">Provide a description for the Site policy (optional).</span></span>

3.  <span data-ttu-id="e4407-134">En el sitio o la Directiva de usuario, seleccione **habilitar las comunicaciones con usuarios federados**.</span><span class="sxs-lookup"><span data-stu-id="e4407-134">In the site or user policy, select **Enable communications with federated users**.</span></span>

4.  <span data-ttu-id="e4407-135">Seleccione **Habilitar comunicaciones con usuarios federados de XMPP**.</span><span class="sxs-lookup"><span data-stu-id="e4407-135">Select **Enable communications with XMPP federated users**.</span></span>

5.  <span data-ttu-id="e4407-136">Haga clic en **confirmar** para guardar los cambios en el sitio o en la Directiva de usuario.</span><span class="sxs-lookup"><span data-stu-id="e4407-136">Click **Commit** to save your changes to the site or user policy.</span></span>

</div>

<div>

## <a name="to-edit-an-existing-policy-for-xmpp-federated-partners"></a><span data-ttu-id="e4407-137">Para editar una directiva existente para socios de XMPP federados</span><span class="sxs-lookup"><span data-stu-id="e4407-137">To edit an existing policy for XMPP federated partners</span></span>

1.  <span data-ttu-id="e4407-138">Para cambiar una directiva existente, seleccione la directiva correspondiente en la lista, haga clic en **Editar** y, a continuación, haga clic en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="e4407-138">To change an existing policy, select the appropriate policy in the list, click **Edit**, and then click **Show details**.</span></span>

2.  <span data-ttu-id="e4407-139">Cambiar o actualizar la descripción de la Directiva (opcional).</span><span class="sxs-lookup"><span data-stu-id="e4407-139">Change or update the description for the policy (optional).</span></span>

3.  <span data-ttu-id="e4407-140">Active o desactive **Habilitar comunicaciones con usuarios federados**.</span><span class="sxs-lookup"><span data-stu-id="e4407-140">Select or unselect **Enable communications with federated users**.</span></span>

4.  <span data-ttu-id="e4407-141">Active o desactive **Habilitar comunicaciones con usuarios federados de XMPP**.</span><span class="sxs-lookup"><span data-stu-id="e4407-141">Select or unselect **Enable communications with XMPP federated users**.</span></span>

5.  <span data-ttu-id="e4407-142">Haga clic en **confirmar** para guardar los cambios en la Directiva.</span><span class="sxs-lookup"><span data-stu-id="e4407-142">Click **Commit** to save your changes to the policy.</span></span>

</div>

<div>

## <a name="to-edit-an-existing-policy-for-xmpp-federated-partners-by-using-windows-powershell"></a><span data-ttu-id="e4407-143">Para editar una directiva existente para los socios de XMPP federados mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4407-143">To edit an existing policy for XMPP federated partners by using Windows PowerShell</span></span>

1.  <span data-ttu-id="e4407-144">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="e4407-144">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e4407-145">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e4407-145">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e4407-146">Escriba lo siguiente en el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="e4407-146">Type the following in the Lync Server Management Shell:</span></span>
    
        Set-CsExternalAccessPolicy -Identity <name of global, site or user policy - policy must exist when using Set-CsExternalAccessPolicy > -Description <descriptive name for policy> -EnableFederationAccess <$true, $false> -EnableXmppAccess <$true, $false>
    
    <span data-ttu-id="e4407-147">Un comando de ejemplo que establecerá la directiva global para el acceso de usuarios federados a verdadero (habilitado) y el acceso al dominio XMPP a verdadero (habilitado):</span><span class="sxs-lookup"><span data-stu-id="e4407-147">An example command that will set the global policy for Federated user access to True (enabled) and XMPP domain access to True (enabled):</span></span>
    
        Set-CsExternalAccessPolicy -Identity global -EnableFederationAccess $true -EnableXmppAccess $true

</div>

<div>

## <a name="to-create-a-site-or-user-policy-for-xmpp-federated-partners-using-windows-powershell"></a><span data-ttu-id="e4407-148">Para crear un sitio o una directiva de usuario para socios de XMPP federados con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4407-148">To create a site or user policy for XMPP federated partners using Windows PowerShell</span></span>

1.  <span data-ttu-id="e4407-149">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="e4407-149">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e4407-150">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e4407-150">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e4407-151">Escriba lo siguiente en el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="e4407-151">Type the following in the Lync Server Management Shell:</span></span>
    
        New-CsExternalAccessPolicy -Identity <name of global, site or user policy - policy must exist when using Set-CsExternalAccessPolicy > -Description <descriptive name for policy> -EnableFederationAccess <$true, $false> -EnableXmppAccess <$true, $false>
    
    <span data-ttu-id="e4407-152">Un comando de ejemplo que establecerá una directiva de sitio para el sitio de Redmond para el acceso de usuarios federados a habilitado y el acceso al dominio XMPP a habilitado:</span><span class="sxs-lookup"><span data-stu-id="e4407-152">An example command that will set a site policy for the Redmond site for Federated user access to enabled and XMPP domain access to enabled:</span></span>
    
        New-CsExternalAccessPolicy -Identity site:Redmond -EnableFederationAccess $true -EnableXmppAccess $true

</div>

<div>

## <a name="to-delete-an-existing-policy-for-xmpp-federated-partners-by-using-windows-powershell"></a><span data-ttu-id="e4407-153">Para eliminar una directiva existente para los socios de XMPP federados mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4407-153">To delete an existing policy for XMPP federated partners by using Windows PowerShell</span></span>

1.  <span data-ttu-id="e4407-154">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="e4407-154">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e4407-155">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e4407-155">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e4407-156">Escriba lo siguiente en el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="e4407-156">Type the following in the Lync Server Management Shell:</span></span>
    
        Remove-CsExternalAccessPolicy -Identity <name of global, site or user policy>
    
    <span data-ttu-id="e4407-157">Un comando de ejemplo que eliminará una directiva de usuario:</span><span class="sxs-lookup"><span data-stu-id="e4407-157">An example command that will delete a user policy:</span></span>
    
        Remove-CsExternalAccessPolicy -Identity EAPUserPolicySetXMPP

4.  <span data-ttu-id="e4407-158">Un comando de ejemplo que restablecerá la directiva global a los valores predeterminados:</span><span class="sxs-lookup"><span data-stu-id="e4407-158">An example command that will reset the global policy to defaults:</span></span>
    
        Remove-CsExternalAccessPolicy -Identity global

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e4407-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4407-159">See Also</span></span>


[<span data-ttu-id="e4407-160">Asignar una directiva de acceso de usuario externo a un usuario habilitado para Lync en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4407-160">Assign an external user access policy to a Lync enabled user in Lync Server 2013</span></span>](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)  
[<span data-ttu-id="e4407-161">Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4407-161">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)  


[<span data-ttu-id="e4407-162">Administrar socios federados XMPP para su organización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4407-162">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
[<span data-ttu-id="e4407-163">Set-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4407-163">Set-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsExternalAccessPolicy)  
[<span data-ttu-id="e4407-164">Nuevo: CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4407-164">New-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsExternalAccessPolicy)  
[<span data-ttu-id="e4407-165">Get-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4407-165">Get-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsExternalAccessPolicy)  
[<span data-ttu-id="e4407-166">Remove-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4407-166">Remove-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsExternalAccessPolicy)  
[<span data-ttu-id="e4407-167">Grant-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4407-167">Grant-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsExternalAccessPolicy)  
  

<span data-ttu-id="e4407-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e4407-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

