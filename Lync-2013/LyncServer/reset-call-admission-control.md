---
title: Restablecer el control de admisión de llamadas
description: Restablece el control de admisión de llamadas.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Reset call admission control
ms:assetid: 5873f56c-f3d6-4d73-beea-c9f37d5077f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688064(v=OCS.15)
ms:contentKeyID: 49733658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4539cda453de6249be3a9b9b61521ecf478cb70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443625"
---
# <a name="reset-call-admission-control"></a><span data-ttu-id="d1c1a-103">Restablecer el control de admisión de llamadas</span><span class="sxs-lookup"><span data-stu-id="d1c1a-103">Reset call admission control</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d1c1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d1c1a-104">

<span> </span></span></span>

<span data-ttu-id="d1c1a-105">_**Última modificación del tema:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="d1c1a-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="d1c1a-106">Si un grupo de aplicaciones para el usuario de Lync Server 2010 hospeda control de admisión de llamadas (CAC), debe mover el alojamiento de hospedaje de CAC a un grupo de servidores de Lync 2013 antes de poder quitar el grupo de aplicaciones para usuario de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d1c1a-106">If a Lync Server 2010 Front End pool is hosting call admission control (CAC), you must move CAC hosting to a Lync Server 2013 pool before you can remove the Lync Server 2010 Front End pool.</span></span>

<div>

## <a name="to-reset-cac"></a><span data-ttu-id="d1c1a-107">Para restablecer CAC</span><span class="sxs-lookup"><span data-stu-id="d1c1a-107">To reset CAC</span></span>

1.  <span data-ttu-id="d1c1a-108">Abra el generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="d1c1a-108">Open Topology Builder.</span></span>

2.  <span data-ttu-id="d1c1a-109">Haga clic con el botón secundario en el nodo del sitio y haga clic en **Editar propiedades**.</span><span class="sxs-lookup"><span data-stu-id="d1c1a-109">Right-click the site node, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="d1c1a-110">En **configuración de control de admisión de llamadas**, asegúrese de que **Habilitar control de admisión de llamadas** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d1c1a-110">Under **Call Admission Control setting**, make sure **Enable Call Admission Control** is selected.</span></span>

4.  <span data-ttu-id="d1c1a-111">En **grupo de servidores front-end para ejecutar el controlador de admisión de llamadas (CAC)**, seleccione el grupo de 2013 de Lync Server que hospedará CAC y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d1c1a-111">Under **Front End pool to run call admission control (CAC)**, select the Lync Server 2013 pool that is to host CAC, and then click **OK**.</span></span>

5.  <span data-ttu-id="d1c1a-112">Publique la topología.</span><span class="sxs-lookup"><span data-stu-id="d1c1a-112">Publish the topology.</span></span>

<span data-ttu-id="d1c1a-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d1c1a-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

