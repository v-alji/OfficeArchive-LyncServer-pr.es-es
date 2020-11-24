---
title: Cambiar las direcciones URL simples tras la migración
description: Cambie las URL simples después de la migración.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Change simple URLs after migration
ms:assetid: addb0dc8-8324-42b1-9a00-f4bd14fdf5c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721844(v=OCS.15)
ms:contentKeyID: 49733777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f9974106d28bcfdc64c2255337baf721a937e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398580"
---
# <a name="change-simple-urls-after-migration"></a><span data-ttu-id="5c272-103">Cambiar las direcciones URL simples tras la migración</span><span class="sxs-lookup"><span data-stu-id="5c272-103">Change simple URLs after migration</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c272-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c272-104">

<span> </span></span></span>

<span data-ttu-id="5c272-105">_**Última modificación del tema:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="5c272-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="5c272-106">Lync Server admite tres direcciones URL simples:</span><span class="sxs-lookup"><span data-stu-id="5c272-106">Lync Server supports three simple URLs:</span></span>

  - <span data-ttu-id="5c272-107">**Reunirse** se usa como la dirección URL base para todas las conferencias del sitio o la organización.</span><span class="sxs-lookup"><span data-stu-id="5c272-107">**Meet** is used as the base URL for all conferences in the site or organization.</span></span> <span data-ttu-id="5c272-108">Con la dirección URL simple, los vínculos a las reuniones de unirse son fáciles de comprender y se pueden comunicar y distribuir fácilmente.</span><span class="sxs-lookup"><span data-stu-id="5c272-108">With the Meet simple URL, links to join meetings are easy to comprehend, and easy to communicate and distribute.</span></span>

  - <span data-ttu-id="5c272-109">El acceso **telefónico** permite el acceso a la Página Web de configuración de conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="5c272-109">**Dial-in** enables access to the Dial-in Conferencing Settings webpage.</span></span> <span data-ttu-id="5c272-110">La dirección URL de acceso telefónico simple está incluida en todas las invitaciones a reuniones para que los usuarios que deseen llamar a la reunión puedan tener acceso a la información del número de teléfono y del PIN necesarios.</span><span class="sxs-lookup"><span data-stu-id="5c272-110">The Dial-in simple URL is included in all meeting invitations so that users who want to dial in to the meeting can access the necessary phone number and PIN information.</span></span>

  - <span data-ttu-id="5c272-111">El **Administrador** permite acceder rápidamente al panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5c272-111">**Admin** enables quick access to the Lync Server Control Panel.</span></span> <span data-ttu-id="5c272-112">La dirección URL simple de administración es interna de su organización.</span><span class="sxs-lookup"><span data-stu-id="5c272-112">The Admin simple URL is internal to your organization.</span></span>

<span data-ttu-id="5c272-113">Después de migrar a Lync Server 2013, debe tener en cuenta cómo afecta el cambio a los registros DNS y los certificados para las direcciones URL simples.</span><span class="sxs-lookup"><span data-stu-id="5c272-113">After migrating to Lync Server 2013, you must be aware of how the change impacts your DNS records and certificates for simple URLs.</span></span> <span data-ttu-id="5c272-114">Si el director de Lync Server 2010 heredado permanece en uso en la topología, no es necesario realizar cambios en las direcciones URL simples.</span><span class="sxs-lookup"><span data-stu-id="5c272-114">If the legacy Lync Server 2010 Director remains in use in the topology, no changes to your simple URLs are required.</span></span> <span data-ttu-id="5c272-115">Si se quita Lync Server 2010 Director de la topología después de la migración, los registros DNS de direcciones URL simples deben actualizarse para que apunten a uno de los grupos de servidores de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5c272-115">If the Lync Server 2010 Director is removed from the topology after migration, the simple URL DNS records must be updated to point to one of the Lync Server 2013 pools.</span></span> <span data-ttu-id="5c272-116">Sin embargo, cada vez que cambie un nombre de dirección URL simple, debe ejecutar Enable-CsComputer en cada director y en el servidor front-end para registrar el cambio.</span><span class="sxs-lookup"><span data-stu-id="5c272-116">Whenever you change a simple URL name, however, you must run Enable-CsComputer on each Director and Front End Server to register the change.</span></span>

<div>

## <a name="changing-simple-urls-after-migration"></a><span data-ttu-id="5c272-117">Cambiar las URL simples después de la migración</span><span class="sxs-lookup"><span data-stu-id="5c272-117">Changing Simple URLs after Migration</span></span>

<span data-ttu-id="5c272-118">**Para actualizar la dirección URL simple de reunirse**</span><span class="sxs-lookup"><span data-stu-id="5c272-118">**To update the Meet simple URL**</span></span>

1.  <span data-ttu-id="5c272-119">En el generador de topología, haga clic con el botón secundario en el nodo superior de **Lync Server** y, a continuación, haga clic en **Editar propiedades**.</span><span class="sxs-lookup"><span data-stu-id="5c272-119">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="5c272-120">Seleccione **URL simples** en el panel izquierdo y, a continuación, debajo de **direcciones URL de reunión:** seleccione la dirección URL de la reunión y haga clic en **Editar URL**.</span><span class="sxs-lookup"><span data-stu-id="5c272-120">Select **Simple URLs** in the left pane, then below **Meeting URLs:** select the Meet URL and then click **Edit URL**.</span></span>

3.  <span data-ttu-id="5c272-121">Actualice la dirección URL con el valor que quiera y haga clic en **Aceptar** para guardar la dirección URL modificada.</span><span class="sxs-lookup"><span data-stu-id="5c272-121">Update the URL to the value you want, and then click **OK** to save the edited URL.</span></span>

<span data-ttu-id="5c272-122">**Para actualizar la dirección URL simple de administración**</span><span class="sxs-lookup"><span data-stu-id="5c272-122">**To update the Admin simple URL**</span></span>

1.  <span data-ttu-id="5c272-123">En el generador de topología, haga clic con el botón secundario en el nodo superior de **Lync Server** y, a continuación, haga clic en **Editar propiedades**.</span><span class="sxs-lookup"><span data-stu-id="5c272-123">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="5c272-124">Seleccione **URL simples** en el panel izquierdo y, a continuación, haga clic en **dirección URL de acceso administrativo** , escriba la dirección URL simple que desee para el acceso administrativo al panel de Control de Lync Server 2013 y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5c272-124">Select **Simple URLs** in the left pane, then below **Administrative access URL** box, enter the simple URL you want for administrative access to Lync Server 2013 Control Panel, and then click **OK**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="5c272-125">Recomendamos usar la dirección URL más simple posible como dirección URL sencilla de administración.</span><span class="sxs-lookup"><span data-stu-id="5c272-125">We recommend using the simplest possible URL for the Admin URL.</span></span> <span data-ttu-id="5c272-126">La opción más sencilla es <STRONG> https://admin .</STRONG> &lt; dominio &gt; .</span><span class="sxs-lookup"><span data-stu-id="5c272-126">The simplest option is <STRONG>https://admin.</STRONG>&lt;domain&gt;.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5c272-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c272-127">See Also</span></span>


[<span data-ttu-id="5c272-128">Planeación de las direcciones URL simples en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c272-128">Planning for simple URLs in Lync Server 2013</span></span>](lync-server-2013-planning-for-simple-urls.md)  
  

<span data-ttu-id="5c272-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c272-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

