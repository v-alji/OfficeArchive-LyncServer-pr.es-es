---
title: 'Lync Server 2013: Preparación de la infraestructura y los sistemas'
description: 'Lync Server 2013: preparación de la infraestructura y los sistemas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the infrastructure and systems
ms:assetid: 1254ee38-0679-4714-b293-1050f107c158
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398205(v=OCS.15)
ms:contentKeyID: 48183458
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bfabdda9d117af1534578c8543f9ce72808d5a53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424103"
---
# <a name="preparing-the-infrastructure-and-systems-for-lync-server-2013"></a><span data-ttu-id="39518-103">Preparación de la infraestructura y los sistemas para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39518-103">Preparing the infrastructure and systems for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39518-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39518-104">

<span> </span></span></span>

<span data-ttu-id="39518-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="39518-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="39518-106">La implementación de Lync Server 2013 requiere el uso de Topology Builder para definir y publicar el diseño de la topología.</span><span class="sxs-lookup"><span data-stu-id="39518-106">Deployment of Lync Server 2013 requires the use of Topology Builder to define and publish the topology design.</span></span> <span data-ttu-id="39518-107">Para identificar los componentes necesarios para su topología, use el generador de topología para crear y guardar un diseño de topología.</span><span class="sxs-lookup"><span data-stu-id="39518-107">To identify the components required for your topology, you use Topology Builder to create and save a topology design.</span></span> <span data-ttu-id="39518-108">Antes de publicar su topología en el generador de topología, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="39518-108">Prior to publishing your topology in Topology Builder, you do the following:</span></span>

  - <span data-ttu-id="39518-109">Adquiera e instale el hardware de cada componente en el diseño de topología que haya creado y guardado con el generador de topología, incluidos los equipos (servidores que ejecutan Lync Server 2013, servidores de bases de datos, servidores de Internet Information Services (IIS) y los servidores proxy inversos, según corresponda), adaptadores de red, equilibradores de carga de hardware y dispositivos de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="39518-109">Acquire and install the hardware for each component in the topology design that you created and saved by using Topology Builder, including all required computers (servers running Lync Server 2013, database servers, servers running Internet Information Services (IIS), and reverse proxy servers, as appropriate), network adapters, hardware load balancers, and storage devices (such as file servers).</span></span> <span data-ttu-id="39518-110">Para obtener más información sobre cómo definir una topología que especifique los componentes necesarios para su implementación, consulte [definir y configurar la topología en Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="39518-110">For details about how to define a topology that specifies the components needed for your deployment, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span> <span data-ttu-id="39518-111">Para obtener más información sobre los requisitos de hardware para servidores, consulte [hardware compatible para Lync Server 2013](lync-server-2013-supported-hardware.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="39518-111">For details about hardware requirements for servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="39518-112">Asegúrese de que la infraestructura de red cumpla con los requisitos.</span><span class="sxs-lookup"><span data-stu-id="39518-112">Make sure that the networking infrastructure meets requirements.</span></span> <span data-ttu-id="39518-113">Para obtener más información, consulte [requisitos de infraestructura de red para Lync Server 2013](lync-server-2013-network-infrastructure-requirements.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="39518-113">For details, see [Network infrastructure requirements for Lync Server 2013](lync-server-2013-network-infrastructure-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="39518-114">Configurar los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="39518-114">Set up Active Directory Domain Services.</span></span> <span data-ttu-id="39518-115">Para publicar y habilitar la topología, necesita que los servidores internos estén representados por cuentas de equipos en AD DS.</span><span class="sxs-lookup"><span data-stu-id="39518-115">To publish and enable the topology, you need the internal servers to be represented by computer accounts in AD DS.</span></span> <span data-ttu-id="39518-116">Esto se logra al unir los equipos a AD DS.</span><span class="sxs-lookup"><span data-stu-id="39518-116">This is accomplished by joining the computers to AD DS.</span></span> <span data-ttu-id="39518-117">Para obtener detalles sobre la preparación de AD DS, consulte [preparar los servicios de dominio de Active Directory para Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="39518-117">For details about preparing AD DS, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span></span>

  - <span data-ttu-id="39518-118">Crear un recurso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="39518-118">Create a file share.</span></span> <span data-ttu-id="39518-119">Los servidores Standard Edition pueden hospedar el recurso compartido de archivos para el archivo requerido, mientras que en una implementación empresarial el recurso compartido de archivos no se puede hospedar en el servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="39518-119">Standard Edition servers can host the file share for the required file, while in an Enterprise deployment the file share cannot be hosted on the front end server.</span></span> <span data-ttu-id="39518-120">Los permisos y pertenencias a grupos necesarios para implementar y establecer la lista de control de acceso (ACL) en la carpeta y el recurso compartido deben establecerse correctamente para que el generador de topología se complete correctamente.</span><span class="sxs-lookup"><span data-stu-id="39518-120">The permissions and group memberships required for deploying and setting the access control list (ACL) on the folder and the share must be set correctly for Topology Builder to complete successfully.</span></span> <span data-ttu-id="39518-121">Debe asegurarse de que la persona que ejecuta el generador de topología tenga los siguientes permisos y pertenencias a grupos:</span><span class="sxs-lookup"><span data-stu-id="39518-121">You should make sure that the person running Topology Builder has the following permissions and group memberships:</span></span>
    
      - <span data-ttu-id="39518-122">Miembro de administradores locales</span><span class="sxs-lookup"><span data-stu-id="39518-122">Member of Local Administrators</span></span>
    
      - <span data-ttu-id="39518-123">Miembro de usuarios del dominio</span><span class="sxs-lookup"><span data-stu-id="39518-123">Member of Domain Users</span></span>
    
      - <span data-ttu-id="39518-124">Control total sobre el recurso compartido y la carpeta del almacén de archivos</span><span class="sxs-lookup"><span data-stu-id="39518-124">Full Control on share and folder of file store</span></span>

  - <span data-ttu-id="39518-125">Para Enterprise Edition, instale y Configure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="39518-125">For Enterprise Edition, install and configure SQL Server.</span></span> <span data-ttu-id="39518-126">Para que el programa de instalación de SQL Server funcione correctamente, el servidor basado en SQL Server debe estar en línea y la persona que publica la topología es un administrador local en SQL Server y debe ser miembro del grupo de administradores de SQL Server en la instancia de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="39518-126">For SQL Server setup to succeed the SQL Server-based server must be online and the person publishing the topology be a local admin on the SQL Server and must be a member of the SQL Server sysadmin group on the SQL Server instance.</span></span>

<span data-ttu-id="39518-127">Después de completar todas las tareas de preparación según se describe en este tema, pero antes de publicar la topología, también tendrá que realizar las otras tareas de preparación, entre las que se incluyen la instalación de los sistemas operativos de Windows y otros requisitos previos de software, la configuración de IIS y la configuración de DNS.</span><span class="sxs-lookup"><span data-stu-id="39518-127">After you complete all of the preparation tasks as described in this topic, but prior to publishing the topology, you also need to perform the other preparation tasks, including installing the Windows operating systems and other prerequisite software, setting up IIS, and configuring DNS.</span></span> <span data-ttu-id="39518-128">Para obtener más información sobre estas tareas, consulte [requisitos del sistema para servidores que ejecutan Lync server 2013](lync-server-2013-system-requirements-for-servers-running-lync-server-2013.md), [configurar IIS para Lync Server 2013](lync-server-2013-configure-iis.md)y [preparar la infraestructura y los sistemas para Lync Server 2013](lync-server-2013-preparing-the-infrastructure-and-systems.md).</span><span class="sxs-lookup"><span data-stu-id="39518-128">For details about these tasks, see [System requirements for servers running Lync Server 2013](lync-server-2013-system-requirements-for-servers-running-lync-server-2013.md), [Configure IIS for Lync Server 2013](lync-server-2013-configure-iis.md), and [Preparing the infrastructure and systems for Lync Server 2013](lync-server-2013-preparing-the-infrastructure-and-systems.md).</span></span> <span data-ttu-id="39518-129">Además, debe familiarizarse con los requisitos de clientes y clientes.</span><span class="sxs-lookup"><span data-stu-id="39518-129">Additionally, you should familiarize yourself with the clients and client requirements.</span></span> <span data-ttu-id="39518-130">Para obtener más información, consulte [implementación de clientes y dispositivos en Lync Server 2013](lync-server-2013-deploying-clients-and-devices.md).</span><span class="sxs-lookup"><span data-stu-id="39518-130">For details, see [Deploying clients and devices in Lync Server 2013](lync-server-2013-deploying-clients-and-devices.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="39518-131">En esta sección</span><span class="sxs-lookup"><span data-stu-id="39518-131">In This Section</span></span>

  - [<span data-ttu-id="39518-132">Configuración del hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39518-132">Hardware setup for Lync Server 2013</span></span>](lync-server-2013-hardware-setup.md)

  - [<span data-ttu-id="39518-133">Configuración del software para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39518-133">Software setup for Lync Server 2013</span></span>](lync-server-2013-software-setup.md)

  - [<span data-ttu-id="39518-134">Preparar Servicios de dominio de Active Directory en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39518-134">Preparing Active Directory Domain Services for Lync Server 2013</span></span>](lync-server-2013-preparing-active-directory-domain-services.md)

  - [<span data-ttu-id="39518-135">Configurar SQL Server para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39518-135">Configure SQL Server for Lync Server 2013</span></span>](lync-server-2013-configure-sql-server-for-lync-server.md)

  - [<span data-ttu-id="39518-136">Configurar los registros DNS para un grupo de servidores front-end o un servidor Standard Edition en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39518-136">Configure DNS records in Lync Server 2013 for a Front End pool or Standard Edition server</span></span>](lync-server-2013-configure-dns-records-for-a-front-end-pool-or-standard-edition-server.md)

  - [<span data-ttu-id="39518-137">Instalar las herramientas administrativas de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39518-137">Install Lync Server 2013 administrative tools</span></span>](lync-server-2013-install-lync-server-administrative-tools.md)

<span data-ttu-id="39518-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39518-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

