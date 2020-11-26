---
title: Migración de reuniones existentes y contenido de reuniones
description: Migrar las reuniones y el contenido de la reunión existentes.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate existing meetings and meeting content
ms:assetid: 30516731-2ae1-4a6d-a7e1-d3f05778c954
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688011(v=OCS.15)
ms:contentKeyID: 49733599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d94dd35063a121a057a218c27fdb36e42a155b77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443807"
---
# <a name="migrate-existing-meetings-and-meeting-content"></a>Migración de reuniones existentes y contenido de reuniones

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-02-22_

Cuando una cuenta de usuario se mueve de Lync Server 2010 a un servidor de Lync Server 2013, la siguiente información se mueve con esa cuenta de usuario:

  - **Reuniones ya programadas por el usuario**. Esto incluye mover los directorios de conferencias y los datos de la Conferencia.

  - **Número de identificación personal (PIN) del usuario**. El PIN actual del usuario sigue funcionando hasta que venza o cuando el usuario solicite un nuevo PIN.

La siguiente información de la cuenta de usuario no se mueve al nuevo servidor.

  - **Contenido** de la reunión. Para mover el contenido compartido durante una reunión, por ejemplo, PowerPoint, whiteboard, datos adjuntos o sondeo de datos, use el parámetro **-MoveConferenceData** como parte del cmdlet **Move-CsUser** .

</div>

<span> </span>

</div>

</div>

</div>

