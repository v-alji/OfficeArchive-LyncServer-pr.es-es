---
title: 'Lync Server 2013: administración de llamadas a números no asignados'
description: 'Lync Server 2013: administración de llamadas a números no asignados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing calls to unassigned numbers
ms:assetid: a45a7546-5ee6-4c1e-ab13-20a71a058f80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688167(v=OCS.15)
ms:contentKeyID: 49733772
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a91c1ec30ea1e942fa3ea27fbcd369572884a52a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399120"
---
# <a name="managing-calls-to-unassigned-numbers-in-lync-server-2013"></a><span data-ttu-id="aca05-103">Administración de llamadas a números no asignados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aca05-103">Managing calls to unassigned numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aca05-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aca05-104">

<span> </span></span></span>

<span data-ttu-id="aca05-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="aca05-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="aca05-106">Lync Server le permite configurar el control de las llamadas telefónicas entrantes cuando el número marcado es válido para su organización, pero no está asignado a un usuario o teléfono.</span><span class="sxs-lookup"><span data-stu-id="aca05-106">Lync Server lets you configure the handling of incoming phone calls when the dialed number is valid for your organization, but is not assigned to a user or phone.</span></span> <span data-ttu-id="aca05-107">Puede usar la aplicación de anuncios para transferir estas llamadas a un destino predeterminado (número de teléfono, URI del SIP o correo de voz), o reproducir un anuncio de audio o ambos.</span><span class="sxs-lookup"><span data-stu-id="aca05-107">You can use the Announcement application to transfer these calls to a predetermined destination (phone number, SIP URI, or voice mail), or play an audio announcement, or both.</span></span> <span data-ttu-id="aca05-108">También puedes transferir estas llamadas a un número de teléfono de operador automático de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="aca05-108">You can also transfer these calls to an Exchange UM Auto Attendant phone number.</span></span> <span data-ttu-id="aca05-109">Controlar las llamadas a números no asignados de una de estas maneras le ayuda a evitar las situaciones en las que una persona que llama marca y escucha un tono de ocupado, o el cliente SIP recibe un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="aca05-109">Handling calls to unassigned numbers in one of these ways helps you avoid the situations in which a caller misdials and then hears a busy tone, or the SIP client receives an error message.</span></span>

<span data-ttu-id="aca05-110">En esta sección se describe cómo administrar intervalos numéricos no asignados para controlar llamadas a números de teléfono sin asignar.</span><span class="sxs-lookup"><span data-stu-id="aca05-110">This section describes how to manage unassigned number ranges to handle calls to unassigned phone numbers.</span></span> <span data-ttu-id="aca05-111">En la sección también se describe cómo administrar los anuncios durante la recuperación de desastres si quiere esta funcionalidad durante una interrupción.</span><span class="sxs-lookup"><span data-stu-id="aca05-111">The section also describes how to manage Announcements during disaster recovery if you want this functionality during an outage.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="aca05-112">El manejo de números no asignados durante una interrupción es opcional.</span><span class="sxs-lookup"><span data-stu-id="aca05-112">Using unassigned number handling during an outage is optional.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="aca05-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="aca05-113">In This Section</span></span>

  - [<span data-ttu-id="aca05-114">Crear un anuncio en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aca05-114">Create an announcement in Lync Server 2013</span></span>](lync-server-2013-create-an-announcement.md)

  - [<span data-ttu-id="aca05-115">Configurar números de teléfono sin asignar en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aca05-115">Configure unassigned phone numbers in Lync Server 2013</span></span>](lync-server-2013-configure-unassigned-phone-numbers.md)

  - [<span data-ttu-id="aca05-116">Administrar anuncios durante la recuperación ante desastres en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aca05-116">Manage announcements during disaster recovery in Lync Server 2013</span></span>](lync-server-2013-manage-announcements-during-disaster-recovery.md)

<span data-ttu-id="aca05-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aca05-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

