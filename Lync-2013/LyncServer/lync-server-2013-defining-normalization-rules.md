---
title: 'Lync Server 2013: Definir las reglas de normalización'
description: 'Lync Server 2013: definición de reglas de normalización.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining normalization rules
ms:assetid: ed31d56c-00b5-4f72-bd9f-beb4100d441f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399071(v=OCS.15)
ms:contentKeyID: 48185741
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a123e17b1d3256781ff34e4cade2b344ba8fe14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430997"
---
# <a name="defining-normalization-rules-in-lync-server-2013"></a>Definir las reglas de normalización en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2014-04-22_

Reglas de normalización de Lync Server 2013 usar expresiones regulares de .NET Framework para traducir números de teléfono marcados al formato E. 164; en otras palabras, las reglas de normalización toman el número de teléfono marcado por un usuario y convierten ese número al formato usado internamente por Lync Server. Cada plan de marcado debe tener asignadas una o más reglas de normalización.

Para obtener más información sobre las reglas de normalización, consulte [planes de marcado y reglas de normalización en Lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) en la documentación de planeación.

Para obtener más información sobre cómo escribir expresiones regulares, vea "expresiones regulares de .NET Framework" en [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927) .

Puede usar cualquiera de los siguientes métodos para definir o editar una regla de normalización:

  - Use la herramienta **crear una regla de normalización** para especificar valores para los dígitos iniciales, la longitud, los dígitos que se van a quitar y los dígitos que se van a agregar y, a continuación, deje que el panel de control de Lync Server genere el patrón correspondiente y la regla de traducción correspondiente.

  - Escriba de forma manual expresiones regulares para definir el patrón de coincidencia y la regla de traducción.

<div>

## <a name="in-this-section"></a>En esta sección

  - [Crear o modificar una regla de normalización mediante la creación de una regla de normalización en Lync Server 2013](lync-server-2013-create-or-modify-a-normalization-rule-by-using-build-a-normalization-rule.md)

  - [Crear o modificar una regla de normalización manualmente en Lync Server 2013](lync-server-2013-create-or-modify-a-normalization-rule-manually.md)

</div>

<div>

## <a name="see-also"></a>Vea también


[Crear un plan de marcado en Lync Server 2013](lync-server-2013-create-a-dial-plan.md)  
[Modificar un plan de marcado en Lync Server 2013](lync-server-2013-modify-a-dial-plan.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

