---
title: 'Lync Server 2013: habilitar o deshabilitar las conferencias de acceso telefónico local para reuniones'
description: 'Lync Server 2013: habilitar o deshabilitar las conferencias de acceso telefónico local para reuniones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable dial-in conferencing for meetings
ms:assetid: 418dcf2d-c8d6-4b2c-b1ab-8723c7ef53e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688036(v=OCS.15)
ms:contentKeyID: 49733627
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3caa7b8cee14ca8471e7b7e42af7f7398e3b6c2d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437556"
---
# <a name="enable-or-disable-dial-in-conferencing-for-meetings-in-lync-server-2013"></a><span data-ttu-id="fcd6f-103">Habilitar o deshabilitar las conferencias de acceso telefónico local para reuniones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fcd6f-103">Enable or disable dial-in conferencing for meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fcd6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fcd6f-104">

<span> </span></span></span>

<span data-ttu-id="fcd6f-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="fcd6f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="fcd6f-106">En el procedimiento siguiente se describe cómo permitir que el usuario se una a una reunión con acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="fcd6f-106">The following procedure describes how to allow user to join a meeting using dial-in.</span></span>

<div>

## <a name="to-enable-or-disable-dial-in-conferencing"></a><span data-ttu-id="fcd6f-107">Para habilitar o deshabilitar las conferencias de acceso telefónico local</span><span class="sxs-lookup"><span data-stu-id="fcd6f-107">To enable or disable dial-in conferencing</span></span>

1.  <span data-ttu-id="fcd6f-108">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="fcd6f-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fcd6f-109">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fcd6f-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="fcd6f-110">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="fcd6f-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="fcd6f-111">En la barra de navegación izquierda, haga clic en **Conferencia** y, a continuación, en **Directiva de conferencia**.</span><span class="sxs-lookup"><span data-stu-id="fcd6f-111">In the left navigation bar, click **Conferencing** and then click **Conferencing Policy**.</span></span>

4.  <span data-ttu-id="fcd6f-112">En la lista de directivas de conferencia, seleccione la directiva para la que desea habilitar la conferencia de acceso telefónico local, haga clic en **Editar** y luego en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="fcd6f-112">In the list of conferencing policies, select the policy for which you want to enable dial-in conferencing, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="fcd6f-p102">Para permitir que los usuarios se unan a la reunión con acceso telefónico local, active la casilla **Habilitar conferencia de acceso telefónico local por RTC**. De forma predeterminada, los usuarios pueden acceder telefónicamente a las reuniones con la red telefónica conmutada (RTC).</span><span class="sxs-lookup"><span data-stu-id="fcd6f-p102">To allow users to join meeting by dialing in, check the **Enable PSTN dial-in conferencing** check box. By default, users can dial in to meetings by using the public switched telephone network (PSTN).</span></span>

6.  <span data-ttu-id="fcd6f-115">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="fcd6f-115">Click **Commit**.</span></span>

<span data-ttu-id="fcd6f-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fcd6f-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

