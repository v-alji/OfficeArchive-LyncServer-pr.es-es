---
title: Información general de conferencia de Lync Server 2013 A/V
description: 'Lync Server 2013: información general sobre conferencias A/V.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: A/V conferencing overview
ms:assetid: 9583de87-4618-4a99-a47a-45e8cc4cc221
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619186(v=OCS.15)
ms:contentKeyID: 49733747
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76ef4f76a4df0187a7c36394b2c95e99876df9be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439553"
---
# <a name="overview-of-av-conferencing-in-lync-server-2013"></a>Información general sobre las conferencias A/V en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-13_

La conferencia A/V permite comunicaciones de audio y vídeo en tiempo real entre los usuarios. Al implementar las conferencias, puede elegir entre habilitar y usar conferencias web y conferencias A/V, o simplemente conferencias web.

Para planear una conferencia A/V, necesita conocer el ancho de banda necesario para el tipo de medio de conferencia que requiere su organización. Esto podría incluir audio, vídeo y vídeo panorámico.

Antes de habilitar a los usuarios para conferencias de A/V, asegúrese de que su red puede controlar la carga resultante. Si el ancho de banda de red no es suficiente, la experiencia del usuario puede verse afectada en gran medida. Puede usar control de admisión de llamadas (CAC) para administrar el ancho de banda de red usado por conferencias A/V. Esto es importante para redes restringidas, como vínculos de ancho de banda limitados entre los sitios centrales y de sucursal. Para obtener más información, vea [información general sobre el control de admisión de llamadas en Lync Server 2013](lync-server-2013-overview-of-call-admission-control.md). Para obtener más información sobre los requisitos de ancho de banda de multimedia, consulte [requisitos de ancho de banda de red para el tráfico multimedia en Lync Server 2013](lync-server-2013-network-bandwidth-requirements-for-media-traffic.md).

Si implementa las audioconferencias en su red, los usuarios necesitarán dispositivos de audio, como pueden ser auriculares, para participar en las audioconferencias. Si implementa las videoconferencias, necesita implementar dispositivos de vídeo, como cámaras web para los usuarios. Le recomendamos que use dispositivos de comunicaciones unificadas (UC) certificados por Microsoft para todos los tipos de dispositivos, para garantizar una experiencia de usuario óptima. Para obtener más información sobre los dispositivos certificados por UC, consulte "teléfonos y dispositivos para Lync" en [https://go.microsoft.com/fwlink/p/?LinkId=263861](https://go.microsoft.com/fwlink/p/?linkid=263861) . Para los dispositivos de audio o vídeo, la implementación de dispositivos y el aprendizaje del usuario, es importante tener en cuenta y planear.

En las siguientes secciones se describen las características de las conferencias de audio y vídeo, incluida la información sobre la administración del ancho de banda y la selección de los clientes apropiados.

<div>

## <a name="audio-conferencing-features"></a>Características de las conferencias de audio

Lync Server 2013 ofrece varias características que puede usar para configurar la experiencia de audioconferencia para el usuario, entre las que se incluyen las siguientes:

  - **Silencio**   de la audiencia   El moderador puede usar esta configuración para silenciar a todos los participantes de audio de la Conferencia y poner la Conferencia en un estado en el que no los moderadores no puedan reactivarse.

  - **Anuncios de entrada y salida de conferencias**   Si ha habilitado las conferencias de acceso telefónico local, los moderadores pueden usar esta opción para activar o desactivar los anuncios de entrada y salida a fin de minimizar las distracciones mientras está en curso una conferencia.

  - **Agregar un usuario marcando**   Los moderadores y los asistentes a los que se les ha concedido permiso pueden agregar números de RTC a las conferencias y hacer que la Conferencia se llame a esos números.

</div>

<div>

## <a name="video-conferencing-features"></a>Características de videoconferencias

Lync Server 2013 ofrece varias características que puede usar para configurar la experiencia de videoconferencia para el usuario, entre las que se incluyen las siguientes:

  - **Vista de Galería**   En las videoconferencias que tengan más de dos personas, los usuarios verán automáticamente a todos los participantes de la Conferencia. Si la conferencia tiene más de cinco participantes, el vídeo de los participantes más activos se muestra en la fila superior y solo se muestra la foto de los demás participantes. De forma predeterminada, el vídeo entre varias partes está activado. Para obtener detalles sobre la configuración o desactivación del vídeo de varias partes, vea [configurar el ancho de banda de vídeo en Lync Server 2013](lync-server-2013-configuring-video-bandwidth.md).

  - **Vídeo panorámico**   Si un dispositivo de videoconferencia RoundTable está instalado en el salón de conferencias, esta característica proporciona una vista completa de 360 grados de la sala de conferencias. La tira de vídeo panorámico solo está disponible con dispositivos RoundTable.

  - **Modo de vídeo solo para el moderador**   Los moderadores pueden configurar la reunión para que solo se muestre el vídeo del moderador. Así se evitan distracciones en reuniones grandes cuando hay disponibles varias secuencias de vídeo y se bloquean los diferentes orígenes. Este modo también se aplica al vídeo capturado y proporcionado por dispositivos RoundTable.

  - **Video de alta definición**   Los usuarios pueden experimentar resoluciones de hasta 1080P HD en llamadas de dos participantes y en conferencias de varias partes.

  - **Foco de vídeo**   Los moderadores pueden configurar la reunión para que los otros participantes de la Conferencia solo vean el vídeo de un participante seleccionado que sea una fuente de video. Este modo también se aplica al vídeo capturado y proporcionado por dispositivos RoundTable de vídeo panorámico.

</div>

</div>

<span> </span>

</div>

</div>

</div>

