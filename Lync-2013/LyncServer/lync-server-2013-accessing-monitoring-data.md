---
title: 'Lync Server 2013: acceso a datos de supervisión'
description: 'Lync Server 2013: acceso a datos de supervisión.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Accessing monitoring data
ms:assetid: 845385ca-5532-4fa2-91b9-51c6de6fec91
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688116(v=OCS.15)
ms:contentKeyID: 49733714
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c183a66c98072f2ab30bb49e561f9f95c753142f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439502"
---
# <a name="accessing-monitoring-data-in-lync-server-2013"></a>Acceso a datos de supervisión en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-09-05_

Los datos de supervisión se almacenan en dos bases de datos de SQL Server: LcsCdr para obtener los datos del registro detallado y QoEMetrics para los datos de Calidad de la experiencia. No hay nada especial en estas dos bases de datos; esto significa que los datos almacenados en estas bases de datos pueden accederse con cualquiera de las herramientas que usa generalmente para obtener acceso y analizar los datos de SQL Server.

Una de las herramientas que debe considerar para acceder y analizar los datos de supervisión son los informes de supervisión de Lync Server. Son un conjunto de informes estándares que son publicados por el servicio de informes del servidor de Microsoft SQL. Estos informes, a los que se puede obtener acceso con un explorador web, proporcionan información de uso, diagnóstico de llamadas y calidad de medios, basada en la información del registro detallado de llamadas (CDR) y la calidad de la experiencia (QoE) almacenada en las bases de datos de CDR y QoE. Los informes de supervisión se incluyen en Lync Server 2013 y se pueden instalar desde el Asistente para la implementación de Lync Server después de la instalación de Lync Server y la supervisión se ha configurado.

Como se observó, los Informes de supervisión requieren el uso del servicio de informes del servidor SQL. El servicio de informes del servidor SQL puede instalarse simultáneamente con el Servidor SQL o puede instalarse en cualquier momento después de haber instalado el Servidor SQL.

Para obtener más información, vea el tema sobre [Cómo instalar los informes de supervisión de Lync server 2013](lync-server-2013-installing-lync-server-2013-monitoring-reports.md) en la guía de implementación de lync Server 2013.

</div>

<span> </span>

</div>

</div>

</div>

