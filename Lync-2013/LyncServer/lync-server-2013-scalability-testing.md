---
title: Pruebas de escalabilidad de Lync Server 2013
description: Pruebas de escalabilidad de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scalability testing
ms:assetid: bf41bac6-d4ec-4de6-9a44-a82d01a87279
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205226(v=OCS.15)
ms:contentKeyID: 48185289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 73b4ab8726de7ea068ed60fedf104b01fe91ac1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442127"
---
# <a name="scalability-testing-in-lync-server-2013"></a><span data-ttu-id="714c1-103">Pruebas de escalabilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="714c1-103">Scalability testing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="714c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="714c1-104">

<span> </span></span></span>

<span data-ttu-id="714c1-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="714c1-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="714c1-106">Lync Server 2013 proporciona la infraestructura de servidor para todas las comunicaciones en tiempo real de Lync Server, incluidas la mensajería instantánea (mi) y la presencia, Conferencia y telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="714c1-106">Lync Server 2013 provides the server infrastructure for all Lync Server real-time communications, including instant messaging (IM) and presence, conferencing, and Enterprise Voice.</span></span> <span data-ttu-id="714c1-107">Esto incluye todas las características que usan los recursos de hardware de un grupo de 2013 de Lync Server y, por lo tanto, afectan al rendimiento y la escala.</span><span class="sxs-lookup"><span data-stu-id="714c1-107">This includes any features that use the hardware resources of a Lync Server 2013 pool and, therefore, affect performance and scale.</span></span> <span data-ttu-id="714c1-108">Todas las organizaciones no usan todas las características.</span><span class="sxs-lookup"><span data-stu-id="714c1-108">All organizations do not use all features equally.</span></span>

<span data-ttu-id="714c1-109">Por ejemplo, es posible que algunas organizaciones usen el vídeo en conferencias muy intensa, mientras que otras pueden tener poco o ningún uso de video.</span><span class="sxs-lookup"><span data-stu-id="714c1-109">For example, some organizations might use video in conferences very heavily while others might have little or no video usage.</span></span> <span data-ttu-id="714c1-110">Algunas organizaciones prefieren el uso compartido de diapositivas de PowerPoint para compartir aplicaciones, mientras que otras prefieren lo opuesto.</span><span class="sxs-lookup"><span data-stu-id="714c1-110">Some organizations prefer PowerPoint slide sharing to application sharing, while others prefer the opposite.</span></span> <span data-ttu-id="714c1-111">Las organizaciones que implementan la telefonía IP empresarial pueden o no usar en gran medida la aplicación de grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="714c1-111">Those organizations that deploy Enterprise Voice might or might not use the Response Group application heavily.</span></span> <span data-ttu-id="714c1-112">La mayoría de las organizaciones implementan servidores de supervisión, pero no muchos de ellos implementan servidores de archivado.</span><span class="sxs-lookup"><span data-stu-id="714c1-112">Most organizations deploy Monitoring Servers, but not many of them deploy Archiving Servers.</span></span> <span data-ttu-id="714c1-113">Además, las organizaciones no tienen las mismas infraestructuras, entre ellas, capacidades de hardware, capacidades de red y la cantidad de pools y el tamaño de los pools implementados.</span><span class="sxs-lookup"><span data-stu-id="714c1-113">Additionally, organizations do not all have the same infrastructures, including hardware capacities, network capacities, and the number of pools and size of pools deployed.</span></span> <span data-ttu-id="714c1-114">La diversidad de características e infraestructuras supone un reto para las pruebas de escalabilidad; no es posible simular todas las combinaciones posibles de las características y las infraestructuras.</span><span class="sxs-lookup"><span data-stu-id="714c1-114">The diversity of features and infrastructures poses a challenge to scalability testing – it is not possible to simulate all possible combinations of features and infrastructures.</span></span>

<span data-ttu-id="714c1-115">Para determinar la compatibilidad de escalabilidad de Lync Server, realizamos pruebas con todas las características de Lync Server de forma simultánea, en función de un modelo de uso promedio (modelo de usuario).</span><span class="sxs-lookup"><span data-stu-id="714c1-115">To determine scalability support for Lync Server, we conduct testing by using all Lync Server features concurrently, based on an average usage model (user model).</span></span> <span data-ttu-id="714c1-116">Para determinar un modelo de usuario adecuado para las cargas de trabajo de Lync Server, analizamos muchos puntos de datos, entre los que se incluyen encuestas de clientes, comentarios del programa para la mejora de la experiencia del cliente de Microsoft, datos de uso de Lync Server del Departamento de TI interno de Microsoft y datos extraídos de nuestro servicio de Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="714c1-116">To determine an appropriate user model for Lync Server workloads, we analyze many data points, including customer surveys, feedback from the Microsoft customer experience improvement program, Lync Server usage data from the internal IT department at Microsoft, and data mined from our Live Meeting Service.</span></span> <span data-ttu-id="714c1-117">En muchos casos, el modelo de usuario tiene un sesgo hacia cargas más pesadas para proporcionar un margen cómodo para el uso dentro de una organización.</span><span class="sxs-lookup"><span data-stu-id="714c1-117">In many cases, the user model has a bias towards heavier loads to provide a comfortable margin for usage within an organization.</span></span>

<span data-ttu-id="714c1-118">En nuestras pruebas de escalabilidad, configuramos los grupos de aplicaciones de Lync Server 2013 según las especificaciones de hardware y software recomendadas, incluidos los componentes de la infraestructura, como los servicios de dominio de Active Directory, los equilibradores de carga de hardware y los firewalls.</span><span class="sxs-lookup"><span data-stu-id="714c1-118">In our scalability tests, we set up Lync Server 2013 pools according to the recommended hardware and software specifications, including infrastructure components, such as Active Directory Domain Services, hardware load balancers, and firewalls.</span></span> <span data-ttu-id="714c1-119">La configuración de entornos de Lync Server es lo más parecida a la de los entornos reales típicos.</span><span class="sxs-lookup"><span data-stu-id="714c1-119">We set up Lync Server environments as closely as possible to typical real-world environments.</span></span> <span data-ttu-id="714c1-120">A continuación, usamos la herramienta de estrés y rendimiento de Lync Server 2013 para simular las cargas de Lync Server 2013 (según nuestro modelo de usuario).</span><span class="sxs-lookup"><span data-stu-id="714c1-120">We then use the Lync Server 2013 Stress and Performance Tool to simulate Lync Server 2013 loads (based on our user model).</span></span> <span data-ttu-id="714c1-121">.</span><span class="sxs-lookup"><span data-stu-id="714c1-121">.</span></span>

<span data-ttu-id="714c1-122">Realizamos varias iteraciones de pruebas de escalabilidad (incluidas varias ejecuciones de prueba de tres semanas).</span><span class="sxs-lookup"><span data-stu-id="714c1-122">We do multiple iterations of scalability tests (including multiple three-week test runs).</span></span> <span data-ttu-id="714c1-123">Usamos los resultados de todas las pruebas para ayudar con el ajuste de rendimiento y para comprobar la compatibilidad con los números de escalabilidad en nuestro modelo de usuario.</span><span class="sxs-lookup"><span data-stu-id="714c1-123">We use the results of all tests to help with performance tuning and to verify support for the scalability numbers in our user model.</span></span>

<span data-ttu-id="714c1-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="714c1-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

