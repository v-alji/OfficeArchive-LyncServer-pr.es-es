---
title: 'Lync Server 2013: Habilitar usuarios para el almacenamiento de contactos unificado'
description: 'Lync Server 2013: habilitar usuarios para el almacén de contactos unificado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for unified contact store
ms:assetid: 7b46a01f-beb5-4a33-adb0-35f0502b168d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205024(v=OCS.15)
ms:contentKeyID: 48184599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2249249d314e13d840b276e46f1fe38ad271664a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428821"
---
# <a name="enable-users-for-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="3080c-103">Habilitar usuarios para el almacenamiento de contactos unificado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3080c-103">Enable users for unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3080c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3080c-104">

<span> </span></span></span>

<span data-ttu-id="3080c-105">_**Última modificación del tema:** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="3080c-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="3080c-106">Al implementar Lync Server 2013 y publicar la topología, el almacén de contactos unificado está habilitado para todos los usuarios de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3080c-106">When you deploy Lync Server 2013 and publish the topology, unified contact store is enabled for all users by default.</span></span> <span data-ttu-id="3080c-107">No es necesario realizar ninguna acción adicional para habilitar el almacén de contactos unificado después de implementar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3080c-107">You do not need to take any additional action to enable unified contact store after you deploy Lync Server 2013.</span></span> <span data-ttu-id="3080c-108">Pero, puede usar el cmdlet **Set-CsUserServicesPolicy** para personalizar qué usuarios tienen disponible el almacén de contactos unificado.</span><span class="sxs-lookup"><span data-stu-id="3080c-108">However, you can use the **Set-CsUserServicesPolicy** cmdlet to customize which users have unified contact store available.</span></span> <span data-ttu-id="3080c-109">Puede habilitar esta característica globalmente, por sitio, por inquilino, por individuo o por grupos de individuos.</span><span class="sxs-lookup"><span data-stu-id="3080c-109">You can enable this feature globally, by site, by tenant, or by individuals or groups of individuals.</span></span>

<div>

## <a name="to-enable-users-for-unified-contact-store"></a><span data-ttu-id="3080c-110">Para habilitar usuarios para el almacén de contactos unificado</span><span class="sxs-lookup"><span data-stu-id="3080c-110">To enable users for unified contact store</span></span>

1.  <span data-ttu-id="3080c-111">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="3080c-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="3080c-112">Siga uno de estos pasos:</span><span class="sxs-lookup"><span data-stu-id="3080c-112">Do any of the following:</span></span>
    
      - <span data-ttu-id="3080c-113">Para habilitar el almacén de contactos unificado globalmente para todos los usuarios de Lync Server, en la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="3080c-113">To enable unified contact store globally for all Lync Server users, at the command line, type:</span></span>
        
            Set-CsUserServicesPolicy -Identity global -UcsAllowed $True
    
      - <span data-ttu-id="3080c-114">Para habilitar el almacén de contactos unificado para los usuarios de un sitio específico, en la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="3080c-114">To enable unified contact store for the users at a specific site, at the command line, type:</span></span>
        
            New-CsUserServicesPolicy -Identity site:<site name> -UcsAllowed $True
        
        <span data-ttu-id="3080c-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3080c-115">For example:</span></span>
        
            New-CsUserServicesPolicy -Identity site:Redmond -UcsAllowed $True
    
      - <span data-ttu-id="3080c-116">Para habilitar el almacén de contactos unificado por inquilino, en la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="3080c-116">To enable unified contact store by tenant, at the command line, type:</span></span>
        
            Set-CsUserServicesPolicy -Tenant <tenantId> -UcsAllowed $True
        
        <span data-ttu-id="3080c-117">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3080c-117">For example:</span></span>
        
            Set-CsUserServicesPolicy -Tenant "38aad667-af54-4397-aaa7-e94c79ec2308" -UcsAllowed $True
    
      - <span data-ttu-id="3080c-118">Para habilitar el almacén de contactos unificado para usuarios específicos, en la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="3080c-118">To enable unified contact store for specific users, at the command line, type:</span></span>
        
            New-CsUserServicesPolicy -Identity "<policy name>" -UcsAllowed $True
            Grant-CsUserServicesPolicy -Identity "<user display name>" -PolicyName <"policy name">
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="3080c-119">También puede usar alias de usuario o URI de SIP en lugar del nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="3080c-119">You can also use user alias or SIP URI instead of the user display name.</span></span>

        
        </div>
        
        <span data-ttu-id="3080c-120">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3080c-120">For example:</span></span>
        
            New-CsUserServicesPolicy -Identity "UCS Enabled Users" -UcsAllowed $True
            Grant-CsUserServicesPolicy -Identity "Ken Myer" -PolicyName "UCS Enabled Users"
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="3080c-p102">En el ejemplo anterior, el primer comando crea una directiva por usuario denominada <EM>Usuarios habilitados para UCS</EM> con el indicador UcsAllowed establecido en True. El segundo comando asigna la directiva al usuario con el nombre para mostrar Ken Myer, lo que significa que Ken Myer ahora está habilitado para el almacén de contactos unificado.</span><span class="sxs-lookup"><span data-stu-id="3080c-p102">In the preceding example, the first command creates a new per-user policy named <EM>UCS Enabled Users</EM> with the UcsAllowed flag set to True. The second command assigns the policy to the user with the display name Ken Myer, which means that Ken Myer is now enabled for unified contact store.</span></span>

        
        <span data-ttu-id="3080c-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3080c-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

