---
title: 'Lync Server 2013: informes de QoE'
description: 'Lync Server 2013: informes de QoE.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE reports
ms:assetid: 49c827af-b8dd-4c6e-b0dc-b4bc6d60e9a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720913(v=OCS.15)
ms:contentKeyID: 63969601
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55965d246b7f0ddd71eaeeec99d218eaf8819c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398999"
---
# <a name="qoe-reports-in-lync-server-2013"></a><span data-ttu-id="00c51-103">Informes de calidad de la calidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="00c51-103">QoE reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00c51-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00c51-104">

<span> </span></span></span>

<span data-ttu-id="00c51-105">_**Última modificación del tema:** 2014-05-01_</span><span class="sxs-lookup"><span data-stu-id="00c51-105">_**Topic Last Modified:** 2014-05-01_</span></span>

<div>

## <a name="qoe-summarytrend-reports"></a><span data-ttu-id="00c51-106">Resumen/informes de tendencias de QoE</span><span class="sxs-lookup"><span data-stu-id="00c51-106">QoE summary/trend reports</span></span>

<span data-ttu-id="00c51-107">Los informes de tendencias y de Resumen de la QoE son útiles para encontrar las horas de uso máxima del día y examinar la calidad de los medios para asegurarse de que los recursos de red de la organización son suficientes.</span><span class="sxs-lookup"><span data-stu-id="00c51-107">The QoE summary/trends reports are useful for finding the peak usage times of day and examining the media quality during those times to help assure that your organization's network resources are sufficient.</span></span> <span data-ttu-id="00c51-108">Su organización también puede usar los muchos filtros disponibles en el informe para aislar los números de rendimiento para determinadas ubicaciones, tipos de dispositivos y clientes, y servidores.</span><span class="sxs-lookup"><span data-stu-id="00c51-108">Your organization can also use the many filters available in the report to isolate performance numbers for certain locations, client and device types, and servers.</span></span>

<span data-ttu-id="00c51-109">Los informes de tendencias y de Resumen de QoE constan de:</span><span class="sxs-lookup"><span data-stu-id="00c51-109">QoE summary/trend reports consist of:</span></span>

  - <span data-ttu-id="00c51-110">Resumen/Informe de tendencias de UC a UC</span><span class="sxs-lookup"><span data-stu-id="00c51-110">UC-to-UC Summary/Trend Report</span></span>

  - <span data-ttu-id="00c51-111">Informe de tendencias o Resumen de RTC</span><span class="sxs-lookup"><span data-stu-id="00c51-111">PSTN Summary/Trend Report</span></span>

  - <span data-ttu-id="00c51-112">Resumen de la Conferencia/informe de tendencias</span><span class="sxs-lookup"><span data-stu-id="00c51-112">Conference Summary/Trend Report</span></span>

</div>

<div>

## <a name="qoe-performance-reports"></a><span data-ttu-id="00c51-113">Informes de rendimiento de QoE</span><span class="sxs-lookup"><span data-stu-id="00c51-113">QoE performance reports</span></span>

<span data-ttu-id="00c51-114">Los informes de rendimiento de QoE proporcionan detalles sobre los tres informes que se concentran en el rendimiento de QoE de los servidores de mediación, servidores de conferencia A/V y ubicaciones de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="00c51-114">QoE performance reports provide details about the three reports that concentrate on the QoE performance of Mediation Servers, A/V Conferencing Servers, and endpoint locations.</span></span>

</div>

<div>

## <a name="mediation-server-performance-report"></a><span data-ttu-id="00c51-115">Informe de rendimiento del servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="00c51-115">Mediation server performance report</span></span>

<span data-ttu-id="00c51-116">El informe de rendimiento del servidor de mediación enumera las métricas logradas por una o más mediación durante el período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="00c51-116">The Mediation Server Performance report lists the metrics achieved by one or more Mediation during the specified time period.</span></span> <span data-ttu-id="00c51-117">Se informa por separado de las métricas de la pierna de las comunicaciones unificadas (UC) y la pierna del servidor a la puerta de enlace de cada llamada.</span><span class="sxs-lookup"><span data-stu-id="00c51-117">The metrics for the unified communications (UC)-to-Mediation Server leg and the Mediation Server-to-Gateway leg of each call are reported separately.</span></span> <span data-ttu-id="00c51-118">Use este informe para comparar el volumen y el rendimiento de los diversos servidores de mediación de su organización.</span><span class="sxs-lookup"><span data-stu-id="00c51-118">Use this report to compare the volume and performance of your organization's various Mediation Servers.</span></span>

<span data-ttu-id="00c51-119">Para cada servidor de mediación (y para cada una de las llamadas), el informe muestra lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="00c51-119">For each Mediation Server (and for each call leg), the report displays the following:</span></span>

  - <span data-ttu-id="00c51-120">Número de llamadas</span><span class="sxs-lookup"><span data-stu-id="00c51-120">Number of calls</span></span>

  - <span data-ttu-id="00c51-121">Pérdida de paquetes</span><span class="sxs-lookup"><span data-stu-id="00c51-121">Packet Loss</span></span>

  - <span data-ttu-id="00c51-122">Tiempo de ida y vuelta</span><span class="sxs-lookup"><span data-stu-id="00c51-122">Round Trip Time</span></span>

  - <span data-ttu-id="00c51-123">Vibración</span><span class="sxs-lookup"><span data-stu-id="00c51-123">Jitter</span></span>

  - <span data-ttu-id="00c51-124">Puntuación de la media de conversación (MOS)</span><span class="sxs-lookup"><span data-stu-id="00c51-124">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="00c51-125">Envío de MOS</span><span class="sxs-lookup"><span data-stu-id="00c51-125">Sending MOS</span></span>

  - <span data-ttu-id="00c51-126">Escuchando MOS</span><span class="sxs-lookup"><span data-stu-id="00c51-126">Listening MOS</span></span>

  - <span data-ttu-id="00c51-127">MOS de red</span><span class="sxs-lookup"><span data-stu-id="00c51-127">Network MOS</span></span>

  - <span data-ttu-id="00c51-128">Degradación de MOS de red</span><span class="sxs-lookup"><span data-stu-id="00c51-128">Network MOS Degradation</span></span>

  - <span data-ttu-id="00c51-129">Retorno de eco</span><span class="sxs-lookup"><span data-stu-id="00c51-129">Echo Return</span></span>

  - <span data-ttu-id="00c51-130">Nivel de señal</span><span class="sxs-lookup"><span data-stu-id="00c51-130">Signal Level</span></span>

</div>

<div>

## <a name="av-conferencing-server-performance-report"></a><span data-ttu-id="00c51-131">Informe de rendimiento del servidor de conferencia A/V</span><span class="sxs-lookup"><span data-stu-id="00c51-131">A/V conferencing server performance report</span></span>

<span data-ttu-id="00c51-132">El informe de rendimiento del servidor de conferencia A/V proporciona listas de métricas realizadas por uno o varios servidores de conferencia A/V durante el período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="00c51-132">The A/V Conferencing Server Performance report provides lists of metrics achieved by one or more A/V Conferencing Servers during the specified time period.</span></span> <span data-ttu-id="00c51-133">Este informe se puede usar para comparar el volumen y el rendimiento de varios servidores de conferencia A/V de su organización.</span><span class="sxs-lookup"><span data-stu-id="00c51-133">This report can be used to compare the volume and performance of your organization’s various A/V Conferencing Servers.</span></span> <span data-ttu-id="00c51-134">Su organización también puede aislar el informe para que muestre solo la experiencia de tipos de clientes específicos, como clientes de Lync o clientes RTC.</span><span class="sxs-lookup"><span data-stu-id="00c51-134">Your organization can also isolate the report to show only the experience for specific client types, such as Lync clients or PSTN clients.</span></span>

<span data-ttu-id="00c51-135">Para cada servidor de conferencia A/V, el informe muestra lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="00c51-135">For each A/V Conferencing Server, the report displays the following:</span></span>

  - <span data-ttu-id="00c51-136">Número de conferencias</span><span class="sxs-lookup"><span data-stu-id="00c51-136">Number of conferences</span></span>

  - <span data-ttu-id="00c51-137">Pérdida de paquetes</span><span class="sxs-lookup"><span data-stu-id="00c51-137">Packet Loss</span></span>

  - <span data-ttu-id="00c51-138">Tiempo de ida y vuelta</span><span class="sxs-lookup"><span data-stu-id="00c51-138">Round Trip Time</span></span>

  - <span data-ttu-id="00c51-139">Vibración</span><span class="sxs-lookup"><span data-stu-id="00c51-139">Jitter</span></span>

  - <span data-ttu-id="00c51-140">Puntuación de la media de conversación (MOS)</span><span class="sxs-lookup"><span data-stu-id="00c51-140">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="00c51-141">Envío de MOS</span><span class="sxs-lookup"><span data-stu-id="00c51-141">Sending MOS</span></span>

  - <span data-ttu-id="00c51-142">Escuchando MOS</span><span class="sxs-lookup"><span data-stu-id="00c51-142">Listening MOS</span></span>

  - <span data-ttu-id="00c51-143">MOS de red</span><span class="sxs-lookup"><span data-stu-id="00c51-143">Network MOS</span></span>

  - <span data-ttu-id="00c51-144">Degradación de MOS de red</span><span class="sxs-lookup"><span data-stu-id="00c51-144">Network MOS Degradation</span></span>

  - <span data-ttu-id="00c51-145">Retorno de eco</span><span class="sxs-lookup"><span data-stu-id="00c51-145">Echo Return</span></span>

  - <span data-ttu-id="00c51-146">Nivel de señal</span><span class="sxs-lookup"><span data-stu-id="00c51-146">Signal Level</span></span>

</div>

<div>

## <a name="location-based-performance-report"></a><span data-ttu-id="00c51-147">Informe de rendimiento basado en la ubicación</span><span class="sxs-lookup"><span data-stu-id="00c51-147">Location-based performance report</span></span>

<span data-ttu-id="00c51-148">El informe de rendimiento de Location-Based proporciona una lista de ubicaciones de red y de cada ubicación muestra el número de llamadas en cada rango predeterminado de calidad.</span><span class="sxs-lookup"><span data-stu-id="00c51-148">The Location-Based Performance report provides a list of network locations and for each location shows the number of calls in each pre-determined range of quality.</span></span> <span data-ttu-id="00c51-149">El objetivo de este informe es proporcionar una perspectiva de la calidad de los medios de la mayor parte de las llamadas telefónicas de la organización para las distintas ubicaciones, de modo que pueda identificar las ubicaciones con mal rendimiento y ver los distintos grados de calidad de los medios en las diferentes ubicaciones de su organización.</span><span class="sxs-lookup"><span data-stu-id="00c51-149">The goal of this report is to provide insight into the media quality of the bulk of your organization’s telephone calls for various locations so that you can identify poorly performing locations, and see the different grades of media quality in your organization’s different locations.</span></span>

<span data-ttu-id="00c51-150">Al mostrar el informe, aparecen tablas de métricas diferentes: una tabla por cada métrica en la que la organización decide informar.</span><span class="sxs-lookup"><span data-stu-id="00c51-150">When displaying the report, different tables of metrics appear—one table for each metric your organization decides to report on.</span></span> <span data-ttu-id="00c51-151">Puede elegir entre las siguientes métricas para este informe:</span><span class="sxs-lookup"><span data-stu-id="00c51-151">You can choose from the following metrics for this report:</span></span>

  - <span data-ttu-id="00c51-152">Puntuación de la media de conversación (MOS)</span><span class="sxs-lookup"><span data-stu-id="00c51-152">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="00c51-153">MOS de red</span><span class="sxs-lookup"><span data-stu-id="00c51-153">Network MOS</span></span>

  - <span data-ttu-id="00c51-154">Degradación de MOS de red</span><span class="sxs-lookup"><span data-stu-id="00c51-154">Network MOS Degradation</span></span>

  - <span data-ttu-id="00c51-155">Envío de MOS</span><span class="sxs-lookup"><span data-stu-id="00c51-155">Sending MOS</span></span>

  - <span data-ttu-id="00c51-156">Escuchando MOS</span><span class="sxs-lookup"><span data-stu-id="00c51-156">Listening MOS</span></span>

  - <span data-ttu-id="00c51-157">Pérdida de paquetes</span><span class="sxs-lookup"><span data-stu-id="00c51-157">Packet Loss</span></span>

  - <span data-ttu-id="00c51-158">Vibración</span><span class="sxs-lookup"><span data-stu-id="00c51-158">Jitter</span></span>

  - <span data-ttu-id="00c51-159">Latencia</span><span class="sxs-lookup"><span data-stu-id="00c51-159">Latency</span></span>

<span data-ttu-id="00c51-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00c51-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

