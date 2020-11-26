---
title: Quitar BackCompatSite
description: Quitar BackCompatSite.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove BackCompatSite
ms:assetid: 039650e3-541b-45c2-a682-c4fa08423118
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204637(v=OCS.15)
ms:contentKeyID: 48183265
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 809324320ec1869ac0c9d324b8fc270a3cf8f174
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440304"
---
# <a name="remove-backcompatsite"></a>Quitar BackCompatSite

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-09-28_

Una vez desactivados todos los grupos y todos los servidores perimetrales se han desinstalado, ejecute el Asistente para combinar el generador de topología para quitar el **BackCompatSite**.

<div>

## <a name="to-remove-backcompat-site-from-topology-builder"></a>Para quitar el sitio de BackCompat del generador de topología

1.  Abra una implementación existente desde el generador de topología.

2.  En el menú **acción** , haga clic en **fusionar topología R2 de 2007**.

3.  Haga clic en **Siguiente** para continuar.

4.  En la página **especificar borde heredado** , asegúrese de que la lista de servidores perimetrales esté vacía. Si la lista no está vacía, use el botón **quitar** para quitar todos los servidores perimetrales heredados y, a continuación, haga clic en **siguiente**.
    
    ![Asistente para combinar topología, especificar página de configuración de Edge](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Asistente para combinar topología, especificar página de configuración de Edge")  

5.  En la página **especificar la configuración interna del puerto SIP** , haga clic en **siguiente**.

6.  En la página **Resumen** , haga clic en **siguiente** para empezar a combinar las topologías para quitar el sitio heredado.

7.  En la columna **Estado** , compruebe que el valor es **correcto** y, a continuación, haga clic en **Finalizar** para cerrar el asistente.

8.  En el panel izquierdo del generador de topologías, expanda el BackCompatSite y asegúrese de que no hay servidores en la lista.

9.  Haga clic con el botón secundario en el **BackCompatSite** y luego haga clic en **eliminar**.

10. En el **generador de topologías**, seleccione el nodo de nivel superior de **Lync Server**.

11. En el menú **acción** , seleccione **publicar topología** y, a continuación, haga clic en **siguiente**.

12. Cuando finalice el Asistente para la **publicación** , haga clic en **Finalizar** para cerrar el asistente.

</div>

</div>

<span> </span>

</div>

</div>

</div>

