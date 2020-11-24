---
title: Crear o modificar una colección de parámetros de configuración de la versión de cliente
description: Crear o modificar una colección de parámetros de configuración de la versión de cliente.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a collection of client version configuration settings
ms:assetid: 4e6faffd-a36f-40f1-8734-78d84b7df921
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ898477(v=OCS.15)
ms:contentKeyID: 50873757
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0082b618b8417c9d0da44599f1606cd238dfd7e8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399347"
---
# <a name="create-or-modify-a-collection-of-client-version-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="911ee-103">Crear o modificar una colección de parámetros de configuración de la versión de cliente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="911ee-103">Create or modify a collection of client version configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="911ee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="911ee-104">

<span> </span></span></span>

<span data-ttu-id="911ee-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="911ee-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="911ee-106">Los ajustes de configuración de versión de cliente se usan para activar o desactivar el control de versiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="911ee-106">Client version configuration settings are used to turn client version control on or off.</span></span> <span data-ttu-id="911ee-107">La configuración de la versión de cliente global se instala con Lync Server y se usa para habilitar o deshabilitar el control de versiones de cliente para toda la implementación del servidor.</span><span class="sxs-lookup"><span data-stu-id="911ee-107">The global client version configuration installs with Lync Server and is used to enable or disable client version control for the entire server deployment.</span></span> <span data-ttu-id="911ee-108">También puede configurar las opciones de configuración de versión de cliente para los sitios individuales.</span><span class="sxs-lookup"><span data-stu-id="911ee-108">You can also configure client version configuration settings for individual sites.</span></span> <span data-ttu-id="911ee-109">Puede crear o modificar los parámetros de configuración de la versión del cliente desde el panel de control de Lync Server 2013 o del shell de administración de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="911ee-109">You can create or modify client version configuration settings from Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="911ee-110">Debido a que los usuarios anónimos no están asociados a un usuario, sitio o servicio, este tipo de usuarios solo se ven afectados por directivas de nivel global.</span><span class="sxs-lookup"><span data-stu-id="911ee-110">Because anonymous users are not associated with a user, site, or service, anonymous users are affected by global-level policies only.</span></span>



</div>

<div>

## <a name="to-create-or-modify-client-version-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="911ee-111">Para crear o modificar parámetros de configuración de la versión del cliente mediante el panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="911ee-111">To create or modify client version configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="911ee-112">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="911ee-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="911ee-113">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="911ee-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="911ee-114">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="911ee-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="911ee-115">En la barra de navegación izquierda, haga clic en **clientes** y, a continuación, haga clic en el botón de navegación de **configuración de versión de cliente** .</span><span class="sxs-lookup"><span data-stu-id="911ee-115">In the left navigation bar, click **Clients**, and then click the **Client Version Configuration** navigation button.</span></span>

4.  <span data-ttu-id="911ee-116">En la página Configuración de la **versión del cliente** , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="911ee-116">On the **Client Version Configuration** page, do the following:</span></span>
    
      - <span data-ttu-id="911ee-117">Para crear una nueva configuración, haga clic en **nuevo**, seleccione un sitio, haga clic en **Aceptar** nombre y actualice la configuración.</span><span class="sxs-lookup"><span data-stu-id="911ee-117">To create a new configuration, click **New**, select a site, click **OK** name, and update the settings.</span></span>
    
      - <span data-ttu-id="911ee-118">Para modificar una configuración, seleccione la configuración, haga clic en **Editar**, haga clic en **Mostrar detalles** y realice cambios en la configuración.</span><span class="sxs-lookup"><span data-stu-id="911ee-118">To modify a configuration, select the configuration, click **Edit**, click **Show details**, and make changes to the settings.</span></span>

</div>

<div>

## <a name="creating-or-modifying-client-version-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="911ee-119">Crear o modificar la configuración de la versión de cliente mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="911ee-119">Creating or Modifying Client Version Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="911ee-120">Puede crear parámetros de configuración de la versión de cliente con el cmdlet **New-CsClientVersionConfiguration** y modificarlos mediante el cmdlet **set-CsClientVersionConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="911ee-120">You can create client version configuration settings by using the **New-CsClientVersionConfiguration** cmdlet, and modify them by using the **Set-CsClientVersionConfiguration** cmdlet.</span></span> <span data-ttu-id="911ee-121">Estos cmdlets se pueden ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="911ee-121">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="911ee-122">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="911ee-122">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-collection-of-client-version-configuration-settings"></a><span data-ttu-id="911ee-123">Para crear una nueva colección de parámetros de configuración de la versión de cliente</span><span class="sxs-lookup"><span data-stu-id="911ee-123">To create a new collection of client version configuration settings</span></span>

  - <span data-ttu-id="911ee-124">El siguiente comando crea una nueva colección de parámetros de configuración de la versión de cliente que se aplican al sitio de Redmond.</span><span class="sxs-lookup"><span data-stu-id="911ee-124">The following command creates a new collection of client version configuration settings applied to the Redmond site.</span></span> <span data-ttu-id="911ee-125">En este ejemplo, el control de versiones del cliente está deshabilitado para el sitio de Redmond.</span><span class="sxs-lookup"><span data-stu-id="911ee-125">In this example, client versioning is disabled for the Redmond site.</span></span>
    
        New-CsClientVersionConfiguration -Identity "site:Redmond" -Enabled $False

</div>

<div>

## <a name="to-enable-client-versioning-for-a-site"></a><span data-ttu-id="911ee-126">Para habilitar el control de versiones de cliente en un sitio</span><span class="sxs-lookup"><span data-stu-id="911ee-126">To enable client versioning for a site</span></span>

  - <span data-ttu-id="911ee-127">Este comando habilita el control de versiones de cliente para el sitio de Redmond.</span><span class="sxs-lookup"><span data-stu-id="911ee-127">This command enables client versioning for the Redmond site.</span></span>
    
        Set-CsClientVersionConfiguration -Identity "site:Redmond" -Enabled $True

</div>

<div>

## <a name="to-disable-client-versioning-throughout-the-organization"></a><span data-ttu-id="911ee-128">Para deshabilitar el control de versiones de cliente en toda la organización</span><span class="sxs-lookup"><span data-stu-id="911ee-128">To disable client versioning throughout the organization</span></span>

  - <span data-ttu-id="911ee-129">En este ejemplo, el control de versiones de cliente está deshabilitado para todas las opciones de configuración de la versión de cliente en uso en la organización.</span><span class="sxs-lookup"><span data-stu-id="911ee-129">In this example, client versioning is disabled for all the client version configuration settings in use in the organization.</span></span>
    
        Get-CsClientVersionConfiguration | Set-CsClientVersionConfiguration  -Enabled $False

</div>

<span data-ttu-id="911ee-130">Para obtener más información, vea el tema de ayuda sobre los cmdlets [New-CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg399029(v=OCS.15)) y [set-CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg398623(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="911ee-130">For details, see the Help topic for the [New-CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg399029(v=OCS.15)) and [Set-CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg398623(v=OCS.15)) cmdlets.</span></span>

<span data-ttu-id="911ee-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="911ee-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

