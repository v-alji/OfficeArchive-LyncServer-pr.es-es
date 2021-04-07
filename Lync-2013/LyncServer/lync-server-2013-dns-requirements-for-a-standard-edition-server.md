---
title: 'Lync Server 2013: Requisitos DNS para un servidor Standard Edition'
description: 'Lync Server 2013: requisitos DNS para un servidor Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for a Standard Edition server
ms:assetid: 5d1daf54-6e60-4ce0-9254-7d57a0835fa4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204936(v=OCS.15)
ms:contentKeyID: 48184259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea0c7219563d62a9d99bd85655b3d3fcb0c551f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399750"
---
# <a name="dns-requirements-for-a-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="a6d66-103">Requisitos DNS para un servidor Standard Edition en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6d66-103">DNS requirements for a Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6d66-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6d66-104">

<span> </span></span></span>

<span data-ttu-id="a6d66-105">_**Tema Última modificación:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="a6d66-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="a6d66-106">En esta sección se describen los registros del sistema de nombres de dominio (DNS) necesarios para la implementación de servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a6d66-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="a6d66-107">Registros de DNS para servidores Standard Edition</span><span class="sxs-lookup"><span data-stu-id="a6d66-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="a6d66-108">En la tabla siguiente se especifican los requisitos DNS para la implementación del servidor Lync Server 2013 Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a6d66-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6d66-109">Escenario de implementación</span><span class="sxs-lookup"><span data-stu-id="a6d66-109">Deployment scenario</span></span></th>
<th><span data-ttu-id="a6d66-110">Requisito de DNS</span><span class="sxs-lookup"><span data-stu-id="a6d66-110">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6d66-111">Servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="a6d66-111">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="a6d66-112">Un registro A interno que resuelve el nombre de dominio completo (FQDN) del servidor en su dirección IP.</span><span class="sxs-lookup"><span data-stu-id="a6d66-112">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6d66-113">Inicio de sesión de clientes automático</span><span class="sxs-lookup"><span data-stu-id="a6d66-113">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="a6d66-114">Para cada dominio SIP compatible, un registro SRV para _sipinternaltls._tcp. &lt; dominio &gt; a través del puerto 5061 que se asigna al FQDN del servidor Standard Edition que autentica y redirige las solicitudes de inicio de sesión del cliente.</span><span class="sxs-lookup"><span data-stu-id="a6d66-114">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="a6d66-115">Para obtener más información, vea Requisitos DNS para el inicio de sesión automático del cliente <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">en Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="a6d66-115">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6d66-116">Detección del servicio web de actualización de dispositivos por los dispositivos de comunicaciones unificadas (UC)</span><span class="sxs-lookup"><span data-stu-id="a6d66-116">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="a6d66-117">Un registro A interno con el nombre ucupdates-r2. &lt; Dominio SIP que se resuelve en la dirección IP del servidor Standard Edition que &gt; hospeda el servicio web de actualización de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a6d66-117">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="a6d66-118">En una situación en la que un dispositivo de comunicaciones unificadas esté activado, pero en el que nunca un usuario inició sesión, el registro A permite al dispositivo detectar el servidor que hospeda el servicio web de actualización de dispositivos y obtener actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="a6d66-118">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="a6d66-119">De lo contrario, los dispositivos obtienen la información del servidor a través del aprovisionamiento en banda la primera vez que un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="a6d66-119">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span> <span data-ttu-id="a6d66-120">Para obtener más información, vea <a href="lync-server-2013-device-update-web-service.md">Servicio web de actualización de dispositivos en Lync Server 2013</a> en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="a6d66-120">For details, see <a href="lync-server-2013-device-update-web-service.md">Device Update Web service in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6d66-121">Un proxy inverso compatible con el tráfico HTTP</span><span class="sxs-lookup"><span data-stu-id="a6d66-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="a6d66-122">Un registro A externo que resuelve el FQDN externo de la granja de servidores web en la dirección IP externa del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="a6d66-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="a6d66-123">Los clientes y los dispositivos de UC usan este registro para conectarse al proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="a6d66-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="a6d66-124">Para obtener más información, vea <a href="lync-server-2013-determine-dns-requirements.md">Determinar los requisitos DNS para Lync Server 2013</a> en la documentación de planeamiento.</span><span class="sxs-lookup"><span data-stu-id="a6d66-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a6d66-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6d66-125">See Also</span></span>


[<span data-ttu-id="a6d66-126">Requisitos DNS para el inicio de sesión automático del cliente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6d66-126">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)  
[<span data-ttu-id="a6d66-127">Determinar los requisitos DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6d66-127">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="a6d66-128">Servicio web de actualización de dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6d66-128">Device Update Web service in Lync Server 2013</span></span>](lync-server-2013-device-update-web-service.md)  
  

<span data-ttu-id="a6d66-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6d66-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

