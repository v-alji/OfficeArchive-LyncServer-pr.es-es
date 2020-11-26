---
title: Eliminar una colección existente de opciones de configuración de Lync Phone Edition
description: Eliminar una colección existente de opciones de configuración de Lync Phone Edition.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of Lync Phone Edition configuration settings
ms:assetid: 1bfc427d-4dcd-4199-b25f-8d5cfec2164f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687984(v=OCS.15)
ms:contentKeyID: 49733574
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5137590a37b8bbb47f7445d20639157953597ca6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430558"
---
# <a name="delete-an-existing-collection-of-lync-phone-edition-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="215d0-103">Eliminar una colección existente de opciones de configuración de Lync Phone Edition en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="215d0-103">Delete an existing collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="215d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="215d0-104">

<span> </span></span></span>

<span data-ttu-id="215d0-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="215d0-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="215d0-106">Si ya no desea usar una colección de configuraciones para dispositivos que ejecutan Lync Phone Edition, elimínelo.</span><span class="sxs-lookup"><span data-stu-id="215d0-106">If you no longer want to use a collection of settings for devices running Lync Phone Edition, delete it.</span></span> <span data-ttu-id="215d0-107">Si elimina una colección de un sitio, la configuración global se aplicará a los teléfonos de ese sitio.</span><span class="sxs-lookup"><span data-stu-id="215d0-107">If you delete a collection for a site, the global settings will apply to the phones in that site.</span></span> <span data-ttu-id="215d0-108">No se puede eliminar la colección global.</span><span class="sxs-lookup"><span data-stu-id="215d0-108">You cannot delete the global collection.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="215d0-109">En lugar de eliminar una colección, es posible que solo desee cambiar algunos de los valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="215d0-109">Instead of deleting a collection, you might just want to change some of the settings.</span></span> <span data-ttu-id="215d0-110">Para obtener más información sobre cómo hacerlo, vea <A href="lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md">crear o modificar una colección de opciones de configuración de Lync Phone Edition en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="215d0-110">For details about how to do so, see <A href="lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md">Create or modify a collection of Lync Phone Edition configuration settings in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-delete-a-collection-of-lync-phone-edition-configuration-settings"></a><span data-ttu-id="215d0-111">Para eliminar una colección de opciones de configuración de Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="215d0-111">To delete a collection of Lync Phone Edition configuration settings</span></span>

1.  <span data-ttu-id="215d0-112">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="215d0-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="215d0-113">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="215d0-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="215d0-114">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="215d0-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="215d0-115">En la barra de navegación izquierda, haga clic en **clientes** y, a continuación, haga clic en el botón de navegación **configuración de dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="215d0-115">In the left navigation bar, click **Clients**, and then click the **Device Configuration** navigation button.</span></span>

4.  <span data-ttu-id="215d0-116">En la página **configuración de dispositivo** , haga clic en la colección que desea eliminar, haga clic en el menú **Editar** y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="215d0-116">On the **Device Configuration** page, click the collection you want to delete, click the **Edit** menu, and then click **Delete**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="215d0-117">Si elimina la colección global, la configuración solo volverá a la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="215d0-117">If you delete the global collection, the settings just revert to the default settings.</span></span> <span data-ttu-id="215d0-118">La colección no desaparece.</span><span class="sxs-lookup"><span data-stu-id="215d0-118">The collection does not go away.</span></span>

    
    </div>

5.  <span data-ttu-id="215d0-119">En el cuadro de confirmación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="215d0-119">In the confirmation box, click **OK**.</span></span>

</div>

<div>

## <a name="removing-lync-phone-edition-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="215d0-120">Quitar las opciones de configuración de Lync Phone Edition mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="215d0-120">Removing Lync Phone Edition Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="215d0-121">Puede eliminar la configuración de Lync Phone Edition con Windows PowerShell y el cmdlet **Remove-CsUCConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="215d0-121">You can delete Lync Phone Edition configuration settings by using Windows PowerShell and the **Remove-CsUCConfiguration** cmdlet.</span></span> <span data-ttu-id="215d0-122">Puede ejecutar este cmdlet desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="215d0-122">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="215d0-123">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="215d0-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-lync-phone-edition-configuration-settings"></a><span data-ttu-id="215d0-124">Para quitar una colección especificada de opciones de configuración de Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="215d0-124">To remove a specified collection of Lync Phone Edition configuration settings</span></span>

  - <span data-ttu-id="215d0-125">Este comando elimina la configuración de la configuración del teléfono UC aplicada al sitio de Redmond:</span><span class="sxs-lookup"><span data-stu-id="215d0-125">This command deletes the UC phone configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsUCPhoneConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-of-the-lync-phone-edition-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="215d0-126">Para quitar todas las opciones de configuración de Lync Phone Edition aplicadas al ámbito del sitio</span><span class="sxs-lookup"><span data-stu-id="215d0-126">To remove all of the Lync Phone Edition configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="215d0-127">Este comando elimina todas las opciones de configuración del teléfono UC aplicadas al ámbito de servicio:</span><span class="sxs-lookup"><span data-stu-id="215d0-127">This command removes all the UC phone configuration settings applied to the service scope:</span></span>
    
        Get-CsUCPhoneConfiguration -Filter "site:*" | Remove-CsUCPhoneConfiguration

</div>

<div>

## <a name="to-remove-all-of-the-lync-phone-edition-configuration-settings-where-phone-locking-is-disabled"></a><span data-ttu-id="215d0-128">Para quitar todas las opciones de configuración de Lync Phone Edition en las que el bloqueo de teléfono está deshabilitado</span><span class="sxs-lookup"><span data-stu-id="215d0-128">To remove all of the Lync Phone Edition configuration settings where phone locking is disabled</span></span>

  - <span data-ttu-id="215d0-129">Este comando elimina cualquier colección de parámetros de configuración de teléfono UC en los que se ha deshabilitado el bloqueo de teléfono:</span><span class="sxs-lookup"><span data-stu-id="215d0-129">This command deletes any collection of UC phone configuration settings where phone locking has been disabled:</span></span>
    
        Get-CsUCPhoneConfiguration | Where-Object {$_.EnforcePhoneLock -eq $False} | Remove-CsUCPhoneConfiguration

</div>

<span data-ttu-id="215d0-130">Para obtener más información, consulte [Remove-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398249(v=OCS.15)).</span><span class="sxs-lookup"><span data-stu-id="215d0-130">For details, see [Remove-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398249(v=OCS.15)).</span></span>

<span data-ttu-id="215d0-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="215d0-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

