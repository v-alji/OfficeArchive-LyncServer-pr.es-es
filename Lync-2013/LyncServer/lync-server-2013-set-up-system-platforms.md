---
title: 'Lync Server 2013: Configurar plataformas del sistema'
description: 'Lync Server 2013: configurar plataformas del sistema.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up system platforms
ms:assetid: 2e72e49d-2737-4b5b-8c0a-60f6ecb15bf1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204783(v=OCS.15)
ms:contentKeyID: 48183756
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd02c519d5632b7aa5732fbd9b880f7d1084b50f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423976"
---
# <a name="set-up-system-platforms-in-lync-server-2013"></a><span data-ttu-id="57bc1-103">Configurar plataformas del sistema en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57bc1-103">Set up system platforms in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="57bc1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="57bc1-104">

<span> </span></span></span>

<span data-ttu-id="57bc1-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="57bc1-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="57bc1-106">Antes de iniciar la implementación de un servidor de chat persistente, debe instalar el sistema operativo necesario en el hardware que cumpla con los requisitos del sistema en los servidores:</span><span class="sxs-lookup"><span data-stu-id="57bc1-106">Before starting the deployment of Persistent Chat Server, you must install the required operating system on hardware that meets system requirements on servers:</span></span>

<span data-ttu-id="57bc1-107">Para obtener detalles sobre el hardware compatible con servidores que ejecutan Lync Server 2013, servidores de bases de datos y servidores de archivos, consulte [hardware compatible para Lync server 2013](lync-server-2013-supported-hardware.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="57bc1-107">For details about supported hardware for servers running Lync Server 2013, database servers, and file servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span> <span data-ttu-id="57bc1-108">Para obtener más información sobre los sistemas operativos y el software de base de datos compatibles, vea [compatibilidad de software y infraestructura de servidor en Lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="57bc1-108">For details about supported operating systems and database software, see [Server software and infrastructure support in Lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md) in the Supportability documentation.</span></span> <span data-ttu-id="57bc1-109">Para obtener más información sobre los requisitos de Windows Update, consulte [compatibilidad y requisitos de servidor adicionales en Lync server 2013](lync-server-2013-additional-server-support-and-requirements.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="57bc1-109">For details about Windows update requirements, see [Additional server support and requirements in Lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md) in the Supportability documentation.</span></span>

<span data-ttu-id="57bc1-110">El servidor de solicitudes de cliente de chat persistente, **PersistentChatService**, se puede implementar en uno o varios equipos independientes de un grupo de servidores de Lync Server 2013 Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="57bc1-110">The Persistent Chat Server Front End Server, **PersistentChatService**, can be deployed on one or more stand-alone computers in a Lync Server 2013 Enterprise Edition pool.</span></span> <span data-ttu-id="57bc1-111">No se pueden colocar en los servidores front-end de Lync Server Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="57bc1-111">They cannot be collocated on the Lync Server Enterprise Edition Front End Servers.</span></span> <span data-ttu-id="57bc1-112">El programa previo puede implementar el servidor de chat persistente, del mismo modo que otros roles de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="57bc1-112">Persistent Chat Server can be deployed by the Bootstrapper, just like other Lync Server roles.</span></span> <span data-ttu-id="57bc1-113">Los **servicios Web de chat persistentes para la carga y descarga de archivos** y los **servicios Web de chat persistentes para la administración de salones de chat** son componentes Web implementados en los servidores Front-End de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57bc1-113">The **Persistent Chat Web Services for File Upload/Download**, and **Persistent Chat Web Services for Chat Room Management** are web components deployed on the Lync Server 2013 Front End Servers.</span></span>

<span data-ttu-id="57bc1-114">Un solo servidor de cliente de servidor de chat persistente puede admitir usuarios activos de 20.000.</span><span class="sxs-lookup"><span data-stu-id="57bc1-114">A single Persistent Chat Server Front End Server can support 20,000 active users.</span></span> <span data-ttu-id="57bc1-115">Puede tener un grupo de servidores de chat persistente con hasta 4 extremos frontales activos que admitan un total de 80.000 usuarios simultáneos.</span><span class="sxs-lookup"><span data-stu-id="57bc1-115">You can have a Persistent Chat Server pool with up to 4 active front ends supporting a total of 80,000 concurrent users.</span></span> <span data-ttu-id="57bc1-116">El servidor de back-end de chat persistente, **PersistentChatStore**, almacena las categorías y los salones de chat.</span><span class="sxs-lookup"><span data-stu-id="57bc1-116">The Persistent Chat Back End Server, **PersistentChatStore**, stores the chat rooms and categories.</span></span> <span data-ttu-id="57bc1-117">Le recomendamos que instale el **PersistentChatStore** en un servidor de back-end de SQL Server dedicado en el grupo de servidores Enterprise Edition. aunque admitimos collocating servidor back-end y **PersistentChatStore** de Lync Server 2013 en la misma instancia de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="57bc1-117">We recommend that you install the **PersistentChatStore** on a dedicated SQL Server Back End Server in your Enterprise Edition pool; although we support collocating Lync Server 2013 Back End Server and **PersistentChatStore** on the same SQL Server instance.</span></span>

<span data-ttu-id="57bc1-118">Si su organización requiere soporte de cumplimiento, puede instalarlo con el generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="57bc1-118">If your organization requires compliance support, you can install it by using Topology Builder.</span></span> <span data-ttu-id="57bc1-119">El servicio de cumplimiento del servidor de chat persistente está instalado en el mismo equipo que el servidor de solicitudes de cliente de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="57bc1-119">The Persistent Chat Server Compliance service is installed on the same computer as the Persistent Chat Server Front End Server.</span></span> <span data-ttu-id="57bc1-120">Se necesita una base de datos independiente para el cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="57bc1-120">A separate database is required for compliance.</span></span> <span data-ttu-id="57bc1-121">Para obtener más información sobre los requisitos de cumplimiento para el servidor de chat persistente, consulte [planificación de servidor de chat persistente en Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) en la documentación de planificación.</span><span class="sxs-lookup"><span data-stu-id="57bc1-121">For details about compliance requirements for Persistent Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

<span data-ttu-id="57bc1-122">Como mínimo, cada topología requiere un servidor con Lync Server 2013 instalado y un servidor con el software de base de datos de SQL Server instalado.</span><span class="sxs-lookup"><span data-stu-id="57bc1-122">At a minimum, each topology requires a server with Lync Server 2013 installed and a server with SQL Server database software installed.</span></span> <span data-ttu-id="57bc1-123">El generador de topología admite varios grupos de servidores de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="57bc1-123">Topology Builder supports multiple Persistent Chat Server pools.</span></span> <span data-ttu-id="57bc1-124">Siga las mismas instrucciones de implementación para implementar varios grupos de servidores de chat persistentes como lo haría para cualquier grupo de servidores desde la [implementación de Lync Server 2013](lync-server-2013-deploying-lync-server.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="57bc1-124">Follow the same deployment instructions for deploying multiple Persistent Chat Server pools as you would for any pool from [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="57bc1-125">También puede implementar un servidor de chat persistente con Lync Server 2013 Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="57bc1-125">You can also deploy Persistent Chat Server with Lync Server 2013 Standard Edition.</span></span> <span data-ttu-id="57bc1-126">En este caso, el servidor front-end **PersistentChatService** se colocará en el servidor Standard Edition y puede implementar el servidor back-end **PersistentChatStore** en la instancia local de SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="57bc1-126">In this case, the **PersistentChatService** Front End Server is collocated on the Standard Edition server, and you can deploy the **PersistentChatStore** Back End Server on the local SQL Server Express instance.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="57bc1-127">No se admite el servidor de chat persistente, &nbsp; Standard Edition, para una alta disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="57bc1-127">We do not support Persistent Chat Server&nbsp;Standard Edition for high availability.</span></span> <span data-ttu-id="57bc1-128">El rendimiento y la escala serán limitados.</span><span class="sxs-lookup"><span data-stu-id="57bc1-128">Performance and scale will be limited.</span></span> <span data-ttu-id="57bc1-129">Además, solo admitimos implementaciones de servidor de servidor de chat, &nbsp; Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="57bc1-129">Furthermore, we support only new Persistent Chat Server&nbsp;Standard Edition server deployments.</span></span> <span data-ttu-id="57bc1-130">No se admite una actualización de Lync Server 2010, servidor de chats grupales a un servidor de Lync Server 2013, una &nbsp; versión estándar de servidor de chat &nbsp; .</span><span class="sxs-lookup"><span data-stu-id="57bc1-130">We do not support an upgrade of Lync Server 2010, Group Chat Server to a Lync Server 2013&nbsp;Persistent Chat Server&nbsp;Standard Edition.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="57bc1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="57bc1-131">See Also</span></span>


[<span data-ttu-id="57bc1-132">Compatibilidad y requisitos para un servidor adicional en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57bc1-132">Additional server support and requirements in Lync Server 2013</span></span>](lync-server-2013-additional-server-support-and-requirements.md)  


[<span data-ttu-id="57bc1-133">Hardware admitido en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57bc1-133">Supported hardware for Lync Server 2013</span></span>](lync-server-2013-supported-hardware.md)  
[<span data-ttu-id="57bc1-134">Software de servidor y compatibilidad con la infraestructura en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57bc1-134">Server software and infrastructure support in Lync Server 2013</span></span>](lync-server-2013-server-software-and-infrastructure-support.md)  
[<span data-ttu-id="57bc1-135">Planeación del servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57bc1-135">Planning for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-planning-for-persistent-chat-server.md)  
[<span data-ttu-id="57bc1-136">Implementar Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57bc1-136">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="57bc1-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="57bc1-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

