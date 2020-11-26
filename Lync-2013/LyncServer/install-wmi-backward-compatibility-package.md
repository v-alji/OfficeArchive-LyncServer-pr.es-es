---
title: Instalar el paquete de compatibilidad con versiones anteriores de WMI
description: Instalar el paquete de compatibilidad con versiones anteriores de WMI.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Install WMI Backward Compatibility package
ms:assetid: 38797fbd-06a0-4008-b099-158e7b5d7703
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204816(v=OCS.15)
ms:contentKeyID: 48183893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9062e209981fd180b8772801960bd94d2256513a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439585"
---
# <a name="install-wmi-backward-compatibility-package"></a>Instalar el paquete de compatibilidad con versiones anteriores de WMI

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-02_

Si intenta ejecutar el Asistente para la combinación del generador de topología sin instalar el paquete de compatibilidad con versiones anteriores de WMI, verá el siguiente error:

![Mensaje de error de WMI](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "Mensaje de error de WMI")

Si intenta ejecutar el cmdlet **Merge-CsLegacytopology** sin instalar el paquete de compatibilidad con versiones anteriores de WMI, verá el siguiente error:

![Error del proveedor WMI de Windows PowerShell](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Error del proveedor WMI de Windows PowerShell")

Para instalar el paquete de compatibilidad con versiones anteriores de WMI

1.  Desde los medios de instalación, vaya a configuración de instalación de \\ \\ AMD64 \\ \\OCSWMIBC.MSI.

2.  Instalar OCSWMIBC.MSI.
    
    <div>
    

    > [!IMPORTANT]  
    > OCSWMIBC.msi debe instalarse en el equipo en el que se ejecuta el Asistente para la combinación del generador de topología. Sin embargo, le recomendamos que instale OCSWMIBC.msi en todos los servidores front-end de su topología.

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > OCSWMIBC.msi se puede instalar en cualquier equipo del dominio que tenga instalados los componentes principales de Lync Server 2013 y el shell de administración de Lync Server 2013, y tiene acceso a la topología de Office Communications Server 2007 R2 (proveedor WMI a servicios de dominio de Active Directory (AD DS) y a SQL Server).

    
    </div>

</div>

<span> </span>

</div>

</div>

</div>

