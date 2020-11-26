---
title: 'Lync Server 2013: deshabilitar la omisión de medios de red'
description: 'Lync Server 2013: deshabilitar la omisión de medios de red.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disabling network media bypass
ms:assetid: 936d2678-d712-4589-b172-b5793013652f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688141(v=OCS.15)
ms:contentKeyID: 49733741
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1472711417218aa87936a3ccabe1bb465dd07c20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429101"
---
# <a name="disabling-network-media-bypass-in-lync-server-2013"></a><span data-ttu-id="47c26-103">Deshabilitar la omisión de medios de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47c26-103">Disabling network media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47c26-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47c26-104">

<span> </span></span></span>

<span data-ttu-id="47c26-105">_**Última modificación del tema:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="47c26-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="47c26-106">La configuración de omisión de medios se aplica globalmente en una implementación de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="47c26-106">Media bypass settings apply globally across a Microsoft Lync Server 2013 deployment.</span></span> <span data-ttu-id="47c26-107">La omisión de medios permite que las llamadas omitan el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="47c26-107">Media bypass allows calls to bypass the Mediation Server.</span></span> <span data-ttu-id="47c26-108">Para obtener información sobre Cuándo usar la omisión de medios, consulte [planificación de la omisión de medios en Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) en la sección planificación. Puede deshabilitar la omisión de medios en el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="47c26-108">For details about when to use Media bypass, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) in the Planning section.You can disable media bypass from the Lync Server Control Panel.</span></span> <span data-ttu-id="47c26-109">Para obtener más información sobre cómo habilitar y configurar el bypass medial, consulte [Habilitar el omisión de medios de red en Lync Server 2013](lync-server-2013-enabling-network-media-bypass.md)</span><span class="sxs-lookup"><span data-stu-id="47c26-109">For details on enabling and configuring medial bypass, see [Enabling network media bypass in Lync Server 2013](lync-server-2013-enabling-network-media-bypass.md)</span></span>

<div>

## <a name="to-disable-media-bypass"></a><span data-ttu-id="47c26-110">Para deshabilitar la omisión de medios</span><span class="sxs-lookup"><span data-stu-id="47c26-110">To disable media bypass</span></span>

1.  <span data-ttu-id="47c26-111">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="47c26-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="47c26-112">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="47c26-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="47c26-113">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="47c26-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="47c26-114">En la barra de navegación izquierda, haga clic en **configuración de red** y, después, en **global**.</span><span class="sxs-lookup"><span data-stu-id="47c26-114">In the left navigation bar, click **Network Configuration** and then click **Global**.</span></span>

4.  <span data-ttu-id="47c26-115">En la página **global** , haga clic en la configuración **global** .</span><span class="sxs-lookup"><span data-stu-id="47c26-115">On the **Global** page, click the **Global** configuration.</span></span> <span data-ttu-id="47c26-116">Siempre hay una sola configuración y siempre se denomina global.</span><span class="sxs-lookup"><span data-stu-id="47c26-116">There is always only one configuration, and it is always named Global.</span></span>

5.  <span data-ttu-id="47c26-117">En el menú **Editar** , haga clic en **Ver detalles**.</span><span class="sxs-lookup"><span data-stu-id="47c26-117">On the **Edit** menu, click **View details**.</span></span>

6.  <span data-ttu-id="47c26-118">En la página **Editar configuración global** , desactive la casilla **Habilitar omisión de medios** .</span><span class="sxs-lookup"><span data-stu-id="47c26-118">On the **Edit Global Setting** page, clear the **Enable media bypass** check box.</span></span>

7.  <span data-ttu-id="47c26-119">Haga clic en **confirmar** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="47c26-119">Click **Commit** to save your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="47c26-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="47c26-120">See Also</span></span>


[<span data-ttu-id="47c26-121">Habilitar el omisión de medios de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47c26-121">Enabling network media bypass in Lync Server 2013</span></span>](lync-server-2013-enabling-network-media-bypass.md)  
  

<span data-ttu-id="47c26-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47c26-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

