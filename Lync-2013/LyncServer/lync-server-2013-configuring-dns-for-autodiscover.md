---
title: 'Lync Server 2013: configuración de DNS para la detección automática'
description: 'Lync Server 2013: configuración de DNS para la detección automática.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring DNS for Autodiscover
ms:assetid: f07a634c-3cf3-4958-8556-84596319ef54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945656(v=OCS.15)
ms:contentKeyID: 51541528
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98a56cf3aa260bcbec9099e65958a9b17c3eaf26
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433188"
---
# <a name="configuring-dns-for-autodiscover-in-lync-server-2013"></a><span data-ttu-id="f1fc4-103">Configuración de DNS para la detección automática en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1fc4-103">Configuring DNS for Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1fc4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1fc4-104">

<span> </span></span></span>

<span data-ttu-id="f1fc4-105">_**Última modificación del tema:** 2012-12-12_</span><span class="sxs-lookup"><span data-stu-id="f1fc4-105">_**Topic Last Modified:** 2012-12-12_</span></span>

<span data-ttu-id="f1fc4-106">Para admitir la detección automática de los clientes de Lync, debe crear los siguientes registros del sistema de nombres de dominio (DNS):</span><span class="sxs-lookup"><span data-stu-id="f1fc4-106">To support autodiscovery for Lync clients, you need to create the following Domain Name System (DNS) records:</span></span>

  - <span data-ttu-id="f1fc4-107">Un registro DNS interno para admitir clientes de Lync que se conecten desde la red de la organización</span><span class="sxs-lookup"><span data-stu-id="f1fc4-107">An internal DNS record to support Lync clients who connect from within your organization's network</span></span>

  - <span data-ttu-id="f1fc4-108">Un registro DNS público o externo para admitir clientes de Lync que se conectan desde Internet</span><span class="sxs-lookup"><span data-stu-id="f1fc4-108">An external, or public, DNS record to support Lync clients who connect from the Internet</span></span>

<span data-ttu-id="f1fc4-109">Debe crear un registro DNS interno y un registro DNS externo para cada dominio SIP.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-109">You must create an internal DNS record and an external DNS record for each SIP domain.</span></span>

<span data-ttu-id="f1fc4-110">Los registros DNS pueden ser A (host) o registros CNAME, en función de su capacidad para crear certificados nuevos con el nombre alternativo de asunto adicional (SAN).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-110">The DNS records can be either A (host) records or CNAME records, based on your ability to create new certificates with the additional subject alternate name (SAN).</span></span> <span data-ttu-id="f1fc4-111">Si no puede solicitar e implementar un nuevo certificado externo (público) con el lyncdiscover.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="f1fc4-111">If you are not able to request and deploy a new external (public) certificate with the lyncdiscover.\<domain name\></span></span> <span data-ttu-id="f1fc4-112">SAN, use el procedimiento para usar el puerto HTTP/TCP 80.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-112">SAN, use the procedure for using HTTP/TCP port 80.</span></span> <span data-ttu-id="f1fc4-113">Los procedimientos siguientes describen cómo crear registros DNS internos y externos.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-113">The following procedures describe how to create internal and external DNS records.</span></span>

<div>

## <a name="to-create-dns-cname-records"></a><span data-ttu-id="f1fc4-114">Para crear registros CNAME de DNS</span><span class="sxs-lookup"><span data-stu-id="f1fc4-114">To create DNS CNAME records</span></span>

1.  <span data-ttu-id="f1fc4-115">Inicie sesión en un servidor DNS de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-115">Log on to a DNS server as follows:</span></span>
    
      - <span data-ttu-id="f1fc4-116">Para crear un registro DNS interno, inicie sesión en un servidor DNS de la red como miembro del grupo administradores de dominio o miembro del grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-116">To create an internal DNS record, log on to a DNS server in your network as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>
    
      - <span data-ttu-id="f1fc4-117">Para crear un registro DNS externo, conéctese a su proveedor de DNS público.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-117">To create an external DNS record, connect to your public DNS provider.</span></span>

2.  <span data-ttu-id="f1fc4-118">Abra el complemento administrativo DNS: haga clic en **Inicio**, haga clic en **herramientas administrativas** y, a continuación, haga clic en **DNS**.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-118">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="f1fc4-119">Realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-119">Do one of the following:</span></span>
    
      - <span data-ttu-id="f1fc4-120">Para un registro DNS interno, en el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para el dominio de Active Directory (por ejemplo, contoso. local).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-120">For an internal DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your Active Directory domain (for example, contoso.local).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="f1fc4-121">Este dominio es el dominio de Active Directory donde &nbsp; se instalan el grupo de directores de Lync Server 2013 y el grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-121">This domain is the Active Directory domain where your Lync Server 2013&nbsp;Director pool and Front End pool are installed.</span></span>

        
        </div>
    
      - <span data-ttu-id="f1fc4-122">Para un registro DNS externo, en el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para su dominio SIP (por ejemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-122">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

4.  <span data-ttu-id="f1fc4-123">Compruebe que existe un registro para el grupo de directores de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-123">Verify that a host A record exists for your Director pool as follows:</span></span>
    
      - <span data-ttu-id="f1fc4-124">Para un registro DNS interno, debe existir un registro A para el nombre de dominio completo (FQDN) de los servicios Web internos para el grupo de directores (por ejemplo, lyncwebdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-124">For an internal DNS record, a host A record should exist for the internal Web Services fully qualified domain name (FQDN) for your Director pool (for example, lyncwebdir01.contoso.local).</span></span>
    
      - <span data-ttu-id="f1fc4-125">Para un registro DNS externo, debe existir un registro A host para el FQDN de los servicios web externos para el grupo de directores (por ejemplo, lyncwebextdir.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-125">For an external DNS record, a host A record should exist for the external web services FQDN for your Director pool (for example, lyncwebextdir.contoso.com).</span></span>

5.  <span data-ttu-id="f1fc4-126">Compruebe que existe un registro de host para el grupo de servidores front-end de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-126">Verify that a host A record exists for your Front End pool as follows:</span></span>
    
      - <span data-ttu-id="f1fc4-127">Para un registro DNS interno, debe existir un registro A en el FQDN de los servicios Web internos para el grupo de servidores front-end (por ejemplo, lyncwebpool01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-127">For an internal DNS record, a host A record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span>
    
      - <span data-ttu-id="f1fc4-128">Para un registro DNS externo, debe existir un registro A host para el FQDN de los servicios web externos para el grupo de front-end (por ejemplo, lyncwebextpool01.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-128">For an external DNS record, a host A record should exist for the external Web Services FQDN for your Front End pool (for example, lyncwebextpool01.contoso.com).</span></span>

6.  <span data-ttu-id="f1fc4-129">Para un registro DNS interno, en el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para su dominio SIP (por ejemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-129">For an internal DNS record, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1fc4-130">Si va a crear un registro DNS externo, las <STRONG>zonas de búsqueda directa</STRONG> ya están expandidas para su dominio SIP del paso 3.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-130">If you are creating an external DNS record, <STRONG>Forward Lookup Zones</STRONG> is already expanded for your SIP domain from step 3.</span></span>

    
    </div>

7.  <span data-ttu-id="f1fc4-131">Haga clic con el botón derecho en el nombre de dominio SIP y después haga clic en **nuevo alias (CNAME)**.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-131">Right-click the SIP domain name, and then click **New Alias (CNAME)**.</span></span>

8.  <span data-ttu-id="f1fc4-132">En **nombre de alias**, escriba una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-132">In **Alias name**, type one of the following:</span></span>
    
      - <span data-ttu-id="f1fc4-133">Para un registro DNS interno, escriba lyncdiscoverinternal como nombre de host para la dirección URL interna del servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-133">For an internal DNS record, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>
    
      - <span data-ttu-id="f1fc4-134">Para un registro DNS externo, escriba lyncdiscover como nombre de host para la dirección URL del servicio de detección automática externa.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-134">For an external DNS record, type lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>

9.  <span data-ttu-id="f1fc4-135">En el **nombre de dominio completo (FQDN) del host de destino**, realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-135">In **Fully qualified domain name (FQDN) for target host**, do one of the following:</span></span>
    
      - <span data-ttu-id="f1fc4-136">Para un registro DNS interno, escriba o busque el FQDN de servicios Web internos de su grupo de directores (por ejemplo, lyncwebdir01. contoso. local) y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-136">For an internal DNS record, type or browse to the internal Web Services FQDN for your Director pool (for example, lyncwebdir01.contoso.local), and then click **OK**.</span></span>
    
      - <span data-ttu-id="f1fc4-137">Para un registro DNS externo, escriba o busque el FQDN de servicios web externos para el grupo de directores (por ejemplo, lyncwebextdir.contoso.com) y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-137">For an external DNS record, type or browse to the external Web Services FQDN for your Director pool (for example, lyncwebextdir.contoso.com), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1fc4-138">Si no usa un director, use el FQDN de los servicios Web internos y externos para el grupo de servidores front-end, o bien, para un único servidor, el FQDN del servidor front-end o el servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-138">If you do not use a Director, use the internal and external Web Services FQDN for the Front End pool, or, for a single server, the FQDN for the Front End Server or Standard Edition server.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f1fc4-139">Debe crear un nuevo registro CNAME de detección automática en la zona de búsqueda directa de cada dominio SIP que admita en el entorno de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-139">You must create a new Autodiscover CNAME record in the forward lookup zone of each SIP domain that you support in your Lync Server 2013 environment.</span></span>

    
    </div>

</div>

<div>

## <a name="to-create-dns-a-records"></a><span data-ttu-id="f1fc4-140">Para crear registros A de DNS</span><span class="sxs-lookup"><span data-stu-id="f1fc4-140">To create DNS A records</span></span>

1.  <span data-ttu-id="f1fc4-141">Inicie sesión en un servidor DNS de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-141">Log on to a DNS server as follows:</span></span>
    
      - <span data-ttu-id="f1fc4-142">Para crear un registro DNS interno, inicie sesión en un servidor DNS de la red como miembro del grupo administradores de dominio o miembro del grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-142">To create an internal DNS record, log on to a DNS server in your network as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>
    
      - <span data-ttu-id="f1fc4-143">Para crear un registro DNS externo, conéctese a su proveedor de DNS público o servidor DNS externo.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-143">To create an external DNS record, connect to your public DNS provider or external DNS server.</span></span>

2.  <span data-ttu-id="f1fc4-144">Abra el complemento administrativo DNS: haga clic en **Inicio**, haga clic en **herramientas administrativas** y, a continuación, haga clic en **DNS**.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-144">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="f1fc4-145">Realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-145">Do one of the following:</span></span>
    
      - <span data-ttu-id="f1fc4-146">Para un registro DNS interno, en el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para el dominio de Active Directory (por ejemplo, contoso. local).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-146">For an internal DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your Active Directory domain (for example, contoso.local).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="f1fc4-147">Este dominio es el dominio de Active Directory donde &nbsp; se instalan el grupo de directores de Lync Server 2013 y el grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-147">This domain is the Active Directory domain where your Lync Server 2013&nbsp;Director pool and Front End pool are installed.</span></span>

        
        </div>
    
      - <span data-ttu-id="f1fc4-148">Para un registro DNS externo, en el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para su dominio SIP (por ejemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-148">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

4.  <span data-ttu-id="f1fc4-149">Compruebe que existe un registro A (para IPv6, AAAA) para el grupo de directores de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-149">Verify that a host A (for IPv6, AAAA) record exists for your Director pool as follows:</span></span>
    
      - <span data-ttu-id="f1fc4-150">Para un registro DNS interno, debe existir un registro host A (para IPv6, AAAA) para el FQDN de los servicios Web internos para el grupo de directores (por ejemplo, lyncwebdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-150">For an internal DNS record, a host A (for IPv6, AAAA) record should exist for the internal Web Services FQDN for your Director pool (for example, lyncwebdir01.contoso.local).</span></span>
    
      - <span data-ttu-id="f1fc4-151">Para un registro DNS externo, debe existir un registro host A (para IPv6, AAAA) para el FQDN de los servicios web externos para el grupo de directores (por ejemplo, lyncwebextdir.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-151">For an external DNS record, a host A (for IPv6, AAAA) record should exist for the external Web Services FQDN for your Director pool (for example, lyncwebextdir.contoso.com).</span></span>

5.  <span data-ttu-id="f1fc4-152">Compruebe que existe un registro host (para IPv6, AAAA) para el grupo de servidores front-end de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-152">Verify that a host A (for IPv6, AAAA) record exists for your Front End pool as follows:</span></span>
    
      - <span data-ttu-id="f1fc4-153">Para un registro DNS interno, debe existir un registro host A (para IPv6, AAAA) para el FQDN de los servicios Web internos de su grupo de front-end (por ejemplo, lyncwebpool01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-153">For an internal DNS record, a host A (for IPv6, AAAA) record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span>
    
      - <span data-ttu-id="f1fc4-154">Para un registro DNS externo, debe existir un registro host (para IPv6, AAAA) para el FQDN de los servicios web externos para el grupo de front-end (por ejemplo, lyncwebextpool01.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-154">For an external DNS record, a host A (for IPv6, AAAA) record should exist for the external Web Services FQDN for your Front End pool (for example, lyncwebextpool01.contoso.com).</span></span>

6.  <span data-ttu-id="f1fc4-155">Para un registro DNS interno, en el árbol de consola del servidor DNS, expanda **zonas de búsqueda directa** para su dominio SIP (por ejemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-155">For an internal DNS record, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1fc4-156">Si va a crear un registro DNS externo, las <STRONG>zonas de búsqueda directa</STRONG> ya están expandidas para su dominio SIP del paso 3.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-156">If you are creating an external DNS record, <STRONG>Forward Lookup Zones</STRONG> is already expanded for your SIP domain from step 3.</span></span>

    
    </div>

7.  <span data-ttu-id="f1fc4-157">Haga clic con el botón secundario en el nombre de dominio SIP y, a continuación, haga clic en **nuevo host (A o aaaa)**.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-157">Right-click the SIP domain name, and then click **New Host (A or AAAA)**.</span></span>

8.  <span data-ttu-id="f1fc4-158">En **nombre**, escriba el nombre de host como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-158">In **Name**, type the host name as follows:</span></span>
    
      - <span data-ttu-id="f1fc4-159">Para un registro DNS interno, escriba lyncdiscoverinternal como nombre de host para la dirección URL interna del servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-159">For an internal DNS record, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>
    
      - <span data-ttu-id="f1fc4-160">Para un registro DNS externo, escriba lyncdiscover como nombre de host para la dirección URL del servicio de detección automática externa.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-160">For an external DNS record, type lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f1fc4-161">El nombre de dominio se supone de la zona en la que se define el registro y, por lo tanto, no es necesario escribirlo como parte del registro A.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-161">The domain name is assumed from the zone in which the record is defined and, therefore, does not need to be entered as part of the A record.</span></span>

    
    </div>

9.  <span data-ttu-id="f1fc4-162">En **dirección IP**, escriba la dirección IP de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f1fc4-162">In **IP Address**, type the IP address as follows:</span></span>
    
      - <span data-ttu-id="f1fc4-163">Para un registro DNS interno, escriba la dirección IP de los servicios Web internos del Director (o bien, si usa un equilibrador de carga, escriba la dirección IP virtual (VIP) del equilibrador de carga del Director).</span><span class="sxs-lookup"><span data-stu-id="f1fc4-163">For an internal DNS record, type the internal Web Services IP address of the Director (or, if you use a load balancer, type the virtual IP (VIP) of the Director load balancer).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="f1fc4-164">Si no usa un director, escriba la dirección IP del servidor front-end o del servidor Standard Edition, o bien, si usa un equilibrador de carga, escriba la VIP del equilibrador de carga del grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-164">If you do not use a Director, type the IP address of the Front End Server or Standard Edition server, or, if you use a load balancer, type the VIP of the Front End pool load balancer.</span></span>

        
        </div>
    
      - <span data-ttu-id="f1fc4-165">Para un registro DNS externo, escriba la dirección IP externa o pública del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-165">For an external DNS record, type the external or public IP address of the reverse proxy.</span></span>

10. <span data-ttu-id="f1fc4-166">Haga clic en **Agregar host** y, a continuación, en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-166">Click **Add Host**, and then click **OK**.</span></span>

11. <span data-ttu-id="f1fc4-167">Para crear un registro A adicional, repita los pasos 8 a 10.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-167">To create an additional A record, repeat steps 8 through 10.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f1fc4-168">Debe crear una nueva lyncdiscover y lyncdiscoverinternal registros A en la zona de búsqueda directa de cada dominio SIP que admita en el entorno de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-168">You must create a new lyncdiscover and lyncdiscoverinternal A records in the forward lookup zone of each SIP domain that you support in your Lync Server 2013 environment.</span></span>

    
    </div>

12. <span data-ttu-id="f1fc4-169">Cuando haya terminado de crear un registro (para IPv6, AAAA), haga clic en **listo**.</span><span class="sxs-lookup"><span data-stu-id="f1fc4-169">When you are finished creating A (for IPv6, AAAA) records, click **Done**.</span></span>

<span data-ttu-id="f1fc4-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1fc4-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

