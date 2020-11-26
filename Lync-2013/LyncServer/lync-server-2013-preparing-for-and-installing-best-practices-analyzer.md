---
title: 'Lync Server 2013: preparación para la instalación del analizador de procedimientos recomendados'
description: 'Lync Server 2013: preparación de e instalación del analizador de procedimientos recomendados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing for and installing Best Practices Analyzer
ms:assetid: 550613dd-dc08-482e-9980-a3fe187cd162
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591347(v=OCS.15)
ms:contentKeyID: 48184149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 005c5ac372a3564e74af549832830ebae899e9d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424145"
---
# <a name="preparing-for-and-installing-best-practices-analyzer-in-lync-server-2013"></a>Preparación de e instalación del analizador de procedimientos recomendados en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-11-07_

Para realizar las tareas que se describen en este tema, debe haber iniciado sesión como miembro del grupo administradores.

<div>

## <a name="system-requirements-for-best-practices-analyzer-installation"></a>Requisitos del sistema para la instalación del analizador de procedimientos recomendados

Para ejecutar Lync Server 2013, analizador de procedimientos recomendados para explorar su entorno, el equipo debe ejecutar una edición de 64 bits de uno de los siguientes sistemas operativos:

  - Sistema operativo estándar Windows Server 2008 R2 con Service Pack 1 (SP1)

  - Sistema operativo Windows Server 2008 R2 con SP1 Enterprise

  - Sistema operativo Windows Server 2008 R2 con SP1 Datacenter

  - Sistema operativo Windows Server 2012 Datacenter

  - Sistema operativo Windows Server 2012 Standard

  - Sistema operativo Windows Server 2012 Enterprise

  - Sistema operativo Windows Server 2012 R2 Datacenter

  - Sistema operativo Windows Server 2012 R2 Standard

  - Sistema operativo Windows Server 2012 R2 Enterprise

  - Sistema operativo Windows 8

  - Sistema operativo Windows 7

El equipo también debe estar ejecutando lo siguiente:

  - Microsoft .NET Framework 4,5. Para Lync Server 2013, debe instalar manualmente la edición de 64 bits de Microsoft .NET Framework 4,5 en el servidor antes de instalar Lync Server 2013.

  - Lync Server 2013, componentes principales.

  - Paquete de compatibilidad con versiones anteriores de WMI. Para obtener más información, consulte [instalar el paquete de compatibilidad con versiones anteriores de WMI](install-wmi-backward-compatibility-package.md) en la documentación de la migración.

  - Windows PowerShell 3,0. Para obtener más información, consulte [instalar Windows PowerShell 3,0 para Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md) en la documentación de implementación.

Puede instalar Best Practices Analyzer en equipos con un sistema operativo compatible que no ejecute Lync Server 2013, los componentes básicos o el paquete de compatibilidad con versiones anteriores de WMI, pero puede usar Best Practices Analyzer en esos equipos solo para ver los informes, no para realizar análisis.

</div>

<div>

## <a name="choosing-a-computer-for-installation"></a>Elegir un equipo para la instalación

Le recomendamos que instale Lync Server 2013, Best Practices Analyzer en un equipo dedicado a la administración de Lync Server 2013. Puede instalar la herramienta en un servidor que ejecute Lync Server 2013 o en un equipo administrativo que ejecute herramientas administrativas 2013 de Lync Server. Si instala la herramienta en un servidor que ejecuta Lync Server, le recomendamos que use la herramienta para examinar solo ese servidor.

</div>

<div>

## <a name="installing-best-practices-analyzer"></a>Instalación del analizador de procedimientos recomendados

Puede descargar Best Practices Analyzer para Lync Server 2013 en [https://go.microsoft.com/fwlink/p/?linkId=266539](https://go.microsoft.com/fwlink/p/?linkid=266539) .

Para instalar Best Practices Analyzer, inicie el archivo de Microsoft Installer RtcBPA.msi en el equipo en el que desea instalar la herramienta y, a continuación, siga las instrucciones que aparecen en la pantalla. La ubicación predeterminada para instalar los archivos de programa es \<system drive\> \\ archivos de programa de \\ Lync Server 2013 \\ BPA.

</div>

</div>

<span> </span>

</div>

</div>

</div>

