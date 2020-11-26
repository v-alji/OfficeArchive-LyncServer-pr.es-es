---
title: Eliminar un conjunto existente de opciones de configuración de troncos SIP
description: Eliminar una colección existente de parámetros de configuración del tronco del SIP.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of SIP trunk configuration settings
ms:assetid: 3b25f14d-884b-42dd-a866-460d276d3e43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688024(v=OCS.15)
ms:contentKeyID: 49733614
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98acede458d34eb30202d898414b2e17076d32d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430521"
---
# <a name="delete-an-existing-collection-of-sip-trunk-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="fcaa5-103">Eliminar una colección existente de parámetros de configuración del tronco de SIP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fcaa5-103">Delete an existing collection of SIP trunk configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fcaa5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fcaa5-104">

<span> </span></span></span>

<span data-ttu-id="fcaa5-105">_**Última modificación del tema:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="fcaa5-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="fcaa5-106">Los ajustes de configuración del tronco del SIP definen la relación y las capacidades entre un servidor de mediación y la puerta de enlace de red de telefonía pública conmutada (RTC), una central de conmutación (PBX) IP o un controlador de borde de sesión (SBC) en el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="fcaa5-107">Estas opciones de configuración especifican:</span><span class="sxs-lookup"><span data-stu-id="fcaa5-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="fcaa5-108">Si se debe activar la omisión de medios en los troncos.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="fcaa5-109">Las condiciones en que se envían paquetes de protocolo de control de transporte (RTCP) en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="fcaa5-110">Si se requiere o no cifrado de protocolo en tiempo real seguro (SRTP) en cada tronco.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="fcaa5-111">Al instalar Microsoft Lync Server 2013, se crea una colección global de parámetros de configuración del tronco del SIP.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="fcaa5-112">Esta recopilación global de configuraciones no puede eliminarse.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-112">This global collection of settings cannot be deleted.</span></span> <span data-ttu-id="fcaa5-113">Sin embargo, puede usar el panel de control de Lync Server o el cmdlet [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) para "restablecer" las propiedades de la colección global a sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-113">However, you can use the Lync Server Control Panel or the [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) cmdlet to "reset" the properties in the global collection to their default values.</span></span> <span data-ttu-id="fcaa5-114">Por ejemplo, si ha definido el parámetro Enable3pccRefer en True, al restablecer la recopilación global el parámetro Enable3pccRefer volverá al valor predeterminado False.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-114">For example, if you have set the Enable3pccRefer property to True, when you reset the global collection the Enable3pccRefer property will revert to its default value of False.</span></span>

<span data-ttu-id="fcaa5-p103">Los Administradores también pueden crear configuraciones de tronco personalizadas en el ámbito del sitio o en el ámbito del servicio (para una puerta de enlace PSTN individual); estas configuraciones personalizadas pueden eliminarse. Al eliminar estas configuraciones personalizadas tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fcaa5-p103">Administrators can also create custom trunk configuration settings at the site scope or at the service scope (for an individual PSTN gateway); these custom settings can be removed. When removing these custom settings keep the following in mind:</span></span>

  - <span data-ttu-id="fcaa5-p104">Si elimina la configuración del ámbito del servicio, el tronco SIP administrado por esas configuraciones será administrado por las configuraciones aplicadas a su sitio, si existieran. Si no existen las configuraciones del sitio, esos troncos serán administrados por la recopilación global de configuraciones de tronco.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-p104">If you remove service scope settings, then the SIP trunk managed by those settings will be managed by the settings applied to their site, if they exist. If site settings do not exist, those trunks will then be managed by the global collection of trunk configuration settings.</span></span>

  - <span data-ttu-id="fcaa5-119">Si elimina las configuraciones del ámbito del sitio, cualquier tronco SIP administrado por esas configuraciones será entonces administrado por la recopilación global de configuraciones de tronco.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-119">If you remove site-scoped settings then any SIP trunks managed by those settings will now be managed by the global collection of trunk configuration settings.</span></span>

<div>

## <a name="to-remove-trunk-configuration-settings-with-lync-server-control-panel"></a><span data-ttu-id="fcaa5-120">Para quitar la configuración de troncal con el panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="fcaa5-120">To remove trunk configuration settings with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="fcaa5-121">En el panel de control de Lync Server, haga clic en **enrutamiento de voz** y luego en **configuración troncal**.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-121">In Lync Server Control Panel, click **Voice Routing** and then click **Trunk Configuration**.</span></span>

2.  <span data-ttu-id="fcaa5-p105">En la pestaña **Configuración de tronco**, seleccione la recopilación de configuraciones de tronco SIP que desea eliminar, haga clic en **Editar** y, a continuación, haga clic en **Eliminar**. Para eliminar varias recopilaciones en la misma operación, haga clic en la primera recopilación que desea eliminar, luego mantenga presionada la tecla Ctrl y haga clic en cualquier otra recopilación que desee eliminar.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-p105">On the **Trunk Configuration** tab, select the collection of SIP trunk configuration settings to be deleted, click **Edit** and then click **Delete**. To delete multiple collections in the same operation, click the first collection to be deleted, then hold down the Ctrl key and click any additional collections that you want to remove.</span></span>

3.  <span data-ttu-id="fcaa5-p106">La propiedad **Estado** para la recopilación se actualizará a **No confirmado**. Para confirmar los cambios y eliminar la recopilación, haga clic en **Confirmar** y luego en **Confirmar todo**.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-p106">The **State** property for the collection will be updated to **Uncommitted**. To commit the changes, and to delete the collection, click **Commit** and then click **Commit All**.</span></span>

4.  <span data-ttu-id="fcaa5-126">En el cuadro de diálogo **Valores de configuración de voz no confirmados**, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-126">In the **Uncommitted Voice Configuration Settings** dialog box, click **OK**.</span></span>

5.  <span data-ttu-id="fcaa5-127">En el cuadro de diálogo **Panel de control de Microsoft Lync Server 2013** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-127">In the **Microsoft Lync Server 2013 Control Panel** dialog box click **OK**.</span></span>

6.  <span data-ttu-id="fcaa5-128">If you change your mind and decide not to delete the collection, click **Commit** and then click **Cancel All Uncommitted Changes**.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-128">If you change your mind and decide not to delete the collection, click **Commit** and then click **Cancel All Uncommitted Changes**.</span></span> <span data-ttu-id="fcaa5-129">Cuando aparezca el cuadro de diálogo **Panel de control de Microsoft Lync Server 2013** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-129">When the **Microsoft Lync Server 2013 Control Panel** dialog box appears, click **OK**.</span></span>

</div>

<div>

## <a name="removing-trunk-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="fcaa5-130">Quitar las opciones de configuración de troncal mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fcaa5-130">Removing Trunk Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="fcaa5-131">Puede eliminar las opciones de configuración del tronco mediante Windows PowerShell y el cmdlet **Remove-CsTrunkConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="fcaa5-131">You can delete trunk configuration settings by using Windows PowerShell and the **Remove-CsTrunkConfiguration** cmdlet.</span></span> <span data-ttu-id="fcaa5-132">Puede ejecutar este cmdlet desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fcaa5-132">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="fcaa5-133">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="fcaa5-133">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-settings"></a><span data-ttu-id="fcaa5-134">Para quitar una recopilación concreta de opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="fcaa5-134">To remove a specified collection of settings</span></span>

  - <span data-ttu-id="fcaa5-135">El siguiente comando elimina las configuraciones de tronco aplicadas al sitio Redmond:</span><span class="sxs-lookup"><span data-stu-id="fcaa5-135">The following command removes the trunk configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsTrunkConfiguration -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-collections-applied-to-the-site-scope"></a><span data-ttu-id="fcaa5-136">Quitar todas las recopilaciones aplicadas al ámbito del sitio</span><span class="sxs-lookup"><span data-stu-id="fcaa5-136">To remove all the collections applied to the site scope</span></span>

  - <span data-ttu-id="fcaa5-137">Este comando elimina todas las configuraciones de tronco aplicadas al ámbito del servicio:</span><span class="sxs-lookup"><span data-stu-id="fcaa5-137">This command removes all the trunk configuration settings applied to the service scope:</span></span>
    
        Get-CsTrunkConfiguration -Filter "service:*" | Remove-CsTrunkConfiguration

</div>

<div>

## <a name="to-remove-all-the-collections-where-media-bypass-is-enabled"></a><span data-ttu-id="fcaa5-138">Quitar todas las recopilaciones en las que la omisión de medios está habilitada</span><span class="sxs-lookup"><span data-stu-id="fcaa5-138">To remove all the collections where media bypass is enabled</span></span>

  - <span data-ttu-id="fcaa5-139">El siguiente comando quita las configuraciones de tronco en las que la omisión de medios se ha habilitado:</span><span class="sxs-lookup"><span data-stu-id="fcaa5-139">The following command removes all the trunk configuration settings where media bypass has been enabled:</span></span>
    
        Get-CsTrunkConfiguration | Where-Object {$_.EnableBypass -eq $True} | Remove-CsTrunkConfiguration

</div>

<span data-ttu-id="fcaa5-140">Para obtener más información, consulte el tema de ayuda para el cmdlet [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="fcaa5-140">For more information, see the help topic for the [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="fcaa5-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fcaa5-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

