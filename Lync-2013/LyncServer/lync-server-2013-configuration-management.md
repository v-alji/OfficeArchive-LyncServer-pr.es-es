---
title: 'Lync Server 2013: administración de la configuración'
description: 'Lync Server 2013: administración de la configuración.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration management
ms:assetid: 00ea1196-cb40-427f-99a4-5e8037cbf367
ms:mtpsurl: https://technet.microsoft.com/library/Dn720316(v=OCS.15)
ms:contentKeyID: 63969570
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5999708811cc4a34cf846a1ddd481ba38e07c62
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434252"
---
# <a name="configuration-management-in-lync-server-2013"></a>Administración de la configuración en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2015-05-15_

La administración de la configuración es el proceso de grabación y seguimiento de los activos de hardware y software y la información de configuración del sistema. Generalmente, se usa para realizar un seguimiento de las licencias de software, mantener una compilación estándar de hardware y software para equipos y servidores cliente, y definir los estándares de nomenclatura para equipos nuevos. La administración de la configuración generalmente cubre las siguientes categorías:

  - **Hardware**   Esta categoría realiza un seguimiento de los elementos de los equipos de los que es propietario la organización de ti, dónde se encuentra el equipo y quién usa el equipo. Esta información permite a una organización planificar y presupuestar actualizaciones, mantener compilaciones de hardware estándar, informar sobre el valor de los activos de TI con fines de contabilidad y ayudar a evitar robos.

  - **Software**   Esta categoría realiza un seguimiento del software que está instalado en cada equipo, los números de versión y dónde se encuentran las licencias. Esta información ayuda a planificar las actualizaciones, garantizar la licencia del software y detectar la presencia de software no autorizado (y sin licencia).

  - **Compilaciones estándar**   Esta categoría realiza un seguimiento de la compilación estándar actual para los equipos y servidores cliente y si los equipos cliente y los servidores cumplen este estándar. Definir e imponer compilaciones estándar ayuda al personal de soporte técnico porque el personal debe mantener un número limitado de versiones de cada elemento de software.

  - **Actualizaciones y revisiones acumulativas**   Esta categoría hace un seguimiento de los Service Packs probados y aprobados para su uso y de los equipos que están actualizados. Esta información es importante para reducir el riesgo de que los equipos se vean comprometidos y detectar a los usuarios que han instalado actualizaciones no aprobadas.

  - **Información de configuración del sistema**   Esta categoría realiza un seguimiento de la función de un sistema, la interacción entre los elementos del sistema y los procesos que dependen de un sistema que se ejecuta sin problemas. Por ejemplo, se puede configurar un servidor proxy de terceros en un solo servidor. Es posible que se entienda la dependencia del servidor proxy en este servidor y que se requieran planes de contingencia si se produce un error. Si el servidor proxy se puede configurar para que también se comunique con otro servidor front-end, las dependencias y los planes de contingencia probablemente cambiarán.

<div>

## <a name="implementing-configuration-management"></a>Implementación de la administración de configuración

Después de determinar qué elementos necesitan administrar, implementar la administración de la configuración mediante la recopilación de datos e informes de datos. El método más sencillo para las organizaciones pequeñas es recopilar datos manualmente (número y modelo de equipos cliente, sistema operativo, software instalado) y guardarlos en un documento de Office Word u Office Excel. Para sistemas de mayor tamaño, complejidad y cambio constante, debe automatizarse el descubrimiento de activos y la recopilación de información detallada. Decida qué información es relevante para su organización y guárdela en una base de datos.

La base de datos de administración de la configuración es una herramienta útil para el personal de soporte técnico y la administración en las siguientes áreas:

  - **Auditorías de seguridad**   La base de datos le permite identificar los servidores que ejecutan Lync Server y los sistemas de equipos cliente que deben tener correcciones aplicadas o que han perdido la instalación de un Service Pack o las últimas actualizaciones de antivirus.

  - **Instalación de software**   Identificar las versiones de software de cliente y realizar un seguimiento de ellas ayudará a los administradores a planear las actualizaciones de versión y las nuevas instalaciones, además de ayudarle con la documentación de licencias y el cumplimiento.

  - **Información de configuración**   Si mantiene una lista actualizada de todos los valores de configuración que se cambiaron de forma predeterminada, podrá solucionar problemas de forma rápida y eficaz.

  - **Actualizaciones de planeación**   Si una revisión de capacidad revela que es necesario disponer de espacio de almacenamiento adicional en sus servidores de base de datos de Lync, es importante saber si cada servidor tiene un controlador RAID interno. Si lo hacen, ¿son el mismo modelo? ¿Tienen el mismo número de discos instalados? La base de datos de administración de la configuración indicará el tipo de disco que se puede instalar, el número y la ruta de actualización en cada caso.

</div>

<div>

## <a name="tools-used-for-configuration-management"></a>Herramientas usadas para la administración de la configuración

Existen muchas herramientas para descubrir, auditar y denunciar activos. Algunas de estas herramientas se describen en esta sección.

  - **Scripts automáticos**   Puede escribir secuencias de comandos sencillas para notificar elementos como el sistema operativo, el nivel de Service Pack y si el software existe en un conjunto específico de equipos. Puede escribir estos scripts en los requisitos exactos de una organización. Sin embargo, el número necesario de scripts y su complejidad pueden crear y mantener los scripts de forma costosa.

  - **Herramientas automatizadas**   Según el tamaño de su empresa y las necesidades de su organización, es posible que desee considerar el uso de herramientas automatizadas. Herramientas como Microsoft Endpoint Configuration Manager incorporan plantillas de informe estándar (como el nivel de Service Pack) y también le permiten crear informes personalizados, por ejemplo, para una aplicación personalizada. El administrador de configuración de Microsoft Endpoint también se puede usar para informar sobre configuraciones de hardware y software.

</div>

<div>

## <a name="relationship-with-change-management"></a>Relación con la administración de cambios

La administración de la configuración está estrechamente relacionada con la administración de cambios. La administración de la configuración identifica la necesidad de cambiar e identifica y registra que se ha producido un cambio. Por ejemplo, la base de datos de administración de la configuración se puede usar para identificar los servidores que requieren una revisión. Después, la administración de cambios define el proceso de aplicación de la revisión.

Por el contrario, si se ha implementado una nueva actualización acumulativa, el proceso de administración de cambios debe suministrar esta información al sistema de administración de la configuración. Es probable que tenga que configurar las herramientas de administración de la configuración para identificar el nuevo software de modo que puedan descubrir y realizar un seguimiento de dónde y cuándo se implementa el software.

</div>

</div>

<span> </span>

</div>

</div>

</div>

