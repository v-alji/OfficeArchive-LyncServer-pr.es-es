---
title: Configuración XMPP de ejemplo - Federación XMPP con Google Talk
description: 'Ejemplo de configuración XMPP: Federación XMPP con Google Talk.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428456"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a>Configuración XMPP de ejemplo en Lync Server 2013 - Federación XMPP con Google Talk

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2014-04-22_

Un ejemplo de configuración para implementar el proxy XMPP define una federación con Google Talk.

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a>Configuración XMPP de ejemplo - Federación XMPP con Google Talk

1.  En el servidor front-end, abra el Asistente para la implementación de Lync Server. Haga clic en **instalar** o **actualizar el sistema Lync Server** y, a continuación, haga clic en **configurar** o **quitar los componentes de Lync Server**. **Vuelva a** hacer clic en ejecutar.

2.  En **instalación de los componentes de Lync Server**, haga clic en **siguiente**. La pantalla resumen mostrará las acciones a medida que se ejecutan. Una vez completada la implementación, haga clic en **Ver registro** para ver los archivos de registro disponibles. Haga clic en **Finalizar** para completar la implementación.

3.  En el servidor perimetral, abra el Asistente para la implementación de Lync Server. Haga clic en **instalar** o **actualizar el sistema Lync Server** y, a continuación, haga clic en **configurar** o **quitar los componentes de Lync Server**. **Vuelva a** hacer clic en ejecutar.

4.  Agregue Google Talk como socio XMPP permitido. Actualmente, Google Talk solo admite conexiones TCP sin cifrar para la Federación de XMPP de servidor a servidor y solo admite el Dialback de servidor para la verificación de identidad. (Consulte <http://xmpp.org/extensions/xep-0220.html> ).
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  Para habilitar la Federación perimetral, escriba lo siguiente:
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  En **instalación de los componentes de Lync Server**, haga clic en **siguiente**. La pantalla resumen mostrará las acciones a medida que se ejecutan. Una vez completada la implementación, haga clic en **Ver registro** para ver los archivos de registro disponibles. Haga clic en **Finalizar** para completar la implementación.

7.  En el servidor perimetral, en el Asistente de implementación de Lync Server, junto al **paso 3: solicitar, instalar o asignar certificados**, haga clic en **Ejecutar de nuevo**.
    
    <div>
    

    > [!TIP]
    > Si está implementando el servidor perimetral por primera vez, verá ejecutar en lugar de volver a ejecutar.

    
    </div>

8.  En la página **Tareas de certificado disponibles**, haga clic en **Crear una nueva solicitud de certificado**.

9.  En la página **solicitud de certificado** , haga clic en certificado de **borde externo**.

10. En la página **solicitud inmediata o demorada** , active la casilla **preparar la solicitud ahora pero enviarla más tarde** .

11. En la página **archivo de solicitud de certificado** , escriba la ruta de acceso completa y el nombre del archivo en el que se va a guardar la solicitud (por ejemplo, c: \\ CERT \_ la \_ Edge. cer).

12. En la página **especificar plantilla de certificado alternativa** , para usar una plantilla distinta de la plantilla predeterminada de WebServer, seleccione la casilla **Usar plantilla de certificado alternativa para la entidad emisora de certificados seleccionada** .

13. En la página **nombre y configuración de seguridad** , haga lo siguiente:
    
    1.  En **nombre descriptivo**, escriba un nombre para mostrar para el certificado.
    
    2.  En **longitud bit**, especifique la longitud en bits (normalmente, el valor predeterminado de **2048**).
    
    3.  Compruebe que la casilla **marcar clave privada de certificado como exportable** está seleccionada

14. En la página información de la **organización** , escriba el nombre de la organización y la unidad organizativa (por ejemplo, una división o un departamento).

15. En la página **información geográfica** , especifique la información de ubicación

16. En la página **nombre de sujeto/nombres alternativos de asunto** , se muestra la información que el asistente rellenará automáticamente. Si se necesitan nombres alternativos de asunto adicionales, debe especificarlos en los dos pasos siguientes.

17. En la página **configuración del dominio SIP en la página de nombres alternativos de asunto (San)** , seleccione la casilla dominio para agregar un SIP. \<sipdomain\> entrada a la lista de nombres alternativos de asunto.

18. En la página **configurar otros nombres alternativos de asunto** , especifique los nombres alternativos adicionales que sean obligatorios.
    
    <div>
    

    > [!TIP]
    > Si el proxy XMPP está instalado, de forma predeterminada, el nombre de dominio (por ejemplo, contoso.com) se rellena en las entradas SAN. Si necesita más entradas, agréguelos en este paso.

    
    </div>

19. En la página **solicitar Resumen** , revise la información del certificado que se va a usar para generar la solicitud.

20. Cuando termine de ejecutarse los comandos, puede **ver el registro** o hacer clic en **siguiente** para continuar.

21. En la página de **archivo de solicitud de certificado** , puede ver el archivo de solicitud de firma de certificado generado (CSR) haciendo clic en **Ver** o salir del asistente de certificados haciendo clic en **Finalizar**.

22. Copie el archivo de solicitud y envíelo a la entidad emisora de certificados pública.

23. Después de recibir, importar y asignar el certificado público, debe detener y reiniciar los servicios del servidor perimetral. Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**. En el shell de administración de Lync Server, escriba:
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. Para configurar DNS para la Federación XMPP, agregue el siguiente registro SRV a DNS externo: \_ XMPP-Server. \_ TCP.\<domain name\> El registro SRV se resolverá en el FQDN perimetral de acceso del servidor perimetral, con un valor de puerto de 5269

25. Configure una nueva Directiva de acceso externo para habilitar todos los usuarios abriendo el shell de administración de Lync Server en un servidor front-end y escribiendo lo siguiente:
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

</div>

</div>

<span> </span>

</div>

</div>

</div>

