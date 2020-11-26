---
title: 'Lync Server 2013: Configurar la compatibilidad con dominios externos bloqueados'
description: 'Lync Server 2013: configurar la compatibilidad con dominios externos bloqueados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure support for blocked external domains
ms:assetid: 49103138-e1ab-42bf-91aa-57cf23bbf260
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619176(v=OCS.15)
ms:contentKeyID: 49733638
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81c2c76dc32dd5e8d458dad4e91ff375d2ab005c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433678"
---
# <a name="configure-support-for-blocked-external-domains-in-lync-server-2013"></a><span data-ttu-id="700f6-103">Configurar la compatibilidad con dominios externos bloqueados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="700f6-103">Configure support for blocked external domains in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="700f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="700f6-104">

<span> </span></span></span>

<span data-ttu-id="700f6-105">_**Última modificación del tema:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="700f6-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="700f6-106">Si ha configurado la compatibilidad con los socios federados, puede administrar los dominios que estarán bloqueados para que no se federen con su organización.</span><span class="sxs-lookup"><span data-stu-id="700f6-106">If you have configured support for federated partners, you can manage which domains will be blocked from federating with your organization.</span></span> <span data-ttu-id="700f6-107">La lista de dominios bloqueados actuará como una lista de bloqueados (lista de entradas explícitas no permitidas) y se aplicará en la detección de dominios federados, si tiene esta opción habilitada.</span><span class="sxs-lookup"><span data-stu-id="700f6-107">The list of blocked domains will act as a block list (listing of explicit entries that are not to be allowed) and will apply in federated domain discovery, if you have this option enabled.</span></span> <span data-ttu-id="700f6-108">Para obtener más información, vea [habilitar o deshabilitar la detección de socios de Federación en Lync Server 2013](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md).</span><span class="sxs-lookup"><span data-stu-id="700f6-108">For details, see [Enable or disable discovery of federation partners in Lync Server 2013](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md).</span></span>

<span data-ttu-id="700f6-109">Bloquear la conexión de uno o varios dominios externos a su organización.</span><span class="sxs-lookup"><span data-stu-id="700f6-109">Block one or more external domains from connecting to your organization.</span></span> <span data-ttu-id="700f6-110">Para ello, agregue el dominio a la lista de dominios bloqueados.</span><span class="sxs-lookup"><span data-stu-id="700f6-110">To do this, add the domain to the list of blocked domains.</span></span>

<div>

## <a name="to-add-an-external-domain-to-the-list-of-blocked-domains"></a><span data-ttu-id="700f6-111">Para agregar un dominio externo a la lista de dominios bloqueados</span><span class="sxs-lookup"><span data-stu-id="700f6-111">To add an external domain to the list of blocked domains</span></span>

1.  <span data-ttu-id="700f6-112">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="700f6-112">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="700f6-113">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="700f6-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="700f6-114">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="700f6-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="700f6-115">En la barra de navegación izquierda, haga clic en **acceso de usuarios externos**.</span><span class="sxs-lookup"><span data-stu-id="700f6-115">In the left navigation bar, click **External User Access**.</span></span>

4.  <span data-ttu-id="700f6-116">Haga clic en **dominios federados**, en **nuevo** y, a continuación, en **dominio bloqueado**.</span><span class="sxs-lookup"><span data-stu-id="700f6-116">Click **Federated Domains**, click **New**, and then click **Blocked domain**.</span></span>

5.  <span data-ttu-id="700f6-117">En **nuevos dominios federados**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="700f6-117">In **New Federated Domains**, do the following:</span></span>
    
      - <span data-ttu-id="700f6-118">En **nombre de dominio (o FQDN)**, escriba el nombre del dominio del socio federado que desea bloquear.</span><span class="sxs-lookup"><span data-stu-id="700f6-118">In **Domain name (or FQDN)**, type the name of the federated partner domain that you want to block.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="700f6-119">El nombre no puede superar los 256 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="700f6-119">The name cannot exceed 256 characters in length.</span></span><BR><span data-ttu-id="700f6-120">La búsqueda en el nombre de dominio del socio federado realiza una coincidencia de sufijo.</span><span class="sxs-lookup"><span data-stu-id="700f6-120">The search on the federated partner domain name performs a suffix match.</span></span> <span data-ttu-id="700f6-121">Por ejemplo, si escribe <STRONG>contoso.com</STRONG>, la búsqueda también devolverá el dominio <STRONG>it.contoso.com</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="700f6-121">For example, if you type <STRONG>contoso.com</STRONG>, the search will also return the domain <STRONG>it.contoso.com</STRONG>.</span></span><BR><span data-ttu-id="700f6-122">Un dominio del socio federado no puede bloquearse y permitirse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="700f6-122">A federated partner domain cannot simultaneously be blocked and allowed.</span></span> <span data-ttu-id="700f6-123">Lync Server 2013 impide que esto suceda, por lo que no es necesario sincronizar las listas.</span><span class="sxs-lookup"><span data-stu-id="700f6-123">Lync Server 2013 prevents this from happening so that you do not have to synch up your lists.</span></span>

        
        </div>
    
      - <span data-ttu-id="700f6-124">Faculta En **Comentario**, escriba la información que desea compartir con otros administradores del sistema acerca de esta configuración.</span><span class="sxs-lookup"><span data-stu-id="700f6-124">(Optional) In **Comment**, type information that you want to share with other system administrators about this configuration.</span></span>

6.  <span data-ttu-id="700f6-125">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="700f6-125">Click **Commit**.</span></span>

7.  <span data-ttu-id="700f6-126">Repita los pasos 4 a 6 para cada socio federado que desee bloquear.</span><span class="sxs-lookup"><span data-stu-id="700f6-126">Repeat steps 4 through 6 for each federated partner that you want to block.</span></span>

<span data-ttu-id="700f6-127">Para habilitar el acceso de usuarios federados, también debe habilitar la compatibilidad con el acceso de usuarios federados de su organización.</span><span class="sxs-lookup"><span data-stu-id="700f6-127">To enable federated user access, you must also enable support for federated user access in your organization.</span></span> <span data-ttu-id="700f6-128">Para obtener más información, vea [habilitar o deshabilitar el acceso de usuarios remotos en Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="700f6-128">For details, see [Enable or disable remote user access in Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span></span>

<span data-ttu-id="700f6-129">Además, debe configurar y aplicar la Directiva a los usuarios que desee que puedan colaborar con los usuarios federados.</span><span class="sxs-lookup"><span data-stu-id="700f6-129">Additionally, you must configure and apply the policy to users that you want to be able to collaborate with federated users.</span></span> <span data-ttu-id="700f6-130">Para obtener más información, vea [configurar directivas para controlar el acceso de usuarios federados en Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="700f6-130">For details, see [Configure policies to control federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span></span>

<span data-ttu-id="700f6-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="700f6-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

