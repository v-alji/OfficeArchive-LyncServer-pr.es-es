---
title: 'Lync Server 2013: Administrar la configuración perimetral de acceso para su organización'
description: 'Lync Server 2013: administrar la configuración perimetral de acceso de su organización.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage Access Edge Configuration for your organization
ms:assetid: 0145eb08-984f-4ecd-bf9c-364817619c2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552443(v=OCS.15)
ms:contentKeyID: 48679555
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2161385f9c03f025bcf6f5e599b7e0276f6d592c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426140"
---
# <a name="manage-access-edge-configuration-for-your-organization-in-lync-server-2013"></a><span data-ttu-id="b72fe-103">Administrar la configuración perimetral de acceso para su organización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b72fe-103">Manage Access Edge Configuration for your organization in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b72fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b72fe-104">

<span> </span></span></span>

<span data-ttu-id="b72fe-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="b72fe-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="b72fe-106">Esta documentación es preliminar y está sujeta a cambios.</span><span class="sxs-lookup"><span data-stu-id="b72fe-106">This is preliminary documentation and is subject to change.</span></span> <span data-ttu-id="b72fe-107">Los temas en blanco que se incluyen actúan como marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="b72fe-107">Blank topics are included as placeholders.</span></span>

<span data-ttu-id="b72fe-108">Después de implementar uno o varios servidores perimetrales, debe habilitar el acceso de los tipos de dominios externos o proveedores, el acceso de usuarios remotos y el acceso de usuarios anónimos a las conferencias a través de los servidores perimetrales que serán compatibles con su organización.</span><span class="sxs-lookup"><span data-stu-id="b72fe-108">After deploying one or more Edge Servers, you must enable the types of external domain or provider access, remote user access, and anonymous user access to conferences through the Edge Servers that will be supported for your organization.</span></span>

<span data-ttu-id="b72fe-109">Estas opciones incluyen los siguientes tipos de acceso que se pueden configurar a través de la página **configuración de Edge de Access** :</span><span class="sxs-lookup"><span data-stu-id="b72fe-109">These options include the following types of access that can be configured through the **Access Edge Configuration** page:</span></span>

  - <span data-ttu-id="b72fe-110">**Habilitar la Federación y la conectividad de mensajería instantánea pública**   Habilite esta opción si desea admitir el acceso de los usuarios a dominios federados.</span><span class="sxs-lookup"><span data-stu-id="b72fe-110">**Enable federation and public IM connectivity**   Enable this if you want to support user access to federated partner domains.</span></span> <span data-ttu-id="b72fe-111">Esta configuración se aplica a la Federación de SIP y a la Federación de XMPP que están configuradas para los ámbitos globales, de sitio o de usuario en la página de la **Directiva de acceso externo** .</span><span class="sxs-lookup"><span data-stu-id="b72fe-111">This setting applies to both SIP federation and XMPP federation that are configured for global, site or user scopes on the **External Access Policy** page.</span></span> <span data-ttu-id="b72fe-112">Para que se aplique la configuración de Federación, debe configurar la compatibilidad de Federación en ambas páginas.</span><span class="sxs-lookup"><span data-stu-id="b72fe-112">For federation settings to apply, you must configure federation support on both pages.</span></span>
    
    <span data-ttu-id="b72fe-113">Existen dos opciones opcionales para conocer el modo en que se descubren los socios federados y si archivar descargos de responsabilidad (la notificación a los contactos federados con los que se comunica la implementación tiene habilitado el archivado y se enviarán los detalles de las comunicaciones) a los contactos</span><span class="sxs-lookup"><span data-stu-id="b72fe-113">Two options exist that are optional settings for how federated partners are discovered, and whether archiving disclaimers (notification to federated contacts that you communicate with that your deployment has archiving enabled and that the communications details will be archived) will be sent to contacts</span></span>
    
      - <span data-ttu-id="b72fe-114">**Habilitar detección de dominios del socio**   Al seleccionar esta opción, se habilita la detección automática de dominios con los que se puede federar.</span><span class="sxs-lookup"><span data-stu-id="b72fe-114">**Enable partner domain discovery**   Selecting this option enables the automatic discovery of domains that you can federate with.</span></span> <span data-ttu-id="b72fe-115">Lync Server 2013 usa registros del sistema de nombres de dominio (DNS) para intentar descubrir dominios no incluidos en la lista de dominios permitidos, evaluar automáticamente el tráfico entrante de socios federados descubiertos y limitar o bloquear ese tráfico en función del nivel de confianza, la cantidad de tráfico y la configuración del administrador.</span><span class="sxs-lookup"><span data-stu-id="b72fe-115">Lync Server 2013 uses Domain Name System (DNS) records to try to discover domains not listed in the allowed domains list, automatically evaluating incoming traffic from discovered federated partners and limiting or blocking that traffic based on trust level, amount of traffic, and administrator settings.</span></span> <span data-ttu-id="b72fe-116">Si no selecciona esta opción, acceso de usuarios federados solo se habilitará para los usuarios de los dominios que incluya en la lista de dominios permitidos.</span><span class="sxs-lookup"><span data-stu-id="b72fe-116">If you do not select this option, federated user access is enabled only for users in the domains that you include on the allowed domains list.</span></span> <span data-ttu-id="b72fe-117">Independientemente de si selecciona esta opción, puede especificar que los dominios individuales se bloqueen o se permitan, incluido el acceso restringido a servidores específicos que ejecuten el servicio perimetral de acceso en el dominio federado.</span><span class="sxs-lookup"><span data-stu-id="b72fe-117">Whether or not you select this option, you can specify that individual domains to be blocked or allowed, including restricting access to specific servers running the Access Edge service in the federated domain.</span></span> <span data-ttu-id="b72fe-118">Para obtener más información, vea [configurar la compatibilidad de dominios externos permitidos en Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).</span><span class="sxs-lookup"><span data-stu-id="b72fe-118">For details, see [Configure support for allowed external domains in Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).</span></span>
    
      - <span data-ttu-id="b72fe-119">**Enviar renuncia de archivado a socios federados**   Al seleccionar esta opción, el envío de un mensaje de renuncia de archivado a los socios federados le informa de que se registran los detalles de la comunicación.</span><span class="sxs-lookup"><span data-stu-id="b72fe-119">**Send archiving disclaimer to federated partners**   Selecting this option enables the sending of an archiving disclaimer message to federated partners that advises them that communications details are recorded.</span></span> <span data-ttu-id="b72fe-120">Si archiva comunicaciones externas con dominios federados de socios federados, debe habilitar la notificación de renuncia de archivado para avisar a los socios de que su implementación ha archivado sus mensajes y sus detalles de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="b72fe-120">If you archive external communications with federated partner domains, you should enable the archiving disclaimer notification to warn partners that their messages and communications details are being archived by your deployment.</span></span> <span data-ttu-id="b72fe-121">Para obtener más información sobre el archivado, vea [definir los requisitos para el archivado en Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="b72fe-121">For details on archiving, see [Defining your requirements for Archiving in Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md).</span></span>

  - <span data-ttu-id="b72fe-122">**Habilitar el acceso de usuarios remotos**   Habilite esta opción si quiere que los usuarios de su organización que estén fuera del firewall, como teletrabajadores y usuarios que viajan, puedan conectarse a Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b72fe-122">**Enable remote user access**   Enable this option if you want users in your organization who are outside your firewall, such as telecommuters and users who are traveling, to be able to connect to Lync Server.</span></span> <span data-ttu-id="b72fe-123">Para obtener más información, vea [habilitar o deshabilitar el acceso de usuarios remotos en Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="b72fe-123">For details, see [Enable or disable remote user access in Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span></span>

  - <span data-ttu-id="b72fe-124">**Permitir que los usuarios anónimos tengan acceso a conferencias**   Habilite esta opción si desea que los usuarios internos inviten a usuarios anónimos externos a conferencias que organizan.</span><span class="sxs-lookup"><span data-stu-id="b72fe-124">**Enable anonymous users to access conferences**   Enable this option if you want internal users to invite external anonymous users to conferences that they organize.</span></span> <span data-ttu-id="b72fe-125">Habilitar esta opción solo permite usuarios anónimos en conferencias.</span><span class="sxs-lookup"><span data-stu-id="b72fe-125">Enabling this setting only allows anonymous users for conferences.</span></span> <span data-ttu-id="b72fe-126">Para configurar la experiencia de conferencia y las opciones que definen cómo y qué pueden hacer los usuarios con las conferencias y para la inclusión de usuarios anónimos, vea detalles en [crear o modificar la experiencia de usuario de conferencias para un sitio o una](https://technet.microsoft.com/library/gg429715\(v=ocs.15\)) [referencia de configuración de directiva de usuarios y conferencias para Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b72fe-126">To configure the conferencing experience and options that will define how and what your users can do with conferences and for the inclusion of anonymous users, see details at [Create or Modify Conferencing User Experience for a Site or Users](https://technet.microsoft.com/library/gg429715\(v=ocs.15\)) and [Conferencing policy settings reference for Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b72fe-127">Además de habilitar la compatibilidad con el acceso de usuarios externos, también puede configurar directivas para controlar el uso del acceso de usuarios remotos de su organización antes de que los usuarios puedan tener acceso a cualquier tipo de acceso de usuario externo.</span><span class="sxs-lookup"><span data-stu-id="b72fe-127">In addition to enabling external user access support, you also configure policies to control the use of remote user access in your organization before any type of external user access is available to users.</span></span> <span data-ttu-id="b72fe-128">Para obtener más información sobre cómo crear, configurar y aplicar directivas para el acceso de usuarios externos, vea <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">administrar la Directiva de acceso externo en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="b72fe-128">For details about creating, configuring, and applying policies for external user access, see <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">Manage external access policy in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="b72fe-129">**Ver la información de configuración perimetral de acceso mediante cmdlets de Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="b72fe-129">**Viewing Access Edge configuration information by using Windows PowerShell cmdlets**</span></span>

  - <span data-ttu-id="b72fe-130">La información de configuración perimetral de acceso se puede ver con Windows PowerShell y el cmdlet **Get-CsAccessEdgeConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="b72fe-130">Access Edge configuration information can be viewed by using Windows PowerShell and the **Get-CsAccessEdgeConfiguration** cmdlet.</span></span> <span data-ttu-id="b72fe-131">Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b72fe-131">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="b72fe-132">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="b72fe-132">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>
    
    <span data-ttu-id="b72fe-133">Para ver información sobre todas las opciones de configuración de los límites de acceso, escriba el siguiente comando en el shell de administración de Lync Server y, a continuación, presione ENTRAR:</span><span class="sxs-lookup"><span data-stu-id="b72fe-133">To view information about all your Access Edge configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsAccessEdgeConfiguration
    
    <span data-ttu-id="b72fe-134">Devolverá información similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="b72fe-134">That will return information similar to this:</span></span>
    
        Identity                               : Global
        AllowAnonymousUsers                    : False
        AllowFederatedUsers                    : False
        AllowOutsideUsers                      : True
        BeClearingHouse                        : False
        EnablePartnerDiscovery                 : False
        EnableArchivingDisclaimer              : False
        EnableUserReplicator                   : True
        KeepCrlsUpToDateForPeers               : True
        MarkSourceVerifiableOnOutgoingMessages : True
        OutgoingTlsCountForFederatedPartners   : 4
        DiscoveredPartnerStandardRate          : 20
        EnableDiscoveredPartnerContactsLimit   : True
        MaxContactsPerDiscoveredPartner        : 1000
        DiscoveredPartnerReportPeriodMinutes   : 60
        MaxAcceptedCertificatesStored          : 1000
        MaxRejectedCertificatesStored          : 500
        CertificatesDeletedPercentage          : 20
        RoutingMethod                          : UseDnsSrvRouting

<div>

## <a name="in-this-section"></a><span data-ttu-id="b72fe-135">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b72fe-135">In This Section</span></span>

  - [<span data-ttu-id="b72fe-136">Habilitar o deshabilitar la federación y conectividad de mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b72fe-136">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)

  - [<span data-ttu-id="b72fe-137">Habilitar o deshabilitar la detección de socios de federación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b72fe-137">Enable or disable discovery of federation partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md)

  - [<span data-ttu-id="b72fe-138">Habilitar o deshabilitar el envío de una renuncia de archivado a socios federados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b72fe-138">Enable or disable sending an Archiving disclaimer to federated partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md)

  - [<span data-ttu-id="b72fe-139">Habilitar y deshabilitar el acceso de usuarios remotos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b72fe-139">Enable or disable remote user access in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-remote-user-access.md)

  - [<span data-ttu-id="b72fe-140">Habilitar y deshabilitar el acceso anónimo de usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b72fe-140">Enable or disable anonymous user access in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-anonymous-user-access.md)

  - [<span data-ttu-id="b72fe-141">Asignar directivas de conferencia para admitir usuarios anónimos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b72fe-141">Assign conferencing policies to support anonymous users in Lync Server 2013</span></span>](lync-server-2013-assign-conferencing-policies-to-support-anonymous-users.md)

<span data-ttu-id="b72fe-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b72fe-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

