---
title: 'Lync Server 2013: implementación de la apariencia de línea compartida'
description: 'Lync Server 2013: implementar la apariencia de la línea compartida.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy Shared Line Appearance
ms:assetid: 6666dfef-9ecf-4834-af6a-2d5da227dfa3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Mt712152(v=OCS.15)
ms:contentKeyID: 72522137
ms.date: 06/13/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c83c06bbc9b91e11cabc0abee20de28fc7281205
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430178"
---
# <a name="deploy-shared-line-appearance-in-lync-server-2013"></a><span data-ttu-id="c277d-103">Implementar la apariencia de línea compartida en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c277d-103">Deploy Shared Line Appearance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c277d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c277d-104">

<span> </span></span></span>

<span data-ttu-id="c277d-105">_**Última modificación del tema:** 2016-06-13_</span><span class="sxs-lookup"><span data-stu-id="c277d-105">_**Topic Last Modified:** 2016-06-13_</span></span>

<span data-ttu-id="c277d-106">Lea este tema para obtener información sobre cómo implementar el aspecto de línea compartida (SLA) en Lync Server 2013, actualización acumulativa de abril de 2016.</span><span class="sxs-lookup"><span data-stu-id="c277d-106">Read this topic to learn how to deploy Shared Line Appearance (SLA) in Lync Server 2013, Cumulative Update April 2016.</span></span> <span data-ttu-id="c277d-107">Apariencia de líneas compartida es una característica para administrar varias llamadas en un número específico, denominado número compartido.</span><span class="sxs-lookup"><span data-stu-id="c277d-107">SLA is a feature for handling multiple calls on a specific number called a shared number.</span></span>

<span data-ttu-id="c277d-108">Para obtener más información sobre esta característica, vea [planear la apariencia de líneas compartidas en Lync Server 2013](lync-server-2013-plan-for-shared-line-appearance.md).</span><span class="sxs-lookup"><span data-stu-id="c277d-108">For more information about this feature, see [Plan for Shared Line Appearance in Lync Server 2013](lync-server-2013-plan-for-shared-line-appearance.md).</span></span>

<span data-ttu-id="c277d-109">La apariencia de línea compartida (SLA) es una característica nueva de Lync Server 2013, actualización acumulativa de abril de 2016.</span><span class="sxs-lookup"><span data-stu-id="c277d-109">Shared Line Appearance (SLA) is a new feature in Lync Server 2013, Cumulative Update April 2016.</span></span> <span data-ttu-id="c277d-110">Para habilitar esta característica, primero tiene que implementar esta actualización acumulativa.</span><span class="sxs-lookup"><span data-stu-id="c277d-110">To enable this feature, you must have first deployed this cumulative update.</span></span>

<div>

## <a name="install-shared-line-appearance"></a><span data-ttu-id="c277d-111">Instalar Apariencia de línea compartida</span><span class="sxs-lookup"><span data-stu-id="c277d-111">Install Shared Line Appearance</span></span>

1.  <span data-ttu-id="c277d-112">Después de implementar Lync Server 2013, la actualización acumulativa de abril de 2016, la aplicación SLA no está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c277d-112">After Lync Server 2013, Cumulative Update April 2016 is deployed, the SLA application is not enabled by default.</span></span> <span data-ttu-id="c277d-113">Para habilitar la aplicación, siga los pasos que se indican a continuación:</span><span class="sxs-lookup"><span data-stu-id="c277d-113">To enable the application, follow the steps below:</span></span>
    
    1.  <span data-ttu-id="c277d-114">Registre SLA como una aplicación de servidor; para ello, ejecute el comando siguiente para cada grupo:</span><span class="sxs-lookup"><span data-stu-id="c277d-114">Register SLA as a server application by running the following command for each pool:</span></span>
        ```powershell
        New-CsServerApplication -Identity
                        'Service:Registrar:%FQDN%/SharedLineAppearance' -Uri
                        http://www.microsoft.com/LCS/SharedLineAppearance -Critical $false -Enabled
                        $true -Priority (Get-CsServerApplication -Identity
                        'Service:Registrar:%FQDN%/UserServices').Priority 
        ```
        <span data-ttu-id="c277d-115">donde %FQDN% es el nombre de dominio completo del grupo.</span><span class="sxs-lookup"><span data-stu-id="c277d-115">where %FQDN% is the fully qualified domain name of the pool.</span></span>
    
    2.  <span data-ttu-id="c277d-116">Ejecute el comando siguiente para actualizar los roles RBAC para los cmdlets de SLA:</span><span class="sxs-lookup"><span data-stu-id="c277d-116">Run the following command to update the RBAC roles for the SLA cmdlets:</span></span>
        ```powershell
        Update-CsAdminRole 
        ```
    3.  <span data-ttu-id="c277d-117">Reinicie todos los servidores front-end (servicio RTCSRV) en todos los grupos donde se instaló y habilitó SLA:</span><span class="sxs-lookup"><span data-stu-id="c277d-117">Restart all the Front End Servers (RTCSRV service) in all the pools where SLA was installed and enabled:</span></span>
        
        ```powershell 
        Stop-CsWindowsService RTCSRV Start-CsWindowsService RTCSRV
                        
        ```

</div>

<div>

## <a name="create-an-sla-group-and-add-users-to-it"></a><span data-ttu-id="c277d-118">Crear un grupo de SLA y agregar usuarios</span><span class="sxs-lookup"><span data-stu-id="c277d-118">Create an SLA group and add users to it</span></span>

1.  <span data-ttu-id="c277d-119">Para crear el grupo de SLA, use el cmdlet de [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration):</span><span class="sxs-lookup"><span data-stu-id="c277d-119">Create the SLA group by using the [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity <IdentityOfGroup>
                -MaxNumberOfCalls <Number> -BusyOption
                <BusyOnBusy|Voicemail|Forward> [-Target
                <TargetUserOrPhoneNumber>]
    ```
    <span data-ttu-id="c277d-p104">El cmdlet Set-CsSlaConfiguration marca la cuenta de telefonía IP empresarial SLAGrupo1 como una entidad de SLA y el número de SLAGrupo1 se convierte en el número para el grupo de SLA. Todas las llamadas del SLAGrupo1 llamarán a todo el grupo de SLA.</span><span class="sxs-lookup"><span data-stu-id="c277d-p104">The Set-CsSlaConfiguration cmdlet marks the Enterprise Voice account SLAGroup1 as an SLA entity, and the number of SLAGroup1 becomes the number for the SLA group. All calls to SLAGroup1 will ring the entire SLA group.</span></span>
    
    <span data-ttu-id="c277d-122">En el ejemplo siguiente se crea un grupo de SLA para un usuario de telefonía IP empresarial existente (SLAGrupo1) y se usa el número asignado para SLAGrupo1 como el número de la línea principal de SLA.</span><span class="sxs-lookup"><span data-stu-id="c277d-122">The following example creates an SLA group for an existing Enterprise Voice user, SLAGroup1, and uses the number assigned for SLAGroup1 as the SLA mainline number.</span></span>
    
    <span data-ttu-id="c277d-123">El comando establece el número máximo de llamadas simultáneas para el nuevo grupo de SLA en 3 y configura las llamadas que superen ese número para que escuchen una señal de línea ocupada:</span><span class="sxs-lookup"><span data-stu-id="c277d-123">The command sets the maximum number of concurrent calls for the new SLA group to 3, and for calls in excess of that to hear a busy signal:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity SLAGroup1 -MaxNumberOfCalls 3
                -BusyOption BusyOnBusy
    ```
    <span data-ttu-id="c277d-124">Puede usar Set-CsSlaConfiguration para crear un grupo de SLA o modificar uno existente.</span><span class="sxs-lookup"><span data-stu-id="c277d-124">You can use Set-CsSlaConfiguration to create a new SLA group or modify an existing one.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c277d-125">Ten en cuenta que lo que especifiques <CODE>-Identity</CODE> debe ser una cuenta de usuario válida habilitada para voz de empresa existente.</span><span class="sxs-lookup"><span data-stu-id="c277d-125">Note that what you specify for <CODE>-Identity</CODE> must be a valid existing Enterprise Voice-enabled user account.</span></span>

    
    </div>

2.  <span data-ttu-id="c277d-126">Agregue delegados al grupo con el cmdlet [Add-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/add-cssladelegates):</span><span class="sxs-lookup"><span data-stu-id="c277d-126">Add delegates to the group by using the [Add-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/add-cssladelegates) cmdlet:</span></span>
    ```powershell
    Add-CsSlaDelegates -Identity <IdentityOfGroup> -Delegate
              <NameOfDelegate@domain>
    ```
    <span data-ttu-id="c277d-127">En el ejemplo siguiente se agrega un usuario al grupo de SLA.</span><span class="sxs-lookup"><span data-stu-id="c277d-127">The following example adds a user to the SLA group.</span></span> <span data-ttu-id="c277d-128">Cada usuario agregado al grupo debe ser un usuario válido habilitado para voz empresarial:</span><span class="sxs-lookup"><span data-stu-id="c277d-128">Each user added to the group must be a valid Enterprise Voice-enabled user:</span></span>
    ```powershell
    Add-CsSlaDelegates -Identity SLAGroup1 -Delegate
              sip:SLA_Delegate1@contoso.com
    ```
    <span data-ttu-id="c277d-p106">Repita el cmdlet para cada usuario que quiera agregar al grupo. Los usuarios solo pueden pertenecer a un único grupo de SLA.</span><span class="sxs-lookup"><span data-stu-id="c277d-p106">Repeat the cmdlet for each user you want to add to the group. Users can only belong to a single SLA group.</span></span>

</div>

<div>

## <a name="configure-the-sla-group-busy-option"></a><span data-ttu-id="c277d-131">Configurar la opción de ocupado del grupo de SLA</span><span class="sxs-lookup"><span data-stu-id="c277d-131">Configure the SLA group Busy Option</span></span>

1.  <span data-ttu-id="c277d-132">Configure la opción de ocupado del grupo de SLA con el cmdlet [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration):</span><span class="sxs-lookup"><span data-stu-id="c277d-132">Configure the SLA group Busy Option by using the [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity <IdentityOfGroup>
              -BusyOption <Option> [-Target <TargetUserOrPhoneNumber>]
    ```
    <span data-ttu-id="c277d-133">En el ejemplo siguiente se muestran llamadas que superan el número máximo de llamadas simultáneas que se reenviarán al número de teléfono 202-555-1234.</span><span class="sxs-lookup"><span data-stu-id="c277d-133">The following example sets calls that exceed the maximum number of concurrent calls to be forwarded to the telephone number 202-555-1234.</span></span> <span data-ttu-id="c277d-134">El objetivo puede ser un usuario de su organización en lugar de un número de teléfono; en ese caso, la sintaxis de la persona que recibe las llamadas desviadas es la misma que cuando se especifica un delegado: `sip:<NameofDelegate@domain>` .</span><span class="sxs-lookup"><span data-stu-id="c277d-134">The target could be a user in your organization instead of a phone number; in that case, the syntax for the person to receive the forwarded calls is the same as when you specify a delegate: `sip:<NameofDelegate@domain>`.</span></span> <span data-ttu-id="c277d-135">El otro parámetro posible para `BusyOption` es `Voicemail` :</span><span class="sxs-lookup"><span data-stu-id="c277d-135">The other possible parameter for `BusyOption` is `Voicemail`:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity SLAGroup1 -BusyOption Forward
              -Target tel:+2025551234]
    ```
</div>

<div>

## <a name="configure-the-sla-group-missed-call-option"></a><span data-ttu-id="c277d-136">Configurar la opción de llamada perdida del grupo de SLA</span><span class="sxs-lookup"><span data-stu-id="c277d-136">Configure the SLA group Missed Call Option</span></span>

1.  <span data-ttu-id="c277d-137">Configure la opción de llamada perdida del grupo de SLA con el cmdlet [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration):</span><span class="sxs-lookup"><span data-stu-id="c277d-137">Configure the SLA group Missed Call Option by using the [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity <IdentityOfGroup> 
              -MissedCallOption <Option> -MissedCallForwardTarget
              <TargetUserOrPhoneNumber> -BusyOption <Option> -MaxNumberofCalls <#> -Target [Target]
    ```
    <span data-ttu-id="c277d-138">En el ejemplo siguiente se especifica que las llamadas perdidas se desviarán al usuario con nombre `sla_forward_number` .</span><span class="sxs-lookup"><span data-stu-id="c277d-138">The following example specifies that missed calls are to be forwarded to the user named `sla_forward_number`.</span></span> <span data-ttu-id="c277d-139">Las opciones válidas para el `-MissedCallOption` parámetro son `Forward` , `BusySignal` o `Disconnect` .</span><span class="sxs-lookup"><span data-stu-id="c277d-139">The valid options for the `-MissedCallOption` parameter are `Forward`, `BusySignal`, or `Disconnect`.</span></span> <span data-ttu-id="c277d-140">Si lo desea `Forward` , también debe incluir el `-MissedCallForwardTarget` parámetro, con un número de teléfono o usuario como destino:</span><span class="sxs-lookup"><span data-stu-id="c277d-140">If you choose `Forward`, you must also include the `-MissedCallForwardTarget` parameter, with a user or phone number as the target:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity SLAGroup1 -MissedCallOption
              Forward -MissedCallForwardTarget sip:sla_forward_number@contoso.com 
        -BusyOption Forward -MaxNumberOfCalls 2 -Target sip:sla_forward_number@contoso.com 
    ```
</div>

<div>

## <a name="remove-a-delegate-from-a-group"></a><span data-ttu-id="c277d-141">Quitar un delegado de un grupo</span><span class="sxs-lookup"><span data-stu-id="c277d-141">Remove a delegate from a group</span></span>

1.  <span data-ttu-id="c277d-142">Para quitar un delegado de un grupo, use el cmdlet [Remove-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/remove-cssladelegates):</span><span class="sxs-lookup"><span data-stu-id="c277d-142">Remove a delegate from a group by using the [Remove-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/remove-cssladelegates) cmdlet:</span></span>
    ```powershell
    Remove-CsSlaDelegates -Identity <IdentityOfGroup> -Delegate
              <NameOfDelegate@domain>
    ```
    <span data-ttu-id="c277d-143">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c277d-143">For example:</span></span>
    ```powershell
    Remove-CsSlaDelegates -Identity SLAGroup1 -Delegate
              sip:SLA_Delegate3@contoso.com
    ```
</div>

<div>

## <a name="delete-an-sla-group"></a><span data-ttu-id="c277d-144">Eliminar un grupo de SLA</span><span class="sxs-lookup"><span data-stu-id="c277d-144">Delete an SLA group</span></span>

1.  <span data-ttu-id="c277d-145">Eliminar un grupo de SLA mediante el cmdlet [Remove-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/remove-csslaconfiguration?view=skype-ps):</span><span class="sxs-lookup"><span data-stu-id="c277d-145">Delete an SLA group by using the [Remove-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/remove-csslaconfiguration?view=skype-ps) cmdlet:</span></span>
    
    ```powershell
    Remove-CsSlaConfiguration -Identity <IdentityOfGroup>
              
    ```
    
    <span data-ttu-id="c277d-146">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c277d-146">For example:</span></span>
    ```powershell
    Remove-CsSlaConfiguration -Identity SLAGroup1 
    ```
<span data-ttu-id="c277d-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c277d-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

