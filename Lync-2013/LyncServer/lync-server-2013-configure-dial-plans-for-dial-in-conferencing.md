---
title: 'Lync Server 2013: Configurar planes de marcado para las conferencias de acceso telefónico local'
description: 'Lync Server 2013: configurar planes de marcado para conferencias de acceso telefónico local.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial plans for dial-in conferencing
ms:assetid: a3e0958e-384f-43e5-b4c9-686b6ecac7ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412768(v=OCS.15)
ms:contentKeyID: 48185051
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28123f905288ce35b6f470168962a3d8e6faa22b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399900"
---
# <a name="configure-dial-plans-for-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="9aec0-103">Configurar planes de marcado para las conferencias de acceso telefónico local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9aec0-103">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9aec0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9aec0-104">

<span> </span></span></span>

<span data-ttu-id="9aec0-105">_**Última modificación del tema:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="9aec0-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="9aec0-106">Al implementar la conferencia de acceso telefónico local, tiene que crear o modificar uno o más planes de marcado para enrutar números de teléfono de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="9aec0-106">When you deploy dial-in conferencing, you need to create or modify one or more dial plans for routing dial-in access phone numbers.</span></span> <span data-ttu-id="9aec0-107">Asegúrese de que al menos una regla de normalización de cada plan de marcado convierte las extensiones telefónicas en números de teléfono completos en formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="9aec0-107">Make sure that at least one normalization rule in each dial plan converts telephone extensions into complete phone numbers in E.164 format.</span></span> <span data-ttu-id="9aec0-108">Los usuarios de la conferencia de acceso telefónico local se unen a las conferencias como usuarios de empresa autenticados al escribir su número de identificación personal (PIN) y su número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="9aec0-108">Users of dial-in conferencing join conferences as authenticated enterprise users by entering their personal identification number (PIN) and their phone number.</span></span> <span data-ttu-id="9aec0-109">Necesita una regla de normalización para convertir las extensiones en números de teléfono completos, de modo que los usuarios puedan autenticarse cuando solo introduzcan una extensión telefónica.</span><span class="sxs-lookup"><span data-stu-id="9aec0-109">You need a normalization rule to convert extensions into complete phone numbers so that users can be authenticated when they enter just a telephone extension.</span></span>

<span data-ttu-id="9aec0-110">Para configurar planes de marcado para conferencias de acceso telefónico local, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9aec0-110">To set up dial plans for dial-in conferencing, do the following:</span></span>

  - <span data-ttu-id="9aec0-111">Tanto si implementa la Telefonía IP empresarial como si no, modifique el plan de marcado global para agregar una región de conferencia de acceso telefónico local y para garantizar que una regla de normalización convierta de forma precisa los números de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="9aec0-111">Whether or not you deploy Enterprise Voice, modify the global dial plan to add a dial-in conferencing region and to make sure that a normalization rule accurately converts your dial-in access numbers.</span></span> <span data-ttu-id="9aec0-112">Para obtener instrucciones detalladas, vea [modificar un plan de marcado en Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="9aec0-112">For detailed instructions, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

  - <span data-ttu-id="9aec0-113">Si no implementó la Telefonía IP empresarial, cree planes de marcado para los números de acceso a conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="9aec0-113">If you did not deploy Enterprise Voice, create dial plans for your dial-in conferencing access numbers.</span></span> <span data-ttu-id="9aec0-114">Recuerde incluir una región de conferencia de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="9aec0-114">Be sure to include a dial-in conferencing region.</span></span> <span data-ttu-id="9aec0-115">Para obtener instrucciones detalladas, consulte [crear un plan de marcado en Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="9aec0-115">For detailed instructions, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

  - <span data-ttu-id="9aec0-116">Si ha implementado la Telefonía IP empresarial, modifique los planes de marcado de la Telefonía IP empresarial según sea necesario para incluir regiones y usar las reglas de normalización pertinentes para los números de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="9aec0-116">If you deployed Enterprise Voice, modify Enterprise Voice dial plans as necessary to include regions and use appropriate normalization rules for dial-in access numbers.</span></span> <span data-ttu-id="9aec0-117">Para obtener instrucciones detalladas, vea [modificar un plan de marcado en Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="9aec0-117">For detailed instructions, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span> <span data-ttu-id="9aec0-118">También puede crear planes de marcado dedicados que solo se usarán para números de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="9aec0-118">You can also create dedicated dial plans that are used only for dial-in access numbers.</span></span> <span data-ttu-id="9aec0-119">Para obtener instrucciones detalladas, consulte [crear un plan de marcado en Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="9aec0-119">For detailed instructions, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

<span data-ttu-id="9aec0-120">Para obtener más información acerca de las regiones de planeación, consulte [requisitos de conferencias de acceso telefónico local en Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="9aec0-120">For details about planning regions, see [Dial-in conferencing requirements in Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9aec0-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9aec0-121">In This Section</span></span>

  - [<span data-ttu-id="9aec0-122">Ver información de un plan de marcado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9aec0-122">View dial plan information in Lync Server 2013</span></span>](lync-server-2013-view-dial-plan-information.md)

  - [<span data-ttu-id="9aec0-123">Crear un plan de marcado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9aec0-123">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)

  - [<span data-ttu-id="9aec0-124">Modificar un plan de marcado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9aec0-124">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)

  - [<span data-ttu-id="9aec0-125">Definir las reglas de normalización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9aec0-125">Defining normalization rules in Lync Server 2013</span></span>](lync-server-2013-defining-normalization-rules.md)

<span data-ttu-id="9aec0-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9aec0-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

