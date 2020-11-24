---
title: Cambiar las rutas de voz para usar el nuevo servidor de mediación de Lync Server 2013
description: Cambie las rutas de voz para usar el nuevo servidor de mediación de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Change voice routes to use the new Lync Server 2013 Mediation Server
ms:assetid: acd487b3-377c-46bf-9f71-fe6152002664
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205162(v=OCS.15)
ms:contentKeyID: 48185069
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef58ba61512b5de31a74b79e554dbb3f94b67d99
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398585"
---
# <a name="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server"></a><span data-ttu-id="55cbd-103">Cambiar las rutas de voz para usar el nuevo servidor de mediación de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="55cbd-103">Change voice routes to use the new Lync Server 2013 Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="55cbd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="55cbd-104">

<span> </span></span></span>

<span data-ttu-id="55cbd-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="55cbd-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="55cbd-106">En este procedimiento se cambian las rutas de voz para usar el servidor de mediación de Lync Server 2013, en lugar del servidor de mediación de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="55cbd-106">This procedure changes the voice routes to use the Lync Server 2013 Mediation Server, instead of the legacy Office Communications Server 2007 R2 Mediation Server.</span></span>

<div>

## <a name="to-change-the-voice-routes-to-use-the-new-mediation-server"></a><span data-ttu-id="55cbd-107">Para cambiar las rutas de voz para usar el nuevo servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="55cbd-107">To change the voice routes to use the new Mediation Server</span></span>

1.  <span data-ttu-id="55cbd-108">Panel de control de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="55cbd-108">Lync Server 2013 Control Panel</span></span>

2.  <span data-ttu-id="55cbd-109">En el panel izquierdo, seleccione **enrutamiento de voz** y, a continuación, **enrutar**.</span><span class="sxs-lookup"><span data-stu-id="55cbd-109">In the left pane, select **Voice Routing** and then **Route**.</span></span>

3.  <span data-ttu-id="55cbd-110">Haga clic en **nuevo** para crear una nueva ruta de voz.</span><span class="sxs-lookup"><span data-stu-id="55cbd-110">Click **New** to create a New Voice Route.</span></span>

4.  <span data-ttu-id="55cbd-111">Rellene los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="55cbd-111">Fill in the following fields:</span></span>
    
      - <span data-ttu-id="55cbd-112">**Nombre**: escriba un nombre descriptivo para la ruta de voz.</span><span class="sxs-lookup"><span data-stu-id="55cbd-112">**Name**: Type a descriptive name of the voice route.</span></span> <span data-ttu-id="55cbd-113">Para este documento, usaremos **W15PSTNRoute**.</span><span class="sxs-lookup"><span data-stu-id="55cbd-113">For this document we will use **W15PSTNRoute**.</span></span>
    
      - <span data-ttu-id="55cbd-114">**Descripción**: escriba una breve descripción de la ruta de voz.</span><span class="sxs-lookup"><span data-stu-id="55cbd-114">**Description**: Type a short description of the voice route.</span></span>

5.  <span data-ttu-id="55cbd-115">Omita todas las secciones restantes hasta que llegue **a las puertas de enlace asociadas**.</span><span class="sxs-lookup"><span data-stu-id="55cbd-115">Skip all remaining sections until you reach **Associated gateways**.</span></span> <span data-ttu-id="55cbd-116">Haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="55cbd-116">Click **Add**.</span></span> <span data-ttu-id="55cbd-117">Seleccione la nueva puerta de enlace predeterminada y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="55cbd-117">Select the new default gateway and click **OK**.</span></span>

6.  <span data-ttu-id="55cbd-118">En **usos de RTC asociados**, haga clic en **seleccionar**.</span><span class="sxs-lookup"><span data-stu-id="55cbd-118">Under **Associated PSTN Usages**, click **Select**.</span></span>

7.  <span data-ttu-id="55cbd-119">En la página **seleccionar registro de uso de RTC** , seleccione un nombre de registro y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="55cbd-119">From the **Select PSTN Usage Record** page, select a record name and then click **OK**.</span></span>

8.  <span data-ttu-id="55cbd-120">En la **nueva** página de la ruta de voz, haga clic en **Aceptar** para crear la **ruta de voz**.</span><span class="sxs-lookup"><span data-stu-id="55cbd-120">From the **New Voice Route** page, click **OK** to create the **Voice Route**.</span></span>

9.  <span data-ttu-id="55cbd-121">En la página de **enrutamiento de voz** , seleccione **enrutar**.</span><span class="sxs-lookup"><span data-stu-id="55cbd-121">From the **Voice Routing** page, select **Route**.</span></span>

10. <span data-ttu-id="55cbd-122">Mueva la ruta recién creada a la parte superior de la lista y, a continuación, seleccione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="55cbd-122">Move the newly created route to the top of the list and then select **Commit**.</span></span>

<span data-ttu-id="55cbd-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="55cbd-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

