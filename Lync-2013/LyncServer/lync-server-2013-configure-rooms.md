---
title: 'Lync Server 2013: Configurar salones'
description: 'Lync Server 2013: configurar salas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure rooms
ms:assetid: 8956bd2c-c863-4704-bc65-5c0d83556258
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205067(v=OCS.15)
ms:contentKeyID: 48184750
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e9f5b2ece8cf436fe69c000da73871cb92686d82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399360"
---
# <a name="configure-rooms-in-lync-server-2013"></a><span data-ttu-id="44937-103">Configurar salones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="44937-103">Configure rooms in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="44937-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="44937-104">

<span> </span></span></span>

<span data-ttu-id="44937-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="44937-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="44937-106">La configuración de los salones de chat persistentes la controlan normalmente los usuarios u otros equipos centrales mediante la interfaz de línea de comandos de Windows PowerShell; por lo general, los administradores no administran salones de chat.</span><span class="sxs-lookup"><span data-stu-id="44937-106">Configuring Persistent Chat rooms is commonly handled by users or other central teams by using Windows PowerShell command-line interface; an administrator typically does not manage chat rooms.</span></span> <span data-ttu-id="44937-107">Sin embargo, si tiene que crear y administrar salones de chat, puede usar la interfaz de línea de comandos de Windows PowerShell o agregarse como miembro a un salón de chat y usar el cliente de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="44937-107">However, if you have to create and manage chat rooms, you can use the Windows PowerShell command-line interface, or add yourself as a member to a chat room and use the Lync 2013 client.</span></span>

<span data-ttu-id="44937-108">Para obtener detalles sobre la configuración de salones de chat con la interfaz de línea de comandos de Windows PowerShell, consulte "administración de salas" en [configurar el servidor de chat persistente mediante cmdlets de Windows PowerShell](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="44937-108">For details about configuring chat rooms by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span>

<div>

## <a name="managing-data-in-chat-rooms"></a><span data-ttu-id="44937-109">Administración de datos en salones de chat</span><span class="sxs-lookup"><span data-stu-id="44937-109">Managing Data in Chat Rooms</span></span>

<span data-ttu-id="44937-110">El servidor de chat persistente permite a los usuarios colaborar mediante la publicación de mensajes en salas de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="44937-110">Persistent Chat Server lets users collaborate by posting messages into Persistent Chat rooms.</span></span> <span data-ttu-id="44937-111">Los datos se conservan en el servidor y los miembros de la sala pueden tener acceso a los datos, incluidos los datos históricos.</span><span class="sxs-lookup"><span data-stu-id="44937-111">The data is persisted on the server, and members of the room can have access to the data, including historical data.</span></span> <span data-ttu-id="44937-112">Sin embargo, los usuarios con diferentes roles tienen acceso diferente a los datos persistentes, como se describe en la siguiente lista.</span><span class="sxs-lookup"><span data-stu-id="44937-112">However, users with different roles have different access to the persisted data, as outlined in the following list.</span></span>

  - <span data-ttu-id="44937-113">Los administradores pueden eliminar contenido antiguo (por ejemplo, contenido que fue publicado antes de una determinada fecha) de cualquier salón de chat para conservar la base de datos e impedir que crezca demasiado.</span><span class="sxs-lookup"><span data-stu-id="44937-113">Administrators can delete earlier content (for example, content that was posted before a certain date) from any chat room to keep the database from growing too large.</span></span> <span data-ttu-id="44937-114">O bien, pueden quitar o reemplazar mensajes que se consideren inapropiados para un salón de chat en particular.</span><span class="sxs-lookup"><span data-stu-id="44937-114">Or, they can remove or replace messages that are considered inappropriate for a particular chat room.</span></span>

  - <span data-ttu-id="44937-115">Los usuarios finales, incluidos los autores de los mensajes, no pueden eliminar contenido de ningún salón de chat.</span><span class="sxs-lookup"><span data-stu-id="44937-115">End users, including message authors, cannot delete content from any chat room.</span></span>

  - <span data-ttu-id="44937-116">Los administradores de salones de chat pueden deshabilitar salas, pero no pueden eliminar salas.</span><span class="sxs-lookup"><span data-stu-id="44937-116">Chat room managers can disable rooms, but cannot delete rooms.</span></span> <span data-ttu-id="44937-117">Solo los administradores pueden eliminar un salón de chat una vez que se ha creado.</span><span class="sxs-lookup"><span data-stu-id="44937-117">Only administrators can delete a chat room after it has been created.</span></span>

<span data-ttu-id="44937-118">Cuando se elimina un mensaje, no se puede deshacer la acción.</span><span class="sxs-lookup"><span data-stu-id="44937-118">When a message is deleted, you cannot undo the action.</span></span> <span data-ttu-id="44937-119">Sin embargo, los mensajes eliminados se pueden restaurar si hay una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="44937-119">However, deleted messages can be restored if there is a backup.</span></span> <span data-ttu-id="44937-120">Si un servidor de cumplimiento de chat persistente está habilitado, los mensajes antiguos se conservan en la base de datos de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="44937-120">If a Persistent Chat Compliance server is enabled, old messages are persisted in the compliance database.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="44937-121">Este uso de datos del salón de chat se aplica a Lync Server 2013, aplicación API de servidor de chat persistente, excepto en el caso de que intervenga el rol de administrador.</span><span class="sxs-lookup"><span data-stu-id="44937-121">This chat room data usage applies to the Lync Server 2013, Persistent Chat Server API application, except for the case when the administrator role is involved.</span></span> <span data-ttu-id="44937-122">La API del servidor de chat persistente no se puede usar para realizar ninguna de las operaciones del administrador.</span><span class="sxs-lookup"><span data-stu-id="44937-122">The Persistent Chat Server API cannot be used to do any of the administrator’s operations.</span></span> <span data-ttu-id="44937-123">Debe realizar estas operaciones en el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="44937-123">You must perform these operations in the Lync Server Management Shell.</span></span>



<span data-ttu-id="44937-124"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="44937-124"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

