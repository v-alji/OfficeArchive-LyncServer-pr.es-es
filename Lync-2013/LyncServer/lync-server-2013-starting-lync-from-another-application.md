---
title: 'Lync Server 2013: Inicio de Lync desde otra aplicación'
description: 'Lync Server 2013: iniciar Lync desde otra aplicación.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Starting Lync from another application
ms:assetid: 573b30b1-6590-4b24-8e96-a41be57cb0ef
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398376(v=OCS.15)
ms:contentKeyID: 48184184
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd64b8b9f335638b54a0bf6473b5d159c97a0e7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398130"
---
# <a name="starting-lync-from-another-application"></a><span data-ttu-id="829c4-103">Iniciar Lync desde otra aplicación</span><span class="sxs-lookup"><span data-stu-id="829c4-103">Starting Lync from another application</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="829c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="829c4-104">

<span> </span></span></span>

<span data-ttu-id="829c4-105">_**Última modificación del tema:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="829c4-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="829c4-106">Puede usar parámetros de la línea de comandos para iniciar rápidamente Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="829c4-106">You can use command-line parameters to quick-start Lync 2013.</span></span> <span data-ttu-id="829c4-107">Por ejemplo, si un usuario hace clic en un número de teléfono de otra aplicación, la aplicación puede iniciar una instancia de Lync 2013 e iniciar una llamada a ese número.</span><span class="sxs-lookup"><span data-stu-id="829c4-107">For example, if a user clicks a phone number in another application, the application can start an instance of Lync 2013 and initiate a call to that number.</span></span>

<span data-ttu-id="829c4-108">Lync 2013 también puede reconocer una lista de nombres de contactos delimitados por punto y coma para las conferencias de varias partes.</span><span class="sxs-lookup"><span data-stu-id="829c4-108">Lync 2013 can also recognize a semicolon-delimited list of contact names for multiparty conferencing.</span></span>

<span data-ttu-id="829c4-109">Si Lync 2013 está configurado para iniciar sesión automáticamente al iniciarse, al iniciar Lync 2013 con parámetros de línea de comandos se abrirá la ventana principal de Lync.</span><span class="sxs-lookup"><span data-stu-id="829c4-109">If Lync 2013 is configured to automatically sign in when started, then starting Lync 2013 with command-line parameters will open the Lync main window.</span></span> <span data-ttu-id="829c4-110">Si Lync no está configurado para iniciar sesión automáticamente al iniciarse, se abrirá la ventana de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="829c4-110">If Lync is not configured to automatically sign in when started, the sign-in window opens.</span></span>

<span data-ttu-id="829c4-111">En la tabla siguiente se muestran los parámetros disponibles.</span><span class="sxs-lookup"><span data-stu-id="829c4-111">The following table shows the available parameters.</span></span>

### <a name="lync-2013-command-line-parameters"></a><span data-ttu-id="829c4-112">2013 Command-Line parámetros de Lync</span><span class="sxs-lookup"><span data-stu-id="829c4-112">Lync 2013 Command-Line Parameters</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="829c4-113">Extensiones</span><span class="sxs-lookup"><span data-stu-id="829c4-113">Extension</span></span></th>
<th><span data-ttu-id="829c4-114">Formato de datos</span><span class="sxs-lookup"><span data-stu-id="829c4-114">Format of Data</span></span></th>
<th><span data-ttu-id="829c4-115">Action</span><span class="sxs-lookup"><span data-stu-id="829c4-115">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="829c4-116">Tel</span><span class="sxs-lookup"><span data-stu-id="829c4-116">tel:</span></span></p></td>
<td><p><span data-ttu-id="829c4-117">URI de Tel</span><span class="sxs-lookup"><span data-stu-id="829c4-117">tel URI</span></span></p></td>
<td><p><span data-ttu-id="829c4-118">Abre la ventana de conversación de una llamada de audio, pero no marca el número especificado.</span><span class="sxs-lookup"><span data-stu-id="829c4-118">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="829c4-119">callto</span><span class="sxs-lookup"><span data-stu-id="829c4-119">callto:</span></span></p></td>
<td><p><span data-ttu-id="829c4-120">Tel:, SIP:, o URI de Tel.</span><span class="sxs-lookup"><span data-stu-id="829c4-120">tel:, sip:, or typeable tel URI</span></span></p></td>
<td><p><span data-ttu-id="829c4-121">Abre la ventana de conversación de una llamada de audio, pero no marca el número especificado.</span><span class="sxs-lookup"><span data-stu-id="829c4-121">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="829c4-122">SIP</span><span class="sxs-lookup"><span data-stu-id="829c4-122">sip:</span></span></p></td>
<td><p><span data-ttu-id="829c4-123">URI del SIP</span><span class="sxs-lookup"><span data-stu-id="829c4-123">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="829c4-124">Abre la ventana de conversación con el identificador uniforme de recursos (URI) SIP especificado en la lista de participantes.</span><span class="sxs-lookup"><span data-stu-id="829c4-124">Opens the Conversation window with the specified SIP Uniform Resource Identifier (URI) in the participant list.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="829c4-125">SIPs</span><span class="sxs-lookup"><span data-stu-id="829c4-125">Sips:</span></span></p></td>
<td><p><span data-ttu-id="829c4-126">URI del SIP</span><span class="sxs-lookup"><span data-stu-id="829c4-126">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="829c4-127">Si Lync 2013 está configurado para usar el protocolo seguridad de la capa de transporte (TLS), funciona exactamente igual que SIP:.</span><span class="sxs-lookup"><span data-stu-id="829c4-127">If Lync 2013 is configured to use the Transport Layer Security (TLS) protocol, functions exactly like sip:.</span></span> <span data-ttu-id="829c4-128">Si no se usa TLS, se muestra un cuadro de diálogo que informa al usuario de que se requiere un mayor nivel de seguridad.</span><span class="sxs-lookup"><span data-stu-id="829c4-128">If TLS is not being used, displays a dialog box informing the user that a higher level of security is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="829c4-129">Conferencia</span><span class="sxs-lookup"><span data-stu-id="829c4-129">conf:</span></span></p></td>
<td><p><span data-ttu-id="829c4-130">URI SIP de conferencia para unirse</span><span class="sxs-lookup"><span data-stu-id="829c4-130">SIP URI of conference to join</span></span></p></td>
<td><p><span data-ttu-id="829c4-131">Si el URI es self, crea una instancia del foco y abre la vista de solo configuración.</span><span class="sxs-lookup"><span data-stu-id="829c4-131">If URI is self, instantiates the focus and brings up roster-only view.</span></span> <span data-ttu-id="829c4-132">De lo contrario, muestra la vista de lista, pero no envía la invitación.</span><span class="sxs-lookup"><span data-stu-id="829c4-132">Otherwise, brings up roster view but does not send INVITE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="829c4-133">mensajería</span><span class="sxs-lookup"><span data-stu-id="829c4-133">im:</span></span></p></td>
<td><p><span data-ttu-id="829c4-134">URI del SIP</span><span class="sxs-lookup"><span data-stu-id="829c4-134">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="829c4-135">Muestra una ventana de conversación de mensajería instantánea solo con el URI del SIP.</span><span class="sxs-lookup"><span data-stu-id="829c4-135">Displays an instant messaging (IM)-only Conversation window with the SIP URI.</span></span> <span data-ttu-id="829c4-136">Acepta varios URI de SIP especificados entre corchetes angulares ( &lt; &gt; ) sin separador.</span><span class="sxs-lookup"><span data-stu-id="829c4-136">Accepts multiple SIP URIs specified inside angle brackets (&lt;&gt;) without any separator.</span></span></p>
<pre><code>im:&lt;sip:user1@host&gt;&lt;sip:user2@host&gt;</code></pre></td>
</tr>
</tbody>
</table>


<span data-ttu-id="829c4-137">En la tabla siguiente se muestran algunos ejemplos de estos parámetros de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="829c4-137">The following table provides examples of these command-line parameters.</span></span>

### <a name="command-line-parameter-examples"></a><span data-ttu-id="829c4-138">Command-Line ejemplos de parámetros</span><span class="sxs-lookup"><span data-stu-id="829c4-138">Command-Line Parameter Examples</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="829c4-139">Vez</span><span class="sxs-lookup"><span data-stu-id="829c4-139">Instance</span></span></th>
<th><span data-ttu-id="829c4-140">Obtenidos</span><span class="sxs-lookup"><span data-stu-id="829c4-140">Results</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="829c4-141">Tel: + 14255550101</span><span class="sxs-lookup"><span data-stu-id="829c4-141">Tel:+14255550101</span></span></p></td>
<td><p><span data-ttu-id="829c4-142">Abre una vista de solo teléfono con + 14255550101.</span><span class="sxs-lookup"><span data-stu-id="829c4-142">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="829c4-143">Callto: Tel: + 14255550101</span><span class="sxs-lookup"><span data-stu-id="829c4-143">Callto:tel:+ 14255550101</span></span></p></td>
<td><p><span data-ttu-id="829c4-144">Abre una vista de solo teléfono con + 14255550101.</span><span class="sxs-lookup"><span data-stu-id="829c4-144">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="829c4-145">Callto:sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="829c4-145">Callto:sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="829c4-146">Abre una vista solo para teléfono con kazuto@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="829c4-146">Opens a phone-only view with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="829c4-147">sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="829c4-147">sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="829c4-148">Abre una ventana de conversación con kazuto@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="829c4-148">Opens a Conversation window with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="829c4-149">conf: SIP:https://meet.contoso.com/kazuto/7322994</span><span class="sxs-lookup"><span data-stu-id="829c4-149">conf:sip:https://meet.contoso.com/kazuto/7322994</span></span></p></td>
<td><p><span data-ttu-id="829c4-150">Abre una ventana de conversación y muestra las opciones de combinación de audio de la reunión.</span><span class="sxs-lookup"><span data-stu-id="829c4-150">Opens a Conversation window and displays meeting audio join options.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="829c4-151">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="829c4-151">


</div>

<span> </span>

</div>

</div>

</span></span></div>

