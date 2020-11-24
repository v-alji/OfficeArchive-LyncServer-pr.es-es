---
title: Proceso de migración
description: Proceso de migración.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migration process
ms:assetid: 13d71f4b-9d5e-4ea3-9e93-29fdad7ac68f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204696(v=OCS.15)
ms:contentKeyID: 48183474
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f363bd79a3d3be709d731d2ca4bffb4f83fe89ea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399192"
---
# <a name="migration-process"></a><span data-ttu-id="038f2-103">Proceso de migración</span><span class="sxs-lookup"><span data-stu-id="038f2-103">Migration process</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="038f2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="038f2-104">

<span> </span></span></span>

<span data-ttu-id="038f2-105">_**Última modificación del tema:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="038f2-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="038f2-106">El procedimiento de migración recomendado y admitido para Lync Server 2013 es la migración en paralelo.</span><span class="sxs-lookup"><span data-stu-id="038f2-106">The recommended and supported migration procedure for Lync Server 2013 is side-by-side migration.</span></span> <span data-ttu-id="038f2-107">En este tema se describe por qué debería usar la migración en paralelo y también se incluye información sobre las pruebas de coexistencia.</span><span class="sxs-lookup"><span data-stu-id="038f2-107">This topic describes why you should use side-by-side migration and also includes information about coexistence testing.</span></span>

<div>

## <a name="side-by-side-migration"></a><span data-ttu-id="038f2-108">Migración en paralelo</span><span class="sxs-lookup"><span data-stu-id="038f2-108">Side-By-Side Migration</span></span>

<span data-ttu-id="038f2-109">En casi todas las migraciones, debe usar la ruta de migración en paralelo.</span><span class="sxs-lookup"><span data-stu-id="038f2-109">In nearly every migration, you should use the side-by-side migration path.</span></span> <span data-ttu-id="038f2-110">En una migración en paralelo, se implementa un nuevo servidor con Lync Server 2013 junto a un servidor correspondiente que ejecuta Lync Server 2010 y, después, se transfieren las operaciones al nuevo servidor.</span><span class="sxs-lookup"><span data-stu-id="038f2-110">In a side-by-side migration, you deploy a new server with Lync Server 2013 alongside a corresponding server that is running Lync Server 2010, and then transfer operations to the new server.</span></span> <span data-ttu-id="038f2-111">Si es necesario revertir a Lync Server 2010, solo tiene que desplazar las operaciones de vuelta a los servidores originales.</span><span class="sxs-lookup"><span data-stu-id="038f2-111">If it becomes necessary to roll back to Lync Server 2010, you have only to shift operations back to the original servers.</span></span> <span data-ttu-id="038f2-112">Tenga en cuenta que, en este caso, las reuniones nuevas programadas con clientes actualizados no funcionarán y los clientes también necesitarán cambiar de versión.</span><span class="sxs-lookup"><span data-stu-id="038f2-112">Be aware that in this situation any new meetings scheduled with upgraded clients will not work, and the clients would also need to be downgraded.</span></span>

</div>

<div>

## <a name="coexistence-testing"></a><span data-ttu-id="038f2-113">Pruebas de coexistencia</span><span class="sxs-lookup"><span data-stu-id="038f2-113">Coexistence Testing</span></span>

<span data-ttu-id="038f2-114">Después de implementar Lync Server 2013 en paralelo con Lync Server 2010, la implementación representa un estado de prueba de coexistencia de Lync Server 2013 y Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="038f2-114">After you have deployed Lync Server 2013 in parallel with Lync Server 2010, the deployment represents a coexistence testing state of Lync Server 2013 and Lync Server 2010.</span></span> <span data-ttu-id="038f2-115">Mientras se encuentre en este estado, es importante probar y asegurarse de que se inician los servicios, que cada sitio se puede administrar y que los clientes pueden comunicarse con los usuarios actuales y heredados.</span><span class="sxs-lookup"><span data-stu-id="038f2-115">While in this state, it is important to test and ensure that services are started, each site can be administered, and clients can communicate with current and legacy users.</span></span> <span data-ttu-id="038f2-116">Antes de la migración de todos los usuarios, es muy importante comprender el estado de cada implementación y asegurarse de que cada implementación es funcional y funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="038f2-116">Prior to the migration of all users, it is very important that you understand the state of each deployment and ensure that each deployment is functional and working properly.</span></span> <span data-ttu-id="038f2-117">Por lo general, la fase de pruebas de coexistencia se produce durante las pruebas piloto de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="038f2-117">Typically, the coexistence testing phase exists throughout the pilot testing of Lync Server 2013.</span></span> <span data-ttu-id="038f2-118">Los usuarios heredados se mueven a Lync Server 2013 durante un período de tiempo para garantizar que la compatibilidad de aplicaciones y las características y funciones funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="038f2-118">Legacy users are moved to Lync Server 2013 for a period of time to ensure that application compatibility and features and functions are working properly.</span></span> <span data-ttu-id="038f2-119">Después de las pruebas piloto, los usuarios y las aplicaciones se mueven a la versión de producción de Lync Server 2013, y se retirarán las aplicaciones y los grupos heredados de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="038f2-119">After pilot testing, users and applications are moved to the production version of Lync Server 2013, and the legacy pools and applications of Lync Server 2010 are retired.</span></span>

<span data-ttu-id="038f2-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="038f2-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

