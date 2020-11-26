---
title: 'Lync Server 2013: Restauración de contenidos de conferencia mediante el servicio de copias de seguridad'
description: 'Lync Server 2013: restauración de contenido de la Conferencia con el servicio de copia de seguridad.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring conference contents using the Backup Service
ms:assetid: 3e0f18ec-7319-4c07-a59b-2938e7787bc9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688030(v=OCS.15)
ms:contentKeyID: 49733620
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3a0037af711948c008e74c5444373ed995f0e6e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442547"
---
# <a name="restoring-conference-contents-using-the-backup-service-in-lync-server-2013"></a><span data-ttu-id="72cf0-103">Restauración de contenidos de conferencia mediante el servicio de copias de seguridad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72cf0-103">Restoring conference contents using the Backup Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="72cf0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="72cf0-104">

<span> </span></span></span>

<span data-ttu-id="72cf0-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="72cf0-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="72cf0-106">Si la información de conferencia almacenada en el almacén de archivos de un grupo de servidores front-end no está disponible.</span><span class="sxs-lookup"><span data-stu-id="72cf0-106">If the conference information stored in the file store of a Front End pool becomes unavailable.</span></span> <span data-ttu-id="72cf0-107">debe restaurar esta información para que los usuarios alojados en el grupo conserven sus datos de conferencia.</span><span class="sxs-lookup"><span data-stu-id="72cf0-107">you must restore this information so that users homed on the pool retain their conference data.</span></span> <span data-ttu-id="72cf0-108">Si el grupo de servidores front-end que ha perdido los datos de la Conferencia está emparejado con otro grupo de servidores front-end, puede usar el servicio de copia de seguridad para restaurar los datos.</span><span class="sxs-lookup"><span data-stu-id="72cf0-108">If the Front End pool which has lost conference data is paired with another Front End pool, you can use the Backup Service to restore the data.</span></span>

<span data-ttu-id="72cf0-109">También debe realizar esta tarea si se ha producido un error en un grupo completo y tiene que migrar por error sus usuarios a un grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="72cf0-109">You must also perform this task if an entire pool has failed and you have to fail over its users to a backup pool.</span></span> <span data-ttu-id="72cf0-110">Cuando estos usuarios no realicen una conmutación por error a su grupo original, debe usar este procedimiento para copiar el contenido de la Conferencia a su grupo original.</span><span class="sxs-lookup"><span data-stu-id="72cf0-110">When these users are failed back over to their original pool, you must use this procedure to copy their conference content back to their original pool as well.</span></span>

<span data-ttu-id="72cf0-111">Supongamos que Pool1 está emparejado con Pool2, y se pierden los datos de la Conferencia en Pool1.</span><span class="sxs-lookup"><span data-stu-id="72cf0-111">Assume that Pool1 is paired with Pool2, and the conference data in Pool1 is lost.</span></span> <span data-ttu-id="72cf0-112">Puede usar el siguiente cmdlet para invocar el servicio de copia de seguridad para restaurar el contenido:</span><span class="sxs-lookup"><span data-stu-id="72cf0-112">You can use the following cmdlet to invoke the Backup Service to restore the contents:</span></span>

    Invoke-CsBackupServiceSync -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="72cf0-113">La restauración del contenido de la Conferencia puede llevar algún tiempo, dependiendo de su tamaño.</span><span class="sxs-lookup"><span data-stu-id="72cf0-113">Restoring the conference contents may take some time, depending on their size.</span></span> <span data-ttu-id="72cf0-114">Puede usar el siguiente cmdlet para comprobar el estado del proceso:</span><span class="sxs-lookup"><span data-stu-id="72cf0-114">You can use the following cmdlet to check the process status:</span></span>

    Get-CsBackupServiceStatus -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="72cf0-115">El proceso se realiza cuando este cmdlet devuelve un valor de estado estable para el módulo de conferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="72cf0-115">The process is done when this cmdlet returns a value of Steady State for the data conference module.</span></span>

<span data-ttu-id="72cf0-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="72cf0-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

