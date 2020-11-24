---
title: Configurar servidores de aplicaciones de confianza
description: Configure los servidores de aplicaciones de confianza.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure trusted application servers
ms:assetid: 20c3815f-3048-4940-8c0f-cdfcd0801d5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204735(v=OCS.15)
ms:contentKeyID: 48183592
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39f439ea3e5996e0a3464540069024b70c415e3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398861"
---
# <a name="configure-trusted-application-servers"></a>Configurar servidores de aplicaciones de confianza

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-11_

En un entorno mixto, si crea un nuevo servidor de aplicaciones de confianza, debe configurar el grupo de próximos saltos para que sea un grupo de servidores de Lync 2013. En un entorno mixto, tanto el grupo heredado de Lync Server 2010 y el grupo de servidores Lync Server 2013 aparecen en la lista desplegable. No se puede seleccionar el grupo heredado.

**Seleccione Lync Server 2013 como próximo salto al crear un servidor de aplicaciones de confianza**

1.  Abra el generador de topologías.

2.  En el panel izquierdo, haga clic con el botón secundario en **servidores de aplicaciones de confianza** y haga clic en **nuevo grupo de aplicaciones de confianza**.

3.  Escriba el **FQDN del grupo** del grupo de aplicaciones de confianza y seleccione si será un servidor único o de varios servidores.

4.  Haga clic en **Siguiente**.

5.  En la página **seleccionar el próximo salto** , en la lista, seleccione el grupo de servidores front-end de Lync Server 2013.

6.  Haga clic en **Finalizar**.

7.  Seleccione el nodo superior de **Lync Server** y, en el menú **acción** , seleccione **publicar**.
    
    Compruebe que el **grupo de aplicaciones de confianza** se haya creado correctamente y que esté asociado al grupo de servidores front-end correcto.

</div>

<span> </span>

</div>

</div>

</div>

