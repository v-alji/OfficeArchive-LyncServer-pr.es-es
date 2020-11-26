---
title: 'Lync Server 2013: Requisitos de Internet Information Services (IIS)'
description: 'Lync Server 2013: requisitos de servicios de Internet Information Server (IIS).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Internet Information Services (IIS) requirements
ms:assetid: 4f57a605-a8a9-4c5a-9a18-05ecb3d9ab6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398321(v=OCS.15)
ms:contentKeyID: 48184128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd8de55fa4611c3ab29eac7d7c28c522b418e77d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426858"
---
# <a name="internet-information-services-iis-requirements-in-lync-server-2013"></a><span data-ttu-id="49800-103">Requisitos de Internet Information Services (IIS) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49800-103">Internet Information Services (IIS) requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="49800-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="49800-104">

<span> </span></span></span>

<span data-ttu-id="49800-105">_**Última modificación del tema:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="49800-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="49800-106">Varios componentes de Lync Server 2013 requieren servicios de Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="49800-106">Several Lync Server 2013 components require Internet Information Services (IIS).</span></span> <span data-ttu-id="49800-107">En este tema se describen las características específicas de IIS necesarias para admitir Lync Server.</span><span class="sxs-lookup"><span data-stu-id="49800-107">This topic describes the specific IIS features required to support Lync Server.</span></span> <span data-ttu-id="49800-108">En los temas de esta sección se describen los requisitos de los componentes específicos de IIS.</span><span class="sxs-lookup"><span data-stu-id="49800-108">The topics in this section describe the requirements of specific components for IIS.</span></span>

<span data-ttu-id="49800-109">Cuando el rol servidor Web (IIS) está habilitado en Windows Server 2008, se instalan varios servicios de rol de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49800-109">When the Web Server (IIS) role is enabled on Windows Server 2008, various role services are installed by default.</span></span> <span data-ttu-id="49800-110">En la siguiente tabla se describen los servicios de rol adicionales que deben instalarse cuando el rol servidor Web (IIS) está habilitado en Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="49800-110">The following table describes the additional role services that must be installed when the Web Server (IIS) role is enabled on Windows Server 2008.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49800-111">Servicio de rol</span><span class="sxs-lookup"><span data-stu-id="49800-111">Role service</span></span></th>
<th><span data-ttu-id="49800-112">Característica</span><span class="sxs-lookup"><span data-stu-id="49800-112">Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49800-113">Características HTTP comunes</span><span class="sxs-lookup"><span data-stu-id="49800-113">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="49800-114">Redireccionamiento HTTP</span><span class="sxs-lookup"><span data-stu-id="49800-114">HTTP Redirection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49800-115">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="49800-115">Application Development</span></span></p></td>
<td><p><span data-ttu-id="49800-116">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="49800-116">ASP.NET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49800-117">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="49800-117">Application Development</span></span></p></td>
<td><p><span data-ttu-id="49800-118">Extensibilidad de .NET</span><span class="sxs-lookup"><span data-stu-id="49800-118">.NET Extensibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49800-119">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="49800-119">Application Development</span></span></p></td>
<td><p><span data-ttu-id="49800-120">Extensiones ISAPI</span><span class="sxs-lookup"><span data-stu-id="49800-120">ISAPI Extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49800-121">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="49800-121">Application Development</span></span></p></td>
<td><p><span data-ttu-id="49800-122">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="49800-122">ISAPI Filters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49800-123">Estado y diagnóstico</span><span class="sxs-lookup"><span data-stu-id="49800-123">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="49800-124">Herramientas de registro</span><span class="sxs-lookup"><span data-stu-id="49800-124">Logging Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49800-125">Estado y diagnóstico</span><span class="sxs-lookup"><span data-stu-id="49800-125">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="49800-126">Seguimiento</span><span class="sxs-lookup"><span data-stu-id="49800-126">Tracing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49800-127">Seguridad</span><span class="sxs-lookup"><span data-stu-id="49800-127">Security</span></span></p></td>
<td><p><span data-ttu-id="49800-128">Autenticación básica</span><span class="sxs-lookup"><span data-stu-id="49800-128">Basic Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49800-129">Seguridad</span><span class="sxs-lookup"><span data-stu-id="49800-129">Security</span></span></p></td>
<td><p><span data-ttu-id="49800-130">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="49800-130">Windows Authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49800-131">Herramientas de administración</span><span class="sxs-lookup"><span data-stu-id="49800-131">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="49800-132">Scripts y herramientas de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="49800-132">IIS Management Scripts and Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49800-133">Herramientas de administración</span><span class="sxs-lookup"><span data-stu-id="49800-133">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="49800-134">Compatibilidad con la administración de IIS 6</span><span class="sxs-lookup"><span data-stu-id="49800-134">IIS 6 Management Compatibility</span></span></p></td>
</tr>
</tbody>
</table>


<div>

<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="seguridad" alt="security" /><span data-ttu-id="49800-136">Nota de seguridad:</span><span class="sxs-lookup"><span data-stu-id="49800-136">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="49800-137">Si está usando IIS 7,0 en un sistema operativo Windows Server 2008, el programa de instalación de Lync Server deshabilita la autenticación de modo kernel en IIS.</span><span class="sxs-lookup"><span data-stu-id="49800-137">If you are using IIS 7.0 on a Windows Server 2008 operating system, Lync Server Setup disables kernel mode authentication in IIS.</span></span></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="49800-138">En esta sección</span><span class="sxs-lookup"><span data-stu-id="49800-138">In This Section</span></span>

  - [<span data-ttu-id="49800-139">Requisitos de IIS para grupos de servidores front-end y servidores Standard Edition en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49800-139">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-iis-requirements-for-front-end-pools-and-standard-edition-servers.md)

<span data-ttu-id="49800-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="49800-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

