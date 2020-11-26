---
title: Administrar salones
description: Administrar salas.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Manage rooms
ms:assetid: d4835cf4-cd09-4769-a08e-e92706861b64
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205292(v=OCS.15)
ms:contentKeyID: 48185505
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be093e14a68639fdde73b58936e1b2f5cf4424cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446159"
---
# <a name="manage-rooms"></a><span data-ttu-id="de999-103">Administrar salones</span><span class="sxs-lookup"><span data-stu-id="de999-103">Manage rooms</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de999-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de999-104">

<span> </span></span></span>

<span data-ttu-id="de999-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="de999-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="de999-106">Para crear un nuevo salón de servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="de999-106">To create a new Persistent Chat Server room</span></span>

    New-CsPersistentChatRoom -Name Foo1 -PersistentChatPoolFqdn client.contoso.com -Category client.contoso.com\Foo [other parameters]

<div>


> [!IMPORTANT]  
> <span data-ttu-id="de999-107">-PersistentChatPoolFqdn no es necesario si se cumple una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="de999-107">-PersistentChatPoolFqdn is not needed if one of the following is true:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="de999-108">Solo hay un grupo de servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="de999-108">There is only one Persistent Chat Server pool.</span></span></P>
> <LI>
> <P><span data-ttu-id="de999-109">Proporciona un FQDN del grupo de servidores a la categoría.</span><span class="sxs-lookup"><span data-stu-id="de999-109">You provide a pool FQDN to the category.</span></span></P>
> <LI>
> <P><span data-ttu-id="de999-110">Proporciona un FQDN del grupo de servidores para agregar el salón.</span><span class="sxs-lookup"><span data-stu-id="de999-110">You provide a pool FQDN to adding the room.</span></span></P></LI></UL>



</div>

<span data-ttu-id="de999-111">Para realizar cambios en una sala de servidores de chat persistente existente</span><span class="sxs-lookup"><span data-stu-id="de999-111">To make changes to an existing Persistent Chat Server room</span></span>

    Set-CsPersistentChatRoom -Identity testCat -Members @{Add="sip:user1@contoso.com", "CN=container,DC=contoso,DC=com"}
    Set-CsPersistentChatRoom -Identity testCat -Managers @{Add="sip:user2@contoso.com"}
    Set-CsPersistentChatRoom -Identity testCat -Presenters @{Add="sip:user1@contoso.com"}

<span data-ttu-id="de999-112">Windows PowerShell: los miembros, los administradores y los moderadores pueden establecerse de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="de999-112">Windows PowerShell: Members, Managers and Presenters can be set simultaneously.</span></span> <span data-ttu-id="de999-113">Todos deben ser el subconjunto de AllowedMembers menos DeniedMembers de la categoría de host.</span><span class="sxs-lookup"><span data-stu-id="de999-113">They all should be the subset of AllowedMembers minus DeniedMembers of the host Category.</span></span> <span data-ttu-id="de999-114">Un salón que es Type = normal no puede incluir moderadores.</span><span class="sxs-lookup"><span data-stu-id="de999-114">A room that is type=normal cannot include Presenters.</span></span>

<div>

## <a name="create-get-set-clear-or-remove-a-room"></a><span data-ttu-id="de999-115">Crear, obtener, establecer, borrar o quitar una sala</span><span class="sxs-lookup"><span data-stu-id="de999-115">Create, Get, Set, Clear, or Remove a Room</span></span>

<span data-ttu-id="de999-116">Para crear un nuevo salón</span><span class="sxs-lookup"><span data-stu-id="de999-116">To create a new room</span></span>

    New-CsPersistentChatRoom -Name <String> [-PersistentChatPoolFqdn <String>]-Category <String> [-Description <String>] [-Disabled <Switch Parameter>] [-Type <Normal | Auditorium>] [-AddIn <String>] [-Privacy <ChatRoomPrivacy> {Open | Closed | Secret}] [-Invitations <Switch Parameter>]

<span data-ttu-id="de999-117">Para establecer un salón</span><span class="sxs-lookup"><span data-stu-id="de999-117">To set a room</span></span>

    Set-CsPersistentChatRoom -Identity <String> [-Name <String>] [-Category <String>] [-Description <String>] [-Disabled <boolean>] [-Type <Normal | Auditorium>] [-AddIn <String>] [-Privacy <ChatRoomPrivacy> {Open | Closed | Secret}] [-Invitations <Enum>] [-Members <PSListModifier<String>>] [-Managers <PSListModifier<String>>] [-Presenters <PSListModifier<String>>] [-Force < Switch Parameter >] [-Confirm <Switch Parameter>][-WhatIf <Switch Parameter>]

<span data-ttu-id="de999-118">Para obtener un salón</span><span class="sxs-lookup"><span data-stu-id="de999-118">To get a room</span></span>

    Get-CsPersistentChatRoom -Identity <String>

<span data-ttu-id="de999-119">o</span><span class="sxs-lookup"><span data-stu-id="de999-119">or</span></span>

    Get-CsPersistentChatRoom -filter <String> [-PersistentChatPoolFqdn <String>] [-SearchDescription] [-Member <String>] [-Manager <string>] [-Category <string>] [-Addin <string>] [-Disabled <bool>] [-Privacy <ChatRoomPrivacy> {Open | Closed | Secret}] [-Type <ChatRoomType> {Normal | Auditorium}] [-Invitations <ChatRoomInvitations> {False | Inherit}] [-ChatContentExceedsMB <int>] [-ResultSize <int>]

<span data-ttu-id="de999-120">Dónde: filtrar solo admite nombre y descripción, y ayuda a buscar salas cuyo nombre/Descripción coincide con la cadena de palabra clave.</span><span class="sxs-lookup"><span data-stu-id="de999-120">where –filter supports only Name and Description and helps you find rooms whose Name/Description matches the keyword string.</span></span> <span data-ttu-id="de999-121">PoolFqdn busca en un grupo de servidores de chat persistente determinado.</span><span class="sxs-lookup"><span data-stu-id="de999-121">PoolFqdn searches in a given Persistent Chat Server pool.</span></span>

<span data-ttu-id="de999-122">Para borrar una sala y borrar los mensajes de una sala</span><span class="sxs-lookup"><span data-stu-id="de999-122">To clear a room and clear messages from a room</span></span>

    Clear-CsPersistentChatRoom [-Identity] <string> -EndDate <DateTime> [-WhatIf] [-Confirm]  [<CommonParameters>]

<span data-ttu-id="de999-123">o</span><span class="sxs-lookup"><span data-stu-id="de999-123">or</span></span>

    Clear-CsPersistentChatRoom [-Instance] <ChatRoomObject> -EndDate <DateTime> [-WhatIf] [-Confirm] [<CommonParameters>]

<span data-ttu-id="de999-124">Para quitar una sala</span><span class="sxs-lookup"><span data-stu-id="de999-124">To remove a room</span></span>

    Remove-CsPersistentChatRoom [-Identity] <string> [-Force] [-WhatIf] [-Confirm]  [<CommonParameters>]

<span data-ttu-id="de999-125">o</span><span class="sxs-lookup"><span data-stu-id="de999-125">or</span></span>

    Remove-CsPersistentChatRoom [-Instance] <ChatRoomObject> [-Force] [-WhatIf] [-Confirm]  [<CommonParameters>]

<span data-ttu-id="de999-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de999-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

