---
title: 'Lync Server 2013: Configuración de la negociación para socios federados XMPP'
description: 'Lync Server 2013: configuración de la negociación para socios de XMPP federados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Negotiation settings for XMPP federated partners
ms:assetid: ef773942-ef92-4f71-85a1-738dfebdfa00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552456(v=OCS.15)
ms:contentKeyID: 48679567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ac3d9c69d407dc750a1afb35f0a448869a88f09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445591"
---
# <a name="negotiation-settings-for-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="59513-103">Configuración de la negociación para socios federados XMPP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="59513-103">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="59513-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="59513-104">

<span> </span></span></span>

<span data-ttu-id="59513-105">_**Última modificación del tema:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="59513-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="59513-106">La configuración de los tipos de negociación en la configuración de un socio XMPP tiene una amplia variedad de combinaciones posibles.</span><span class="sxs-lookup"><span data-stu-id="59513-106">The settings for the negotiation types in the configuration of an XMPP Partner have a wide variety of possible combinations.</span></span> <span data-ttu-id="59513-107">No todas estas combinaciones son válidas.</span><span class="sxs-lookup"><span data-stu-id="59513-107">Not all of these combinations are valid.</span></span> <span data-ttu-id="59513-108">La tabla que se describe en este tema definirá la configuración válida y no válida.</span><span class="sxs-lookup"><span data-stu-id="59513-108">The table detailed in this topic will define the valid and not valid settings.</span></span> <span data-ttu-id="59513-109">Las configuraciones comunes se presentan en la primera tabla, en la segunda tabla, en la que se detallan todas las combinaciones posibles.</span><span class="sxs-lookup"><span data-stu-id="59513-109">Common configurations are presented in the first table, the second table detailing all possible combinations.</span></span> <span data-ttu-id="59513-110">Tenga en cuenta que no puede tener *nivel de autenticación y seguridad simple* (SASL) **a menos que** la seguridad de la *capa de transporte* (TLS) también esté disponible.</span><span class="sxs-lookup"><span data-stu-id="59513-110">Note that you cannot have *Simple Authentication and Security Layer* (SASL) **unless** *Transport Layer Security* (TLS) is also available.</span></span> <span data-ttu-id="59513-111">SASL se envía en un formato no cifrado (legible) y nunca debe transmitirse a menos que esté protegido por otro medio, como TLS.</span><span class="sxs-lookup"><span data-stu-id="59513-111">SASL is sent in an unencrypted (readable) format and should never be transmitted unless protected by another means, such as TLS.</span></span>

### <a name="common-xmpp-federation-negotiation-methods"></a><span data-ttu-id="59513-112">Métodos comunes de negociación de Federación de XMPP</span><span class="sxs-lookup"><span data-stu-id="59513-112">Common XMPP Federation Negotiation Methods</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59513-113">Seguridad de la capa de transporte (TLS)</span><span class="sxs-lookup"><span data-stu-id="59513-113">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="59513-114">Capa de seguridad y autenticación simple (SASL)</span><span class="sxs-lookup"><span data-stu-id="59513-114">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="59513-115">Autenticación Dialback</span><span class="sxs-lookup"><span data-stu-id="59513-115">Dialback Authentication</span></span></th>
<th><span data-ttu-id="59513-116">Métodos de autenticación esperados</span><span class="sxs-lookup"><span data-stu-id="59513-116">Expected Authentication Method(s)</span></span></th>
<th><span data-ttu-id="59513-117">Notas</span><span class="sxs-lookup"><span data-stu-id="59513-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59513-118">Requerido </span><span class="sxs-lookup"><span data-stu-id="59513-118">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-119">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-120">Falso</span><span class="sxs-lookup"><span data-stu-id="59513-120">False</span></span></p></td>
<td><p><span data-ttu-id="59513-121">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="59513-121">SASL over TLS</span></span></p></td>
<td><p><span data-ttu-id="59513-122">TLS y SASL requeridos ayudan a garantizar que la secuencia de mensajes SASL sea segura.</span><span class="sxs-lookup"><span data-stu-id="59513-122">TLS and SASL required helps to ensure that the SASL message stream is secure.</span></span> <span data-ttu-id="59513-123">Dialback no está disponible y no se puede usar para un método de reserva si el socio de XMPP federado no ha establecido TLS en requerido u opcional.</span><span class="sxs-lookup"><span data-stu-id="59513-123">Dialback is not available and cannot be used for a fallback method if the XMPP federated partner has not set TLS to required or optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59513-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-124">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-126">True</span></span></p></td>
<td><p><span data-ttu-id="59513-127">SASL sobre TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="59513-127">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="59513-128">Al requerir TLS, si el socio XMPP federado ha establecido SASL a la opción SASL opcional o requerida.</span><span class="sxs-lookup"><span data-stu-id="59513-128">By requiring TLS, if the XMPP federated partner has set SASL to optional or required SASL is used.</span></span> <span data-ttu-id="59513-129">Si SASL no está disponible, se usará Dialback a través de TLS.</span><span class="sxs-lookup"><span data-stu-id="59513-129">If SASL is not available, Dialback over TLS will be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59513-130">Opcional </span><span class="sxs-lookup"><span data-stu-id="59513-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-131">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-132">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-132">True</span></span></p></td>
<td><p><span data-ttu-id="59513-133">SASL sobre TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="59513-133">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="59513-134">Aunque es muy flexible en los métodos de negociación ofrecidos, esta configuración depende de la configuración del socio de Federación de XMPP.</span><span class="sxs-lookup"><span data-stu-id="59513-134">While very flexible in the negotiation methods offered, these settings rely on the XMPP federation partner’s settings.</span></span> <span data-ttu-id="59513-135">Si el socio tiene TLS opcional o obligatorio, pero no se admite SASL, la Dialback de TLS estará disponible.</span><span class="sxs-lookup"><span data-stu-id="59513-135">If the partner has TLS optional or required but SASL is not supported, TLS Dialback will be available.</span></span> <span data-ttu-id="59513-136">Si el asociado tiene TLS y SASL establecido en opcional o en obligatorio, se usa la selección óptima de TLS por SASL.</span><span class="sxs-lookup"><span data-stu-id="59513-136">If the partner has TLS and SASL set to optional or required, the optimal selection of TLS over SASL is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59513-137">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-137">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-138">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-138">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-139">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-139">True</span></span></p></td>
<td><p><span data-ttu-id="59513-140">Dialback TCP</span><span class="sxs-lookup"><span data-stu-id="59513-140">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="59513-141">En muchos casos, TCP Dialback es la única solución posible.</span><span class="sxs-lookup"><span data-stu-id="59513-141">In many cases, TCP Dialback is the only possible solution.</span></span> <span data-ttu-id="59513-142">Menos conveniente que otras opciones, proporciona un cierto nivel de confianza.</span><span class="sxs-lookup"><span data-stu-id="59513-142">Less desirable than other options, it does provide some level of trust.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="xmpp-federation-negotiation-methods-matrix---complete"></a><span data-ttu-id="59513-143">Matriz de métodos de negociación de Federación XMPP-completada</span><span class="sxs-lookup"><span data-stu-id="59513-143">XMPP Federation Negotiation Methods Matrix - Complete</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59513-144">Seguridad de la capa de transporte (TLS)</span><span class="sxs-lookup"><span data-stu-id="59513-144">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="59513-145">Capa de seguridad y autenticación simple (SASL)</span><span class="sxs-lookup"><span data-stu-id="59513-145">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="59513-146">Autenticación Dialback</span><span class="sxs-lookup"><span data-stu-id="59513-146">Dialback Authentication</span></span></th>
<th><span data-ttu-id="59513-147">Método de autenticación esperado</span><span class="sxs-lookup"><span data-stu-id="59513-147">Expected Authentication Method</span></span></th>
<th><span data-ttu-id="59513-148">Notas, ADVERTENCIA o error para una configuración no válida</span><span class="sxs-lookup"><span data-stu-id="59513-148">Notes, Warning or Error for Not Valid Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59513-149">Requerido </span><span class="sxs-lookup"><span data-stu-id="59513-149">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-150">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-150">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-151">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-151">True</span></span></p></td>
<td><p><span data-ttu-id="59513-152">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="59513-152">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-153">Dialback no funcionará si se necesitan SASL y TLS.</span><span class="sxs-lookup"><span data-stu-id="59513-153">Dialback will not operate if both SASL and TLS are required.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59513-154">Requerido </span><span class="sxs-lookup"><span data-stu-id="59513-154">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-155">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-155">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-156">Falso</span><span class="sxs-lookup"><span data-stu-id="59513-156">False</span></span></p></td>
<td><p><span data-ttu-id="59513-157">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="59513-157">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59513-158">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-158">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-159">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-159">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-160">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-160">True</span></span></p></td>
<td><p><span data-ttu-id="59513-161">SASL sobre TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="59513-161">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-162">SASL requiere TLS.</span><span class="sxs-lookup"><span data-stu-id="59513-162">SASL requires TLS.</span></span> <span data-ttu-id="59513-163">Permitir que TLS sea opcional puede provocar errores en las negociaciones de la sesión.</span><span class="sxs-lookup"><span data-stu-id="59513-163">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59513-164">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-164">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-165">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-165">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-166">Falso</span><span class="sxs-lookup"><span data-stu-id="59513-166">False</span></span></p></td>
<td><p><span data-ttu-id="59513-167">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="59513-167">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-168">SASL requiere TLS.</span><span class="sxs-lookup"><span data-stu-id="59513-168">SASL requires TLS.</span></span> <span data-ttu-id="59513-169">Permitir que TLS sea opcional puede provocar errores en las negociaciones de la sesión.</span><span class="sxs-lookup"><span data-stu-id="59513-169">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59513-170">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-170">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-171">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-171">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-172">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-172">True</span></span></p></td>
<td><p><span data-ttu-id="59513-173">Dialback TCP</span><span class="sxs-lookup"><span data-stu-id="59513-173">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-174">SASL requiere TLS.</span><span class="sxs-lookup"><span data-stu-id="59513-174">SASL requires TLS.</span></span> <span data-ttu-id="59513-175">Permitir que TLS sea opcional puede provocar errores en las negociaciones de la sesión.</span><span class="sxs-lookup"><span data-stu-id="59513-175">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59513-176">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-176">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-177">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-177">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-178">Falso</span><span class="sxs-lookup"><span data-stu-id="59513-178">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-179">Configuración no válida</span><span class="sxs-lookup"><span data-stu-id="59513-179">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-180">Como SASL requiere TLS, y TLS no está disponible, SASL/TLS no se pueden realizar correctamente.</span><span class="sxs-lookup"><span data-stu-id="59513-180">Because SASL requires TLS, and TLS is not available, SASL/TLS cannot succeed.</span></span> <span data-ttu-id="59513-181">TCP Dialback se establece en false y no se puede usar.</span><span class="sxs-lookup"><span data-stu-id="59513-181">TCP Dialback is set to false, and cannot be used.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59513-182">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-182">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-183">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-183">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-184">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-184">True</span></span></p></td>
<td><p><span data-ttu-id="59513-185">SASL sobre TLS, TLS Dialback</span><span class="sxs-lookup"><span data-stu-id="59513-185">SASL over TLS, TLS Dialback</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59513-186">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-186">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-187">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-187">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-188">Falso</span><span class="sxs-lookup"><span data-stu-id="59513-188">False</span></span></p></td>
<td><p><span data-ttu-id="59513-189">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="59513-189">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59513-190">Opcional </span><span class="sxs-lookup"><span data-stu-id="59513-190">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-191">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-191">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-192">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-192">True</span></span></p></td>
<td><p><span data-ttu-id="59513-193">SASL sobre TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="59513-193">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-194">SASL requiere TLS.</span><span class="sxs-lookup"><span data-stu-id="59513-194">SASL requires TLS.</span></span> <span data-ttu-id="59513-195">Permitir que TLS sea opcional puede provocar errores en las negociaciones de la sesión.</span><span class="sxs-lookup"><span data-stu-id="59513-195">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59513-196">Opcional </span><span class="sxs-lookup"><span data-stu-id="59513-196">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-197">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-197">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-198">Falso</span><span class="sxs-lookup"><span data-stu-id="59513-198">False</span></span></p></td>
<td><p><span data-ttu-id="59513-199">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="59513-199">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-200">SASL requiere TLS.</span><span class="sxs-lookup"><span data-stu-id="59513-200">SASL requires TLS.</span></span> <span data-ttu-id="59513-201">Permitir que TLS sea opcional puede provocar errores en las negociaciones de la sesión.</span><span class="sxs-lookup"><span data-stu-id="59513-201">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59513-202">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-202">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-203">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-203">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-204">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-204">True</span></span></p></td>
<td><p><span data-ttu-id="59513-205">Dialback TCP</span><span class="sxs-lookup"><span data-stu-id="59513-205">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-206">SASL requiere TLS.</span><span class="sxs-lookup"><span data-stu-id="59513-206">SASL requires TLS.</span></span> <span data-ttu-id="59513-207">Permitir que TLS sea opcional puede provocar errores en las negociaciones de la sesión.</span><span class="sxs-lookup"><span data-stu-id="59513-207">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59513-208">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-208">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-209">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-209">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-210">Falso</span><span class="sxs-lookup"><span data-stu-id="59513-210">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-211">Configuración no válida</span><span class="sxs-lookup"><span data-stu-id="59513-211">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-212">SASL requiere TLS.</span><span class="sxs-lookup"><span data-stu-id="59513-212">SASL requires TLS.</span></span> <span data-ttu-id="59513-213">Permitir que TLS sea opcional puede provocar errores en las negociaciones de la sesión.</span><span class="sxs-lookup"><span data-stu-id="59513-213">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59513-214">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-214">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-215">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-215">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-216">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-216">True</span></span></p></td>
<td><p><span data-ttu-id="59513-217">TLS Dialback</span><span class="sxs-lookup"><span data-stu-id="59513-217">TLS Dialback</span></span></p></td>
<td><p><span data-ttu-id="59513-218">La configuración permite Dialback TLS.</span><span class="sxs-lookup"><span data-stu-id="59513-218">Configuration allows for TLS Dialback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59513-219">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59513-219">Required</span></span></p></td>
<td><p><span data-ttu-id="59513-220">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-220">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-221">Falso</span><span class="sxs-lookup"><span data-stu-id="59513-221">False</span></span></p></td>
<td><p><span data-ttu-id="59513-222">Configuración no válida</span><span class="sxs-lookup"><span data-stu-id="59513-222">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-223">SASL o Dialback deben estar habilitados.</span><span class="sxs-lookup"><span data-stu-id="59513-223">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59513-224">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-224">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-225">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-225">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-226">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-226">True</span></span></p></td>
<td><p><span data-ttu-id="59513-227">TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="59513-227">TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="59513-228">Según las opciones de negociación del otro punto final, se aceptarán TCP o TLS Dialback.</span><span class="sxs-lookup"><span data-stu-id="59513-228">Based on negotiation choices of the other end point, TCP or TLS Dialback will be accepted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59513-229">Opcional</span><span class="sxs-lookup"><span data-stu-id="59513-229">Optional</span></span></p></td>
<td><p><span data-ttu-id="59513-230">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-230">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-231">Falso</span><span class="sxs-lookup"><span data-stu-id="59513-231">False</span></span></p></td>
<td><p><span data-ttu-id="59513-232">Configuración no válida</span><span class="sxs-lookup"><span data-stu-id="59513-232">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-233">SASL o Dialback deben estar habilitados.</span><span class="sxs-lookup"><span data-stu-id="59513-233">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59513-234">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-234">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-235">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-235">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-236">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59513-236">True</span></span></p></td>
<td><p><span data-ttu-id="59513-237">Dialback TCP</span><span class="sxs-lookup"><span data-stu-id="59513-237">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="59513-238">TCP Dialback es el único método de negociación disponible</span><span class="sxs-lookup"><span data-stu-id="59513-238">TCP Dialback is the only negotiation method available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59513-239">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-239">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-240">No compatible</span><span class="sxs-lookup"><span data-stu-id="59513-240">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="59513-241">Falso</span><span class="sxs-lookup"><span data-stu-id="59513-241">False</span></span></p></td>
<td><p><span data-ttu-id="59513-242">Configuración no válida</span><span class="sxs-lookup"><span data-stu-id="59513-242">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="59513-243">SASL o Dialback deben estar habilitados.</span><span class="sxs-lookup"><span data-stu-id="59513-243">SASL or Dialback must be enabled.</span></span>


<span data-ttu-id="59513-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="59513-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

