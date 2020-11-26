---
title: Instalar los sistemas operativos y el software necesario como requisito previo en los servidores
description: Instale los sistemas operativos y el software necesario en los servidores.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install operating systems and prerequisite software on servers
ms:assetid: 055991e0-5aeb-43fc-a7ba-d4b02316d73b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398103(v=OCS.15)
ms:contentKeyID: 48183288
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2bae9e57db9c2f1d3f3bde7ce9cc7071b73aa01d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427176"
---
# <a name="install-operating-systems-and-prerequisite-software-on-servers-for-lync-server-2013"></a><span data-ttu-id="91a55-103">Instalar los sistemas operativos y el software necesario como requisito previo en los servidores en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91a55-103">Install operating systems and prerequisite software on servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91a55-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91a55-104">

<span> </span></span></span>

<span data-ttu-id="91a55-105">_**Última modificación del tema:** 2014-07-24_</span><span class="sxs-lookup"><span data-stu-id="91a55-105">_**Topic Last Modified:** 2014-07-24_</span></span>

<span data-ttu-id="91a55-106">Una vez que haya configurado el hardware y la infraestructura del sistema, tendrá que instalar los sistemas operativos de Windows y las actualizaciones correspondientes, además de todos los demás programas de requisitos previos en cada servidor que vaya a implementar.</span><span class="sxs-lookup"><span data-stu-id="91a55-106">After you have set up the hardware and system infrastructure, you need to install the appropriate Windows operating systems and updates, in addition to all other prerequisite software on each server that you are deploying.</span></span> <span data-ttu-id="91a55-107">Esto incluye cada rol de servidor de Lync Server 2013 y todos los servidores de infraestructura adicionales o servidores que ejecuten SQL Server que sean necesarios para su implementación.</span><span class="sxs-lookup"><span data-stu-id="91a55-107">This includes each Lync Server 2013 server role and any additional infrastructure servers or servers running SQL Server that are required for your deployment.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="91a55-108">En esta sección se describe la instalación de sistemas operativos y el software necesario para servidores internos.</span><span class="sxs-lookup"><span data-stu-id="91a55-108">This section describes installation of operating systems and prerequisite software for internal servers.</span></span> <span data-ttu-id="91a55-109">Si implementa servidores perimetrales para admitir el acceso de usuarios externos, también tendrá que instalar sistemas operativos y el software necesario para esos servidores, incluidos los servidores perimetrales y los servidores proxy inversos.</span><span class="sxs-lookup"><span data-stu-id="91a55-109">If you are deploying Edge Servers to support external user access, you also need to install operating systems and prerequisite software for those servers, including Edge Servers and reverse proxy servers.</span></span> <span data-ttu-id="91a55-110">Para obtener más información sobre la preparación de servidores para admitir el acceso de usuarios externos, vea preparación de la <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">instalación de servidores en la red perimetral para Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="91a55-110">For details about preparing servers to support external user access, see <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">Preparing for installation of servers in the perimeter network for Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="install-windows-operating-systems-on-servers"></a><span data-ttu-id="91a55-111">Instalar sistemas operativos Windows en servidores</span><span class="sxs-lookup"><span data-stu-id="91a55-111">Install Windows Operating Systems on Servers</span></span>

<span data-ttu-id="91a55-112">En cada servidor que va a implementar, instale el sistema operativo Windows adecuado de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="91a55-112">On each server that you are deploying, install the appropriate Windows operating system as follows:</span></span>

  - <span data-ttu-id="91a55-113">**Servidores que ejecutan Lync Server 2013**   Para obtener más información sobre los requisitos del sistema operativo para servidores que ejecutan Lync Server 2013, consulte [compatibilidad del sistema operativo servidor y herramientas en Lync server 2013](lync-server-2013-server-and-tools-operating-system-support.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="91a55-113">**Servers running Lync Server 2013**   For details about the operating system requirements for servers running Lync Server 2013, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="91a55-114">**Servidores de bases de datos**   Para obtener más información sobre los requisitos del sistema operativo para servidores de base de datos, como la base de datos back-end, la base de datos de archivado y la base de datos de supervisión, consulte la documentación de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="91a55-114">**Database servers**   For details about operating system requirements for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server documentation.</span></span> <span data-ttu-id="91a55-115">Para SQL Server 2012, consulte los libros en línea de SQL Server 2012 en [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .</span><span class="sxs-lookup"><span data-stu-id="91a55-115">For SQL Server 2012, see the SQL Server 2012 Books Online at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="91a55-116">Si está instalando Lync Server 2013 en Windows Server &nbsp; 2008 &nbsp; R2 con SP1, primero debe instalar la actualización descrita en el artículo 2646886 de Microsoft Knowledge base, "Fix: el montón de daños se produce cuando un módulo llama al método INSERTENTITYBODY en IIS 7,5", en <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp ; kbid = 2646886</A>.</span><span class="sxs-lookup"><span data-stu-id="91a55-116">If you are installing Lync Server 2013 on Windows Server&nbsp;2008&nbsp;R2 with SP1, you must first install the update described in the Microsoft Knowledge Based article 2646886, “FIX: Heap corruption occurs when a module calls the InsertEntityBody method in IIS 7.5”, at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886">https://go.microsoft.com/fwlink/p/?linkid=3052&amp;kbid=2646886</A>.</span></span><BR><span data-ttu-id="91a55-117">También debe modificar el registro según se describe en el artículo de KB, los <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">identificadores de eventos 32402, 61045 se registran en los servidores front-end de Lync server 2013 que se instalan en Windows server 2012 R2</A>.</span><span class="sxs-lookup"><span data-stu-id="91a55-117">You must also modify the registry as described in the KB article, <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">Event IDs 32402, 61045 are logged in Lync Server 2013 Front End servers that are installed in Windows Server 2012 R2</A>.</span></span>



</div>

</div>

<div>

## <a name="install-windows-update-on-servers"></a><span data-ttu-id="91a55-118">Instalar Windows Update en servidores</span><span class="sxs-lookup"><span data-stu-id="91a55-118">Install Windows Update on Servers</span></span>

<span data-ttu-id="91a55-119">Instale las actualizaciones siguientes desde Windows Update en cada servidor:</span><span class="sxs-lookup"><span data-stu-id="91a55-119">Install the following updates from Windows Update on each server:</span></span>

  - <span data-ttu-id="91a55-120">**Windows Update para servidores que ejecutan Lync Server 2013**   Para obtener información sobre las actualizaciones de Windows Update necesarias para servidores que ejecutan Lync Server 2013, consulte [requisitos de software adicionales para Lync Server 2013](lync-server-2013-additional-software-requirements.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="91a55-120">**Windows Update for servers running Lync Server 2013**   For details about the updates from Windows Update that are required for servers running Lync Server 2013, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="91a55-121">**Servidores de bases de datos**   Para más información sobre las actualizaciones de Windows Update necesarias para servidores de bases de datos, como la base de datos back-end, la base de datos de archivado y la base de datos de supervisión, consulte la documentación 2012 de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="91a55-121">**Database servers**   For details about the updates from Windows Update that are required for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server 2012 documentation.</span></span> <span data-ttu-id="91a55-122">Para SQL Server 2012, consulte los libros en línea de SQL Server 2012 en [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .</span><span class="sxs-lookup"><span data-stu-id="91a55-122">For SQL Server 2012, see the SQL Server 2012 Books Online at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>

</div>

<div>

## <a name="install-other-prerequisite-software-on-servers"></a><span data-ttu-id="91a55-123">Instalar otro software necesario en los servidores</span><span class="sxs-lookup"><span data-stu-id="91a55-123">Install Other Prerequisite Software on Servers</span></span>

<span data-ttu-id="91a55-124">Lync Server 2013 requiere la instalación del siguiente software adicional en los servidores:</span><span class="sxs-lookup"><span data-stu-id="91a55-124">Lync Server 2013 requires the installation of the following additional software on servers:</span></span>

  - <span data-ttu-id="91a55-125">**Requisitos previos de software para servidores que ejecutan Lync Server 2013**   Los requisitos de software adicionales para servidores que ejecutan Lync Server 2013 dependen del rol de servidor que se implemente.</span><span class="sxs-lookup"><span data-stu-id="91a55-125">**Prerequisite software for servers running Lync Server 2013**   The additional software prerequisites for servers running Lync Server 2013 depend on the server role being deployed.</span></span> <span data-ttu-id="91a55-126">Para obtener más información sobre los requisitos de software específicos para cada servidor, consulte [requisitos de software adicionales para Lync server 2013](lync-server-2013-additional-software-requirements.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="91a55-126">For details about the specific software requirements for each server, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="91a55-127">**Windows Identity Foundation**   Lync Server 2013 requiere la instalación de Windows Identity Foundation para poder admitir los escenarios de autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="91a55-127">**Windows Identity Foundation**   Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server-to-server authentication scenarios.</span></span> <span data-ttu-id="91a55-128">Para comprobar que ya se ha instalado en el equipo, vaya a panel de control, haga clic en **programas y características**, **vea actualizaciones instaladas** y busque en **Microsoft Windows**.</span><span class="sxs-lookup"><span data-stu-id="91a55-128">To verify that it has already been installed on your computer, go to Control Panel, click **Programs and Features**, **View installed updates**, and look under **Microsoft Windows**.</span></span> <span data-ttu-id="91a55-129">Para obtener más información sobre cómo instalar Windows Identity Foundation, consulte [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .</span><span class="sxs-lookup"><span data-stu-id="91a55-129">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>

  - <span data-ttu-id="91a55-130">**Microsoft .NET Framework 4,5**   La edición de 64 bits de Microsoft .NET Framework 4,5 es necesaria para Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="91a55-130">**Microsoft .NET Framework 4.5**   The 64-bit edition of Microsoft .NET Framework 4.5 is required for Lync Server 2013.</span></span>

  - <span data-ttu-id="91a55-131">**Requisitos previos de software para servidores de bases de datos**   Para obtener información sobre la actualización de Windows que se requiere para los servidores de bases de datos, como la base de datos back-end, la base de datos de archivado y la base de datos de supervisión, consulte la documentación de SQL Server 2012 en [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .</span><span class="sxs-lookup"><span data-stu-id="91a55-131">**Prerequisite software for database servers**   For details about the Windows Update required for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server 2012 documentation at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="91a55-132">Lync Server 2013 instala automáticamente Microsoft SQL Server 2012 Express en cada servidor Standard Edition y en cada servidor que ejecuta Lync Server 2013 en el que se encuentra el almacén de configuración local.</span><span class="sxs-lookup"><span data-stu-id="91a55-132">Lync Server 2013 automatically installs Microsoft SQL Server 2012 Express on each Standard Edition server and each server running Lync Server 2013 on which the local configuration store is located.</span></span>

    
    </div>

  - <span data-ttu-id="91a55-133">**Windows Media Format Runtime**   Todos los servidores front-end y los servidores Standard Edition en los que se implemente la Conferencia deben tener instalado el Windows Media Format Runtime.</span><span class="sxs-lookup"><span data-stu-id="91a55-133">**Windows Media Format Runtime**   All Front End Servers and Standard Edition servers where conferencing will be deployed must have the Windows Media Format Runtime installed.</span></span> <span data-ttu-id="91a55-134">El tiempo de ejecución de Windows Media Format es necesario para ejecutar los archivos de audio de Windows Media (. WMA) que las aplicaciones de los grupos estacionamiento, anuncio y respuesta de llamadas se reproducen para anuncios y música.</span><span class="sxs-lookup"><span data-stu-id="91a55-134">The Windows Media Format Runtime is required to run the Windows Media Audio (.wma) files that the Call Park, Announcement, and Response Group applications play for announcements and music.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="91a55-135">Para Windows Server 2012 y Windows Server 2012 R2, el tiempo de ejecución de Windows Media Format se instala con Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="91a55-135">For Windows Server 2012 and Windows Server 2012 R2 the Windows Media Format Runtime installs with Microsoft Media Foundation.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="91a55-136">Para Windows Server &nbsp; 2008 y Windows server &nbsp; 2008 &nbsp; R2, el tiempo de ejecución de Windows Media Format se instala como parte de la experiencia de escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="91a55-136">For Windows Server&nbsp;2008 and Windows Server&nbsp;2008&nbsp;R2 the Windows Media Format Runtime installs as part of the Windows Desktop Experience.</span></span> <span data-ttu-id="91a55-137">Se recomienda instalar la experiencia de escritorio de Windows antes de instalar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="91a55-137">It is recommended that you install Windows Desktop Experience before you install Lync Server 2013.</span></span> <span data-ttu-id="91a55-138">Si Lync Server 2013 no encuentra este software en el servidor, le pedirá que lo instale y, a continuación, deberá reiniciar el servidor para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="91a55-138">If Lync Server 2013 does not find this software on the server, it will prompt you to install it, and then you must restart the server to complete installation.</span></span>

    
    <span data-ttu-id="91a55-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91a55-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

