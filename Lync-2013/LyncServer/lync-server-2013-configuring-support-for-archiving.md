---
title: 'Lync Server 2013: configuración de la compatibilidad con el archivado'
description: 'Lync Server 2013: configuración de la compatibilidad con el archivado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring support for Archiving
ms:assetid: 579283fe-909c-46f2-a0c9-52ca1e7d63d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204905(v=OCS.15)
ms:contentKeyID: 48184187
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4209614ed1248ab0caf3cf438a922d569ba79630
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432635"
---
# <a name="configuring-support-for-archiving-in-lync-server-2013"></a><span data-ttu-id="6ae97-103">Configuración de la compatibilidad con el archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ae97-103">Configuring support for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ae97-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ae97-104">

<span> </span></span></span>

<span data-ttu-id="6ae97-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="6ae97-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="6ae97-106">Después de agregar el archivado a la topología y publicar la nueva topología, debe configurar las opciones para el modo en que el archivado se implementa inicialmente en la implementación y, a continuación, configurar una o más directivas de archivado para habilitar el archivado de la implementación y, opcionalmente, para usuarios y sitios específicos.</span><span class="sxs-lookup"><span data-stu-id="6ae97-106">After adding Archiving to your topology and publishing the new topology, you need to configure options for how Archiving is initially implemented in your deployment, and then configure one or more Archiving policies to enable Archiving for your deployment and, optionally, for specific sites and users.</span></span> <span data-ttu-id="6ae97-107">Puede usar el panel de control de Lync Server 2013 para realizar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="6ae97-107">You can use Lync Server 2013 Control Panel to do this.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6ae97-108">Después de la implementación, puede cambiar la configuración de archivado para habilitar o deshabilitar el archivado.</span><span class="sxs-lookup"><span data-stu-id="6ae97-108">After deployment, you can change Archiving settings to disable or enable Archiving.</span></span> <span data-ttu-id="6ae97-109">Para obtener más información sobre cómo implementar el soporte técnico para la administración diaria o para cumplir nuevos requisitos de la organización después de la implementación, consulte <A href="lync-server-2013-managing-archiving.md">administrar el archivado de Lync Server 2013</A> en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="6ae97-109">For details about how to implement archiving support for day-to-day management or to meet new requirements in your organization after deployment, see <A href="lync-server-2013-managing-archiving.md">Managing Lync Server 2013 Archiving</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6ae97-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6ae97-110">In This Section</span></span>

  - [<span data-ttu-id="6ae97-111">Configuración de las opciones de archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ae97-111">Configuring Archiving options in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options.md)

  - [<span data-ttu-id="6ae97-112">Configurar y asignar directivas de archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ae97-112">Configuring and assigning Archiving policies in Lync Server 2013</span></span>](lync-server-2013-configuring-and-assigning-archiving-policies.md)

  - [<span data-ttu-id="6ae97-113">Habilitar o deshabilitar el envío de una renuncia de archivado a socios federados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ae97-113">Enable or disable sending an Archiving disclaimer to federated partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md)

<span data-ttu-id="6ae97-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ae97-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

