---
title: 'Lync Server 2013: asignación de directivas de presencia por usuario'
description: 'Lync Server 2013: asignación de directivas de presencia por usuario.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning per-user presence policies
ms:assetid: fd1097b7-248d-4b78-8c43-456b03257c18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182614(v=OCS.15)
ms:contentKeyID: 48185955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c3d4b4bda0c4bb85065d546fdbb4b2578db0e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399972"
---
# <a name="assigning-per-user-presence-policies-in-lync-server-2013"></a><span data-ttu-id="910b3-103">Asignar directivas de presencia por usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="910b3-103">Assigning per-user presence policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="910b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="910b3-104">

<span> </span></span></span>

<span data-ttu-id="910b3-105">_**Última modificación del tema:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="910b3-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="910b3-106">Una directiva de presencia es un conjunto de límites y restricciones que afectan a la presencia.</span><span class="sxs-lookup"><span data-stu-id="910b3-106">A presence policy is a set of limits and restrictions that affect presence.</span></span> <span data-ttu-id="910b3-107">La siguiente tabla describe la configuración de la Directiva de presencia disponible en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="910b3-107">The following table describes the presence policy settings available in Lync Server 2013.</span></span>

### <a name="presence-policy-settings"></a><span data-ttu-id="910b3-108">Configuración de la Directiva de presencia</span><span class="sxs-lookup"><span data-stu-id="910b3-108">Presence Policy Settings</span></span>

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
<th><span data-ttu-id="910b3-109">Nombre XML</span><span class="sxs-lookup"><span data-stu-id="910b3-109">XML name</span></span></th>
<th><span data-ttu-id="910b3-110">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="910b3-110">Display name</span></span></th>
<th><span data-ttu-id="910b3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="910b3-111">Description</span></span></th>
<th><span data-ttu-id="910b3-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="910b3-112">Type</span></span></th>
<th><span data-ttu-id="910b3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="910b3-113">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="910b3-114">CategorySubscriptions</span><span class="sxs-lookup"><span data-stu-id="910b3-114">CategorySubscriptions</span></span></p></td>
<td><p><span data-ttu-id="910b3-115">Número máximo de suscripciones de categorías de suscriptores</span><span class="sxs-lookup"><span data-stu-id="910b3-115">Maximum Number of Subscriber Category Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="910b3-116">Limita la cantidad de suscripciones de categorías de abonados.</span><span class="sxs-lookup"><span data-stu-id="910b3-116">Limits the number of subscriber category subscriptions.</span></span> <span data-ttu-id="910b3-117">Por ejemplo, cuando Communicator se suscribe a la presencia de un usuario, obtiene una suscripción de categoría para cada una de las categorías de tarjeta de contacto, datos de calendario, notas, servicios y estado.</span><span class="sxs-lookup"><span data-stu-id="910b3-117">For example, when Communicator subscribes to a user’s presence, it obtains a category subscription for each of the contact card, calendar data, notes, services, and state categories.</span></span></p>
<p><span data-ttu-id="910b3-118">El valor 0 significa que otros usuarios no pueden suscribirse al objeto de usuario o contacto.</span><span class="sxs-lookup"><span data-stu-id="910b3-118">A setting of 0 means that the user or contact object cannot be subscribed to by others.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="910b3-119">Esta configuración puede tener un impacto significativo en el rendimiento si se establece en un número alto y el usuario promedio tiene un gran número de usuarios que se suscriben a su presencia.</span><span class="sxs-lookup"><span data-stu-id="910b3-119">This setting can have a significant impact on performance if it is set to a high number, and the average user has a large number of users subscribing to his or her presence.</span></span>


</div></td>
<td><p><span data-ttu-id="910b3-120">Entero</span><span class="sxs-lookup"><span data-stu-id="910b3-120">Integer</span></span></p></td>
<td><p><span data-ttu-id="910b3-121">0-3000</span><span class="sxs-lookup"><span data-stu-id="910b3-121">0-3000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="910b3-122">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="910b3-122">PromptedSubscribers</span></span></p></td>
<td><p><span data-ttu-id="910b3-123">Número máximo de alertas de suscripción de presencia en cola</span><span class="sxs-lookup"><span data-stu-id="910b3-123">Maximum Number of Queued Presence Subscription Alerts</span></span></p></td>
<td><p><span data-ttu-id="910b3-124">Limita el número de entradas de la tabla suscriptores solicitada.</span><span class="sxs-lookup"><span data-stu-id="910b3-124">Limits the number of entries in the prompted subscribers table.</span></span> <span data-ttu-id="910b3-125">Esta configuración determina el número máximo de mensajes que se pueden poner en cola para un usuario dado.</span><span class="sxs-lookup"><span data-stu-id="910b3-125">This setting determines the maximum number of prompts that can be queued for a given user.</span></span> <span data-ttu-id="910b3-126">Por ejemplo, cuando el usuario se suscribe a la presencia del usuario B, recibe un mensaje que indica que el usuario A ya está suscrito al usuario B y se crea un mensaje de confirmación en la tabla de suscriptores solicitada por el usuario B.</span><span class="sxs-lookup"><span data-stu-id="910b3-126">For example, when user A subscribes to user B’s presence, user B receives a prompt that user A is now subscribed to user B, and an acknowledgement prompt is created in user B’s prompted subscribers table.</span></span> <span data-ttu-id="910b3-127">Después de que el usuario B acepte o confirme la suscripción, se eliminará la solicitud de confirmación de la tabla de suscriptores solicitada por el usuario B.</span><span class="sxs-lookup"><span data-stu-id="910b3-127">After user B accepts, or acknowledges, the subscription, the acknowledgement prompt is removed from user B’s prompted subscribers table.</span></span></p>
<p><span data-ttu-id="910b3-128">Un valor de 0 significa que no se le pide confirmación al usuario cuando alguien se suscribe a su presencia.</span><span class="sxs-lookup"><span data-stu-id="910b3-128">A setting of 0 means that the user is not prompted when someone subscribes to his or her presence.</span></span></p></td>
<td><p><span data-ttu-id="910b3-129">Entero o token</span><span class="sxs-lookup"><span data-stu-id="910b3-129">Integer or Token</span></span></p></td>
<td><p><span data-ttu-id="910b3-130">0-500</span><span class="sxs-lookup"><span data-stu-id="910b3-130">0-500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="910b3-131">De forma predeterminada, la Directiva y el servicio **predeterminados** : las directivas de presencia **media** se instalan al implementar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="910b3-131">By default, the **Default Policy** and **Service: Medium** presence policies are installed when you deploy Lync Server.</span></span> <span data-ttu-id="910b3-132">En la siguiente tabla se describen las opciones específicas de las dos directivas de presencia.</span><span class="sxs-lookup"><span data-stu-id="910b3-132">The following table describes the specific settings of the two presence policies.</span></span>

### <a name="presence-policies"></a><span data-ttu-id="910b3-133">Directivas de presencia</span><span class="sxs-lookup"><span data-stu-id="910b3-133">Presence Policies</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="910b3-134">Nombre de la directiva</span><span class="sxs-lookup"><span data-stu-id="910b3-134">Policy name</span></span></th>
<th><span data-ttu-id="910b3-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="910b3-135">Description</span></span></th>
<th><span data-ttu-id="910b3-136">CategorySubscriptions</span><span class="sxs-lookup"><span data-stu-id="910b3-136">CategorySubscriptions</span></span></th>
<th><span data-ttu-id="910b3-137">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="910b3-137">PromptedSubscribers</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="910b3-138">Directiva predeterminada</span><span class="sxs-lookup"><span data-stu-id="910b3-138">Default Policy</span></span></p></td>
<td><p><span data-ttu-id="910b3-139">Directiva para usuarios típicos.</span><span class="sxs-lookup"><span data-stu-id="910b3-139">Policy for typical users.</span></span> <span data-ttu-id="910b3-140">Esta es la Directiva de presencia predeterminada.</span><span class="sxs-lookup"><span data-stu-id="910b3-140">This is the default presence policy.</span></span></p></td>
<td><p><span data-ttu-id="910b3-141">1000</span><span class="sxs-lookup"><span data-stu-id="910b3-141">1000</span></span></p></td>
<td><p><span data-ttu-id="910b3-142">200</span><span class="sxs-lookup"><span data-stu-id="910b3-142">200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="910b3-143">Servicio: medio</span><span class="sxs-lookup"><span data-stu-id="910b3-143">Service: Medium</span></span></p></td>
<td><p><span data-ttu-id="910b3-144">Directiva para las aplicaciones que requieren más usuarios para suscribirse a la presencia del objeto.</span><span class="sxs-lookup"><span data-stu-id="910b3-144">Policy for applications that require more users to subscribe to the object’s presence.</span></span></p></td>
<td><p><span data-ttu-id="910b3-145">1000</span><span class="sxs-lookup"><span data-stu-id="910b3-145">1000</span></span></p></td>
<td><p><span data-ttu-id="910b3-146">,0</span><span class="sxs-lookup"><span data-stu-id="910b3-146">0</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="910b3-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="910b3-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

