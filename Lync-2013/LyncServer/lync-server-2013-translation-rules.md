---
title: 'Lync Server 2013: reglas de traducción'
description: 'Lync Server 2013: reglas de traducción.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Translation rules
ms:assetid: 6e067bd4-4931-4385-81ac-2acae45a16d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398520(v=OCS.15)
ms:contentKeyID: 48184460
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65ee21459123ea09f54eb52e65a4d9ecba61c386
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397872"
---
# <a name="translation-rules-in-lync-server-2013"></a><span data-ttu-id="ee95d-103">Reglas de traducción en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee95d-103">Translation rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee95d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee95d-104">

<span> </span></span></span>

<span data-ttu-id="ee95d-105">_**Última modificación del tema:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="ee95d-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="ee95d-106">Lync Server 2013 Enterprise Voice requiere que todas las cadenas de marcado se normalizaran al formato E. 164 con el fin de realizar la búsqueda de números inversos (RNL).</span><span class="sxs-lookup"><span data-stu-id="ee95d-106">Lync Server 2013 Enterprise Voice requires that all dial strings be normalized to E.164 format for the purpose of performing reverse number lookup (RNL).</span></span> <span data-ttu-id="ee95d-107">En Microsoft Lync Server 2010, las reglas de traducción solo se admiten para números llamados.</span><span class="sxs-lookup"><span data-stu-id="ee95d-107">In Microsoft Lync Server 2010, translation rules are supported only for called numbers.</span></span> <span data-ttu-id="ee95d-108">En Microsoft Lync Server 2013, también se admiten las reglas de traducción para llamar a los números.</span><span class="sxs-lookup"><span data-stu-id="ee95d-108">New in Microsoft Lync Server 2013, translation rules are also supported for calling numbers.</span></span> <span data-ttu-id="ee95d-109">El *tronco del mismo nivel* (es decir, la puerta de enlace asociada, la central de conmutación [PBX] o el tronco SIP) puede necesitar que los números estén en un formato de marcado local.</span><span class="sxs-lookup"><span data-stu-id="ee95d-109">The *trunk peer* (that is, the associated gateway, private branch exchange (PBX), or SIP trunk) may require that numbers be in a local dialing format.</span></span> <span data-ttu-id="ee95d-110">Para convertir números del formato E.164 a un formato de marcado local, puede definir una o más reglas de conversión para manipular el URI de solicitud antes de redirigirlo al tronco del mismo nivel que el tronco.</span><span class="sxs-lookup"><span data-stu-id="ee95d-110">To translate numbers from E.164 format to a local dialing format, you can define one or more translation rules to manipulate the request URI before you route it to the trunk peer.</span></span> <span data-ttu-id="ee95d-111">Por ejemplo, puede escribir una regla de conversión para quitar +44 del inicio de la cadena de marcado y cambiarlo por 0144.</span><span class="sxs-lookup"><span data-stu-id="ee95d-111">For example, you could write a translation rule to remove +44 from the beginning of a dial string and replace it with 0144.</span></span>

<span data-ttu-id="ee95d-112">Con la conversión de la ruta saliente del servidor, puedes reducir los requisitos de configuración de cada tronco del mismo nivel individual para convertir los números de teléfono en un formato de marcado local.</span><span class="sxs-lookup"><span data-stu-id="ee95d-112">By performing outbound route translation on the server, you can reduce the configuration requirements on each individual trunk peer in order to translate phone numbers into a local dialing format.</span></span> <span data-ttu-id="ee95d-113">Cuando se planean las puertas de enlace y el número de puertas de enlace para asociarlas con un clúster de servidor de mediación específico, puede resultar útil agrupar los pares de troncales con requisitos de marcado local similares.</span><span class="sxs-lookup"><span data-stu-id="ee95d-113">When you plan which gateways, and how many gateways, to associate with a specific Mediation Server cluster, it may be useful to group trunk peers with similar local dialing requirements.</span></span> <span data-ttu-id="ee95d-114">Así, se puede reducir la cantidad de reglas de conversión necesarias y el tiempo necesario para escribirlas.</span><span class="sxs-lookup"><span data-stu-id="ee95d-114">This can reduce the number of required translation rules and the time it takes to write them.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ee95d-115">La Asociación de una o más reglas de traducción con una configuración de telefonía IP empresarial debe utilizarse como alternativa a la configuración de reglas de traducción en el sistema troncal.</span><span class="sxs-lookup"><span data-stu-id="ee95d-115">Associating one or more translation rules with an Enterprise Voice trunk configuration should be used as an alternative to configuring translation rules on the trunk peer.</span></span> <span data-ttu-id="ee95d-116">No asociar reglas de traducción con una configuración de troncal empresarial de voz si ha configurado reglas de traducción en el sistema troncal del mismo nivel, porque las dos reglas podrían entrar en conflicto.</span><span class="sxs-lookup"><span data-stu-id="ee95d-116">Do not associate translation rules with an Enterprise Voice trunk configuration if you have configured translation rules on the trunk peer, because the two rules might conflict.</span></span>



</div>

<div>

## <a name="example-translation-rules"></a><span data-ttu-id="ee95d-117">Reglas de conversión de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee95d-117">Example Translation Rules</span></span>

<span data-ttu-id="ee95d-118">Los siguientes ejemplos de reglas de conversión muestran cómo se pueden desarrollar reglas en el servidor para convertir números del formato E.164 a un formato local para el tronco del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="ee95d-118">The following examples of translation rules show how you can develop rules on the server to translate numbers from E.164 format to a local format for the trunk peer.</span></span>

<span data-ttu-id="ee95d-119">Para obtener más información sobre cómo implementar reglas de traducción, consulte [definición de reglas de traducción en Lync Server 2013](lync-server-2013-defining-translation-rules.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="ee95d-119">For details about how to implement translation rules, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>


<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee95d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee95d-120">Description</span></span></th>
<th><span data-ttu-id="ee95d-121">Dígitos iniciales</span><span class="sxs-lookup"><span data-stu-id="ee95d-121">Starting Digits</span></span></th>
<th><span data-ttu-id="ee95d-122">Longitud</span><span class="sxs-lookup"><span data-stu-id="ee95d-122">Length</span></span></th>
<th><span data-ttu-id="ee95d-123">Dígitos que se van a quitar</span><span class="sxs-lookup"><span data-stu-id="ee95d-123">Digits to Remove</span></span></th>
<th><span data-ttu-id="ee95d-124">Dígitos que se van a agregar</span><span class="sxs-lookup"><span data-stu-id="ee95d-124">Digits to Add</span></span></th>
<th><span data-ttu-id="ee95d-125">Patrón de comparación</span><span class="sxs-lookup"><span data-stu-id="ee95d-125">Matching Pattern</span></span></th>
<th><span data-ttu-id="ee95d-126">Conversión</span><span class="sxs-lookup"><span data-stu-id="ee95d-126">Translation</span></span></th>
<th><span data-ttu-id="ee95d-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee95d-127">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee95d-128">Marcado convencional de larga distancia de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="ee95d-128">Conventional long-distance dialing in U.S.</span></span></p>
<p><span data-ttu-id="ee95d-129">(quita el "+")</span><span class="sxs-lookup"><span data-stu-id="ee95d-129">(strip out the ‘+’)</span></span></p></td>
<td><p><span data-ttu-id="ee95d-130">+1</span><span class="sxs-lookup"><span data-stu-id="ee95d-130">+1</span></span></p></td>
<td><p><span data-ttu-id="ee95d-131">Exactamente 12</span><span class="sxs-lookup"><span data-stu-id="ee95d-131">Exactly 12</span></span></p></td>
<td><p><span data-ttu-id="ee95d-132">1</span><span class="sxs-lookup"><span data-stu-id="ee95d-132">1</span></span></p></td>
<td><p><span data-ttu-id="ee95d-133">,0</span><span class="sxs-lookup"><span data-stu-id="ee95d-133">0</span></span></p></td>
<td><p><span data-ttu-id="ee95d-134">^\+(1 \ d {10} ) $</span><span class="sxs-lookup"><span data-stu-id="ee95d-134">^\+(1\d{10})$</span></span></p></td>
<td><p><span data-ttu-id="ee95d-135">$1</span><span class="sxs-lookup"><span data-stu-id="ee95d-135">$1</span></span></p></td>
<td><p><span data-ttu-id="ee95d-136">+14255551010 se convierte en 14255551010</span><span class="sxs-lookup"><span data-stu-id="ee95d-136">+14255551010 becomes 14255551010</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee95d-137">Marcado internacional de larga distancia de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="ee95d-137">U.S. international long-distance dialing</span></span></p>
<p><span data-ttu-id="ee95d-138">(quita el "+" y agrega 011)</span><span class="sxs-lookup"><span data-stu-id="ee95d-138">(strip out ‘+’ and add 011)</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="ee95d-139">11 como mínimo</span><span class="sxs-lookup"><span data-stu-id="ee95d-139">At least 11</span></span></p></td>
<td><p><span data-ttu-id="ee95d-140">1</span><span class="sxs-lookup"><span data-stu-id="ee95d-140">1</span></span></p></td>
<td><p><span data-ttu-id="ee95d-141">011</span><span class="sxs-lookup"><span data-stu-id="ee95d-141">011</span></span></p></td>
<td><p><span data-ttu-id="ee95d-142">^\+(\d {9} \d +) $</span><span class="sxs-lookup"><span data-stu-id="ee95d-142">^\+(\d{9}\d+)$</span></span></p></td>
<td><p><span data-ttu-id="ee95d-143">011$1</span><span class="sxs-lookup"><span data-stu-id="ee95d-143">011$1</span></span></p></td>
<td><p><span data-ttu-id="ee95d-144">+441235551010 se convierte en 011441235551010</span><span class="sxs-lookup"><span data-stu-id="ee95d-144">+441235551010 becomes 011441235551010</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ee95d-145">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee95d-145">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

