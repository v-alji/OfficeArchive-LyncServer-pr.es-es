---
title: 'Lync Server 2013: Requisitos técnicos para la movilidad'
description: 'Lync Server 2013: requisitos técnicos para la movilidad.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for mobility
ms:assetid: 831be681-4de0-4e42-b04f-8879ca4dcd23
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690030(v=OCS.15)
ms:contentKeyID: 48184679
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6fc9c262ec8253b83a5bda5a47087579f5adc7d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441347"
---
# <a name="technical-requirements-for-mobility-in-lync-server-2013"></a><span data-ttu-id="a41ae-103">Requisitos técnicos para la movilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a41ae-103">Technical requirements for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a41ae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a41ae-104">

<span> </span></span></span>

<span data-ttu-id="a41ae-105">_**Última modificación del tema:** 2014-07-24_</span><span class="sxs-lookup"><span data-stu-id="a41ae-105">_**Topic Last Modified:** 2014-07-24_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="a41ae-106">Los usuarios móviles pueden encontrarse con diversos escenarios de aplicaciones móviles que requieren una planificación especial.</span><span class="sxs-lookup"><span data-stu-id="a41ae-106">Mobile users encounter various mobile application scenarios that require special planning.</span></span> <span data-ttu-id="a41ae-107">Por ejemplo, es posible que alguien empiece a usar una aplicación móvil mientras está fuera de trabajo conectándose a través de la red 3G, luego cambie a la red Wi-Fi corporativa al llegar al trabajo y, a continuación, vuelva a 3G cuando abandone el edificio.</span><span class="sxs-lookup"><span data-stu-id="a41ae-107">For example, someone might start using a mobile application while away from work by connecting through the 3G network, then switch to the corporate Wi-Fi network when arriving at work, and then switch back to 3G when leaving the building.</span></span> <span data-ttu-id="a41ae-108">Debe planificar su entorno para que admita dichas transiciones de red y garantizar una experiencia de usuario coherente.</span><span class="sxs-lookup"><span data-stu-id="a41ae-108">You need to plan your environment to support such network transitions and guarantee a consistent user experience.</span></span> <span data-ttu-id="a41ae-109">En esta sección se describen los requisitos de infraestructura que debe tener para admitir las aplicaciones móviles y el descubrimiento automático de recursos de movilidad.</span><span class="sxs-lookup"><span data-stu-id="a41ae-109">This section describes the infrastructure requirements that you must have in order to support mobile applications and automatic discovery of mobility resources.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a41ae-110">Aunque las aplicaciones móviles también pueden conectarse a otros servicios de Lync Server 2013, el requisito de enviar todas las solicitudes Web de aplicaciones móviles al mismo nombre de dominio completo (FQDN) de la web externa solo se aplica al servicio de movilidad de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a41ae-110">Although mobile applications can also connect to other Lync Server 2013 services, the requirement to send all mobile application web requests to the same external web fully qualified domain name (FQDN) applies only to the Lync Server 2013 Mobility Service.</span></span> <span data-ttu-id="a41ae-111">Otros servicios de movilidad no requieren esta configuración.</span><span class="sxs-lookup"><span data-stu-id="a41ae-111">Other mobility services do not require this configuration.</span></span>



</div>

<span data-ttu-id="a41ae-112">El requisito de afinidad de cookies en los equilibradores de carga de hardware se reduce drásticamente y usted sustituye la afinidad del Protocolo de control de transmisión (TCP) si usa Lync Mobile entregado con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a41ae-112">The requirement for cookie affinity in hardware load balancers is dramatically reduced, and you substitute Transmission Control Protocol (TCP) affinity if you are using the Lync Mobile delivered with Lync Server 2013.</span></span> <span data-ttu-id="a41ae-113">La afinidad de cookies aún puede usarse, pero los servicios web ya no la necesitan.</span><span class="sxs-lookup"><span data-stu-id="a41ae-113">Cookie affinity can still be used, but the web services no longer require it.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a41ae-114">Todo el tráfico del servicio de movilidad pasa por el proxy inverso, independientemente de dónde se encuentra el punto de origen, ya sea interno o externo.</span><span class="sxs-lookup"><span data-stu-id="a41ae-114">All Mobility Service traffic goes through the reverse proxy, regardless of where the origination point is—internal or external.</span></span> <span data-ttu-id="a41ae-115">En el caso de un único proxy inverso o de una matriz de proxies inversos, o de un dispositivo que proporciona la función de proxy inverso, puede surgir un problema cuando el tráfico interno está desplazado a través de una interfaz e intenta inmediatamente la entrada en la misma interfaz.</span><span class="sxs-lookup"><span data-stu-id="a41ae-115">In the case of a single reverse proxy or a farm of reverse proxies, or a device that is providing the reverse proxy function, an issue can arise when the internal traffic is egressing through an interface and attempting to immediately ingress on the same interface.</span></span> <span data-ttu-id="a41ae-116">Esto suele conducir a una violación de la regla de seguridad conocida como imitación de paquetes TCP o suplantación.</span><span class="sxs-lookup"><span data-stu-id="a41ae-116">This often leads to a Security rule violation known as TCP packet spoofing or just spoofing.</span></span> <span data-ttu-id="a41ae-117">El <EM>anclaje de cabello</EM> (salida y los ingresos inmediatos de un paquete o de una serie de paquetes) debe permitirse para que la movilidad funcione.</span><span class="sxs-lookup"><span data-stu-id="a41ae-117"><EM>Hair pinning</EM> (the egress and immediate ingress of a packet or series of packets) must be allowed in order for mobility to function.</span></span> <span data-ttu-id="a41ae-118">Una forma de resolver este problema es usar un proxy inverso que sea independiente del firewall (la regla de prevención de suplantaciones debe aplicarse siempre en el firewall, por razones de seguridad).</span><span class="sxs-lookup"><span data-stu-id="a41ae-118">One way to resolve this issue is to use a reverse proxy that is separate from the firewall (the spoofing prevention rule should always be enforced at the firewall, for security purposes).</span></span> <span data-ttu-id="a41ae-119">El Hairpin puede producirse en la interfaz externa del proxy inverso, en lugar de en la interfaz externa del firewall.</span><span class="sxs-lookup"><span data-stu-id="a41ae-119">The hairpin can occur at the external interface of the reverse proxy instead of the firewall external interface.</span></span> <span data-ttu-id="a41ae-120">Usted detecta la suplantación de identidad en el firewall y relaja la regla en el proxy inverso, lo que permite el Hairpin que requiere la movilidad.</span><span class="sxs-lookup"><span data-stu-id="a41ae-120">You detect the spoofing at the firewall, and relax the rule at the reverse proxy, thereby allowing the hairpin that mobility requires.</span></span><BR><span data-ttu-id="a41ae-121">Use el host del sistema de nombres de dominio (DNS) o los registros CNAME para definir el proxy inverso para el comportamiento Hairpin (no el firewall), si es posible.</span><span class="sxs-lookup"><span data-stu-id="a41ae-121">Use the Domain Name System (DNS) host or CNAME records to define the reverse proxy for the hairpin behavior (not the firewall), if at all possible.</span></span>



</div>

<span data-ttu-id="a41ae-122">Lync Server 2013 es compatible con los servicios de movilidad para Lync 2010 Mobile y los clientes móviles de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="a41ae-122">Lync Server 2013 supports mobility services for Lync 2010 Mobile and Lync 2013 mobile clients.</span></span> <span data-ttu-id="a41ae-123">Ambos clientes usan el servicio Detección automática de Lync Server 2013 para encontrar su punto de entrada de movilidad pero varían según el servicio de movilidad que usen.</span><span class="sxs-lookup"><span data-stu-id="a41ae-123">Both clients use the Lync Server 2013 Autodiscover Service to find its mobility entry point, but differ on which mobility service they use.</span></span> <span data-ttu-id="a41ae-124">Lync 2010 Mobile usa el servicio de movilidad conocido como *MCX*, presentado con la actualización acumulativa para Lync Server 2010:2011 de noviembre.</span><span class="sxs-lookup"><span data-stu-id="a41ae-124">Lync 2010 Mobile uses the Mobility Service known as *Mcx*, introduced with the Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="a41ae-125">Los clientes móviles de Lync 2013 usan la API Web de comunicaciones unificadas, o *UCWA*, como su proveedor de servicios de movilidad.</span><span class="sxs-lookup"><span data-stu-id="a41ae-125">Lync 2013 mobile clients use the Unified Communications Web API, or *UCWA*, as their mobility service provider.</span></span>

<div>

## <a name="internal-and-external-dns-configuration"></a><span data-ttu-id="a41ae-126">Configuración DNS interna y externa</span><span class="sxs-lookup"><span data-stu-id="a41ae-126">Internal and External DNS Configuration</span></span>

<span data-ttu-id="a41ae-127">Los servicios de movilidad de MCX (introducidos con la actualización acumulativa para Lync Server 2010: noviembre de 2011) y UCWA (introducidos en las actualizaciones acumulativas para Lync Server 2013: febrero de 2013) usan DNS de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="a41ae-127">The Mobility Services Mcx (introduced with the Cumulative Update for Lync Server 2010: November 2011) and UCWA (introduced in the Cumulative Updates for Lync Server 2013: February 2013) use DNS in the same way.</span></span>

<span data-ttu-id="a41ae-128">Cuando se usa el descubrimiento automático, los dispositivos móviles usan DNS para ubicar recursos.</span><span class="sxs-lookup"><span data-stu-id="a41ae-128">When you use Automatic Discovery, mobile devices use DNS to locate resources.</span></span> <span data-ttu-id="a41ae-129">Durante la búsqueda de DNS, se intenta primero una conexión con el FQDN asociado al registro DNS interno (lyncdiscoverinternal. \<internal domain name\> ).</span><span class="sxs-lookup"><span data-stu-id="a41ae-129">During the DNS lookup, a connection is first attempted to the FQDN that is associated with the internal DNS record (lyncdiscoverinternal.\<internal domain name\>).</span></span> <span data-ttu-id="a41ae-130">Si no se puede realizar una conexión mediante el registro DNS interno, se intenta una conexión mediante el registro DNS externo (lyncdiscover. \<sipdomain\> ).</span><span class="sxs-lookup"><span data-stu-id="a41ae-130">If a connection cannot be made by using the internal DNS record, a connection is attempted by using the external DNS record (lyncdiscover.\<sipdomain\>).</span></span> <span data-ttu-id="a41ae-131">Un dispositivo móvil que es interno a la red se conecta a la dirección URL del servicio de detección automática interna y un dispositivo móvil que es externo a la red se conecta a la dirección URL del servicio de detección automática externa.</span><span class="sxs-lookup"><span data-stu-id="a41ae-131">A mobile device that is internal to the network connects to the internal Autodiscover Service URL, and a mobile device that is external to the network connects to the external Autodiscover Service URL.</span></span> <span data-ttu-id="a41ae-132">Las solicitudes de detección automática externas atraviesan el proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="a41ae-132">External Autodiscover requests go through the reverse proxy.</span></span> <span data-ttu-id="a41ae-133">El servicio Detección automática de Lync Server 2013 devuelve todas las direcciones URL de servicios web para el grupo de servidores principales del usuario, incluidas las direcciones URL del servicio de movilidad (MCX y UCWA).</span><span class="sxs-lookup"><span data-stu-id="a41ae-133">The Lync Server 2013 Autodiscover Service returns all Web Services URLs for the user's home pool, including the Mobility Service (Mcx and UCWA) URLs.</span></span> <span data-ttu-id="a41ae-134">Sin embargo, la dirección URL del servicio de movilidad interna y la dirección URL del servicio de movilidad externa están asociados con el FQDN de los servicios web externos.</span><span class="sxs-lookup"><span data-stu-id="a41ae-134">However, both the internal Mobility Service URL and the external Mobility Service URL are associated with the external Web Services FQDN.</span></span> <span data-ttu-id="a41ae-135">Por tanto, independientemente de si un dispositivo móvil es interno o externo a la red, el dispositivo siempre se conecta al servicio de movilidad de Lync Server 2013 externamente a través del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="a41ae-135">Therefore, regardless of whether a mobile device is internal or external to the network, the device always connects to the Lync Server 2013 Mobility Service externally through the reverse proxy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a41ae-136">Es importante comprender que su implementación puede constar de varios espacios de nombres distintos para uso interno y externo.</span><span class="sxs-lookup"><span data-stu-id="a41ae-136">It is important to understand that your deployment can consist of multiple distinct namespaces for internal and external use.</span></span> <span data-ttu-id="a41ae-137">El nombre de dominio SIP puede ser diferente del nombre de dominio de la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="a41ae-137">Your SIP domain name may be different than the internal deployment domain name.</span></span> <span data-ttu-id="a41ae-138">Por ejemplo, el dominio SIP puede ser <STRONG>contoso.com</STRONG>, mientras que la implementación interna puede ser <STRONG>contoso.net</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a41ae-138">For example, your SIP domain may be <STRONG>contoso.com</STRONG>, while your internal deployment may be <STRONG>contoso.net</STRONG>.</span></span> <span data-ttu-id="a41ae-139">Los usuarios que inicien sesión en Lync Server usarán el nombre de dominio SIP, como <STRONG>John@contoso.com</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a41ae-139">Users who log in to Lync Server will use the SIP domain name, such as <STRONG>john@contoso.com</STRONG>.</span></span> <span data-ttu-id="a41ae-140">Al tratar los servicios web externos (definidos en el generador de topología como <STRONG>servicios web externos</STRONG>), el nombre de dominio y el nombre de dominio SIP serán coherentes, tal y como se define en DNS.</span><span class="sxs-lookup"><span data-stu-id="a41ae-140">When addressing the external web services (defined in Topology Builder as <STRONG>External web services</STRONG>), the domain name and the SIP domain name will be consistent, as defined in DNS.</span></span> <span data-ttu-id="a41ae-141">Al tratar los servicios Web internos (definidos en el generador de topología como <STRONG>servicios Web internos</STRONG>), el nombre predeterminado de los servicios Web internos será el FQDN del servidor front-end, del grupo de servidores front-end, del director o del grupo de directores.</span><span class="sxs-lookup"><span data-stu-id="a41ae-141">When addressing the internal Web services (defined in Topology Builder as <STRONG>Internal web services</STRONG>), the default name of the internal web services will be the FQDN of the Front End Server, Front End pool, Director, or Director pool.</span></span> <span data-ttu-id="a41ae-142">Tiene la opción de invalidar el nombre de los servicios Web internos.</span><span class="sxs-lookup"><span data-stu-id="a41ae-142">You have the option to override the internal web services name.</span></span> <span data-ttu-id="a41ae-143">Debe usar el nombre de dominio interno (y no el nombre de dominio SIP) para los servicios Web internos y definir el registro del host DNS A (o, para IPv6, AAAA) para reflejar el nombre reemplazado.</span><span class="sxs-lookup"><span data-stu-id="a41ae-143">You should use the internal domain name (and not the SIP domain name) for internal web services and define the DNS host A (or, for IPv6, AAAA) record to reflect the overridden name.</span></span> <span data-ttu-id="a41ae-144">Por ejemplo, el FQDN predeterminado de los servicios Web internos puede ser <STRONG>pool01.contoso.net</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a41ae-144">For example, the default internal web services FQDN may be <STRONG>pool01.contoso.net</STRONG>.</span></span> <span data-ttu-id="a41ae-145">Un FQDN de servicios Web internos invalidado puede ser <STRONG>webpool.contoso.net</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a41ae-145">An overridden internal web services FQDN may be <STRONG>webpool.contoso.net</STRONG>.</span></span> <span data-ttu-id="a41ae-146">La definición de los servicios Web de esta forma ayuda a garantizar que se respete la localidad interna y externa de los servicios, y no la localidad del usuario que los está usando.</span><span class="sxs-lookup"><span data-stu-id="a41ae-146">Defining the web services in this way helps to ensure that the internal and external locality of the services—and not the locality of the user who is using them—is observed.</span></span><BR><span data-ttu-id="a41ae-147">Sin embargo, dado que los servicios web se definen en el generador de topología y el nombre de los servicios Web internos puede reemplazarse, siempre que el nombre de los servicios Web resultante, el certificado que lo valide y los registros DNS que lo definen sean coherentes, puede definir los servicios Web internos con cualquier nombre de dominio, incluido el nombre de dominio de SIP, que desee.</span><span class="sxs-lookup"><span data-stu-id="a41ae-147">However, because the web services are defined in Topology Builder and the internal web services name can be overridden, as long as the resulting web services name, the certificate that validates it, and the DNS records that define it, are consistent, you can define the internal web services with any domain name—including the SIP domain name—that you want.</span></span> <span data-ttu-id="a41ae-148">En última instancia, la resolución del nombre de la dirección IP la determinan los registros de host DNS y un espacio de nombres coherente.</span><span class="sxs-lookup"><span data-stu-id="a41ae-148">Ultimately, the resolution for the name to the IP address is determined by DNS host records and a consistent namespace.</span></span><BR><span data-ttu-id="a41ae-149">Para los fines de este tema y los ejemplos, se usa el nombre de dominio interno para ilustrar la topología y las definiciones de DNS.</span><span class="sxs-lookup"><span data-stu-id="a41ae-149">For the purposes of this topic and the examples, the internal domain name is used to illustrate the topology and the DNS definitions.</span></span>



</div>

<span data-ttu-id="a41ae-150">En el siguiente diagrama se muestra el flujo de solicitudes Web de aplicaciones móviles para el servicio de movilidad y para el servicio de detección automática cuando se usa una configuración de DNS interna y externa.</span><span class="sxs-lookup"><span data-stu-id="a41ae-150">The following diagram illustrates the flow of mobile application web requests for the Mobility Service and for the Autodiscover Service when using an internal and external DNS configuration.</span></span>

<span data-ttu-id="a41ae-151">**Flujo de servicio de movilidad con detección automática**</span><span class="sxs-lookup"><span data-stu-id="a41ae-151">**Mobility service flow using AutoDiscover**</span></span>

<span data-ttu-id="a41ae-152">![cdb96424-96f2-4abf-88d7-1d32d1010ffd](images/Hh690030.cdb96424-96f2-4abf-88d7-1d32d1010ffd(OCS.15).jpg "cdb96424-96f2-4abf-88d7-1d32d1010ffd")</span><span class="sxs-lookup"><span data-stu-id="a41ae-152">![cdb96424-96f2-4abf-88d7-1d32d1010ffd](images/Hh690030.cdb96424-96f2-4abf-88d7-1d32d1010ffd(OCS.15).jpg "cdb96424-96f2-4abf-88d7-1d32d1010ffd")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a41ae-153">El diagrama muestra los servicios web genéricos.</span><span class="sxs-lookup"><span data-stu-id="a41ae-153">The diagram illustrates generic web services.</span></span> <span data-ttu-id="a41ae-154">Un directorio virtual denominado Mobility describe los servicios de movilidad MCX o UCWA.</span><span class="sxs-lookup"><span data-stu-id="a41ae-154">A virtual directory named Mobility depicts the Mobility services Mcx and/or UCWA.</span></span> <span data-ttu-id="a41ae-155">Si no ha aplicado las actualizaciones acumulativas para Lync Server 2013:2013 de febrero, puede que tenga o no el directorio virtual Ucwa definido en los servicios Web internos y externos.</span><span class="sxs-lookup"><span data-stu-id="a41ae-155">If you have not applied the Cumulative Updates for Lync Server 2013: February 2013, you may or may not have the virtual directory Ucwa defined on your internal and external Web services.</span></span> <span data-ttu-id="a41ae-156">Tendrá una detección automática de directorio virtual y es posible que tenga un directorio virtual MCX.</span><span class="sxs-lookup"><span data-stu-id="a41ae-156">You will have a virtual directory Autodiscover, and you may have a virtual directory Mcx.</span></span><BR><span data-ttu-id="a41ae-157">La detección automática y el descubrimiento de servicios funcionan de la misma manera, independientemente de la tecnología de Mobility Services que haya implementado.</span><span class="sxs-lookup"><span data-stu-id="a41ae-157">Autodiscover and the discovery of services work the same way, regardless of the mobility services technology that you have deployed.</span></span>



</div>

<span data-ttu-id="a41ae-158">Para admitir usuarios móviles de dentro y fuera de la red corporativa, los FQDN de la web interna y externa deben cumplir algunos requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="a41ae-158">To support mobile users from both inside and outside the corporate network, your internal and external web FQDNs must meet some prerequisites.</span></span> <span data-ttu-id="a41ae-159">Además, es posible que tenga que cumplir con otros requisitos, dependiendo de las características que decida implementar:</span><span class="sxs-lookup"><span data-stu-id="a41ae-159">In addition, you may need to meet other requirements, depending on the features you choose to implement:</span></span>

  - <span data-ttu-id="a41ae-160">Nuevos registros DNS, CNAME o A (host, si IPv6, AAAA), para el descubrimiento automático.</span><span class="sxs-lookup"><span data-stu-id="a41ae-160">New DNS, CNAME or A (host, if IPv6, AAAA) records, for automatic discovery.</span></span>

  - <span data-ttu-id="a41ae-161">Nueva regla de firewall, si desea admitir notificaciones de inserción a través de la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="a41ae-161">New firewall rule, if you want to support push notifications through your Wi-Fi network.</span></span>

  - <span data-ttu-id="a41ae-162">Para el descubrimiento automático, los nombres alternativos del firmante en certificados de servidor interno y en los certificados de proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="a41ae-162">Subject alternative names on internal server certificates and reverse proxy certificates, for automatic discovery.</span></span>

  - <span data-ttu-id="a41ae-163">La configuración del equilibrador de carga de hardware de servidor front-end cambia la afinidad de origen.</span><span class="sxs-lookup"><span data-stu-id="a41ae-163">Front End Server hardware load balancer configuration changes source affinity.</span></span>

<span data-ttu-id="a41ae-164">Su topología debe cumplir con los siguientes requisitos para admitir el servicio de movilidad y el servicio Detección automática:</span><span class="sxs-lookup"><span data-stu-id="a41ae-164">Your topology must meet the following requirements to support the Mobility Service and the Autodiscover Service:</span></span>

  - <span data-ttu-id="a41ae-165">El FQDN de la web interna del grupo de servidores front-end debe ser distinto del FQDN de la web externa del grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="a41ae-165">The Front End pool internal web FQDN must be distinct from the Front End pool external web FQDN.</span></span>

  - <span data-ttu-id="a41ae-166">El FQDN de la web interna solo debe resolver y ser accesible desde dentro de la red corporativa.</span><span class="sxs-lookup"><span data-stu-id="a41ae-166">The internal web FQDN must only resolve to and be accessible from inside the corporate network.</span></span>

  - <span data-ttu-id="a41ae-167">El FQDN de la web externa solo debe resolver y ser accesible desde Internet.</span><span class="sxs-lookup"><span data-stu-id="a41ae-167">The external web FQDN must only resolve to and be accessible from the Internet.</span></span>

  - <span data-ttu-id="a41ae-168">Para un usuario que está dentro de la red corporativa, la dirección URL del servicio de movilidad debe dirigirse al FQDN de la web externa.</span><span class="sxs-lookup"><span data-stu-id="a41ae-168">For a user who is inside the corporate network, the Mobility Service URL must be addressed to the external web FQDN.</span></span> <span data-ttu-id="a41ae-169">Este requisito es para el servicio de movilidad y solo se aplica a esta dirección URL.</span><span class="sxs-lookup"><span data-stu-id="a41ae-169">This requirement is for the Mobility Service and applies only to this URL.</span></span>

  - <span data-ttu-id="a41ae-170">Para un usuario que está fuera de la red corporativa, la solicitud debe ir al FQDN de la web externa del grupo o del Director de front-end.</span><span class="sxs-lookup"><span data-stu-id="a41ae-170">For a user who is outside the corporate network, the request must go to the external web FQDN of the Front End pool or Director.</span></span>

<span data-ttu-id="a41ae-171">Si admite el descubrimiento automático, debe crear los siguientes registros DNS para cada dominio SIP:</span><span class="sxs-lookup"><span data-stu-id="a41ae-171">If you support automatic discovery, you need to create the following DNS records for each SIP domain:</span></span>

  - <span data-ttu-id="a41ae-172">Un registro DNS interno para admitir usuarios móviles que se conectan desde la red de su organización.</span><span class="sxs-lookup"><span data-stu-id="a41ae-172">An internal DNS record to support mobile users who connect from within your organization's network.</span></span>

  - <span data-ttu-id="a41ae-173">Registro DNS externo o público para admitir usuarios móviles que se conectan desde Internet.</span><span class="sxs-lookup"><span data-stu-id="a41ae-173">An external, or public, DNS record to support mobile users who connect from the Internet.</span></span>

<span data-ttu-id="a41ae-174">La URL de detección automática interna no tiene que ser direccionable desde fuera de su red.</span><span class="sxs-lookup"><span data-stu-id="a41ae-174">The internal automatic discovery URL should not be addressable from outside your network.</span></span> <span data-ttu-id="a41ae-175">La dirección URL de detección automática externa no tiene que ser direccionable desde dentro de su red.</span><span class="sxs-lookup"><span data-stu-id="a41ae-175">The external automatic discovery URL should not be addressable from within your network.</span></span> <span data-ttu-id="a41ae-176">Sin embargo, si no puede cumplir con este requisito para la dirección URL externa, es probable que el cliente móvil no se vea afectado, ya que la dirección URL interna siempre se prueba en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="a41ae-176">However, if you cannot meet this requirement for the external URL, mobile client functionally will probably not be affected, because the internal URL is always tried first.</span></span>

<span data-ttu-id="a41ae-177">Los registros DNS pueden ser registros CNAME o (host, si IPv6, AAAA).</span><span class="sxs-lookup"><span data-stu-id="a41ae-177">The DNS records can be either CNAME records or A (host, if IPv6, AAAA) records.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a41ae-178">Los clientes de dispositivos móviles no admiten varios certificados de capa de sockets seguros (SSL) de diferentes dominios.</span><span class="sxs-lookup"><span data-stu-id="a41ae-178">Mobile device clients do not support multiple Secure Sockets Layer (SSL) certificates from different domains.</span></span> <span data-ttu-id="a41ae-179">Por lo tanto, no se admite la redirección CNAME a dominios diferentes a través de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a41ae-179">Therefore, CNAME redirection to different domains is not supported over HTTPS.</span></span> <span data-ttu-id="a41ae-180">Por ejemplo, un registro CNAME de DNS para lyncdiscover.contoso.com que redirige a una dirección de director.contoso.net no es compatible con HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a41ae-180">For example, a DNS CNAME record for lyncdiscover.contoso.com that redirects to an address of director.contoso.net is not supported over HTTPS.</span></span> <span data-ttu-id="a41ae-181">En una topología de este tipo, un cliente de dispositivo móvil debe usar HTTP para la primera solicitud, de modo que la redirección CNAME se resuelva por HTTP.</span><span class="sxs-lookup"><span data-stu-id="a41ae-181">In such a topology, a mobile device client needs to use HTTP for the first request, so that the CNAME redirection is resolved over HTTP.</span></span> <span data-ttu-id="a41ae-182">Después, las solicitudes posteriores usan HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a41ae-182">Subsequent requests then use HTTPS.</span></span> <span data-ttu-id="a41ae-183">Para admitir este escenario, debe configurar el proxy inverso con una regla de publicación web para el puerto 80 (HTTP).</span><span class="sxs-lookup"><span data-stu-id="a41ae-183">To support this scenario, you need to configure your reverse proxy with a web publishing rule for port 80 (HTTP).</span></span> <span data-ttu-id="a41ae-184">Para obtener más información, consulte "para crear una regla de publicación web para el puerto 80" en <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">configurar el proxy inverso para la movilidad en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a41ae-184">For details, see "To create a web publishing rule for port 80" in <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuring the reverse proxy for mobility in Lync Server 2013</A>.</span></span><BR><span data-ttu-id="a41ae-185">El redireccionamiento CNAME para el mismo dominio es compatible con HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a41ae-185">CNAME redirection to the same domain is supported over HTTPS.</span></span> <span data-ttu-id="a41ae-186">En este caso, el certificado del dominio de destino cubre el dominio de origen.</span><span class="sxs-lookup"><span data-stu-id="a41ae-186">In this case, the destination domain's certificate covers the originating domain.</span></span>



</div>

<span data-ttu-id="a41ae-187">Para obtener más información sobre los registros DNS necesarios para su escenario, consulte [Resumen de DNS-detección automática en Lync Server 2013](lync-server-2013-dns-summary-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="a41ae-187">For details about the DNS records required for your scenario, see [DNS summary - Autodiscover in Lync Server 2013](lync-server-2013-dns-summary-autodiscover.md).</span></span>

</div>

<div>

## <a name="port-and-firewall-requirements"></a><span data-ttu-id="a41ae-188">Requisitos de puertos y firewalls</span><span class="sxs-lookup"><span data-stu-id="a41ae-188">Port and Firewall Requirements</span></span>

<span data-ttu-id="a41ae-189">Si admite notificaciones de inserción y desea que los dispositivos móviles de Apple reciban notificaciones push sobre su red Wi-Fi, también tendrá que abrir el puerto 5223 en la red Wi-Fi de la empresa.</span><span class="sxs-lookup"><span data-stu-id="a41ae-189">If you support push notifications and want Apple mobile devices to receive push notifications over your Wi-Fi network, you also need to open port 5223 on your enterprise Wi-Fi network.</span></span> <span data-ttu-id="a41ae-190">El puerto 5223 es un puerto TCP saliente usado por el servicio de notificaciones push de Apple (APN).</span><span class="sxs-lookup"><span data-stu-id="a41ae-190">Port 5223 is an outbound TCP port used by the Apple Push Notification Service (APNS).</span></span> <span data-ttu-id="a41ae-191">El dispositivo móvil inicia la conexión.</span><span class="sxs-lookup"><span data-stu-id="a41ae-191">The mobile device initiates the connection.</span></span> <span data-ttu-id="a41ae-192">Para obtener más información, consulte [http://support.apple.com/kb/TS1629](http://support.apple.com/kb/ts1629) .</span><span class="sxs-lookup"><span data-stu-id="a41ae-192">For details, see [http://support.apple.com/kb/TS1629](http://support.apple.com/kb/ts1629) .</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="a41ae-193">Un dispositivo Apple que use el cliente móvil de Lync 2013 no necesita notificaciones Push.</span><span class="sxs-lookup"><span data-stu-id="a41ae-193">An Apple device using the Lync 2013 Mobile client does not require push notifications.</span></span>



</div>

<span data-ttu-id="a41ae-194">Tenga en cuenta que si un usuario está alojado en un dispositivo de sucursal con la supervivencia (SBA), se necesitan los puertos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a41ae-194">Note that if a user is homed on a Survivable Branch Appliance (SBA) then the following ports are required:</span></span>

  - <span data-ttu-id="a41ae-195">UcwaSipExternalListeningPort necesita el puerto 5088</span><span class="sxs-lookup"><span data-stu-id="a41ae-195">UcwaSipExternalListeningPort requires port 5088</span></span>

  - <span data-ttu-id="a41ae-196">UcwaSipPrimaryListeningPort necesita el puerto 5089</span><span class="sxs-lookup"><span data-stu-id="a41ae-196">UcwaSipPrimaryListeningPort requires port 5089</span></span>

<span data-ttu-id="a41ae-197">Para obtener más información y orientación sobre los requisitos de puerto y protocolo para la detección automática, consulte [Resumen de puertos-detección automática en Lync Server 2013](lync-server-2013-port-summary-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="a41ae-197">For additional details and guidance on port and protocol requirements for Autodiscover, see [Port summary - Autodiscover in Lync Server 2013](lync-server-2013-port-summary-autodiscover.md).</span></span>

</div>

<div>

## <a name="certificate-requirements"></a><span data-ttu-id="a41ae-198">Requisitos de certificados</span><span class="sxs-lookup"><span data-stu-id="a41ae-198">Certificate Requirements</span></span>

<span data-ttu-id="a41ae-199">Si admite el descubrimiento automático para clientes móviles de Lync, debe modificar las listas de nombres alternativos de asunto de los certificados para admitir conexiones seguras desde los clientes móviles.</span><span class="sxs-lookup"><span data-stu-id="a41ae-199">If you support automatic discovery for Lync mobile clients, you need to modify the subject alternative name lists on certificates to support secure connections from the mobile clients.</span></span> <span data-ttu-id="a41ae-200">Debe solicitar y asignar certificados nuevos, agregando las entradas de nombre alternativo de asunto descritas en esta sección para cada servidor y director de front-end que ejecute el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="a41ae-200">You need to request and assign new certificates, adding the subject alternative name entries described in this section, for each Front End Server and Director that runs the Autodiscover Service.</span></span> <span data-ttu-id="a41ae-201">El enfoque recomendado es modificar también las listas de nombres alternativos de asunto en los certificados de los proxies inversos.</span><span class="sxs-lookup"><span data-stu-id="a41ae-201">The recommended approach is to also modify the subject alternative names lists on certificates for your reverse proxies.</span></span> <span data-ttu-id="a41ae-202">Debe agregar entradas de nombre alternativo para todos los dominios SIP de su organización.</span><span class="sxs-lookup"><span data-stu-id="a41ae-202">You need to add subject alternative name entries for every SIP domain in your organization.</span></span>

<span data-ttu-id="a41ae-203">La reemisión de certificados mediante una entidad emisora de certificados interna suele ser un proceso simple, pero la adición de varias entradas de nombre alternativo de asunto a certificados públicos que usa el proxy inverso puede ser costosa.</span><span class="sxs-lookup"><span data-stu-id="a41ae-203">Reissuing certificates by using an internal certificate authority is typically a simple process, but adding multiple subject alternative name entries to public certificates used by the reverse proxy can be expensive.</span></span> <span data-ttu-id="a41ae-204">Si tiene muchos dominios SIP, lo que hace que la adición de nombres alternativos del sujeto sea muy costosa, puede configurar el proxy inverso para hacer que el servicio de detección automática inicial se solicite en el puerto 80 mediante HTTP, en lugar de con el puerto 443 con HTTPS (la configuración predeterminada).</span><span class="sxs-lookup"><span data-stu-id="a41ae-204">If you have many SIP domains, making the addition of subject alternative names very expensive, you can configure the reverse proxy to make the initial Autodiscover Service request over port 80 using HTTP, instead of port 443 using HTTPS (the default configuration).</span></span> <span data-ttu-id="a41ae-205">Después, la solicitud se redirige al puerto 8080 del director o del grupo front-end.</span><span class="sxs-lookup"><span data-stu-id="a41ae-205">The request is then redirected to port 8080 on the Director or Front End pool.</span></span> <span data-ttu-id="a41ae-206">Al publicar la solicitud de servicio de detección automática inicial en el puerto 80, no es necesario cambiar los certificados del proxy inverso porque la solicitud usa HTTP en lugar de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a41ae-206">When you publish the initial Autodiscover Service request on port 80, you do not need to change certificates for the reverse proxy, because the request uses HTTP rather than HTTPS.</span></span> <span data-ttu-id="a41ae-207">Este enfoque es compatible, pero no lo recomendamos.</span><span class="sxs-lookup"><span data-stu-id="a41ae-207">This approach is supported, but we do not recommend it.</span></span>

</div>

<div>

## <a name="internet-information-services-iis-requirements"></a><span data-ttu-id="a41ae-208">Requisitos de servicios de Internet Information Server (IIS)</span><span class="sxs-lookup"><span data-stu-id="a41ae-208">Internet Information Services (IIS) Requirements</span></span>

<span data-ttu-id="a41ae-209">Le recomendamos que use IIS 7,5, IIS 8,0 o IIS 8,5 para la movilidad.</span><span class="sxs-lookup"><span data-stu-id="a41ae-209">We recommend that you use IIS 7.5, IIS 8.0, or IIS 8.5 for mobility.</span></span> <span data-ttu-id="a41ae-210">El instalador del servicio de movilidad establece indicadores en ASP.NET para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a41ae-210">The Mobility Service installer sets flags in ASP.NET to improve performance.</span></span> <span data-ttu-id="a41ae-211">IIS 7,5 está instalado de forma predeterminada en Windows Server 2008 R2, IIS 8,0 está instalado en Windows Server 2012 y IIS 8,5 está instalado en Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="a41ae-211">IIS 7.5 is installed by default on Windows Server 2008 R2, IIS 8.0 is installed on Windows Server 2012, and IIS 8.5 is installed on Windows Server 2012 R2.</span></span> <span data-ttu-id="a41ae-212">El instalador del servicio de movilidad cambia automáticamente la configuración de ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="a41ae-212">The Mobility Service installer automatically changes the ASP.NET settings.</span></span>

</div>

<div>

## <a name="hardware-load-balancer-requirements"></a><span data-ttu-id="a41ae-213">Requisitos del equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="a41ae-213">Hardware Load Balancer Requirements</span></span>

<span data-ttu-id="a41ae-214">En el equilibrador de carga de hardware que admite el grupo de servidores front-end, el tráfico de IP virtual de servicios web externos (VIP) del tráfico de servicios web se debe configurar para el origen.</span><span class="sxs-lookup"><span data-stu-id="a41ae-214">On the hardware load balancer that is supporting the Front End pool, the external Web Services virtual IPs (VIPs) for Web Services traffic must be configured for source.</span></span> <span data-ttu-id="a41ae-215">La afinidad de origen ayuda a garantizar que se envíen varias conexiones de un solo cliente a un servidor para mantener el estado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="a41ae-215">Source affinity helps to ensure that multiple connections from a single client are sent to one server to maintain session state.</span></span> <span data-ttu-id="a41ae-216">Para obtener más información sobre los requisitos de afinidad, consulte [requisitos de equilibrio de carga para Lync Server 2013](lync-server-2013-load-balancing-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a41ae-216">For details about affinity requirements, see [Load balancing requirements for Lync Server 2013](lync-server-2013-load-balancing-requirements.md).</span></span>

<span data-ttu-id="a41ae-217">Si tiene previsto admitir clientes móviles de Lync solo en su red interna de Wi-Fi, debe configurar los VIP de servicios Web internos para el origen como se describe para los VIP de servicios web externos.</span><span class="sxs-lookup"><span data-stu-id="a41ae-217">If you plan to support Lync mobile clients only over your internal Wi-Fi network, you should configure the internal Web Services VIPS for source as described for external Web Services VIPs.</span></span> <span data-ttu-id="a41ae-218">En esta situación, debe usar \_ la afinidad de dirección de origen (o TCP) para los VIP de los servicios Web internos en el equilibrador de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="a41ae-218">In this situation, you should use source\_addr (or TCP) affinity for the internal Web Services VIPs on the hardware load balancer.</span></span> <span data-ttu-id="a41ae-219">Para obtener más información, consulte [requisitos de equilibrio de carga para Lync Server 2013](lync-server-2013-load-balancing-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a41ae-219">For details, see [Load balancing requirements for Lync Server 2013](lync-server-2013-load-balancing-requirements.md).</span></span>

</div>

<div>

## <a name="reverse-proxy-requirements"></a><span data-ttu-id="a41ae-220">Requisitos del proxy inverso</span><span class="sxs-lookup"><span data-stu-id="a41ae-220">Reverse Proxy Requirements</span></span>

<span data-ttu-id="a41ae-221">Si admite el descubrimiento automático para clientes móviles de Lync, debe actualizar la regla de publicación actual de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a41ae-221">If you support automatic discovery for Lync mobile clients, you need to update the current publishing rule as follows:</span></span>

  - <span data-ttu-id="a41ae-222">Si decide actualizar las listas Subject Alternative names en los certificados de proxy inverso y usa HTTPS para la solicitud de servicio de detección automática, debe actualizar la regla de publicación web para lyncdiscover. \<sipdomain\> .</span><span class="sxs-lookup"><span data-stu-id="a41ae-222">If you decide to update the subject alternative names lists on the reverse proxy certificates and use HTTPS for the initial Autodiscover Service request, you must update the web publishing rule for lyncdiscover.\<sipdomain\>.</span></span> <span data-ttu-id="a41ae-223">Normalmente, se combina con la regla de publicación de la dirección URL de servicios web externos en el grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="a41ae-223">Typically, this is combined with the publishing rule for the external Web Services URL on the Front End pool.</span></span>

  - <span data-ttu-id="a41ae-224">Si decide usar HTTP para la solicitud de servicio de detección automática inicial para que no tenga que actualizar la lista de nombres alternativos de asunto en los certificados de proxy inverso, debe crear una nueva regla de publicación web para el puerto HTTP/TCP 80, si aún no existe.</span><span class="sxs-lookup"><span data-stu-id="a41ae-224">If you decide to use HTTP for the initial Autodiscover Service request so that you do not need to update the subject alternative names list on the reverse proxy certificates, you must create a new web publishing rule for port HTTP/TCP 80, if one does not already exist.</span></span> <span data-ttu-id="a41ae-225">Si ya existe una regla para HTTP/TCP 80, puede actualizarla para que incluya el lyncdiscover.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="a41ae-225">If a rule for HTTP/TCP 80 does already exist, you can update that rule to include the lyncdiscover.\<sipdomain\></span></span> <span data-ttu-id="a41ae-226">MOV.</span><span class="sxs-lookup"><span data-stu-id="a41ae-226">entry.</span></span>

<span data-ttu-id="a41ae-227"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a41ae-227"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

