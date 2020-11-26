---
title: 'Lync Server 2013: Eliminar un salón de chat o una categoría'
description: 'Lync Server 2013: eliminar una categoría o un salón de chat.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting a chat room or category
ms:assetid: adccb869-0015-4eba-ac73-718bac7843b5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215881(v=OCS.15)
ms:contentKeyID: 48706009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3ef89802171a1eeca7de18ff0a4eb8eb3895f1b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430416"
---
# <a name="deleting-a-chat-room-or-category-in-lync-server-2013"></a><span data-ttu-id="be07a-103">Eliminar un salón de chat o una categoría en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be07a-103">Deleting a chat room or category in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be07a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be07a-104">

<span> </span></span></span>

<span data-ttu-id="be07a-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="be07a-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="be07a-106">Se pueden eliminar los salones de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="be07a-106">Persistent Chat rooms can be deleted.</span></span> <span data-ttu-id="be07a-107">Si tiene un salón de chat que ya no se usa, puede deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="be07a-107">If you have a chat room that is no longer being used, you can disable it.</span></span> <span data-ttu-id="be07a-108">Para obtener más información, vea [deshabilitar o habilitar un salón de chat en Lync Server 2013](lync-server-2013-disabling-or-enabling-a-chat-room.md).</span><span class="sxs-lookup"><span data-stu-id="be07a-108">For details, see [Disabling or enabling a chat room in Lync Server 2013](lync-server-2013-disabling-or-enabling-a-chat-room.md).</span></span>

<span data-ttu-id="be07a-109">Un administrador de chat persistente puede consultar salones de chat desactivados y, de forma periódica, purgar y eliminar de forma permanente los salones de chat, mediante el cmdlet de Windows PowerShell, **Remove-CsPersistentChatRoom**.</span><span class="sxs-lookup"><span data-stu-id="be07a-109">A Persistent Chat administrator can query for disabled chat rooms, and can periodically purge and permanently delete the chat rooms, by using the Windows PowerShell cmdlet, **Remove-CsPersistentChatRoom**.</span></span>

<span data-ttu-id="be07a-110">Las categorías se pueden eliminar.</span><span class="sxs-lookup"><span data-stu-id="be07a-110">Categories can be deleted.</span></span> <span data-ttu-id="be07a-111">Sin embargo, para eliminar una categoría, primero debes eliminar todos los salones de chat que haya debajo o mover los salones de chat a una nueva categoría, dejando una categoría vacía para eliminarla.</span><span class="sxs-lookup"><span data-stu-id="be07a-111">However, to delete a category, you must first either delete all chat rooms under it or move the chat rooms to a new category, leaving an empty category for deletion.</span></span> <span data-ttu-id="be07a-112">El servidor de chat persistente no le permite eliminar una categoría que contiene salones de chat.</span><span class="sxs-lookup"><span data-stu-id="be07a-112">Persistent Chat Server does not allow you to delete a category that contains chat rooms.</span></span> <span data-ttu-id="be07a-113">Para obtener más información, vea [mover un salón de chat de una categoría a otra en Lync Server 2013](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="be07a-113">For details, see [Moving a chat room from one category to another in Lync Server 2013](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md).</span></span>

<span data-ttu-id="be07a-114">Para obtener detalles acerca de cómo eliminar categorías vacías mediante la interfaz de línea de comandos de Windows PowerShell, consulte "administración de salas" en [configurar el servidor de chat persistente mediante cmdlets de Windows PowerShell](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="be07a-114">For details about deleting empty categories by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span>

<span data-ttu-id="be07a-115">Para obtener más información sobre los salones de chat y las categorías, consulte [configurar salas en Lync server 2013](lync-server-2013-configure-rooms.md) y [configurar categorías en Lync Server 2013](lync-server-2013-configure-categories.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="be07a-115">For details about chat rooms and categories, see [Configure rooms in Lync Server 2013](lync-server-2013-configure-rooms.md) and [Configure categories in Lync Server 2013](lync-server-2013-configure-categories.md) in the Deployment documentation.</span></span>

<span data-ttu-id="be07a-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be07a-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

