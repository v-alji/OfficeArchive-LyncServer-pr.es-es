---
title: 'Lync Server 2013: proceso de implementación de cliente móvil'
description: 'Lync Server 2013: proceso de implementación de cliente móvil.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobile client deployment process
ms:assetid: 6498235b-2fa9-421d-bfa0-0ccc09508dbd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690982(v=OCS.15)
ms:contentKeyID: 51541484
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4fa4e9e1d272915e06009df5c06480309ce104e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425566"
---
# <a name="mobile-client-deployment-process-in-lync-server-2013"></a><span data-ttu-id="3d8f1-103">Proceso de implementación de cliente móvil en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3d8f1-103">Mobile client deployment process in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d8f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d8f1-104">

<span> </span></span></span>

<span data-ttu-id="3d8f1-105">_**Última modificación del tema:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="3d8f1-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="3d8f1-106">Una vez completada una implementación de Microsoft Lync Server 2013, los usuarios pueden instalar la aplicación Lync 2013 desde el Marketplace móvil, que están acostumbrados a usar para su dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-106">After a deployment of Microsoft Lync Server 2013 has been completed, users can install the Lync 2013 app from the mobile marketplace that they are accustomed to using for their specific device.</span></span>

<div>

## <a name="lync-mobile-deployment-process"></a><span data-ttu-id="3d8f1-107">Proceso de implementación de Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="3d8f1-107">Lync Mobile Deployment Process</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d8f1-108">Fase</span><span class="sxs-lookup"><span data-stu-id="3d8f1-108">Phase</span></span></th>
<th><span data-ttu-id="3d8f1-109">Pasos</span><span class="sxs-lookup"><span data-stu-id="3d8f1-109">Steps</span></span></th>
<th><span data-ttu-id="3d8f1-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="3d8f1-110">Permissions</span></span></th>
<th><span data-ttu-id="3d8f1-111">Documentación</span><span class="sxs-lookup"><span data-stu-id="3d8f1-111">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d8f1-112">Realizar tareas previas a la configuración.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-112">Perform pre-setup tasks.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="3d8f1-113">Compruebe la implementación de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-113">Verify Lync Server 2013 deployment.</span></span></p></li>
<li><p><span data-ttu-id="3d8f1-114">Comprobar los requisitos de los certificados.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-114">Verify certificate requirements.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="3d8f1-115">Administrador</span><span class="sxs-lookup"><span data-stu-id="3d8f1-115">Administrator</span></span></p></td>
<td><p><span data-ttu-id="3d8f1-116"><a href="lync-server-2013-planning-for-mobility.md">Planear la movilidad en Lync Server 2013</a> en la documentación de planeación del servidor.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-116"><a href="lync-server-2013-planning-for-mobility.md">Planning for mobility in Lync Server 2013</a> in the server planning documentation.</span></span></p>
<p><span data-ttu-id="3d8f1-117"><a href="lync-server-2013-deploying-mobility.md">Implementación de movilidad en Lync Server 2013</a> en la documentación de implementación del servidor.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-117"><a href="lync-server-2013-deploying-mobility.md">Deploying mobility in Lync Server 2013</a> in the server deployment documentation.</span></span></p>
<p><span data-ttu-id="3d8f1-118"><a href="lync-server-2013-certificate-infrastructure-requirements.md">Requisitos de infraestructura de certificados para Lync Server 2013</a> en la documentación de planeación del servidor.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-118"><a href="lync-server-2013-certificate-infrastructure-requirements.md">Certificate infrastructure requirements for Lync Server 2013</a> in the server planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d8f1-119">Instale la aplicación de Lync en un dispositivo de prueba.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-119">Install the Lync application on a test device.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="3d8f1-120">Instale los requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-120">Install prerequisites.</span></span></p></li>
<li><p><span data-ttu-id="3d8f1-121">Instale desde el Marketplace específico para el dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-121">Install from the marketplace specific to the mobile device.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="3d8f1-122">Administrador</span><span class="sxs-lookup"><span data-stu-id="3d8f1-122">Administrator</span></span></p></td>
<td><p><span data-ttu-id="3d8f1-123">Instrucciones de instalación específicas del dispositivo móvil en la <a href="lync-server-2013-deploying-mobile-clients.md">implementación de clientes móviles en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-123">Installation instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d8f1-124">Configure el cliente.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-124">Configure the client.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="3d8f1-125">Configure las opciones de inicio de sesión y la información del servidor.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-125">Configure sign-in settings and server information.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3d8f1-126">Administrador</span><span class="sxs-lookup"><span data-stu-id="3d8f1-126">Administrator</span></span></p></td>
<td><p><span data-ttu-id="3d8f1-127"><a href="lync-server-2013-deploying-mobile-clients.md">Implementación de clientes móviles en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3d8f1-127"><a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d8f1-128">Probar escenarios de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-128">Test mobile scenarios.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="3d8f1-129">Pruebe la mensajería instantánea (mi) y la presencia.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-129">Test instant messaging (IM) and presence.</span></span></p></li>
<li><p><span data-ttu-id="3d8f1-130">Probar las conferencias de acceso telefónico saliente.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-130">Test dial-out conferencing.</span></span></p></li>
<li><p><span data-ttu-id="3d8f1-131">Buscar un contacto en el directorio corporativo.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-131">Search for a contact in the corporate directory.</span></span></p></li>
<li><p><span data-ttu-id="3d8f1-132">Probar las notificaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-132">Test push notifications.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="3d8f1-133">Administrador</span><span class="sxs-lookup"><span data-stu-id="3d8f1-133">Administrator</span></span></p></td>
<td><p><span data-ttu-id="3d8f1-134">Instrucciones de comprobación específicas del dispositivo móvil en la <a href="lync-server-2013-deploying-mobile-clients.md">implementación de clientes móviles en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-134">Verification instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d8f1-135">Instale la aplicación de Lync en teléfonos móviles.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-135">Install the Lync application on mobile phones.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="3d8f1-136">Instale los requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-136">Install prerequisites.</span></span></p></li>
<li><p><span data-ttu-id="3d8f1-137">Instale desde el Marketplace específico para el dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-137">Install from the marketplace specific to the mobile device.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="3d8f1-138">Usuario</span><span class="sxs-lookup"><span data-stu-id="3d8f1-138">User</span></span></p></td>
<td><p><span data-ttu-id="3d8f1-139">Instrucciones de instalación específicas del dispositivo móvil en la <a href="lync-server-2013-deploying-mobile-clients.md">implementación de clientes móviles en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3d8f1-139">Installation instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3d8f1-140">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d8f1-140">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

