---
title: 'Lync Server 2013: eventos de UCWA'
description: 'Lync Server 2013: eventos de UCWA.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UCWA events
ms:assetid: 26cb409d-f4e4-43c7-873f-b694702d491d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945621(v=OCS.15)
ms:contentKeyID: 51541461
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8104ce9c7533350f40ce194e1cde205bc3692792
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440468"
---
# <a name="ucwa-events-in-lync-server-2013"></a><span data-ttu-id="bbd41-103">Eventos de UCWA en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bbd41-103">UCWA events in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bbd41-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bbd41-104">

<span> </span></span></span>

<span data-ttu-id="bbd41-105">_**Última modificación del tema:** 2013-02-15_</span><span class="sxs-lookup"><span data-stu-id="bbd41-105">_**Topic Last Modified:** 2013-02-15_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="bbd41-106">Lync Server 2013 usa la API Web de comunicaciones unificadas (UCWA) para una serie de propósitos, desde el acceso a Microsoft Exchange para las búsquedas de contactos hasta la actualización de presencia para clientes móviles.</span><span class="sxs-lookup"><span data-stu-id="bbd41-106">Lync Server 2013 uses the Unified Communications Web API (UCWA) for a number of purposes, from accessing Microsoft Exchange for contact searches to updating presence for mobile clients.</span></span>

<span data-ttu-id="bbd41-p101">UCWA escribirá los registros del comportamiento operativo como tipos de evento informativos, de advertencia y de error. En la siguiente tabla se describen los eventos que pueden escribir los componentes de UCWA.</span><span class="sxs-lookup"><span data-stu-id="bbd41-p101">UCWA will write records of operational behavior as event types Informational, Warning, and Error. The following table describes the events that can be written by the UCWA components.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbd41-109">Id. del evento</span><span class="sxs-lookup"><span data-stu-id="bbd41-109">Event ID</span></span></th>
<th><span data-ttu-id="bbd41-110">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="bbd41-110">Event Type</span></span></th>
<th><span data-ttu-id="bbd41-111">Resumen</span><span class="sxs-lookup"><span data-stu-id="bbd41-111">Summary</span></span></th>
<th><span data-ttu-id="bbd41-112">Causa y solución</span><span class="sxs-lookup"><span data-stu-id="bbd41-112">Cause and Resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-113">20001</span><span class="sxs-lookup"><span data-stu-id="bbd41-113">20001</span></span></p></td>
<td><p><span data-ttu-id="bbd41-114">Informativo</span><span class="sxs-lookup"><span data-stu-id="bbd41-114">Informational</span></span></p></td>
<td><p><span data-ttu-id="bbd41-115">Se inicializó UCWA</span><span class="sxs-lookup"><span data-stu-id="bbd41-115">UCWA initialized</span></span></p></td>
<td><p><span data-ttu-id="bbd41-116">N/D</span><span class="sxs-lookup"><span data-stu-id="bbd41-116">N/A</span></span></p>
<p><span data-ttu-id="bbd41-117">N/D</span><span class="sxs-lookup"><span data-stu-id="bbd41-117">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-118">20002</span><span class="sxs-lookup"><span data-stu-id="bbd41-118">20002</span></span></p></td>
<td><p><span data-ttu-id="bbd41-119">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-119">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-120">UCWA encontró una excepción inesperada durante la inicialización</span><span class="sxs-lookup"><span data-stu-id="bbd41-120">UCWA encountered an unexpected exception during initialization</span></span></p></td>
<td><p><span data-ttu-id="bbd41-121">Se produjo un error inesperado durante la inicialización</span><span class="sxs-lookup"><span data-stu-id="bbd41-121">An unexpected error has occurred during initialization</span></span></p>
<p><span data-ttu-id="bbd41-122">Examine los detalles de la excepción en la entrada del registro de eventos asociada para determinar la posible causa</span><span class="sxs-lookup"><span data-stu-id="bbd41-122">Examine the exception details in the associated event log entry to determine the possible cause</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-123">20003</span><span class="sxs-lookup"><span data-stu-id="bbd41-123">20003</span></span></p></td>
<td><p><span data-ttu-id="bbd41-124">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-124">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-125">UCWA encontró una excepción no controlada</span><span class="sxs-lookup"><span data-stu-id="bbd41-125">UCWA encountered an unhandled exception</span></span></p></td>
<td><p><span data-ttu-id="bbd41-126">Se produjo una excepción no controlada</span><span class="sxs-lookup"><span data-stu-id="bbd41-126">An unhandled exception happened</span></span></p>
<p><span data-ttu-id="bbd41-p102">Reinicie el servidor. Si persiste el problema, póngase en contacto con el soporte técnico</span><span class="sxs-lookup"><span data-stu-id="bbd41-p102">Restart the server. If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-129">20004</span><span class="sxs-lookup"><span data-stu-id="bbd41-129">20004</span></span></p></td>
<td><p><span data-ttu-id="bbd41-130">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-130">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-131">No se puede obtener acceso a Exchange para fotos HD</span><span class="sxs-lookup"><span data-stu-id="bbd41-131">Cannot access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="bbd41-132">La conexión a Exchange no está disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-132">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="bbd41-133">Asegúrese de que la conexión a Exchange esté disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-133">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-134">20005</span><span class="sxs-lookup"><span data-stu-id="bbd41-134">20005</span></span></p></td>
<td><p><span data-ttu-id="bbd41-135">Informativo</span><span class="sxs-lookup"><span data-stu-id="bbd41-135">Informational</span></span></p></td>
<td><p><span data-ttu-id="bbd41-136">Se recuperó el acceso a Exchange para fotos HD</span><span class="sxs-lookup"><span data-stu-id="bbd41-136">Recovered from failing to access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="bbd41-137">N/D</span><span class="sxs-lookup"><span data-stu-id="bbd41-137">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-138">20006</span><span class="sxs-lookup"><span data-stu-id="bbd41-138">20006</span></span></p></td>
<td><p><span data-ttu-id="bbd41-139">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-139">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-140">No se puede obtener acceso a Exchange para la búsqueda de contactos</span><span class="sxs-lookup"><span data-stu-id="bbd41-140">Cannot access Exchange for contact search</span></span></p></td>
<td><p><span data-ttu-id="bbd41-141">La conexión a Exchange no está disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-141">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="bbd41-142">Asegúrese de que la conexión a Exchange esté disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-142">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-143">20007</span><span class="sxs-lookup"><span data-stu-id="bbd41-143">20007</span></span></p></td>
<td><p><span data-ttu-id="bbd41-144">Informativo</span><span class="sxs-lookup"><span data-stu-id="bbd41-144">Informational</span></span></p></td>
<td><p><span data-ttu-id="bbd41-145">Se recuperó el acceso a Exchange para la búsqueda de contactos</span><span class="sxs-lookup"><span data-stu-id="bbd41-145">Recovered from failing to search contact in Exchange</span></span></p></td>
<td><p><span data-ttu-id="bbd41-146">N/D</span><span class="sxs-lookup"><span data-stu-id="bbd41-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-147">20008</span><span class="sxs-lookup"><span data-stu-id="bbd41-147">20008</span></span></p></td>
<td><p><span data-ttu-id="bbd41-148">Advertencia</span><span class="sxs-lookup"><span data-stu-id="bbd41-148">Warning</span></span></p></td>
<td><p><span data-ttu-id="bbd41-149">Se intentó un número de suscripciones de presencia mayor que el permitido por aplicación</span><span class="sxs-lookup"><span data-stu-id="bbd41-149">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p></td>
<td><p><span data-ttu-id="bbd41-150">Se intentó un número de suscripciones de presencia mayor que el permitido por aplicación</span><span class="sxs-lookup"><span data-stu-id="bbd41-150">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p>
<p><span data-ttu-id="bbd41-151">Compruebe los clientes para determinar las suscripciones innecesarias</span><span class="sxs-lookup"><span data-stu-id="bbd41-151">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-152">20009</span><span class="sxs-lookup"><span data-stu-id="bbd41-152">20009</span></span></p></td>
<td><p><span data-ttu-id="bbd41-153">Advertencia</span><span class="sxs-lookup"><span data-stu-id="bbd41-153">Warning</span></span></p></td>
<td><p><span data-ttu-id="bbd41-154">Se intentó un número de suscripciones de presencia mayor que el permitido por lote</span><span class="sxs-lookup"><span data-stu-id="bbd41-154">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p></td>
<td><p><span data-ttu-id="bbd41-155">Se intentó un número de suscripciones de presencia mayor que el permitido por lote</span><span class="sxs-lookup"><span data-stu-id="bbd41-155">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p>
<p><span data-ttu-id="bbd41-156">Compruebe los clientes para determinar las suscripciones innecesarias</span><span class="sxs-lookup"><span data-stu-id="bbd41-156">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-157">20010</span><span class="sxs-lookup"><span data-stu-id="bbd41-157">20010</span></span></p></td>
<td><p><span data-ttu-id="bbd41-158">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-158">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-159">No se pueden recuperar los datos en banda</span><span class="sxs-lookup"><span data-stu-id="bbd41-159">Cannot retrieve inband data</span></span></p></td>
<td><p><span data-ttu-id="bbd41-160">No se pueden recuperar los datos en banda</span><span class="sxs-lookup"><span data-stu-id="bbd41-160">Cannot retrieve inband data</span></span></p>
<p><span data-ttu-id="bbd41-161">Si persiste el problema, póngase en contacto con el soporte técnico</span><span class="sxs-lookup"><span data-stu-id="bbd41-161">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-162">20011</span><span class="sxs-lookup"><span data-stu-id="bbd41-162">20011</span></span></p></td>
<td><p><span data-ttu-id="bbd41-163">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-163">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-164">No se puede suscribir la presencia</span><span class="sxs-lookup"><span data-stu-id="bbd41-164">Cannot subscribe presence</span></span></p></td>
<td><p><span data-ttu-id="bbd41-165">No se puede suscribir la presencia</span><span class="sxs-lookup"><span data-stu-id="bbd41-165">Cannot subscribe presence</span></span></p>
<p><span data-ttu-id="bbd41-166">Si persiste el problema, póngase en contacto con el soporte técnico</span><span class="sxs-lookup"><span data-stu-id="bbd41-166">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-167">20012</span><span class="sxs-lookup"><span data-stu-id="bbd41-167">20012</span></span></p></td>
<td><p><span data-ttu-id="bbd41-168">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-168">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-169">Error al registrar el extremo</span><span class="sxs-lookup"><span data-stu-id="bbd41-169">Failed to register endpoint</span></span></p></td>
<td><p><span data-ttu-id="bbd41-170">Error al registrar el extremo</span><span class="sxs-lookup"><span data-stu-id="bbd41-170">Failed to register endpoint</span></span></p>
<p><span data-ttu-id="bbd41-171">Si persiste el problema, póngase en contacto con el soporte técnico</span><span class="sxs-lookup"><span data-stu-id="bbd41-171">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-172">20013</span><span class="sxs-lookup"><span data-stu-id="bbd41-172">20013</span></span></p></td>
<td><p><span data-ttu-id="bbd41-173">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-173">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-174">La MCU de mensajería instantánea no está disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-174">IM MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="bbd41-175">La MCU de mensajería instantánea no está disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-175">IM MCU is unavailable</span></span></p>
<p><span data-ttu-id="bbd41-176">Compruebe si la MCU de mensajería instantánea se está ejecutando</span><span class="sxs-lookup"><span data-stu-id="bbd41-176">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-177">20014</span><span class="sxs-lookup"><span data-stu-id="bbd41-177">20014</span></span></p></td>
<td><p><span data-ttu-id="bbd41-178">Informativo</span><span class="sxs-lookup"><span data-stu-id="bbd41-178">Informational</span></span></p></td>
<td><p><span data-ttu-id="bbd41-179">Se recuperó la conexión a la MCU de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="bbd41-179">Recovered from failing to connect to IM MCU</span></span></p></td>
<td><p><span data-ttu-id="bbd41-180">N/D</span><span class="sxs-lookup"><span data-stu-id="bbd41-180">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-181">20015</span><span class="sxs-lookup"><span data-stu-id="bbd41-181">20015</span></span></p></td>
<td><p><span data-ttu-id="bbd41-182">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-182">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-183">La MCU de audio y vídeo no está disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-183">AV MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="bbd41-184">La MCU de audio y vídeo no está disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-184">AV MCU is unavailable</span></span></p>
<p><span data-ttu-id="bbd41-185">Compruebe si la MCU de audio y vídeo se está ejecutando</span><span class="sxs-lookup"><span data-stu-id="bbd41-185">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-186">20016</span><span class="sxs-lookup"><span data-stu-id="bbd41-186">20016</span></span></p></td>
<td><p><span data-ttu-id="bbd41-187">Informativo</span><span class="sxs-lookup"><span data-stu-id="bbd41-187">Informational</span></span></p></td>
<td><p><span data-ttu-id="bbd41-188">Se recuperó la conexión a la MCU de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="bbd41-188">Recovered from failing to connect to AV MCU</span></span></p></td>
<td><p><span data-ttu-id="bbd41-189">N/D</span><span class="sxs-lookup"><span data-stu-id="bbd41-189">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-190">20017</span><span class="sxs-lookup"><span data-stu-id="bbd41-190">20017</span></span></p></td>
<td><p><span data-ttu-id="bbd41-191">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-191">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-192">La MCU de AS no está disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-192">AS MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="bbd41-193">La MCU de AS no está disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-193">AS MCU is unavailable</span></span></p>
<p><span data-ttu-id="bbd41-194">Compruebe si la MCU de AS se está ejecutando</span><span class="sxs-lookup"><span data-stu-id="bbd41-194">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-195">20018</span><span class="sxs-lookup"><span data-stu-id="bbd41-195">20018</span></span></p></td>
<td><p><span data-ttu-id="bbd41-196">Informativo</span><span class="sxs-lookup"><span data-stu-id="bbd41-196">Informational</span></span></p></td>
<td><p><span data-ttu-id="bbd41-197">Se recuperó la conexión a la MCU de AS</span><span class="sxs-lookup"><span data-stu-id="bbd41-197">Recovered from failing to connect to AS MCU</span></span></p></td>
<td><p><span data-ttu-id="bbd41-198">N/D</span><span class="sxs-lookup"><span data-stu-id="bbd41-198">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-199">20019</span><span class="sxs-lookup"><span data-stu-id="bbd41-199">20019</span></span></p></td>
<td><p><span data-ttu-id="bbd41-200">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-200">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-201">La MCU de datos no está disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-201">Data MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="bbd41-202">La MCU de datos no está disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-202">Data MCU is unavailable</span></span></p>
<p><span data-ttu-id="bbd41-203">Compruebe si la MCU de datos se está ejecutando</span><span class="sxs-lookup"><span data-stu-id="bbd41-203">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-204">20020</span><span class="sxs-lookup"><span data-stu-id="bbd41-204">20020</span></span></p></td>
<td><p><span data-ttu-id="bbd41-205">Informativo</span><span class="sxs-lookup"><span data-stu-id="bbd41-205">Informational</span></span></p></td>
<td><p><span data-ttu-id="bbd41-206">Se recuperó la conexión a la MCU de datos</span><span class="sxs-lookup"><span data-stu-id="bbd41-206">Recovered from failing to connect to Data MCU</span></span></p></td>
<td><p><span data-ttu-id="bbd41-207">N/D</span><span class="sxs-lookup"><span data-stu-id="bbd41-207">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-208">20021</span><span class="sxs-lookup"><span data-stu-id="bbd41-208">20021</span></span></p></td>
<td><p><span data-ttu-id="bbd41-209">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-209">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-210">No se puede conectar la MCU de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="bbd41-210">Cannot join IM MCU</span></span></p></td>
<td><p><span data-ttu-id="bbd41-211">No se puede conectar la MCU de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="bbd41-211">Cannot join IM MCU</span></span></p>
<p><span data-ttu-id="bbd41-212">Compruebe si la MCU de mensajería instantánea se está ejecutando</span><span class="sxs-lookup"><span data-stu-id="bbd41-212">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-213">20022</span><span class="sxs-lookup"><span data-stu-id="bbd41-213">20022</span></span></p></td>
<td><p><span data-ttu-id="bbd41-214">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-214">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-215">No se puede conectar la MCU de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="bbd41-215">Cannot join AV MCU</span></span></p></td>
<td><p><span data-ttu-id="bbd41-216">No se puede conectar la MCU de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="bbd41-216">Cannot join AV MCU</span></span></p>
<p><span data-ttu-id="bbd41-217">Compruebe si la MCU de audio y vídeo se está ejecutando</span><span class="sxs-lookup"><span data-stu-id="bbd41-217">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-218">20023</span><span class="sxs-lookup"><span data-stu-id="bbd41-218">20023</span></span></p></td>
<td><p><span data-ttu-id="bbd41-219">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-219">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-220">No se puede conectar la MCU de AS</span><span class="sxs-lookup"><span data-stu-id="bbd41-220">Cannot join AS MCU</span></span></p></td>
<td><p><span data-ttu-id="bbd41-221">No se puede conectar la MCU de AS</span><span class="sxs-lookup"><span data-stu-id="bbd41-221">Cannot join AS MCU</span></span></p>
<p><span data-ttu-id="bbd41-222">Compruebe si la MCU de AS se está ejecutando</span><span class="sxs-lookup"><span data-stu-id="bbd41-222">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-223">20024</span><span class="sxs-lookup"><span data-stu-id="bbd41-223">20024</span></span></p></td>
<td><p><span data-ttu-id="bbd41-224">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-224">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-225">No se puede conectar la MCU de datos</span><span class="sxs-lookup"><span data-stu-id="bbd41-225">Cannot join Data MCU</span></span></p></td>
<td><p><span data-ttu-id="bbd41-226">No se puede conectar la MCU de datos</span><span class="sxs-lookup"><span data-stu-id="bbd41-226">Cannot join Data MCU</span></span></p>
<p><span data-ttu-id="bbd41-227">Compruebe si la MCU de datos se está ejecutando</span><span class="sxs-lookup"><span data-stu-id="bbd41-227">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-228">20025</span><span class="sxs-lookup"><span data-stu-id="bbd41-228">20025</span></span></p></td>
<td><p><span data-ttu-id="bbd41-229">Error</span><span class="sxs-lookup"><span data-stu-id="bbd41-229">Error</span></span></p></td>
<td><p><span data-ttu-id="bbd41-230">No se puede obtener acceso a Active Directory para las fotos</span><span class="sxs-lookup"><span data-stu-id="bbd41-230">Cannot access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="bbd41-231">La conexión a Active Directory no está disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-231">Connection to active directory is not available</span></span></p>
<p><span data-ttu-id="bbd41-232">Asegúrese de que la conexión a Active Directory esté disponible</span><span class="sxs-lookup"><span data-stu-id="bbd41-232">Make sure the connection to active directory is available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd41-233">20026</span><span class="sxs-lookup"><span data-stu-id="bbd41-233">20026</span></span></p></td>
<td><p><span data-ttu-id="bbd41-234">Informativo</span><span class="sxs-lookup"><span data-stu-id="bbd41-234">Informational</span></span></p></td>
<td><p><span data-ttu-id="bbd41-235">Se recuperó el acceso a Active Directory para las fotos</span><span class="sxs-lookup"><span data-stu-id="bbd41-235">Recovered from failing to access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="bbd41-236">N/D</span><span class="sxs-lookup"><span data-stu-id="bbd41-236">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd41-237">20027</span><span class="sxs-lookup"><span data-stu-id="bbd41-237">20027</span></span></p></td>
<td><p><span data-ttu-id="bbd41-238">Advertencia</span><span class="sxs-lookup"><span data-stu-id="bbd41-238">Warning</span></span></p></td>
<td><p><span data-ttu-id="bbd41-239">No se puede deserializar</span><span class="sxs-lookup"><span data-stu-id="bbd41-239">Cannot deserialize</span></span></p></td>
<td><p><span data-ttu-id="bbd41-240">No se puede deserializar</span><span class="sxs-lookup"><span data-stu-id="bbd41-240">Cannot deserialize</span></span></p>
<p><span data-ttu-id="bbd41-241">Si persiste el problema, póngase en contacto con el soporte técnico</span><span class="sxs-lookup"><span data-stu-id="bbd41-241">If the problem persists contact product support</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bbd41-242">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bbd41-242">


</div>

<span> </span>

</div>

</div>

</span></span></div>

