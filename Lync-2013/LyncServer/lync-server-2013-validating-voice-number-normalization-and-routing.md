---
title: 'Lync Server 2013: validación de la normalización y el enrutamiento de números de voz'
description: 'Lync Server 2013: validación de la normalización y el enrutamiento de números de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating voice number normalization and routing
ms:assetid: a6a825c7-6928-4e80-b7e9-803b7f7ebd13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720922(v=OCS.15)
ms:contentKeyID: 63969633
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f28f679cbb991bdb90362eb61c9c7b68879791e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438627"
---
# <a name="validating-voice-number-normalization-and-routing-in-lync-server-2013"></a><span data-ttu-id="dcc9f-103">Validación de la normalización y el enrutamiento de números de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dcc9f-103">Validating voice number normalization and routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dcc9f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dcc9f-104">

<span> </span></span></span>

<span data-ttu-id="dcc9f-105">_**Última modificación del tema:** 2014-05-19_</span><span class="sxs-lookup"><span data-stu-id="dcc9f-105">_**Topic Last Modified:** 2014-05-19_</span></span>

<span data-ttu-id="dcc9f-106">Corregir la normalización de números y el enrutamiento es muy importante para un entorno funcional de telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-106">Correct number normalization and routing is very important for functional Enterprise Voice environment.</span></span> <span data-ttu-id="dcc9f-107">Especialmente durante las migraciones desde la central de conmutación (PBX) a un entorno independiente de Lync Server, una de las claves para la migración correcta es mostrar y documentar todas las reglas de marcado existentes y crear reglas de normalización apropiadas, directivas de voz, usos de teléfono y rutas.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-107">Especially during migrations from private branch exchange (PBX) to stand-alone Lync Server environment, one of the keys to successful migration is to reveal and document all existing dialing rules, and create appropriate normalization rules, voice policies, phone usages and routes.</span></span>

<span data-ttu-id="dcc9f-108">Validar la normalización de números y el enrutamiento es importante no solo durante las migraciones, sino también durante el funcionamiento normal y estable del sistema.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-108">Validating number normalization and routing is important not only during migrations but also during normal, stable operation of the system.</span></span>

<span data-ttu-id="dcc9f-109">Se recomienda realizar esta validación diariamente con el panel de control de Lync Server, empezando por desarrollar un conjunto sólido de casos de prueba en comparación con el conjunto actual de reglas de normalización publicadas en la configuración global de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-109">We recommend conducting this validation daily by using the Lync Server Control Panel, starting with developing a robust set of test cases against the current set of normalization rules that were published in the Lync Server global settings.</span></span> <span data-ttu-id="dcc9f-110">Estos casos de prueba deben ejecutarse todos los días para resaltar los cambios no deseados que se hayan realizado y que se hayan confirmado en el plan de marcado.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-110">These test cases should be run daily to highlight any unwanted changes that were made and committed to the dial plan.</span></span>

<span data-ttu-id="dcc9f-111">El panel de control de Lync Server también le ayuda a visualizar, probar, cambiar, archivar y compartir información de configuración sobre el enrutamiento de voz y para cambiar las reglas de normalización de números de voz de empresa, los planes de marcado, la Directiva de voz y las rutas.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-111">Lync Server Control Panel also helps you visualize, test, change, archive, and share configuration information about voice routing and in changing Enterprise Voice number normalization rules, dial plans, voice policy, and routes.</span></span> <span data-ttu-id="dcc9f-112">Tiene características adicionales para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="dcc9f-112">It has additional features for doing the following:</span></span>

  - <span data-ttu-id="dcc9f-113">Exportar e importar o realizar copias de seguridad de los datos de enrutamiento de voz entre sistemas.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-113">Exporting and importing or backing up voice routing data between systems.</span></span>

  - <span data-ttu-id="dcc9f-114">Probar los cambios de configuración antes de cargarlos en un sistema en vivo.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-114">Testing configuration changes before uploading them to a live system.</span></span>

  - <span data-ttu-id="dcc9f-115">Crear y ejecutar casos de pruebas de configuración para ayudar a garantizar la facilidad de uso de los datos de enrutamiento después de realizar cambios en ellos, pero antes de confirmarlos en un sistema implementado.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-115">Creating and running configuration test cases to help ensure the usability of routing data after you make changes to it, but before committing them the changes to a deployed system.</span></span>

  - <span data-ttu-id="dcc9f-116">Crear y cambiar las reglas de normalización de números, los perfiles de ubicación, la Directiva de voz y los datos de enrutamiento sin escribir las expresiones regulares necesarias.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-116">Creating and changing number normalization rules, location profiles, voice policy, and routing data without writing the necessary regular expressions.</span></span>

  - <span data-ttu-id="dcc9f-117">Analizar un perfil de ubicación para la compatibilidad con la edición telefónica de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-117">Analyzing a location profile for compatibility with the Lync Server Phone Edition.</span></span>

  - <span data-ttu-id="dcc9f-118">Puede encontrar más información sobre las pruebas de enrutamiento de voz en el [enrutamiento de voz de prueba en Lync Server 2013](lync-server-2013-test-voice-routing.md)</span><span class="sxs-lookup"><span data-stu-id="dcc9f-118">More information about voice routing tests can be found at [Test voice routing in Lync Server 2013](lync-server-2013-test-voice-routing.md)</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="dcc9f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcc9f-119">See Also</span></span>


[<span data-ttu-id="dcc9f-120">Probar el enrutamiento de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dcc9f-120">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="dcc9f-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dcc9f-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

