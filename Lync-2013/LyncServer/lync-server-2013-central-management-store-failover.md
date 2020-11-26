---
title: 'Lync Server 2013: Conmutación por error del almacén de administración central'
description: La conmutación por error del almacén central de administración de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Central Management store failover
ms:assetid: f464d715-68a4-462c-9584-00f41ab10db0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205376(v=OCS.15)
ms:contentKeyID: 48185809
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2960a55d6bdc49e00bf22997bc53946d4770fde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435470"
---
# <a name="central-management-store-failover-in-lync-server-2013"></a>Conmutación por error del almacén de administración central en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-18_

El almacén central de administración contiene datos de configuración sobre servidores y servicios de la implementación de Lync 2013. Proporciona un almacenamiento schematized sólido de los datos necesarios para definir, configurar, mantener, administrar, describir y usar una implementación de Lync 2013. También comprueba los datos para asegurarse de que la configuración es coherente.

Cada implementación de Lync incluye un almacén de administración central, que se hospeda en el servidor back-end de un grupo de servidores front-end.

Al establecer un emparejamiento de grupo que incluye el grupo que hospeda el almacén central de administración, se configura una base de datos de almacenamiento central de administración de copia de seguridad en el grupo de copias de seguridad y los servicios del almacén central de administración se instalan en ambos grupos. En cualquier momento, una de las dos bases de datos del almacén de administración central es la principal activa y la otra es una en espera. El servicio de copia de seguridad Replica el contenido desde el maestro activo al modo de espera.

Durante la conmutación por error de un grupo de servidores que implica a los grupos que hospedan el almacén de administración central, el administrador debe realizar la conmutación por error del almacén central de administración antes de realizar la conmutación por error.

Después de que se repara el desastre, no es necesario llevar a cabo la conmutación por recuperación del almacén de administración central. Después de la reparación, el almacén de administración central del grupo de copia de seguridad original puede permanecer como maestro activo.

Los objetivos de ingeniería para la conmutación por error del almacén de administración central son 5 minutos para el de tiempo de recuperación (RTO) y 5 minutos para el de punto de recuperación (RPO).

</div>

<span> </span>

</div>

</div>

</div>

