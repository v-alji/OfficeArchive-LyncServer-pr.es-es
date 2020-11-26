---
title: 'Lync Server 2013: Configuración de la mensajería unificada en Microsoft Exchange Server para trabajar con Lync Server 2013'
description: 'Lync Server 2013: configuración de mensajería unificada en Microsoft Exchange Server para que funcione con Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Unified Messaging on Microsoft Exchange Server to work with Lync Server 2013
ms:assetid: 058da9c4-23af-4ddb-9f63-70133a8aafc6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398106(v=OCS.15)
ms:contentKeyID: 48183289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 53c303f0ae659536aafcbdfcd829ed236e35a0ba
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432432"
---
# <a name="configuring-unified-messaging-on-microsoft-exchange-server-to-work-with-lync-server-2013"></a><span data-ttu-id="a3748-103">Configuración de la mensajería unificada en Microsoft Exchange Server para trabajar con Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3748-103">Configuring Unified Messaging on Microsoft Exchange Server to work with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3748-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3748-104">

<span> </span></span></span>

<span data-ttu-id="a3748-105">_**Última modificación del tema:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="a3748-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a3748-106">Si desea usar la mensajería unificada de Exchange (UM) para proporcionar contestador automático, Outlook Voice Access o los servicios de operador automático para usuarios de Enterprise Voice, consulte <A href="lync-server-2013-planning-for-exchange-unified-messaging-integration.md">planificación de la integración de mensajería unificada de Exchange en Lync Server 2013</A> en la documentación de planeación y, a continuación, siga las instrucciones de esta sección.</span><span class="sxs-lookup"><span data-stu-id="a3748-106">If you want to use Exchange Unified Messaging (UM) to provide call answering, Outlook Voice Access, or auto-attendant services for Enterprise Voice users, read <A href="lync-server-2013-planning-for-exchange-unified-messaging-integration.md">Planning for Exchange Unified Messaging integration in Lync Server 2013</A> in the Planning documentation, and then follow the instructions in this section.</span></span>



</div>

<span data-ttu-id="a3748-107">Para configurar la mensajería unificada de Exchange para que funcione con la telefonía IP empresarial, tendrá que realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="a3748-107">To configure Exchange Unified Messaging (UM) to work with Enterprise Voice, you’ll need to perform the following tasks:</span></span>

  - <span data-ttu-id="a3748-108">Configurar certificados en el servidor que ejecuta los servicios de mensajería unificada (UM) de Exchange</span><span class="sxs-lookup"><span data-stu-id="a3748-108">Configure certificates on the server running Exchange Unified Messaging (UM) services</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a3748-109">Agregar todos los servidores de acceso de cliente y de buzón a todos los planes de marcado URI SIP de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="a3748-109">Add all Client Access and Mailbox servers to all UM SIP URI dial plans.</span></span> <span data-ttu-id="a3748-110">Si no es así, el enrutamiento de llamadas salientes no funciona según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="a3748-110">If not, outbound call routing won’t work as expected.</span></span>

    
    </div>

  - <span data-ttu-id="a3748-111">Cree uno o varios planes de marcado URI SIP de MU, junto con los números de teléfono de acceso del suscriptor, según sea necesario y, a continuación, cree los planes de marcado de Lync Server correspondientes.</span><span class="sxs-lookup"><span data-stu-id="a3748-111">Create one or more UM SIP URI dial plans, along with the subscriber access phone numbers, as needed, and then create corresponding Lync Server dial plans.</span></span>

  - <span data-ttu-id="a3748-112">Use el script de **exchucutil.ps1** para:</span><span class="sxs-lookup"><span data-stu-id="a3748-112">Use the **exchucutil.ps1** script to:</span></span>
    
      - <span data-ttu-id="a3748-113">Crear puertas de enlace IP de MU.</span><span class="sxs-lookup"><span data-stu-id="a3748-113">Create UM IP gateways.</span></span>
    
      - <span data-ttu-id="a3748-114">Crear grupos de extensiones de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="a3748-114">Create UM hunt groups.</span></span>
    
      - <span data-ttu-id="a3748-115">Otorgue a Lync Server 2013 permiso para leer objetos de servicios de dominio de Active Directory de MU.</span><span class="sxs-lookup"><span data-stu-id="a3748-115">Grant Lync Server 2013 permission to read UM Active Directory Domain Services objects.</span></span>

  - <span data-ttu-id="a3748-116">Crear un objeto de operador automático de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="a3748-116">Create a UM auto-attendant object.</span></span>

  - <span data-ttu-id="a3748-117">Crear un objeto de acceso de suscriptor.</span><span class="sxs-lookup"><span data-stu-id="a3748-117">Create a subscriber access object.</span></span>

  - <span data-ttu-id="a3748-118">Crear un URI de SIP para cada usuario y asociar a los usuarios con un plan de marcado URI SIP de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="a3748-118">Create a SIP URI for each user and associating users with a UM SIP URI dial plan.</span></span>

<div>

## <a name="requirements-and-recommendations"></a><span data-ttu-id="a3748-119">Requisitos y recomendaciones</span><span class="sxs-lookup"><span data-stu-id="a3748-119">Requirements and Recommendations</span></span>

<span data-ttu-id="a3748-120">Antes de empezar, en la documentación de esta sección se supone que ha implementado los siguientes roles de Exchange 2013: acceso de cliente y buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a3748-120">Before you begin, the documentation in this section assumes that you have deployed the following Exchange 2013 roles: Client Access and Mailbox.</span></span> <span data-ttu-id="a3748-121">En Microsoft Exchange Server 2013, la mensajería unificada de Exchange se ejecuta como un servicio en estos servidores.</span><span class="sxs-lookup"><span data-stu-id="a3748-121">In Microsoft Exchange Server 2013, Exchange UM runs as a service on these servers.</span></span>

<span data-ttu-id="a3748-122">Para obtener más información sobre la implementación de Exchange 2013, consulte la biblioteca de TechNet de Exchange 2013 en [https://go.microsoft.com/fwlink/p/?LinkId=266637](https://go.microsoft.com/fwlink/p/?linkid=266637)</span><span class="sxs-lookup"><span data-stu-id="a3748-122">For details about deploying Exchange 2013, see the Exchange 2013 TechNet Library at [https://go.microsoft.com/fwlink/p/?LinkId=266637](https://go.microsoft.com/fwlink/p/?linkid=266637)</span></span>

<span data-ttu-id="a3748-123">Además, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a3748-123">Also note the following:</span></span>

  - <span data-ttu-id="a3748-124">Si la mensajería unificada de Exchange se instala en varios bosques, los pasos de integración del servidor de Exchange deben realizarse para cada bosque de MU.</span><span class="sxs-lookup"><span data-stu-id="a3748-124">If Exchange UM is installed in multiple forests, the Exchange Server integration steps must be performed for each UM forest.</span></span> <span data-ttu-id="a3748-125">Además, cada bosque de MU debe estar configurado para confiar en el bosque en el que se implementa Lync Server 2013, y el bosque en el que se implementa Lync Server 2013 debe estar configurado para confiar en cada bosque de MU.</span><span class="sxs-lookup"><span data-stu-id="a3748-125">In addition, each UM forest must be configured to trust the forest in which Lync Server 2013 is deployed, and the forest in which Lync Server 2013 is deployed must be configured to trust each UM forest.</span></span>

  - <span data-ttu-id="a3748-126">Los pasos de integración se realizan en las funciones de Exchange Server donde se ejecutan los servicios de mensajería unificada y en el servidor que ejecuta Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a3748-126">Integration steps are performed on both the Exchange Server roles where Unified Messaging services are running, and on the server running Lync Server 2013.</span></span> <span data-ttu-id="a3748-127">Debe realizar los pasos de integración de mensajería unificada de Exchange Server antes de realizar los pasos de integración de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a3748-127">You should perform the Exchange Server Unified Messaging integration steps before you perform the Lync Server 2013 integration steps.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a3748-128">Para ver qué pasos de integración se realizan en qué servidores y con qué roles de administrador, vea <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">proceso de implementación para integrar mensajería unificada local y Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a3748-128">To see which integration steps are performed on which servers and by which administrator roles, see <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</A>.</span></span>

    
    </div>

<span data-ttu-id="a3748-129">Las siguientes herramientas deben estar disponibles en cada servidor que ejecute la mensajería unificada de Exchange:</span><span class="sxs-lookup"><span data-stu-id="a3748-129">The following tools must be available on each server running Exchange UM:</span></span>

  - <span data-ttu-id="a3748-130">Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="a3748-130">Exchange Management Shell</span></span>

  - <span data-ttu-id="a3748-131">El script **exchucutil.ps1**, que realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="a3748-131">The script **exchucutil.ps1**, which performs the following tasks:</span></span>
    
      - <span data-ttu-id="a3748-132">Crea una puerta de enlace IP de MU para cada servidor de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="a3748-132">Creates a UM IP gateway for each Lync Server 2013.</span></span>
    
      - <span data-ttu-id="a3748-133">Crea un grupo de captura para cada puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="a3748-133">Creates a hunt group for each gateway.</span></span> <span data-ttu-id="a3748-134">El identificador piloto de cada grupo de captura especifica el plan de marcado URI SIP de MU usado por el grupo de servidores front-end o el servidor Standard Edition asociado a la puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="a3748-134">The pilot identifier of each hunt group specifies the UM SIP URI dial plan used by the Front End pool or Standard Edition server that is associated with the gateway.</span></span>
    
      - <span data-ttu-id="a3748-135">Concede el permiso 2013 de Lync Server para leer objetos de mensajería unificada de Exchange en servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a3748-135">Grants Lync Server 2013 permission to read Exchange UM objects in Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a3748-136">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a3748-136">In This Section</span></span>

  - [<span data-ttu-id="a3748-137">Configurar certificados en el servidor que ejecuta la mensajería unificada de Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="a3748-137">Configure certificates on the server running Microsoft Exchange Server Unified Messaging</span></span>](lync-server-2013-configure-certificates-on-the-server-running-microsoft-exchange-server-unified-messaging.md)

  - [<span data-ttu-id="a3748-138">Configurar la mensajería unificada en Microsoft Exchange para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3748-138">Configure Unified Messaging on Microsoft Exchange for Lync Server 2013</span></span>](lync-server-2013-configure-unified-messaging-on-microsoft-exchange.md)

<span data-ttu-id="a3748-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3748-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

