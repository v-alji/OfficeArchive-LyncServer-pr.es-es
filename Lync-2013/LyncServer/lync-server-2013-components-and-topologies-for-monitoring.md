---
title: 'Lync Server 2013: Componentes y topologías para la supervisión'
description: 'Lync Server 2013: componentes y topologías que se supervisan.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components and topologies for monitoring
ms:assetid: c1bb36b0-1fb8-4d8e-9cc9-9bef740fe3c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412952(v=OCS.15)
ms:contentKeyID: 48185313
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8767a7eb16ca85e9606838606a6e86ee1296fc0e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434581"
---
# <a name="components-and-topologies-for-monitoring-in-lync-server-2013"></a><span data-ttu-id="76953-103">Componentes y topologías para la supervisión en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76953-103">Components and topologies for monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="76953-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="76953-104">

<span> </span></span></span>

<span data-ttu-id="76953-105">_**Última modificación del tema:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="76953-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="76953-106">Debido a que los agentes de recopilación de datos unificados se instalan y activan automáticamente en cada servidor front-end, no es necesario configurar un servidor para que actúe como servidor de supervisión; cada servidor front-end funciona como servidor de supervisión.</span><span class="sxs-lookup"><span data-stu-id="76953-106">Because the unified data collection agents are automatically installed and activated on each Front End server you do not need to configure a server to act as the Monitoring server; each Front End server already functions as a Monitoring server.</span></span> <span data-ttu-id="76953-107">Sin embargo, necesitará instalar y configurar una base de datos para que actúe como almacén de datos del back-end para los datos de supervisión.</span><span class="sxs-lookup"><span data-stu-id="76953-107">However, you will need to install and configure a database to act as the backend data store for your monitoring data.</span></span> <span data-ttu-id="76953-108">Microsoft Lync Server 2013 puede usar cualquiera de las siguientes bases de datos como almacén back-end para la supervisión:</span><span class="sxs-lookup"><span data-stu-id="76953-108">Microsoft Lync Server 2013 can use any of the following databases as the backend store for monitoring:</span></span>

  - <span data-ttu-id="76953-109">Microsoft SQL Server 2008 R2 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="76953-109">Microsoft SQL Server 2008 R2 Enterprise Edition</span></span>

  - <span data-ttu-id="76953-110">Microsoft SQL Server 2008 R2 Standard Edition</span><span class="sxs-lookup"><span data-stu-id="76953-110">Microsoft SQL Server 2008 R2 Standard Edition</span></span>

  - <span data-ttu-id="76953-111">Microsoft SQL Server 2012 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="76953-111">Microsoft SQL Server 2012 Enterprise Edition</span></span>

  - <span data-ttu-id="76953-112">Microsoft SQL Server 2012 Standard Edition</span><span class="sxs-lookup"><span data-stu-id="76953-112">Microsoft SQL Server 2012 Standard Edition</span></span>

<span data-ttu-id="76953-113">Tenga en cuenta que debe usar las ediciones de 64 bits de estas bases de datos; las versiones de 32 bits de SQL Server no se pueden usar como almacén de back-end para la supervisión.</span><span class="sxs-lookup"><span data-stu-id="76953-113">Note that you must use the 64-bit editions of these databases; 32-bit versions of SQL Server cannot be used as the backend store for monitoring.</span></span> <span data-ttu-id="76953-114">Del mismo modo, Lync Server 2013 no es compatible con las ediciones Express de SQL Server 2008 o SQL Server 2012.</span><span class="sxs-lookup"><span data-stu-id="76953-114">Likewise, Lync Server 2013 does not support the Express Editions of SQL Server 2008 or SQL Server 2012.</span></span> <span data-ttu-id="76953-115">Para obtener más información sobre los requisitos de base de datos de Lync Server 2013 consulte el tema [compatibilidad de software de base de datos en Lync server 2013](lync-server-2013-database-software-support.md) en la guía de compatibilidad de lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="76953-115">For more information on database requirements for Lync Server 2013 see the topic [Database software support in Lync Server 2013](lync-server-2013-database-software-support.md) in the Lync Server 2013 Supportability guide.</span></span>

<span data-ttu-id="76953-116">Recuerde que es preciso que SQL Server esté instalado y configurado antes de implementar y configurar la supervisión.</span><span class="sxs-lookup"><span data-stu-id="76953-116">Keep in mind that SQL Server must be installed and configured before you deploy and configure monitoring.</span></span> <span data-ttu-id="76953-117">Sin embargo, solo necesita implementar SQL Server en sí; no es necesario configurar las bases de datos de supervisión con antelación.</span><span class="sxs-lookup"><span data-stu-id="76953-117">However, you only need to deploy SQL Server itself; you do not have to setup the monitoring databases in advance.</span></span> <span data-ttu-id="76953-118">En su lugar, estas bases de datos se crearán automáticamente cuando publique la topología de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="76953-118">Instead, those databases will automatically be created for you when you publish your Lync Server topology.</span></span>

<span data-ttu-id="76953-p104">Al supervisar los datos se puede compartir una instancia de SQL Server con otros tipos de datos. Generalmente, las bases de datos del registro detallado de llamadas (LcsCdr) y de la calidad de la experiencia (QoEMetrics) comparten la misma instancia de SQL. También es habitual que las dos bases de datos de supervisión se encuentren en la misma instancia de SQL que la base de datos de archivado (LcsLog). El único requisito real con relación a las instancias de SQL Server es que cada una de ellas se limite conforme a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="76953-p104">Monitoring data can share a SQL Server instance with other types of data. Typically, the call detail recording database (LcsCdr) and the Quality of Experience database (QoEMetrics) share the same SQL instance; it is also common for the two monitoring databases to be in the same SQL instance as the archiving database (LcsLog). About the only real requirement with SQL Server instances is that any one instance of SQL Server is limited to the following:</span></span>

  - <span data-ttu-id="76953-122">Una instancia de la base de datos back-end de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="76953-122">One instance of the Lync Server 2013 backend database.</span></span> <span data-ttu-id="76953-123">Como norma general, no recomendamos que la base de datos de supervisión se encuentre en la misma instancia de SQL, ni siquiera en el mismo equipo, que la base de datos back-end.</span><span class="sxs-lookup"><span data-stu-id="76953-123">(As a general rule, it is not recommended that your monitoring database be collocated in the same SQL instance, or even on the same computer, as the backend database.</span></span> <span data-ttu-id="76953-124">Aunque técnicamente es posible, corre el riesgo de que la base de datos de supervisión agote el espacio en disco que necesita la base de datos back-end.</span><span class="sxs-lookup"><span data-stu-id="76953-124">Although technically possible, you run the risk of the monitoring database using up disk space needed by the backend database.)</span></span>

  - <span data-ttu-id="76953-125">Una instancia de la base de datos del registro detallado de llamadas.</span><span class="sxs-lookup"><span data-stu-id="76953-125">One instance of the call detail recording database.</span></span>

  - <span data-ttu-id="76953-126">Una instancia de la base de datos de la calidad de la experiencia.</span><span class="sxs-lookup"><span data-stu-id="76953-126">One instance of the Quality of Experience database.</span></span>

  - <span data-ttu-id="76953-127">Una instancia de la base de datos de archivado.</span><span class="sxs-lookup"><span data-stu-id="76953-127">One instance of the archiving database.</span></span>

<span data-ttu-id="76953-128">En otras palabras, no puede tener dos instancias de la base de datos LcsCdr en la misma instancia de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="76953-128">In other words, you cannot have two instances of the LcsCdr database in the same instance of SQL Server.</span></span> <span data-ttu-id="76953-129">Si necesita varias instancias de la base de datos LcsCdr, tendrá que configurar varias instancias de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="76953-129">If you need multiple instances of the LcsCdr database then you will need to configure multiple instances of SQL Server.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="76953-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="76953-130">See Also</span></span>


[<span data-ttu-id="76953-131">Implementación de la supervisión en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76953-131">Deploying monitoring in Lync Server 2013</span></span>](lync-server-2013-deploying-monitoring.md)  
  

<span data-ttu-id="76953-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="76953-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

