---
title: 'Lync Server 2013: tareas necesarias'
description: 'Lync Server 2013: tareas necesarias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: As-needed tasks
ms:assetid: b66bc6fe-f138-4cf4-ba7f-aee9a3e0497e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn722431(v=OCS.15)
ms:contentKeyID: 63969643
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91fe249d9615bb619426c58b22606c3ef182f9a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440552"
---
# <a name="as-needed-tasks-in-lync-server-2013"></a>Tareas necesarias en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2014-08-18_

Realice las siguientes tareas según sea necesario. Suelen estar cubiertos por procedimientos estándar:

  - * * Auditoría de seguridad completa * * puede realizar esta auditoría regularmente, en respuesta a una actualización o un nuevo diseño del sistema de mensajería, o en respuesta a una infracción de seguridad intentada (o exitosa). El procedimiento puede implicar recorridos de puertos en servidores y firewalls, auditorías de correcciones de seguridad y pruebas de penetración de terceros.

  - **Reemplazar certificados a punto de expirar**   La comprobación de los certificados de Lync Server es una de las tareas semanales normales y, como parte del procedimiento, un administrador debe tener un registro de todas las fechas de vencimiento de los certificados. Este registro permite a un administrador crear una notificación cuando un certificado determinado va a expirar y sustituirse según sea necesario.

  - **Actualizar líneas de base de rendimiento**   Actualice las líneas de base del rendimiento después de un cambio de configuración o actualización. Su organización puede usar líneas base para medir los cambios de rendimiento y detectar problemas que afectan al rendimiento del sistema.

  - **Administrar un grupo**   de servidores Enterprise   Durante la implementación de los servidores individuales, se realizó la configuración inicial de los grupos empresariales, los servidores Standard Edition y cualquier otro servidor del entorno de la organización. La administración posterior a la implementación de servidores y grupos de servidores Standard Edition y grupos de servidores Enterprise incluye las siguientes tareas:
    
      - Administración de servidores front-end
    
      - Administrar conferencias web
    
      - Administrar conferencias
    
      - Cambiar las credenciales de la cuenta de servicio
    
      - Administración de bases de datos
    
      - Iniciar y detener servicios y desactivar roles de servidor
    
      - Quitar servidores y roles de servidor, quitar grupos y retirar servidores y grupos de servidores

  - **Administrar el uso**   Puede configurar Lync Server 2013 para proporcionar las características y funcionalidades más apropiadas para su organización. Entre estas directivas se incluyen:
    
      - Administración de la compatibilidad de las reuniones de conferencias web locales
    
      - Administrar el uso de grupos de distribución para enviar mensajes instantáneos
    
      - Administración de contactos, presencia y consultas
    
      - Configuración del filtrado de versiones de cliente
    
      - Configuración del filtrado inteligente de mensajes instantáneos
    
      - Configurar el archivado, grabación de llamadas en profundidad y cumplimiento de las reuniones

  - **Administración de la Conectividad del servidor perimetral**   La administración continua de los servidores y la configuración necesaria para proporcionar conectividad externa incluye lo siguiente:
    
      - Administración de la conectividad entre servidores internos y servidores perimetrales
    
      - Configuración de interfaces y certificados internos y externos para servidores perimetrales
    
      - Administrar el acceso de socios federados

  - **Administración de la libreta de direcciones**   La administración de los servidores de la libreta de direcciones incluye lo siguiente:
    
      - Configuración de la normalización del teléfono del servidor de libreta de direcciones
    
      - Administrar el servidor de la libreta de direcciones desde la línea de comandos

  - **Administrar cuentas de usuario**   La administración de cuentas de usuario incluye lo siguiente:
    
      - Habilitar cuentas de usuario para Lync Server
    
      - Configuración de usuarios de Lync Server mediante el asistente
    
      - Configuración de las propiedades de la cuenta de usuario de Lync Server
    
      - Buscar usuarios de Lync Server
    
      - Mover usuarios de Lync Server
    
      - Eliminar usuarios de Lync Server

  - **Analizar los archivos de registro de 2013 de Lync Server**   Una herramienta muy útil, generalmente usada para la solución de problemas, es la herramienta de registro de Lync Server 2013, que se describe en detalle en uso de la [herramienta de registro de Lync server 2013](https://technet.microsoft.com/library/gg558599.aspx).

Como la herramienta de registro genera archivos de registro (en cada servidor), estos archivos de registro se pueden ver y analizar mediante la herramienta de supervisión, si las herramientas del kit de recursos de Microsoft Office Server 12 están instaladas en el equipo. De lo contrario, los registros también se pueden analizar con un editor de texto, que es mucho menos transparente y más complejo que el uso de la utilidad de supervisión.

Para ver y analizar los mensajes de protocolo

En la herramienta de registro, cuando haya finalizado la sesión de depuración, haga clic en analizar archivos de registro para ver los archivos de registro con la herramienta de supervisión. Puede analizar los registros de protocolo para los siguientes componentes:

  - Lync Server SipStack (SIP)

  - Lync Server S4 (SIP)

  - El tráfico de señalización de conferencias de Lync Server (C3P), incluido el C3P de infrarrojos y el foco C3P

  - Tráfico de conferencias web de Lync Server (PSOM)

  - Cliente de la plataforma de cliente de comunicaciones unificadas de Lync Server (UCCP)

  - Informes de errores de la base de datos de archivado

Para ayudarle a organizar el rendimiento de las tareas necesarias, consulte As-Needed lista de comprobación de operaciones.

<div>


> [!IMPORTANT]  
> Para obtener información detallada sobre la administración y los procedimientos de administración, consulte la guía de administración de Microsoft Lync Server 2013.



</div>

<div>

## <a name="backup-and-restore-policies-or-configuration-settings"></a>Directivas de copia de seguridad (y restauración) o configuración

Lync Server 2013 le permite realizar copias de seguridad y restaurar todo el sistema. IIF quiere hacer una copia de seguridad (y, a continuación, quizás una vez restaurada) una sola directiva o una sola recopilación de parámetros de configuración, recuperar la directiva correspondiente y, a continuación, canalizar ese objeto al cmdlet Export-Clixml, que guarda la información de la Directiva como un archivo XML:

`Get-CsClientPolicy -Identity "RedmondClientPolicy" | Export-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

Ahora puede experimentar con RedmondClientPolicy y cambiar la configuración. Si, en su lugar, decide restaurar la directiva anterior, escriba:

`$x = Import-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

`Set-CsClientPolicy -Instance $x`

Tenga en cuenta que este enfoque funcionará para la mayoría de las directivas y la configuración, pero no funcionará con algunos de los elementos más complejos (elementos que contienen varios subobjetos, como las opciones de configuración de enrutamiento, que contienen distintas rutas de voz).

</div>

</div>

<span> </span>

</div>

</div>

</div>

