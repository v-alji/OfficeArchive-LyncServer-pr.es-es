---
title: 'Lync Server 2013: supervisión de Lync Server con System Center Operations Manager'
description: 'Lync Server 2013: supervisión de Lync Server con System Center Operations Manager.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Lync 2013 with SCOM
ms:assetid: a74bde92-97ff-4d90-acb9-7a70272f0f31
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720343(v=OCS.15)
ms:contentKeyID: 63969636
ms.date: 05/06/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ad93c47ab8d157b1e18b4bccc5094408f3d68ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425412"
---
# <a name="monitoring-lync-server-2013-with-system-center-operations-manager"></a><span data-ttu-id="0eec9-103">Supervisión de Lync Server 2013 con System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="0eec9-103">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0eec9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0eec9-104">

<span> </span></span></span>

<span data-ttu-id="0eec9-105">_**Última modificación del tema:** 2015-05-06_</span><span class="sxs-lookup"><span data-stu-id="0eec9-105">_**Topic Last Modified:** 2015-05-06_</span></span>

<span data-ttu-id="0eec9-106">El módulo de administración de Lync Server (MP) es la solución de supervisión elegida para supervisar cualquier implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0eec9-106">The Lync Server Management Pack (MP) is your monitoring solution of choice for monitoring any Lync Server deployment.</span></span>

<span data-ttu-id="0eec9-107">El panel de administración implementa el registro de eventos tradicional y el instrumental basado en contadores de rendimiento, y habilita el nuevo instrumental disponible en Lync Server, como los eventos de pareja (error/éxito) para varios indicadores de estado de claves, y también implementa completamente las nuevas transacciones sintéticas (cmdlet de prueba de \* Windows PowerShell).</span><span class="sxs-lookup"><span data-stu-id="0eec9-107">The MP implements traditional Event Log and Performance counter-based instrumentation and enables newly available instrumentation in Lync Server, such as pair events (failure/success) for several Key Health Indicators, and also fully implements the new Synthetic Transactions (Test-Cs\* Windows PowerShell cmdlets).</span></span>

<span data-ttu-id="0eec9-108">Puede encontrar el paquete de administración de Lync Server 2013 y su documentación relacionada en [https://go.microsoft.com/fwlink/p/?LinkId=400468](https://go.microsoft.com/fwlink/p/?linkid=400468) .</span><span class="sxs-lookup"><span data-stu-id="0eec9-108">You can find the Lync Server 2013 Management Pack and its related documentation at [https://go.microsoft.com/fwlink/p/?LinkId=400468](https://go.microsoft.com/fwlink/p/?linkid=400468).</span></span> <span data-ttu-id="0eec9-109">Esta opción se recomienda si está ejecutando System Center Operations Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="0eec9-109">This is recommended if you are running System Center Operations Manager 2012.</span></span>

<span data-ttu-id="0eec9-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0eec9-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

