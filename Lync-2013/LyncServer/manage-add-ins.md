---
title: Administrar complementos
description: Administrar complementos.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Manage add-ins
ms:assetid: b84f868e-b36e-4ab4-b284-7db212d401c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205193(v=OCS.15)
ms:contentKeyID: 48185204
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f2f381e73d8da33e1347ccc81e7b0d98270827d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446972"
---
# <a name="manage-add-ins"></a><span data-ttu-id="cb2ec-103">Administrar complementos</span><span class="sxs-lookup"><span data-stu-id="cb2ec-103">Manage add-ins</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb2ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb2ec-104">

<span> </span></span></span>

<span data-ttu-id="cb2ec-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="cb2ec-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="cb2ec-106">Para crear un nuevo complemento de servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="cb2ec-106">To create a new Persistent Chat Server Add-in</span></span>

    New-CsPersistentChatAddin -Name Contoso -PersistentChatPoolFqdn client.contoso.com -Url http://contoso.com 

<div>

## <a name="create-get-set-or-remove-an-add-in"></a><span data-ttu-id="cb2ec-107">Crear, obtener, establecer o quitar un complemento</span><span class="sxs-lookup"><span data-stu-id="cb2ec-107">Create, Get, Set, or Remove an Add-in</span></span>

<span data-ttu-id="cb2ec-108">Para crear un nuevo complemento</span><span class="sxs-lookup"><span data-stu-id="cb2ec-108">To create a new Add-in</span></span>

    New-CsPersistentChatAddin -PersistentChatPoolFqdn <String> -Name <String> -Url<String>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="cb2ec-109">La &lt; cadena PersistentChatPoolFqdn &gt; solo se requiere si hay más de un grupo de servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="cb2ec-109">PersistentChatPoolFqdn &lt;String&gt; is required only if there is more than one Persistent Chat Server pool.</span></span>



</div>

<span data-ttu-id="cb2ec-110">Para obtener un complemento</span><span class="sxs-lookup"><span data-stu-id="cb2ec-110">To get an Add-in</span></span>

    Get-CsPersistentChatAddin -Identity <String>]

<span data-ttu-id="cb2ec-111">o</span><span class="sxs-lookup"><span data-stu-id="cb2ec-111">or</span></span>

    Get-CsPersistentChatAddin -PersistentChatPoolFqdn <String>

<span data-ttu-id="cb2ec-112">Para establecer un complemento</span><span class="sxs-lookup"><span data-stu-id="cb2ec-112">To set an Add-in</span></span>

    Set-CsPersistentChatAddIn -Instance <AddinObject> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="cb2ec-113">o</span><span class="sxs-lookup"><span data-stu-id="cb2ec-113">or</span></span>

    Set-CsPersistentChatAddIn -Identity <String> [-Name <String>] [-Url<String>] [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="cb2ec-114">Para quitar un complemento</span><span class="sxs-lookup"><span data-stu-id="cb2ec-114">To remove an Add-in</span></span>

    Remove-CsPersistentChatAddIn -Instance <AddinObject> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="cb2ec-115">o</span><span class="sxs-lookup"><span data-stu-id="cb2ec-115">or</span></span>

    Remove-CsPersistentChatAddIn -Identity <String> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="cb2ec-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb2ec-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

