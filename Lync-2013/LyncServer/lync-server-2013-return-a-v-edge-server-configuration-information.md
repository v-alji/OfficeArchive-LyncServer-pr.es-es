---
title: 'Lync Server 2013: devolver información de configuración del servidor perimetral A/V'
description: 'Lync Server 2013: devuelva la información de configuración del servidor perimetral A/V.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Return A/V Edge Server configuration information
ms:assetid: b041f5a4-2387-4075-846c-ec4f99640903
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721850(v=OCS.15)
ms:contentKeyID: 49733783
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4f72fccfe51b946dc0dc285aee12a07e59c844b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442477"
---
# <a name="return-av-edge-server-configuration-information-in-lync-server-2013"></a><span data-ttu-id="ddf83-103">Devolver información de configuración del servidor perimetral A/V en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddf83-103">Return A/V Edge Server configuration information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ddf83-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ddf83-104">

<span> </span></span></span>

<span data-ttu-id="ddf83-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="ddf83-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="ddf83-106">El servicio perimetral A/V proporciona a los usuarios internos (los usuarios que han iniciado sesión en la red de la organización) una forma de compartir audio y vídeo con usuarios externos (usuarios que no han iniciado sesión en la red de su organización).</span><span class="sxs-lookup"><span data-stu-id="ddf83-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="ddf83-107">El servicio perimetral A/V se administra principalmente usando la configuración de borde de A/V, la configuración que se puede configurar en el ámbito del sitio o en el ámbito del servicio (es decir, se puede configurar para un servidor perimetral de A/V individual).</span><span class="sxs-lookup"><span data-stu-id="ddf83-107">The A/V Edge service is primarily managed by using A/V Edge configuration settings, setting that can be configured at the site scope or at the service scope (that is, can be configured for an individual A/V Edge server).</span></span>

<span data-ttu-id="ddf83-108">Para obtener información sobre las opciones de configuración del borde A/V en uso en su organización, debe usar Windows PowerShell y el cmdlet Get-CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ddf83-108">To return information about the A/V Edge configuration settings in use in your organization, you must use Windows PowerShell and the Get-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="ddf83-109">Para obtener más información, consulte el tema de ayuda para el cmdlet [Get-CsAVEdgeConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAVEdgeConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="ddf83-109">For more information, see the help topic for the [Get-CsAVEdgeConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAVEdgeConfiguration) cmdlet.</span></span>

<span data-ttu-id="ddf83-110">La información devuelta desde el cmdlet Get-CsAVEdgeConfiguration tendrá un aspecto similar a este:</span><span class="sxs-lookup"><span data-stu-id="ddf83-110">Information returned from the Get-CsAVEdgeConfiguration cmdlet will look similar to this:</span></span>

    Identity              : Global
    MaxTokenLifetime      : 08:00:00
    MaxBandwidthPerUserKb : 10000
    MaxBandwidthPerPortKb : 3000

<div>

## <a name="to-return-information-for-all-your-av-edge-configuration-settings"></a><span data-ttu-id="ddf83-111">Para obtener información sobre todas las opciones de configuración del borde A/V</span><span class="sxs-lookup"><span data-stu-id="ddf83-111">To return information for all your A/V Edge configuration settings</span></span>

  - <span data-ttu-id="ddf83-112">El siguiente comando devuelve información acerca de todas las opciones de configuración de borde A/V que se usan actualmente en su organización:</span><span class="sxs-lookup"><span data-stu-id="ddf83-112">The following command returns information about all the A/V Edge configuration settings currently in use in your organization:</span></span>
    
        Get-CsAVEdgeConfiguration

</div>

<div>

## <a name="to-return-information-for-site-scoped-av-edge-configuration-settings"></a><span data-ttu-id="ddf83-113">Para devolver información para la configuración del borde a/V del ámbito de un sitio</span><span class="sxs-lookup"><span data-stu-id="ddf83-113">To return information for site-scoped A/V Edge configuration settings</span></span>

  - <span data-ttu-id="ddf83-114">Para obtener información sobre una colección específica de valores de configuración de borde A/V, especifique la identidad de esa colección al ejecutar el cmdlet Get-CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ddf83-114">To return information about a specific collection of A/V Edge configuration settings, specify the Identity of that collection when running the Get-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="ddf83-115">Por ejemplo, este comando devuelve información solo de la configuración que se aplica al sitio de Redmond:</span><span class="sxs-lookup"><span data-stu-id="ddf83-115">For example, this command returns information only for the settings applied to the Redmond site:</span></span>
    
        Get-CsAVEdgeConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-return-information-for-service-scoped-av-edge-configuration-settings"></a><span data-ttu-id="ddf83-116">Para devolver información para las opciones de configuración del borde a/V del ámbito de servicio</span><span class="sxs-lookup"><span data-stu-id="ddf83-116">To return information for service-scoped A/V Edge configuration settings</span></span>

  - <span data-ttu-id="ddf83-117">Y este comando solo devuelve información para la configuración que ha aplicado el servidor perimetral A/V específico:</span><span class="sxs-lookup"><span data-stu-id="ddf83-117">And this command returns information only for settings applied the a specific A/V Edge server:</span></span>
    
        Get-CsAVEdgeConfiguration -Identity "service:EdgeServer:atl-edge-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ddf83-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddf83-118">See Also</span></span>


[<span data-ttu-id="ddf83-119">Crear o modificar una colección de valores de configuración del servidor perimetral A/V en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddf83-119">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)  
[<span data-ttu-id="ddf83-120">Eliminar una colección existente de valores de configuración del servidor perimetral A/V en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddf83-120">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-a-v-edge-server-configuration-settings.md)  


[<span data-ttu-id="ddf83-121">Servidores perimetrales de audio y vídeo (A/V) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddf83-121">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>](lync-server-2013-audio-video-a-v-edge-servers.md)  
  

<span data-ttu-id="ddf83-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ddf83-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

