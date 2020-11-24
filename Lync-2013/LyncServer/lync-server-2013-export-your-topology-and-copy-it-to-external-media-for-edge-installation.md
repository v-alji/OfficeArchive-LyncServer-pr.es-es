---
title: Exportar la topología y copiarla en un medio externo para la instalación perimetral
description: Exporte su topología y cópiela en medios externos para la instalación perimetral.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export your topology and copy it to external media for edge installation
ms:assetid: def9f416-c519-4a72-b242-7d3057d9c1fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398983(v=OCS.15)
ms:contentKeyID: 48185615
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47fcee032b4c0e667455ae7f35afe8b99c2d12cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397883"
---
# <a name="export-your-lync-server-2013-topology-and-copy-it-to-external-media-for-edge-installation"></a><span data-ttu-id="fd95f-103">Exportar la topología de Lync Server 2013 y copiarla en un medio externo para la instalación perimetral</span><span class="sxs-lookup"><span data-stu-id="fd95f-103">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd95f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd95f-104">

<span> </span></span></span>

<span data-ttu-id="fd95f-105">_**Última modificación del tema:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="fd95f-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="fd95f-106">Después de publicar su topología, el Asistente para la implementación de Lync Server necesita acceso a los datos del almacén central de administración para iniciar el proceso de implementación en el servidor.</span><span class="sxs-lookup"><span data-stu-id="fd95f-106">After you publish your topology, the Lync Server Deployment Wizard needs access to the Central Management store data in order to start the deployment process on the server.</span></span> <span data-ttu-id="fd95f-107">En la red interna, los datos están disponibles directamente desde los servidores, pero los servidores perimetrales que no se encuentran en el dominio interno no tienen acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="fd95f-107">In the internal network, the data is available directly from the servers, but Edge Servers that are not in the internal domain cannot access the data.</span></span> <span data-ttu-id="fd95f-108">Para que los datos de configuración de topología estén disponibles para una implementación de servidor perimetral, debe exportar los datos de la topología a un archivo y copiarlos en medios externos (por ejemplo, una unidad USB o un recurso compartido de red que esté disponible desde el servidor perimetral) antes de ejecutar el Asistente para la implementación de Lync Server en el servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="fd95f-108">To make the topology configuration data available for an Edge Server deployment, you must export the topology data to a file and copy it to external media (for example, a USB drive or a network share that is available from the Edge Server) before you run the Lync Server Deployment Wizard on the Edge Server.</span></span> <span data-ttu-id="fd95f-109">Use el siguiente procedimiento para que los datos de configuración de su topología estén disponibles en el servidor perimetral que va a implementar.</span><span class="sxs-lookup"><span data-stu-id="fd95f-109">Use the following procedure to make your topology configuration data available on the Edge Server that you are deploying.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="fd95f-110">Después de instalar Lync Server 2013 en un servidor perimetral, administra el servidor perimetral con las herramientas administrativas de la red interna, que automáticamente replican la configuración en los servidores perimetrales de la implementación.</span><span class="sxs-lookup"><span data-stu-id="fd95f-110">After you install Lync Server 2013 on an Edge Server, you manage the Edge Server using the administrative tools in the internal network, which automatically replicate configuration to any Edge Servers in your deployment.</span></span> <span data-ttu-id="fd95f-111">La única excepción es asignar e instalar certificados e detener e iniciar servicios, ambos deben realizarse en el servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="fd95f-111">The only exception is assigning and installing certificates and stopping and starting services, both of which must be done on the Edge Server.</span></span>



</div>

<div>

## <a name="to-make-your-topology-data-available-on-an-edge-server-by-using-lync-server-management-shell"></a><span data-ttu-id="fd95f-112">Para hacer que los datos de su topología estén disponibles en un servidor perimetral mediante el shell de administración de Lync Server</span><span class="sxs-lookup"><span data-stu-id="fd95f-112">To make your topology data available on an Edge Server by using Lync Server Management Shell</span></span>

1.  <span data-ttu-id="fd95f-113">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="fd95f-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="fd95f-114">En el shell de administración de Lync Server, ejecute el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fd95f-114">In the Lync Server Management Shell, run the following cmdlet:</span></span>
    
        Export-CsConfiguration -FileName <ConfigurationFilePath.zip>

3.  <span data-ttu-id="fd95f-115">Copie el archivo exportado a un medio externo (por ejemplo, una unidad USB o un recurso compartido de red que esté disponible desde el servidor perimetral durante la implementación).</span><span class="sxs-lookup"><span data-stu-id="fd95f-115">Copy the exported file to external media (for example, a USB drive or a network share that is available from the Edge Server during deployment).</span></span>

<span data-ttu-id="fd95f-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd95f-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

