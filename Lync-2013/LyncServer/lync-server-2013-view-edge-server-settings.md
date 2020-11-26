---
title: 'Lync Server 2013: ver la configuración del servidor perimetral'
description: 'Lync Server 2013: ver la configuración del servidor perimetral.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Edge Server settings
ms:assetid: 684154cc-cffc-4d2e-8baa-be52c625e5d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747890(v=OCS.15)
ms:contentKeyID: 63969612
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4318b8c97f53f267bb79953af504977f6437214d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446288"
---
# <a name="view-edge-server-settings-in-lync-server-2013"></a><span data-ttu-id="f9f7c-103">Ver la configuración del servidor perimetral en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9f7c-103">View Edge Server settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9f7c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9f7c-104">

<span> </span></span></span>

<span data-ttu-id="f9f7c-105">_**Última modificación del tema:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="f9f7c-105">_**Topic Last Modified:** 2014-05-20_</span></span>

<span data-ttu-id="f9f7c-106">Las configuraciones de servidor de borde general se deben revisar según los datos de la base de datos de administración de la configuración, para ayudar a garantizar que todos los cambios se documentaron según los procedimientos de control de cambios definidos.</span><span class="sxs-lookup"><span data-stu-id="f9f7c-106">General Edge Server configurations should be reviewed against the data in the configuration management database—to help guarantee that all changes were documented as per the defined change control procedures.</span></span>

<span data-ttu-id="f9f7c-107">Las comprobaciones adicionales podrían incluir las que se describen en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="f9f7c-107">Additional checks could include those that are described in the following sections:</span></span>

<div>

## <a name="verify-the-allow-and-block-lists"></a><span data-ttu-id="f9f7c-108">Comprobar las listas permitir o bloquear</span><span class="sxs-lookup"><span data-stu-id="f9f7c-108">Verify the Allow and block lists</span></span>

<span data-ttu-id="f9f7c-109">Comprobar el URI del SIP las listas "permitir" y "bloquear" de los dominios federados, para determinar si los espacios de nombres en la lista siguen siendo válidos.</span><span class="sxs-lookup"><span data-stu-id="f9f7c-109">Verify the SIP URI "Allow" and "Block" lists for Federated domains—to determine whether listed namespaces are still valid.</span></span>

<span data-ttu-id="f9f7c-110">Puede usar Windows PowerShell para ver las listas permitidas y bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="f9f7c-110">You can use Windows PowerShell to view the allowed and blocked lists.</span></span> <span data-ttu-id="f9f7c-111">Para revisar los dominios en la lista dominios permitidos, ejecute el siguiente comando de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f9f7c-111">To review the domains on the Allowed Domains list, run the following Windows PowerShell command:</span></span>

`Get-CsAllowedDomain`

<span data-ttu-id="f9f7c-112">Ese comando devuelve información similar a la siguiente para los dominios de la lista de dominios permitidos:</span><span class="sxs-lookup"><span data-stu-id="f9f7c-112">That command returns information similar to this for the domains on the Allowed Domains list:</span></span>

<span data-ttu-id="f9f7c-113">Identidad: contoso.com</span><span class="sxs-lookup"><span data-stu-id="f9f7c-113">Identity : contoso.com</span></span>

<span data-ttu-id="f9f7c-114">Dominio: contoso.com</span><span class="sxs-lookup"><span data-stu-id="f9f7c-114">Domain : contoso.com</span></span>

<span data-ttu-id="f9f7c-115">ProxyFqdn :</span><span class="sxs-lookup"><span data-stu-id="f9f7c-115">ProxyFqdn :</span></span>

<span data-ttu-id="f9f7c-116">Lín</span><span class="sxs-lookup"><span data-stu-id="f9f7c-116">Comment :</span></span>

<span data-ttu-id="f9f7c-117">MarkForMonitoring: falso</span><span class="sxs-lookup"><span data-stu-id="f9f7c-117">MarkForMonitoring : False</span></span>

<span data-ttu-id="f9f7c-118">Lín</span><span class="sxs-lookup"><span data-stu-id="f9f7c-118">Comment :</span></span>

<span data-ttu-id="f9f7c-119">Para revisar los dominios de la lista de dominios bloqueados, use este comando:</span><span class="sxs-lookup"><span data-stu-id="f9f7c-119">To review the domains on the blocked domains list, use this command:</span></span>

`Get-CsBlockedDomain`

<span data-ttu-id="f9f7c-120">A su vez, recibirá información como esta para cada dominio bloqueado:</span><span class="sxs-lookup"><span data-stu-id="f9f7c-120">In turn, you'll receive information such as this for each blocked domain:</span></span>

<span data-ttu-id="f9f7c-121">Identidad: tailspintoys.com</span><span class="sxs-lookup"><span data-stu-id="f9f7c-121">Identity : tailspintoys.com</span></span>

<span data-ttu-id="f9f7c-122">Dominio: tailspintoys.com</span><span class="sxs-lookup"><span data-stu-id="f9f7c-122">Domain : tailspintoys.com</span></span>

<span data-ttu-id="f9f7c-123">Windows PowerShell también le permite comprobar si puede conectarse a los dominios de su lista de dominios permitidos.</span><span class="sxs-lookup"><span data-stu-id="f9f7c-123">Windows PowerShell also enables you to verify that you can connection to the domains on your Allowed Domains list.</span></span> <span data-ttu-id="f9f7c-124">Por ejemplo, este comando comprueba la conexión entre el servidor perimetral (el TargetFqdn) y el dominio federado contoso.com:</span><span class="sxs-lookup"><span data-stu-id="f9f7c-124">For example, this command verifies the connection between your Edge Server (the TargetFqdn) and the federated domain contoso.com:</span></span>

`Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com"`

<span data-ttu-id="f9f7c-125">Y este comando comprueba la conexión entre el servidor perimetral y todos los dominios que se encuentran en la lista de dominios permitidos:</span><span class="sxs-lookup"><span data-stu-id="f9f7c-125">And this command verifies the connection between your Edge Server and all of the domains found on your Allowed Domains list:</span></span>

`Get-CsAllowedDomain | ForEach-Object {Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain $_.Domain}`

</div>

<div>

## <a name="verify-multiple-edge-servers-are-identical"></a><span data-ttu-id="f9f7c-126">Comprobar si hay varios servidores perimetrales idénticos</span><span class="sxs-lookup"><span data-stu-id="f9f7c-126">Verify multiple Edge Servers are identical</span></span>

<span data-ttu-id="f9f7c-127">Si se implementan varios servidores perimetrales en una matriz de equilibrio de carga, le recomendamos verificar que todos los servidores perimetrales de la matriz estén configurados de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="f9f7c-127">If multiple Edge Servers are deployed in a load balanced array, we recommend verifying that all Edge Servers in the array are configured in the same manner.</span></span>

<span data-ttu-id="f9f7c-128">Puede ver la configuración de los servidores perimetrales en el panel de detalles de la extensión 2013 de Lync Server para el complemento Administración de equipos.</span><span class="sxs-lookup"><span data-stu-id="f9f7c-128">You can view settings for Edge Servers in the details pane of the Lync Server 2013 extension for the Computer Management snap-in.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f9f7c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9f7c-129">See Also</span></span>


[<span data-ttu-id="f9f7c-130">Get-CsAllowedDomain</span><span class="sxs-lookup"><span data-stu-id="f9f7c-130">Get-CsAllowedDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAllowedDomain)  
[<span data-ttu-id="f9f7c-131">Get-CsBlockedDomain</span><span class="sxs-lookup"><span data-stu-id="f9f7c-131">Get-CsBlockedDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsBlockedDomain)  
[<span data-ttu-id="f9f7c-132">Prueba-CsFederatedPartner</span><span class="sxs-lookup"><span data-stu-id="f9f7c-132">Test-CsFederatedPartner</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner)  
  

<span data-ttu-id="f9f7c-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9f7c-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

