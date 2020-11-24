---
title: 'Lync Server 2013: configuración de clientes para su uso con Office Web Apps Server'
description: 'Lync Server 2013: configuración de clientes para su uso con Office Web Apps Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring clients for use with Office Web Apps Server
ms:assetid: e5eaead7-0b32-42fb-97eb-ca203af59a9d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205339(v=OCS.15)
ms:contentKeyID: 48185668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b9bd7cf1e76c481c40381234ba1a84cda5500dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399875"
---
# <a name="configuring-clients-of-lync-server-2013-for-use-with-office-web-apps-server"></a><span data-ttu-id="d0b19-103">Configuración de clientes de Lync Server 2013 para su uso con Office Web Apps Server</span><span class="sxs-lookup"><span data-stu-id="d0b19-103">Configuring clients of Lync Server 2013 for use with Office Web Apps Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d0b19-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d0b19-104">

<span> </span></span></span>

<span data-ttu-id="d0b19-105">_**Última modificación del tema:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="d0b19-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="d0b19-106">Si quiere que los usuarios experimenten todas las capacidades de Office Web App Server, debe actualizar esos usuarios a Microsoft Lync 2013. solo los usuarios de Lync 2013 podrán realizar tareas como desplazarse por las diapositivas de PowerPoint independientemente de la presentación real de PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="d0b19-106">If you want users to experience the full capabilities of Office Web App Server then you should upgrade those users to Microsoft Lync 2013; only users of Lync 2013 will be able to do such things as scroll through PowerPoint slides independent of the actual PowerPoint presentation.</span></span> <span data-ttu-id="d0b19-107">(Es decir, estos usuarios pueden ver cualquier diapositiva de la presentación en cualquier momento, sin interferir de ninguna manera con la presentación real). Los usuarios que no utilicen Lync 2013 seguirán pudiendo unirse a conferencias en línea y ver la presentación de PowerPoint. sin embargo, no podrán desplazarse independientemente por las diapositivas, ni podrán ver las transiciones de diapositivas ni ver los vídeos incrustados.</span><span class="sxs-lookup"><span data-stu-id="d0b19-107">(That is, these users can look at any slide in the presentation at any time, without interfering in any way with the actual presentation.) Users who are not using Lync 2013 will still be able to join online conferences and view the PowerPoint presentation; however, they will not be able to independently scroll through the slides, nor will they be able to see slide transitions or view embedded videos.</span></span>

<span data-ttu-id="d0b19-108">Tenga en cuenta que estas capacidades siempre estarán disponibles para los usuarios de Lync 2013. Esto es cierto incluso si el moderador de PowerPoint ejecuta Microsoft Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="d0b19-108">Note that these capabilities will always be available to users of Lync 2013; this is true even if the PowerPoint presenter is running Microsoft Lync 2010.</span></span> <span data-ttu-id="d0b19-109">Si un usuario que ejecuta Lync 2010 está hospedando una presentación de PowerPoint, Lync Server 2013 se coordinará con Office Web Apps Server para asegurarse de que los usuarios de Lync 2013 verán la versión de Office Web Apps Server de la presentación.</span><span class="sxs-lookup"><span data-stu-id="d0b19-109">If a PowerPoint presentation is being hosted by a user running Lync 2010, Lync Server 2013 will coordinate with Office Web Apps Server to make sure that Lync 2013 users will view the Office Web Apps Server version of that presentation.</span></span> <span data-ttu-id="d0b19-110">Office Web Apps Server no proporciona servicios de PowerPoint para los usuarios que ejecutan clientes distintos de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="d0b19-110">Office Web Apps Server does not provide PowerPoint services for users running clients other than Lync 2013.</span></span> <span data-ttu-id="d0b19-111">En su lugar, estos usuarios se conectan al servicio del servidor de conferencia y ven las presentaciones de PowerPoint de la misma manera que lo hacían en Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d0b19-111">Instead, those users connect to the Conferencing server service and view PowerPoint presentations the same way they did in Microsoft Lync Server 2010.</span></span> <span data-ttu-id="d0b19-112">Esto también significa que estos usuarios solo tendrán acceso a las funciones más limitadas que ofrece Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d0b19-112">This also means that these users will only have access to the more-limited capabilities offered by Lync Server 2010.</span></span>

<span data-ttu-id="d0b19-113">Aunque no se necesita ninguna configuración de cliente para Office Web Apps Server (aparte de la actualización de usuarios a Lync 2013), se recomienda que los asistentes a la Conferencia se actualicen a Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d0b19-113">Although no client configuration is required for Office Web Apps Server (other than upgrading users to Lync 2013), it is recommended that conference attendees be upgrade to Internet Explorer 9.</span></span> <span data-ttu-id="d0b19-114">A pesar de que se puede acceder a las conferencias con Internet Explorer 8, hay algunas limitaciones en el uso de ese explorador Web.</span><span class="sxs-lookup"><span data-stu-id="d0b19-114">Although conferences can be accessed using Internet Explorer 8, there are some limitations to using that Web browser.</span></span> <span data-ttu-id="d0b19-115">Por ejemplo, los usuarios de Internet Explorer 8 no podrán cambiar el tamaño de la fase de PowerPoint a un tamaño personalizado; en su lugar, se limitarán a usar uno de los tres tamaños de escenario predefinidos.</span><span class="sxs-lookup"><span data-stu-id="d0b19-115">For example, users of Internet Explorer 8 will not be able to resize the PowerPoint stage to a custom size; instead, they will be limited to using one of three predefined stage sizes.</span></span> <span data-ttu-id="d0b19-116">Del mismo modo, los usuarios de Internet Explorer 8 no podrán reproducir archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="d0b19-116">Likewise, Internet Explorer 8 users will not be able to play media files.</span></span>

<span data-ttu-id="d0b19-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d0b19-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

