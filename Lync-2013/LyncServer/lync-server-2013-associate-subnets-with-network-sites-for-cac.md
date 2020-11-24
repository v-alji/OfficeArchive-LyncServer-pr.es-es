---
title: 'Lync Server 2013: asociar subredes con sitios de red para CAC'
description: 'Lync Server 2013: asocie subredes con sitios de red para CAC.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Associate subnets with network sites for CAC
ms:assetid: a749c9b3-15f3-4e74-9f43-1507d3c2c940
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412786(v=OCS.15)
ms:contentKeyID: 48185017
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8d68607c1674bb964c27c8408583be7f5e092f4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399965"
---
# <a name="associate-subnets-with-network-sites-for-cac-in-lync-server-2013"></a>Asociar subredes con sitios de red para CAC en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-20_

Cada subred de su red debe estar asociada a un sitio de red específico. Esto se debe a que la información de subred se usa para determinar el sitio de red en el que se encuentra un extremo. Cuando se conocen las ubicaciones de ambas partes en una sesión, control de admisión de llamadas (CAC) puede determinar si hay suficiente ancho de banda para establecer una llamada.

El control de admisión de llamadas no tiene ningún requisito especial para la Asociación de subredes con sitios de red. Para crear una asociación entre las subredes y los sitios de red de su topología, siga los procedimientos que se describen en [asociar una subred con un sitio de red en Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md). Para ver los sitios de red (y sus respectivas subredes) en la topología de red de ejemplo para el control de admisión de llamadas, vea [ejemplo: recopilar los requisitos para el control de admisión de llamadas en Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) en la documentación de planeación.

</div>

<span> </span>

</div>

</div>

</div>

