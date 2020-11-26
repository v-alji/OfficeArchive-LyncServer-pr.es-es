---
title: Comprobar que todos los objetos de contacto de mensajería unificada de Exchange se han quitado del grupo heredado
description: Compruebe que todos los objetos de contacto de mensajería unificada de Exchange se han quitado del grupo heredado.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify that all Exchange UM Contact objects are removed from the legacy pool
ms:assetid: 5a813169-0ed7-4f84-a242-ed2cd4ea5c43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688068(v=OCS.15)
ms:contentKeyID: 49733664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af5dea6cf746c55d8fecf074e132f721c380de1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440139"
---
# <a name="verify-that-all-exchange-um-contact-objects-are-removed-from-the-legacy-pool"></a><span data-ttu-id="81055-103">Comprobar que todos los objetos de contacto de mensajería unificada de Exchange se han quitado del grupo heredado</span><span class="sxs-lookup"><span data-stu-id="81055-103">Verify that all Exchange UM Contact objects are removed from the legacy pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="81055-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="81055-104">

<span> </span></span></span>

<span data-ttu-id="81055-105">_**Última modificación del tema:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="81055-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="81055-106">Use la herramienta **OCSUmUtil** o el cmdlet **Get-CsExumContact** para comprobar que los objetos de contacto de MU de Exchange se han quitado del grupo heredado de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="81055-106">Use either the **OCSUmUtil** tool or the **Get-CsExumContact** cmdlet to verify that Exchange UM contact objects have been removed from the legacy Office Communications Server 2007 R2 pool.</span></span> <span data-ttu-id="81055-107">**OCSUmUtil** se encuentra en la siguiente carpeta:</span><span class="sxs-lookup"><span data-stu-id="81055-107">**OCSUmUtil** is located in the following folder:</span></span>

<span data-ttu-id="81055-108">% Archivos de programa% \\ archivos comunes \\ soporte técnico de Lync Server 2013 \\ \\OcsUMUtil.exe</span><span class="sxs-lookup"><span data-stu-id="81055-108">%Program Files%\\Common Files\\Lync Server 2013\\Support\\OcsUMUtil.exe</span></span>

<span data-ttu-id="81055-109">**OCSUmUtil** debe ejecutarse desde una cuenta de usuario que tenga:</span><span class="sxs-lookup"><span data-stu-id="81055-109">**OCSUmUtil** must be run from a user account that has:</span></span>

  - <span data-ttu-id="81055-110">Pertenencia al grupo RTCUniversalServerAdmins y RTCUniversalUserAdmins (que incluye derechos para leer la configuración de mensajería unificada de Exchange Server)</span><span class="sxs-lookup"><span data-stu-id="81055-110">Membership in the RTCUniversalServerAdmins and RTCUniversalUserAdmins group (which includes rights to read Exchange Server Unified Messaging settings)</span></span>

  - <span data-ttu-id="81055-111">Derechos de dominio para crear objetos de contacto en el contenedor de unidades organizativas (OU) especificadas</span><span class="sxs-lookup"><span data-stu-id="81055-111">Domain rights to create contact objects in the specified organizational unit (OU) container</span></span>

<span data-ttu-id="81055-112">Para obtener detalles sobre el uso del cmdlet **Get-CsExumContact** , vea [Get-CsExumContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) en la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="81055-112">For details about using the **Get-CsExumContact** cmdlet, see [Get-CsExUmContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) in the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="81055-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="81055-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

