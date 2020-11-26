---
title: 'Lync Server 2013: Plan para certificados de servidores perimetrales'
description: 'Lync Server 2013: planear certificados de servidor perimetral.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Plan for Edge Server certificates
ms:assetid: f1dfe220-2398-4ac8-ba4c-206c8c0cbc50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413010(v=OCS.15)
ms:contentKeyID: 48185798
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22ec3743256fe3e4c55dba0f6357a85b1ad81cd0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437133"
---
# <a name="plan-for-edge-server-certificates-in-lync-server-2013"></a><span data-ttu-id="3f9d3-103">Plan para certificados de servidores perimetrales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f9d3-103">Plan for Edge Server certificates in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f9d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f9d3-104">

<span> </span></span></span>

<span data-ttu-id="3f9d3-105">_**Última modificación del tema:** 2012-11-05_</span><span class="sxs-lookup"><span data-stu-id="3f9d3-105">_**Topic Last Modified:** 2012-11-05_</span></span>

<span data-ttu-id="3f9d3-106">La creación de certificados para Edge se ha simplificado en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-106">Certificate creation for Edge is simplified in Lync Server 2013.</span></span>

<span data-ttu-id="3f9d3-107">**Diagrama de flujo de certificados para el servidor perimetral**</span><span class="sxs-lookup"><span data-stu-id="3f9d3-107">**Certificates Flow Chart for Edge Server**</span></span>

<span data-ttu-id="3f9d3-108">![a5fc20db-7ced-4364-b577-6a709a8367cd](images/Gg413010.a5fc20db-7ced-4364-b577-6a709a8367cd(OCS.15).jpg "a5fc20db-7ced-4364-b577-6a709a8367cd")</span><span class="sxs-lookup"><span data-stu-id="3f9d3-108">![a5fc20db-7ced-4364-b577-6a709a8367cd](images/Gg413010.a5fc20db-7ced-4364-b577-6a709a8367cd(OCS.15).jpg "a5fc20db-7ced-4364-b577-6a709a8367cd")</span></span>

<span data-ttu-id="3f9d3-109">Cree un único certificado público, asegúrese de que tiene una clave privada exportable definida para el certificado y asígnela a las siguientes interfaces externas de servidor perimetral con el Asistente para certificados:</span><span class="sxs-lookup"><span data-stu-id="3f9d3-109">Create a single public certificate, ensure that you have an exportable private key defined for the certificate, and assign it to the following Edge Server external interfaces using the certificate wizard:</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3f9d3-110">Los certificados comodín no se admiten en Lync Server, excepto cuando se usan para resumir las direcciones URL simples a través del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-110">Wildcard certificates are not supported in Lync Server, except where used to summarize the Simple URLs through the reverse proxy.</span></span> <span data-ttu-id="3f9d3-111">Debe definir distintos nombres alternativos de sujeto (San) para cada nombre de dominio SIP, servicio perimetral de conferencias web, servicio perimetral A/V y dominio XMPP ofrecido por su implementación.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-111">You must define distinct subject alternate names (SANs) for each SIP domain name, Web Conferencing Edge service, A/V Edge service and XMPP domain offered by your deployment.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="3f9d3-112">Introducida en Lync Server 2013, el almacenamiento provisional de certificados de autenticación de audio y vídeo con antelación a la fecha de expiración del certificado actual requiere una planificación adicional.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-112">Introduced in Lync Server 2013, staging Audio/Video Authentication certificates in advance of the expiration time of the current certificate requires some additional planning.</span></span> <span data-ttu-id="3f9d3-113">En lugar de un certificado con varios propósitos para la interfaz de borde externo, necesitará dos certificados, uno asignado al servicio perimetral de acceso y el servicio perimetral de conferencia Web, y un certificado para el servicio perimetral de a/V.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-113">Instead of one certificate with multiple purposes for the external Edge interface, you will require two certificates, one assigned to the Access Edge service and Web Conferencing Edge service, and one certificate for the A/V Edge service.</span></span> <span data-ttu-id="3f9d3-114">Para obtener más información, consulte <A href="lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate">almacenamiento provisional de certificados AV y OAuth en Lync Server 2013 uso de-roll en Set-CsCertificate</A></span><span class="sxs-lookup"><span data-stu-id="3f9d3-114">For additional details, see <A href="lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate">Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate</A></span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3f9d3-115">En el caso de un grupo de servidores perimetrales, exporte el certificado con la clave privada a cada servidor perimetral y asigne el certificado a cada servicio de servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-115">In the event of a pool of Edge Servers, you export the certificate with the private key to each Edge Server and assign the certificate to each Edge Server service.</span></span> <span data-ttu-id="3f9d3-116">Haga lo mismo para el certificado de servidor perimetral interno, exporte el certificado con la clave privada y asignándole la asignación a cada interfaz de borde interno.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-116">Do the same for the internal Edge Server certificate, exporting the certificate with the private key and assigning to each internal Edge interface.</span></span>



</div>

  - <span data-ttu-id="3f9d3-117">Asegúrese de que tiene asignada una clave privada exportable para el certificado</span><span class="sxs-lookup"><span data-stu-id="3f9d3-117">Ensure that you have an exportable private key assigned for the certificate</span></span>

  - <span data-ttu-id="3f9d3-118">Servicio perimetral de acceso (denominado **SIP perimetral de acceso externo** en el Asistente para certificados)</span><span class="sxs-lookup"><span data-stu-id="3f9d3-118">Access Edge service (referred to as **SIP Access Edge External** in the certificate wizard)</span></span>

  - <span data-ttu-id="3f9d3-119">Servicio perimetral de conferencias web (denominado **borde de conferencias web externo** en el Asistente para certificados)</span><span class="sxs-lookup"><span data-stu-id="3f9d3-119">Web Conferencing Edge service (referred to as **Web Conferencing Edge External** in the certificate wizard)</span></span>

  - <span data-ttu-id="3f9d3-120">Servicio de autenticación a/V (denominado **borde a/v externo** en el Asistente para certificados)</span><span class="sxs-lookup"><span data-stu-id="3f9d3-120">A/V Authentication service (referred to as **A/V Edge External** in the certificate wizard)</span></span>

<span data-ttu-id="3f9d3-121">Crear un único certificado interno con una clave privada exportable, cópielo y asígnelo a cada una de las interfaces internas del servidor perimetral:</span><span class="sxs-lookup"><span data-stu-id="3f9d3-121">Create a single internal certificate with exportable private key, copy and assign it to each of the Edge Server internal interfaces:</span></span>

  - <span data-ttu-id="3f9d3-122">Servidor perimetral (denominado interno de la **arista** en el Asistente para certificados)</span><span class="sxs-lookup"><span data-stu-id="3f9d3-122">Edge Server (referred to as **Edge Internal** in the certificate wizard)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3f9d3-123">Es posible usar certificados diferentes y diferentes para cada servicio de servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-123">It is possible to use separate and distinct certificates for each Edge Server service.</span></span> <span data-ttu-id="3f9d3-124">Una buena razón para elegir certificados independientes es si desea usar la nueva característica de certificados sucesivos para el certificado de servicio perimetral A/V.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-124">A good reason to choose separate certificates is if you want to use the new rolling certificate feature for the A/V Edge service certificate.</span></span> <span data-ttu-id="3f9d3-125">En el caso de esta característica, se recomienda disociar el certificado de servicio perimetral A/V del servicio perimetral de acceso y el servicio perimetral de conferencia Web.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-125">In the case of this feature, decoupling the A/V Edge service certificate from the Access Edge service and Web Conferencing Edge service is recommended.</span></span> <span data-ttu-id="3f9d3-126">Si elige solicitar, adquirir y asignar certificados independientes para cada servicio, debe solicitar que la clave privada sea exportable para el servicio perimetral de A/V (de nuevo, esto es en realidad el servicio de autenticación A/V) y asignar el mismo certificado a la interfaz externa perimetral de A/V en cada servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-126">If you choose to request, acquire and assign separate certificates for each service, you must request that the private key be exportable for the A/V Edge service (again, this is in actuality the A/V Authentication service) and assign the same certificate to the A/V Edge External interface on each Edge Server.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3f9d3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f9d3-127">See Also</span></span>


[<span data-ttu-id="3f9d3-128">Almacenamiento provisional de certificados AV y OAuth en Lync Server 2013 usar-Roll en Set-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="3f9d3-128">Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate</span></span>](lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  


[<span data-ttu-id="3f9d3-129">Cambios en Lync Server 2013 que afectan a la planificación del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="3f9d3-129">Changes in Lync Server 2013 that affect Edge Server planning</span></span>](lync-server-2013-changes-in-lync-server-that-affect-edge-server-planning.md)  
  

<span data-ttu-id="3f9d3-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f9d3-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

