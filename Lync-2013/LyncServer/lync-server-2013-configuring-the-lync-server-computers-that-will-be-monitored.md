---
title: 'Lync Server 2013: configuración de los equipos de Lync Server que se supervisarán'
description: 'Lync Server 2013: configuración de los equipos de Lync Server que se van a supervisar.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the Lync Server computers that will be monitored
ms:assetid: 9f1b2b91-d5af-42ad-a27d-b0815f762ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205118(v=OCS.15)
ms:contentKeyID: 48184927
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 742bd8a67eb42472e598c45619514e9407cb29cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432558"
---
# <a name="configuring-the-lync-server-computers-that-will-be-monitored-in-lync-server-2013"></a><span data-ttu-id="ec875-103">Configurar los equipos de Lync Server que se supervisarán en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec875-103">Configuring the Lync Server computers that will be monitored in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ec875-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ec875-104">

<span> </span></span></span>

<span data-ttu-id="ec875-105">_**Última modificación del tema:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="ec875-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="ec875-106">Puesto que Lync Server 2013 no usa el proceso de detección central que se usa en Microsoft Lync Server 2010, cada equipo de Lync Server 2013 que desee supervisar debe poder autoinformar sobre su existencia en el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="ec875-106">Because Lync Server 2013 does not use the central discovery process used in Microsoft Lync Server 2010, each Lync Server 2013 computer that you want to monitor must be able to self-report its existence to the management server.</span></span> <span data-ttu-id="ec875-107">Para que esto sea posible, debe instalar los archivos del agente Operations Manager en cada uno de los equipos que se van a supervisar.</span><span class="sxs-lookup"><span data-stu-id="ec875-107">To make this possible, you must install the Operations Manager agent files on each of the computers to be monitored.</span></span> <span data-ttu-id="ec875-108">Después de instalar los archivos del agente, debe configurar el equipo para que funcione como un proxy de System Center.</span><span class="sxs-lookup"><span data-stu-id="ec875-108">After the agent files have been installed, you must configure the computer to act as a System Center proxy.</span></span> <span data-ttu-id="ec875-109">Tenga en cuenta que estos procedimientos deben llevarse a cabo después de haber instalado y configurado Lync Server en estos equipos.</span><span class="sxs-lookup"><span data-stu-id="ec875-109">Note that these procedures should be carried out after you have installed and configured Lync Server on these computers.</span></span>

<span data-ttu-id="ec875-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ec875-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

