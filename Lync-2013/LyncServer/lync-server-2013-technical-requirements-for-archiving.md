---
title: 'Lync Server 2013: requisitos técnicos para el archivado'
description: 'Lync Server 2013: requisitos técnicos para el archivado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Archiving
ms:assetid: 896d60e2-be4b-462d-8357-4cd307ab7304
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205059(v=OCS.15)
ms:contentKeyID: 48184732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6100753ad2c62424eb68c8c258094ba51848170e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423389"
---
# <a name="technical-requirements-for-archiving-in-lync-server-2013"></a><span data-ttu-id="1cace-103">Requisitos técnicos para archivar en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cace-103">Technical requirements for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1cace-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1cace-104">

<span> </span></span></span>

<span data-ttu-id="1cace-105">_**Última modificación del tema:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="1cace-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="1cace-106">Entre los requisitos técnicos de Lync Server 2013 se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1cace-106">Lync Server 2013 technical requirements include the following:</span></span>

  - <span data-ttu-id="1cace-107">Requisitos de infraestructura.</span><span class="sxs-lookup"><span data-stu-id="1cace-107">Infrastructure requirements.</span></span>

  - <span data-ttu-id="1cace-108">Requisitos previos de software que deben instalarse para el archivado.</span><span class="sxs-lookup"><span data-stu-id="1cace-108">Prerequisite software that must be installed for Archiving.</span></span>

  - <span data-ttu-id="1cace-109">Requisitos de almacenamiento de datos para archivar.</span><span class="sxs-lookup"><span data-stu-id="1cace-109">Data storage requirements for Archiving.</span></span>

  - <span data-ttu-id="1cace-110">Las consideraciones y los requisitos de escalado para la implementación de archivado.</span><span class="sxs-lookup"><span data-stu-id="1cace-110">Scaling requirements and considerations for your Archiving deployment.</span></span>

  - <span data-ttu-id="1cace-111">Consideraciones y requisitos de rendimiento para las bases de datos de archivado.</span><span class="sxs-lookup"><span data-stu-id="1cace-111">Performance requirements and considerations for your Archiving databases.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1cace-112">La información de escalabilidad y rendimiento no está disponible en esta versión 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1cace-112">Scaling and performance information is not available in this Lync Server 2013 release.</span></span>



</div>

<div>

## <a name="infrastructure-requirements"></a><span data-ttu-id="1cace-113">Requisitos de infraestructura</span><span class="sxs-lookup"><span data-stu-id="1cace-113">Infrastructure Requirements</span></span>

<span data-ttu-id="1cace-114">Los requisitos de la infraestructura de archivado de Lync Server 2013 son los mismos que para la implementación de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1cace-114">Lync Server 2013 Archiving infrastructure requirements are the same as for deployment of Lync Server 2013.</span></span> <span data-ttu-id="1cace-115">Para obtener más información, consulte [determinar los requisitos de infraestructura para Lync Server 2013](lync-server-2013-determining-your-infrastructure-requirements.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="1cace-115">For details, see [Determining your infrastructure requirements for Lync Server 2013](lync-server-2013-determining-your-infrastructure-requirements.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="archiving-prerequisites"></a><span data-ttu-id="1cace-116">Requisitos previos de archivado</span><span class="sxs-lookup"><span data-stu-id="1cace-116">Archiving Prerequisites</span></span>

<span data-ttu-id="1cace-117">Lync Server 2013 optimiza los requisitos previos para el archivado debido a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1cace-117">Lync Server 2013 streamlines prerequisites for Archiving because of the following:</span></span>

  - <span data-ttu-id="1cace-118">El servidor de archivado ya no es un rol de servidor.</span><span class="sxs-lookup"><span data-stu-id="1cace-118">Archiving Server is no longer a server role.</span></span> <span data-ttu-id="1cace-119">En su lugar, los agentes de recopilación de datos unificados se ejecutan en los servidores front-end de un grupo de servidores y servidores Standard Edition para capturar datos para su archivado, por lo que no se configuran plataformas de sistema independientes para archivar.</span><span class="sxs-lookup"><span data-stu-id="1cace-119">Instead, Unified Data Collection Agents run on the Front End Servers in a pool and Standard Edition servers to capture data for Archiving, so you do not set up separate system platforms for Archiving.</span></span>

  - <span data-ttu-id="1cace-120">El archivado usa el almacenamiento de archivos de Lync Server 2013 para almacenar temporalmente los archivos de contenido de la reunión, por lo que no se configura un almacén de archivos independiente para archivado.</span><span class="sxs-lookup"><span data-stu-id="1cace-120">Archiving uses the Lync Server 2013 file storage for temporary storage of meeting content files, so you do not set up a separate file store for archiving.</span></span>

  - <span data-ttu-id="1cace-121">En Lync Server 2013, no se necesita Message Queue Server.</span><span class="sxs-lookup"><span data-stu-id="1cace-121">In Lync Server 2013, Message Queuing is not required.</span></span>

</div>

<div>

## <a name="data-storage-requirements-for-archiving"></a><span data-ttu-id="1cace-122">Requisitos de almacenamiento de datos para archivar</span><span class="sxs-lookup"><span data-stu-id="1cace-122">Data Storage Requirements for Archiving</span></span>

<span data-ttu-id="1cace-123">Además, debe configurar la infraestructura para archivar el almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="1cace-123">Additionally, you need to set up the infrastructure for Archiving storage.</span></span> <span data-ttu-id="1cace-124">Esto incluye una o ambas de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="1cace-124">This includes one or both of the following:</span></span>

  - <span data-ttu-id="1cace-125">**Almacenamiento de Microsoft Exchange**.</span><span class="sxs-lookup"><span data-stu-id="1cace-125">**Microsoft Exchange storage**.</span></span> <span data-ttu-id="1cace-126">Meeting content files, such as PowerPoint presentations, are archived as attachments.</span><span class="sxs-lookup"><span data-stu-id="1cace-126">Meeting content files, such as PowerPoint presentations, are archived as attachments.</span></span> <span data-ttu-id="1cace-127">Si desea usar la integración de Microsoft Exchange para que los datos del archivo de Lync se almacenen con datos de cumplimiento de Exchange, debe usar Exchange 2013 para su implementación de Exchange y asegurarse de que el tamaño máximo de almacenamiento admita el almacenamiento de los archivos de contenido de la reunión.</span><span class="sxs-lookup"><span data-stu-id="1cace-127">If you want to use Microsoft Exchange integration so that Lync archive data is stored with Exchange compliance data, you must use Exchange 2013 for your Exchange deployment and ensure that the maximum storage size supports storage of the meeting content files.</span></span> <span data-ttu-id="1cace-128">Si implementa el archivado con la opción de integración de Microsoft Exchange, los datos del archivo de Lync se almacenan con los datos de cumplimiento de Exchange 2013 solo para los usuarios alojados en los servidores de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="1cace-128">If you deploy Archiving using the Microsoft Exchange integration option, Lync archive data is stored with Exchange 2013 compliance data only for the users who are homed on your Exchange 2013 servers.</span></span> <span data-ttu-id="1cace-129">Debe implementar Exchange 2013 antes de implementar y habilitar el archivado mediante la opción de integración de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="1cace-129">You must deploy Exchange 2013 prior to deploying and enabling Archiving using the Microsoft Exchange integration option.</span></span> <span data-ttu-id="1cace-130">Si elige usar el almacenamiento de Exchange 2013, no necesita implementar bases de datos de SQL Server independientes para archivar, a menos que tenga usuarios de Lync que no estén alojados en los servidores de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="1cace-130">If you choose to use Exchange 2013 storage, you do not need to deploy separate SQL Server databases for Archiving, unless you have Lync users who are not homed on your Exchange 2013 servers.</span></span>

  - <span data-ttu-id="1cace-131">**Almacenamiento de base de datos de SQL Server para archivar**.</span><span class="sxs-lookup"><span data-stu-id="1cace-131">**SQL Server database storage for Archiving**.</span></span> <span data-ttu-id="1cace-132">Para admitir usuarios que no están alojados en servidores de Exchange 2013, o si no desea usar la opción de integración de Microsoft Exchange, debe implementar el almacenamiento de archivado con una base de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1cace-132">To support users who are not homed on Exchange 2013 servers, or if you do not want to use the Microsoft Exchange integration option, you must deploy Archiving storage using a SQL Server database.</span></span> <span data-ttu-id="1cace-133">Lync Server 2013 admite las siguientes versiones de 64 bits de SQL Server:</span><span class="sxs-lookup"><span data-stu-id="1cace-133">Lync Server 2013 supports the following 64-bit versions of SQL Server:</span></span>
    
      - <span data-ttu-id="1cace-134">Microsoft SQL Server 2008 R2 Enterprise</span><span class="sxs-lookup"><span data-stu-id="1cace-134">Microsoft SQL Server 2008 R2 Enterprise</span></span>
    
      - <span data-ttu-id="1cace-135">Microsoft SQL Server 2008 R2 Standard</span><span class="sxs-lookup"><span data-stu-id="1cace-135">Microsoft SQL Server 2008 R2 Standard</span></span>
    
      - <span data-ttu-id="1cace-136">Microsoft SQL Server 2012 Enterprise</span><span class="sxs-lookup"><span data-stu-id="1cace-136">Microsoft SQL Server 2012 Enterprise</span></span>
    
      - <span data-ttu-id="1cace-137">Microsoft SQL Server 2012 Standard</span><span class="sxs-lookup"><span data-stu-id="1cace-137">Microsoft SQL Server 2012 Standard</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cace-138">Microsoft SQL Server 2008 R2 Express y Microsoft SQL Server 2012 Express no son compatibles con el archivado.</span><span class="sxs-lookup"><span data-stu-id="1cace-138">Microsoft SQL Server 2008 R2 Express and Microsoft SQL Server 2012 Express are not supported for Archiving.</span></span> <span data-ttu-id="1cace-139">no se admiten las versiones de 32 bits de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1cace-139">32-bit versions of SQL Server are not supported.</span></span> <span data-ttu-id="1cace-140">Para obtener más información sobre restricciones y requisitos de SQL Server, consulte <A href="lync-server-2013-database-software-support.md">compatibilidad de software de base de datos en Lync Server 2013</A> en la documentación de planeación o en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="1cace-140">For additional SQL Server requirements and restrictions, see <A href="lync-server-2013-database-software-support.md">Database software support in Lync Server 2013</A> in the Planning documentation or in the Supportability documentation.</span></span>

    
    </div>
    
    <span data-ttu-id="1cace-141">Debe configurar las plataformas de SQL Server antes de implementar y habilitar el archivado.</span><span class="sxs-lookup"><span data-stu-id="1cace-141">You must set up the SQL Server platforms prior to deploying and enabling Archiving.</span></span> <span data-ttu-id="1cace-142">Si la cuenta que se usará para publicar la topología tiene los derechos y permisos de administrador apropiados, puede crear la base de datos de archivado (LcsLog) al publicar la topología.</span><span class="sxs-lookup"><span data-stu-id="1cace-142">If the account to be used to publish the topology has the appropriate administrator rights and permissions, you can create the Archiving database (LcsLog) when you publish your topology.</span></span> <span data-ttu-id="1cace-143">También puede crear la base de datos más adelante, incluyendo como parte del procedimiento de instalación.</span><span class="sxs-lookup"><span data-stu-id="1cace-143">You can also create the database later, including as part of the installation procedure.</span></span> <span data-ttu-id="1cace-144">Para obtener más información sobre SQL Server, consulte SQL Server TechCenter en [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045) .</span><span class="sxs-lookup"><span data-stu-id="1cace-144">For details about SQL Server, see the SQL Server TechCenter at [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045).</span></span>

<span data-ttu-id="1cace-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1cace-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

