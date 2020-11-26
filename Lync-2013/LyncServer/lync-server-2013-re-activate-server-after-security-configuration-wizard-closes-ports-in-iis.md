---
title: Volver a activar el servidor después de que el Asistente para la configuración de la seguridad cierre los puertos en IIS
description: Reactivar servidor después de que el Asistente para configuración de seguridad cierre los puertos en IIS.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Re-activate server after Security Configuration Wizard closes ports in IIS
ms:assetid: cb8e17cf-f8c1-4099-b63b-c242d656c26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398851(v=OCS.15)
ms:contentKeyID: 48185644
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d824845a7f89c28087a7b5d180a6ed017cb47ade
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436723"
---
# <a name="re-activate-server-after-security-configuration-wizard-closes-ports-in-iis"></a><span data-ttu-id="b8b30-103">Volver a activar el servidor después de que el Asistente para la configuración de la seguridad cierre los puertos en IIS</span><span class="sxs-lookup"><span data-stu-id="b8b30-103">Re-activate server after Security Configuration Wizard closes ports in IIS</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8b30-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8b30-104">

<span> </span></span></span>

<span data-ttu-id="b8b30-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="b8b30-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="b8b30-106">Algunas funciones de Lync Server 2013 ejecutan servicios web en el puerto 4443 de Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="b8b30-106">Some Lync Server 2013 roles run Web Services on Internet Information Services (IIS) port 4443.</span></span> <span data-ttu-id="b8b30-107">Al ejecutar el Asistente para la implementación de Lync Server, Bootstrapper.exe o mediante el cmdlet **enable-CsComputer** se crea una excepción en el firewall y se abre el puerto.</span><span class="sxs-lookup"><span data-stu-id="b8b30-107">Running the Lync Server Deployment Wizard, Bootstrapper.exe, or using the **Enable-CsComputer** cmdlet creates an exception in the firewall and opens the port.</span></span> <span data-ttu-id="b8b30-108">Si, a continuación, ejecuta el Asistente para la configuración de seguridad de Windows Server 2008 R2 (u otros scripts de refuerzo), el puerto 4443 se bloqueará y los clientes externos no podrán comunicarse con los servicios Web.</span><span class="sxs-lookup"><span data-stu-id="b8b30-108">If you then run the Windows Server 2008 R2 Security Configuration Wizard (or other hardening scripts), port 4443 will be blocked, and external clients will not be able to contact Web Services.</span></span> <span data-ttu-id="b8b30-109">Para volver a abrir el puerto, puede modificar la excepción del firewall directamente o reactivar el servidor.</span><span class="sxs-lookup"><span data-stu-id="b8b30-109">To reopen the port you can either modify the firewall exception directly or re-activate the server.</span></span>

<div>

## <a name="to-re-activate-the-server-by-using-the-deployment-wizard"></a><span data-ttu-id="b8b30-110">Para volver a activar el servidor mediante el Asistente para la implementación</span><span class="sxs-lookup"><span data-stu-id="b8b30-110">To re-activate the server by using the Deployment Wizard</span></span>

1.  <span data-ttu-id="b8b30-111">En la página Asistente para la implementación de Lync Server, haga clic en **Ejecutar** junto al **paso 2: configurar o quitar los componentes de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="b8b30-111">On the Lync Server Deployment Wizard page, click **Run** next to **Step 2: Setup or Remove Lync Server Components**.</span></span>

2.  <span data-ttu-id="b8b30-112">En la página **configuración de los componentes de Lync Server** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b8b30-112">On **Setup Lync Server components** page, click **Next**.</span></span>

3.  <span data-ttu-id="b8b30-113">En la página **comandos en ejecución** , cuando el estado de la tarea se muestre como completado, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="b8b30-113">On the **Executing Commands** page, when the task status is shown as completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="b8b30-114">También puede usar bootstrapper.exe o <STRONG>enable-CsComputer</STRONG> para volver a activar el servidor.</span><span class="sxs-lookup"><span data-stu-id="b8b30-114">You can also use bootstrapper.exe or <STRONG>Enable-CsComputer</STRONG> to re-activate the server.</span></span>

    
    <span data-ttu-id="b8b30-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8b30-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

