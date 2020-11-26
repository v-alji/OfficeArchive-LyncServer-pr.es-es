---
title: 'Lync Server 2013: Reforzar y proteger los servidores y las aplicaciones'
description: 'Lync Server 2013: refuerzo y protección de servidores y aplicaciones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardening and protecting servers and applications for Lync Server 2013
ms:assetid: 9ca2b233-26f1-4d72-96e7-81a82c727806
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518331(v=OCS.15)
ms:contentKeyID: 62625491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ed1205439208dfdadf5396b976d5d4876fb0aa24
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427757"
---
# <a name="hardening-and-protecting-servers-and-applications-for-lync-server-2013"></a>Reforzar y proteger los servidores y las aplicaciones de Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-12-05_

Debe proteger y proteger el sistema operativo y las aplicaciones según los procedimientos recomendados para ese componente específico. En esta sección se describe cómo reforzar los servidores de aplicaciones y usar la Directiva de grupo para implementar bloqueos de seguridad.

<div>


> [!NOTE]  
> También puede reforzar y proteger las bases de datos que se usan para la implementación de Microsoft Lync Server 2013. Para obtener más información, consulte <A href="lync-server-2013-hardening-and-protecting-databases.md">refuerzo y protección de las bases de datos de Lync Server 2013</A>.



</div>

<div>

## <a name="securing-application-servers"></a>Proteger servidores de aplicaciones

En el caso de los servidores de aplicaciones, se debe reforzar el sistema operativo y la aplicación. Por ejemplo, un equipo Windows Server 2008 dedicado a ejecutar Microsoft Internet Security and Acceleration (ISA) Server 2006 debe reforzarse desde el sistema operativo y desde la perspectiva de la aplicación. Minimizar la cantidad de servicios que se ejecutan y proporcionados por el servidor debe ser un objetivo principal.

</div>

<div>

## <a name="securing-virtual-servers"></a>Proteger servidores virtuales

Las instantáneas de Virtual Server contienen copias de los discos de datos del servidor y también contienen volcados de datos en memoria, que pueden contener datos criptográficos confidenciales, que podrían conducir a ataques. Para los servidores de producción implementados mediante la virtualización, debe deshabilitar todas las instantáneas del servidor o administrarlas de una manera controlada. Para obtener detalles sobre la protección de servidores virtuales Hyper-V, consulte la guía de seguridad de Hyper-V en: [https://go.microsoft.com/fwlink/p/?LinkId=214176](https://go.microsoft.com/fwlink/p/?linkid=214176) .

</div>

<div>

## <a name="group-policy"></a>Directiva de grupo

En Windows Server 2008 y Windows Server 2008 R2, la Directiva de grupo proporciona administración de la configuración de escritorio basada en directorios. Puede usar la Directiva de grupo para implementar bloqueos de seguridad definiendo la configuración del usuario y del equipo dentro de un objeto de directiva de grupo (GPO) para lo siguiente:

  - Directivas basadas en el registro

  - Seguridad

  - Instalación de software

  - Scripts

  - Redireccionamiento de carpetas

  - Servicios de instalación remota

Para proporcionar una interfaz de usuario para que el Administrador configure estas opciones, las plantillas administrativas se incluyen con las versiones del sistema operativo, versiones de Service Pack y algunas aplicaciones, entre las que se incluyen Lync Server 2013.

El archivo Communicator. adm es una plantilla administrativa que se incluye con Lync Server 2013, se instala en el directorio% WINDIR% \\ INF \\ y proporciona una interfaz para la configuración de directiva de grupo. Cada configuración de Communicator. adm corresponde a una configuración del registro que afecta al comportamiento de la aplicación.

Se puede acceder a la configuración desde GPedit.dll, que está disponible en la consola de usuarios y equipos de Active Directory y en la consola de administración de directivas de grupo (GPMC).

</div>

<div>

## <a name="group-policy-security-settings"></a>Configuración de seguridad de la Directiva de grupo

La Directiva de grupo contiene la configuración de seguridad de un GPO en configuración del equipo/Configuración de Windows/configuración de seguridad cuando se accede desde GPedit.dll. Puede importar plantillas de seguridad para configurar las opciones de seguridad del GPO. La guía de seguridad de Windows Server 2008 [https://go.microsoft.com/fwlink/p/?LinkId=145186](https://go.microsoft.com/fwlink/p/?linkid=145186) , que se encuentra en el Windows server 2008 R2 Security Compliance Management Toolkit [https://go.microsoft.com/fwlink/p/?LinkId=211882](https://go.microsoft.com/fwlink/p/?linkid=211882) , incluye un número de plantillas de ejemplo que puede modificar para satisfacer sus necesidades.

</div>

<div>

## <a name="best-practices"></a>Procedimientos recomendados

  - Proteger todos los sistemas operativos de servidor y las aplicaciones.

  - Proteger las instantáneas del servidor y mejorar la seguridad de todos los servidores virtuales.

  - Use directivas de grupo para implementar bloqueos de seguridad.

</div>

</div>

<span> </span>

</div>

</div>

</div>

