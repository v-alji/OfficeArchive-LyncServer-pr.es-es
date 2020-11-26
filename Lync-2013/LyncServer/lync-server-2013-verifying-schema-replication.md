---
title: 'Lync Server 2013: Comprobar la replicación de esquemas'
description: 'Lync Server 2013: comprobación de la replicación del esquema.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verifying schema replication
ms:assetid: ad01a7cf-aa79-4648-ba5a-a7a09172db36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412822(v=OCS.15)
ms:contentKeyID: 48185124
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 019cd06db05a9ba683767f550a712ef188b47508
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438900"
---
# <a name="verifying-active-directory-schema-replication-in-lync-server-2013"></a>Comprobar la replicación de esquemas de Active Directory en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-29_

Antes de ejecutar la preparación del bosque, compruebe manualmente que la partición de esquema se ha replicado.

<div>

## <a name="to-manually-verify-schema-replication"></a>Para comprobar manualmente la replicación del esquema

1.  Inicie sesión en un controlador de dominio como miembro del grupo administradores de la empresa.

2.  Abra ADSI Edit haciendo clic en **Inicio**, en **herramientas administrativas** y, a continuación, en **ADSI Edit**.
    
    <div>
    

    > [!TIP]  
    > Como alternativa, puede ejecutar <STRONG>ADSIEdit. msc</STRONG> desde la línea de comandos.

    
    </div>

3.  En el árbol de Microsoft Management Console (MMC), si aún no está seleccionado, haga clic en **ADSI Edit**.

4.  En el menú **Acción**, haga clic en **Conectar con**.

5.  En el cuadro de diálogo **Configuración de conexión**, en **Seleccione un contexto de nomenclatura conocido**, seleccione **Esquema** y, luego, haga clic en **Aceptar**.

6.  En el contenedor de esquema, busque CN=ms-RTC-SIP-SchemaVersion. Si este objeto existe y el valor del atributo **rangeUpper** es 1150 y el valor del atributo **rangeLower** es 3, el esquema se ha actualizado y replicado correctamente. Si este objeto no existe o los valores de los atributos **rangeUpper** y **rangeLower** no se especifican, el esquema no se modificó o no se ha replicado.

</div>

<div>

## <a name="see-also"></a>Vea también


[Ejecutar la preparación del esquema de Active Directory en Lync Server 2013](lync-server-2013-running-schema-preparation.md)  


[Preparación del esquema de Active Directory en Lync Server 2013](lync-server-2013-preparing-the-active-directory-schema.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

