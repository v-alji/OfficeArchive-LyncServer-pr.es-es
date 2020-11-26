---
title: 'Lync Server 2013: Requisitos previos y roles para configurar anuncios'
description: 'Lync Server 2013: requisitos previos y roles de configuración de la presentación.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Announcement configuration prerequisites and roles
ms:assetid: 82f2dfe9-4c5e-4d65-96a1-96495d506ea4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398658(v=OCS.15)
ms:contentKeyID: 48184674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8e6e7009adc6826c255e28ddda925b0e9be5fd6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439971"
---
# <a name="announcement-configuration-prerequisites-and-roles-in-lync-server-2013"></a><span data-ttu-id="4da84-103">Requisitos previos y roles para configurar anuncios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4da84-103">Announcement configuration prerequisites and roles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4da84-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4da84-104">

<span> </span></span></span>

<span data-ttu-id="4da84-105">_**Última modificación del tema:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="4da84-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="4da84-106">El anuncio es una característica de administración de llamadas de voz de empresa.</span><span class="sxs-lookup"><span data-stu-id="4da84-106">Announcement is an Enterprise Voice call management feature.</span></span> <span data-ttu-id="4da84-107">En este tema se describe lo que debe tener en cuenta antes de poder configurar el anuncio y las asignaciones de roles que necesita para realizar tareas de configuración.</span><span class="sxs-lookup"><span data-stu-id="4da84-107">This topic describes what you need to have in place before you can configure Announcement and the role assignments that you need to perform configuration tasks.</span></span>

<span data-ttu-id="4da84-108">En esta sección se supone que ha leído la documentación de planeación relacionada con el anuncio (vea [planear las características de administración de llamadas en Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span><span class="sxs-lookup"><span data-stu-id="4da84-108">This section assumes that you have read the planning documentation related to Announcement (see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span></span>

<div>

## <a name="announcement-configuration-prerequisites"></a><span data-ttu-id="4da84-109">Requisitos previos de configuración del anuncio</span><span class="sxs-lookup"><span data-stu-id="4da84-109">Announcement Configuration Prerequisites</span></span>

<span data-ttu-id="4da84-110">La aplicación de anuncios requiere los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="4da84-110">The Announcement application requires the following components:</span></span>

  - <span data-ttu-id="4da84-111">Servicio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4da84-111">Application service</span></span>

  - <span data-ttu-id="4da84-112">Aplicación de grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="4da84-112">Response Group application</span></span>

  - <span data-ttu-id="4da84-113">Almacén de archivos, para mantener los archivos de audio</span><span class="sxs-lookup"><span data-stu-id="4da84-113">File Store, to hold audio files</span></span>

<span data-ttu-id="4da84-114">Todos estos componentes se instalan de forma predeterminada al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="4da84-114">All of these components are installed by default when you deploy Enterprise Voice.</span></span>

</div>

<div>

## <a name="announcement-configuration-roles"></a><span data-ttu-id="4da84-115">Roles de configuración de anuncio</span><span class="sxs-lookup"><span data-stu-id="4da84-115">Announcement Configuration Roles</span></span>

<span data-ttu-id="4da84-116">Puede usar las siguientes herramientas administrativas para configurar anuncios:</span><span class="sxs-lookup"><span data-stu-id="4da84-116">You can use the following administrative tools to configure announcements:</span></span>

  - <span data-ttu-id="4da84-117">Panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="4da84-117">Lync Server Control Panel</span></span>

  - <span data-ttu-id="4da84-118">Shell de administración de Communications Server</span><span class="sxs-lookup"><span data-stu-id="4da84-118">Lync Server Management Shell</span></span>

<span data-ttu-id="4da84-119">La configuración de la aplicación de anuncio requiere uno de los siguientes roles administrativos:</span><span class="sxs-lookup"><span data-stu-id="4da84-119">Configuring Announcement application requires one of the following administrative roles:</span></span>

  - <span data-ttu-id="4da84-120">**CsVoiceAdministrator**   Esta función de administrador puede crear, configurar y administrar todas las configuraciones y directivas relacionadas con la voz, incluyendo la configuración de la presentación.</span><span class="sxs-lookup"><span data-stu-id="4da84-120">**CsVoiceAdministrator**   This administrator role can create, configure, and manage all voice-related settings and policies, including Announcement settings.</span></span>

  - <span data-ttu-id="4da84-121">**CsServerAdministrator**   Esta función de administrador puede administrar, supervisar y solucionar problemas de servidores y servicios, así como configurar todas las opciones de presentación.</span><span class="sxs-lookup"><span data-stu-id="4da84-121">**CsServerAdministrator**   This administrator role can manage, monitor, and troubleshoot servers and services, and configure all Announcement settings.</span></span>

  - <span data-ttu-id="4da84-122">**CsAdministrator**   Esta función de administrador puede realizar todas las tareas administrativas y modificar toda la configuración.</span><span class="sxs-lookup"><span data-stu-id="4da84-122">**CsAdministrator**   This administrator role can perform all administrative tasks and modify all settings.</span></span>

  - <span data-ttu-id="4da84-123">**CsViewOnlyAdministrator**   Este rol de administrador puede ver la implementación para supervisar el estado de implementación.</span><span class="sxs-lookup"><span data-stu-id="4da84-123">**CsViewOnlyAdministrator**   This administrator role can view the deployment to monitor deployment health.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4da84-124">Para obtener más información sobre los derechos de usuario administrativos, consulte <A href="lync-server-2013-planning-for-role-based-access-control.md">planificación de control de acceso basado en roles en Lync Server 2013</A> en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="4da84-124">For details about administrative user rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4da84-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4da84-125">See Also</span></span>


[<span data-ttu-id="4da84-126">Implementación de telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4da84-126">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="4da84-127">Planeamiento de las características de administración de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4da84-127">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="4da84-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4da84-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

