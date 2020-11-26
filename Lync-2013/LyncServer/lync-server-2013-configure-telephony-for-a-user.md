---
title: 'Lync Server 2013: configurar telefonía para un usuario'
description: 'Lync Server 2013: configurar telefonía para un usuario.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure telephony for a user
ms:assetid: 4546432e-c839-4517-a2c5-bc0d4d8c6a03
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520988(v=OCS.15)
ms:contentKeyID: 48183987
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b82cecb67ea11928d187bd2a4a00625fbca7b23e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433657"
---
# <a name="configure-telephony-for-a-user-in-lync-server-2013"></a><span data-ttu-id="a1fba-103">Configurar la telefonía de un usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a1fba-103">Configure telephony for a user in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a1fba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a1fba-104">

<span> </span></span></span>

<span data-ttu-id="a1fba-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a1fba-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a1fba-106">La configuración de telefonía es una parte de la configuración individual de una cuenta de usuario que se puede configurar en el panel de control de Lync Server para el usuario (es decir, si el usuario individual se ha habilitado para Lync Server 2013 y la organización admite telefonía).</span><span class="sxs-lookup"><span data-stu-id="a1fba-106">Telephony settings are some of the individual settings of a user account that can be configured in Lync Server Control Panel for the user (that is, if the individual user has been enabled for Lync Server 2013 and the organization supports telephony).</span></span>

<span data-ttu-id="a1fba-107">Entre las opciones de telefonía de usuario de Lync Server se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="a1fba-107">Lync Server user telephony options include the following:</span></span>

  - <span data-ttu-id="a1fba-108">**Audio/vídeo deshabilitado**   El usuario no puede hacer llamadas con audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1fba-108">**Audio/video disabled**   The user cannot make calls with audio and video.</span></span>

  - <span data-ttu-id="a1fba-109">**Solo de PC a PC**   El usuario solo puede hacer videollamadas o videollamadas de PC a PC.</span><span class="sxs-lookup"><span data-stu-id="a1fba-109">**PC-to-PC only**   The user can make only PC-to-PC audio or video calls.</span></span>

  - <span data-ttu-id="a1fba-110">**Telefonía IP empresarial**   El usuario puede usar la infraestructura de Lync Server 2013 para enrutar todas las llamadas entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="a1fba-110">**Enterprise Voice**   The user can use the Lync Server 2013 infrastructure to route all incoming and outgoing calls.</span></span> <span data-ttu-id="a1fba-111">El usuario también puede hacer llamadas de PC a PC.</span><span class="sxs-lookup"><span data-stu-id="a1fba-111">The user can also make PC-to-PC calls.</span></span>

  - <span data-ttu-id="a1fba-112">**Control remoto de llamadas**   El usuario puede usar Lync Server 2013 para controlar el teléfono de escritorio y también puede hacer llamadas entre equipos.</span><span class="sxs-lookup"><span data-stu-id="a1fba-112">**Remote call control**   The user can use Lync Server 2013 to control the desktop phone, and can also make PC-to-PC calls.</span></span>

<span data-ttu-id="a1fba-113">Para obtener detalles sobre la configuración de telefonía para una organización, vea [configurar la telefonía de un usuario en Lync server 2013](lync-server-2013-configure-telephony-for-a-user.md) e implementar la telefonía [IP empresarial en Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="a1fba-113">For details about configuring telephony for an organization, see [Configure telephony for a user in Lync Server 2013](lync-server-2013-configure-telephony-for-a-user.md) and [Deploying Enterprise Voice in Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) in the Deployment documentation.</span></span>

<div>

## <a name="to-configure-telephony-for-a-specific-user-account"></a><span data-ttu-id="a1fba-114">Para configurar telefonía para una cuenta de usuario específica</span><span class="sxs-lookup"><span data-stu-id="a1fba-114">To configure telephony for a specific user account</span></span>

1.  <span data-ttu-id="a1fba-115">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="a1fba-115">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a1fba-116">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a1fba-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a1fba-117">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a1fba-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a1fba-118">En la barra de navegación izquierda, haga clic en **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="a1fba-118">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="a1fba-119">En el cuadro **Buscar usuarios** , escriba todas o la primera parte del nombre para mostrar, el nombre, el apellido, el nombre de cuenta del administrador de cuentas de seguridad (SAM), la dirección SIP o el identificador uniforme de recursos (URI) de la cuenta de usuario que desee y, a continuación, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="a1fba-119">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want, and then click **Find**.</span></span>

5.  <span data-ttu-id="a1fba-120">En la tabla, haga clic en la cuenta de usuario que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="a1fba-120">In the table, click the user account that you want to modify.</span></span>

6.  <span data-ttu-id="a1fba-121">En el menú **Editar** , haga clic en **modificar**.</span><span class="sxs-lookup"><span data-stu-id="a1fba-121">On the **Edit** menu, click **Modify**.</span></span>

7.  <span data-ttu-id="a1fba-122">En **telefonía**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a1fba-122">In **Telephony**, do the following:</span></span>
    
      - <span data-ttu-id="a1fba-123">Para deshabilitar las llamadas de audio y vídeo para el usuario, haga clic en **audio/vídeo deshabilitado**.</span><span class="sxs-lookup"><span data-stu-id="a1fba-123">To disable audio and video calls for the user, click **Audio/video disabled**.</span></span>
    
      - <span data-ttu-id="a1fba-124">Para habilitar las comunicaciones de audio de PC a PC para el usuario, pero no para el control remoto de llamadas ni para la telefonía IP empresarial, haga clic en **solo de PC a PC**.</span><span class="sxs-lookup"><span data-stu-id="a1fba-124">To enable PC-to-PC audio communications for the user, but not remote call control or Enterprise Voice, click **PC-to-PC only**.</span></span> <span data-ttu-id="a1fba-125">Especifique un valor para el **URI de línea** del teléfono que usa el usuario para las comunicaciones de audio de PC a PC.</span><span class="sxs-lookup"><span data-stu-id="a1fba-125">Specify a value for **Line URI** for the telephone that the user uses for PC-to-PC audio communications.</span></span>
    
      - <span data-ttu-id="a1fba-126">Para enrutar las llamadas telefónicas del usuario mediante la infraestructura de Lync Server 2010 de acuerdo con la Directiva de clase de servicio, incluida la comunicación de audio de PC a PC, haga clic en **telefonía IP empresarial**.</span><span class="sxs-lookup"><span data-stu-id="a1fba-126">To route the user's phone calls by using the Lync Server 2010 infrastructure in accordance with the class of service policy, including PC-to-PC audio communication, click **Enterprise Voice**.</span></span> <span data-ttu-id="a1fba-127">En **URI de línea**, especifique el número de teléfono de la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="a1fba-127">In **Line URI**, specify the telephone number for Enterprise Voice.</span></span> <span data-ttu-id="a1fba-128">En **Directiva de plan de marcado** y **Directiva de voz**, especifique las directivas apropiadas para el usuario.</span><span class="sxs-lookup"><span data-stu-id="a1fba-128">In **Dial plan policy** and **Voice policy**, specify the appropriate policies for the user.</span></span> <span data-ttu-id="a1fba-129">Para especificar las reglas de normalización para traducir números de teléfono marcados por el usuario al formato E. 164, seleccione el perfil de ubicación adecuado en la **política de ubicación**.</span><span class="sxs-lookup"><span data-stu-id="a1fba-129">To specify the normalization rules for translating phone numbers dialed by the user to the E.164 format, select the appropriate location profile in **Location policy**.</span></span>
    
      - <span data-ttu-id="a1fba-130">Para habilitar el control remoto de llamadas, que permite a los usuarios controlar la línea telefónica de escritorio de Lync Server 2013 para hacer llamadas de PC a PC y llamadas de PC a teléfono, haga clic en **control remoto de llamadas**.</span><span class="sxs-lookup"><span data-stu-id="a1fba-130">To enable remote call control, which enables users to control their desktop phone line from Lync Server 2013 to make PC-to-PC calls and PC-to-phone calls, click **Remote call control**.</span></span> <span data-ttu-id="a1fba-131">En **URI de línea**, especifique el número de teléfono para el control de llamada remota.</span><span class="sxs-lookup"><span data-stu-id="a1fba-131">In **Line URI**, specify the telephone number for remote call control.</span></span> <span data-ttu-id="a1fba-132">El usuario debe tener una conexión de teléfono de escritorio y de central de conmutación (PBX) para el enrutamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="a1fba-132">The user must have a desktop phone and private branch exchange (PBX) connection for call routing.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a1fba-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1fba-133">See Also</span></span>


[<span data-ttu-id="a1fba-134">Modificar las propiedades de la cuenta de usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a1fba-134">Modifying user account properties in Lync Server 2013</span></span>](lync-server-2013-modifying-user-account-properties.md)  
  

<span data-ttu-id="a1fba-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a1fba-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

