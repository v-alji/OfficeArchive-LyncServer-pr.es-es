---
title: 'Lync Server 2013: Conmutación por error de una base de datos reflejada'
description: 'Lync Server 2013: error en una base de datos reflejada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over a mirrored database
ms:assetid: 70185476-e3d4-440a-9316-fa24b226343e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204991(v=OCS.15)
ms:contentKeyID: 48184450
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc7c401157c79762f674721ca717296c0fe502db
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428296"
---
# <a name="failing-over-a-mirrored-database-in-lync-server-2013"></a>Conmutación por error de una base de datos reflejada en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2014-03-14_

Si ha configurado la base de datos back-end para usar el reflejo sincronizado con un testigo, la conmutación por error es automática. Si ha configurado el reflejo sincronizado sin un testigo, puede usar los siguientes procedimientos para realizar la conmutación por error y la recuperación de la base de datos. También puede usar estos procedimientos para realizar un failover manual de las bases de datos y hacer un failback, incluso si ha configurado un testigo.

<div>

## <a name="to-fail-over-your-back-end-database"></a>Para conmutar por error a la base de datos back-end

1.  Antes de realizar la conmutación por error, determine qué base de datos back-end es el principal y cuál es el reflejo; para ello, escriba el siguiente cmdlet:
    
        Get-CsDatabaseMirrorState -PoolFqdn <poolFQDN> -DatabaseType User

2.  Si el almacén de administración central está hospedado en este grupo, escriba el siguiente cmdlet para determinar cuál es el principal y cuál es el reflejo del almacén central de administración:
    
        Get-CsDatabaseMirrorState -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt

3.  Realice la conmutación por error de la base de datos de usuario:
    
      - Si el principal ha fallado y se está produciendo un error en el reflejo, escriba:
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType User -NewPrincipal mirror -Verbose
    
      - Si el reflejo ha fallado y se está conmutando por error al principal, escriba:
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType User -NewPrincipal primary -Verbose

4.  Si el grupo hospeda el servidor de administración central, realice la conmutación por error del almacén de administración central.
    
      - Si el principal ha fallado y se está produciendo un error en el reflejo, escriba:
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt -NewPrincipal mirror -Verbose
    
      - Si el reflejo ha fallado y se está conmutando por error al principal, escriba:
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt -NewPrincipal primary -Verbose

</div>

</div>

<span> </span>

</div>

</div>

</div>

