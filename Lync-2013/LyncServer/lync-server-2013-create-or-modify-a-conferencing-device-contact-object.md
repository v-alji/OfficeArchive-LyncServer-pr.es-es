---
title: 'Lync Server 2013: crear o modificar un objeto de contacto de dispositivo de conferencia'
description: 'Lync Server 2013: crear o modificar un objeto de contacto de dispositivos de conferencia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a conferencing device Contact object
ms:assetid: 62ed64be-379c-417d-9453-511881cf5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994035(v=OCS.15)
ms:contentKeyID: 51803945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 853ee1c7dfda2fda99431b8cc1a5210a51f39a4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398777"
---
# <a name="create-or-modify-a-conferencing-device-contact-object-in-lync-server-2013"></a>Crear o modificar un objeto de contacto de dispositivo de conferencia en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-10-02_

Para crear un objeto de sala de conferencias, primero debe crear una cuenta de usuario de Active Directory para representar el dispositivo. A continuación, use el cmdlet **enable-CsMeetingRoom** para habilitar esa cuenta como dispositivo de conferencia. Si necesita cambiar las propiedades de un dispositivo de conferencia existente, use el cmdlet **set-CsMeetingRoom** .

Estos cmdlets se pueden ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.

<div>


> [!NOTE]  
> Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

<div>


<div>

## <a name="creating-a-conferencing-device"></a>Crear un dispositivo de conferencia

  - Después de crear la cuenta de usuario de Active Directory que representa el nuevo dispositivo de conferencia, habilítelo mediante el cmdlet **enable-CsMeetingRoom** . Asegúrese de incluir a la identidad del dispositivo de conferencia, b) el grupo registrador en el que se va a alojar la cuenta de sala, y c) la dirección SIP que se va a asignar a esa cuenta. Por ejemplo:
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="modifying-a-conferencing-device"></a>Modificar un dispositivo de conferencia

  - Para modificar los valores de propiedad de un dispositivo de conferencia existente, use el cmdlet **set-CsMeetingRoom** . Por ejemplo, el siguiente comando actualiza el número de teléfono (LineUri) asociado a un dispositivo de Conferencia:
    
        Set-CsMeetingRoom -Identity "Redmond Conferencing device" -LineUri "tel:+12065551219"

</div>

Para obtener más información, consulte los temas de ayuda para el cmdlet [enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) y el cmdlet [set-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Set-CsMeetingRoom) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

