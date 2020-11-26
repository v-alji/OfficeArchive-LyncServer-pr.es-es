---
title: Pertenencias a grupos y requisitos de derechos de usuario para el analizador de procedimientos recomendados
description: Pertenencias a grupos y requisitos de derechos de usuario para el analizador de procedimientos recomendados.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group memberships and user rights requirements for Best Practices Analyzer
ms:assetid: f812e343-8f75-454e-b7a8-1b404e32071a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591354(v=OCS.15)
ms:contentKeyID: 48185869
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 64a7d785a77701c6796488178a7cce10caf54f42
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427827"
---
# <a name="group-memberships-and-user-rights-requirements-for-best-practices-analyzer-in-lync-server-2013"></a>Pertenencias a grupos y requisitos de derechos de usuario para el analizador de procedimientos recomendados de Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-21_

Para ejecutar correctamente el analizador de procedimientos recomendados, la cuenta de usuario que usa para iniciar sesión debe ser miembro del grupo administradores en el equipo local. Además, para analizar su entorno, la cuenta de usuario debe ser miembro de los siguientes grupos:

  - **Administradores de dominio**   Para enumerar la información de los servicios de dominio de Active Directory y para llamar a los proveedores de instrumental de administración de Windows (WMI) en controladores de dominio y servidores de catálogo global.

  - **Administradores**   Se requiere en cada equipo interno 2013 de Lync Server y en cada servidor perimetral para llamar a los proveedores de instrumental de administración de Windows (WMI) y para obtener acceso al registro.

  - **RTCUniversalReadOnlyAdmins**   Solo lectura o delegada derechos administrativos de Lync Server 2013.

  - **Administrador con permiso de vista de Exchange**   Administrador con permiso de vista de Exchange completo o delegado en la organización de Microsoft Exchange.

Si su cuenta de usuario no tiene suficientes derechos de usuario, tiene dos opciones:

  - En un símbolo del sistema, use el comando **runas** para ejecutar la herramienta en una cuenta que tenga derechos de usuario suficientes. La sintaxis es la siguiente:
    
        runas /netonly /user:<domain>\<userName> rtcbpa.exe

  - En la página **conectar a Active Directory** , establezca las credenciales de las cuentas que planea usar para ejecutar Best Practices Analyzer. Haga clic en **Mostrar opciones de inicio de sesión avanzadas**. Puede especificar tres cuentas: una para conectarse a servicios de dominio de Active Directory, una para conectar con servidores perimetrales de Lync Server 2013 y otra para conectarse a los servidores de Exchange. Si no especifica ninguna de estas cuentas, se usa la cuenta de usuario que usó para iniciar sesión y ejecutar el analizador de procedimientos recomendados.

</div>

<span> </span>

</div>

</div>

</div>

