---
title: 'Lync Server 2013: cmdlets del servidor de libreta de direcciones'
description: 'Lync Server 2013: cmdlets del servidor de libreta de direcciones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Address Book Server cmdlets
ms:assetid: 33da45da-3c57-4d04-9679-f0e5a0cfd37e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415643(v=OCS.15)
ms:contentKeyID: 48183793
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e4fef903d25f0d2707410e017f4eb280282bbdab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439999"
---
# <a name="address-book-server-cmdlets-in-lync-server-2013"></a><span data-ttu-id="fe7b8-103">Cmdlets del servidor de la libreta de direcciones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fe7b8-103">Address Book Server cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fe7b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fe7b8-104">

<span> </span></span></span>

<span data-ttu-id="fe7b8-105">_**Última modificación del tema:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="fe7b8-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="fe7b8-106">Los servidores de la libreta de direcciones son intermediarios entre los servicios de dominio de Active Directory y Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fe7b8-106">Address Book servers are intermediaries between Active Directory Domain Services and Microsoft Lync Server 2013.</span></span> <span data-ttu-id="fe7b8-107">El servidor de la libreta de direcciones garantiza que la información del usuario almacenada en Lync Server 2013 está sincronizada con la información de usuario almacenada en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fe7b8-107">The Address Book server ensures that the user information stored in Lync Server 2013 is in synch with the user information stored in Active Directory.</span></span> <span data-ttu-id="fe7b8-108">Esto se realiza mediante la sincronización periódica de archivos de libreta de direcciones con información almacenada en la base de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="fe7b8-108">This is done by periodically synching Address Book files with information stored in the User database.</span></span> <span data-ttu-id="fe7b8-109">A su vez, Lync Server incluye varios cmdlets para administrar servidores de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="fe7b8-109">In turn, Lync Server includes a number of cmdlets for managing Address Book servers.</span></span>

<div>

## <a name="address-book-server-cmdlets"></a><span data-ttu-id="fe7b8-110">Cmdlets del servidor de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="fe7b8-110">Address Book Server Cmdlets</span></span>

<span data-ttu-id="fe7b8-111">No puede configurar la configuración del servidor de la libreta de direcciones en el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe7b8-111">You cannot configure the Address Book Server settings in Lync Server Control Panel.</span></span> <span data-ttu-id="fe7b8-112">Windows PowerShell es la herramienta principal para administrar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="fe7b8-112">Windows PowerShell is the primary tool for managing these settings.</span></span> <span data-ttu-id="fe7b8-113">A continuación se muestra una lista de cmdlets que se relacionan directamente con la administración del servidor de la libreta de direcciones:</span><span class="sxs-lookup"><span data-stu-id="fe7b8-113">The following is a list of cmdlets that relate directly to managing the Address Book Server:</span></span>

<span data-ttu-id="fe7b8-114">**Servidor de libreta de direcciones**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-114">**Address Book Server**</span></span>

  - <span></span>  
    <span data-ttu-id="fe7b8-115">[Get-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398132(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="fe7b8-115">[Get-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398132(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="fe7b8-116">[Nuevo: CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398395(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="fe7b8-116">[New-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398395(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="fe7b8-117">[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="fe7b8-117">[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="fe7b8-118">[Set-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg412784(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="fe7b8-118">[Set-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg412784(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="fe7b8-119">[Update-CsAddressBook](https://technet.microsoft.com/library/Gg398194(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="fe7b8-119">[Update-CsAddressBook](https://technet.microsoft.com/library/Gg398194(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="fe7b8-120">[Debug-CsAddressBookReplication](https://technet.microsoft.com/library/JJ205232(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="fe7b8-120">[Debug-CsAddressBookReplication](https://technet.microsoft.com/library/JJ205232(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="fe7b8-121">[Prueba-CsAddressBookService](https://technet.microsoft.com/library/Gg398661(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="fe7b8-121">[Test-CsAddressBookService](https://technet.microsoft.com/library/Gg398661(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="fe7b8-122">[Test-CsAddressBookWebQuery](https://technet.microsoft.com/library/Gg398773(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="fe7b8-122">[Test-CsAddressBookWebQuery](https://technet.microsoft.com/library/Gg398773(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fe7b8-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe7b8-123">See Also</span></span>


[<span data-ttu-id="fe7b8-124">Blog de Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe7b8-124">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="fe7b8-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fe7b8-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

