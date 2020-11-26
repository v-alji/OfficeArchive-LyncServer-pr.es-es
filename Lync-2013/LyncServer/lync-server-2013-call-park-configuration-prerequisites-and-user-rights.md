---
title: 'Lync Server 2013: Requisitos previos de configuración del estacionamiento de llamadas y derechos de usuario'
description: 'Lync Server 2013: requisitos previos y derechos de usuario para la configuración de llamadas en el parque.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Park configuration prerequisites and user rights
ms:assetid: 25b8cfe0-e4e7-487c-9e78-8c040f629059
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425730(v=OCS.15)
ms:contentKeyID: 48183648
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b01187ad32fa7338765c0fa5b409b4e185e8ad35
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435715"
---
# <a name="call-park-configuration-prerequisites-and-user-rights-in-lync-server-2013"></a><span data-ttu-id="a6b35-103">Requisitos previos de configuración del estacionamiento de llamadas y derechos de usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6b35-103">Call Park configuration prerequisites and user rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6b35-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6b35-104">

<span> </span></span></span>

<span data-ttu-id="a6b35-105">_**Última modificación del tema:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="a6b35-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="a6b35-106">Estacionamiento de llamadas es una característica de administración de llamadas que se instala de forma predeterminada al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="a6b35-106">Call Park is a call management feature that is installed by default when you deploy Enterprise Voice.</span></span> <span data-ttu-id="a6b35-107">En este tema se describe lo que debe tener en cuenta antes de poder configurar el parque de llamadas y los derechos de usuario que necesita para realizar las tareas de configuración.</span><span class="sxs-lookup"><span data-stu-id="a6b35-107">This topic describes what you need to have in place before you can configure Call Park and the user rights that you need to perform configuration tasks.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a6b35-108">No se realiza una copia de seguridad de los archivos personalizados de música en espera para la aplicación de estacionamiento de llamadas como parte del proceso de recuperación de desastres de Lync Server 2013, y los archivos se perderán si los archivos cargados en el grupo están dañados, están dañados o se han borrado.</span><span class="sxs-lookup"><span data-stu-id="a6b35-108">Customized music-on-hold files for the Call Park application are not backed up as part of the Lync Server 2013 disaster recovery process, and the files will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span> <span data-ttu-id="a6b35-109">Guarda siempre una copia de seguridad independiente de los archivos de música en espera personalizados que haya cargado para el estacionamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="a6b35-109">Always keep a separate backup copy of the customized music-on-hold files that you have uploaded for Call Park.</span></span>



</div>

<span data-ttu-id="a6b35-110">En esta sección se supone que ha leído la documentación de planificación relacionada con Call Park (consulte [planificación de las características de administración de llamadas en Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span><span class="sxs-lookup"><span data-stu-id="a6b35-110">This section assumes that you have read the planning documentation related to Call Park (see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span></span>

<div>

## <a name="call-park-configuration-prerequisites"></a><span data-ttu-id="a6b35-111">Requisitos previos de configuración del parque de llamadas</span><span class="sxs-lookup"><span data-stu-id="a6b35-111">Call Park Configuration Prerequisites</span></span>

<span data-ttu-id="a6b35-112">El parque de llamadas requiere los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="a6b35-112">Call Park requires the following components:</span></span>

  - <span data-ttu-id="a6b35-113">Servicio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a6b35-113">Application service</span></span>

  - <span data-ttu-id="a6b35-114">Aplicación de estacionamiento de llamadas</span><span class="sxs-lookup"><span data-stu-id="a6b35-114">Call Park application</span></span>

<span data-ttu-id="a6b35-115">Estos componentes se instalan automáticamente al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="a6b35-115">These components are installed automatically when you deploy Enterprise Voice.</span></span>

<span data-ttu-id="a6b35-116">Si desea que las personas que llaman oigan música mientras se estaciona la llamada, también se necesita un archivo de música en espera.</span><span class="sxs-lookup"><span data-stu-id="a6b35-116">If you want callers to hear music while the call is parked, a music-on-hold file is also required.</span></span> <span data-ttu-id="a6b35-117">El archivo de música en espera predeterminada se instala automáticamente al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="a6b35-117">A default music-on-hold file is installed automatically when you deploy Enterprise Voice.</span></span> <span data-ttu-id="a6b35-118">Puede sustituir el archivo predeterminado con su propio archivo de música en espera.</span><span class="sxs-lookup"><span data-stu-id="a6b35-118">You can substitute the default file with your own music-on-hold file.</span></span> <span data-ttu-id="a6b35-119">El parque de llamadas usa el almacén de archivos para almacenar el archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="a6b35-119">Call Park uses File Store to hold the audio file.</span></span>

</div>

<div>

## <a name="call-park-configuration-user-rights"></a><span data-ttu-id="a6b35-120">Derechos de usuario de configuración de estacionamiento de llamadas</span><span class="sxs-lookup"><span data-stu-id="a6b35-120">Call Park Configuration User Rights</span></span>

<span data-ttu-id="a6b35-121">Puede usar las siguientes herramientas administrativas para configurar el parque de llamadas:</span><span class="sxs-lookup"><span data-stu-id="a6b35-121">You can use the following administrative tools to configure Call Park:</span></span>

  - <span data-ttu-id="a6b35-122">Panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="a6b35-122">Lync Server Control Panel</span></span>

  - <span data-ttu-id="a6b35-123">Shell de administración de Communications Server</span><span class="sxs-lookup"><span data-stu-id="a6b35-123">Lync Server Management Shell</span></span>

<span data-ttu-id="a6b35-124">Use estas herramientas para configurar la tabla de llamadas en órbita y para configurar otras opciones que usa el parque de llamadas.</span><span class="sxs-lookup"><span data-stu-id="a6b35-124">You use these tools to set up the Call Park orbit table and to configure other settings used by Call Park.</span></span>

<span data-ttu-id="a6b35-125">La configuración de estacionamiento requiere cualquiera de los siguientes roles administrativos, en función de la tarea:</span><span class="sxs-lookup"><span data-stu-id="a6b35-125">Configuring Call Park requires any of the following administrative roles, depending on the task:</span></span>

  - <span data-ttu-id="a6b35-126">**CsVoiceAdministrator:** Esta función de administrador puede crear, configurar y administrar todas las configuraciones y directivas relacionadas con las voz.</span><span class="sxs-lookup"><span data-stu-id="a6b35-126">**CsVoiceAdministrator:** This administrator role can create, configure, and manage all voice-related settings and policies.</span></span>

  - <span data-ttu-id="a6b35-127">**CsUserAdministrator:** Esta función de administrador puede habilitar el parque de llamadas en la política de voz.</span><span class="sxs-lookup"><span data-stu-id="a6b35-127">**CsUserAdministrator:** This administrator role can enable Call Park in voice policy.</span></span> <span data-ttu-id="a6b35-128">Esta función de administrador también tiene acceso de vista de solo lectura a todas las configuraciones de voz.</span><span class="sxs-lookup"><span data-stu-id="a6b35-128">This administrator role also has read-only view access to all voice configurations.</span></span>

  - <span data-ttu-id="a6b35-129">**CsServerAdministrator:** Esta función de administrador puede administrar, supervisar y solucionar problemas de servidores y servicios.</span><span class="sxs-lookup"><span data-stu-id="a6b35-129">**CsServerAdministrator:** This administrator role can manage, monitor, and troubleshoot servers and services.</span></span>

  - <span data-ttu-id="a6b35-130">**CsAdministrator:** Esta función de administrador puede realizar todas las tareas de CsVoiceAdministrator, CsServerAdministrator y CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="a6b35-130">**CsAdministrator:** This administrator role can perform all of the tasks of CsVoiceAdministrator, CsServerAdministrator, and CsUserAdministrator.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6b35-131">Para obtener más información sobre los derechos administrativos, consulte <A href="lync-server-2013-planning-for-role-based-access-control.md">planificación de control de acceso basado en roles en Lync Server 2013</A> en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="a6b35-131">For details about administrative rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a6b35-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6b35-132">See Also</span></span>


[<span data-ttu-id="a6b35-133">Implementación de telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6b35-133">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="a6b35-134">Planeamiento de las características de administración de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6b35-134">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="a6b35-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6b35-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

