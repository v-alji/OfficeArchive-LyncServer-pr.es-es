---
title: Configurar un nodo de monitor para que participe en la detección de System Center
description: Configurar un nodo de monitor para que participe en la detección de System Center.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to participate in System Center discovery
ms:assetid: 15c5dcfd-603b-47ea-af1b-8714c2ec08af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204704(v=OCS.15)
ms:contentKeyID: 48183500
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6a42ae77e0c8bde8b8e4de4461180ad00380a5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433474"
---
# <a name="configuring-a-watcher-node-in-lync-server-2013-to-participate-in-system-center-discovery"></a><span data-ttu-id="0634d-103">Configuración de un nodo de monitor en Lync Server 2013 para participar en la detección de System Center</span><span class="sxs-lookup"><span data-stu-id="0634d-103">Configuring a watcher node in Lync Server 2013 to participate in System Center discovery</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0634d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0634d-104">

<span> </span></span></span>

<span data-ttu-id="0634d-105">_**Última modificación del tema:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="0634d-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="0634d-106">Para asegurarse de que el nodo de monitor participe en el proceso de descubrimiento de System Center Operations Manager, debe completar el siguiente procedimiento en un equipo en el que se haya instalado la consola de System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="0634d-106">To make sure that your watcher node participates in the discovery process for System Center Operations Manager, you must complete the following procedure on a computer where the System Center Operations Manager console has been installed:</span></span>

1.  <span data-ttu-id="0634d-107">En la pestaña **Administración** , haga clic en **agente administrado**.</span><span class="sxs-lookup"><span data-stu-id="0634d-107">On the **Administration** tab, click **Agent Managed**.</span></span>

2.  <span data-ttu-id="0634d-108">Haga clic con el botón secundario en el nombre del equipo del nodo de monitor y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="0634d-108">Right-click the name of the watcher node computer, and then click **Properties**.</span></span> <span data-ttu-id="0634d-109">En el cuadro de diálogo **propiedades** , en la pestaña **seguridad** , seleccione **permitir que este agente actúe como proxy y descubrir objetos administrados en otros equipos** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0634d-109">In the **Properties** dialog box, on the **Security** tab, select **Allow this agent to act as a proxy and discover managed objects on other computers**, and then click **OK**.</span></span>

<span data-ttu-id="0634d-110">Después de configurar el nodo de monitor para que actúe como proxy, reinicie el equipo del nodo de monitor.</span><span class="sxs-lookup"><span data-stu-id="0634d-110">After configuring the watcher node to act as a proxy, reboot the watcher node computer.</span></span> <span data-ttu-id="0634d-111">Después de reiniciar el equipo, compruebe que no se graban eventos de error en el registro de eventos de Operations Manager de ese equipo.</span><span class="sxs-lookup"><span data-stu-id="0634d-111">After the computer has rebooted, verify that no error events are being recorded in the Operations Manager event log on that computer.</span></span> <span data-ttu-id="0634d-112">Una vez que el equipo se haya ejecutado durante 15 minutos o más, use la consola de Operations Manager para comprobar que los equipos de Lync Server aparecen en la categoría **Lync** .</span><span class="sxs-lookup"><span data-stu-id="0634d-112">After the computer has been running for 15 minutes or so, use the Operations Manager console to verify that your Lync Server computers are listed under the **Lync** category.</span></span>

<span data-ttu-id="0634d-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0634d-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

