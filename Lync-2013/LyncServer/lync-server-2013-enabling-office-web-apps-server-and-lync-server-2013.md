---
title: 'Lync Server 2013: Habilitación de Office Web Apps Server y Lync Server 2013'
description: 'Lync Server 2013: habilitar Office Web Apps Server y Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Office Web Apps Server and Lync Server 2013
ms:assetid: 3370ab55-9949-4f32-b88b-5cffed6aaad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204792(v=OCS.15)
ms:contentKeyID: 48183790
ms.date: 08/19/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a1bf4e09dc29bf344b78df50595258f0663cd731
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399269"
---
# <a name="configuring-integration-with-office-web-apps-server-and-lync-server-2013"></a><span data-ttu-id="82ac3-103">Configuración de la integración de Office Web Apps Server y Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="82ac3-103">Configuring integration with Office Web Apps Server and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="82ac3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="82ac3-104">

<span> </span></span></span>

<span data-ttu-id="82ac3-105">_**Última modificación del tema:** 2016-08-19_</span><span class="sxs-lookup"><span data-stu-id="82ac3-105">_**Topic Last Modified:** 2016-08-19_</span></span>

<span data-ttu-id="82ac3-106">Lync Server 2013 usa Office Web Apps Server para controlar presentaciones de PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="82ac3-106">Lync Server 2013 employs Office Web Apps Server to handle PowerPoint presentations.</span></span> <span data-ttu-id="82ac3-107">Para obtener más información sobre las ventajas de este enfoque, vea [información general sobre las conferencias web en Lync Server 2013](lync-server-2013-web-conferencing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="82ac3-107">For information about the advantages to this approach, see [Overview of web conferencing in Lync Server 2013](lync-server-2013-web-conferencing-overview.md).</span></span>

<span data-ttu-id="82ac3-108">Para poder usar estas nuevas funciones, los administradores deben instalar Office Web Apps Server y deben configurar Lync Server 2013 para comunicarse con Office Web Apps Server.</span><span class="sxs-lookup"><span data-stu-id="82ac3-108">In order to use these new capabilities administrators must install Office Web Apps Server and they must configure Lync Server 2013 to communicate with Office Web Apps Server.</span></span> <span data-ttu-id="82ac3-109">Esta documentación proporciona información sobre cómo configurar Lync Server 2013 para que funcione con Office Web Apps Server.</span><span class="sxs-lookup"><span data-stu-id="82ac3-109">This documentation provides information on how to configure Lync Server 2013 to work with Office Web Apps Server.</span></span> <span data-ttu-id="82ac3-110">Lo que no proporciona esta documentación es información sobre cómo instalar el servidor de Office Web Apps en sí; para obtener más información, vea el sitio web de implementación de Microsoft Office Web Apps en <https://go.microsoft.com/fwlink/p/?linkid=257525> .</span><span class="sxs-lookup"><span data-stu-id="82ac3-110">What this documentation does not provide is information on how to install Office Web Apps Server itself; for that information, see the Microsoft Office Web Apps Deployment website at <https://go.microsoft.com/fwlink/p/?linkid=257525>.</span></span> <span data-ttu-id="82ac3-111">Esta guía incluye información completa de requisitos previos para Office Web Apps Server; Tenga en cuenta que Office Web Apps Server debe instalarse en un equipo independiente que no ejecute Lync Server, Microsoft SQL Server ni ninguna otra aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="82ac3-111">That guide includes complete prerequisite information for Office Web Apps Server; note that Office Web Apps Server should be installed on a stand-alone computer that is not running Lync Server, Microsoft SQL Server, or any other server application.</span></span> <span data-ttu-id="82ac3-112">(No debe tener ninguna versión de Microsoft Office instalada en ese equipo). Cualquier equipo usado para ejecutar Office Web Apps Server también debe tener instalado un conjunto específico de software (incluidos .NET Framework 4,5 y Windows PowerShell 3,0); Estos requisitos, junto con información sobre la configuración de certificados y servicios de Internet Information Server (IIS), se tratan en detalle en el sitio web de implementación de Microsoft Office Web Apps en <https://go.microsoft.com/fwlink/p/?linkid=257525> .</span><span class="sxs-lookup"><span data-stu-id="82ac3-112">(You must not have any version of Microsoft Office installed on that computer.) Any computer used to run Office Web Apps Server must also have a specific set of software installed (including .NET Framework 4.5 and Windows PowerShell 3.0); these requirements, along with information on configuring certificates and Internet Information Services (IIS), are discussed in detail in the Microsoft Office Web Apps Deployment website at <https://go.microsoft.com/fwlink/p/?linkid=257525>.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="82ac3-113">La última iteración de Office Web Apps Server se denomina Office Online Server, que es compatible con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="82ac3-113">The latest iteration of Office Web Apps Server is named Office Online Server, which is supported by Lync Server 2013.</span></span> <span data-ttu-id="82ac3-114">Para obtener más información, consulte la <A href="https://technet.microsoft.com/library/jj219456(v=office.16).aspx">documentación del servidor de Office Online</A>.</span><span class="sxs-lookup"><span data-stu-id="82ac3-114">For more detail, refer to the <A href="https://technet.microsoft.com/library/jj219456(v=office.16).aspx">Office Online Server documentation</A>.</span></span>



</div>

<span data-ttu-id="82ac3-115">En este documento se tratan las siguientes áreas de temas:</span><span class="sxs-lookup"><span data-stu-id="82ac3-115">This document covers the following topic areas:</span></span>

  - [<span data-ttu-id="82ac3-116">Configuración de Lync Server 2013 para que funcione con Office Web Apps Server</span><span class="sxs-lookup"><span data-stu-id="82ac3-116">Configuring Lync Server 2013 to work with Office Web Apps Server</span></span>](lync-server-2013-configuring-lync-server-2013-to-work-with-office-web-apps-server.md)

  - [<span data-ttu-id="82ac3-117">Publicación de Office Web Apps Server en Lync Server 2013 con un servidor proxy inverso</span><span class="sxs-lookup"><span data-stu-id="82ac3-117">Publishing Office Web Apps Server in Lync Server 2013 using a reverse proxy server</span></span>](lync-server-2013-publishing-office-web-apps-server-using-a-reverse-proxy-server.md)

  - [<span data-ttu-id="82ac3-118">Validar la configuración de Office Web Apps Server en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="82ac3-118">Validating the configuration of Office Web Apps Server in Lync Server 2013</span></span>](lync-server-2013-validating-the-configuration-of-office-web-apps-server.md)

  - [<span data-ttu-id="82ac3-119">Configuración de clientes de Lync Server 2013 para su uso con Office Web Apps Server</span><span class="sxs-lookup"><span data-stu-id="82ac3-119">Configuring clients of Lync Server 2013 for use with Office Web Apps Server</span></span>](lync-server-2013-configuring-clients-for-use-with-office-web-apps-server.md)

<span data-ttu-id="82ac3-120"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="82ac3-120"></div>

<span> </span>

</div>

</div>

</span></span></div>

