---
title: 'Lync Server 2013: asignar números de llamada de grupo a los usuarios'
description: 'Lync Server 2013: asignar números de llamada de grupo a los usuarios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign Group Call Pickup numbers to users
ms:assetid: b8e79275-8e7e-4799-b908-f34f61df22f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945647(v=OCS.15)
ms:contentKeyID: 51541508
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d550b4556af427e11e99ffb26fb2a6c34d019490
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438347"
---
# <a name="assign-group-call-pickup-numbers-to-users-in-lync-server-2013"></a><span data-ttu-id="ecea8-103">Asignar números de recogida de llamadas grupales a los usuarios de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecea8-103">Assign Group Call Pickup numbers to users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ecea8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ecea8-104">

<span> </span></span></span>

<span data-ttu-id="ecea8-105">_**Última modificación del tema:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="ecea8-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="ecea8-106">Después de agregar los números del grupo de recogida de llamadas grupales a la tabla de llamadas en órbita, puede asignar los grupos a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ecea8-106">After you add Group Call Pickup group numbers to the call park orbit table, you can assign the groups to users.</span></span> <span data-ttu-id="ecea8-107">Use la herramienta del kit de recursos de activación de características de extensión secundaria (SEFAUtil) para asignar grupos de recogida de llamadas a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ecea8-107">Use the secondary extension feature activation (SEFAUtil ) resource kit tool to assign call pickup groups to users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ecea8-108">En una implementación híbrida, no asigne un grupo de recogida de llamadas grupal a los usuarios alojados en línea.</span><span class="sxs-lookup"><span data-stu-id="ecea8-108">In a hybrid deployment, do not assign a Group Call Pickup group to users who are homed online.</span></span> <span data-ttu-id="ecea8-109">Los usuarios alojados en Internet no pueden participar en la recogida de llamadas grupales.</span><span class="sxs-lookup"><span data-stu-id="ecea8-109">Users who are homed online cannot participate in Group Call Pickup.</span></span> <span data-ttu-id="ecea8-110">Es decir, otros usuarios no pueden contestar las llamadas y no pueden responder llamadas a otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="ecea8-110">That is, their calls cannot be answered by other users, and they cannot answer calls to other users.</span></span>



</div>

<div>

## <a name="to-assign-a-group-call-pickup-group-to-a-user"></a><span data-ttu-id="ecea8-111">Para asignar un grupo de recogida de llamadas grupal a un usuario</span><span class="sxs-lookup"><span data-stu-id="ecea8-111">To assign a Group Call Pickup group to a user</span></span>

1.  <span data-ttu-id="ecea8-112">Inicie sesión como administrador en el equipo en el que haya instalado la herramienta SEFAUtil.</span><span class="sxs-lookup"><span data-stu-id="ecea8-112">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="ecea8-113">En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="ecea8-113">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    <span data-ttu-id="ecea8-114">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ecea8-114">For example:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ecea8-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecea8-115">See Also</span></span>


[<span data-ttu-id="ecea8-116">Habilitar la recogida de llamadas grupales para los usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecea8-116">Enable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-enable-group-call-pickup-for-users.md)  
[<span data-ttu-id="ecea8-117">Deshabilitar la recogida de llamadas grupales para los usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecea8-117">Disable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="ecea8-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ecea8-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

