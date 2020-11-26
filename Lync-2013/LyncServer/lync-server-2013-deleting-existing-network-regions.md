---
title: 'Lync Server 2013: eliminar regiones de red existentes'
description: 'Lync Server 2013: eliminar regiones de red existentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting existing network regions
ms:assetid: c7293a2f-2b49-4c4a-903f-f7edcea2bc5f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721882(v=OCS.15)
ms:contentKeyID: 49733815
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b148f0bd92ad398ab7057a5a291bf3245df3e47e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430325"
---
# <a name="deleting-existing-network-regions-in-lync-server-2013"></a><span data-ttu-id="ae938-103">Eliminar regiones de red existentes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae938-103">Deleting existing network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae938-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae938-104">

<span> </span></span></span>

<span data-ttu-id="ae938-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ae938-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ae938-106">Una región de red interconecta varias partes de una red en varias áreas geográficas.</span><span class="sxs-lookup"><span data-stu-id="ae938-106">A network region interconnects various parts of a network across multiple geographic areas.</span></span> <span data-ttu-id="ae938-107">Cada región de la red debe estar asociada con un sitio central.</span><span class="sxs-lookup"><span data-stu-id="ae938-107">Every network region must be associated with a central site.</span></span> <span data-ttu-id="ae938-108">El sitio central es el sitio del centro de datos en el que se está ejecutando el servicio de directivas de ancho de banda de control de admisión de llamadas (CAC).</span><span class="sxs-lookup"><span data-stu-id="ae938-108">The central site is the data center site on which the call admission control (CAC) bandwidth policy service is running.</span></span> <span data-ttu-id="ae938-109">Puede usar el panel de control de Lync Server para configurar regiones de red.</span><span class="sxs-lookup"><span data-stu-id="ae938-109">You can use Lync Server Control Panel to configure network regions.</span></span> <span data-ttu-id="ae938-110">Las regiones de red incluyen opciones que determinan si se permiten rutas alternativas a través de Internet para conexiones de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae938-110">Network regions include settings that determine whether alternate paths through the Internet are allowed for audio and video connections.</span></span> <span data-ttu-id="ae938-111">En el panel de control de Lync Server, puede crear, modificar o eliminar una región de red.</span><span class="sxs-lookup"><span data-stu-id="ae938-111">From the Lync Server Control Panel, you can create, modify, or delete a network region.</span></span> <span data-ttu-id="ae938-112">Use este tema para eliminar regiones de red existentes.</span><span class="sxs-lookup"><span data-stu-id="ae938-112">Use this topic to delete existing network regions.</span></span> <span data-ttu-id="ae938-113">Para obtener detalles sobre cómo crear o modificar regiones de red existentes, vea [crear o modificar regiones de red en Lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span><span class="sxs-lookup"><span data-stu-id="ae938-113">For details about creating or modifying existing network regions, see [Creating or modifying network regions in Lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span></span>

<div>

## <a name="to-delete-a-network-region"></a><span data-ttu-id="ae938-114">Para eliminar una región de red</span><span class="sxs-lookup"><span data-stu-id="ae938-114">To delete a network region</span></span>

1.  <span data-ttu-id="ae938-115">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="ae938-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ae938-116">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ae938-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ae938-117">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ae938-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ae938-118">En la barra de navegación izquierda, haga clic en **configuración de red** y, después, en **región**.</span><span class="sxs-lookup"><span data-stu-id="ae938-118">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="ae938-119">En la página **región** , haga clic en la región que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="ae938-119">On the **Region** page, click the region you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ae938-120">Puedes eliminar más de una región a la vez.</span><span class="sxs-lookup"><span data-stu-id="ae938-120">You can delete more than one region at a time.</span></span> <span data-ttu-id="ae938-121">Para ello, presione CTRL y seleccione varias regiones mientras mantiene presionada la tecla CTRL.</span><span class="sxs-lookup"><span data-stu-id="ae938-121">To do this, press CTRL and select multiple regions while holding down the CTRL key.</span></span> <span data-ttu-id="ae938-122">O bien, para seleccionar todas las regiones, haga clic en <STRONG>seleccionar todo</STRONG> en el menú <STRONG>edición</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ae938-122">Or, to select all regions, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="ae938-123">En el menú **Editar** , haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="ae938-123">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="ae938-124">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ae938-124">Click **OK**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="ae938-125">No se puede quitar una región de red si está asociada a un sitio de red.</span><span class="sxs-lookup"><span data-stu-id="ae938-125">A network region cannot be removed if it is associated with a network site.</span></span> <span data-ttu-id="ae938-126">Si intenta quitar una región asociada a un sitio, recibirá un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="ae938-126">If you attempt to remove a region associated with a site you will receive an error message.</span></span> <span data-ttu-id="ae938-127">Para ver si una región está asociada a algún sitio, seleccione la región y, a continuación, haga clic en <STRONG>Mostrar detalles</STRONG> en el menú <STRONG>edición</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ae938-127">To see if a region is associated with any sites, select the region and then click <STRONG>Show details</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ae938-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae938-128">See Also</span></span>


[<span data-ttu-id="ae938-129">Crear o modificar regiones de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae938-129">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)  
  

<span data-ttu-id="ae938-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae938-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

