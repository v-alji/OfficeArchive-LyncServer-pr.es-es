---
title: 'Lync Server 2013: Implementar el control remoto de llamadas'
description: 'Lync Server 2013: implementación de control de llamada remota.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying remote call control
ms:assetid: 763037f7-7a2a-49ae-acc3-9781b0bff7e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558664(v=OCS.15)
ms:contentKeyID: 48184536
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cc5e79f3ee44c354baf435585d304574d6a980c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429786"
---
# <a name="deploying-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="2ebd3-103">Implementar el control remoto de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ebd3-103">Deploying remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2ebd3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2ebd3-104">

<span> </span></span></span>

<span data-ttu-id="2ebd3-105">_**Última modificación del tema:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="2ebd3-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="2ebd3-106">Esta sección le guiará a través del proceso de implementación de la funcionalidad de control de llamadas remotas a los usuarios de su organización.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-106">This section guides you through the process of deploying remote call control functionality to users in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2ebd3-107">Aunque las características de control remoto de llamadas están disponibles para los usuarios remotos mientras están fuera del firewall de la organización, los detalles sobre la implementación de escenarios de acceso externo están fuera del ámbito de esta documentación.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-107">Although remote call control features are available to remote users while they are outside of your organization’s firewall, details about deploying external access scenarios are beyond the scope of this documentation.</span></span> <span data-ttu-id="2ebd3-108">Para obtener detalles sobre cómo implementar el acceso de usuarios externos, vea <A href="lync-server-2013-deploying-external-user-access.md">implementar el acceso de usuarios externos en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="2ebd3-108">For details about deploying external user access, see <A href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2ebd3-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2ebd3-109">In This Section</span></span>

  - [<span data-ttu-id="2ebd3-110">Configurar Lync Server 2013 para enrutar a una puerta de enlace SIP/CSTA</span><span class="sxs-lookup"><span data-stu-id="2ebd3-110">Configuring Lync Server 2013 to route to a SIP/CSTA gateway</span></span>](lync-server-2013-configuring-lync-server-to-route-to-a-sip-csta-gateway.md)

  - [<span data-ttu-id="2ebd3-111">Configurar una ruta estática para el control remoto de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ebd3-111">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)

  - [<span data-ttu-id="2ebd3-112">Configurar una entrada de aplicación de confianza para control remoto de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ebd3-112">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)

  - <span data-ttu-id="2ebd3-113">[Definir una dirección IP de puerta de enlace SIP/CSTA en Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) (solo si la puerta de enlace está configurada para usar TCP)</span><span class="sxs-lookup"><span data-stu-id="2ebd3-113">[Define a SIP/CSTA gateway IP address in Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) (only if the gateway is configured to use TCP)</span></span>

  - [<span data-ttu-id="2ebd3-114">Habilitar a los usuarios de Lync para el control remoto de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ebd3-114">Enable Lync users for remote call control in Lync Server 2013</span></span>](lync-server-2013-enable-lync-users-for-remote-call-control.md)

  - [<span data-ttu-id="2ebd3-115">Control remoto de llamadas y normalización de números de teléfono en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ebd3-115">Remote call control and phone number normalization in Lync Server 2013</span></span>](lync-server-2013-remote-call-control-and-phone-number-normalization.md)

  - <span data-ttu-id="2ebd3-116">[Quitar un host autorizado heredado en Lync Server 2013 (opcional)](lync-server-2013-remove-a-legacy-authorized-host-optional.md) (solo si está migrando usuarios previamente habilitados para el control remoto de llamadas)</span><span class="sxs-lookup"><span data-stu-id="2ebd3-116">[Remove a legacy authorized host in Lync Server 2013 (optional)](lync-server-2013-remove-a-legacy-authorized-host-optional.md) (only if you are migrating users previously enabled for remote call control)</span></span>

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="2ebd3-117">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="2ebd3-117">Related Sections</span></span>

[<span data-ttu-id="2ebd3-118">Planear el control remoto de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ebd3-118">Planning for remote call control in Lync Server 2013</span></span>](lync-server-2013-planning-for-remote-call-control.md)

<span data-ttu-id="2ebd3-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2ebd3-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

