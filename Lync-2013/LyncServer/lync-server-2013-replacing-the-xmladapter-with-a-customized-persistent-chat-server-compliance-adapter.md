---
title: 'Lync Server 2013: reemplazar XmlAdapter por un adaptador de cumplimiento de servidor de chat persistente personalizado'
description: 'Lync Server 2013: reemplazar XmlAdapter por un adaptador de cumplimiento de servidor de chat persistente personalizado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Replacing the XmlAdapter with a customized Persistent Chat Server Compliance adapter
ms:assetid: 2cb70db2-663f-40a6-abcf-89ea7d4a8b65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ680106(v=OCS.15)
ms:contentKeyID: 49558152
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a90b4df7df42ffdc6c55e9b551b0eb53d07ab1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398976"
---
# <a name="replacing-the-xmladapter-with-a-customized-persistent-chat-server-compliance-adapter-in-lync-server-2013"></a>Reemplazar XmlAdapter por un adaptador de cumplimiento de servidor de chat persistente personalizado en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-11-01_

Puede escribir un adaptador personalizado en lugar de usar el XmlAdapter que se instala con el servidor de chat persistente. Para lograr esto, es necesario brindar un ensamblado de .NET Framework que contenga una clase pública que implemente la interfaz de **IComplianceAdapter**. Debe colocar este ensamblado en la carpeta de instalación del servidor de chat persistente de cada servidor del grupo de servidores de chat persistente. Cualquiera de los servidores de cumplimiento puede brindar datos de cumplimiento al adaptador, pero los servidores de cumplimiento no brindarán datos de cumplimiento duplicados a varias instancias del adaptador.

<div>

## <a name="implementing-the-icomplianceadapter-interface"></a>Implementación de la interfaz de IComplianceAdapter

La interfaz se define en el Compliance.dll ensamblado en el espacio de nombres `Microsoft.Rtc.Internal.Chat.Server.Compliance` . La interfaz define dos métodos que el adaptador personalizado necesita implementar.

    void SetConfig(AdapterConfig config)

El servidor de cumplimiento de chat persistente llamará a este método cuando se cargue el adaptador por primera vez. El `AdapterConfig` contiene la configuración de cumplimiento de la conversación persistente que es relevante para el adaptador de cumplimiento.

    void Translate(ConversationCollection conversations)

El servidor de cumplimiento de chat persistente llama a este método a intervalos periódicos, siempre y cuando haya nuevos datos para traducir. Este intervalo de tiempo es igual al `RunInterval` establecido en la configuración de cumplimiento de la conversación persistente.

El `ConversationCollection` contiene la información de la conversación que se recopiló desde la última vez que se llamó a este método.

</div>

</div>

<span> </span>

</div>

</div>

</div>

