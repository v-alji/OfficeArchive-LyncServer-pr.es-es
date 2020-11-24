---
title: 'Lync Server 2013: Configurar el almacenamiento de archivos'
description: 'Lync Server 2013: configurar el almacenamiento de archivos DFS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DFS file storage
ms:assetid: a985be20-5a00-4f38-b45b-83dc82de3827
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205150(v=OCS.15)
ms:contentKeyID: 48185037
ms.date: 05/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d70ae93db188ec51d04dd33d6c3cb5659db5a2c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399935"
---
# <a name="configure-dfs-file-storage-for-lync-server-2013"></a><span data-ttu-id="51942-103">Configurar el almacenamiento de archivos para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51942-103">Configure DFS file storage for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="51942-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="51942-104">

<span> </span></span></span>

<span data-ttu-id="51942-105">_**Última modificación del tema:** 2016-05-23_</span><span class="sxs-lookup"><span data-stu-id="51942-105">_**Topic Last Modified:** 2016-05-23_</span></span>

<span data-ttu-id="51942-106">Lync Server 2013 admite el uso de recursos compartidos de archivos en un sistema de archivos distribuido (DFS).</span><span class="sxs-lookup"><span data-stu-id="51942-106">Lync Server 2013 supports using file shares on a Distributed File System (DFS).</span></span> <span data-ttu-id="51942-107">Para obtener más información sobre DFS para Windows Server 2008, consulte la guía paso a paso de DFS para Windows Server 2008 en [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835) . Para usar un DFS, Lync Server 2013 requiere lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="51942-107">For details about DFS for Windows Server 2008, see the DFS Step-by-Step Guide for Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835).To use a DFS, Lync Server 2013 requires the following:</span></span>

  - <span data-ttu-id="51942-108">Los espacios de nombres se basan en dominios</span><span class="sxs-lookup"><span data-stu-id="51942-108">Namespaces are domain based</span></span>

  - <span data-ttu-id="51942-109">Todos los servidores de espacio de nombres se ejecutan con un mínimo de Windows 2008</span><span class="sxs-lookup"><span data-stu-id="51942-109">All namespace servers are running a minimum of Windows 2008</span></span>

<span data-ttu-id="51942-110">El programa de instalación de Lync Server 2013 requiere que los permisos para la carpeta compartida permitan el acceso total al administrador.</span><span class="sxs-lookup"><span data-stu-id="51942-110">Lync Server 2013 setup requires that permissions on shared folder allow full access to Administrator.</span></span> <span data-ttu-id="51942-111">Lync Server 2013 usará permisos de archivo NTFS para las ACL de las carpetas.</span><span class="sxs-lookup"><span data-stu-id="51942-111">Lync Server 2013 will then use NTFS file permissions to ACL the folders.</span></span> <span data-ttu-id="51942-112">Los permisos de recursos compartidos DFS heredados no se usarán para restringir el acceso.</span><span class="sxs-lookup"><span data-stu-id="51942-112">Inherited DFS share permissions will not be used to restrict access.</span></span>

<span data-ttu-id="51942-113">Para obtener más información sobre los requisitos de uso compartido de archivos, consulte [compatibilidad de almacenamiento de archivos en Lync Server 2013](lync-server-2013-file-storage-support.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="51942-113">For more details about File Share requirements, see [File storage support in Lync Server 2013](lync-server-2013-file-storage-support.md) in the Supportability documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="51942-114">Es posible que esté buscando información sobre cómo configurar un recurso compartido no DFS.</span><span class="sxs-lookup"><span data-stu-id="51942-114">You may be looking for information on configuring a non-DFS share.</span></span> <span data-ttu-id="51942-115">Si es así, consulte <A href="lync-server-2013-hardware-setup.md">configuración de hardware para Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="51942-115">If so, check out <A href="lync-server-2013-hardware-setup.md">Hardware setup for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="51942-116">El procedimiento siguiente describe cómo configurar correctamente los permisos de carpetas compartidas mediante el Asistente para espacio de nombres DFS (como se describe en la guía de configuración de DFS).</span><span class="sxs-lookup"><span data-stu-id="51942-116">The following procedure describes how to correctly configure shared folder permissions using the DFS Namespace Wizard (as described in DFS setup guide).</span></span>

<div>

## <a name="to-configure-shared-folder-permissions"></a><span data-ttu-id="51942-117">Para configurar permisos de carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="51942-117">To configure shared folder permissions</span></span>

1.  <span data-ttu-id="51942-118">Haga clic en **Inicio**, elija **todos los programas**, seleccione **herramientas administrativas** y, a continuación, haga clic en **Administración de DFS**.</span><span class="sxs-lookup"><span data-stu-id="51942-118">Click **Start**, point to **All Programs**, point to **Administrative Tools**, and then click **DFS Management**.</span></span>

2.  <span data-ttu-id="51942-119">En el árbol de consola del complemento Administración de DFS, haga clic con el botón secundario en el servidor de espacio de nombres (por ejemplo, filesrv1.contoso.com) y, a continuación, haga clic en **Editar configuración**.</span><span class="sxs-lookup"><span data-stu-id="51942-119">In the console tree of the DFS Management snap-in, right-click the namespace server (for example filesrv1.contoso.com), and then click **Edit Settings**.</span></span>

3.  <span data-ttu-id="51942-120">Seleccione **permisos de carpetas compartidas**.</span><span class="sxs-lookup"><span data-stu-id="51942-120">Select **Shared Folder Permissions**.</span></span>

4.  <span data-ttu-id="51942-121">Seleccione **usar permisos personalizados**.</span><span class="sxs-lookup"><span data-stu-id="51942-121">Select **Use Custom Permissions**.</span></span>

5.  <span data-ttu-id="51942-122">En el grupo administrador, seleccione las siguientes opciones en **permitir**:</span><span class="sxs-lookup"><span data-stu-id="51942-122">For the Administrator group, select the following under **Allow**:</span></span>
    
      - <span data-ttu-id="51942-123">**Control total**</span><span class="sxs-lookup"><span data-stu-id="51942-123">**Full Control**</span></span>
    
      - <span data-ttu-id="51942-124">**Cambio**</span><span class="sxs-lookup"><span data-stu-id="51942-124">**Change**</span></span>
    
      - <span data-ttu-id="51942-125">**Consulte**</span><span class="sxs-lookup"><span data-stu-id="51942-125">**Read**</span></span>

6.  <span data-ttu-id="51942-126">Haga clic en **aplicar** y, a continuación, en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="51942-126">Click **Apply**, and then click **OK**.</span></span>

<span data-ttu-id="51942-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="51942-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

