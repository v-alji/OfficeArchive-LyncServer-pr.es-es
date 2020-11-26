---
title: 'Lync Server 2013: copia de seguridad de los almacenes de archivos'
description: 'Lync Server 2013: copia de seguridad de los almacenes de archivos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up file stores
ms:assetid: 1a7f4e93-aa3d-461e-878e-2c572baa1293
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202167(v=OCS.15)
ms:contentKeyID: 51541449
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba6a92d189c39242be1b2167ffc336d9eb406719
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438053"
---
# <a name="backing-up-file-stores-in-lync-server-2013"></a><span data-ttu-id="199a5-103">Copia de seguridad de almacenes de archivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="199a5-103">Backing up file stores in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="199a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="199a5-104">

<span> </span></span></span>

<span data-ttu-id="199a5-105">_**Última modificación del tema:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="199a5-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="199a5-106">La copia de seguridad de los almacenes de archivos de Lync Server incluye todos los archivos y carpetas que usan los componentes de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="199a5-106">Backing up the Lync Server File Stores includes all the files and folders used by Lync Server components.</span></span>

<div>

## <a name="to-back-up-file-stores"></a><span data-ttu-id="199a5-107">Para hacer una copia de seguridad de los almacenes de archivos</span><span class="sxs-lookup"><span data-stu-id="199a5-107">To back up File Stores</span></span>

1.  <span data-ttu-id="199a5-108">Para buscar las ubicaciones específicas de los almacenes de archivos de Lync Server, abra el generador de topologías y mire en el nodo **almacenes de archivos** .</span><span class="sxs-lookup"><span data-stu-id="199a5-108">To find the specific locations of your Lync Server File Stores, open Topology Builder and look in the **File stores** node.</span></span>

2.  <span data-ttu-id="199a5-109">Use Robocopy u otra herramienta de administración del sistema de archivos para copiar cada almacén de archivos en $Backup almacén de archivos \\ .</span><span class="sxs-lookup"><span data-stu-id="199a5-109">Use Robocopy or another file system management tool to copy each File Store to $Backup\\filestore.</span></span>

<span data-ttu-id="199a5-110"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="199a5-110"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

