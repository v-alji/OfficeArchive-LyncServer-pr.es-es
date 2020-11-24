---
title: 'Lync Server 2013: crear o modificar un objeto de contacto de dispositivo de conferencia'
description: 'Lync Server 2013: crear o modificar un objeto de contacto de dispositivos de conferencia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a conferencing device Contact object
ms:assetid: 62ed64be-379c-417d-9453-511881cf5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994035(v=OCS.15)
ms:contentKeyID: 51803945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 853ee1c7dfda2fda99431b8cc1a5210a51f39a4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398777"
---
# <a name="create-or-modify-a-conferencing-device-contact-object-in-lync-server-2013"></a><span data-ttu-id="8f4be-103">Crear o modificar un objeto de contacto de dispositivo de conferencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f4be-103">Create or modify a conferencing device Contact object in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f4be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f4be-104">

<span> </span></span></span>

<span data-ttu-id="8f4be-105">_**Última modificación del tema:** 2013-10-02_</span><span class="sxs-lookup"><span data-stu-id="8f4be-105">_**Topic Last Modified:** 2013-10-02_</span></span>

<span data-ttu-id="8f4be-106">Para crear un objeto de sala de conferencias, primero debe crear una cuenta de usuario de Active Directory para representar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f4be-106">To create a conferencing room object, first create an Active Directory user account to represent the device.</span></span> <span data-ttu-id="8f4be-107">A continuación, use el cmdlet **enable-CsMeetingRoom** para habilitar esa cuenta como dispositivo de conferencia.</span><span class="sxs-lookup"><span data-stu-id="8f4be-107">Then, use the **Enable-CsMeetingRoom** cmdlet to enable that account to function as a conferencing device.</span></span> <span data-ttu-id="8f4be-108">Si necesita cambiar las propiedades de un dispositivo de conferencia existente, use el cmdlet **set-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="8f4be-108">If you need to change the properties of an existing conferencing device, use the **Set-CsMeetingRoom** cmdlet.</span></span>

<span data-ttu-id="8f4be-109">Estos cmdlets se pueden ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8f4be-109">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8f4be-110">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="8f4be-110">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="creating-a-conferencing-device"></a><span data-ttu-id="8f4be-111">Crear un dispositivo de conferencia</span><span class="sxs-lookup"><span data-stu-id="8f4be-111">Creating a Conferencing Device</span></span>

  - <span data-ttu-id="8f4be-112">Después de crear la cuenta de usuario de Active Directory que representa el nuevo dispositivo de conferencia, habilítelo mediante el cmdlet **enable-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="8f4be-112">After you create the Active Directory user account that represents the new conferencing device, enable it by using the **Enable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="8f4be-113">Asegúrese de incluir a la identidad del dispositivo de conferencia, b) el grupo registrador en el que se va a alojar la cuenta de sala, y c) la dirección SIP que se va a asignar a esa cuenta.</span><span class="sxs-lookup"><span data-stu-id="8f4be-113">Be sure to include a) the conferencing device identity, b) the registrar pool where the room account will be homed, and c) the SIP address to be assigned to that account.</span></span> <span data-ttu-id="8f4be-114">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8f4be-114">For example:</span></span>
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="modifying-a-conferencing-device"></a><span data-ttu-id="8f4be-115">Modificar un dispositivo de conferencia</span><span class="sxs-lookup"><span data-stu-id="8f4be-115">Modifying a Conferencing Device</span></span>

  - <span data-ttu-id="8f4be-116">Para modificar los valores de propiedad de un dispositivo de conferencia existente, use el cmdlet **set-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="8f4be-116">To modify the property values of an existing conferencing device, use the **Set-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="8f4be-117">Por ejemplo, el siguiente comando actualiza el número de teléfono (LineUri) asociado a un dispositivo de Conferencia:</span><span class="sxs-lookup"><span data-stu-id="8f4be-117">For example, the following command updates the phone number (LineUri) associated with a conferencing device:</span></span>
    
        Set-CsMeetingRoom -Identity "Redmond Conferencing device" -LineUri "tel:+12065551219"

</div>

<span data-ttu-id="8f4be-118">Para obtener más información, consulte los temas de ayuda para el cmdlet [enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) y el cmdlet [set-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Set-CsMeetingRoom) .</span><span class="sxs-lookup"><span data-stu-id="8f4be-118">For details, see the Help topics for the [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) cmdlet and the [Set-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Set-CsMeetingRoom) cmdlet.</span></span>

<span data-ttu-id="8f4be-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f4be-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

