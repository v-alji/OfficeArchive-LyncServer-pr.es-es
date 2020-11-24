---
title: Configurar servidores de aplicaciones de confianza
description: Configure los servidores de aplicaciones de confianza.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure trusted application servers
ms:assetid: 20c3815f-3048-4940-8c0f-cdfcd0801d5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204735(v=OCS.15)
ms:contentKeyID: 48183592
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39f439ea3e5996e0a3464540069024b70c415e3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398861"
---
# <a name="configure-trusted-application-servers"></a><span data-ttu-id="5b1a7-103">Configurar servidores de aplicaciones de confianza</span><span class="sxs-lookup"><span data-stu-id="5b1a7-103">Configure trusted application servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b1a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b1a7-104">

<span> </span></span></span>

<span data-ttu-id="5b1a7-105">_**Última modificación del tema:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="5b1a7-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="5b1a7-106">En un entorno mixto, si crea un nuevo servidor de aplicaciones de confianza, debe configurar el grupo de próximos saltos para que sea un grupo de servidores de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="5b1a7-106">In a mixed environment, if you create a new trusted application server, you must set the next hop pool to be a Lync Server 2013 pool.</span></span> <span data-ttu-id="5b1a7-107">En un entorno mixto, tanto el grupo heredado de Lync Server 2010 y el grupo de servidores Lync Server 2013 aparecen en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="5b1a7-107">In a mixed environment, both the legacy Lync Server 2010 pool and the Lync Server 2013 pool appear in the drop down list.</span></span> <span data-ttu-id="5b1a7-108">No se puede seleccionar el grupo heredado.</span><span class="sxs-lookup"><span data-stu-id="5b1a7-108">Selecting the legacy pool is not supported.</span></span>

<span data-ttu-id="5b1a7-109">**Seleccione Lync Server 2013 como próximo salto al crear un servidor de aplicaciones de confianza**</span><span class="sxs-lookup"><span data-stu-id="5b1a7-109">**Select Lync Server 2013 as next hop when creating a Trusted application server**</span></span>

1.  <span data-ttu-id="5b1a7-110">Abra el generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="5b1a7-110">Open Topology Builder.</span></span>

2.  <span data-ttu-id="5b1a7-111">En el panel izquierdo, haga clic con el botón secundario en **servidores de aplicaciones de confianza** y haga clic en **nuevo grupo de aplicaciones de confianza**.</span><span class="sxs-lookup"><span data-stu-id="5b1a7-111">In the left pane, right click **Trusted application servers** and click **New Trusted Application Pool**.</span></span>

3.  <span data-ttu-id="5b1a7-112">Escriba el **FQDN del grupo** del grupo de aplicaciones de confianza y seleccione si será un servidor único o de varios servidores.</span><span class="sxs-lookup"><span data-stu-id="5b1a7-112">Enter the **Pool FQDN** of the trusted application pool and select whether it will be a single-server or multiple-server.</span></span>

4.  <span data-ttu-id="5b1a7-113">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5b1a7-113">Click **Next**.</span></span>

5.  <span data-ttu-id="5b1a7-114">En la página **seleccionar el próximo salto** , en la lista, seleccione el grupo de servidores front-end de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b1a7-114">On the **Select the next hop** page, from the list, select the Lync Server 2013 Front End pool.</span></span>

6.  <span data-ttu-id="5b1a7-115">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="5b1a7-115">Click **Finish**.</span></span>

7.  <span data-ttu-id="5b1a7-116">Seleccione el nodo superior de **Lync Server** y, en el menú **acción** , seleccione **publicar**.</span><span class="sxs-lookup"><span data-stu-id="5b1a7-116">Select the top node **Lync Server** and from the **Action** menu, select **Publish**.</span></span>
    
    <span data-ttu-id="5b1a7-117">Compruebe que el **grupo de aplicaciones de confianza** se haya creado correctamente y que esté asociado al grupo de servidores front-end correcto.</span><span class="sxs-lookup"><span data-stu-id="5b1a7-117">Verify the **Trusted Application Pool** has been created successfully and is associated with the correct Front End pool.</span></span>

<span data-ttu-id="5b1a7-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b1a7-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

