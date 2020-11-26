---
title: 'Lync Server 2013: crear una directiva de correo de voz hospedado en el nivel de sitio'
description: 'Lync Server 2013: crear una directiva de correo de voz hospedado en el nivel de sitio.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a site-level hosted voice mail policy
ms:assetid: 145892c8-a6ca-45fb-9e83-786f709dd775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398216(v=OCS.15)
ms:contentKeyID: 48183481
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8cd578359a8d20562e8887b61b86d53332e6f8d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432117"
---
# <a name="create-a-site-level-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="57a7b-103">Crear una directiva de correo de voz hospedado en el nivel de sitio en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57a7b-103">Create a site-level hosted voice mail policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="57a7b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="57a7b-104">

<span> </span></span></span>

<span data-ttu-id="57a7b-105">_**Última modificación del tema:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="57a7b-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="57a7b-106">Una directiva de *sitio* puede afectar a todos los usuarios alojados en el sitio para el que se define la Directiva.</span><span class="sxs-lookup"><span data-stu-id="57a7b-106">A *site* policy can impact all users that are homed on the site for which the policy is defined.</span></span> <span data-ttu-id="57a7b-107">Si un usuario está configurado para el acceso a mensajería unificada de Exchange hospedado y no se le ha asignado una directiva por usuario, se aplicará la Directiva de sitio.</span><span class="sxs-lookup"><span data-stu-id="57a7b-107">If a user is configured for hosted Exchange UM access and has not been assigned a Per-user policy, the site policy applies.</span></span> <span data-ttu-id="57a7b-108">Si no ha implementado una directiva de sitio, se aplica la directiva global.</span><span class="sxs-lookup"><span data-stu-id="57a7b-108">If you have not deployed a site policy, the global policy applies.</span></span>

<span data-ttu-id="57a7b-109">Para obtener más información sobre cómo configurar directivas de sitio, consulte la documentación del shell de administración de Lync Server para los siguientes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="57a7b-109">For details about configuring site policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="57a7b-110">Nuevo: CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="57a7b-110">New-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="57a7b-111">Set-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="57a7b-111">Set-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="57a7b-112">Get-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="57a7b-112">Get-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsHostedVoicemailPolicy)

<div>

## <a name="to-create-a-site-hosted-voice-mail-policy"></a><span data-ttu-id="57a7b-113">Para crear una directiva de correo de voz hospedada en un sitio</span><span class="sxs-lookup"><span data-stu-id="57a7b-113">To create a site hosted voice mail policy</span></span>

1.  <span data-ttu-id="57a7b-114">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="57a7b-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="57a7b-115">Ejecute el cmdlet New-CsHostedVoicemailPolicy para crear la Directiva.</span><span class="sxs-lookup"><span data-stu-id="57a7b-115">Run the New-CsHostedVoicemailPolicy cmdlet to create the policy.</span></span> <span data-ttu-id="57a7b-116">Por ejemplo, ejecute lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="57a7b-116">For example, run:</span></span>
    
        New-CsHostedVoicemailPolicy -Identity site:Redmond -Destination ExUM.fabrikam.com -Description "Hosted voice mail policy for the Redmond site." -Organization "corp1.litwareinc.com, corp2.litwareinc.com"
    
    <span data-ttu-id="57a7b-117">En este ejemplo se crea una directiva de correo de voz hospedada con ámbito de sitio y se establecen los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="57a7b-117">This example creates a hosted voice mail policy with site scope, and sets the following parameters:</span></span>
    
      - <span data-ttu-id="57a7b-118">**Identity** especifica un identificador único para la Directiva, que incluye el ámbito.</span><span class="sxs-lookup"><span data-stu-id="57a7b-118">**Identity** specifies a unique identifier for the policy, which includes the scope.</span></span> <span data-ttu-id="57a7b-119">En el caso de una directiva con ámbito de sitio, el valor del parámetro Identity debe especificarse en el formato `site:` *\<name\>* , por ejemplo `site:Redmond` .</span><span class="sxs-lookup"><span data-stu-id="57a7b-119">For a policy with site scope, the Identity parameter value must be specified in the format `site:`*\<name\>*, for example, `site:Redmond`.</span></span>
    
      - <span data-ttu-id="57a7b-120">**Destino** especifica el nombre de dominio completo (FQDN) del servicio de mensajería unificada de Exchange hospedado.</span><span class="sxs-lookup"><span data-stu-id="57a7b-120">**Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="57a7b-121">Este parámetro es opcional, pero si intenta habilitar un usuario para el correo de voz hospedado y la directiva asignada al usuario no tiene un valor de destino, se producirá un error de habilitar.</span><span class="sxs-lookup"><span data-stu-id="57a7b-121">This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.</span></span>
    
      - <span data-ttu-id="57a7b-122">**Descripción** proporciona información descriptiva opcional sobre la Directiva.</span><span class="sxs-lookup"><span data-stu-id="57a7b-122">**Description** provides optional descriptive information about the policy.</span></span>
    
      - <span data-ttu-id="57a7b-123">**Organización** especifica una lista separada por comas de los inquilinos de Exchange que alojan los usuarios de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57a7b-123">**Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server 2013 users.</span></span> <span data-ttu-id="57a7b-124">Cada inquilino debe especificarse como el FQDN de ese inquilino en el servicio de mensajería unificada de Exchange hospedado.</span><span class="sxs-lookup"><span data-stu-id="57a7b-124">Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.</span></span>

<span data-ttu-id="57a7b-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="57a7b-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

