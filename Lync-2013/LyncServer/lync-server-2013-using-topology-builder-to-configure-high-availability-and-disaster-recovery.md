---
title: Usar Topology Builder para configurar la alta disponibilidad y la recuperación ante desastres
description: Usar el generador de topología para configurar la alta disponibilidad y la recuperación ante desastres.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Topology Builder to configure high availability and disaster recovery
ms:assetid: abc1a25d-1f5e-46ef-91d2-0144fc847206
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205172(v=OCS.15)
ms:contentKeyID: 48185113
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04764a58ac3ae1bbe0df97aadeabb03158ce8100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400116"
---
# <a name="using-topology-builder-to-configure-high-availability-and-disaster-recovery-in-lync-server-2013"></a>Usar Topology Builder para configurar la alta disponibilidad y la recuperación ante desastres en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-06_

Siga los pasos que se indican en el generador de topología para configurar la alta disponibilidad y la recuperación ante desastres para el servidor de chat persistente.

1.  Agregue las bases de datos reflejadas y de trasvase de registros que SQL Server almacena.

2.  Edite las propiedades del servicio del servidor de chat persistentes en:
    
    1.  Habilite la creación de reflejo para la base de datos principal.
    
    2.  Agregue el almacén de SQL Server de reflejo principal.
    
    3.  Habilite la base de datos de trasvase de registros de SQL Server.
    
    4.  Agregue el almacén de SQL Server secundario de trasvase de registros de SQL Server.
    
    5.  Agregue el reflejo de la tienda SQL Server para la base de datos secundaria.
    
    6.  Publique la topología.

</div>

<span> </span>

</div>

</div>

</div>

