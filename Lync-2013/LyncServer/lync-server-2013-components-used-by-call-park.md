---
title: 'Lync Server 2013: Componentes que usa el estacionamiento de llamadas'
description: 'Lync Server 2013: componentes usados por el parque de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Call Park
ms:assetid: c7ffbee3-0ce1-48c0-bb56-af098b41d6d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398824(v=OCS.15)
ms:contentKeyID: 48185374
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 285af316fa2d49e8bebf68e11de6d9526e12ae29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398526"
---
# <a name="components-used-by-call-park-in-lync-server-2013"></a><span data-ttu-id="238ec-103">Componentes que usa el estacionamiento de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="238ec-103">Components used by Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="238ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="238ec-104">

<span> </span></span></span>

<span data-ttu-id="238ec-105">_**Última modificación del tema:** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="238ec-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="238ec-106">La aplicación de estacionamiento de llamadas se instala automáticamente al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="238ec-106">The Call Park application is automatically installed when you deploy Enterprise Voice.</span></span> <span data-ttu-id="238ec-107">Para habilitar el parque de llamadas, configure la Directiva de voz.</span><span class="sxs-lookup"><span data-stu-id="238ec-107">You enable Call Park by configuring voice policy.</span></span> <span data-ttu-id="238ec-108">Los siguientes componentes de Lync Server 2013 son compatibles con la aplicación estacionamiento de llamadas:</span><span class="sxs-lookup"><span data-stu-id="238ec-108">The following Lync Server 2013 components support the Call Park application:</span></span>

  - <span data-ttu-id="238ec-109">**Servicio de aplicación**   El servicio de aplicación proporciona una plataforma para implementar, hospedar y administrar aplicaciones de comunicaciones unificadas, como la aplicación de estacionamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="238ec-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="238ec-110">El servicio de aplicaciones se instala automáticamente en todos los servidores front-end de un grupo de servidores front-end y en todos los servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="238ec-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="238ec-111">**Aplicación de estacionamiento de llamadas**   La aplicación de estacionamiento de llamadas es una de las aplicaciones de comunicaciones unificadas que se hospedan en el servicio de aplicación.</span><span class="sxs-lookup"><span data-stu-id="238ec-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="238ec-112">Se incluye automáticamente al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="238ec-112">It is included automatically when you deploy Enterprise Voice.</span></span> <span data-ttu-id="238ec-113">Llama a parques de aparcamiento y recupera llamadas y administra las órbitas del parque de llamadas.</span><span class="sxs-lookup"><span data-stu-id="238ec-113">Call Park parks and retrieves calls and manages call park orbits.</span></span>

  - <span data-ttu-id="238ec-114">**Música en espera-archivo**   Si está habilitada la música, el archivo de música se reproduce mientras se estaciona una llamada.</span><span class="sxs-lookup"><span data-stu-id="238ec-114">**Music-on hold-file**   If music in enabled, the music file is played while a call is parked.</span></span> <span data-ttu-id="238ec-115">Cuando se instala la aplicación de estacionamiento de llamadas, se incluye un archivo de música predeterminado.</span><span class="sxs-lookup"><span data-stu-id="238ec-115">A default music file is included when the Call Park application is installed.</span></span>

  - <span data-ttu-id="238ec-116">**Almacén de archivos**   La aplicación de estacionamiento de llamadas usa el almacén de archivos para almacenar los archivos de audio personalizados.</span><span class="sxs-lookup"><span data-stu-id="238ec-116">**File Store**   The Call Park application uses File Store to hold custom audio files.</span></span>

  - <span data-ttu-id="238ec-117">**Panel de control de Lync Server**   Puede usar el panel de control de Lync Server para configurar la tabla orbital de llamadas y para habilitar el parque de llamadas para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="238ec-117">**Lync Server Control Panel**   You can use Lync Server Control Panel to configure the call park orbit table and to enable Call Park for users.</span></span>

  - <span data-ttu-id="238ec-118">**Shell de administración de Lync Server**   Toda la configuración de la aplicación estacionamiento de llamadas se puede realizar con los cmdlets del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="238ec-118">**Lync Server Management Shell**   All Call Park application configuration can be performed by using Lync Server Management Shell cmdlets.</span></span>

<span data-ttu-id="238ec-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="238ec-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

