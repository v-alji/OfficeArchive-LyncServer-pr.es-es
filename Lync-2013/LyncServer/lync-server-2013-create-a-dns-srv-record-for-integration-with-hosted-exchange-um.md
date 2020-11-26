---
title: Crear un registro DNS SRV para la integración con mensajería unificada (UM) hospedada de Exchange
description: Crear un registro SRV de DNS para la integración con mensajería unificada de Exchange hospedado.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a DNS SRV record for integration with hosted Exchange UM
ms:assetid: 8ea590ae-58ea-4ca5-9853-e0708b3ea760
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh500728(v=OCS.15)
ms:contentKeyID: 48184770
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 694a595977abe33bebbb5fbcf2a508c9bb4e35a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432236"
---
# <a name="create-a-dns-srv-record-for-integration-with-hosted-exchange-um"></a><span data-ttu-id="36916-103">Crear un registro DNS SRV para la integración con mensajería unificada (UM) hospedada de Exchange</span><span class="sxs-lookup"><span data-stu-id="36916-103">Create a DNS SRV record for integration with hosted Exchange UM</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36916-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36916-104">

<span> </span></span></span>

<span data-ttu-id="36916-105">_**Última modificación del tema:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="36916-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="36916-106">En este tema se describe cómo configurar el registro SRV de sistema de nombres de dominio (DNS) necesario para que un servidor perimetral de Lync Server 2013 se pueda enrutar a un servicio de Exchange hospedado como Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="36916-106">This topic describes how to configure the Domain Name System (DNS) SRV record that is required for a Lync Server 2013 Edge Server to route to a hosted Exchange service such as Microsoft Exchange Online.</span></span>

<div>

## <a name="to-create-an-external-dns-srv-record-for-the-hosted-exchange-service"></a><span data-ttu-id="36916-107">Para crear un registro SRV de DNS externo para el servicio hospedado de Exchange</span><span class="sxs-lookup"><span data-stu-id="36916-107">To create an external DNS SRV record for the hosted Exchange service</span></span>

1.  <span data-ttu-id="36916-108">Inicie sesión en el servidor DNS externo como miembro del grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="36916-108">Log on to the external DNS server as a member of the DnsAdmins group.</span></span>

2.  <span data-ttu-id="36916-109">Haga clic en **Inicio**, seleccione **herramientas administrativas** y, a continuación, haga clic en **DNS**.</span><span class="sxs-lookup"><span data-stu-id="36916-109">Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="36916-110">En el árbol de consola de su dominio SIP, expanda **zonas de búsqueda directa** y seleccione el dominio SIP en el que se instalará Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="36916-110">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and select the SIP domain in which Lync Server 2013 will be installed.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="36916-111">Debe crear el registro SRV de DNS en el dominio SIP en el que se instalará o se instalará Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36916-111">You must create the DNS SRV record in the SIP domain in which Lync Server is or will be installed.</span></span> <span data-ttu-id="36916-112">Al crear el registro SRV, el FQDN usado para el host que ofrece este campo de servicio debe ser el FQDN externo del grupo Edge.</span><span class="sxs-lookup"><span data-stu-id="36916-112">When you create the SRV record, the FQDN used for the Host offering this service field must be the external FQDN of the Edge pool.</span></span> <span data-ttu-id="36916-113">Por ejemplo, si el nombre completo externo del grupo de servidores perimetrales es edge01.contoso.net, escriba ese valor.</span><span class="sxs-lookup"><span data-stu-id="36916-113">For example, if the external FQDN of your Edge pool is edge01.contoso.net, enter that value.</span></span> <span data-ttu-id="36916-114">También debe estar en el mismo dominio que el registro de hosts DNS (A).</span><span class="sxs-lookup"><span data-stu-id="36916-114">This must also be in the same domain as the DNS Hosts (A) record.</span></span>

    
    </div>

4.  <span data-ttu-id="36916-115">Haga clic con el botón secundario en el dominio seleccionado y, a continuación, haga clic en **otros registros nuevos**.</span><span class="sxs-lookup"><span data-stu-id="36916-115">Right-click the selected domain, and then click **Other New Records**.</span></span>

5.  <span data-ttu-id="36916-116">En **tipo de registro de recursos**, haga clic en **Ubicación de servicio (SRV)** y, a continuación, haga clic en **crear registro**.</span><span class="sxs-lookup"><span data-stu-id="36916-116">In **Resource Record Type**, click **Service Location (SRV)**, and then click **Create Record**.</span></span>

6.  <span data-ttu-id="36916-117">En **nuevo registro de recursos**, haga clic en **servicio** y, a continuación, escriba **\_ sipfederationtls**.</span><span class="sxs-lookup"><span data-stu-id="36916-117">In **New Resource Record**, click **Service**, and then type **\_sipfederationtls**.</span></span>

7.  <span data-ttu-id="36916-118">Haga clic en **Protocolo** y, a continuación, escriba **\_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="36916-118">Click **Protocol**, and then type **\_tcp**.</span></span>

8.  <span data-ttu-id="36916-119">Haga clic en **Número de puerto** y, luego, escriba **5061**.</span><span class="sxs-lookup"><span data-stu-id="36916-119">Click **Port Number**, and then type **5061**.</span></span>

9.  <span data-ttu-id="36916-120">Haga clic en **host que ofrece este servicio** y, a continuación, escriba el nombre de dominio completo (FQDN) del grupo perimetral de lync Server 2013 que proporciona acceso a su sistema de lync Server 2013 para clientes externos de confianza.</span><span class="sxs-lookup"><span data-stu-id="36916-120">Click **Host offering this service**, and then type the fully qualified domain name (FQDN) of the Lync Server 2013 Edge pool that provides access to your Lync Server 2013 system for trusted external clients.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="36916-121">El dominio también debe configurarse como un dominio autorizado y aceptado en la configuración de Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="36916-121">The domain must also be set up as an authoritative, accepted domain in your Exchange Online settings.</span></span> <span data-ttu-id="36916-122">Para obtener más información, consulte crear dominios aceptados en <A href="https://go.microsoft.com/fwlink/p/?linkid=229762">https://go.microsoft.com/fwlink/p/?linkId=229762</A> .</span><span class="sxs-lookup"><span data-stu-id="36916-122">For details, see Create Accepted Domains at <A href="https://go.microsoft.com/fwlink/p/?linkid=229762">https://go.microsoft.com/fwlink/p/?linkId=229762</A>.</span></span>

    
    </div>

10. <span data-ttu-id="36916-123">Haga clic en **Aceptar** y, luego, haga clic en **Listo**.</span><span class="sxs-lookup"><span data-stu-id="36916-123">Click **OK**, and then click **Done**.</span></span>

</div>

<div>

## <a name="to-verify-that-the-dns-srv-record-was-created-successfully"></a><span data-ttu-id="36916-124">Para comprobar que el registro SRV de DNS se ha creado correctamente</span><span class="sxs-lookup"><span data-stu-id="36916-124">To verify that the DNS SRV record was created successfully</span></span>

1.  <span data-ttu-id="36916-125">Inicie sesión en un equipo cliente del dominio.</span><span class="sxs-lookup"><span data-stu-id="36916-125">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="36916-126">Haga clic en  **Inicio** y en  **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="36916-126">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="36916-127">En el símbolo del sistema, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="36916-127">At the command prompt, run the following command:</span></span>
    
        nslookup <FQDN Lync Edge Pool>

4.  <span data-ttu-id="36916-128">Compruebe que recibe una respuesta que se resuelve en la dirección IP adecuada para el nombre de dominio completo (FQDN).</span><span class="sxs-lookup"><span data-stu-id="36916-128">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="36916-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="36916-129">See Also</span></span>


[<span data-ttu-id="36916-130">Crear registros DNS para servidores de proxy inverso en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36916-130">Create DNS records for reverse proxy servers in Lync Server 2013</span></span>](lync-server-2013-create-dns-records-for-reverse-proxy-servers.md)  
  

<span data-ttu-id="36916-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36916-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

