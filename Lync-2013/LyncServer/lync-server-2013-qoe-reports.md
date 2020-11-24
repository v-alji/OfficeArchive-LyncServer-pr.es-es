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
# <a name="qoe-reports-in-lync-server-2013"></a>Informes de calidad de la calidad en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2014-05-01_

<div>

## <a name="qoe-summarytrend-reports"></a>Resumen/informes de tendencias de QoE

Los informes de tendencias y de Resumen de la QoE son útiles para encontrar las horas de uso máxima del día y examinar la calidad de los medios para asegurarse de que los recursos de red de la organización son suficientes. Su organización también puede usar los muchos filtros disponibles en el informe para aislar los números de rendimiento para determinadas ubicaciones, tipos de dispositivos y clientes, y servidores.

Los informes de tendencias y de Resumen de QoE constan de:

  - Resumen/Informe de tendencias de UC a UC

  - Informe de tendencias o Resumen de RTC

  - Resumen de la Conferencia/informe de tendencias

</div>

<div>

## <a name="qoe-performance-reports"></a>Informes de rendimiento de QoE

Los informes de rendimiento de QoE proporcionan detalles sobre los tres informes que se concentran en el rendimiento de QoE de los servidores de mediación, servidores de conferencia A/V y ubicaciones de puntos de conexión.

</div>

<div>

## <a name="mediation-server-performance-report"></a>Informe de rendimiento del servidor de mediación

El informe de rendimiento del servidor de mediación enumera las métricas logradas por una o más mediación durante el período de tiempo especificado. Se informa por separado de las métricas de la pierna de las comunicaciones unificadas (UC) y la pierna del servidor a la puerta de enlace de cada llamada. Use este informe para comparar el volumen y el rendimiento de los diversos servidores de mediación de su organización.

Para cada servidor de mediación (y para cada una de las llamadas), el informe muestra lo siguiente:

  - Número de llamadas

  - Pérdida de paquetes

  - Tiempo de ida y vuelta

  - Vibración

  - Puntuación de la media de conversación (MOS)

  - Envío de MOS

  - Escuchando MOS

  - MOS de red

  - Degradación de MOS de red

  - Retorno de eco

  - Nivel de señal

</div>

<div>

## <a name="av-conferencing-server-performance-report"></a>Informe de rendimiento del servidor de conferencia A/V

El informe de rendimiento del servidor de conferencia A/V proporciona listas de métricas realizadas por uno o varios servidores de conferencia A/V durante el período de tiempo especificado. Este informe se puede usar para comparar el volumen y el rendimiento de varios servidores de conferencia A/V de su organización. Su organización también puede aislar el informe para que muestre solo la experiencia de tipos de clientes específicos, como clientes de Lync o clientes RTC.

Para cada servidor de conferencia A/V, el informe muestra lo siguiente:

  - Número de conferencias

  - Pérdida de paquetes

  - Tiempo de ida y vuelta

  - Vibración

  - Puntuación de la media de conversación (MOS)

  - Envío de MOS

  - Escuchando MOS

  - MOS de red

  - Degradación de MOS de red

  - Retorno de eco

  - Nivel de señal

</div>

<div>

## <a name="location-based-performance-report"></a>Informe de rendimiento basado en la ubicación

El informe de rendimiento de Location-Based proporciona una lista de ubicaciones de red y de cada ubicación muestra el número de llamadas en cada rango predeterminado de calidad. El objetivo de este informe es proporcionar una perspectiva de la calidad de los medios de la mayor parte de las llamadas telefónicas de la organización para las distintas ubicaciones, de modo que pueda identificar las ubicaciones con mal rendimiento y ver los distintos grados de calidad de los medios en las diferentes ubicaciones de su organización.

Al mostrar el informe, aparecen tablas de métricas diferentes: una tabla por cada métrica en la que la organización decide informar. Puede elegir entre las siguientes métricas para este informe:

  - Puntuación de la media de conversación (MOS)

  - MOS de red

  - Degradación de MOS de red

  - Envío de MOS

  - Escuchando MOS

  - Pérdida de paquetes

  - Vibración

  - Latencia

</div>

</div>

<span> </span>

</div>

</div>

</div>

