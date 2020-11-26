---
title: 'Lync Server 2013: Permisos y requisitos previos de configuración de grupos de respuesta'
description: 'Lync Server 2013: permisos y requisitos previos de configuración del grupo de respuesta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response Group configuration permissions and prerequisites
ms:assetid: 4266f16a-b387-452c-a8ca-d771a3c58f0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204840(v=OCS.15)
ms:contentKeyID: 48183972
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7a0548c1d8886eb7741d1a31b24b480c1a2d30f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436317"
---
# <a name="response-group-configuration-permissions-and-prerequisites-in-lync-server-2013"></a><span data-ttu-id="d6395-103">Permisos y requisitos previos de configuración de grupos de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6395-103">Response Group configuration permissions and prerequisites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d6395-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d6395-104">

<span> </span></span></span>

<span data-ttu-id="d6395-105">_**Última modificación del tema:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="d6395-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="d6395-106">El grupo de respuesta es una característica de administración de llamadas de voz de empresa.</span><span class="sxs-lookup"><span data-stu-id="d6395-106">Response Group is an Enterprise Voice call management feature.</span></span> <span data-ttu-id="d6395-107">En este tema se describe lo que debe tener en cuenta antes de poder configurar el grupo de respuesta y las credenciales administrativas y los permisos que necesita para realizar las tareas de configuración.</span><span class="sxs-lookup"><span data-stu-id="d6395-107">This topic describes what you need to have in place before you can configure Response Group and the administrative credentials and permissions you need to perform configuration tasks.</span></span>

<span data-ttu-id="d6395-108">En esta sección se presupone que ha leído la documentación de planificación relacionada con el grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6395-108">This section assumes that you have read the planning documentation related to Response Group.</span></span> <span data-ttu-id="d6395-109">Para obtener más información, consulte [planear las características de administración de llamadas en Lync Server 2013](lync-server-2013-planning-for-call-management-features.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="d6395-109">For details, see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md) in the Planning documentation.</span></span>

<div>

## <a name="configuration-tools-and-administrative-roles"></a><span data-ttu-id="d6395-110">Herramientas de configuración y roles administrativos</span><span class="sxs-lookup"><span data-stu-id="d6395-110">Configuration Tools and Administrative Roles</span></span>

<span data-ttu-id="d6395-111">Puede usar las siguientes herramientas administrativas para configurar el grupo de respuesta:</span><span class="sxs-lookup"><span data-stu-id="d6395-111">You can use the following administrative tools to configure Response Group:</span></span>

  - <span data-ttu-id="d6395-112">Panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="d6395-112">Lync Server Control Panel</span></span>

  - <span data-ttu-id="d6395-113">Herramienta de configuración de grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="d6395-113">Response Group Configuration Tool</span></span>

  - <span data-ttu-id="d6395-114">Shell de administración de Communications Server</span><span class="sxs-lookup"><span data-stu-id="d6395-114">Lync Server Management Shell</span></span>

<span data-ttu-id="d6395-115">Para configurar el grupo de respuesta, debe ser un miembro de al menos uno de los siguientes roles administrativos:</span><span class="sxs-lookup"><span data-stu-id="d6395-115">To configure response groups, you must be a member of at least one of the following administrative roles:</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6395-116"><strong>Grupo de seguridad de Active Directory (1)</strong></span><span class="sxs-lookup"><span data-stu-id="d6395-116"><strong>Active Directory Security Group (1)</strong></span></span></p></td>
<td><p><span data-ttu-id="d6395-117">Crear flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d6395-117">Create Workflow</span></span></p></td>
<td><p><span data-ttu-id="d6395-118">Asignar administrador</span><span class="sxs-lookup"><span data-stu-id="d6395-118">Assign Manager</span></span></p></td>
<td><p><span data-ttu-id="d6395-119">Crear/asignar agentes, colas</span><span class="sxs-lookup"><span data-stu-id="d6395-119">Create /assign agents, queues</span></span></p></td>
<td><p><span data-ttu-id="d6395-120">Crear/administrar vacaciones y horas laborales</span><span class="sxs-lookup"><span data-stu-id="d6395-120">Create / manage holiday and business hours</span></span></p></td>
<td><p><span data-ttu-id="d6395-121">Activar/desactivar flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d6395-121">Activate / deactivate workflow</span></span></p></td>
<td><p><span data-ttu-id="d6395-122">Configurar flujo de trabajo (IVR o grupo de extensiones)</span><span class="sxs-lookup"><span data-stu-id="d6395-122">Configure workflow (IVR or Hunt Group)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6395-123"><strong>CsResponseGroupAdministrator</strong></span><span class="sxs-lookup"><span data-stu-id="d6395-123"><strong>CsResponseGroupAdministrator</strong></span></span></p></td>
<td><p><span data-ttu-id="d6395-124">√</span><span class="sxs-lookup"><span data-stu-id="d6395-124">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-125">√</span><span class="sxs-lookup"><span data-stu-id="d6395-125">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-126">√</span><span class="sxs-lookup"><span data-stu-id="d6395-126">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-127">√</span><span class="sxs-lookup"><span data-stu-id="d6395-127">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-128">√</span><span class="sxs-lookup"><span data-stu-id="d6395-128">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-129">√</span><span class="sxs-lookup"><span data-stu-id="d6395-129">√</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6395-130"><strong>CsResponseGroupManager</strong></span><span class="sxs-lookup"><span data-stu-id="d6395-130"><strong>CsResponseGroupManager</strong></span></span></p></td>
<td> </td>
<td><p><span data-ttu-id="d6395-131">√(2)</span><span class="sxs-lookup"><span data-stu-id="d6395-131">√(2)</span></span></p></td>
<td><p><span data-ttu-id="d6395-132">√(3)</span><span class="sxs-lookup"><span data-stu-id="d6395-132">√(3)</span></span></p></td>
<td><p><span data-ttu-id="d6395-133">√(3)</span><span class="sxs-lookup"><span data-stu-id="d6395-133">√(3)</span></span></p></td>
<td><p><span data-ttu-id="d6395-134">√(3)</span><span class="sxs-lookup"><span data-stu-id="d6395-134">√(3)</span></span></p></td>
<td><p><span data-ttu-id="d6395-135">√(3)</span><span class="sxs-lookup"><span data-stu-id="d6395-135">√(3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6395-136"><strong>CsVoiceAdministrator</strong></span><span class="sxs-lookup"><span data-stu-id="d6395-136"><strong>CsVoiceAdministrator</strong></span></span></p></td>
<td><p><span data-ttu-id="d6395-137">√</span><span class="sxs-lookup"><span data-stu-id="d6395-137">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-138">√</span><span class="sxs-lookup"><span data-stu-id="d6395-138">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-139">√</span><span class="sxs-lookup"><span data-stu-id="d6395-139">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-140">√</span><span class="sxs-lookup"><span data-stu-id="d6395-140">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-141">√</span><span class="sxs-lookup"><span data-stu-id="d6395-141">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-142">√</span><span class="sxs-lookup"><span data-stu-id="d6395-142">√</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6395-143"><strong>CsServerAdministrator</strong></span><span class="sxs-lookup"><span data-stu-id="d6395-143"><strong>CsServerAdministrator</strong></span></span></p></td>
<td><p><span data-ttu-id="d6395-144">√</span><span class="sxs-lookup"><span data-stu-id="d6395-144">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-145">√</span><span class="sxs-lookup"><span data-stu-id="d6395-145">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-146">√</span><span class="sxs-lookup"><span data-stu-id="d6395-146">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-147">√</span><span class="sxs-lookup"><span data-stu-id="d6395-147">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-148">√</span><span class="sxs-lookup"><span data-stu-id="d6395-148">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-149">√</span><span class="sxs-lookup"><span data-stu-id="d6395-149">√</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6395-150"><strong>CsAdministrator</strong></span><span class="sxs-lookup"><span data-stu-id="d6395-150"><strong>CsAdministrator</strong></span></span></p></td>
<td><p><span data-ttu-id="d6395-151">√</span><span class="sxs-lookup"><span data-stu-id="d6395-151">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-152">√</span><span class="sxs-lookup"><span data-stu-id="d6395-152">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-153">√</span><span class="sxs-lookup"><span data-stu-id="d6395-153">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-154">√</span><span class="sxs-lookup"><span data-stu-id="d6395-154">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-155">√</span><span class="sxs-lookup"><span data-stu-id="d6395-155">√</span></span></p></td>
<td><p><span data-ttu-id="d6395-156">√</span><span class="sxs-lookup"><span data-stu-id="d6395-156">√</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6395-157"><strong>CsViewOnlyAdministrator</strong></span><span class="sxs-lookup"><span data-stu-id="d6395-157"><strong>CsViewOnlyAdministrator</strong></span></span></p></td>
<td><p><span data-ttu-id="d6395-158">√(4)</span><span class="sxs-lookup"><span data-stu-id="d6395-158">√(4)</span></span></p></td>
<td><p><span data-ttu-id="d6395-159">√(4)</span><span class="sxs-lookup"><span data-stu-id="d6395-159">√(4)</span></span></p></td>
<td><p><span data-ttu-id="d6395-160">√(4)</span><span class="sxs-lookup"><span data-stu-id="d6395-160">√(4)</span></span></p></td>
<td><p><span data-ttu-id="d6395-161">√(4)</span><span class="sxs-lookup"><span data-stu-id="d6395-161">√(4)</span></span></p></td>
<td><p><span data-ttu-id="d6395-162">√(4)</span><span class="sxs-lookup"><span data-stu-id="d6395-162">√(4)</span></span></p></td>
<td><p><span data-ttu-id="d6395-163">√(4)</span><span class="sxs-lookup"><span data-stu-id="d6395-163">√(4)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="d6395-164"><STRONG>(1)</STRONG> un objeto de usuario de los servicios de dominio de Active Directory debe ser miembro del grupo de seguridad de Active Directory especificado de la lista.</span><span class="sxs-lookup"><span data-stu-id="d6395-164"><STRONG>(1)</STRONG> An Active Directory Domain Services user object must be a member of the specified Active Directory security group listed.</span></span> <span data-ttu-id="d6395-165">Un administrador u otro miembro delegado de un grupo de Active Directory con los permisos adecuados para agregar usuarios a un grupo de seguridad (por ejemplo, administrador, operadores de cuenta) debe agregar un objeto de usuario al grupo o grupo de seguridad de la lista para que el usuario pueda realizar las funciones de la lista.</span><span class="sxs-lookup"><span data-stu-id="d6395-165">An administrator or other delegated Active Directory group member with appropriate permissions to add users to a security group (For example, Administrator, Account Operators) must add a user object to the listed security group or group for the user to be able to perform the functions listed.</span></span> <span data-ttu-id="d6395-166"><STRONG>(2)</STRONG> solo para los flujos de trabajo que ha asignado el CsResponseGroupAdministrator a la CsResponseGroupManager.</span><span class="sxs-lookup"><span data-stu-id="d6395-166"><STRONG>(2)</STRONG> Only for workflows that the CsResponseGroupAdministrator has assigned to the CsResponseGroupManager.</span></span> <span data-ttu-id="d6395-167"><STRONG>(3)</STRONG> un administrador de grupo de respuesta puede asignar otro miembro de CsResponseGroupManager a un flujo de trabajo que el administrador actual ya administra.</span><span class="sxs-lookup"><span data-stu-id="d6395-167"><STRONG>(3)</STRONG> A Response Group Manager can assign another member of CsResponseGroupManager to a workflow that the current manager already manages.</span></span> <span data-ttu-id="d6395-168"><STRONG>(4)</STRONG> CsViewOnlyAdministrator solo puede ejecutar verbos de Shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d6395-168"><STRONG>(4)</STRONG> CsViewOnlyAdministrator can only run verb "Get" Lync Server Management Shell cmdlets.</span></span>



</div>

</div>

<div>

## <a name="response-group-configuration-prerequisites"></a><span data-ttu-id="d6395-169">Requisitos previos de configuración del grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="d6395-169">Response Group Configuration Prerequisites</span></span>

<span data-ttu-id="d6395-170">El grupo de respuesta requiere los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="d6395-170">Response Group requires the following components:</span></span>

  - <span data-ttu-id="d6395-171">Servicio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d6395-171">Application service</span></span>

  - <span data-ttu-id="d6395-172">Aplicación de grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="d6395-172">Response Group application</span></span>

  - <span data-ttu-id="d6395-173">Paquetes de idioma</span><span class="sxs-lookup"><span data-stu-id="d6395-173">Language packs</span></span>

  - <span data-ttu-id="d6395-174">Almacén de archivos (para contener los archivos de audio)</span><span class="sxs-lookup"><span data-stu-id="d6395-174">File store (to hold audio files)</span></span>

  - <span data-ttu-id="d6395-175">Servicios web (incluye la herramienta de configuración de grupos de respuesta y la consola de inicio de sesión y cierre de sesión de los agentes)</span><span class="sxs-lookup"><span data-stu-id="d6395-175">Web Services (includes the Response Group Configuration Tool and the agents' sign-in and sign-out console)</span></span>

<span data-ttu-id="d6395-176">Todos estos componentes se instalan de forma predeterminada al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="d6395-176">All of these components are installed by default when you deploy Enterprise Voice.</span></span>

<span data-ttu-id="d6395-177">Es posible que tenga que realizar las siguientes tareas antes de configurar el grupo de respuesta:</span><span class="sxs-lookup"><span data-stu-id="d6395-177">You might need to perform the following tasks before configuring Response Group:</span></span>

  - <span data-ttu-id="d6395-178">Habilitar usuarios para Lync Server 2013 y Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="d6395-178">Enable users for Lync Server 2013 and Enterprise Voice.</span></span>

  - <span data-ttu-id="d6395-179">Modificar un archivo de configuración para que sea compatible con estándares federales de procesamiento de información (FIPS).</span><span class="sxs-lookup"><span data-stu-id="d6395-179">Modify a configuration file to be compliant with Federal Information Processing Standards (FIPS).</span></span>

  - <span data-ttu-id="d6395-180">Modificar la intercalación de base de datos para admitir caracteres Yi, Meng y Zang para nombres de cola y los nombres de grupo de agente.</span><span class="sxs-lookup"><span data-stu-id="d6395-180">Modify the database collation to support Yi, Meng, and Zang characters for queue names and agent group names.</span></span>

<div>

## <a name="enabling-users"></a><span data-ttu-id="d6395-181">Habilitar a los usuarios</span><span class="sxs-lookup"><span data-stu-id="d6395-181">Enabling Users</span></span>

<span data-ttu-id="d6395-182">El primer paso para configurar el grupo de respuesta es crear grupos de agentes.</span><span class="sxs-lookup"><span data-stu-id="d6395-182">The first step in configuring Response Group is to create agent groups.</span></span> <span data-ttu-id="d6395-183">Antes de crear un grupo de agentes, debe habilitar los usuarios que serán agentes para el grupo de respuesta para Lync Server 2013 y Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="d6395-183">Before you can create an agent group, you must enable the users who will be agents for Response Group for Lync Server 2013 and Enterprise Voice.</span></span> <span data-ttu-id="d6395-184">Habilitar usuarios para Lync Server 2013 suele ser un paso de la implementación del servidor Enterprise Edition o del servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d6395-184">Enabling users for Lync Server 2013 is typically a step in the Enterprise Edition server or Standard Edition server deployment.</span></span> <span data-ttu-id="d6395-185">Para obtener más información sobre cómo habilitar usuarios para Lync Server 2013, vea [deshabilitar o volver a habilitar la cuenta de usuario para Lync server 2013](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="d6395-185">For details about enabling users for Lync Server 2013, see [Disable or re-enable user account for Lync Server 2013](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md).</span></span> <span data-ttu-id="d6395-186">Habilitar a los usuarios para Enterprise Voice suele ser un paso en la implementación de telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="d6395-186">Enabling users for Enterprise Voice is typically a step in the Enterprise Voice deployment.</span></span> <span data-ttu-id="d6395-187">Para obtener más información, consulte [Habilitar usuarios para telefonía IP empresarial en Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span><span class="sxs-lookup"><span data-stu-id="d6395-187">For details, see [Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span></span>

</div>

<div>

## <a name="complying-with-fips-requirements"></a><span data-ttu-id="d6395-188">Cumplir con los requisitos de FIPS</span><span class="sxs-lookup"><span data-stu-id="d6395-188">Complying with FIPS requirements</span></span>

<span data-ttu-id="d6395-189">Esta sección se le aplica solo si su organización necesita cumplir con estándares federales de procesamiento de información (FIPS).</span><span class="sxs-lookup"><span data-stu-id="d6395-189">This section applies to you only if your organization needs to comply with Federal Information Processing Standards (FIPS).</span></span>

<span data-ttu-id="d6395-190">Para cumplir los FIPS, debe modificar el archivo Web.config del nivel de aplicación para usar otro algoritmo de criptografía diferente después de instalar los servicios web.</span><span class="sxs-lookup"><span data-stu-id="d6395-190">To be compliant with FIPS, you need to modify the application-level Web.config file to use a different cryptography algorithm after you install Web Services.</span></span> <span data-ttu-id="d6395-191">Debe especificar que ASP.NET use el algoritmo 3DES (Triple Data Encryption Standard) para procesar los datos de ver estado.</span><span class="sxs-lookup"><span data-stu-id="d6395-191">You need to specify that ASP.NET use the Triple Data Encryption Standard (3DES) algorithm to process view state data.</span></span> <span data-ttu-id="d6395-192">Para la aplicación de grupo de respuesta, este requisito se aplica a la herramienta de configuración de grupos de respuesta y a la consola de inicio de sesión y de inicio de sesión del agente.</span><span class="sxs-lookup"><span data-stu-id="d6395-192">For the Response Group application, this requirement applies to the Response Group Configuration Tool and the agent sign-in and sign-out console.</span></span> <span data-ttu-id="d6395-193">Para obtener más información sobre este requisito, consulte el artículo 911722 de Microsoft Knowledge base, "puede recibir un mensaje de error al obtener acceso a ASP.NET páginas web que tengan habilitado ViewState después de la actualización de ASP.NET 1,1 a ASP.NET 2,0," en [https://go.microsoft.com/fwlink/p/?linkId=196183](https://go.microsoft.com/fwlink/p/?linkid=196183) .</span><span class="sxs-lookup"><span data-stu-id="d6395-193">For details about this requirement, see Microsoft Knowledge Base article 911722, "You may receive an error message when you access ASP.NET webpages that have ViewState enabled after you upgrade from ASP.NET 1.1 to ASP.NET 2.0," at [https://go.microsoft.com/fwlink/p/?linkId=196183](https://go.microsoft.com/fwlink/p/?linkid=196183).</span></span>

<span data-ttu-id="d6395-194">Para modificar el archivo Web.config, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d6395-194">To modify the Web.config file, do the following:</span></span>

1.  <span data-ttu-id="d6395-195">En un editor de texto como Bloc de notas, abra el archivo Web.config de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d6395-195">In a text editor such as Notepad, open the application-level Web.config file.</span></span>

2.  <span data-ttu-id="d6395-196">En el archivo de Web.config, busque la `<system.web>` sección.</span><span class="sxs-lookup"><span data-stu-id="d6395-196">In the Web.config file, locate the `<system.web>` section.</span></span>

3.  <span data-ttu-id="d6395-197">Agregue la `<machineKey>` sección siguiente a la `<system.web>` sección:</span><span class="sxs-lookup"><span data-stu-id="d6395-197">Add the following `<machineKey>` section to in the `<system.web>` section:</span></span>
    
        <machineKey validationKey="AutoGenerate,IsolateApps" decryptionKey="AutoGenerate,IsolateApps" validation="3DES" decryption="3DES"/>

4.  <span data-ttu-id="d6395-198">Guarde el archivo Web.config.</span><span class="sxs-lookup"><span data-stu-id="d6395-198">Save the Web.config file.</span></span>

5.  <span data-ttu-id="d6395-199">Reinicie el servicio de Internet Information Services (IIS) ejecutando el siguiente comando en un símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="d6395-199">Restart the Internet Information Services (IIS) service by running the following command at a command prompt:</span></span>
    
        iisreset

</div>

<div>

## <a name="supporting-yi-meng-and-zang-characters"></a><span data-ttu-id="d6395-200">Compatibilidad con caracteres Yi, Meng y Zang</span><span class="sxs-lookup"><span data-stu-id="d6395-200">Supporting Yi, Meng, and Zang Characters</span></span>

<span data-ttu-id="d6395-201">Esta sección se le aplica solo si su organización necesita admitir caracteres Yi, Meng o Zang.</span><span class="sxs-lookup"><span data-stu-id="d6395-201">This section applies to you only if your organization needs to support Yi, Meng, or Zang characters.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d6395-202">Para obtener información sobre los caracteres Yi, Meng y Zang y por qué es posible que sean importantes para su implementación, vea la información de los conjuntos de caracteres de GB18030 <A href="https://go.microsoft.com/fwlink/p/?linkid=240223">https://go.microsoft.com/fwlink/p/?linkId=240223</A> .</span><span class="sxs-lookup"><span data-stu-id="d6395-202">For information on what the Yi, Meng, and Zang characters are and why they may be important to your deployment, see the information on the GB18030 character sets <A href="https://go.microsoft.com/fwlink/p/?linkid=240223">https://go.microsoft.com/fwlink/p/?linkId=240223</A>.</span></span>



</div>

<span data-ttu-id="d6395-p106">Para admitir caracteres Yi, Meng o Zang, es necesario modificar la intercalación de la base de datos de Rgsconfig. Cambie la intercalación de la columna **Nombre** en las siguientes tablas de cada base de datos de Rgsconfig:</span><span class="sxs-lookup"><span data-stu-id="d6395-p106">To support Yi, Meng, or Zang characters, you need to modify the collation for the Rgsconfig database. Change the collation of the **Name** column in the following tables in each Rgsconfig database:</span></span>

  - <span data-ttu-id="d6395-205">dbo.AgentGroups</span><span class="sxs-lookup"><span data-stu-id="d6395-205">dbo.AgentGroups</span></span>

  - <span data-ttu-id="d6395-206">dbo.BusinessHours</span><span class="sxs-lookup"><span data-stu-id="d6395-206">dbo.BusinessHours</span></span>

  - <span data-ttu-id="d6395-207">dbo.HolidaySets</span><span class="sxs-lookup"><span data-stu-id="d6395-207">dbo.HolidaySets</span></span>

  - <span data-ttu-id="d6395-208">dbo.Queues</span><span class="sxs-lookup"><span data-stu-id="d6395-208">dbo.Queues</span></span>

  - <span data-ttu-id="d6395-209">dbo.Workflows</span><span class="sxs-lookup"><span data-stu-id="d6395-209">dbo.Workflows</span></span>

<span data-ttu-id="d6395-210">Para SQL Server 2008 R2 y SQL Server 2012, use la \_ \_ intercalación de latín general 100 (sensible a la tilde).</span><span class="sxs-lookup"><span data-stu-id="d6395-210">For SQL Server 2008 R2 and SQL Server 2012, use the Latin\_General\_100 (Accent Sensitive) collation.</span></span> <span data-ttu-id="d6395-211">Si usa esta intercalación, ningún nombre de objeto distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d6395-211">If you use this collation, all object names are not case-sensitive.</span></span>

<span data-ttu-id="d6395-212">Puede cambiar la intercalación con Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="d6395-212">You can change the collation by using Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="d6395-213">Para obtener más información sobre cómo usar esta herramienta, consulte "uso de SQL Server Management Studio" en [https://go.microsoft.com/fwlink/p/?linkId=196184](https://go.microsoft.com/fwlink/p/?linkid=196184) .</span><span class="sxs-lookup"><span data-stu-id="d6395-213">For details about using this tool, see "Using SQL Server Management Studio" at [https://go.microsoft.com/fwlink/p/?linkId=196184](https://go.microsoft.com/fwlink/p/?linkid=196184).</span></span> <span data-ttu-id="d6395-214">Siga estos pasos para cambiar la intercalación:</span><span class="sxs-lookup"><span data-stu-id="d6395-214">Follow these steps to change the collation:</span></span>

1.  <span data-ttu-id="d6395-215">Asegúrese de que SQL Server Management Studio está configurado para permitir los cambios que requieren que las tablas se vuelvan a crear.</span><span class="sxs-lookup"><span data-stu-id="d6395-215">Be sure that SQL Server Management Studio is configured to allow changes that require tables to be recreated.</span></span> <span data-ttu-id="d6395-216">Para obtener más información, vea "cuadro de diálogo Guardar (no permitido)" en [https://go.microsoft.com/fwlink/p/?linkId=196186](https://go.microsoft.com/fwlink/p/?linkid=196186) .</span><span class="sxs-lookup"><span data-stu-id="d6395-216">For details, see "Save (Not Permitted) Dialog Box" at [https://go.microsoft.com/fwlink/p/?linkId=196186](https://go.microsoft.com/fwlink/p/?linkid=196186).</span></span> <span data-ttu-id="d6395-217">Para obtener más información sobre cómo establecer una intercalación de columna, vea "Cómo: establecer la intercalación de columnas (Visual Database Tools)" en [https://go.microsoft.com/fwlink/p/?linkId=196185](https://go.microsoft.com/fwlink/p/?linkid=196185) .</span><span class="sxs-lookup"><span data-stu-id="d6395-217">For details about setting a column collation, see "How to: Set Column Collation (Visual Database Tools)" at [https://go.microsoft.com/fwlink/p/?linkId=196185](https://go.microsoft.com/fwlink/p/?linkid=196185).</span></span>

2.  <span data-ttu-id="d6395-218">Use Microsoft SQL Server Management Studio para conectarse a la base de datos de Rgsconfig.</span><span class="sxs-lookup"><span data-stu-id="d6395-218">Using Microsoft SQL Server Management Studio, connect to the Rgsconfig database.</span></span>

3.  <span data-ttu-id="d6395-219">Busque la tabla que desea cambiar en la base de datos de Rgsconfig, haga clic con el botón secundario en ella y, a continuación, haga clic en **Diseño**.</span><span class="sxs-lookup"><span data-stu-id="d6395-219">Find the table you want to change in the Rgsconfig database, right-click the table, and click **Design**.</span></span>

4.  <span data-ttu-id="d6395-220">Cambie la intercalación de la columna **Nombre** y guarde la tabla.</span><span class="sxs-lookup"><span data-stu-id="d6395-220">Change the collation of the **Name** column and save the table.</span></span>

<span data-ttu-id="d6395-221"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d6395-221"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

