---
title: 'Lync Server 2013: Crear y comprobar registros DNS SRV'
description: 'Lync Server 2013: crear y comprobar registros SRV de DNS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create and verify DNS SRV records
ms:assetid: 86888c7e-1401-458f-9a7b-08ac726deeec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398680(v=OCS.15)
ms:contentKeyID: 48184714
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a71c876d0b26b9305feed7146fa6321a3983588d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432019"
---
# <a name="create-and-verify-dns-srv-records-in-lync-server-2013"></a><span data-ttu-id="04105-103">Crear y comprobar registros DNS SRV en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="04105-103">Create and verify DNS SRV records in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="04105-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="04105-104">

<span> </span></span></span>

<span data-ttu-id="04105-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="04105-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="04105-106">Para completar correctamente este procedimiento, debe haber iniciado sesión en el servidor o dominio como miembro del grupo administradores de dominio o en miembro del grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="04105-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="04105-107">En este tema se describe cómo configurar los registros del sistema de nombres de dominio (DNS) que se deben crear en implementaciones de Lync Server 2013 y los necesarios para iniciar sesión automáticamente en el cliente.</span><span class="sxs-lookup"><span data-stu-id="04105-107">This topic describes how to configure the Domain Name System (DNS) records that you are required to create in Lync Server 2013 deployments and those required for automatic client sign in.</span></span> <span data-ttu-id="04105-108">Al crear un grupo de servidores front-end, el programa de instalación crea los objetos y la configuración de Active Directory para el grupo, incluido el nombre de dominio completo (FQDN) del grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="04105-108">When you create a Front End pool, Setup creates Active Directory objects and settings for the pool, including the pool fully qualified domain name (FQDN).</span></span> <span data-ttu-id="04105-109">Se crean objetos y configuraciones similares para un servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="04105-109">Similar objects and settings are created for a Standard Edition server.</span></span> <span data-ttu-id="04105-110">Para que los clientes puedan conectarse al servidor Standard Edition o del grupo, el FQDN del grupo o del servidor Standard Edition debe estar registrado en DNS.</span><span class="sxs-lookup"><span data-stu-id="04105-110">For clients to be able to connect to the pool or Standard Edition server, the FQDN of the pool or Standard Edition server must be registered in DNS.</span></span> <span data-ttu-id="04105-111">Debe crear registros SRV de DNS en el DNS interno para cada dominio SIP.</span><span class="sxs-lookup"><span data-stu-id="04105-111">You must create DNS SRV records in your internal DNS for every SIP domain.</span></span> <span data-ttu-id="04105-112">En este procedimiento se supone que su DNS interno tiene zonas para sus dominios de usuario SIP.</span><span class="sxs-lookup"><span data-stu-id="04105-112">This procedure assumes that your internal DNS has zones for your SIP user domains.</span></span>

<div>

## <a name="to-configure-a-dns-srv-record"></a><span data-ttu-id="04105-113">Para configurar un registro SRV de DNS</span><span class="sxs-lookup"><span data-stu-id="04105-113">To configure a DNS SRV record</span></span>

1.  <span data-ttu-id="04105-114">En el servidor DNS, haga clic en **Inicio**, haga clic en **herramientas administrativas** y, a continuación, haga clic en **DNS**.</span><span class="sxs-lookup"><span data-stu-id="04105-114">On the DNS server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="04105-115">En el árbol de consola de su dominio SIP, expanda **zonas de búsqueda directa** y, a continuación, haga clic con el botón secundario en el dominio SIP en el que se instalará Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04105-115">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and then right-click the SIP domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="04105-116">Haga clic en **otros registros nuevos**.</span><span class="sxs-lookup"><span data-stu-id="04105-116">Click **Other New Records**.</span></span>

4.  <span data-ttu-id="04105-117">En **Seleccione el tipo de registro del recurso**, haga clic en **Ubicación de servicio (SRV)** y, luego, haga clic en **Crear registro**.</span><span class="sxs-lookup"><span data-stu-id="04105-117">In **Select a resource record type**, click **Service Location (SRV)**, and then click **Create Record**.</span></span>

5.  <span data-ttu-id="04105-118">Haga clic en **servicio** y, a continuación, escriba **\_ sipinternaltls**.</span><span class="sxs-lookup"><span data-stu-id="04105-118">Click **Service**, and then type **\_sipinternaltls**.</span></span>

6.  <span data-ttu-id="04105-119">Haga clic en **Protocolo** y, a continuación, escriba **\_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="04105-119">Click **Protocol**, and then type **\_tcp**.</span></span>

7.  <span data-ttu-id="04105-120">Haga clic en **Número de puerto** y, luego, escriba **5061**.</span><span class="sxs-lookup"><span data-stu-id="04105-120">Click **Port Number**, and then type **5061**.</span></span>

8.  <span data-ttu-id="04105-121">Haga clic en **Host que ofrece este servicio** y, luego, escriba el FQDN del grupo de servidores o del servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="04105-121">Click **Host offering this service**, and then type the FQDN of the pool or Standard Edition server.</span></span>

9.  <span data-ttu-id="04105-122">Haga clic en **Aceptar** y, luego, haga clic en **Listo**.</span><span class="sxs-lookup"><span data-stu-id="04105-122">Click **OK**, and then click **Done**.</span></span>

</div>

<div>

## <a name="to-verify-the-creation-of-a-dns-srv-record"></a><span data-ttu-id="04105-123">Para comprobar la creación de un registro SRV de DNS</span><span class="sxs-lookup"><span data-stu-id="04105-123">To verify the creation of a DNS SRV record</span></span>

1.  <span data-ttu-id="04105-124">Inicie sesión en un equipo cliente del dominio con una cuenta que sea miembro del grupo Usuarios autenticados o que tenga permisos equivalentes.</span><span class="sxs-lookup"><span data-stu-id="04105-124">Log on to a client computer in the domain with an account that is a member of the Authenticated Users group or has equivalent permissions.</span></span>

2.  <span data-ttu-id="04105-125">Haga clic en  **Inicio** y en  **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="04105-125">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="04105-126">En el cuadro **abrir** , escriba **cmd** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="04105-126">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="04105-127">En el símbolo del sistema, escriba **nslookup** y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="04105-127">At the command prompt, type **nslookup**, and then press ENTER.</span></span>

5.  <span data-ttu-id="04105-128">Escriba **set Type = SRV** y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="04105-128">Type **set type=srv**, and then press ENTER.</span></span>

6.  <span data-ttu-id="04105-129">Escriba **\_ sipinternaltls. \_ tcp.contoso.com** y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="04105-129">Type **\_sipinternaltls.\_tcp.contoso.com**, and then press ENTER.</span></span> <span data-ttu-id="04105-130">La salida mostrada para el registro de seguridad de la capa de transporte (TLS) es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="04105-130">The output displayed for the Transport Layer Security (TLS) record is as follows:</span></span>
    
    <span data-ttu-id="04105-131">Server: \<dns server\> . contoso.com</span><span class="sxs-lookup"><span data-stu-id="04105-131">Server: \<dns server\>.contoso.com</span></span>
    
    <span data-ttu-id="04105-132">Direcciones \<IP address of DNS server\></span><span class="sxs-lookup"><span data-stu-id="04105-132">Address: \<IP address of DNS server\></span></span>
    
    <span data-ttu-id="04105-133">Respuesta no autoritaria:</span><span class="sxs-lookup"><span data-stu-id="04105-133">Non-authoritative answer:</span></span>
    
    <span data-ttu-id="04105-134">\_sipinternaltls. \_ Ubicación del servicio tcp.contoso.com SRV:</span><span class="sxs-lookup"><span data-stu-id="04105-134">\_sipinternaltls.\_tcp.contoso.com SRV service location:</span></span>
    
    <span data-ttu-id="04105-135">prioridad = 0</span><span class="sxs-lookup"><span data-stu-id="04105-135">priority = 0</span></span>
    
    <span data-ttu-id="04105-136">peso = 0</span><span class="sxs-lookup"><span data-stu-id="04105-136">weight = 0</span></span>
    
    <span data-ttu-id="04105-137">puerto = 5061</span><span class="sxs-lookup"><span data-stu-id="04105-137">port = 5061</span></span>
    
    <span data-ttu-id="04105-138">SVR hostname = poolname.contoso.com (o un registro de servidor Standard Edition A)</span><span class="sxs-lookup"><span data-stu-id="04105-138">svr hostname = poolname.contoso.com (or Standard Edition server A record)</span></span>
    
    <span data-ttu-id="04105-139">poolname.contoso.com internet address = \<virtual IP Address of the load balancer\> or \<IP address of a single Enterprise Edition server for pools with only one Enterprise Edition server\> o \<IP address of the Standard Edition server\></span><span class="sxs-lookup"><span data-stu-id="04105-139">poolname.contoso.com internet address = \<virtual IP Address of the load balancer\> or \<IP address of a single Enterprise Edition server for pools with only one Enterprise Edition server\> or \<IP address of the Standard Edition server\></span></span>

7.  <span data-ttu-id="04105-140">Cuando haya terminado, en el símbolo del sistema, escriba **Exit** y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="04105-140">When you are finished, at the command prompt, type **exit**, and then press ENTER.</span></span>

</div>

<div>

## <a name="to-verify-that-the-fqdn-of-the-front-end-pool-or-standard-edition-server-can-be-resolved"></a><span data-ttu-id="04105-141">Para comprobar que se puede resolver el FQDN del grupo de servidores front-end o del servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="04105-141">To verify that the FQDN of the Front End pool or Standard Edition server can be resolved</span></span>

1.  <span data-ttu-id="04105-142">Inicie sesión en un equipo cliente del dominio.</span><span class="sxs-lookup"><span data-stu-id="04105-142">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="04105-143">Haga clic en  **Inicio** y en  **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="04105-143">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="04105-144">En el cuadro **abrir** , escriba **cmd** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="04105-144">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="04105-145">En el símbolo del sistema, escriba **nslookup** \<FQDN of the Front End pool\> o \<FQDN of the Standard Edition server\> , y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="04105-145">At the command prompt, type **nslookup** \<FQDN of the Front End pool\> or \<FQDN of the Standard Edition server\>, and then press ENTER.</span></span>

5.  <span data-ttu-id="04105-146">Compruebe que recibe una respuesta que se resuelve en la dirección IP adecuada para el nombre de dominio completo (FQDN).</span><span class="sxs-lookup"><span data-stu-id="04105-146">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

<span data-ttu-id="04105-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="04105-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

