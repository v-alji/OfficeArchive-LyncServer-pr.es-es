---
title: 'Lync Server 2013: modificar las opciones de configuración del tronco del SIP'
description: 'Lync Server 2013: modificar las opciones de configuración del tronco del SIP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify SIP trunk configuration settings
ms:assetid: 7d68b09c-9ea0-43bd-997c-df887869d607
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688104(v=OCS.15)
ms:contentKeyID: 49733703
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42cb213211a11494a96b5a762734a2b5db49dfbb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425454"
---
# <a name="modify-sip-trunk-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="41342-103">Modificar la configuración de los enlaces de SIP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41342-103">Modify SIP trunk configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41342-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41342-104">

<span> </span></span></span>

<span data-ttu-id="41342-105">_**Última modificación del tema:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="41342-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="41342-106">Los ajustes de configuración del tronco del SIP definen la relación y las capacidades entre un servidor de mediación y la puerta de enlace de red de telefonía pública conmutada (RTC), una central de conmutación (PBX) IP o un controlador de borde de sesión (SBC) en el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="41342-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="41342-107">Estas opciones de configuración especifican:</span><span class="sxs-lookup"><span data-stu-id="41342-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="41342-108">Si se debe activar la omisión de medios en los troncos.</span><span class="sxs-lookup"><span data-stu-id="41342-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="41342-109">Las condiciones en que se envían paquetes de protocolo de control de transporte (RTCP) en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="41342-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="41342-110">Si se requiere o no cifrado de protocolo en tiempo real seguro (SRTP) en cada tronco.</span><span class="sxs-lookup"><span data-stu-id="41342-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="41342-111">Al instalar Microsoft Lync Server 2013, se crea una colección global de parámetros de configuración del tronco del SIP.</span><span class="sxs-lookup"><span data-stu-id="41342-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="41342-112">Los administradores también pueden crear colecciones de valores personalizadas en el ámbito del sitio o servicio (solo para el servicio de puerta de enlace de RTC).</span><span class="sxs-lookup"><span data-stu-id="41342-112">In addition, administrators can create custom setting collections at the site scope or at the service scope (for the PSTN gateway service, only).</span></span> <span data-ttu-id="41342-113">Cualquiera de estas colecciones se puede modificar posteriormente con el panel de control de Lync Server o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="41342-113">Any of these collections can later be modified using either Lync Server Control Panel or Windows PowerShell.</span></span>

<span data-ttu-id="41342-114">Al modificar las opciones de configuración del tronco del SIP mediante el panel de control de Lync Server, las siguientes opciones están disponibles:</span><span class="sxs-lookup"><span data-stu-id="41342-114">When modifying SIP trunk configuration settings using Lync Server Control Panel, the following options are available to you:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41342-115">Valor de IU</span><span class="sxs-lookup"><span data-stu-id="41342-115">UI Setting</span></span></th>
<th><span data-ttu-id="41342-116">Parámetro de PowerShell</span><span class="sxs-lookup"><span data-stu-id="41342-116">PowerShell Parameter</span></span></th>
<th><span data-ttu-id="41342-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="41342-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41342-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="41342-118">Name</span></span></p></td>
<td><p><span data-ttu-id="41342-119">Identity</span><span class="sxs-lookup"><span data-stu-id="41342-119">Identity</span></span></p></td>
<td><p><span data-ttu-id="41342-p103">Identificador único para la colección. Esta propiedad es de solo lectura; no puede cambiar la Identidad de una colección o las opciones de configuración de troncos.</span><span class="sxs-lookup"><span data-stu-id="41342-p103">Unique identifier for the collection. This property is read-only; you cannot change the Identity of a collection of trunk configuration settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41342-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="41342-122">Description</span></span></p></td>
<td><p><span data-ttu-id="41342-123">Description</span><span class="sxs-lookup"><span data-stu-id="41342-123">Description</span></span></p></td>
<td><p><span data-ttu-id="41342-124">Proporciona un método para que los administradores almacenen información adicional acerca de la configuración (por ejemplo, el propósito de la configuración de troncos).</span><span class="sxs-lookup"><span data-stu-id="41342-124">Provides a way for administrators to store addition information about the settings (for example, the purpose of the trunk configuration).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41342-125">Número máximo de diálogos iniciales admitidos</span><span class="sxs-lookup"><span data-stu-id="41342-125">Maximum early dialogs supported</span></span></p></td>
<td><p><span data-ttu-id="41342-126">MaxEarlyDialogs</span><span class="sxs-lookup"><span data-stu-id="41342-126">MaxEarlyDialogs</span></span></p></td>
<td><p><span data-ttu-id="41342-127">Cantidad máxima de respuestas bifurcadas que puede recibir una puerta de enlace RTC, IP-PBX o SBC en el proveedor de servicio para una invitación enviada al Servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="41342-127">The maximum number of forked responses a PSTN gateway, IP-PBX, or SBC at the service provider can receive to an Invite that it sent to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41342-128">Nivel de compatibilidad de cifrado</span><span class="sxs-lookup"><span data-stu-id="41342-128">Encryption support level</span></span></p></td>
<td><p><span data-ttu-id="41342-129">SRTPMode</span><span class="sxs-lookup"><span data-stu-id="41342-129">SRTPMode</span></span></p></td>
<td><p><span data-ttu-id="41342-130">Indica el nivel de compatibilidad para proteger el tráfico de medios entre el Servidor de mediación y la puerta de enlace RTC, IP-PBX o SBC en el proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="41342-130">Indicates the level of support for protecting media traffic between the Mediation Server and the PSTN Gateway, IP-PBX, or SBC at the service provider.</span></span> <span data-ttu-id="41342-131">Para los casos de omisión de medios, este valor debe ser compatible con la configuración de EncryptionLevel en la configuración de medios.</span><span class="sxs-lookup"><span data-stu-id="41342-131">For media bypass cases, this value must be compatible with the EncryptionLevel setting in the media configuration.</span></span> <span data-ttu-id="41342-132">La configuración multimedia se establece mediante los cmdlets <a href="https://docs.microsoft.com/powershell/module/skype/New-CsMediaConfiguration">New-CsMediaConfiguration</a> y <a href="https://docs.microsoft.com/powershell/module/skype/Set-CsMediaConfiguration">set-CsMediaConfiguration</a> .</span><span class="sxs-lookup"><span data-stu-id="41342-132">Media configuration is set by using the <a href="https://docs.microsoft.com/powershell/module/skype/New-CsMediaConfiguration">New-CsMediaConfiguration</a> and <a href="https://docs.microsoft.com/powershell/module/skype/Set-CsMediaConfiguration">Set-CsMediaConfiguration</a> cmdlets.</span></span></p>
<p><span data-ttu-id="41342-133">Los valores permitidos son:</span><span class="sxs-lookup"><span data-stu-id="41342-133">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="41342-134">Requeridos: debe usarse el cifrado SRTP.</span><span class="sxs-lookup"><span data-stu-id="41342-134">Required: SRTP encryption must be used.</span></span></p></li>
<li><p><span data-ttu-id="41342-135">Opcional: el SRTP se usará si la puerta de enlace lo admite.</span><span class="sxs-lookup"><span data-stu-id="41342-135">Optional: SRTP will be used if the gateway supports it.</span></span></p></li>
<li><p><span data-ttu-id="41342-136">No admitido: el cifrado SRTP no está admitido y, por lo tanto, no se usará.</span><span class="sxs-lookup"><span data-stu-id="41342-136">Not Supported: SRTP encryption is not supported and therefore will not be used.</span></span></p></li>
</ul>
<p><span data-ttu-id="41342-p105">El SRTPMode se usa solo si la puerta de enlace está configurada para usar la Seguridad de la capa de transporte (TLS). Si la puerta de enlace está configurada con el Protocolo de control de transporte (TCP) como transporte, SRTPMode se configura internamente como No admitido.</span><span class="sxs-lookup"><span data-stu-id="41342-p105">SRTPMode is used only if the gateway is configured to use Transport Layer Security (TLS). If the gateway is configured with Transmission Control Protocol (TCP) as the transport, SRTPMode is internally set to Not Supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41342-139">Compatibilidad con referencias</span><span class="sxs-lookup"><span data-stu-id="41342-139">Refer support</span></span></p></td>
<td><p><span data-ttu-id="41342-140">Enable3pccRefer</span><span class="sxs-lookup"><span data-stu-id="41342-140">Enable3pccRefer</span></span></p>
<p><span data-ttu-id="41342-141">EnableReferSupport</span><span class="sxs-lookup"><span data-stu-id="41342-141">EnableReferSupport</span></span></p></td>
<td><p><span data-ttu-id="41342-142">Si se establece en <strong>Habilitar referencias de envío a la puerta de enlace</strong>, indica que el tronco admite la recepción de Solicitudes de referencia del Servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="41342-142">If set to <strong>Enable sending refer to the gateway</strong>, indicates that the trunk supports receiving Refer requests from the Mediation Server.</span></span></p>
<p><span data-ttu-id="41342-143">Si se establece en en <strong>Habilitar referencia mediante el control de llamadas a terceros</strong>, indica que se puede usar el protocolo 3pcc para permitir llamadas transferidas para omitir el sitio hospedado.</span><span class="sxs-lookup"><span data-stu-id="41342-143">If set to <strong>Enable refer using third-party call control</strong>, indicates that the 3pcc protocol can be used to allow transferred calls to bypass the hosted site.</span></span> <span data-ttu-id="41342-144">3pcc también se conoce como &quot; control &quot; de terceros y se produce cuando se usa un tercero para conectar un par de personas que llaman (por ejemplo, un operador que llama a la persona a a la persona B).</span><span class="sxs-lookup"><span data-stu-id="41342-144">3pcc is also known as &quot;third party control,&quot; and occurs when a third-party is used to connect a pair of callers (for example, an operator placing a call from person A to person B).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41342-145">Habilitar omisión de medios</span><span class="sxs-lookup"><span data-stu-id="41342-145">Enable media bypass</span></span></p></td>
<td><p><span data-ttu-id="41342-146">EnableBypass</span><span class="sxs-lookup"><span data-stu-id="41342-146">EnableBypass</span></span></p></td>
<td><p><span data-ttu-id="41342-p107">Indica si la omisión de medios está habilitada para este tronco. La omisión de medios solo puede estar habilitada si la opción <strong>Procesamiento de medios centralizado</strong> también está habilitada.</span><span class="sxs-lookup"><span data-stu-id="41342-p107">Indicates whether media bypass is enabled for this trunk. Media bypass can only be enabled if <strong>Centralized media processing</strong> is also enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41342-149">Procesamiento de medios centralizado</span><span class="sxs-lookup"><span data-stu-id="41342-149">Centralized media processing</span></span></p></td>
<td><p><span data-ttu-id="41342-150">ConcentratedTopology</span><span class="sxs-lookup"><span data-stu-id="41342-150">ConcentratedTopology</span></span></p></td>
<td><p><span data-ttu-id="41342-p108">Indica si existe un punto de terminación de medios conocido. (Un ejemplo de punto de terminación de medios conocido puede ser una puerta de enlace RTC donde una terminación de medios tiene la misma IP que la terminación de señal).</span><span class="sxs-lookup"><span data-stu-id="41342-p108">Indicates whether there is a well-known media termination point. (An example of a well-known media termination point would be a PSTN gateway where the media termination has the same IP as the signaling termination.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41342-153">Habilitar cierre RTP</span><span class="sxs-lookup"><span data-stu-id="41342-153">Enable RTP latching</span></span></p></td>
<td><p><span data-ttu-id="41342-154">EnableRTPLatching</span><span class="sxs-lookup"><span data-stu-id="41342-154">EnableRTPLatching</span></span></p></td>
<td><p><span data-ttu-id="41342-p109">Indica si los troncos admiten o no el cierre RTP. El cierre RTP es una tecnología que permite la conectividad RTP/RTCP mediante un firewall o dispositivo NAT (traductor de direcciones de red).</span><span class="sxs-lookup"><span data-stu-id="41342-p109">Indicates whether or not the SIP trunks support RTP latching. RTP latching is a technology that enables RTP/RTCP connectivity through a NAT (network address translator) device or firewall.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41342-157">Habilitar el historial de llamadas reenviadas</span><span class="sxs-lookup"><span data-stu-id="41342-157">Enable forward call history</span></span></p></td>
<td><p><span data-ttu-id="41342-158">ForwardCallHistory</span><span class="sxs-lookup"><span data-stu-id="41342-158">ForwardCallHistory</span></span></p></td>
<td><p><span data-ttu-id="41342-159">Indica si la información del historial de llamadas se reenviará a través del tronco.</span><span class="sxs-lookup"><span data-stu-id="41342-159">Indicates whether call history information will be forwarded through the trunk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41342-160">Habilitar el reenvío de datos P-Asserted-Identity</span><span class="sxs-lookup"><span data-stu-id="41342-160">Enable forward P-Asserted-Identity data</span></span></p></td>
<td><p><span data-ttu-id="41342-161">ForwardPAI</span><span class="sxs-lookup"><span data-stu-id="41342-161">ForwardPAI</span></span></p></td>
<td><p><span data-ttu-id="41342-p110">Indica si el encabezado P-Asserted-Identity (PAI) se reenviará junto con la llamada. El encabezado PAI proporciona un método para comprobar la identidad de la persona que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="41342-p110">Indicates whether the P-Asserted-Identity (PAI) header will be forwarded along with the call. The PAI header provides a way to verify the identity of the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41342-164">Habilitar temporizador de conmutación por error del enrutamiento de salida</span><span class="sxs-lookup"><span data-stu-id="41342-164">Enable outbound routing failover timer</span></span></p></td>
<td><p><span data-ttu-id="41342-165">EnableFastFailoverTimer</span><span class="sxs-lookup"><span data-stu-id="41342-165">EnableFastFailoverTimer</span></span></p></td>
<td><p><span data-ttu-id="41342-p111">Indica que si las llamadas salientes no son respondidas por la puerta de enlace en el plazo de 10 segundos se enrutarán al siguiente tronco disponible; si no existen troncos adicionales, la llamada se perderá automáticamente. En una organización con redes y respuestas de puerta de enlace lentas, esto puede tener como resultado que las llamadas se pierdan innecesariamente.</span><span class="sxs-lookup"><span data-stu-id="41342-p111">Indicates whether outbound calls that are not answered by the gateway within 10 seconds will be routed to the next available trunk; if there are no additional trunks then the call will automatically be dropped. In an organization with slow networks and gateway responses, that could potentially result in calls being dropped unnecessarily.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41342-168">Usos de la RTC asociados</span><span class="sxs-lookup"><span data-stu-id="41342-168">Associated PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="41342-169">PSTNUsages</span><span class="sxs-lookup"><span data-stu-id="41342-169">PSTNUsages</span></span></p></td>
<td><p><span data-ttu-id="41342-170">Colección de usos de RTC asignados al tronco.</span><span class="sxs-lookup"><span data-stu-id="41342-170">Collection of PSTN usages assigned to the trunk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41342-171">Número traducido para probar</span><span class="sxs-lookup"><span data-stu-id="41342-171">Translated number to test</span></span></p></td>
<td><p><span data-ttu-id="41342-172">N/D</span><span class="sxs-lookup"><span data-stu-id="41342-172">N/A</span></span></p></td>
<td><p><span data-ttu-id="41342-173">Número telefónico que puede usare para realizar una prueba ad hoc de la configuración del tronco.</span><span class="sxs-lookup"><span data-stu-id="41342-173">Phone number that can be used to do an ad hoc test of the trunk configuration settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41342-174">Reglas de conversión asociadas</span><span class="sxs-lookup"><span data-stu-id="41342-174">Associated translation rules</span></span></p></td>
<td><p><span data-ttu-id="41342-175">OutboundTranslationRulesList</span><span class="sxs-lookup"><span data-stu-id="41342-175">OutboundTranslationRulesList</span></span></p></td>
<td><p><span data-ttu-id="41342-176">Recopilación de reglas de conversión de números telefónicos que se aplican a las llamadas administradas por el Enrutamiento de salida (llamadas enrutadas a destinos PBX o RTC).</span><span class="sxs-lookup"><span data-stu-id="41342-176">Collection of phone number translation rules that apply to calls handled by Outbound Routing (calls routed to PBX or PSTN destinations).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41342-177">Reglas de traducción de números llamados</span><span class="sxs-lookup"><span data-stu-id="41342-177">Called number translation rules</span></span></p></td>
<td><p><span data-ttu-id="41342-178">OutboundCallingNumberTranslationRulesList</span><span class="sxs-lookup"><span data-stu-id="41342-178">OutboundCallingNumberTranslationRulesList</span></span></p></td>
<td><p><span data-ttu-id="41342-179">Colección de reglas de conversión de números de llamadas salientes asignadas al tronco.</span><span class="sxs-lookup"><span data-stu-id="41342-179">Collection of outbound calling number translation rules assigned to the trunk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41342-180">Número de teléfono para probar</span><span class="sxs-lookup"><span data-stu-id="41342-180">Phone number to test</span></span></p></td>
<td><p><span data-ttu-id="41342-181">N/D</span><span class="sxs-lookup"><span data-stu-id="41342-181">N/A</span></span></p></td>
<td><p><span data-ttu-id="41342-182">Número telefónico que puede usarse para realizar una prueba ad hoc de las reglas de conversión.</span><span class="sxs-lookup"><span data-stu-id="41342-182">Phone number that can be used to do an ad hoc test of the translation rules.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41342-183">Número que llamada</span><span class="sxs-lookup"><span data-stu-id="41342-183">Calling number</span></span></p></td>
<td><p><span data-ttu-id="41342-184">N/D</span><span class="sxs-lookup"><span data-stu-id="41342-184">N/A</span></span></p></td>
<td><p><span data-ttu-id="41342-185">Indica que el número de teléfono que se debe probar es el número telefónico de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="41342-185">Indicates that the phone number to test is the phone number of the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41342-186">Número llamado</span><span class="sxs-lookup"><span data-stu-id="41342-186">Called number</span></span></p></td>
<td><p><span data-ttu-id="41342-187">N/D</span><span class="sxs-lookup"><span data-stu-id="41342-187">N/A</span></span></p></td>
<td><p><span data-ttu-id="41342-188">Indica que el número de teléfono que se debe probar es el número telefónico de la persona llamada.</span><span class="sxs-lookup"><span data-stu-id="41342-188">Indicates that the phone number to test is the phone number of the person being called.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="41342-189">Los cmdlets de CsTrunkConfiguration de Lync Server admiten propiedades adicionales que no se muestran en el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="41342-189">The Lync Server CsTrunkConfiguration cmdlets support additional properties not shown in Lync Server Control Panel.</span></span> <span data-ttu-id="41342-190">Para obtener más información, consulte el tema de ayuda para el cmdlet <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsTrunkConfiguration">set-CsTrunkConfiguration</A> .</span><span class="sxs-lookup"><span data-stu-id="41342-190">For more information, see the help topic for the <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsTrunkConfiguration">Set-CsTrunkConfiguration</A> cmdlet.</span></span>



</div>

<div>

## <a name="to-modify-sip-trunk-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="41342-191">Para modificar los ajustes de configuración del tronco del Protocolo de PREENLACE SIP con el panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="41342-191">To modify SIP trunk configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="41342-192">En el panel de control de Lync Server, haga clic en **enrutamiento de voz** y luego en **configuración troncal**.</span><span class="sxs-lookup"><span data-stu-id="41342-192">In Lync Server Control Panel, click **Voice Routing**, and then click **Trunk Configuration**.</span></span>

2.  <span data-ttu-id="41342-p113">En la pestaña **Configuración de tronco**, haga doble clic en las opciones de configuración de tronco que se modificarán. Tenga en cuenta que solo puede editar un grupo de opciones de configuración a la vez. Si desea realizar los mismos cambios en varias colecciones, use Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="41342-p113">On the **Trunk Configuration** tab, double-click the trunk configuration settings to be modified. Note that you can only edit one collection of settings at a time. If you would like to make the same changes on multiple collections, use Windows PowerShell instead.</span></span>

3.  <span data-ttu-id="41342-196">En el cuadro de diálogo **Editar configuración de tronco**, realice las selecciones apropiadas y seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="41342-196">In the **Edit Trunk Configuration** dialog, make the appropriate selections and then click **OK**.</span></span>

4.  <span data-ttu-id="41342-p114">La propiedad **Estado** para la colección se actualizará a **No confirmado**. Para confirmar los cambios y eliminar la colección, haga clic en **Confirmar** y luego en **Confirmar todo**.</span><span class="sxs-lookup"><span data-stu-id="41342-p114">The **State** property for the collection will be updated to **Uncommitted**. To commit the changes, and to delete the collection, click **Commit** and then click **Commit All**.</span></span>

5.  <span data-ttu-id="41342-199">En el cuadro de diálogo **Valores de configuración de voz no confirmados**, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="41342-199">In the **Uncommitted Voice Configuration Settings** dialog box, click **OK**.</span></span>

6.  <span data-ttu-id="41342-200">En el cuadro de diálogo **Panel de control de Microsoft Lync Server 2013** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="41342-200">In the **Microsoft Lync Server 2013 Control Panel** dialog box click **OK**.</span></span>

<span data-ttu-id="41342-201"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41342-201"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

