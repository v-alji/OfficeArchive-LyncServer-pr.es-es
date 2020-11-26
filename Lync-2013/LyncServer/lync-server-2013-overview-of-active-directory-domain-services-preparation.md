---
title: 'Lync Server 2013: Información general sobre la preparación de los Servicios de dominio de Active Directory'
description: 'Lync Server 2013: información general sobre la preparación de los servicios de dominio de Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Active Directory Domain Services preparation
ms:assetid: cdd2a652-6a0d-4728-9950-3fcaa7a80066
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398869(v=OCS.15)
ms:contentKeyID: 48185662
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18b22e11a73ad7a181e2eaf887b1b49b934d9db5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445165"
---
# <a name="overview-of-active-directory-domain-services-preparation-in-lync-server-2013"></a><span data-ttu-id="dad74-103">Información general sobre la preparación de los Servicios de dominio de Active Directory en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dad74-103">Overview of Active Directory Domain Services preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dad74-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dad74-104">

<span> </span></span></span>

<span data-ttu-id="dad74-105">_**Última modificación del tema:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="dad74-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="dad74-106">Para preparar los servicios de dominio de Active Directory para la implementación de Lync Server 2013, debe realizar tres pasos en una secuencia específica.</span><span class="sxs-lookup"><span data-stu-id="dad74-106">To prepare Active Directory Domain Services for your Lync Server 2013 deployment, you must perform three steps in a specific sequence.</span></span>

<span data-ttu-id="dad74-107">En la tabla siguiente se describen los pasos necesarios para preparar AD DS para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dad74-107">The following table describes the steps required to prepare AD DS for Lync Server.</span></span>

### <a name="active-directory-preparation-steps"></a><span data-ttu-id="dad74-108">Pasos de preparación de Active Directory</span><span class="sxs-lookup"><span data-stu-id="dad74-108">Active Directory Preparation Steps</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="dad74-109">Paso</span><span class="sxs-lookup"><span data-stu-id="dad74-109">Step</span></span></th>
<th><span data-ttu-id="dad74-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="dad74-110">Description</span></span></th>
<th><span data-ttu-id="dad74-111">Donde se ejecuta</span><span class="sxs-lookup"><span data-stu-id="dad74-111">Where run</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.</p></td>
<td><p><span data-ttu-id="dad74-112"><a href="lync-server-2013-preparing-the-active-directory-schema.md">Preparación del esquema de Active Directory en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="dad74-112"><a href="lync-server-2013-preparing-the-active-directory-schema.md">Preparing the Active Directory schema in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="dad74-113">Extiende el esquema de Active Directory agregando nuevas clases y atributos usados por Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dad74-113">Extends the Active Directory schema by adding new classes and attributes that are used by Lync Server.</span></span></p>
<p><span data-ttu-id="dad74-114">Se ejecuta una vez para cada bosque de su implementación donde se implementará Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dad74-114">Run once for each forest in your deployment where Lync Server will be deployed.</span></span></p></td>
<td><p><span data-ttu-id="dad74-115">Contra el maestro de esquema en el dominio raíz de cada bosque donde se va a implementar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dad74-115">Against the schema master in the root domain of each forest where Lync Server will be deployed.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="dad74-116">No es necesario ejecutar este paso en el dominio raíz si tiene permisos en el maestro de esquema, pero debe ser miembro del grupo de administradores de esquema en el dominio raíz y miembro del grupo de administradores de empresa en el maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="dad74-116">You do not need to run this step in the root domain if you have permissions on the schema master, but you must be a member of the Schema Admins group in the root domain and a member of the Enterprise Admins group on the schema master.</span></span> <span data-ttu-id="dad74-117">En una topología de bosque de recursos, ejecute este paso solo en el bosque de recursos, no en los bosques de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="dad74-117">In a resource forest topology, run this step only in the resource forest, not in any user forests.</span></span> <span data-ttu-id="dad74-118">En una topología de bosque central, ejecute este paso solo en el bosque central, no en los bosques de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="dad74-118">In a central forest topology, run this step only in the central forest, not in any user forests.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p>2.</p></td>
<td><p><span data-ttu-id="dad74-119"><a href="lync-server-2013-preparing-the-forest.md">Preparación del bosque para Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="dad74-119"><a href="lync-server-2013-preparing-the-forest.md">Preparing the forest for Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="dad74-120">Crea la configuración global y los grupos universales usados por Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dad74-120">Creates global settings and universal groups that are used by Lync Server.</span></span></p>
<p><span data-ttu-id="dad74-121">Se ejecuta una vez para cada bosque de su implementación donde se implementará Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dad74-121">Run once for each forest in your deployment where Lync Server will be deployed.</span></span></p></td>
<td><p><span data-ttu-id="dad74-122">En el dominio raíz de cada bosque donde se va a implementar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dad74-122">In the root domain of each forest where Lync Server will be deployed.</span></span> <span data-ttu-id="dad74-123">Para ejecutar este paso, debe ser miembro del grupo administradores de la empresa.</span><span class="sxs-lookup"><span data-stu-id="dad74-123">To run this step, you must be a member of the Enterprise Admins group.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="dad74-124">En una topología de bosque de recursos, ejecute este paso solo en el bosque de recursos, no en los bosques de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="dad74-124">In a resource forest topology, run this step only in the resource forest, not in any user forests.</span></span> <span data-ttu-id="dad74-125">En una topología de bosque central, ejecute este paso solo en el bosque central, no en los bosques de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="dad74-125">In a central forest topology, run this step only in the central forest, not in any user forests.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p>3.</p></td>
<td><p><span data-ttu-id="dad74-126"><a href="lync-server-2013-preparing-domains.md">Preparar dominios para Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="dad74-126"><a href="lync-server-2013-preparing-domains.md">Preparing domains for Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="dad74-127">Agrega permisos sobre los objetos que usarán los miembros de los grupos universales.</span><span class="sxs-lookup"><span data-stu-id="dad74-127">Adds permissions on objects to be used by members of universal groups.</span></span></p>
<p><span data-ttu-id="dad74-128">Ejecutar una vez por dominio de usuario o dominio de servidor.</span><span class="sxs-lookup"><span data-stu-id="dad74-128">Run once per user domain or server domain.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="dad74-129">Si va a migrar de Lync Server 2010 a Lync Server 2013, es posible que el Asistente para la implementación indique que ya se ha completado la preparación del dominio.</span><span class="sxs-lookup"><span data-stu-id="dad74-129">If you are migrating from Lync Server 2010 to Lync Server 2013, the Deployment Wizard may indicate that domain preparation is already complete.</span></span> <span data-ttu-id="dad74-130">No es necesario volver a ejecutar la preparación del dominio.</span><span class="sxs-lookup"><span data-stu-id="dad74-130">You do not need to run domain preparation again.</span></span> <span data-ttu-id="dad74-131">No se cambiaron los permisos de Lync Server 2010 a Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dad74-131">Permissions were not changed from Lync Server 2010 to Lync Server 2013.</span></span>


</div></td>
<td><p><span data-ttu-id="dad74-132">En un servidor miembro de cada dominio donde se va a implementar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dad74-132">On a member server in each domain where Lync Server will be deployed.</span></span> <span data-ttu-id="dad74-133">Para ejecutar este paso, debe ser miembro del grupo administradores de dominio.</span><span class="sxs-lookup"><span data-stu-id="dad74-133">To run this step, you must be a member of the Domain Admins group.</span></span></p></td>
</tr>
</tbody>
</table>


<div id="sectionSection0" class="section">

<span data-ttu-id="dad74-134">Lync Server 2013, al igual que Lync Server 2010, almacena gran parte de la información de configuración en el almacén central de administración en lugar de en AD DS como sucede en Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="dad74-134">Lync Server 2013, like Lync Server 2010, stores much of the configuration information in the Central Management store instead of in AD DS as was the case in Office Communications Server 2007 R2.</span></span> <span data-ttu-id="dad74-135">Sin embargo, la siguiente información se almacena en AD DS:</span><span class="sxs-lookup"><span data-stu-id="dad74-135">However, the following information is stored in AD DS:</span></span>

  - <span data-ttu-id="dad74-136">**Extensiones de esquema**:</span><span class="sxs-lookup"><span data-stu-id="dad74-136">**Schema extensions**:</span></span>
    
      - <span data-ttu-id="dad74-137">Extensiones de objetos de usuario</span><span class="sxs-lookup"><span data-stu-id="dad74-137">User object extensions</span></span>
    
      - <span data-ttu-id="dad74-138">Extensiones para las clases de Office Communications Server 2007 R2 para mantener la compatibilidad con versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="dad74-138">Extensions for Office Communications Server 2007 R2 classes to maintain backward compatibility</span></span>

<!-- end list -->

  - <span data-ttu-id="dad74-139">**Datos** (almacenados en el esquema extendido de Lync Server y en las clases de esquema existentes):</span><span class="sxs-lookup"><span data-stu-id="dad74-139">**Data** (stored in Lync Server extended schema and in existing schema classes):</span></span>
    
      - <span data-ttu-id="dad74-140">Identificador uniforme de recursos (URI) SIP de usuario y otra configuración de usuario</span><span class="sxs-lookup"><span data-stu-id="dad74-140">User SIP Uniform Resource Identifier (URI) and other user settings</span></span>
    
      - <span data-ttu-id="dad74-141">Objetos de contacto para aplicaciones como el operador de conferencia y el grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="dad74-141">Contact objects for applications such as Response Group and Conferencing Attendant</span></span>
    
      - <span data-ttu-id="dad74-142">Puntero al almacén de administración central</span><span class="sxs-lookup"><span data-stu-id="dad74-142">A pointer to the Central Management store</span></span>
    
      - <span data-ttu-id="dad74-143">Cuenta de autenticación Kerberos (un objeto de equipo opcional)</span><span class="sxs-lookup"><span data-stu-id="dad74-143">Kerberos Authentication Account (an optional computer object)</span></span>

<span data-ttu-id="dad74-144">En Lync Server 2013, delega la configuración y la administración al otorgar permisos de configuración al grupo universal de RTCUniversalServerAdmins para que los miembros de ese grupo puedan instalar y activar Lync Server 2013 en un servidor local (después de que el servidor se haya agregado a la topología, se haya publicado y se haya habilitado).</span><span class="sxs-lookup"><span data-stu-id="dad74-144">In Lync Server 2013, you delegate setup and administration by granting setup permissions to the RTCUniversalServerAdmins universal group so that members of that group can install and activate Lync Server 2013 on a local server (after the server has been added to the topology, published, and enabled).</span></span> <span data-ttu-id="dad74-145">Los usuarios delegados deben ser administradores locales en el equipo en el que están instalando y activando Lync Server 2013, pero no es necesario que sean miembros del grupo administradores de dominio.</span><span class="sxs-lookup"><span data-stu-id="dad74-145">The delegated users must be local administrators on the computer where they are installing and activating Lync Server 2013, but they do not need to be members of the Domain Admins group.</span></span> <span data-ttu-id="dad74-146">También puede conceder permisos a los objetos de unidades organizativas (OU) especificadas para que los miembros de los grupos universales creados durante la preparación del bosque puedan tener acceso a esos objetos sin ser miembros del grupo administradores del dominio.</span><span class="sxs-lookup"><span data-stu-id="dad74-146">You can also grant permissions for objects in specified organizational units (OUs) so that members of the universal groups created during forest preparation can access those objects without being members of the Domain Admins group.</span></span>

<span data-ttu-id="dad74-147">Para implementaciones nuevas de Lync Server 2013, la configuración global debe almacenarse en el contenedor de configuración.</span><span class="sxs-lookup"><span data-stu-id="dad74-147">For new deployments of Lync Server 2013, global settings must be stored in the Configuration container.</span></span> <span data-ttu-id="dad74-148">Si su organización está actualizando desde una versión anterior y aún así tiene una configuración global en el contenedor del sistema, el contenedor del sistema aún es compatible.</span><span class="sxs-lookup"><span data-stu-id="dad74-148">If your organization is upgrading from an earlier version and you still have global settings in the System container, the System container is still supported.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dad74-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="dad74-149">See Also</span></span>


[<span data-ttu-id="dad74-150">Preparación del esquema de Active Directory en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dad74-150">Preparing the Active Directory schema in Lync Server 2013</span></span>](lync-server-2013-preparing-the-active-directory-schema.md)  
[<span data-ttu-id="dad74-151">Extensiones de esquema, clases y atributos de Active Directory usados por Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dad74-151">Active Directory schema extensions, classes, and attributes used by Lync Server 2013</span></span>](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md)  


[<span data-ttu-id="dad74-152">Preparación del bosque para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dad74-152">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
[<span data-ttu-id="dad74-153">Preparar dominios para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dad74-153">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="dad74-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dad74-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

