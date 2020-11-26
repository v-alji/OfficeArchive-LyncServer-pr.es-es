---
title: 'Lync Server 2013: Resumen de puerto - Proxy inverso'
description: 'Lync Server 2013: Resumen de puertos: proxy inverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Reverse proxy
ms:assetid: 59b9ac3c-3e6f-4776-b366-174f0dd1f2eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204932(v=OCS.15)
ms:contentKeyID: 48184251
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf07800c91f5a28165eb05e14e2d775758460f50
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442813"
---
# <a name="port-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="cbbc9-103">Resumen de puerto - Proxy inverso en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cbbc9-103">Port summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cbbc9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cbbc9-104">

<span> </span></span></span>

<span data-ttu-id="cbbc9-105">_**Última modificación del tema:** 2013-02-15_</span><span class="sxs-lookup"><span data-stu-id="cbbc9-105">_**Topic Last Modified:** 2013-02-15_</span></span>

<span data-ttu-id="cbbc9-106">El proxy inverso tiene requisitos mínimos para el firewall y el puerto/protocolo.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-106">The reverse proxy has minimal requirements for firewall and port/protocol.</span></span>

  - <span data-ttu-id="cbbc9-107">Los requisitos del firewall externo son HTTPS/TCP/443 y el HTTP/TCP/80 opcional.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-107">External firewall requirements are the HTTPS/TCP/443 and the optional HTTP/TCP/80.</span></span> <span data-ttu-id="cbbc9-108">HTTPS se usa para comunicaciones seguras SSL y TLS a través del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-108">HTTPS is used for SSL and TLS secure communications through the reverse proxy.</span></span> <span data-ttu-id="cbbc9-109">HTTP se usa si elige permitir el acceso al servicio de detección automática al modificar certificados que puede resultar difícil o no estar justificado.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-109">HTTP is used if you choose to allow access to the Autodiscover Service when modifying certificates might prove difficult or not cost justified.</span></span>

  - <span data-ttu-id="cbbc9-110">Los clientes esperan ponerse en contacto con el servidor de Office Web Apps en HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-110">Clients expect to contact the Office Web Apps Server on HTTPS.</span></span> <span data-ttu-id="cbbc9-111">El servidor de Office Web Apps Server espera la comunicación de los clientes internos en HTTPS/TCP/443.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-111">The Office Web Apps Server expects communication from internal clients on HTTPS/TCP/443.</span></span> <span data-ttu-id="cbbc9-112">La configuración recomendada es permitir HTTPS/TCP/443 desde el proxy inverso hasta el servidor de Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-112">The recommended configuration is to allow HTTPS/TCP/443 from the reverse proxy to the Office Web Apps Server.</span></span>

  - <span data-ttu-id="cbbc9-113">El puerto 8080 se usa para enrutar el tráfico de la interfaz interna de proxy invertida al servidor front-end, la IP virtual de la agrupación de front-end (VIP) o el director opcional o VIP del grupo de directores.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-113">Port 8080 is used to route traffic from the reverse proxy internal interface to the Front End Server, Front End pool virtual IP (VIP) or the optional Director or Director pool VIP.</span></span> <span data-ttu-id="cbbc9-114">El puerto TCP 8080 es necesario para que los dispositivos móviles que ejecutan Lync encuentren el servicio de detección automática en situaciones en las que no es deseable modificar el certificado de la regla de publicación de servicio Web externo (por ejemplo, si tiene un gran número de dominios SIP).</span><span class="sxs-lookup"><span data-stu-id="cbbc9-114">Port TCP 8080 is required for mobile devices running Lync to locate the Autodiscover Service in situations where modifying the external web service publishing rule certificate is undesirable (for example, if you have a large number of SIP domains).</span></span> <span data-ttu-id="cbbc9-115">Si elige adquirir certificados nuevos con las entradas de SAN necesarias, el puerto TCP 8080 no es necesario y es opcional.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-115">If you choose to acquire new certificates with the necessary SAN entries, the port TCP 8080 is not needed and is optional.</span></span>

  - <span data-ttu-id="cbbc9-116">El puerto 4443 se usa para el tráfico de la interfaz interna de proxy invertida al servidor front-end, la IP virtual de grupo de servidores front-end (VIP) o el director opcional o VIP del grupo de directores</span><span class="sxs-lookup"><span data-stu-id="cbbc9-116">Port 4443 is used for traffic from the reverse proxy internal interface to the Front End Server, Front End pool virtual IP (VIP) or the optional Director or Director pool VIP</span></span>
    
    <span data-ttu-id="cbbc9-117">![13142405-d5c9-45b7-a8b7-a8c89f09c97c](images/JJ204932.13142405-d5c9-45b7-a8b7-a8c89f09c97c(OCS.15).jpg "13142405-d5c9-45b7-a8b7-a8c89f09c97c")</span><span class="sxs-lookup"><span data-stu-id="cbbc9-117">![13142405-d5c9-45b7-a8b7-a8c89f09c97c](images/JJ204932.13142405-d5c9-45b7-a8b7-a8c89f09c97c(OCS.15).jpg "13142405-d5c9-45b7-a8b7-a8c89f09c97c")</span></span>  
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="cbbc9-118">No confunda el 4443 sobre TCP del proxy inverso en la implementación interna para el puerto 4443 sobre el tráfico TCP desde el servidor Standard Edition o el grupo de servidores front-end que administra la función de almacén de administración central.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-118">Do not confuse the 4443 over TCP from the reverse proxy to the internal deployment for the port 4443 over TCP traffic from the Standard Edition server or the Front End pool that manages the Central Management store role.</span></span>

    
    </div>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="cbbc9-119">Detalles de protocolo y puerto</span><span class="sxs-lookup"><span data-stu-id="cbbc9-119">Port and Protocol Details</span></span>

### <a name="firewall-details-for-reverse-proxy-server-external-interface"></a><span data-ttu-id="cbbc9-120">Detalles del firewall para el servidor proxy inverso: interfaz externa</span><span class="sxs-lookup"><span data-stu-id="cbbc9-120">Firewall Details for Reverse Proxy Server: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cbbc9-121">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="cbbc9-121">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="cbbc9-122">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="cbbc9-122">Source IP Address</span></span></th>
<th><span data-ttu-id="cbbc9-123">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="cbbc9-123">Destination IP Address</span></span></th>
<th><span data-ttu-id="cbbc9-124">Notas</span><span class="sxs-lookup"><span data-stu-id="cbbc9-124">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbbc9-125">HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="cbbc9-125">HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-126">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cbbc9-126">Any</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-127">Escucha de proxy inverso</span><span class="sxs-lookup"><span data-stu-id="cbbc9-127">Reverse proxy listener</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-128">Faculta Redireccionamiento a HTTPS si el usuario escribe http:// &lt; publishedSiteFQDN &gt; .</span><span class="sxs-lookup"><span data-stu-id="cbbc9-128">(Optional) Redirection to HTTPS if user enters http://&lt;publishedSiteFQDN&gt;.</span></span></p>
<p><span data-ttu-id="cbbc9-129">También se requiere si se usa Office Web Apps para conferencias y el servicio Detección automática para dispositivos móviles que ejecutan Lync en situaciones en las que la organización no desea modificar el certificado de regla de publicación de servicio Web externo.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-129">Also required if using Office Web Apps for conferencing and the Autodiscover Service for mobile devices running Lync in situations where the organization does not want to modify the external web service publishing rule certificate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbbc9-130">HTTPS/TCP/443</span><span class="sxs-lookup"><span data-stu-id="cbbc9-130">HTTPS/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-131">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cbbc9-131">Any</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-132">Escucha de proxy inverso</span><span class="sxs-lookup"><span data-stu-id="cbbc9-132">Reverse proxy listener</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-133">Descargas de la libreta de direcciones, servicio de consultas Web de la libreta de direcciones, detección automática, actualizaciones de cliente, contenido de la reunión, actualizaciones de dispositivos, expansión de grupos, Office Web Apps para conferencias, conferencias de acceso telefónico local y reuniones.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-133">Address book downloads, Address Book Web Query service, Autodiscover, client updates, meeting content, device updates, group expansion, Office Web Apps for conferencing, dial-in conferencing, and meetings.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-details-for-reverse-proxy-server-internal-interface"></a><span data-ttu-id="cbbc9-134">Detalles del firewall para el servidor proxy inverso: interfaz interna</span><span class="sxs-lookup"><span data-stu-id="cbbc9-134">Firewall Details for Reverse Proxy Server: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cbbc9-135">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="cbbc9-135">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="cbbc9-136">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="cbbc9-136">Source IP Address</span></span></th>
<th><span data-ttu-id="cbbc9-137">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="cbbc9-137">Destination IP Address</span></span></th>
<th><span data-ttu-id="cbbc9-138">Notas</span><span class="sxs-lookup"><span data-stu-id="cbbc9-138">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbbc9-139">HTTP/TCP/8080</span><span class="sxs-lookup"><span data-stu-id="cbbc9-139">HTTP/TCP/8080</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-140">Interfaz interna de proxy invertida</span><span class="sxs-lookup"><span data-stu-id="cbbc9-140">Internal reverse proxy interface</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-141">Servidor front-end, grupo front-end, Director, grupo de directores</span><span class="sxs-lookup"><span data-stu-id="cbbc9-141">Front End Server, Front End pool, Director, Director pool</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-142">Necesario si se usa el servicio de detección automática para dispositivos móviles que ejecutan Lync, en situaciones en las que la organización no desea modificar el certificado de la regla de publicación de servicio Web externo.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-142">Required if using the Autodiscover Service for mobile devices running Lync in situations where the organization does not want to modify the external web service publishing rule certificate.</span></span></p>
<p><span data-ttu-id="cbbc9-143">El tráfico enviado al puerto 80 en la interfaz externa de proxy inverso se redirige a un grupo en el puerto 8080 desde la interfaz interna de proxy invertida para que los servicios web del grupo lo diferencien del tráfico web interno.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-143">Traffic sent to port 80 on the reverse proxy external interface is redirected to a pool on port 8080 from the reverse proxy internal interface so that the pool Web Services can distinguish it from internal web traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbbc9-144">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="cbbc9-144">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-145">Interfaz interna de proxy invertida</span><span class="sxs-lookup"><span data-stu-id="cbbc9-145">Internal reverse proxy interface</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-146">Servidor front-end, grupo front-end, Director, grupo de directores</span><span class="sxs-lookup"><span data-stu-id="cbbc9-146">Front End Server, Front End pool, Director, Director pool</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-147">El tráfico enviado al puerto 443 en la interfaz externa de proxy inverso se redirige a un grupo en el puerto 4443 desde la interfaz interna de proxy invertida para que los servicios web del grupo lo diferencien del tráfico web interno.</span><span class="sxs-lookup"><span data-stu-id="cbbc9-147">Traffic sent to port 443 on the reverse proxy external interface is redirected to a pool on port 4443 from the reverse proxy internal interface so that the pool web services can distinguish it from internal web traffic.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbbc9-148">HTTPS/TCP/443</span><span class="sxs-lookup"><span data-stu-id="cbbc9-148">HTTPS/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-149">Interfaz interna de proxy invertida</span><span class="sxs-lookup"><span data-stu-id="cbbc9-149">Internal reverse proxy interface</span></span></p></td>
<td><p><span data-ttu-id="cbbc9-150">Office Web Apps para conferencias</span><span class="sxs-lookup"><span data-stu-id="cbbc9-150">Office Web Apps for conferencing</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="cbbc9-151">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cbbc9-151">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

