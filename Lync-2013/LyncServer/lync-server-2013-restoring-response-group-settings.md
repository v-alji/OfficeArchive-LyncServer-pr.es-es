---
title: 'Lync Server 2013: restauración de la configuración del grupo de respuesta'
description: 'Lync Server 2013: restauración de la configuración del grupo de respuesta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring Response Group settings
ms:assetid: 4f8e1949-925d-4538-be1d-9ac7c06b2aca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202174(v=OCS.15)
ms:contentKeyID: 51541473
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bffec18507d43287e2b56c8f518e93aff602a908
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442505"
---
# <a name="restoring-response-group-settings-in-lync-server-2013"></a><span data-ttu-id="1b047-103">Restauración de la configuración de grupos de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1b047-103">Restoring Response Group settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1b047-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1b047-104">

<span> </span></span></span>

<span data-ttu-id="1b047-105">_**Última modificación del tema:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="1b047-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="1b047-106">Si ha implementado la aplicación de grupo de respuesta y necesita restaurar un servidor de servicios de fondo o un servidor Standard Edition, también tendrá que restaurar los valores de configuración del grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b047-106">If you deployed the Response Group application and you need to restore a Back End Server or a Standard Edition server, you also need to restore the Response Group configuration settings.</span></span>

<div>

## <a name="to-restore-response-group-configuration-settings"></a><span data-ttu-id="1b047-107">Para restaurar las opciones de configuración de grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="1b047-107">To restore Response Group configuration settings</span></span>

1.  <span data-ttu-id="1b047-108">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1b047-108">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<pool FQDN>" -OverwriteOwner -FileName "<path and file name of the backed up file at $Backup>"
    
    <span data-ttu-id="1b047-109">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1b047-109">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service: ApplicationServer:pool01.contoso.com" -OverwriteOwner -FileName "C:\RgsConfiguration.zip"

<span data-ttu-id="1b047-110"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1b047-110"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

