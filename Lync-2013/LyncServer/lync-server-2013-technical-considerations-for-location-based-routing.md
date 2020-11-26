---
title: 'Lync Server 2013: Consideraciones técnicas para el enrutamiento basado en ubicación'
description: 'Lync Server 2013: consideraciones técnicas para el enrutamiento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical considerations for Location-Based Routing
ms:assetid: 2e2a9199-7c6f-48d3-9adb-3873fc4f8c4e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994027(v=OCS.15)
ms:contentKeyID: 51803936
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54a025af81ab148ad41f95d0a8cf4f900beb7e00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423431"
---
# <a name="technical-considerations-for-location-based-routing-in-lync-server-2013"></a>Consideraciones técnicas para el enrutamiento basado en ubicación en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-03-09_

Al planear Location-Based el enrutamiento, debe considerar el impacto en los siguientes escenarios.

<div>

## <a name="disaster-recovery"></a>Recuperación ante desastres

Durante una conmutación por error del repositorio principal a un grupo de copia de seguridad, así como al restaurar las operaciones normales en el grupo principal, el enrutamiento de Location-Based se aplica en todo momento durante un procedimiento de recuperación y desastres.

</div>

<div>

## <a name="survivable-branch-appliance"></a>Aplicación de sucursal con funciones de supervivencia

La configuración del enrutamiento de Location-Based afecta al planeamiento de la ubicación en la que se implementan las puertas de enlace asociadas a los equipos de las sucursales que son revivientes. La puerta de enlace asociada a su SBA debe estar ubicada en el mismo sitio de red que su equipo de sucursal con la supervivencia; de lo contrario, los usuarios alojados en su equipo de sucursal con su supervivencia no podrán realizar llamadas salientes si Location-Based enrutamiento está configurado. Cuando la conexión WAN entre el equipo de la sucursal y el sitio central está inactiva, se exige la aplicación de las restricciones de enrutamiento de Location-Based.

</div>

<div>

## <a name="see-also"></a>Vea también


[Planificar el enrutamiento basado en ubicación en Lync Server 2013](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

