---
title: 'Lync Server 2013: problemas y indicadores de estado de claves'
description: 'Lync Server 2013: problemas y indicadores de estado de claves.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Troubleshooting and Key Health Indicators
ms:assetid: 14ec9e21-aa2b-4d65-9be4-ef2adfbe9a8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720322(v=OCS.15)
ms:contentKeyID: 63969585
ms.date: 05/18/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8fdb214d4ce8472800272a05e81b0402d3bf820e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436219"
---
# <a name="troubleshooting-and-key-health-indicators-in-lync-server-2013"></a><span data-ttu-id="f30d8-103">Indicadores de estado de las claves y solución de problemas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f30d8-103">Troubleshooting and Key Health Indicators in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f30d8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f30d8-104">

<span> </span></span></span>

<span data-ttu-id="f30d8-105">_**Última modificación del tema:** 2015-05-18_</span><span class="sxs-lookup"><span data-stu-id="f30d8-105">_**Topic Last Modified:** 2015-05-18_</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f30d8-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f30d8-106">In This Section</span></span>

<span data-ttu-id="f30d8-107">Para cumplir con los SLAs de arquitectura de referencia y garantizar una transición sin problemas a nuestros equipos de soporte técnico, se debe definir un enfoque de solución de problemas común junto con un conjunto necesario de métodos y herramientas de solución de problemas, tal como se define en la [Guía de redes](https://go.microsoft.com/fwlink/p/?linkid=390677) de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f30d8-107">To meet the Reference Architecture SLAs and to ensure a smooth transition to our support teams, a common troubleshooting approach must be defined together with a required set of troubleshooting tools and approaches as defined in the Lync Server [Networking guide](https://go.microsoft.com/fwlink/p/?linkid=390677) .</span></span>

<span data-ttu-id="f30d8-108">Se recomienda usar System Center Operations Manager para supervisar el estado del sistema Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f30d8-108">We strongly recommend that System Center Operations Manager be used to monitor the health of the Lync Server 2013 system.</span></span> <span data-ttu-id="f30d8-109">Además, consulte la descripción de KHIs en la [Guía de redes](https://go.microsoft.com/fwlink/p/?linkid=390677) de lync Server 2013 y la hoja de cálculo de Excel para usar con Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="f30d8-109">Also, refer to the discussion of KHIs in the Lync Server 2013 [Networking guide](https://go.microsoft.com/fwlink/p/?linkid=390677) and the Excel spreadsheet for use with Lync 2013.</span></span>

</div>

<div>

## <a name="reference"></a><span data-ttu-id="f30d8-110">Referencia</span><span class="sxs-lookup"><span data-stu-id="f30d8-110">Reference</span></span>

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="f30d8-111">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="f30d8-111">Related Sections</span></span>

<span data-ttu-id="f30d8-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f30d8-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

