---
title: 'Lync Server 2013: Comprobar la conectividad de usuarios externos'
description: 'Lync Server 2013: comprobar la conectividad de los usuarios externos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify connectivity for external users
ms:assetid: 5c02bd6e-1c96-448a-a21d-58c9961c6640
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398402(v=OCS.15)
ms:contentKeyID: 48184249
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50ef728157d01b93e7d0b8420442ce083a42b5b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399779"
---
# <a name="verify-connectivity-for-external-users-in-lync-server-2013"></a><span data-ttu-id="de160-103">Comprobar la conectividad de usuarios externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de160-103">Verify connectivity for external users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de160-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de160-104">

<span> </span></span></span>

<span data-ttu-id="de160-105">_**Última modificación del tema:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="de160-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="de160-106">La validación de la conectividad de los usuarios externos requiere garantizar la conectividad de los usuarios con el servidor y el puerto del servicio perimetral de acceso.</span><span class="sxs-lookup"><span data-stu-id="de160-106">Validating connectivity for external users requires ensuring connectivity from users to the server and port for the Access Edge service.</span></span>

<span data-ttu-id="de160-107">Un recurso muy útil para confirmar la configuración y la capacidad de conectar, enviar y recibir los mensajes correctos para los escenarios que requiere el acceso de usuarios externos es el analizador de conectividad remota ( <http://www.testocsconnectivity.com> ).</span><span class="sxs-lookup"><span data-stu-id="de160-107">A valuable resource for confirming your configuration and the ability to connect, send and receive the correct messages for the scenarios that external user access requires is the Remote Connectivity Analyzer site (<http://www.testocsconnectivity.com>).</span></span> <span data-ttu-id="de160-108">El sitio es administrado y mantenido por el soporte técnico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="de160-108">The site is managed and maintained by Microsoft Support.</span></span> <span data-ttu-id="de160-109">Para comunicarse con el analizador de conectividad remota, abra el sitio web en un explorador y siga las instrucciones para seleccionar el escenario.</span><span class="sxs-lookup"><span data-stu-id="de160-109">To reach the Remote Connectivity Analyzer, open the Web site in a browser and follow the instructions to select the scenario.</span></span>

<div>

## <a name="test-connectivity-of-external-users-and-external-access"></a><span data-ttu-id="de160-110">Probar la conectividad de usuarios externos y acceso externo</span><span class="sxs-lookup"><span data-stu-id="de160-110">Test Connectivity of External Users and External access</span></span>

<span data-ttu-id="de160-111">Las pruebas para el acceso de usuarios externos deben incluir cada tipo de usuario externo que admita su organización, incluidos cualquiera de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="de160-111">Tests for external user access should include each type of external user that your organization supports, including any or all of the following:</span></span>

  - <span data-ttu-id="de160-112">Usuarios de al menos un dominio federado y prueba la mensajería instantánea, la presencia, A/V y el uso compartido del escritorio.</span><span class="sxs-lookup"><span data-stu-id="de160-112">Users from at least one federated domain, and test IM, presence, A/V and desktop sharing.</span></span>

  - <span data-ttu-id="de160-113">Usuarios de cada proveedor de servicios de mensajería instantánea pública que admita su organización (y para el que se ha completado el aprovisionamiento).</span><span class="sxs-lookup"><span data-stu-id="de160-113">Users of each public IM service provider that your organization supports (and for which provisioning has been completed).</span></span>

  - <span data-ttu-id="de160-114">Usuarios anónimos.</span><span class="sxs-lookup"><span data-stu-id="de160-114">Anonymous users.</span></span>

  - <span data-ttu-id="de160-115">Los usuarios de su organización que hayan iniciado sesión en Lync de forma remota, pero no utilicen VPN.</span><span class="sxs-lookup"><span data-stu-id="de160-115">Users within your organization who are logged into Lync remotely, but not using VPN.</span></span>

<span data-ttu-id="de160-116">Estas pruebas determinan si su servidor perimetral es:</span><span class="sxs-lookup"><span data-stu-id="de160-116">These tests determine whether your Edge Server is:</span></span>

  - <span data-ttu-id="de160-117">Escucha en los puertos necesarios a través de un cliente de telnet de fuera de la red.</span><span class="sxs-lookup"><span data-stu-id="de160-117">Listening on the necessary ports by using a telnet client from outside your network.</span></span>
    
      - <span data-ttu-id="de160-118">Ejemplo: Telnet sip.contoso.com 443</span><span class="sxs-lookup"><span data-stu-id="de160-118">Example: telnet sip.contoso.com 443</span></span>
    
      - <span data-ttu-id="de160-119">Realice la prueba anterior en los puertos que está usando en el servidor perimetral o en el grupo de servidores perimetrales dependiendo de su implementación.</span><span class="sxs-lookup"><span data-stu-id="de160-119">Perform the preceding test on ports you are using on the Edge Server or Edge Server pool depending on your deployment.</span></span>

  - <span data-ttu-id="de160-120">Logre una resolución de DNS externa precisa.</span><span class="sxs-lookup"><span data-stu-id="de160-120">Performing accurate external DNS resolution.</span></span>
    
      - <span data-ttu-id="de160-121">Desde fuera de la red haga ping a cada uno de los FQDN externos de su grupo perimetral o perimetral.</span><span class="sxs-lookup"><span data-stu-id="de160-121">From outside your network ping each of the external FQDN’s of your Edge or Edge pool.</span></span> <span data-ttu-id="de160-122">Incluso si se produce un error en la ping, verá las direcciones IP, que puede comparar con las que ha asignado.</span><span class="sxs-lookup"><span data-stu-id="de160-122">Even if the ping fails you will see the IP addresses, which you can compare to the ones you have assigned.</span></span>

<span data-ttu-id="de160-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de160-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

