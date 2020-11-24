---
title: 'Lync Server 2013: eliminar un objeto de contacto telefónico de área común'
description: 'Lync Server 2013: eliminar un objeto de contacto telefónico de área común.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a common area phone Contact object
ms:assetid: f4c139dc-f07c-4c75-9345-e291aea41173
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994087(v=OCS.15)
ms:contentKeyID: 51803999
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e918f7a46269f70577f28b2c3e55297959430721
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399870"
---
# <a name="delete-a-common-area-phone-contact-object-in-lync-server-2013"></a><span data-ttu-id="4cda4-103">Eliminar un objeto de contacto telefónico de área común en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cda4-103">Delete a common area phone Contact object in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4cda4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4cda4-104">

<span> </span></span></span>

<span data-ttu-id="4cda4-105">_**Última modificación del tema:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="4cda4-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="4cda4-106">Es posible que desee eliminar el objeto de contacto asociado a un teléfono de área común.</span><span class="sxs-lookup"><span data-stu-id="4cda4-106">You might want to delete the contact object associated with a common area phone.</span></span> <span data-ttu-id="4cda4-107">Por ejemplo, si quitas el teléfono de la sala de un empleado, no es necesario que tengas un objeto de contacto asociado con ese teléfono.</span><span class="sxs-lookup"><span data-stu-id="4cda4-107">For example, if you remove the phone from an employee lounge, there’s no need to have a contact object associated with that phone.</span></span> <span data-ttu-id="4cda4-108">El cmdlet **Remove-CsCommonAreaPhone** le permite eliminar cuentas de teléfono de área común.</span><span class="sxs-lookup"><span data-stu-id="4cda4-108">The **Remove-CsCommonAreaPhone** cmdlet provides a way for you to delete common area phone accounts.</span></span> <span data-ttu-id="4cda4-109">Al ejecutar este cmdlet, el teléfono se elimina de la lista de teléfonos de área común devuelto por **Get-CsCommonAreaPhone**.</span><span class="sxs-lookup"><span data-stu-id="4cda4-109">When you run this cmdlet, the phone is deleted from the list of common area phones returned by **Get-CsCommonAreaPhone**.</span></span> <span data-ttu-id="4cda4-110">Además, el objeto de contacto asociado con ese teléfono se eliminará de los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4cda4-110">In addition, the contact object associated with that phone is deleted from Active Directory Domain Services.</span></span>

<span data-ttu-id="4cda4-111">Usa **Remove-CsCommonAreaPhone** para quitar un teléfono de área común o todos los teléfonos de área común que tengan un elemento común, como un nombre para mostrar o un código de área y país.</span><span class="sxs-lookup"><span data-stu-id="4cda4-111">Use **Remove-CsCommonAreaPhone** to remove one common area phone or all common area phones that have a common element, such as a display name or country and area code.</span></span> <span data-ttu-id="4cda4-112">Puede ejecutar este cmdlet desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4cda4-112">You can run this cmdlet from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="4cda4-113">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="4cda4-113">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="removing-a-specified-common-area-phone"></a><span data-ttu-id="4cda4-114">Quitar un teléfono de área común especificado</span><span class="sxs-lookup"><span data-stu-id="4cda4-114">Removing a Specified Common Area Phone</span></span>

  - <span data-ttu-id="4cda4-115">El siguiente comando quita el teléfono de área común con la dirección SIP sip:mainlobby@litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="4cda4-115">The following command removes the common area phone with the SIP address sip:mainlobby@litwareinc.com:</span></span>
    
        Remove-CsCommonAreaPhone -Identity "sip:mainlobby@litwareinc.com"

</div>

<div>

## <a name="removing-common-area-phones-based-on-their-display-name"></a><span data-ttu-id="4cda4-116">Quitar teléfonos de área común en función de su nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="4cda4-116">Removing Common Area Phones Based on Their Display Name</span></span>

  - <span data-ttu-id="4cda4-117">Este comando quita todos los teléfonos comunes del área donde el nombre para mostrar incluye el valor de cadena "edificio 14":</span><span class="sxs-lookup"><span data-stu-id="4cda4-117">This command removes all the common area phones where the display name includes the string value "Building 14":</span></span>
    
        Get-CsCommonAreaPhone | Where-Object {$_.DisplayName -match "Building 14"} | Remove-CsCommonAreaPhone

</div>

<div>

## <a name="removing-common-area-phones-based-on-their-country-and-area-codes"></a><span data-ttu-id="4cda4-118">Quitar teléfonos de área comunes en función de sus códigos de área y país</span><span class="sxs-lookup"><span data-stu-id="4cda4-118">Removing Common Area Phones Based on Their Country and Area Codes</span></span>

  - <span data-ttu-id="4cda4-119">Este comando elimina todos los teléfonos comunes de las áreas de los Estados Unidos (código de país 1) y el código de área 425:</span><span class="sxs-lookup"><span data-stu-id="4cda4-119">This command removes all the common area phones for the United States (country code 1) and the area code 425:</span></span>
    
        Get-CsCommonAreaPhone | Where-Object {$_.LineUri  -match "^tel:\+1425"} | Remove-CsCommonAreaPhone

</div>

<span data-ttu-id="4cda4-120">Para obtener más información, vea el tema de ayuda sobre el cmdlet [Remove-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Remove-CsCommonAreaPhone) .</span><span class="sxs-lookup"><span data-stu-id="4cda4-120">For details, see the Help topic for the [Remove-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Remove-CsCommonAreaPhone) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4cda4-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cda4-121">See Also</span></span>


[<span data-ttu-id="4cda4-122">Get-CsCommonAreaPhone</span><span class="sxs-lookup"><span data-stu-id="4cda4-122">Get-CsCommonAreaPhone</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone)  
  

<span data-ttu-id="4cda4-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4cda4-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

