---
title: 'Lync Server 2013: administración de la configuración'
description: 'Lync Server 2013: administración de la configuración.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration management
ms:assetid: 00ea1196-cb40-427f-99a4-5e8037cbf367
ms:mtpsurl: https://technet.microsoft.com/library/Dn720316(v=OCS.15)
ms:contentKeyID: 63969570
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5999708811cc4a34cf846a1ddd481ba38e07c62
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434252"
---
# <a name="configuration-management-in-lync-server-2013"></a><span data-ttu-id="06358-103">Administración de la configuración en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06358-103">Configuration management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06358-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06358-104">

<span> </span></span></span>

<span data-ttu-id="06358-105">_**Última modificación del tema:** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="06358-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="06358-106">La administración de la configuración es el proceso de grabación y seguimiento de los activos de hardware y software y la información de configuración del sistema.</span><span class="sxs-lookup"><span data-stu-id="06358-106">Configuration management is the process of recording and tracking hardware and software assets and system configuration information.</span></span> <span data-ttu-id="06358-107">Generalmente, se usa para realizar un seguimiento de las licencias de software, mantener una compilación estándar de hardware y software para equipos y servidores cliente, y definir los estándares de nomenclatura para equipos nuevos.</span><span class="sxs-lookup"><span data-stu-id="06358-107">It is generally used to track software licenses, maintain a standard hardware and software build for client computers and servers, and define naming standards for new computers.</span></span> <span data-ttu-id="06358-108">La administración de la configuración generalmente cubre las siguientes categorías:</span><span class="sxs-lookup"><span data-stu-id="06358-108">Configuration management generally covers the following categories:</span></span>

  - <span data-ttu-id="06358-109">**Hardware**   Esta categoría realiza un seguimiento de los elementos de los equipos de los que es propietario la organización de ti, dónde se encuentra el equipo y quién usa el equipo.</span><span class="sxs-lookup"><span data-stu-id="06358-109">**Hardware**   This category tracks the pieces of equipment that the IT organization owns, where equipment is located, and who uses equipment.</span></span> <span data-ttu-id="06358-110">Esta información permite a una organización planificar y presupuestar actualizaciones, mantener compilaciones de hardware estándar, informar sobre el valor de los activos de TI con fines de contabilidad y ayudar a evitar robos.</span><span class="sxs-lookup"><span data-stu-id="06358-110">This information enables an organization to plan and budget for upgrades, maintain standard hardware builds, report on the value of IT assets for accounting purposes, and help prevent theft.</span></span>

  - <span data-ttu-id="06358-111">**Software**   Esta categoría realiza un seguimiento del software que está instalado en cada equipo, los números de versión y dónde se encuentran las licencias.</span><span class="sxs-lookup"><span data-stu-id="06358-111">**Software**   This category tracks software that is installed on each computer, the version numbers, and where the licenses are held.</span></span> <span data-ttu-id="06358-112">Esta información ayuda a planificar las actualizaciones, garantizar la licencia del software y detectar la presencia de software no autorizado (y sin licencia).</span><span class="sxs-lookup"><span data-stu-id="06358-112">This information helps plan upgrades, to ensure that software is licensed, and detect the presence of unauthorized (and unlicensed) software.</span></span>

  - <span data-ttu-id="06358-113">**Compilaciones estándar**   Esta categoría realiza un seguimiento de la compilación estándar actual para los equipos y servidores cliente y si los equipos cliente y los servidores cumplen este estándar.</span><span class="sxs-lookup"><span data-stu-id="06358-113">**Standard Builds**   This category tracks the current standard build for the client computers and servers and whether the client computers and servers meet this standard.</span></span> <span data-ttu-id="06358-114">Definir e imponer compilaciones estándar ayuda al personal de soporte técnico porque el personal debe mantener un número limitado de versiones de cada elemento de software.</span><span class="sxs-lookup"><span data-stu-id="06358-114">Defining and enforcing standard builds helps support staff because the staff is required to maintain only a limited number of versions of each piece of software.</span></span>

  - <span data-ttu-id="06358-115">**Actualizaciones y revisiones acumulativas**   Esta categoría hace un seguimiento de los Service Packs probados y aprobados para su uso y de los equipos que están actualizados.</span><span class="sxs-lookup"><span data-stu-id="06358-115">**Cumulative Updates and Hotfixes**   This category tracks which service packs are tested and approved for use and which computers are up to date.</span></span> <span data-ttu-id="06358-116">Esta información es importante para reducir el riesgo de que los equipos se vean comprometidos y detectar a los usuarios que han instalado actualizaciones no aprobadas.</span><span class="sxs-lookup"><span data-stu-id="06358-116">This information is important to reduce the risk of computers being compromised and to detect users who have installed unapproved updates.</span></span>

  - <span data-ttu-id="06358-117">**Información de configuración del sistema**   Esta categoría realiza un seguimiento de la función de un sistema, la interacción entre los elementos del sistema y los procesos que dependen de un sistema que se ejecuta sin problemas.</span><span class="sxs-lookup"><span data-stu-id="06358-117">**System Configuration Information**   This category tracks the function of a system, the interaction between system elements, and the processes that depend on a system that is running smoothly.</span></span> <span data-ttu-id="06358-118">Por ejemplo, se puede configurar un servidor proxy de terceros en un solo servidor.</span><span class="sxs-lookup"><span data-stu-id="06358-118">For example, third-party proxy server may be configured on a single server.</span></span> <span data-ttu-id="06358-119">Es posible que se entienda la dependencia del servidor proxy en este servidor y que se requieran planes de contingencia si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="06358-119">The proxy server’s dependence on this server should be understood and contingency plans may be required if there is a failure.</span></span> <span data-ttu-id="06358-120">Si el servidor proxy se puede configurar para que también se comunique con otro servidor front-end, las dependencias y los planes de contingencia probablemente cambiarán.</span><span class="sxs-lookup"><span data-stu-id="06358-120">If the proxy server can be configured to also communicate with another front-end server, dependencies and contingency plans will probably change.</span></span>

<div>

## <a name="implementing-configuration-management"></a><span data-ttu-id="06358-121">Implementación de la administración de configuración</span><span class="sxs-lookup"><span data-stu-id="06358-121">Implementing configuration management</span></span>

<span data-ttu-id="06358-122">Después de determinar qué elementos necesitan administrar, implementar la administración de la configuración mediante la recopilación de datos e informes de datos.</span><span class="sxs-lookup"><span data-stu-id="06358-122">After you determine what items need managing, implement configuration management by collecting data and reporting data.</span></span> <span data-ttu-id="06358-123">El método más sencillo para las organizaciones pequeñas es recopilar datos manualmente (número y modelo de equipos cliente, sistema operativo, software instalado) y guardarlos en un documento de Office Word u Office Excel.</span><span class="sxs-lookup"><span data-stu-id="06358-123">The simplest approach for small organizations is to collect data manually (number and model of client computers, operating system, installed software) and save it in an Office Word or Office Excel document.</span></span> <span data-ttu-id="06358-124">Para sistemas de mayor tamaño, complejidad y cambio constante, debe automatizarse el descubrimiento de activos y la recopilación de información detallada.</span><span class="sxs-lookup"><span data-stu-id="06358-124">For larger, more complex, and constantly changing systems, the discovery of assets and collection of detailed information must be automated.</span></span> <span data-ttu-id="06358-125">Decida qué información es relevante para su organización y guárdela en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="06358-125">Decide what information is relevant to your organization and record it in a database.</span></span>

<span data-ttu-id="06358-126">La base de datos de administración de la configuración es una herramienta útil para el personal de soporte técnico y la administración en las siguientes áreas:</span><span class="sxs-lookup"><span data-stu-id="06358-126">The configuration management database is a useful tool for support staff and management in the following areas:</span></span>

  - <span data-ttu-id="06358-127">**Auditorías de seguridad**   La base de datos le permite identificar los servidores que ejecutan Lync Server y los sistemas de equipos cliente que deben tener correcciones aplicadas o que han perdido la instalación de un Service Pack o las últimas actualizaciones de antivirus.</span><span class="sxs-lookup"><span data-stu-id="06358-127">**Security Audits**   The database enables you to identify servers that are running Lync Server and client computer systems that must have hotfixes applied or that have missed the installation of a service pack or the latest antivirus updates.</span></span>

  - <span data-ttu-id="06358-128">**Instalación de software**   Identificar las versiones de software de cliente y realizar un seguimiento de ellas ayudará a los administradores a planear las actualizaciones de versión y las nuevas instalaciones, además de ayudarle con la documentación de licencias y el cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="06358-128">**Software Installation**   Identifying client software versions and tracking them will aid administrators in planning version updates and new installs and also by helping with licensing documentation and compliance.</span></span>

  - <span data-ttu-id="06358-129">**Información de configuración**   Si mantiene una lista actualizada de todos los valores de configuración que se cambiaron de forma predeterminada, podrá solucionar problemas de forma rápida y eficaz.</span><span class="sxs-lookup"><span data-stu-id="06358-129">**Configuration Information**   If you maintain an up-to-date list of all settings that were changed from their default, then you'll be able to troubleshoot issues quickly and more effectively.</span></span>

  - <span data-ttu-id="06358-130">**Actualizaciones de planeación**   Si una revisión de capacidad revela que es necesario disponer de espacio de almacenamiento adicional en sus servidores de base de datos de Lync, es importante saber si cada servidor tiene un controlador RAID interno.</span><span class="sxs-lookup"><span data-stu-id="06358-130">**Planning Upgrades**   If a capacity review reveals that additional storage space is required on your Lync database servers, it’s important to know whether each server has an internal RAID controller.</span></span> <span data-ttu-id="06358-131">Si lo hacen, ¿son el mismo modelo?</span><span class="sxs-lookup"><span data-stu-id="06358-131">If they do, then are they the same model?</span></span> <span data-ttu-id="06358-132">¿Tienen el mismo número de discos instalados?</span><span class="sxs-lookup"><span data-stu-id="06358-132">Do they have the same number of disks installed?</span></span> <span data-ttu-id="06358-133">La base de datos de administración de la configuración indicará el tipo de disco que se puede instalar, el número y la ruta de actualización en cada caso.</span><span class="sxs-lookup"><span data-stu-id="06358-133">The configuration management database will indicate the type of disk that can be installed, the number, and the upgrade path in each case.</span></span>

</div>

<div>

## <a name="tools-used-for-configuration-management"></a><span data-ttu-id="06358-134">Herramientas usadas para la administración de la configuración</span><span class="sxs-lookup"><span data-stu-id="06358-134">Tools used for configuration management</span></span>

<span data-ttu-id="06358-135">Existen muchas herramientas para descubrir, auditar y denunciar activos.</span><span class="sxs-lookup"><span data-stu-id="06358-135">There are many tools to discover, audit, and report assets.</span></span> <span data-ttu-id="06358-136">Algunas de estas herramientas se describen en esta sección.</span><span class="sxs-lookup"><span data-stu-id="06358-136">Some of these tools are discussed in this section.</span></span>

  - <span data-ttu-id="06358-137">**Scripts automáticos**   Puede escribir secuencias de comandos sencillas para notificar elementos como el sistema operativo, el nivel de Service Pack y si el software existe en un conjunto específico de equipos.</span><span class="sxs-lookup"><span data-stu-id="06358-137">**Automated Scripts**   You can write simple scripts to report items such as the operating system, service pack level, and whether software exists on a specific set of computers.</span></span> <span data-ttu-id="06358-138">Puede escribir estos scripts en los requisitos exactos de una organización.</span><span class="sxs-lookup"><span data-stu-id="06358-138">You can write these scripts to an organization’s exact requirements.</span></span> <span data-ttu-id="06358-139">Sin embargo, el número necesario de scripts y su complejidad pueden crear y mantener los scripts de forma costosa.</span><span class="sxs-lookup"><span data-stu-id="06358-139">However, the required number of scripts and their complexity can make scripts expensive to create and maintain.</span></span>

  - <span data-ttu-id="06358-140">**Herramientas automatizadas**   Según el tamaño de su empresa y las necesidades de su organización, es posible que desee considerar el uso de herramientas automatizadas.</span><span class="sxs-lookup"><span data-stu-id="06358-140">**Automated Tools**   Depending on the size of your business and your organizational needs, you may want to consider using automated tools.</span></span> <span data-ttu-id="06358-141">Herramientas como Microsoft Endpoint Configuration Manager incorporan plantillas de informe estándar (como el nivel de Service Pack) y también le permiten crear informes personalizados, por ejemplo, para una aplicación personalizada.</span><span class="sxs-lookup"><span data-stu-id="06358-141">Tools such as Microsoft Endpoint Configuration Manager incorporate standard report templates (such as service pack level) and also enable you to create customized reports, for example, for a custom application.</span></span> <span data-ttu-id="06358-142">El administrador de configuración de Microsoft Endpoint también se puede usar para informar sobre configuraciones de hardware y software.</span><span class="sxs-lookup"><span data-stu-id="06358-142">The Microsoft Endpoint Configuration Manager can also be used to report on hardware and software configurations.</span></span>

</div>

<div>

## <a name="relationship-with-change-management"></a><span data-ttu-id="06358-143">Relación con la administración de cambios</span><span class="sxs-lookup"><span data-stu-id="06358-143">Relationship with change management</span></span>

<span data-ttu-id="06358-144">La administración de la configuración está estrechamente relacionada con la administración de cambios.</span><span class="sxs-lookup"><span data-stu-id="06358-144">Configuration management is closely related to change management.</span></span> <span data-ttu-id="06358-145">La administración de la configuración identifica la necesidad de cambiar e identifica y registra que se ha producido un cambio.</span><span class="sxs-lookup"><span data-stu-id="06358-145">Configuration management identifies the need for change and identifies and records that a change has occurred.</span></span> <span data-ttu-id="06358-146">Por ejemplo, la base de datos de administración de la configuración se puede usar para identificar los servidores que requieren una revisión.</span><span class="sxs-lookup"><span data-stu-id="06358-146">For example, the configuration management database can be used to identify servers that require a hotfix.</span></span> <span data-ttu-id="06358-147">Después, la administración de cambios define el proceso de aplicación de la revisión.</span><span class="sxs-lookup"><span data-stu-id="06358-147">Change management then defines the process for applying the hotfix.</span></span>

<span data-ttu-id="06358-148">Por el contrario, si se ha implementado una nueva actualización acumulativa, el proceso de administración de cambios debe suministrar esta información al sistema de administración de la configuración.</span><span class="sxs-lookup"><span data-stu-id="06358-148">Conversely, if a new cumulative update is rolled out, the change management process should supply this information to the configuration management system.</span></span> <span data-ttu-id="06358-149">Es probable que tenga que configurar las herramientas de administración de la configuración para identificar el nuevo software de modo que puedan descubrir y realizar un seguimiento de dónde y cuándo se implementa el software.</span><span class="sxs-lookup"><span data-stu-id="06358-149">The configuration management tools will probably need to be configured to identify the new software so that they can discover and track where and when the software is deployed.</span></span>

<span data-ttu-id="06358-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06358-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

