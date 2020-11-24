---
title: Configuración del servidor de chat persistente con cmdlets de Windows PowerShell
description: Configurar el servidor de chat persistente mediante cmdlets de Windows PowerShell.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configuring Persistent Chat Server by using Windows PowerShell cmdlets
ms:assetid: 4c1d1ad7-b6bd-476f-9c5b-f0c1756d5aa8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204877(v=OCS.15)
ms:contentKeyID: 48184089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39d97657684227ef3c36f6ac39389220a6805f82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398844"
---
# <a name="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="4dfd7-103">Configuración del servidor de chat persistente con cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4dfd7-103">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4dfd7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4dfd7-104">

<span> </span></span></span>

<span data-ttu-id="4dfd7-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="4dfd7-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="4dfd7-106">Use los siguientes cmdlets de Windows PowerShell para configurar la administración dentro de Lync Server 2013, el servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-106">Use the following Windows PowerShell cmdlets to configure management within Lync Server 2013, Persistent Chat Server.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4dfd7-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4dfd7-107">In This Section</span></span>

  - [<span data-ttu-id="4dfd7-108">Manage categories</span><span class="sxs-lookup"><span data-stu-id="4dfd7-108">Manage categories</span></span>](manage-categories.md)

  - [<span data-ttu-id="4dfd7-109">Administrar salones</span><span class="sxs-lookup"><span data-stu-id="4dfd7-109">Manage rooms</span></span>](manage-rooms.md)

  - [<span data-ttu-id="4dfd7-110">Administrar complementos</span><span class="sxs-lookup"><span data-stu-id="4dfd7-110">Manage add-ins</span></span>](manage-add-ins.md)

  - [<span data-ttu-id="4dfd7-111">Quitar un mensaje</span><span class="sxs-lookup"><span data-stu-id="4dfd7-111">Remove a message</span></span>](remove-a-message.md)

  - [<span data-ttu-id="4dfd7-112">Probar servidor de chat persistente con una transacción sintética</span><span class="sxs-lookup"><span data-stu-id="4dfd7-112">Test Persistent Chat Server with a synthetic transaction</span></span>](test-persistent-chat-server-with-a-synthetic-transaction.md)

  - [<span data-ttu-id="4dfd7-113">Ejecutar compatibilidad con versiones anteriores para servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="4dfd7-113">Run backward compatibility for Persistent Chat Server</span></span>](run-backward-compatibility-for-persistent-chat-server.md)

  - [<span data-ttu-id="4dfd7-114">Ejecutar, conceder, obtener, quitar o configurar directiva de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4dfd7-114">Run, grant, get, remove, or set Persistent Chat Policy in Lync Server 2013</span></span>](lync-server-2013-run-grant-get-remove-or-set-persistent-chat-policy.md)

  - [<span data-ttu-id="4dfd7-115">Configurar el servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4dfd7-115">Configure Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-configure-persistent-chat-server.md)

  - [<span data-ttu-id="4dfd7-116">Obtener disponibilidad de grupo de servidores de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4dfd7-116">Get Persistent Chat Server pool availability in Lync Server 2013</span></span>](lync-server-2013-get-persistent-chat-server-pool-availability.md)

  - [<span data-ttu-id="4dfd7-117">Cumplimiento de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4dfd7-117">Persistent Chat compliance in Lync Server 2013</span></span>](lync-server-2013-persistent-chat-compliance.md)

<span data-ttu-id="4dfd7-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4dfd7-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

