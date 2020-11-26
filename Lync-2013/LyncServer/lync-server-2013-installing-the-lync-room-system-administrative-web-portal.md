---
title: 'Lync Server 2013: instalar el portal web administrativo del sistema Lync Room'
description: 'Lync Server 2013: instalar el portal web administrativo del sistema de Lync Room.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Room System Administrative Web Portal
ms:assetid: dd19e368-c338-4e21-a40d-6439d46a9748
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436326(v=OCS.15)
ms:contentKeyID: 56737622
ms.date: 04/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0fba239346d75142bb4009c58e0ac67e8e1f3bcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427008"
---
# <a name="installing-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a><span data-ttu-id="e4579-103">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4579-103">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e4579-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e4579-104">

<span> </span></span></span>

<span data-ttu-id="e4579-105">_**Última modificación del tema:** 2015-04-09_</span><span class="sxs-lookup"><span data-stu-id="e4579-105">_**Topic Last Modified:** 2015-04-09_</span></span>

<span data-ttu-id="e4579-106">Puede descargar el portal web administrativo del sistema de Microsoft Lync Room en el centro de descarga de Microsoft en [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044) .</span><span class="sxs-lookup"><span data-stu-id="e4579-106">You can download the Microsoft Lync Room System Administrative Web Portal from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044).</span></span>

<span data-ttu-id="e4579-107">Para instalar el portal web administrativo del sistema de Lync Room, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="e4579-107">To install the Lync Room System Administrative Web Portal, use the following steps.</span></span>

1.  <span data-ttu-id="e4579-108">Configure el puerto de la aplicación de confianza ejecutando el siguiente cmdlet en el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="e4579-108">Configure the Trusted Application Port by running the following cmdlet in Lync Server Management Shell:</span></span>
    
        Set-CsWebServer -Identity POOLFQDN -MeetingRoomAdminPortalInternalListeningPort 4456 -MeetingRoomAdminPortalExternalListeningPort 4457

2.  <span data-ttu-id="e4579-109">Para instalar el portal sala de reuniones, descargue **LyncRoomAdminPortal.exe** y, a continuación, ejecútelo como administrador.</span><span class="sxs-lookup"><span data-stu-id="e4579-109">To install the Meeting Room Portal, download **LyncRoomAdminPortal.exe** and then run it as an administrator.</span></span>

3.  <span data-ttu-id="e4579-110">Abra el archivo Web.config, que se encuentra en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="e4579-110">Open the Web.config file from the following location:</span></span>
    
    <span data-ttu-id="e4579-111">% Archivos de programa% \\ Microsoft Lync Server 2013 \\ Web Components \\ portal sala de reuniones \\ \\ controlador int</span><span class="sxs-lookup"><span data-stu-id="e4579-111">%Program Files%\\Microsoft Lync Server 2013\\Web Components\\Meeting Room Portal\\Int\\Handler</span></span>\\

4.  <span data-ttu-id="e4579-112">En el archivo Web.Config, cambie PortalUserName por el nombre de usuario creado en el paso 2, en la sección "configuración de los requisitos previos para Lync Room System admin portal" (el nombre recomendado en el paso es LRSApp):</span><span class="sxs-lookup"><span data-stu-id="e4579-112">In the Web.Config file, change the PortalUserName to the username created in Step 2 under the section “Configuring Prerequisites for Lync Room System Admin Portal” (the recommended name in the step is LRSApp):</span></span>
    
        <add key="PortalUserName" value="sip:LRSApp@domain.com" />

5.  <span data-ttu-id="e4579-113">Dado que el portal de administración de LRS es una aplicación de confianza, no es necesario que proporcione la contraseña en la configuración del portal.</span><span class="sxs-lookup"><span data-stu-id="e4579-113">Because the LRS Admin Portal is a trusted application, you do not need to provide the password in the portal configuration.</span></span> <span data-ttu-id="e4579-114">Si este usuario utiliza un registrador diferente del local, deberá especificar el registrador que utilizará agregando la siguiente línea en el archivo Web.Config:</span><span class="sxs-lookup"><span data-stu-id="e4579-114">If this user is using a different registrar than local registrar, you need to specify the registrar for it by adding the following line in the Web.Config file:</span></span>
    
        <add key="PortalUserRegistrarFQDN" value="pool-xxxx.domain.com" />

6.  <span data-ttu-id="e4579-115">Si utiliza un puerto diferente de 5061, agregue la siguiente línea en el archivo Web.Config: </span><span class="sxs-lookup"><span data-stu-id="e4579-115">If the port used is other than 5061, add the following line in the Web.Config file:</span></span>
    
        <add key="PortalUserRegistrarPort" value="5061" />

<div>

## <a name="verifying-installation-of-the-lync-room-system-administrative-web-portal"></a><span data-ttu-id="e4579-116">Comprobar la instalación del portal web administrativo del sistema Lync Room</span><span class="sxs-lookup"><span data-stu-id="e4579-116">Verifying Installation of the Lync Room System Administrative Web Portal</span></span>

<span data-ttu-id="e4579-117">Para comprobar la instalación del portal web administrativo del sistema de Lync Room, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e4579-117">To verify installation of the Lync Room System Administrative Web Portal, do the following:</span></span>


1.  <span data-ttu-id="e4579-118">En un servidor front-end, vaya a la siguiente URL:</span><span class="sxs-lookup"><span data-stu-id="e4579-118">On a Front End server, browse to the following URL:</span></span>
    
    <span data-ttu-id="e4579-119"> https:// \<fe-server\> /LRS</span><span class="sxs-lookup"><span data-stu-id="e4579-119">https://\<fe-server\>/lrs</span></span>
    
    <span data-ttu-id="e4579-120">No debería ver ningún error, como se muestra en la imagen siguiente:</span><span class="sxs-lookup"><span data-stu-id="e4579-120">You should not see any errors, as shown in the following image:</span></span>
    
    <span data-ttu-id="e4579-121">![Pantalla de inicio de sesión en el portal de administración del sistema Lync Room](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Pantalla de inicio de sesión en el portal de administración del sistema Lync Room")</span><span class="sxs-lookup"><span data-stu-id="e4579-121">![Lync Room System Admin Portal Sign In screen](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync Room System Admin Portal Sign In screen")</span></span>

2.  <span data-ttu-id="e4579-122">Si no ve ningún error, intente acceder a la siguiente URL desde cualquier otro equipo de la topología:</span><span class="sxs-lookup"><span data-stu-id="e4579-122">If you do not see any errors, try accessing the following URL from any other computer in the topology:</span></span>
    
    <span data-ttu-id="e4579-123"> https:// \<fe-server\> /LRS</span><span class="sxs-lookup"><span data-stu-id="e4579-123">https://\<fe-server\>/lrs</span></span>
    
    <span data-ttu-id="e4579-124">Para obtener acceso a la página, tendrá que agregar los registros DNS tal y como se describe en "registros DNS necesarios para el inicio de sesión de cliente automático" en [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056) .</span><span class="sxs-lookup"><span data-stu-id="e4579-124">To access the page, you will need to add the DNS records as described in “Required DNS Records for Automatic Client Sign-In” at [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056).</span></span>

<span data-ttu-id="e4579-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e4579-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

