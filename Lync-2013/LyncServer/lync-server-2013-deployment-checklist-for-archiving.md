---
title: 'Lync Server 2013: Lista de comprobación para la implementación del archivado'
description: 'Lync Server 2013: lista de comprobación de implementación para archivar.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for Archiving
ms:assetid: 7479734d-be01-40d9-ad82-320a09d19d04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205009(v=OCS.15)
ms:contentKeyID: 48184516
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0e9fb3085950aa1e8a750d36a0aeb8592bc18113
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397944"
---
# <a name="deployment-checklist-for-archiving-in-lync-server-2013"></a><span data-ttu-id="d4086-103">Lista de comprobación para la implementación del archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4086-103">Deployment checklist for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d4086-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d4086-104">

<span> </span></span></span>

<span data-ttu-id="d4086-105">_**Última modificación del tema:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="d4086-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="d4086-106">El archivado se instala automáticamente en cada servidor front-end de su implementación de Lync Server 2013, pero debe configurarlo antes de poder usarlo.</span><span class="sxs-lookup"><span data-stu-id="d4086-106">Archiving is automatically installed on each Front End Server in your Lync Server 2013 deployment, but you still need to set it up before you can use it.</span></span> <span data-ttu-id="d4086-107">Los pasos necesarios para configurarlo, como se resume en esta sección, constituyen la implementación del archivado.</span><span class="sxs-lookup"><span data-stu-id="d4086-107">The steps required to set it up, as summarized in this section, constitute the deployment of Archiving.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="d4086-108">Secuencia de implementación</span><span class="sxs-lookup"><span data-stu-id="d4086-108">Deployment Sequence</span></span>

<span data-ttu-id="d4086-109">La forma en que configure el archivado dependerá de la opción de almacenamiento que elija:</span><span class="sxs-lookup"><span data-stu-id="d4086-109">How you set up Archiving depends on which storage option you choose:</span></span>

  - <span data-ttu-id="d4086-110">Si usa la integración de Microsoft Exchange para todos los usuarios de su implementación, no necesita configurar las directivas de archivado de Lync Server 2013 para sus usuarios.</span><span class="sxs-lookup"><span data-stu-id="d4086-110">If you use Microsoft Exchange integration for all users in your deployment, you don’t need to configure Lync Server 2013 Archiving policies for your users.</span></span> <span data-ttu-id="d4086-111">En su lugar, configure las directivas de retención de In-Place de Exchange para admitir el archivado de usuarios alojados en Exchange 2013, con sus buzones puestos en In-Place.</span><span class="sxs-lookup"><span data-stu-id="d4086-111">Instead, configure your Exchange In-Place Hold policies to support archiving for users homed on Exchange 2013, with their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="d4086-112">Para obtener más información sobre cómo configurar estas directivas, consulte la documentación del producto Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="d4086-112">For details about configuring these policies, see the Exchange 2013 product documentation.</span></span>

  - <span data-ttu-id="d4086-113">Si no usa la integración de Microsoft Exchange para todos los usuarios de su implementación, debe agregar bases de datos de archivado de Lync Server (bases de datos de SQL Server) a su topología y luego publicarla, así como configurar las directivas y la configuración de los usuarios, antes de poder archivar los datos de esos usuarios.</span><span class="sxs-lookup"><span data-stu-id="d4086-113">If you do not use Microsoft Exchange integration for all users in your deployment, you need to add Lync Server Archiving databases (SQL Server databases) to your topology and then publish it, as well as configure policies and settings for your users, before you can archive data for those users.</span></span> <span data-ttu-id="d4086-114">Puede implementar bases de datos de archivado al mismo tiempo que implementa su Topología inicial o después de haber implementado al menos un grupo de servidores front-end o un servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d4086-114">You can deploy Archiving databases at the same time that you deploy your initial topology or after you have deployed at least one Front End pool or Standard Edition server.</span></span> <span data-ttu-id="d4086-115">En este documento se describe cómo implementar las bases de datos de archivado agregándolas a una implementación existente.</span><span class="sxs-lookup"><span data-stu-id="d4086-115">This document describes how to deploy Archiving databases by adding them to an existing deployment.</span></span>

<span data-ttu-id="d4086-116">Si habilita el archivado en un grupo de servidores front-end o un servidor Standard Edition, debe habilitarlo para todos los demás grupos front-end y servidores Standard Edition de su implementación.</span><span class="sxs-lookup"><span data-stu-id="d4086-116">If you enable archiving in one Front End pool or Standard Edition server, you should enable it for all other Front End pools and Standard Edition servers in your deployment.</span></span> <span data-ttu-id="d4086-117">Esto se debe a que los usuarios cuyas comunicaciones deben archivarse pueden ser invitados a una conversación grupal grupal o a reuniones hospedadas en un grupo diferente.</span><span class="sxs-lookup"><span data-stu-id="d4086-117">This is because users whose communications are required to be archived can be invited to a group IM conversation or meetings hosted on a different pool.</span></span> <span data-ttu-id="d4086-118">Si el archivo no está habilitado en el grupo en el que está hospedada la conversación o la reunión, es posible que la sesión completa no se Archive.</span><span class="sxs-lookup"><span data-stu-id="d4086-118">If archiving is not enabled on the pool where the conversation or meeting is hosted, the complete session may not be archived.</span></span> <span data-ttu-id="d4086-119">En estos casos, los mensajes instantáneos con usuarios habilitados para archivado aún pueden archivarse, pero no para archivos de contenido de conferencias, y para eventos de unión o salida de conferencia.</span><span class="sxs-lookup"><span data-stu-id="d4086-119">In these cases, IMs with archiving-enabled users still can be archived, but not for conferencing content files, and conference join or leave events.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d4086-120">Si el archivado es importante en su organización por razones de cumplimiento, asegúrese de implementar el archivado, configurar directivas y otras opciones en el nivel correspondiente y habilitarlo para todos los usuarios apropiados, antes de habilitar esos usuarios para Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d4086-120">If archiving is critical in your organization for compliance reasons, be sure to deploy Archiving, configure policies and other options at the appropriate level, and enable it for all appropriate users, before you enable those users for Lync Server 2013.</span></span>



</div>

</div>

<div>

## <a name="archiving-deployment-process"></a><span data-ttu-id="d4086-121">Proceso de implementación de archivado</span><span class="sxs-lookup"><span data-stu-id="d4086-121">Archiving Deployment Process</span></span>

<span data-ttu-id="d4086-122">La tabla siguiente proporciona información general de los pasos necesarios para implementar el archivado en una topología existente.</span><span class="sxs-lookup"><span data-stu-id="d4086-122">The following table provides an overview of the steps required to deploy archiving in an existing topology.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4086-123">Fase</span><span class="sxs-lookup"><span data-stu-id="d4086-123">Phase</span></span></th>
<th><span data-ttu-id="d4086-124">Pasos</span><span class="sxs-lookup"><span data-stu-id="d4086-124">Steps</span></span></th>
<th><span data-ttu-id="d4086-125">Roles y pertenencias a grupos</span><span class="sxs-lookup"><span data-stu-id="d4086-125">Roles and group memberships</span></span></th>
<th><span data-ttu-id="d4086-126">Documentación</span><span class="sxs-lookup"><span data-stu-id="d4086-126">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4086-127"><strong>Instalar los requisitos previos de hardware y software</strong></span><span class="sxs-lookup"><span data-stu-id="d4086-127"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="d4086-128">Para usar la integración de Microsoft Exchange (con Exchange 2013 para archivar el almacenamiento para algunos o todos los usuarios), necesita una implementación de Exchange 2013 existente.</span><span class="sxs-lookup"><span data-stu-id="d4086-128">To use Microsoft Exchange integration (using Exchange 2013 for archiving storage for some or all users), you need an existing Exchange 2013 deployment.</span></span></p></li>
<li><p><span data-ttu-id="d4086-129">Para usar bases de datos de archivado independientes (con bases de datos de SQL Server) para archivar el almacenamiento de algunos o todos los usuarios, SQL Server en el servidor que almacenará los datos de archivado.</span><span class="sxs-lookup"><span data-stu-id="d4086-129">To use separate Archiving databases (using SQL Server databases) for archiving storage for some or all users, SQL Server on the server that will store archiving data.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="d4086-130">El archivado se ejecuta en servidores front-end de un grupo de servidores Enterprise y servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d4086-130">Archiving runs on Front End Servers of an Enterprise pool and Standard Edition servers.</span></span> <span data-ttu-id="d4086-131">No hay ningún requisito adicional de hardware o de software aparte de los necesarios para instalar dichos servidores.</span><span class="sxs-lookup"><span data-stu-id="d4086-131">It has no additional hardware or software requirements beyond what is required to install those servers.</span></span>


</div></td>
<td><p><span data-ttu-id="d4086-132">Usuario de dominio que es miembro del grupo de administradores locales.</span><span class="sxs-lookup"><span data-stu-id="d4086-132">Domain user who is a member of the local administrators group.</span></span></p></td>
<td><p><span data-ttu-id="d4086-133"><a href="lync-server-2013-supported-hardware.md">Hardware compatible para Lync Server 2013</a> en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="d4086-133"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation.</span></span></p>
<p><span data-ttu-id="d4086-134"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Compatibilidad con el software de servidor y la infraestructura en Lync Server 2013</a> en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="d4086-134"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation.</span></span></p>
<p><span data-ttu-id="d4086-135"><a href="lync-server-2013-technical-requirements-for-archiving.md">Requisitos técnicos para archivar en Lync Server 2013</a> en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="d4086-135"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technical requirements for Archiving in Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="d4086-136"><a href="lync-server-2013-setting-up-systems-and-infrastructure-for-archiving.md">Configurar sistemas e infraestructura para archivar en Lync Server 2013</a> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="d4086-136"><a href="lync-server-2013-setting-up-systems-and-infrastructure-for-archiving.md">Setting up systems and infrastructure for Archiving in Lync Server 2013</a> in the Deployment documentation.</span></span></p>
<p><span data-ttu-id="d4086-137"><a href="lync-server-2013-exchange-and-sharepoint-integration-support.md">Compatibilidad de integración de Exchange Server y SharePoint en Lync server 2013</a> en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="d4086-137"><a href="lync-server-2013-exchange-and-sharepoint-integration-support.md">Exchange Server and SharePoint integration support in Lync Server 2013</a> in the Supportability documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4086-138"><strong>Crear la topología interna adecuada para admitir el archivado (solo si no se usa la integración de Microsoft Exchange para todos los usuarios de la implementación)</strong></span><span class="sxs-lookup"><span data-stu-id="d4086-138"><strong>Create the appropriate internal topology to support archiving (only if not using Microsoft Exchange integration for all users in your deployment)</strong></span></span></p></td>
<td><p><span data-ttu-id="d4086-139">Ejecute el generador de topología para agregar bases de datos de archivo de Lync Server 2013 (bases de datos de SQL Server) a la topología y, después, publique la topología.</span><span class="sxs-lookup"><span data-stu-id="d4086-139">Run Topology Builder to add Lync Server 2013 Archiving databases (SQL Server databases) to the topology, and then publish the topology.</span></span></p></td>
<td><p><span data-ttu-id="d4086-140">Para definir una topología para incorporar bases de datos de archivado, una cuenta que sea miembro del grupo usuarios locales.</span><span class="sxs-lookup"><span data-stu-id="d4086-140">To define a topology to incorporate Archiving databases, an account that is a member of the local users group.</span></span></p>
<p><span data-ttu-id="d4086-141">Para publicar la topología, una cuenta que sea miembro del grupo administradores del dominio y del grupo RTCUniversalServerAdmins, y que tenga permisos de control total (lectura/escritura/modificación) en el recurso compartido de archivos para el almacén de archivos de Lync Server 2013 (para que topología pueda configurar las DACL obligatorias).</span><span class="sxs-lookup"><span data-stu-id="d4086-141">To publish the topology, an account that is a member of the domain admins group and RTCUniversalServerAdmins group, and that has full control permissions (read/write/modify) on the file share to be used for the Lync Server 2013 file store (so that Topology Builder can configure the required DACLs).</span></span></p></td>
<td><p><span data-ttu-id="d4086-142"><a href="lync-server-2013-adding-archiving-databases-to-an-existing-lync-server-2013-deployment.md">Agregar bases de datos de archivado a una implementación existente de Lync Server 2013</a> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="d4086-142"><a href="lync-server-2013-adding-archiving-databases-to-an-existing-lync-server-2013-deployment.md">Adding Archiving databases to an existing Lync Server 2013 Deployment</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4086-143"><strong>Configurar la autenticación de servidor a servidor (solo si se usa la integración de Microsoft Exchange)</strong></span><span class="sxs-lookup"><span data-stu-id="d4086-143"><strong>Configure server-to-server authentication (only if using Microsoft Exchange integration)</strong></span></span></p></td>
<td><p><span data-ttu-id="d4086-144">Configure servidores para habilitar la autenticación entre Lync Server 2013 y Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="d4086-144">Configure servers to enable authentication between Lync Server 2013 and Exchange 2013.</span></span> <span data-ttu-id="d4086-145">Le recomendamos que ejecute <strong>Test-CsExchangeStorageConnectivity testuser_sipUri: contenedor de carpetas</strong> para validar la Conectividad del almacenamiento de archivado de Exchange antes de habilitar el archivado.</span><span class="sxs-lookup"><span data-stu-id="d4086-145">We recommend running <strong>Test-CsExchangeStorageConnectivity testuser_sipUri –Folder Dumpster</strong> to validate Exchange Archiving storage connectivity before enabling archiving.</span></span></p></td>
<td><p><span data-ttu-id="d4086-146">Una cuenta con los permisos necesarios para administrar certificados en los servidores.</span><span class="sxs-lookup"><span data-stu-id="d4086-146">An account with the appropriate permissions for managing certificates on the servers.</span></span></p></td>
<td><p><span data-ttu-id="d4086-147"><a href="lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md">Administrar la autenticación de servidor a servidor (OAuth) y las aplicaciones de socios en Lync server 2013</a> en la documentación de implementación o en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="d4086-147"><a href="lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md">Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013</a> in the Deployment documentation or the Operations documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4086-148"><strong>Configurar directivas y configuraciones de archivado</strong></span><span class="sxs-lookup"><span data-stu-id="d4086-148"><strong>Configure archiving policies and configurations</strong></span></span></p></td>
<td><p><span data-ttu-id="d4086-149">Configure el archivado, incluyendo si se debe usar la integración de Microsoft Exchange, la directiva global y las directivas de sitios y usuarios (cuando no se utiliza la integración de Microsoft Exchange para todo el almacenamiento de datos), así como opciones de archivado específicas, como el modo crítico y la exportación y purga de datos.</span><span class="sxs-lookup"><span data-stu-id="d4086-149">Configure archiving, including whether to use Microsoft Exchange integration, the global policy and any site and user policies (when not using Microsoft Exchange integration for all data storage), and specific archiving options, such as critical mode and data export and purging.</span></span></p>
<p><span data-ttu-id="d4086-150">Si usa la integración de Microsoft Exchange, configure las directivas de retención de Exchange In-Place según corresponda.</span><span class="sxs-lookup"><span data-stu-id="d4086-150">If using Microsoft Exchange integration, configure Exchange In-Place Hold policies as appropriate.</span></span></p></td>
<td><p><span data-ttu-id="d4086-151">Grupo RTCUniversalServerAdmins (solo Windows PowerShell) o asigne los usuarios al rol CSArchivingAdministrator o CSAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d4086-151">RTCUniversalServerAdmins group (Windows PowerShell only) or assign users to the CSArchivingAdministrator or CSAdministrator role.</span></span></p></td>
<td><p><span data-ttu-id="d4086-152"><a href="lync-server-2013-configuring-support-for-archiving.md">Configurar la compatibilidad para archivar en Lync Server 2013</a> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="d4086-152"><a href="lync-server-2013-configuring-support-for-archiving.md">Configuring support for Archiving in Lync Server 2013</a> in the Deployment documentation.</span></span></p>
<p><span data-ttu-id="d4086-153">Documentación de producto de Exchange (si se usa la integración de Microsoft Exchange).</span><span class="sxs-lookup"><span data-stu-id="d4086-153">Exchange product documentation (if using Microsoft Exchange integration).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="deploying-lync-server-and-microsoft-exchange-in-different-forests"></a><span data-ttu-id="d4086-154">Implementar Lync Server y Microsoft Exchange en bosques diferentes</span><span class="sxs-lookup"><span data-stu-id="d4086-154">Deploying Lync Server and Microsoft Exchange in Different Forests</span></span>

<span data-ttu-id="d4086-155">Si Microsoft Exchange Server no está implementado en el mismo bosque que Lync Server, debe asegurarse de que los siguientes atributos de Exchange Active Directory estén sincronizados con el bosque donde se ha implementado Lync Server:</span><span class="sxs-lookup"><span data-stu-id="d4086-155">If Microsoft Exchange Server is not deployed in the same forest as Lync Server, you must make sure that the following Exchange Active Directory attributes are synchronized to the forest where Lync Server is deployed:</span></span>

1.  <span data-ttu-id="d4086-156">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="d4086-156">msExchUserHoldPolicies</span></span>

2.  <span data-ttu-id="d4086-157">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="d4086-157">proxyAddresses</span></span>

<span data-ttu-id="d4086-p107">Este es un atributo de varios valores. Al sincronizarlo, los valores se necesitan combinar, no reemplazar, para garantizar que no se pierdan los valores existentes.</span><span class="sxs-lookup"><span data-stu-id="d4086-p107">This is a multi-value attribute. When synchronizing this attribute, you need to merge the values, not replace them to ensure the existing values are not lost.</span></span>

<span data-ttu-id="d4086-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d4086-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

