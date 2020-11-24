---
title: Proceso de implementación para integrar la mensajería unificada local
description: Proceso de implementación para integrar la mensajería unificada local.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for integrating on-premises Unified Messaging and Lync Server
ms:assetid: 269a4436-f09f-415b-96ab-49a64370a385
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425737(v=OCS.15)
ms:contentKeyID: 48183664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6c1b8f528edb970893198ed06b821535a398f09d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399593"
---
# <a name="deployment-process-for-integrating-on-premises-unified-messaging-and-lync-server-2013"></a><span data-ttu-id="ff201-103">Proceso de implementación de la integración de la mensajería unificada local y Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff201-103">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ff201-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ff201-104">

<span> </span></span></span>

<span data-ttu-id="ff201-105">_**Última modificación del tema:** 2012-12-17_</span><span class="sxs-lookup"><span data-stu-id="ff201-105">_**Topic Last Modified:** 2012-12-17_</span></span>

<span data-ttu-id="ff201-106">Si desea integrar la mensajería unificada de Exchange (UM) con Lync Server 2013, debe realizar las tareas descritas en este tema.</span><span class="sxs-lookup"><span data-stu-id="ff201-106">If you want to integrate Exchange Unified Messaging (UM) with Lync Server 2013, you must perform the tasks described in this topic.</span></span> <span data-ttu-id="ff201-107">Además, asegúrese de revisar las prácticas recomendadas de planeamiento e implementación descritas en [directrices para integrar la mensajería unificada local y Lync Server 2013](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="ff201-107">Also be sure that you review the planning and deployment best practices described in [Guidelines for integrating on-premises Unified Messaging and Lync Server 2013](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md).</span></span> <span data-ttu-id="ff201-108">En este tema se supone que ha implementado Lync Server 2013 con un servidor de mediación en el que ha habilitado usuarios para Lync Server 2013, pero no necesariamente que haya realizado todos los pasos de implementación y configuración para habilitar la telefonía IP empresarial, como se describe en [implementar la telefonía IP empresarial en Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) , en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="ff201-108">This topic assumes that you have deployed Lync Server 2013 with a collocated Mediation Server and that you have enabled users for Lync Server 2013, but not necessarily that you have performed all deployment and configuration steps to enable Enterprise Voice, as described in [Deploying Enterprise Voice in Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) in the Deployment documentation.</span></span>

<div>

## <a name="unified-messaging-integration-process"></a><span data-ttu-id="ff201-109">Proceso de integración de la mensajería unificada</span><span class="sxs-lookup"><span data-stu-id="ff201-109">Unified Messaging Integration Process</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="ff201-110">Es importante estar coordinado con los administradores de Exchange de la organización para constatar qué tareas va a realizar cada uno a fin de que la integración se realice de forma correcta y sin fisuras.</span><span class="sxs-lookup"><span data-stu-id="ff201-110">It is important that you coordinate with your organization’s Exchange administrators to confirm the tasks that each of you will perform to help ensure a smooth, successful integration.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff201-111">Fase</span><span class="sxs-lookup"><span data-stu-id="ff201-111">Phase</span></span></th>
<th><span data-ttu-id="ff201-112">Pasos</span><span class="sxs-lookup"><span data-stu-id="ff201-112">Steps</span></span></th>
<th><span data-ttu-id="ff201-113">Grupos y roles necesarios</span><span class="sxs-lookup"><span data-stu-id="ff201-113">Required groups and roles</span></span></th>
<th><span data-ttu-id="ff201-114">Documentación de implementación</span><span class="sxs-lookup"><span data-stu-id="ff201-114">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff201-115">Implementar una de las siguientes aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="ff201-115">Deploy one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ff201-116">Microsoft Exchange Server 2007 Service Pack 1 (SP2) o el Service Pack más reciente</span><span class="sxs-lookup"><span data-stu-id="ff201-116">Microsoft Exchange Server 2007 Service Pack 1 (SP2) or latest service pack</span></span></p></li>
<li><p><span data-ttu-id="ff201-117">Microsoft Exchange Server 2010 o Service Pack más reciente</span><span class="sxs-lookup"><span data-stu-id="ff201-117">Microsoft Exchange Server 2010 or latest service pack</span></span></p></li>
<li><p><span data-ttu-id="ff201-118">Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff201-118">Microsoft Exchange Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ff201-119">Si usa Microsoft Exchange Server 2013, instale los siguientes roles de servidor de Exchange en el mismo bosque o en un bosque diferente que Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="ff201-119">If you are using Microsoft Exchange Server 2013, install the following Exchange Server roles in either the same forest or a different forest as Lync Server 2013:</span></span></p>
<ul>
<li><p><span data-ttu-id="ff201-120">Acceso de clientes</span><span class="sxs-lookup"><span data-stu-id="ff201-120">Client Access</span></span></p></li>
<li><p><span data-ttu-id="ff201-121">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="ff201-121">Mailbox</span></span></p></li>
</ul>
<p><span data-ttu-id="ff201-122">Si Microsoft Exchange Server 2013 y mensajería unificada de Exchange se instalan en bosques diferentes, configure cada bosque de Exchange para que confíe en el bosque de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ff201-122">If Microsoft Exchange Server 2013 and Exchange Unified Messaging (UM) are installed in different forests, configure each Exchange forest to trust the Lync Server 2013 forest.</span></span></p>
<p><span data-ttu-id="ff201-123">Si usa Exchange 2010, instale los siguientes roles de servidor de Exchange en el mismo bosque o en un bosque diferente que Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="ff201-123">If you are using Exchange 2010, install the following Exchange Server roles in either the same forest or a different forest as Lync Server 2013:</span></span></p>
<ul>
<li><p><span data-ttu-id="ff201-124">Mensajería unificada</span><span class="sxs-lookup"><span data-stu-id="ff201-124">Unified Messaging</span></span></p></li>
<li><p><span data-ttu-id="ff201-125">Transporte de concentradores</span><span class="sxs-lookup"><span data-stu-id="ff201-125">Hub Transport</span></span></p></li>
<li><p><span data-ttu-id="ff201-126">Acceso de clientes</span><span class="sxs-lookup"><span data-stu-id="ff201-126">Client Access</span></span></p></li>
<li><p><span data-ttu-id="ff201-127">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="ff201-127">Mailbox</span></span></p></li>
</ul>
<p><span data-ttu-id="ff201-128">Si Lync Server 2013 y mensajería unificada de Exchange se instalan en bosques diferentes, configure cada bosque de Exchange para que confíe en el bosque de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ff201-128">If Lync Server 2013 and Exchange Unified Messaging (UM) are installed in different forests, configure each Exchange forest to trust the Lync Server 2013 forest.</span></span></p></td>
<td><p><span data-ttu-id="ff201-129">Administradores de organización (si es el primer servidor de Exchange Server en la organización)</span><span class="sxs-lookup"><span data-stu-id="ff201-129">Enterprise administrators (if this is the first Exchange Server in the organization)</span></span></p>
<p><span data-ttu-id="ff201-130">O BIEN:</span><span class="sxs-lookup"><span data-stu-id="ff201-130">-OR-</span></span></p>
<p><span data-ttu-id="ff201-131">Administrador de organización de Exchange (si no es el primer servidor de Exchange Server en la organización)</span><span class="sxs-lookup"><span data-stu-id="ff201-131">Exchange Organization administrator (if this is not the first Exchange Server in the organization)</span></span></p></td>
<td><p><span data-ttu-id="ff201-132">Consulte la documentación correspondiente a la versión de Exchange Server:</span><span class="sxs-lookup"><span data-stu-id="ff201-132">See the appropriate documentation for your version of Exchange Server:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="ff201-133">Documentación de implementación de Exchange Server 2007 en <a href="https://go.microsoft.com/fwlink/p/?linkid=268694">https://go.microsoft.com/fwlink/p/?LinkId=268694</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-133">Exchange Server 2007 deployment documentation at <a href="https://go.microsoft.com/fwlink/p/?linkid=268694">https://go.microsoft.com/fwlink/p/?LinkId=268694</a>.</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="ff201-134">Exchange Server 2010 o la documentación de implementación del Service Pack más reciente en <a href="https://go.microsoft.com/fwlink/p/?linkid=268695">https://go.microsoft.com/fwlink/p/?LinkId=268695</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-134">Exchange Server 2010 or latest service pack deployment documentation at <a href="https://go.microsoft.com/fwlink/p/?linkid=268695">https://go.microsoft.com/fwlink/p/?LinkId=268695</a>.</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="ff201-135">Microsoft Exchange Server 2013 Planning and Deployment en <a href="https://go.microsoft.com/fwlink/p/?linkid=266569">https://go.microsoft.com/fwlink/p/?LinkId=266569</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-135">Microsoft Exchange Server 2013 Planning and Deployment at <a href="https://go.microsoft.com/fwlink/p/?linkid=266569">https://go.microsoft.com/fwlink/p/?LinkId=266569</a>.</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff201-136">Instalar los certificados.</span><span class="sxs-lookup"><span data-stu-id="ff201-136">Install certificates.</span></span></p></td>
<td><p><span data-ttu-id="ff201-137">Descargue e instale certificados para cada servidor de mensajería unificada de Exchange de una entidad de certificación (CA) raíz de confianza.</span><span class="sxs-lookup"><span data-stu-id="ff201-137">Download and install certificates for each Exchange UM server from a trusted root certificate authority (CA).</span></span> <span data-ttu-id="ff201-138">Los certificados son necesarios para la seguridad del nivel de transporte mutuo (MTLS) entre los servidores que ejecutan la mensajería unificada de Exchange y Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ff201-138">The certificates are required for mutual Transport Level Security (MTLS) between the servers running Exchange UM and Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="ff201-139">Administradores</span><span class="sxs-lookup"><span data-stu-id="ff201-139">Administrators</span></span></p></td>
<td><p><span data-ttu-id="ff201-140"><a href="lync-server-2013-configure-certificates-on-the-server-running-microsoft-exchange-server-unified-messaging.md">Configurar certificados en el servidor que ejecuta la mensajería unificada de Microsoft Exchange Server</a></span><span class="sxs-lookup"><span data-stu-id="ff201-140"><a href="lync-server-2013-configure-certificates-on-the-server-running-microsoft-exchange-server-unified-messaging.md">Configure certificates on the server running Microsoft Exchange Server Unified Messaging</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff201-141">Cree y configure un nuevo plan de marcado SIP de Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="ff201-141">Create and configure a new Exchange UM SIP dial plan.</span></span></p></td>
<td><p><span data-ttu-id="ff201-142">En el servidor de mensajería unificada de Exchange, cree un plan de marcado SIP basado en los requisitos de implementación específicos de su organización.</span><span class="sxs-lookup"><span data-stu-id="ff201-142">On the Exchange UM server, create a SIP dial plan based on your organization’s specific deployment requirements.</span></span></p></td>
<td><p><span data-ttu-id="ff201-143">Administrador de organización de Exchange</span><span class="sxs-lookup"><span data-stu-id="ff201-143">Exchange Organization administrator</span></span></p></td>
<td><p><span data-ttu-id="ff201-144">Para Exchange 2007 SP1 o el Service Pack más reciente, vea &quot; Cómo crear un plan de marcado URI del SIP de mensajería unificada &quot; en <a href="https://go.microsoft.com/fwlink/p/?linkid=268632">https://go.microsoft.com/fwlink/p/?linkId=268632</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-144">For Exchange 2007 SP1 or latest service pack, see &quot;How to Create a Unified Messaging SIP URI Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268632">https://go.microsoft.com/fwlink/p/?linkId=268632</a>.</span></span></p>
<p><span data-ttu-id="ff201-145">Para Exchange 2010 o el Service Pack más reciente, consulte &quot; crear un plan de marcado de MU &quot; en <a href="https://go.microsoft.com/fwlink/p/?linkid=268674">https://go.microsoft.com/fwlink/p/?linkId=268674</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-145">For Exchange 2010 or latest service pack, see &quot;Create a UM Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268674">https://go.microsoft.com/fwlink/p/?linkId=268674</a>.</span></span></p>
<p><span data-ttu-id="ff201-146">Para Exchange 2013, consulte mensajería unificada en <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-146">For Exchange 2013, see Unified Messaging at <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff201-147">Configure las opciones de seguridad para el plan de marcado SIP de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff201-147">Configure security settings for the Exchange UM SIP dial plan.</span></span></p></td>
<td><p><span data-ttu-id="ff201-148">Para cifrar el tráfico de voz empresarial, establezca la configuración de seguridad en el plan de marcado SIP de mensajería unificada de Exchange como <strong>SIP protegido</strong> o <strong>seguro</strong>.</span><span class="sxs-lookup"><span data-stu-id="ff201-148">To encrypt Enterprise Voice traffic, configure the security settings on the Exchange UM SIP dial plan as <strong>SIP Secured</strong> or <strong>Secured</strong>.</span></span> <span data-ttu-id="ff201-149">Este es un paso especialmente importante si ha implementado o tiene previsto implementar dispositivos de Lync Phone Edition en su entorno.</span><span class="sxs-lookup"><span data-stu-id="ff201-149">This is an especially important step if you have deployed or plan to deploy Lync Phone Edition devices in your environment.</span></span> <span data-ttu-id="ff201-150">Para que los dispositivos de Lync Phone Edition funcionen en un entorno con integración de MU de Exchange, la configuración de cifrado de Lync Server debe alinearse con la configuración de seguridad del plan de marcado de MU de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff201-150">For Lync Phone Edition devices to function in an environment with Exchange UM integration, Lync Server encryption settings must align with the Exchange UM dial plan security settings.</span></span> <span data-ttu-id="ff201-151">Para obtener información detallada, consulte la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="ff201-151">For details, refer to the Deployment documentation.</span></span></p></td>
<td><p><span data-ttu-id="ff201-152">Administrador de organización de Exchange</span><span class="sxs-lookup"><span data-stu-id="ff201-152">Exchange Organization administrator</span></span></p></td>
<td><p><span data-ttu-id="ff201-153"><a href="lync-server-2013-configure-unified-messaging-on-microsoft-exchange.md">Configurar la mensajería unificada en Microsoft Exchange para Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="ff201-153"><a href="lync-server-2013-configure-unified-messaging-on-microsoft-exchange.md">Configure Unified Messaging on Microsoft Exchange for Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="ff201-154">Para Exchange 2007 SP1 o el Service Pack más reciente, vea también:</span><span class="sxs-lookup"><span data-stu-id="ff201-154">For Exchange 2007 SP1 or latest service pack, see also:</span></span></p>
<p><span data-ttu-id="ff201-155">&quot;Cómo configurar la seguridad en un plan de marcado de mensajería unificada &quot; en <a href="https://go.microsoft.com/fwlink/p/?linkid=268696">https://go.microsoft.com/fwlink/p/?LinkId=268696</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-155">&quot;How to Configure Security on a Unified Messaging Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268696">https://go.microsoft.com/fwlink/p/?LinkId=268696</a>.</span></span></p>
<p><span data-ttu-id="ff201-156">En el caso de Exchange 2010 o el último service pack, véase también:</span><span class="sxs-lookup"><span data-stu-id="ff201-156">For Exchange 2010 or latest service pack, see also:</span></span></p>
<p><span data-ttu-id="ff201-157">&quot;Configurar la seguridad de VoIP en un plan de marcado de MU &quot; <a href="https://go.microsoft.com/fwlink/p/?linkid=268697">https://go.microsoft.com/fwlink/p/?LinkId=268697</a></span><span class="sxs-lookup"><span data-stu-id="ff201-157">&quot;Configure VoIP Security on a UM Dial Plan&quot; <a href="https://go.microsoft.com/fwlink/p/?linkid=268697">https://go.microsoft.com/fwlink/p/?LinkId=268697</a>.</span></span></p>
<p><span data-ttu-id="ff201-158">Para Exchange 2013, consulte mensajería unificada en <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-158">For Exchange 2013, see Unified Messaging at <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff201-159">Agregue servidores de mensajería unificada al plan de marcado SIP de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff201-159">Add Unified Messaging servers to the Exchange UM SIP dial plan.</span></span></p></td>
<td><p><span data-ttu-id="ff201-160">Para que un servidor de mensajería unificada recién instalado pueda responder y procesar llamadas entrantes, es necesario agregarlo a un plan de marcado de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="ff201-160">To enable a newly installed Unified Messaging server to answer and process incoming calls, you must add the Unified Messaging server to a UM dial plan.</span></span> <span data-ttu-id="ff201-161">En este caso, agregue el servidor al plan de marcado SIP de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff201-161">In this case, add the server to the Exchange UM SIP dial plan.</span></span></p></td>
<td><p><span data-ttu-id="ff201-162">Administradores</span><span class="sxs-lookup"><span data-stu-id="ff201-162">Administrators</span></span></p>
<p><span data-ttu-id="ff201-163">Administradores de Exchange Server</span><span class="sxs-lookup"><span data-stu-id="ff201-163">Exchange Server administrators</span></span></p></td>
<td><p><span data-ttu-id="ff201-164">Para Exchange 2007 SP1 o el Service Pack más reciente, vea &quot; Cómo agregar un servidor de mensajería unificada a un plan &quot; de marcado en <a href="https://go.microsoft.com/fwlink/p/?linkid=268681">https://go.microsoft.com/fwlink/p/?linkId=268681</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-164">For Exchange 2007 SP1 or latest service pack, see &quot;How to Add Unified Messaging Server to a Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268681">https://go.microsoft.com/fwlink/p/?linkId=268681</a>.</span></span></p>
<p><span data-ttu-id="ff201-165">Para Exchange 2010 o el Service Pack más reciente, consulte &quot; ver o configurar las propiedades de un servidor de mensajería unificada &quot; en <a href="https://go.microsoft.com/fwlink/p/?linkid=268682">https://go.microsoft.com/fwlink/p/?linkId=268682</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-165">For Exchange 2010 or latest service pack, see &quot;View or Configure the Properties of a UM Server&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268682">https://go.microsoft.com/fwlink/p/?linkId=268682</a>.</span></span></p>
<p><span data-ttu-id="ff201-166">Para Exchange 2013, consulte mensajería unificada en <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-166">For Exchange 2013, see Unified Messaging at <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff201-167">Configurar buzones de correo con direcciones SIP.</span><span class="sxs-lookup"><span data-stu-id="ff201-167">Configure mailboxes with SIP addresses.</span></span></p></td>
<td><p><span data-ttu-id="ff201-168">Asigne direcciones SIP a los buzones de usuarios de telefonía IP que usarán las características de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff201-168">Assign SIP addresses to the mailboxes of Enterprise Voice users who will be using Exchange UM features.</span></span></p></td>
<td><p><span data-ttu-id="ff201-169">Administrador de 2013 de Lync Server</span><span class="sxs-lookup"><span data-stu-id="ff201-169">Lync Server 2013 administrator</span></span></p>
<p><span data-ttu-id="ff201-170">Administrador de destinatarios de Exchange</span><span class="sxs-lookup"><span data-stu-id="ff201-170">Exchange Recipient administrator</span></span></p></td>
<td><p><span data-ttu-id="ff201-171">Para Exchange 2007 SP1 o el Service Pack más reciente, vea &quot; Cómo agregar, quitar o modificar una dirección SIP para un usuario UM-Enabled &quot; en <a href="https://go.microsoft.com/fwlink/p/?linkid=268698">https://go.microsoft.com/fwlink/p/?LinkId=268698</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-171">For Exchange 2007 SP1 or latest service pack, see &quot;How to Add, Remove, or Modify a SIP Address for a UM-Enabled User&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268698">https://go.microsoft.com/fwlink/p/?LinkId=268698</a>.</span></span></p>
<p><span data-ttu-id="ff201-172">Para Exchange 2010 o el Service Pack más reciente, vea &quot; modificar una dirección SIP para un usuario UM-Enabled &quot; en <a href="https://go.microsoft.com/fwlink/p/?linkid=268699">https://go.microsoft.com/fwlink/p/?LinkId=268699</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-172">For Exchange 2010 or latest service pack, see &quot;Modify a SIP Address for a UM-Enabled User&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268699">https://go.microsoft.com/fwlink/p/?LinkId=268699</a>.</span></span></p>
<p><span data-ttu-id="ff201-173">Para Exchange 2013, consulte mensajería unificada en <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-173">For Exchange 2013, see Unified Messaging at <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff201-174">Ejecutar el script exchucutil.ps1.</span><span class="sxs-lookup"><span data-stu-id="ff201-174">Run the exchucutil.ps1 script.</span></span></p></td>
<td><p><span data-ttu-id="ff201-175">En el servidor que ejecuta los servicios de mensajería unificada de Exchange, abra el shell de administración de Exchange y ejecute el exchucutil.ps1 script, que hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ff201-175">On the server running Exchange UM services, open the Exchange Management Shell and run the exchucutil.ps1 script, which does the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ff201-176">Concede el permiso de Lync Server 2013 para leer objetos de servicios de dominio de Active Directory UM de Exchange, específicamente, los planes de marcado SIP creados en la tarea anterior.</span><span class="sxs-lookup"><span data-stu-id="ff201-176">Grants Lync Server 2013 permission to read Exchange UM Active Directory Domain Services objects, specifically, the SIP dial plans created in the previous task.</span></span></p></li>
<li><p><span data-ttu-id="ff201-177">Crea un objeto de puerta de enlace IP de mensajería unificada en Active Directory para cada grupo de servidores de Lync Server 2013 Enterprise Edition o servidor Standard Edition que hospeda usuarios que están habilitados para telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="ff201-177">Creates a Unified Messaging IP gateway object in Active Directory for each Lync Server 2013 Enterprise Edition pool or Standard Edition server that hosts users who are enabled for Enterprise Voice.</span></span></p></li>
<li><p><span data-ttu-id="ff201-178">Crea un grupo de captura de mensajería unificada de Exchange para cada puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="ff201-178">Creates an Exchange UM hunt group for each gateway.</span></span> <span data-ttu-id="ff201-179">El identificador piloto del grupo de extensiones será el nombre del plan de marcado asociado a la puerta de enlace correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ff201-179">The hunt group pilot identifier will be the name of the dial plan that is associated with the corresponding gateway.</span></span> <span data-ttu-id="ff201-180">Es necesario establecer una asignación 1:1 si existe más de un plan de marcado.</span><span class="sxs-lookup"><span data-stu-id="ff201-180">These need to be mapped 1:1 if there is more than one dial plan.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ff201-181">Administrador de organización de Exchange</span><span class="sxs-lookup"><span data-stu-id="ff201-181">Exchange Organization administrator</span></span></p>
<p><span data-ttu-id="ff201-182">Administrador de destinatarios de Exchange</span><span class="sxs-lookup"><span data-stu-id="ff201-182">Exchange Recipient administrator</span></span></p></td>
<td><p><span data-ttu-id="ff201-183"><a href="lync-server-2013-configure-unified-messaging-on-microsoft-exchange.md">Configurar la mensajería unificada en Microsoft Exchange para Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="ff201-183"><a href="lync-server-2013-configure-unified-messaging-on-microsoft-exchange.md">Configure Unified Messaging on Microsoft Exchange for Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff201-184">Configure los planes de marcado de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ff201-184">Configure Lync Server 2013 dial plans.</span></span></p></td>
<td><p><span data-ttu-id="ff201-185">Si está integrando con Exchange 2007 SP1 o el Service Pack más reciente o Exchange 2010, cree un nuevo plan de marcado de voz empresarial con un nombre que coincida con el nombre de dominio completo del plan de marcado de Exchange UM (FQDN).</span><span class="sxs-lookup"><span data-stu-id="ff201-185">If you are integrating with Exchange 2007 SP1 or latest service pack, or Exchange 2010, create a new Enterprise Voice dial plan with a name that matches the Exchange UM dial plan fully qualified domain name (FQDN).</span></span></p>



> [!NOTE]
> <span data-ttu-id="ff201-186">Deberá hacer esto para cada plan de marcado de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="ff201-186">You will need to do this for each UM Dial plan.</span></span>


<p><span data-ttu-id="ff201-187">Si está integrando con el SP1 de Exchange 2010, asegúrese de que los planes de marcado de voz empresariales de nivel global/sitio o de grupo se hayan configurado de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="ff201-187">If you are integrating with Exchange 2010 SP1, ensure that suitable global/site-level or pool-level Enterprise Voice dial plans have been configured.</span></span></p>



> [!NOTE]
> <span data-ttu-id="ff201-188">Si está integrando con Exchange 2010 SP1, no es necesario que coincidan los nombres del plan de marcado de Lync Server y del plan de marcado SIP de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff201-188">If you are integrating with Exchange 2010 SP1, the Lync Server dial plan and Exchange UM SIP dial plan names do not need to match.</span></span>

</td>
<td><p><span data-ttu-id="ff201-189">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="ff201-189">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="ff201-190"><a href="lync-server-2013-configuring-dial-plans.md">Configurar planes de marcado en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="ff201-190"><a href="lync-server-2013-configuring-dial-plans.md">Configuring dial plans in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff201-191">Ejecute la herramienta de integración de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff201-191">Run the Exchange UM Integration tool.</span></span></p></td>
<td><p><span data-ttu-id="ff201-192">En Lync Server 2013, ejecute <strong>ocsumutil.exe</strong>, que:</span><span class="sxs-lookup"><span data-stu-id="ff201-192">On the Lync Server 2013, run <strong>ocsumutil.exe</strong>, which:</span></span></p>
<ul>
<li><p><span data-ttu-id="ff201-193">Crea los objetos de contacto de acceso de suscriptor y operador automático.</span><span class="sxs-lookup"><span data-stu-id="ff201-193">Creates Subscriber Access and Auto Attendant contact objects.</span></span></p></li>
<li><p><span data-ttu-id="ff201-194">Valida que haya un plan de marcado de voz de empresa con un nombre que coincida con el FQDN del plan de marcado de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff201-194">Validates that there is an Enterprise Voice dial plan with a name that matches the Exchange UM dial plan FQDN.</span></span> <span data-ttu-id="ff201-195">Si está ejecutando Exchange 2010 SP1 o posterior, no es necesario que los nombres del plan de marcado coincidan y puede ignorar la advertencia de la herramienta sobre este.</span><span class="sxs-lookup"><span data-stu-id="ff201-195">If you are running Exchange 2010 SP1 or later, the dial plan names do not need to match, and you can ignore the tool’s warning about this.</span></span></p></li>
</ul>
<p><span data-ttu-id="ff201-196">Esta herramienta explora la configuración de mensajería unificada de Active Directory para Exchange y permite que el administrador de 2013 de Lync Server vea, cree y edite objetos de contacto.</span><span class="sxs-lookup"><span data-stu-id="ff201-196">This tool works by scanning the Active Directory for Exchange UM settings and allowing the Lync Server 2013 administrator to view, create, and edit contact objects.</span></span></p></td>
<td><p><span data-ttu-id="ff201-197">RTCUniversalServerAdmins <em>y</em> RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="ff201-197">RTCUniversalServerAdmins <em>and</em> RTCUniversalUserAdmins</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="ff201-198">Para ejecutar ocsumutil.exe correctamente, el usuario debe pertenecer a ambos grupos.</span><span class="sxs-lookup"><span data-stu-id="ff201-198">To run ocsumutil.exe successfully, the user must belong to both of these groups.</span></span>





> [!NOTE]
> <span data-ttu-id="ff201-199">Para crear objetos de contacto, el usuario que ejecute ocsumutil.exe necesita tener el permiso adecuado en la unidad organizativa de Active Directory donde están almacenados los nuevos objetos contacto.</span><span class="sxs-lookup"><span data-stu-id="ff201-199">To create Contact objects, the user who runs ocsumutil.exe must have the correct permission to the Active Directory organizational unit (OU) where the new contact objects are stored.</span></span> <span data-ttu-id="ff201-200">Este permiso se puede conceder si se ejecuta el cmdlet <STRONG>Grant-CsOUPermission</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ff201-200">This permission can be granted by running the <STRONG>Grant-CsOUPermission</STRONG> cmdlet.</span></span> <span data-ttu-id="ff201-201">Para obtener más información, consulte la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ff201-201">For details, see the Lync Server Management Shell documentation.</span></span>

</td>
<td><p><span data-ttu-id="ff201-202"><a href="lync-server-2013-configure-lync-server-2013-to-work-with-unified-messaging-on-microsoft-exchange-server.md">Configurar Lync Server 2013 para trabajar con la mensajería unificada en Microsoft Exchange Server</a></span><span class="sxs-lookup"><span data-stu-id="ff201-202"><a href="lync-server-2013-configure-lync-server-2013-to-work-with-unified-messaging-on-microsoft-exchange-server.md">Configure Lync Server 2013 to work with Unified Messaging on Microsoft Exchange Server</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff201-203">Si es necesario, realice otros pasos de configuración de voz empresarial.</span><span class="sxs-lookup"><span data-stu-id="ff201-203">If necessary, perform other Enterprise Voice configuration steps.</span></span></p></td>
<td><p><span data-ttu-id="ff201-204">Si aún no ha configurado la configuración de voz de empresa en sus servidores o usuarios, siga uno o varios de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="ff201-204">If you have not already configured Enterprise Voice settings on your servers or users, do one or more of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ff201-205">Implementar y configurar</span><span class="sxs-lookup"><span data-stu-id="ff201-205">Deploy and configure</span></span></p>
<p><span data-ttu-id="ff201-206">puertas de enlace de red telefónica conmutada (RTC) y servidores de mediación.</span><span class="sxs-lookup"><span data-stu-id="ff201-206">Public switched telephone network (PSTN) gateways and Mediation Servers</span></span></p></li>
<li><p><span data-ttu-id="ff201-207">Definir directivas de voz, registros de uso de RTC y rutas de llamadas realizadas.</span><span class="sxs-lookup"><span data-stu-id="ff201-207">Define voice policies, PSTN usage records, and outbound call routes.</span></span></p></li>
<li><p><span data-ttu-id="ff201-208">Habilitar a los usuarios para Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="ff201-208">Enable users for Enterprise Voice.</span></span></p></li>
<li><p><span data-ttu-id="ff201-209">De forma alternativa, configurar usuarios específicos con planes de marcado.</span><span class="sxs-lookup"><span data-stu-id="ff201-209">Optionally, configure specific users with dial plans.</span></span></p></li>
</ul>
<p><span data-ttu-id="ff201-210">Puede que se requieran otros pasos de configuración según las características de Enterprise Voice que habilite.</span><span class="sxs-lookup"><span data-stu-id="ff201-210">Other configuration steps may be required depending on the Enterprise Voice features that you enable.</span></span></p></td>
<td><p><span data-ttu-id="ff201-211">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="ff201-211">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="ff201-212">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="ff201-212">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="ff201-213">Consulte los temas de las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="ff201-213">See topics in the following sections:</span></span></p>
<ul>
<li><p><span data-ttu-id="ff201-214"><a href="lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md">Configuración de directivas de voz, registros de uso de RTC y rutas de voz en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="ff201-214"><a href="lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md">Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013</a></span></span></p></li>
<li><p><span data-ttu-id="ff201-215"><a href="lync-server-2013-deploying-enterprise-voice.md">Implementación de telefonía IP empresarial en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="ff201-215"><a href="lync-server-2013-deploying-enterprise-voice.md">Deploying Enterprise Voice in Lync Server 2013</a></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff201-216">Habilite los usuarios de telefonía IP empresarial para la mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff201-216">Enable Enterprise Voice users for Exchange UM.</span></span></p></td>
<td><p><span data-ttu-id="ff201-217">En el servidor de mensajería unificada de Exchange, asegúrese de que se ha creado una directiva de buzón de mensajería unificada y de que cada usuario tiene una asignación de número de extensión única y, después, habilite al usuario para la mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="ff201-217">On the Exchange UM server, ensure that a Unified Messaging mailbox policy has been created and that each user has a unique extension number assignment, and then enable the user for Unified Messaging.</span></span></p></td>
<td><p><span data-ttu-id="ff201-218">Administrador de destinatarios de Exchange</span><span class="sxs-lookup"><span data-stu-id="ff201-218">Exchange Recipient administrator</span></span></p></td>
<td><p><span data-ttu-id="ff201-219">Para Exchange 2007 SP1 o el Service Pack más reciente, vea &quot; Cómo habilitar un usuario para mensajería unificada &quot; en <a href="https://go.microsoft.com/fwlink/p/?linkid=268700">https://go.microsoft.com/fwlink/p/?LinkId=268700</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-219">For Exchange 2007 SP1 or latest service pack, see &quot;How to Enable a User for Unified Messaging&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268700">https://go.microsoft.com/fwlink/p/?LinkId=268700</a>.</span></span></p>
<p><span data-ttu-id="ff201-220">Para Exchange 2010 o el Service Pack más reciente, vea &quot; habilitar un usuario para mensajería unificada &quot; en <a href="https://go.microsoft.com/fwlink/p/?linkid=268701">https://go.microsoft.com/fwlink/p/?LinkId=268701</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-220">For Exchange 2010 or latest service pack, see &quot;Enable a User for Unified Messaging&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=268701">https://go.microsoft.com/fwlink/p/?LinkId=268701</a>.</span></span></p>
<p><span data-ttu-id="ff201-221">Para Exchange 2013, consulte mensajería unificada en <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a> .</span><span class="sxs-lookup"><span data-stu-id="ff201-221">For Exchange 2013, see Unified Messaging at <a href="https://go.microsoft.com/fwlink/p/?linkid=266579">https://go.microsoft.com/fwlink/p/?LinkId=266579</a>.</span></span></p></td>
</tr><span data-ttu-id="ff201-222">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ff201-222">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

