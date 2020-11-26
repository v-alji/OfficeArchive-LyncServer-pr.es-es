---
title: Configurar el equipo de Lync Server para que participe en la detección de System Center
description: Configurar el equipo de Lync Server para que participe en la detección de System Center.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the Lync Server computer to participate in System Center discovery
ms:assetid: 2f9c9cb0-3120-4571-9cd2-657c2123fe21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204776(v=OCS.15)
ms:contentKeyID: 48183731
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44d25ba3de673084b2e64e17790a2776cbe57f07
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432565"
---
# <a name="configuring-the-lync-server-2013-computer-to-participate-in-system-center-discovery"></a><span data-ttu-id="7ad70-103">Configurar el equipo de Lync Server 2013 para que participe en la detección de System Center</span><span class="sxs-lookup"><span data-stu-id="7ad70-103">Configuring the Lync Server 2013 computer to participate in System Center discovery</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ad70-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ad70-104">

<span> </span></span></span>

<span data-ttu-id="7ad70-105">_**Última modificación del tema:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="7ad70-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="7ad70-106">Para asegurarse de que el nuevo agente de Lync Server participa en el proceso de detección de System Center Operations Manager, debe completar el siguiente procedimiento en cada equipo en el que se haya instalado la consola de System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="7ad70-106">To make sure that your new Lync Server agent participates in discovery process for System Center Operations Manager, you must complete the following procedure on each computer where the System Center Operations Manager console has been installed:</span></span>

1.  <span data-ttu-id="7ad70-107">En la pestaña **Administración** , haga clic en **agente administrado**.</span><span class="sxs-lookup"><span data-stu-id="7ad70-107">On the **Administration** tab, click **Agent Managed**.</span></span>

2.  <span data-ttu-id="7ad70-108">Haga clic con el botón secundario en el nombre del equipo y, a continuación, haga clic en **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="7ad70-108">Right-click the name of the computer, and then click **Properties**.</span></span> <span data-ttu-id="7ad70-109">En el cuadro de diálogo **propiedades** , en la pestaña **seguridad** , seleccione **permitir que este agente actúe como proxy y descubrir objetos administrados en otros equipos** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7ad70-109">In the **Properties** dialog box, on the **Security** tab, select **Allow this agent to act as a proxy and discover managed objects on other computers**, and then click **OK**.</span></span>

<span data-ttu-id="7ad70-110">Después de completar el paso 2, reinicie el servicio del agente de estado.</span><span class="sxs-lookup"><span data-stu-id="7ad70-110">After completing step 2, reboot the Health Agent service.</span></span> <span data-ttu-id="7ad70-111">(Si reinicia el servicio, "forzará" el descubrimiento de la nueva máquina.</span><span class="sxs-lookup"><span data-stu-id="7ad70-111">(Rebooting the service will “force” discovery of the new machine.</span></span> <span data-ttu-id="7ad70-112">Si no reinicia el servicio, puede demorar hasta 4 horas antes de que System Center Operations Manager Descubra la nueva máquina.).</span><span class="sxs-lookup"><span data-stu-id="7ad70-112">If you do not reboot the service, it could take as long as 4 hours before the new machine is discovered by System Center Operations Manager.).</span></span> <span data-ttu-id="7ad70-113">Después de que el servicio se haya reiniciado, compruebe que no se graban eventos de error en el registro de eventos de Operations Manager de ese equipo.</span><span class="sxs-lookup"><span data-stu-id="7ad70-113">After the service has rebooted, verify that no error events are being recorded in the Operations Manager event log on that computer.</span></span>

<span data-ttu-id="7ad70-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ad70-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

