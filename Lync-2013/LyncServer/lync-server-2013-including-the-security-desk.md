---
title: 'Lync Server 2013: incluido el escritorio de seguridad'
description: 'Lync Server 2013: incluido el escritorio.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Including the security desk
ms:assetid: 4b1d9125-7488-419b-85dd-a8dd3ab5add3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398299(v=OCS.15)
ms:contentKeyID: 48184084
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23a5b01dff5e3db8293944033f1f3b675bbc4d37
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427309"
---
# <a name="including-the-security-desk-in-lync-server-2013"></a>Incluido el escritorio de seguridad de Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-02_

Puede que su compañía requiera que el servicio de seguridad participe en una llamada de emergencia. Para ayudarle a decidir cómo integrar el servicio de seguridad en la implementación de E9-1-1, necesitarás responder a las preguntas que se indican a continuación.

  - **¿Desea que el departamento de seguridad reciba una notificación cuando haya una llamada de emergencia?**  
    Puede configurar la Directiva de ubicación para que Lync Server envíe alertas de mensajería instantánea (mi) a las direcciones SIP de Lync de uno o más personal de seguridad. Estas alertas incluyen el nombre, el número y la ubicación de la persona que realiza la llamada de emergencia, y facilita que el personal de seguridad pueda ayudar en la situación de emergencia.

<!-- end list -->

  - **¿Desea que el departamento de seguridad establezca una conferencia en todas las llamadas de emergencia?**  
    En el caso de que el proveedor de servicios de emergencia lo permita, puedes configurar la directiva de ubicación para incluir un número de devolución de llamada ante cada llamada de emergencia. Este número lo usa después el proveedor para que el personal de seguridad de la organización establezca una conferencia en las llamadas de emergencia. Esta conferencia se puede configurar en la directiva de ubicación para que sea unidireccional (de solo escucha) o bidireccional (de dos vías).

<div>


> [!NOTE]  
> Si lo deseas, puedes configurar miembros del personal de emergencia diferentes para cada directiva de ubicación. Esto te permite personalizar la respuesta para las diferentes áreas de la compañía o crear un comportamiento diferente para las llamadas de emergencia originadas en el interior en contraposición con las realizadas en el exterior de la red. Puedes usar grupos de distribución para especificar el personal al que deseas notificar.



</div>

</div>

<span> </span>

</div>

</div>

</div>

