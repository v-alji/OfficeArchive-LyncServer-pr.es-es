---
title: 'Lync Server 2013: configuración de las opciones de archivado en el nivel global'
description: 'Lync Server 2013: configuración de las opciones de archivado en el nivel global.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Archiving options at the global level
ms:assetid: bfe415f7-2abf-41ee-a1cb-cf48b2d59c0c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205233(v=OCS.15)
ms:contentKeyID: 48185303
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44b8939ec95d00afa2aa7632f4555bc6fef89834
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433342"
---
# <a name="configuring-archiving-options-at-the-global-level-in-lync-server-2013"></a><span data-ttu-id="5f3d7-103">Configurar las opciones de archivado en el nivel global de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f3d7-103">Configuring Archiving options at the global level in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f3d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f3d7-104">

<span> </span></span></span>

<span data-ttu-id="5f3d7-105">_**Última modificación del tema:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="5f3d7-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="5f3d7-106">Al agregar el archivado a la topología y publicar la topología, Lync Server crea una configuración global para el archivado.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-106">When you add Archiving to your topology and publish the topology, Lync Server creates a global configuration for Archiving.</span></span> <span data-ttu-id="5f3d7-107">De forma predeterminada, no se habilitan opciones de archivado en la configuración global.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-107">By default, no Archiving options are enabled in the global configuration.</span></span> <span data-ttu-id="5f3d7-108">La configuración global controla qué opciones se habilitan para toda la implementación, a menos que realice configuraciones de sitio o de grupo, que omiten la configuración global.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-108">The global configuration controls which options are enabled for your entire deployment, unless you set up site or pool configurations, which override the global configuration.</span></span>

<span data-ttu-id="5f3d7-109">Para obtener detalles sobre cómo funcionan las configuraciones de archivado, incluida la jerarquía para las configuraciones globales, de sitio y de grupo, consulte [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, la documentación de implementación o la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-109">For details about how Archiving configurations work, including the hierarchy for global, site, and pool configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5f3d7-110">Debe especificar todas las opciones apropiadas en las configuraciones de archivado antes de habilitar el archivado.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-110">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span>



</div>

<div>

## <a name="to-configure-archiving-options-at-the-global-level"></a><span data-ttu-id="5f3d7-111">Para configurar las opciones de archivado en el nivel global</span><span class="sxs-lookup"><span data-stu-id="5f3d7-111">To configure archiving options at the global level</span></span>

1.  <span data-ttu-id="5f3d7-112">Desde una cuenta de usuario que se asigne al rol CsArchivingAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-112">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5f3d7-113">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-113">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="5f3d7-114">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server 2013, consulte [abrir las herramientas administrativas de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5f3d7-114">For details about the different methods that you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5f3d7-115">En la barra de navegación izquierda, haga clic en **Supervisión y archivado** y, después, en **Configuración de archivado**.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="5f3d7-116">En la página **Configuración de archivado**, haga clic en **Global**, en **Editar** y, luego, en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-116">On the **Archiving Configuration** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="5f3d7-117">En **Editar configuración de archivado: global**, en la lista desplegable **Configuración de archivado**, seleccione una de las siguientes opciones de archivado:</span><span class="sxs-lookup"><span data-stu-id="5f3d7-117">In **Edit Archiving Setting - Global**, in the **Archiving setting** drop-down list, select one of the following archiving options:</span></span>
    
      - <span data-ttu-id="5f3d7-118">**Deshabilitar archivado**</span><span class="sxs-lookup"><span data-stu-id="5f3d7-118">**Disable archiving**</span></span>
    
      - <span data-ttu-id="5f3d7-119">**Archivar sesiones de mensajería instantánea (MI)**</span><span class="sxs-lookup"><span data-stu-id="5f3d7-119">**Archive IM sessions**</span></span>
    
      - <span data-ttu-id="5f3d7-120">**Archivar sesiones de mensajería instantánea (MI) y conferencias web**</span><span class="sxs-lookup"><span data-stu-id="5f3d7-120">**Archive IM and web conferencing sessions**</span></span>

6.  <span data-ttu-id="5f3d7-121">Además, en la página **Editar configuración de archivado: global**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5f3d7-121">Also on the **Edit Archiving Setting – Global** page, do the following:</span></span>
    
      - <span data-ttu-id="5f3d7-122">Para bloquear la actividad cuando el archivado no está disponible, active la casilla **Bloquear sesiones de mensajería instantánea (MI) o de conferencias web si no se pueden archivar**.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-122">To block activity when archiving is not available, select the **Block instant messaging (IM) or web conferencing sessions if archiving fails** check box.</span></span>
    
      - <span data-ttu-id="5f3d7-123">Para usar Microsoft Exchange Server para almacenar datos de archivado, haga clic en la casilla de verificación **integración con Microsoft Exchange** .</span><span class="sxs-lookup"><span data-stu-id="5f3d7-123">To use Microsoft Exchange Server to store archiving data, click the **Microsoft Exchange integration** check box.</span></span>
    
      - <span data-ttu-id="5f3d7-124">Para habilitar la purga de datos, active la casilla **Habilitar purgado de los datos de archivado** y realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="5f3d7-124">To enable data purging, select the **Enable purging of archiving data** check box, and then do one of the following:</span></span>
        
          - <span data-ttu-id="5f3d7-125">Para especificar la purga al transcurrir una cantidad de días determinada, haga clic en **Purgar los datos de archivado exportados y los datos de archivado almacenados tras la duración máxima (días)** y especifique la cantidad de días.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-125">To specify purging after a specific number of days, click **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="5f3d7-126">Para limitar la purga de los datos de archivado que se han exportado, haga clic en **Purgar solo datos de archivado exportados**.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-126">To limit purging to archiving data that has been exported, click **Purge exported archiving data only**.</span></span>

7.  <span data-ttu-id="5f3d7-127">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="5f3d7-127">Click **Commit**.</span></span>

<span data-ttu-id="5f3d7-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f3d7-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

