---
title: 'Lync Server 2013: Configuración de federación de Lync'
description: 'Lync Server 2013: Configurar la federación de Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399810"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a><span data-ttu-id="de161-103">Configuración de federación de Lync en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de161-103">Setting up Lync federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de161-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de161-104">

<span> </span></span></span>

<span data-ttu-id="de161-105">_**Tema Última modificación:** 2014-03-27_</span><span class="sxs-lookup"><span data-stu-id="de161-105">_**Topic Last Modified:** 2014-03-27_</span></span>

<span data-ttu-id="de161-106">Si ya ha implementado servidores o servidores perimetrales, agregar las características de escenarios federados es un paso adelante.</span><span class="sxs-lookup"><span data-stu-id="de161-106">If you have already deployed you Edge server or servers, adding the federated scenarios features is straight forward.</span></span> <span data-ttu-id="de161-107">Si no ha configurado servidores perimetrales, primero debe hacerlo.</span><span class="sxs-lookup"><span data-stu-id="de161-107">If you have not set up Edge Servers, you must do that first.</span></span> <span data-ttu-id="de161-108">Para obtener más información, vea: Planear el acceso de usuarios externos en [Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) en la documentación de planeamiento e implementar el acceso de usuario externo en [Lync Server 2013](lync-server-2013-deploying-external-user-access.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="de161-108">For details, see: [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="de161-109">Si tiene la intención de configurar cualquier combinación de federación XMPP, federación de Lync o conectividad de mensajería instantánea pública, puede implementarlas simultáneamente o de una en una.</span><span class="sxs-lookup"><span data-stu-id="de161-109">If you intend to setup any combination of XMPP federation, Lync Federation, or public instant messaging connectivity, you can deploy them concurrently or one at a time.</span></span> <span data-ttu-id="de161-110">Si configura las opciones mediante el Generador de topologías y el shell de administración de Lync Server, ejecute el Asistente para la implementación en el servidor perimetral después de configurar las opciones para uno, dos o los tres tipos de federación, puede reducir el número de pasos necesarios.</span><span class="sxs-lookup"><span data-stu-id="de161-110">If you configure the options through the Topology Builder and the Lync Server Management shell, then run the Deployment Wizard at the Edge server after configuring the options for one, two or all three federation types, you can reduce the number of steps required.</span></span>



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a><span data-ttu-id="de161-111">Configurar la federación de Lync en el Generador de topologías y el Asistente para la implementación</span><span class="sxs-lookup"><span data-stu-id="de161-111">Setting Up Lync Federation in Topology Builder and the Deployment Wizard</span></span>

1.  <span data-ttu-id="de161-112">En un servidor front-end, abra generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="de161-112">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="de161-113">Expanda Grupos perimetrales y, a continuación, haga clic con el botón derecho en el servidor perimetral o en el grupo de servidores perimetrales.</span><span class="sxs-lookup"><span data-stu-id="de161-113">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="de161-114">Seleccione Editar propiedades.</span><span class="sxs-lookup"><span data-stu-id="de161-114">Select Edit properties.</span></span>

2.  <span data-ttu-id="de161-115">En Editar propiedades en General, seleccione Habilitar federación para este grupo de servidores perimetrales (Puerto 5061).</span><span class="sxs-lookup"><span data-stu-id="de161-115">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="de161-116">Haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="de161-116">Click OK.</span></span>

3.  <span data-ttu-id="de161-117">Haga clic en Acción, seleccione Topología y publicar.</span><span class="sxs-lookup"><span data-stu-id="de161-117">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="de161-118">Cuando se le solicite en Publicar la topología, haga clic en Siguiente.</span><span class="sxs-lookup"><span data-stu-id="de161-118">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="de161-119">Cuando finalice la publicación, haga clic en Finalizar.</span><span class="sxs-lookup"><span data-stu-id="de161-119">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="de161-120">En el servidor perimetral, abra el Asistente para la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="de161-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="de161-121">Haga clic en Instalar o actualizar Lync Server System y, a continuación, haga clic en Configurar o quitar componentes de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="de161-121">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="de161-122">Haga clic en Ejecutar de nuevo.</span><span class="sxs-lookup"><span data-stu-id="de161-122">Click Run Again.</span></span>

5.  <span data-ttu-id="de161-123">En Configurar componentes de Lync Server, haga clic en Siguiente.</span><span class="sxs-lookup"><span data-stu-id="de161-123">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="de161-124">La pantalla de resumen mostrará las acciones a medida que se ejecuten.</span><span class="sxs-lookup"><span data-stu-id="de161-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="de161-125">Una vez que haya terminado la implementación, haga clic en Ver registro para ver los archivos de registro disponibles.</span><span class="sxs-lookup"><span data-stu-id="de161-125">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="de161-126">Haga clic en Finalizar para completar la implementación.</span><span class="sxs-lookup"><span data-stu-id="de161-126">Click Finish to complete the deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="de161-127">Puede seleccionar esta opción, pero solo un grupo perimetral o un servidor perimetral de su organización se pueden publicar externamente para la federación.</span><span class="sxs-lookup"><span data-stu-id="de161-127">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="de161-128">Todos los accesos de usuarios federados, incluidos los usuarios de mensajería instantánea pública (MI), pasan por el mismo grupo perimetral o un único servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="de161-128">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="de161-129">Por ejemplo, si la implementación incluye un grupo perimetral o un único servidor perimetral implementado en Nueva York y uno implementado en Londres y habilita el soporte de federación en el grupo perimetral de Nueva York o en un único servidor perimetral, el tráfico de señales para los usuarios federados pasará por el grupo perimetral de Nueva York o un único servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="de161-129">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="de161-130">Esto es así incluso para las comunicaciones con usuarios de Londres, aunque un usuario interno de Londres que llame a un usuario federado de Londres usa el grupo de servidores o el servidor perimetral de Londres para el tráfico A/V.</span><span class="sxs-lookup"><span data-stu-id="de161-130">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a><span data-ttu-id="de161-131">Configurar la federación con partners</span><span class="sxs-lookup"><span data-stu-id="de161-131">Configuring Federation with Partners</span></span>

1.  <span data-ttu-id="de161-132">Para configurar una federación correcta con otro Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 u Office Communicator 2007, seleccione el tipo de federación de la tabla siguiente y defina registros SRV dns, host DNS (A o AAAA para IPv6) y configure directivas aplicables al tipo de federación:</span><span class="sxs-lookup"><span data-stu-id="de161-132">To setup a successful federation with another Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2, or Office Communicator 2007, select the type of federation from the following table and define DNS SRV records, DNS host (A or AAAA for IPv6) and configure policies applicable to the type of federation:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="de161-133">Tipo de federación</span><span class="sxs-lookup"><span data-stu-id="de161-133">Federation type</span></span></th>
    <th><span data-ttu-id="de161-134">Registros DNS</span><span class="sxs-lookup"><span data-stu-id="de161-134">DNS Records</span></span></th>
    <th><span data-ttu-id="de161-135">Definición de directiva</span><span class="sxs-lookup"><span data-stu-id="de161-135">Policy Definition</span></span></th>
    <th><span data-ttu-id="de161-136">Notas</span><span class="sxs-lookup"><span data-stu-id="de161-136">Notes</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="de161-137">Dominio de partner detectado</span><span class="sxs-lookup"><span data-stu-id="de161-137">Discovered Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="de161-138">Configure el registro SRV del formato _sipfederationtls._tcp. &lt; Nombre de dominio externo Donde el valor de puerto para el registro SRV es &gt; TCP 5061 y el <strong>host</strong> que ofrece este servicio se define como sip.</span><span class="sxs-lookup"><span data-stu-id="de161-138">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="de161-139">&lt;nombre de dominio &gt; externo: el FQDN de su servicio perimetral de Access.</span><span class="sxs-lookup"><span data-stu-id="de161-139">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="de161-140">Consulte <a href="lync-server-2013-configure-dns-for-edge-support.md">Configurar DNS para soporte técnico perimetral en Lync Server 2013</a> para obtener más información sobre cómo crear el registro SRV</span><span class="sxs-lookup"><span data-stu-id="de161-140">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="de161-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="de161-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="de161-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Habilitar o deshabilitar la detección de socios de federación en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="de161-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Enable or disable discovery of federation partners in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="de161-143">Las versiones anteriores hacían referencia a este tipo de federación como <strong>Federación mejorada abierta.</strong></span><span class="sxs-lookup"><span data-stu-id="de161-143">Previous versions referred to this type of federation as <strong>Open Enhanced Federation</strong>.</span></span> <span data-ttu-id="de161-144">La creación del registro SRV es necesaria para este tipo de federación y es para permitir que otros partners descubran su federación.</span><span class="sxs-lookup"><span data-stu-id="de161-144">The creation of the SRV record is required for this type of federation and is to allow other partners to discover your federation.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="de161-145">Dominio de partner permitido</span><span class="sxs-lookup"><span data-stu-id="de161-145">Allowed Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="de161-146">Configure el registro SRV del formato _sipfederationtls._tcp. &lt; Nombre de dominio externo Donde el valor de puerto para el registro SRV es &gt; TCP 5061 y el <strong>host</strong> que ofrece este servicio se define como sip.</span><span class="sxs-lookup"><span data-stu-id="de161-146">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="de161-147">&lt;nombre de dominio &gt; externo: el FQDN de su servicio perimetral de Access.</span><span class="sxs-lookup"><span data-stu-id="de161-147">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="de161-148">Consulte <a href="lync-server-2013-configure-dns-for-edge-support.md">Configurar DNS para soporte técnico perimetral en Lync Server 2013</a> para obtener más información sobre cómo crear el registro SRV</span><span class="sxs-lookup"><span data-stu-id="de161-148">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="de161-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="de161-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="de161-150">Las versiones anteriores hacían referencia a este tipo de federación como <strong>Federación mejorada.</strong></span><span class="sxs-lookup"><span data-stu-id="de161-150">Previous versions referred to this type of federation as <strong>Enhanced Federation</strong>.</span></span> <span data-ttu-id="de161-151">La creación del registro SRV es opcional para este tipo de federación y permite que otros partners descubran su federación.</span><span class="sxs-lookup"><span data-stu-id="de161-151">The creation of the SRV record is optional for this type of federation and is to allow other partners to discover your federation.</span></span> <span data-ttu-id="de161-152">Por supuesto, se trata de una federación <strong>mejorada abierta</strong>o un dominio de <strong>partner detectado</strong></span><span class="sxs-lookup"><span data-stu-id="de161-152">Of course, this is then an <strong>Open Enhanced Federation</strong>, or <strong>Discovered Partner Domain</strong></span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="de161-153">Servidor asociado permitido</span><span class="sxs-lookup"><span data-stu-id="de161-153">Allowed Partner Server</span></span></p></td>
    <td><p><span data-ttu-id="de161-154">Configurar el nombre de dominio SIP y el FQDN del servidor perimetral asociado como partner de federación en Directivas</span><span class="sxs-lookup"><span data-stu-id="de161-154">Configure the SIP domain name and the partner Edge Server FQDN as a federation partner in Policies</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="de161-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="de161-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="de161-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configurar la compatibilidad con dominios externos permitidos en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="de161-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configure support for allowed external domains in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="de161-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configurar la compatibilidad con dominios externos bloqueados en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="de161-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configure support for blocked external domains in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="de161-158">Este tipo de federación es la definición de una relación uno a uno y no permite la detección de otros partners de federación.</span><span class="sxs-lookup"><span data-stu-id="de161-158">This federation type is the definition of a one to one relationship and does not allow for discovery of other federation partners.</span></span> <span data-ttu-id="de161-159">Cada partner de federación se configura explícitamente.</span><span class="sxs-lookup"><span data-stu-id="de161-159">Each federation partner is configured explicitly.</span></span> <span data-ttu-id="de161-160">En versiones anteriores, esto se conocía como <strong>Federación directa</strong></span><span class="sxs-lookup"><span data-stu-id="de161-160">In previous versions, this was known as <strong>Direct Federation</strong></span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="de161-161">Proveedor de hospedaje y proveedor público de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="de161-161">Hosting Provider and Public IM Provider</span></span></p></td>
    <td><p><span data-ttu-id="de161-162">No se definen requisitos DNS específicos para este tipo de federación</span><span class="sxs-lookup"><span data-stu-id="de161-162">No specific DNS requirements are defined for this type of federation</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="de161-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="de161-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="de161-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Crear o editar proveedores federados de SIP públicos en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="de161-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Create or edit public SIP federated providers in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="de161-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Crear o editar proveedores federados de SIP hospedados en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="de161-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Create or edit hosted SIP federated providers Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="de161-166">Este tipo de federación define los servicios y los proveedores de hospedaje que desea configurar para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="de161-166">This federation type defines services and hosting providers that you want to configure for your users.</span></span> <span data-ttu-id="de161-167">Los usos típicos incluyen la configuración para proveedores de mensajería instantánea públicos como Windows Live Messenger, Yahoo!</span><span class="sxs-lookup"><span data-stu-id="de161-167">Typical uses include configuration for public IM providers like Windows Live Messenger, Yahoo!</span></span> <span data-ttu-id="de161-168">y AOL, así como proveedores de hospedaje como Lync Online y Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="de161-168">and AOL, as well as hosting providers such as Lync Online and Microsoft 365</span></span></p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="de161-169">A partir del 1 de septiembre de 2012, la licencia de suscripción de usuario de conectividad de mensajería instantánea pública de Microsoft Lync ("PIC USL") ya no está disponible para la compra de contratos nuevos o de renovación.</span><span class="sxs-lookup"><span data-stu-id="de161-169">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="de161-170">Los clientes con licencias activas podrán seguir federados con Yahoo!</span><span class="sxs-lookup"><span data-stu-id="de161-170">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="de161-171">Messenger hasta la fecha de cierre del servicio.</span><span class="sxs-lookup"><span data-stu-id="de161-171">Messenger until the service shut down date.</span></span> <span data-ttu-id="de161-172">Una fecha de fin de vida de junio de 2014 para AOL y Yahoo!</span><span class="sxs-lookup"><span data-stu-id="de161-172">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="de161-173">se ha anunciado.</span><span class="sxs-lookup"><span data-stu-id="de161-173">has been announced.</span></span> <span data-ttu-id="de161-174">Para obtener más información, vea <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Soporte para la conectividad de mensajería instantánea pública en Lync Server 2013.</A></span><span class="sxs-lookup"><span data-stu-id="de161-174">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="de161-175">PIC USL es una licencia de suscripción por usuario y mes que se requiere para que Lync Server u Office Communications Server puedan federar con Yahoo!</span><span class="sxs-lookup"><span data-stu-id="de161-175">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="de161-176">Messenger.</span><span class="sxs-lookup"><span data-stu-id="de161-176">Messenger.</span></span> <span data-ttu-id="de161-177">La capacidad de Microsoft para proporcionar este servicio depende del soporte técnico de Yahoo!, cuyo contrato subyacente se está acabando.</span><span class="sxs-lookup"><span data-stu-id="de161-177">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="de161-178">Más que nunca, Lync es una herramienta eficaz para conectarse entre organizaciones y con personas de todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="de161-178">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="de161-179">La federación con Windows Live Messenger no requiere licencias de usuario o dispositivo adicionales más allá de la CAL estándar de Lync.</span><span class="sxs-lookup"><span data-stu-id="de161-179">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="de161-180">La federación de Skype se agregará a esta lista, lo que permitirá a los usuarios de Lync llegar a cientos de millones de personas con mensajería instantánea y voz.</span><span class="sxs-lookup"><span data-stu-id="de161-180">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  <span data-ttu-id="de161-181">Definir y configurar cualquier host DNS necesario (A o AAAA para IPv6) y registros SRV DNS</span><span class="sxs-lookup"><span data-stu-id="de161-181">Define and configure any required DNS host (A or AAAA for IPv6) and DNS SRV records</span></span>

3.  <span data-ttu-id="de161-182">Defina y configure las directivas con el Panel de control de Lync Server o con el Shell de administración de Lync Server y los cmdlets adecuados.</span><span class="sxs-lookup"><span data-stu-id="de161-182">Define and configure any policies using the Lync Server Control Panel or by using the Lync Server Management Shell and the appropriate cmdlets.</span></span> <span data-ttu-id="de161-183">Para obtener más información sobre los cmdlets del Shell de administración de Lync Server, vea Cmdlets de federación y acceso [externo en Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span><span class="sxs-lookup"><span data-stu-id="de161-183">For details on the Lync Server Management Shell cmdlets, see [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="de161-184">Lync Room System (LRS) no muestra el botón unirse a las reuniones enviadas por los organizadores en partners federados de Lync.</span><span class="sxs-lookup"><span data-stu-id="de161-184">Lync Room System (LRS) does not show join button for meetings sent by organizers in federated Lync partners.</span></span> <span data-ttu-id="de161-185">Para que un vínculo de unirse a una reunión aparezca en LRS, la organización de envío debe habilitar TNEF mediante el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="de161-185">For a meeting join link to appear on LRS, the sending organization must enable TNEF by using the following cmdlet:</span></span><BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR><span data-ttu-id="de161-186">Tenga en cuenta que esto no es específico de LRS.</span><span class="sxs-lookup"><span data-stu-id="de161-186">Note that this is not LRS specific.</span></span> <span data-ttu-id="de161-187">Outlook y Lync tampoco mostrarían vínculos de combinación en este caso, ya que las propiedades MAPI no se transportan, pero en el caso de Outlook, el usuario puede abrir la invitación a la reunión y hacer clic en la dirección URL de la reunión.</span><span class="sxs-lookup"><span data-stu-id="de161-187">Outlook and Lync would also not show Join links in this case as MAPI properties are not transported, but in the Outlook case, the user can open up the meeting invite and click on the meeting URL.</span></span> <span data-ttu-id="de161-188">Cuando TNEFEnabled se establece en true Exchange 2013 no quita las propiedades MAPI, incluido OnlineMeetingExternalLink y el botón Unirse se mostrará en el aviso.</span><span class="sxs-lookup"><span data-stu-id="de161-188">When TNEFEnabled is set to true Exchange 2013 does not strip MAPI properties including OnlineMeetingExternalLink and the Join button will be shown on the reminder.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="de161-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="de161-189">See Also</span></span>


[<span data-ttu-id="de161-190">Planeación de sip, federación XMPP y mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de161-190">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[<span data-ttu-id="de161-191">Administración de la federación y el acceso externo a Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de161-191">Managing federation and external access to Lync Server 2013</span></span>](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

<span data-ttu-id="de161-192"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de161-192"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

