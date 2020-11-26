---
title: 'Lync Server 2013: configuración de seguridad para Lync Phone Edition'
description: 'Lync Server 2013: configurar las opciones de seguridad para Lync Phone Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure security settings for Lync Phone Edition
ms:assetid: 6e7cec17-8a79-4428-9300-8821256c46cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521014(v=OCS.15)
ms:contentKeyID: 48184464
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82e6a6488db66a8497930ee6b2d1aec6fc8b0b2d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433769"
---
# <a name="configure-security-settings-for-lync-phone-edition-in-lync-server-2013"></a>Establecer la configuración de seguridad de Lync Phone Edition en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-02-23_

Ayude a mejorar la seguridad de los dispositivos que ejecutan Lync Phone Edition a través de la configuración de seguridad SIP y el bloqueo de teléfono.

<div>

## <a name="to-configure-security-settings-for-lync-phone-edition"></a>Para establecer la configuración de seguridad de Lync Phone Edition

1.  Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.

2.  Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server. Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).

3.  En la barra de navegación izquierda, haga clic en **clientes** y, después, en **configuración de dispositivo**.

4.  En la página **configuración de dispositivo** , en la lista de configuraciones de dispositivos, haga doble clic en la configuración para la que desea cambiar la configuración de seguridad.

5.  En **Editar configuración del dispositivo**, en **seguridad SIP**, especifique el nivel de seguridad SIP. El nivel predeterminado es **alto**, que se recomienda usar.

6.  En **Editar configuración del dispositivo**, en **bloqueo de teléfono**, Active o desactive la casilla **exigir bloqueo del dispositivo** (activada de forma predeterminada) y especifique la longitud mínima del PIN (6 caracteres de forma predeterminada) y el período de tiempo de espera (10 minutos de forma predeterminada). Le recomendamos que use estos valores predeterminados o que aumente la longitud del PIN o reduzca el período de tiempo de espera.
    
    <div>
    

    > [!NOTE]  
    > Para obtener más información, consulte <A href="lync-server-2013-enforce-phone-locking.md">exigir el bloqueo de teléfono en Lync Server 2013</A>.

    
    </div>

</div>

<div>

## <a name="configuring-security-settings-for-lync-phone-edition-phones-by-using-windows-powershell-cmdlets"></a>Configuración de la seguridad de los teléfonos de Lync Phone Edition mediante cmdlets de Windows PowerShell

La configuración de seguridad se puede administrar mediante el shell de administración de Lync Server y el cmdlet **Get-CsUCPhoneConfiguration** . Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell. Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-modify-the-sip-security-mode"></a>Para modificar el modo de seguridad SIP

  - Este comando establece la SIPSecurityMode para la colección global de configuración de teléfono UC en media. La seguridad del SIP también se podría establecer en baja o alta (el valor predeterminado).
    
        Set-CsUCPhoneConfiguration -Identity global -SIPSecurityMode "Medium"

</div>

<div>

## <a name="to-modify-the-minimum-pin-length"></a>Para modificar la longitud mínima del PIN

  - En este ejemplo, todas las opciones de configuración del teléfono UC se modifican para que requieran una longitud mínima de PIN de 7 dígitos.
    
        Get-CsUCPhoneConfiguration | Set-CsUCPhoneConfiguration -MinPhonePinLength 7

</div>

Para obtener más información, vea [Get-CsUCPhoneConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsUCPhoneConfiguration).

</div>

<div>

## <a name="see-also"></a>Vea también


[Administración de la autenticación de Lync Server 2013](lync-server-2013-managing-lync-server-authentication.md)  


[Administrar dispositivos, teléfonos y aplicaciones cliente en Lync Server 2013](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

