---
title: 'Lync Server 2013: asignar una directiva de voz por usuario'
description: 'Lync Server 2013: asignar una directiva de voz por usuario.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user voice policy
ms:assetid: 9ee47ee7-1030-43b8-a4dc-bf685ea24659
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688155(v=OCS.15)
ms:contentKeyID: 49733758
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7ea0b171e10302b4c466187c54324cc2548e821
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443165"
---
# <a name="assign-a-per-user-voice-policy-in-lync-server-2013"></a>Asignar una directiva de voz por usuario en Lync Server 2013

 


Las directivas de voz globales y de nivel de sitio se asignan automáticamente a todas las cuentas de usuario de Lync Server 2013 que están habilitadas para telefonía IP empresarial. También puede asignar directivas de voz a usuarios específicos mediante el panel de control de Lync Server 2013 o el shell de administración de Lync Server 2013. Use los procedimientos de este tema para asignar directivas de usuario explícitamente a los usuarios de Lync Server.

## <a name="to-assign-a-user-specific-voice-policy-using-the-lync-server-control-panel"></a>Para asignar una directiva de voz específica del usuario mediante el panel de control de Lync Server

1.  Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.

2.  Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server. Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).

3.  En la barra de navegación izquierda, haga clic en **Usuarios** y, luego, busque la cuenta de usuario que desea configurar.

4.  En la tabla donde se enumeran los resultados de la búsqueda, haga clic en la cuenta de usuario, en **Editar** y, luego, en **Mostrar detalles**.

5.  En **Editar usuario de Lync Server** en **Directiva de voz**, seleccione la Directiva de usuario que desea aplicar.
    

    > [!NOTE]  
    > La configuración <STRONG> &lt; automática &gt; </STRONG> aplica el servidor predeterminado o la configuración de la directiva global.



## <a name="assign-per-user-voice-policies"></a>Asignar directivas de voz por usuario

Puede asignar directivas de voz por usuario mediante Windows PowerShell y el cmdlet **Grant-CsVoicePolicy** . Puede ejecutar este cmdlet desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell. Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, lea esta entrada de blog de Windows PowerShell de Lync Server: [Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto](https://go.microsoft.com/fwlink/p/?linkId=255876).

### <a name="assign-a-per-user-voice-policy-to-a-single-user"></a>Asignar una directiva de voz por usuario a un solo usuario

  - El comando siguiente asigna la Directiva de voz por usuario RedmondVoicePolicy al usuario Ken Myer.
    
        Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName "RedmondVoicePolicy"

## <a name="assign-a-per-user-voice-policy-to-multiple-users"></a>Asignar una directiva de voz por usuario a varios usuarios

  - Este comando asigna la Directiva de voz por usuario FinanceVoicePolicy a todos los usuarios que tienen cuentas en la OU de Finanzas de Active Directory. Para obtener más información sobre el parámetro de Uo que se usa en este comando, consulte la documentación del cmdlet [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .
    
        Get-CsUser -OU "ou=Finance,ou=North America,dc=litwareinc,dc=com" | Grant-CsVoicePolicy -PolicyName "FinanceVoicePolicy"

## <a name="unassign-a-per-user-voice-policy"></a>Cancelar la asignación de una directiva de voz por usuario

  - El comando siguiente elimina la asignación de cualquier directiva de voz por usuario asignada previamente a Ken Myer. Después de quitar la asignación de la directiva por usuario, se usará automáticamente la directiva global o la directiva del sitio local, si existe, para administrar a Ken Myer. La directiva de sitio tiene prioridad sobre la directiva global.
    
        Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName $Null

Para obtener más información, consulte el tema de ayuda para el cmdlet [Grant-CsVoicePolicy](https://technet.microsoft.com/library/gg398828\(v=ocs.15\)) .

## <a name="see-also"></a>Vea también


[Deshabilitar un usuario de telefonía IP empresarial en Lync Server 2013](lync-server-2013-disable-a-user-for-enterprise-voice.md)  


[Shell de administración de Lync Server 2013](lync-server-2013-lync-server-management-shell.md)

