---
title: 'Lync Server 2013: modificar la Directiva de correo de voz hospedado global'
description: 'Lync Server 2013: modificar la Directiva de correo de voz hospedado global.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the global hosted voice mail policy
ms:assetid: f059b3ce-a7d8-4ea9-b10b-0052222ec2ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412994(v=OCS.15)
ms:contentKeyID: 48185757
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9cd5e16c78049ce79abd936a79b2025a14e45943
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445704"
---
# <a name="modify-the-global-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="7ad0f-103">Modificar la Directiva de correo de voz hospedado global en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ad0f-103">Modify the global hosted voice mail policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ad0f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ad0f-104">

<span> </span></span></span>

<span data-ttu-id="7ad0f-105">_**Última modificación del tema:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="7ad0f-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="7ad0f-106">La Directiva de correo de voz hospedado *global* se instala con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-106">The *global* hosted voice mail policy is installed with Lync Server 2013.</span></span> <span data-ttu-id="7ad0f-107">Puede modificarla para satisfacer sus necesidades, pero no puede cambiarle el nombre ni eliminarla.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-107">You can modify it to meet your needs, but you cannot rename or delete it.</span></span> <span data-ttu-id="7ad0f-108">Para modificar la directiva global, use el cmdlet Set-CsHostedVoicemailPolicy para establecer los parámetros en los valores adecuados para su implementación específica.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-108">To modify the global policy, you use the Set-CsHostedVoicemailPolicy cmdlet to set the parameters to appropriate values for your specific deployment.</span></span>

<span data-ttu-id="7ad0f-109">Para obtener más información sobre el cmdlet [set-CsHostedVoicemailPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy) , consulte la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-109">For details about the [Set-CsHostedVoicemailPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy) cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div>

## <a name="to-modify-the-global-hosted-voice-mail-policy"></a><span data-ttu-id="7ad0f-110">Para modificar la Directiva de correo de voz hospedado global</span><span class="sxs-lookup"><span data-stu-id="7ad0f-110">To modify the global hosted voice mail policy</span></span>

1.  <span data-ttu-id="7ad0f-111">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="7ad0f-112">Ejecute el cmdlet Set-CsHostedVoicemailPolicy para establecer los parámetros de la directiva global de su entorno.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-112">Run the Set-CsHostedVoicemailPolicy cmdlet to set the global policy parameters for your environment.</span></span> <span data-ttu-id="7ad0f-113">Por ejemplo, ejecute lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7ad0f-113">For example, run:</span></span>
    
        Set-CsHostedVoicemailPolicy -Destination ExUM.fabrikam.com -Organization "corp1.litwareinc.com"
    
    <span data-ttu-id="7ad0f-114">Debido a que este comando no especifica el parámetro de identidad de la Directiva, la interfaz de línea de comandos de Windows PowerShell establece los siguientes valores en la Directiva de correo de voz hospedado global:</span><span class="sxs-lookup"><span data-stu-id="7ad0f-114">Because this command does not specify the policy’s Identity parameter, Windows PowerShell command-line interface sets the following values on the global hosted voice mail policy:</span></span>
    
      - <span data-ttu-id="7ad0f-115">**Destino** especifica el nombre de dominio completo (FQDN) del servicio de mensajería unificada de Exchange hospedado.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-115">**Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="7ad0f-116">Este parámetro es opcional, pero si intenta habilitar un usuario para el correo de voz hospedado y la directiva asignada al usuario no tiene un valor de destino, se producirá un error de habilitar.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-116">This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.</span></span>
    
      - <span data-ttu-id="7ad0f-117">**Organización** especifica una lista separada por comas de los inquilinos de Exchange que alojan usuarios de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-117">**Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server users.</span></span> <span data-ttu-id="7ad0f-118">Cada inquilino debe especificarse como el FQDN de ese inquilino en el servicio de mensajería unificada de Exchange hospedado.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-118">Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7ad0f-119">En el cmdlet de ejemplo anterior, el valor "corp1.litwareinc.com" reemplaza cualquier valor que ya pudiera estar presente en el parámetro de organización.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-119">In the previous example cmdlet, the value “corp1.litwareinc.com” replaces any value that might already be present in the Organization parameter.</span></span> <span data-ttu-id="7ad0f-120">Por ejemplo, si la directiva ya contiene una lista de organizaciones separadas por comas, se reemplazaría la lista completa.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-120">For example, if the policy already contains a comma-separated list of organizations, the full list would be replaced.</span></span> <span data-ttu-id="7ad0f-121">Si desea agregar una organización a la lista en lugar de reemplazar toda la lista, ejecute un comando similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-121">If you want to add an organization to the list rather than replace the entire list, run a command similar to the following.</span></span>

    
    </div>
    
        $a = Get-CsHostedVoicemailPolicy
        $a.Organization += ",corp3.litwareinc.com"
        Set-CsHostedVoicemailPolicy -Organization $a.Organization

<span data-ttu-id="7ad0f-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ad0f-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

