---
title: 'Lync Server 2013: grabación de detalles de llamadas (CDR)'
description: 'Lync Server 2013: grabación de detalles de llamadas (CDR).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call detail recording (CDR)
ms:assetid: 67726075-c77c-4191-a64f-a1cf5c7bcbb2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688079(v=OCS.15)
ms:contentKeyID: 49733675
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 590f99fd0b8649ffb3c4df039488dc54a8f3b7b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435778"
---
# <a name="call-detail-recording-cdr-in-lync-server-2013"></a><span data-ttu-id="26c4c-103">Grabación de detalles de llamadas (CDR) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26c4c-103">Call detail recording (CDR) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26c4c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26c4c-104">

<span> </span></span></span>

<span data-ttu-id="26c4c-105">_**Última modificación del tema:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="26c4c-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="26c4c-106">El registro detallado de llamadas (CDR) registra la información de uso y diagnóstico sobre actividades punto a punto, como la mensajería instantánea, las llamadas de voz sobre IP (VoIP), el uso compartido de aplicaciones, la transferencia de archivos y las reuniones.</span><span class="sxs-lookup"><span data-stu-id="26c4c-106">Call detail recording (CDR) records usage and diagnostic information about peer-to-peer activities, including instance messaging, Voice over Internet Protocol (VoIP) calls, application sharing, file transfer, and meetings.</span></span> <span data-ttu-id="26c4c-107">Los datos de uso pueden servir para calcular el rendimiento de la inversión y los datos de diagnóstico se pueden emplear para solucionar problemas de reuniones y actividades punto a punto.</span><span class="sxs-lookup"><span data-stu-id="26c4c-107">The usage data can be used to calculate return on investment (ROI) and the diagnostic data can be used to troubleshoot peer-to-peer activities and meetings.</span></span> <span data-ttu-id="26c4c-108">Al instalar Lync Server 2013, también instalará una colección predefinida de opciones de configuración global para CDR.</span><span class="sxs-lookup"><span data-stu-id="26c4c-108">When you install Lync Server 2013, you will also install a predefined collection of global configuration settings for CDR.</span></span> <span data-ttu-id="26c4c-109">Use los temas de esta sección para configurar CDR.</span><span class="sxs-lookup"><span data-stu-id="26c4c-109">Use the topics in this section to configure CDR.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="26c4c-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="26c4c-110">In This Section</span></span>

  - [<span data-ttu-id="26c4c-111">Ver la información de configuración de CDR en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26c4c-111">View CDR configuration information in Lync Server 2013</span></span>](lync-server-2013-view-cdr-configuration-information.md)

  - [<span data-ttu-id="26c4c-112">Habilitar la grabación de detalles de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26c4c-112">Enable call detail recording in Lync Server 2013</span></span>](lync-server-2013-enable-call-detail-recording.md)

  - [<span data-ttu-id="26c4c-113">Crear o modificar una colección de opciones de configuración de CDR en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26c4c-113">Create or modify a collection of CDR configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-cdr-configuration-settings.md)

  - [<span data-ttu-id="26c4c-114">Eliminar una colección existente de opciones de configuración de CDR en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26c4c-114">Delete an existing collection of CDR configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-cdr-configuration-settings.md)

  - [<span data-ttu-id="26c4c-115">Purgar manualmente las bases de datos de grabación de detalles de llamadas y de calidad de la experiencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26c4c-115">Manually purging the call detail recording and Quality of Experience databases in Lync Server 2013</span></span>](lync-server-2013-manually-purging-the-call-detail-recording-and-quality-of-experience-databases.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="26c4c-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="26c4c-116">See Also</span></span>


[<span data-ttu-id="26c4c-117">Configuración de la grabación de detalles de llamadas y la configuración de la calidad de la experiencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26c4c-117">Configuring call detail recording and Quality of Experience settings in Lync Server 2013</span></span>](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md)  
  

<span data-ttu-id="26c4c-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26c4c-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

