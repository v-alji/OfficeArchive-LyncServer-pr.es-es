---
title: 'Lync Server 2013: componentes usados por la recogida de llamadas grupales'
description: 'Lync Server 2013: componentes usados por la recogida de llamadas grupales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Group Call Pickup
ms:assetid: 45db2f23-d486-4b20-a8cf-7b48a1f9fd3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945625(v=OCS.15)
ms:contentKeyID: 51541470
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 517f75dcbac8bfed0e749c061a9696b7667e10ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398525"
---
# <a name="components-used-by-group-call-pickup-in-lync-server-2013"></a>Componentes usados por la recogida de llamadas grupales en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-01-30_

La recopilación de llamadas grupales se implementa automáticamente al implementar la telefonía IP empresarial y la aplicación estacionamiento de llamadas. Para habilitar la recopilación de llamadas de grupo, configure la tabla de llamadas en órbita con intervalos de números designados como números de grupo de recogida de llamadas y, a continuación, asigne usuarios para llamar a grupos de recogida y habilitar a los usuarios para la recogida de llamadas grupales. Los siguientes componentes de Lync Server admiten la recogida de llamadas de Grupo:

  - **Servicio de aplicación**   El servicio de aplicación proporciona una plataforma para implementar, hospedar y administrar aplicaciones de comunicaciones unificadas, como la aplicación de estacionamiento de llamadas. El servicio de aplicaciones se instala automáticamente en todos los servidores front-end de un grupo de servidores front-end y en todos los servidores Standard Edition.

  - **Aplicación de estacionamiento de llamadas**   La aplicación de estacionamiento de llamadas es una de las aplicaciones de comunicaciones unificadas que se hospedan en el servicio de aplicación. La recogida de llamadas grupales se basa en la aplicación de estacionamiento de llamadas.

  - **Shell de administración de Lync Server**   Use el shell de administración de Lync Server para administrar grupos de recopilación de llamadas de grupo.

  - **Herramienta del kit de recursos de SEFAUtil**   Use la utilidad de activación de características de extensión secundaria (SEFAUtil) para asignar usuarios a un grupo de recogida de llamadas y para habilitar o deshabilitar la recogida de llamadas para los usuarios.

</div>

<span> </span>

</div>

</div>

</div>

