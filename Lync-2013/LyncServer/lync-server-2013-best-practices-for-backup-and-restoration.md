---
title: 'Lync Server 2013: procedimientos recomendados para copias de seguridad y restauración'
description: 'Lync Server 2013: procedimientos recomendados para la copia de seguridad y la restauración.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for backup and restoration
ms:assetid: abbce0e4-973a-4624-a0c1-e0f22e1d348b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202184(v=OCS.15)
ms:contentKeyID: 51541500
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3e8875f03a7b4445af8274ef059f3abad4d21ff8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437892"
---
# <a name="best-practices-for-backup-and-restoration-for-lync-server-2013"></a><span data-ttu-id="16a7a-103">Procedimientos recomendados para copias de seguridad y restauración de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="16a7a-103">Best practices for backup and restoration for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16a7a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16a7a-104">

<span> </span></span></span>

<span data-ttu-id="16a7a-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="16a7a-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="16a7a-106">Esta sección incluye dos tipos de procedimientos recomendados:</span><span class="sxs-lookup"><span data-stu-id="16a7a-106">This section includes two types of best practices:</span></span>

  - <span data-ttu-id="16a7a-107">Procedimientos recomendados para la copia de seguridad y la restauración.</span><span class="sxs-lookup"><span data-stu-id="16a7a-107">Best practices for backup and restoration.</span></span>

  - <span data-ttu-id="16a7a-108">Procedimientos recomendados para minimizar el impacto de un desastre.</span><span class="sxs-lookup"><span data-stu-id="16a7a-108">Best practices for minimizing the impact of a disaster.</span></span>

<div>

## <a name="best-practices-for-backup-and-restoration"></a><span data-ttu-id="16a7a-109">Procedimientos recomendados para copias de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="16a7a-109">Best Practices for Backup and Restoration</span></span>

<span data-ttu-id="16a7a-110">Para facilitar el proceso de copia de seguridad y restauración, al hacer una copia de seguridad o restaurar los datos, siga estos procedimientos recomendados:</span><span class="sxs-lookup"><span data-stu-id="16a7a-110">To facilitate your backup and restoration process, apply the following best practices when you back up or restore your data:</span></span>

  - <span data-ttu-id="16a7a-111">Realice copias de seguridad periódicas en intervalos apropiados.</span><span class="sxs-lookup"><span data-stu-id="16a7a-111">Perform regular backups at appropriate intervals.</span></span> <span data-ttu-id="16a7a-112">La programación de rotación y el tipo de copia de seguridad más simple y frecuente es una copia de seguridad nocturna completa de toda la base de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="16a7a-112">The simplest and most commonly used backup type and rotation schedule is a full, nightly backup of the entire SQL Server database.</span></span> <span data-ttu-id="16a7a-113">Después, si es necesario restaurar, el proceso de restauración solo requiere una copia de seguridad, y no se deben perder más de un día.</span><span class="sxs-lookup"><span data-stu-id="16a7a-113">Then, if restoration is necessary, the restoration process requires only one backup, and no more than a day’s data should be lost.</span></span>

  - <span data-ttu-id="16a7a-114">Si usa cmdlets o el panel de control de Lync Server para realizar cambios de configuración, use el cmdlet **Export-CsConfiguration** para tomar una copia de seguridad de instantáneas del archivo de configuración de topología (XDS. MDF) después de realizar los cambios, de modo que no pierda los cambios si necesita restaurar las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="16a7a-114">If you use cmdlets or the Lync Server Control Panel to make configuration changes, use the **Export-CsConfiguration** cmdlet to take a snapshot backup of the topology configuration file (Xds.mdf) after you make the changes, so that you won't lose the changes if you need to restore your databases.</span></span> <span data-ttu-id="16a7a-115">Tenga en cuenta que se realiza una copia de seguridad de esta configuración en formato XML y se comprime como archivo ZIP.</span><span class="sxs-lookup"><span data-stu-id="16a7a-115">Note that this configuration is backed up in XML format and compressed as a ZIP file.</span></span>

  - <span data-ttu-id="16a7a-116">Asegúrese de que la carpeta compartida que va a usar para realizar copias de seguridad de Lync Server tenga suficiente espacio en disco para almacenar todos los datos de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="16a7a-116">Make sure that the shared folder you plan to use for backing up Lync Server has sufficient disk space to hold all the backed up data.</span></span>

  - <span data-ttu-id="16a7a-117">Programe copias de seguridad cuando el uso de Lync Server sea generalmente bajo, para mejorar el rendimiento del servidor y la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="16a7a-117">Schedule backups when Lync Server usage is typically low, to improve server performance and user experience.</span></span>

  - <span data-ttu-id="16a7a-118">Asegúrese de que la ubicación donde se realiza la copia de seguridad de los datos es segura (recomendamos una ubicación remota).</span><span class="sxs-lookup"><span data-stu-id="16a7a-118">Make sure that the location where you back up data is secure (we recommend a remote location).</span></span>

  - <span data-ttu-id="16a7a-119">Mantenga los archivos de copia de seguridad donde estarán disponibles, en caso de que necesite restaurar los datos.</span><span class="sxs-lookup"><span data-stu-id="16a7a-119">Keep the backup files where they will be available, in case you need to restore the data.</span></span>

  - <span data-ttu-id="16a7a-120">Planear y programar pruebas periódicas de los procesos de restauración admitidos por su organización.</span><span class="sxs-lookup"><span data-stu-id="16a7a-120">Plan for and schedule periodic testing of the restoration processes that are supported by your organization.</span></span>

  - <span data-ttu-id="16a7a-121">Valide los procesos de copia de seguridad y restauración por adelantado para asegurarse de que funcionan de la forma esperada.</span><span class="sxs-lookup"><span data-stu-id="16a7a-121">Validate your backup and restoration processes in advance to make sure that they work as expected.</span></span>

</div>

<div>

## <a name="best-practices-for-minimizing-the-impact-of-a-disaster"></a><span data-ttu-id="16a7a-122">Procedimientos recomendados para minimizar el impacto de un desastre</span><span class="sxs-lookup"><span data-stu-id="16a7a-122">Best Practices for Minimizing the Impact of a Disaster</span></span>

<span data-ttu-id="16a7a-123">La mejor estrategia para resolver interrupciones de servicio desastrosas (causadas por eventos no manejables, como cortes de energía o errores de hardware repentinos) es asumir que ocurrirán y planificar según corresponda.</span><span class="sxs-lookup"><span data-stu-id="16a7a-123">The best strategy for dealing with disastrous service interruptions (caused by unmanageable events such as power outages or sudden hardware failures) is to assume they will happen, and to plan accordingly.</span></span>

<span data-ttu-id="16a7a-124">Si los servicios de Lync, con un mínimo de interrupción y interrupción, son importantes para la empresa, debe considerar la posibilidad de implementar grupos de servidores de solicitudes de cliente emparejados, como se describe en [planear la alta disponibilidad y la recuperación ante desastres en Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="16a7a-124">If Lync services, with a minimum of disruption and outage, are business-critical for your organization, you should consider implementing paired pools of Front End Servers, as described in [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span> <span data-ttu-id="16a7a-125">Después, si uno de estos grupos de servidores tiene un desastre, un administrador puede cambiar los usuarios de ese grupo para que el otro grupo lo atienda, con un mínimo de tiempo de inactividad.</span><span class="sxs-lookup"><span data-stu-id="16a7a-125">Then, if one of these pools has a disaster, an administrator can switch the users of that pool to be served by the other pool, with a minimum of downtime.</span></span>

<span data-ttu-id="16a7a-126">Los planes de administración ante desastres que desarrolla como parte de su estrategia de copia de seguridad y restauración deben incluir lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="16a7a-126">The disaster management plans that you develop as part of your backup and restoration strategy should include the following:</span></span>

  - <span data-ttu-id="16a7a-127">Cómo mantener los medios de software y las actualizaciones de software y firmware disponibles.</span><span class="sxs-lookup"><span data-stu-id="16a7a-127">Keeping your software media, and your software and firmware updates, readily available.</span></span>

  - <span data-ttu-id="16a7a-128">Mantener registros de hardware y software.</span><span class="sxs-lookup"><span data-stu-id="16a7a-128">Maintaining hardware and software records.</span></span>

  - <span data-ttu-id="16a7a-129">Realizar copias de seguridad de los datos de forma periódica y supervisar la integridad de las copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="16a7a-129">Backing up your data regularly and monitoring the integrity of your backups.</span></span>

  - <span data-ttu-id="16a7a-130">Formación de su personal en la recuperación de desastres, documentación de procedimientos e implementación de simulacros de recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="16a7a-130">Training your staff in disaster recovery, documenting procedures, and implementing disaster recovery simulation drills.</span></span>

  - <span data-ttu-id="16a7a-131">Mantener disponible el hardware de repuesto o, si tiene un contrato de nivel de servicio (SLA), contratar a proveedores de hardware y proveedores para el reemplazo de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="16a7a-131">Keeping spare hardware available, or, if you have a service level agreement (SLA), contracting with hardware vendors and suppliers for prompt replacements.</span></span>

  - <span data-ttu-id="16a7a-132">Separar la ubicación de los archivos de registro de transacciones (archivos. ldf) y los archivos de base de datos (archivos. MDF).</span><span class="sxs-lookup"><span data-stu-id="16a7a-132">Separating the location of your transaction log files (.ldf files) and database files (.mdf files).</span></span>

<span data-ttu-id="16a7a-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16a7a-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

