---
title: 'Lync Server 2013: Exportar e importar la configuración del enrutamiento de voz'
description: 'Lync Server 2013: exportar e importar la configuración del enrutamiento de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exporting and importing voice routing configuration
ms:assetid: c9b78622-5725-43b0-9ee1-5b82b1e1c8eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398836(v=OCS.15)
ms:contentKeyID: 48185398
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a94a9c02672debae9f5b30e3a1a96856050d6ab1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428359"
---
# <a name="exporting-and-importing-voice-routing-configuration-in-lync-server-2013"></a><span data-ttu-id="31a75-103">Exportar e importar la configuración del enrutamiento de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31a75-103">Exporting and importing voice routing configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31a75-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31a75-104">

<span> </span></span></span>

<span data-ttu-id="31a75-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="31a75-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="31a75-106">Si desea guardar la configuración de enrutamiento de voz sin publicarla, siga estos pasos para usar los comandos exportar e importar del panel de control de Lync Server para guardar y recuperar una instantánea de su configuración de enrutamiento de voz.</span><span class="sxs-lookup"><span data-stu-id="31a75-106">If you want to save your voice routing configuration without publishing it, follow these steps to use the Lync Server Control Panel configuration export and import commands to save and retrieve a snapshot of your voice routing configuration.</span></span> <span data-ttu-id="31a75-107">Al importar un archivo de configuración de enrutamiento de voz (. vcfg), pero se han realizado cambios en la configuración de enrutamiento de voz en el servidor mientras tanto, las páginas del grupo de **enrutamiento de voz** en el panel de control de Lync Server indicarán que hay cambios no confirmados en el enrutamiento de voz.</span><span class="sxs-lookup"><span data-stu-id="31a75-107">When you import a voice routing configuration file (.vcfg), but changes have been made to the voice routing configuration on the server in the meantime, the pages in the **Voice Routing** group in Lync Server Control Panel will indicate that there are uncommitted changes to voice routing.</span></span> <span data-ttu-id="31a75-108">Estos cambios no confirmados son las diferencias entre las dos configuraciones que requieren reconciliación.</span><span class="sxs-lookup"><span data-stu-id="31a75-108">Those uncommitted changes are the differences between the two configurations that require reconciliation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="31a75-109">Si ha realizado cambios no confirmados en la configuración de cualquier página del grupo de <STRONG>enrutamiento de voz</STRONG> , los cambios se guardan en el archivo de configuración de voz exportado (. vcfg).</span><span class="sxs-lookup"><span data-stu-id="31a75-109">If you have made any uncommitted changes to the settings on any page within the <STRONG>Voice Routing</STRONG> group, the changes are saved in the exported voice configuration file (.vcfg).</span></span> <span data-ttu-id="31a75-110">Esto le permite realizar cambios de configuración del enrutamiento de voz durante varias sesiones del panel de control de Lync Server antes de publicar los cambios.</span><span class="sxs-lookup"><span data-stu-id="31a75-110">This enables you to make voice routing configuration changes during multiple Lync Server Control Panel sessions before you publish the changes.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="31a75-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="31a75-111">In This Section</span></span>

  - [<span data-ttu-id="31a75-112">Exportar un archivo de configuración de la ruta de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31a75-112">Export a voice route configuration file in Lync Server 2013</span></span>](lync-server-2013-export-a-voice-route-configuration-file.md)

  - [<span data-ttu-id="31a75-113">Importar un archivo de configuración de enrutamiento de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31a75-113">Import a voice route configuration file in Lync Server 2013</span></span>](lync-server-2013-import-a-voice-route-configuration-file.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="31a75-114">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="31a75-114">Related Sections</span></span>

<span data-ttu-id="31a75-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31a75-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

