---
title: Cmdlets de Skype empresarial online que usan una identidad de proveedor de conferencias
description: Cmdlets de Skype empresarial online que usan una identidad de proveedor de conferencias.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use a conferencing provider identity
ms:assetid: be5621b6-ec11-4b12-83ec-075af269ca6a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362841(v=OCS.15)
ms:contentKeyID: 56558858
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 61ab4fb410878ca73314b73737948d9961462c87
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398573"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-a-conferencing-provider-identity"></a>Cmdlets de Skype empresarial online que usan una identidad de proveedor de conferencias

 


Para obtener información sobre todos los proveedores de servicios de audioconferencia con los que se ha contratado su organización, simplemente puede llamar al cmdlet [Get-CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\)) sin ningún parámetro:

    Get-CsAudioConferencingProvider

Si desea limitar los datos devueltos a un solo proveedor (en este ejemplo, el proveedor contoso audio Services), use el parámetro Identity:

    Get-CsAudioConferencingProvider -Identity "Contoso Audio Services"

Solo hay un cmdlet de Skype empresarial online que acepta un identificador de proveedor de servicios de audioconferencia:

  - [Get-CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\))

## <a name="see-also"></a>Vea también


[Identidades, ámbitos y espacios empresariales en Skype empresarial online](identities-scopes-and-tenants-in-skype-for-business-online.md)  
[Los cmdlets de Lync Online](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))

