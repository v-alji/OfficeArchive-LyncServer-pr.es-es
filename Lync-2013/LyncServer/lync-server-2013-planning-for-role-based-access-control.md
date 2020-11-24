---
title: 'Lync Server 2013: Planeación del control de acceso basado en roles'
description: 'Lync Server 2013: planeamiento de control de acceso basado en roles.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for role-based access control (RBAC)
ms:assetid: 41204ba3-ce5b-41a8-a6c3-b444468fa328
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425917(v=OCS.15)
ms:contentKeyID: 48183962
ms.date: 01/28/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 971b3353694a1cdd53d88452717e6a9a360c6870
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400182"
---
# <a name="planning-for-role-based-access-control-in-lync-server-2013"></a><span data-ttu-id="75f22-103">Planeación del control de acceso basado en roles en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75f22-103">Planning for role-based access control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="75f22-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="75f22-104">

<span> </span></span></span>

<span data-ttu-id="75f22-105">_**Última modificación del tema:** 2015-01-27_</span><span class="sxs-lookup"><span data-stu-id="75f22-105">_**Topic Last Modified:** 2015-01-27_</span></span>

<span data-ttu-id="75f22-106">Para que pueda delegar tareas administrativas a la vez que se mantienen los altos estándares de seguridad, Lync Server 2013 ofrece control de acceso basado en roles (RBAC).</span><span class="sxs-lookup"><span data-stu-id="75f22-106">To enable you to delegate administrative tasks while maintaining high standards for security, Lync Server 2013 offers role-based access control (RBAC).</span></span> <span data-ttu-id="75f22-107">Con RBAC, el privilegio administrativo se concede mediante la asignación de usuarios a roles administrativos.</span><span class="sxs-lookup"><span data-stu-id="75f22-107">With RBAC, administrative privilege is granted by assigning users to administrative roles.</span></span> <span data-ttu-id="75f22-108">Lync Server 2013 incluye un conjunto completo de funciones administrativas integradas y también le permite crear nuevos roles y especificar una lista personalizada de cmdlets para cada nuevo rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-108">Lync Server 2013 includes a rich set of built-in administrative roles, and also enables you to create new roles and specify a custom list of cmdlets for each new role.</span></span> <span data-ttu-id="75f22-109">También puede agregar scripts de cmdlets a las tareas permitidas de roles de RBAC tanto predefinidos como personalizados.</span><span class="sxs-lookup"><span data-stu-id="75f22-109">You can also add scripts of cmdlets to the allowed tasks of both predefined and custom RBAC roles.</span></span>

<div>

## <a name="better-server-security-and-centralization"></a><span data-ttu-id="75f22-110">Mayor seguridad del servidor y centralización</span><span class="sxs-lookup"><span data-stu-id="75f22-110">Better Server Security and Centralization</span></span>

<span data-ttu-id="75f22-111">Con RBAC, el acceso y la autorización se basan de forma precisa en el rol de servidor de Lync de un usuario.</span><span class="sxs-lookup"><span data-stu-id="75f22-111">With RBAC, access and authorization is based precisely on a user’s Lync Server role.</span></span> <span data-ttu-id="75f22-112">Esto permite el uso de la práctica de seguridad "privilegio mínimo", que concede a los administradores y usuarios solo los derechos necesarios para su trabajo.</span><span class="sxs-lookup"><span data-stu-id="75f22-112">This enables use of the security practice of "least privilege," granting administrators and users only the rights that are necessary for their job.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="75f22-113">Las restricciones de RBAC solo funcionan en los administradores que trabajan de forma remota, mediante el panel de control de Lync Server o el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="75f22-113">RBAC restrictions work only on administrators working remotely, using either the Lync Server Control Panel or Lync Server Management Shell.</span></span> <span data-ttu-id="75f22-114">Un usuario que está sentado en un servidor que ejecuta Lync Server no está restringido por RBAC.</span><span class="sxs-lookup"><span data-stu-id="75f22-114">A user sitting at a server running Lync Server is not restricted by RBAC.</span></span> <span data-ttu-id="75f22-115">Por lo tanto, es importante que la seguridad física de su Lync Server Conserve las restricciones RBAC.</span><span class="sxs-lookup"><span data-stu-id="75f22-115">Therefore, physical security of your Lync Server is important to preserve RBAC restrictions.</span></span>



</div>

</div>

<div>

## <a name="roles-and-scope"></a><span data-ttu-id="75f22-116">Roles y ámbito</span><span class="sxs-lookup"><span data-stu-id="75f22-116">Roles and Scope</span></span>

<span data-ttu-id="75f22-117">En RBAC, un *rol* está habilitado para usar una lista de cmdlets, diseñada para ser útil para un determinado tipo de administrador o técnico.</span><span class="sxs-lookup"><span data-stu-id="75f22-117">In RBAC, a *role* is enabled to use a list of cmdlets, designed to be useful for a certain type of administrator or technician.</span></span> <span data-ttu-id="75f22-118">Un *ámbito* es el conjunto de objetos en el que pueden operar los cmdlets definidos en un rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-118">A *scope* is the set of objects which the cmdlets defined in a role can operate on.</span></span> <span data-ttu-id="75f22-119">Los objetos a los que afecta el ámbito pueden ser cuentas de usuario (agrupadas por unidad de organización) o servidores (agrupados por sitio).</span><span class="sxs-lookup"><span data-stu-id="75f22-119">The objects that scope affects can be either user accounts (grouped by organizational unit) or servers (grouped by site).</span></span>

<span data-ttu-id="75f22-120">En la tabla siguiente se enumeran los roles predefinidos en Lync Server y se ofrece información general sobre los tipos de tareas que cada uno puede realizar.</span><span class="sxs-lookup"><span data-stu-id="75f22-120">The following table lists the predefined roles in Lync Server, and gives a general overview of the types of tasks each can do.</span></span> <span data-ttu-id="75f22-121">La cuarta columna muestra el rol de servidor de Microsoft Exchange similar para cada rol de servidor de Lync, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="75f22-121">The fourth column shows the similar Microsoft Exchange Server role for each Lync Server role, if there is one.</span></span>

### <a name="predefined-administrative-roles"></a><span data-ttu-id="75f22-122">Roles administrativos predefinidos</span><span class="sxs-lookup"><span data-stu-id="75f22-122">Predefined Administrative Roles</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75f22-123">Rol</span><span class="sxs-lookup"><span data-stu-id="75f22-123">Role</span></span></th>
<th><span data-ttu-id="75f22-124">Tareas permitidas</span><span class="sxs-lookup"><span data-stu-id="75f22-124">Tasks allowed</span></span></th>
<th><span data-ttu-id="75f22-125">Grupo de Active Directory subyacente</span><span class="sxs-lookup"><span data-stu-id="75f22-125">Underlying Active Directory group</span></span></th>
<th><span data-ttu-id="75f22-126">Equivalente de Exchange</span><span class="sxs-lookup"><span data-stu-id="75f22-126">Exchange equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75f22-127">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-127">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-128">Permite realizar todas las tareas administrativas y modificar toda la configuración, incluida la creación de roles y la asignación de usuarios a roles.</span><span class="sxs-lookup"><span data-stu-id="75f22-128">Can perform all administrative tasks and modify all settings, including creating roles and assigning users to roles.</span></span> <span data-ttu-id="75f22-129">Puede expandir una implementación agregando nuevos sitios, agrupaciones y servicios.</span><span class="sxs-lookup"><span data-stu-id="75f22-129">Can expand a deployment by adding new sites, pools, and services.</span></span></p></td>
<td><p><span data-ttu-id="75f22-130">CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-130">CSAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-131">Administración de la organización</span><span class="sxs-lookup"><span data-stu-id="75f22-131">Organization Management</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75f22-132">CsUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-132">CsUserAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-133">Permite habilitar y deshabilitar usuarios para Lync Server, mover usuarios y asignar directivas existentes a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="75f22-133">Can enable and disable users for Lync Server, move users and assign existing policies to users.</span></span> <span data-ttu-id="75f22-134">No se pueden modificar las directivas.</span><span class="sxs-lookup"><span data-stu-id="75f22-134">Cannot modify policies.</span></span></p></td>
<td><p><span data-ttu-id="75f22-135">CSUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-135">CSUserAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-136">Destinatarios de correo</span><span class="sxs-lookup"><span data-stu-id="75f22-136">Mail Recipients</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75f22-137">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-137">CsVoiceAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-138">Permite crear, configurar y administrar directivas y configuración relacionadas con la voz.</span><span class="sxs-lookup"><span data-stu-id="75f22-138">Can create, configure, and manage voice-related settings and policies.</span></span></p></td>
<td><p><span data-ttu-id="75f22-139">CSVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-139">CSVoiceAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-140">No aplicable</span><span class="sxs-lookup"><span data-stu-id="75f22-140">Not applicable</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75f22-141">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-141">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-142">Permite administrar, supervisar y solucionar problemas con servidores y servicios.</span><span class="sxs-lookup"><span data-stu-id="75f22-142">Can manage, monitor, and troubleshoot servers and services.</span></span> <span data-ttu-id="75f22-143">Puede evitar nuevas conexiones a los servidores, detener e iniciar servicios, y aplicar actualizaciones de software.</span><span class="sxs-lookup"><span data-stu-id="75f22-143">Can prevent new connections to servers, stop and start services, and apply software updates.</span></span> <span data-ttu-id="75f22-144">No se pueden realizar cambios con el impacto global de la configuración.</span><span class="sxs-lookup"><span data-stu-id="75f22-144">Cannot make changes with global configuration impact.</span></span></p></td>
<td><p><span data-ttu-id="75f22-145">CSServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-145">CSServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-146">Administración de servidores</span><span class="sxs-lookup"><span data-stu-id="75f22-146">Server Management</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75f22-147">CsViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-147">CsViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-148">Permite ver la implementación, incluida la información del usuario y del servidor, a fin de supervisar el estado de implementación.</span><span class="sxs-lookup"><span data-stu-id="75f22-148">Can view the deployment, including user and server information, in order to monitor deployment health.</span></span></p></td>
<td><p><span data-ttu-id="75f22-149">CSViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-149">CSViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-150">Administración de View-Only organización</span><span class="sxs-lookup"><span data-stu-id="75f22-150">View-Only Organization Management</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75f22-151">CsHelpDesk</span><span class="sxs-lookup"><span data-stu-id="75f22-151">CsHelpDesk</span></span></p></td>
<td><p><span data-ttu-id="75f22-152">Permite ver la implementación, incluidas las propiedades y directivas del usuario.</span><span class="sxs-lookup"><span data-stu-id="75f22-152">Can view the deployment, including user's properties and policies.</span></span> <span data-ttu-id="75f22-153">Puede ejecutar tareas específicas de solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="75f22-153">Can run specific troubleshooting tasks.</span></span> <span data-ttu-id="75f22-154">No se pueden cambiar las propiedades o directivas del usuario, la configuración del servidor o los servicios.</span><span class="sxs-lookup"><span data-stu-id="75f22-154">Cannot change user properties or policies, server configuration, or services.</span></span></p></td>
<td><p><span data-ttu-id="75f22-155">CSHelpDesk</span><span class="sxs-lookup"><span data-stu-id="75f22-155">CSHelpDesk</span></span></p></td>
<td><p><span data-ttu-id="75f22-156">Telefónica</span><span class="sxs-lookup"><span data-stu-id="75f22-156">HelpDesk</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75f22-157">CsArchivingAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-157">CsArchivingAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-158">Permite modificar las directivas y la configuración de archivado.</span><span class="sxs-lookup"><span data-stu-id="75f22-158">Can modify archiving configuration and policies.</span></span></p></td>
<td><p><span data-ttu-id="75f22-159">CSArchivingAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-159">CSArchivingAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-160">Administración de retención, retención legal</span><span class="sxs-lookup"><span data-stu-id="75f22-160">Retention Management, Legal Hold</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75f22-161">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-161">CsResponseGroupAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-162">Permite administrar la configuración de la aplicación de grupo de respuesta dentro de un sitio.</span><span class="sxs-lookup"><span data-stu-id="75f22-162">Can manage the configuration of the Response Group application within a site.</span></span></p></td>
<td><p><span data-ttu-id="75f22-163">CSResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-163">CSResponseGroupAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-164">No aplicable</span><span class="sxs-lookup"><span data-stu-id="75f22-164">Not applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75f22-165">CsLocationAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-165">CsLocationAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-166">El nivel más bajo de derechos para la administración mejorada de 9-1-1 (E9-1-1), incluida la creación de ubicaciones e identificadores de red E9-1-1, y la asociación entre sí.</span><span class="sxs-lookup"><span data-stu-id="75f22-166">Lowest level of rights for Enhanced 9-1-1 (E9-1-1) management, including creating E9-1-1 locations and network identifiers, and associating these with each other.</span></span> <span data-ttu-id="75f22-167">Este rol siempre se asigna con un ámbito global.</span><span class="sxs-lookup"><span data-stu-id="75f22-167">This role is always assigned with a global scope.</span></span></p></td>
<td><p><span data-ttu-id="75f22-168">CSLocationAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-168">CSLocationAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-169">No aplicable</span><span class="sxs-lookup"><span data-stu-id="75f22-169">Not applicable</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75f22-170">AdministradorGrupoRespuestaCs</span><span class="sxs-lookup"><span data-stu-id="75f22-170">CsResponseGroupManager</span></span></p></td>
<td><p><span data-ttu-id="75f22-171">Permite administrar grupos de respuesta específicos.</span><span class="sxs-lookup"><span data-stu-id="75f22-171">Can manage specific response groups.</span></span></p></td>
<td><p><span data-ttu-id="75f22-172">CSResponseGroupManager</span><span class="sxs-lookup"><span data-stu-id="75f22-172">CSResponseGroupManager</span></span></p></td>
<td><p><span data-ttu-id="75f22-173">No aplicable</span><span class="sxs-lookup"><span data-stu-id="75f22-173">Not applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75f22-174">CsPersistentChatAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-174">CsPersistentChatAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-175">Permite administrar la característica de chat persistente y las salas de chat persistentes específicas.</span><span class="sxs-lookup"><span data-stu-id="75f22-175">Can manage the Persistent Chat feature and specific Persistent Chat rooms.</span></span></p></td>
<td><p><span data-ttu-id="75f22-176">CSPersistentChatAdministrator</span><span class="sxs-lookup"><span data-stu-id="75f22-176">CSPersistentChatAdministrator</span></span></p></td>
<td><p><span data-ttu-id="75f22-177">No aplicable</span><span class="sxs-lookup"><span data-stu-id="75f22-177">Not applicable</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75f22-178">Todos los roles predefinidos que se incluyen en Lync Server tienen un ámbito global.</span><span class="sxs-lookup"><span data-stu-id="75f22-178">All predefined roles shipped in Lync Server have a global scope.</span></span> <span data-ttu-id="75f22-179">Para seguir las prácticas de privilegios mínimos, no debe asignar usuarios a roles con ámbito global si van a administrar únicamente un conjunto limitado de servidores o usuarios.</span><span class="sxs-lookup"><span data-stu-id="75f22-179">To follow least privilege practices, you should not assign users to roles with global scope if they are going to administer only a limited set of servers or users.</span></span> <span data-ttu-id="75f22-180">Para ello, puede crear roles que se basen en un rol existente, pero con un ámbito más limitado.</span><span class="sxs-lookup"><span data-stu-id="75f22-180">To accomplish this, you can create roles which are based on an existing role, but with a more limited scope.</span></span>

<div>

## <a name="creating-a-scoped-role"></a><span data-ttu-id="75f22-181">Crear un rol con ámbito</span><span class="sxs-lookup"><span data-stu-id="75f22-181">Creating a Scoped Role</span></span>

<span data-ttu-id="75f22-182">Al crear un rol con ámbito limitado (un rol con ámbito), especifique el ámbito, junto con el rol existente en el que se basa y el grupo de Active Directory al que se va a asignar el rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-182">When you create a role with limited scope (a scoped role), you specify the scope, along with the existing role it is based on and the Active Directory group to be assigned the role.</span></span> <span data-ttu-id="75f22-183">El grupo de Active Directory que especifique debe estar ya creado.</span><span class="sxs-lookup"><span data-stu-id="75f22-183">The Active Directory group you specify must already be created.</span></span> <span data-ttu-id="75f22-184">El siguiente cmdlet es un ejemplo de una creación de un rol que tiene los privilegios de una de las funciones administrativas predefinidas, pero con un ámbito limitado.</span><span class="sxs-lookup"><span data-stu-id="75f22-184">The following cmdlet is an example of a creating a role which has the privileges of one of the pre-defined administrative roles, but with limited scope.</span></span> <span data-ttu-id="75f22-185">Crea un nuevo rol denominado `Site01 Server Administrators` .</span><span class="sxs-lookup"><span data-stu-id="75f22-185">It creates a new role called `Site01 Server Administrators`.</span></span> <span data-ttu-id="75f22-186">El rol tiene las capacidades del rol de CsServerAdministrator predefinido, pero solo para los servidores que se encuentran en el sitio de Site01.</span><span class="sxs-lookup"><span data-stu-id="75f22-186">The role has the abilities of the predefined CsServerAdministrator role, but only for the servers located in the Site01 site.</span></span> <span data-ttu-id="75f22-187">Para que este cmdlet funcione, el sitio de Site01 debe estar ya definido y ya debe existir un grupo de seguridad universal con el nombre `Site01 Server Administrators` .</span><span class="sxs-lookup"><span data-stu-id="75f22-187">For this cmdlet to work, the Site01 site must already be defined, and a universal security group named `Site01 Server Administrators` must already exist.</span></span>

    New-CsAdminRole -Identity "Site01 Server Administrators" -Template CsServerAdministrator -ConfigScopes "site:Site01"

<span data-ttu-id="75f22-188">Después de ejecutar este cmdlet, todos los usuarios que sean miembros del `Site01 Server Administrators` Grupo dispondrán de privilegios de administrador de servidor para los servidores de Site01.</span><span class="sxs-lookup"><span data-stu-id="75f22-188">After this cmdlet runs, all users who are members of the `Site01 Server Administrators` group will have server administrator privileges for the servers in Site01.</span></span> <span data-ttu-id="75f22-189">Además, los usuarios que se agreguen posteriormente a este grupo de seguridad universal también obtendrán los privilegios de este rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-189">Additionally, any users who are later added to this universal security group also gain the privileges of this role.</span></span> <span data-ttu-id="75f22-190">Observe que se llama tanto a la propia función como al grupo de seguridad universal al que está asignada `Site01 Server Administrators` .</span><span class="sxs-lookup"><span data-stu-id="75f22-190">Note that both the role itself, and the universal security group it is assigned to are called `Site01 Server Administrators`.</span></span>

<span data-ttu-id="75f22-191">En el ejemplo siguiente se limita el ámbito de usuario en lugar del ámbito del servidor.</span><span class="sxs-lookup"><span data-stu-id="75f22-191">The following example limits user scope instead of server scope.</span></span> <span data-ttu-id="75f22-192">Crea un `Sales Users Administrator` rol para administrar las cuentas de usuario en la unidad organizativa ventas.</span><span class="sxs-lookup"><span data-stu-id="75f22-192">It creates a `Sales Users Administrator` role to administer the user accounts in the Sales organizational unit.</span></span> <span data-ttu-id="75f22-193">El grupo de seguridad universal de SalesUsersAdministrator ya debe crearse para que este cmdlet funcione.</span><span class="sxs-lookup"><span data-stu-id="75f22-193">The SalesUsersAdministrator universal security group must already be created for this cmdlet to work.</span></span>

    New-CsAdminRole -Identity "Sales Users Administrator " -Template CsUserAdministrator -UserScopes "OU:OU=Sales, OU=Lync Tenants, DC=Domain, DC=com"

</div>

<div>

## <a name="creating-a-new-role"></a><span data-ttu-id="75f22-194">Crear un nuevo rol</span><span class="sxs-lookup"><span data-stu-id="75f22-194">Creating a New Role</span></span>

<span data-ttu-id="75f22-195">Para crear un rol que tenga acceso a un conjunto de cmdlets que no se encuentra en una de las funciones predefinidas, o a un conjunto de scripts o módulos, vuelva a empezar a usar uno de los roles predefinidos como una plantilla.</span><span class="sxs-lookup"><span data-stu-id="75f22-195">To create a role that has access to a set of cmdlets not in one of the predefined roles, or to a set of scripts or modules, you again start by using one of the predefined roles as a template.</span></span> <span data-ttu-id="75f22-196">Tenga en cuenta que los scripts y los módulos que los roles pueden ejecutarse deben almacenarse en las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="75f22-196">Note that scripts and modules that roles are to be able to run must be stored in the following locations:</span></span>

  - <span data-ttu-id="75f22-197">La ruta de acceso del módulo de Lync, que es de forma predeterminada C: \\ archivos de programa archivos \\ comunes \\ Microsoft Lync Server 2013 \\ módulos \\ Lync</span><span class="sxs-lookup"><span data-stu-id="75f22-197">The Lync module path, which is by default C:\\Program Files\\Common Files\\Microsoft Lync Server 2013\\Modules\\Lync</span></span>

  - <span data-ttu-id="75f22-198">La ruta de acceso del script de usuario, que es, de forma predeterminada, C: archivos comunes de archivos de \\ programa \\ \\ Microsoft Lync Server 2013 \\ AdminScripts</span><span class="sxs-lookup"><span data-stu-id="75f22-198">The user script path, which is by default C:\\Program Files\\Common Files\\Microsoft Lync Server 2013\\AdminScripts</span></span>

<span data-ttu-id="75f22-199">Para hacer un nuevo rol, use el cmdlet **New-CsAdminRole** .</span><span class="sxs-lookup"><span data-stu-id="75f22-199">To make a new role, you use the **New-CsAdminRole** cmdlet.</span></span> <span data-ttu-id="75f22-200">Antes **de ejecutar New-CsAdminRole**, primero debe crear el grupo de seguridad universal subyacente que se asociará con este rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-200">Before running **New-CsAdminRole**, you must first create the underlying universal security group that will be associated with this role.</span></span>

<span data-ttu-id="75f22-201">Los siguientes cmdlets constituyen un ejemplo de la creación de un nuevo rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-201">The following cmdlets serve as an example of a creating a new role.</span></span> <span data-ttu-id="75f22-202">Crean un nuevo tipo de función denominado `MyHelpDeskScriptRole` .</span><span class="sxs-lookup"><span data-stu-id="75f22-202">They create a new role type called `MyHelpDeskScriptRole`.</span></span> <span data-ttu-id="75f22-203">El nuevo rol tiene las capacidades del rol de CsHelpDesk predefinido y, además, puede ejecutar las funciones en un script denominado "testScript".</span><span class="sxs-lookup"><span data-stu-id="75f22-203">The new role has the abilities of the predefined CsHelpDesk role, and can additionally run the functions in a script named “testscript”.</span></span>

    New-CsAdminRole -Identity "MyHelpDeskScriptRole" -Template CsHelpDesk -ScriptModules @{Add="testScript.ps1"}

<span data-ttu-id="75f22-204">Para que este cmdlet funcione, primero debe haber creado el grupo de seguridad universal MyHelpDeskScriptRole.</span><span class="sxs-lookup"><span data-stu-id="75f22-204">For this cmdlet to work, you must have first created the universal security group MyHelpDeskScriptRole.</span></span>

<span data-ttu-id="75f22-205">Después de que este cmdlet se ejecuta, puede asignar usuarios directamente a este rol (en cuyo caso tienen ámbito global) o crear un rol con ámbito basado en este rol, como se explica en creación de un rol con ámbito, anteriormente en este documento.</span><span class="sxs-lookup"><span data-stu-id="75f22-205">After this cmdlet runs, you can assign users directly to this role (in which case they have global scope), or create a scoped role based on this role, as explained in Creating a Scoped Role, previously in this document.</span></span>

</div>

<div>

## <a name="assigning-roles-to-users"></a><span data-ttu-id="75f22-206">Asignar roles a usuarios</span><span class="sxs-lookup"><span data-stu-id="75f22-206">Assigning Roles to Users</span></span>

<span data-ttu-id="75f22-207">Cada rol de Lync Server está asociado con un grupo subyacente de seguridad universal de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="75f22-207">Each Lync Server role is associated with an underlying Active Directory universal security group.</span></span> <span data-ttu-id="75f22-208">Los usuarios que agregue al grupo subyacente obtienen las funciones de ese rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-208">Any users who you add to the underlying group gain the abilities of that role.</span></span>

<span data-ttu-id="75f22-209">Los ejemplos de las secciones anteriores crearon un nuevo rol y asignaron un grupo de seguridad universal existente al nuevo rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-209">The examples in the preceding sections both created a new role and assigned an existing universal security group to the new role.</span></span> <span data-ttu-id="75f22-210">Para asignar un rol existente a uno o varios usuarios, agregue esos usuarios al grupo asociado con el rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-210">To assign an existing role to one or more users, add those users to the group associated with the role.</span></span> <span data-ttu-id="75f22-211">Puede Agregar usuarios individuales y grupos de seguridad universal a estos grupos.</span><span class="sxs-lookup"><span data-stu-id="75f22-211">You can add both individual users and universal security groups to these groups.</span></span>

<span data-ttu-id="75f22-212">Por ejemplo, el rol **CsAdministrator** se concede automáticamente al grupo de seguridad universal de **administradores de CS** en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="75f22-212">For example, the **CsAdministrator** role is automatically granted to the **CS Administrators** universal security group in Active Directory.</span></span> <span data-ttu-id="75f22-213">Este grupo de seguridad universal se crea en Active Directory al implementar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="75f22-213">This universal security group is created in Active Directory when you deploy Lync Server.</span></span> <span data-ttu-id="75f22-214">Para conceder este privilegio a un usuario o grupo, simplemente puede agregarlos al grupo de **administradores de CS** .</span><span class="sxs-lookup"><span data-stu-id="75f22-214">To grant a user or group this privilege, you can simply add them to the **CS Administrators** group.</span></span>

<span data-ttu-id="75f22-215">A un usuario se le pueden dar varios roles RBAC mediante su adición a los grupos de Active Directory subyacentes que corresponden a cada rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-215">A user can be given multiple RBAC roles by being added to the underlying Active Directory groups that correspond to each role.</span></span>

<span data-ttu-id="75f22-216">Tenga en cuenta que, al crear un rol, los usuarios que se agreguen posteriormente al grupo de Active Directory subyacente ganarán las funciones de ese rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-216">Note that when you create a role, users who are later added to the underlying Active Directory group gain the abilities of that role.</span></span>

</div>

<div>

## <a name="modifying-the-abilities-of-a-role"></a><span data-ttu-id="75f22-217">Modificar las funciones de un rol</span><span class="sxs-lookup"><span data-stu-id="75f22-217">Modifying the Abilities of a Role</span></span>

<span data-ttu-id="75f22-218">Puede modificar la lista de cmdlets y scripts que puede ejecutar un rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-218">You can modify the list of cmdlets and scripts that a role can run.</span></span> <span data-ttu-id="75f22-219">Puede modificar los cmdlets y scripts que pueden ejecutar los roles personalizados, pero solo puede modificar los scripts para roles predefinidos.</span><span class="sxs-lookup"><span data-stu-id="75f22-219">You can modify both the cmdlets and scripts that custom roles can run, but you can modify only the scripts for predefined roles.</span></span> <span data-ttu-id="75f22-220">Cada cmdlet que escriba puede Agregar, quitar o reemplazar cmdlets o scripts.</span><span class="sxs-lookup"><span data-stu-id="75f22-220">Each cmdlet you type can add, remove, or replace cmdlets or scripts.</span></span>

<span data-ttu-id="75f22-221">Para modificar un rol, use el cmdlet **set-CsAdminRole** .</span><span class="sxs-lookup"><span data-stu-id="75f22-221">To modify a role, use the **Set-CsAdminRole** cmdlet.</span></span> <span data-ttu-id="75f22-222">El siguiente cmdlet quita un script del rol.</span><span class="sxs-lookup"><span data-stu-id="75f22-222">The following cmdlet removes one script from the role.</span></span>

    Set-CsAdminRole -Identity "MyHelpDeskScriptRole" -ScriptModules @{Remove="testScript.ps1"}

</div>

</div>

<div>

## <a name="planning-for-rbac"></a><span data-ttu-id="75f22-223">Planificación de RBAC</span><span class="sxs-lookup"><span data-stu-id="75f22-223">Planning for RBAC</span></span>

<span data-ttu-id="75f22-224">Para cada persona a la que se va a conceder algún tipo de derecho administrativo para su implementación de Lync Server, considere exactamente qué tareas necesitan realizar y, a continuación, asígnelos a roles con el menor privilegio y el ámbito necesario para su trabajo.</span><span class="sxs-lookup"><span data-stu-id="75f22-224">For each person who is to be given any kind of administrative rights for your Lync Server deployment, consider exactly which tasks they need to perform, then assign them to roles with the least privilege and scope necessary for their job.</span></span> <span data-ttu-id="75f22-225">Si es necesario, puede usar el cmdlet **set-CsAdminRole** para crear un nuevo rol solo con los cmdlets necesarios para las tareas de esta persona.</span><span class="sxs-lookup"><span data-stu-id="75f22-225">If necessary, you can use the **Set-CsAdminRole** cmdlet to create a new role with only the cmdlets necessary for this person’s tasks.</span></span>

<span data-ttu-id="75f22-226">Los usuarios que tienen el rol CsAdministrator pueden crear todos los tipos de roles, incluidos los roles basados en CsAdministrator, y asignarles usuarios.</span><span class="sxs-lookup"><span data-stu-id="75f22-226">Users who have the CsAdministrator role can create all types of roles, including roles based on CsAdministrator, and assign users to them.</span></span> <span data-ttu-id="75f22-227">El procedimiento recomendado es asignar el rol CsAdministrator a un conjunto muy pequeño de usuarios de confianza.</span><span class="sxs-lookup"><span data-stu-id="75f22-227">The best practice is to assign the CsAdministrator role to a very small set of trusted users.</span></span>

<span data-ttu-id="75f22-228"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="75f22-228"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

