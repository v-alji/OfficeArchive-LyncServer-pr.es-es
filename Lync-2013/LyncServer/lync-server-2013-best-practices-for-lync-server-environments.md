---
title: 'Lync Server 2013: procedimientos recomendados para entornos de Lync Server'
description: 'Lync Server 2013: procedimientos recomendados para entornos de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for Lync Server environments
ms:assetid: b0e45d84-09c8-4d3e-aad0-bc6f34ce233b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720348(v=OCS.15)
ms:contentKeyID: 63969642
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae6c02621bd6506d2a1d379aeaf92b20ce3f7ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436065"
---
# <a name="best-practices-for-lync-server-2013-environments"></a>Procedimientos recomendados para entornos de Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2014-08-04_

Los siguientes principios generales deben aplicarse a las operaciones en curso de su sistema:

  - **Comprender y utilizar MOF**   MOF es una colección de procedimientos recomendados, principios y modelos que proporcionan orientación técnica a la organización sobre la administración de activos de ti, como las operaciones diarias de Lync Server 2013. Las siguientes pautas de MOF pueden ayudarle a lograr la confiabilidad, la disponibilidad, la compatibilidad y la capacidad de administración de los productos de Microsoft de misión crítica. Para obtener más información, consulte [Microsoft Operations Framework 4,0](https://go.microsoft.com/fwlink/p/?linkid=40939).

  - **Obtenga más información sobre los procedimientos recomendados para Lync Server 2013**   Le recomendamos que implemente procedimientos prácticos y probados para administrar Lync Server 2013. El uso de métodos probados, probados y documentados de administración de operaciones puede ser más eficaz que el desarrollo de métodos propios.

  - **Separar operaciones en procesos diarios, semanales y mensuales**   Documente las tareas operativas necesarias que realizará regularmente. Documentar cómo se realizan las tareas ayuda a asegurarse de que su información se conserve cuando haya un cambio en el entorno operativo, como cuando se implementan nuevas tecnologías o se producen cambios en el personal. Recomendamos que las tareas operativas se separen en cargas de trabajo manejables donde las tareas se realizan diariamente, semanalmente y mensualmente. Las tareas diarias podrían centrar esfuerzos en el funcionamiento de un sistema, y las tareas mensuales se centrarían más en asegurar la salud a largo plazo de un sistema.
    
    Este documento se puede usar en entornos que implementan solo los componentes de mensajería instantánea y presencia (mensajes instantáneos/P) o mensajería instantánea/P con Enterprise Voice. Cuando las tareas o los elementos de la lista de comprobación son específicos de Enterprise Voice, esto se menciona y, si su entorno no incluye telefonía IP empresarial, puede que se omita la parte.

  - **Implementar las herramientas necesarias para el funcionamiento de Lync Server 2013**   Hay muchas herramientas disponibles para ayudar a solucionar problemas, automatizar tareas y ayudar a supervisar y mantener el entorno de Lync Server 2013. Defina un conjunto estándar de herramientas para su organización, de modo que las tareas que realiza el equipo de operaciones se realicen de manera precisa, eficiente, coherente y controlada. También debe implementar procesos para realizar un seguimiento de los incidentes y cambios de configuración importantes.

<div>

## <a name="reference"></a>Referencia

Para los lectores que aún no están familiarizados con los conceptos básicos de la administración de servidores, proporcionamos una descripción general de las prácticas de administración de servidores. Los lectores que ya están familiarizados con la administración de servidores pueden omitir esta sección.

Los procedimientos recomendados son recomendaciones que se basan en el conocimiento y la experiencia que los profesionales de TI han ganado en muchos entornos. Proporcionan procedimientos estándar para las tareas típicas que los administradores de Lync Server deben realizar diariamente y muestran las herramientas que deben usar para administrar un entorno de Lync Server.

Entre las tareas típicas de los administradores de Lync se incluyen las siguientes:

  - **Administración de la capacidad y la disponibilidad**   Defina cómo y qué se debe medir para predecir futuros requisitos de capacidad y para informar sobre la capacidad, la confiabilidad y la disponibilidad de sus sistemas. Debe comprobar que los servidores que ejecutan Lync Server tienen el tamaño adecuado para controlar la carga del sistema y que el tiempo de inactividad imprevisto se mantiene bajo los niveles definidos en el contrato de nivel de servicio (SLA). Además, tendrá que actualizar el hardware para seguir cumpliendo los requisitos definidos.

  - Administración **de cambios y administración de la configuración**   Controlar cómo se realizan los cambios en los sistemas de ti. Esto debe incluir pruebas, comentarios sobre la aplicación y planes de contingencias, documentación de todos los cambios y aprobación de la administración si se producen problemas. Mantenga un registro de los activos de software y hardware, así como de sus configuraciones.

  - **Administración del sistema**   Esquema métodos estándar para realizar tareas administrativas, como la administración de bases de datos y la administración de sitios.

  - **Administración de seguridad**   Tener una política y un plan detallados que protejan la confidencialidad de los datos, la integridad de los datos y la disponibilidad de datos de la infraestructura de ti. Esto incluye las actividades diarias y las tareas relacionadas con el mantenimiento y el ajuste de la infraestructura de seguridad de ti.

  - **Solución de problemas del sistema**   Métodos de esquema para tratar problemas inesperados, incluidos los pasos para evitar problemas similares en el futuro.

  - **Acuerdos de nivel de servicio**   Mantenga un conjunto de objetivos para el rendimiento de los sistemas de ti y mida regularmente el rendimiento contra estos objetivos.

  - **Documentación**   Los procedimientos estándar de documentos, como la información de configuración y las lecciones aprendidas, y hacer que estén disponibles para los miembros del personal que los necesiten. Cuando se realicen cambios en la configuración, actualice la documentación según corresponda.

</div>

<div>

## <a name="related-sections"></a>Secciones relacionadas

Revise los temas siguientes relacionados con las operaciones del sistema antes de continuar:

  - [Administración de la capacidad y disponibilidad de Lync Server 2013](lync-server-2013-capacity-and-availability-management.md)

  - [Administración de cambios en Lync Server 2013](lync-server-2013-change-management.md)

  - [Administración de la configuración en Lync Server 2013](lync-server-2013-configuration-management.md)

  - [Administración del sistema en Lync Server 2013](lync-server-2013-system-administration.md)

  - [Acuerdos de nivel de servicio en Lync Server 2013](lync-server-2013-service-level-agreements.md)

  - [Documentación de Lync Server 2013](lync-server-2013-documentation.md)

  - [Procedimientos estándar de Lync Server 2013](lync-server-2013-standard-procedures.md)

  - [Procedimientos de emergencia en Lync Server 2013](lync-server-2013-emergency-procedures.md)

</div>

<div>

## <a name="see-also"></a>Vea también


[Microsoft Operations Framework 4,0](https://go.microsoft.com/fwlink/p/?linkid=40939)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

