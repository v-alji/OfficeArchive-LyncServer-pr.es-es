---
title: 'Lync Server 2013: Creación de registros DNS para el servicio Detección automática'
description: 'Lync Server 2013: crear registros DNS para el servicio Detección automática.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating DNS records for the Autodiscover Service
ms:assetid: 3756ffe4-c6b1-492d-850e-42a832e06567
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690010(v=OCS.15)
ms:contentKeyID: 48183823
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6903e6b07001289db8b65e8cc962e8d8db4b248b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431515"
---
# <a name="creating-dns-records-for-the-autodiscover-service-in-lync-server-2013"></a><span data-ttu-id="309e6-103">Creación de registros DNS para el servicio Detección automática en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="309e6-103">Creating DNS records for the Autodiscover Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="309e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="309e6-104">

<span> </span></span></span>

<span data-ttu-id="309e6-105">_**Última modificación del tema:** 2014-06-20_</span><span class="sxs-lookup"><span data-stu-id="309e6-105">_**Topic Last Modified:** 2014-06-20_</span></span>

<span data-ttu-id="309e6-106">Los usuarios de Lync Mobile deberán habilitar la detección automática y una parte de eso implica crear algunos registros del sistema de nombres de dominio (DNS).</span><span class="sxs-lookup"><span data-stu-id="309e6-106">Your Lync Mobile users will need you to enable autodiscovery, and a part of that involves creating some Domain Name System (DNS) records.</span></span> <span data-ttu-id="309e6-107">Según sus necesidades, necesita lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="309e6-107">Depending on your needs, you need the following:</span></span>

  - <span data-ttu-id="309e6-108">Un registro DNS interno para admitir usuarios móviles que se conectan desde la red de su organización.</span><span class="sxs-lookup"><span data-stu-id="309e6-108">An internal DNS record to support mobile users who’re connecting from within your organization's network.</span></span>

  - <span data-ttu-id="309e6-109">Registro DNS externo o público para admitir usuarios móviles que se conectan desde Internet</span><span class="sxs-lookup"><span data-stu-id="309e6-109">An external, or public, DNS record to support mobile users who’re connecting from the Internet</span></span>

<span data-ttu-id="309e6-110">¿Por qué?</span><span class="sxs-lookup"><span data-stu-id="309e6-110">Why both?</span></span> <span data-ttu-id="309e6-111">Debe crear un registro DNS interno y un registro DNS externo para cada dominio SIP.</span><span class="sxs-lookup"><span data-stu-id="309e6-111">You need to create both an internal DNS record and an external DNS record for each SIP domain.</span></span>

<span data-ttu-id="309e6-112">Los registros DNS que cree pueden ser registros A (hospedaje) o registros CNAME.</span><span class="sxs-lookup"><span data-stu-id="309e6-112">The DNS records you create can be either A (host) records or CNAME records.</span></span> <span data-ttu-id="309e6-113">Para ayudarte, veremos cómo crear estos registros DNS internos y externos a continuación.</span><span class="sxs-lookup"><span data-stu-id="309e6-113">To help you out, we’ll walk through how to create these internal and external DNS records below.</span></span> <span data-ttu-id="309e6-114">Si necesita más información sobre los requisitos de DNS para los usuarios móviles, puede consultar [los requisitos técnicos de movilidad en Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="309e6-114">If you need to do some further reading about the DNS requirements for mobile users, you can check out [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span>

<div>

## <a name="creating-an-internal-dns-cname-record"></a><span data-ttu-id="309e6-115">Crear un registro CNAME de DNS interno</span><span class="sxs-lookup"><span data-stu-id="309e6-115">Creating an internal DNS CNAME record</span></span>

1.  <span data-ttu-id="309e6-116">Para crear un registro DNS interno, tendrá que iniciar sesión en un servidor DNS de su red con una cuenta de dominio que sea miembro del grupo administradores de dominio o miembro del grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="309e6-116">To make an internal DNS record, you’ll need to log on to a DNS server in your network with a domain account that’s either a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

2.  <span data-ttu-id="309e6-117">Abra el complemento administrativo DNS: haga clic en **Inicio**, haga clic en **herramientas administrativas** y, a continuación, haga clic en **DNS**.</span><span class="sxs-lookup"><span data-stu-id="309e6-117">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="309e6-118">En el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para el dominio de Active Directory en el que se instalan el grupo de directores de Lync Server 2013 y el grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="309e6-118">In the console tree of the DNS server, expand **Forward Lookup Zones** for the Active Directory domain where your Lync Server 2013 Director pool and Front End pool are installed.</span></span> <span data-ttu-id="309e6-119">(por ejemplo, contoso. local).</span><span class="sxs-lookup"><span data-stu-id="309e6-119">(for example, contoso.local).</span></span>

4.  <span data-ttu-id="309e6-120">Compruebe si existe un registro A (AAAA para IPv6) para el grupo de directores para un registro DNS interno, debe existir un registro A host para el nombre de dominio completo (FQDN) del servicio Web interno para el grupo de directores (por ejemplo, lyncwebdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="309e6-120">Check and see if a host A (AAAA for IPv6) record exists for your Director pool for an internal DNS record, a host A record should exist for the internal Web Services fully qualified domain name (FQDN) for your Director pool (for example, lyncwebdir01.contoso.local).</span></span> <span data-ttu-id="309e6-121">Si no está aquí, es posible que no esté usando un grupo de directores y tendrá que usar el FQDN de su grupo de servidores front-end o incluso un FQDN de servidor único, si es su configuración.</span><span class="sxs-lookup"><span data-stu-id="309e6-121">If it’s not here, you may not be using a Director pool, and you’ll need to use the FQDN for your Front End pool or even a single server FQDN, if that’s your setup.</span></span>

5.  <span data-ttu-id="309e6-122">Teniendo esto en mente, compruebe si existe un registro A (AAAA para IPv6) para el grupo de servidores front-end para un registro DNS interno, debe existir un registro de host A (o AAAA) para el FQDN de los servicios Web internos de su grupo de front-end (por ejemplo, lyncwebpool01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="309e6-122">Keeping that in mind, check and see if a host A (AAAA for IPv6) record exists for your Front End pool for an internal DNS record, a host A (or AAAA) record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span> <span data-ttu-id="309e6-123">Si no es así, tendrá que tomar nota del FQDN para el servidor front-end o del servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="309e6-123">If it doesn’t, you’ll need to make note of the FQDN for the Front End Server or Standard Edition server.</span></span>

6.  <span data-ttu-id="309e6-124">Una vez que sepa qué registros de host A (o AAAA) existen, en el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para su dominio SIP (por ejemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="309e6-124">Once you know what host A (or AAAA) records exist, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

7.  <span data-ttu-id="309e6-125">Haga clic con el botón derecho en el nombre de dominio SIP y después haga clic en **nuevo alias (CNAME)**.</span><span class="sxs-lookup"><span data-stu-id="309e6-125">Right-click the SIP domain name, and then click **New Alias (CNAME)**.</span></span>

8.  <span data-ttu-id="309e6-126">En **nombre de alias**, escriba lyncdiscoverinternal como nombre de host para la dirección URL interna del servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="309e6-126">In **Alias name**, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>

9.  <span data-ttu-id="309e6-127">En **nombre de dominio completo (FQDN) para el host de destino**, escriba o busque el FQDN de los servicios Web internos de su grupo de directores (por ejemplo, lyncwebdir01. contoso. local) y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="309e6-127">In **Fully qualified domain name (FQDN) for target host**, type or browse to the internal Web Services FQDN for your Director pool (for example, lyncwebdir01.contoso.local) and then click **OK**.</span></span>

10. <span data-ttu-id="309e6-128">Debe crear un nuevo registro CNAME de detección automática en la zona de búsqueda directa de cada dominio SIP que admita en el entorno de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="309e6-128">You must create a new Autodiscover CNAME record in the forward lookup zone of each SIP domain that you support in your Lync Server 2013 environment.</span></span>

</div>

<div>

## <a name="creating-an-external-dns-cname-record"></a><span data-ttu-id="309e6-129">Crear un registro CNAME DNS externo</span><span class="sxs-lookup"><span data-stu-id="309e6-129">Creating an external DNS CNAME record</span></span>

1.  <span data-ttu-id="309e6-130">Para crear un registro CNAME DNS externo, tendrá que conectarse a su proveedor de DNS público y, a continuación, seguir nuestros pasos.</span><span class="sxs-lookup"><span data-stu-id="309e6-130">To create an external DNS CNAME record, you’re going to need to connect to your public DNS provider, and then follow our steps.</span></span> <span data-ttu-id="309e6-131">No podemos describir exactamente dónde va a estar en el entorno de su proveedor de DNS, ya que puede haber diferentes formas de administrar su DNS externo, pero esperamos que estos pasos le ayuden.</span><span class="sxs-lookup"><span data-stu-id="309e6-131">We can’t describe exactly where you’re going in your DNS provider’s environment as there may be different ways of managing your external DNS, but we hope these steps help.</span></span>

2.  <span data-ttu-id="309e6-132">Inicie sesión en su proveedor de DNS externo con una cuenta que pueda crear registros DNS en ese entorno.</span><span class="sxs-lookup"><span data-stu-id="309e6-132">Log into your external DNS provider with an account that can create DNS records in that environment.</span></span>

3.  <span data-ttu-id="309e6-133">Ya se ha creado un dominio SIP para este entorno.</span><span class="sxs-lookup"><span data-stu-id="309e6-133">You should have a SIP domain created for this environment already.</span></span> <span data-ttu-id="309e6-134">Expanda la **zona de búsqueda directa** para este dominio SIP o selecciónela en función de la interfaz DNS externa que se esté usando.</span><span class="sxs-lookup"><span data-stu-id="309e6-134">Expand the **Forward Lookup Zone** for this SIP domain, or otherwise select it depending on the external DNS interface being used.</span></span>

4.  <span data-ttu-id="309e6-135">Ya debería ver un registro host A (AAAA para IPv6) para el grupo de directores (como lyncwebexdir01.contoso.com), por lo que debe confirmar que está allí.</span><span class="sxs-lookup"><span data-stu-id="309e6-135">You should already see a host A (AAAA for IPv6) record for your Director pool (such as lyncwebexdir01.contoso.com), so confirm that it’s there.</span></span> <span data-ttu-id="309e6-136">De lo contrario, es posible que no esté usando un grupo de directores.</span><span class="sxs-lookup"><span data-stu-id="309e6-136">If it’s not, then you may not be using a Director pool.</span></span> <span data-ttu-id="309e6-137">Si este es el caso, tendrá que usar el FQDN de su grupo de servidores front-end o, si hace esto para un único servidor, para el servidor de Front-End Server o Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="309e6-137">If that’s the case, you’ll need to use the FQDN of your Front End Pool, or if you’re doing this for a single server, for your Front-End server or Standard Edition server.</span></span>

5.  <span data-ttu-id="309e6-138">También necesitará confirmar que existe un registro de host A (AAAA para IPv6) para su servicio Web externo nombre de dominio completo (FQDN) para el grupo front-end (como lyncwebextpool01.contoso.com), o un FQDN para su FQDN de servidor único si no tiene ningún grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="309e6-138">You’ll also need to confirm that a host A (AAAA for IPv6) record exists for your external Web Services Fully Qualified Domain Name (FQDN) for your Front End pool (such as lyncwebextpool01.contoso.com), or a FQDN for your single-server FQDN if you have no Front End pool.</span></span> <span data-ttu-id="309e6-139">Tal y como se indicó en el paso anterior, necesitará lo siguiente si no tiene un grupo de directores.</span><span class="sxs-lookup"><span data-stu-id="309e6-139">As noted in the previous step, you’ll need this below if you don’t have a Director pool.</span></span>

6.  <span data-ttu-id="309e6-140">Ahora, en el formato adecuado para su proveedor de DNS externo, elija la opción para crear un **nuevo alias (CNAME)** (puede ser una opción de menú o un vínculo, según el formato del proveedor DNS).</span><span class="sxs-lookup"><span data-stu-id="309e6-140">Now, in the appropriate format for your external DNS provider, choose the option for creating a **New Alias (CNAME)** (this may be a menu option or a link, depending on the format of the DNS provider).</span></span>

7.  <span data-ttu-id="309e6-141">Debe haber alguna forma de cuadro de texto **nombre de alias** como con el DNS interno, debe escribir lyncdiscover como nombre de host para la dirección URL del servicio de detección automática externa.</span><span class="sxs-lookup"><span data-stu-id="309e6-141">There should be some form of **Alias name** text box as with the internal DNS, you should enter lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>

8.  <span data-ttu-id="309e6-142">También debe haber alguna forma de un **nombre de dominio completo (FQDN) para** el cuadro de texto de host de destino, aquí es donde especificará el FQDN de servicios web externos para el grupo de directores (por ejemplo, lyncwebexdir01.contoso.com) y, a continuación, haga clic en aceptar o realice cualquier acción en el DNS externo para aceptar la creación de esta entrada.</span><span class="sxs-lookup"><span data-stu-id="309e6-142">There should also be some form of a **Fully qualified domain name (FQDN) for target host** text box, here’s where you’ll enter the external Web Services FQDN for your Director pool (for example, lyncwebexdir01.contoso.com) and then click OK or take whatever action in the external DNS to accept the creation of this entry.</span></span> <span data-ttu-id="309e6-143">Como se mencionó anteriormente en el paso 4, si no tiene un grupo de directores, tendrá que usar el FQDN del grupo de servidores front-end o el FQDN de servidor único que ha configurado, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="309e6-143">As noted in Step 4, above, if you don’t have a Director pool, you’ll need to use the Front End pool FQDN or the single-server FQDN you have set up, as appropriate.</span></span>

9.  <span data-ttu-id="309e6-144">Tendrá que crear un nuevo registro CNAME de detección automática en la zona de búsqueda directa de cada dominio SIP que se admita en su entorno de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="309e6-144">You’ll need to make a new Autodiscover CNAME record in the forward lookup zone of each SIP domain that’s supported in your Lync 2013 environment.</span></span>

</div>

<div>

## <a name="creating-an-internal-dns-a-record"></a><span data-ttu-id="309e6-145">Crear un registro DNS interno A</span><span class="sxs-lookup"><span data-stu-id="309e6-145">Creating an internal DNS A record</span></span>

1.  <span data-ttu-id="309e6-146">Para crear un registro DNS interno, inicie sesión en un servidor DNS de la red con una cuenta de dominio que sea miembro del grupo administradores de dominio o miembro del grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="309e6-146">To make an internal DNS record, log on to a DNS server in your network with a domain account that’s a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

2.  <span data-ttu-id="309e6-147">Abra el complemento administrativo DNS: haga clic en **Inicio**, haga clic en **herramientas administrativas** y, a continuación, haga clic en **DNS**.</span><span class="sxs-lookup"><span data-stu-id="309e6-147">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="309e6-148">Para un registro DNS interno, en el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para el dominio de Active Directory (por ejemplo, contoso. local) donde esté instalado el grupo de directores de Lync Server 2013 y el grupo front-end.</span><span class="sxs-lookup"><span data-stu-id="309e6-148">For an internal DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your Active Directory domain (for example, contoso.local) where your Lync Server 2013 Director pool and Front End pool are installed.</span></span>

4.  <span data-ttu-id="309e6-149">Compruebe si existe un registro A (AAAA para IPv6) para el grupo de directores para un registro DNS interno, debe existir un registro A host para el nombre de dominio completo (FQDN) del servicio Web interno para el grupo de directores (por ejemplo, lyncwebdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="309e6-149">Check and see if a host A (AAAA for IPv6) record exists for your Director pool for an internal DNS record, a host A record should exist for the internal Web Services fully qualified domain name (FQDN) for your Director pool (for example, lyncwebdir01.contoso.local).</span></span> <span data-ttu-id="309e6-150">Si no está aquí, es posible que no esté usando un grupo de directores y tendrá que usar la dirección IP del grupo de servidores front-end o incluso una dirección IP del servidor, si se trata de la configuración.</span><span class="sxs-lookup"><span data-stu-id="309e6-150">If it’s not here, you may not be using a Director pool, and you’ll need to use the IP address for your Front End pool or even a single server IP address, if that’s your setup.</span></span>

5.  <span data-ttu-id="309e6-151">Teniendo esto en mente, compruebe si existe un registro A (AAAA para IPv6) para el grupo de servidores front-end para un registro DNS interno, debe existir un registro de host A (o AAAA) para el FQDN de los servicios Web internos de su grupo de front-end (por ejemplo, lyncwebpool01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="309e6-151">Keeping that in mind, check and see if a host A (AAAA for IPv6) record exists for your Front End pool for an internal DNS record, a host A (or AAAA) record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span> <span data-ttu-id="309e6-152">Si no es así, tendrá que tomar nota de la dirección IP del servidor front-end o del servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="309e6-152">If it doesn’t, you’ll need to make note of the IP address for the Front End Server or Standard Edition server.</span></span>

6.  <span data-ttu-id="309e6-153">Una vez que sepa qué registros de host A (o AAAA) existen, en el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para su dominio SIP (por ejemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="309e6-153">Once you know what host A (or AAAA) records exist, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

7.  <span data-ttu-id="309e6-154">Haga clic con el botón secundario en el nombre de dominio SIP y, a continuación, haga clic en **nuevo host (A o aaaa)**.</span><span class="sxs-lookup"><span data-stu-id="309e6-154">Right-click the SIP domain name, and then click **New Host (A or AAAA)**.</span></span>

8.  <span data-ttu-id="309e6-155">En **nombre**, escriba lyncdiscoverinternal como nombre de host para la dirección URL interna del servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="309e6-155">In **Name**, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>

9.  <span data-ttu-id="309e6-156">En **dirección IP**, escriba la dirección IP de los servicios Web internos del Director (o bien, si usa un equilibrador de carga, escriba la dirección IP virtual (VIP) del equilibrador de carga del Director).</span><span class="sxs-lookup"><span data-stu-id="309e6-156">In **IP Address**, type the internal Web Services IP address of the Director (or, if you use a load balancer, type the virtual IP (VIP) of the Director load balancer).</span></span> <span data-ttu-id="309e6-157">Como se mencionó anteriormente en el paso 4, si no está usando un director, es posible que tenga que escribir la dirección IP del servidor front-end o el servidor Standard Edition o, si usa un equilibrador de carga, escriba la VIP del equilibrador de carga del grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="309e6-157">As noted in Step 4 above, if you aren’t using a Director, you may need to enter the IP address of the Front End Server or Standard Edition server or, if you use a load balancer, type the VIP of the Front End pool load balancer.</span></span>

10. <span data-ttu-id="309e6-158">Haga clic en **Agregar host** y, a continuación, en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="309e6-158">Click **Add Host**, and then click **OK**.</span></span>

11. <span data-ttu-id="309e6-159">Para crear un registro A o AAAA adicional, repita los pasos 8 a 10, teniendo en cuenta que tendrá que crear nuevos registros A o AAAA de detección automática en la zona de búsqueda directa de cada dominio SIP que se admita en su entorno de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="309e6-159">To create an additional A or AAAA record, repeat steps 8 through 10, keeping in mind that you’ll need to create new Autodiscover A or AAAA records in the forward lookup zone of each SIP domain that’s supported in your Lync Server 2013 environment.</span></span>

12. <span data-ttu-id="309e6-160">Cuando haya terminado de crear un registro (para IPv6, AAAA), haga clic en **listo**.</span><span class="sxs-lookup"><span data-stu-id="309e6-160">When you are finished creating A (for IPv6, AAAA) records, click **Done**.</span></span>

</div>

<div>

## <a name="creating-an-external-dns-a-record"></a><span data-ttu-id="309e6-161">Crear un registro DNS externo</span><span class="sxs-lookup"><span data-stu-id="309e6-161">Creating an external DNS A record</span></span>

1.  <span data-ttu-id="309e6-162">Para crear un registro DNS externo, conéctese a su proveedor de DNS público y, a continuación, siga nuestros pasos.</span><span class="sxs-lookup"><span data-stu-id="309e6-162">To create an external DNS record, connect to your public DNS provider, and then follow our steps.</span></span> <span data-ttu-id="309e6-163">No podemos describir exactamente dónde va a estar en el entorno de su proveedor de DNS, ya que puede haber diferentes formas de administrar su DNS externo, pero esperamos que estos pasos le ayuden.</span><span class="sxs-lookup"><span data-stu-id="309e6-163">We can’t describe exactly where you’re going in your DNS provider’s environment as there may be different ways of managing your external DNS, but we hope these steps help.</span></span>

2.  <span data-ttu-id="309e6-164">Tendrá que haber iniciado sesión como una cuenta que puede crear registros DNS en ese entorno.</span><span class="sxs-lookup"><span data-stu-id="309e6-164">You’ll need to be logged in as an account that can create DNS records in that environment.</span></span>

3.  <span data-ttu-id="309e6-165">Para un registro DNS externo, en el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para su dominio SIP (por ejemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="309e6-165">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span> <span data-ttu-id="309e6-166">Para un registro DNS externo, en el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para su dominio SIP (por ejemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="309e6-166">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

4.  <span data-ttu-id="309e6-167">Ya debería ver un registro host A (AAAA para IPv6) para el grupo de directores (como lyncwebexdir01.contoso.com), por lo que debe confirmar que está allí y cuál es la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="309e6-167">You should already see a host A (AAAA for IPv6) record for your Director pool (such as lyncwebexdir01.contoso.com), so confirm that it’s there and what the IP address is.</span></span> <span data-ttu-id="309e6-168">De lo contrario, es posible que no esté usando un grupo de directores.</span><span class="sxs-lookup"><span data-stu-id="309e6-168">If it’s not, then you may not be using a Director pool.</span></span> <span data-ttu-id="309e6-169">Si ese es el caso, tendrá que usar la dirección IP de su grupo de servidores front-end o, si lo hace para un único servidor, para el servidor de Front-End Server o Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="309e6-169">If that’s the case, you’ll need to use the IP address of your Front End Pool, or if you’re doing this for a single server, for your Front-End server or Standard Edition server.</span></span> <span data-ttu-id="309e6-170">Tenga en cuenta que los servidores también pueden estar detrás de un equilibrador de carga o con un proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="309e6-170">Keep in mind that your servers may also be behind a load-balancer, or using a reverse proxy.</span></span> <span data-ttu-id="309e6-171">Anote las direcciones IP también para seguir los pasos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="309e6-171">Make note of the IP addresses as well for following the steps below.</span></span>

5.  <span data-ttu-id="309e6-172">También necesitará confirmar que existe un registro de host A (AAAA para IPv6) para su servicio Web externo nombre de dominio completo (FQDN) para el grupo de front-end (como lyncwebextpool01.contoso.com) o una dirección IP para la instalación de Lync de servidor único si no tiene ningún grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="309e6-172">You’ll also need to confirm that a host A (AAAA for IPv6) record exists for your external Web Services Fully Qualified Domain Name (FQDN) for your Front End pool (such as lyncwebextpool01.contoso.com), or an IP address for your single-server Lync installation if you have no Front End pool.</span></span> <span data-ttu-id="309e6-173">Tal y como se indicó en el paso anterior, necesitará lo siguiente si no tiene un grupo de directores.</span><span class="sxs-lookup"><span data-stu-id="309e6-173">As noted in the previous step, you’ll need this below if you don’t have a Director pool.</span></span>

6.  <span data-ttu-id="309e6-174">Ahora, en el formato adecuado para su proveedor de DNS externo, elija la opción para crear un **nuevo host a o AAAA** (puede ser una opción de menú o un vínculo, según el formato del proveedor DNS).</span><span class="sxs-lookup"><span data-stu-id="309e6-174">Now, in the appropriate format for your external DNS provider, choose the option for creating a **New Host A or AAAA** (this may be a menu option or a link, depending on the format of the DNS provider).</span></span>

7.  <span data-ttu-id="309e6-175">Debe haber un lugar para escribir un **nombre**, escriba lyncdiscover como nombre de host para la dirección URL del servicio de detección automática externa.</span><span class="sxs-lookup"><span data-stu-id="309e6-175">There should be a place to enter a **Name**, type lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>

8.  <span data-ttu-id="309e6-176">También debe haber un cuadro de texto **dirección IP** , aquí es donde debe especificar la IP de su grupo de directores (por ejemplo, lyncwebexdir01.contoso.com) o posiblemente la IP del equilibrador de carga del grupo (o una IP de proxy invertida que lleva a la misma) y, a continuación, haga clic en aceptar o realice cualquier acción en el DNS externo para aceptar la creación de esta entrada.</span><span class="sxs-lookup"><span data-stu-id="309e6-176">There should also be an **IP Address** text box, here’s where you’ll enter the IP for your for your Director pool (for example, lyncwebexdir01.contoso.com) or possibly the IP of your pool’s load balancer (or a reverse proxy IP that leads to the same) and then click OK or take whatever action in the external DNS to accept the creation of this entry.</span></span> <span data-ttu-id="309e6-177">Como se mencionó anteriormente en el paso 4, si no tiene un grupo de directores, tendrá que usar la dirección IP del grupo de servidores front-end o la dirección IP del servidor único que haya configurado, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="309e6-177">As noted in Step 4, above, if you don’t have a Director pool, you’ll need to use the Front End pool IP address or the single-server IP address you have set up, as appropriate.</span></span>

9.  <span data-ttu-id="309e6-178">Tendrá que crear un nuevo registro de detección automática A o AAAA en la zona de búsqueda directa de cada dominio SIP que se admita en su entorno de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="309e6-178">You’ll need to make a new Autodiscover A or AAAA record in the forward lookup zone of each SIP domain that’s supported in your Lync 2013 environment.</span></span>

<span data-ttu-id="309e6-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="309e6-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

