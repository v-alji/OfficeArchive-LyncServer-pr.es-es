---
title: 'Lync Server 2013: cuentas de usuario habilitadas para Lync Server'
description: 'Lync Server 2013: cuentas de usuario habilitadas para Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User accounts enabled for Lync Server 2013
ms:assetid: 8021087e-5084-4a39-9fef-ab9376c6d371
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182543(v=OCS.15)
ms:contentKeyID: 48184651
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf87177c378ffe61715d5332d2fd23b1d8e6fce6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399432"
---
# <a name="user-accounts-enabled-for-lync-server-2013"></a><span data-ttu-id="f50d8-103">Cuentas de usuario habilitadas para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f50d8-103">User accounts enabled for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f50d8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f50d8-104">

<span> </span></span></span>

<span data-ttu-id="f50d8-105">_**Última modificación del tema:** 2014-04-18_</span><span class="sxs-lookup"><span data-stu-id="f50d8-105">_**Topic Last Modified:** 2014-04-18_</span></span>

<span data-ttu-id="f50d8-106">Los temas de esta sección proporcionan procedimientos paso a paso para configurar las opciones de usuario que puede realizar con el panel de control de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f50d8-106">Topics in this section provide step-by-step procedures for configuring user settings that you can perform using the Lync Server 2013 Control Panel.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f50d8-107">No puede usar el panel de control de Lync Server para administrar los usuarios que son miembros del grupo administradores de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f50d8-107">You cannot use Lync Server Control Panel to manage users who are members of the Active Directory Domain Admins group.</span></span> <span data-ttu-id="f50d8-108">Para los usuarios de administradores de dominio, puede usar el panel de control de Lync Server solo para realizar operaciones de búsqueda de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f50d8-108">For Domain Admins users, you can use Lync Server Control Panel only to perform read-only search operations.</span></span> <span data-ttu-id="f50d8-109">Para realizar operaciones de escritura en los usuarios de administradores de dominio (por ejemplo, habilitar o deshabilitar el panel de control de Lync Server, cambiar las asignaciones de directivas, la configuración de telefonía, la dirección SIP), debe usar los cmdlets de Windows PowerShell al iniciar sesión como un usuario administrador de dominio.</span><span class="sxs-lookup"><span data-stu-id="f50d8-109">To perform write operations on Domain Admins users (for example, enable or disable for Lync Server Control Panel, change pool or policy assignments, telephony settings, SIP address), you must use Windows PowerShell cmdlets while logged on as a Domain Admins user.</span></span> <span data-ttu-id="f50d8-110">Para obtener más información sobre cómo usar los cmdlets de Windows PowerShell para administrar usuarios, consulte <A href="lync-server-2013-lync-server-management-shell.md">consola de administración de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="f50d8-110">For details about using Windows PowerShell cmdlets to manage users, see <A href="lync-server-2013-lync-server-management-shell.md">Lync Server 2013 Management Shell</A>.</span></span>



</div>

<span data-ttu-id="f50d8-111">Al realizar cualquier tarea administrativa de Lync Server 2013 que implique buscar un usuario o filtrar los resultados de la búsqueda de usuarios, hay algunas propiedades de usuario que existen como atributos en los servicios de dominio de Active Directory, pero que no se replican en el catálogo global hasta que se implemente Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f50d8-111">When you perform any Lync Server 2013 administrative task that involves searching for a user or filtering user search results, there are some user properties that exist as attributes in Active Directory Domain Services but are not replicated to the global catalog until Microsoft Exchange Server is deployed.</span></span> <span data-ttu-id="f50d8-112">Microsoft Exchange, no Lync Server, marca los siguientes atributos para la replicación en el catálogo global cuando está instalado:</span><span class="sxs-lookup"><span data-stu-id="f50d8-112">Microsoft Exchange, not Lync Server, marks the following attributes for replication to the global catalog when it is installed:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f50d8-113">Información de usuario</span><span class="sxs-lookup"><span data-stu-id="f50d8-113">User Information</span></span></th>
<th><span data-ttu-id="f50d8-114">Dirección y teléfono</span><span class="sxs-lookup"><span data-stu-id="f50d8-114">Address and Phone</span></span></th>
<th><span data-ttu-id="f50d8-115">Organización</span><span class="sxs-lookup"><span data-stu-id="f50d8-115">Organization</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f50d8-116">Iniciales</span><span class="sxs-lookup"><span data-stu-id="f50d8-116">Initials</span></span></p></td>
<td><p><span data-ttu-id="f50d8-117">Dirección</span><span class="sxs-lookup"><span data-stu-id="f50d8-117">Street address</span></span></p>
<p><span data-ttu-id="f50d8-118">País o región</span><span class="sxs-lookup"><span data-stu-id="f50d8-118">Country/region</span></span></p>
<p><span data-ttu-id="f50d8-119">Localizador</span><span class="sxs-lookup"><span data-stu-id="f50d8-119">Pager</span></span></p>
<p><span data-ttu-id="f50d8-120">Fax</span><span class="sxs-lookup"><span data-stu-id="f50d8-120">Fax</span></span></p>
<p><span data-ttu-id="f50d8-121">Móvil</span><span class="sxs-lookup"><span data-stu-id="f50d8-121">Mobile</span></span></p></td>
<td><p><span data-ttu-id="f50d8-122">Título</span><span class="sxs-lookup"><span data-stu-id="f50d8-122">Title</span></span></p>
<p><span data-ttu-id="f50d8-123">Compañía</span><span class="sxs-lookup"><span data-stu-id="f50d8-123">Company</span></span></p>
<p><span data-ttu-id="f50d8-124">Grandes</span><span class="sxs-lookup"><span data-stu-id="f50d8-124">Department</span></span></p>
<p><span data-ttu-id="f50d8-125">Office</span><span class="sxs-lookup"><span data-stu-id="f50d8-125">Office</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="f50d8-126">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f50d8-126">In This Section</span></span>

  - [<span data-ttu-id="f50d8-127">Ver información sobre las cuentas de usuario habilitadas para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f50d8-127">Viewing information about user accounts enabled for Lync Server 2013</span></span>](lync-server-2013-viewing-information-about-user-accounts-enabled-for-lync-server.md)

  - [<span data-ttu-id="f50d8-128">Habilitar y deshabilitar usuarios para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f50d8-128">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)

  - [<span data-ttu-id="f50d8-129">Administración de telefonía IP empresarial para usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f50d8-129">Managing Enterprise Voice for users in Lync Server 2013</span></span>](lync-server-2013-managing-enterprise-voice-for-users.md)

  - [<span data-ttu-id="f50d8-130">Modificar las propiedades de la cuenta de usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f50d8-130">Modifying user account properties in Lync Server 2013</span></span>](lync-server-2013-modifying-user-account-properties.md)

  - [<span data-ttu-id="f50d8-131">Administrar la directiva de acceso de la organización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f50d8-131">Manage external access policy in Lync Server 2013</span></span>](lync-server-2013-manage-external-access-policy-for-your-organization.md)

  - [<span data-ttu-id="f50d8-132">Asignación de directivas por usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f50d8-132">Assigning per-user policies in Lync Server 2013</span></span>](lync-server-2013-assigning-per-user-policies.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f50d8-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f50d8-133">See Also</span></span>


[<span data-ttu-id="f50d8-134">Cmdlets de administración de usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f50d8-134">User management cmdlets in Lync Server 2013</span></span>](lync-server-2013-user-management-cmdlets.md)  


[<span data-ttu-id="f50d8-135">Administración de usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f50d8-135">Managing users in Lync Server 2013</span></span>](lync-server-2013-managing-users-in-lync-server.md)  
  

<span data-ttu-id="f50d8-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f50d8-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

