---
title: 'Lync Server 2013: regiones de red'
description: 'Lync Server 2013: regiones de red.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Network regions
ms:assetid: 1818e9d2-bbb7-420a-93ea-4c3da3a55ad3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687979(v=OCS.15)
ms:contentKeyID: 49733567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3506f3c543c0728f27bd091b9cd63991c4633da7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425166"
---
# <a name="network-regions-in-lync-server-2013"></a><span data-ttu-id="d993f-103">Regiones de red de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d993f-103">Network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d993f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d993f-104">

<span> </span></span></span>

<span data-ttu-id="d993f-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="d993f-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="d993f-106">Las *regiones de red* son los concentradores de red o las redes troncales que se usan en la configuración de control de admisión de llamadas, E9-1-1 y omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="d993f-106">*Network regions* are the network hubs or backbones used in the configuration of call admission control, E9-1-1, and media bypass.</span></span> <span data-ttu-id="d993f-107">Use los procedimientos siguientes para ver, crear o modificar regiones de red.</span><span class="sxs-lookup"><span data-stu-id="d993f-107">Use the following procedures to view, create, or modify network regions.</span></span> <span data-ttu-id="d993f-108">Por ejemplo, si ya ha creado regiones de red para una característica de voz, no es necesario crear regiones de red nuevas; otras características avanzadas de telefonía empresarial usarán esas mismas regiones de red.</span><span class="sxs-lookup"><span data-stu-id="d993f-108">For example, if you have already created network regions for one Voice feature, you do not need to create new network regions; other advanced Enterprise Voice features will use those same network regions.</span></span> <span data-ttu-id="d993f-109">Sin embargo, es posible que necesite modificar una definición de región de red existente para aplicar una configuración específica de una característica.</span><span class="sxs-lookup"><span data-stu-id="d993f-109">You may, however, need to modify an existing network region definition to apply feature-specific settings.</span></span> <span data-ttu-id="d993f-110">Por ejemplo, si ha creado regiones de red para E9-1-1 (que no requieren un sitio central asociado) y, a continuación, implementa el control de admisión de llamadas, debe modificar las definiciones de región de red para especificar un sitio central.</span><span class="sxs-lookup"><span data-stu-id="d993f-110">For example, if you have created network regions for E9-1-1 (which do not require an associated central site) and you then deploy call admission control, you need to modify the network region definitions to specify a central site.</span></span> <span data-ttu-id="d993f-111">Para obtener más información, vea [configurar regiones de red para CAC en Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span><span class="sxs-lookup"><span data-stu-id="d993f-111">For details, see [Configure network regions for CAC in Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d993f-112">En los temas de implementación de la característica se documentan los requisitos específicos de las características de las definiciones de regiones de red.</span><span class="sxs-lookup"><span data-stu-id="d993f-112">Any feature-specific requirements for network region definitions are documented in the Deployment topics for the feature.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d993f-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d993f-113">In This Section</span></span>

  - [<span data-ttu-id="d993f-114">Ver información de la región de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d993f-114">Viewing network region information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-region-information.md)

  - [<span data-ttu-id="d993f-115">Crear o modificar regiones de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d993f-115">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)

  - [<span data-ttu-id="d993f-116">Eliminar regiones de red existentes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d993f-116">Deleting existing network regions in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-regions.md)

</div>

<div>

## <a name="reference"></a><span data-ttu-id="d993f-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="d993f-117">Reference</span></span>

[<span data-ttu-id="d993f-118">Implementación de características avanzadas de telefonía empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d993f-118">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

<span data-ttu-id="d993f-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d993f-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

