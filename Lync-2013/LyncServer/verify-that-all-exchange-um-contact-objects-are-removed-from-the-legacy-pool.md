---
title: Comprobar que todos los objetos de contacto de mensajería unificada de Exchange se han quitado del grupo heredado
description: Compruebe que todos los objetos de contacto de mensajería unificada de Exchange se han quitado del grupo heredado.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify that all Exchange UM Contact objects are removed from the legacy pool
ms:assetid: 5a813169-0ed7-4f84-a242-ed2cd4ea5c43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688068(v=OCS.15)
ms:contentKeyID: 49733664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af5dea6cf746c55d8fecf074e132f721c380de1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440139"
---
# <a name="verify-that-all-exchange-um-contact-objects-are-removed-from-the-legacy-pool"></a>Comprobar que todos los objetos de contacto de mensajería unificada de Exchange se han quitado del grupo heredado

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-09-26_

Use la herramienta **OCSUmUtil** o el cmdlet **Get-CsExumContact** para comprobar que los objetos de contacto de MU de Exchange se han quitado del grupo heredado de Office Communications Server 2007 R2. **OCSUmUtil** se encuentra en la siguiente carpeta:

% Archivos de programa% \\ archivos comunes \\ soporte técnico de Lync Server 2013 \\ \\OcsUMUtil.exe

**OCSUmUtil** debe ejecutarse desde una cuenta de usuario que tenga:

  - Pertenencia al grupo RTCUniversalServerAdmins y RTCUniversalUserAdmins (que incluye derechos para leer la configuración de mensajería unificada de Exchange Server)

  - Derechos de dominio para crear objetos de contacto en el contenedor de unidades organizativas (OU) especificadas

Para obtener detalles sobre el uso del cmdlet **Get-CsExumContact** , vea [Get-CsExumContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) en la documentación del shell de administración de Lync Server.

</div>

<span> </span>

</div>

</div>

</div>

