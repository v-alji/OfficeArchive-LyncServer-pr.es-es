---
title: 'Lync Server 2013: Probar la implementación del grupo de servidores'
description: 'Lync Server 2013: Pruebe la implementación del grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test the pool deployment
ms:assetid: ffd80617-155a-4041-bbeb-74503e7938dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413092(v=OCS.15)
ms:contentKeyID: 48185976
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28101a252eda5048ded9f1eaf76c092c5cb7f986
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444234"
---
# <a name="test-the-pool-deployment-in-lync-server-2013"></a><span data-ttu-id="2131c-103">Probar la implementación del grupo de servidores en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2131c-103">Test the pool deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2131c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2131c-104">

<span> </span></span></span>

<span data-ttu-id="2131c-105">_**Última modificación del tema:** 2013-09-25_</span><span class="sxs-lookup"><span data-stu-id="2131c-105">_**Topic Last Modified:** 2013-09-25_</span></span>

<span data-ttu-id="2131c-106">En el procedimiento siguiente se describe cómo probar la implementación del grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="2131c-106">The following procedure describes how to test the deployment of the Front End pool.</span></span>

<div>

## <a name="to-test-the-pool-deployment"></a><span data-ttu-id="2131c-107">Para probar la implementación de la agrupación</span><span class="sxs-lookup"><span data-stu-id="2131c-107">To test the pool deployment</span></span>

1.  <span data-ttu-id="2131c-108">Use equipos y usuarios de Active Directory para agregar el objeto de usuario de Active Directory de la función Administrador de la implementación de Lync Server 2013 (en la que está instalado el panel de control de Lync Server 2013) en el grupo **CSAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="2131c-108">Use Active Directory Computers and Users to add the Active Directory user object of the administrator role for the Lync Server 2013 deployment (on which Lync Server 2013 Control Panel is installed) to the **CSAdministrator** group.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="2131c-109">Si no agrega los usuarios y grupos adecuados al grupo CsAdministors, recibirá un error al abrir el panel de control de Lync Server, que indica "no autorizado: acceso denegado debido a un error de autorización de control de acceso basado en roles (RBAC)."</span><span class="sxs-lookup"><span data-stu-id="2131c-109">If you do not add the appropriate users and groups to the CsAdministors group, you will receive an error when opening Lync Server Control Panel, which states that “Unauthorized: Access is denied due to a role-based access control (RBAC) authorization failure.”</span></span>

    
    </div>

2.  <span data-ttu-id="2131c-110">Si actualmente el objeto de usuario ha iniciado sesión, cierre sesión y, luego, vuelva a iniciarla para registrar la nueva asignación de grupo.</span><span class="sxs-lookup"><span data-stu-id="2131c-110">If the user object is currently logged on, log off and then log on again to register the new group assignment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2131c-111">La cuenta de usuario no puede ser el administrador local de ningún servidor que ejecute Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2131c-111">The user account cannot be the local administrator of any server running Lync Server 2013.</span></span>

    
    </div>

3.  <span data-ttu-id="2131c-112">Use la cuenta administrativa para iniciar sesión en el equipo en el que está instalado el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2131c-112">Use the administrative account to log on to the computer where Lync Server Control Panel is installed.</span></span>

4.  <span data-ttu-id="2131c-113">Inicie el panel de control de Lync Server y, si se le solicita, proporcione las credenciales.</span><span class="sxs-lookup"><span data-stu-id="2131c-113">Start Lync Server Control Panel, and then provide credentials, if prompted.</span></span> <span data-ttu-id="2131c-114">El panel de control de Lync Server muestra información de implementación.</span><span class="sxs-lookup"><span data-stu-id="2131c-114">Lync Server Control Panel displays deployment information.</span></span>

5.  <span data-ttu-id="2131c-115">En la barra de navegación izquierda, haga clic en **topología** y, a continuación, confirme que el estado del servicio muestra un equipo con una flecha verde y que una marca de verificación verde para el estado de replicación está junto a cada rol de servidor de Lync Server que se ha implementado y se ha puesto en conexión.</span><span class="sxs-lookup"><span data-stu-id="2131c-115">In the left navigation bar, click **Topology**, and then confirm that the service status shows a computer with a green arrow and that a green check mark for replication status is next to each Lync Server server role that has been deployed and brought online.</span></span>

6.  <span data-ttu-id="2131c-116">En la barra de navegación izquierda, haga clic en **Usuarios** y, luego, haga clic en **Habilitar usuarios**.</span><span class="sxs-lookup"><span data-stu-id="2131c-116">In the left navigation bar, click **Users**, and then click **Enable users**.</span></span>

7.  <span data-ttu-id="2131c-117">En la página **nuevo usuario de Lync Server** , haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="2131c-117">On the **New Lync Server User** page, click **Add**.</span></span>

8.  <span data-ttu-id="2131c-118">Para definir parámetros de búsqueda de los objetos que quiera encontrar, en la página **Seleccionar de Active Directory**, seleccione **Buscar** y, si lo desea, haga clic en **Agregar filtro**.</span><span class="sxs-lookup"><span data-stu-id="2131c-118">To define search parameters for the objects you want to find, on the **Select from Active Directory** page, you can select **Search**, and then optionally click **Add Filter**.</span></span> <span data-ttu-id="2131c-119">También puede seleccionar **Búsqueda LDAP** y especificar una expresión de LDAP para filtrar o limitar los objetos que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="2131c-119">You can also select **LDAP search** and enter an LDAP expression to filter or limit the objects that will be returned.</span></span> <span data-ttu-id="2131c-120">Una vez que haya decidido las opciones de búsqueda, **Busque** vínculos de vínculos.</span><span class="sxs-lookup"><span data-stu-id="2131c-120">After you have decided on your Search options, clink **Find**.</span></span>

9.  <span data-ttu-id="2131c-121">En el panel Resultados de la búsqueda, seleccione todos los objetos de esta sesión de búsqueda y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="2131c-121">In the Search results pane, select all the objects for this search session, and then click **OK**.</span></span>

10. <span data-ttu-id="2131c-122">En la página **nuevo usuario de Lync Server** , el objeto o los objetos que haya seleccionado aparecerán en la pantalla **usuarios** .</span><span class="sxs-lookup"><span data-stu-id="2131c-122">On the **New Lync Server User** page, the object or objects you selected are in the **Users** display.</span></span> <span data-ttu-id="2131c-123">En la lista **asignar usuarios a un grupo** , seleccione el servidor en el que se deben alojar los objetos.</span><span class="sxs-lookup"><span data-stu-id="2131c-123">In the **Assign users to a pool** list, select the server where the objects should be homed.</span></span>
    
    <span data-ttu-id="2131c-124">A continuación se muestran varias opciones para configurar los objetos.</span><span class="sxs-lookup"><span data-stu-id="2131c-124">Following are a number of options for configuring the objects.</span></span>
    
      - <span data-ttu-id="2131c-125">**Generar el URI de SIP del usuario**</span><span class="sxs-lookup"><span data-stu-id="2131c-125">**Generate user’s SIP URI**</span></span>
    
      - <span data-ttu-id="2131c-126">**Telefonía**</span><span class="sxs-lookup"><span data-stu-id="2131c-126">**Telephony**</span></span>
    
      - <span data-ttu-id="2131c-127">**URI de línea**</span><span class="sxs-lookup"><span data-stu-id="2131c-127">**Line URI**</span></span>
    
      - <span data-ttu-id="2131c-128">**Directiva de conferencia**</span><span class="sxs-lookup"><span data-stu-id="2131c-128">**Conferencing policy**</span></span>
    
      - <span data-ttu-id="2131c-129">**Directiva de versión de cliente**</span><span class="sxs-lookup"><span data-stu-id="2131c-129">**Client version policy**</span></span>
    
      - <span data-ttu-id="2131c-130">**Directiva de PIN**</span><span class="sxs-lookup"><span data-stu-id="2131c-130">**PIN policy**</span></span>
    
      - <span data-ttu-id="2131c-131">**Directiva de acceso externo**</span><span class="sxs-lookup"><span data-stu-id="2131c-131">**External access policy**</span></span>
    
      - <span data-ttu-id="2131c-132">**Directiva de archivado**</span><span class="sxs-lookup"><span data-stu-id="2131c-132">**Archiving policy**</span></span>
    
      - <span data-ttu-id="2131c-133">**Directiva de ubicación**</span><span class="sxs-lookup"><span data-stu-id="2131c-133">**Location policy**</span></span>
    
      - <span data-ttu-id="2131c-134">**Directiva de cliente**</span><span class="sxs-lookup"><span data-stu-id="2131c-134">**Client policy**</span></span>
    
    <span data-ttu-id="2131c-135">A fin de probar la funcionalidad básica, seleccione la opción que prefiera para la configuración de **URI de SIP del usuario** (las demás opciones de la configuración usarán la configuración predeterminada) y, a continuación, haga clic en **Habilitar**.</span><span class="sxs-lookup"><span data-stu-id="2131c-135">For the purposes of testing the basic functionality, select the option you prefer for the **Generate user’s SIP URI** setting (the other options in the configuration will use default settings), and then click **Enable**.</span></span>

11. <span data-ttu-id="2131c-136">Se muestra una página de resumen que muestra una marca de verificación en la columna **habilitada** para indicar que los objetos ya están listos para su uso.</span><span class="sxs-lookup"><span data-stu-id="2131c-136">A summary page is displayed that shows a check mark in the **Enabled** column to indicate that the objects are now ready for use.</span></span> <span data-ttu-id="2131c-137">En la columna **Dirección SIP** figura la dirección que se necesita para configurar el inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="2131c-137">The **SIP address** column displays the address you need for the user sign-in configuration.</span></span>

12. <span data-ttu-id="2131c-138">Iniciar sesión de un usuario en un equipo que se une al dominio y otro usuario en otro equipo del dominio.</span><span class="sxs-lookup"><span data-stu-id="2131c-138">Log one user on to a computer that is joined to the domain, and another user on to another computer in the domain.</span></span>

13. <span data-ttu-id="2131c-139">Instale Lync 2013 en cada uno de los dos equipos cliente y, a continuación, compruebe que ambos usuarios pueden iniciar sesión en Lync Server 2013 y pueden enviar mensajes instantáneos entre sí.</span><span class="sxs-lookup"><span data-stu-id="2131c-139">Install Lync 2013 on each of the two client computers, and then verify that both users can sign in to Lync Server 2013 and can send instant messages to each other.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2131c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2131c-140">See Also</span></span>


[<span data-ttu-id="2131c-141">Implementación de clientes y dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2131c-141">Deploying clients and devices in Lync Server 2013</span></span>](lync-server-2013-deploying-clients-and-devices.md)  
  

<span data-ttu-id="2131c-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2131c-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

