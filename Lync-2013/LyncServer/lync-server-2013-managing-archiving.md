---
title: 'Lync Server 2013: Administración de archivado'
description: 'Lync Server 2013: administración del archivado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Lync Server 2013 Archiving
ms:assetid: 48c6cc8c-c2c1-4534-9a8a-fd5eb738076a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520990(v=OCS.15)
ms:contentKeyID: 48184003
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c7010645f36a7144ea508447d2c628bc8feacb0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425979"
---
# <a name="managing-lync-server-2013-archiving"></a><span data-ttu-id="41c9f-103">Administración de archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41c9f-103">Managing Lync Server 2013 Archiving</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41c9f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41c9f-104">

<span> </span></span></span>

<span data-ttu-id="41c9f-105">_**Última modificación del tema:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="41c9f-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="41c9f-106">Al implementar el archivado de la organización, se especifica la configuración inicial durante la implementación.</span><span class="sxs-lookup"><span data-stu-id="41c9f-106">When you deploy Archiving for your organization, you specify the initial configuration during deployment.</span></span> <span data-ttu-id="41c9f-107">Sin embargo, puede haber ocasiones en las que desee cambiar el modo en que implementa la compatibilidad de archivado para la administración diaria o para cumplir los nuevos requisitos de la organización.</span><span class="sxs-lookup"><span data-stu-id="41c9f-107">However, there may be times when you want to change how you implement archiving support for day-to-day management or to meet new requirements in your organization.</span></span> <span data-ttu-id="41c9f-108">Por ejemplo, es posible que tenga que configurar el soporte de archivo de forma diferente para un sitio, grupo de servidores o usuarios específicos de la organización.</span><span class="sxs-lookup"><span data-stu-id="41c9f-108">For example, you may need to set up archiving support differently for a specific site, pool, or users within your organization.</span></span> <span data-ttu-id="41c9f-109">Para los usuarios alojados en Lync Server 2013, lo que debe hacer es crear y personalizar las directivas y configuraciones de archivado.</span><span class="sxs-lookup"><span data-stu-id="41c9f-109">For users homed on Lync Server 2013, you do this be creating and customizing archiving policies and configurations.</span></span> <span data-ttu-id="41c9f-110">Si usa la integración de Microsoft Exchange, también debe configurar las opciones de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="41c9f-110">If you use Microsoft Exchange integration, you must also configure Exchange 2013 settings.</span></span> <span data-ttu-id="41c9f-111">Esta sección proporciona información y procedimientos para que pueda realizar cambios en la implementación de archivado.</span><span class="sxs-lookup"><span data-stu-id="41c9f-111">This section provides information and procedures to enable you to make changes to your Archiving deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="41c9f-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="41c9f-112">In This Section</span></span>

  - [<span data-ttu-id="41c9f-113">Cómo funciona el archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41c9f-113">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)

  - [<span data-ttu-id="41c9f-114">Administrar el archivado de comunicaciones internas y externas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41c9f-114">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)

  - [<span data-ttu-id="41c9f-115">Administrar las opciones de configuración de archivado en Lync Server 2013 para su organización, sitios y grupos</span><span class="sxs-lookup"><span data-stu-id="41c9f-115">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)

  - [<span data-ttu-id="41c9f-116">Cambiar las opciones de base de datos de archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41c9f-116">Changing Archiving database options in Lync Server 2013</span></span>](lync-server-2013-changing-archiving-database-options.md)

  - [<span data-ttu-id="41c9f-117">Exportar datos archivados desde Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41c9f-117">Exporting archived data from Lync Server 2013</span></span>](lync-server-2013-exporting-archived-data.md)

<span data-ttu-id="41c9f-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41c9f-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

