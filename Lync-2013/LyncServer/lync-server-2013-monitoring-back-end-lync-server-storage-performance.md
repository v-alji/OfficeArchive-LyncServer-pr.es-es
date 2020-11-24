---
title: 'Lync Server 2013: supervisar el rendimiento de almacenamiento de back end de Lync Server'
description: 'Lync Server 2013: supervisar el rendimiento de almacenamiento de back end de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring back end Lync Server 2013 storage performance
ms:assetid: 71627c70-1953-4ac2-afbe-f3ad85be0f44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720917(v=OCS.15)
ms:contentKeyID: 63969619
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7501418d3589b941b7e92d2b414492c1d27a3ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398466"
---
# <a name="monitoring-back-end-lync-server-2013-storage-performance"></a><span data-ttu-id="895c0-103">Supervisar el rendimiento de almacenamiento de back end de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="895c0-103">Monitoring back end Lync Server 2013 storage performance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="895c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="895c0-104">

<span> </span></span></span>

<span data-ttu-id="895c0-105">_**Última modificación del tema:** 2014-05-02_</span><span class="sxs-lookup"><span data-stu-id="895c0-105">_**Topic Last Modified:** 2014-05-02_</span></span>

<span data-ttu-id="895c0-106">Las bases de datos back-end de Lync Server 2013 son una parte muy importante de la implementación de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="895c0-106">The Lync Server 2013 back-end databases are a very important part of the Lync Server 2013 deployment.</span></span> <span data-ttu-id="895c0-107">Recomendamos supervisar constantemente las bases de datos y los registros de transacciones respectivos para asegurarse de que el back-end de 2013 de Lync Server está funcionando de manera óptima.</span><span class="sxs-lookup"><span data-stu-id="895c0-107">We recommend constantly monitoring the databases and respective transaction logs to help to make sure that the Lync Server 2013 back end is performing optimally.</span></span>

<span data-ttu-id="895c0-108">La siguiente tabla identifica los contadores de rendimiento que deben supervisarse para obtener información sobre el rendimiento del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="895c0-108">The following table identifies performance counters that should be monitored to learn information about Storage Performance.</span></span> <span data-ttu-id="895c0-109">Los valores de línea base de estos contadores deben determinarse en primer lugar (cuando el sistema tiene la carga normal, esperada) para comprender los cambios de rendimiento cuando el sistema está estresado.</span><span class="sxs-lookup"><span data-stu-id="895c0-109">The baseline values for these counters must be determined first (when system is at its normal, expected load) to understand the performance changes when system is stressed.</span></span>

### <a name="performance-counters-to-be-monitored"></a><span data-ttu-id="895c0-110">Contadores de rendimiento que se van a supervisar</span><span class="sxs-lookup"><span data-stu-id="895c0-110">Performance counters to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="895c0-111">Contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="895c0-111">Performance Counter</span></span></th>
<th><span data-ttu-id="895c0-112">Umbrales de línea base</span><span class="sxs-lookup"><span data-stu-id="895c0-112">Baseline thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="895c0-113">Transacciones/s (RTC)</span><span class="sxs-lookup"><span data-stu-id="895c0-113">Transactions/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="895c0-114">Transacciones/seg (RTCDyn)</span><span class="sxs-lookup"><span data-stu-id="895c0-114">Transactions/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="895c0-115">Transacciones/s (tempdb)</span><span class="sxs-lookup"><span data-stu-id="895c0-115">Transactions/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="895c0-116">Vaciados del registro/s (RTC)</span><span class="sxs-lookup"><span data-stu-id="895c0-116">Log Flushes/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="895c0-117">Vaciados del registro/seg (RTCDyn)</span><span class="sxs-lookup"><span data-stu-id="895c0-117">Log Flushes/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="895c0-118">Vaciados de registro/sec (tempdb)</span><span class="sxs-lookup"><span data-stu-id="895c0-118">Log Flushes/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="895c0-119">Transferencias de disco/seg (lectura y escritura): base de BD de RTC</span><span class="sxs-lookup"><span data-stu-id="895c0-119">Disk Transfers/sec (read+write) - RTC db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="895c0-120">Transferencias de disco/seg.</span><span class="sxs-lookup"><span data-stu-id="895c0-120">Disk Transfers/sec - RTC log</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="895c0-121">Transferencias de disco/seg-RTCDyn dB</span><span class="sxs-lookup"><span data-stu-id="895c0-121">Disk Transfers/sec - rtcdyn db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="895c0-122">Transferencias de disco/seg: registro de RTCDyn</span><span class="sxs-lookup"><span data-stu-id="895c0-122">Disk Transfers/sec - rtcdyn log</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="895c0-123">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="895c0-123">


</div>

<span> </span>

</div>

</div>

</span></span></div>

