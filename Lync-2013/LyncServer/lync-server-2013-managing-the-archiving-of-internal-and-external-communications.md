---
title: Administrar el archivado de las comunicaciones internas y externas
description: Administrar el archivado de las comunicaciones internas y externas.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Archiving of internal and external communications
ms:assetid: 6c2cf941-3204-4f1a-a7e0-416c828056d9
ms:mtpsurl: https://technet.microsoft.com/library/JJ204977(v=OCS.15)
ms:contentKeyID: 48184417
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 857e4772d93ead01c3914b2ee04b71bddb1feed4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437192"
---
# <a name="managing-the-archiving-of-internal-and-external-communications-in-lync-server-2013"></a><span data-ttu-id="ff3c1-103">Administrar el archivado de comunicaciones internas y externas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff3c1-103">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ff3c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ff3c1-104">

<span> </span></span></span>

<span data-ttu-id="ff3c1-105">_**Última modificación del tema:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="ff3c1-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="ff3c1-106">En Lync Server 2013, se usan directivas de archivado para habilitar y deshabilitar el archivado de comunicaciones internas y comunicaciones externas si no se usa la integración de Microsoft Exchange o si hay usuarios que no están alojados en Exchange 2013 con sus buzones colocados en In-Place en espera.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-106">In Lync Server 2013, you use Archiving policies to enable and disable archiving for internal communications and external communications if you do not use Microsoft Exchange integration or you have users who are not homed on Exchange 2013 with their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="ff3c1-107">Esto incluye las siguientes directivas de archivado:</span><span class="sxs-lookup"><span data-stu-id="ff3c1-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="ff3c1-108">Una directiva global que se crea de forma predeterminada al implementar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="ff3c1-109">Directivas opcionales a nivel de sitio y de usuario que puede crear y usar para especificar cómo se implementa el archivado para usuarios o sitios específicos.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="ff3c1-110">Inicialmente, debe configurar las directivas de archivado al implementar el archivado, pero puede cambiar, agregar y eliminar directivas después de la implementación.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="ff3c1-111">En el panel de control de Lync Server 2013, puede usar la página **Directiva de archivado** del grupo **archivado y supervisión** para administrar directivas a nivel global, nivel de sitio y nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="ff3c1-112">Si integra el almacenamiento de Lync Server con el almacenamiento de Exchange 2013, las directivas de usuario de Exchange tienen prioridad sobre las directivas de archivado de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="ff3c1-113">Para obtener más información sobre cómo se implementan las directivas, incluida la jerarquía de directivas, consulte [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, la documentación de implementación o la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="ff3c1-114">Para controlar la implementación de archivado, debe especificar las opciones para archivar las configuraciones, por ejemplo, si desea archivar la mensajería instantánea o la Conferencia, el uso del modo crítico y las opciones de depuración.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-114">To control the implementation of Archiving, you must specify options in Archiving configurations, such as whether to archive IM or conferencing, the use of critical mode, and purging options.</span></span> <span data-ttu-id="ff3c1-115">De forma predeterminada, no se habilita ninguna opción en la configuración global de archivado ni en ninguna configuración de archivado de sitios o grupos.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-115">By default no options are enabled in the global Archiving configuration or any site or pool Archiving configuration.</span></span> <span data-ttu-id="ff3c1-116">Debe especificar todas las opciones apropiadas en las configuraciones de archivado antes de habilitar el archivado de las comunicaciones internas o externas en las directivas de archivado.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving for internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="ff3c1-117">Para obtener más información, vea <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">administrar las opciones de configuración de archivado en Lync Server 2013 para su organización, sitios y grupos</A> en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span><BR><span data-ttu-id="ff3c1-118">Si habilita la integración de Microsoft Exchange para su implementación, las directivas de Exchange controlan si el archivado está habilitado para los usuarios que estén alojados en Exchange 2013 y que sus buzones se pongan en espera In-Place.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-118">If you enable Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="ff3c1-119">Para obtener más información, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configurar directivas para archivar en Lync Server 2013 al usar la integración de Exchange Server</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="ff3c1-119">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ff3c1-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ff3c1-120">In This Section</span></span>

  - [<span data-ttu-id="ff3c1-121">Crear una directiva de archivado en Lync Server 2013 para habilitar o deshabilitar el archivado de las comunicaciones internas o externas para usuarios o sitios específicos</span><span class="sxs-lookup"><span data-stu-id="ff3c1-121">Creating an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for specific sites or users</span></span>](lync-server-2013-create-archiving-policy-sites-users.md)

  - [<span data-ttu-id="ff3c1-122">Cambiar una directiva de archivado en Lync Server 2013 para habilitar o deshabilitar el archivado de comunicaciones internas o externas para la organización, los sitios o los usuarios</span><span class="sxs-lookup"><span data-stu-id="ff3c1-122">Changing an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for your organization, sites, or users</span></span>](lync-server-2013-change-archiving-policy-org-sites-users.md)

  - [<span data-ttu-id="ff3c1-123">Aplicar una directiva de archivado a los usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff3c1-123">Applying an Archiving policy to users in Lync Server 2013</span></span>](lync-server-2013-applying-an-archiving-policy-to-users.md)

  - [<span data-ttu-id="ff3c1-124">Configurar directivas para archivar en Lync Server 2013 al usar la integración de Exchange Server</span><span class="sxs-lookup"><span data-stu-id="ff3c1-124">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</span></span>](lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md)

  - [<span data-ttu-id="ff3c1-125">Eliminar una directiva de archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff3c1-125">Deleting an Archiving policy in Lync Server 2013</span></span>](lync-server-2013-deleting-an-archiving-policy.md)

<span data-ttu-id="ff3c1-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ff3c1-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

