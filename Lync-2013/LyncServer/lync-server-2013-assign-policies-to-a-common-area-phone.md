---
title: 'Lync Server 2013: asignar directivas a un teléfono de área común'
description: 'Lync Server 2013: asigne directivas a un teléfono de área común.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign policies to a common area phone
ms:assetid: f0554fd1-b237-49b3-9eb4-26f4b91f5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994082(v=OCS.15)
ms:contentKeyID: 51803993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe437ec87ba30eff834239db2b4815adb2d5718c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438319"
---
# <a name="assign-policies-in-lync-server-2013-to-a-common-area-phone"></a><span data-ttu-id="dd289-103">Asignar directivas en Lync Server 2013 a un teléfono de área común</span><span class="sxs-lookup"><span data-stu-id="dd289-103">Assign policies in Lync Server 2013 to a common area phone</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dd289-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dd289-104">

<span> </span></span></span>

<span data-ttu-id="dd289-105">_**Última modificación del tema:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="dd289-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="dd289-106">Después de crear la Directiva para teléfonos de área común (para obtener información detallada, consulte [crear una directiva de voz y configurar registros de uso de RTC en Lync Server 2013](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)), puede asignar la Directiva a un teléfono de área común mediante Windows PowerShell y el cmdlet **Grant-CS** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="dd289-106">After you create your policy for common area phones (for details, see [Create a voice policy and configure PSTN usage records in Lync Server 2013](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)), you can assign the policy to a common area phone by using Windows PowerShell and the appropriate **Grant-Cs** cmdlet.</span></span> <span data-ttu-id="dd289-107">Estos cmdlets se pueden ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd289-107">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="dd289-108">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="dd289-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="assigning-a-policy-to-a-single-common-area-phone"></a><span data-ttu-id="dd289-109">Asignar una directiva a un solo teléfono de área común</span><span class="sxs-lookup"><span data-stu-id="dd289-109">Assigning a Policy to a Single Common Area Phone</span></span>

  - <span data-ttu-id="dd289-110">El comando siguiente asigna la Directiva de voz por usuario RedmondVoice al teléfono de área común que tiene la firma de la compilación 14 de la identidad.</span><span class="sxs-lookup"><span data-stu-id="dd289-110">The following command assigns the per-user voice policy RedmondVoice to the common area phone that has the Identity Building 14 Lobby.</span></span>
    
        Grant-CsVoicePolicy -Identity "Building 14 Lobby" -PolicyName "RedmondVoicePolicy"

</div>

<div>

## <a name="assigning-a-policy-to-multiple-common-area-phones"></a><span data-ttu-id="dd289-111">Asignación de una directiva a varios teléfonos de área común</span><span class="sxs-lookup"><span data-stu-id="dd289-111">Assigning a Policy to Multiple Common Area Phones</span></span>

  - <span data-ttu-id="dd289-112">En este ejemplo, la Directiva de voz por usuario RedmondVoice se asigna a todos los teléfonos de área común configurados para su uso en la organización.</span><span class="sxs-lookup"><span data-stu-id="dd289-112">In this example, the per-user voice policy RedmondVoice is assigned to all the common area phones configured for use in the organization.</span></span>
    
        Get-CsCommonAreaPhone | Grant-CsVoicePolicy  -PolicyName "RedmondVoicePolicy"

</div>

<span data-ttu-id="dd289-113">Para obtener más información, consulte los temas de ayuda para la [concesión-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsVoicePolicy).</span><span class="sxs-lookup"><span data-stu-id="dd289-113">For details, see the Help topics for the [Grant-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsVoicePolicy).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dd289-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd289-114">See Also</span></span>


[<span data-ttu-id="dd289-115">Get-CsCommonAreaPhone</span><span class="sxs-lookup"><span data-stu-id="dd289-115">Get-CsCommonAreaPhone</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone)  
  

<span data-ttu-id="dd289-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dd289-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

