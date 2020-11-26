---
title: 'Lync Server 2013: Get-CsService para la administración de libretas de direcciones'
description: 'Lync Server 2013: Get-CsService para la administración de libretas de direcciones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsService for Address Book management
ms:assetid: 373b717d-5efa-4c36-a899-a23a5bd922b4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429698(v=OCS.15)
ms:contentKeyID: 48183853
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e46173429988d87022c13fab33e3778279dd0e9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427988"
---
# <a name="get-csservice-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="d8bc2-103">Get-CsService para la administración de libretas de direcciones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8bc2-103">Get-CsService for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8bc2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8bc2-104">

<span> </span></span></span>

<span data-ttu-id="d8bc2-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="d8bc2-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="d8bc2-106">¿Quién puede ejecutar este cmdlet? de forma predeterminada, los miembros de los siguientes grupos tienen autorización para ejecutar el cmdlet Get-CsService de forma local: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="d8bc2-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsService cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="d8bc2-107">Para devolver una lista de todas las funciones de control de acceso basado en roles (RBAC) a las que se ha asignado este cmdlet (incluidos los roles RBAC que haya creado usted mismo), ejecute el siguiente comando desde el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="d8bc2-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsService"}

<span data-ttu-id="d8bc2-108">Get-CsService es útil para recuperar y mostrar la configuración actual de los servicios web definidos de su infraestructura.</span><span class="sxs-lookup"><span data-stu-id="d8bc2-108">Get-CsService is valuable to retrieve and display the current configuration of your infrastructure’s defined Web Services.</span></span> <span data-ttu-id="d8bc2-109">Al definir el nombre de dominio completo (FQDN) de la agrupación y el parámetro webserver, el cmdlet devuelve los servicios basados en web ofrecidos por su servidor, incluidos los URI de expansión de la lista de distribución y el controlador de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d8bc2-109">By defining the pool’s fully qualified domain name (FQDN) and the parameter WebServer, the cmdlet returns the web-based services offered by your server, including the Address Book handler and distribution list expansion URIs.</span></span>

<span data-ttu-id="d8bc2-110">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d8bc2-110">For example:</span></span>

    Get-CsService -PoolFqdn "fe01.contoso.net" -WebServer

<span data-ttu-id="d8bc2-111">Este cmdlet devuelve lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d8bc2-111">This cmdlet returns the following:</span></span>

<span data-ttu-id="d8bc2-112">Identidad: WebServer:pool01. contoso. net</span><span class="sxs-lookup"><span data-stu-id="d8bc2-112">Identity : WebServer:pool01.contoso.net</span></span>

<span data-ttu-id="d8bc2-113">Almacén de almacén::DC01. contoso. net</span><span class="sxs-lookup"><span data-stu-id="d8bc2-113">FileStore : FileStore:dc01.contoso.net</span></span>

<span data-ttu-id="d8bc2-114">UserServer: UserServer:pool01. contoso. net</span><span class="sxs-lookup"><span data-stu-id="d8bc2-114">UserServer : UserServer:pool01.contoso.net</span></span>

<span data-ttu-id="d8bc2-115">PrimaryHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="d8bc2-115">PrimaryHttpPort : 80</span></span>

<span data-ttu-id="d8bc2-116">PrimaryHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="d8bc2-116">PrimaryHttpsPort : 443</span></span>

<span data-ttu-id="d8bc2-117">ExternalHttpPort: 8080</span><span class="sxs-lookup"><span data-stu-id="d8bc2-117">ExternalHttpPort : 8080</span></span>

<span data-ttu-id="d8bc2-118">ExternalHttpsPort: 4443</span><span class="sxs-lookup"><span data-stu-id="d8bc2-118">ExternalHttpsPort : 4443</span></span>

<span data-ttu-id="d8bc2-119">PublishedPrimaryHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="d8bc2-119">PublishedPrimaryHttpPort : 80</span></span>

<span data-ttu-id="d8bc2-120">PublishedPrimaryHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="d8bc2-120">PublishedPrimaryHttpsPort : 443</span></span>

<span data-ttu-id="d8bc2-121">PublishedExternalHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="d8bc2-121">PublishedExternalHttpPort : 80</span></span>

<span data-ttu-id="d8bc2-122">PublishedExternalHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="d8bc2-122">PublishedExternalHttpsPort : 443</span></span>

<span data-ttu-id="d8bc2-123">ReachPrimaryPsomServerPort: 8060</span><span class="sxs-lookup"><span data-stu-id="d8bc2-123">ReachPrimaryPsomServerPort : 8060</span></span>

<span data-ttu-id="d8bc2-124">ReachExternalPsomServerPort: 8061</span><span class="sxs-lookup"><span data-stu-id="d8bc2-124">ReachExternalPsomServerPort : 8061</span></span>

<span data-ttu-id="d8bc2-125">AppSharingPortStart: 49152</span><span class="sxs-lookup"><span data-stu-id="d8bc2-125">AppSharingPortStart : 49152</span></span>

<span data-ttu-id="d8bc2-126">AppSharingPortCount: 16383</span><span class="sxs-lookup"><span data-stu-id="d8bc2-126">AppSharingPortCount : 16383</span></span>

<span data-ttu-id="d8bc2-127">LIServiceInternalUri : https://internalweb.contoso.net/locationinformation/liservice.svc</span><span class="sxs-lookup"><span data-stu-id="d8bc2-127">LIServiceInternalUri : https://internalweb.contoso.net/locationinformation/liservice.svc</span></span>

<span data-ttu-id="d8bc2-128">ABHandlerInternalUri : https://internalweb.contoso.net/abs/handler</span><span class="sxs-lookup"><span data-stu-id="d8bc2-128">ABHandlerInternalUri : https://internalweb.contoso.net/abs/handler</span></span>

<span data-ttu-id="d8bc2-129">ABHandlerExternalUri : https://csweb.contoso.com/abs/handler</span><span class="sxs-lookup"><span data-stu-id="d8bc2-129">ABHandlerExternalUri : https://csweb.contoso.com/abs/handler</span></span>

<span data-ttu-id="d8bc2-130">DLExpansionInternalUri : https://internalweb.contoso.net/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="d8bc2-130">DLExpansionInternalUri : https://internalweb.contoso.net/groupexpansion/service.svc</span></span>

<span data-ttu-id="d8bc2-131">DLExpansionExternalUri : https://csweb.contoso.com/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="d8bc2-131">DLExpansionExternalUri : https://csweb.contoso.com/groupexpansion/service.svc</span></span>

<span data-ttu-id="d8bc2-132">CAHandlerInternalUri : https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="d8bc2-132">CAHandlerInternalUri : https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="d8bc2-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="d8bc2-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="d8bc2-134">CollabContentInternalUri : https://internalweb.contoso.net/CollabContent</span><span class="sxs-lookup"><span data-stu-id="d8bc2-134">CollabContentInternalUri : https://internalweb.contoso.net/CollabContent</span></span>

<span data-ttu-id="d8bc2-135">CollabContentExternalUri : https://csweb.contoso.com/CollabContent</span><span class="sxs-lookup"><span data-stu-id="d8bc2-135">CollabContentExternalUri : https://csweb.contoso.com/CollabContent</span></span>

<span data-ttu-id="d8bc2-136">CAHandlerExternalUri : https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="d8bc2-136">CAHandlerExternalUri : https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="d8bc2-137">DeviceUpdateDownloadInternalUri : https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="d8bc2-137">DeviceUpdateDownloadInternalUri : https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span></span>

<span data-ttu-id="d8bc2-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="d8bc2-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span></span>

<span data-ttu-id="d8bc2-139">DeviceUpdateStoreInternalUri : http://internalweb.contoso.net/RequestHandler/Files</span><span class="sxs-lookup"><span data-stu-id="d8bc2-139">DeviceUpdateStoreInternalUri : http://internalweb.contoso.net/RequestHandler/Files</span></span>

<span data-ttu-id="d8bc2-140">DeviceUpdateStoreExternalUri : https://csweb.contoso.com/RequestHandlerExt/Files</span><span class="sxs-lookup"><span data-stu-id="d8bc2-140">DeviceUpdateStoreExternalUri : https://csweb.contoso.com/RequestHandlerExt/Files</span></span>

<span data-ttu-id="d8bc2-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="d8bc2-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="d8bc2-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="d8bc2-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="d8bc2-143">MeetExternalUri : https://csweb.contoso.com/Meet</span><span class="sxs-lookup"><span data-stu-id="d8bc2-143">MeetExternalUri : https://csweb.contoso.com/Meet</span></span>

<span data-ttu-id="d8bc2-144">DialinExternalUri : https://csweb.contoso.com/Dialin</span><span class="sxs-lookup"><span data-stu-id="d8bc2-144">DialinExternalUri : https://csweb.contoso.com/Dialin</span></span>

<span data-ttu-id="d8bc2-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span><span class="sxs-lookup"><span data-stu-id="d8bc2-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span></span>

<span data-ttu-id="d8bc2-146">ReachExternalUri : https://csweb.contoso.com/Reach</span><span class="sxs-lookup"><span data-stu-id="d8bc2-146">ReachExternalUri : https://csweb.contoso.com/Reach</span></span>

<span data-ttu-id="d8bc2-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span><span class="sxs-lookup"><span data-stu-id="d8bc2-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span></span>

<span data-ttu-id="d8bc2-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="d8bc2-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="d8bc2-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="d8bc2-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="d8bc2-150">ExternalFqdn: csweb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d8bc2-150">ExternalFqdn : csweb.contoso.com</span></span>

<span data-ttu-id="d8bc2-151">InternalFqdn: internalweb.contoso.net</span><span class="sxs-lookup"><span data-stu-id="d8bc2-151">InternalFqdn : internalweb.contoso.net</span></span>

<span data-ttu-id="d8bc2-152">DependentServiceList: {registrar:pool01. contoso. net, ConferencingServer:pool01. contoso. net}</span><span class="sxs-lookup"><span data-stu-id="d8bc2-152">DependentServiceList : {Registrar:pool01.contoso.net, ConferencingServer:pool01.contoso.net}</span></span>

<span data-ttu-id="d8bc2-153">ServiceId: 1-webservices-1</span><span class="sxs-lookup"><span data-stu-id="d8bc2-153">ServiceId : 1-WebServices-1</span></span>

<span data-ttu-id="d8bc2-154">SiteId: sitio: Redmond</span><span class="sxs-lookup"><span data-stu-id="d8bc2-154">SiteId : Site:Redmond</span></span>

<span data-ttu-id="d8bc2-155">PoolFqdn: pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="d8bc2-155">PoolFqdn : pool01.contoso.net</span></span>

<span data-ttu-id="d8bc2-156">Versión: 5</span><span class="sxs-lookup"><span data-stu-id="d8bc2-156">Version : 5</span></span>

<span data-ttu-id="d8bc2-157">Rol: servidor WebServer</span><span class="sxs-lookup"><span data-stu-id="d8bc2-157">Role : WebServer</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="d8bc2-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8bc2-158">See Also</span></span>


[<span data-ttu-id="d8bc2-159">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="d8bc2-159">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
  

<span data-ttu-id="d8bc2-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8bc2-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

