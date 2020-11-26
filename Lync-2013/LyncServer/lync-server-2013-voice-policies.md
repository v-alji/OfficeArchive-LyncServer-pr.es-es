---
title: 'Lync Server 2013: Directivas de voz'
description: 'Lync Server 2013: directivas de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Voice policies
ms:assetid: b7433c62-9d8c-48af-89a0-19f0d34806ec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412891(v=OCS.15)
ms:contentKeyID: 48185223
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b85e69c83a8f964d9114a83abe6978f040f044d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438641"
---
# <a name="voice-policies-in-lync-server-2013"></a><span data-ttu-id="86bb0-103">Directivas de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86bb0-103">Voice policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="86bb0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="86bb0-104">

<span> </span></span></span>

<span data-ttu-id="86bb0-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="86bb0-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="86bb0-106">*Las directivas de voz* de Lync Server definen lo siguiente para cada usuario, sitio u organización a la que se asigna la Directiva:</span><span class="sxs-lookup"><span data-stu-id="86bb0-106">Lync Server *voice policies* define the following for each user, site, or organization that is assigned the policy:</span></span>

  - <span data-ttu-id="86bb0-107">Un conjunto de características de llamadas que se pueden habilitar o deshabilitar para determinar la funcionalidad de telefonía IP empresarial disponible para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="86bb0-107">A set of calling features that can be enabled or disabled to determine the Enterprise Voice functionality available to users.</span></span>

  - <span data-ttu-id="86bb0-108">Un conjunto de registros de uso de la red telefónica conmutada (RTC) que definen qué tipo de llamadas están autorizadas.</span><span class="sxs-lookup"><span data-stu-id="86bb0-108">A set of public switched telephone network (PSTN) usage records that define what types of calls are authorized.</span></span>

<div>

## <a name="planning-for-voice-policies"></a><span data-ttu-id="86bb0-109">Planificación de directivas de voz</span><span class="sxs-lookup"><span data-stu-id="86bb0-109">Planning for Voice Policies</span></span>

<span data-ttu-id="86bb0-110">Los pasos siguientes le ayudarán a planear las directivas de voz que necesitará para su implementación de telefonía IP empresarial:</span><span class="sxs-lookup"><span data-stu-id="86bb0-110">The following steps will help you plan the voice policies that you will need for your Enterprise Voice deployment:</span></span>

  - <span data-ttu-id="86bb0-111">Determina cómo configurarás la directiva de voz global (la directiva de voz predeterminada que se instala con el producto).</span><span class="sxs-lookup"><span data-stu-id="86bb0-111">Determine how you will configure your global voice policy (the default voice policy that is installed with the product).</span></span> <span data-ttu-id="86bb0-112">Esta Directiva se aplicará a todos los usuarios de telefonía de telefonía empresarial a los que no se les haya asignado explícitamente una directiva de sitio o usuario.</span><span class="sxs-lookup"><span data-stu-id="86bb0-112">This policy will apply to all Enterprise Voice users who are not explicitly assigned a site-level or per-user policy.</span></span>

  - <span data-ttu-id="86bb0-113">Identifica cualquier directiva de voz de sitio que puedas necesitar.</span><span class="sxs-lookup"><span data-stu-id="86bb0-113">Identify any site-level voice policies that you might need.</span></span>

  - <span data-ttu-id="86bb0-114">Identifica cualquier directiva de voz de usuario que puedas necesitar.</span><span class="sxs-lookup"><span data-stu-id="86bb0-114">Identify any per-user voice policies that you might need.</span></span>

  - <span data-ttu-id="86bb0-115">Decide qué características de llamada deseas habilitar para cada directiva de voz.</span><span class="sxs-lookup"><span data-stu-id="86bb0-115">Decide which call features to enable for each voice policy.</span></span>

  - <span data-ttu-id="86bb0-116">Determina qué registros de uso de RTC deseas configurar para cada directiva de voz.</span><span class="sxs-lookup"><span data-stu-id="86bb0-116">Determine what PSTN usage records to configure for each voice policy.</span></span>

<div>

## <a name="voice-policy-scope"></a><span data-ttu-id="86bb0-117">Ámbito de directiva de voz</span><span class="sxs-lookup"><span data-stu-id="86bb0-117">Voice Policy Scope</span></span>

<span data-ttu-id="86bb0-118">El *ámbito de directiva de voz* determina el nivel jerárquico en el que se puede aplicar la directiva.</span><span class="sxs-lookup"><span data-stu-id="86bb0-118">*Voice policy scope* determines the hierarchical level at which the policy can be applied.</span></span> <span data-ttu-id="86bb0-119">En Lync Server, puede configurar directivas de voz con los siguientes niveles de ámbito (enumerados de la más específica a la más general).</span><span class="sxs-lookup"><span data-stu-id="86bb0-119">In Lync Server, you can configure voice policies with the following scope levels (listed from the most specific to the most general).</span></span>

  - <span data-ttu-id="86bb0-p103">La **directiva de voz de usuario** se puede asignar a usuarios, grupos u objetos de contacto individuales. Es la directiva de nivel más bajo. Las directivas de voz de usuario se pueden implementar para habilitar características para usuarios y grupos determinados en un sitio, pero no para otros en el mismo sitio. Por ejemplo, puedes deshabilitar las llamadas de larga distancia para algunos empleados. Con el fin de asignar una directiva de voz, un objeto de contacto se considera un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="86bb0-p103">**User voice policy** can be assigned to individual users, groups, or contact objects. This is the lowest level policy. User voice policies can be deployed to enable features for certain users or groups at a site, but not for others in the same site. For example, you may want to disable long distance dialing for some employees. For the purpose of assigning a voice policy, a contact object is treated as an individual user.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="86bb0-125">Le recomendamos que implemente una directiva de voz de usuario para los usuarios de la empresa de voz de un sitio de sucursal que estén registrados en la implementación de sitio central o los usuarios que estén registrados en un dispositivo de sucursal con la supervivencia.</span><span class="sxs-lookup"><span data-stu-id="86bb0-125">We recommend that you deploy a user voice policy for branch site Enterprise Voice users who are registered with the central site deployment, or users who are registered on a Survivable Branch Appliance.</span></span>

    
    </div>

  - <span data-ttu-id="86bb0-p104">La **directiva de voz de sitio** se aplica a todo un sitio, excepto para los usuarios, grupos u objetos de contacto a los que se ha asignado una directiva de voz de usuario. Para definir una directiva de voz de sitio, necesitas especificar el sitio al que se aplica la directiva. Si no se asignó una directiva de voz de usuario, se usa la directiva de voz de sitio.</span><span class="sxs-lookup"><span data-stu-id="86bb0-p104">**Site voice policy** applies to an entire site, except for any users, groups, or contact objects that are assigned a user voice policy. To define a site voice policy, you must specify the site to which the policy applies. If a user voice policy is not assigned, the site voice policy is used.</span></span>

  - <span data-ttu-id="86bb0-129">La **directiva de voz global** es la directiva de voz predeterminada que se instala con el producto.</span><span class="sxs-lookup"><span data-stu-id="86bb0-129">**Global voice policy** is the default voice policy that is installed with the product.</span></span> <span data-ttu-id="86bb0-130">Puedes editar la directiva de voz global para cumplir las necesidades específicas de tu organización, pero no puedes cambiar su nombre ni eliminarla.</span><span class="sxs-lookup"><span data-stu-id="86bb0-130">You can edit the global voice policy to meet the specific needs of your organization, but you cannot rename or delete it.</span></span> <span data-ttu-id="86bb0-131">Esta directiva de voz se aplica a todos los usuarios, grupos y objetos de contacto de Enterprise Voice de su implementación, a menos que configure y asigne una directiva de voz con un ámbito más específico.</span><span class="sxs-lookup"><span data-stu-id="86bb0-131">This voice policy applies to all Enterprise Voice users, groups, and contact objects in your deployment unless you configure and assign a voice policy with more specific scope.</span></span> <span data-ttu-id="86bb0-132">Si deseas deshabilitar esta directiva en su totalidad, asegúrate de que todos los sitios y todos los usuarios tengan asignadas directivas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="86bb0-132">If you want to disable this policy entirely, be sure that all sites and users have custom policies assigned to them.</span></span>

</div>

<div>

## <a name="call-features"></a><span data-ttu-id="86bb0-133">Características de llamada</span><span class="sxs-lookup"><span data-stu-id="86bb0-133">Call Features</span></span>

<span data-ttu-id="86bb0-134">Puedes habilitar o deshabilitar las siguientes características de llamada para cada directiva de voz:</span><span class="sxs-lookup"><span data-stu-id="86bb0-134">You can enable or disable the following call features for each voice policy:</span></span>

  - <span data-ttu-id="86bb0-p106">El **desvío de llamadas** permite que los usuarios desvíen llamadas a otros teléfonos y dispositivos de cliente. Está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86bb0-p106">**Call forwarding** enables users to forward calls to other phones and client devices. Enabled by default.</span></span>

  - <span data-ttu-id="86bb0-p107">La **delegación** permite a los usuarios especificar otros usuarios para que realicen y reciban llamadas en su nombre. Está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86bb0-p107">**Delegation** enables users to specify other users to send and receive calls on their behalf. Enabled by default.</span></span>

  - <span data-ttu-id="86bb0-p108">La **transferencia de llamadas** permite a los usuarios transferir llamadas a otros usuarios. Está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86bb0-p108">**Call transfer** enables users to transfer calls to other users. Enabled by default.</span></span>

  - <span data-ttu-id="86bb0-p109">El **estacionamiento de llamadas** permite a los usuarios estacionar llamadas y atenderlas en otro teléfono o cliente. Está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86bb0-p109">**Call park** enables users to park calls and then pick up the call from a different phone or client. Disabled by default.</span></span>

  - <span data-ttu-id="86bb0-p110">La característica de **llamadas simultáneas** permite que las llamadas entrantes suenen en un teléfono adicional (por ejemplo, un móvil) u otros dispositivos de extremo. Está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86bb0-p110">**Simultaneous ringing** enables incoming calls to ring on an additional phone (for example, a mobile phone) or other endpoint devices. Enabled by default.</span></span>

  - <span data-ttu-id="86bb0-p111">La **llamada de equipo** permite a los usuarios de un equipo determinado responder llamadas por otros miembros del equipo. Está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86bb0-p111">**Team call** enables users on a defined team to answer calls for other members of the team. Enabled by default.</span></span>

  - <span data-ttu-id="86bb0-p112">El **desvío de RTC** permite que las llamadas realizadas por usuarios que tienen asignada esta directiva a otros usuarios de la empresa se puedan desviar en la red telefónica conmutada (RTC) si la red WAN está saturada o no disponible. Está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86bb0-p112">**PSTN reroute** enables calls made by users who are assigned this policy to other enterprise users to be rerouted on the public switched telephone network (PSTN) if the WAN is congested or unavailable. Enabled by default.</span></span>

  - <span data-ttu-id="86bb0-p113">El **reemplazo de directiva de ancho de banda** permite a los administradores cambiar las decisiones de la directiva del servicio de control de admisión de llamadas para un usuario en concreto. Está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86bb0-p113">**Bandwidth policy override** enables administrators to override call admission control policy decisions for a particular user. Disabled by default.</span></span>

  - <span data-ttu-id="86bb0-151">El **seguimiento de llamadas malintencionadas** permite a los usuarios denunciar llamadas malintencionadas mediante el cliente de Lync y, a continuación, marca dichas llamadas en los registros de detalles de llamadas.</span><span class="sxs-lookup"><span data-stu-id="86bb0-151">**Malicious call tracing** enables users to report malicious calls by using the Lync client, and then flags such calls in the call detail records.</span></span> <span data-ttu-id="86bb0-152">Está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86bb0-152">Disabled by default.</span></span>

  - <span data-ttu-id="86bb0-153">El **escape en correo de voz** impide que las llamadas se redirijan de inmediato al sistema de correo de voz del teléfono móvil del usuario cuando se configura la característica de llamadas simultáneas y el teléfono está apagado, sin batería o fuera del alcance, y se basa en un valor del temporizador.</span><span class="sxs-lookup"><span data-stu-id="86bb0-153">**Voicemail escape** prevents calls from being immediately routed to the user’s mobile phone voicemail system when simultaneous ringing is configured and the phone is turned off, out of battery, or out of range, and is based on a timer value.</span></span> <span data-ttu-id="86bb0-154">Esta configuración habilita y deshabilita el temporizador, y establece su valor.</span><span class="sxs-lookup"><span data-stu-id="86bb0-154">This setting enables and disables the timer and sets the value of the timer.</span></span> <span data-ttu-id="86bb0-155">Solo se puede configurar mediante el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="86bb0-155">It can be configured only by using the Lync Server Management Shell.</span></span> <span data-ttu-id="86bb0-156">Está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86bb0-156">Disabled by default.</span></span>

  - <span data-ttu-id="86bb0-157">El **desvío de llamadas y los usos simultáneos de RTC** permiten a los administradores especificar el mismo uso de la RTC que la Directiva de voz para el desvío de llamadas y las llamadas simultáneas, restringir el desvío de llamadas y las llamadas simultáneas a usuarios internos de Lync, o especificar un uso de RTC personalizado que sea diferente del uso de RTC de la Directiva de voz.</span><span class="sxs-lookup"><span data-stu-id="86bb0-157">**Call forwarding and simultaneous ringing PSTN usages** enables administrators to specify the same PSTN usage as the voice policy for call forwarding and simultaneous ringing, restrict call forwarding and simultaneous ringing to internal Lync users only, or specify a custom PSTN usage that is different from the voice policy’s PSTN usage.</span></span> <span data-ttu-id="86bb0-158">La opción predeterminada es usar el mismo uso de RTC que la directiva de voz para el desvío de llamadas y las llamadas simultáneas.</span><span class="sxs-lookup"><span data-stu-id="86bb0-158">The default is to use the same PSTN usage as the voice policy for call forwarding and simultaneous ringing.</span></span>

</div>

<div>

## <a name="pstn-usage-records"></a><span data-ttu-id="86bb0-159">Registros de uso de RTC</span><span class="sxs-lookup"><span data-stu-id="86bb0-159">PSTN Usage Records</span></span>

<span data-ttu-id="86bb0-160">Cada directiva de voz necesita tener uno o más registros de uso de RTC asociados.</span><span class="sxs-lookup"><span data-stu-id="86bb0-160">Each voice policy should have one or more associated PSTN usage records.</span></span> <span data-ttu-id="86bb0-161">Los usos de RTC se pueden asociar a una directiva de voz únicamente para las llamadas simultáneas y el desvío de llamadas.</span><span class="sxs-lookup"><span data-stu-id="86bb0-161">PSTN usages can be associated with a voice policy for the purpose of simultaneous ringing and call forwarding only.</span></span> <span data-ttu-id="86bb0-162">Para obtener más información sobre la planificación de registros de uso de RTC, consulte [registros de uso de RTC en Lync Server 2013](lync-server-2013-pstn-usage-records.md).</span><span class="sxs-lookup"><span data-stu-id="86bb0-162">For details about planning PSTN usage records, see [PSTN usage records in Lync Server 2013](lync-server-2013-pstn-usage-records.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="86bb0-p118">El orden de los usos de RTC es fundamental ya que, al asociar usuarios a rutas, la función de enrutamiento saliente compara los usos de RTC desde el principio hasta el final. Si el primer uso coincide con la ruta de la llamada, se usa la ruta. En caso contrario, la función de enrutamiento saliente pasa al siguiente uso de RTC de la lista y sigue así hasta que encuentra alguna coincidencia. De hecho, los usos de RTC siguientes se usan a modo de copia de seguridad si el primero de la lista no está disponible.</span><span class="sxs-lookup"><span data-stu-id="86bb0-p118">PSTN usage order is critical because in matching users to routes, the outbound routing functionality compares PSTN usages from top to bottom. If the first usage matches the call route, that route is used. If not, the outbound routing functionality looks at the next PSTN usage on the list and continues until a match is found. In effect, the subsequent PSTN usages provide backup if the first one on the list is unavailable.</span></span>



<span data-ttu-id="86bb0-167"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="86bb0-167"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

