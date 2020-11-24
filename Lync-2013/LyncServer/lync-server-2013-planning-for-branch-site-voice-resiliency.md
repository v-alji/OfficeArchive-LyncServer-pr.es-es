---
title: 'Lync Server 2013: Planificar la resistencia de voz en sitios de sucursal'
description: 'Lync Server 2013: planeamiento de resistencia a la voz de un sitio de sucursal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for branch-site voice resiliency
ms:assetid: 67713f57-3ded-4127-ac37-57d8099bf384
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398477(v=OCS.15)
ms:contentKeyID: 48184351
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9ce7eb25e1d3078cd2114fc26428f4c8c2ff6508
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399539"
---
# <a name="planning-for-branch-site-voice-resiliency-in-lync-server-2013"></a><span data-ttu-id="96248-103">Planificar la resistencia de voz en sitios de sucursal en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96248-103">Planning for branch-site voice resiliency in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96248-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96248-104">

<span> </span></span></span>

<span data-ttu-id="96248-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="96248-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="96248-106">Si desea proporcionar resistencia al sitio de la sucursal, es decir, servicio de voz empresarial de alta disponibilidad, tiene tres opciones para ello:</span><span class="sxs-lookup"><span data-stu-id="96248-106">If you want to provide branch-site resiliency, that is, high-availability Enterprise Voice service, you have three options for doing so:</span></span>

  - <span data-ttu-id="96248-107">Aplicación de sucursal con funciones de supervivencia</span><span class="sxs-lookup"><span data-stu-id="96248-107">Survivable Branch Appliance</span></span>

  - <span data-ttu-id="96248-108">Servidor de sucursal con funciones de supervivencia</span><span class="sxs-lookup"><span data-stu-id="96248-108">Survivable Branch Server</span></span>

  - <span data-ttu-id="96248-109">Implementación completa de Lync Server en el sitio de la sucursal</span><span class="sxs-lookup"><span data-stu-id="96248-109">A full Lync Server deployment at the branch site</span></span>

<span data-ttu-id="96248-110">Esta guía le ayudará a evaluar qué solución de resistencia es la mejor para su organización y, en función de su solución de resistencia, qué solución de conectividad RTC va a usar.</span><span class="sxs-lookup"><span data-stu-id="96248-110">This guide will help you evaluate which resiliency solution is best for your organization and, based on your resiliency solution, which PSTN-connectivity solution to use.</span></span> <span data-ttu-id="96248-111">También le ayudará a prepararse para implementar la solución que elija al describir los requisitos previos y otras consideraciones de planeación.</span><span class="sxs-lookup"><span data-stu-id="96248-111">It will also help you prepare to deploy the solution that you choose by describing prerequisites and other planning considerations.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="96248-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="96248-112">In This Section</span></span>

  - [<span data-ttu-id="96248-113">Características de resistencia de sitios de sucursal en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96248-113">Branch-site resiliency features in Lync Server 2013</span></span>](lync-server-2013-branch-site-resiliency-features.md)

  - [<span data-ttu-id="96248-114">Soluciones de resistencia de sitios de sucursales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96248-114">Branch-site resiliency solutions in Lync Server 2013</span></span>](lync-server-2013-branch-site-resiliency-solutions.md)

  - [<span data-ttu-id="96248-115">Requisitos de resistencia de sitios de sucursal para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96248-115">Branch-site resiliency requirements for Lync Server 2013</span></span>](lync-server-2013-branch-site-resiliency-requirements.md)

<span data-ttu-id="96248-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96248-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

