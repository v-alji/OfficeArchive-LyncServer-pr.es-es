---
title: 'Lync Server 2013: Configuración de la directiva de movilidad'
description: 'Lync Server 2013: configuración de la Directiva de movilidad.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring mobility policy
ms:assetid: 595536e0-9bb3-49a3-8d13-1a77351ebc62
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690018(v=OCS.15)
ms:contentKeyID: 48184204
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbbf7f9db54c8436f2db24d593dbd7a1372d5e00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432922"
---
# <a name="configuring-mobility-policy-in-lync-server-2013"></a><span data-ttu-id="33979-103">Configuración de la directiva de movilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33979-103">Configuring mobility policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="33979-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="33979-104">

<span> </span></span></span>

<span data-ttu-id="33979-105">_**Última modificación del tema:** 2013-02-13_</span><span class="sxs-lookup"><span data-stu-id="33979-105">_**Topic Last Modified:** 2013-02-13_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="33979-106">Lync Server 2013 proporciona directivas de movilidad que determinan quién puede usar las características de movilidad, llamar a través del trabajo, voz sobre IP (VoIP) o vídeo, y si se necesitará WiFi para VoIP o video.</span><span class="sxs-lookup"><span data-stu-id="33979-106">Lync Server 2013 provides mobility policies that determine who can use mobility features, Call via Work, voice over IP (VoIP) or video, and whether WiFi will be required for either VoIP or video.</span></span> <span data-ttu-id="33979-107">La característica llamar a través del trabajo permite a un usuario móvil realizar y recibir llamadas en un teléfono móvil con un número de teléfono del trabajo en lugar del número de teléfono móvil.</span><span class="sxs-lookup"><span data-stu-id="33979-107">The Call via Work feature enables a mobile user to make and receive calls on a mobile phone by using a work phone number instead of the mobile phone number.</span></span> <span data-ttu-id="33979-108">Esta característica impide que la persona llamada Vea el número de teléfono móvil de la persona que llama y permite a un usuario evitar cargos por llamadas salientes.</span><span class="sxs-lookup"><span data-stu-id="33979-108">This feature prevents the called party from seeing the caller's mobile phone number and enables a user to avoid outbound calling charges.</span></span> <span data-ttu-id="33979-109">La configuración de VoIP y vídeo permite que los usuarios reciban y realicen llamadas y videollamadas con VoIP.</span><span class="sxs-lookup"><span data-stu-id="33979-109">Configuring VoIP and video makes it possible for users to receive and make VoIP calls and video.</span></span> <span data-ttu-id="33979-110">Configuración para uso de WiFi defina si el dispositivo de un usuario necesita usar una red WiFi a través de una red de datos móviles.</span><span class="sxs-lookup"><span data-stu-id="33979-110">Settings for WiFi usage define if a user’s device will be required to use a WiFi network over a cellular data network.</span></span>

<span data-ttu-id="33979-111">De forma predeterminada, la movilidad, la llamada a través del trabajo y las características de VoIP y vídeo están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="33979-111">By default, mobility, Call via Work, and the VoIP and video features are enabled.</span></span> <span data-ttu-id="33979-112">La configuración para requerir WiFi para VoIp y vídeo está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="33979-112">The settings to require WiFi for VoIp and video are disabled.</span></span> <span data-ttu-id="33979-113">Los administradores pueden determinar quién tiene acceso a estas características ejecutando un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33979-113">Administrators can determine who has access to these features by running a cmdlet.</span></span> <span data-ttu-id="33979-114">Puede desactivar las opciones globalmente, por sitio o por usuario.</span><span class="sxs-lookup"><span data-stu-id="33979-114">You can turn options off globally, by site, or by user.</span></span>

<span data-ttu-id="33979-115">Para poder usar las características de movilidad y llamar a través del trabajo, los usuarios deben cumplir los siguientes requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="33979-115">To be able to use mobility features and Call via Work, users must meet the following prerequisites:</span></span>

  - <span data-ttu-id="33979-116">Los usuarios deben estar habilitados para Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="33979-116">Users must be enabled for Lync Server 2013.</span></span>

  - <span data-ttu-id="33979-117">Los usuarios deben estar habilitados para telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="33979-117">Users must be enabled for Enterprise Voice.</span></span>

  - <span data-ttu-id="33979-118">Los usuarios deben tener asignada una directiva de movilidad que tenga la opción **EnableMobility** establecida en true.</span><span class="sxs-lookup"><span data-stu-id="33979-118">Users must be assigned a mobility policy that has the **EnableMobility** option set to True.</span></span>

<span data-ttu-id="33979-119">Para que los usuarios puedan usar las llamadas a través del trabajo, deben cumplir los siguientes dos requisitos previos adicionales:</span><span class="sxs-lookup"><span data-stu-id="33979-119">For users to be able to use Call via Work, they must meet the following two additional prerequisites:</span></span>

  - <span data-ttu-id="33979-120">A los usuarios se les debe asignar una directiva de voz que tenga seleccionada la opción **Habilitar llamadas simultáneas a teléfonos** .</span><span class="sxs-lookup"><span data-stu-id="33979-120">Users must be assigned a voice policy that has the **Enable simultaneous ringing of phones** option selected.</span></span>

  - <span data-ttu-id="33979-121">Los usuarios deben tener asignada una directiva de movilidad que tenga la opción **EnableOutsideVoice** establecida en true.</span><span class="sxs-lookup"><span data-stu-id="33979-121">Users must be assigned a mobility policy that has the **EnableOutsideVoice** option set to True.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="33979-122">Los usuarios que no tienen habilitada la telefonía IP empresarial pueden usar sus dispositivos móviles para hacer llamadas de voz sobre IP (VoIP) de Lync a Lync o pueden unirse a conferencias con el vínculo haga clic para unirse en sus dispositivos móviles, si asigna a esos usuarios las opciones adecuadas para la Directiva de voz.</span><span class="sxs-lookup"><span data-stu-id="33979-122">Users who are not enabled for Enterprise Voice can use their mobile devices to make Lync to Lync Voice over IP (VoIP) calls, or can join conferences by using the Click to Join link on their mobile devices, if you assign those users the appropriate options for voice policy.</span></span> <span data-ttu-id="33979-123">Para obtener más información, vea <A href="lync-server-2013-defining-your-mobility-requirements.md">definir los requisitos de movilidad para Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="33979-123">For details, see <A href="lync-server-2013-defining-your-mobility-requirements.md">Defining your mobility requirements for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="33979-124">Para obtener más información sobre cómo habilitar usuarios para Lync Server 2013, vea [deshabilitar o volver a habilitar la cuenta de usuario para Lync server 2013](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="33979-124">For details about enabling users for Lync Server 2013, see [Disable or re-enable user account for Lync Server 2013](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md).</span></span> <span data-ttu-id="33979-125">Para obtener más información sobre cómo habilitar usuarios para telefonía IP empresarial, consulte [Habilitar usuarios para telefonía IP empresarial en Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span><span class="sxs-lookup"><span data-stu-id="33979-125">For details about enabling users for Enterprise Voice, see [Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span></span> <span data-ttu-id="33979-126">Para obtener más información sobre cómo configurar las opciones de directiva de voz, consulte [modificar una directiva de voz y configurar los registros de uso de RTC en Lync Server 2013](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md).</span><span class="sxs-lookup"><span data-stu-id="33979-126">For details about setting voice policy options, see [Modify a voice policy and configure PSTN usage records in Lync Server 2013](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md).</span></span>

<div>

## <a name="to-modify-global-mobility-policy"></a><span data-ttu-id="33979-127">Para modificar la Directiva de movilidad global</span><span class="sxs-lookup"><span data-stu-id="33979-127">To modify global mobility policy</span></span>

1.  <span data-ttu-id="33979-128">Inicie sesión en cualquier equipo donde esté instalado shell de administración de Lync Server y Ocscore como miembro del rol CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="33979-128">Log on to any computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="33979-129">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="33979-129">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="33979-130">Desactiva el acceso a la movilidad y llama a través del trabajo de forma global.</span><span class="sxs-lookup"><span data-stu-id="33979-130">Turn off access to mobility and Call via Work globally.</span></span> <span data-ttu-id="33979-131">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="33979-131">At the command line, type:</span></span>
    
        Set-CsMobilityPolicy -EnableMobility $False -EnableOutsideVoice $False
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="33979-132">Puede desactivar la llamada por trabajo sin desactivar el acceso a la movilidad.</span><span class="sxs-lookup"><span data-stu-id="33979-132">You can turn off Call via Work without turning off access to mobility.</span></span> <span data-ttu-id="33979-133">Sin embargo, no puede desactivar la movilidad sin desactivar también la llamada a través del trabajo.</span><span class="sxs-lookup"><span data-stu-id="33979-133">However, you cannot turn off mobility without also turning off Call via Work.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-mobility-policy-by-site"></a><span data-ttu-id="33979-134">Para modificar la Directiva de movilidad por sitio</span><span class="sxs-lookup"><span data-stu-id="33979-134">To modify mobility policy by site</span></span>

1.  <span data-ttu-id="33979-135">Inicie sesión en cualquier equipo donde esté instalado shell de administración de Lync Server y Ocscore como miembro del rol CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="33979-135">Log on to any computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="33979-136">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="33979-136">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="33979-137">Cree una directiva de nivel de sitio, desactive VoIP y vídeo, y habilite la opción requerir WiFi para audio IP y para video IP por sitio.</span><span class="sxs-lookup"><span data-stu-id="33979-137">Create a site-level policy, and turn off VoIP and video, and enable Require WiFi for IP Audio and for IP Video by site.</span></span> <span data-ttu-id="33979-138">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="33979-138">At the command line, type:</span></span>
    
        New-CsMobilityPolicy -Identity site:<site identifier> -EnableIPAudioVideo $False -RequireWiFiForIPAudio $True -RequireWiFiForIPVideo $True

</div>

<div>

## <a name="to-modify-mobility-policy-by-user"></a><span data-ttu-id="33979-139">Para modificar la Directiva de movilidad por usuario</span><span class="sxs-lookup"><span data-stu-id="33979-139">To modify mobility policy by user</span></span>

1.  <span data-ttu-id="33979-140">Inicie sesión en cualquier equipo donde esté instalado shell de administración de Lync Server y Ocscore como miembro del rol CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="33979-140">Log on to any computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="33979-141">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="33979-141">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="33979-142">Crear directivas de movilidad de nivel de usuario y desactivar la movilidad y la llamada a través del trabajo por usuario.</span><span class="sxs-lookup"><span data-stu-id="33979-142">Create user level mobility policies and turn off mobility and Call via Work by user.</span></span> <span data-ttu-id="33979-143">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="33979-143">At the command line, type:</span></span>
    
        New-CsMobilityPolicy -Identity <policy name> -EnableMobility $False -EnableOutsideVoice $False
        Grant-CsMobilityPolicy -Identity <user identifier> -PolicyName <policy name>
    
    <span data-ttu-id="33979-144">Puede desactivar la llamada por trabajo sin desactivar el acceso a la movilidad.</span><span class="sxs-lookup"><span data-stu-id="33979-144">You can turn off Call via Work without turning off access to mobility.</span></span> <span data-ttu-id="33979-145">Sin embargo, no puede desactivar la movilidad sin desactivar también la llamada a través del trabajo.</span><span class="sxs-lookup"><span data-stu-id="33979-145">However, you cannot turn off mobility without also turning off Call via Work.</span></span>
    
    <span data-ttu-id="33979-146">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="33979-146">For example:</span></span>
    
        New-CsMobilityPolicy "tag:disableOutsideVoice" -EnableOutsideVoice $False
        Grant-CsMobilityPolicy -Identity -MobileUser1@contoso.com -PolicyName Tag:disableOutsideVoice

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="33979-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="33979-147">See Also</span></span>


[<span data-ttu-id="33979-148">Deshabilitar o volver a habilitar la cuenta de usuario para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33979-148">Disable or re-enable user account for Lync Server 2013</span></span>](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  
[<span data-ttu-id="33979-149">Habilitar usuarios para telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33979-149">Enable users for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-enable-users-for-enterprise-voice.md)  
[<span data-ttu-id="33979-150">Modificar una directiva de voz y configurar los registros de uso de RTC en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33979-150">Modify a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md)  


[<span data-ttu-id="33979-151">Definir los requisitos de movilidad para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33979-151">Defining your mobility requirements for Lync Server 2013</span></span>](lync-server-2013-defining-your-mobility-requirements.md)  


[<span data-ttu-id="33979-152">New-CsMobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="33979-152">New-CsMobilityPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy)  
[<span data-ttu-id="33979-153">Set-CsMobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="33979-153">Set-CsMobilityPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy)  
[<span data-ttu-id="33979-154">Get-CsMobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="33979-154">Get-CsMobilityPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsMobilityPolicy)  
[<span data-ttu-id="33979-155">Grant-CsMobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="33979-155">Grant-CsMobilityPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsMobilityPolicy)  
[<span data-ttu-id="33979-156">Remove-CsMobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="33979-156">Remove-CsMobilityPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsMobilityPolicy)  
  

<span data-ttu-id="33979-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="33979-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

