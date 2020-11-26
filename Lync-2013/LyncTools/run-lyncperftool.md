---
title: Ejecutar LyncPerfTool
description: Ejecute LyncPerfTool.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Run LyncPerfTool
ms:assetid: f2fd1940-d744-47b5-b299-04a914039182
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945612(v=OCS.15)
ms:contentKeyID: 51541437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3278754c9154f47602c5c4f1fa95cdc4b465b228
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446410"
---
# <a name="run-lyncperftool"></a>Ejecutar LyncPerfTool

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-02-24_

Antes de ejecutar la herramienta Lync Server 2013 stress and Performance (LyncPerfTool.exe), debe crear usuarios, contactos y escenarios. Para obtener más información sobre cómo usar las herramientas para realizar estas acciones, consulte [crear usuarios y contactos](create-users-and-contacts.md) y [configurar el perfil de usuario](configure-user-profile.md). Al ejecutar estas herramientas, también se generará un archivo que se ejecutará LyncPerfTool.exe como parte de un archivo por lotes con los parámetros obligatorios incluidos.

<div>

## <a name="running-the-lync-server-2013-stress-and-performance-tool"></a>Ejecutar la herramienta Lync Server 2013 stress and Performance

La herramienta de UserProfileGenerator.exe crea un archivo por lotes que le permite ejecutar LyncPerfTool.exe registrando los contadores de rendimiento de LyncPerfTool y cargando el archivo de configuración XML. El archivo de proceso por lotes ejecuta una instancia de LyncPerfTool.exe por archivo de configuración. Para ejecutar el archivo de proceso por lotes, haga lo siguiente:

1.  Copie la carpeta que contiene los archivos y las carpetas de configuración en el directorio que contiene LyncStressTool.exe en cada equipo cliente. (Por ejemplo, si ha generado los archivos de configuración en la carpeta denominada 1,28 \_ 13.16.16, copie esa carpeta a la carpeta que contiene LyncPerfTool.exe en cada cliente).

2.  Vaya a la carpeta cliente con el número adecuado y ejecute el script de proceso por lotes RunClient. Simplemente puede hacer doble clic en el archivo de proceso por lotes en el explorador de Windows y se ejecutarán todos los archivos de configuración de ese número de cliente. También puede ejecutar el script desde la carpeta de cliente adecuada con la siguiente sintaxis:

    ```Batch
        RunClient0.bat "C:\Program Files\Microsoft Lync Server 2013\LyncStressAndPerfTool\LyncStress" 
    ```
Para ejecutar LyncPerfTool.exe directamente, abra un símbolo del sistema y escriba el comando siguiente en la línea de comandos (al hacerlo por primera vez, asegúrese de registrar los contadores de rendimiento regsvr32/i/n/s LyncPerfToolPerf.dll, tal y como se muestra en la nota más adelante en este tema) :LyncPerfTool.exe/File:\<configXML\>
```Powershell
    LyncPerfTool.exe /file:IM_client0.xml
```
Para que la herramienta muestre los valores en el archivo de configuración, incluya el parámetro/displayfile en el comando anterior, como este:
```Powershell
    LyncPerfTool.exe /file:IM_client0.xml /displayfile
```
Para finalizar el proceso, presione Ctrl + C.

<div>


> [!NOTE]  
> Antes de ejecutar LyncPerfTool directamente, debe registrar los contadores de rendimiento. Escriba el siguiente comando para registrar los contadores de rendimiento:



</div>

```Powershell
    regsvr32 /i /n /s LyncPerfToolPerf.dll
```
<div>


> [!NOTE]  
> Cada instancia de LyncPerfTool.exe que inicie iniciará inmediatamente la sesión de los usuarios, generalmente a una tarifa de un usuario por segundo. La frecuencia máxima de inicio de sesión de usuario para el grupo es de aproximadamente 12 por segundo. Esto significa que no debe iniciar más de 12 instancias de LyncPerfTool al mismo tiempo, mientras los usuarios aún están iniciando sesión. 1000 los usuarios tomarán aproximadamente 20 minutos para iniciar sesión por completo, a una por segundo.



</div>

</div>

<div>

## <a name="see-also"></a>Vea también


[Crear usuarios y contactos](create-users-and-contacts.md)  
[Configurar Perfil de usuario](configure-user-profile.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

