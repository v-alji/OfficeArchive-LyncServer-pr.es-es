---
title: 'Lync Server 2013: proceso de implementación para el grupo de respuesta'
description: 'Lync Server 2013: proceso de implementación para el grupo de respuesta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Response Group
ms:assetid: d390c8a1-dc6e-44d8-b386-2be1fca9877c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205270(v=OCS.15)
ms:contentKeyID: 48185437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b50fb7903a2fcc301bbf435013b8f8df4e775a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429660"
---
# <a name="deployment-process-for-response-group-in-lync-server-2013"></a><span data-ttu-id="704fe-103">Proceso de implementación para un grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="704fe-103">Deployment process for Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="704fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="704fe-104">

<span> </span></span></span>

<span data-ttu-id="704fe-105">_**Última modificación del tema:** 2012-09-27_</span><span class="sxs-lookup"><span data-stu-id="704fe-105">_**Topic Last Modified:** 2012-09-27_</span></span>

<span data-ttu-id="704fe-106">Esta sección proporciona una descripción general de las fases y los pasos necesarios para implementar la aplicación de grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="704fe-106">This section provides an overview of the phases and steps involved in deploying the Response Group application.</span></span>

### <a name="response-group-deployment-process"></a><span data-ttu-id="704fe-107">Proceso de implementación de grupos de respuesta</span><span class="sxs-lookup"><span data-stu-id="704fe-107">Response Group Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="704fe-108">Fase</span><span class="sxs-lookup"><span data-stu-id="704fe-108">Phase</span></span></th>
<th><span data-ttu-id="704fe-109">Pasos</span><span class="sxs-lookup"><span data-stu-id="704fe-109">Steps</span></span></th>
<th><span data-ttu-id="704fe-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="704fe-110">Permissions</span></span></th>
<th><span data-ttu-id="704fe-111">Documentación de implementación</span><span class="sxs-lookup"><span data-stu-id="704fe-111">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="704fe-112">Instalar la aplicación de grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="704fe-112">Install the Response Group application</span></span></p></td>
<td><p><span data-ttu-id="704fe-113">La aplicación de grupo de respuesta se instala y activa de forma predeterminada al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="704fe-113">The Response Group application is installed and activated by default when you deploy Enterprise Voice.</span></span></p></td>
<td><p><span data-ttu-id="704fe-114">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="704fe-114">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="704fe-115"><a href="lync-server-2013-deploying-enterprise-voice.md">Implementación de telefonía IP empresarial en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="704fe-115"><a href="lync-server-2013-deploying-enterprise-voice.md">Deploying Enterprise Voice in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="704fe-116">Instalar componentes para grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="704fe-116">Install components for Response Group</span></span></p></td>
<td><p><span data-ttu-id="704fe-117">Los cmdlets de Lync Server, el panel de control de Lync Server, la herramienta de configuración de grupos de respuesta, la consola de inicio de sesión y cierre de sesión de los agentes y el servicio Web cliente de grupo de respuesta se instalan como parte de los servicios Web.</span><span class="sxs-lookup"><span data-stu-id="704fe-117">Lync Server cmdlets, the Lync Server Control Panel, Response Group Configuration Tool, agents' sign-in and sign-out console, and Response Group Client Web service are installed as part of Web Services.</span></span> <span data-ttu-id="704fe-118">Los servicios web se instalan al implementar un grupo de servidores Enterprise Edition o un servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="704fe-118">Web Services is installed when you deploy an Enterprise Edition pool or a Standard Edition server.</span></span></p></td>
<td><p><span data-ttu-id="704fe-119">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="704fe-119">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="704fe-120"><a href="lync-server-2013-deploying-lync-server.md">Implementar Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="704fe-120"><a href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="704fe-121">Habilitar usuarios para Lync 2013 y para telefonía IP empresarial</span><span class="sxs-lookup"><span data-stu-id="704fe-121">Enable users for Lync 2013 and for Enterprise Voice</span></span></p></td>
<td><p><span data-ttu-id="704fe-122">Habilitar usuarios que serán agentes de Lync Server y Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="704fe-122">Enable users who will be agents for Lync Server and Enterprise Voice.</span></span> <span data-ttu-id="704fe-123">Estos usuarios necesitan estar habilitados para agregarlos a grupos de agentes.</span><span class="sxs-lookup"><span data-stu-id="704fe-123">Users must be enabled before you can add them to agent groups.</span></span> <span data-ttu-id="704fe-124">Normalmente, los usuarios están habilitados para Lync Server durante la implementación de servidor Standard Edition o Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="704fe-124">Typically, users are enabled for Lync Server during the Enterprise Edition or Standard Edition server deployment.</span></span> <span data-ttu-id="704fe-125">Los usuarios están habilitados para telefonía IP empresarial durante la implementación de telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="704fe-125">Users are enabled for Enterprise Voice during the Enterprise Voice deployment.</span></span></p></td>
<td><p><span data-ttu-id="704fe-126">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="704fe-126">RTCUniversalUserAdmins</span></span></p>
<p><span data-ttu-id="704fe-127">CsUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-127">CsUserAdministrator</span></span></p>
<p><span data-ttu-id="704fe-128">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-128">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="704fe-129"><a href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">Deshabilitar o volver a habilitar la cuenta de usuario para Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="704fe-129"><a href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">Disable or re-enable user account for Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="704fe-130"><a href="lync-server-2013-enable-users-for-enterprise-voice.md">Habilitar usuarios para telefonía IP empresarial en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="704fe-130"><a href="lync-server-2013-enable-users-for-enterprise-voice.md">Enable users for Enterprise Voice in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="704fe-131">Crear y configurar grupos de respuesta formados por grupos de agentes, colas y flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="704fe-131">Create and configure response groups, which consist of agent groups, queues, and workflows</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="704fe-132">Use el panel de control de Lync Server o el shell de administración de Lync Server para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="704fe-132">Use the Lync Server Control Panel or Lync Server Management Shell to do the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="704fe-133">Crear y configurar grupos de respuesta</span><span class="sxs-lookup"><span data-stu-id="704fe-133">Create and configure agent groups.</span></span></p></li>
<li><p><span data-ttu-id="704fe-134">Crear y configurar colas</span><span class="sxs-lookup"><span data-stu-id="704fe-134">Create and configure queues.</span></span></p></li>
</ol></li>
<li><p><span data-ttu-id="704fe-135">De manera opcional, use el shell de administración de Lync Server para crear vacaciones y días laborables de grupo de respuesta predefinidos.</span><span class="sxs-lookup"><span data-stu-id="704fe-135">Optionally, use Lync Server Management Shell to create predefined response group business hours and holidays.</span></span></p></li>
<li><p><span data-ttu-id="704fe-136">Use la herramienta de configuración de grupos de respuesta o el shell de administración de Lync Server para crear flujos de trabajo (grupos de captura o flujos de llamada de voz interactiva (IVR), incluidos los días laborables y las horas laborables de grupo de respuesta personalizado.</span><span class="sxs-lookup"><span data-stu-id="704fe-136">Use the Response Group Configuration Tool or Lync Server Management Shell to create workflows (hunt groups or interactive voice response (IVR) call flows), including custom response group business hours and holidays.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="704fe-137">Puede acceder a la herramienta de configuración de grupos de respuesta a través del panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="704fe-137">You can access the Response Group Configuration Tool through Lync Server Control Panel.</span></span>


</div></li>
</ol></td>
<td><p><span data-ttu-id="704fe-138">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="704fe-138">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="704fe-139">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-139">CsResponseGroupAdministrator</span></span></p>
<p><span data-ttu-id="704fe-140">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-140">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="704fe-141">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-141">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="704fe-142">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-142">CsAdministrator</span></span></p>
<p><span data-ttu-id="704fe-143">AdministradorGrupoRespuestaCs</span><span class="sxs-lookup"><span data-stu-id="704fe-143">CsResponseGroupManager</span></span></p></td>
<td><p><span data-ttu-id="704fe-144"><a href="lync-server-2013-create-response-group-agent-groups.md">Crear grupos de agentes de grupos de respuesta en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="704fe-144"><a href="lync-server-2013-create-response-group-agent-groups.md">Create Response Group agent groups Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="704fe-145"><a href="lync-server-2013-create-response-group-queues.md">Crear colas de grupo de respuesta en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="704fe-145"><a href="lync-server-2013-create-response-group-queues.md">Create Response Group queues in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="704fe-146"><a href="lync-server-2013-optional-define-response-group-business-hours.md">Faculta Definir las horas de trabajo del grupo de respuesta en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="704fe-146"><a href="lync-server-2013-optional-define-response-group-business-hours.md">(Optional) Define Response Group business hours in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="704fe-147"><a href="lync-server-2013-optional-define-response-group-holiday-sets.md">Faculta Definir conjuntos de días festivos de grupos de respuesta en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="704fe-147"><a href="lync-server-2013-optional-define-response-group-holiday-sets.md">(Optional) Define Response Group holiday sets in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="704fe-148"><a href="lync-server-2013-create-or-modify-a-workflow.md">Crear o modificar un flujo de trabajo en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="704fe-148"><a href="lync-server-2013-create-or-modify-a-workflow.md">Create or modify a workflow in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="704fe-149">(Opcional) Personalizar la configuración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="704fe-149">(Optional) Customize application-level settings</span></span></p></td>
<td><p><span data-ttu-id="704fe-150">Use el shell de administración de Lync Server para personalizar la configuración predeterminada de música en espera, el archivo de audio de música activa predeterminada, el período de gracia de timbre de timbre y la configuración de contexto de llamada.</span><span class="sxs-lookup"><span data-stu-id="704fe-150">Use Lync Server Management Shell to customize the default music-on-hold configuration, the default music-on-hold audio file, the agent ringback grace period, and the call context configuration.</span></span></p></td>
<td><p><span data-ttu-id="704fe-151">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="704fe-151">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="704fe-152">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-152">CsResponseGroupAdministrator</span></span></p>
<p><span data-ttu-id="704fe-153">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-153">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="704fe-154">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-154">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="704fe-155">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-155">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="704fe-156"><a href="lync-server-2013-managing-application-level-response-group-settings.md">Administrar la configuración de grupo de respuesta de nivel de aplicación en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="704fe-156"><a href="lync-server-2013-managing-application-level-response-group-settings.md">Managing application-level Response Group settings in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="704fe-157">(Opcional) Delegar la administración de los grupos de respuesta</span><span class="sxs-lookup"><span data-stu-id="704fe-157">(Optional) Delegate management of response groups</span></span></p></td>
<td><p><span data-ttu-id="704fe-158">Asigne a los usuarios el rol CsResponseGroupManager para delegar la configuración de grupos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="704fe-158">Assign users the CsResponseGroupManager role to delegate configuration of response groups.</span></span> <span data-ttu-id="704fe-159">Los administradores de grupos de respuesta pueden configurar los grupos de respuesta que tienen asignados.</span><span class="sxs-lookup"><span data-stu-id="704fe-159">Response Group Managers can then configure the response groups assigned to them.</span></span></p></td>
<td><p><span data-ttu-id="704fe-160">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="704fe-160">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="704fe-161">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-161">CsResponseGroupAdministrator</span></span></p>
<p><span data-ttu-id="704fe-162">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-162">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="704fe-163">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-163">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="704fe-164">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="704fe-164">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="704fe-165"><a href="lync-server-2013-planning-for-role-based-access-control.md">Planeación del control de acceso basado en roles en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="704fe-165"><a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="704fe-166">Comprobar la implementación del grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="704fe-166">Verify your Response Group deployment</span></span></p></td>
<td><p><span data-ttu-id="704fe-167">Compruebe los mensajes de contestador automático del grupo de búsqueda y los flujos de trabajo de respuestas de voz interactiva para asegurarse de que la configuración funcione según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="704fe-167">Test answering calls to your hunt group and interactive voice response workflows to ensure that your configuration works as expected.</span></span></p></td>
<td><p>-</p></td>
<td><p>-</p></td>
</tr><span data-ttu-id="704fe-168">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="704fe-168">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

