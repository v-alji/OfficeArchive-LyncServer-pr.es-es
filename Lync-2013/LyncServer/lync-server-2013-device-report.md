---
title: 'Lync Server 2013: informe de dispositivos'
description: 'Lync Server 2013: informe de dispositivos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Report
ms:assetid: f42e4d60-699b-4870-8bb5-13b51bb6eb2b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615049(v=OCS.15)
ms:contentKeyID: 48185807
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8bff8e973d5c3e2d96c18992a2a2d917d4deb1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429429"
---
# <a name="device-report-in-lync-server-2013"></a><span data-ttu-id="4e811-103">Informe de dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4e811-103">Device Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4e811-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4e811-104">

<span> </span></span></span>

<span data-ttu-id="4e811-105">_**Última modificación del tema:** 2013-11-12_</span><span class="sxs-lookup"><span data-stu-id="4e811-105">_**Topic Last Modified:** 2013-11-12_</span></span>

<span data-ttu-id="4e811-106">El informe de dispositivos tendría que llamarse más bien Informe de micrófono y altavoces porque el informe de dispositivos recupera las métricas relacionadas con las llamadas (como porcentaje de llamadas deficientes, eco y tiempo de conmutación de voz) agrupadas por los micrófonos y los altavoces utilizados durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="4e811-106">The Device Report might be better titled the Microphone and Speakers Report; that's because the Device Report retrieves call-related metrics (such as poor call percentage, echo, and voice switch time) grouped by the microphones and speakers used in the call.</span></span> <span data-ttu-id="4e811-107">Si está interesado en teléfonos IP (también conocidos como "dispositivos"), use el [Informe de inventario telefónico de IP en Lync Server 2013 en](lync-server-2013-ip-phone-inventory-report.md) su lugar.</span><span class="sxs-lookup"><span data-stu-id="4e811-107">If you are interested in IP phones (also commonly referred to as "devices"), use the [IP Phone Inventory Report in Lync Server 2013](lync-server-2013-ip-phone-inventory-report.md) instead.</span></span>

<span data-ttu-id="4e811-p102">El informe de dispositivos es muy útil para los administradores a la hora de determinar si un tipo concreto de dispositivo está sufriendo un número de llamadas de calidad deficiente superior al de otros. A su vez, puede influir en las decisiones que se tomen respecto a comprar nuevos dispositivos o sustituir los actuales.</span><span class="sxs-lookup"><span data-stu-id="4e811-p102">The Device Report is extremely useful for administrators in determining if a specific type of device is experiencing high volumes of poor quality calls than others. In turn, this could influence any decisions you must make when it comes time to buy new devices or to replace existing devices.</span></span>

<span data-ttu-id="4e811-p103">De forma predeterminada, la información mostrada en el informe de dispositivos también atañe al micrófono (el dispositivo de captura) y los altavoces o auriculares (los dispositivos de presentación) empleados durante la llamada. Por ejemplo, si hay varios usuarios que utilizan el siguiente dispositivo de captura y el siguiente dispositivo de presentación:</span><span class="sxs-lookup"><span data-stu-id="4e811-p103">By default, the information displayed in the Device Report is also based on the microphone (the capture device) and speakers/headset (the render device) used in the call. For example, suppose you have several users who use the following capture device and the following render device: By default, the information displayed in the Device Report is also based on the microphone (the capture device) and speakers/headset (the render device) used in the call. For example, suppose you have several users who use the following capture device and the following render device:</span></span>

  - <span data-ttu-id="4e811-113">Dispositivo de captura: micrófono (audio HD digital integrado SoundMAX)</span><span class="sxs-lookup"><span data-stu-id="4e811-113">Capture device -- Microphone (SoundMAX Integrated Digital HD Audio)</span></span>

  - <span data-ttu-id="4e811-114">Dispositivo de presentación: auriculares (Microsoft LifeChat LX-3000)</span><span class="sxs-lookup"><span data-stu-id="4e811-114">Render device -- Headset Earphone (Microsoft LifeChat LX-3000)</span></span>

<span data-ttu-id="4e811-115">Si estos usuarios realizaron un total de 254 llamadas, verá una entrada como la siguiente en el informe:</span><span class="sxs-lookup"><span data-stu-id="4e811-115">If those users made a total of 254 calls you'll see an entry like this in the report:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e811-116">Dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="4e811-116">Capture device</span></span></th>
<th><span data-ttu-id="4e811-117">Dispositivo de presentación</span><span class="sxs-lookup"><span data-stu-id="4e811-117">Render device</span></span></th>
<th><span data-ttu-id="4e811-118">Volumen de llamadas</span><span class="sxs-lookup"><span data-stu-id="4e811-118">Call volume</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e811-119">Micrófono (Audio HD digital integrado SoundMAX)</span><span class="sxs-lookup"><span data-stu-id="4e811-119">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="4e811-120">Auriculares (Microsoft LifeChat LX-3000)</span><span class="sxs-lookup"><span data-stu-id="4e811-120">Headset Earphone (Microsoft LifeChat LX-3000)</span></span></p></td>
<td><p><span data-ttu-id="4e811-121">254</span><span class="sxs-lookup"><span data-stu-id="4e811-121">254</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4e811-p104">Ahora, supongamos que tiene una serie de usuarios que utilizan ese mismo dispositivo de captura, pero un dispositivo de presentación diferente. En ese caso, tendrá una segunda entrada en el informe referente a esta combinación única de dispositivo de captura y dispositivo de presentación:</span><span class="sxs-lookup"><span data-stu-id="4e811-p104">Now, suppose you have a number of users who use that same capture device but a different render device. In that case, you'll have a second line entry in the report, one for that unique combination of capture device and render device:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e811-124">Dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="4e811-124">Capture device</span></span></th>
<th><span data-ttu-id="4e811-125">Dispositivo de presentación</span><span class="sxs-lookup"><span data-stu-id="4e811-125">Render device</span></span></th>
<th><span data-ttu-id="4e811-126">Volumen de llamadas</span><span class="sxs-lookup"><span data-stu-id="4e811-126">Call volume</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e811-127">Micrófono (Audio HD digital integrado SoundMAX)</span><span class="sxs-lookup"><span data-stu-id="4e811-127">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="4e811-128">Auriculares (Microsoft LifeChat LX-3000)</span><span class="sxs-lookup"><span data-stu-id="4e811-128">Headset Earphone (Microsoft LifeChat LX-3000)</span></span></p></td>
<td><p><span data-ttu-id="4e811-129">254</span><span class="sxs-lookup"><span data-stu-id="4e811-129">254</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-130">Micrófono (Audio HD digital integrado SoundMAX)</span><span class="sxs-lookup"><span data-stu-id="4e811-130">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="4e811-131">Altavoces (Audio HD digital integrado SoundMAX)</span><span class="sxs-lookup"><span data-stu-id="4e811-131">Speakers (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="4e811-132">319</span><span class="sxs-lookup"><span data-stu-id="4e811-132">319</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4e811-p105">Si prefiere ver los totales combinados de un dispositivo concreto (por ejemplo, del dispositivo de captura SoundMAX, independientemente de cual sea el dispositivo de presentación utilizado), seleccione la opción correspondiente en la lista desplegable Tipo de dispositivo (a saber, Dispositivo de captura o Dispositivo de presentación). Si selecciona dispositivo de captura, por ejemplo, el resultado será similar a:</span><span class="sxs-lookup"><span data-stu-id="4e811-p105">If you would rather see combined totals for a given device (for example, for the SoundMAX capture device, regardless of the render device used), select the appropriate option from the Device type dropdown list (either Capture device or Render device). If you select Capture device in this example, that will give you output similar to this:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e811-135">Dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="4e811-135">Capture device</span></span></th>
<th><span data-ttu-id="4e811-136">Volumen de llamadas</span><span class="sxs-lookup"><span data-stu-id="4e811-136">Call volume</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e811-137">Micrófono (Audio HD digital integrado SoundMAX)</span><span class="sxs-lookup"><span data-stu-id="4e811-137">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="4e811-138">573</span><span class="sxs-lookup"><span data-stu-id="4e811-138">573</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="accessing-the-device-report"></a><span data-ttu-id="4e811-139">Acceso al informe de dispositivos</span><span class="sxs-lookup"><span data-stu-id="4e811-139">Accessing the Device Report</span></span>

<span data-ttu-id="4e811-140">Generalmente, se accede al informe de dispositivos desde la página de inicio de Informes de supervisión.</span><span class="sxs-lookup"><span data-stu-id="4e811-140">The Device Report is typically accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="4e811-141">Sin embargo, si visualiza el [Informe de detalles de llamadas en Lync Server 2013](lync-server-2013-call-detail-report.md) puede explorar en profundidad el informe de dispositivos para un dispositivo específico haciendo clic en una de las siguientes métricas:</span><span class="sxs-lookup"><span data-stu-id="4e811-141">However, if you are viewing the [Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md) you can drill down to the Device Report for a specific device by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="4e811-142">Dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="4e811-142">Capture Device</span></span>

  - <span data-ttu-id="4e811-143">Dispositivo de presentación</span><span class="sxs-lookup"><span data-stu-id="4e811-143">Render Device</span></span>

<span data-ttu-id="4e811-144">En el informe de dispositivos, puede explorar en profundidad el [Informe de la lista de llamadas en Lync Server 2013](lync-server-2013-call-list-report.md) haciendo clic en cualquiera de las siguientes métricas:</span><span class="sxs-lookup"><span data-stu-id="4e811-144">From the Device Report you can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="4e811-145">Volumen de llamadas</span><span class="sxs-lookup"><span data-stu-id="4e811-145">Call volume</span></span>

  - <span data-ttu-id="4e811-146">Porcentaje de llamadas deficientes</span><span class="sxs-lookup"><span data-stu-id="4e811-146">Poor call percentage</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-device-report"></a><span data-ttu-id="4e811-147">Aprovechamiento del informe de dispositivos</span><span class="sxs-lookup"><span data-stu-id="4e811-147">Making the Best Use of the Device Report</span></span>

<span data-ttu-id="4e811-148">En lo que se refiere a los nombres de dispositivos, el informe de dispositivos es muy detallado. Por ejemplo, supongamos que tiene los siguientes dispositivos de captura:</span><span class="sxs-lookup"><span data-stu-id="4e811-148">When it comes to device names, the Device Report is extremely detailed; for example, suppose you have the following capture devices:</span></span>

  - <span data-ttu-id="4e811-149">Micrófono Aastra 3002 (2- Aastra 3002)</span><span class="sxs-lookup"><span data-stu-id="4e811-149">Aastra 3002 Microphone (2- Aastra 3002)</span></span>

  - <span data-ttu-id="4e811-150">Micrófono Aastra 3002 (3- Aastra 3002)</span><span class="sxs-lookup"><span data-stu-id="4e811-150">Aastra 3002 Microphone (3- Aastra 3002)</span></span>

  - <span data-ttu-id="4e811-151">Micrófono Aastra 3002 (Aastra 3002)</span><span class="sxs-lookup"><span data-stu-id="4e811-151">Aastra 3002 Microphone (Aastra 3002)</span></span>

  - <span data-ttu-id="4e811-152">Aastra 6725ip</span><span class="sxs-lookup"><span data-stu-id="4e811-152">Aastra 6725ip</span></span>

  - <span data-ttu-id="4e811-153">Micrófono Aastra 6725ip (10- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="4e811-153">Aastra 6725ip Microphone (10- Aastra 6725ip)</span></span>

  - <span data-ttu-id="4e811-154">Micrófono Aastra 6725ip (10- Aastra 6725ip)-V0</span><span class="sxs-lookup"><span data-stu-id="4e811-154">Aastra 6725ip Microphone (10- Aastra 6725ip)-V0</span></span>

  - <span data-ttu-id="4e811-155">Micrófono Aastra 6725ip (2- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="4e811-155">Aastra 6725ip Microphone (2- Aastra 6725ip)</span></span>

  - <span data-ttu-id="4e811-156">Micrófono Aastra 6725ip (3- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="4e811-156">Aastra 6725ip Microphone (3- Aastra 6725ip)</span></span>

  - <span data-ttu-id="4e811-157">Micrófono Aastra 6725ip (4- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="4e811-157">Aastra 6725ip Microphone (4- Aastra 6725ip)</span></span>

  - <span data-ttu-id="4e811-158">Micrófono Aastra 6725ip (5- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="4e811-158">Aastra 6725ip Microphone (5- Aastra 6725ip)</span></span>

  - <span data-ttu-id="4e811-159">Micrófono Aastra 6725ip (6- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="4e811-159">Aastra 6725ip Microphone (6- Aastra 6725ip)</span></span>

  - <span data-ttu-id="4e811-160">Micrófono Aastra 6725ip (7- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="4e811-160">Aastra 6725ip Microphone (7- Aastra 6725ip)</span></span>

  - <span data-ttu-id="4e811-161">Micrófono Aastra 6725ip (9- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="4e811-161">Aastra 6725ip Microphone (9- Aastra 6725ip)</span></span>

  - <span data-ttu-id="4e811-162">Micrófono Aastra 6725ip (9- Aastra 6725ip)-V0</span><span class="sxs-lookup"><span data-stu-id="4e811-162">Aastra 6725ip Microphone (9- Aastra 6725ip)-V0</span></span>

  - <span data-ttu-id="4e811-163">Micrófono Aastra 6725ip (Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="4e811-163">Aastra 6725ip Microphone (Aastra 6725ip)</span></span>

  - <span data-ttu-id="4e811-164">Micrófono Aastra 6725ip (Aastra 6725ip)-V0</span><span class="sxs-lookup"><span data-stu-id="4e811-164">Aastra 6725ip Microphone (Aastra 6725ip)-V0</span></span>

  - <span data-ttu-id="4e811-165">Micrófono Aastra 6725ip (USB Audio Device)</span><span class="sxs-lookup"><span data-stu-id="4e811-165">Aastra 6725ip Microphone (USB Audio Device)</span></span>

  - <span data-ttu-id="4e811-166">Micrófono Aastra 6725ip (USB Audio Device)-V0</span><span class="sxs-lookup"><span data-stu-id="4e811-166">Aastra 6725ip Microphone (USB Audio Device)-V0</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4e811-167">Recuerde que es posible que los nombres de los dispositivos de captura no sean los mismos si ejecuta versiones localizadas de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4e811-167">Keep in mind that capture device names might not be the same if you are running localized versions of Lync Server 2013.</span></span> <span data-ttu-id="4e811-168">El dispositivo Aastra 6725ip Microphone (Aastra 6725ip)-V0 en inglés, podría tener otro nombre en francés o en español.</span><span class="sxs-lookup"><span data-stu-id="4e811-168">A device named Aastra 6725ip Microphone (Aastra 6725ip)-V0 in US English could have a different name in French or Spanish.</span></span>



</div>

<span data-ttu-id="4e811-169">Habrá casos en los que desee trabajar con ese nivel de detalles, pero habrá otros en los que solo le interese saber cuántas llamadas utilizaron un micrófono Aastra, sea cual sea, sin importar el número de modelo.</span><span class="sxs-lookup"><span data-stu-id="4e811-169">Often times you'll want that level of detail; at other times, however, you might only be interested in how many calls use any Aastra microphone, regardless of model number.</span></span> <span data-ttu-id="4e811-170">Una forma de obtener información como esta es exportar los datos del informe de dispositivos a Microsoft Excel y, a continuación, guardarlos en un archivo de valores separados por comas (por ejemplo, los \\ dispositivos de datos C \\ \_Report.csv).</span><span class="sxs-lookup"><span data-stu-id="4e811-170">One way to get information like that is to export the Device Report data to Microsoft Excel and then save that data to a comma-separated values file (for example, C:\\Data\\Devices\_Report.csv).</span></span> <span data-ttu-id="4e811-171">A continuación, podrá utilizar un conjunto de comandos similar al siguiente para importar el archivo .CSB en Windows PowerShell y crear un informe del total de llamadas realizadas con un dispositivo de captura Aastra:</span><span class="sxs-lookup"><span data-stu-id="4e811-171">You can then use a set of commands similar to these to import the .CSV file into Windows PowerShell and report back the total number of calls made using an Aastra capture device:</span></span>

    $devices = Import-Csv "C:\Data\Device_Report.csv
    $sum = $devices | Where-Object {$_."Capture device" -match "Aastra"}
    $sum | foreach-object {[Int]$x = [Int]$x + [Int]$_."call volume"}
    $x

<span data-ttu-id="4e811-p109">Así se devolverá un único valor correspondiente al número total de llamadas realizadas con un dispositivo de captura Aastra. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4e811-p109">That will return a single value representing the total number of calls made using an Aastra capture device. For example:</span></span>

    384

</div>

<div>

## <a name="filters"></a><span data-ttu-id="4e811-174">Filtros</span><span class="sxs-lookup"><span data-stu-id="4e811-174">Filters</span></span>

<span data-ttu-id="4e811-p110">Los filtros se emplean para recuperar un conjunto de datos más específico o para ver los datos devueltos de diferentes formas. Por ejemplo, el informe de dispositivos permite filtrar elementos como el tipo de llamada (es decir, si la llamada era de un cliente), una llamada de conferencia o una llamada de red telefónica conmutada (RTC). También se puede elegir cómo agrupar los datos. En este caso, los dispositivos se agrupan por hora, día, semana o mes.</span><span class="sxs-lookup"><span data-stu-id="4e811-p110">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Device Report enables you to filter on such things as call type (that is, was the call a client call), a conference call, or a public switched telephone network (PSTN) call. You can also choose how data should be grouped. In this case, devices are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="4e811-179">En la tabla siguiente, se muestran los filtros que se pueden utilizar en el informe de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4e811-179">The following table lists the filters that you can use with the Device Report.</span></span>

### <a name="device-report-filters"></a><span data-ttu-id="4e811-180">Filtros del informe de dispositivos</span><span class="sxs-lookup"><span data-stu-id="4e811-180">Device Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e811-181">Nombre</span><span class="sxs-lookup"><span data-stu-id="4e811-181">Name</span></span></th>
<th><span data-ttu-id="4e811-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e811-182">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e811-183"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-183"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-p111">Fecha y hora de inicio del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de inicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="4e811-p111">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="4e811-186">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="4e811-186">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="4e811-p112">Si no escribe una hora de inicio, el informe se iniciará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="4e811-p112">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="4e811-189">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="4e811-189">7/7/2012</span></span></p>
<p><span data-ttu-id="4e811-190">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="4e811-190">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="4e811-191">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="4e811-191">7/3/2012</span></span></p>
<p><span data-ttu-id="4e811-192">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="4e811-192">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-193"><strong>Hasta</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-193"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-p113">Fecha y hora de finalización del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de finalización como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="4e811-p113">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="4e811-196">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="4e811-196">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="4e811-p114">Si no escribe una hora de finalización, el informe finalizará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="4e811-p114">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="4e811-199">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="4e811-199">7/7/2012</span></span></p>
<p><span data-ttu-id="4e811-200">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="4e811-200">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="4e811-201">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="4e811-201">7/3/2012</span></span></p>
<p><span data-ttu-id="4e811-202">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="4e811-202">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e811-203"><strong>Causa de la conmutación de voz</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-203"><strong>Voice switch cause</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-p115">Motivo por el que se tuvo que realizar una llamada en modo de dúplex medio para evitar el eco. En el modo de dúplex medio, la comunicación no puede realizarse en ambos sentidos a la vez, es similar al modo por turnos utilizado para comunicarse con un walkie-talkie. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="4e811-p115">Reason why a call had to be placed into half duplex mode in order to prevent echo. In half duplex mode, communication can travel in only one direction at a time, similar to the way users take turns when communicating with a walkie-talkie. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-207">[Todas]</span><span class="sxs-lookup"><span data-stu-id="4e811-207">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-208">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4e811-208">None</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-209">Marca de tiempo incorrecta</span><span class="sxs-lookup"><span data-stu-id="4e811-209">Bad timestamp</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-210">Eco</span><span class="sxs-lookup"><span data-stu-id="4e811-210">Echo</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-211">DNLP (procesador no lineal dinámico)</span><span class="sxs-lookup"><span data-stu-id="4e811-211">DNLP (dynamic nonlinear processor)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-212">Complejidad baja</span><span class="sxs-lookup"><span data-stu-id="4e811-212">Low complexity</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-213">Estado del dispositivo incorrecto</span><span class="sxs-lookup"><span data-stu-id="4e811-213">Bad device state</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-214">Eco posterior a AEC (cancelación de eco acústico)</span><span class="sxs-lookup"><span data-stu-id="4e811-214">Post-AEC echo (acoustic echo cancellation)</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-215"><strong>Causa del eco</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-215"><strong>Echo cause</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-p116">Motivo por el que se ha detectado en una llamada un eco que supera el nivel aceptado (en las telecomunicaciones, el eco es un reflejo del sonido, el mismo fenómeno que se produce cuando se grita en un pozo). Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="4e811-p116">Reason why echo above the accepted level was detected in a call. (In telecommunications, echo is a reflection of sound, the same phenomenon you will hear if you yell down to the bottom of a well.) Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-218">[Todas]</span><span class="sxs-lookup"><span data-stu-id="4e811-218">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-219">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4e811-219">None</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-220">Marca de tiempo incorrecta</span><span class="sxs-lookup"><span data-stu-id="4e811-220">Bad timestamp</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-221">Eco posterior a AEC (cancelación de eco acústico)</span><span class="sxs-lookup"><span data-stu-id="4e811-221">Post-AEC echo (acoustic echo cancellation)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-222">ANLP (procesador no lineal adaptable)</span><span class="sxs-lookup"><span data-stu-id="4e811-222">ANLP (adaptive nonlinear processor)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-223">DNLP (procesador no lineal dinámico)</span><span class="sxs-lookup"><span data-stu-id="4e811-223">DNLP (dynamic nonlinear processor)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-224">Recorte de micrófono</span><span class="sxs-lookup"><span data-stu-id="4e811-224">Microphone clipping</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e811-225"><strong>Tipo de llamada</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-225"><strong>Call type</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-p117">Indica el tipo de llamada realizada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="4e811-p117">Indicates the type of call that was made. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-228">[Todas]</span><span class="sxs-lookup"><span data-stu-id="4e811-228">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-229">Llamada de cliente</span><span class="sxs-lookup"><span data-stu-id="4e811-229">Client call</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-230">Llamada RTC</span><span class="sxs-lookup"><span data-stu-id="4e811-230">PSTN call</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-231">Llamada de conferencia</span><span class="sxs-lookup"><span data-stu-id="4e811-231">Conference call</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-232"><strong>Tipo de acceso</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-232"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-p118">Indica si el cliente había iniciado sesión en la red interna o en la externa cuando se realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="4e811-p118">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-235">[Todas]</span><span class="sxs-lookup"><span data-stu-id="4e811-235">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-236">Interno</span><span class="sxs-lookup"><span data-stu-id="4e811-236">Internal</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-237">Externo</span><span class="sxs-lookup"><span data-stu-id="4e811-237">External</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e811-238"><strong>Tipo de red</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-238"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-p119">Indica el tipo de red al que estaba conectado el cliente cuando realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="4e811-p119">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-241">[Todas]</span><span class="sxs-lookup"><span data-stu-id="4e811-241">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-242">Cableada</span><span class="sxs-lookup"><span data-stu-id="4e811-242">Wired</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-243">Inalámbrica</span><span class="sxs-lookup"><span data-stu-id="4e811-243">Wireless</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-244"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-244"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-p120">Indica si un cliente externo estaba utilizando una conexión de red privada virtual (VPN) cuando se realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="4e811-p120">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-247">[Todas]</span><span class="sxs-lookup"><span data-stu-id="4e811-247">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-248">VPN</span><span class="sxs-lookup"><span data-stu-id="4e811-248">VPN</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-249">Distinto de VPN</span><span class="sxs-lookup"><span data-stu-id="4e811-249">Non-VPN</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e811-250"><strong>Tipo de dispositivo</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-250"><strong>Device type</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-p121">Indica el tipo de dispositivo. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="4e811-p121">Indicates the type of device. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-253">Dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="4e811-253">Capture device</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-254">Dispositivo de presentación</span><span class="sxs-lookup"><span data-stu-id="4e811-254">Render device</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="4e811-255">Pareja de dispositivos de captura/presentación</span><span class="sxs-lookup"><span data-stu-id="4e811-255">Capture/Render device pair</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-256"><strong>Nombre del dispositivo</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-256"><strong>Device name</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-p122">Nombre del dispositivo de captura o presentación. Puede escribir el nombre completo del dispositivo o cualquier parte del mismo. Por ejemplo, para encontrar el dispositivo Micrófono (Microsoft LifeCam VX-1000), puede escribir el nombre completo del dispositivo del modo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4e811-p122">Name of the capture or render device. You can enter the complete device name or any portion of the device name. For example, to find the device Microphone (Microsoft LifeCam VX-1000.), you can enter the complete device name as follows:</span></span></p>
<p><span data-ttu-id="4e811-260">Micrófono (Microsoft LifeCam VX-1000)</span><span class="sxs-lookup"><span data-stu-id="4e811-260">Microphone (Microsoft LifeCam VX-1000.)</span></span></p>
<p><span data-ttu-id="4e811-p123">También puede escribir solo una parte del nombre. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4e811-p123">Or, you can enter just a portion of the name. For example:</span></span></p>
<p><span data-ttu-id="4e811-263">LifeCam</span><span class="sxs-lookup"><span data-stu-id="4e811-263">LifeCam</span></span></p>
<p><span data-ttu-id="4e811-264">Observe que el filtro anterior devuelve cualquier dispositivo que contenga la cadena &quot; LifeCam &quot; en su nombre.</span><span class="sxs-lookup"><span data-stu-id="4e811-264">Note that the preceding filter returns any device that contains the string &quot;LifeCam&quot; anywhere in its name.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="4e811-265">Métricas</span><span class="sxs-lookup"><span data-stu-id="4e811-265">Metrics</span></span>

<span data-ttu-id="4e811-266">En la tabla siguiente, se muestra la información que recoge el informe de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4e811-266">The following table lists the information provided in the Device Report.</span></span>

### <a name="device-report-metrics"></a><span data-ttu-id="4e811-267">Métricas del informe de dispositivos</span><span class="sxs-lookup"><span data-stu-id="4e811-267">Device Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e811-268">Nombre</span><span class="sxs-lookup"><span data-stu-id="4e811-268">Name</span></span></th>
<th><span data-ttu-id="4e811-269">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="4e811-269">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4e811-270">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e811-270">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e811-271"><strong>Dispositivo de captura</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-271"><strong>Capture device</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-272">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-272">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-273">Dispositivo (por ejemplo, un micrófono o una cámara web) utilizado para transmitir audio.</span><span class="sxs-lookup"><span data-stu-id="4e811-273">Device (for example, a microphone or webcam) used for transmitting audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-274"><strong>Dispositivo de presentación</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-274"><strong>Render device</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-275">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-275">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-276">Dispositivo (por ejemplo, unos auriculares o altavoces) utilizado para recibir audio.</span><span class="sxs-lookup"><span data-stu-id="4e811-276">Device (for example, a headset or speakers) used for receiving audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e811-277"><strong>Volumen de llamadas</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-277"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-278">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-278">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-279">Cantidad total de llamadas realizadas.</span><span class="sxs-lookup"><span data-stu-id="4e811-279">Total number of calls placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-280"><strong>Porcentaje de llamadas deficientes</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-280"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-281">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-281">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-282">Porcentaje de llamadas que se han clasificado como &quot; malas. &quot; Una llamada deficiente es cualquier llamada que al menos una de las métricas medidas superó el valor permitido (por ejemplo, una llamada que experimentó una vibración excesiva).</span><span class="sxs-lookup"><span data-stu-id="4e811-282">Percentage of calls that were classified as &quot;poor.&quot; A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e811-283"><strong>Usuarios únicos</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-283"><strong>Unique users</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-284">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-284">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-p124">Usuarios únicos que han utilizado el dispositivo. Si un usuario ha utilizado el dispositivo 13 veces, se contará como un usuario único, igual que un usuario que solo haya utilizado el dispositivo una única vez.</span><span class="sxs-lookup"><span data-stu-id="4e811-p124">Unique users who used the device. If a user used the device 13 times he or she would count as one unique user, the same as a user who only used the device a single time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-287"><strong>Relación de tiempo de conmutación de voz</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-287"><strong>Ratio of voice switch time</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-288">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-288">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-p125">Porcentaje de la llamada que se ha tenido que realizar en modo de dúplex medio para evitar el eco. En el modo de dúplex medio, la comunicación no puede realizarse en ambos sentidos a la vez, similar al modo por turnos utilizado para comunicarse con un walkie-talkie.</span><span class="sxs-lookup"><span data-stu-id="4e811-p125">Percentage of the call that had to be conducted in half duplex mode in order to prevent echo. In half duplex mode, communication can travel in only one direction at a time, similar to the way users take turns when communicating with a walkie-talkie.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e811-291"><strong>Relación de tiempo durante el que el micrófono estuvo sin funcionar</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-291"><strong>Ratio of microphone not functioning</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-292">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-292">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-p126">Porcentaje de la llamada en el que el dispositivo de captura no funcionaba a un nivel aceptable. Un valor elevado sugiere que los problemas de calidad de la llamada se deben principalmente a que el dispositivo de captura no funciona como debería.</span><span class="sxs-lookup"><span data-stu-id="4e811-p126">Percentage of the call in which the capture device was not functioning at an acceptable level. A high values suggests that quality issues with the call were primarily due to the capture device not working as expected.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-295"><strong>Relación de tiempo durante el que el altavoz estuvo sin funcionar</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-295"><strong>Ratio of speaker not functioning</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-296">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-296">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-p127">Porcentaje de la llamada en el que el dispositivo de presentación no funcionaba a un nivel aceptable. Un valor elevado sugiere que los problemas de calidad de la llamada se deben principalmente a que el dispositivo de presentación no funciona como debería.</span><span class="sxs-lookup"><span data-stu-id="4e811-p127">Percentage of the call in which the render device was not functioning at an acceptable level. A high values suggests that quality issues with the call were primarily due to the render device not working as expected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e811-299"><strong>Llamadas con conmutación de voz (%)</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-299"><strong>Calls with voice switch (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-300">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-300">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-p128">Porcentaje del total de llamadas que se han tenido que realizar en modo de dúplex medio. En el modo de dúplex medio, la comunicación no puede realizarse en ambos sentidos a la vez, algo similar al modo por turnos utilizado para comunicarse con un walkie-talkie.</span><span class="sxs-lookup"><span data-stu-id="4e811-p128">Percentage of the total calls which had to be placed into half duplex mode. In half duplex mode, communication can travel in only one direction at a time, similar to the way users take turns when communicating with a walkie-talkie.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-303"><strong>Eco del micrófono en (%)</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-303"><strong>Echo microphone in (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-304">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-304">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-p129">Porcentaje de tiempo para la detección del eco en la secuencia de captura del micrófono. En general, los valores son bajos para auriculares, y altos para altavoces de teléfono o independientes. En el caso de dispositivos que son compatibles con la cancelación del eco acústico incorporada, los valores altos indican filtraciones de eco. En otros dispositivos, esta métrica no debe utilizarse para evaluar la calidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e811-p129">Percentage of time when echo was detected in the microphone capture stream. Typically, values are low for headsets or handsets, and higher for speaker phones or stand-alone speakers. For devices that support on-board acoustic echo cancellation, high values indicate echo leak. For other devices, this metric should not be used to evaluate device quality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e811-309"><strong>Envío de eco (%)</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-309"><strong>Echo send (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-310">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-310">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-311">Porcentaje de eco transmitido a otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="4e811-311">Percentage of echo transmitted to other users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e811-312"><strong>Llamadas con eco (%)</strong></span><span class="sxs-lookup"><span data-stu-id="4e811-312"><strong>Calls with echo (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="4e811-313">Sí</span><span class="sxs-lookup"><span data-stu-id="4e811-313">Yes</span></span></p></td>
<td><p><span data-ttu-id="4e811-314">Porcentaje del total de llamadas cuyo eco superaba el nivel aceptable.</span><span class="sxs-lookup"><span data-stu-id="4e811-314">Percentage of the total calls that had echo exceeding the acceptable level.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4e811-315">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4e811-315">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

