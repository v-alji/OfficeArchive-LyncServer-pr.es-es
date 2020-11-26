---
title: 'Lync Server 2013: crear o modificar un objeto de contacto telefónico de área común'
description: 'Lync Server 2013: crear o modificar un objeto de contacto telefónico de área común.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a common area phone Contact object
ms:assetid: eec33ad1-e4f2-49b2-91d6-d5a9d2e1714b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994083(v=OCS.15)
ms:contentKeyID: 51803995
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: adc5ede23f495a63b2d556b556817d4171a08723
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431844"
---
# <a name="create-or-modify-a-common-area-phone-contact-object-in-lync-server-2013"></a><span data-ttu-id="b2b87-103">Crear o modificar un objeto de contacto telefónico de área común en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2b87-103">Create or modify a common area phone Contact object in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2b87-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2b87-104">

<span> </span></span></span>

<span data-ttu-id="b2b87-105">_**Última modificación del tema:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="b2b87-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="b2b87-106">Para crear objetos de contacto de servicios de dominio de Active Directory para todos los teléfonos de área común, use el cmdlet **New-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="b2b87-106">To create Active Directory Domain Services contact objects for all your common area phones, use the **New-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="b2b87-107">Este cmdlet puede crear nuevos objetos de contacto para usarlos con teléfonos de área común o puede asociar objetos de contacto existentes con un nuevo teléfono de área común.</span><span class="sxs-lookup"><span data-stu-id="b2b87-107">This cmdlet can either create new contact objects for use with common area phones, or it can associate existing contact objects with a new common area phone.</span></span> <span data-ttu-id="b2b87-108">Para modificar las propiedades de los objetos de contacto asociados con teléfonos de área común, use el cmdlet **set-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="b2b87-108">To modify the properties of the contact objects associated with common area phones, use the **Set-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="b2b87-109">Los parámetros opcionales para **set-CsCommonAreaPhone** permiten cambiar elementos, como el nombre para mostrar de Active Directory del contacto o el identificador uniforme de recursos (URI) de la línea asociada al teléfono, y habilitar y deshabilitar la cuenta para su uso con Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b2b87-109">Optional parameters for **Set-CsCommonAreaPhone** enable you to change items, such as the contact’s Active Directory display name or the line Uniform Resource Identifier (URI) associated with the phone, and enable and disable the account for use with Lync Server.</span></span> <span data-ttu-id="b2b87-110">Para obtener más información sobre todas las modificaciones disponibles, consulte la sección parámetros en [set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone).</span><span class="sxs-lookup"><span data-stu-id="b2b87-110">For details about all the available modifications, see the Parameters section at [Set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone).</span></span> <span data-ttu-id="b2b87-111">Para obtener más información sobre los parámetros **de CsCommonAreaPhone nuevos** , consulte [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone).</span><span class="sxs-lookup"><span data-stu-id="b2b87-111">For details about **New-CsCommonAreaPhone** parameters, see [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone).</span></span>

<span data-ttu-id="b2b87-112">Puede ejecutar estos dos cmdlets desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b2b87-112">You can run these two cmdlets from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="b2b87-113">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="b2b87-113">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="creating-a-common-area-phone-contact-object"></a><span data-ttu-id="b2b87-114">Crear un objeto de contacto de teléfono de área común</span><span class="sxs-lookup"><span data-stu-id="b2b87-114">Creating a common area phone contact object</span></span>

  - <span data-ttu-id="b2b87-115">Para crear un nuevo objeto de contacto de teléfono de área común, use el cmdlet **New-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="b2b87-115">To create a new common area phone contact object, use the **New-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="b2b87-116">Como mínimo, debe proporcionar la siguiente información al crear un objeto de contacto:</span><span class="sxs-lookup"><span data-stu-id="b2b87-116">At a minimum, you must supply the following information when creating a contact object:</span></span>
    
      - <span data-ttu-id="b2b87-117">**LineUri**: el número de teléfono asignado al teléfono de área común.</span><span class="sxs-lookup"><span data-stu-id="b2b87-117">**LineUri**: The telephone number assigned to the common area phone.</span></span> <span data-ttu-id="b2b87-118">Ten en cuenta que debes usar el formato E. 164 al especificar el número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="b2b87-118">Note that you must use the E.164 format when specifying the phone number.</span></span>
    
      - <span data-ttu-id="b2b87-119">**RegistrarPool**: el nombre de dominio completo (FQDN) del grupo de servidores de registro que hospedará el objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="b2b87-119">**RegistrarPool**: The fully qualified domain name (FQDN) of the Registrar pool that will host the contact object.</span></span>
    
      - <span data-ttu-id="b2b87-120">**Ou**: nombre distintivo del contenedor de Active Directory en el que se creará el objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="b2b87-120">**OU**: Distinguished name of the Active Directory container where the contact object will be created.</span></span>
    
    <span data-ttu-id="b2b87-121">También le recomendamos que proporcione un nombre para mostrar de los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b2b87-121">We also recommend that you provide an Active Directory Domain Services display name.</span></span> <span data-ttu-id="b2b87-122">De lo contrario, tendrá que usar un GUID para especificar la identidad del teléfono.</span><span class="sxs-lookup"><span data-stu-id="b2b87-122">Otherwise, you will need to use a GUID to specify the phone Identity.</span></span> <span data-ttu-id="b2b87-123">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b2b87-123">For example:</span></span>
    
        New-CsCommonAreaPhone -LineUri "tel:+12065551219" -RegistrarPool "atl-cs-001.litwareinc.com" -OU "OU=Phones,dc=litwareinc,dc=com" -DisplayName "Lobby"

</div>

<div>

## <a name="modifying-a-common-area-phone-contact-object"></a><span data-ttu-id="b2b87-124">Modificar un objeto de contacto de teléfono de área común</span><span class="sxs-lookup"><span data-stu-id="b2b87-124">Modifying a common area phone contact object</span></span>

  - <span data-ttu-id="b2b87-125">Para modificar las propiedades de un teléfono de área común existente, objeto de contacto use el cmdlet **set-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="b2b87-125">To modify the properties of an existing common area phone, contact object use the **Set-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="b2b87-126">Por ejemplo, este comando configura la dirección SIP de la zona telefónica común con DisplayName:</span><span class="sxs-lookup"><span data-stu-id="b2b87-126">For example, this command configures the SIP address for the common area phone with the DisplayName Lobby:</span></span>
    
        Set-CsCommonAreaPhone -Identity "Lobby" -SipAddress "sip:lobby@litwareinc.com"

</div>

<span data-ttu-id="b2b87-127">Para obtener más información, consulte los temas de ayuda para el cmdlet [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone) y el cmdlet [set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone) .</span><span class="sxs-lookup"><span data-stu-id="b2b87-127">For details, see the Help topics for the [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone) cmdlet and the [Set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone) cmdlet.</span></span>

<span data-ttu-id="b2b87-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2b87-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

