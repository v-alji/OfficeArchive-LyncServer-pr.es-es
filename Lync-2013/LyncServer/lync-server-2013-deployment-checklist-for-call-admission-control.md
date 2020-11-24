---
title: 'Lync Server 2013: Lista de comprobación para la implementación del control de admisión de llamadas'
description: 'Lync Server 2013: lista de comprobación de implementación para el control de admisión de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for call admission control
ms:assetid: 7e56a169-3e63-44ab-bf28-1fdeb52381c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398631(v=OCS.15)
ms:contentKeyID: 48184621
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea5b16d41228faf01637e7e0d78f5ce56f950a19
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397943"
---
# <a name="deployment-checklist-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="59362-103">Lista de comprobación para la implementación del control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="59362-103">Deployment checklist for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="59362-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="59362-104">

<span> </span></span></span>

<span data-ttu-id="59362-105">_**Última modificación del tema:** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="59362-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="59362-106">Para planear de forma eficaz el control de admisión de llamadas (CAC), debe tener en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="59362-106">To plan effectively for call admission control (CAC), you need to consider the following:</span></span>

  - <span data-ttu-id="59362-107">Requisitos previos para implementar CAC.</span><span class="sxs-lookup"><span data-stu-id="59362-107">Prerequisites for deploying CAC.</span></span>

  - <span data-ttu-id="59362-108">Información necesaria para el CAC y las decisiones de configuración que debe realizar antes de la implementación.</span><span class="sxs-lookup"><span data-stu-id="59362-108">Information required for CAC and configuration decisions that you must make in advance of deployment.</span></span>

<div>

## <a name="deployment-prerequisites-for-call-admission-control"></a><span data-ttu-id="59362-109">Requisitos previos de implementación para el control de admisión de llamadas</span><span class="sxs-lookup"><span data-stu-id="59362-109">Deployment Prerequisites for Call Admission Control</span></span>

<span data-ttu-id="59362-110">Antes de implementar el control de admisión de llamadas, debe haber implementado los servidores internos de Lync Server 2013, incluido un grupo de servidores front-end o un servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="59362-110">Before you deploy call admission control, you must already have deployed your Lync Server 2013 internal servers, including either a Front End pool or a Standard Edition server.</span></span>

</div>

<div>

## <a name="information-requirements-for-call-admission-control"></a><span data-ttu-id="59362-111">Requisitos de información para el control de admisión de llamadas</span><span class="sxs-lookup"><span data-stu-id="59362-111">Information Requirements for Call Admission Control</span></span>

<span data-ttu-id="59362-112">En la tabla siguiente se resume la información necesaria para implementar el control de admisión de llamadas.</span><span class="sxs-lookup"><span data-stu-id="59362-112">The following table summarizes the required information for deploying call admission control.</span></span>

### <a name="information-requirements-for-call-admission-control-deployment"></a><span data-ttu-id="59362-113">Requisitos de información para la implementación de control de admisión de llamadas</span><span class="sxs-lookup"><span data-stu-id="59362-113">Information Requirements for Call Admission Control Deployment</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59362-114">Información</span><span class="sxs-lookup"><span data-stu-id="59362-114">Information</span></span></th>
<th><span data-ttu-id="59362-115">Resumen de la información necesaria</span><span class="sxs-lookup"><span data-stu-id="59362-115">Summary of Information Required</span></span></th>
<th><span data-ttu-id="59362-116">Documentación</span><span class="sxs-lookup"><span data-stu-id="59362-116">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59362-117">Capacidades de Lync Server requeridas por su organización</span><span class="sxs-lookup"><span data-stu-id="59362-117">Lync Server capabilities required by your organization</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="59362-118">Capacidades que la organización debe admitir</span><span class="sxs-lookup"><span data-stu-id="59362-118">Capabilities to be supported by your organization</span></span></p></li>
<li><p><span data-ttu-id="59362-119">Capacidades que se deben habilitar para usuarios individuales</span><span class="sxs-lookup"><span data-stu-id="59362-119">Capabilities to be enabled for individual users</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="59362-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Definición de los requisitos de la organización para el servicio de control de admisión de llamadas en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="59362-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59362-121">Topologías y componentes que se van a implementar</span><span class="sxs-lookup"><span data-stu-id="59362-121">Topologies and components to be deployed</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="59362-122">Los componentes relacionados con CAC se instalan automáticamente como parte de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="59362-122">CAC related components are automatically installed as part of Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="59362-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Definición de los requisitos de la organización para el servicio de control de admisión de llamadas en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="59362-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59362-124">Requisitos del sistema</span><span class="sxs-lookup"><span data-stu-id="59362-124">System requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="59362-125">Requisitos de hardware</span><span class="sxs-lookup"><span data-stu-id="59362-125">Hardware requirements</span></span></p></li>
<li><p><span data-ttu-id="59362-126">Requisitos de software</span><span class="sxs-lookup"><span data-stu-id="59362-126">Software requirements</span></span></p></li>
<li><p><span data-ttu-id="59362-127">Requisitos de collocation</span><span class="sxs-lookup"><span data-stu-id="59362-127">Collocation requirements</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="59362-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determinar los requisitos del sistema para Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="59362-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59362-129">Requisitos de infraestructura</span><span class="sxs-lookup"><span data-stu-id="59362-129">Infrastructure requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="59362-130">No se necesitan requisitos de infraestructura específicos para CAC</span><span class="sxs-lookup"><span data-stu-id="59362-130">No specific infrastructure requirements are necessary for CAC</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="59362-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Requisitos de infraestructura para el control de admisión de llamadas en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="59362-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Infrastructure requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59362-132">Requisitos de interfaz de red</span><span class="sxs-lookup"><span data-stu-id="59362-132">Network interface requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="59362-133">Información de la interfaz interna y externa</span><span class="sxs-lookup"><span data-stu-id="59362-133">Internal and external interface information</span></span></p></li>
<li><p><span data-ttu-id="59362-134">Información de enrutamiento (incluida información sobre el blog de NextHop en <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a> , canal de respuesta para clientes del equipo de Microsoft Lync Server)</span><span class="sxs-lookup"><span data-stu-id="59362-134">Routing information (including information on the NextHop blog at <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a>, Microsoft Lync Server team’s customer response channel)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="59362-135"><a href="lync-server-2013-deploying-external-user-access.md">Implementar el acceso de usuarios externos en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="59362-135"><a href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59362-136">Estrategia de implementación</span><span class="sxs-lookup"><span data-stu-id="59362-136">Deployment strategy</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="59362-137">Secuencia de implementación</span><span class="sxs-lookup"><span data-stu-id="59362-137">Deployment sequence</span></span></p></li>
<li><p><span data-ttu-id="59362-138">Grupo de trabajo o dominio</span><span class="sxs-lookup"><span data-stu-id="59362-138">Workgroup or domain</span></span></p></li>
<li><p><span data-ttu-id="59362-139">Seguridad</span><span class="sxs-lookup"><span data-stu-id="59362-139">Security</span></span></p></li>
<li><p><span data-ttu-id="59362-140">Supervisión y auditoría</span><span class="sxs-lookup"><span data-stu-id="59362-140">Monitoring and auditing</span></span></p></li>
<li><p><span data-ttu-id="59362-141">Consideraciones de hardware</span><span class="sxs-lookup"><span data-stu-id="59362-141">Hardware considerations</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="59362-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Procedimientos recomendados para el servicio de control de admisión de llamadas en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="59362-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Best practices for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59362-143">Proceso de implementación</span><span class="sxs-lookup"><span data-stu-id="59362-143">Deployment process</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="59362-144">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="59362-144">Prerequisites</span></span></p></li>
<li><p><span data-ttu-id="59362-145">Requisitos de información</span><span class="sxs-lookup"><span data-stu-id="59362-145">Information requirements</span></span></p></li>
<li><p><span data-ttu-id="59362-146">Procesos y procedimientos</span><span class="sxs-lookup"><span data-stu-id="59362-146">Process and procedures</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="59362-147"><a href="lync-server-2013-configure-call-admission-control.md">Configurar el control de admisión de llamadas en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="59362-147"><a href="lync-server-2013-configure-call-admission-control.md">Configure call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="59362-148">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="59362-148">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

