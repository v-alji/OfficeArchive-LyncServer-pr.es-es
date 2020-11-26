---
title: Modificar la acción predeterminada de los clientes que no se admiten o restringen explícitamente
description: Modificar la acción predeterminada para los clientes que no son explícitamente compatibles o restringidos.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the default action for clients not explicitly supported or restricted
ms:assetid: 548dd0f5-62fe-4c3f-8952-2b9fd4c5fff3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520994(v=OCS.15)
ms:contentKeyID: 48184137
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2c28ad4d357953c22f889309323ccbb95c6840e2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445739"
---
# <a name="modify-the-default-action-for-clients-not-explicitly-supported-or-restricted-in-lync-server-2013"></a><span data-ttu-id="3fc83-103">Modificar la acción predeterminada de los clientes que no se admiten explícitamente o restringen en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fc83-103">Modify the default action for clients not explicitly supported or restricted in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3fc83-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3fc83-104">

<span> </span></span></span>

<span data-ttu-id="3fc83-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="3fc83-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="3fc83-106">Además de especificar la versión de clientes que desea admitir en su entorno de Lync Server 2013, también puede especificar una acción predeterminada para los clientes que aún no tienen definida una directiva de versión.</span><span class="sxs-lookup"><span data-stu-id="3fc83-106">In addition to specifying the version of clients that you want to support in your Lync Server 2013 environment, you can also specify a default action for clients that do not already have a version policy defined.</span></span> <span data-ttu-id="3fc83-107">Esto le permite restringir las versiones de cliente que se usan en su entorno de Lync Server, lo que puede ayudarle a controlar los costos asociados con la compatibilidad de varias versiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="3fc83-107">This enables you to restrict which client versions are used in your Lync Server environment, which can help you control the costs associated with supporting multiple client versions.</span></span>

<div>

## <a name="to-modify-the-default-action-for-clients-not-explicitly-supported-or-restricted"></a><span data-ttu-id="3fc83-108">Para modificar la acción predeterminada para los clientes que no son explícitamente compatibles o restringidos</span><span class="sxs-lookup"><span data-stu-id="3fc83-108">To modify the default action for clients not explicitly supported or restricted</span></span>

1.  <span data-ttu-id="3fc83-109">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="3fc83-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="3fc83-110">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3fc83-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3fc83-111">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3fc83-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3fc83-112">En la barra de navegación izquierda, haga clic en **clientes** y, después, en **configuración de versión de cliente**.</span><span class="sxs-lookup"><span data-stu-id="3fc83-112">In the left navigation bar, click **Clients**, and then click **Client Version Configuration**.</span></span>

4.  <span data-ttu-id="3fc83-113">En la página Configuración de la **versión del cliente** , haga doble clic en la configuración **global** de la lista.</span><span class="sxs-lookup"><span data-stu-id="3fc83-113">On the **Client Version Configuration** page, double-click the **Global** configuration in the list.</span></span>

5.  <span data-ttu-id="3fc83-114">En el cuadro de diálogo **Editar configuración** de la versión del cliente, compruebe que la casilla de verificación **Habilitar control de versiones** está seleccionada y, a continuación, en **acción predeterminada**, seleccione una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="3fc83-114">In the **Edit Client Version Configuration** dialog box, verify that the **Enable version control** check box is selected and then, under **Default action**, select one of the following:</span></span>
    
      - <span data-ttu-id="3fc83-115">**Permitir**   Permite al cliente iniciar sesión si la versión del cliente no coincide con ningún filtro de la lista de **directivas de versión del cliente** .</span><span class="sxs-lookup"><span data-stu-id="3fc83-115">**Allow**   Allows the client to log on if the client version does not match any filter in the **Client version policies** list.</span></span>
    
      - <span data-ttu-id="3fc83-116">**Bloquear**   Impide que el cliente inicie sesión si la versión del cliente no coincide con ningún filtro de la lista de **directivas de versión del cliente** .</span><span class="sxs-lookup"><span data-stu-id="3fc83-116">**Block**   Prevents the client from logging on if the client version does not match any filter in the **Client version policies** list.</span></span>
    
      - <span data-ttu-id="3fc83-117">**Bloque con dirección URL**   Impide que el cliente inicie sesión si la versión del cliente no coincide con ningún filtro de la lista de **directivas de versión del cliente** e incluye un mensaje de error que contiene una dirección URL donde se puede descargar un cliente más reciente.</span><span class="sxs-lookup"><span data-stu-id="3fc83-117">**Block with URL**   Prevents the client from logging on if the client version does not match any filter in the **Client version policies** list, and include an error message containing a URL where a newer client can be downloaded.</span></span>
    
      - <span data-ttu-id="3fc83-118">**Permitir con URL**   Permite al cliente iniciar sesión si la versión del cliente no coincide con ningún filtro de la lista de **directivas de versión del cliente** e incluye un mensaje de error que contenga una dirección URL donde se pueda descargar un cliente más reciente.</span><span class="sxs-lookup"><span data-stu-id="3fc83-118">**Allow with URL**   Allows the client to log on if the client version does not match any filter in the **Client version policies** list, and include an error message containing a URL where a newer client can be downloaded.</span></span>

6.  <span data-ttu-id="3fc83-119">Si seleccionó **bloquear con URL**, escriba la dirección URL de descarga del cliente que desea incluir en el mensaje de error en el cuadro **dirección URL** .</span><span class="sxs-lookup"><span data-stu-id="3fc83-119">If you selected **Block with URL**, type the client download URL to include in the error message in the **URL** box.</span></span>

7.  <span data-ttu-id="3fc83-120">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="3fc83-120">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-disable-client-version-control"></a><span data-ttu-id="3fc83-121">Para deshabilitar el control de versiones del cliente</span><span class="sxs-lookup"><span data-stu-id="3fc83-121">To disable client version control</span></span>

  - <span data-ttu-id="3fc83-122">Para deshabilitar el control de versiones y permitir que todos los clientes inicien sesión independientemente de la versión del cliente, desactive la casilla **Habilitar control de versiones** y, a continuación, haga clic en **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="3fc83-122">To disable version control to allow all clients to log on regardless of the client version, clear the **Enable version control** check box, and then click **Commit**.</span></span>

</div>

<div>

## <a name="modifying-the-default-action-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="3fc83-123">Modificar la acción predeterminada mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3fc83-123">Modifying the Default Action by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="3fc83-124">La acción predeterminada que hay que realizar cuando los usuarios intentan iniciar sesión con clientes que no son explícitamente compatibles o restringidos por una directiva de versión de cliente se pueden administrar mediante la interfaz de línea de comandos de Windows PowerShell y el cmdlet **set-CsClientVersionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="3fc83-124">The default action to be taken when users try to sign on using clients that are not explicitly supported or restricted by a client version policy can be managed by using Windows PowerShell command-line interface and the **Set-CsClientVersionPolicy** cmdlet.</span></span> <span data-ttu-id="3fc83-125">Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3fc83-125">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="3fc83-126">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="3fc83-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-configure-the-default-action-to-block-access"></a><span data-ttu-id="3fc83-127">Para configurar la acción predeterminada para bloquear el acceso</span><span class="sxs-lookup"><span data-stu-id="3fc83-127">To configure the default action to block access</span></span>

  - <span data-ttu-id="3fc83-128">El siguiente comando establece la acción predeterminada para el bloque de sitio de Redmond.</span><span class="sxs-lookup"><span data-stu-id="3fc83-128">The following command sets the default action for the Redmond site Block.</span></span> <span data-ttu-id="3fc83-129">Esto bloqueará el registro de cualquier cliente para el que no exista ninguna regla de configuración de versión de cliente.</span><span class="sxs-lookup"><span data-stu-id="3fc83-129">This will block registration for any client for which no client version configuration rule exists.</span></span>
    
        Set-CsClientVersionConfiguration -Identity "site:Redmond" -DefaultAction Block

</div>

<div>

## <a name="to-configure-the-default-action-to-allow-access"></a><span data-ttu-id="3fc83-130">Para configurar la acción predeterminada para permitir el acceso</span><span class="sxs-lookup"><span data-stu-id="3fc83-130">To configure the default action to allow access</span></span>

  - <span data-ttu-id="3fc83-131">En este ejemplo, la acción predeterminada para el sitio de Redmond es permitir.</span><span class="sxs-lookup"><span data-stu-id="3fc83-131">In this example, the default action for the Redmond site is set to Allow.</span></span> <span data-ttu-id="3fc83-132">Esto permitirá el registro de cualquier cliente para el que no exista ninguna regla de configuración de la versión de cliente.</span><span class="sxs-lookup"><span data-stu-id="3fc83-132">This will allow registration for any client for which no client version configuration rule exists.</span></span>
    
        Set-CsClientVersionConfiguration -Identity "site:Redmond" -DefaultAction Allow

</div>

<span data-ttu-id="3fc83-133">Para obtener más información, vea el tema de ayuda sobre el cmdlet [set-CsClientVersionPolicy](https://technet.microsoft.com/library/Gg398876(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="3fc83-133">For details, see the Help topic for the [Set-CsClientVersionPolicy](https://technet.microsoft.com/library/Gg398876(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3fc83-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fc83-134">See Also</span></span>


[<span data-ttu-id="3fc83-135">Administrar dispositivos, teléfonos y aplicaciones cliente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fc83-135">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="3fc83-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3fc83-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

