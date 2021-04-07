---
title: 'Lync Server 2013: Planeación de implementaciones híbridas'
description: 'Lync Server 2013: Planeación de implementaciones híbridas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424551"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a><span data-ttu-id="e98a7-103">Planeación de implementaciones híbridas de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e98a7-103">Planning for Lync Server 2013 hybrid deployments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e98a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e98a7-104">

<span> </span></span></span>

<span data-ttu-id="e98a7-105">_**Tema Última modificación:** 2016-05-25_</span><span class="sxs-lookup"><span data-stu-id="e98a7-105">_**Topic Last Modified:** 2016-05-25_</span></span>

<span data-ttu-id="e98a7-106">Debe tener en cuenta los siguientes requisitos para los usuarios y su infraestructura de red al planear una implementación híbrida.</span><span class="sxs-lookup"><span data-stu-id="e98a7-106">You should consider the following requirements for users and your network infrastructure while planning for a hybrid deployment.</span></span>

<div>

## <a name="infrastructure-requirements"></a><span data-ttu-id="e98a7-107">Requisitos de infraestructura</span><span class="sxs-lookup"><span data-stu-id="e98a7-107">Infrastructure Requirements</span></span>

<span data-ttu-id="e98a7-108">Debe tener lo siguiente configurado en su entorno para implementar e implementar una implementación híbrida.</span><span class="sxs-lookup"><span data-stu-id="e98a7-108">You must have the following configured in your environment in order to implement and deploy a hybrid deployment.</span></span>

  - <span data-ttu-id="e98a7-109">Una organización de Microsoft 365 u Office 365 con Skype Empresarial Online habilitado.</span><span class="sxs-lookup"><span data-stu-id="e98a7-109">A Microsoft 365 or Office 365 organization with Skype for Business Online enabled.</span></span> <span data-ttu-id="e98a7-110">Tenga en cuenta que solo puede usar un único espacio empresarial para una configuración híbrida con su implementación local.</span><span class="sxs-lookup"><span data-stu-id="e98a7-110">Note that you can use only a single tenant for a hybrid configuration with your on-premises deployment.</span></span>

  - <span data-ttu-id="e98a7-111">Una única implementación local (infraestructura) de Skype Empresarial Server o Lync Server que se implementa en una topología compatible.</span><span class="sxs-lookup"><span data-stu-id="e98a7-111">A single on-premises deployment (infrastructure) of Skype for Business Server or Lync Server that is deployed in a supported topology.</span></span> <span data-ttu-id="e98a7-112">Consulte Requisitos de topología.</span><span class="sxs-lookup"><span data-stu-id="e98a7-112">See Topology Requirements.</span></span>
    
    <span data-ttu-id="e98a7-113">Para obtener información sobre cómo configurar la implementación de Lync Server 2013 o Lync Server 2010 para la implementación híbrida, vea Configurar implementaciones híbridas de [Lync Server 2013.](lync-server-2013-configuring-hybrid-deployments.md)</span><span class="sxs-lookup"><span data-stu-id="e98a7-113">For information about configuring your Lync Server 2013 or Lync Server 2010 deployment for hybrid, see [Configuring Lync Server 2013 hybrid deployments](lync-server-2013-configuring-hybrid-deployments.md).</span></span>

  - <span data-ttu-id="e98a7-114">Herramientas administrativas de Skype Empresarial Server 2015.</span><span class="sxs-lookup"><span data-stu-id="e98a7-114">Skype for Business Server 2015 administrative tools.</span></span> <span data-ttu-id="e98a7-115">Si usa Lync Server 2013 o Lync Server 2010, puede usar las herramientas administrativas de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e98a7-115">If you are using Lync Server 2013 or Lync Server 2010, you can use the Lync Server 2013 administrative tools.</span></span>

  - <span data-ttu-id="e98a7-116">Para admitir el inicio de sesión único con Microsoft 365 u Office 365 para que los usuarios puedan usar las mismas credenciales de inicio de sesión para iniciar sesión en Office de forma local, puede usar las características de sincronización de contraseña de Azure Active Directory (AAD) Connect.</span><span class="sxs-lookup"><span data-stu-id="e98a7-116">To support Single Sign-on with Microsoft 365 or Office 365 so that users can use the same login credentials for signing in to Office as they do on-premises, you can use the password sync features of Azure Active Directory (AAD) Connect.</span></span> <span data-ttu-id="e98a7-117">También puede usar los Servicios de federación de Active Directory (AD FS) para el inicio de sesión único con Microsoft 365 u Office 365.</span><span class="sxs-lookup"><span data-stu-id="e98a7-117">You can also use Active Directory Federation Services (AD FS) for single sign-on with Microsoft 365 or Office 365.</span></span>
    
    <span data-ttu-id="e98a7-118">Para obtener más información, vea Integrar las identidades locales [con Azure Active Directory.](https://go.microsoft.com/fwlink/p/?linkid=619754)</span><span class="sxs-lookup"><span data-stu-id="e98a7-118">For more information, see [Integrating your on-premises identities with Azure Active Directory](https://go.microsoft.com/fwlink/p/?linkid=619754).</span></span>

  - <span data-ttu-id="e98a7-119">Una solución de sincronización de directorio único para mantener sincronizados los objetos locales y en línea de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e98a7-119">A single directory synchronization solution to keep your on-premises and online Active Directory objects synchronized.</span></span> <span data-ttu-id="e98a7-120">Para obtener más información sobre la sincronización de directorios, vea [Herramientas de integración de directorios.](https://go.microsoft.com/fwlink/p/?linkid=530320)</span><span class="sxs-lookup"><span data-stu-id="e98a7-120">For details about Directory Synchronization, see [Directory Integration Tools](https://go.microsoft.com/fwlink/p/?linkid=530320).</span></span>

</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="e98a7-121">Soporte técnico de cliente de Lync</span><span class="sxs-lookup"><span data-stu-id="e98a7-121">Lync Client Support</span></span>

<span data-ttu-id="e98a7-122">Hay algunas diferencias en las características admitidas en los clientes de Lync, así como en las características disponibles en entornos locales y en línea.</span><span class="sxs-lookup"><span data-stu-id="e98a7-122">There are some differences in the features supported in Lync clients, as well as the features available in on-premises and online environments.</span></span> <span data-ttu-id="e98a7-123">Antes de decidir dónde desea hospedar usuarios de su organización, puede ver el soporte técnico del cliente para las distintas configuraciones de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e98a7-123">Before you decide where you want to home users in your organization, you can view the client support for the various configurations of Lync Server.</span></span> <span data-ttu-id="e98a7-124">Los siguientes clientes son compatibles con Skype Empresarial Online en una implementación híbrida de Lync:</span><span class="sxs-lookup"><span data-stu-id="e98a7-124">The following clients are supported with Skype for Business Online in a Lync hybrid deployment:</span></span>

  - <span data-ttu-id="e98a7-125">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="e98a7-125">Lync 2010</span></span>

  - <span data-ttu-id="e98a7-126">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="e98a7-126">Lync 2013</span></span>

  - <span data-ttu-id="e98a7-127">Aplicación de la Tienda Windows de Lync</span><span class="sxs-lookup"><span data-stu-id="e98a7-127">Lync Windows Store app</span></span>

  - <span data-ttu-id="e98a7-128">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="e98a7-128">Lync Web App</span></span>

  - <span data-ttu-id="e98a7-129">Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="e98a7-129">Lync Mobile</span></span>

  - <span data-ttu-id="e98a7-130">Lync para Mac 2011</span><span class="sxs-lookup"><span data-stu-id="e98a7-130">Lync for Mac 2011</span></span>

  - <span data-ttu-id="e98a7-131">Sistema Lync Room</span><span class="sxs-lookup"><span data-stu-id="e98a7-131">Lync Room System</span></span>

  - <span data-ttu-id="e98a7-132">Lync Basic 2013</span><span class="sxs-lookup"><span data-stu-id="e98a7-132">Lync Basic 2013</span></span>

<span data-ttu-id="e98a7-133">Para obtener más información sobre el soporte técnico del cliente, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e98a7-133">For details about client support, see the following topics:</span></span>

  - [<span data-ttu-id="e98a7-134">Clientes para Lync Online</span><span class="sxs-lookup"><span data-stu-id="e98a7-134">Clients for Lync Online</span></span>](https://go.microsoft.com/fwlink/?linkid=281902)

  - [<span data-ttu-id="e98a7-135">Tablas de comparación de clientes para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e98a7-135">Client comparison tables for Lync Server 2013</span></span>](lync-server-2013-desktop-client-comparison-tables.md)

  - [<span data-ttu-id="e98a7-136">Tablas de comparación de clientes móviles para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e98a7-136">Mobile client comparison tables for Lync Server 2013</span></span>](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a><span data-ttu-id="e98a7-137">Requisitos de topología</span><span class="sxs-lookup"><span data-stu-id="e98a7-137">Topology Requirements</span></span>

<span data-ttu-id="e98a7-138">Para configurar la implementación para la implementación híbrida con Skype Empresarial Online, debe tener una de las siguientes topologías compatibles:</span><span class="sxs-lookup"><span data-stu-id="e98a7-138">To configure your deployment for hybrid with Skype for Business Online, you need to have one of the following supported topologies:</span></span>

  - <span data-ttu-id="e98a7-139">Una implementación de Skype Empresarial Server 2015 con todos los servidores que ejecutan Skype Empresarial Server 2015.</span><span class="sxs-lookup"><span data-stu-id="e98a7-139">A Skype for Business Server 2015 deployment with all servers running Skype for Business Server 2015.</span></span>

  - <span data-ttu-id="e98a7-140">Una implementación de Lync Server 2013 con todos los servidores que ejecutan Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e98a7-140">A Lync Server 2013 deployment with all servers running Lync Server 2013.</span></span>

  - <span data-ttu-id="e98a7-141">Una implementación de Lync Server 2010 con todos los servidores que ejecutan Lync Server 2010 con las actualizaciones acumulativas más recientes.</span><span class="sxs-lookup"><span data-stu-id="e98a7-141">A Lync Server 2010 deployment with all servers running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="e98a7-142">El servidor perimetral de federación y el servidor de salto siguiente del servidor perimetral de federación deben ejecutar Lync Server 2010 con las actualizaciones acumulativas más recientes.</span><span class="sxs-lookup"><span data-stu-id="e98a7-142">The federation Edge Server and next hop server from the federation Edge Server must be running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="e98a7-143">Las herramientas administrativas de Skype Empresarial Server 2015 o Lync Server 2013 deben estar instaladas en al menos un servidor o estación de trabajo de administración.</span><span class="sxs-lookup"><span data-stu-id="e98a7-143">The Skype for Business Server 2015 or Lync Server 2013 Administrative Tools must be installed on at least one server or management workstation.</span></span>

  - <span data-ttu-id="e98a7-144">Una implementación mixta de Lync Server 2013 y Skype Empresarial Server 2015 con los siguientes roles de servidor en al menos un sitio que ejecute Skype Empresarial Server 2015:</span><span class="sxs-lookup"><span data-stu-id="e98a7-144">A mixed Lync Server 2013 and Skype for Business Server 2015 deployment with the following server roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="e98a7-145">Al menos un grupo de servidores Enterprise o un servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="e98a7-145">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="e98a7-146">El grupo de directores asociado con la federación SIP, si existe</span><span class="sxs-lookup"><span data-stu-id="e98a7-146">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="e98a7-147">El grupo de servidores perimetrales asociado con la federación SIP</span><span class="sxs-lookup"><span data-stu-id="e98a7-147">The Edge Pool associated with SIP federation</span></span>

  - <span data-ttu-id="e98a7-148">Una implementación mixta de Lync Server 2010 y Skype Empresarial Server 2015 con los siguientes roles de servidores en al menos un sitio que ejecuta Skype Empresarial Server 2015:</span><span class="sxs-lookup"><span data-stu-id="e98a7-148">A mixed Lync Server 2010 and Skype for Business Server 2015 deployment with the following servers roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="e98a7-149">Al menos un grupo de servidores Enterprise o un servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="e98a7-149">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="e98a7-150">El grupo de directores asociado con la federación SIP, si existe</span><span class="sxs-lookup"><span data-stu-id="e98a7-150">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="e98a7-151">El grupo de servidores perimetrales asociado con la federación SIP para el sitio</span><span class="sxs-lookup"><span data-stu-id="e98a7-151">The Edge Pool associated with SIP federation for the Site</span></span>

  - <span data-ttu-id="e98a7-152">Una implementación mixta de Lync Server 2010 y Lync Server 2013 con los siguientes roles de servidor en al menos un sitio que ejecute Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="e98a7-152">A mixed Lync Server 2010 and Lync Server 2013 deployment with the following server roles in at least one site running Lync Server 2013:</span></span>
    
      - <span data-ttu-id="e98a7-153">Al menos un grupo de servidores Enterprise o un servidor Standard Edition en el sitio</span><span class="sxs-lookup"><span data-stu-id="e98a7-153">At least one Enterprise Pool or Standard Edition server in the site</span></span>
    
      - <span data-ttu-id="e98a7-154">El grupo de directores asociado con la federación SIP, si existe en el sitio</span><span class="sxs-lookup"><span data-stu-id="e98a7-154">The Director Pool associated with SIP federation, if it exists in the site</span></span>
    
      - <span data-ttu-id="e98a7-155">El grupo de servidores perimetrales asociado con la federación SIP para el sitio</span><span class="sxs-lookup"><span data-stu-id="e98a7-155">The Edge Pool associated with SIP federation for the site</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e98a7-156">Toda la administración de usuarios, incluidos los movimientos de usuario entre locales y UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, debe realizarse con la última versión instalada de las herramientas administrativas.</span><span class="sxs-lookup"><span data-stu-id="e98a7-156">All user management, including user moves between on-premises and UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, needs to be done using the latest installed version of the administrative tools.</span></span> <span data-ttu-id="e98a7-157">Las herramientas administrativas deben instalarse en un servidor independiente que tenga acceso a la implementación local existente y a Internet.</span><span class="sxs-lookup"><span data-stu-id="e98a7-157">The administrative tools must be installed on a separate server that has connect access to the existing on-premises deployment and to the Internet.</span></span> <span data-ttu-id="e98a7-158">El cmdlet <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> para mover usuarios de su implementación local a UNRESOLVED_TOKEN_VAL(skype16_online) debe ejecutarse desde las herramientas administrativas conectadas a su implementación local.</span><span class="sxs-lookup"><span data-stu-id="e98a7-158">The <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> cmdlet to move users from your on-premises deployment to UNRESOLVED_TOKEN_VAL(skype16_online) must be run from the administrative tools connected to your on-premises deployment.</span></span>



</div>

<span data-ttu-id="e98a7-159">Para obtener más información sobre las topologías compatibles, vea Topologías admitidas en [Lync Server 2013](lync-server-2013-supported-topologies.md)y Topologías de referencia de [Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=398709)para implementaciones híbridas empresariales.</span><span class="sxs-lookup"><span data-stu-id="e98a7-159">For more information about supported topologies, see [Supported topologies in Lync Server 2013](lync-server-2013-supported-topologies.md), and [Lync Server 2013 Reference Topologies for Enterprise Hybrid Deployments](https://go.microsoft.com/fwlink/p/?linkid=398709).</span></span>

<span data-ttu-id="e98a7-160">Para solucionar problemas de información sobre implementaciones híbridas y conectar PowerShell a Lync Online, vea [Lync Online: Lync PowerShell y Solución de problemas híbridos.](https://go.microsoft.com/fwlink/p/?linkid=306718)</span><span class="sxs-lookup"><span data-stu-id="e98a7-160">For troubleshooting information about hybrid deployments and connecting PowerShell to Lync Online, see [Lync Online: Lync PowerShell and Hybrid Troubleshooting](https://go.microsoft.com/fwlink/p/?linkid=306718).</span></span>

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a><span data-ttu-id="e98a7-161">Requisitos para listas de federación permitidas o bloqueadas</span><span class="sxs-lookup"><span data-stu-id="e98a7-161">Requirements for Federation Allowed/Blocked Lists</span></span>

<span data-ttu-id="e98a7-p108">La lista de dominios permitidos incluye los dominios que tienen configurado un nombre de dominio completo (FQDN) del perímetro de asociado. En ocasiones, se conocen como *servidores de asociado permitidos* o *asociados directos de federación*. Familiarícese con la diferencia entre las federaciones abiertas y cerradas, conocidas respectivamente como *detección de asociado* o *lista de dominios de asociado permitidos* en las implementaciones locales.</span><span class="sxs-lookup"><span data-stu-id="e98a7-p108">The Allowed domains list includes domains that have a partner Edge fully qualified domain name (FQDN) configured. These are sometimes referred to as *allowed partner servers* or *direct federation partners*. You should be familiar with the difference between Open Federation and Closed Federation, referred to as *partner discovery* and *allowed partner domain list*, respectively, in on-premises deployments.</span></span>

<span data-ttu-id="e98a7-165">Los requisitos siguientes necesitan cumplirse para configurar correctamente una implementación híbrida:</span><span class="sxs-lookup"><span data-stu-id="e98a7-165">The following requirements must be met to successfully configure a hybrid deployment:</span></span>

  - <span data-ttu-id="e98a7-166">La coincidencia de dominios debe configurarse igual para su implementación local y su organización de Microsoft 365 u Office 365.</span><span class="sxs-lookup"><span data-stu-id="e98a7-166">Domain matching must be configured the same for your on-premises deployment and your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="e98a7-167">Si la detección de asociado está habilitada en la implementación local, configure una federación abierta para el inquilino en línea.</span><span class="sxs-lookup"><span data-stu-id="e98a7-167">If partner discovery is enabled on the on-premises deployment, then open federation must be configured for your online tenant.</span></span> <span data-ttu-id="e98a7-168">Si, por el contrario, la detección de asociado no está habilitada, configure una federación cerrada para el inquilino en línea.</span><span class="sxs-lookup"><span data-stu-id="e98a7-168">If partner discovery is not enabled, then closed federation must be configured for your online tenant.</span></span>

  - <span data-ttu-id="e98a7-169">La lista de dominios bloqueados de la implementación local necesita coincidir exactamente con la lista de dominios bloqueados del inquilino en línea.</span><span class="sxs-lookup"><span data-stu-id="e98a7-169">The Blocked domains list in the on-premises deployment must exactly match the Blocked domains list for your online tenant.</span></span>

  - <span data-ttu-id="e98a7-170">La lista de dominios permitidos de la implementación local necesita coincidir exactamente con la lista de dominios permitidos del inquilino en línea.</span><span class="sxs-lookup"><span data-stu-id="e98a7-170">The Allowed domains list in the on-premises deployment must exactly match the Allowed domains list for your online tenant.</span></span>

  - <span data-ttu-id="e98a7-171">La federación debe estar habilitada para las comunicaciones externas para el inquilino en línea, que se configura mediante el Panel de control de Lync Online.</span><span class="sxs-lookup"><span data-stu-id="e98a7-171">Federation must be enabled for the external communications for the online tenant, which is configured by using the Lync Online Control Panel.</span></span>

</div>

<div>

## <a name="dns-settings"></a><span data-ttu-id="e98a7-172">Configuración DNS</span><span class="sxs-lookup"><span data-stu-id="e98a7-172">DNS Settings</span></span>

<span data-ttu-id="e98a7-173">Al crear registros DNS para implementaciones híbridas, todos los registros DNS externos de Lync deben apuntar a la infraestructura local.</span><span class="sxs-lookup"><span data-stu-id="e98a7-173">When creating DNS records for hybrid deployments, all Lync external DNS records should point to the on-premises infrastructure.</span></span> <span data-ttu-id="e98a7-174">Para obtener más información sobre los registros DNS necesarios, consulte Requisitos del Sistema de nombres de dominio [(DNS) para Lync Server 2013.](lync-server-2013-domain-name-system-dns-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="e98a7-174">For details on required DNS records, please refer to [Domain Name System (DNS) requirements for Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md).</span></span>

<span data-ttu-id="e98a7-175">Además, debe asegurarse de que la resolución DNS que se describe en la siguiente tabla funciona en su implementación local:</span><span class="sxs-lookup"><span data-stu-id="e98a7-175">Additionally you need to ensure that the DNS resolution described in the following table works in your on-premises deployment:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e98a7-176">Registro DNS</span><span class="sxs-lookup"><span data-stu-id="e98a7-176">DNS record</span></span></p></td>
<td><p><span data-ttu-id="e98a7-177">Lo puede resolver</span><span class="sxs-lookup"><span data-stu-id="e98a7-177">Resolvable by</span></span></p></td>
<td><p><span data-ttu-id="e98a7-178">Requisito de DNS</span><span class="sxs-lookup"><span data-stu-id="e98a7-178">DNS requirement</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e98a7-179">Registro SRV dns para _sipfederationtls._tcp. &lt; sipdomain.com &gt; para todos los dominios SIP compatibles que se resuelven en IP externas de Access Edge</span><span class="sxs-lookup"><span data-stu-id="e98a7-179">DNS SRV record for _sipfederationtls._tcp.&lt;sipdomain.com&gt; for all supported SIP domains resolving to Access Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="e98a7-180">Servidores perimetrales</span><span class="sxs-lookup"><span data-stu-id="e98a7-180">Edge server(s)</span></span></p></td>
<td><p><span data-ttu-id="e98a7-p111">Habilite la comunicación federada en una configuración híbrida. El servidor perimetral tiene que saber hacia dónde redirigir el tráfico federado para el dominio SIP que se divide entre las formas local y en línea.</span><span class="sxs-lookup"><span data-stu-id="e98a7-p111">Enable federated communication in a hybrid configuration. The Edge Server needs to know where to route federated traffic for the SIP domain that is split between on premises and online.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e98a7-183">DNS A registros para FQDN del servicio de conferencia web perimetral, por ejemplo, webcon.contoso.com resolver en IP externas del perímetro de conferencia web</span><span class="sxs-lookup"><span data-stu-id="e98a7-183">DNS A record(s) for Edge Web Conferencing Service FQDN, e.g. webcon.contoso.com resolving to Web Conferencing Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="e98a7-184">Equipos de usuarios conectados a la red corporativa interna</span><span class="sxs-lookup"><span data-stu-id="e98a7-184">Internal corporate network connected users’ computers</span></span></p></td>
<td><p><span data-ttu-id="e98a7-185">Permitir a los usuarios en línea presentar o ver contenido en reuniones hospedadas locales.</span><span class="sxs-lookup"><span data-stu-id="e98a7-185">Enable online users to present or view content in on-premises hosted meetings.</span></span> <span data-ttu-id="e98a7-186">El contenido incluye archivos de PowerPoint, pizarras, sondeos y notas compartidas.</span><span class="sxs-lookup"><span data-stu-id="e98a7-186">Content includes PowerPoint files, whiteboards, polls, and shared notes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e98a7-187">Dependiendo de cómo esté configurado DNS en su organización, es posible que tenga que agregar estos registros a la zona DNS hospedada interna para los dominios SIP correspondientes para proporcionar una resolución dns interna a estos registros.</span><span class="sxs-lookup"><span data-stu-id="e98a7-187">Depending on how DNS is configured in your organization, you may need to add these records to the internal hosted DNS zone for the corresponding SIP domain(s) to provide internal DNS resolution to these records.</span></span>

</div>

<div>

## <a name="firewall-considerations"></a><span data-ttu-id="e98a7-188">Consideraciones del firewall</span><span class="sxs-lookup"><span data-stu-id="e98a7-188">Firewall Considerations</span></span>

<span data-ttu-id="e98a7-189">Los equipos de la red deben poder realizar búsquedas DNS de Internet estándar.</span><span class="sxs-lookup"><span data-stu-id="e98a7-189">Computers on your network must be able to perform standard Internet DNS lookups.</span></span> <span data-ttu-id="e98a7-190">Si estos equipos pueden llegar a sitios de Internet estándar, la red cumple este requisito.</span><span class="sxs-lookup"><span data-stu-id="e98a7-190">If these computers can reach standard Internet sites, your network meets this requirement.</span></span>

<span data-ttu-id="e98a7-191">Según la ubicación del centro de datos de Microsoft Online Services, también debe configurar los dispositivos de firewall de red para que acepten conexiones basadas en nombres de dominio comodín (por ejemplo, todo el tráfico de \* .outlook.com).</span><span class="sxs-lookup"><span data-stu-id="e98a7-191">Depending on the location of your Microsoft Online Services data center, you must also configure your network firewall devices to accept connections based on wildcard domain names (for example, all traffic from \*.outlook.com).</span></span> <span data-ttu-id="e98a7-192">Si los firewalls de su organización no admiten configuraciones de nombres comodín, tendrá que determinar manualmente los intervalos de direcciones IP que le gustaría permitir y los puertos especificados.</span><span class="sxs-lookup"><span data-stu-id="e98a7-192">If your organization’s firewalls do not support wildcard name configurations, you will have to manually determine the IP address ranges that you would like to allow and the specified ports.</span></span>

<span data-ttu-id="e98a7-193">Consulte el tema de ayuda Direcciones URL e [intervalos de direcciones IP de Office 365.](https://go.microsoft.com/fwlink/p/?linkid=252942)</span><span class="sxs-lookup"><span data-stu-id="e98a7-193">Refer to the Help topic [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=252942).</span></span>

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a><span data-ttu-id="e98a7-194">Requisitos de puerto y protocolo</span><span class="sxs-lookup"><span data-stu-id="e98a7-194">Port and Protocol Requirements</span></span>

<span data-ttu-id="e98a7-195">Además de los requisitos de puerto para la comunicación interna de Lync Server 2013, también debe configurar los siguientes puertos.</span><span class="sxs-lookup"><span data-stu-id="e98a7-195">In addition to the port requirements for internal Lync Server 2013 communication, you must also configure the following ports.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e98a7-196">Protocolo /Puerto</span><span class="sxs-lookup"><span data-stu-id="e98a7-196">Protocol / Port</span></span></th>
<th><span data-ttu-id="e98a7-197">Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e98a7-197">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e98a7-198">TCP 443</span><span class="sxs-lookup"><span data-stu-id="e98a7-198">TCP 443</span></span></p></td>
<td><p><span data-ttu-id="e98a7-199">Abrir entrada</span><span class="sxs-lookup"><span data-stu-id="e98a7-199">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="e98a7-200">Servicios de federación de Active Directory (rol de servidor de federación)</span><span class="sxs-lookup"><span data-stu-id="e98a7-200">Active Directory Federation Services (federation server role)</span></span></p>
<p><span data-ttu-id="e98a7-201">Para obtener más información, vea <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Descripción de los servicios de rol de AD FS</a>.</span><span class="sxs-lookup"><span data-stu-id="e98a7-201">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Understanding AD FS Role Services</a>.</span></span></p></li>
<li><p><span data-ttu-id="e98a7-202">Servicios de federación de Active Directory (rol de servidor proxy)</span><span class="sxs-lookup"><span data-stu-id="e98a7-202">Active Directory Federation Services (proxy server role)</span></span></p></li>
<li><p><span data-ttu-id="e98a7-203">Microsoft Online Services Portal</span><span class="sxs-lookup"><span data-stu-id="e98a7-203">Microsoft Online Services Portal</span></span></p></li>
<li><p><span data-ttu-id="e98a7-204">Portal de mi empresa</span><span class="sxs-lookup"><span data-stu-id="e98a7-204">My Company Portal</span></span></p></li>
<li><p><span data-ttu-id="e98a7-205">Outlook Web App</span><span class="sxs-lookup"><span data-stu-id="e98a7-205">Outlook Web App</span></span></p></li>
<li><p><span data-ttu-id="e98a7-206">Cliente de Lync (comunicación a Lync Online desde Lync Server local)</span><span class="sxs-lookup"><span data-stu-id="e98a7-206">Lync client (communication to Lync Online from on-premises Lync Server)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e98a7-207">TCP 80 y 443</span><span class="sxs-lookup"><span data-stu-id="e98a7-207">TCP 80 and 443</span></span></p></td>
<td><p><span data-ttu-id="e98a7-208">Abrir entrada</span><span class="sxs-lookup"><span data-stu-id="e98a7-208">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="e98a7-209">Microsoft Online Services - Herramienta de sincronización de directorios</span><span class="sxs-lookup"><span data-stu-id="e98a7-209">Microsoft Online Services Directory Synchronization Tool</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e98a7-210">TCP 5061</span><span class="sxs-lookup"><span data-stu-id="e98a7-210">TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="e98a7-211">Abrir entrada y salida en el servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="e98a7-211">Open inbound/outbound on the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e98a7-212">PSOM/TLS 443</span><span class="sxs-lookup"><span data-stu-id="e98a7-212">PSOM/TLS 443</span></span></p></td>
<td><p><span data-ttu-id="e98a7-213">Abrir entrantes y salientes para sesiones de uso compartido de datos</span><span class="sxs-lookup"><span data-stu-id="e98a7-213">Open inbound/outbound for data sharing sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e98a7-214">STUN/TCP 443</span><span class="sxs-lookup"><span data-stu-id="e98a7-214">STUN/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="e98a7-215">Abrir sesiones entrantes y salientes para audio, vídeo y uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e98a7-215">Open inbound/outbound for audio, video, application sharing sessions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e98a7-216">STUN/UDP 3478</span><span class="sxs-lookup"><span data-stu-id="e98a7-216">STUN/UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="e98a7-217">Abrir entradas y salidas para sesiones de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="e98a7-217">Open inbound/outbound for audio and video sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e98a7-218">RTP/TCP 50000-59999</span><span class="sxs-lookup"><span data-stu-id="e98a7-218">RTP/TCP 50000-59999</span></span></p></td>
<td><p><span data-ttu-id="e98a7-219">Abrir salida para sesiones de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="e98a7-219">Open outbound for audio and video sessions</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a><span data-ttu-id="e98a7-220">Cuentas de usuario y datos</span><span class="sxs-lookup"><span data-stu-id="e98a7-220">User Accounts and Data</span></span>

<span data-ttu-id="e98a7-221">En una implementación híbrida de Lync Server 2013, cualquier usuario que desee hospedar en Lync Online primero debe crearse en la implementación local, de modo que la cuenta de usuario se cree en Servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e98a7-221">In a Lync Server 2013 hybrid deployment, any user that you want to home in Lync Online must first be created in the on-premises deployment, so that the user account is created in Active Directory Domain Services.</span></span> <span data-ttu-id="e98a7-222">A continuación, puede mover el usuario a Skype Empresarial Online, que moverá la lista de contactos del usuario.</span><span class="sxs-lookup"><span data-stu-id="e98a7-222">You can then move the user to Skype for Business Online, which will move the user’s contact list.</span></span>

<span data-ttu-id="e98a7-223">Al sincronizar cuentas de usuario entre las implementaciones de Lync local y Lync Online con AD FS y Dirsync, debe sincronizar las cuentas de AD para todos los usuarios de Lync de su organización entre sus implementaciones de Lync locales y en línea, incluso si los usuarios no se mueven a Lync Online.</span><span class="sxs-lookup"><span data-stu-id="e98a7-223">When you synchronize user accounts between your Lync on-premises and Lync Online deployments with AD FS and Dirsync, you need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="e98a7-224">Si no sincroniza todos los usuarios, puede ser que la comunicación entre los usuarios locales y en línea de su organización no funcione como se podría esperar.</span><span class="sxs-lookup"><span data-stu-id="e98a7-224">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e98a7-225">Si el usuario se crea mediante el portal en línea para el Centro de administración de Microsoft 365, la cuenta de usuario no se sincronizará con Active Directory local y el usuario no existirá en el Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="e98a7-225">If the user is created by using the online portal for Microsoft 365 admin center, the user account will not be synchronized with on-premises Active Directory, and the user will not exist in the on-premises Active Directory.</span></span> <span data-ttu-id="e98a7-226">Si ya ha creado usuarios en Lync Online y desea configurar la implementación híbrida con un Lync Server local, consulte Mover usuarios de Lync Online a Lync local en <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Lync Server 2013.</A></span><span class="sxs-lookup"><span data-stu-id="e98a7-226">If you have already created users in Lync Online, and want to configure hybrid with an on-premises Lync Server, see <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="e98a7-227">También debe tener en cuenta los siguientes problemas relacionados con el usuario al planear una implementación híbrida.</span><span class="sxs-lookup"><span data-stu-id="e98a7-227">You should also consider the following user-related issues when planning for a hybrid deployment.</span></span>

  - <span data-ttu-id="e98a7-228">**Contactos de usuario**   El límite de contactos para los usuarios de Lync Online es 250.</span><span class="sxs-lookup"><span data-stu-id="e98a7-228">**User contacts**   The limit for contacts for Lync Online users is 250.</span></span> <span data-ttu-id="e98a7-229">Los contactos que supere ese número se quitarán de la lista de contactos del usuario cuando la cuenta se mueve a Lync Online.</span><span class="sxs-lookup"><span data-stu-id="e98a7-229">Any contacts beyond that number will be removed from the user’s contact list when the account is moved to Lync Online.</span></span>

  - <span data-ttu-id="e98a7-230">**Mensajería instantánea y presencia**   Las listas de contactos de usuario, grupos y listas de control de acceso (ACL) se migran con la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="e98a7-230">**Instant Messaging and Presence**   User contact lists, groups, and access control lists (ACLs) are migrated with the user account.</span></span>

  - <span data-ttu-id="e98a7-231">**Datos de conferencia, contenido de la reunión y reuniones programadas**   Este contenido no se migra con la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="e98a7-231">**Conferencing data, meeting content, and scheduled meetings**   This content is not migrated with the user account.</span></span> <span data-ttu-id="e98a7-232">Los usuarios deben reprogramar reuniones después de migrar sus cuentas a Lync Online.</span><span class="sxs-lookup"><span data-stu-id="e98a7-232">Users must reschedule meetings after their accounts are migrated to Lync Online.</span></span>

</div>

<div>

## <a name="user-policies-and-features"></a><span data-ttu-id="e98a7-233">Características y directivas de usuario</span><span class="sxs-lookup"><span data-stu-id="e98a7-233">User Policies and Features</span></span>

  - <span data-ttu-id="e98a7-234">En un entorno híbrido de Lync Server 2013, los usuarios pueden habilitarse para mensajería instantánea, voz y reuniones locales o en línea, pero no ambas simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="e98a7-234">In a Lync Server 2013 hybrid environment, users can be enabled for Instant Messaging, voice, and meetings either on-premises or online, but not both simultaneously.</span></span>

  - <span data-ttu-id="e98a7-235">**Cliente de Lync**    Es posible que algunos usuarios necesiten una nueva versión de cliente cuando se mueven a Lync Online.</span><span class="sxs-lookup"><span data-stu-id="e98a7-235">**Lync Client**    Some users may require a new client version when they are moved to Lync Online.</span></span> <span data-ttu-id="e98a7-236">Para Office Communications Server 2007 R2, los usuarios deben moverse a un grupo de servidores de Lync Server 2013 antes de la migración a Lync Online.</span><span class="sxs-lookup"><span data-stu-id="e98a7-236">For Office Communications Server 2007 R2, users must be moved to a Lync Server 2013 pool prior to migration to Lync Online.</span></span>
    
    <span data-ttu-id="e98a7-237">Para obtener más información sobre el soporte técnico del cliente, vea Clientes [para Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) y clientes de Lync compatibles y [configuraciones de puerto de red.](https://go.microsoft.com/fwlink/p/?linkid=281901)</span><span class="sxs-lookup"><span data-stu-id="e98a7-237">For more information about client support, see [Clients for Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) and [Supported Lync clients and network port configurations](https://go.microsoft.com/fwlink/p/?linkid=281901).</span></span>

  - <span data-ttu-id="e98a7-238">**Configuración y directivas locales (no usuario)**   Las directivas locales y en línea requieren una configuración independiente.</span><span class="sxs-lookup"><span data-stu-id="e98a7-238">**On-premises policies and configuration (non-user)**   Online and on-premises policies require separate configuration.</span></span> <span data-ttu-id="e98a7-239">No puede establecer directivas globales que se apliquen a ambos.</span><span class="sxs-lookup"><span data-stu-id="e98a7-239">You cannot set global policies that apply to both.</span></span>

<span data-ttu-id="e98a7-240"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e98a7-240"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
