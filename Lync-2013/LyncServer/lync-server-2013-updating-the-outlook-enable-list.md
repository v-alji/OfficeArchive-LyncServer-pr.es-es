---
title: 'Lync Server 2013: actualización de la lista de habilitación de Outlook'
description: 'Lync Server 2013: actualización de la lista de habilitaciones de Outlook.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Updating the Outlook enable list
ms:assetid: 5db120dc-52f9-4dde-acb9-3824ae245086
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215438(v=OCS.15)
ms:contentKeyID: 48242739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96edc327fa1b63d5da95eb6ea36a2296659910d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399473"
---
# <a name="updating-the-outlook-enable-list-in-lync-server-2013"></a><span data-ttu-id="78916-103">Actualización de la lista de habilitación de Outlook en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78916-103">Updating the Outlook enable list in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78916-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78916-104">

<span> </span></span></span>

<span data-ttu-id="78916-105">_**Última modificación del tema:** 2013-01-07_</span><span class="sxs-lookup"><span data-stu-id="78916-105">_**Topic Last Modified:** 2013-01-07_</span></span>

<span data-ttu-id="78916-106">Puede asegurarse de que el complemento de reuniones en línea para Microsoft Lync 2013 permanezca siempre habilitado para los usuarios mediante la creación de una directiva que lo incluya en la lista de administración de complementos para Outlook.</span><span class="sxs-lookup"><span data-stu-id="78916-106">You can ensure that Online Meeting Add-in for Microsoft Lync 2013 always remains enabled for users by creating a policy that includes it in the Add-in Management List for Outlook.</span></span> <span data-ttu-id="78916-107">La Directiva de lista de administración de complementos se incluye en los archivos de plantillas administrativas de Office para la consola de administración de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="78916-107">The Add-in Management List policy is included in the Office administrative template files for the Group Policy Management Console.</span></span> <span data-ttu-id="78916-108">Crea una clave del registro en HKCU \\ software \\ Policies \\ Microsoft \\ Office \\ 15,0 \\ Outlook15 \\ Resiliency \\ AddinList.</span><span class="sxs-lookup"><span data-stu-id="78916-108">It creates a registry key under HKCU\\Software\\Policies\\Microsoft\\Office\\15.0\\Outlook15\\Resiliency\\AddinList.</span></span> <span data-ttu-id="78916-109">Puede Agregar un valor para el ucaddin.dll a esta clave y configurar el valor de ucaddin.dll para que esté siempre habilitado y para que los usuarios no puedan deshabilitarlo manualmente</span><span class="sxs-lookup"><span data-stu-id="78916-109">You can add a value for the ucaddin.dll to this key, and configure the ucaddin.dll value so that it is always enabled and so that users cannot manually disable it</span></span>

<div>

## <a name="to-add-ucaddindll-to-the-outlook-add-in-list"></a><span data-ttu-id="78916-110">Para agregar ucaddin.dll a la lista de complementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="78916-110">To Add ucaddin.dll to the Outlook Add-in List</span></span>

  - <span data-ttu-id="78916-111">Para la clave del registro AddinList, que se encuentra en la sección \\ directivas de software HKCU \\ \\ Microsoft \\ Office \\ 15,0 \\ Outlook15 \\ Resiliency \\ AddinList, agregue el siguiente valor:</span><span class="sxs-lookup"><span data-stu-id="78916-111">To the AddinList registry key, located under HKCU\\Software\\Policies\\Microsoft\\Office\\15.0\\Outlook15\\Resiliency\\AddinList, add the following value:</span></span>
    
      - <span data-ttu-id="78916-112">Tipo de registro = REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="78916-112">Registry Type = REG\_SZ</span></span>
    
      - <span data-ttu-id="78916-113">Name = ucaddin.dll</span><span class="sxs-lookup"><span data-stu-id="78916-113">Name = ucaddin.dll</span></span>
    
      - <span data-ttu-id="78916-114">Valor = 1 (especifica que el complemento está siempre habilitado y que el usuario final no puede administrarlo)</span><span class="sxs-lookup"><span data-stu-id="78916-114">Value = 1 (specifies that the add-in is always enabled and cannot be managed by the end user)</span></span>

<span data-ttu-id="78916-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78916-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

