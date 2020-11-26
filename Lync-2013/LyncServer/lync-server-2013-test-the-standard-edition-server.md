---
title: 'Lync Server 2013: Comprobar el servidor Standard Edition'
description: 'Lync Server 2013: Pruebe el servidor Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test the Standard Edition server
ms:assetid: b6ef67bb-9665-43e4-b8b3-eac8898eebf6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412890(v=OCS.15)
ms:contentKeyID: 48185220
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 35dc13fc01979cc8b293d0647a7886b7d65d7669
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441182"
---
# <a name="test-the-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="42e96-103">Comprobar el servidor Standard Edition en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42e96-103">Test the Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42e96-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42e96-104">

<span> </span></span></span>

<span data-ttu-id="42e96-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="42e96-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="42e96-106">En el procedimiento siguiente se describe cómo probar la implementación de un servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="42e96-106">The following procedure describes how to test the deployment of a Standard Edition server.</span></span>

<div>

## <a name="to-test-the-deployment-of-a-standard-edition-server"></a><span data-ttu-id="42e96-107">Para probar la implementación de un servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="42e96-107">To test the deployment of a Standard Edition Server</span></span>

1.  <span data-ttu-id="42e96-108">Use equipos y usuarios de Active Directory para agregar el objeto de usuario de Active Directory de la función Administrador de la implementación de Lync Server 2013 (en la que está instalado el panel de control de Lync Server) en el grupo **CSAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="42e96-108">Use Active Directory Computers and Users to add the Active Directory user object of the administrator role for the Lync Server 2013 deployment (on which Lync Server Control Panel is installed) to the **CSAdministrator** group.</span></span>

2.  <span data-ttu-id="42e96-109">Si actualmente el objeto de usuario ha iniciado sesión, cierre sesión y, luego, vuelva a iniciarla para registrar la nueva asignación de grupo.</span><span class="sxs-lookup"><span data-stu-id="42e96-109">If the user object is currently logged on, log off and then log on again to register the new group assignment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="42e96-110">La cuenta de usuario no puede ser el administrador local del servidor que ejecuta Lync Server 2013, Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="42e96-110">The user account cannot be the local administrator of the server running Lync Server 2013, Standard Edition.</span></span> <span data-ttu-id="42e96-111">Si no agrega los usuarios y grupos adecuados al grupo CsAdministors, recibirá un error al abrir el panel de control de Lync Server 2013, que indica que "no autorizado: acceso denegado debido a un error de autorización de control de acceso basado en roles (RBAC)."</span><span class="sxs-lookup"><span data-stu-id="42e96-111">If you do not add the appropriate users and groups to the CsAdministors group, you will receive an error when opening Lync Server 2013 Control Panel, which states that “Unauthorized: Access is denied due to a role-based access control (RBAC) authorization failure.”</span></span>

    
    </div>

3.  <span data-ttu-id="42e96-112">Use la cuenta administrativa para iniciar sesión en el equipo en el que está instalado el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="42e96-112">Use the administrative account to log on to the computer where Lync Server Control Panel is installed.</span></span>

4.  <span data-ttu-id="42e96-113">Inicie el panel de control de Lync Server y proporcione credenciales, si se le solicita.</span><span class="sxs-lookup"><span data-stu-id="42e96-113">Start Lync Server Control Panel and provide credentials, if prompted.</span></span> <span data-ttu-id="42e96-114">El panel de control de Lync Server 2013 muestra información de implementación.</span><span class="sxs-lookup"><span data-stu-id="42e96-114">Lync Server 2013 Control Panel displays deployment information.</span></span>

5.  <span data-ttu-id="42e96-115">En la barra de navegación izquierda, haga clic en **topología** y, a continuación, confirme que el estado del servicio es un icono de equipo con una flecha verde y hay una marca de verificación verde junto a cada rol de servidor de Lync Server que se ha implementado y se ha puesto en conexión.</span><span class="sxs-lookup"><span data-stu-id="42e96-115">In the left navigation bar, click **Topology**, and then confirm that the service status is a computer icon with a green arrow and there is a green check mark next to each Lync Server server role that has been deployed and brought online.</span></span>

6.  <span data-ttu-id="42e96-116">En la barra de navegación izquierda, haga clic en **usuarios** y, a continuación, habilite los dos usuarios para Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="42e96-116">In the left navigation bar, click **Users**, and then enable the two users for Lync Server 2013.</span></span>

7.  <span data-ttu-id="42e96-117">Iniciar sesión de un usuario en un equipo unido al dominio y el otro usuario en otro equipo del dominio.</span><span class="sxs-lookup"><span data-stu-id="42e96-117">Log one user on to a computer that is joined to the domain, and the other user on to another computer in the domain.</span></span>

8.  <span data-ttu-id="42e96-118">Instale Lync Server 2013 en cada uno de los dos equipos cliente y, a continuación, compruebe que ambos usuarios pueden iniciar sesión en Lync Server 2013 y pueden enviar mensajes instantáneos entre sí.</span><span class="sxs-lookup"><span data-stu-id="42e96-118">Install Lync Server 2013 on each of the two client computers, and then verify that both users can sign in to Lync Server 2013 and can send instant messages to each other.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="42e96-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="42e96-119">See Also</span></span>


[<span data-ttu-id="42e96-120">Implementación de clientes y dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42e96-120">Deploying clients and devices in Lync Server 2013</span></span>](lync-server-2013-deploying-clients-and-devices.md)  
  

<span data-ttu-id="42e96-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42e96-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

