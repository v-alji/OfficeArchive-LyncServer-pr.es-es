---
title: 'Lync Server 2013: crear parámetros de configuración de registradores'
description: 'Lync Server 2013: crear parámetros de configuración de registro.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create Registrar configuration settings
ms:assetid: eddfbdd2-cfd0-4c03-986e-443d6728db7d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182601(v=OCS.15)
ms:contentKeyID: 48185758
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ada10302b3c2319e0f713ce2d3bea00b6fed126
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431606"
---
# <a name="create-registrar-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="adca5-103">Crear opciones de configuración de registradores en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="adca5-103">Create Registrar configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="adca5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="adca5-104">

<span> </span></span></span>

<span data-ttu-id="adca5-105">_**Última modificación del tema:** 2013-03-17_</span><span class="sxs-lookup"><span data-stu-id="adca5-105">_**Topic Last Modified:** 2013-03-17_</span></span>

<span data-ttu-id="adca5-p101">Puede usar el registrador para configurar los métodos de autenticación de servidores proxy. El protocolo de autenticación que especifique definirá el tipo de desafío que presentarán los servidores del grupo a los clientes. Los protocolos disponibles son:</span><span class="sxs-lookup"><span data-stu-id="adca5-p101">You can use the Registrar to configure proxy server authentication methods. The authentication protocol you specify determines which type of challenges the servers in the pool issue to clients. The available protocols are:</span></span>

  - <span data-ttu-id="adca5-109">**Kerberos**   Este es el esquema de autenticación basado en contraseñas más seguro disponible para los clientes, pero normalmente solo está disponible para clientes de empresa, ya que requiere conexión de cliente a un centro de distribución de claves (controlador de dominio de Kerberos).</span><span class="sxs-lookup"><span data-stu-id="adca5-109">**Kerberos**   This is the strongest password-based authentication scheme available to clients, but it is normally available only to enterprise clients because it requires client connection to a Key Distribution Center (Kerberos domain controller).</span></span> <span data-ttu-id="adca5-110">Esta configuración es adecuada si el servidor autentica solo clientes de empresa.</span><span class="sxs-lookup"><span data-stu-id="adca5-110">This setting is appropriate if the server authenticates only enterprise clients.</span></span>

  - <span data-ttu-id="adca5-111">**NTLM**   Esta es la autenticación basada en contraseña disponible para los clientes que usan un esquema de hash de desafío/respuesta en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="adca5-111">**NTLM**   This is the password-based authentication available to clients that use a challenge-response hashing scheme on the password.</span></span> <span data-ttu-id="adca5-112">Esta es la única forma de autenticación disponible para los clientes sin conexión a un centro de distribución de claves (controlador de dominio de Kerberos), como los usuarios remotos.</span><span class="sxs-lookup"><span data-stu-id="adca5-112">This is the only form of authentication available to clients without connectivity to a Key Distribution Center (Kerberos domain controller), such as remote users.</span></span> <span data-ttu-id="adca5-113">Si un servidor autentica solo usuarios remotos, debe elegir NTLM.</span><span class="sxs-lookup"><span data-stu-id="adca5-113">If a server authenticates only remote users, you should choose NTLM.</span></span>

  - <span data-ttu-id="adca5-114">**Autenticación de certificados**   Este es el método de autenticación nuevo cuando el servidor necesita obtener certificados de clientes de Lync Phone Edition, teléfonos de área común, Lync 2013 y la aplicación de la tienda Windows de Lync.</span><span class="sxs-lookup"><span data-stu-id="adca5-114">**Certificate authentication**   This is the new authentication method when the server needs to obtain certificates from Lync Phone Edition clients, common area phones, Lync 2013 and the Lync Windows Store app.</span></span> <span data-ttu-id="adca5-115">En los clientes de Lync Phone Edition, después de que un usuario inicie sesión y se autentique correctamente proporcionando un número de identificación personal (PIN), Lync Server 2013 entonces le da el URI del SIP al teléfono y aprovisiona un certificado firmado de Lync Server o un certificado de usuario que identifica Joe (por ejemplo: SN=joe@contoso.com) en el teléfono.</span><span class="sxs-lookup"><span data-stu-id="adca5-115">On Lync Phone Edition clients, after a user signs in and is successfully authenticated by providing a personal identification number (PIN), Lync Server 2013 then provisions the SIP URI to the phone and provisions a Lync Server signed certificate or a user certificate that identifies Joe (Ex: SN=joe@contoso.com ) to the phone.</span></span> <span data-ttu-id="adca5-116">Este certificado se usa para autenticarse con el Registrador y los Servicios web.</span><span class="sxs-lookup"><span data-stu-id="adca5-116">This certificate is used for authenticating with the Registrar and Web Services.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="adca5-p105">Se recomienda habilitar Kerberos y NTLM cuando un servidor admita la autenticación para los clientes remotos y de empresa. El servidor perimetral y los servidores internos se comunican para garantizar que solamente se ofrezca la autenticación NTLM a clientes remotos. Si solamente se habilita Kerberos en estos servidores, no podrán autenticar usuarios remotos. Si los usuarios de empresa también se autentican frente al servidor, se usa Kerberos.</span><span class="sxs-lookup"><span data-stu-id="adca5-p105">We recommend that you enable both Kerberos and NTLM when a server supports authentication for both remote and enterprise clients. The Edge Server and internal servers communicate to ensure that only NTLM authentication is offered to remote clients. If only Kerberos is enabled on these servers, they cannot authenticate remote users. If enterprise users also authenticate against the server, Kerberos is used.</span></span><BR><span data-ttu-id="adca5-121">Si va a usar los clientes de la aplicación de la tienda Windows de Lync, debe habilitar la autenticación de certificados.</span><span class="sxs-lookup"><span data-stu-id="adca5-121">If you will use Lync Windows Store app clients, you must enable certificate authentication.</span></span>



</div>

<span data-ttu-id="adca5-122">Siga estos pasos para crear un registrador nuevo.</span><span class="sxs-lookup"><span data-stu-id="adca5-122">Follow these steps to create a new Registrar.</span></span>

<div>

## <a name="to-create-new-registrar-configuration-settings"></a><span data-ttu-id="adca5-123">Para crear nuevas opciones de configuración de registrador</span><span class="sxs-lookup"><span data-stu-id="adca5-123">To create new Registrar configuration settings</span></span>

1.  <span data-ttu-id="adca5-124">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o asignada al rol CsServerAdministrator o CsAdministrator, inicie sesión en cualquier equipo de la red en el que haya implementado Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="adca5-124">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="adca5-125">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="adca5-125">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="adca5-126">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="adca5-126">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="adca5-127">En la barra de navegación izquierda, haga clic en **Seguridad** y, a continuación, en **Registrador**.</span><span class="sxs-lookup"><span data-stu-id="adca5-127">In the left navigation bar, click **Security** and then click **Registrar**.</span></span>

4.  <span data-ttu-id="adca5-128">En la página **Registrador**, haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="adca5-128">On the **Registrar** page, click **New**</span></span>

5.  <span data-ttu-id="adca5-129">En **Seleccionar un servicio**, haga clic en el servicio al que se aplicará el Registrador y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="adca5-129">In **Select a Service**, click the service to which the Registrar is to be applied and then click **OK**.</span></span>

6.  <span data-ttu-id="adca5-130">En **Nueva configuración de registrador**, seleccione uno o más de los siguientes elementos en función de las funciones de los clientes y la compatibilidad de su entorno:</span><span class="sxs-lookup"><span data-stu-id="adca5-130">In **New Registrar Setting**, select one or more of the following depending on the capabilities of the clients and support in your environment:</span></span>
    
      - <span data-ttu-id="adca5-131">**Habilitar autenticación Kerberos** para que los servidores del grupo emitan desafíos mediante la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="adca5-131">**Enable Kerberos authentication** to have the servers in the pool issue challenges using Kerberos authentication.</span></span>
    
      - <span data-ttu-id="adca5-132">**Habilitar autenticación NTLM** para que los servidores del grupo emitan desafíos mediante la autenticación NTLM.</span><span class="sxs-lookup"><span data-stu-id="adca5-132">**Enable NTLM authentication** to have the servers in the pool issue challenges using NTLM.</span></span>
    
      - <span data-ttu-id="adca5-133">**Habilitar autenticación de certificados** para que los servidores del grupo emitan desafíos mediante la autenticación de certificados.</span><span class="sxs-lookup"><span data-stu-id="adca5-133">**Enable certificate authentication** to have the servers in the pool issue certificates to clients.</span></span>

7.  <span data-ttu-id="adca5-134">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="adca5-134">Click **Commit**.</span></span>

<span data-ttu-id="adca5-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="adca5-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

