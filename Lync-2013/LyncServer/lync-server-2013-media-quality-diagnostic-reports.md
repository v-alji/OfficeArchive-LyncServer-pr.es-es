---
title: 'Lync Server 2013: informes de diagnóstico de calidad multimedia'
description: 'Lync Server 2013: informes de diagnóstico de calidad multimedia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Diagnostic Reports
ms:assetid: ea61428e-a1d5-4189-aae6-3db19ddc5cf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615044(v=OCS.15)
ms:contentKeyID: 48185935
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2e346d0f9b8997158cb926ad830d5477950e846d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400014"
---
# <a name="media-quality-diagnostic-reports-in-lync-server-2013"></a><span data-ttu-id="c59d7-103">Informes de diagnóstico de calidad multimedia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c59d7-103">Media Quality Diagnostic Reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c59d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c59d7-104">

<span> </span></span></span>

<span data-ttu-id="c59d7-105">_**Última modificación del tema:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="c59d7-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="c59d7-106">Los Informes de diagnósticos de calidad de medios proporcionan información sobre la calidad de las llamadas, e información de diagnóstico y solución de problemas para las llamadas en las que se produjeron errores.</span><span class="sxs-lookup"><span data-stu-id="c59d7-106">The Media Quality Diagnostic Reports provide information about call quality, and diagnostic and troubleshooting information for failed calls.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c59d7-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c59d7-107">In This Section</span></span>

  - <span data-ttu-id="c59d7-108">[Informe Resumen de calidad de medios en Lync Server 2013](lync-server-2013-media-quality-summary-report.md)   Proporciona datos de calidad general para diferentes tipos de extremos, entre los que se incluyen llamadas de punto a punto de telefonía IP, llamadas en Conferencia de telefonía IP y llamadas que dependen, al menos, de la red de telefonía pública conmutada (RTC).</span><span class="sxs-lookup"><span data-stu-id="c59d7-108">[Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md)   Provides overall quality data for different endpoint types, including Enterprise Voice peer-to-peer calls, Enterprise Voice conference calls, and calls that rely, at least in part, on the public switched telephone network (PSTN).</span></span>

  - <span data-ttu-id="c59d7-109">[Informe de comparación de calidad multimedia en Lync Server 2013](lync-server-2013-media-quality-comparison-report.md)   Proporciona una comparación de los valores de calidad de las llamadas para diferentes tipos de llamadas de audio (por ejemplo, llamadas hechas a través de una red inalámbrica o llamadas hechas a través de una conexión por cable).</span><span class="sxs-lookup"><span data-stu-id="c59d7-109">[Media Quality Comparison Report in Lync Server 2013](lync-server-2013-media-quality-comparison-report.md)   Provides a comparison of call quality values for different types of audio calls (for example, calls made over a wireless network vs. calls made across a wired connection).</span></span>

  - <span data-ttu-id="c59d7-110">[Informe de rendimiento del servidor en Lync Server 2013](lync-server-2013-server-performance-report.md)   Enumera los servidores que han experimentado la mayoría de los problemas, basados en mediciones de métricas de calidad clave como degradación, pérdida de paquetes y vibración.</span><span class="sxs-lookup"><span data-stu-id="c59d7-110">[Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md)   Lists the servers that have experienced the most problems, based on measurements of such key quality metrics as degradation, packet loss, and jitter.</span></span>

  - <span data-ttu-id="c59d7-111">[Informe de ubicación en Lync Server 2013](lync-server-2013-location-report.md)   Proporciona una lista de ubicaciones de red y un resumen de la calidad de los medios de las llamadas que se producen en cada ubicación.</span><span class="sxs-lookup"><span data-stu-id="c59d7-111">[Location Report in Lync Server 2013](lync-server-2013-location-report.md)   Provides a list of network locations and a summary of the media quality of the calls that occur at each location.</span></span> <span data-ttu-id="c59d7-112">Para este informe, las ubicaciones se basan en subredes IP.</span><span class="sxs-lookup"><span data-stu-id="c59d7-112">For purposes of this report, locations are based on IP subnets.</span></span>

  - <span data-ttu-id="c59d7-113">[Informe de dispositivos en Lync Server 2013](lync-server-2013-device-report.md)   Proporciona un resumen de los dispositivos que se usan para las llamadas de telefonía IP e incluye la media de la calidad de medios de las llamadas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c59d7-113">[Device Report in Lync Server 2013](lync-server-2013-device-report.md)   Provides a summary of devices that are used for Enterprise Voice calls and it includes the average media quality of the calls by device.</span></span>

  - <span data-ttu-id="c59d7-114">[Informe de la lista de llamadas en Lync Server 2013](lync-server-2013-call-list-report.md)   Proporciona información detallada sobre las llamadas telefónicas realizadas o recibidas en su organización.</span><span class="sxs-lookup"><span data-stu-id="c59d7-114">[Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md)   Provides detailed information about phone calls made or received within your organization.</span></span>

  - <span data-ttu-id="c59d7-115">[Informe de detalles de llamadas en Lync Server 2013](lync-server-2013-call-detail-report.md)   Proporciona información detallada sobre las llamadas telefónicas hechas desde su organización o recibidas en ella.</span><span class="sxs-lookup"><span data-stu-id="c59d7-115">[Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md)   Provides detailed information about phone calls made from or received within your organization.</span></span>

  - <span data-ttu-id="c59d7-116">[Informe de tendencias de calidad de Media Server en Lync Server 2013](lync-server-2013-server-media-quality-trend-report.md)   Proporciona una manera de comparar gráficamente hasta 5 servidores en métricas de la calidad de la experiencia, como el volumen de las llamadas, el porcentaje de llamada deficiente, la pérdida de paquetes y la vibración.</span><span class="sxs-lookup"><span data-stu-id="c59d7-116">[Server Media Quality Trend Report in Lync Server 2013](lync-server-2013-server-media-quality-trend-report.md)   Provides a way for you to graphically compare up to 5 servers on Quality of Experience metrics such as call volume, poor call percentage, packet loss, and jitter.</span></span>

  - <span data-ttu-id="c59d7-117">[El informe de distribución de métricas de calidad media en Lync Server 2013](lync-server-2013-media-quality-metrics-distribution-report.md)   Proporciona un gráfico en el que se muestran los valores de distribución para una métrica de la calidad de la experiencia, como vibración o pérdida de paquetes.</span><span class="sxs-lookup"><span data-stu-id="c59d7-117">[The Media Quality Metrics Distribution Report in Lync Server 2013](lync-server-2013-media-quality-metrics-distribution-report.md)   Provides a graph that shows the distribution values for a Quality of Experience metric such as jitter or packet loss.</span></span>

  - <span data-ttu-id="c59d7-118">[Informe de tendencias de ubicación en Lync Server 2013](lync-server-2013-location-trend-report.md)   Proporciona información sobre la tendencia de la calidad de las llamadas para ubicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="c59d7-118">[Location Trend Report in Lync Server 2013](lync-server-2013-location-trend-report.md)   Provides call quality trend information for network locations.</span></span>

<span data-ttu-id="c59d7-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c59d7-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

