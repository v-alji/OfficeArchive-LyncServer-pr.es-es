---
title: 'Guía de operaciones de Lync Server 2013:'
description: 'Lync Server 2013: Guía de operaciones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Operations Guide
ms:assetid: dcb9ddff-6fe3-4077-a2e3-0ba64f65e264
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720467(v=OCS.15)
ms:contentKeyID: 63969658
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 85e562b96e87f54529a9e2ce077a0a82574020c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445284"
---
# <a name="operations-guide-for-lync-server-2013"></a><span data-ttu-id="b3676-103">Operations Guide for Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-103">Operations Guide for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3676-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3676-104">

<span> </span></span></span>

<span data-ttu-id="b3676-105">_**Última modificación del tema:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="b3676-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="b3676-106">En este documento se describen los procesos operativos, las tareas y las herramientas que necesita para mantener un entorno de software de comunicaciones de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b3676-106">This document describes the operational processes, tasks, and tools that are required for you to maintain a Microsoft Lync Server 2013 communications software environment.</span></span> <span data-ttu-id="b3676-107">Explica cómo administrar Lync Server 2013 según el modelo de Microsoft Operations Framework (MOF) y le ayudará a diseñar un entorno de administración funcional eficaz, que incluye la implementación de programaciones, procesos y procedimientos para mantener un entorno de trabajo eficaz.</span><span class="sxs-lookup"><span data-stu-id="b3676-107">It explains how to manage Lync Server 2013 according to the Microsoft Operations Framework (MOF) model and it will help you design an efficient operational management environment, which includes implementing schedules, processes and procedures to maintain an efficient working environment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b3676-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b3676-108">In This Section</span></span>

<span data-ttu-id="b3676-109">Se incluyen las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="b3676-109">The following sections are included:</span></span>

  - [<span data-ttu-id="b3676-110">Procedimientos recomendados para entornos de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-110">Best practices for Lync Server 2013 environments</span></span>](lync-server-2013-best-practices-for-lync-server-environments.md)

  - [<span data-ttu-id="b3676-111">Tareas diarias en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-111">Daily tasks in Lync Server 2013</span></span>](lync-server-2013-daily-tasks.md)

  - [<span data-ttu-id="b3676-112">Tareas semanales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-112">Weekly tasks in Lync Server 2013</span></span>](lync-server-2013-weekly-tasks.md)

  - [<span data-ttu-id="b3676-113">Tareas mensuales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-113">Monthly tasks in Lync Server 2013</span></span>](lync-server-2013-monthly-tasks.md)

  - [<span data-ttu-id="b3676-114">Tareas necesarias en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-114">As-needed tasks in Lync Server 2013</span></span>](lync-server-2013-as-needed-tasks.md)

  - [<span data-ttu-id="b3676-115">Listas de comprobación de operaciones para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-115">Operations checklists for Lync Server 2013</span></span>](lync-server-2013-operations-checklists.md)

  - [<span data-ttu-id="b3676-116">Supervisión de Lync Server 2013 con System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="b3676-116">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md)

  - [<span data-ttu-id="b3676-117">Dependencias operativas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-117">Operational dependencies in Lync Server 2013</span></span>](lync-server-2013-operational-dependencies.md)

  - [<span data-ttu-id="b3676-118">Indicadores de estado de las claves y solución de problemas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-118">Troubleshooting and Key Health Indicators in Lync Server 2013</span></span>](lync-server-2013-troubleshooting-and-key-health-indicators.md)

<span data-ttu-id="b3676-119">Se supone que se completa la implementación de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b3676-119">It is assumed that your Microsoft Lync Server 2013 deployment is completed.</span></span> <span data-ttu-id="b3676-120">Si este no es el caso, consulte el contenido de Planning and Deployment para Microsoft Lync Server 2013 antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="b3676-120">If this is not the case, refer to the planning and deployment content for Microsoft Lync Server 2013 before you continue.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b3676-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3676-121">See Also</span></span>


[<span data-ttu-id="b3676-122">Introducción a Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-122">Getting started with Lync Server 2013</span></span>](lync-server-2013-getting-started.md)  
[<span data-ttu-id="b3676-123">Planeación de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-123">Planning for Lync Server 2013</span></span>](lync-server-2013-planning.md)  
[<span data-ttu-id="b3676-124">Implementación de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-124">Deployment of Lync Server 2013</span></span>](lync-server-2013-deployment.md)  
[<span data-ttu-id="b3676-125">Shell de administración de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3676-125">Lync Server 2013 Management Shell</span></span>](lync-server-2013-lync-server-management-shell.md)  
  

<span data-ttu-id="b3676-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3676-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

