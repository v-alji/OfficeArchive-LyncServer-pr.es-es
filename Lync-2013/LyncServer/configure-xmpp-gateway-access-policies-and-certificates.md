---
title: Configurar certificados y directivas de acceso por puerta de enlace XMPP
description: Configure certificados y directivas de acceso de puerta de enlace XMPP.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure XMPP gateway access policies and certificates
ms:assetid: fac02f4e-d14d-4be3-b53c-74c82436fd93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721945(v=OCS.15)
ms:contentKeyID: 49733882
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e958100501ad9ca87d1ab970162f4be8c7692a99
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398357"
---
# <a name="configure-xmpp-gateway-access-policies-and-certificates"></a><span data-ttu-id="acbae-103">Configurar certificados y directivas de acceso por puerta de enlace XMPP</span><span class="sxs-lookup"><span data-stu-id="acbae-103">Configure XMPP gateway access policies and certificates</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="acbae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="acbae-104">

<span> </span></span></span>

<span data-ttu-id="acbae-105">_**Última modificación del tema:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="acbae-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="acbae-106">La Federación XMPP define una implementación externa basada en el protocolo de presencia y mensajería extensible (XMPP).</span><span class="sxs-lookup"><span data-stu-id="acbae-106">XMPP federation defines an external deployment based on the eXtensible Messaging and Presence Protocol (XMPP).</span></span> <span data-ttu-id="acbae-107">Una configuración XMPP permite a los usuarios de Lync acceder a los usuarios del dominio XMPP de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="acbae-107">An XMPP configuration allows Lync users access to XMPP domain users by:</span></span>

  - <span data-ttu-id="acbae-108">Mensajería instantánea y presencia: solo para personas</span><span class="sxs-lookup"><span data-stu-id="acbae-108">IM and Presence – person to person only</span></span>

  - <span data-ttu-id="acbae-109">Creación de los contactos de XMPP federados en el cliente de Lync</span><span class="sxs-lookup"><span data-stu-id="acbae-109">Creation of XMPP federated contacts in the Lync client</span></span>

<span data-ttu-id="acbae-110">Al configurar directivas para la compatibilidad de los socios federados protocolo de presencia y mensajería extensible (XMPP), las directivas se aplican a los usuarios de XMPP Federated Domains, pero no a los usuarios de proveedores de servicios de mensajería instantánea (mi) o de protocolo de inicio de sesión (por ejemplo, Windows Live) ni a los dominios federados de SIP.</span><span class="sxs-lookup"><span data-stu-id="acbae-110">When you configure policies for support of extensible messaging and presence protocol (XMPP) federated partners, the policies apply to users of XMPP federated domains, but not to users of session initiation protocol (SIP) instant messaging (IM) service providers (for example, Windows Live), or SIP federated domains.</span></span> <span data-ttu-id="acbae-111">Configure un socio de XMPP federado para cada dominio de XMPP federado que desee permitir a los usuarios que añadan contactos y se comuniquen con ellos.</span><span class="sxs-lookup"><span data-stu-id="acbae-111">You configure an XMPP Federated Partner for each XMPP federated domain that you want to allow your users to add contacts and communicate with.</span></span> <span data-ttu-id="acbae-112">Una vez que las directivas estén en vigor, tendrá que configurar los certificados de la puerta de enlace XMPP.</span><span class="sxs-lookup"><span data-stu-id="acbae-112">Once the policies are in place, you need to configure the XMPP Gateway certificates.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="acbae-113">Para comenzar la migración de la puerta de enlace XMPP, debe implementar la puerta de enlace 2013 XMPP de Lync Server y configurar directivas de acceso para habilitar usuarios para la puerta de enlace XMPP de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="acbae-113">To begin the XMPP Gateway migration, you need to deploy the Lync Server 2013 XMPP Gateway, and configure access policies to enable users for Lync Server 2013 XMPP Gateway.</span></span> <span data-ttu-id="acbae-114">Debe mover todos los usuarios a la implementación de Lync Server 2013 antes de realizar estos pasos.</span><span class="sxs-lookup"><span data-stu-id="acbae-114">All users must be moved to the Lync Server 2013 deployment before you perform these steps.</span></span> <span data-ttu-id="acbae-115">Para obtener más información, consulte <A href="configure-xmpp-gateway-on-lync-server-2013.md">configurar la puerta de enlace XMPP en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="acbae-115">For details, see <A href="configure-xmpp-gateway-on-lync-server-2013.md">Configure XMPP gateway on Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="configure-an-external-access-policy-to-enable-users-for-lync-server-2013-xmpp-gateway"></a><span data-ttu-id="acbae-116">Configurar una directiva de acceso externo para habilitar usuarios en la puerta de enlace de Lync Server 2013 XMPP</span><span class="sxs-lookup"><span data-stu-id="acbae-116">Configure an External Access Policy to Enable Users for Lync Server 2013 XMPP Gateway</span></span>

1.  <span data-ttu-id="acbae-117">Abra el Panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="acbae-117">Open Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="acbae-118">En la barra de navegación izquierda, haga clic en **Federación y acceso externo** y, después, haga clic en **Directiva de acceso externo**.</span><span class="sxs-lookup"><span data-stu-id="acbae-118">In the left navigation bar, click **Federation and External Access**, and then click **External Access Policy**.</span></span>

3.  <span data-ttu-id="acbae-119">Haga clic en **nuevo** y, a continuación, en **Directiva de usuario**.</span><span class="sxs-lookup"><span data-stu-id="acbae-119">Click **New** and then click **User policy**.</span></span>

4.  <span data-ttu-id="acbae-120">Escriba un nombre para la Directiva de usuario de acceso externo.</span><span class="sxs-lookup"><span data-stu-id="acbae-120">Enter a name for the external access user policy.</span></span>

5.  <span data-ttu-id="acbae-121">Proporcione una descripción para la Directiva de usuario de acceso externo.</span><span class="sxs-lookup"><span data-stu-id="acbae-121">Provide a description for external access user policy.</span></span>

6.  <span data-ttu-id="acbae-122">Seleccione **Habilitar comunicaciones con usuarios federados**.</span><span class="sxs-lookup"><span data-stu-id="acbae-122">Select **Enable communications with federated users**.</span></span>

7.  <span data-ttu-id="acbae-123">Seleccione **Habilitar comunicaciones con usuarios federados de XMPP**.</span><span class="sxs-lookup"><span data-stu-id="acbae-123">Select **Enable communications with XMPP federated users**.</span></span>

8.  <span data-ttu-id="acbae-124">Haga clic en **confirmar** para guardar los cambios en el sitio o en la Directiva de usuario.</span><span class="sxs-lookup"><span data-stu-id="acbae-124">Click **Commit** to save your changes to the site or user policy.</span></span>

<span data-ttu-id="acbae-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="acbae-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

