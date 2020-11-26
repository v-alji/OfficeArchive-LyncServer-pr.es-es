---
title: 'Lync Server 2013: Resumen de puertos: conectividad de mensajería instantánea pública'
description: 'Lync Server 2013: Resumen de puertos: conectividad pública de mensajería instantánea.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Public instant messaging connectivity
ms:assetid: f46756ec-1401-4ca2-a4a4-5cd28bcfdc7f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618376(v=OCS.15)
ms:contentKeyID: 49105663
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4137b5f92e043dc15dc9aa1f0b9593b4d9f7c2ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424278"
---
# <a name="port-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="5353e-103">Resumen de puertos: conectividad de mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5353e-103">Port summary - Public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5353e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5353e-104">

<span> </span></span></span>

<span data-ttu-id="5353e-105">_**Última modificación del tema:** 2013-02-16_</span><span class="sxs-lookup"><span data-stu-id="5353e-105">_**Topic Last Modified:** 2013-02-16_</span></span>

<span data-ttu-id="5353e-106">Para configurar el firewall para los puertos y protocolos necesarios para admitir la conectividad de mensajería instantánea pública, primero tenga en cuenta que los SIP/MTLS/TCP 5061 son bidireccionales para tener en cuenta la capacidad de los contactos en el proveedor de mi pública para ponerse en contacto con los clientes de Lync o para que Lync pueda comunicarse con los contactos públicos de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="5353e-106">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="5353e-107">Windows Live Messenger puede participar en comunicaciones de audio y vídeo con clientes de Lync.</span><span class="sxs-lookup"><span data-stu-id="5353e-107">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="5353e-108">Esto cuenta con una configuración de protocolo y un puerto de Firewall muy similar que normalmente tendría en el firewall para admitir clientes de Lync como usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="5353e-108">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="5353e-109">Más que nunca, Lync es una herramienta eficaz para la conexión entre organizaciones y con personas de todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="5353e-109">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="5353e-110">La Federación con Windows Live Messenger no requiere licencias de usuario o de dispositivo adicionales aparte de la licencia de acceso de cliente (CAL) de Lync.</span><span class="sxs-lookup"><span data-stu-id="5353e-110">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="5353e-111">La Federación de Skype se agrega a esta lista, lo que permite a los usuarios de Lync llegar a cientos de millones de personas con la mensajería instantánea y la voz.</span><span class="sxs-lookup"><span data-stu-id="5353e-111">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="5353e-112">La Federación con los contactos de los clientes de Messenger terminará oficialmente el 15 de marzo de 2013, excepto en el caso de China continental.</span><span class="sxs-lookup"><span data-stu-id="5353e-112">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="5353e-113">Skype se convertirá en el cliente de Federación para los usuarios federados que antes usaban Messenger.</span><span class="sxs-lookup"><span data-stu-id="5353e-113">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="5353e-114">Resumen del firewall: conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="5353e-114">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5353e-115">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="5353e-115">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="5353e-116">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="5353e-116">Source IP address</span></span></th>
<th><span data-ttu-id="5353e-117">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="5353e-117">Destination IP address</span></span></th>
<th><span data-ttu-id="5353e-118">Notas</span><span class="sxs-lookup"><span data-stu-id="5353e-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5353e-119">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="5353e-119">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="5353e-120">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="5353e-120">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="5353e-121">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="5353e-121">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="5353e-122">Para la conectividad de mensajería instantánea pública y federada que usan SIP.</span><span class="sxs-lookup"><span data-stu-id="5353e-122">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5353e-123">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="5353e-123">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="5353e-124">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="5353e-124">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="5353e-125">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="5353e-125">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="5353e-126">Para la conectividad de mensajería instantánea pública y federada que usan SIP.</span><span class="sxs-lookup"><span data-stu-id="5353e-126">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5353e-127">Acceso/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="5353e-127">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="5353e-128">Clientes</span><span class="sxs-lookup"><span data-stu-id="5353e-128">Clients</span></span></p></td>
<td><p><span data-ttu-id="5353e-129">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="5353e-129">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="5353e-130">Tráfico SIP de cliente a servidor para el acceso de usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="5353e-130">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5353e-131">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="5353e-131">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="5353e-132">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="5353e-132">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="5353e-133">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="5353e-133">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="5353e-134">Se usa para sesiones de A/V con Windows Live Messenger si está configurada la conectividad de mensajería instantánea pública.</span><span class="sxs-lookup"><span data-stu-id="5353e-134">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5353e-135">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="5353e-135">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="5353e-136">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="5353e-136">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="5353e-137">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="5353e-137">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="5353e-138">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="5353e-138">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5353e-139">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="5353e-139">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="5353e-140">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="5353e-140">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="5353e-141">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="5353e-141">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="5353e-142">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="5353e-142">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5353e-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="5353e-143">See Also</span></span>


[<span data-ttu-id="5353e-144">Escenarios para el acceso de usuarios externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5353e-144">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="5353e-145">Determinar los requisitos de los puertos y el firewall de A/V externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5353e-145">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
  

<span data-ttu-id="5353e-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5353e-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

