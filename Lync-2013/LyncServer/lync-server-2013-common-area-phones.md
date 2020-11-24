---
title: 'Lync Server 2013: teléfonos de área común'
description: 'Lync Server 2013: teléfonos de área común.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Common area phones
ms:assetid: d63bb3de-154e-4347-9251-9fa94e7d593a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994076(v=OCS.15)
ms:contentKeyID: 51803987
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af8a68f875bba1d43a91e5a252259841d7a6bbda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400073"
---
# <a name="common-area-phones-in-lync-server-2013"></a><span data-ttu-id="69b7f-103">Teléfonos de área común en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69b7f-103">Common area phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69b7f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69b7f-104">

<span> </span></span></span>

<span data-ttu-id="69b7f-105">_**Última modificación del tema:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="69b7f-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="69b7f-106">Los teléfonos de área común son teléfonos IP que no están asociados a un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="69b7f-106">Common area phones are IP phones that are not associated with an individual user.</span></span> <span data-ttu-id="69b7f-107">En lugar de estar ubicado en la oficina de alguien, los teléfonos de área común suelen encontrarse en la creación de salas, cafeterías, salas de reuniones de la reunión y otras ubicaciones en las que es probable que una gran cantidad de personas recopilen.</span><span class="sxs-lookup"><span data-stu-id="69b7f-107">Instead of being located in someone’s office, common area phones are typically located in building lobbies, cafeterias, employee lounges, meeting rooms, and other locations where a large number of people are likely to gather.</span></span> <span data-ttu-id="69b7f-108">A diferencia de otros teléfonos de Lync Server, que se suelen mantener con las directivas de voz y los planes de marcado que se asignan a los usuarios individuales, los teléfonos de área común no tienen usuarios individuales asignados.</span><span class="sxs-lookup"><span data-stu-id="69b7f-108">Unlike other phones in Lync Server, which are typically maintained by using voice policies and dial plans that are assigned to individual users, common area phones do not have individual users assigned to them.</span></span> <span data-ttu-id="69b7f-109">Esto significa que deben administrarse de forma diferente a los demás teléfonos.</span><span class="sxs-lookup"><span data-stu-id="69b7f-109">This means that they must be managed differently than your other phones.</span></span>

<span data-ttu-id="69b7f-110">Para administrar teléfonos de área común, puede crear objetos de contacto de los servicios de dominio de Active Directory para todos los teléfonos comunes de área que, al igual que las cuentas de usuario, pueden asignarse a directivas y planes de voz.</span><span class="sxs-lookup"><span data-stu-id="69b7f-110">To manage common area phones, you create Active Directory Domain Services contact objects for all your common area phones that, like user accounts, can be assigned policies and voice plans.</span></span> <span data-ttu-id="69b7f-111">Este enfoque te permite mantener el control sobre teléfonos comunes de área, aunque dichos teléfonos no estén asociados con un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="69b7f-111">This approach enables you to maintain control over common area phones, even though those phones are not associated with an individual user.</span></span>

<span data-ttu-id="69b7f-112">Use los temas de esta sección para obtener información sobre cómo crear objetos de contacto para teléfonos de área común, modificarlos y eliminarlos, y configurar y ver la información de configuración de los teléfonos de área común de su implementación.</span><span class="sxs-lookup"><span data-stu-id="69b7f-112">Use the topics in this section to learn how to create contact objects for common area phones, modify and delete them, and configure and view configuration information about the common area phones in your deployment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="69b7f-113">Tiene tres opciones para teléfonos de área común: el teléfono de área común Aastra 6721ip, el teléfono IP HP 4110 y el teléfono de área común IP Polycom CX500.</span><span class="sxs-lookup"><span data-stu-id="69b7f-113">You have three options for common area phones: the Aastra 6721ip common area phone, the HP 4110 IP Phone, and the Polycom CX500 IP common area phone.</span></span> <span data-ttu-id="69b7f-114">El teléfono de conferencia IP Polycom CX3000 es otra variante de teléfono de área común.</span><span class="sxs-lookup"><span data-stu-id="69b7f-114">The Polycom CX3000 IP conferencing phone is another variant common area phone.</span></span> <span data-ttu-id="69b7f-115">Sin embargo, está pensada para su uso en salas de conferencia.</span><span class="sxs-lookup"><span data-stu-id="69b7f-115">However, it is intended for use in conference rooms.</span></span> <span data-ttu-id="69b7f-116">Para obtener más información sobre teléfonos de área común, consulte la sección teléfonos de área común de <A href="https://technet.microsoft.com/library/gg398958(v=ocs.14).aspx">elección de nuevos dispositivos</A>.</span><span class="sxs-lookup"><span data-stu-id="69b7f-116">For details about common area phones, see the Common Area Phones section of <A href="https://technet.microsoft.com/library/gg398958(v=ocs.14).aspx">Choosing New Devices</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="69b7f-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="69b7f-117">In This Section</span></span>

  - [<span data-ttu-id="69b7f-118">Ver la información de los teléfonos comunes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69b7f-118">View common area phone information in Lync Server 2013</span></span>](lync-server-2013-view-common-area-phone-information.md)

  - [<span data-ttu-id="69b7f-119">Crear o modificar un objeto de contacto telefónico de área común en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69b7f-119">Create or modify a common area phone Contact object in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-common-area-phone-contact-object.md)

  - [<span data-ttu-id="69b7f-120">Habilitar o deshabilitar la entrada manuscrita en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69b7f-120">Enable or disable hot desking in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-hot-desking.md)

  - [<span data-ttu-id="69b7f-121">Eliminar un objeto de contacto telefónico de área común en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69b7f-121">Delete a common area phone Contact object in Lync Server 2013</span></span>](lync-server-2013-delete-a-common-area-phone-contact-object.md)

  - [<span data-ttu-id="69b7f-122">Asignar directivas en Lync Server 2013 a un teléfono de área común</span><span class="sxs-lookup"><span data-stu-id="69b7f-122">Assign policies in Lync Server 2013 to a common area phone</span></span>](lync-server-2013-assign-policies-to-a-common-area-phone.md)

<span data-ttu-id="69b7f-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69b7f-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

