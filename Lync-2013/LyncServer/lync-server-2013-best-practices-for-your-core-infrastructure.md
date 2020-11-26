---
title: 'Lync Server 2013: procedimientos recomendados para su infraestructura básica'
description: 'Lync Server 2013: procedimientos recomendados para su infraestructura básica.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for your core infrastructure in Lync Server 2013
ms:assetid: 44aff88d-536c-4613-a81e-5398c9c6a648
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518328(v=OCS.15)
ms:contentKeyID: 61071242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0ea7cb9c7685a3b6f7c04146ec5631bbac10fe6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436044"
---
# <a name="best-practices-for-your-core-infrastructure-in-lync-server-2013"></a><span data-ttu-id="e6d06-103">Procedimientos recomendados para su infraestructura básica en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e6d06-103">Best practices for your core infrastructure in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e6d06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e6d06-104">

<span> </span></span></span>

<span data-ttu-id="e6d06-105">_**Última modificación del tema:** 2014-01-27_</span><span class="sxs-lookup"><span data-stu-id="e6d06-105">_**Topic Last Modified:** 2014-01-27_</span></span>

<span data-ttu-id="e6d06-106">Es probable que ya haya tomado las medidas para diseñar la tolerancia a errores en el sistema, con prácticas tales como garantizar la redundancia de hardware, protegerse contra la pérdida de energía, instalar de forma rutinaria actualizaciones de seguridad y medidas antivirus, y supervisar la actividad del servidor.</span><span class="sxs-lookup"><span data-stu-id="e6d06-106">You have probably already taken steps to design fault tolerance in your system, using practices such as ensuring hardware redundancy, guarding against power loss, routinely installing security updates and antivirus measures, and Monitoring Server activity.</span></span> <span data-ttu-id="e6d06-107">Estas prácticas no solo benefician la infraestructura de Microsoft Lync Server 2013, sino también de toda la red.</span><span class="sxs-lookup"><span data-stu-id="e6d06-107">These practices benefit not only your Microsoft Lync Server 2013 infrastructure, but also your entire network.</span></span> <span data-ttu-id="e6d06-108">Si no ha implementado estos procedimientos, le recomendamos que lo haga antes de implementar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e6d06-108">If you have not implemented these practices, we recommend that you do so before deploying Lync Server 2013.</span></span>

<span data-ttu-id="e6d06-109">Para ayudar a proteger los servidores de su implementación de Lync Server 2013 de daños accidentales o intencionados que pueden dar lugar a un tiempo de inactividad, tome las siguientes precauciones:</span><span class="sxs-lookup"><span data-stu-id="e6d06-109">To help protect the servers in your Lync Server 2013 deployment from accidental or purposeful harm that might result in downtime, take the following precautions:</span></span>

  - <span data-ttu-id="e6d06-110">Mantenga sus servidores al día con las actualizaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e6d06-110">Keep your servers up-to-date with security updates.</span></span> <span data-ttu-id="e6d06-111">Suscribirse al servicio de notificaciones de seguridad de Microsoft le ayuda a recibir notificaciones inmediatas de versiones de boletines de seguridad para cualquier producto de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6d06-111">Subscribing to the Microsoft Security Notification Service helps ensure that you receive immediate notification of security bulletin releases for any Microsoft product.</span></span> <span data-ttu-id="e6d06-112">Para suscribirse, vaya al sitio web de notificaciones de seguridad técnica de Microsoft en [https://go.microsoft.com/fwlink/p/?LinkId=145202](https://go.microsoft.com/fwlink/p/?linkid=145202) .</span><span class="sxs-lookup"><span data-stu-id="e6d06-112">To subscribe, go to the Microsoft Technical Security Notifications website at [https://go.microsoft.com/fwlink/p/?LinkId=145202](https://go.microsoft.com/fwlink/p/?linkid=145202).</span></span>

  - <span data-ttu-id="e6d06-113">Asegúrese de que los derechos de acceso están configurados correctamente.</span><span class="sxs-lookup"><span data-stu-id="e6d06-113">Ensure that access rights are set up correctly.</span></span>

  - <span data-ttu-id="e6d06-114">Mantenga los servidores en un entorno físico que evite el acceso no autorizado.</span><span class="sxs-lookup"><span data-stu-id="e6d06-114">Keep your servers in a physical environment that prevents unauthorized access.</span></span> <span data-ttu-id="e6d06-115">Asegúrese de que el software antivirus adecuado esté instalado en todos los servidores.</span><span class="sxs-lookup"><span data-stu-id="e6d06-115">Ensure that adequate antivirus software is installed on all your servers.</span></span> <span data-ttu-id="e6d06-116">Mantenga el software actualizado con los últimos archivos de firma de virus.</span><span class="sxs-lookup"><span data-stu-id="e6d06-116">Keep the software up-to-date with the latest virus signature files.</span></span> <span data-ttu-id="e6d06-117">Use la característica de actualización automática de su aplicación antivirus para mantener actualizadas las firmas de virus.</span><span class="sxs-lookup"><span data-stu-id="e6d06-117">Use the automatic update feature of your antivirus application to keep the virus signatures current.</span></span>

  - <span data-ttu-id="e6d06-118">Le recomendamos que deshabilite los servicios del sistema operativo Windows Server que no son necesarios en los equipos en los que instala Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e6d06-118">We recommend that you disable the Windows Server operating system services that are not required on the computers where you install Lync Server 2013.</span></span>

  - <span data-ttu-id="e6d06-119">Cifre los sistemas operativos y las unidades de disco donde los datos se almacenan con un sistema de cifrado de volumen completo, a menos que pueda garantizar un control completo y constante de los servidores, el aislamiento físico total y la retirada correcta y segura de las unidades de disco reemplazadas o fallidas.</span><span class="sxs-lookup"><span data-stu-id="e6d06-119">Encrypt operating systems and disk drives where data is stored with a full-volume encryption system, unless you can guarantee constant and complete control of the servers, total physical isolation, and proper and secure decommissioning of replaced or failed disk drives.</span></span>

  - <span data-ttu-id="e6d06-120">Deshabilite todos los puertos de acceso directo a memoria (DMA) externos del servidor, a menos que pueda garantizar un control muy estricto sobre el acceso físico a los servidores.</span><span class="sxs-lookup"><span data-stu-id="e6d06-120">Disable all external Direct Memory Access (DMA) ports of the server, unless you can guarantee very tight control over the physical access to the servers.</span></span> <span data-ttu-id="e6d06-121">Los ataques basados en DMA, que se pueden iniciar con bastante facilidad, pueden exponer información muy confidencial, como las claves de cifrado privadas.</span><span class="sxs-lookup"><span data-stu-id="e6d06-121">DMA-based attacks, which can be initiated fairly easily, could expose very sensitive information, such as private encryption keys.</span></span>

<span data-ttu-id="e6d06-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e6d06-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

