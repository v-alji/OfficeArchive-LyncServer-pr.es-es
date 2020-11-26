---
title: 'Lync Server 2013: servidores perimetrales de audio/vídeo (A/V)'
description: 'Lync Server 2013: servidores perimetrales de audio/vídeo (A/V).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Audio/Video (A/V) Edge Servers
ms:assetid: b0cc538b-77eb-47fb-be82-5ab0631c6219
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721852(v=OCS.15)
ms:contentKeyID: 49733785
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d5aefd4516540485b84ba0eb80f1a809d89eba0e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438242"
---
# <a name="audiovideo-av-edge-servers-in-lync-server-2013"></a><span data-ttu-id="b24f3-103">Servidores perimetrales de audio y vídeo (A/V) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b24f3-103">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b24f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b24f3-104">

<span> </span></span></span>

<span data-ttu-id="b24f3-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="b24f3-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="b24f3-106">El servicio perimetral A/V proporciona a los usuarios internos (los usuarios que han iniciado sesión en la red de la organización) una forma de compartir audio y vídeo con usuarios externos (usuarios que no han iniciado sesión en la red de su organización).</span><span class="sxs-lookup"><span data-stu-id="b24f3-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="b24f3-107">Además de audio y vídeo, el servicio perimetral A/V también proporciona soporte técnico para el uso compartido del escritorio y la transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="b24f3-107">In addition to audio and video, the A/V Edge service also provides support for such things desktop sharing and file transfer.</span></span>

<span data-ttu-id="b24f3-108">El servicio perimetral A/V se administra principalmente mediante la configuración A/V Edge; Esta configuración le permite administrar la cantidad máxima de ancho de banda que se va a asignar por puerto y por usuario, y especificar la cantidad de tiempo que se puede usar un token de autenticación antes de que se renueve ese token.</span><span class="sxs-lookup"><span data-stu-id="b24f3-108">The A/V Edge service is primarily managed by using A/V Edge configuration; these settings enable you to manage the maximum amount of bandwidth to be allocated per port and per user, and to specify the length of time that an authentication token can be used before that token must be renewed.</span></span> <span data-ttu-id="b24f3-109">La configuración del borde a/V puede aplicarse a sitios o a servidores perimetrales individuales a/V.</span><span class="sxs-lookup"><span data-stu-id="b24f3-109">A/V Edge configuration settings can be applied to sites or to individual A/V Edge servers.</span></span> <span data-ttu-id="b24f3-110">Cuando determine qué colección de configuraciones tendrá prioridad, use la siguiente guía:</span><span class="sxs-lookup"><span data-stu-id="b24f3-110">When determining which collection of settings will take priority, use the following guide:</span></span>

  - <span data-ttu-id="b24f3-111">La configuración establecida en el ámbito del servicio (es decir, en un servidor individual) tiene prioridad sobre todo.</span><span class="sxs-lookup"><span data-stu-id="b24f3-111">Settings configured at the service scope (that is, on an individual server) take priority over everything.</span></span>

  - <span data-ttu-id="b24f3-112">La configuración establecida en el ámbito del sitio tiene prioridad sobre la configuración establecida en el ámbito global.</span><span class="sxs-lookup"><span data-stu-id="b24f3-112">Settings configured at the site scope take priority over settings configured at the global scope.</span></span> <span data-ttu-id="b24f3-113">Sin embargo, la configuración del ámbito del servicio también reemplaza la configuración del ámbito del sitio.</span><span class="sxs-lookup"><span data-stu-id="b24f3-113">However, service scope settings will also supersede site-scope settings.</span></span>

  - <span data-ttu-id="b24f3-114">La configuración del ámbito global se usará solo si no hay ninguna configuración de servicio establecida en el servidor individual y no hay configuración de sitio para el sitio en el que se encuentra el servidor.</span><span class="sxs-lookup"><span data-stu-id="b24f3-114">Settings at the global scope will be used only if there are no service settings configured on the individual server and if there are no site settings for the site where that server is located.</span></span>

<span data-ttu-id="b24f3-115">El servicio perimetral de A/V solo se puede administrar con Lync Server PowerShell y los cmdlets CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b24f3-115">The A/V Edge service can only be managed by using Lync Server PowerShell and the CsAVEdgeConfiguration cmdlets.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b24f3-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b24f3-116">In This Section</span></span>

  - [<span data-ttu-id="b24f3-117">Devolver información de configuración del servidor perimetral A/V en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b24f3-117">Return A/V Edge Server configuration information in Lync Server 2013</span></span>](lync-server-2013-return-a-v-edge-server-configuration-information.md)

  - [<span data-ttu-id="b24f3-118">Crear o modificar una colección de valores de configuración del servidor perimetral A/V en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b24f3-118">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)

  - [<span data-ttu-id="b24f3-119">Eliminar una colección existente de valores de configuración del servidor perimetral A/V en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b24f3-119">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-a-v-edge-server-configuration-settings.md)

<span data-ttu-id="b24f3-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b24f3-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

