---
title: 'Lync Server 2013: configuración de un nodo de monitor para ejecutar transacciones sintéticas'
description: 'Lync Server 2013: configuración de un nodo de monitor para ejecutar transacciones sintéticas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to run synthetic transactions
ms:assetid: cedda508-8881-4079-88d5-49798f342ddf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205314(v=OCS.15)
ms:contentKeyID: 48185578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd5fdb3d1a1499a6ef79e962a41d9eb3ee174c33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433475"
---
# <a name="configuring-a-watcher-node-to-run-synthetic-transactions-in-lync-server-2013"></a>Configuración de un nodo de monitor para ejecutar transacciones sintéticas en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2014-02-07_

Una vez instalados los archivos del agente de System Center, debe configurar el nodo de monitor en sí. Los pasos que debe seguir para configurar un nodo de monitor variarán en función de si el equipo nodo de observador está dentro de la red perimetral o fuera de la red perimetral.

Al configurar un nodo de monitor, también debe elegir el tipo de método de autenticación que se va a usar en ese nodo. Lync Server 2013 le permite elegir uno de los dos métodos de autenticación: servidor de confianza o autenticación de credenciales. Las diferencias entre estos dos métodos se describen en la tabla siguiente:


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Configuración</th>
<th>Descripción</th>
<th>Ubicaciones admitidas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Servidor de confianza</p></td>
<td><p>Usa un certificado para representar a un servidor interno y evitar problemas de autenticación.</p>
<p>Esto es útil para los administradores que prefieren administrar un único certificado en lugar de muchas contraseñas de usuario en cada nodo de monitor.</p></td>
<td><p>Dentro de la empresa.</p>
<p>Tenga en cuenta que, con este método, el nodo de monitor debe estar en el mismo dominio que los grupos que se están supervisando. Si el nodo de monitor y los grupos supervisados se encuentran en dominios diferentes, use en su lugar la autenticación de credenciales.</p></td>
</tr>
<tr class="even">
<td><p>Autenticación de credenciales</p></td>
<td><p>Almacena los nombres de usuario y las contraseñas con seguridad en Windows Credential Manager en cada nodo de monitor.</p>
<p>Este modo requiere más administración de contraseñas, pero es la única opción para los nodos de monitor que se encuentran fuera de la empresa. Estos nodos de monitor no se pueden tratar como un extremo de confianza para la autenticación.</p></td>
<td><p>Fuera de la empresa.</p>
<p>Dentro de la empresa.</p></td>
</tr>
</tbody>
</table>


También debe verificar que el firewall tiene reglas de entrada para MonitoringHost.exe y PowerShell.exe. Si el Firewall bloquea estos procesos, las transacciones sintéticas fallarán con un error de 504 (tiempo de espera del servidor).

</div>

<span> </span>

</div>

</div>

</div>

