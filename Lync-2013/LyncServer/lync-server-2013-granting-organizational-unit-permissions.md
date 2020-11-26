---
title: 'Lync Server 2013: Conceder permisos de unidad organizativa'
description: 'Lync Server 2013: concesión de permisos para unidades organizativas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting organizational unit permissions
ms:assetid: 95ee5ffa-39b1-4d80-87a2-27bb364f7396
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398763(v=OCS.15)
ms:contentKeyID: 48184849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47ad862241e409190620afa7dbf4fa73adf339de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427903"
---
# <a name="granting-organizational-unit-permissions-in-lync-server-2013"></a><span data-ttu-id="7f7e2-103">Conceder permisos de unidad organizativa en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f7e2-103">Granting organizational unit permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f7e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f7e2-104">

<span> </span></span></span>

<span data-ttu-id="7f7e2-105">_**Última modificación del tema:** 2012-05-14_</span><span class="sxs-lookup"><span data-stu-id="7f7e2-105">_**Topic Last Modified:** 2012-05-14_</span></span>

<span data-ttu-id="7f7e2-106">Puede usar el cmdlet **Grant-CsOuPermission** para conceder permisos a los objetos de unidades organizativas (OU) especificadas de modo que los miembros de los grupos RTC universales creados por la preparación del bosque puedan tener acceso a ellos sin ser miembros del grupo administradores del dominio.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-106">You can use the **Grant-CsOuPermission** cmdlet to grant permissions to objects in specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access them without being members of the Domain Admins group.</span></span> <span data-ttu-id="7f7e2-107">Los permisos agregados a la unidad organizativa especificada son los mismos permisos que el cmdlet **enable-CsAdDomain** agrega a los contenedores de equipos y usuarios durante la preparación del dominio.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-107">The permissions added to the specified OU are the same permissions that the **Enable-CsAdDomain** cmdlet adds to the computers and users containers during domain preparation.</span></span>

<span data-ttu-id="7f7e2-108">Use el cmdlet **Test-CsOuPermission** para comprobar los permisos que configuró mediante el cmdlet **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="7f7e2-108">Use the **Test-CsOuPermission** cmdlet to verify the permissions you set up by using the **Grant-CsOuPermission** cmdlet.</span></span>

<span data-ttu-id="7f7e2-109">Puede usar el cmdlet **REVOKE-CsOuPermission** para quitar los permisos que ha otorgado mediante el cmdlet **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="7f7e2-109">You can use the **Revoke-CsOuPermission** cmdlet to remove permissions that you granted by using the **Grant-CsOuPermission** cmdlet.</span></span>

<div>

## <a name="to-grant-ou-permissions"></a><span data-ttu-id="7f7e2-110">Para conceder permisos de Uo</span><span class="sxs-lookup"><span data-stu-id="7f7e2-110">To grant OU permissions</span></span>

1.  <span data-ttu-id="7f7e2-111">Inicie sesión en un equipo que ejecute Lync Server 2013 en el dominio al que desee conceder permisos de Uo.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-111">Log on to a computer running Lync Server 2013 in the domain where you want to grant OU permissions.</span></span> <span data-ttu-id="7f7e2-112">Use una cuenta que sea miembro del grupo administradores del dominio o del grupo administradores de la organización si la OU está en otro dominio secundario.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-112">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="7f7e2-113">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="7f7e2-114">Ejecute:</span><span class="sxs-lookup"><span data-stu-id="7f7e2-114">Run:</span></span>
    
        Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="7f7e2-115">Si no especifica el parámetro domain, el valor predeterminado es el dominio local.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-115">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-verify-ou-permissions"></a><span data-ttu-id="7f7e2-116">Para comprobar los permisos de Uo</span><span class="sxs-lookup"><span data-stu-id="7f7e2-116">To verify OU permissions</span></span>

1.  <span data-ttu-id="7f7e2-117">Inicie sesión en un equipo que ejecute Lync Server 2013 en el dominio en el que desea comprobar los permisos de Uo que ha otorgado mediante el cmdlet **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="7f7e2-117">Log on to a computer running Lync Server 2013 in the domain where you want to verify OU permissions that you granted by using the **Grant-CsOuPermission** cmdlet.</span></span> <span data-ttu-id="7f7e2-118">Use una cuenta que sea miembro del grupo administradores del dominio o del grupo administradores de la organización si la OU está en otro dominio secundario.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-118">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="7f7e2-119">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="7f7e2-120">Ejecute:</span><span class="sxs-lookup"><span data-stu-id="7f7e2-120">Run:</span></span>
    
        Test-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="7f7e2-121">Si no especifica el parámetro domain, el valor predeterminado es el dominio local.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-121">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-revoke-ou-permissions"></a><span data-ttu-id="7f7e2-122">Para revocar permisos de Uo</span><span class="sxs-lookup"><span data-stu-id="7f7e2-122">To revoke OU permissions</span></span>

1.  <span data-ttu-id="7f7e2-123">Inicie sesión en un equipo que ejecute Lync Server 2013 en el dominio en el que desea revocar permisos de OU que ha otorgado el cmdlet **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="7f7e2-123">Log on to a computer running Lync Server 2013 in the domain where you want to revoke OU permissions that were granted by the **Grant-CsOuPermission** cmdlet.</span></span> <span data-ttu-id="7f7e2-124">Use una cuenta que sea miembro del grupo administradores del dominio o del grupo administradores de la organización si la OU está en otro dominio secundario.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-124">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="7f7e2-125">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-125">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="7f7e2-126">Ejecute:</span><span class="sxs-lookup"><span data-stu-id="7f7e2-126">Run:</span></span>
    
        Revoke-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="7f7e2-127">Si no especifica el parámetro domain, el valor predeterminado es el dominio local.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-127">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

<span data-ttu-id="7f7e2-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f7e2-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

