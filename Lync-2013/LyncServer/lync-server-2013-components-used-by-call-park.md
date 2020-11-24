---
title: 'Lync Server 2013: Componentes que usa el estacionamiento de llamadas'
description: 'Lync Server 2013: componentes usados por el parque de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Call Park
ms:assetid: c7ffbee3-0ce1-48c0-bb56-af098b41d6d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398824(v=OCS.15)
ms:contentKeyID: 48185374
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 285af316fa2d49e8bebf68e11de6d9526e12ae29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398526"
---
# <a name="components-used-by-call-park-in-lync-server-2013"></a>Componentes que usa el estacionamiento de llamadas en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-09-13_

La aplicación de estacionamiento de llamadas se instala automáticamente al implementar la telefonía IP empresarial. Para habilitar el parque de llamadas, configure la Directiva de voz. Los siguientes componentes de Lync Server 2013 son compatibles con la aplicación estacionamiento de llamadas:

  - **Servicio de aplicación**   El servicio de aplicación proporciona una plataforma para implementar, hospedar y administrar aplicaciones de comunicaciones unificadas, como la aplicación de estacionamiento de llamadas. El servicio de aplicaciones se instala automáticamente en todos los servidores front-end de un grupo de servidores front-end y en todos los servidores Standard Edition.

  - **Aplicación de estacionamiento de llamadas**   La aplicación de estacionamiento de llamadas es una de las aplicaciones de comunicaciones unificadas que se hospedan en el servicio de aplicación. Se incluye automáticamente al implementar la telefonía IP empresarial. Llama a parques de aparcamiento y recupera llamadas y administra las órbitas del parque de llamadas.

  - **Música en espera-archivo**   Si está habilitada la música, el archivo de música se reproduce mientras se estaciona una llamada. Cuando se instala la aplicación de estacionamiento de llamadas, se incluye un archivo de música predeterminado.

  - **Almacén de archivos**   La aplicación de estacionamiento de llamadas usa el almacén de archivos para almacenar los archivos de audio personalizados.

  - **Panel de control de Lync Server**   Puede usar el panel de control de Lync Server para configurar la tabla orbital de llamadas y para habilitar el parque de llamadas para los usuarios.

  - **Shell de administración de Lync Server**   Toda la configuración de la aplicación estacionamiento de llamadas se puede realizar con los cmdlets del shell de administración de Lync Server.

</div>

<span> </span>

</div>

</div>

</div>

