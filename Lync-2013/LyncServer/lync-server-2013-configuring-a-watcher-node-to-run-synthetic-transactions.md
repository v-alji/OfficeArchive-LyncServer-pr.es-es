---
title: 'Lync Server 2013: configuración de un nodo de monitor para ejecutar transacciones sintéticas'
description: 'Lync Server 2013: configuración de un nodo de monitor para ejecutar transacciones sintéticas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to run synthetic transactions
ms:assetid: cedda508-8881-4079-88d5-49798f342ddf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205314(v=OCS.15)
ms:contentKeyID: 48185578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd5fdb3d1a1499a6ef79e962a41d9eb3ee174c33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433475"
---
# <a name="configuring-a-watcher-node-to-run-synthetic-transactions-in-lync-server-2013"></a><span data-ttu-id="131a5-103">Configuración de un nodo de monitor para ejecutar transacciones sintéticas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="131a5-103">Configuring a watcher node to run synthetic transactions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="131a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="131a5-104">

<span> </span></span></span>

<span data-ttu-id="131a5-105">_**Última modificación del tema:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="131a5-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="131a5-106">Una vez instalados los archivos del agente de System Center, debe configurar el nodo de monitor en sí.</span><span class="sxs-lookup"><span data-stu-id="131a5-106">After the System Center agent files have been installed, you must next configure the watcher node itself.</span></span> <span data-ttu-id="131a5-107">Los pasos que debe seguir para configurar un nodo de monitor variarán en función de si el equipo nodo de observador está dentro de la red perimetral o fuera de la red perimetral.</span><span class="sxs-lookup"><span data-stu-id="131a5-107">The steps you take to configure a watcher node will vary depending on whether your watcher node computer lies inside your perimeter network or outside your perimeter network.</span></span>

<span data-ttu-id="131a5-108">Al configurar un nodo de monitor, también debe elegir el tipo de método de autenticación que se va a usar en ese nodo.</span><span class="sxs-lookup"><span data-stu-id="131a5-108">When you configure a watcher node, you must also choose the type of authentication method to be employed by that node.</span></span> <span data-ttu-id="131a5-109">Lync Server 2013 le permite elegir uno de los dos métodos de autenticación: servidor de confianza o autenticación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="131a5-109">Lync Server 2013 enables you to choose one of two authentication methods: Trusted Server or Credential Authentication.</span></span> <span data-ttu-id="131a5-110">Las diferencias entre estos dos métodos se describen en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="131a5-110">The differences between these two methods are outlined in the following table:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="131a5-111">Configuración</span><span class="sxs-lookup"><span data-stu-id="131a5-111">Configuration</span></span></th>
<th><span data-ttu-id="131a5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="131a5-112">Description</span></span></th>
<th><span data-ttu-id="131a5-113">Ubicaciones admitidas</span><span class="sxs-lookup"><span data-stu-id="131a5-113">Locations Supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="131a5-114">Servidor de confianza</span><span class="sxs-lookup"><span data-stu-id="131a5-114">Trusted Server</span></span></p></td>
<td><p><span data-ttu-id="131a5-115">Usa un certificado para representar a un servidor interno y evitar problemas de autenticación.</span><span class="sxs-lookup"><span data-stu-id="131a5-115">Uses a certificate to impersonate an internal server and bypass authentication challenges.</span></span></p>
<p><span data-ttu-id="131a5-116">Esto es útil para los administradores que prefieren administrar un único certificado en lugar de muchas contraseñas de usuario en cada nodo de monitor.</span><span class="sxs-lookup"><span data-stu-id="131a5-116">This is useful for administrators who would prefer to manage a single certificate instead of many user passwords on each watcher node.</span></span></p></td>
<td><p><span data-ttu-id="131a5-117">Dentro de la empresa.</span><span class="sxs-lookup"><span data-stu-id="131a5-117">Inside the enterprise.</span></span></p>
<p><span data-ttu-id="131a5-118">Tenga en cuenta que, con este método, el nodo de monitor debe estar en el mismo dominio que los grupos que se están supervisando.</span><span class="sxs-lookup"><span data-stu-id="131a5-118">Note that, with this method, the watcher node must be in the same domain as the pools being monitored.</span></span> <span data-ttu-id="131a5-119">Si el nodo de monitor y los grupos supervisados se encuentran en dominios diferentes, use en su lugar la autenticación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="131a5-119">If the watcher node and the monitored pools are in different domains, use Credential Authentication instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="131a5-120">Autenticación de credenciales</span><span class="sxs-lookup"><span data-stu-id="131a5-120">Credential Authentication</span></span></p></td>
<td><p><span data-ttu-id="131a5-121">Almacena los nombres de usuario y las contraseñas con seguridad en Windows Credential Manager en cada nodo de monitor.</span><span class="sxs-lookup"><span data-stu-id="131a5-121">Stores user names and passwords securely in Windows Credential Manager on each watcher node.</span></span></p>
<p><span data-ttu-id="131a5-122">Este modo requiere más administración de contraseñas, pero es la única opción para los nodos de monitor que se encuentran fuera de la empresa.</span><span class="sxs-lookup"><span data-stu-id="131a5-122">This mode requires more password management, but is the only option for watcher nodes located outside of the enterprise.</span></span> <span data-ttu-id="131a5-123">Estos nodos de monitor no se pueden tratar como un extremo de confianza para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="131a5-123">These watcher nodes cannot be treated as an endpoint trusted for authentication.</span></span></p></td>
<td><p><span data-ttu-id="131a5-124">Fuera de la empresa.</span><span class="sxs-lookup"><span data-stu-id="131a5-124">Outside the enterprise.</span></span></p>
<p><span data-ttu-id="131a5-125">Dentro de la empresa.</span><span class="sxs-lookup"><span data-stu-id="131a5-125">Inside the enterprise.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="131a5-126">También debe verificar que el firewall tiene reglas de entrada para MonitoringHost.exe y PowerShell.exe.</span><span class="sxs-lookup"><span data-stu-id="131a5-126">You should also verify that your firewall has inbound rules for both MonitoringHost.exe and PowerShell.exe.</span></span> <span data-ttu-id="131a5-127">Si el Firewall bloquea estos procesos, las transacciones sintéticas fallarán con un error de 504 (tiempo de espera del servidor).</span><span class="sxs-lookup"><span data-stu-id="131a5-127">If these processes are blocked by the firewall then your synthetic transactions will fail with a 504 (server timeout) error.</span></span>

<span data-ttu-id="131a5-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="131a5-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

