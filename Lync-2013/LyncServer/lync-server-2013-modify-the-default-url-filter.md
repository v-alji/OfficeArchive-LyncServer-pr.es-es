---
title: 'Lync Server 2013: modificar el filtro de dirección URL predeterminado'
description: 'Lync Server 2013: modifique el filtro de dirección URL predeterminado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the default URL filter
ms:assetid: 80a472b3-054e-45a6-80fc-9ee2bda28ee6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182544(v=OCS.15)
ms:contentKeyID: 48184653
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 079fcc83cd9041f99f1d14663ad51e86f6c23619
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445711"
---
# <a name="modify-the-default-url-filter-in-lync-server-2013"></a><span data-ttu-id="8b4e7-103">Modificar el filtro de dirección URL predeterminado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b4e7-103">Modify the default URL filter in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b4e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b4e7-104">

<span> </span></span></span>

<span data-ttu-id="8b4e7-105">_**Última modificación del tema:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="8b4e7-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="8b4e7-106">Al usar el filtro de mensajería instantánea (mi), Lync Server 2013 proporciona un filtro de URL global que bloquea las direcciones URL específicas contenidas en las conversaciones de mensajería instantánea entre los usuarios de toda la implementación de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8b4e7-106">By using the instant messaging (IM) filter, Lync Server 2013 provides a global URL filter that blocks specific URLs contained in IM conversations among users throughout your Lync Server 2013 deployment.</span></span> <span data-ttu-id="8b4e7-107">Mediante el panel de control de Lync Server, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8b4e7-107">By using Lync Server Control Panel, you can do the following:</span></span>

  - <span data-ttu-id="8b4e7-108">Bloquear todo o un subconjunto de direcciones URL en conversaciones de mensajes instantáneos.</span><span class="sxs-lookup"><span data-stu-id="8b4e7-108">Block all or a subset of URLs in instant message conversations.</span></span>

  - <span data-ttu-id="8b4e7-109">Permitir todas las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="8b4e7-109">Allow all URLs.</span></span> <span data-ttu-id="8b4e7-110">Como opción, puede crear un aviso que se inserte al principio de cada mensaje instantáneo que contenga una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="8b4e7-110">As an option, you can create a notice that is inserted at the beginning of each instant message that contains a URL.</span></span>

  - <span data-ttu-id="8b4e7-111">Permitir direcciones URL específicas e incluir una advertencia con cada mensaje instantáneo que contenga una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="8b4e7-111">Allow specific URLs and include a warning with each instant message that contains a URL.</span></span>

<span data-ttu-id="8b4e7-112">Además, puede elegir bloquear las direcciones URL que contienen determinados tipos de archivo o bloquear solo las direcciones URL de Internet permitiendo que las direcciones URL que se encuentran dentro de la zona de Intranet local del servidor (direcciones URL de la intranet) pasen a través del servidor.</span><span class="sxs-lookup"><span data-stu-id="8b4e7-112">In addition, you can choose to block URLs that contain specific file types, or block only Internet URLs by allowing URLs that are within the server’s local intranet zone — intranet URLs — to pass through the server.</span></span> <span data-ttu-id="8b4e7-113">Para obtener más información sobre el filtrado de URL, consulte [configuración de la transferencia de archivos y filtrado de URL para mensajería instantánea (mi) en Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span><span class="sxs-lookup"><span data-stu-id="8b4e7-113">For details about URL filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="8b4e7-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b4e7-114">See Also</span></span>


[<span data-ttu-id="8b4e7-115">Configuración de la transferencia de archivos y el filtrado de URL para mensajería instantánea (mi) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b4e7-115">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="8b4e7-116">Crear un filtro de transferencia de archivos nuevo en Lync Server 2013 para un sitio específico</span><span class="sxs-lookup"><span data-stu-id="8b4e7-116">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)  
[<span data-ttu-id="8b4e7-117">Crear un filtro de dirección URL en Lync Server 2013 para administrar hipervínculos en conversaciones de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="8b4e7-117">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)  
[<span data-ttu-id="8b4e7-118">Modificar el filtro de transferencia de archivos predeterminado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b4e7-118">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)  
  

<span data-ttu-id="8b4e7-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b4e7-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

