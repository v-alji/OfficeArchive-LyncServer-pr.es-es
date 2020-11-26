---
title: 'Lync Server 2013: Instalar la base de datos del servidor Standard Edition'
description: 'Lync Server 2013: instalar la base de datos del servidor Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Standard Edition server database
ms:assetid: 0bd3a804-aad6-48cb-981b-54725af032db
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398167(v=OCS.15)
ms:contentKeyID: 48183385
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a20d2c01de94ad88960555db78c57c6b79d92f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427155"
---
# <a name="install-standard-edition-server-database-for-lync-server-2013"></a>Instalar la base de datos del servidor Standard Edition en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-01_

Configurar un servidor Standard Edition como el único servidor de la infraestructura en el que los usuarios de la casa difiere de otras instalaciones de servidor, en la que hay una selección en el Asistente para la **implementación** específicamente para configurar el servidor inicial.

<div>

## <a name="to-install-a-standard-edition-server"></a>Para instalar un servidor Standard Edition

1.  Inicie sesión en el servidor en el que va a instalar el servidor Standard Edition como administrador local o como un equivalente de dominio.

2.  Si no ha preparado los servicios de dominio de Active Directory, primero realice esos procedimientos. Para obtener más información, vea [preparar los servicios de dominio de Active Directory para Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).

3.  En el Asistente para la implementación de Lync Server, haga clic en **preparar el primer servidor Standard Edition**.

4.  En la página **preparar un solo servidor Standard Edition** , haga clic en **siguiente**.

5.  En la página **comandos en ejecución** , SQL Server 2012 Express está instalado como almacén de administración central. Se crean las reglas de Firewall necesarias. Cuando haya finalizado la instalación de la base de datos y el software necesario, haga clic en **Finalizar**.
    
    <div>
    

    > [!NOTE]  
    > La instalación inicial puede llevar algún tiempo sin actualizaciones visibles en la pantalla Resumen de salida del comando. Esto se debe a la instalación de SQL Server Express. Si necesita supervisar la instalación de la base de datos, use el administrador de tareas para supervisar la configuración.

    
    </div>

6.  En la página del Asistente para la implementación de Lync Server, haga clic en **instalar generador de topologías** si todavía no ha instalado las herramientas administrativas. Para obtener información detallada, consulte [instalar herramientas administrativas 2013 de Lync Server](lync-server-2013-install-lync-server-administrative-tools.md).

7.  Confirme que hay marcas de verificación verdes junto a "preparar Active Directory", "preparar el primer servidor Standard Edition" e "instalar el generador de topología".

</div>

</div>

<span> </span>

</div>

</div>

</div>

