---
title: 'Lync Server 2013: tabla AppSharingMetricsThreshold'
description: 'Lync Server 2013: tabla AppSharingMetricsThreshold.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingMetricsThreshold table
ms:assetid: 782cfab9-01a6-4843-aea1-28f47b0b51f7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205018(v=OCS.15)
ms:contentKeyID: 48184556
ms.date: 12/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 092c7d08026e6b736b81043a71b4ecaabc4d5f1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439875"
---
# <a name="appsharingmetricsthreshold-table-in-lync-server-2013"></a>Tabla AppSharingMetricsThreshold en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2015-12-08_

La tabla AppSharingMetricsThreshold contiene valores óptimos y aceptables para las métricas de la calidad de la experiencia que se usan con el uso compartido de aplicaciones. Estos umbrales se usan para determinar si la experiencia de uso compartido de aplicaciones se debe clasificar como mala.

Esta tabla se introdujo en Microsoft Lync Server 2013.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Columna</strong></th>
<th><strong>Tipo de datos</strong></th>
<th><strong>Clave o índice</strong></th>
<th><strong>Detalles</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>CallType</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>Tipo de llamada que se realizó.</p></td>
</tr>
<tr class="even">
<td><p><strong>AppliedBandwidthLimitOptimal</strong></p></td>
<td><p>int</p></td>
<td></td>
<td><p>Límite de ancho de banda óptimo para compartir aplicaciones. El valor predeterminado es 1 millón.</p></td>
</tr>
<tr class="odd">
<td><p><strong>AppliedBandwidthLimitAcceptable</strong></p></td>
<td><p>int</p></td>
<td></td>
<td><p>Limitación de ancho de banda aceptable para el uso compartido de aplicaciones. El valor predeterminado es 500000.</p></td>
</tr>
<tr class="even">
<td><p><strong>SpoiledTilePercentTotalOptimal</strong></p></td>
<td><p>decimal (4,5)</p></td>
<td></td>
<td><p>Tasa de porcentaje óptima para los mosaicos "estropeados" para clasificar la calidad de uso compartido de una aplicación. Este valor es el porcentaje del contenido del que el que comparte no ha podido comunicarse con el visor. El contenido puede ser descartado (o estropeado) cuando el compartidor descarta los mosaicos del origen de los gráficos o los mosaicos de ASMCU descarta los mosaicos del compartidor, respectivamente. El valor predeterminado es 11 por ciento.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SpoiledTilePercentTotalAcceptable</strong></p></td>
<td><p>decimal (4,5)</p></td>
<td></td>
<td><p>tasa porcentual de cceptable para los cuadros "estropeados" para clasificar la calidad de uso compartido de una aplicación. Este valor es el porcentaje del contenido del que el que comparte no ha podido comunicarse con el visor. El contenido puede ser descartado (o estropeado) cuando el compartidor descarta los mosaicos del origen de los gráficos o los mosaicos de ASMCU descarta los mosaicos del compartidor, respectivamente. El valor predeterminado es 36 por ciento.</p></td>
</tr>
<tr class="even">
<td><p><strong>JitterInterArrivalOptimal</strong></p></td>
<td><p>int</p></td>
<td></td>
<td><p>Esta columna no se usa en Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>JitterInterArrivalAcceptable</strong></p></td>
<td><p>int</p></td>
<td></td>
<td><p>Esta columna no se usa en Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayBurstDensityOptimal</strong></p></td>
<td><p>float</p></td>
<td></td>
<td><p>Esta columna no se usa en Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayBurstDensityAcceptable</strong></p></td>
<td><p>float</p></td>
<td></td>
<td><p>Esta columna no se usa en Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></p></td>
<td><p>float</p></td>
<td></td>
<td><p>Esta columna no se usa en Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></p></td>
<td><p>float</p></td>
<td></td>
<td><p>Esta columna no se usa en Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayAverageOptimal</strong></p></td>
<td><p>float</p></td>
<td></td>
<td><p>Valor óptimo para el retraso relativo relativo entre los dos extremos multimedia implicados en el uso compartido de la aplicación. Es una medición de la latencia de un solo salto. El valor predeterminado es 1,0 segundos.</p>
<p>La columna se introdujo en Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayAverageAcceptable</strong></p></td>
<td><p>float</p></td>
<td></td>
<td><p>Valor óptimo para el retraso relativo relativo entre los dos extremos multimedia implicados en el uso compartido de la aplicación. Es una medición de la latencia de un solo salto. El valor predeterminado es 1,75 segundos.</p>
<p>La columna se introdujo en Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RDPTileProcessingLatencyAverageOptimal</strong></p></td>
<td><p>float</p></td>
<td></td>
<td><p>Valor óptimo de la latencia media de procesamiento de mosaicos RDP en el servidor de conferencia como durante la duración de la sesión de visualización. Latencia es la diferencia horaria entre cuando el fotograma inicial está codificado en el servidor (compartidor o MCU, según el escenario) y se descodifica el mismo fotograma de inicio en el visor.</p>
<p>Una media alta refleja un retraso mayor en la experiencia de visualización. Un servidor de conferencias sobrecargado podría experimentar una media mayor de retrasos. El valor predeterminado es 200ms.</p>
<p>La columna se introdujo en Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RDPTileProcessingLatencyAverageAcceptable</strong></p></td>
<td><p>float</p></td>
<td></td>
<td><p>Valor aceptable de la latencia media de procesamiento de mosaicos RDP en el servidor de conferencia como durante la duración de la sesión de visualización. Latencia es la diferencia horaria entre cuando el fotograma inicial está codificado en el servidor (compartidor o MCU, según el escenario) y se descodifica el mismo fotograma de inicio en el visor.</p>
<p>Una media alta refleja un retraso mayor en la experiencia de visualización. Un servidor de conferencias sobrecargado podría experimentar una media mayor de retrasos. El valor predeterminado es 200ms.</p>
<p>La columna se introdujo en Microsoft Lync Server 2013.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

