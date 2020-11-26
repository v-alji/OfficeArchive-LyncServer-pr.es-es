---
title: 'Lync Server 2013: New-CsWebServiceConfiguration para la administración de libretas de direcciones'
description: 'Lync Server 2013: New-CsWebServiceConfiguration para la administración de libretas de direcciones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsWebServiceConfiguration for Address Book management
ms:assetid: 49e4ecc5-aa3e-4dd4-a32c-b0dea3758fab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429703(v=OCS.15)
ms:contentKeyID: 48184067
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8972f1b4fe71554e6a8925ddebea6303e2f074a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445438"
---
# <a name="new-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="b699f-103">New-CsWebServiceConfiguration para la administración de libretas de direcciones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b699f-103">New-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b699f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b699f-104">

<span> </span></span></span>

<span data-ttu-id="b699f-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="b699f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="b699f-106">¿Quién puede ejecutar este cmdlet? de forma predeterminada, los miembros de los siguientes grupos tienen autorización para ejecutar el cmdlet New-CsWebServiceConfiguration localmente: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="b699f-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsWebServiceConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="b699f-107">Para devolver una lista de todas las funciones de control de acceso basado en roles (RBAC) a las que se ha asignado este cmdlet (incluidos los roles RBAC que haya creado usted mismo), ejecute el siguiente comando desde el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b699f-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsWebServiceConfiguration"}

<span data-ttu-id="b699f-108">El cmdlet New-CsWebServiceConfiguration define una nueva configuración para los servicios Web de su organización.</span><span class="sxs-lookup"><span data-stu-id="b699f-108">The cmdlet New-CsWebServiceConfiguration defines a new configuration for Web Services in your organization.</span></span> <span data-ttu-id="b699f-109">El ámbito de la configuración de los servicios web solo puede encontrarse en el nivel de sitio o de servicio.</span><span class="sxs-lookup"><span data-stu-id="b699f-109">The scope for the Web Services configuration can only be at the site or service level.</span></span> <span data-ttu-id="b699f-110">No puede crear una nueva configuración de servicios web en el nivel global.</span><span class="sxs-lookup"><span data-stu-id="b699f-110">It cannot create a new Web Services configuration at the global level.</span></span> <span data-ttu-id="b699f-111">Específicamente de interés para la libreta de direcciones es el atributo EnableGroupExansion.</span><span class="sxs-lookup"><span data-stu-id="b699f-111">Specifically of interest to the Address Book is the EnableGroupExansion attribute.</span></span> <span data-ttu-id="b699f-112">Si se establece en true, los servicios Web pueden responder a las solicitudes de expansión de grupo.</span><span class="sxs-lookup"><span data-stu-id="b699f-112">If set to True, the Web Services can respond to requests for group expansion.</span></span>

<span data-ttu-id="b699f-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b699f-113">For example:</span></span>

    New-CsWebServiceConfiguration -Identity site:Redmond -EnableGroupExpansion $False -UseCertificateAuth $True

<div>

## <a name="see-also"></a><span data-ttu-id="b699f-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="b699f-114">See Also</span></span>


[<span data-ttu-id="b699f-115">Nuevo: CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b699f-115">New-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsWebServiceConfiguration)  
  

<span data-ttu-id="b699f-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b699f-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

