---
title: 'Lync Server 2013: cambios realizados por la preparación del bosque'
description: 'Lync Server 2013: cambios realizados por la preparación del bosque.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by forest preparation
ms:assetid: 2e12613e-59f2-4810-a32d-24a9789a4a6e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425791(v=OCS.15)
ms:contentKeyID: 48183734
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c9bc40539c285e03610b2fc97166842473997fb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435078"
---
# <a name="changes-made-by-forest-preparation-in-lync-server-2013"></a><span data-ttu-id="69b7f-103">Cambios realizados por la preparación del bosque en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69b7f-103">Changes made by forest preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69b7f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69b7f-104">

<span> </span></span></span>

<span data-ttu-id="69b7f-105">_**Última modificación del tema:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="69b7f-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="69b7f-106">En esta sección se describen la configuración global y los objetos, así como el servicio universal y los grupos de administración creados por el paso de preparación del bosque.</span><span class="sxs-lookup"><span data-stu-id="69b7f-106">This section describes the global settings and objects, and the universal service and administration groups that are created by the forest preparation step.</span></span>

<div>

## <a name="active-directory-global-settings-and-objects"></a><span data-ttu-id="69b7f-107">Objetos y configuración global de Active Directory</span><span class="sxs-lookup"><span data-stu-id="69b7f-107">Active Directory Global Settings and Objects</span></span>

<span data-ttu-id="69b7f-108">Si almacena la configuración global en el contenedor de configuración (como es el caso de todas las implementaciones de Lync Server 2013 nuevas), la preparación del bosque usa el contenedor servicios existentes y agrega un objeto de **servicio RTC** en el objeto de servicios de configuración \\ .</span><span class="sxs-lookup"><span data-stu-id="69b7f-108">If you store global settings in the Configuration container (as is the case for all new Lync Server 2013 deployments), forest preparation uses the existing Services container and adds an **RTC Service** object under the Configuration\\Services object.</span></span> <span data-ttu-id="69b7f-109">En el objeto de servicio RTC, la preparación del bosque agrega un objeto de **configuración global** de tipo MsRTCSIP-GlobalContainer.</span><span class="sxs-lookup"><span data-stu-id="69b7f-109">Under the RTC Service object, forest preparation adds a **Global Settings** object of type msRTCSIP-GlobalContainer.</span></span> <span data-ttu-id="69b7f-110">El objeto configuración global contiene toda la configuración que se aplica a la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69b7f-110">The global settings object holds all the settings that apply to the Lync Server deployment.</span></span> <span data-ttu-id="69b7f-111">Si almacena la configuración global en el contenedor del sistema, la preparación del bosque usa un contenedor de Microsoft en el contenedor del sistema del dominio raíz y un objeto de servicio RTC bajo el \\ objeto Microsoft del sistema.</span><span class="sxs-lookup"><span data-stu-id="69b7f-111">If you store global settings in the System container, forest preparation uses a Microsoft container under the root domain System container and an RTC Service object under the System\\Microsoft object.</span></span>

<span data-ttu-id="69b7f-112">La preparación del bosque también agrega un nuevo objeto **msRTCSIP-Domain** para el dominio raíz en el que se ejecuta el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="69b7f-112">Forest preparation also adds a new **msRTCSIP-Domain** object for the root domain in which the procedure is run.</span></span>

</div>

<div>

## <a name="active-directory-universal-service-and-administration-groups"></a><span data-ttu-id="69b7f-113">Servicio universal de Active Directory y grupos de administración</span><span class="sxs-lookup"><span data-stu-id="69b7f-113">Active Directory Universal Service and Administration Groups</span></span>

<span data-ttu-id="69b7f-114">La preparación del bosque crea grupos universales basados en el dominio que especifique y agrega entradas de control de acceso (ACE) para estos grupos.</span><span class="sxs-lookup"><span data-stu-id="69b7f-114">Forest preparation creates universal groups based on the domain that you specify and adds access control entries (ACEs) for these groups.</span></span> <span data-ttu-id="69b7f-115">Este paso crea los grupos universales en los contenedores de usuario del dominio que especifique.</span><span class="sxs-lookup"><span data-stu-id="69b7f-115">This step creates the universal groups in the User containers of the domain that you specify.</span></span>

<span data-ttu-id="69b7f-116">Los grupos universales permiten a los administradores acceder y administrar la configuración y los servicios globales.</span><span class="sxs-lookup"><span data-stu-id="69b7f-116">Universal groups allow administrators to access and manage global settings and services.</span></span> <span data-ttu-id="69b7f-117">La preparación del bosque agrega los siguientes tipos de grupos universales:</span><span class="sxs-lookup"><span data-stu-id="69b7f-117">Forest preparation adds the following types of universal groups:</span></span>

  - <span data-ttu-id="69b7f-118">**Grupos administrativos**   Estos grupos definen los roles de administrador para una red de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69b7f-118">**Administrative groups**   These groups define administrator roles for a Lync Server network.</span></span>

  - <span data-ttu-id="69b7f-119">**Grupos de infraestructura**   Estos grupos proporcionan permiso para acceder a áreas específicas de la infraestructura de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69b7f-119">**Infrastructure groups**   These groups provide permission to access specific areas of the Lync Server infrastructure.</span></span> <span data-ttu-id="69b7f-120">Funcionan como componentes de grupos administrativos.</span><span class="sxs-lookup"><span data-stu-id="69b7f-120">They function as components of administrative groups.</span></span> <span data-ttu-id="69b7f-121">No debe modificar estos grupos ni agregar usuarios directamente.</span><span class="sxs-lookup"><span data-stu-id="69b7f-121">You should not modify these groups or add users directly to them.</span></span>

  - <span data-ttu-id="69b7f-122">**Grupos de servicio**   Estos grupos son cuentas de servicio necesarias para acceder a diversos servicios de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69b7f-122">**Service groups**   These groups are service accounts that are required to access various Lync Server services.</span></span>

<span data-ttu-id="69b7f-123">En la tabla siguiente se describen los grupos administrativos.</span><span class="sxs-lookup"><span data-stu-id="69b7f-123">The following table describes the administrative groups.</span></span>

### <a name="administrative-groups-created-during-forest-preparation"></a><span data-ttu-id="69b7f-124">Grupos administrativos creados durante la preparación del bosque</span><span class="sxs-lookup"><span data-stu-id="69b7f-124">Administrative Groups Created During Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69b7f-125">Grupo administrativo</span><span class="sxs-lookup"><span data-stu-id="69b7f-125">Administrative group</span></span></th>
<th><span data-ttu-id="69b7f-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="69b7f-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69b7f-127">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="69b7f-127">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="69b7f-128">Permite a los miembros administrar la configuración del servidor y del grupo, incluidos los roles de servidor, la configuración global y los usuarios.</span><span class="sxs-lookup"><span data-stu-id="69b7f-128">Allows members to manage server and pool settings, including all server roles, global settings, and users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69b7f-129">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="69b7f-129">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="69b7f-130">Permite a los miembros administrar la configuración de usuario y mover los usuarios de un servidor o grupo a otro.</span><span class="sxs-lookup"><span data-stu-id="69b7f-130">Allows members to manage user settings and move users from one server or pool to another.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69b7f-131">RTCUniversalReadOnlyAdmins</span><span class="sxs-lookup"><span data-stu-id="69b7f-131">RTCUniversalReadOnlyAdmins</span></span></p></td>
<td><p><span data-ttu-id="69b7f-132">Permite que los miembros lean la configuración del servidor, del grupo y del usuario.</span><span class="sxs-lookup"><span data-stu-id="69b7f-132">Allows members to read server, pool, and user settings.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="69b7f-133">En la tabla siguiente se describen los grupos de infraestructura.</span><span class="sxs-lookup"><span data-stu-id="69b7f-133">The following table describes the infrastructure groups.</span></span>

### <a name="infrastructure-groups-created-during-forest-preparation"></a><span data-ttu-id="69b7f-134">Grupos de infraestructura creados durante la preparación del bosque</span><span class="sxs-lookup"><span data-stu-id="69b7f-134">Infrastructure Groups Created During Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69b7f-135">Grupo de infraestructura</span><span class="sxs-lookup"><span data-stu-id="69b7f-135">Infrastructure group</span></span></th>
<th><span data-ttu-id="69b7f-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="69b7f-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69b7f-137">RTCUniversalGlobalWriteGroup</span><span class="sxs-lookup"><span data-stu-id="69b7f-137">RTCUniversalGlobalWriteGroup</span></span></p></td>
<td><p><span data-ttu-id="69b7f-138">Concede acceso de escritura a los objetos de configuración global de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69b7f-138">Grants write access to global setting objects for Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69b7f-139">RTCUniversalGlobalReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="69b7f-139">RTCUniversalGlobalReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="69b7f-140">Concede acceso de solo lectura a objetos de configuración global para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69b7f-140">Grants read-only access to global setting objects for Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69b7f-141">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="69b7f-141">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="69b7f-142">Concede acceso de solo lectura a la configuración de usuario de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69b7f-142">Grants read-only access to Lync Server user settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69b7f-143">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="69b7f-143">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="69b7f-144">Concede acceso de solo lectura a la configuración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69b7f-144">Grants read-only access to Lync Server settings.</span></span> <span data-ttu-id="69b7f-145">Este grupo no tiene acceso a la configuración del nivel de grupo, solo a la configuración específica de un servidor individual.</span><span class="sxs-lookup"><span data-stu-id="69b7f-145">This group does not have access to pool level settings, only to settings specific to an individual server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69b7f-146">RTCUniversalSBATechnicians</span><span class="sxs-lookup"><span data-stu-id="69b7f-146">RTCUniversalSBATechnicians</span></span></p></td>
<td><p><span data-ttu-id="69b7f-147">Concede acceso de solo lectura a la configuración de Lync Server y se coloca en el grupo de administradores locales de las aplicaciones de las sucursales que son supervivientes durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="69b7f-147">Grants read-only access to Lync Server configuration and are placed in the Local Administrators group of the survivable branch appliances during installation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="69b7f-148">En la siguiente tabla se describen los grupos de servicios.</span><span class="sxs-lookup"><span data-stu-id="69b7f-148">The following table describes the service groups.</span></span>

### <a name="service-groups-created-during-forest-preparation"></a><span data-ttu-id="69b7f-149">Grupos de servicio creados durante la preparación del bosque</span><span class="sxs-lookup"><span data-stu-id="69b7f-149">Service Groups Created During Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69b7f-150">Grupo de servicio</span><span class="sxs-lookup"><span data-stu-id="69b7f-150">Service group</span></span></th>
<th><span data-ttu-id="69b7f-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="69b7f-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69b7f-152">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="69b7f-152">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="69b7f-153">Incluye cuentas de servicio que se usan para ejecutar servidores front-end y servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="69b7f-153">Includes service accounts used to run Front End Server and Standard Edition servers.</span></span> <span data-ttu-id="69b7f-154">Este grupo permite que los servidores tengan acceso de lectura y escritura a la configuración global de Lync Server y a los objetos de usuario de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="69b7f-154">This group allows servers read/write access to Lync Server global settings and Active Directory user objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69b7f-155">RTCComponentUniversalServices</span><span class="sxs-lookup"><span data-stu-id="69b7f-155">RTCComponentUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="69b7f-156">Incluye cuentas de servicio que se usan para ejecutar servidores de conferencia A/V, servicios Web, servidor de mediación, servidor de archivado y servidor de supervisión.</span><span class="sxs-lookup"><span data-stu-id="69b7f-156">Includes service accounts used to run A/V Conferencing Servers, Web Services, Mediation Server, Archiving Server, and Monitoring Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69b7f-157">RTCProxyUniversalServices</span><span class="sxs-lookup"><span data-stu-id="69b7f-157">RTCProxyUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="69b7f-158">Incluye cuentas de servicio que se usan para ejecutar servidores perimetrales de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69b7f-158">Includes service accounts used to run Lync Server Edge Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69b7f-159">RTCUniversalConfigReplicator</span><span class="sxs-lookup"><span data-stu-id="69b7f-159">RTCUniversalConfigReplicator</span></span></p></td>
<td><p><span data-ttu-id="69b7f-160">Incluye servidores que pueden participar en la replicación del almacén central de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69b7f-160">Includes servers that can participate in Lync Server Central Management store replication.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69b7f-161">RTCSBAUniversalServices</span><span class="sxs-lookup"><span data-stu-id="69b7f-161">RTCSBAUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="69b7f-162">Concede acceso de solo lectura a la configuración del servidor de Lync, pero permite la configuración de la instalación de un servidor de sucursal y una implementación de dispositivos de rama supervivientes.</span><span class="sxs-lookup"><span data-stu-id="69b7f-162">Grants read-only access to Lync Server settings, but allows for configuration for the installation of a survivable branch server and survivable branch appliance deployment.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="69b7f-163">La preparación del bosque, a continuación, agrega grupos de servicio y administración a los grupos de infraestructura adecuados, de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="69b7f-163">Forest preparation then adds service and administration groups to the appropriate infrastructure groups, as follows:</span></span>

  - <span data-ttu-id="69b7f-164">RTCUniversalServerAdmins se agrega a RTCUniversalGlobalReadOnlyGroup, RTCUniversalGlobalWriteGroup, RTCUniversalServerReadOnlyGroup y RTCUniversalUserReadOnlyGroup.</span><span class="sxs-lookup"><span data-stu-id="69b7f-164">RTCUniversalServerAdmins is added to RTCUniversalGlobalReadOnlyGroup, RTCUniversalGlobalWriteGroup, RTCUniversalServerReadOnlyGroup, and RTCUniversalUserReadOnlyGroup.</span></span>

  - <span data-ttu-id="69b7f-165">RTCUniversalUserAdmins se agrega como miembro de RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup y RTCUniversalUserReadOnlyGroup.</span><span class="sxs-lookup"><span data-stu-id="69b7f-165">RTCUniversalUserAdmins is added as a member of RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup, and RTCUniversalUserReadOnlyGroup.</span></span>

  - <span data-ttu-id="69b7f-166">RTCHSUniversalServices, RTCComponentUniversalServices y RTCUniversalReadOnlyAdmins se agregan como miembros de RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup y RTCUniversalUserReadOnlyGroup.</span><span class="sxs-lookup"><span data-stu-id="69b7f-166">RTCHSUniversalServices, RTCComponentUniversalServices and RTCUniversalReadOnlyAdmins are added as members of RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup, and RTCUniversalUserReadOnlyGroup.</span></span>

<span data-ttu-id="69b7f-167">La preparación del bosque también crea los siguientes grupos de control de acceso basado en roles (RBAC):</span><span class="sxs-lookup"><span data-stu-id="69b7f-167">Forest preparation also creates the following role-based access control (RBAC) groups:</span></span>

  - <span data-ttu-id="69b7f-168">CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="69b7f-168">CSAdministrator</span></span>

  - <span data-ttu-id="69b7f-169">CSArchivingAdministrator</span><span class="sxs-lookup"><span data-stu-id="69b7f-169">CSArchivingAdministrator</span></span>

  - <span data-ttu-id="69b7f-170">CSHelpDesk</span><span class="sxs-lookup"><span data-stu-id="69b7f-170">CSHelpDesk</span></span>

  - <span data-ttu-id="69b7f-171">CSLocationAdministrator</span><span class="sxs-lookup"><span data-stu-id="69b7f-171">CSLocationAdministrator</span></span>

  - <span data-ttu-id="69b7f-172">CSResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="69b7f-172">CSResponseGroupAdministrator</span></span>

  - <span data-ttu-id="69b7f-173">CSServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="69b7f-173">CSServerAdministrator</span></span>

  - <span data-ttu-id="69b7f-174">CSUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="69b7f-174">CSUserAdministrator</span></span>

  - <span data-ttu-id="69b7f-175">CSViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="69b7f-175">CSViewOnlyAdministrator</span></span>

  - <span data-ttu-id="69b7f-176">CSVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="69b7f-176">CSVoiceAdministrator</span></span>

  - <span data-ttu-id="69b7f-177">CsPersistentChatAdministator</span><span class="sxs-lookup"><span data-stu-id="69b7f-177">CsPersistentChatAdministator</span></span>

  - <span data-ttu-id="69b7f-178">AdministradorGrupoRespuestaCs</span><span class="sxs-lookup"><span data-stu-id="69b7f-178">CsResponseGroupManager</span></span>

<span data-ttu-id="69b7f-179">Para obtener más información sobre los roles RBAC y las tareas permitidas para cada uno, vea [planear el control de acceso basado en roles en Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="69b7f-179">For details about RBAC roles and the tasks allowed for each, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="69b7f-180">La preparación del bosque crea entradas de acceso privadas y públicas.</span><span class="sxs-lookup"><span data-stu-id="69b7f-180">Forest preparation creates both private and public ACEs.</span></span> <span data-ttu-id="69b7f-181">Crea ACE privadas en el contenedor de configuración global usado por Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69b7f-181">It creates private ACEs on the global settings container used by Lync Server.</span></span> <span data-ttu-id="69b7f-182">Este contenedor solo es utilizado por Lync Server y se encuentra en el contenedor configuración o en el contenedor del sistema en el dominio raíz, según dónde se almacene la configuración global.</span><span class="sxs-lookup"><span data-stu-id="69b7f-182">This container is used only by Lync Server and is located either in the Configuration container or the System container in the root domain, depending on where you store global settings.</span></span> <span data-ttu-id="69b7f-183">Las ACE públicas creadas por la preparación del bosque se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="69b7f-183">The public ACEs created by forest preparation are listed in the following table.</span></span>

### <a name="public-aces-created-by-forest-preparation"></a><span data-ttu-id="69b7f-184">ACE públicas creadas por la preparación del bosque</span><span class="sxs-lookup"><span data-stu-id="69b7f-184">Public ACEs created by Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69b7f-185">ENTRADA</span><span class="sxs-lookup"><span data-stu-id="69b7f-185">ACE</span></span></th>
<th><span data-ttu-id="69b7f-186">RTCUniversalGlobalReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="69b7f-186">RTCUniversalGlobalReadOnlyGroup</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69b7f-187">Leer el contenedor del sistema del dominio raíz (no heredado)<strong>\*</strong></span><span class="sxs-lookup"><span data-stu-id="69b7f-187">Read root domain System Container (not inherited)<strong>\*</strong></span></span></p></td>
<td><p><span data-ttu-id="69b7f-188">X</span><span class="sxs-lookup"><span data-stu-id="69b7f-188">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69b7f-189">Contenedor DisplaySpecifiers de lectura de la configuración (no heredado)</span><span class="sxs-lookup"><span data-stu-id="69b7f-189">Read Configuration’s DisplaySpecifiers container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="69b7f-190">X</span><span class="sxs-lookup"><span data-stu-id="69b7f-190">X</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="69b7f-191"><STRONG>\*</STRONG>Las ACE que no se heredan no conceden acceso a objetos secundarios en estos contenedores.</span><span class="sxs-lookup"><span data-stu-id="69b7f-191"><STRONG>\*</STRONG>ACEs that are not inherited do not grant access to child objects under these containers.</span></span> <span data-ttu-id="69b7f-192">Las ACE que se heredan otorgan acceso a objetos secundarios en estos contenedores.</span><span class="sxs-lookup"><span data-stu-id="69b7f-192">ACEs that are inherited grant access to child objects under these containers.</span></span>



</div>

<span data-ttu-id="69b7f-193">En el contenedor configuración, en el contexto de nomenclatura de configuración, la preparación del bosque realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="69b7f-193">On the Configuration container, under the Configuration naming context, forest preparation performs the following tasks:</span></span>

  - <span data-ttu-id="69b7f-194">Agrega una entrada **{AB255F23-2DBD-4bb6-891D-38754AC280EF}** para la página de **propiedades RTC** en los atributos adminContextMenu y adminPropertyPages del especificador de presentación de idioma para usuarios, contactos y InetOrgPersons (por ejemplo, CN = user-Display, CN = 409, CN = DisplaySpecifiers).</span><span class="sxs-lookup"><span data-stu-id="69b7f-194">Adds an entry **{AB255F23-2DBD-4bb6-891D-38754AC280EF}** for the **RTC property** page under the adminContextMenu and adminPropertyPages attributes of the language display specifier for users, contacts, and InetOrgPersons (for example, CN=user-Display,CN=409,CN=DisplaySpecifiers).</span></span>

  - <span data-ttu-id="69b7f-195">Agrega un objeto **RTCPropertySet** de tipo **controlAccessRight** bajo **Extended-Rights** que se aplica a las clases User y contact.</span><span class="sxs-lookup"><span data-stu-id="69b7f-195">Adds an **RTCPropertySet** object of type **controlAccessRight** under **Extended-Rights** that applies to the User and Contact classes.</span></span>

  - <span data-ttu-id="69b7f-196">Agrega un objeto **RTCUserSearchPropertySet** de tipo **controlAccessRight** bajo **Extended-Rights** que se aplica a las clases User, Contact, ou y DomainDNS.</span><span class="sxs-lookup"><span data-stu-id="69b7f-196">Adds an **RTCUserSearchPropertySet** object of type **controlAccessRight** under **Extended-Rights** that applies to User, Contact, OU, and DomainDNS classes.</span></span>

  - <span data-ttu-id="69b7f-197">Agrega **msRTCSIP-PrimaryUserAddress** en el atributo **extracolumns** del especificador de pantalla de cada idioma de unidad organizativa (OU) (por ejemplo, CN = ORGANIZATIONALUNIT-display, CN = 409, CN = DisplaySpecifiers) y copia los valores del atributo **extracolumns** de la presentación predeterminada (por ejemplo, CN = default-display, CN = 409, CN = DisplaySpecifiers).</span><span class="sxs-lookup"><span data-stu-id="69b7f-197">Adds **msRTCSIP-PrimaryUserAddress** under the **extraColumns** attribute of each language organizational unit (OU) display specifier (for example, CN=organizationalUnit-Display,CN=409,CN=DisplaySpecifiers) and copies the values of the **extraColumns** attribute of the default display (for example, CN=default-Display, CN=409,CN=DisplaySpecifiers).</span></span>

  - <span data-ttu-id="69b7f-198">Agrega **atributos msRTCSIP-PrimaryUserAddress**, **msRTCSIP-PrimaryHomeServer** y **msRTCSIP-UserEnabled** al atributo **attributeDisplayNames** de cada especificador de visualización de idioma para los objetos users, Contacts e INETORGPERSON (por ejemplo, en Inglés: CN = user-Display, CN = 409, CN = DisplaySpecifiers).</span><span class="sxs-lookup"><span data-stu-id="69b7f-198">Adds **msRTCSIP-PrimaryUserAddress**, **msRTCSIP-PrimaryHomeServer**, and **msRTCSIP-UserEnabled** filtering attributes under the **attributeDisplayNames** attribute of each language display specifier for Users, Contacts, and InetOrgPerson objects (for example, in English: CN=user-Display,CN=409,CN=DisplaySpecifiers).</span></span>

<span data-ttu-id="69b7f-199"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69b7f-199"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

