---
title: 'Lync Server 2013: Activar la conectividad entre Lync y Skype'
description: 'Lync Server 2013: habilitar la conectividad de Lync-Skype.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Lync-Skype connectivity
ms:assetid: 34c4db3e-582f-41fb-85c4-3438ae02f09f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440170(v=OCS.15)
ms:contentKeyID: 57793361
ms.date: 12/16/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f31856299b05af7d6b8e934d6e9784d1571b7e29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428812"
---
# <a name="enabling-lync-skype-connectivity-in-lync-server-2013"></a><span data-ttu-id="02325-103">Activar la conectividad entre Lync y Skype en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="02325-103">Enabling Lync-Skype connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="02325-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="02325-104">

<span> </span></span></span>

<span data-ttu-id="02325-105">_**Última modificación del tema:** 2014-12-16_</span><span class="sxs-lookup"><span data-stu-id="02325-105">_**Topic Last Modified:** 2014-12-16_</span></span>

<span data-ttu-id="02325-106">Después de enviar la solicitud de aprovisionamiento, puede centrarse en el entorno de Lync Server y en las tareas administrativas necesarias para configurar la conectividad de Lync-Skype.</span><span class="sxs-lookup"><span data-stu-id="02325-106">After you have submitted the provisioning request, you can focus on the Lync Server environment and administrative tasks required to configure Lync-Skype connectivity.</span></span> <span data-ttu-id="02325-107">En esta sección, damos por hecho que el administrador de Lync Server ha implementado Lync Server y ha configurado el acceso externo.</span><span class="sxs-lookup"><span data-stu-id="02325-107">In this section, we assume that the Lync Server administrator has deployed Lync Server and configured external access.</span></span> <span data-ttu-id="02325-108">Para obtener más información sobre cómo configurar el acceso externo para Lync Server, consulte [planear el acceso de usuarios externos en Lync server 2013](lync-server-2013-planning-for-external-user-access.md) e [implementar el acceso de usuarios externos en Lync Server 2013](lync-server-2013-deploying-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="02325-108">For additional information on configuring external access for Lync Server, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md).</span></span>

<span data-ttu-id="02325-109">Para preparar el entorno de Lync Server para la conectividad de Lync-Skype, el administrador de Lync Server debe completar las tres tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="02325-109">To prepare the Lync Server environment for Lync-Skype connectivity, the Lync Server administrator must complete the following three tasks:</span></span>

<div>

## <a name="1-configure-federation-and-pic"></a><span data-ttu-id="02325-110">1 \.</span><span class="sxs-lookup"><span data-stu-id="02325-110">1\.</span></span> <span data-ttu-id="02325-111">Configurar la federación y la PIC</span><span class="sxs-lookup"><span data-stu-id="02325-111">Configure Federation and PIC</span></span>

<span data-ttu-id="02325-112">La Federación es necesaria para que los usuarios de Skype puedan comunicarse con los usuarios de Lync de su organización.</span><span class="sxs-lookup"><span data-stu-id="02325-112">Federation is required to enable Skype users to communicate with Lync users in your organization.</span></span> <span data-ttu-id="02325-113">La conectividad de mensajería instantánea pública (PIC) es una clase de Federación y debe estar configurada para permitir que los usuarios de Lync se comuniquen con usuarios de Skype.</span><span class="sxs-lookup"><span data-stu-id="02325-113">Public Instant Messaging Connectivity (PIC) is a class of federation, and it must be configured to enable your Lync users to communicate with Skype users.</span></span> <span data-ttu-id="02325-114">La Federación y el PIC se configuran mediante el panel de control de Lync Server, que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="02325-114">Federation and PIC are configured by using the Lync Server Control Panel, shown below.</span></span>

<span data-ttu-id="02325-115">![Mostrando PIC](images/Dn440170.451b94e3-0b38-488c-835f-1f25690e8074(OCS.15).jpg "Mostrando PIC")</span><span class="sxs-lookup"><span data-stu-id="02325-115">![Showing PIC](images/Dn440170.451b94e3-0b38-488c-835f-1f25690e8074(OCS.15).jpg "Showing PIC")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="02325-116">La federación de PIC ya no es compatible con Live Communication Server 2005 SP1 ni con Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="02325-116">PIC federation is no longer supported by Live Communication Server 2005 SP1 or by Office Communications Server 2007.</span></span> <span data-ttu-id="02325-117">Las plataformas compatibles con la Federación de PIC incluyen Lync Server 2013, Lync Server 2010 y Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="02325-117">The supported platforms for PIC federation include Lync Server 2013, Lync Server 2010, and Office Communications Server 2007 R2.</span></span>



</div>

</div>

<div>

## <a name="2-configure-at-least-one-policy-to-support-federated-user-access"></a><span data-ttu-id="02325-118">2 \.</span><span class="sxs-lookup"><span data-stu-id="02325-118">2\.</span></span> <span data-ttu-id="02325-119">Configurar al menos una directiva para permitir el acceso de usuarios federados</span><span class="sxs-lookup"><span data-stu-id="02325-119">Configure at least one policy to support federated user access</span></span>

<span data-ttu-id="02325-120">Con el panel de control de Lync Server, un administrador debe configurar una o más directivas de acceso de usuarios externos para controlar si los usuarios de Skype pueden colaborar con usuarios internos de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="02325-120">Using the Lync Server Control Panel, an administrator must configure one or more external user access policies to control whether Skype users can collaborate with internal Lync Server users.</span></span>

<span data-ttu-id="02325-121">![Directivas](images/Dn440170.8fd46ad1-9749-422c-8c47-c16ac9032cdb(OCS.15).jpg "Directivas")</span><span class="sxs-lookup"><span data-stu-id="02325-121">![Policies](images/Dn440170.8fd46ad1-9749-422c-8c47-c16ac9032cdb(OCS.15).jpg "Policies")</span></span>

</div>

<div>

## <a name="3-configure-the-skype-pic-provider-setting-for-lync"></a><span data-ttu-id="02325-122">3 \.</span><span class="sxs-lookup"><span data-stu-id="02325-122">3\.</span></span> <span data-ttu-id="02325-123">Configurar la configuración del proveedor PIC de Skype para Lync</span><span class="sxs-lookup"><span data-stu-id="02325-123">Configure the Skype PIC provider setting for Lync</span></span>

<span data-ttu-id="02325-124">Con el shell de administración de Lync Server, un administrador debe configurar la Directiva de cliente de Lync para mostrar Skype como proveedor de PIC adicional.</span><span class="sxs-lookup"><span data-stu-id="02325-124">Using the Lync Server Management Shell, an administrator must configure the Lync client policy to display Skype as an additional PIC provider.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="02325-125">Los usuarios de los proveedores de servicios de conectividad de mensajería instantánea pública (PIC) no pueden participar en mensajería instantánea o en conferencias de audio o vídeo de su organización hasta que también configure al menos una directiva (paso 2, anteriormente en este procedimiento) para admitir la conectividad de mensajería instantánea pública.</span><span class="sxs-lookup"><span data-stu-id="02325-125">Users of the Public Instant Messaging Connectivity (PIC) service providers can’t participate in IM or audio or video conferences in your organization until you also configure at least one policy (step 2, earlier in this procedure) to support public IM connectivity.</span></span>



</div>

1.  <span data-ttu-id="02325-126">Para configurar la Federación y el PIC, consulte "habilitar o deshabilitar la Federación y la conectividad de mensajería instantánea pública" en [https://go.microsoft.com/fwlink/p/?LinkId=306063](https://go.microsoft.com/fwlink/p/?linkid=306063) .</span><span class="sxs-lookup"><span data-stu-id="02325-126">To configure federation and PIC, see "Enable or Disable Federation and Public IM Connectivity" at [https://go.microsoft.com/fwlink/p/?LinkId=306063](https://go.microsoft.com/fwlink/p/?linkid=306063).</span></span>

2.  <span data-ttu-id="02325-127">Para configurar al menos una directiva para admitir el acceso de usuarios federados, consulte "configurar directivas para controlar el acceso de usuarios públicos" en [https://go.microsoft.com/fwlink/p/?LinkId=306064](https://go.microsoft.com/fwlink/p/?linkid=306064) .</span><span class="sxs-lookup"><span data-stu-id="02325-127">To configure at least one policy to support federated user access, see "Configure Policies to Control Public User Access" at [https://go.microsoft.com/fwlink/p/?LinkId=306064](https://go.microsoft.com/fwlink/p/?linkid=306064).</span></span>

<span data-ttu-id="02325-128">**Para editar un Messenger existente o un proveedor de PIC de Skype y configurarlo para Skype**</span><span class="sxs-lookup"><span data-stu-id="02325-128">**To edit an existing Messenger or Skype PIC provider and configure it for Skype**</span></span>

1.  <span data-ttu-id="02325-129">Desde un servidor front-end de Lync Server, abra el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="02325-129">From a Lync Server Front End Server, open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="02325-130">Ejecute estos dos comandos:</span><span class="sxs-lookup"><span data-stu-id="02325-130">Run the following two commands:</span></span>
    
    `Remove-CsPublicProvider -Identity <identity-name>`
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="02325-131">Si todavía no tiene un proveedor PIC en su entorno y está creando un nuevo proveedor PIC, no necesita ejecutar el cmdlet <STRONG>Remove-CsPublicProvider</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="02325-131">If you do not already have a PIC provider in your environment and are creating a new PIC provider then you do not need to run the <STRONG>Remove-CsPublicProvider</STRONG> cmdlet.</span></span>

    
    </div>
    
    `New-CsPublicProvider -ProxyFqdn federation.messenger.msn.com -Enabled 1 -Identity Skype  -VerificationLevel 2 -NameDecorationRoutingDomain msn.com -NameDecorationExcludedDomainList "msn.com,outlook.com,live.com,hotmail.com" -IconUrl "https://images.edge.messenger.live.com/Messenger_16x16.png"`
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="02325-132">Agregado en el cliente de escritorio de Lync Server 2013 CU5 &amp; en el SP1 de Office 2013, la NameDecorationRoutingDomain y NameDecorationExcludedDomainList mejoran la situación en la que los usuarios de Lync agregan contactos de Skype necesitan "decorar" Dominios que no son de Microsoft para identificarlos y enrutarlos a Skype (el formato de: usuario (contoso. com) @msn. com).</span><span class="sxs-lookup"><span data-stu-id="02325-132">Added in Lync Server 2013 CU5 &amp; Lync desktop client in Office 2013 SP1, the NameDecorationRoutingDomain and NameDecorationExcludedDomainList improve the situation where Lync users adding Skype contacts needed to “decorate” non-Microsoft domains to identify and route them to Skype (the format of: user(contoso.com)@msn.com).</span></span> <span data-ttu-id="02325-133">Esta nueva configuración permitirá la conversión automática del formato de la dirección que los usuarios introduzcan en el cuadro de diálogo “Agregar contacto de Skype” con NameDecorationRoutingDomain (que se necesita establecer en msn.com) si no contiene los dominios en NameDecorationExcludedDomainList (actualmente, se admite msn.com, live.com, Hotmail.com y outlook.com).</span><span class="sxs-lookup"><span data-stu-id="02325-133">These new settings will allow automatic formatting of the address user’s enter in the “Add Skype contact” dialog box with the NameDecorationRoutingDomain (which should be set to msn.com) if it does not contain the domains in the NameDecorationExcludedDomainList (we currently can support msn.com, live.com, Hotmail.com, outlook.com).</span></span>

    
    </div>

3.  <span data-ttu-id="02325-134">Desde un cliente de Lync, ahora puede seleccionar Skype como proveedor PIC y agregar un cliente de Skype especificando su cuenta Microsoft.</span><span class="sxs-lookup"><span data-stu-id="02325-134">From a Lync client, you can now select Skype as the PIC provider, and add a Skype client by specifying their Microsoft account.</span></span> <span data-ttu-id="02325-135">Además, un usuario de Skype que ha fusionado y ha iniciado sesión con su cuenta de Microsoft puede enviar una solicitud de contacto a los usuarios de Lync.</span><span class="sxs-lookup"><span data-stu-id="02325-135">In addition, a Skype user who has merged and logged in with their Microsoft account can send contact request to Lync users.</span></span> <span data-ttu-id="02325-136">Para obtener más información sobre las cuentas de Microsoft, vea [¿Qué es una cuenta de Microsoft?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span><span class="sxs-lookup"><span data-stu-id="02325-136">For more information about Microsoft accounts, see [What is a Microsoft account?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span></span> <span data-ttu-id="02325-137">Para obtener más información sobre cómo agregar clientes a Lync, consulte [usar Lync-Skype conectividad en Lync Server 2013 como usuario final](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span><span class="sxs-lookup"><span data-stu-id="02325-137">For additional information on adding clients to Lync, see [Using Lync-Skype connectivity in Lync Server 2013 as an end user](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span></span>
    
    <span data-ttu-id="02325-138">![Añadir contacto de Skype](images/Dn440170.df0e6ed9-2374-4dfa-a815-87281989487c(OCS.15).jpg "Añadir contacto de Skype")</span><span class="sxs-lookup"><span data-stu-id="02325-138">![Add Skype Contact](images/Dn440170.df0e6ed9-2374-4dfa-a815-87281989487c(OCS.15).jpg "Add Skype Contact")</span></span>

4.  <span data-ttu-id="02325-139">Para obtener información detallada sobre cómo modificar proveedores hospedados, vea "crear o editar proveedores federados de SIP alojados" en [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065) .</span><span class="sxs-lookup"><span data-stu-id="02325-139">For detailed information on modifying hosted providers, see "Create or Edit Hosted SIP Federated Providers" at [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065).</span></span>

<span data-ttu-id="02325-140">Estas son todas las tareas administrativas que se necesitan llevar a cabo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="02325-140">This completes the administrative tasks that must be performed on the server.</span></span> <span data-ttu-id="02325-141">Ya está configurada para Lync-Skype conectividad.</span><span class="sxs-lookup"><span data-stu-id="02325-141">You are now set up for Lync-Skype connectivity.</span></span>

<span data-ttu-id="02325-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="02325-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

