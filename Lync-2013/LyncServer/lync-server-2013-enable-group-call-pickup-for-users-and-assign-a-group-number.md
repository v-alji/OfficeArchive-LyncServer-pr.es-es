---
title: 'Lync Server 2013: habilitar la recogida de llamadas grupales para los usuarios y asignar un número de grupo'
description: 'Lync Server 2013: habilitar la recogida de llamadas grupales para los usuarios y asignar un número de grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Group Call Pickup for users and assign a group number
ms:assetid: c33bb6c2-d43b-4fb6-a0fa-6d82a7b09abe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945650(v=OCS.15)
ms:contentKeyID: 51541517
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a03fcb20bfd88842dc8b29100b9ece595bf76254
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428926"
---
# <a name="enable-group-call-pickup-for-users-in-lync-server-2013-and-assign-a-group-number"></a><span data-ttu-id="96510-103">Habilitar la recogida de llamadas grupales para los usuarios en Lync Server 2013 y asignar un número de grupo</span><span class="sxs-lookup"><span data-stu-id="96510-103">Enable Group Call Pickup for users in Lync Server 2013 and assign a group number</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96510-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96510-104">

<span> </span></span></span>

<span data-ttu-id="96510-105">_**Última modificación del tema:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="96510-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="96510-106">Después de agregar los números del grupo de recogida de llamadas a la tabla de llamadas en órbita, asigne los números de grupo a los usuarios y habilite la recogida de llamadas grupales.</span><span class="sxs-lookup"><span data-stu-id="96510-106">After you add call pickup group numbers to the call park orbit table, you assign the group numbers to users and enable Group Call Pickup for them.</span></span> <span data-ttu-id="96510-107">Use la herramienta del kit de recursos de activación de características de extensión secundaria (SEFAUtil) para asignar números de grupo y habilitar la recogida de llamadas grupales.</span><span class="sxs-lookup"><span data-stu-id="96510-107">Use the secondary extension feature activation (SEFAUtil) resource kit tool to assign group numbers and enable Group Call Pickup.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="96510-108">En una implementación híbrida, no asigne un grupo de recogida de llamadas grupal a los usuarios alojados en línea.</span><span class="sxs-lookup"><span data-stu-id="96510-108">In a hybrid deployment, do not assign a Group Call Pickup group to users who are homed online.</span></span> <span data-ttu-id="96510-109">Los usuarios alojados en Internet no pueden participar en la recogida de llamadas grupales.</span><span class="sxs-lookup"><span data-stu-id="96510-109">Users who are homed online cannot participate in Group Call Pickup.</span></span> <span data-ttu-id="96510-110">Es decir, otros usuarios no pueden contestar las llamadas y no pueden responder llamadas a otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="96510-110">That is, their calls cannot be answered by other users, and they cannot answer calls to other users.</span></span>



</div>

<div>

## <a name="to-assign-a-group-number-and-enable-group-call-pickup-for-a-user"></a><span data-ttu-id="96510-111">Para asignar un número de grupo y habilitar la recogida de llamadas grupales para un usuario</span><span class="sxs-lookup"><span data-stu-id="96510-111">To assign a group number and enable Group Call Pickup for a user</span></span>

1.  <span data-ttu-id="96510-112">Inicie sesión como administrador en el equipo en el que haya instalado la herramienta SEFAUtil.</span><span class="sxs-lookup"><span data-stu-id="96510-112">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="96510-113">En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="96510-113">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    <span data-ttu-id="96510-114">Por ejemplo, para asignar el número de grupo 199 a un usuario:</span><span class="sxs-lookup"><span data-stu-id="96510-114">For example, to assign group number 199 to a user:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199 

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="96510-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="96510-115">See Also</span></span>


[<span data-ttu-id="96510-116">Deshabilitar la recogida de llamadas grupales para los usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96510-116">Disable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="96510-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96510-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

