---
title: 'Lync Server 2013: configuración de una ubicación de copia de seguridad'
description: 'Lync Server 2013: configuración de una ubicación de copia de seguridad.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up a backup location
ms:assetid: 006732eb-3d44-414d-8010-227a855caa93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202158(v=OCS.15)
ms:contentKeyID: 51541440
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 344baea1b7e51454bb28d31d88451d29fd6aa3a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399653"
---
# <a name="setting-up-a-backup-location-for-lync-server-2013"></a><span data-ttu-id="2bab1-103">Configuración de una ubicación de copia de seguridad para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2bab1-103">Setting up a backup location for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2bab1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2bab1-104">

<span> </span></span></span>

<span data-ttu-id="2bab1-105">_**Última modificación del tema:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="2bab1-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="2bab1-106">Antes de llevar a cabo la primera copia de seguridad de Lync Server, configure el hardware y el software que necesita para almacenar y mantener las copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2bab1-106">Before you take your first backup of Lync Server, set up the hardware and software that you need in order to store and maintain the backups.</span></span> <span data-ttu-id="2bab1-107">Necesita obtener acceso a los medios y al contenido, según corresponda, y proporcionar conectividad de red entre cada servidor en el que realizar una copia de seguridad y los medios de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2bab1-107">You need to obtain access to the media and content, as appropriate, and provide network connectivity between each server to be backed up and the backup media.</span></span> <span data-ttu-id="2bab1-108">El medio y la ubicación que use deben definirse en su estrategia de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="2bab1-108">The media and location that you use should be defined in your backup and restoration strategy.</span></span> <span data-ttu-id="2bab1-109">La ubicación que use para las copias de seguridad periódicas puede ser local o remota, pero debe ser segura y debe ser accesible tanto para la copia de seguridad como para la restauración.</span><span class="sxs-lookup"><span data-stu-id="2bab1-109">The location that you use for regular backups can be local or remote, but it must be secure, and it must be accessible for both backup and restoration.</span></span> <span data-ttu-id="2bab1-110">Le recomendamos que use una ubicación remota para protegerse contra un evento catastrófico en su sitio primario.</span><span class="sxs-lookup"><span data-stu-id="2bab1-110">We recommend using a remote location to protect against a catastrophic event at your primary site.</span></span>

<span data-ttu-id="2bab1-111">Después de configurar y probar los componentes individuales, Compruebe la accesibilidad a las copias de seguridad de cada servidor.</span><span class="sxs-lookup"><span data-stu-id="2bab1-111">After you set up and test the individual components, verify accessibility to the backups from each server.</span></span>

<span data-ttu-id="2bab1-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2bab1-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

