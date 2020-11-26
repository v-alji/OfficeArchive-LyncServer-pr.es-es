---
title: Comprobación de direcciones de cívica con la guía de dirección principal
description: Comprobación de direcciones de cívica con la guía de dirección principal.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing civic addresses against the master street address guide
ms:assetid: dc680de9-2a0f-4fd3-a99e-9bab0bc30ae5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690132(v=OCS.15)
ms:contentKeyID: 63969657
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16e0d721b70e3db175b2d23ddee6f59d13a13c4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439831"
---
# <a name="testing-civic-addresses-against-the-master-street-address-guide-in-lync-server-2013"></a>Comprobación de direcciones de cívica con la guía de dirección principal de Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2014-06-05_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Programación de verificación</p></td>
<td><p>Cada día</p></td>
</tr>
<tr class="even">
<td><p>Herramienta de prueba</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>Permisos necesarios</p></td>
<td><p>Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</p>
<p>Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsRegistration. Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisCivicAddress &quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Descripción

El cmdlet Test-CsLisCivicAddress se usa para comprobar las ubicaciones que se han agregado a la base de datos del servicio de información de ubicación (LIS). El cmdlet compara las ubicaciones con las ubicaciones que se encuentran en la guía de dirección principal (MSAG) que pertenece a su proveedor de enrutamiento de red E9-1-1. Si no tiene un proveedor de enrutamiento de red o si no se puede comunicar con el proveedor, las pruebas no se realizarán correctamente.

Si agrega el parámetro de modificador opcional UpdateValidationStatus a su comando, la propiedad de base de datos de MSAGValid correspondiente se establecerá en true para cada dirección que pase la prueba.

</div>

<div>

## <a name="running-the-test"></a>Ejecutar la prueba

El cmdlet Test-CsLisCivicAddress se puede usar para probar direcciones individuales o para probar varias direcciones. Por ejemplo, este comando comprueba una única dirección que se encuentra en Redmond, WA:

    Test-CsLisCivicAddress -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName Main -StreetSuffix St -PostDirectional "" -City Redmond -State WA -PostalCode 98052 -Country US -UpdateValidationStatus

Por comparación, este comando prueba todas las direcciones que se encuentran en la base de datos de LIS:

    Get-CsLisCivicAddress | Test-CsLisCivicAddress -UpdateValidationStatus

Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15)) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Determinar el éxito o el fracaso

Test-CsLisCivicAddress enviará un informe de éxito o error a las direcciones suministradas. Se producirá un error en una prueba de dirección si no se puede encontrar la dirección o si no se puede contactar con el proveedor de servicios.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Razones por las que se ha producido un error en la prueba

Estas son algunas de las razones comunes por las que Test-CsLisCivicAddress puede dar error:

  - Es posible que el proveedor de servicios LIS no esté disponible. Puede recuperar la dirección URL de su proveedor de servicios LIS ejecutando el cmdlet Get-CsLisConfiguration:
    
        Get-CsLisConfiguration 
    
    Después, puede hacer ping a esa dirección URL para comprobar que el proveedor de servicios está disponible.

</div>

</div>

<span> </span>

</div>

</div>

</div>

