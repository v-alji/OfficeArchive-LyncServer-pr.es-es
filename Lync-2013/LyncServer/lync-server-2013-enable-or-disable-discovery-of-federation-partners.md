---
title: 'Lync Server 2013: Habilitar o deshabilitar la detección de socios de federación'
description: 'Lync Server 2013: habilitar o deshabilitar la detección de socios de Federación.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable discovery of federation partners
ms:assetid: 91fd036b-b1af-47cf-b1cf-0aa0a783c2aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182550(v=OCS.15)
ms:contentKeyID: 48184857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 36b91120ffc1ce2bd6cd8b8114f0330e6d39d996
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428905"
---
# <a name="enable-or-disable-discovery-of-federation-partners-in-lync-server-2013"></a><span data-ttu-id="fd7fa-103">Habilitar o deshabilitar la detección de socios de federación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd7fa-103">Enable or disable discovery of federation partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd7fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd7fa-104">

<span> </span></span></span>

<span data-ttu-id="fd7fa-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="fd7fa-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="fd7fa-106">En el momento de implementar los servidores perimetrales y de habilitar la Federación de su organización, debe haber especificado si se debe admitir la detección automática de dominios federados de socios.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-106">At the time you deployed your Edge Servers and enabled federation for your organization, you should have specified whether to support automatic discovery of federated partner domains.</span></span> <span data-ttu-id="fd7fa-107">Use el procedimiento de este tema para cambiar esa configuración.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-107">Use the procedure in this topic to change that configuration.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fd7fa-108">En el procedimiento siguiente se supone que ya ha habilitado la Federación de su organización.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-108">The following procedure assumes that you have already enabled federation for your organization.</span></span> <span data-ttu-id="fd7fa-109">Para obtener más información sobre cómo habilitar la Federación, vea <A href="lync-server-2013-enable-or-disable-remote-user-access.md">habilitar o deshabilitar el acceso de usuarios remotos en Lync Server 2013</A> en la documentación de implementación o en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-109">For details about enabling federation, see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A> in the Deployment documentation or the Operations documentation.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-automatic-discovery-of-federated-domains-for-your-organization"></a><span data-ttu-id="fd7fa-110">Para habilitar o deshabilitar la detección automática de dominios federados para su organización</span><span class="sxs-lookup"><span data-stu-id="fd7fa-110">To enable or disable automatic discovery of federated domains for your organization</span></span>

1.  <span data-ttu-id="fd7fa-111">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fd7fa-112">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="fd7fa-113">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="fd7fa-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="fd7fa-114">En la barra de navegación izquierda, haga clic en **acceso de usuarios externos**, haga clic en **configuración del borde de Access**.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-114">In the left navigation bar, click **External User Access**, click **Access Edge Configuration**.</span></span>

4.  <span data-ttu-id="fd7fa-115">En la página **configuración de perímetro de Access** , haga clic en **global**, haga clic en **Editar** y, a continuación, haga clic en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-115">On the **Access Edge Configuration** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="fd7fa-116">En **Editar configuración del límite de acceso**, en **habilitar las comunicaciones con usuarios federados**, Active o desactive la casilla **Habilitar la detección** de dominios asociados para habilitar o deshabilitar la detección automática de dominios asociados.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-116">In **Edit Access Edge Configuration**, under **Enable communications with federated users**, select or clear the **Enable partner domain discovery** check box to enable or disable automatic discovery of partner domains.</span></span>

6.  <span data-ttu-id="fd7fa-117">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-117">Click **Commit**.</span></span>

<span data-ttu-id="fd7fa-118">Para permitir que los usuarios federados colaboren con los usuarios de su implementación de Lync Server, también debe haber configurado al menos una directiva de acceso externa para admitir el acceso de usuarios federados.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-118">To enable federated users to collaborate with users in your Lync Server deployment, you must have also configured at least one external access policy to support federated user access.</span></span> <span data-ttu-id="fd7fa-119">Para obtener más información, vea [habilitar o deshabilitar la Federación y la conectividad de mensajería instantánea pública en Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) en la documentación de implementación o en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-119">For details, see [Enable or disable federation and public IM connectivity in Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) in the Deployment documentation or the Operations documentation.</span></span> <span data-ttu-id="fd7fa-120">Para más información sobre cómo controlar el acceso a dominios federados específicos, consulte [administrar dominios federados SIP para su organización en Lync server 2013](lync-server-2013-manage-sip-federated-domains-for-your-organization.md), [administrar proveedores federados SIP para su organización en Lync Server 2013](lync-server-2013-manage-sip-federated-providers-for-your-organization.md) y [administrar XMPP federados socios en Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md) en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-120">For details about controlling access for specific federated domains, see [Manage SIP federated domains for your organization in Lync Server 2013](lync-server-2013-manage-sip-federated-domains-for-your-organization.md), [Manage SIP federated providers for your organization in Lync Server 2013](lync-server-2013-manage-sip-federated-providers-for-your-organization.md) and [Manage XMPP federated partners in Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md) in the Operations documentation.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-discovery-of-federation-partners-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="fd7fa-121">Habilitar o deshabilitar la detección de socios de Federación mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fd7fa-121">Enabling or Disabling Discovery of Federation Partners by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="fd7fa-122">El descubrimiento de los socios de Federación se puede administrar mediante Windows PowerShell y el cmdlet Set-CsAccessEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-122">Discovery of federation partners can be managed by using Windows PowerShell and the Set-CsAccessEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="fd7fa-123">Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-123">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="fd7fa-124">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="fd7fa-124">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-discovery-of-federation-partners"></a><span data-ttu-id="fd7fa-125">Para habilitar la detección de socios de Federación</span><span class="sxs-lookup"><span data-stu-id="fd7fa-125">To enable discovery of federation partners</span></span>

  - <span data-ttu-id="fd7fa-126">Para habilitar la detección de socios de Federación, establezca el valor de la propiedad **EnablePartnerDiscovery** en True ($true).</span><span class="sxs-lookup"><span data-stu-id="fd7fa-126">To enable discovery of federation partners, set the value of the **EnablePartnerDiscovery** property to True ($True).</span></span> <span data-ttu-id="fd7fa-127">Tenga en cuenta que debe habilitar el enrutamiento SRV de DNS para poder cambiar este valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-127">Note that you must enable DNS SRV routing in order to change this property value.</span></span>
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -EnablePartnerDiscovery $True

</div>

<div>

## <a name="to-disable-discovery-of-federation-partners"></a><span data-ttu-id="fd7fa-128">Para deshabilitar la detección de socios de Federación</span><span class="sxs-lookup"><span data-stu-id="fd7fa-128">To disable discovery of federation partners</span></span>

  - <span data-ttu-id="fd7fa-129">Para deshabilitar la detección de socios de Federación, establezca el valor de la propiedad **EnablePartnerDiscovery** en False ($false):</span><span class="sxs-lookup"><span data-stu-id="fd7fa-129">To disable discovery of federation partners, set the value of the **EnablePartnerDiscovery** property to False ($False):</span></span>
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -EnablePartnerDiscovery $False

<span data-ttu-id="fd7fa-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd7fa-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

