---
title: Migrar teléfonos de área común
description: Migrar teléfonos de área común.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Common Area Phones
ms:assetid: 31bd26fc-861b-45c6-8221-18df16e575de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688015(v=OCS.15)
ms:contentKeyID: 49733604
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b8df4d94a3db3274df7e4e82ed2185c3626de12
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443828"
---
# <a name="migrate-common-area-phones"></a><span data-ttu-id="f71ed-103">Migrar teléfonos de área común</span><span class="sxs-lookup"><span data-stu-id="f71ed-103">Migrate Common Area Phones</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f71ed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f71ed-104">

<span> </span></span></span>

<span data-ttu-id="f71ed-105">_**Última modificación del tema:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="f71ed-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="f71ed-106">Los teléfonos de área común son teléfonos IP que suelen residir en un área de trabajo compartida o en un área común, como un vestíbulo, una cocina o una fábrica.</span><span class="sxs-lookup"><span data-stu-id="f71ed-106">Common Area Phones are IP phones that most often reside in a shared workspace or common area, like a lobby, kitchen, or factory floor.</span></span> <span data-ttu-id="f71ed-107">No es necesario que los teléfonos de área común estén conectados a un equipo para proporcionar la funcionalidad de UC de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f71ed-107">Common Area Phones do not need to be connected to a computer to provide Lync Server UC functionality.</span></span> <span data-ttu-id="f71ed-108">Después de migrar una implementación de Lync Server 2010 a Lync Server 2013, también debe migrar los objetos de contacto asociados con el teléfono de área común heredado.</span><span class="sxs-lookup"><span data-stu-id="f71ed-108">After migrating an Lync Server 2010 deployment to Lync Server 2013, you must also migrate the contact objects associated with the legacy Common Area Phone.</span></span> <span data-ttu-id="f71ed-109">Usar el shell de administración de Lync Server primero se recuperarán todos los objetos de contacto asociados a los teléfonos de área común de Lync Server 2010 y, a continuación, se moverán esos objetos al grupo de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f71ed-109">Using Lync Server Management Shell you will first retrieve all contact objects associated with the Lync Server 2010 Common Area Phones, and then move those objects to the Lync Server 2013 pool.</span></span>

<span data-ttu-id="f71ed-110">**Migrar teléfonos de área común**</span><span class="sxs-lookup"><span data-stu-id="f71ed-110">**Migrate Common Area Phones**</span></span>

1.  <span data-ttu-id="f71ed-111">En el servidor front-end de Lync Server 2013, abra el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f71ed-111">From the Lync Server 2013 Front End server, open Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="f71ed-112">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f71ed-112">From the command line, type the following:</span></span>
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsCommonAreaPhone -Target pool02.contoso.net

3.  <span data-ttu-id="f71ed-113">Para comprobar que todos los objetos de contacto se han movido al grupo de 2013 de Lync Server, escriba lo siguiente en el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="f71ed-113">To verify all contact objects have been moved to the Lync Server 2013 pool, from the Lync Server Management Shell type the following:</span></span>
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool02.contoso.net"}
    
    <span data-ttu-id="f71ed-114">Compruebe que todos los objetos de contacto estén ahora asociados con el grupo de servidores de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f71ed-114">Verify all contact objects are now associated with the Lync Server 2013 pool.</span></span>

<span data-ttu-id="f71ed-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f71ed-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

