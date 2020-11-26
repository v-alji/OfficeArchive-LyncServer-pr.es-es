---
title: 'Lync Server 2013: Implementar archivado'
description: 'Lync Server 2013: implementación del archivado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Archiving
ms:assetid: a89edd16-12d5-4602-ad2f-194b47d1188e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205147(v=OCS.15)
ms:contentKeyID: 48185031
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4ba38b7dcde0c72469e361f59ade7cb7f6ebb53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430108"
---
# <a name="deploying-archiving-in-lync-server-2013"></a><span data-ttu-id="39b9d-103">Implementar archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39b9d-103">Deploying Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39b9d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39b9d-104">

<span> </span></span></span>

<span data-ttu-id="39b9d-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="39b9d-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="39b9d-106">Lync Server 2013 ofrece una solución para archivar contenido y comunicaciones de conferencia de mensajería instantánea en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="39b9d-106">Lync Server 2013 provides a solution for archiving instant messaging (IM) content and conferencing communications in Lync Server.</span></span> <span data-ttu-id="39b9d-107">Puede implementar la compatibilidad de archivado mediante la integración del almacenamiento de archivado con el almacenamiento de Exchange 2013, mediante el uso de bases de datos de SQL Server para el almacenamiento de datos de archivado de Lync Server 2013, o bien mediante Lync Server 2013 y almacenamiento de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="39b9d-107">You can implement archiving support by integrating archiving storage with Exchange 2013 storage, by using SQL Server databases for storage of Lync Server 2013 archiving data, or by using both Lync Server 2013 and Exchange 2013 storage.</span></span> <span data-ttu-id="39b9d-108">Usted controla cómo se archivan los datos con las directivas y las configuraciones de archivado.</span><span class="sxs-lookup"><span data-stu-id="39b9d-108">You control how data is archived using policies and archiving configurations.</span></span> <span data-ttu-id="39b9d-109">Para obtener más información, consulte [planeamiento de archivado en Lync server 2013](lync-server-2013-planning-for-archiving.md) en la documentación de planeación y [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, la documentación de implementación o la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="39b9d-109">For details, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation and [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<span data-ttu-id="39b9d-110">Puede usar la información de esta sección para configurar y configurar el archivado inicialmente.</span><span class="sxs-lookup"><span data-stu-id="39b9d-110">You can use the information in this section to set up and configure Archiving initially.</span></span> <span data-ttu-id="39b9d-111">Después de la implementación, puede cambiar la configuración de archivado.</span><span class="sxs-lookup"><span data-stu-id="39b9d-111">After deployment, you can change Archiving settings.</span></span> <span data-ttu-id="39b9d-112">Para obtener más información sobre cómo implementar el soporte de archivado para la administración diaria o para cumplir los nuevos requisitos de su organización, vea [administrar el archivado de Lync Server 2013](lync-server-2013-managing-archiving.md) en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="39b9d-112">For details about how you implement archiving support for day-to-day management or to meet new requirements in your organization, see [Managing Lync Server 2013 Archiving](lync-server-2013-managing-archiving.md) in the Operations documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="39b9d-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="39b9d-113">In This Section</span></span>

  - [<span data-ttu-id="39b9d-114">Cómo funciona el archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39b9d-114">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)

  - [<span data-ttu-id="39b9d-115">Lista de comprobación para la implementación del archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39b9d-115">Deployment checklist for Archiving in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-archiving.md)

  - [<span data-ttu-id="39b9d-116">Configurar sistemas e infraestructura para archivar en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39b9d-116">Setting up systems and infrastructure for Archiving in Lync Server 2013</span></span>](lync-server-2013-setting-up-systems-and-infrastructure-for-archiving.md)

  - [<span data-ttu-id="39b9d-117">Agregar bases de datos de archivado a una implementación existente de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39b9d-117">Adding Archiving databases to an existing Lync Server 2013 Deployment</span></span>](lync-server-2013-adding-archiving-databases-to-an-existing-lync-server-2013-deployment.md)

  - [<span data-ttu-id="39b9d-118">Configuración de la compatibilidad con el archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39b9d-118">Configuring support for Archiving in Lync Server 2013</span></span>](lync-server-2013-configuring-support-for-archiving.md)

<span data-ttu-id="39b9d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39b9d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

