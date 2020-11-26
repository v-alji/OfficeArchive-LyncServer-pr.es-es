---
title: 'Lync Server 2013: probar el acceso anónimo a aplicaciones Web'
description: 'Lync Server 2013: Pruebe el acceso anónimo a la aplicación Web.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test anonymous Web App access
ms:assetid: 92f691cd-e05e-4bab-beb5-251d4b837a19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767949(v=OCS.15)
ms:contentKeyID: 63969630
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c33840912fefcaeef069e14773cfefd0834a8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441273"
---
# <a name="test-anonymous-web-app-access-in-lync-server-2013"></a>Probar el acceso anónimo a aplicaciones web en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2014-06-07_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Programación de verificación</p></td>
<td><p>Cada mes</p></td>
</tr>
<tr class="even">
<td><p>Herramienta de prueba</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>Permisos necesarios</p></td>
<td><p>Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</p>
<p>Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsWebAppAnonymous. Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebAppAnonymous&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Descripción

El cmdlet Test-CsWebAppAnonymous comprueba que un usuario anónimo puede unirse a conferencias de Lync Server mediante Lync Web App. Al ejecutar el cmdlet, Test-CsWebAppAnonymous se pone en contacto con el servicio de vales web para obtener un vale web para el usuario anónimo. Si el cmdlet consigue obtener este vale, Test-CsWebAppAnonymous se pondrá en contacto con Lync Server e intentará establecer conferencias independientes para la mensajería instantánea, el uso compartido de aplicaciones y la colaboración de datos.

Tenga en cuenta que Test-CsWebAppAnonymous solo comprueba las API y las conexiones usadas para crear estas conferencias. En realidad, el cmdlet no crea ni dirige ninguna Conferencia.

</div>

<div>

## <a name="running-the-test"></a>Ejecutar la prueba

El cmdlet Test-CsWebAppAnonymous se puede ejecutar con un par de cuentas de prueba preconfiguradas o con las cuentas de dos usuarios que están habilitados para Lync Server. Para ejecutar esta comprobación mediante cuentas de prueba, solo tiene que especificar el nombre de dominio completo del grupo de servidores de Lync que se está probando. Por ejemplo:

    Test-CsWebAppAnonymous -TargetFqdn atl-cs-001.litwareinc.com

Para ejecutar esta comprobación con las cuentas de usuario reales, debe crear dos objetos de credenciales del shell de administración de Lync Server (objetos que contengan el nombre y la contraseña de la cuenta) de cada cuenta. Después, debe incluir esos objetos de credenciales y las direcciones SIP de las dos cuentas cuando llame a test-CsWebAppAnonymous:

    $cred1 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1

Para obtener más información, consulte el tema de ayuda para el cmdlet Test-CsWebAppAnonymous. Tenga en cuenta que Test-CsWebAppAnonymous está en desuso para su uso en Lync Server 2013.

</div>

<div>

## <a name="determining-success-or-failure"></a>Determinar el éxito o el fracaso

Si Test-CsWebAppAnonymous puede unir al usuario anónimo a su conferencia, el cmdlet devolverá el resultado de la prueba correcto:

FQDN de destino:

Resultado: éxito

Latencia: 00:00:00

Mensaje de error:

Diagnóstico

Si el usuario anónimo no puede unirse a las conferencias necesarias, el resultado de la prueba se marcará como erróneo. Por lo general, Test-CsWebAppAnonymous también devolverá un mensaje de error y un diagnóstico detallados:

FQDN de destino: atl-cs-001.litwareinc.com

Resultado: error

Latencia: 00:00:05.9746266

Mensaje de error: no se recibió respuesta para el servicio Web-Ticket

Diagnóstico: la solicitud HTTP no está autorizada con el cliente

esquema de autenticación ' NTLM '. La autenticación

el encabezado recibido del servidor era ' Negotiate, NTLM '.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Razones por las que se ha producido un error en la prueba

Los errores de Test-CsWebAppAnonymous suelen girar en relación con errores de autenticación de usuario: debe ejecutar la prueba con una cuenta de usuario válida, aunque el cmdlet está comprobando la capacidad de un usuario anónimo para conectarse a Lync Server. Si Test-CsWebAppAnonymous da error, debe comprobar que el usuario especificado tiene una cuenta de usuario válida de Lync Server. Puede recuperar la información de la cuenta de Lync Server mediante un comando similar al siguiente:

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

Si la propiedad Enabled no es igual a true o si se produce un error en el comando, significa que el usuario no tiene una cuenta válida de Lync Server.

También debe comprobar que la contraseña que proporcionó al ejecutar el cmdlet es una contraseña válida.

Los problemas de configuración con Office Web Apps Server también pueden hacer que Test-CsWebAppAnonymous no se realice correctamente; Esto suele ser el caso si recibe el siguiente diagnóstico:

La solicitud HTTP no está autorizada con el esquema de autenticación de cliente ' NTLM '. El encabezado de autenticación recibido desde el servidor era ' Negotiate, NTLM '.

Para obtener más información sobre cómo diagnosticar y resolver problemas de Office Web Apps Server, consulte el blog de las aplicaciones de correo de Office [Web Apps server 2013: los equipos se muestran siempre como en mal estado](http://www.wictorwilen.se/office-web-apps-server-2013---machines-are-always-reported-as-unhealthy).

</div>

</div>

<span> </span>

</div>

</div>

</div>

