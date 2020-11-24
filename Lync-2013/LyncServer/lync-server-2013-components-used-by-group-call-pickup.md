---
title: 'Lync Server 2013: componentes usados por la recogida de llamadas grupales'
description: 'Lync Server 2013: componentes usados por la recogida de llamadas grupales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Group Call Pickup
ms:assetid: 45db2f23-d486-4b20-a8cf-7b48a1f9fd3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945625(v=OCS.15)
ms:contentKeyID: 51541470
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 517f75dcbac8bfed0e749c061a9696b7667e10ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398525"
---
# <a name="components-used-by-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="de6a7-103">Componentes usados por la recogida de llamadas grupales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de6a7-103">Components used by Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de6a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de6a7-104">

<span> </span></span></span>

<span data-ttu-id="de6a7-105">_**Última modificación del tema:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="de6a7-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="de6a7-106">La recopilación de llamadas grupales se implementa automáticamente al implementar la telefonía IP empresarial y la aplicación estacionamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="de6a7-106">Group Call Pickup is automatically deployed when you deploy Enterprise Voice and the Call Park application.</span></span> <span data-ttu-id="de6a7-107">Para habilitar la recopilación de llamadas de grupo, configure la tabla de llamadas en órbita con intervalos de números designados como números de grupo de recogida de llamadas y, a continuación, asigne usuarios para llamar a grupos de recogida y habilitar a los usuarios para la recogida de llamadas grupales.</span><span class="sxs-lookup"><span data-stu-id="de6a7-107">You enable Group Call Pickup by configuring the Call Park orbit table with separate ranges of numbers designated as call pickup group numbers, and then by assigning users to call pickup groups and enabling the users for Group Call Pickup.</span></span> <span data-ttu-id="de6a7-108">Los siguientes componentes de Lync Server admiten la recogida de llamadas de Grupo:</span><span class="sxs-lookup"><span data-stu-id="de6a7-108">The following Lync Server components support Group Call Pickup:</span></span>

  - <span data-ttu-id="de6a7-109">**Servicio de aplicación**   El servicio de aplicación proporciona una plataforma para implementar, hospedar y administrar aplicaciones de comunicaciones unificadas, como la aplicación de estacionamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="de6a7-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="de6a7-110">El servicio de aplicaciones se instala automáticamente en todos los servidores front-end de un grupo de servidores front-end y en todos los servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="de6a7-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="de6a7-111">**Aplicación de estacionamiento de llamadas**   La aplicación de estacionamiento de llamadas es una de las aplicaciones de comunicaciones unificadas que se hospedan en el servicio de aplicación.</span><span class="sxs-lookup"><span data-stu-id="de6a7-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="de6a7-112">La recogida de llamadas grupales se basa en la aplicación de estacionamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="de6a7-112">Group Call Pickup is based on the Call Park application.</span></span>

  - <span data-ttu-id="de6a7-113">**Shell de administración de Lync Server**   Use el shell de administración de Lync Server para administrar grupos de recopilación de llamadas de grupo.</span><span class="sxs-lookup"><span data-stu-id="de6a7-113">**Lync Server Management Shell**   You use Lync Server Management Shell to manage Group Call Pickup groups.</span></span>

  - <span data-ttu-id="de6a7-114">**Herramienta del kit de recursos de SEFAUtil**   Use la utilidad de activación de características de extensión secundaria (SEFAUtil) para asignar usuarios a un grupo de recogida de llamadas y para habilitar o deshabilitar la recogida de llamadas para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="de6a7-114">**SEFAUtil resource kit tool**   You use the secondary extension feature activation utility (SEFAUtil) to assign users to a call pickup group and to enable or disable call pickup for users.</span></span>

<span data-ttu-id="de6a7-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de6a7-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

