---
title: 'Lync Server 2013: deshabilitar la recogida de llamadas grupales para usuarios'
description: 'Lync Server 2013: deshabilitar la recogida de llamadas grupales para los usuarios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disable Group Call Pickup for users
ms:assetid: 91b06f9e-2840-45a2-bbb3-6a29179b9a9f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945638(v=OCS.15)
ms:contentKeyID: 51541492
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b3f5b4542cf7bb8ea5be524d2695701979ec2987
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429108"
---
# <a name="disable-group-call-pickup-for-users-in-lync-server-2013"></a><span data-ttu-id="f202d-103">Deshabilitar la recogida de llamadas grupales para los usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f202d-103">Disable Group Call Pickup for users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f202d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f202d-104">

<span> </span></span></span>

<span data-ttu-id="f202d-105">_**Última modificación del tema:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="f202d-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="f202d-106">Use el siguiente procedimiento para deshabilitar la recogida de llamadas grupales para un usuario.</span><span class="sxs-lookup"><span data-stu-id="f202d-106">Use the following procedure to disable Group Call Pickup for a user.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f202d-107">Al deshabilitar la recogida de llamadas grupales para un usuario, el número del grupo de recogida de llamadas que se asignó al usuario no se conserva.</span><span class="sxs-lookup"><span data-stu-id="f202d-107">When you disable Group Call Pickup for a user, the call pickup group number that was assigned to the user is not retained.</span></span> <span data-ttu-id="f202d-108">Si posteriormente deseas volver a habilitar la recogida de llamadas grupales para ese usuario, debes asignar el número del grupo de recogida de llamadas de nuevo con el parámetro/enablegrouppickup.</span><span class="sxs-lookup"><span data-stu-id="f202d-108">If you subsequently want to re-enable Group Call Pickup for that user, you must assign the call pickup group number again with the /enablegrouppickup parameter.</span></span>



</div>

<div>

## <a name="to-disable-group-call-pickup-for-a-user"></a><span data-ttu-id="f202d-109">Para deshabilitar la recogida de llamadas grupales para un usuario</span><span class="sxs-lookup"><span data-stu-id="f202d-109">To disable Group Call Pickup for a user</span></span>

1.  <span data-ttu-id="f202d-110">Inicie sesión como administrador en el equipo en el que haya instalado la herramienta SEFAUtil.</span><span class="sxs-lookup"><span data-stu-id="f202d-110">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="f202d-111">En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="f202d-111">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /disablegrouppickup
    
    <span data-ttu-id="f202d-112">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f202d-112">For example:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /disablegrouppickup

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f202d-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="f202d-113">See Also</span></span>


[<span data-ttu-id="f202d-114">Asignar números de recogida de llamadas grupales a los usuarios de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f202d-114">Assign Group Call Pickup numbers to users in Lync Server 2013</span></span>](lync-server-2013-assign-group-call-pickup-numbers-to-users.md)  
[<span data-ttu-id="f202d-115">Habilitar la recogida de llamadas grupales para los usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f202d-115">Enable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-enable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="f202d-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f202d-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

