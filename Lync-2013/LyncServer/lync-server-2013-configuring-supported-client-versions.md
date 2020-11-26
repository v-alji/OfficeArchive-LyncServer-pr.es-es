---
title: 'Lync Server 2013: configuración de versiones de cliente compatibles'
description: 'Lync Server 2013: configuración de versiones de cliente compatibles.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring supported client versions
ms:assetid: aebf7b48-9aa2-4a06-adc5-0c9d11b6358d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412832(v=OCS.15)
ms:contentKeyID: 48185137
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74396314cae864fae134531b71375c750be8d3da
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432600"
---
# <a name="configuring-supported-client-versions-in-lync-server-2013"></a><span data-ttu-id="a8d5b-103">Configuración de las versiones de cliente compatibles en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8d5b-103">Configuring supported client versions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8d5b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8d5b-104">

<span> </span></span></span>

<span data-ttu-id="a8d5b-105">_**Última modificación del tema:** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="a8d5b-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="a8d5b-106">En Lync Server 2013, puede configurar directivas de versión de cliente para especificar las versiones de clientes que son compatibles con su entorno.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-106">In Lync Server 2013, you can set up client version policies to specify the versions of clients that are supported in your environment.</span></span> <span data-ttu-id="a8d5b-107">Además, puede usar la configuración de la versión de cliente global para especificar una acción predeterminada para clientes que aún no tienen una directiva de versión definida y, por lo tanto, no se admiten o restringen explícitamente.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-107">Additionally, you can use the global client version configuration to specify a default action for clients that do not already have a version policy defined and, therefore, are not explicitly supported or restricted.</span></span>

<span data-ttu-id="a8d5b-108">También puede usar las directivas de versión de cliente para administrar las actualizaciones de cliente.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-108">You can also use client version policies to manage client updates.</span></span> <span data-ttu-id="a8d5b-109">Al establecer una directiva de versión de cliente y usar las opciones **permitir y actualizar** , y **bloquear y actualizar**, los clientes recibirán software actualizado del servicio de actualización de Windows Server (si está usando este servicio) o de Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-109">When you set a client version policy and use the options **Allow and upgrade** and **Block and upgrade**, clients will receive updated software from the Windows Server Update Service (if you are using this service) or from Microsoft Update.</span></span>

<div>

## <a name="client-version-policy-settings"></a><span data-ttu-id="a8d5b-110">Configuración de la Directiva de versión del cliente</span><span class="sxs-lookup"><span data-stu-id="a8d5b-110">Client Version Policy Settings</span></span>

<span data-ttu-id="a8d5b-111">La Directiva de versión de cliente predeterminada requiere que todos los clientes ejecuten Lync.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-111">The default client version policy requires that all clients run Lync.</span></span> <span data-ttu-id="a8d5b-112">Si los clientes de su entorno ejecutan versiones anteriores de Communicator, es posible que tenga que volver a configurar las reglas de versión de cliente para evitar que los clientes y dispositivos se bloqueen o actualicen de forma inesperada al conectarse a Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-112">If clients in your environment are running earlier versions of Communicator, you may need to reconfigure the Client Version rules to prevent clients and devices from being unexpectedly blocked or updated when connecting to Lync Server 2013.</span></span> <span data-ttu-id="a8d5b-113">Puede modificar la regla predeterminada o puede Agregar una regla en la lista de directivas de versión de cliente para invalidar la regla predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-113">You can modify the default rule, or you can add a rule higher in the Client Version Policy list to override the default rule.</span></span> <span data-ttu-id="a8d5b-114">Además, a medida que se publican las actualizaciones acumulativas (CUs), debe configurar la Directiva de versión del cliente para que requiera las actualizaciones más recientes.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-114">Additionally, as Cumulative Updates (CUs) are released, you should configure the Client Version Policy to require the latest updates.</span></span> <span data-ttu-id="a8d5b-115">Para obtener más información, vea [especificar las aplicaciones cliente que se pueden usar para iniciar sesión en Lync Server 2013](lync-server-2013-specifying-the-client-applications-that-can-be-used-to-log-on-to-lync-server-2013.md) en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-115">For details, see [Specifying the client applications that can be used to log on to Lync Server 2013](lync-server-2013-specifying-the-client-applications-that-can-be-used-to-log-on-to-lync-server-2013.md) in the Operations documentation.</span></span>

<span data-ttu-id="a8d5b-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8d5b-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

