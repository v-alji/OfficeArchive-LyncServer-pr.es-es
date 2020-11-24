---
title: 'Lync Server 2013: Compatibilidad de servicios de dominio de Active Directory'
description: 'Lync Server 2013: compatibilidad con los servicios de dominio de Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory Domain Services support
ms:assetid: aeb62d5e-e424-473a-b795-9452150c98dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412831(v=OCS.15)
ms:contentKeyID: 48185136
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb2a85bab90557c28c4802721d4202f6188cb3f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398033"
---
# <a name="active-directory-domain-services-support-in-lync-server-2013"></a><span data-ttu-id="a9064-103">Compatibilidad de servicios de dominio de Active Directory en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9064-103">Active Directory Domain Services support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a9064-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a9064-104">

<span> </span></span></span>

<span data-ttu-id="a9064-105">_**Última modificación del tema:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="a9064-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="a9064-106">Lync Server 2013 usa el almacén de administración central para almacenar los datos de configuración de servidores y servicios, en lugar de depender de los servicios de dominio de Active Directory para esta información, como en el pasado.</span><span class="sxs-lookup"><span data-stu-id="a9064-106">Lync Server 2013 uses the Central Management store to store configuration data for servers and services, instead of relying on Active Directory Domain Services for this information, as in the past.</span></span> <span data-ttu-id="a9064-107">Lync Server 2013 sigue almacenando lo siguiente en AD DS:</span><span class="sxs-lookup"><span data-stu-id="a9064-107">Lync Server 2013 still stores the following in AD DS:</span></span>

  - <span data-ttu-id="a9064-108">**Extensiones de esquema**</span><span class="sxs-lookup"><span data-stu-id="a9064-108">**Schema extensions**</span></span>
    
      - <span data-ttu-id="a9064-109">Extensiones de objetos de usuario</span><span class="sxs-lookup"><span data-stu-id="a9064-109">User object extensions</span></span>
    
      - <span data-ttu-id="a9064-110">Extensiones de Lync Server 2010 y las clases de Office Communications Server 2007 R2 para mantener la compatibilidad con versiones anteriores compatibles</span><span class="sxs-lookup"><span data-stu-id="a9064-110">Extensions for Lync Server 2010 and Office Communications Server 2007 R2 classes to maintain backward compatibility with previous supported versions</span></span>

  - <span data-ttu-id="a9064-111">**Datos** (almacenados en el esquema extendido de Lync Server 2013 y en las clases existentes)</span><span class="sxs-lookup"><span data-stu-id="a9064-111">**Data** (stored in Lync Server 2013 extended schema and in existing classes)</span></span>
    
      - <span data-ttu-id="a9064-112">URI de SIP del usuario y otros parámetros de usuario</span><span class="sxs-lookup"><span data-stu-id="a9064-112">User SIP URI and other user settings</span></span>
    
      - <span data-ttu-id="a9064-113">Objetos de contacto para aplicaciones (por ejemplo, la aplicación de grupo de respuesta y la aplicación de operador de conferencia)</span><span class="sxs-lookup"><span data-stu-id="a9064-113">Contact objects for applications (for example, the Response Group application and the Conferencing Attendant application)</span></span>
    
      - <span data-ttu-id="a9064-114">Datos publicados para la compatibilidad con versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="a9064-114">Data published for backward compatibility</span></span>
    
      - <span data-ttu-id="a9064-115">Un punto de control de servicio (SCP) para el almacén de administración central</span><span class="sxs-lookup"><span data-stu-id="a9064-115">A service control point (SCP) for the Central Management store</span></span>
    
      - <span data-ttu-id="a9064-116">Cuenta de autenticación Kerberos (un objeto de equipo opcional)</span><span class="sxs-lookup"><span data-stu-id="a9064-116">Kerberos Authentication Account (an optional computer object)</span></span>

<span data-ttu-id="a9064-117">En esta sección se describen los requisitos de compatibilidad de AD DS para Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a9064-117">This section describes the AD DS support requirements for Lync Server 2013.</span></span> <span data-ttu-id="a9064-118">Para obtener más información sobre la compatibilidad de topología, consulte [topologías de Active Directory admitidas en Lync Server 2013](lync-server-2013-supported-active-directory-topologies.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="a9064-118">For details about topology support, see [Supported Active Directory topologies in Lync Server 2013](lync-server-2013-supported-active-directory-topologies.md) in the Supportability documentation.</span></span>

<div>

## <a name="supported-domain-controller-operating-systems"></a><span data-ttu-id="a9064-119">Sistemas operativos de controlador de dominio compatibles</span><span class="sxs-lookup"><span data-stu-id="a9064-119">Supported Domain Controller Operating Systems</span></span>

<span data-ttu-id="a9064-120">Lync Server 2013 admite controladores de dominio que ejecutan los siguientes sistemas operativos:</span><span class="sxs-lookup"><span data-stu-id="a9064-120">Lync Server 2013 supports domain controllers running the following operating systems:</span></span>

  - <span data-ttu-id="a9064-121">Sistema operativo Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a9064-121">Windows Server 2012 R2 operating system</span></span>

  - <span data-ttu-id="a9064-122">Sistema operativo Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9064-122">Windows Server 2012 operating system</span></span>

  - <span data-ttu-id="a9064-123">Sistema operativo Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9064-123">Windows Server 2008 R2 operating system</span></span>

  - <span data-ttu-id="a9064-124">Sistema operativo Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9064-124">Windows Server 2008 operating system</span></span>

  - <span data-ttu-id="a9064-125">Windows Server 2008 Enterprise 32 bits</span><span class="sxs-lookup"><span data-stu-id="a9064-125">Windows Server 2008 Enterprise 32-Bit</span></span>

  - <span data-ttu-id="a9064-126">Las versiones de 32 o 64 bits del sistema operativo Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a9064-126">The 32-bit or 64-bit versions of the Window Server 2003 R2 operating system</span></span>

  - <span data-ttu-id="a9064-127">Las versiones de 32 o 64 bits del sistema operativo Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9064-127">The 32-bit or 64-bit versions of the Windows Server 2003 operating system</span></span>

</div>

<div>

## <a name="forest-and-domain-functional-level"></a><span data-ttu-id="a9064-128">Nivel funcional de bosque y dominio</span><span class="sxs-lookup"><span data-stu-id="a9064-128">Forest and Domain Functional Level</span></span>

<span data-ttu-id="a9064-129">Debe elevar todos los dominios en los que implementa Lync Server 2013 a un nivel funcional de dominio de Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 o, como mínimo, Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a9064-129">You must raise all domains in which you deploy Lync Server 2013 to a domain functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>

<span data-ttu-id="a9064-130">Todos los bosques en los que implemente Lync Server 2013 deben elevarse al nivel funcional de bosque de Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 o al menos Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a9064-130">All forests in which you deploy Lync Server 2013 must be raised to a forest functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>

</div>

<div>

## <a name="support-for-read-only-domain-controllers"></a><span data-ttu-id="a9064-131">Compatibilidad con Read-Only controladores de dominio</span><span class="sxs-lookup"><span data-stu-id="a9064-131">Support for Read-Only Domain Controllers</span></span>

<span data-ttu-id="a9064-132">Lync Server 2013 admite implementaciones de servicios de dominio de Active Directory que incluyen controladores de dominio de solo lectura o servidores de catálogo global de solo lectura, siempre que haya controladores de dominio de escritura disponibles.</span><span class="sxs-lookup"><span data-stu-id="a9064-132">Lync Server 2013 supports Active Directory Domain Services deployments that include read-only domain controllers or read-only global catalog servers, as long as there are writable domain controllers available.</span></span>

</div>

<div>

## <a name="domain-names"></a><span data-ttu-id="a9064-133">Nombres de dominio</span><span class="sxs-lookup"><span data-stu-id="a9064-133">Domain Names</span></span>

<span data-ttu-id="a9064-134">Lync Server no es compatible con los dominios con etiqueta única.</span><span class="sxs-lookup"><span data-stu-id="a9064-134">Lync Server does not support single-labeled domains.</span></span> <span data-ttu-id="a9064-135">Por ejemplo, un bosque con un dominio raíz denominado **contoso. local** es compatible, pero no se admite un dominio raíz denominado **local** .</span><span class="sxs-lookup"><span data-stu-id="a9064-135">For example, a forest with a root domain named **contoso.local** is supported, but a root domain named **local** is not supported.</span></span> <span data-ttu-id="a9064-136">Para obtener más información, consulte el artículo 300684 de Microsoft Knowledge base, "información sobre la configuración de Windows para dominios con nombres DNS de etiqueta única" en [https://go.microsoft.com/fwlink/p/?linkId=143752](https://go.microsoft.com/fwlink/p/?linkid=143752) .</span><span class="sxs-lookup"><span data-stu-id="a9064-136">For details, see Microsoft Knowledge Base article 300684, “Information about configuring Windows for domains with single-label DNS names,” at [https://go.microsoft.com/fwlink/p/?linkId=143752](https://go.microsoft.com/fwlink/p/?linkid=143752).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a9064-137">Lync Server no permite cambiar el nombre de los dominios.</span><span class="sxs-lookup"><span data-stu-id="a9064-137">Lync Server does not support renaming domains.</span></span> <span data-ttu-id="a9064-138">Si necesita cambiar el nombre de un dominio donde se ha implementado Lync Server, primero debe desinstalar Lync Server, después cambiar el nombre del dominio y, a continuación, volver a instalar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a9064-138">If you need to rename a domain where Lync Server is deployed, you need to first uninstall Lync Server, then rename the domain, and then reinstall Lync Server.</span></span>



</div>

</div>

<div>

## <a name="locked-down-ad-ds-environments"></a><span data-ttu-id="a9064-139">Entornos AD DS bloqueados</span><span class="sxs-lookup"><span data-stu-id="a9064-139">Locked Down AD DS Environments</span></span>

<span data-ttu-id="a9064-140">En un entorno de AD DS bloqueado, los usuarios y los objetos de equipos se colocan a menudo en unidades organizativas específicas con la herencia de permisos deshabilitada para ayudar a proteger la delegación administrativa y habilitar el uso de objetos de directiva de grupo (GPO) para aplicar directivas de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a9064-140">In a locked-down AD DS environment, Users and Computer objects are often placed in specific organizational units (OUs) with permissions inheritance disabled to help secure administrative delegation and to enable use of Group Policy objects (GPOs) to enforce security policies.</span></span> <span data-ttu-id="a9064-141">Lync Server 2013 se puede implementar en un entorno de Active Directory bloqueado.</span><span class="sxs-lookup"><span data-stu-id="a9064-141">Lync Server 2013 can be deployed in a locked-down Active Directory environment.</span></span> <span data-ttu-id="a9064-142">Para obtener más información sobre lo que se necesita para implementar Lync Server en un entorno bloqueado, consulte [preparar los servicios de dominio de Active Directory bloqueados en Lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="a9064-142">For details about what is required to deploy Lync Server in a locked-down environment, see [Preparing a locked-down Active Directory Domain Services in Lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md) in the Deployment documentation.</span></span>

<span data-ttu-id="a9064-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a9064-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

