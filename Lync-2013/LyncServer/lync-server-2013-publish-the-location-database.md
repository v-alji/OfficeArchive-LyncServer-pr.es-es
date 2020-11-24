---
title: 'Lync Server 2013: publicar la base de datos de ubicaciones'
description: 'Lync Server 2013: publicar la base de datos de ubicaciones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the location database
ms:assetid: dd032b5b-df0e-4017-ac46-e17570c1ab1e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398974(v=OCS.15)
ms:contentKeyID: 48185598
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26892429c7bf5fd9cbfebd0d7ac62482767a541e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399054"
---
# <a name="publish-the-location-database-from-lync-server-2013"></a><span data-ttu-id="f1cf0-103">Publicar la base de datos de ubicación desde Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1cf0-103">Publish the location database from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1cf0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1cf0-104">

<span> </span></span></span>

<span data-ttu-id="f1cf0-105">_**Última modificación del tema:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="f1cf0-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="f1cf0-106">Las nuevas ubicaciones agregadas a la base de datos de ubicaciones no estarán disponibles para el cliente hasta que no se publiquen.</span><span class="sxs-lookup"><span data-stu-id="f1cf0-106">The new locations that you added to the location database will not be made available to the client until they have been published.</span></span>

<span data-ttu-id="f1cf0-107">Para obtener más información, consulte la documentación del shell de administración de Lync Server para el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f1cf0-107">For details, see the Lync Server Management Shell documentation for the following cmdlet:</span></span>

  - <span data-ttu-id="f1cf0-108">**Publish-CsLisConfiguration**</span><span class="sxs-lookup"><span data-stu-id="f1cf0-108">**Publish-CsLisConfiguration**</span></span>

<span data-ttu-id="f1cf0-109">Si usa puertas de enlace de número de identificación de ubicación de emergencia (ELIN), cargue también los ELIN en la base de datos de identificación de ubicación automática (ALI) del proveedor de la red telefónica conmutada (RTC).</span><span class="sxs-lookup"><span data-stu-id="f1cf0-109">If you use Emergency Location Identification Number (ELIN) gateways, you also need to upload the ELINs to your public switched telephone network (PSTN) carrier's Automatic Location Identification (ALI) database.</span></span> <span data-ttu-id="f1cf0-110">Probablemente el proveedor de RTC le solicite que use un formato específico para los registros de ELIN.</span><span class="sxs-lookup"><span data-stu-id="f1cf0-110">Your PSTN carrier may require you to use a specific format for the ELIN records.</span></span> <span data-ttu-id="f1cf0-111">Póngase en contacto con el proveedor de RTC para obtener más información al respecto.</span><span class="sxs-lookup"><span data-stu-id="f1cf0-111">Contact your PSTN carrier for details.</span></span> <span data-ttu-id="f1cf0-112">Puede exportar los registros de la base de datos de servicios de información de ubicación y darles formato según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f1cf0-112">You can export the records from the Location Information service database and format them as required.</span></span>

<div>

## <a name="to-publish-the-location-database"></a><span data-ttu-id="f1cf0-113">Para publicar la base de datos de ubicaciones</span><span class="sxs-lookup"><span data-stu-id="f1cf0-113">To publish the location database</span></span>

  - <span data-ttu-id="f1cf0-114">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="f1cf0-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

  - <span data-ttu-id="f1cf0-115">Ejecute el cmdlet siguiente para publicar la base de datos de ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="f1cf0-115">Run the following cmdlet to publish the location database.</span></span>
    
        Publish-CsLisConfiguration

<span data-ttu-id="f1cf0-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1cf0-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

