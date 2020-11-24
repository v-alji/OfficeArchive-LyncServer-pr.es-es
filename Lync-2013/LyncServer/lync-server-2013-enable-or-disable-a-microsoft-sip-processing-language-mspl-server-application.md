---
title: 'Lync Server 2013: habilitar o deshabilitar una aplicación de servidor de Microsoft SIP Processing language (MSPL)'
description: 'Lync Server 2013: habilite o deshabilite una aplicación de servidor de Microsoft SIP Processing language (MSPL).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable a Microsoft SIP Processing Language (MSPL) server application
ms:assetid: b20af38d-224a-4459-991d-0b7eabb3ca7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182573(v=OCS.15)
ms:contentKeyID: 48185145
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8f919599d6c6a39fea73424f4e287f00636c0982
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398484"
---
# <a name="enable-or-disable-a-microsoft-sip-processing-language-mspl-server-application-in-lync-server-2013"></a><span data-ttu-id="0e3bb-103">Habilitar o deshabilitar una aplicación de servidor de Microsoft SIP Processing language (MSPL) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e3bb-103">Enable or disable a Microsoft SIP Processing Language (MSPL) server application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0e3bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0e3bb-104">

<span> </span></span></span>

<span data-ttu-id="0e3bb-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="0e3bb-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="0e3bb-106">Puede usar el panel de control de Lync Server para habilitar o deshabilitar aplicaciones de servidor de Microsoft SIP Processing language (MSPL) que se ejecutan en su entorno de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-106">You can use Lync Server Control Panel to enable or disable Microsoft SIP Processing Language (MSPL) server applications that run in your Lync Server 2013 environment.</span></span> <span data-ttu-id="0e3bb-107">Estas aplicaciones solo son aplicaciones de script que usan un lenguaje de scripting en lugar de la API de Microsoft Lync 2013 Preview.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-107">These applications are script-only applications that use a scripting language instead of the Microsoft Lync 2013 Preview API.</span></span>

<span data-ttu-id="0e3bb-108">No todos los scripts se pueden habilitar o deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-108">Not all scripts can be enabled or disabled.</span></span> <span data-ttu-id="0e3bb-109">Por ejemplo, el script DefaultRouting está habilitado y esta opción no se puede cambiar para DefaultRouting.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-109">For instance, the DefaultRouting script is enabled and this option cannot be changed for DefaultRouting.</span></span>

<div>

## <a name="to-enable-or-disable-an-mspl-server-application"></a><span data-ttu-id="0e3bb-110">Para habilitar o deshabilitar una aplicación de servidor MSPL</span><span class="sxs-lookup"><span data-stu-id="0e3bb-110">To enable or disable an MSPL server application</span></span>

1.  <span data-ttu-id="0e3bb-111">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o asignada al rol CsServerAdministrator o CsAdministrator, inicie sesión en cualquier equipo de la red en el que haya implementado Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="0e3bb-112">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0e3bb-113">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0e3bb-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0e3bb-114">En la barra de navegación izquierda, haga clic en **topología** y después haga clic en **aplicación de servidor**.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-114">In the left navigation bar, click **Topology** and then click **Server Application**.</span></span>

4.  <span data-ttu-id="0e3bb-115">En la página de la **aplicación servidor** , haga clic en un encabezado de columna para ordenar las aplicaciones, si es necesario, y, a continuación, haga clic en la aplicación de servidor que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-115">On the **Server Application** page, click a column heading to sort the applications, if needed, and then click the server application that you want to modify.</span></span>

5.  <span data-ttu-id="0e3bb-116">Haga clic en **acción**.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-116">Click **Action**.</span></span>

6.  <span data-ttu-id="0e3bb-117">Haga clic en **Habilitar aplicación** o **deshabilitar aplicación** (es decir, si el script admite esta opción).</span><span class="sxs-lookup"><span data-stu-id="0e3bb-117">Click **Enable application** or **Disable application** (that is, if the script supports this option).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0e3bb-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e3bb-118">See Also</span></span>


[<span data-ttu-id="0e3bb-119">Marcar una aplicación de Microsoft SIP Processing language (MSPL) como crítica o incrítica en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e3bb-119">Mark a Microsoft SIP Processing Language (MSPL) application as critical or not critical in Lync Server 2013</span></span>](lync-server-2013-mark-a-microsoft-sip-processing-language-mspl-application-as-critical-or-not-critical.md)  


[<span data-ttu-id="0e3bb-120">Ver las aplicaciones de servidor del lenguaje de procesamiento de SIP de Microsoft (MSPL) de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e3bb-120">View Microsoft SIP Processing Language (MSPL) server applications in Lync Server 2013</span></span>](lync-server-2013-view-microsoft-sip-processing-language-mspl-server-applications.md)  


[<span data-ttu-id="0e3bb-121">Administración de la topología de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e3bb-121">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="0e3bb-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0e3bb-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

