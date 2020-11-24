---
title: 'Lync Server 2013: configuración del enrutamiento basado en ubicación para conferencias'
description: 'Lync Server 2013: configuración de Location-Based enrutamiento para conferencias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399948"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a>Configuración del enrutamiento basado en ubicación para conferencias de Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-09-11_

La aplicación de conferencia de Location-Based enrutamiento depende de la configuración del enrutamiento de Location-Based de Lync Server 2013. Las siguientes son las opciones de configuración principales:

  - La ubicación de los participantes que se unen a una reunión se determina a partir de su sitio de red. Para exigir Location-Based enrutamiento, debe definirse un sitio de red y sus subredes de red asociadas en Lync Server.

  - Para exigir Location-Based el enrutamiento de reuniones, los participantes de Lync deben estar habilitados para Location-Based el enrutamiento.

  - Para exigir Location-Based enrutamiento de puntos de conexión RTC que se unen a las reuniones, el troncal SIP usado para conectar los puntos de conexión RTC debe configurarse para el enrutamiento de Location-Based.

Para obtener más información sobre cómo implementar y configurar Lync Server 2013 Location-Based enrutamiento, consulte Configuración del [enrutamiento basado en la ubicación](lync-server-2013-configuring-location-based-routing.md).

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a>Habilitar la aplicación Location-Based de conferencia de enrutamiento

La aplicación Location-Based de conferencia de enrutamiento está deshabilitada de forma predeterminada. Antes de habilitar esta aplicación, tienes que determinar la prioridad adecuada para asignar a la aplicación. Para determinar esta prioridad, ejecute el siguiente cmdlet en el shell de administración de Lync Server:

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

En este cmdlet, \<Pool FQDN\> se encuentra el grupo en el que se habilitará la aplicación de conferencia de enrutamiento de Location-Based.

Este cmdlet devolverá la lista de las aplicaciones hospedadas por Lync Server y el valor de prioridad de cada una de ellas. La aplicación de conferencia de Location-Based enrutamiento debe tener asignado un valor de prioridad mayor que el de la aplicación "UdcAgent" y menor que las aplicaciones "DefaultRouting", "ExumRouting" y "OutboundRouting". Le recomendamos que asigne el Location-Based aplicación de conferencia de enrutamiento un valor de prioridad que sea un punto superior al valor de prioridad de la aplicación "UdcAgent".

Por ejemplo, si la aplicación "UdcAgent" tiene un valor de prioridad de "2", la aplicación "DefaultRouting" tiene un valor de prioridad de "8", la aplicación "ExumRouting" tiene un valor de prioridad de "9" y la aplicación "OutboundRouting" tiene un valor de prioridad de "10", debe asignar la Location-Based aplicación de conferencia de enrutamiento como valor de prioridad Al hacerlo, la prioridad de las aplicaciones quedará ordenada así: otras aplicaciones (prioridades: de 0 a 1), “UdcAgent” (prioridad: 2), aplicación de conferencias con enrutamiento basado en ubicación (prioridad: 3), otras aplicaciones (prioridades: de 4 a 8), “DefaultRouting” (prioridad: 9), “ExumRouting” (prioridad: 10) y “OutboundRouting” (prioridad: 11).

Después de encontrar el valor de prioridad correcto para la aplicación de conferencia de enrutamiento de Location-Based, escriba el siguiente cmdlet para cada Front-End servidor Standard Edition o grupo de servidores que aloje usuarios habilitados para Location-Based enrutamiento:

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

Por ejemplo:

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

Después de usar este cmdlet, reinicie todos los servidores front-end del grupo o los servidores Standard Edition donde se haya habilitado la aplicación de conferencia de enrutamiento de Location-Based.

<div>


> [!IMPORTANT]  
> Location-Based la aplicación de enrutamiento a las conferencias o a las transferencias de asesoría no se aplicará hasta que se reinicien todos los servidores front-end de los servidores Standard Edition o Standard Edition.



</div>

Una vez que la aplicación de conferencia de enrutamiento de Location-Based se haya habilitado correctamente y se hayan reiniciado todos los servidores de Lync aplicables, se supervisarán todas las conferencias organizadas por usuarios de Lync habilitados para Location-Based enrutamiento para evitar el bypass de llamadas RTC.

</div>

</div>

<span> </span>

</div>

</div>

</div>

