---
title: Planeación de la Federación de Lync Server y Office Communications Server
description: Planificación de la Federación de Lync Server y Office Communications Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Lync Server and Office Communications Server federation
ms:assetid: c9eaf06b-054f-41a4-ad0c-499400d6c4c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205335(v=OCS.15)
ms:contentKeyID: 48185640
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5d7385b8fde27446fb0648802544a8840a0f6276
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424544"
---
# <a name="planning-for-lync-server-2013-and-office-communications-server-federation"></a><span data-ttu-id="297b3-103">Planificación de la Federación de Lync Server 2013 y Office Communications Server</span><span class="sxs-lookup"><span data-stu-id="297b3-103">Planning for Lync Server 2013 and Office Communications Server federation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="297b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="297b3-104">

<span> </span></span></span>

<span data-ttu-id="297b3-105">_**Última modificación del tema:** 2013-02-13_</span><span class="sxs-lookup"><span data-stu-id="297b3-105">_**Topic Last Modified:** 2013-02-13_</span></span>

<span data-ttu-id="297b3-106">La Federación entre Microsoft Lync Server 2013, Lync Server 2010 y Office Communications Server admite comunicaciones de punto a punto y de varias personas.</span><span class="sxs-lookup"><span data-stu-id="297b3-106">Federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server supports peer-to-peer and multi-party communications.</span></span> <span data-ttu-id="297b3-107">Las conversaciones de punto a punto se pueden remitir a conversaciones de varios participantes, lo que permite las reuniones ad hoc.</span><span class="sxs-lookup"><span data-stu-id="297b3-107">Peer-to-peer conversations can be escalated to multi-party conversations, allowing for ad hoc meetings.</span></span> <span data-ttu-id="297b3-108">Las reuniones (conferencias web o conferencias de audio y vídeo) se pueden programar para incluir contactos dentro de su organización, así como contactos en socios con los que se federe.</span><span class="sxs-lookup"><span data-stu-id="297b3-108">Meetings – Web conferencing or audio/visual conferences – can be scheduled to include contacts inside your organization as well as contacts in partners that you federate with.</span></span>

<span data-ttu-id="297b3-109">La Federación apareció por primera vez en Microsoft Office Live Communications Server 2005 y admitía un tipo de Federación, la Federación directa.</span><span class="sxs-lookup"><span data-stu-id="297b3-109">Federation first appeared in Microsoft Office Live Communications Server 2005 and supported one kind of federation, Direct Federation.</span></span> <span data-ttu-id="297b3-110">La Federación directa requirió conocer el dominio del Protocolo de inicio de sesión (SIP) del socio de Federación y el nombre de dominio completo (FQDN) del servidor perimetral del socio.</span><span class="sxs-lookup"><span data-stu-id="297b3-110">Direct Federation required you to know the federation partner’s session initiation protocol (SIP) domain and the fully qualified domain name (FQDN) of the partner’s Edge Server.</span></span> <span data-ttu-id="297b3-111">Live Communications Server 2005 con SP1 introdujo tipos de Federación adicionales, todos los cuales requerían que el socio federado publique los registros SRV del sistema de nombres de dominio (DNS) para ubicar su servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="297b3-111">Live Communications Server 2005 with SP1 introduced additional federation types, all of which required domain name system (DNS) SRV records to be published by the federated partner to locate their Edge Server.</span></span> <span data-ttu-id="297b3-112">La terminología de esa versión era:</span><span class="sxs-lookup"><span data-stu-id="297b3-112">The terminology for that release was:</span></span>

  - <span data-ttu-id="297b3-113">*Abrir Federación mejorada*: aceptar cualquier nombre de dominio SIP y usar DNS SRV para ubicar el servidor perimetral asociado</span><span class="sxs-lookup"><span data-stu-id="297b3-113">*Open Enhanced Federation*: Accept any SIP domain name and use DNS SRV to locate the partner Edge Server</span></span>

  - <span data-ttu-id="297b3-114">*Federación mejorada*: configure el nombre de dominio SIP del socio como un asociado de Federación de su organización y use DNS SRV para buscar el servidor perimetral asociado</span><span class="sxs-lookup"><span data-stu-id="297b3-114">*Enhanced Federation*: Configure the partner’s SIP domain name as a federation partner for your organization and use DNS SRV to find the partner Edge Server</span></span>

  - <span data-ttu-id="297b3-115">*Federación directa*: configurar el nombre de dominio SIP del socio y el FQDN al servidor perimetral del socio</span><span class="sxs-lookup"><span data-stu-id="297b3-115">*Direct Federation*: Configure the partner’s SIP domain name and the FQDN to the partner’s Edge Server</span></span>

  - <span data-ttu-id="297b3-116">*Lista de permitidos del servidor*: aceptar cualquier dominio, usar DNS SRV para buscar el servidor perimetral de un proveedor de hospedaje o un proveedor de conectividad de mensajería instantánea pública (mi)</span><span class="sxs-lookup"><span data-stu-id="297b3-116">*Server Allow List*: Accept any domain, use DNS SRV to find the Edge Server of a hosting provider or a public instant messaging (IM) connectivity provider</span></span>

<span data-ttu-id="297b3-117">Microsoft Office Communications Server 2007 introdujo nombres actualizados para los tipos de Federación para definir mejor lo que hace realmente cada tipo de Federación:</span><span class="sxs-lookup"><span data-stu-id="297b3-117">Microsoft Office Communications Server 2007 introduced updated naming for federation types to better define what each federation type actually accomplished:</span></span>

  - <span data-ttu-id="297b3-118">Abrir la Federación mejorada se conocía como *dominio de socio descubierto*</span><span class="sxs-lookup"><span data-stu-id="297b3-118">Open Enhanced Federation became known as *Discovered Partner Domain*</span></span>

  - <span data-ttu-id="297b3-119">La Federación mejorada se conocía como *dominio asociado permitido*</span><span class="sxs-lookup"><span data-stu-id="297b3-119">Enhanced Federation became known as *Allowed Partner Domain*</span></span>

  - <span data-ttu-id="297b3-120">La Federación directa se conocía como *servidor asociado permitido*</span><span class="sxs-lookup"><span data-stu-id="297b3-120">Direct Federation became known as *Allowed Partner Server*</span></span>

  - <span data-ttu-id="297b3-121">La lista de permitidos del servidor se conocía como *proveedor de hospedaje* y *proveedor de mensajería instantánea pública*</span><span class="sxs-lookup"><span data-stu-id="297b3-121">Server Allow List became known as *Hosting Provider* and *Public IM Provider*</span></span>

<span data-ttu-id="297b3-122">Microsoft Lync Server 2010 introdujo una definición más estrecha de proveedor de hospedaje de acuerdo con Microsoft Lync Online 2010 y Microsoft Office 365, y también lo hizo según la misma lista permitida definida por el tipo de Federación de dominios de socio autorizado.</span><span class="sxs-lookup"><span data-stu-id="297b3-122">Microsoft Lync Server 2010 introduced a narrower definition of Hosting Provider in accordance with Microsoft Lync Online 2010 and Microsoft Office 365 and also made it subject to the same allowed list defined by the Allowed Partner Domain federation type.</span></span>

<span data-ttu-id="297b3-123">Habilitar la Federación entre Microsoft Lync Server 2013, Lync Server 2010 y Office Communications Server usa los servidores perimetrales y los proxy inversos para exigir las reglas y los dominios asociados permitidos que usted defina.</span><span class="sxs-lookup"><span data-stu-id="297b3-123">Enabling federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server uses the Edge Servers and reverse proxies to enforce the rules and allowed partner domains that you define.</span></span> <span data-ttu-id="297b3-124">Desde una perspectiva de planeación, la Federación con otro Lync Server, Office Communications Server requiere lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="297b3-124">From a planning perspective, federating with other Lync Server, Office Communications Server requires the following:</span></span>

  - <span data-ttu-id="297b3-125">Habilitar la Federación en el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="297b3-125">Enable federation in Topology Builder.</span></span> <span data-ttu-id="297b3-126">Para obtener más información, vea el tema sobre la implementación de la [Federación SIP, la Federación XMPP y la mensajería instantánea pública en Lync Server 2013](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="297b3-126">For details, see the Deployment topic [Configuring SIP federation, XMPP federation and public instant messaging in Lync Server 2013](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md).</span></span>

  - <span data-ttu-id="297b3-127">Determinar los requisitos para la detección de dominios federados:</span><span class="sxs-lookup"><span data-stu-id="297b3-127">Determine your requirements for federated domain discovery:</span></span>
    
      - <span></span>  
        <span data-ttu-id="297b3-128">Para la configuración manual de la Federación, debe tener el nombre de dominio completo (FQDN) del servidor perimetral y el nombre de dominio del asociado, o el nombre de dominio en línea, que se especifica en el panel de control de Lync Server, **Federación y acceso externo**, **dominios federados de SIP**.</span><span class="sxs-lookup"><span data-stu-id="297b3-128">For manual configuration of federation, you must have the fully qualified domain name (FQDN) of the partner’s Edge Server and domain name, or online domain name, which is entered in the Lync Server Control Panel, **Federation and External Access**, **SIP Federated Domains**.</span></span> <span data-ttu-id="297b3-129">Cree una directiva **nueva** o **edite** una existente para permitir o bloquear dominios por FQDN.</span><span class="sxs-lookup"><span data-stu-id="297b3-129">Create a **New** policy or **Edit** an existing policy to either allow or block domains by FQDN.</span></span>
        
        <div>
        

        > [!WARNING]
        > <span data-ttu-id="297b3-130">La configuración manual del servidor perimetral de un socio de Federación es propenso a fallar en el caso de que el socio cambie la dirección IP de su servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="297b3-130">Manual configuration of a federation partner’s Edge Server is prone to failure in the event that the partner changes the IP address of their Edge Server.</span></span>

        
        </div>
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="297b3-131">Para los <STRONG>nuevos dominios federados de SIP</STRONG>, debe proporcionar el <STRONG>nombre de dominio (o FQDN)</STRONG> para Microsoft Lync Online y microsoft 365 u Office 365.</span><span class="sxs-lookup"><span data-stu-id="297b3-131">For <STRONG>New SIP Federated Domains</STRONG>, you must provide the <STRONG>Domain name (or FQDN)</STRONG> for Microsoft Lync Online and Microsoft 365 or Office 365.</span></span> <span data-ttu-id="297b3-132">Para Microsoft Lync Server 2013, Lync Server 2010 y Office Communications Server, también debe proporcionar un <STRONG>servicio perimetral de acceso (FQDN)</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="297b3-132">For Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server you must also provide an <STRONG>Access Edge service (FQDN)</STRONG></span></span>

        
        </div>
    
      - <span></span>  
        <span data-ttu-id="297b3-133">Para la Federación de Partners detectada, donde los socios pueden descubrir su servidor perimetral, cree un registro SRV en su DNS externo- \_ sipfederationtls. \_ tcp.contoso.com, que apunta al puerto 5061 y al registro de host (A) de su servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="297b3-133">For discovered partner federation, where partners can discover your Edge Server, you create an SRV record in your external DNS - \_sipfederationtls.\_tcp.contoso.com – which points to the port 5061 and the host (A) record of your Edge Server</span></span>
        
        <div>
        

        > [!IMPORTANT]
        > <span data-ttu-id="297b3-134">Si admite clientes móviles de Microsoft Lync en Windows Phone o Apple iPhone, iPad u otros dispositivos Apple y está usando el servicio de notificaciones Push o el servicio de notificaciones push, debe planear _sipfederationtls. _ TCP.</span><span class="sxs-lookup"><span data-stu-id="297b3-134">If you are supporting Microsoft Lync Mobile clients on either Windows Phone or Apple iPhone, iPad, or other Apple devices and are using the Push Notification Service or Push Notification Service, you must plan for _sipfederationtls._tcp.</span></span> <span data-ttu-id="297b3-135">&lt;&gt;Registros SRV de dominio SIP para cada dominio SIP que tenga clientes móviles de Lync.</span><span class="sxs-lookup"><span data-stu-id="297b3-135">&lt;SIP domain&gt; SRV records for each SIP domain that you have Lync Mobile clients.</span></span> <span data-ttu-id="297b3-136">Android y Nokia Symbian Lync Mobile no usan la notificación de inserción y no están sujetos a este requisito.</span><span class="sxs-lookup"><span data-stu-id="297b3-136">Android and Nokia Symbian Lync Mobile do not use push notification and are not subject to this requirement.</span></span>

        
        </div>

  - <span data-ttu-id="297b3-137">Configurar directivas de acceso de usuarios externos para admitir dominios federados</span><span class="sxs-lookup"><span data-stu-id="297b3-137">Configure external user access policies to support federated domains</span></span>

  - <span data-ttu-id="297b3-138">Abra puertos de Firewall para el protocolo de inicio de sesión (SIP), las conferencias web y el audio/vídeo para alojar la Federación o los contactos que está habilitando.</span><span class="sxs-lookup"><span data-stu-id="297b3-138">Open firewall ports for session initiation protocol (SIP), web conferencing and audio/visual to accommodate the federation or contacts that you are enabling.</span></span> <span data-ttu-id="297b3-139">Para obtener más información, consulte: [determinar el firewall externo a/V y los requisitos de puerto para Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="297b3-139">For details, see: [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span></span>

<span data-ttu-id="297b3-140">La siguiente información le ayudará a definir el certificado, el puerto/protocolo y los requisitos de DNS para la Federación con Microsoft Lync Server 2013 y Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="297b3-140">The following information will aid you in defining the certificate, port/protocol and DNS requirements for federation with Microsoft Lync Server 2013 and Lync Server 2010.</span></span>

<span data-ttu-id="297b3-141">Generalmente es un proceso de reenvío directo si ha planeado o implementado los servidores perimetrales de Microsoft Lync Server 2013, por lo general, en el planeamiento de certificados, Firewall y requisitos de Puerto/protocolo.</span><span class="sxs-lookup"><span data-stu-id="297b3-141">Planning for certificates, firewall and port/protocol requirements and DNS requirements is generally a straight forward process if you have planned or deployed your Microsoft Lync Server 2013 Edge Servers.</span></span> <span data-ttu-id="297b3-142">Puesto que la Federación es una característica adicional que usa el servidor perimetral existente, los requisitos de planeación suelen cumplirse al planear e implementar el servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="297b3-142">Because federation is an additional feature that uses the existing Edge Server, the planning requirements are generally met by the Edge Server planning and deployment.</span></span> <span data-ttu-id="297b3-143">Debe usar las siguientes tablas para determinar que se cumplen sus requisitos y realizar cambios en el puerto, protocolo y DNS según corresponda.</span><span class="sxs-lookup"><span data-stu-id="297b3-143">You should use the following tables to determine that your requirements are met and make changes in port/protocol and DNS accordingly.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="297b3-144">Si tiene un grupo de servidores de tecnología perimetral y se está federando con socios de Lync Server 2013 o Lync Server 2010, puede usar equilibrio de carga DNS o equilibradores de carga de hardware en los lados frontales internos y externos de los servidores perimetrales.</span><span class="sxs-lookup"><span data-stu-id="297b3-144">If you have a pool of Edge Servers and are federating with Lync Server 2013 or Lync Server 2010 partners, then you can use either DNS load balancing or hardware load balancers on the internal and external facing sides of the Edge Servers.</span></span> <span data-ttu-id="297b3-145">Si va a federar con Office Communications Server 2007 o con Office Communications Server 2007 R2, el equilibrio de carga de hardware proporcionará compatibilidad con la conmutación por error en el caso de un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="297b3-145">If you are federating with Office Communications Server 2007 or Office Communications Server 2007 R2, hardware load balancing will provide failover support in the event of an Edge Server.</span></span> <span data-ttu-id="297b3-146">Office Communications Server 2007 y Office Communications Server 2007 R2 no tienen en cuenta el equilibrio de carga de DNS.</span><span class="sxs-lookup"><span data-stu-id="297b3-146">Office Communications Server 2007 and Office Communications Server 2007 R2 are not DNS load balancing aware.</span></span> <span data-ttu-id="297b3-147">Los servidores perimetrales asociados establecerán comunicación con el primer servidor perimetral de su grupo que responda.</span><span class="sxs-lookup"><span data-stu-id="297b3-147">The partner Edge Servers will establish communication with the first Edge Server in your pool that responds.</span></span> <span data-ttu-id="297b3-148">Si se produce un error en ese servidor perimetral, la comunicación no se realiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="297b3-148">If that Edge Server fails, communication does not automatically failover.</span></span>



</div>

<span data-ttu-id="297b3-149">Los requisitos de certificados se suelen cumplir a través de la planificación de certificados para el servidor perimetral elegido o el plan del servidor perimetral agrupado.</span><span class="sxs-lookup"><span data-stu-id="297b3-149">Certificate requirements are typically met through the planning of certificates for your chosen Edge Server or pooled Edge Server plan.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="297b3-150">En esta sección</span><span class="sxs-lookup"><span data-stu-id="297b3-150">In This Section</span></span>

  - [<span data-ttu-id="297b3-151">Resumen del certificado: SIP, Federación XMPP y mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="297b3-151">Certificate summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - [<span data-ttu-id="297b3-152">Resumen de puertos: SIP, Federación XMPP y mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="297b3-152">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-port-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - [<span data-ttu-id="297b3-153">Resumen DNS: SIP, Federación XMPP y mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="297b3-153">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-dns-summary-sip-xmpp-federation-and-public-instant-messaging.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="297b3-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="297b3-154">See Also</span></span>


[<span data-ttu-id="297b3-155">Configurar directivas para controlar el acceso de usuarios federados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="297b3-155">Configure policies to control federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-federated-user-access.md)  


[<span data-ttu-id="297b3-156">Escenarios para el acceso de usuarios externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="297b3-156">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="297b3-157">Determinar los requisitos de los puertos y el firewall de A/V externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="297b3-157">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
[<span data-ttu-id="297b3-158">Determinar los requisitos DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="297b3-158">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="297b3-159">Administrar la configuración perimetral de acceso para su organización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="297b3-159">Manage Access Edge Configuration for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-access-edge-configuration-for-your-organization.md)  
[<span data-ttu-id="297b3-160">Administrar dominios federados SIP para la organización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="297b3-160">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)  
[<span data-ttu-id="297b3-161">Administrar proveedores federados SIP para la organización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="297b3-161">Manage SIP federated providers for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-providers-for-your-organization.md)  
  

<span data-ttu-id="297b3-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="297b3-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

