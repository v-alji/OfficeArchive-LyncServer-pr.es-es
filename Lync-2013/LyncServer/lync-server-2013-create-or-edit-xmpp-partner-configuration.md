---
title: 'Lync Server 2013: Crear o editar la configuración de socios de XMPP'
description: 'Lync Server 2013: crear o modificar la configuración del socio XMPP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or edit XMPP partner configuration
ms:assetid: 362dbe5e-8ee9-4aba-8c26-5907312b4a60
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552447(v=OCS.15)
ms:contentKeyID: 48679558
ms.date: 09/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 19289df1920287984f104bb1bdfa214d6f83f5cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431858"
---
# <a name="create-or-edit-xmpp-partner-configuration-in-lync-server-2013"></a><span data-ttu-id="d4bf1-103">Crear o editar la configuración de socios de XMPP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4bf1-103">Create or edit XMPP partner configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d4bf1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d4bf1-104">

<span> </span></span></span>

<span data-ttu-id="d4bf1-105">_**Última modificación del tema:** 2014-09-03_</span><span class="sxs-lookup"><span data-stu-id="d4bf1-105">_**Topic Last Modified:** 2014-09-03_</span></span>

<span data-ttu-id="d4bf1-106">Microsoft Lync Server 2013 integra un proxy de protocolo de presencia y mensajería extensible (XMPP) en el servidor perimetral y una puerta de enlace XMPP en el servidor front-end o en el grupo front-end.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-106">Microsoft Lync Server 2013 integrates an Extensible Messaging and Presence Protocol (XMPP) proxy on the Edge Server and an XMPP Gateway on the Front End Server or Front End pool.</span></span> <span data-ttu-id="d4bf1-107">Para permitir conexiones de otras implementaciones de XMPP, debe configurar el XMPP en el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-107">To allow connections from other XMPP deployments, you must configure XMPP in the Lync Server Control Panel.</span></span> <span data-ttu-id="d4bf1-108">La configuración se establece en un dominio XMPP.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-108">You configure settings on an XMPP domain basis.</span></span> <span data-ttu-id="d4bf1-109">Para crear una nueva asociación de socio, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d4bf1-109">To create a new partner association, you do the following:</span></span>

<div>

## <a name="to-create-a-new-federated-partner-or-edit-an-existing-configuration"></a><span data-ttu-id="d4bf1-110">Para crear un nuevo socio federado o editar una configuración existente</span><span class="sxs-lookup"><span data-stu-id="d4bf1-110">To create a new federated partner or edit an existing configuration</span></span>

1.  <span data-ttu-id="d4bf1-111">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d4bf1-112">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d4bf1-113">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d4bf1-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d4bf1-114">En la barra de navegación izquierda, haga clic en **Federación y acceso externo** y, a continuación, haga clic en los **socios de XMPP federados**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-114">In the left navigation bar, click **Federation and External Access**, and then click **XMPP Federated Partners**.</span></span>

4.  <span data-ttu-id="d4bf1-115">Para crear una configuración nueva, haga clic en **nuevo** .</span><span class="sxs-lookup"><span data-stu-id="d4bf1-115">To create a new configuration, click **New**</span></span>

5.  <span data-ttu-id="d4bf1-116">Para editar una configuración existente, seleccione la configuración y haga clic en **Editar** .</span><span class="sxs-lookup"><span data-stu-id="d4bf1-116">To edit an existing configuration, select the configuration and click **Edit**</span></span>

6.  <span data-ttu-id="d4bf1-117">Para crear o Editar configuraciones para los **socios de XMPP federados**, defina las siguientes opciones de configuración:</span><span class="sxs-lookup"><span data-stu-id="d4bf1-117">To create or edit configurations for **XMPP Federated Partners**, you define the following settings:</span></span>

7.  <span data-ttu-id="d4bf1-118">**Dominio principal** (obligatorio).</span><span class="sxs-lookup"><span data-stu-id="d4bf1-118">**Primary domain** (Required).</span></span> <span data-ttu-id="d4bf1-119">El dominio principal es el dominio base del socio XMPP.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-119">The primary domain is the base domain of the XMPP partner.</span></span> <span data-ttu-id="d4bf1-120">Por ejemplo, tendría que escribir **fabrikam.com** para el nombre de dominio del socio XMPP.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-120">For example, you would enter **fabrikam.com** for the XMPP partner domain name.</span></span> <span data-ttu-id="d4bf1-121">Esta es una entrada obligatoria.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-121">This is a required entry.</span></span>

8.  <span data-ttu-id="d4bf1-122">**Descripción**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-122">**Description**.</span></span> <span data-ttu-id="d4bf1-123">La descripción es para notas u otra información que la identifique para esta configuración en particular.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-123">The description is for notes or other identifying information for this particular configuration.</span></span> <span data-ttu-id="d4bf1-124">Esta entrada es opcional.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-124">This entry is optional.</span></span>

9.  <span data-ttu-id="d4bf1-125">**Dominios adicionales**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-125">**Additional domains**.</span></span> <span data-ttu-id="d4bf1-126">Los dominios adicionales son dominios que forman parte de su dominio del asociado XMPP y que deben incluirse como parte de la comunicación XMPP permitida.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-126">Additional domains are domains that are a part of your XMPP partner’s domain that should be included as part of the allowed XMPP communication.</span></span> <span data-ttu-id="d4bf1-127">Por ejemplo, si el dominio principal es **fabrikam.com**, se mostrarán todos los demás dominios de fabrikam.com con los que se comunicará mediante XMPP.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-127">For example, if the primary domain is **fabrikam.com**, then you would list all other domains that are under fabrikam.com that you will communicate with by way of XMPP.</span></span> <span data-ttu-id="d4bf1-128">Por ejemplo, puede escribir **Corp.fabrikam.com** y **it.fabrikam.com** para el dominio de la empresa XMPP y el dominio XMPP de tecnologías de la información en el dominio XMPP principal de fabrikam.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-128">For example, you might enter **corp.fabrikam.com** and **it.fabrikam.com** for the Corporate XMPP domain and the Information Technologies XMPP domain under fabrikam.com’s main XMPP domain.</span></span>

10. <span data-ttu-id="d4bf1-129">**Tipo de socio**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-129">**Partner type**.</span></span> <span data-ttu-id="d4bf1-130">El **tipo de socio** es un valor obligatorio y le ofrece una selección de tres opciones en un menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-130">The **Partner type** is a required setting and gives you a selection of three choices in a drop-down menu.</span></span> <span data-ttu-id="d4bf1-131">Debe elegir una de las siguientes opciones para describir y exigir qué contactos se pueden agregar.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-131">You must choose one of the following to describe and enforce what contacts can be added.</span></span> <span data-ttu-id="d4bf1-132">Puede seleccionar:</span><span class="sxs-lookup"><span data-stu-id="d4bf1-132">You can select from:</span></span>
    
      - <span data-ttu-id="d4bf1-133">**Federado**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-133">**Federated**.</span></span> <span data-ttu-id="d4bf1-134">Un tipo de socio **federado** es una conexión de confianza entre una implementación de un partner de Lync Server o de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-134">A **Federated** partner type is a trusted connection between a Lync Server or Office Communications Server 2007 R2 partner deployment.</span></span>
    
      - <span data-ttu-id="d4bf1-135">**Verificado público**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-135">**Public verified**.</span></span> <span data-ttu-id="d4bf1-136">Un socio **verificado público** es cuando los contactos que forman parte de una implementación verificada por el proveedor se pueden agregar a la lista de contactos del usuario.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-136">A **Public verified** partner is when contacts that are part of a deployment that are verified by the provider can be added to your user’s list of contacts.</span></span> <span data-ttu-id="d4bf1-137">Las invitaciones pueden enviarse desde el usuario de Lync o el usuario de Lync puede aceptar invitaciones del contacto del socio.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-137">Invites can be sent from the Lync user or the Lync user can accept invites from the partner contact.</span></span>
    
      - <span data-ttu-id="d4bf1-138">No se ha **comprobado el público**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-138">**Public unverified**.</span></span> <span data-ttu-id="d4bf1-139">Una relación **pública no verificada** implica que no hay ningún estado verificado y comprobado entre las dos implementaciones.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-139">A **Public unverified** relationship implies that there is no established and verifiable status between the two deployments.</span></span> <span data-ttu-id="d4bf1-140">Un usuario de Lync debe invitar al contacto no verificado para que sea capaz de agregar el usuario de Lync a su lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-140">A Lync user must invite the unverified contact for that contact to be able to add the Lync user to his contact list.</span></span> <span data-ttu-id="d4bf1-141">Por ejemplo, Google GTalk no es un servicio XMPP de comprobación pública, ya que se relaciona con Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-141">For example, Google GTalk is not a public verified XMPP service as it relates to Lync Server.</span></span> <span data-ttu-id="d4bf1-142">Un usuario de GTalk no podrá agregar el usuario de Lync como contacto, a menos que haya una invitación explícita enviada por el usuario de Lync.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-142">A GTalk user will not be able to add the Lync user as a contact unless there is an explicit invite sent from the Lync user.</span></span>

11. <span data-ttu-id="d4bf1-143">Notas sobre la negociación de secuencias y los métodos de seguridad seguridad de la capa de transporte (TLS) y nivel de seguridad y autenticación de software (SASL):</span><span class="sxs-lookup"><span data-stu-id="d4bf1-143">Notes on stream negotiation and the security methods Transport Layer Security (TLS) and Software Authentication and Security Layer (SASL):</span></span>
    
    <span data-ttu-id="d4bf1-144">Los **estándares XMPP Standard** (xsf) e **Internet Engineering Task Force** (IETF) definen un conjunto de reglas y estándares para usar y administrar certificados de cliente TLS, certificados de servidor TLS y el mecanismo SASL.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-144">The **XMPP Standards Foundation** (XSF) and the **Internet Engineering Task Force** (IETF) define a set of rules and standards for using and managing TLS client certificates, TLS server certificates, and the SASL mechanism.</span></span> <span data-ttu-id="d4bf1-145">El uso de TLS y SASL es el proceso necesario para proteger la secuencia XMPP.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-145">Using TLS and SASL is the required process for securing the XMPP stream.</span></span> <span data-ttu-id="d4bf1-146">En el documento de normas XMPP **XEP-0178**, se especifica un flujo de protocolo recomendado para el uso del mecanismo externo SASL con certificados PKIX, especialmente cuando un servicio XMPP indica que TLS es obligatorio para negociar.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-146">From the XMPP Standards document **XEP-0178**, “specifies a recommended protocol flow for use of the SASL EXTERNAL mechanism with PKIX certificates, especially when an XMPP service indicates that TLS is mandatory-to-negotiate.”</span></span> <span data-ttu-id="d4bf1-147">PKIX, como se indica en la documentación de XSF, hace referencia a la infraestructura de claves públicas, también conocida como PKI.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-147">PKIX, as stated in the XSF documentation, refers to public key infrastructure, also known as PKI.</span></span>
    
    <span data-ttu-id="d4bf1-148">Para obtener más información sobre los requisitos del XMPP, consulte el documento XSF XEP-0178.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-148">Refer to the XSF document XEP-0178 for more details on the XMPP requirements.</span></span> <span data-ttu-id="d4bf1-149">Para obtener más información, consulte "XEP-0178: procedimientos recomendados para usar SASL externo con certificados".</span><span class="sxs-lookup"><span data-stu-id="d4bf1-149">For details, refer to “XEP-0178: Best Practices for Use of SASL EXTERNAL with Certificates”.</span></span> <http://xmpp.org/extensions/xep-0178.html>
    
    <span data-ttu-id="d4bf1-150">Consulte el documento IETF "Protocolo de presencia y mensajería extensible (XMPP): núcleo", sección 5,0, negociación STARTTLS <https://tools.ietf.org/html/rfc6120> .</span><span class="sxs-lookup"><span data-stu-id="d4bf1-150">Refer to the IETF document “Extensible Messaging and Presence Protocol (XMPP): Core“, Section 5.0, STARTTLS Negotiation <https://tools.ietf.org/html/rfc6120>.</span></span>
    
      - <span data-ttu-id="d4bf1-151">**Negociación TLS**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-151">**TLS Negotiation**.</span></span> <span data-ttu-id="d4bf1-152">Define las reglas de negociación de TLS.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-152">Defines the TLS negotiation rules.</span></span> <span data-ttu-id="d4bf1-153">Un servicio XMPP puede requerir TLS, puede hacer que TLS sea opcional o usted define que no se admite la TLS.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-153">An XMPP service can require TLS, can make TLS optional, or you define that TLS is not supported.</span></span> <span data-ttu-id="d4bf1-154">Si elige opcional, el requisito quedará en el servicio XMPP para una decisión obligatoria para la negociación.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-154">Choosing Optional leaves the requirement up to the XMPP service for a mandatory-to-negotiate decision.</span></span> <span data-ttu-id="d4bf1-155">Para ver todas las configuraciones posibles y los detalles de la negociación SASL, TLS y Dialback, incluidas las configuraciones no válidas y de errores conocidos, vea [configuración de la negociación para socios de XMPP federados en Lync Server 2013](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md).</span><span class="sxs-lookup"><span data-stu-id="d4bf1-155">To view all possible settings and details for SASL, TLS and Dialback negotiation –including not valid and known error configurations - see [Negotiation settings for XMPP federated partners in Lync Server 2013](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md).</span></span>
        
          - <span></span>  
            <span data-ttu-id="d4bf1-156">**Requerido**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-156">**Required**.</span></span> <span data-ttu-id="d4bf1-157">El servicio XMPP requiere negociación TLS.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-157">The XMPP service requires TLS negotiation.</span></span>
        
          - <span></span>  
            <span data-ttu-id="d4bf1-158">**Opcional**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-158">**Optional**.</span></span> <span data-ttu-id="d4bf1-159">El servicio XMPP indica que TLS es obligatorio para negociar.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-159">The XMPP service indicates that TLS is mandatory-to-negotiate.</span></span>
        
          - <span></span>  
            <span data-ttu-id="d4bf1-160">**No es compatible**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-160">**Not Supported**.</span></span> <span data-ttu-id="d4bf1-161">El servicio XMPP no admite TLS.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-161">The XMPP service does not support TLS.</span></span>
    
      - <span data-ttu-id="d4bf1-162">**Negociación de SASL**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-162">**SASL negotiation**.</span></span> <span data-ttu-id="d4bf1-163">Define las reglas de negociación de SASL.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-163">Defines the SASL negotiation rules.</span></span> <span data-ttu-id="d4bf1-164">Un servicio XMPP puede requerir SASL, puede hacer que SASL sea opcional o usted define que SASL no es compatible.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-164">An XMPP service can require SASL, can make SASL optional, or you define that SASL is not supported.</span></span> <span data-ttu-id="d4bf1-165">Si elige opcional, el servicio XMPP del socio dejará de ser necesario para una decisión obligatoria para la negociación.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-165">Choosing Optional leaves the requirement up to the partner XMPP service for a mandatory-to-negotiate decision.</span></span>
        
        <div>
        

        > [!WARNING]  
        > <span data-ttu-id="d4bf1-166">SASL requiere TLS.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-166">SASL requires TLS.</span></span> <span data-ttu-id="d4bf1-167">Para usar SASL, TLS debe ser obligatorio u opcional.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-167">To use SASL, TLS must either be required or optional.</span></span> <span data-ttu-id="d4bf1-168">Cualquier configuración que defina SASL como requerido u opcional debe tener compatibilidad con TLS.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-168">Any configuration that defines SASL as either required or optional must have TLS support.</span></span> <span data-ttu-id="d4bf1-169">Al hacer clic en <STRONG>confirmar</STRONG> para guardar los cambios, si no ha establecido TLS en obligatorio u opcional, se le advertirá de que SASL debe tener compatibilidad con TLS y los cambios no se guardarán.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-169">When clicking <STRONG>Commit</STRONG> to save your changes, if you have not set TLS to required or optional, you will be warned that SASL must have TLS support and your changes are not saved.</span></span> <span data-ttu-id="d4bf1-170">Para resolver el error, establezca TLS en <STRONG>required</STRONG> u <STRONG>Optional</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-170">To resolve the error, set TLS to <STRONG>Required</STRONG> or <STRONG>Optional</STRONG>.</span></span> <span data-ttu-id="d4bf1-171">Si el uso de SASL es opcional y la compatibilidad con la negociación TLS no es posible, debe establecer la negociación de SASL en <STRONG>no compatible</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-171">If use of SASL is optional and TLS negotiation support is not possible, you must set SASL negotiation to <STRONG>Not Supported</STRONG>.</span></span> <span data-ttu-id="d4bf1-172">Confirmar con el servicio XMPP qué deben tener las secuencias de negociación apropiadas para TLS y SASL, o se producirá una interrupción del servicio.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-172">Confirm with the XMPP service what the proper negotiation streams must be for TLS and SASL or service interruption will occur.</span></span>

        
        </div>
        
          - <span></span>  
            <span data-ttu-id="d4bf1-173">**Requerido**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-173">**Required**.</span></span> <span data-ttu-id="d4bf1-174">El servicio XMPP requiere negociación SASL.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-174">The XMPP service requires SASL negotiation.</span></span>
        
          - <span></span>  
            <span data-ttu-id="d4bf1-175">**Opcional**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-175">**Optional**.</span></span> <span data-ttu-id="d4bf1-176">El servicio XMPP indica que SASL es obligatorio para negociar.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-176">The XMPP service indicates that SASL is mandatory-to-negotiate.</span></span>
        
          - <span></span>  
            <span data-ttu-id="d4bf1-177">**No es compatible**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-177">**Not Supported**.</span></span> <span data-ttu-id="d4bf1-178">El servicio XMPP no admite SASL.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-178">The XMPP service does not support SASL.</span></span>
    
      - <span data-ttu-id="d4bf1-179">**Negociación de Dialback**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-179">**Dialback negotiation**.</span></span> <span data-ttu-id="d4bf1-180">El XSF en el documento **XEP-220: Server Dialback** define la negociación de Dialback <http://xmpp.org/extensions/xep-0220.html> .</span><span class="sxs-lookup"><span data-stu-id="d4bf1-180">Dialback negotiation is defined by the XSF in document **XEP-220 : Server Dialback** <http://xmpp.org/extensions/xep-0220.html>.</span></span> <span data-ttu-id="d4bf1-181">El proceso de Dialback del servidor usa el sistema de nombres de dominio (DNS) y un servidor autorizado para verificar que la solicitud procede de un socio XMPP válido.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-181">The server dialback process uses the domain name system (DNS) and an authoritative server to verify that the request came from a valid XMPP partner.</span></span> <span data-ttu-id="d4bf1-182">Para ello, el servidor de origen crea un mensaje de un tipo específico con una clave de Dialback generada y busca el servidor de recepción en DNS.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-182">To do this, the originating server creates a message of a specific type with a generated dialback key and looks up the receiving server in DNS.</span></span> <span data-ttu-id="d4bf1-183">El servidor de origen envía la clave en una secuencia XML a la búsqueda DNS resultante, supuestamente el servidor de recepción.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-183">The originating server sends the key in an XML stream to the resulting DNS lookup, presumably the receiving server.</span></span> <span data-ttu-id="d4bf1-184">Al recibir la clave sobre la secuencia XML, el servidor de recepción no responde al servidor de origen, pero envía la clave a un servidor conocido de autorización.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-184">On receipt of the key over the XML stream, the receiving server does not respond to the originating server, but sends the key to a known authoritative server.</span></span> <span data-ttu-id="d4bf1-185">El servidor autorizado verifica que la clave sea válida o no válida.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-185">The authoritative server verifies that the key is either valid or not valid.</span></span> <span data-ttu-id="d4bf1-186">Si no es válido, el servidor de recepción no responde al servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-186">If not valid, the receiving server does not respond to the originating server.</span></span> <span data-ttu-id="d4bf1-187">Si la clave es válida, el servidor receptor informa al servidor de origen de que la identidad y la clave son válidas y que la conversación puede comenzar.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-187">If the key is valid, the receiving server informs the originating server that the identity and key is valid and the conversation can commence.</span></span>
        
        <span data-ttu-id="d4bf1-188">Existen dos Estados válidos para la **negociación de Dialback**:</span><span class="sxs-lookup"><span data-stu-id="d4bf1-188">There are two valid states for **Dialback negotiation**:</span></span>
        
          - <span></span>  
            <span data-ttu-id="d4bf1-189">**Verdadero**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-189">**True**.</span></span> <span data-ttu-id="d4bf1-190">El servidor XMPP está configurado para usar la negociación de Dialback si se debe recibir una solicitud de un servidor de origen</span><span class="sxs-lookup"><span data-stu-id="d4bf1-190">The XMPP server is configured to use Dialback negotiation if a request should be received from an originating server</span></span>
        
          - <span></span>  
            <span data-ttu-id="d4bf1-191">**Falso**.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-191">**False**.</span></span> <span data-ttu-id="d4bf1-192">El servidor XMPP no está configurado para usar la negociación de Dialback y si se debe recibir una solicitud de un servidor de origen, se pasará por alto.</span><span class="sxs-lookup"><span data-stu-id="d4bf1-192">The XMPP server is not configured to use Dialback negotiation and if a request should be received from an originating server, it will be ignored</span></span>

<span data-ttu-id="d4bf1-193"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d4bf1-193"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

