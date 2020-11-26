---
title: 'Lync Server 2013: copia de seguridad y control de bases de datos'
description: 'Lync Server 2013: realizar copias de seguridad y supervisar las bases de datos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up Archiving and Monitoring databases
ms:assetid: c120db81-b02c-4a4c-90cd-8aca6cff64f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202188(v=OCS.15)
ms:contentKeyID: 51541515
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49b4fa194bffa27a52f32d61a729eeaa31cc0ad3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438123"
---
# <a name="backing-up-archiving-and-monitoring-databases-in-lync-server-2013"></a><span data-ttu-id="80421-103">Realizar copias de seguridad del archivado y la supervisión de bases de datos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="80421-103">Backing up Archiving and Monitoring databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80421-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80421-104">

<span> </span></span></span>

<span data-ttu-id="80421-105">_**Última modificación del tema:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="80421-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="80421-106">Si implementó el archivado o la supervisión, tendrá que realizar una copia de seguridad de estas bases de datos de acuerdo con la Directiva de copia de seguridad de SQL Server de su organización.</span><span class="sxs-lookup"><span data-stu-id="80421-106">If you deployed Archiving or Monitoring, you need to back up these databases according to your organization's SQL Server backup policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="80421-107">Se realiza una copia de seguridad de la configuración de archivado y supervisión cuando se realiza una copia de seguridad del almacén de administración central.</span><span class="sxs-lookup"><span data-stu-id="80421-107">The settings for Archiving and Monitoring are backed up when you back up the Central Management store.</span></span> <span data-ttu-id="80421-108">Para obtener más información, consulte <A href="lync-server-2013-backing-up-core-data-and-settings.md">realizar copias de seguridad de datos y configuraciones en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="80421-108">For details, see <A href="lync-server-2013-backing-up-core-data-and-settings.md">Backing up core data and settings in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="80421-109">Para archivar y supervisar, puede usar una herramienta de SQL Server, como SQL Server Management Studio, para realizar una copia de seguridad manual, o bien, puede usar las herramientas de administración de SQL Server para programar copias de seguridad regulares y automáticas.</span><span class="sxs-lookup"><span data-stu-id="80421-109">For Archiving and Monitoring, you can use a SQL Server tool such as SQL Server Management Studio to perform a manual backup, or you can use SQL Server management tools to schedule regular, automatic backups.</span></span>

<span data-ttu-id="80421-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80421-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

