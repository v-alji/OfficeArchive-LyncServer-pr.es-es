---
title: 'Lync Server 2013: Requisitos para la pertenencia a grupos'
description: 'Lync Server 2013: requisitos de pertenencia a grupos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group membership requirements
ms:assetid: 01876843-8717-4e72-baf5-866ac8cceee6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204623(v=OCS.15)
ms:contentKeyID: 48183239
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f18fb6fbc782ecd41b7a782965f2cd6a82f6fd5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427841"
---
# <a name="group-membership-requirements-for-lync-server-2013"></a><span data-ttu-id="f81c8-103">Requisitos para la pertenencia a grupos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f81c8-103">Group membership requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f81c8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f81c8-104">

<span> </span></span></span>

<span data-ttu-id="f81c8-105">_**Última modificación del tema:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="f81c8-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="f81c8-106">En la tabla siguiente se resume el grupo o los grupos a los que debe pertenecer una persona para poder instalar, administrar y solucionar problemas de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f81c8-106">The following table summarizes the group or groups that a person should belong to in order to successfully install, manage, and troubleshoot Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f81c8-107">Ejecutable 2013 de Lync Server</span><span class="sxs-lookup"><span data-stu-id="f81c8-107">Lync Server 2013 Executable</span></span></th>
<th><span data-ttu-id="f81c8-108">Se requiere pertenencia al grupo</span><span class="sxs-lookup"><span data-stu-id="f81c8-108">Group Membership Required</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f81c8-109"><strong>Setup.exe</strong> : ejecutable que inicia la instalación de las herramientas administrativas 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f81c8-109"><strong>Setup.exe</strong> – Executable that starts the installation of the Lync Server 2013 administrative tools.</span></span></p></td>
<td><p><span data-ttu-id="f81c8-110">Miembro del grupo de administradores locales en el equipo desde el que se ejecuta el ejecutable.</span><span class="sxs-lookup"><span data-stu-id="f81c8-110">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="f81c8-111">Miembro del grupo usuarios del dominio para leer la información de los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f81c8-111">Member of Domain Users group to read information in Active Directory Domain Services.</span></span> <span data-ttu-id="f81c8-112">Este nivel de permisos es necesario porque la instalación automática de paquetes MSI necesarios en el equipo local requiere privilegios que permitan leer y escribir en recursos de equipos locales protegidos, como directorios de archivos de programa y el registro protegido, como el subárbol del equipo local.</span><span class="sxs-lookup"><span data-stu-id="f81c8-112">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span></p>
<div>

> [!TIP]  
> <span data-ttu-id="f81c8-113">También puede delegar permisos de configuración a los usuarios o grupos a los que no desee conceder la pertenencia al grupo administradores de dominio.</span><span class="sxs-lookup"><span data-stu-id="f81c8-113">You can also delegate setup permissions to users or groups to whom you do not want to grant membership in the Domain Admins group.</span></span> <span data-ttu-id="f81c8-114">Para obtener más información, vea <A href="lync-server-2013-granting-setup-permissions.md">conceder permisos de configuración en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="f81c8-114">For details, see <A href="lync-server-2013-granting-setup-permissions.md">Granting setup permissions in Lync Server 2013</A> in the Deployment documentation.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f81c8-115"><strong>Deploy.exe</strong> : setup.exe, deploy.exe es responsable de la implementación de los componentes de software para los roles de servidor.</span><span class="sxs-lookup"><span data-stu-id="f81c8-115"><strong>Deploy.exe</strong> – Called by setup.exe, deploy.exe is responsible for the deployment of the software components for the server roles.</span></span></p></td>
<td><p><span data-ttu-id="f81c8-116">Miembro del grupo de administradores locales en el equipo desde el que se ejecuta el ejecutable.</span><span class="sxs-lookup"><span data-stu-id="f81c8-116">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="f81c8-117">Miembro del grupo usuarios del dominio para leer la información de AD DS.</span><span class="sxs-lookup"><span data-stu-id="f81c8-117">Member of Domain Users group to read information in AD DS.</span></span> <span data-ttu-id="f81c8-118">Este nivel de permisos es necesario porque la instalación automática de paquetes MSI necesarios en el equipo local requiere privilegios que permitan leer y escribir en recursos de equipos locales protegidos, como directorios de archivos de programa y el registro protegido, como el subárbol del equipo local.</span><span class="sxs-lookup"><span data-stu-id="f81c8-118">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span> <span data-ttu-id="f81c8-119">Es necesario pertenecer al grupo RtcUniversalReadOnlyAdmins para leer el almacén de administración central.</span><span class="sxs-lookup"><span data-stu-id="f81c8-119">Membership in RtcUniversalReadOnlyAdmins group is necessary to read the Central Management store.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="f81c8-120">Si está ejecutando el sistema operativo Windows Vista o Windows 7, el control de cuentas de usuario (UAC) le pedirá que continúe con la instalación.</span><span class="sxs-lookup"><span data-stu-id="f81c8-120">If you are running the Windows Vista operating system or Windows 7 operating system, you will be prompted by User Account Control (UAC) to proceed with installation.</span></span> <span data-ttu-id="f81c8-121">Si ha iniciado sesión con una cuenta de usuario estándar, necesitará una persona que sea miembro del grupo de administradores locales para proporcionar credenciales cuando se le pida una cuenta con permisos para instalar el software.</span><span class="sxs-lookup"><span data-stu-id="f81c8-121">If you are logged on with a standard user account, you will need someone who is a member of the Local Administrators group to provide credentials when prompted for an account with permissions to install the software.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f81c8-122"><strong>Bootstrapper.exe</strong> : setup.exe, bootstrapper.exe es responsable de la implementación y la configuración de los roles de servidor.</span><span class="sxs-lookup"><span data-stu-id="f81c8-122"><strong>Bootstrapper.exe</strong> – Called by setup.exe, bootstrapper.exe is responsible for deployment and configuration of server roles.</span></span></p></td>
<td><p><span data-ttu-id="f81c8-123">Miembro del grupo de administradores locales en el equipo desde el que se ejecuta el ejecutable.</span><span class="sxs-lookup"><span data-stu-id="f81c8-123">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="f81c8-124">Miembro del grupo RTCUniversalServerAdmins para ejecutar Bootstrapper.exe.</span><span class="sxs-lookup"><span data-stu-id="f81c8-124">Member of the RTCUniversalServerAdmins group to run Bootstrapper.exe.</span></span> <span data-ttu-id="f81c8-125">Miembro del grupo usuarios del dominio para leer la información de AD DS.</span><span class="sxs-lookup"><span data-stu-id="f81c8-125">Member of Domain Users group to read information in AD DS.</span></span> <span data-ttu-id="f81c8-126">Este nivel de permisos es necesario porque la instalación automática de paquetes MSI necesarios en el equipo local requiere privilegios que permitan leer y escribir en recursos de equipos locales protegidos, como directorios de archivos de programa y el registro protegido, como el subárbol del equipo local.</span><span class="sxs-lookup"><span data-stu-id="f81c8-126">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f81c8-127"><strong>TopologyBuilder</strong> : interfaz de usuario guiada por asistente para crear, ver, ajustar y validar topologías de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f81c8-127"><strong>TopologyBuilder</strong> – Wizard-driven user interface to create, view, adjust, and validate Lync Server 2013 topologies.</span></span></p></td>
<td><p><span data-ttu-id="f81c8-128">Miembro del grupo de administradores locales en el equipo desde el que se ejecuta el ejecutable para ver la topología.</span><span class="sxs-lookup"><span data-stu-id="f81c8-128">Member of the Local Administrators group on the computer from which the executable is run to view the topology.</span></span> <span data-ttu-id="f81c8-129">Miembro del grupo RTCUniversalServerAdmins para cambiar los valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="f81c8-129">Member of the RTCUniversalServerAdmins group to change configuration settings.</span></span> <span data-ttu-id="f81c8-130">Miembro del grupo RTCUniversalServerAdmins y del grupo administradores de dominio, o miembro del grupo RTCUniversalServerAdmins (solo si se le han otorgado permisos de configuración de delegado), para publicar la topología.</span><span class="sxs-lookup"><span data-stu-id="f81c8-130">Member of the RTCUniversalServerAdmins group and Domain Admins group, or member of the RTCUniversalServerAdmins group (only if the group has been granted delegate setup permissions), to publish the topology.</span></span> <span data-ttu-id="f81c8-131">Para obtener más información sobre cómo delegar permisos de configuración para permitir que los miembros del grupo RTCUniversalServerAdmins publiquen la topología sin ser miembros del grupo administradores de dominio, vea <a href="lync-server-2013-granting-setup-permissions.md">conceder permisos de configuración en Lync Server 2013</a> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="f81c8-131">For details about delegating setup permissions to allow members of the RTCUniversalServerAdmins group to publish the topology without being members of the Domain Admins group, see <a href="lync-server-2013-granting-setup-permissions.md">Granting setup permissions in Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f81c8-132"><strong>AdminUIHost</strong> : interfaz gráfica de usuario basada en web para administrar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f81c8-132"><strong>AdminUIHost</strong> – Web-based graphical user interface for managing Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="f81c8-133">Miembro de CsAdministrator grupo o miembro de otra función de control de acceso basado en roles (RBAC) a la que se asigna la tarea administrativa específica.</span><span class="sxs-lookup"><span data-stu-id="f81c8-133">Member of CsAdministrator group or member of another role-based access control (RBAC) role to which the specific administrative task is assigned.</span></span> <span data-ttu-id="f81c8-134">El panel de control 2013 de Lync Server implementa los cambios de configuración ejecutando los cmdlets del shell de administración de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f81c8-134">Lync Server 2013 Control Panel implements configuration changes by running Lync Server 2013 Management Shell cmdlets.</span></span> <span data-ttu-id="f81c8-135">Para obtener una lista de los roles predefinidos y permitir la ejecución de los miembros de cmdlets, consulte <a href="lync-server-2013-planning-for-role-based-access-control.md">planificación de control de acceso basado en roles en Lync Server 2013</a> en la documentación de planificación.</span><span class="sxs-lookup"><span data-stu-id="f81c8-135">For a list of predefined roles and the cmdlets members are permitted to run, see <a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f81c8-136"><strong>PowerShell.exe con el módulo de Lync server 2013 cargado</strong> : herramienta administrativa de línea de comandos con cmdlets específicos para la administración de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f81c8-136"><strong>PowerShell.exe with the Lync Server 2013 module loaded</strong> – Command-line administrative tool with cmdlets specific to management of Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="f81c8-137">Miembro de CsAdministrator grupo o miembro de otro rol RBAC al que se ha asignado el cmdlet específico.</span><span class="sxs-lookup"><span data-stu-id="f81c8-137">Member of CsAdministrator group or member of another RBAC role to which the specific cmdlet has been assigned.</span></span> <span data-ttu-id="f81c8-138">Para obtener una lista de los roles predefinidos y permitir la ejecución de los miembros de cmdlets, consulte <a href="lync-server-2013-planning-for-role-based-access-control.md">planificación de control de acceso basado en roles en Lync Server 2013</a> en la documentación de planificación.</span><span class="sxs-lookup"><span data-stu-id="f81c8-138">For a list of predefined roles and the cmdlets members are permitted to run, see <a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="f81c8-139">O miembro de uno o más de los siguientes grupos, según el cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f81c8-139">Or, member of one or more of the following groups, depending on the cmdlet:</span></span></p>
<ul>
<li><p><span data-ttu-id="f81c8-140">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="f81c8-140">RTCUniversalServerAdmins</span></span></p></li>
<li><p><span data-ttu-id="f81c8-141">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="f81c8-141">RTCUniversalUserAdmins</span></span></p></li>
<li><p><span data-ttu-id="f81c8-142">RTCUniversalReadOnlyAdmins</span><span class="sxs-lookup"><span data-stu-id="f81c8-142">RTCUniversalReadOnlyAdmins</span></span></p></li>
</ul></td>
</tr><span data-ttu-id="f81c8-143">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f81c8-143">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

