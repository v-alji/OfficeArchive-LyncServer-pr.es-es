---
title: 'Lync Server 2013: crear un filtro de transferencia de archivos para un sitio específico'
description: 'Lync Server 2013: crear un filtro de transferencia de archivos para un sitio específico.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a new file transfer filter for a specific site
ms:assetid: d0006487-5217-491c-b730-e6c551cd9825
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182589(v=OCS.15)
ms:contentKeyID: 48185577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d3b5003711c2f2e74b726809fba5da6d9fd0aa57
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432173"
---
# <a name="create-a-new-file-transfer-filter-in-lync-server-2013-for-a-specific-site"></a><span data-ttu-id="9c7c5-103">Crear un filtro de transferencia de archivos nuevo en Lync Server 2013 para un sitio específico</span><span class="sxs-lookup"><span data-stu-id="9c7c5-103">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c7c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c7c5-104">

<span> </span></span></span>

<span data-ttu-id="9c7c5-105">_**Última modificación del tema:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="9c7c5-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="9c7c5-106">Además de modificar el filtro global de transferencia de archivos, puede configurar filtros de transferencia de archivos personalizados para sitios específicos dentro de la implementación de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-106">In addition to modifying the global file transfer filter, you can configure custom file transfer filters for specific sites within your Lync Server 2013 deployment.</span></span> <span data-ttu-id="9c7c5-107">Para más información sobre el filtrado de transferencia de archivos, vea [configuración de la transferencia de archivos y filtrado de URL para mensajería instantánea (mi) en Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span><span class="sxs-lookup"><span data-stu-id="9c7c5-107">For details about file transfer filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="to-create-a-file-transfer-filter-for-a-specific-site"></a><span data-ttu-id="9c7c5-108">Para crear un filtro de transferencia de archivos para un sitio específico</span><span class="sxs-lookup"><span data-stu-id="9c7c5-108">To create a file transfer filter for a specific site</span></span>

1.  <span data-ttu-id="9c7c5-109">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9c7c5-110">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9c7c5-111">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9c7c5-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9c7c5-112">En la barra de navegación izquierda, haga clic en **mensajería instantánea y presencia** y, a continuación, haga clic en **filtro de archivos**.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-112">In the left navigation bar, click **IM and Presence** and then click **File Filter**.</span></span>

4.  <span data-ttu-id="9c7c5-113">En la página **filtro de archivos** , haga clic en **nuevo**.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-113">On the **File Filter** page, click **New**.</span></span>

5.  <span data-ttu-id="9c7c5-114">En el cuadro de diálogo **seleccionar un sitio** , haga clic en el sitio para el que desea crear el filtro de transferencia de archivos y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-114">In the **Select a Site** dialog box, click the site for which you want to create the file transfer filter, and then click **OK**.</span></span>

6.  <span data-ttu-id="9c7c5-115">En **filtro de archivo nuevo**, haga clic en la casilla de verificación **Habilitar filtro de archivos** .</span><span class="sxs-lookup"><span data-stu-id="9c7c5-115">In **New File Filter**, click the **Enable file filter** check box.</span></span>

7.  <span data-ttu-id="9c7c5-116">En el cuadro de lista desplegable **transferencia de archivos** , haga clic en **bloquear todo** o **bloquear tipos de archivo específicos**.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-116">In **File transfer** drop-down list box, click **Block All** or **Block specific file types**.</span></span>

8.  <span data-ttu-id="9c7c5-117">Si hizo clic en **bloquear todo**, vaya al paso 10.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-117">If you clicked **Block All**, skip to step 10.</span></span>

9.  <span data-ttu-id="9c7c5-118">Si hizo clic en **bloquear tipos de archivo específicos**, siga este procedimiento:</span><span class="sxs-lookup"><span data-stu-id="9c7c5-118">If you clicked **Block specific file types**, do the following:</span></span>
    
    1.  <span data-ttu-id="9c7c5-119">Haga clic en **seleccionar** para modificar la lista predeterminada de extensiones de tipo de archivo que desea bloquear.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-119">Click **Select** to modify the default list of file type extensions that you want to block.</span></span>
    
    2.  <span data-ttu-id="9c7c5-120">En el cuadro de diálogo **Seleccionar tipo de archivo** , seleccione los tipos de archivo que desea bloquear o permitir agregando o quitando sus extensiones de las categorías de **extensiones de tipo de archivo**.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-120">In the **Select File Type** dialog box, select the file types that you want to block or allow by adding or removing their extensions from the categories under **File type extensions**.</span></span>
    
    3.  <span data-ttu-id="9c7c5-121">Si no ve la extensión de un tipo de archivo que desea bloquear, escriba la extensión en el cuadro de texto en **Agregar extensiones de tipo de archivo a la lista** y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-121">If you do not see the extension for a file type that you want to block, type the extension in the text box under **Add file type extensions to the list**, and then click **Add**.</span></span>
    
    4.  <span data-ttu-id="9c7c5-122">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-122">Click **OK**.</span></span>

10. <span data-ttu-id="9c7c5-123">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="9c7c5-123">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9c7c5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c7c5-124">See Also</span></span>


[<span data-ttu-id="9c7c5-125">Configuración de la transferencia de archivos y el filtrado de URL para mensajería instantánea (mi) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c7c5-125">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="9c7c5-126">Crear un filtro de dirección URL en Lync Server 2013 para administrar hipervínculos en conversaciones de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="9c7c5-126">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)  
[<span data-ttu-id="9c7c5-127">Modificar el filtro de transferencia de archivos predeterminado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c7c5-127">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)  


[<span data-ttu-id="9c7c5-128">Modificar el filtro de dirección URL predeterminado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c7c5-128">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)  
  

<span data-ttu-id="9c7c5-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c7c5-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

