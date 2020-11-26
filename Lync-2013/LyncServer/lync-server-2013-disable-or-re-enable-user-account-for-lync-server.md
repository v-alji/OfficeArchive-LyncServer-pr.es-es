---
title: 'Lync Server 2013: deshabilitar o volver a habilitar la cuenta de usuario para Lync Server'
description: 'Lync Server 2013: deshabilitar o volver a habilitar la cuenta de usuario para Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disable or re-enable user account for Lync Server
ms:assetid: 12497d00-f665-4a97-be68-854c5a8be4fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429696(v=OCS.15)
ms:contentKeyID: 48183455
ms.date: 04/05/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b30d83d7a7f38b84f8e669ac06947eebf4a8545
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437843"
---
# <a name="disable-or-re-enable-user-account-for-lync-server-2013"></a><span data-ttu-id="b63e0-103">Deshabilitar o volver a habilitar la cuenta de usuario para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b63e0-103">Disable or re-enable user account for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b63e0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b63e0-104">

<span> </span></span></span>

<span data-ttu-id="b63e0-105">_**Última modificación del tema:** 2016-04-04_</span><span class="sxs-lookup"><span data-stu-id="b63e0-105">_**Topic Last Modified:** 2016-04-04_</span></span>

<span data-ttu-id="b63e0-106">Puede usar el siguiente procedimiento para deshabilitar una cuenta de usuario habilitada previamente en Lync Server 2013 sin perder la configuración de Lync Server que ha configurado para la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="b63e0-106">You can use the following procedure to disable a previously enabled user account in Lync Server 2013 without losing the Lync Server settings that you configured for the user account.</span></span> <span data-ttu-id="b63e0-107">Como no pierde la configuración de la cuenta de usuario de Lync Server, puede volver a habilitar otra cuenta de usuario habilitada previamente sin tener que volver a configurar la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="b63e0-107">Because you do not lose the Lync Server user account settings, you can re-enable a previously enabled user account again without having to reconfigure the user account.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="b63e0-108">Simplemente deshabilitar una cuenta de usuario en Active Directory <STRONG>no impedirá</STRONG> que un usuario pueda iniciar sesión o usar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b63e0-108">Simply disabling a user account in Active Directory <STRONG>will not</STRONG> stop a user from being able to sign into or use Lync Server.</span></span> <span data-ttu-id="b63e0-109">Esto se debe a que Lync usa la autenticación de certificados que optimiza el proceso de autenticación y estos certificados de cliente son válidos durante 180 días.</span><span class="sxs-lookup"><span data-stu-id="b63e0-109">This is because Lync uses certificate authentication that streamlines the authentication process, and these client certificates are valid for 180 days.</span></span> <span data-ttu-id="b63e0-110">Si desea detener la deshabilitación de las cuentas de Active Directory que se han habilitado para que Lync tenga acceso a Lync Server, debe usar el cmdlet <STRONG>Disable-CsUser</STRONG> , o el <STRONG>Panel de control de Lync Server</STRONG> , como se indica en este artículo.</span><span class="sxs-lookup"><span data-stu-id="b63e0-110">If you want to stop disabled Active Directory accounts that had been enabled for Lync from having access to Lync Server, you must use the <STRONG>Disable-CsUser</STRONG> cmdlet, or use the <STRONG>Lync Server Control Panel</STRONG> as laid out in this article.</span></span> <span data-ttu-id="b63e0-111">Una vez que el usuario está deshabilitado en Lync y el almacén central de administración se ha replicado en el entorno, los usuarios ya no podrán iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="b63e0-111">Once the user is disabled in Lync and the Central Management store has been replicated in the environment the users will no longer be able to sign in.</span></span> <span data-ttu-id="b63e0-112">Además, se desconectarán los usuarios que hayan iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="b63e0-112">Also, users that are signed in will get disconnected.</span></span>



</div>

<div>

## <a name="to-disable-or-re-enable-a-previously-enabled-user-account-for-lync-server"></a><span data-ttu-id="b63e0-113">Para deshabilitar o volver a habilitar una cuenta de usuario habilitada previamente para Lync Server</span><span class="sxs-lookup"><span data-stu-id="b63e0-113">To disable or re-enable a previously enabled user account for Lync Server</span></span>

1.  <span data-ttu-id="b63e0-114">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="b63e0-114">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="b63e0-115">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b63e0-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="b63e0-116">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b63e0-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="b63e0-117">En la barra de navegación izquierda, haga clic en **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="b63e0-117">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="b63e0-118">En el cuadro **Buscar usuarios** , escriba todas o la primera parte del nombre para mostrar, el nombre, el apellido, el nombre de cuenta del administrador de cuentas de seguridad (SAM), la dirección SIP o el identificador uniforme de recursos (URI) de la cuenta de usuario que desea deshabilitar o volver a habilitar y, a continuación, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="b63e0-118">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want to disable or re-enable, and then click **Find**.</span></span>

5.  <span data-ttu-id="b63e0-119">En la tabla, haga clic en la cuenta de usuario que desea deshabilitar o volver a habilitar.</span><span class="sxs-lookup"><span data-stu-id="b63e0-119">In the table, click the user account that you want to disable or re-enable.</span></span>

6.  <span data-ttu-id="b63e0-120">En el menú **acción** , siga uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="b63e0-120">On the **Action** menu, do one of the following:</span></span>
    
      - <span data-ttu-id="b63e0-121">Para deshabilitar temporalmente la cuenta de usuario de Lync Server 2013, haga clic en **deshabilitar temporalmente para Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="b63e0-121">To temporarily disable the user account for Lync Server 2013, click **Temporarily disable for Lync Server**.</span></span>
    
      - <span data-ttu-id="b63e0-122">Para habilitar la cuenta de usuario de Lync Server 2013, haga clic en **volver a habilitar para Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="b63e0-122">To enable the user account for Lync Server 2013, click **Re-enable for Lync Server**.</span></span>

</div>

<div>

## <a name="using-windows-powershell-to-disable-or-re-enable-user-accounts"></a><span data-ttu-id="b63e0-123">Usar Windows PowerShell para deshabilitar o volver a habilitar cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="b63e0-123">Using Windows PowerShell to Disable or Re-enable User Accounts</span></span>

<span data-ttu-id="b63e0-124">Las cuentas de usuario se pueden deshabilitar temporalmente y, después, volverlas a habilitar más tarde mediante el cmdlet **set-CsUser** .</span><span class="sxs-lookup"><span data-stu-id="b63e0-124">User accounts can be temporarily disabled, and then later re-enabled, by using the **Set-CsUser** cmdlet.</span></span> <span data-ttu-id="b63e0-125">Puede ejecutar este cmdlet desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b63e0-125">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="b63e0-126">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="b63e0-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-disable-a-user-account"></a><span data-ttu-id="b63e0-127">Para deshabilitar una cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="b63e0-127">To disable a user account</span></span>

  - <span data-ttu-id="b63e0-128">Para deshabilitar temporalmente una cuenta de usuario, establezca el valor de la propiedad Enabled en false ($False).</span><span class="sxs-lookup"><span data-stu-id="b63e0-128">To temporarily disable a user account, set the value of the Enabled property to False ($False).</span></span> <span data-ttu-id="b63e0-129">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b63e0-129">For example:</span></span>
    
        Set-CsUser -Identity "Ken Myer" -Enabled $False

</div>

<div>

## <a name="to-re-enable-a-user-account"></a><span data-ttu-id="b63e0-130">Para volver a habilitar una cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="b63e0-130">To re-enable a user account</span></span>

  - <span data-ttu-id="b63e0-131">Para volver a habilitar una cuenta de usuario deshabilitada, establezca el valor de la propiedad Enabled en true ($True).</span><span class="sxs-lookup"><span data-stu-id="b63e0-131">To re-enable a disabled user account, set the value of the Enabled property to True ($True).</span></span> <span data-ttu-id="b63e0-132">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b63e0-132">For example:</span></span>
    
        Set-CsUser -Identity "Ken Myer" -Enabled $True

</div>

<span data-ttu-id="b63e0-133">Para obtener más información, consulte el tema de ayuda para el cmdlet [set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) .</span><span class="sxs-lookup"><span data-stu-id="b63e0-133">For more information, see the help topic for the [Set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b63e0-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b63e0-134">See Also</span></span>


[<span data-ttu-id="b63e0-135">Agregar y habilitar una cuenta de usuario para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b63e0-135">Add and enable user account for Lync Server 2013</span></span>](lync-server-2013-add-and-enable-user-account-for-lync-server.md)  


[<span data-ttu-id="b63e0-136">Habilitar y deshabilitar usuarios para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b63e0-136">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="b63e0-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b63e0-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

