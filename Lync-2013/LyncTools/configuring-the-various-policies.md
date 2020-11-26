---
title: Configurar las diversas directivas
description: Configurar las diversas directivas.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configuring the Various Policies
ms:assetid: e3b3cbda-7c17-470b-acb0-82fdcc473184
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945610(v=OCS.15)
ms:contentKeyID: 51541436
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 746d299ac605c7dfe89a957246d47309dfbc0a5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440069"
---
# <a name="configuring-the-various-policies"></a>Configurar las diversas directivas

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-02-24_

<div>

Estas son las diversas directivas que puede configurar en su topología de Lync Server 2013, antes de ejecutar la herramienta Lync Server 2013 stress and performance.

<div>

## <a name="configuring-the-archiving-policy"></a>Configuración de la Directiva de archivado

Vea la ArchivingPolicy.ps1 de script de ejemplo. Debe usar este script solo si un servidor de archivado está implementado en su topología. Para obtener más información, consulte la documentación 2013 de Lync Server y la ayuda de cmdlet para [archivar y supervisar cmdlets en Lync server 2013](https://technet.microsoft.com/library/gg415629\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-conferencing-policy"></a>Configuración de la Directiva de conferencia

Vea la MeetingPolicy.ps1 de script de ejemplo. Para obtener más información, consulte la documentación 2013 de Lync Server y la ayuda del cmdlet para [cmdlets de conferencias web en Lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-contacts-policy"></a>Configuración de la Directiva de contactos

Vea el ContactsPolicy.ps1 de ejemplo. Para obtener más información, consulte la documentación 2013 de Lync Server y la ayuda del cmdlet de [mensajería instantánea y cmdlets de presencia en Lync Server 2013](https://technet.microsoft.com/library/gg398611\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-federation-policy"></a>Configuración de la Directiva de Federación

Vea el FederationPolicy.ps1 de ejemplo. Para obtener más información, consulte la documentación 2013 de Lync Server y la ayuda del cmdlet para [cmdlets de servidor perimetral en Lync server 2013](https://technet.microsoft.com/library/gg415635\(v=ocs.15\)) y [cmdlets de Federación y de acceso externo en Lync Server 2013](https://technet.microsoft.com/library/gg415651\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-call-admission-control-policy"></a>Configuración de la Directiva de control de admisión de llamadas

Vea el BandwidthPolicy.ps1 de ejemplo. Para obtener más información, vea información general sobre la documentación de Lync Server 2013 [sobre el control de admisión de llamadas en Lync server 2013](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) y la ayuda del cmdlet para [cmdlets de control de admisión de llamadas en Lync Server 2013](https://technet.microsoft.com/library/gg415676\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-voice-routing-rules"></a>Configuración de las reglas de enrutamiento de voz

Vea el RoutingRules.ps1 de ejemplo. Al configurar las reglas de enrutamiento de voz, tome nota del contexto de teléfono (es decir, perfil de/Location o/SimpleName) y códigos de área interna y externa para poder especificarlos al crear usuarios y durante la configuración de LyncPerfTool (específicamente para RTC-UC y UC-PSTN). Por ejemplo, el parámetro SimpleName en la llamada al cmdlet **New-CsDialPlan** en el ejemplo RoutingRules.ps1 se debe usar para el valor LocationProfile en la siguiente ilustración de UserProfileGenerator.exe.

![Regla de ejemplo de enrutamiento de voz.](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "Regla de ejemplo de enrutamiento de voz.")

Para obtener más información, consulte la documentación 2013 de Lync Server y la ayuda del cmdlet para [cmdlets de telefonía IP empresarial en Lync server 2013](https://technet.microsoft.com/library/gg415658\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-conferencing-attendant-application"></a>Configurar la aplicación de operador de conferencia

Vea el ConferenceAutoAttendantConfiguration.ps1 de ejemplo. Tome nota del número de teléfono ConferencingAutoAttendant (1121111111, de forma predeterminada), de modo que pueda escribirlo en la herramienta de configuración de herramientas de LyncPerf para la generación de configuración.

![Configuración de la aplicación Operador de conferencia](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "Configuración de la aplicación Operador de conferencia")

Para obtener más información, consulte la documentación 2013 de Lync Server y la ayuda cmdlet para [cmdlets de conferencias web en Lync server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) y [cmdlets de conferencias de acceso telefónico local en Lync Server 2013](https://technet.microsoft.com/library/gg415630\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-lync-server-call-park-service"></a>Configuración del servicio de estacionamiento de llamadas de Lync Server

El parque de llamadas está deshabilitado de forma predeterminada. Vea el CallParkConfiguration.ps1 de ejemplo. Para obtener más información, consulte la documentación 2013 de Lync Server y la ayuda del cmdlet para [cmdlets de aplicaciones de estacionamiento de llamadas en Lync Server 2013](https://technet.microsoft.com/library/gg415639\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-emergency-calls"></a>Configuración de llamadas de emergencia

Realice los siguientes pasos para configurar las pruebas de rendimiento y estrés para las llamadas de emergencia.

1.  Configura una ruta de voz para llamadas de emergencia. Para obtener un ejemplo de la configuración de esta ruta de voz, vea el script de RoutingRules.ps1 en el comentario "Route E911 to RTC".
    
    <div>
    

    > [!WARNING]  
    > El comando de ejemplo de RoutingRules.ps1 tiene un patrón de números que incluye el número 119 en lugar de 911. Debes evitar usar 911 (o tu número de emergencia local) para evitar llamadas accidentales a tus operadores de emergencia locales durante las pruebas de carga. Esta configuración es solo para fines de simulación.

    
    </div>

2.  Configure las direcciones rellenando los valores de la pestaña **Lis** en la UserProvisioningTool, tal como se muestra en la siguiente ilustración.
    
    ![Configuración del servicio de información de ubicación.](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "Configuración del servicio de información de ubicación.")  

3.  Haga clic en **generar archivos de configuración Lis**.

4.  Se generan archivos CSV para puertos, subredes, conmutadores y puntos de acceso inalámbrico (WAP), así como un archivo XML para la herramienta de estrés y rendimiento de Lync Server 2013. Los archivos CSV se deben usar como entradas (en la misma carpeta) al configurar el servicio de información de ubicación (LIS) con el script de LisConfiguration.ps1. Mueva el archivo de Locations0.xml generado a la misma carpeta que el ejecutable de la herramienta de estrés y rendimiento de Lync Server 2013 (LyncPerfTool.exe), que ejecutará los escenarios de Perfil de ubicación (plan de marcado).

</div>

<div>

## <a name="creating-enabling-configuring-and-disabling-users"></a>Crear, habilitar, configurar y deshabilitar usuarios

Debe crear todos los usuarios antes de ejecutar las siguientes secuencias de comandos. Siga las instrucciones de [crear usuarios y contactos](create-users-and-contacts.md) para crear usuarios. Para obtener más información, consulte la documentación del cmdlet 2013 de Lync Server para los cmdlets [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)), [set-CsUser](https://technet.microsoft.com/library/gg398510\(v=ocs.15\))y [Disable-CsUser](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) .

</div>

<div>

## <a name="configuring-response-group-application"></a>Configuración de la aplicación de grupo de respuesta

Vea el ResponseGroupConfiguration.ps1 de ejemplo. Para obtener más información, consulte la documentación 2013 de Lync Server y la ayuda del cmdlet para [cmdlets de la aplicación de grupos de respuesta en Lync server 2013](https://technet.microsoft.com/library/gg415654\(v=ocs.15\)). Para revisar la configuración de la aplicación de grupo de respuesta, consulte `https://<poolfqdn>/RgsConfig/` , como se muestra en la siguiente ilustración.

![La herramienta Configuración del grupo de respuesta.](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "La herramienta Configuración del grupo de respuesta.")

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

