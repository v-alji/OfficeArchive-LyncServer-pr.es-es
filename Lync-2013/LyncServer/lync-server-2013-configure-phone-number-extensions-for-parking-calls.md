---
title: 'Lync Server 2013: configurar extensiones de números de teléfono para llamadas de aparcamiento'
description: 'Lync Server 2013: configurar extensiones de números de teléfono para las llamadas de aparcamiento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure phone number extensions for parking calls
ms:assetid: fbf97624-9587-42a6-b276-1b69c574a74d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182611(v=OCS.15)
ms:contentKeyID: 48185980
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6219e04243d0c19bc37251f7d113f7ebdd09fb72
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433811"
---
# <a name="configure-phone-number-extensions-for-parking-calls-in-lync-server-2013"></a><span data-ttu-id="339a9-103">Configurar extensiones de números de teléfono para llamadas de aparcamiento en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="339a9-103">Configure phone number extensions for parking calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="339a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="339a9-104">

<span> </span></span></span>

<span data-ttu-id="339a9-105">_**Última modificación del tema:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="339a9-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="339a9-106">La aplicación de estacionamiento de llamadas usa números de extensión en la tabla de llamadas de la órbita de estacionamiento para detener llamadas.</span><span class="sxs-lookup"><span data-stu-id="339a9-106">The Call Park application uses extension numbers in the Call Park orbit table to park calls.</span></span> <span data-ttu-id="339a9-107">Debe configurar la tabla de llamadas en órbita con los intervalos de números de extensión en los que la organización reserva las llamadas estacionadas.</span><span class="sxs-lookup"><span data-stu-id="339a9-107">You need to configure the Call Park orbit table with the ranges of extension numbers that your organization reserves for parked calls.</span></span> <span data-ttu-id="339a9-108">Estas extensiones tienen que ser extensiones virtuales (es decir, extensiones que no tengan ningún usuario ni teléfono asignado).</span><span class="sxs-lookup"><span data-stu-id="339a9-108">These extensions need to be virtual extensions (that is, extensions that have no user or phone assigned to them).</span></span> <span data-ttu-id="339a9-109">Cada grupo de Lync Server en el que se implementa y configura una aplicación de estacionamiento de llamadas puede tener uno o más intervalos Orbitantes.</span><span class="sxs-lookup"><span data-stu-id="339a9-109">Each Lync Server pool where a Call Park application is deployed and configured can have one or more orbit ranges.</span></span> <span data-ttu-id="339a9-110">Los intervalos de órbita deben ser únicos globalmente en la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="339a9-110">Orbit ranges must be globally unique across the Lync Server deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="339a9-111">Debe activar la casilla <STRONG>Habilitar estacionamiento de llamada</STRONG> en su Directiva de voz antes de poder usar el parque de llamadas.</span><span class="sxs-lookup"><span data-stu-id="339a9-111">You must select the <STRONG>Enable call park</STRONG> check box in your voice policy before you can use Call Park.</span></span> <span data-ttu-id="339a9-112">De forma predeterminada, esta opción no está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="339a9-112">By default, this option is not selected.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="339a9-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="339a9-113">In This Section</span></span>

  - [<span data-ttu-id="339a9-114">Crear o modificar un intervalo orbitar de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="339a9-114">Create or modify a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)

  - [<span data-ttu-id="339a9-115">Eliminar un intervalo orbitar de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="339a9-115">Delete a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-delete-a-call-park-orbit-range.md)

<span data-ttu-id="339a9-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="339a9-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

