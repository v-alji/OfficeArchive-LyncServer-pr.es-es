---
title: 'Lync Server 2013: Administrar categorías, salones de chat y complementos'
description: 'Lync Server 2013: administración de categorías, salas y complementos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing categories, rooms, and add-ins
ms:assetid: a9807031-7369-4a51-9369-6f09bec24141
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412799(v=OCS.15)
ms:contentKeyID: 48185100
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba09ed3e021ba24f424d28bbb2c5c379ab975741
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425958"
---
# <a name="managing-categories-rooms-and-add-ins-in-lync-server-2013"></a><span data-ttu-id="bafc9-103">Administrar categorías, salones de chat y complementos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bafc9-103">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bafc9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bafc9-104">

<span> </span></span></span>

<span data-ttu-id="bafc9-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="bafc9-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="bafc9-106">En el panel de control de Lync Server 2013 o mediante cmdlets de Windows PowerShell, los administradores de chat persistentes pueden usar la página de **chat persistente** para crear categorías y complementos. Para administrar salones de chat persistentes, los administradores pueden usar cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bafc9-106">In Lync Server 2013 Control Panel, or by using Windows PowerShell cmdlets, Persistent Chat Administrators can use the **Persistent Chat** page to create categories and add-ins. For managing Persistent Chat rooms, Administrators can use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="bafc9-107">Como alternativa, si el administrador de chat persistente también está habilitado para SIP, puede usar el cliente de Lync para iniciar una página web para crear y administrar salones de chat.</span><span class="sxs-lookup"><span data-stu-id="bafc9-107">Alternatively, if the Persistent Chat administrator is also SIP-enabled, they can use the Lync client to launch a web page to create and manage chat rooms.</span></span>

<span data-ttu-id="bafc9-108">En los siguientes temas se describe cómo crear y trabajar con categorías y salones de chat.</span><span class="sxs-lookup"><span data-stu-id="bafc9-108">The following topics describe how to create and work with categories and chat rooms.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bafc9-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bafc9-109">In This Section</span></span>

  - [<span data-ttu-id="bafc9-110">Crear o editar una categoría nueva en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bafc9-110">Creating or editing a new category in Lync Server 2013</span></span>](lync-server-2013-creating-or-editing-a-new-category.md)

  - [<span data-ttu-id="bafc9-111">Crear o editar un salón de chat nuevo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bafc9-111">Creating or editing a new room in Lync Server 2013</span></span>](lync-server-2013-creating-or-editing-a-new-room.md)

  - [<span data-ttu-id="bafc9-112">Creación de complementos para salones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bafc9-112">Creating new add-ins for rooms in Lync Server 2013</span></span>](lync-server-2013-creating-new-add-ins-for-rooms.md)

  - [<span data-ttu-id="bafc9-113">Establecer quién puede enviar mensajes en un salón de chat de tipo auditorio en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bafc9-113">Setting who can post messages in an auditorium chat room in Lync Server 2013</span></span>](lync-server-2013-setting-who-can-post-messages-in-an-auditorium-chat-room.md)

  - [<span data-ttu-id="bafc9-114">Habilitar o deshabilitar un salón de chat en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bafc9-114">Disabling or enabling a chat room in Lync Server 2013</span></span>](lync-server-2013-disabling-or-enabling-a-chat-room.md)

  - [<span data-ttu-id="bafc9-115">Mover un salón de chat de una categoría a otra en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bafc9-115">Moving a chat room from one category to another in Lync Server 2013</span></span>](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md)

  - [<span data-ttu-id="bafc9-116">Eliminar un salón de chat o una categoría en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bafc9-116">Deleting a chat room or category in Lync Server 2013</span></span>](lync-server-2013-deleting-a-chat-room-or-category.md)

  - [<span data-ttu-id="bafc9-117">Eliminación de un mensaje o depuración de mensajes obsoletos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bafc9-117">Deleting a message or purging obsolete messages in Lync Server 2013</span></span>](lync-server-2013-deleting-a-message-or-purging-obsolete-messages.md)

<span data-ttu-id="bafc9-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bafc9-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

