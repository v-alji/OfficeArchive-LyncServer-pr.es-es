---
title: 'Lync Server 2013: Get-CsWebServiceConfiguration para la administración de libretas de direcciones'
description: 'Lync Server 2013: Get-CsWebServiceConfiguration para la administración de libretas de direcciones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsWebServiceConfiguration for Address Book management
ms:assetid: 0b223733-5224-47d1-9b47-2109e6f135c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429692(v=OCS.15)
ms:contentKeyID: 48183372
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb22d7607f9ac18cda9c8653374ae86839b033e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427946"
---
# <a name="get-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="34dc9-103">Get-CsWebServiceConfiguration para la administración de libretas de direcciones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34dc9-103">Get-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34dc9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34dc9-104">

<span> </span></span></span>

<span data-ttu-id="34dc9-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="34dc9-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="34dc9-106">¿Quién puede ejecutar este cmdlet? de forma predeterminada, los miembros de los siguientes grupos tienen autorización para ejecutar el cmdlet Get-CsWebServiceConfiguration de forma local: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="34dc9-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsWebServiceConfiguration cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="34dc9-107">Para devolver una lista de todas las funciones de control de acceso basado en roles (RBAC) a las que se ha asignado este cmdlet (incluidos los roles RBAC que haya creado usted mismo), ejecute el siguiente comando desde el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="34dc9-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsWebServiceConfiguration"}

<span data-ttu-id="34dc9-108">Get-CsWebServiceConfiguration devuelve información de la configuración de los servicios web actualmente en uso en su organización.</span><span class="sxs-lookup"><span data-stu-id="34dc9-108">Get-CsWebServiceConfiguration returns information of the Web Services configuration currently in use in your organization.</span></span> <span data-ttu-id="34dc9-109">De interés para los servicios de la libreta de direcciones es el estado de la función de expansión lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="34dc9-109">Of interest to the Address Book Services is the status of Distribution List Expansion function.</span></span> <span data-ttu-id="34dc9-110">Si el atributo EnableGroupExpansion es verdadero, su organización actualmente permite la expansión grupal.</span><span class="sxs-lookup"><span data-stu-id="34dc9-110">If the attribute EnableGroupExpansion is True, your organization currently allows group expansion.</span></span>

<span data-ttu-id="34dc9-111">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="34dc9-111">For example:</span></span>

    Get-CsWebServiceConfiguration -Identity site:Redmond

<div>

## <a name="see-also"></a><span data-ttu-id="34dc9-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="34dc9-112">See Also</span></span>


[<span data-ttu-id="34dc9-113">Get-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="34dc9-113">Get-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsWebServiceConfiguration)  
  

<span data-ttu-id="34dc9-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34dc9-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

