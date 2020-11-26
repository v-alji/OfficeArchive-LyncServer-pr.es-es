---
title: 'Lync Server 2013: Definición y configuración de la topología'
description: 'Lync Server 2013: definir y configurar la topología.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining and configuring the topology
ms:assetid: 51d1601e-4f83-48d4-ad08-3b4d5e2003aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398339(v=OCS.15)
ms:contentKeyID: 48184146
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec444a1ddf434c5a80fdc2d56bdba27573da14ab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431004"
---
# <a name="defining-and-configuring-the-topology-in-lync-server-2013"></a><span data-ttu-id="60df5-103">Definición y configuración de la topología en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60df5-103">Defining and configuring the topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="60df5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="60df5-104">

<span> </span></span></span>

<span data-ttu-id="60df5-105">_**Última modificación del tema:** 2012-09-14_</span><span class="sxs-lookup"><span data-stu-id="60df5-105">_**Topic Last Modified:** 2012-09-14_</span></span>

<span data-ttu-id="60df5-106">Defina y configure su topología con el generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="60df5-106">You define and configure your topology by using Topology Builder.</span></span> <span data-ttu-id="60df5-107">El generador de topología no requiere que usted sea miembro del grupo de administradores locales o de un grupo de dominios privilegiado (como administradores de dominio).</span><span class="sxs-lookup"><span data-stu-id="60df5-107">Topology Builder does not require you to be a member of the local Administrators group or a privileged domain group (such as Domain Admins).</span></span> <span data-ttu-id="60df5-108">Puede definir su topología como usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="60df5-108">You can define your topology as a standard user.</span></span> <span data-ttu-id="60df5-109">Al iniciar el generador de topología en el primer uso y en sesiones de edición posteriores, se le pedirá la ubicación en la que desea que el generador de topología cargue el documento de configuración actual.</span><span class="sxs-lookup"><span data-stu-id="60df5-109">When you start Topology Builder on first use and subsequent edit sessions, you are prompted for the location where you want Topology Builder to load the current configuration document.</span></span> <span data-ttu-id="60df5-110">Las opciones son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="60df5-110">The choices are the following:</span></span>

  - <span data-ttu-id="60df5-111">Descargar una topología desde una implementación existente</span><span class="sxs-lookup"><span data-stu-id="60df5-111">Download topology from existing deployment</span></span>

  - <span data-ttu-id="60df5-112">Abrir topología desde un archivo local</span><span class="sxs-lookup"><span data-stu-id="60df5-112">Open topology from a local file</span></span>

  - <span data-ttu-id="60df5-113">Nueva topología</span><span class="sxs-lookup"><span data-stu-id="60df5-113">New topology</span></span>

<span data-ttu-id="60df5-114">Si ya ha definido una topología y ha establecido el almacén de administración central, debe elegir descargar una topología de una implementación existente.</span><span class="sxs-lookup"><span data-stu-id="60df5-114">If you have already defined a topology and have established the Central Management store, you should choose to download a topology from an existing deployment.</span></span> <span data-ttu-id="60df5-115">El generador de topología leerá la base de datos y recuperará la definición actual.</span><span class="sxs-lookup"><span data-stu-id="60df5-115">Topology Builder will read the database and retrieve the current definition.</span></span> <span data-ttu-id="60df5-116">Si ya tiene un almacén de administración central, siempre debe elegir esta opción.</span><span class="sxs-lookup"><span data-stu-id="60df5-116">If you have an existing Central Management store, you should always choose this option.</span></span>

<span data-ttu-id="60df5-117">Si no ha establecido un almacén de administración central y desea editar una configuración guardada anteriormente, debe optar por abrir la topología desde un archivo local.</span><span class="sxs-lookup"><span data-stu-id="60df5-117">If you have not established a Central Management store and want to edit a previously saved configuration, you should choose to open the topology from a local file.</span></span> <span data-ttu-id="60df5-118">El archivo que se abrirá sería el archivo de configuración que se guardó en una sesión anterior.</span><span class="sxs-lookup"><span data-stu-id="60df5-118">The file that you will open would be the configuration file that was saved in a previous session.</span></span> <span data-ttu-id="60df5-119">Puede usar esta opción para editar la topología guardada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="60df5-119">You can use this option to edit the previously saved topology.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="60df5-120">Si ya tiene una topología publicada, no debe cargar un archivo de configuración local.</span><span class="sxs-lookup"><span data-stu-id="60df5-120">If you already have a published topology, you should not load a local configuration file.</span></span> <span data-ttu-id="60df5-121">Debe elegir descargar la topología de una implementación existente.</span><span class="sxs-lookup"><span data-stu-id="60df5-121">You should choose to download the topology from an existing deployment.</span></span>



</div>

<span data-ttu-id="60df5-122">Elija esta opción para crear una nueva topología, si desea crear una configuración de topología nueva.</span><span class="sxs-lookup"><span data-stu-id="60df5-122">Choose to create a new topology, if you want to create a new Topology Builder configuration.</span></span> <span data-ttu-id="60df5-123">Un diseño guardado anteriormente no se sobrescribe a menos que decida guardarlo como el mismo archivo que ha creado en una sesión de diseño anterior.</span><span class="sxs-lookup"><span data-stu-id="60df5-123">A previously saved design is not overwritten unless you choose to save it as the same file that you created in an earlier design session.</span></span>

<span data-ttu-id="60df5-124">En cada una de estas opciones, se le pedirá una ubicación para almacenar el archivo de configuración de Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="60df5-124">In each of these options, you will be prompted for a location to store the Topology Builder configuration file.</span></span> <span data-ttu-id="60df5-125">La ubicación del archivo puede ser una ubicación local, una ubicación compartida en un recurso compartido de archivos o un medio extraíble.</span><span class="sxs-lookup"><span data-stu-id="60df5-125">The location for the file could be a local location, a shared location on an established file share, or removable media.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="60df5-126">En esta sección</span><span class="sxs-lookup"><span data-stu-id="60df5-126">In This Section</span></span>

  - [<span data-ttu-id="60df5-127">Definir y configurar una topología en Topology Builder para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60df5-127">Define and configure a topology in Topology Builder for Lync Server 2013</span></span>](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md)

  - [<span data-ttu-id="60df5-128">Definir y configurar un grupo de servidores front-end o un servidor Standard Edition en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60df5-128">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</span></span>](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md)

  - [<span data-ttu-id="60df5-129">Implementación de grupos front-end emparejados para recuperación ante desastres en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60df5-129">Deploying paired Front End pools for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-deploying-paired-front-end-pools-for-disaster-recovery.md)

  - [<span data-ttu-id="60df5-130">Implementar un reflejo de SQL para alta disponibilidad de servidores back-end en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60df5-130">Deploying SQL mirroring for Back End Server high availability in Lync Server 2013</span></span>](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)

  - [<span data-ttu-id="60df5-131">Editar o configurar direcciones URL sencillas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60df5-131">Edit or configure simple URLs in Lync Server 2013</span></span>](lync-server-2013-edit-or-configure-simple-urls.md)

  - [<span data-ttu-id="60df5-132">Seleccionar el servidor de administración central en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60df5-132">Select the Central Management Server in Lync Server 2013</span></span>](lync-server-2013-select-the-central-management-server.md)

<span data-ttu-id="60df5-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="60df5-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

