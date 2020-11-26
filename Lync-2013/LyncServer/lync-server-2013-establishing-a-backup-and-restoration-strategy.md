---
title: 'Lync Server 2013: establecimiento de una estrategia de copia de seguridad y restauración'
description: 'Lync Server 2013: establecimiento de una estrategia de copia de seguridad y restauración.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Establishing a backup and restoration strategy
ms:assetid: f545a75f-bbc4-4968-b510-8f6f3920112b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202195(v=OCS.15)
ms:contentKeyID: 51541532
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4fdefed873d1fd69d82f8ecebceeb92f06f65f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428471"
---
# <a name="establishing-a-backup-and-restoration-strategy-for-lync-server-2013"></a>Establecer una estrategia de copia de seguridad y restauración para Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-03-26_

Para poder desarrollar un plan de copia de seguridad y restauración de Lync Server, necesita desarrollar una estrategia que se ajuste a los objetivos de su organización. Para desarrollar una estrategia de copia de seguridad y restauración eficaz, tendrá que:

  - Establecer prioridades empresariales.

  - Identifique los requisitos de copia de seguridad y restauración.

<div>

## <a name="establishing-business-priorities"></a>Establecer prioridades empresariales

Evaluar las prioridades empresariales de su organización. Normalmente, las prioridades empresariales principales que afectan a la copia de seguridad y la estrategia de restauración son las siguientes:

  - Requisitos de continuidad empresarial

  - Integridad de los datos

  - Criticidad de los datos

  - Requisitos de portabilidad

  - Restricciones de costo

Necesidades empresariales, como estas ayudan a determinar los contratos de nivel de servicio (SLA) que usted desarrolla con sus clientes. Los acuerdos de nivel de servicio influyen considerablemente en su estrategia de copia de seguridad y recuperación.

</div>

<div>

## <a name="identifying-backup-and-restoration-requirements"></a>Identificar los requisitos de copia de seguridad y restauración

Las prioridades empresariales y los acuerdos de nivel de servicio actúan en la determinación de los requisitos de las organizaciones para realizar copias de seguridad y restaurar el servidor de Lync. Identifique y documente sus requisitos para lo siguiente:

  - **Frecuencia de las copias de seguridad**   Para obtener más información sobre los procedimientos recomendados para la frecuencia de copia de seguridad, vea [procedimientos recomendados para copias de seguridad y restauración de Lync Server 2013](lync-server-2013-best-practices-for-backup-and-restoration.md).

  - **Herramientas de copia de seguridad y restauración**   Incluya quién va a usar las herramientas y en qué equipos. Para obtener más información sobre las herramientas descritas en este tema y los permisos necesarios, consulte [requisitos de copia de seguridad y restauración en Lync Server 2013: herramientas y permisos](lync-server-2013-backup-and-restoration-requirements-tools-and-permissions.md).

  - **Ubicación de copia de seguridad**   Identifique si las copias de seguridad se guardan de forma local o remota, teniendo en cuenta la seguridad y la accesibilidad. Especifique el medio que se va a usar para las copias de seguridad.

  - **Requisitos de hardware y software**   Identifique y documente los requisitos específicos de hardware y software, incluido el hardware para el almacenamiento de copias de seguridad y la restauración de componentes específicos, así como cualquier conectividad de software y red necesaria para admitir la copia de seguridad y la restauración. A medida que desarrolla los requisitos de hardware y software, tenga en cuenta los distintos escenarios de restauración que siguen.

  - **Escenarios de restauración**   Estos son los procesos de restauración de los siguientes escenarios:
    
      - Se produce un error en un grupo de Lync Server. Este escenario requiere que se Recompile cada servidor del grupo.
    
      - Se produce un error en un servidor Standard Edition. Este escenario requiere que se recompile el servidor en un equipo nuevo o limpio, y el restore de las bases de datos.
    
      - Pérdida del almacén de administración central. Como mínimo, este escenario requiere restaurar y publicar el almacén de administración central.
    
      - Pérdida de un servidor back-end cuando el almacén de administración central sigue funcionando con normalidad. Este escenario requiere que se recompile el servidor en un equipo nuevo o limpio, y el restore de las bases de datos.
    
      - Se produce un error en un servidor que es miembro de un grupo de servidores de Lync. Este escenario requiere que se recompile el servidor en un equipo nuevo o limpio.
    
      - Se produce un error en el almacén de archivos. Este escenario requiere restaurar el servidor de archivos o el clúster de archivos.
    
      - Se produce un error en un archivo, supervisión o base de datos de chat persistente. Este escenario requiere volver a crear las bases de datos y, si los datos son críticos para su organización, restaurar los datos. El archivado, la supervisión y los datos persistentes del chat no son necesarios para obtener la copia de seguridad y la ejecución de Lync Server.

</div>

</div>

<span> </span>

</div>

</div>

</div>

