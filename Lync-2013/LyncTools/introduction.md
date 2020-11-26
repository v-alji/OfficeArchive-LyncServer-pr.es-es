---
title: Introducción
description: Incorporación.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Introduction
ms:assetid: 276395be-93df-4a16-97e2-cb468cd0f2e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945588(v=OCS.15)
ms:contentKeyID: 51541414
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8eb847c499bde077ccaf2aa050de801ceeedcc6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438746"
---
# <a name="introduction"></a><span data-ttu-id="93c6b-103">Introducción</span><span class="sxs-lookup"><span data-stu-id="93c6b-103">Introduction</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93c6b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93c6b-104">

<span> </span></span></span>

<span data-ttu-id="93c6b-105">_**Última modificación del tema:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="93c6b-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="93c6b-106">La herramienta Lync Server 2013 stress and Performance (denominada LyncPerfTool) puede simular la carga de usuarios de los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="93c6b-106">The Lync Server 2013 Stress and Performance Tool (referred to as LyncPerfTool) can simulate user load of the following types:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93c6b-107">Mensajería instantánea (mi) y presencia</span><span class="sxs-lookup"><span data-stu-id="93c6b-107">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="93c6b-108">Audioconferencia</span><span class="sxs-lookup"><span data-stu-id="93c6b-108">Audio conferencing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93c6b-109">Uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="93c6b-109">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="93c6b-110">Voz sobre IP (VoIP), incluida la simulación de red telefónica conmutada (RTC)</span><span class="sxs-lookup"><span data-stu-id="93c6b-110">Voice over IP (VoIP), including public switched telephone network (PSTN) simulation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93c6b-111">Conferencia de cliente de Web Access</span><span class="sxs-lookup"><span data-stu-id="93c6b-111">Web Access Client conferencing</span></span></p></td>
<td><p><span data-ttu-id="93c6b-112">Operador de 2013 de Microsoft Lync</span><span class="sxs-lookup"><span data-stu-id="93c6b-112">Microsoft Lync 2013 Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93c6b-113">Grupos de respuesta</span><span class="sxs-lookup"><span data-stu-id="93c6b-113">Response Groups</span></span></p></td>
<td><p><span data-ttu-id="93c6b-114">Expansión de la lista de distribución</span><span class="sxs-lookup"><span data-stu-id="93c6b-114">Distribution list expansion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93c6b-115">Consulta de la libreta de direcciones y descarga de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="93c6b-115">Address book download and address book query</span></span></p></td>
<td><p><span data-ttu-id="93c6b-116">Las llamadas y el perfil de ubicación de 9-1-1 (E9-1-1) mejorado (plan de marcado)</span><span class="sxs-lookup"><span data-stu-id="93c6b-116">Enhanced 9-1-1 (E9-1-1) calls and location profile (dial plan)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93c6b-117">Multivista</span><span class="sxs-lookup"><span data-stu-id="93c6b-117">MultiView</span></span></p></td>
<td><p><span data-ttu-id="93c6b-118">Ver varias transmisiones desde una conferencia</span><span class="sxs-lookup"><span data-stu-id="93c6b-118">Viewing multiple streams from a conference</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93c6b-119">La herramienta Lync Server 2013 stress and Performance admite la generación de carga entre grupos y la Federación solo a través de una configuración avanzada.</span><span class="sxs-lookup"><span data-stu-id="93c6b-119">The Lync Server 2013 Stress and Performance Tool supports cross-pool load generation and federation through advanced configuration only.</span></span>

<span data-ttu-id="93c6b-120">La herramienta tampoco simula la carga de usuarios para los siguientes clientes:</span><span class="sxs-lookup"><span data-stu-id="93c6b-120">The tool also does not simulate user load for the following clients:</span></span>

  - <span data-ttu-id="93c6b-121">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="93c6b-121">Office Live Meeting 2007</span></span>

  - <span data-ttu-id="93c6b-122">Lync 2013 chat persistente</span><span class="sxs-lookup"><span data-stu-id="93c6b-122">Lync 2013 Persistent Chat</span></span>

<span data-ttu-id="93c6b-123">Como resultado, la herramienta de rendimiento y estrés de Lync Server 2013 no admite la prueba de los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="93c6b-123">As a result, the Lync Server 2013 Stress and Performance Tool will not support testing the following components:</span></span>

  - <span data-ttu-id="93c6b-124">Lync 2013 chat persistente</span><span class="sxs-lookup"><span data-stu-id="93c6b-124">Lync 2013 Persistent Chat</span></span>

  - <span data-ttu-id="93c6b-125">Escenarios de integración de Exchange</span><span class="sxs-lookup"><span data-stu-id="93c6b-125">Exchange integration scenarios</span></span>

<div>

## <a name="applications-and-files-included-with-the-lync-server-2013-stress-and-performance-tool"></a><span data-ttu-id="93c6b-126">Aplicaciones y archivos incluidos con la herramienta Lync Server 2013 stress and Performance</span><span class="sxs-lookup"><span data-stu-id="93c6b-126">Applications and Files Included with the Lync Server 2013 Stress and Performance Tool</span></span>

<span data-ttu-id="93c6b-127">Las siguientes aplicaciones están incluidas en la herramienta Lync Server 2013 stress and Performance:</span><span class="sxs-lookup"><span data-stu-id="93c6b-127">The following applications are included in the Lync Server 2013 Stress and Performance Tool:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93c6b-128">Utilidad</span><span class="sxs-lookup"><span data-stu-id="93c6b-128">Tool</span></span></th>
<th><span data-ttu-id="93c6b-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="93c6b-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93c6b-130">UserProvisioningTool.exe</span><span class="sxs-lookup"><span data-stu-id="93c6b-130">UserProvisioningTool.exe</span></span></p></td>
<td><p><span data-ttu-id="93c6b-131">La herramienta de aprovisionamiento de usuarios de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93c6b-131">The Lync Server 2013 User Provisioning tool.</span></span> <span data-ttu-id="93c6b-132">Esta herramienta se usa para crear usuarios y contactos.</span><span class="sxs-lookup"><span data-stu-id="93c6b-132">This tool is used to create users and contacts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93c6b-133">UserProfileGenerator.exe</span><span class="sxs-lookup"><span data-stu-id="93c6b-133">UserProfileGenerator.exe</span></span></p></td>
<td><p><span data-ttu-id="93c6b-134">La herramienta de configuración de carga de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93c6b-134">The Lync Server 2013 Load Configuration Tool.</span></span> <span data-ttu-id="93c6b-135">Esta herramienta se usa para configurar las características de la carga de usuarios para simular.</span><span class="sxs-lookup"><span data-stu-id="93c6b-135">This tool is used to configure the characteristics of the user load to simulate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93c6b-136">LyncPerfTool.exe</span><span class="sxs-lookup"><span data-stu-id="93c6b-136">LyncPerfTool.exe</span></span></p></td>
<td><p><span data-ttu-id="93c6b-137">La herramienta Lync Server 2013 de estrés y rendimiento.</span><span class="sxs-lookup"><span data-stu-id="93c6b-137">The Lync Server 2013 Stress and Performance Tool.</span></span> <span data-ttu-id="93c6b-138">LyncPerfTool es la herramienta que simula la carga de usuarios.</span><span class="sxs-lookup"><span data-stu-id="93c6b-138">LyncPerfTool is the tool that simulates the user load.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93c6b-139">Default. TMX</span><span class="sxs-lookup"><span data-stu-id="93c6b-139">Default.tmx</span></span></p></td>
<td><p><span data-ttu-id="93c6b-140">Default. TMX es necesario para usar la herramienta de registro de 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="93c6b-140">Default.tmx is required to use the Lync Server 2013 Logging Tool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93c6b-141">Ejemplos de scripts de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="93c6b-141">Example provisioning scripts</span></span></p></td>
<td><p><span data-ttu-id="93c6b-142">Estos ejemplos se usan para configurar la topología para ejecutar pruebas de carga, en función de escenarios específicos.</span><span class="sxs-lookup"><span data-stu-id="93c6b-142">These examples are used to configure the topology for running load tests, based on specific scenarios</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="93c6b-143">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93c6b-143">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

