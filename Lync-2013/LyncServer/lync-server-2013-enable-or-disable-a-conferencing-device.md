---
title: 'Lync Server 2013: habilitar o deshabilitar un dispositivo de conferencia'
description: 'Lync Server 2013: habilitar o deshabilitar un dispositivo de conferencia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable a conferencing device
ms:assetid: d5140e38-d015-4706-9bde-cf2fa748c36b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994070(v=OCS.15)
ms:contentKeyID: 51803981
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 761bc19536c889cced68ff586753f6800df0da59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437577"
---
# <a name="enable-or-disable-a-conferencing-device-in-lync-server-2013"></a><span data-ttu-id="09657-103">Habilitar o deshabilitar un dispositivo de conferencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09657-103">Enable or disable a conferencing device in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09657-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09657-104">

<span> </span></span></span>

<span data-ttu-id="09657-105">_**Última modificación del tema:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="09657-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="09657-106">Habilitar y deshabilitar un dispositivo de Conferencia mediante el cmdlet **enable-CsMeetingRoom** y el cmdlet **Disable-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="09657-106">Enable and disable a conferencing device by using the **Enable-CsMeetingRoom** cmdlet and the **Disable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="09657-107">Estos cmdlets se pueden ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09657-107">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="09657-108">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="09657-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="enabling-a-conferencing-device"></a><span data-ttu-id="09657-109">Habilitar un dispositivo de conferencia</span><span class="sxs-lookup"><span data-stu-id="09657-109">Enabling a Conferencing Device</span></span>

  - <span data-ttu-id="09657-110">Para habilitar un dispositivo de conferencia, use el cmdlet **enable-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="09657-110">To enable a conferencing device, use the **Enable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="09657-111">Al habilitar un dispositivo de conferencia, debe incluir una) la identidad del dispositivo de conferencia, b) el registrador en el que se va a alojar la cuenta de sala, y c) la dirección SIP que se va a asignar a esa cuenta.</span><span class="sxs-lookup"><span data-stu-id="09657-111">When enabling a conferencing device, you must include a) the conferencing device identity, b) the Registrar pool where the room account will be homed, and c) the SIP address to be assigned to that account.</span></span>
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="disabling-a-conferencing-device"></a><span data-ttu-id="09657-112">Deshabilitar un dispositivo de conferencia</span><span class="sxs-lookup"><span data-stu-id="09657-112">Disabling a Conferencing Device</span></span>

  - <span data-ttu-id="09657-113">Para deshabilitar un dispositivo de conferencia, use el cmdlet **Disable-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="09657-113">To disable a conferencing device, use the **Disable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="09657-114">Asegúrese de especificar la identidad del dispositivo de conferencia que se va a deshabilitar:</span><span class="sxs-lookup"><span data-stu-id="09657-114">Make sure that you specify the identity of the conferencing device to be disabled:</span></span>
    
        Disable-CsMeetingRoom -Identity "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<span data-ttu-id="09657-115">Para obtener más información, consulte los temas de ayuda para el cmdlet [enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) y el cmdlet [Disable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Disable-CsMeetingRoom) .</span><span class="sxs-lookup"><span data-stu-id="09657-115">For details, see the Help topics for the [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) cmdlet and the [Disable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Disable-CsMeetingRoom) cmdlet.</span></span>

<span data-ttu-id="09657-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09657-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

