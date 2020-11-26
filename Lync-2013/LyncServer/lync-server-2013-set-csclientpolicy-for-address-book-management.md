---
title: 'Lync Server 2013: Set-CsClientPolicy para la administración de libretas de direcciones'
description: 'Lync Server 2013: Set-CsClientPolicy para la administración de libretas de direcciones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set-CsClientPolicy for Address Book management
ms:assetid: e7788bea-606f-481a-a3a4-1855ac028493
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429723(v=OCS.15)
ms:contentKeyID: 48185726
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10cbf6cb23315715ddb71680f3725808a55ad4a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441763"
---
# <a name="set-csclientpolicy-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="841ee-103">Set-CsClientPolicy para la administración de libretas de direcciones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="841ee-103">Set-CsClientPolicy for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="841ee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="841ee-104">

<span> </span></span></span>

<span data-ttu-id="841ee-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="841ee-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="841ee-106">¿Quién puede ejecutar este cmdlet? de forma predeterminada, los miembros de los siguientes grupos tienen autorización para ejecutar el cmdlet Set-CsClientPolicy localmente: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="841ee-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Set-CsClientPolicy cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="841ee-107">Para devolver una lista de todas las funciones de control de acceso basado en roles (RBAC) a las que se ha asignado este cmdlet (incluidos los roles RBAC que haya creado usted mismo), ejecute el siguiente comando desde el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="841ee-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Set-CsClientPolicy"}

<span data-ttu-id="841ee-108">Al igual que en New-ClientPolicy, el cmdlet Set-CsClientPolicy le permite modificar la configuración de los clientes que ya están en el lugar.</span><span class="sxs-lookup"><span data-stu-id="841ee-108">Similar to New-CsClientPolicy, the Set-CsClientPolicy cmdlet allows you to modify client settings that are already in place.</span></span>

<span data-ttu-id="841ee-109">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="841ee-109">For example:</span></span>

    Set-CsClientPolicy -Identity RedmondClientPolicy -WebServicePollInterval "00:15:00" -AddressBookAvailability "WebSearchAndFileDownload"

<div>

## <a name="see-also"></a><span data-ttu-id="841ee-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="841ee-110">See Also</span></span>


[<span data-ttu-id="841ee-111">Set-ClientPolicy</span><span class="sxs-lookup"><span data-stu-id="841ee-111">Set-CsClientPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy)  
  

<span data-ttu-id="841ee-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="841ee-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

