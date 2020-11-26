---
title: 'Lync Server 2013: Resumen de puertos-detección automática'
description: 'Lync Server 2013: Resumen de puertos-detección automática.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Autodiscover
ms:assetid: 8bd16363-5e18-4e4b-be99-b3e6457b4c99
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945642(v=OCS.15)
ms:contentKeyID: 51541497
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20a5ef54d4ad8419fd6e73909f97764bf1290c22
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442820"
---
# <a name="port-summary---autodiscover-in-lync-server-2013"></a><span data-ttu-id="f3ecc-103">Resumen de puertos-detección automática en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3ecc-103">Port summary - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3ecc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3ecc-104">

<span> </span></span></span>

<span data-ttu-id="f3ecc-105">_**Última modificación del tema:** 2013-03-05_</span><span class="sxs-lookup"><span data-stu-id="f3ecc-105">_**Topic Last Modified:** 2013-03-05_</span></span>

<span data-ttu-id="f3ecc-106">El servicio de detección automática de Lync Server 2013 se ejecuta en los servidores de director y de grupo de servidores front-end y, cuando se publican en DNS con los `lyncdiscover.<domain>` registros de host y de `lyncdiscoverinternal.<domain>` hospedaje, los clientes pueden usarlos para localizar las características de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-106">The Lync Server 2013 Autodiscover Service runs on the Director and Front End pool servers, and when published in DNS using the `lyncdiscover.<domain>` and `lyncdiscoverinternal.<domain>` host records, can be used by clients to locate Lync Server features.</span></span> <span data-ttu-id="f3ecc-107">Para que los dispositivos móviles que ejecutan Lync Mobile puedan usar la detección automática, es posible que primero tenga que modificar las listas de nombres alternativos del sujeto de certificado en cualquier Director y servidor front-end que ejecute el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-107">In order for mobile devices running Lync Mobile to use Autodiscover, you may first need to modify certificate subject alternative name lists on any Director and Front End Server running the Autodiscover Service.</span></span> <span data-ttu-id="f3ecc-108">Además, puede que sea necesario modificar las listas de nombres alternativos del asunto en los certificados que se usan para las reglas de publicación de servicios web externos en los proxies inversos.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-108">In addition, it may be necessary to modify the subject alternative name lists on certificates used for external web service publishing rules on reverse proxies.</span></span>

<span data-ttu-id="f3ecc-109">La decisión sobre si usar o no las listas de nombres alternativos del sujeto en proxies inversos se basa en si publica el servicio de detección automática en el puerto 80 o en el puerto 443:</span><span class="sxs-lookup"><span data-stu-id="f3ecc-109">The decision about whether to use subject alternative name lists on reverse proxies is based on whether you publish the Autodiscover Service on port 80 or on port 443:</span></span>

  - <span data-ttu-id="f3ecc-110">**Publicado en el puerto 80**   En el caso de los dispositivos móviles, no es necesario realizar cambios en los certificados si la consulta inicial para el servicio de detección automática se realiza a través del puerto 80.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-110">**Published on port 80**   For Mobile devices, no certificate changes are required if the initial query to the Autodiscover Service occurs over port 80.</span></span> <span data-ttu-id="f3ecc-111">Esto se debe a que los dispositivos móviles que ejecutan Lync tendrán acceso al proxy inverso en el puerto 80 externamente y se redirigirá a un director o servidor front-end en el puerto 8080 de forma interna.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-111">This is because mobile devices running Lync will access the reverse proxy on port 80 externally and then be redirected to a Director or Front End Server on port 8080 internally.</span></span>

  - <span data-ttu-id="f3ecc-112">**Publicado en el puerto 443**   La lista de nombres alternativos de asunto en certificados usados por la regla de publicación de servicios web externos debe contener una `lyncdiscover.<sipdomain>` entrada para cada dominio SIP de su organización.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-112">**Published on port 443**   The subject alternative name list on certificates used by the external web services publishing rule must contain a `lyncdiscover.<sipdomain>` entry for each SIP domain within your organization.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f3ecc-113">En el caso de instalaciones nuevas o actualizaciones de Lync Server 2010 donde ha implementado la movilidad, ya ha usado el puerto 80 para la detección automática del servicio de movilidad o ha reemitido certificados con el nombre de asunto y los nombres alternativos de asunto correctos.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-113">For new installations or upgrades from Lync Server 2010 where you deployed Mobility, you either used Port 80 for Autodiscover of the Mobility service, or reissued certificates with the proper subject name and subject alternative names in place.</span></span> <span data-ttu-id="f3ecc-114">Revise los certificados de su director y del servidor front-end para confirmar qué ruta de acceso elegida.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-114">Review the certificates on your Director and Front End Server to confirm which path you chose.</span></span>

    
    </div>

### <a name="firewall-details-for-reverse-proxy-server-external-interface"></a><span data-ttu-id="f3ecc-115">Detalles del firewall para el servidor proxy inverso: interfaz externa</span><span class="sxs-lookup"><span data-stu-id="f3ecc-115">Firewall Details for Reverse Proxy Server: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3ecc-116">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="f3ecc-116">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="f3ecc-117">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="f3ecc-117">Source IP Address</span></span></th>
<th><span data-ttu-id="f3ecc-118">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="f3ecc-118">Destination IP Address</span></span></th>
<th><span data-ttu-id="f3ecc-119">Notas</span><span class="sxs-lookup"><span data-stu-id="f3ecc-119">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3ecc-120">HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="f3ecc-120">HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-121">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f3ecc-121">Any</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-122">Escucha de proxy inverso</span><span class="sxs-lookup"><span data-stu-id="f3ecc-122">Reverse proxy listener</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-123">Faculta Redireccionamiento a HTTPS si el usuario escribe http:// &lt; publishedSiteFQDN &gt; .</span><span class="sxs-lookup"><span data-stu-id="f3ecc-123">(Optional) Redirection to HTTPS if user enters http://&lt;publishedSiteFQDN&gt;.</span></span> <span data-ttu-id="f3ecc-124">También se requiere si se usa Office Web Apps para conferencias y el servicio Detección automática para dispositivos móviles que ejecutan Lync en situaciones en las que la organización no desea modificar el certificado de regla de publicación de servicio Web externo.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-124">Also required if using Office Web Apps for conferencing and the Autodiscover Service for mobile devices running Lync in situations where the organization does not want to modify the external web service publishing rule certificate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3ecc-125">HTTPS/TCP/443</span><span class="sxs-lookup"><span data-stu-id="f3ecc-125">HTTPS/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-126">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f3ecc-126">Any</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-127">Escucha de proxy inverso</span><span class="sxs-lookup"><span data-stu-id="f3ecc-127">Reverse proxy listener</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-128">Descargas de la libreta de direcciones, servicio de consultas Web de la libreta de direcciones, detección automática, actualizaciones de cliente, contenido de la reunión, actualizaciones de dispositivos, expansión de grupos, Office Web Apps para conferencias, conferencias de acceso telefónico local y reuniones.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-128">Address book downloads, Address Book Web Query service, Autodiscover, client updates, meeting content, device updates, group expansion, Office Web Apps for conferencing, dial-in conferencing, and meetings.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-details-for-reverse-proxy-server-internal-interface"></a><span data-ttu-id="f3ecc-129">Detalles del firewall para el servidor proxy inverso: interfaz interna</span><span class="sxs-lookup"><span data-stu-id="f3ecc-129">Firewall Details for Reverse Proxy Server: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3ecc-130">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="f3ecc-130">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="f3ecc-131">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="f3ecc-131">Source IP Address</span></span></th>
<th><span data-ttu-id="f3ecc-132">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="f3ecc-132">Destination IP Address</span></span></th>
<th><span data-ttu-id="f3ecc-133">Notas</span><span class="sxs-lookup"><span data-stu-id="f3ecc-133">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3ecc-134">HTTP/TCP/8080</span><span class="sxs-lookup"><span data-stu-id="f3ecc-134">HTTP/TCP/8080</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-135">Interfaz interna de proxy invertida</span><span class="sxs-lookup"><span data-stu-id="f3ecc-135">Internal reverse proxy interface</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-136">Servidor front-end, grupo front-end, Director, grupo de directores, Office Web Apps para conferencias</span><span class="sxs-lookup"><span data-stu-id="f3ecc-136">Front End Server, Front End pool, Director, Director pool, Office Web Apps for conferencing</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-137">Necesario si se usa el servicio de detección automática para dispositivos móviles que ejecutan Lync, en situaciones en las que la organización no desea modificar el certificado de la regla de publicación de servicio Web externo.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-137">Required if using the Autodiscover Service for mobile devices running Lync in situations where the organization does not want to modify the external web service publishing rule certificate.</span></span> <span data-ttu-id="f3ecc-138">El tráfico enviado al puerto 80 en la interfaz externa de proxy inverso se redirige a un grupo en el puerto 8080 desde la interfaz interna de proxy invertida para que los servicios web del grupo lo diferencien del tráfico web interno.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-138">Traffic sent to port 80 on the reverse proxy external interface is redirected to a pool on port 8080 from the reverse proxy internal interface so that the pool Web Services can distinguish it from internal web traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3ecc-139">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="f3ecc-139">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-140">Interfaz interna de proxy invertida</span><span class="sxs-lookup"><span data-stu-id="f3ecc-140">Internal reverse proxy interface</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-141">Servidor front-end, grupo front-end, Director, grupo de directores, Office Web Apps para conferencias</span><span class="sxs-lookup"><span data-stu-id="f3ecc-141">Front End Server, Front End pool, Director, Director pool, Office Web Apps for conferencing</span></span></p></td>
<td><p><span data-ttu-id="f3ecc-142">El tráfico enviado al puerto 443 en la interfaz externa de proxy inverso se redirige a un grupo en el puerto 4443 desde la interfaz interna de proxy invertida para que los servicios web del grupo lo diferencien del tráfico web interno.</span><span class="sxs-lookup"><span data-stu-id="f3ecc-142">Traffic sent to port 443 on the reverse proxy external interface is redirected to a pool on port 4443 from the reverse proxy internal interface so that the pool web services can distinguish it from internal web traffic.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f3ecc-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3ecc-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

