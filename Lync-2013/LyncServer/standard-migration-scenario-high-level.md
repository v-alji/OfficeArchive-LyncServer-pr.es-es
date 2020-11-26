---
title: Escenario de migración estándar - Alto nivel
description: 'Escenario de migración estándar: alto nivel.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Standard migration scenario - high-level
ms:assetid: e768a7ca-44e3-4969-a6d9-7ed3e7029c5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205354(v=OCS.15)
ms:contentKeyID: 48185709
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a931b76e528b7e6468f6b7e7b9a718724d27501f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438760"
---
# <a name="standard-migration-scenario---high-level"></a><span data-ttu-id="72251-103">Escenario de migración estándar - Alto nivel</span><span class="sxs-lookup"><span data-stu-id="72251-103">Standard migration scenario - high-level</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="72251-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="72251-104">

<span> </span></span></span>

<span data-ttu-id="72251-105">_**Última modificación del tema:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="72251-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="72251-106">Use los siguientes elementos como punto de partida al migrar Lync Server 2010, chat grupal u Office Communications Server 2007 R2 chat grupal a Lync Server 2013, servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="72251-106">Use the following items as a starting point when migrating Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="72251-107">La ruta de migración estándar de Lync Server 2013 es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="72251-107">The standard Lync Server 2013 migration path is as follows:</span></span>

  - <span data-ttu-id="72251-108">Su organización ha implementado previamente Lync Server 2010, chat grupal o chat grupal de Office Communications Server 2007 R2 y desea implementar Lync Server 2013, servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="72251-108">Your organization has previously deployed Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat, and you want to deploy Lync Server 2013, Persistent Chat Server.</span></span>

  - <span data-ttu-id="72251-109">Implemente Lync Server 2013 y, a continuación, implemente grupos de servidores de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="72251-109">Deploy Lync Server 2013, and then deploy Persistent Chat Server pool(s).</span></span>

  - <span data-ttu-id="72251-110">Prepare y planifique la migración de sus salones de chat persistentes y determine el momento adecuado para apagar el sistema para la migración.</span><span class="sxs-lookup"><span data-stu-id="72251-110">Prepare and plan for migration of your Persistent Chat rooms, and determine an appropriate time to shut down the system for migration.</span></span>

  - <span data-ttu-id="72251-111">Ejecute los cmdlets de Windows PowerShell para la migración (**Export-CsPersistentChatData** e **Import-CsPersistentChatData**) para mover el contenido a un servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="72251-111">Run the Windows PowerShell cmdlets for migration (**Export-CsPersistentChatData** and **Import-CsPersistentChatData**) to move content to Persistent Chat Server.</span></span>

  - <span data-ttu-id="72251-112">Comprobar que la migración se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="72251-112">Verify that migration has succeeded.</span></span>

  - <span data-ttu-id="72251-113">Dar de baja la implementación heredada.</span><span class="sxs-lookup"><span data-stu-id="72251-113">Decommission your legacy deployment.</span></span>

  - <span data-ttu-id="72251-114">Configure el servidor de chat persistente para que los clientes heredados puedan conectarse a Lync Server 2013, servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="72251-114">Configure Persistent Chat Server so that legacy clients can connect to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="72251-115">Esto es necesario porque lleva tiempo implementar nuevos clientes y quiere permitir que los usuarios existentes con clientes heredados tengan acceso a sus salones de chat tan pronto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="72251-115">This is necessary because it takes time to deploy new clients, and you want to enable existing users with legacy clients to have access to their chat rooms as soon as possible.</span></span>

  - <span data-ttu-id="72251-116">Implemente nuevos clientes y siga ayudando a garantizar que los trabajadores con chat grupal heredado (clientes) puedan acceder a sus salones de chat.</span><span class="sxs-lookup"><span data-stu-id="72251-116">Deploy new clients, while continuing to help ensure that workers with legacy Group Chat (clients) can get to their chat rooms.</span></span>

<span data-ttu-id="72251-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="72251-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

