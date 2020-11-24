---
title: 'Lync Server 2013: configuración y asignación de directivas de archivado'
description: 'Lync Server 2013: configuración y asignación de directivas de archivado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring and assigning Archiving policies
ms:assetid: acd18ea8-c7f1-4178-871a-cd3b75bdaa8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205175(v=OCS.15)
ms:contentKeyID: 48185121
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ebe08715433e04e56758c7fb09b331065fbd6f44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399179"
---
# <a name="configuring-and-assigning-archiving-policies-in-lync-server-2013"></a><span data-ttu-id="f92ef-103">Configurar y asignar directivas de archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f92ef-103">Configuring and assigning Archiving policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f92ef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f92ef-104">

<span> </span></span></span>

<span data-ttu-id="f92ef-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="f92ef-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="f92ef-106">En Lync Server 2013, se usan directivas para habilitar y deshabilitar el archivado de comunicaciones internas y comunicaciones externas para los usuarios alojados en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f92ef-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users who are homed on Lync Server 2013.</span></span> <span data-ttu-id="f92ef-107">Esto incluye las siguientes directivas de archivado:</span><span class="sxs-lookup"><span data-stu-id="f92ef-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="f92ef-108">Una directiva global que se crea de forma predeterminada al implementar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f92ef-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="f92ef-109">Directivas opcionales a nivel de sitio y de usuario que puede crear y usar para especificar cómo se implementa el archivado para usuarios o sitios específicos.</span><span class="sxs-lookup"><span data-stu-id="f92ef-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="f92ef-110">Inicialmente, debe configurar las directivas de archivado al implementar el archivado, pero puede cambiar, agregar y eliminar directivas después de la implementación.</span><span class="sxs-lookup"><span data-stu-id="f92ef-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="f92ef-111">En el panel de control de Lync Server 2013, puede usar la página **Directiva de archivado** del grupo **archivado y supervisión** para administrar directivas a nivel global, nivel de sitio y nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="f92ef-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f92ef-112">Para controlar la implementación de archivado, debe especificar las opciones para archivar las configuraciones, por ejemplo, si desea archivar la mensajería instantánea o la Conferencia, el uso del modo crítico y las opciones de depuración.</span><span class="sxs-lookup"><span data-stu-id="f92ef-112">To control the implementation of Archiving, you must specify options in Archiving configurations, such as whether to archive IM or conferencing, the use of critical mode, and purging options.</span></span> <span data-ttu-id="f92ef-113">De forma predeterminada, no se habilita ninguna opción en la configuración global de archivado ni en ninguna configuración de archivado de sitios o grupos.</span><span class="sxs-lookup"><span data-stu-id="f92ef-113">By default no options are enabled in the global Archiving configuration or any site or pool Archiving configuration.</span></span> <span data-ttu-id="f92ef-114">Debe especificar todas las opciones apropiadas en las configuraciones de archivado antes de habilitar el archivado de las comunicaciones internas o externas en las directivas de archivado.</span><span class="sxs-lookup"><span data-stu-id="f92ef-114">You should specify all appropriate options in the Archiving configurations before enabling Archiving for internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="f92ef-115">Para obtener más información, vea <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">administrar las opciones de configuración de archivado en Lync Server 2013 para su organización, sitios y grupos</A> en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="f92ef-115">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span><BR><span data-ttu-id="f92ef-116">Si integra el almacenamiento de Lync Server con el almacenamiento de Exchange 2013, las directivas de usuario de Exchange prevalecen sobre las directivas de archivado de Lync Server 2013, pero solo para aquellos usuarios que estén alojados en Exchange 2013 que tengan sus buzones puestos en In-Place en espera.</span><span class="sxs-lookup"><span data-stu-id="f92ef-116">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies but only for those users who are homed on Exchange 2013 who have had their mailboxes put on In-Place Hold.</span></span>



</div>

<span data-ttu-id="f92ef-117">Para obtener más información sobre cómo se implementan las directivas, incluida la jerarquía de directivas, consulte [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, la documentación de implementación o la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="f92ef-117">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span> <span data-ttu-id="f92ef-118">Para obtener detalles sobre cómo administrar directivas después de la implementación, vea [administrar el archivado de comunicaciones internas y externas en Lync Server 2013](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md) en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="f92ef-118">For details about how to manage policies after deployment, see [Managing the Archiving of internal and external communications in Lync Server 2013](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md) in the Operations documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f92ef-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f92ef-119">In This Section</span></span>

  - [<span data-ttu-id="f92ef-120">Configuración de la directiva global para archivar en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f92ef-120">Configuring the global policy for Archiving in Lync Server 2013</span></span>](lync-server-2013-configuring-the-global-policy-for-archiving.md)

  - [<span data-ttu-id="f92ef-121">Configurar directivas de sitio para archivar en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f92ef-121">Setting up site policies for Archiving in Lync Server 2013</span></span>](lync-server-2013-setting-up-site-policies-for-archiving.md)

  - [<span data-ttu-id="f92ef-122">Configuración de directivas de archivado para usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f92ef-122">Setting up Archiving policies for users in Lync Server 2013</span></span>](lync-server-2013-setting-up-archiving-policies-for-users.md)

<span data-ttu-id="f92ef-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f92ef-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

