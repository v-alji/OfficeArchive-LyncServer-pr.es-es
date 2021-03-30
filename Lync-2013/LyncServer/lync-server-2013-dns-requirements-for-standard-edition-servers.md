---
title: 'Lync Server 2013: requisitos DNS para servidores Standard Edition'
description: 'Lync Server 2013: requisitos DNS para servidores Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Standard Edition servers
ms:assetid: 3d6bbe65-e7ce-491b-a0bd-d2f7197f240d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425900(v=OCS.15)
ms:contentKeyID: 48183920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc93549e07fb82304ad76b051730eab972530764
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398184"
---
# <a name="dns-requirements-for-standard-edition-servers-in-lync-server-2013"></a><span data-ttu-id="375f2-103">Requisitos DNS para servidores Standard Edition en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="375f2-103">DNS requirements for Standard Edition servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="375f2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="375f2-104">

<span> </span></span></span>

<span data-ttu-id="375f2-105">_**Tema Última modificación:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="375f2-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="375f2-106">En esta sección se describen los registros del sistema de nombres de dominio (DNS) necesarios para la implementación de servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="375f2-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="375f2-107">Registros de DNS para servidores Standard Edition</span><span class="sxs-lookup"><span data-stu-id="375f2-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="375f2-108">En la tabla siguiente se especifican los requisitos DNS para la implementación del servidor Lync Server 2013 Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="375f2-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>

### <a name="dns-requirements-for-a-standard-edition-server"></a><span data-ttu-id="375f2-109">Requisitos de DNS para un servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="375f2-109">DNS Requirements for a Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="375f2-110">Escenario de implementación</span><span class="sxs-lookup"><span data-stu-id="375f2-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="375f2-111">Requisito de DNS</span><span class="sxs-lookup"><span data-stu-id="375f2-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="375f2-112">Servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="375f2-112">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="375f2-113">Un registro A interno que resuelve el nombre de dominio completo (FQDN) del servidor en su dirección IP.</span><span class="sxs-lookup"><span data-stu-id="375f2-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="375f2-114">Inicio de sesión de clientes automático</span><span class="sxs-lookup"><span data-stu-id="375f2-114">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="375f2-115">Para cada dominio SIP compatible, un registro SRV para _sipinternaltls._tcp. &lt; dominio &gt; a través del puerto 5061 que se asigna al FQDN del servidor Standard Edition que autentica y redirige las solicitudes de inicio de sesión del cliente.</span><span class="sxs-lookup"><span data-stu-id="375f2-115">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="375f2-116">Para obtener más información, vea Requisitos DNS para el inicio de sesión automático del cliente <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">en Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="375f2-116">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="375f2-117">Detección del servicio web de actualización de dispositivos por los dispositivos de comunicaciones unificadas (UC)</span><span class="sxs-lookup"><span data-stu-id="375f2-117">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="375f2-118">Un registro A interno con el nombre ucupdates-r2. &lt; Dominio SIP que se resuelve en la dirección IP del servidor Standard Edition que &gt; hospeda el servicio web de actualización de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="375f2-118">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="375f2-119">En una situación en la que un dispositivo de comunicaciones unificadas esté activado, pero en el que nunca un usuario inició sesión, el registro A permite al dispositivo detectar el servidor que hospeda el servicio web de actualización de dispositivos y obtener actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="375f2-119">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="375f2-120">De lo contrario, los dispositivos obtienen la información del servidor a través del aprovisionamiento en banda la primera vez que un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="375f2-120">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="375f2-121">Un proxy inverso compatible con el tráfico HTTP</span><span class="sxs-lookup"><span data-stu-id="375f2-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="375f2-122">Un registro A externo que resuelve el FQDN externo de la granja de servidores web en la dirección IP externa del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="375f2-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="375f2-123">Los clientes y los dispositivos de UC usan este registro para conectarse al proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="375f2-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="375f2-124">Para obtener más información, vea <a href="lync-server-2013-determine-dns-requirements.md">Determinar los requisitos DNS para Lync Server 2013</a> en la documentación de planeamiento.</span><span class="sxs-lookup"><span data-stu-id="375f2-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="375f2-125">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="375f2-125">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

