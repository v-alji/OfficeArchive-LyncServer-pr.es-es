---
title: 'Lync Server 2013: requisitos de DNS para servidores de chat persistentes'
description: 'Lync Server 2013: requisitos de DNS para servidores de chat persistentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Persistent Chat Servers
ms:assetid: f7531374-d7ed-4b63-ae81-02294cb4496a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205391(v=OCS.15)
ms:contentKeyID: 48185857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01bfc126ab588542ef5160a0eabe0c839dcf0e44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429059"
---
# <a name="dns-requirements-for-persistent-chat-servers-in-lync-server-2013"></a><span data-ttu-id="5dcb1-103">Requisitos de DNS para servidores de chat persistentes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5dcb1-103">DNS requirements for Persistent Chat Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5dcb1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5dcb1-104">

<span> </span></span></span>

<span data-ttu-id="5dcb1-105">_**Última modificación del tema:** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="5dcb1-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="5dcb1-106">En esta sección se describen los registros del sistema de nombres de dominio (DNS) necesarios para la implementación de servidores de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="5dcb1-106">This section describes the Domain Name System (DNS) records that are required for deployment of Persistent Chat Servers.</span></span>

<div>

## <a name="dns-records-for-persistent-chat-servers"></a><span data-ttu-id="5dcb1-107">Registros de DNS para los servidores de chat persistente</span><span class="sxs-lookup"><span data-stu-id="5dcb1-107">DNS Records for Persistent Chat Servers</span></span>

<span data-ttu-id="5dcb1-108">En la tabla siguiente se especifican los requisitos de DNS para la implementación del servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="5dcb1-108">The following table specifies DNS requirements for Persistent Chat Server deployment.</span></span>

### <a name="dns-requirements-for-a-persistent-chat-server"></a><span data-ttu-id="5dcb1-109">Requisitos de DNS para un servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="5dcb1-109">DNS Requirements for a Persistent Chat Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5dcb1-110">Escenario de implementación</span><span class="sxs-lookup"><span data-stu-id="5dcb1-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="5dcb1-111">Requisito de DNS</span><span class="sxs-lookup"><span data-stu-id="5dcb1-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dcb1-112">Un servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="5dcb1-112">One Persistent Chat Server</span></span></p></td>
<td><p><span data-ttu-id="5dcb1-113">Un registro A interno que resuelve el nombre de dominio completo (FQDN) del servidor en su dirección IP.</span><span class="sxs-lookup"><span data-stu-id="5dcb1-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dcb1-114">Grupo de servidores de chat persistente</span><span class="sxs-lookup"><span data-stu-id="5dcb1-114">Persistent Chat pool</span></span></p></td>
<td><p><span data-ttu-id="5dcb1-115">Un registro A interno que resuelve el nombre de dominio completo (FQDN) de los servidores en su dirección IP.</span><span class="sxs-lookup"><span data-stu-id="5dcb1-115">An internal A record that resolves the fully qualified domain name (FQDN) of the servers to its IP address.</span></span></p>
<p><span data-ttu-id="5dcb1-116"><strong>Ejemplo</strong></span><span class="sxs-lookup"><span data-stu-id="5dcb1-116"><strong>Example</strong></span></span></p>
<p><span data-ttu-id="5dcb1-117">PersistentChatServer01.contoso.com 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="5dcb1-117">PersistentChatServer01.contoso.com     10.10.10.1</span></span></p>
<p><span data-ttu-id="5dcb1-118">PersistentChatServer02.contoso.com 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="5dcb1-118">PersistentChatServer02.contoso.com     10.10.10.2</span></span></p>
<p><span data-ttu-id="5dcb1-119">Un registro A interno que resuelve el nombre de dominio completo (FQDN) de los servidores en su dirección IP.</span><span class="sxs-lookup"><span data-stu-id="5dcb1-119">An internal A record that resolves the fully qualified domain name (FQDN) of the servers to its IP address.</span></span></p>
<p><span data-ttu-id="5dcb1-120"><strong>Ejemplo</strong></span><span class="sxs-lookup"><span data-stu-id="5dcb1-120"><strong>Example</strong></span></span></p>
<p><span data-ttu-id="5dcb1-121">PersistentChatPool.contoso.com 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="5dcb1-121">PersistentChatPool.contoso.com    10.10.10.1</span></span></p>
<p><span data-ttu-id="5dcb1-122">PersistentChatPool.contoso.com 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="5dcb1-122">PersistentChatPool.contoso.com    10.10.10.2</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5dcb1-123">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5dcb1-123">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

