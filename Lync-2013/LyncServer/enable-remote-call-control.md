---
title: Habilitar control remoto de llamadas
description: Habilitar el control remoto de llamadas.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Enable remote call control
ms:assetid: 0b91d418-e6ed-4556-97af-e8523e01f249
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204664(v=OCS.15)
ms:contentKeyID: 48183380
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8009ffc927ad3f7a4f83ad3505100f3a9d4e82d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398783"
---
# <a name="enable-remote-call-control"></a><span data-ttu-id="2dcee-103">Habilitar control remoto de llamadas</span><span class="sxs-lookup"><span data-stu-id="2dcee-103">Enable remote call control</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2dcee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2dcee-104">

<span> </span></span></span>

<span data-ttu-id="2dcee-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="2dcee-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="2dcee-106">El control remoto de llamadas permite a los usuarios controlar sus teléfonos de escritorio privado de escritorio (PBX) con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2dcee-106">Remote call control enables users to control their desktop private branch exchange (PBX) phones by using Lync Server 2013.</span></span> <span data-ttu-id="2dcee-107">Si ha implementado el control remoto de llamadas en su entorno heredado y desea migrar it Lync Server 2013, debe realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="2dcee-107">If you deployed remote call control in your legacy environment and want to migrate it Lync Server 2013, you need to perform the following tasks:</span></span>

1.  <span data-ttu-id="2dcee-108">Instala una puerta de enlace SIP/CSTA y configúrela para comunicarse con tu PBX.</span><span class="sxs-lookup"><span data-stu-id="2dcee-108">Install a SIP/CSTA gateway and configure it to communicate with your PBX.</span></span> <span data-ttu-id="2dcee-109">Debe realizar este paso al implementar el grupo piloto de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2dcee-109">You need to do this step when you deploy your Lync Server 2013 pilot pool.</span></span>

2.  <span data-ttu-id="2dcee-110">Después de combinar su topología y migrar las directivas y la configuración, configure Lync Server 2013 para que enruten las solicitudes de CSTA a la puerta de enlace SIP/CSTA.</span><span class="sxs-lookup"><span data-stu-id="2dcee-110">After you merge your topology and migrate your policies and settings, configure Lync Server 2013 to route CSTA requests to the SIP/CSTA gateway.</span></span> <span data-ttu-id="2dcee-111">Este paso es un paso manual que sigue la migración automática.</span><span class="sxs-lookup"><span data-stu-id="2dcee-111">This step is a manual step that follows the automated migration.</span></span> <span data-ttu-id="2dcee-112">Para configurar el enrutamiento de las solicitudes de CSTA, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2dcee-112">To configure routing for CSTA requests, do the following:</span></span>
    
      - <span data-ttu-id="2dcee-113">Elimine las entradas de host autorizadas heredadas (conocidas como *entradas de servidor de confianza* en Lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="2dcee-113">Remove legacy authorized host entries (known as *trusted server entries* in Lync Server 2013).</span></span> <span data-ttu-id="2dcee-114">Si va a migrar usuarios de la implementación heredada, asegúrese de quitar todas las entradas de host autorizadas existentes que haya creado para la puerta de enlace SIP/CSTA antes de configurar las nuevas entradas de aplicaciones de confianza en el grupo piloto de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2dcee-114">If you are migrating users from your legacy deployment, ensure that you remove all existing authorized host entries that you created for the SIP/CSTA gateway before you configure new trusted application entries on the Lync Server 2013 pilot pool.</span></span> <span data-ttu-id="2dcee-115">Para obtener más información sobre cómo quitar entradas de host heredadas, consulte [quitar una entrada de host autorizado](remove-an-authorized-host-entry.md).</span><span class="sxs-lookup"><span data-stu-id="2dcee-115">For details about how to remove legacy authorized host entries, see [Remove an authorized host entry](remove-an-authorized-host-entry.md).</span></span>
    
      - <span data-ttu-id="2dcee-116">Configurar una ruta estática para el control remoto de llamadas.</span><span class="sxs-lookup"><span data-stu-id="2dcee-116">Configure a static route for remote call control.</span></span> <span data-ttu-id="2dcee-117">Puede configurar una ruta estática para agrupaciones individuales que desee que admitan el control remoto de llamadas o puede configurar una ruta estática global para que cada grupo de servidores que no esté configurado con una ruta estática en el nivel de grupo use la ruta estática global.</span><span class="sxs-lookup"><span data-stu-id="2dcee-117">You can configure a static route for individual pools that you want to support remote call control, or you can configure a global static route so that each pool that is not configured with a pool-level static route uses the global static route.</span></span> <span data-ttu-id="2dcee-118">Para obtener más información sobre cómo configurar la ruta estática, vea [configurar una ruta estática para el control remoto de llamadas en Lync Server 2013](lync-server-2013-configure-a-static-route-for-remote-call-control.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="2dcee-118">For details about how to configure the static route, see [Configure a static route for remote call control in Lync Server 2013](lync-server-2013-configure-a-static-route-for-remote-call-control.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="2dcee-119">Configure una entrada de aplicación de confianza para el control remoto de llamadas en cada grupo para el que desee admitir el control remoto de llamadas.</span><span class="sxs-lookup"><span data-stu-id="2dcee-119">Configure a trusted application entry for remote call control on each pool for which you want to support remote call control.</span></span> <span data-ttu-id="2dcee-120">Para obtener más información sobre cómo configurar una entrada de aplicación de confianza, vea [configurar una entrada de aplicación de confianza para el control remoto de llamadas en Lync Server 2013](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="2dcee-120">For details about how to configure a trusted application entry, see [Configure a trusted application entry for remote call control in Lync Server 2013](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md) in the Deployment documentation.</span></span>

3.  <span data-ttu-id="2dcee-121">Si ha implementado una puerta de enlace SIP/CSTA que usa el protocolo de control de transmisión (TCP) para conectarse a Lync Server 2013, defina la dirección IP de la puerta de enlace en el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="2dcee-121">If you deployed a SIP/CSTA gateway that uses Transmission Control Protocol (TCP) to connect to Lync Server 2013, define the IP address of the gateway in Topology Builder.</span></span> <span data-ttu-id="2dcee-122">Para obtener más información sobre cómo definir la dirección IP, consulte [definir una dirección IP de puerta de enlace SIP/CSTA en Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="2dcee-122">For details about defining the IP address, see [Define a SIP/CSTA gateway IP address in Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) in the Deployment documentation.</span></span>

4.  <span data-ttu-id="2dcee-123">Configure los usuarios de Lync 2013 para el control remoto de llamadas habilitando el control remoto de llamadas y asignando un identificador uniforme de recursos (URI) de line Server y un URI de línea.</span><span class="sxs-lookup"><span data-stu-id="2dcee-123">Configure Lync 2013 users for remote call control by enabling remote call control and assigning a line server Uniform Resource Identifier (URI) and a line URI.</span></span> <span data-ttu-id="2dcee-124">Al migrar usuarios de la implementación heredada a Lync Server 2013, se migra la configuración de control de llamada remota junto con la configuración del otro usuario.</span><span class="sxs-lookup"><span data-stu-id="2dcee-124">When you migrate users from your legacy deployment to Lync Server 2013, the remote call control settings are migrated along with the other user settings.</span></span>

5.  <span data-ttu-id="2dcee-125">Si ha personalizado las reglas de normalización de números de teléfono de la libreta de direcciones en la implementación heredada, tendrá que realizar algunas tareas manuales una vez completada la migración automática de las directivas y la configuración para migrar las reglas de normalización personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2dcee-125">If you customized Address Book phone number normalization rules in your legacy deployment, you need to perform some manual tasks after the automated migration of policies and settings is complete to migrate the customized normalization rules.</span></span> <span data-ttu-id="2dcee-126">Si no ha personalizado las reglas de normalización, la libreta de direcciones se migrará junto con el resto de la topología.</span><span class="sxs-lookup"><span data-stu-id="2dcee-126">If you did not customize normalization rules, Address Book is migrated along with the rest of your topology.</span></span> <span data-ttu-id="2dcee-127">Para obtener detalles sobre la migración manual de reglas de normalización, consulte [migrar la libreta de direcciones](migrate-address-book.md).</span><span class="sxs-lookup"><span data-stu-id="2dcee-127">For details about manually migrating customized normalization rules, see [Migrate Address Book](migrate-address-book.md).</span></span>

<span data-ttu-id="2dcee-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2dcee-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

