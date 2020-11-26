---
title: Configuración de la integración de Lync Server local con Exchange Online
description: Configurar la integración de Lync Server local con Exchange Online.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring on-premises Lync Server integration with Exchange Online
ms:assetid: 95a20117-2064-43c4-94fe-cac892cadb6f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh533880(v=OCS.15)
ms:contentKeyID: 48184900
ms.date: 03/30/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59c612bcdcdf4803bd6f9f2b38f1f9bb7dbad016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432838"
---
# <a name="configuring-on-premises-lync-server-2013-integration-with-exchange-online"></a><span data-ttu-id="d69f7-103">Configuración de la integración de Lync Server 2013 local con Exchange Online</span><span class="sxs-lookup"><span data-stu-id="d69f7-103">Configuring on-premises Lync Server 2013 integration with Exchange Online</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d69f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d69f7-104">

<span> </span></span></span>

<span data-ttu-id="d69f7-105">_**Última modificación del tema:** 2018-03-30_</span><span class="sxs-lookup"><span data-stu-id="d69f7-105">_**Topic Last Modified:** 2018-03-30_</span></span>

<span data-ttu-id="d69f7-106">Los clientes que usan las implementaciones locales de Lync Server 2013 pueden configurar la interoperabilidad con Microsoft Outlook Web App en Microsoft Exchange online en modo de implementación híbrida.</span><span class="sxs-lookup"><span data-stu-id="d69f7-106">Customers who are using on-premises Lync Server 2013 deployments can configure interoperability with Microsoft Outlook Web App in Microsoft Exchange Online in a hybrid deployment mode.</span></span> <span data-ttu-id="d69f7-107">Las características de interoperabilidad incluyen el inicio de sesión único y la integración de mensajería instantánea (MI) y presencia en la interfaz de Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="d69f7-107">Interoperability features include single sign on and instant messaging (IM) and presence integration with the Outlook Web App interface.</span></span> <span data-ttu-id="d69f7-108">Para habilitar esta integración, debe configurar el servidor perimetral en la implementación de Lync Server local completando las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="d69f7-108">To enable this integration, you must configure the Edge Server in your on-premises Lync Server deployment by completing the following tasks:</span></span>

  - <span data-ttu-id="d69f7-109">Configurar un espacio de direcciones SIP compartido</span><span class="sxs-lookup"><span data-stu-id="d69f7-109">Configure a shared SIP address space</span></span>

  - <span data-ttu-id="d69f7-110">Configurar un proveedor de hospedaje en el servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="d69f7-110">Configure a hosting provider on the Edge Server</span></span>

  - <span data-ttu-id="d69f7-111">Comprobar la replicación del almacén de administración central actualizado</span><span class="sxs-lookup"><span data-stu-id="d69f7-111">Verify replication of the updated Central Management store</span></span>

<span data-ttu-id="d69f7-112">Si Lync Server 2013 está integrado en Exchange Online, un usuario que está intentando iniciar sesión en mensajería instantánea desde OWA se considera un usuario remoto o externo.</span><span class="sxs-lookup"><span data-stu-id="d69f7-112">If Lync Server 2013 is integrated with Exchange Online, a user who is trying to sign in to IM from OWA is considered a remote or external user.</span></span> <span data-ttu-id="d69f7-113">En este escenario, este usuario debe tener una directiva de acceso externo asignada que tenga la siguiente opción seleccionada:</span><span class="sxs-lookup"><span data-stu-id="d69f7-113">In this scenario, this user must have an external access policy assigned that has the following option selected:</span></span>

<span data-ttu-id="d69f7-114">**Habilitar las comunicaciones con usuarios remotos**</span><span class="sxs-lookup"><span data-stu-id="d69f7-114">**Enable communications with remote users**</span></span>

<span data-ttu-id="d69f7-115">Habilite esta opción si quiere que los usuarios de su organización que estén fuera del firewall, como teletrabajadores y usuarios que viajan, puedan conectarse a Lync Server a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="d69f7-115">Enable this option if you want users in your organization who are outside your firewall, such as telecommuters and users who are traveling, to be able to connect to Lync Server over the Internet.</span></span>

<span data-ttu-id="d69f7-116">Para obtener más información, vea [administrar la Directiva de acceso externo en Lync Server 2013](lync-server-2013-manage-external-access-policy-for-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="d69f7-116">For more information, see [Manage external access policy in Lync Server 2013](lync-server-2013-manage-external-access-policy-for-your-organization.md).</span></span>

<div>

## <a name="configure-a-shared-sip-address-space"></a><span data-ttu-id="d69f7-117">Configurar un espacio de direcciones SIP compartido</span><span class="sxs-lookup"><span data-stu-id="d69f7-117">Configure a Shared SIP Address Space</span></span>

<span data-ttu-id="d69f7-118">Para integrar Lync Server local 2013 con Exchange Online, debe configurar un espacio de direcciones SIP compartido.</span><span class="sxs-lookup"><span data-stu-id="d69f7-118">To integrate on-premises Lync Server 2013 with Exchange Online, you must configure a shared SIP address space.</span></span> <span data-ttu-id="d69f7-119">El mismo espacio de direcciones de dominio SIP es compatible con Lync Server y el servicio Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d69f7-119">The same SIP domain address space is supported by both Lync Server and the Exchange Online service.</span></span>

<span data-ttu-id="d69f7-120">Con el shell de administración de Lync Server, configure el servidor perimetral para la Federación ejecutando el cmdlet **set-CSAccessEdgeConfiguration** , usando los parámetros que se muestran en el siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d69f7-120">Using the Lync Server Management Shell, configure the Edge Server for federation by running the **Set-CSAccessEdgeConfiguration** cmdlet, using the parameters that are displayed in the following example:</span></span>

    Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

  - <span data-ttu-id="d69f7-121">**AllowFederatedUsers** especifica si los usuarios internos pueden comunicarse con usuarios de dominios federados.</span><span class="sxs-lookup"><span data-stu-id="d69f7-121">**AllowFederatedUsers** specifies whether internal users are allowed to communicate with users from federated domains.</span></span> <span data-ttu-id="d69f7-122">Esta propiedad también determina si los usuarios internos pueden comunicarse con los usuarios en un escenario de espacio de direcciones SIP compartido con Lync Server y Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d69f7-122">This property also determines whether internal users can communicate with users in a shared SIP address space scenario with Lync Server and Exchange Online.</span></span>

<span data-ttu-id="d69f7-123">Para obtener más información sobre cómo usar el shell de administración de Lync Server, consulte [consola de administración de Lync server 2013](lync-server-2013-lync-server-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="d69f7-123">For details about how to use the Lync Server Management Shell, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

</div>

<div>

## <a name="configure-a-hosting-provider-on-the-edge-server"></a><span data-ttu-id="d69f7-124">Configurar un proveedor de hospedaje en el servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="d69f7-124">Configure a Hosting Provider on the Edge Server</span></span>

<span data-ttu-id="d69f7-125">Use el shell de administración de Lync Server para configurar un proveedor de hospedaje en el servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="d69f7-125">Use the Lync Server Management Shell to configure a hosting provider on the Edge Server.</span></span> <span data-ttu-id="d69f7-126">Para ello, ejecute el cmdlet **New-CsHostingProvider** con los parámetros del siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d69f7-126">To do this, run the **New-CsHostingProvider** cmdlet, using the parameters in the following example:</span></span>

    New-CsHostingProvider -Identity "Exchange Online" -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFqdn "exap.um.outlook.com" -IsLocal $False -VerificationLevel UseSourceVerification

<div>


> [!NOTE]
> <span data-ttu-id="d69f7-127">Si utiliza Office 365 operado por 21Vianet en China, reemplace el valor del parámetro <STRONG>ProxyFqdn</STRONG> de este ejemplo ("exap.um.outlook.com") por el FQDN del servicio operado por 21Vianet: "exap.um.partner.outlook.cn".</span><span class="sxs-lookup"><span data-stu-id="d69f7-127">If you are using Office 365 operated by 21Vianet in China, replace the value for the <STRONG>ProxyFqdn</STRONG> parameter in this example ("exap.um.outlook.com") with the FQDN for the service operated by 21Vianet: "exap.um.partner.outlook.cn".</span></span>



</div>

  - <span data-ttu-id="d69f7-128">**Identity** especifica un identificador de valor de cadena único para el proveedor de hospedaje que está creando (por ejemplo, "Exchange Online").</span><span class="sxs-lookup"><span data-stu-id="d69f7-128">**Identity** specifies a unique string value identifier for the hosting provider that you are creating (for example, "Exchange Online").</span></span> <span data-ttu-id="d69f7-129">Los valores que contienen espacios deben ir entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="d69f7-129">Values that contain spaces must be in double quotation marks.</span></span>

  - <span data-ttu-id="d69f7-130">**Habilitada** indica si la conexión de red entre el dominio y el proveedor de hospedaje está habilitada.</span><span class="sxs-lookup"><span data-stu-id="d69f7-130">**Enabled** indicates whether the network connection between your domain and the hosting provider is enabled.</span></span> <span data-ttu-id="d69f7-131">Debe establecerse en **true**.</span><span class="sxs-lookup"><span data-stu-id="d69f7-131">This must be set to **True**.</span></span>

  - <span data-ttu-id="d69f7-132">**EnabledSharedAddressSpace** indica si el proveedor de hospedaje se usará en un escenario de espacio de direcciones SIP compartido.</span><span class="sxs-lookup"><span data-stu-id="d69f7-132">**EnabledSharedAddressSpace** indicates whether the hosting provider will be used in a shared SIP address space scenario.</span></span> <span data-ttu-id="d69f7-133">Debe establecerse en **true**.</span><span class="sxs-lookup"><span data-stu-id="d69f7-133">This must be set to **True**.</span></span>

  - <span data-ttu-id="d69f7-134">**HostsOCSUsers** indica si el proveedor de hospedaje se usa para hospedar Office Communications Server o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d69f7-134">**HostsOCSUsers** indicates whether the hosting provider is used to host Office Communications Server or Lync Server.</span></span> <span data-ttu-id="d69f7-135">Debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="d69f7-135">This must be set to **False**.</span></span>

  - <span data-ttu-id="d69f7-136">**ProxyFQDN** especifica el nombre de dominio completo (FQDN) para el servidor proxy usado por el proveedor de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="d69f7-136">**ProxyFQDN** specifies the fully qualified domain name (FQDN) for the proxy server used by the hosting provider.</span></span> <span data-ttu-id="d69f7-137">Para Exchange Online, el FQDN es exap.um.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="d69f7-137">For Exchange Online, the FQDN is exap.um.outlook.com.</span></span>

  - <span data-ttu-id="d69f7-138">**IsLocal** indica si el servidor proxy usado por el proveedor de hospedaje está incluido en la topología de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d69f7-138">**IsLocal** indicates whether the proxy server used by the hosting provider is contained within your Lync Server topology.</span></span> <span data-ttu-id="d69f7-139">Debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="d69f7-139">This must be set to **False**.</span></span>

  - <span data-ttu-id="d69f7-140">**VerificationLevel** indica el nivel de comprobación permitido para los mensajes que se envían al proveedor hospedado y desde él.</span><span class="sxs-lookup"><span data-stu-id="d69f7-140">**VerificationLevel** indicates the verification level allowed for messages that are sent to and from the hosted provider.</span></span> <span data-ttu-id="d69f7-141">Especifique **UseSourceVerification**.</span><span class="sxs-lookup"><span data-stu-id="d69f7-141">Specify **UseSourceVerification**.</span></span> <span data-ttu-id="d69f7-142">Esta opción se basa en el nivel de comprobación que está incluido en los mensajes que se envían desde el proveedor de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="d69f7-142">This option relies on the verification level that is included in messages that are sent from the hosting provider.</span></span> <span data-ttu-id="d69f7-143">Si no se especifica este nivel, el mensaje se rechazará como no verificable.</span><span class="sxs-lookup"><span data-stu-id="d69f7-143">If this level is not specified, the message will be rejected as being unverifiable.</span></span>

</div>

<div>

## <a name="verify-replication-of-the-updated-central-management-store"></a><span data-ttu-id="d69f7-144">Comprobar la replicación del almacén de administración central actualizada</span><span class="sxs-lookup"><span data-stu-id="d69f7-144">Verify Replication of the Updated Central Management Store</span></span>

<span data-ttu-id="d69f7-145">Los cambios que realizó usando los cmdlets de las secciones anteriores se aplican automáticamente al servidor perimetral y generalmente tardan menos de un minuto en replicarse.</span><span class="sxs-lookup"><span data-stu-id="d69f7-145">The changes that you made by using the cmdlets in the preceding sections are automatically applied to the Edge Server, and generally take less than one minute to replicate.</span></span> <span data-ttu-id="d69f7-146">Puede comprobar el estado de replicación y que se aplicaron los cambios a su servidor perimetral mediante los cmdlets siguientes.</span><span class="sxs-lookup"><span data-stu-id="d69f7-146">You can verify the replication status and that the changes were applied to your Edge Server by using the following cmdlets.</span></span>

<span data-ttu-id="d69f7-147">Para comprobar las actualizaciones de replicación en un servidor interno de la implementación de Lync Server, ejecute el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d69f7-147">To verify replication updates on a server internal in your Lync Server deployment, run the following cmdlet:</span></span>

    Get-CsManagementStoreReplicationStatus

<span data-ttu-id="d69f7-148">Para comprobar que se han aplicado los cambios, ejecute el siguiente cmdlet en el servidor perimetral:</span><span class="sxs-lookup"><span data-stu-id="d69f7-148">To verify that the changes were applied, run the following cmdlet on the Edge Server:</span></span>

    Get-CsHostingProvider -LocalStore

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d69f7-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="d69f7-149">See Also</span></span>


[<span data-ttu-id="d69f7-150">Proporcionar correo de voz a usuarios de Lync Server 2013 en la mensajería unificada de Exchange hospedada</span><span class="sxs-lookup"><span data-stu-id="d69f7-150">Providing Lync Server 2013 users voice mail on hosted Exchange UM</span></span>](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md)  
[<span data-ttu-id="d69f7-151">Integración de la mensajería unificada de Exchange hospedada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d69f7-151">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-unified-messaging-integration.md)  
  

<span data-ttu-id="d69f7-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d69f7-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
