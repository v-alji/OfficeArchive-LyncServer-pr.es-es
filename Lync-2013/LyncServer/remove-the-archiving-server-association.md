---
title: Quitar la asociación del servidor de archivado
description: Quite la Asociación del servidor de archivado.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the Archiving server association
ms:assetid: dabac157-71ee-4afe-b0b6-4a083d165ffb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721903(v=OCS.15)
ms:contentKeyID: 49733837
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f6c34e49b0217a8318a83752b3878a7625e5d58
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400085"
---
# <a name="remove-the-archiving-server-association"></a>Quitar la asociación del servidor de archivado

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-04_

Para quitar un servidor de archivado, debe cambiar o borrar la dependencia en el grupo frontal, el servidor front-end, el equipo de la sucursal y el servidor de la sucursal que siguen funcionando. Edite las propiedades del grupo de servidores front-end, el servidor front-end, el equipo de sucursales con la supervivencia y el servidor de sucursal con la supervivencia para quitar la dependencia. Después de borrar la dependencia y de eliminar el servidor en el generador de topología, se le notificará que el objeto de almacén de base de datos asociado en el generador de topología también se eliminará.

<div>

## <a name="to-remove-the-archiving-server-association"></a>Para quitar la Asociación del servidor de archivado

1.  Abra el servidor front-end 2013 de Lync Server, abra Topology Builder.

2.  Vaya al nodo de 2010 de Lync Server.

3.  En el generador de topología, expanda las **agrupaciones front end de Enterprise Edition**, **los servidores de aplicaciones para el usuario Standard Edition** o los **sitios de sucursales** en función de dónde se defina el servidor de archivado.

4.  Si tiene asociado un servidor de sucursal, expanda **sitios de sucursales**, expanda el nombre del sitio de la sucursal y, a continuación, expanda **aplicaciones de sucursales** reutilizables.
    
    <div>
    

    > [!NOTE]  
    > Los <STRONG>dispositivos</STRONG> de la interfaz de usuario que son supervivientes se aplican a los servidores de sucursal con supervivencia y con la aplicación de rama superviviente.

    
    </div>

5.  Haga clic con el botón secundario en el grupo, servidor o dispositivo asociado al servidor de archivado y, a continuación, haga clic en **Editar propiedades**.

6.  En **Editar propiedades**, en **General**, en **asociaciones**, desactive la casilla **asociar servidor de archivado** y, a continuación, haga clic en **Aceptar**.

7.  Repita el paso anterior para cualquier otro grupo, servidor o dispositivo asociado al servidor de archivado que desee quitar.

8.  Haga clic con el botón secundario en el servidor de archivado y luego haga clic en **eliminar**.

9.  En **eliminar almacenes dependientes**, haga clic en **Aceptar**.

10. Publique la topología, compruebe el estado de replicación y, a continuación, ejecute el Asistente para la implementación de Lync Server según sea necesario.

</div>

</div>

<span> </span>

</div>

</div>

</div>

