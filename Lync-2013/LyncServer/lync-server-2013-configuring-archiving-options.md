---
title: 'Lync Server 2013: configuración de las opciones de archivado'
description: 'Lync Server 2013: configuración de las opciones de archivado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Archiving options
ms:assetid: b2f7f74d-e1ad-494e-9d46-5eb0efe5fb29
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205182(v=OCS.15)
ms:contentKeyID: 48185158
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 99d57f016d76f9ae6a538ef28663a4b4c965b0a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433314"
---
# <a name="configuring-archiving-options-in-lync-server-2013"></a><span data-ttu-id="3358e-103">Configuración de las opciones de archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3358e-103">Configuring Archiving options in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3358e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3358e-104">

<span> </span></span></span>

<span data-ttu-id="3358e-105">_**Última modificación del tema:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="3358e-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="3358e-106">En el panel de control de Lync Server 2013, se usan configuraciones de archivado para especificar cómo se implementa el archivado.</span><span class="sxs-lookup"><span data-stu-id="3358e-106">In Lync Server 2013 Control Panel, you use Archiving configurations to specify how archiving is implemented.</span></span> <span data-ttu-id="3358e-107">Esto incluye las siguientes configuraciones de archivado:</span><span class="sxs-lookup"><span data-stu-id="3358e-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="3358e-108">Una configuración global que se crea de forma predeterminada al implementar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3358e-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="3358e-109">Configuraciones de nivel de sitio y de grupo opcionales que puede crear y usar para especificar cómo se implementa el archivado para grupos o sitios específicos.</span><span class="sxs-lookup"><span data-stu-id="3358e-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="3358e-110">Inicialmente, debe configurar las configuraciones de archivado al implementar el archivado, pero puede cambiar, agregar y eliminar configuraciones después de la implementación.</span><span class="sxs-lookup"><span data-stu-id="3358e-110">You initially set up Archiving configurations when you deploy Archiving, but you can change, add, and delete configurations after deployment.</span></span> <span data-ttu-id="3358e-111">En el panel de control de Lync Server 2013, puede usar la página **configuración de archivado** del grupo **archivado y supervisión** para administrar las configuraciones a nivel global, nivel de sitio y nivel de grupo.</span><span class="sxs-lookup"><span data-stu-id="3358e-111">In Lync Server 2013 Control Panel, you can use the **Archiving Configuration** page of the **Archiving and Monitoring** group to manage configurations at the global level, site level, and pool level.</span></span> <span data-ttu-id="3358e-112">Para obtener detalles sobre cómo se implementan las configuraciones de archivado, incluidas las opciones que puede especificar y la jerarquía de las configuraciones de archivado, consulte [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, la documentación de implementación o la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="3358e-112">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span> <span data-ttu-id="3358e-113">Para más información sobre cómo administrar las configuraciones después de la implementación, consulte [administrar las opciones de configuración de archivado en Lync Server 2013 para su organización, sitios y grupos](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md) en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="3358e-113">For details about how to manage configurations after deployment, see [Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md) in the Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3358e-114">Para usar el archivado, debe configurar las directivas de archivado para especificar si desea habilitar el archivado de las comunicaciones internas, de las comunicaciones externas o de ambos para los usuarios alojados en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3358e-114">To use archiving, you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both for users homed on Lync Server 2013.</span></span> <span data-ttu-id="3358e-115">De forma predeterminada, el archivado no está habilitado para las comunicaciones internas o externas.</span><span class="sxs-lookup"><span data-stu-id="3358e-115">By default, archiving is not enabled for either internal or external communications.</span></span> <span data-ttu-id="3358e-116">Antes de habilitar el archivado en cualquier directiva, debe especificar las configuraciones de archivado apropiadas para su implementación y, opcionalmente, para determinados sitios y grupos, tal y como se describe en esta sección.</span><span class="sxs-lookup"><span data-stu-id="3358e-116">Before enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="3358e-117">Para obtener más información sobre cómo habilitar el archivado, vea <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">configurar y asignar directivas de archivado en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="3358e-117">For details about enabling Archiving, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="3358e-118">Si no usa la integración de Microsoft Exchange para todos los usuarios de su implementación, debe configurar las directivas de archivado para especificar si desea habilitar el archivado de las comunicaciones internas, de las comunicaciones externas o de ambos.</span><span class="sxs-lookup"><span data-stu-id="3358e-118">If you do not use Microsoft Exchange integration for all users in your deployment, you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both.</span></span> <span data-ttu-id="3358e-119">De forma predeterminada, el archivado no está habilitado para las comunicaciones internas o externas para el archivado de datos al usar las bases de datos de archivado de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3358e-119">By default, archiving is not enabled for either internal or external communications for archiving of data when using Lync Server 2013 Archiving databases.</span></span> <span data-ttu-id="3358e-120">Antes de habilitar el archivado en cualquier directiva, debe especificar las configuraciones de archivado apropiadas para su implementación y, opcionalmente, para determinados sitios y grupos, tal y como se describe en esta sección.</span><span class="sxs-lookup"><span data-stu-id="3358e-120">Prior to enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="3358e-121">Para obtener más información sobre cómo habilitar el archivado para su uso con bases de datos de archivado de Lync Server 2013, consulte <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">configuración y asignación de directivas de archivado en Lync server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="3358e-121">For details about enabling Archiving for use with Lync Server 2013 Archiving databases, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3358e-122">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3358e-122">In This Section</span></span>

  - [<span data-ttu-id="3358e-123">Configurar las opciones de archivado en el nivel global de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3358e-123">Configuring Archiving options at the global level in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options-at-the-global-level.md)

  - [<span data-ttu-id="3358e-124">Configuración de las opciones de archivado de un sitio en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3358e-124">Configuring Archiving options for a site in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options-for-a-site.md)

  - [<span data-ttu-id="3358e-125">Configuración de las opciones de archivado de un grupo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3358e-125">Configuring Archiving options for a pool in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options-for-a-pool.md)

<span data-ttu-id="3358e-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3358e-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

