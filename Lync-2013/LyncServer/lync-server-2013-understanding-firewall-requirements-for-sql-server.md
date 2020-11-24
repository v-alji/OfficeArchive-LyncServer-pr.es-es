---
title: 'Lync Server 2013: Descripción de los requisitos de firewall para SQL Server'
description: 'Lync Server 2013: Descripción de los requisitos de Firewall para SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding firewall requirements for SQL Server
ms:assetid: 31d7df2c-589f-465e-be74-cf6767db190d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425818(v=OCS.15)
ms:contentKeyID: 48183781
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c434474b36ced0fe64b9398f7d0e6136ff523a93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399485"
---
# <a name="understanding-firewall-requirements-for-sql-server-with-lync-server-2013"></a><span data-ttu-id="db365-103">Descripción de los requisitos de firewall para SQL Server con Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db365-103">Understanding firewall requirements for SQL Server with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db365-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db365-104">

<span> </span></span></span>

<span data-ttu-id="db365-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="db365-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="db365-106">Para una implementación de Standard Edition, las excepciones de Firewall se crean automáticamente durante la instalación de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="db365-106">For a Standard Edition deployment, firewall exceptions are created automatically during Lync Server 2013 Setup.</span></span> <span data-ttu-id="db365-107">Sin embargo, para las implementaciones de Enterprise Edition, debe configurar las excepciones de Firewall manualmente en el servidor back-end de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="db365-107">However, for Enterprise Edition deployments, you must configure the firewall exceptions manually on the SQL Server Back End Server.</span></span> <span data-ttu-id="db365-108">El protocolo TCP/IP permite que un puerto determinado se use una vez para una determinada dirección IP.</span><span class="sxs-lookup"><span data-stu-id="db365-108">The TCP/IP protocol allows for a given port to be used once for a given IP address.</span></span> <span data-ttu-id="db365-109">Esto significa que para el servidor basado en SQL Server, puede asignar la instancia de base de datos predeterminada al puerto TCP predeterminado 1433.</span><span class="sxs-lookup"><span data-stu-id="db365-109">This means that for the SQL Server-based server you can assign the default database instance the default TCP port 1433.</span></span> <span data-ttu-id="db365-110">En el caso de otras instancias, tendrá que usar el administrador de configuración de SQL Server para asignar puertos únicos y sin usar.</span><span class="sxs-lookup"><span data-stu-id="db365-110">For any other instances you will need to use the SQL Server Configuration Manager to assign unique and unused ports.</span></span> <span data-ttu-id="db365-111">Este tema trata:</span><span class="sxs-lookup"><span data-stu-id="db365-111">This topic covers:</span></span>

  - <span data-ttu-id="db365-112">Requisitos para una excepción de Firewall al usar la instancia predeterminada</span><span class="sxs-lookup"><span data-stu-id="db365-112">Requirements for a firewall exception when using the default instance</span></span>

  - <span data-ttu-id="db365-113">Requisitos de una excepción de Firewall para el servicio SQL Server Browser</span><span class="sxs-lookup"><span data-stu-id="db365-113">Requirements for a firewall exception for the SQL Server Browser service</span></span>

  - <span data-ttu-id="db365-114">Requisitos para puertos de escucha estáticos al utilizar instancias con nombre</span><span class="sxs-lookup"><span data-stu-id="db365-114">Requirements for static listening ports when using named instances</span></span>

<div>

## <a name="requirements-for-a-firewall-exception-when-using-the-default-instance"></a><span data-ttu-id="db365-115">Requisitos para una excepción de Firewall al usar la instancia predeterminada</span><span class="sxs-lookup"><span data-stu-id="db365-115">Requirements for a Firewall Exception When Using the Default Instance</span></span>

<span data-ttu-id="db365-116">Si está usando la instancia predeterminada de SQL Server para cualquier base de datos al implementar Lync Server 2013, se usan los siguientes requisitos de regla de Firewall para garantizar la comunicación desde el grupo de servidores front-end a la instancia predeterminada de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="db365-116">If you are using the SQL Server default instance for any database when deploying Lync Server 2013, the following firewall rule requirements are used to help ensure communication from the Front End pool to the SQL Server default instance.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db365-117">Protocolo</span><span class="sxs-lookup"><span data-stu-id="db365-117">Protocol</span></span></th>
<th><span data-ttu-id="db365-118">Puerto</span><span class="sxs-lookup"><span data-stu-id="db365-118">Port</span></span></th>
<th><span data-ttu-id="db365-119">Dirección</span><span class="sxs-lookup"><span data-stu-id="db365-119">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db365-120">TCP</span><span class="sxs-lookup"><span data-stu-id="db365-120">TCP</span></span></p></td>
<td><p><span data-ttu-id="db365-121">1433</span><span class="sxs-lookup"><span data-stu-id="db365-121">1433</span></span></p></td>
<td><p><span data-ttu-id="db365-122">Entrante a SQL Server</span><span class="sxs-lookup"><span data-stu-id="db365-122">Inbound to SQL Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-a-firewall-exception-for-the-sql-server-browser-service"></a><span data-ttu-id="db365-123">Requisitos de una excepción de Firewall para el servicio SQL Server Browser</span><span class="sxs-lookup"><span data-stu-id="db365-123">Requirements for a Firewall Exception for the SQL Server Browser Service</span></span>

<span data-ttu-id="db365-124">El servicio SQL Server Browser buscará instancias de base de datos y comunicará el puerto que la instancia (con nombre o predeterminado) está configurada para usar.</span><span class="sxs-lookup"><span data-stu-id="db365-124">The SQL Server Browser service will locate database instances and communicate the port that the instance (named or default) is configured to use.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db365-125">Protocolo</span><span class="sxs-lookup"><span data-stu-id="db365-125">Protocol</span></span></th>
<th><span data-ttu-id="db365-126">Puerto</span><span class="sxs-lookup"><span data-stu-id="db365-126">Port</span></span></th>
<th><span data-ttu-id="db365-127">Dirección</span><span class="sxs-lookup"><span data-stu-id="db365-127">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db365-128">UDP</span><span class="sxs-lookup"><span data-stu-id="db365-128">UDP</span></span></p></td>
<td><p><span data-ttu-id="db365-129">1434</span><span class="sxs-lookup"><span data-stu-id="db365-129">1434</span></span></p></td>
<td><p><span data-ttu-id="db365-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="db365-130">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-static-listening-ports-when-using-named-instances"></a><span data-ttu-id="db365-131">Requisitos para puertos de escucha estáticos al utilizar instancias con nombre</span><span class="sxs-lookup"><span data-stu-id="db365-131">Requirements for Static Listening Ports When Using Named Instances</span></span>

<span data-ttu-id="db365-132">Al usar instancias con nombre en la configuración de SQL Server para bases de datos compatibles con Lync Server 2013, debe configurar los puertos estáticos mediante el administrador de configuración de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="db365-132">When using named instances in the SQL Server configuration for databases supporting Lync Server 2013, you configure static ports by using SQL Server Configuration Manager.</span></span> <span data-ttu-id="db365-133">Después de asignar los puertos estáticos a cada instancia con nombre, cree excepciones para cada puerto estático en el firewall.</span><span class="sxs-lookup"><span data-stu-id="db365-133">After the static ports have been assigned to each named instance, you create exceptions for each static port in the firewall.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db365-134">Protocolo</span><span class="sxs-lookup"><span data-stu-id="db365-134">Protocol</span></span></th>
<th><span data-ttu-id="db365-135">Puerto</span><span class="sxs-lookup"><span data-stu-id="db365-135">Port</span></span></th>
<th><span data-ttu-id="db365-136">Dirección</span><span class="sxs-lookup"><span data-stu-id="db365-136">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db365-137">TCP</span><span class="sxs-lookup"><span data-stu-id="db365-137">TCP</span></span></p></td>
<td><p><span data-ttu-id="db365-138">Definición estática</span><span class="sxs-lookup"><span data-stu-id="db365-138">Statically defined</span></span></p></td>
<td><p><span data-ttu-id="db365-139">Entrada</span><span class="sxs-lookup"><span data-stu-id="db365-139">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sql-server-documentation"></a><span data-ttu-id="db365-140">Documentación de SQL Server</span><span class="sxs-lookup"><span data-stu-id="db365-140">SQL Server Documentation</span></span>

<span data-ttu-id="db365-141">La documentación de 2012 de Microsoft SQL Server proporciona instrucciones detalladas sobre cómo configurar el acceso a Firewall para bases de datos.</span><span class="sxs-lookup"><span data-stu-id="db365-141">Microsoft SQL Server 2012 documentation provides detailed guidance on how to configure firewall access for databases.</span></span> <span data-ttu-id="db365-142">Para obtener más información sobre Microsoft SQL Server 2012, consulte "configurar el Firewall de Windows para permitir el acceso a SQL Server" en [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031) .</span><span class="sxs-lookup"><span data-stu-id="db365-142">For details about Microsoft SQL Server 2012, see “Configuring the Windows Firewall to Allow SQL Server Access” at [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031).</span></span>

<span data-ttu-id="db365-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db365-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

