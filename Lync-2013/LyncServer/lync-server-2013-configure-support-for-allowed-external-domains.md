---
title: 'Lync Server 2013: Configurar la compatibilidad con dominios externos permitidos'
description: 'Lync Server 2013: configurar la compatibilidad para dominios externos permitidos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure support for allowed external domains
ms:assetid: 3ee6e175-986d-4c33-b03a-b9f93083dca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425908(v=OCS.15)
ms:contentKeyID: 48183943
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 13845638bca8791d43b8644c5dcb30ec73751a5b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433685"
---
# <a name="configure-support-for-allowed-external-domains-in-lync-server-2013"></a><span data-ttu-id="7e84d-103">Configurar la compatibilidad con dominios externos permitidos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7e84d-103">Configure support for allowed external domains in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7e84d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7e84d-104">

<span> </span></span></span>

<span data-ttu-id="7e84d-105">_**Última modificación del tema:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="7e84d-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="7e84d-106">Si ha configurado la compatibilidad con los socios federados, puede administrar los dominios específicos que se pueden federar con su organización.</span><span class="sxs-lookup"><span data-stu-id="7e84d-106">If you have configured support for federated partners, you can manage which specific domains can federate with your organization.</span></span> <span data-ttu-id="7e84d-107">Configure uno o varios dominios externos específicos como dominios federados permitidos.</span><span class="sxs-lookup"><span data-stu-id="7e84d-107">You configure one or more specific external domains as allowed federated domains.</span></span> <span data-ttu-id="7e84d-108">Para ello, agregue cada dominio a la lista de dominios permitidos.</span><span class="sxs-lookup"><span data-stu-id="7e84d-108">To do this, add each domain to the list of allowed domains.</span></span> <span data-ttu-id="7e84d-109">Incluso si el descubrimiento de Partners está habilitado para su organización, haga esto si el dominio es un socio federado que puede que necesite comunicarse con más de 1.000 de sus usuarios o que necesite enviar más de 20 mensajes por segundo.</span><span class="sxs-lookup"><span data-stu-id="7e84d-109">Even if partner discovery is enabled for your organization, do this if the domain is a federated partner that might need to communicate with more than 1,000 of your users or might need to send more than 20 messages per second.</span></span> <span data-ttu-id="7e84d-110">Si el descubrimiento de Partners no está habilitado para su organización, solo los usuarios de dominios externos que agregue a la lista de dominios permitidos podrán participar en la mensajería instantánea y las conferencias con los usuarios de su organización.</span><span class="sxs-lookup"><span data-stu-id="7e84d-110">If partner discovery is not enabled for your organization, only users of external domains that you add to the allowed domains list can participate in IM and conferencing with users in your organization.</span></span> <span data-ttu-id="7e84d-111">Si desea restringir el acceso de un dominio federado a un servidor específico que ejecute el servicio perimetral de acceso del socio federado, puede especificar el nombre de dominio del servidor que ejecuta el servicio perimetral de acceso para cada dominio de la lista de dominios permitidos.</span><span class="sxs-lookup"><span data-stu-id="7e84d-111">If you want to restrict access for a federated domain to a specific server running the Access Edge service of the federated partner, you can specify the domain name of the server running the Access Edge service for each domain in the list of allowed domains.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7e84d-112">Este procedimiento describe cómo configurar la compatibilidad con dominios específicos, pero la implementación de soporte técnico para usuarios federados también requiere que habilite la compatibilidad con usuarios federados para su organización, y configure y aplique directivas para controlar qué usuarios pueden colaborar con usuarios federados.</span><span class="sxs-lookup"><span data-stu-id="7e84d-112">This procedure describes how to configure support for specific domains, but implementing support for federated users also requires that you enable support for federated users for your organization, and configure and apply policies to control which users can collaborate with federated users.</span></span> <span data-ttu-id="7e84d-113">Para obtener más información sobre cómo habilitar la compatibilidad para usuarios federados, consulte <A href="lync-server-2013-enable-or-disable-remote-user-access.md">habilitar o deshabilitar el acceso de usuarios remotos en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7e84d-113">For details about enabling support for federated users, see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A>.</span></span> <span data-ttu-id="7e84d-114">Para obtener más información sobre cómo configurar directivas para controlar la Federación, consulte <A href="lync-server-2013-configure-policies-to-control-federated-user-access.md">configurar directivas para controlar el acceso de usuarios federados en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7e84d-114">For details about configuring policies to control federation, see <A href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Configure policies to control federated user access in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-add-an-external-domain-to-the-list-of-allowed-domains"></a><span data-ttu-id="7e84d-115">Para agregar un dominio externo a la lista de dominios permitidos</span><span class="sxs-lookup"><span data-stu-id="7e84d-115">To add an external domain to the list of allowed domains</span></span>

1.  <span data-ttu-id="7e84d-116">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="7e84d-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="7e84d-117">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7e84d-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7e84d-118">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7e84d-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7e84d-119">En la barra de navegación izquierda, haga clic en **acceso de usuarios externos** y, a continuación, en **dominios federados**.</span><span class="sxs-lookup"><span data-stu-id="7e84d-119">In the left navigation bar, click **External User Access**, and then click **Federated Domains**.</span></span>

4.  <span data-ttu-id="7e84d-120">En la página **dominios federados** , haga clic en **nuevo** y, a continuación, haga clic en **dominio permitido**.</span><span class="sxs-lookup"><span data-stu-id="7e84d-120">On the **Federated Domains** page, click **New**, and then click **Allowed domain**.</span></span>

5.  <span data-ttu-id="7e84d-121">En **nuevos dominios federados**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7e84d-121">In **New Federated Domains**, do the following:</span></span>
    
      - <span data-ttu-id="7e84d-122">En **nombre de dominio (o FQDN)**, escriba el nombre del dominio del socio federado.</span><span class="sxs-lookup"><span data-stu-id="7e84d-122">In **Domain name (or FQDN)**, type the name of the federated partner domain.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="7e84d-123">Este nombre debe ser único y no puede existir como dominio permitido para este servidor que ejecuta el servicio perimetral de acceso.</span><span class="sxs-lookup"><span data-stu-id="7e84d-123">This name must be unique and cannot already exist as an allowed domain for this server running the Access Edge service.</span></span> <span data-ttu-id="7e84d-124">El nombre no puede superar los 256 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="7e84d-124">The name cannot exceed 256 characters in length.</span></span><BR><span data-ttu-id="7e84d-125">La búsqueda en el nombre de dominio del socio federado realiza una coincidencia de sufijo.</span><span class="sxs-lookup"><span data-stu-id="7e84d-125">The search on the federated partner domain name performs a suffix match.</span></span> <span data-ttu-id="7e84d-126">Por ejemplo, si escribe <STRONG>contoso.com</STRONG>, la búsqueda también devolverá el dominio <STRONG>it.contoso.com</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7e84d-126">For example, if you type <STRONG>contoso.com</STRONG>, the search will also return the domain <STRONG>it.contoso.com</STRONG>.</span></span><BR><span data-ttu-id="7e84d-127">Un dominio del socio federado no puede bloquearse y permitirse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="7e84d-127">A federated partner domain cannot simultaneously be blocked and allowed.</span></span> <span data-ttu-id="7e84d-128">Lync Server 2013 impide que esto suceda, por lo que no es necesario sincronizar las listas.</span><span class="sxs-lookup"><span data-stu-id="7e84d-128">Lync Server 2013 prevents this from happening so that you do not have to synch up your lists.</span></span>

        
        </div>
    
      - <span data-ttu-id="7e84d-129">Si desea restringir el acceso a este dominio federado a los usuarios de un servidor específico que ejecute el servicio perimetral de acceso, en el **servicio perimetral de acceso (FQDN)**, escriba el FQDN del servidor del dominio federado que ejecuta el servicio perimetral de acceso.</span><span class="sxs-lookup"><span data-stu-id="7e84d-129">If you want to restrict access for this federated domain to users of a specific server running the Access Edge service, in **Access Edge service (FQDN)**, type the FQDN of the federated domain’s server running the Access Edge service.</span></span>
    
      - <span data-ttu-id="7e84d-130">Si desea proporcionar información adicional, en **Comentario**, escriba la información que desea compartir con otros administradores del sistema acerca de esta configuración.</span><span class="sxs-lookup"><span data-stu-id="7e84d-130">If you want to provide additional information, in **Comment**, type information that you want to share with other system administrators about this configuration.</span></span>

6.  <span data-ttu-id="7e84d-131">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="7e84d-131">Click **Commit**.</span></span>

7.  <span data-ttu-id="7e84d-132">Repita los pasos 4 a 6 para cada dominio de socio federado que desee permitir.</span><span class="sxs-lookup"><span data-stu-id="7e84d-132">Repeat steps 4 through 6 for each federated partner domain that you want to allow.</span></span>

<span data-ttu-id="7e84d-133">Para habilitar el acceso de usuarios federados, también debe habilitar la compatibilidad con el acceso de usuarios federados de su organización.</span><span class="sxs-lookup"><span data-stu-id="7e84d-133">To enable federated user access, you must also enable support for federated user access in your organization.</span></span> <span data-ttu-id="7e84d-134">Para obtener más información, vea [habilitar o deshabilitar el acceso de usuarios remotos en Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="7e84d-134">For details, see [Enable or disable remote user access in Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span></span>

<span data-ttu-id="7e84d-135">Además, debe configurar y aplicar la Directiva a los usuarios que desee que puedan colaborar con los usuarios federados.</span><span class="sxs-lookup"><span data-stu-id="7e84d-135">Additionally, you must configure and apply the policy to users that you want to be able to collaborate with federated users.</span></span> <span data-ttu-id="7e84d-136">Para obtener más información, vea [configurar directivas para controlar el acceso de usuarios federados en Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="7e84d-136">For details, see [Configure policies to control federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span></span>

<span data-ttu-id="7e84d-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7e84d-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

