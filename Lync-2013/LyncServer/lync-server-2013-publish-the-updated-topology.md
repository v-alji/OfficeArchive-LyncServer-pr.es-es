---
title: 'Lync Server 2013: Publicar la topología actualizada'
description: 'Lync Server 2013: publicar la topología actualizada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the updated topology
ms:assetid: 59455dd1-6a9e-433f-a714-d3636c068100
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204910(v=OCS.15)
ms:contentKeyID: 48184203
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c27cca2eae86eadaf1ff37e2c3520eaec3f86c98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399048"
---
# <a name="publish-the-updated-topology-in-lync-server-2013"></a><span data-ttu-id="3f56d-103">Publicar la topología actualizada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f56d-103">Publish the updated topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f56d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f56d-104">

<span> </span></span></span>

<span data-ttu-id="3f56d-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="3f56d-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="3f56d-106">Después de actualizar su topología en el generador de topología, debe publicarla en el almacén de administración central para poder configurar y usar el servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="3f56d-106">After updating your topology in Topology Builder, you must publish the topology to the Central Management store before you can configure and use Persistent Chat Server.</span></span> <span data-ttu-id="3f56d-107">Las copias de solo lectura de los datos se replican en todos los servidores de la topología para mantener todos los servidores sincronizados con los cambios en la topología y en otras opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="3f56d-107">Read-only copies of the data are replicated to all servers in the topology to keep all servers in sync with topology and other configuration changes.</span></span>

<div>

## <a name="to-publish-an-updated-topology"></a><span data-ttu-id="3f56d-108">Para publicar una topología actualizada</span><span class="sxs-lookup"><span data-stu-id="3f56d-108">To publish an updated topology</span></span>

<span data-ttu-id="3f56d-109">Antes de publicar su topología, instale las bases de datos para el servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="3f56d-109">Before you publish your topology, install the databases for Persistent Chat Server.</span></span> <span data-ttu-id="3f56d-110">Use el generador de topología para instalar bases de datos seleccionando **acción** e **instalar base de datos**.</span><span class="sxs-lookup"><span data-stu-id="3f56d-110">Use Topology Builder to install databases by selecting **Action** and **Install Database**.</span></span>

1.  <span data-ttu-id="3f56d-111">En un equipo que ejecute Lync Server 2013 o en el que estén instaladas las herramientas administrativas de Lync Server, inicie sesión con una cuenta que sea miembro del grupo **administradores de dominio** y el grupo **RTCUniversalServerAdmins** . y que tiene permisos de control total (es decir, leer, escribir y modificar) en el almacén de archivos para usarlos en el almacén de archivos del servidor de chat persistente (para que el generador de topología pueda configurar las listas de control de acceso discrecional (DACL) obligatorias) o una cuenta con derechos de usuario equivalentes.</span><span class="sxs-lookup"><span data-stu-id="3f56d-111">On a computer that is running Lync Server 2013 or on which the Lync Server administrative tools are installed, log on using an account that is a member of both the **Domain Admins** group and the **RTCUniversalServerAdmins** group, and that has full control permissions (that is, read, write, and modify) on the file store to be used for the Persistent Chat Server file store (so that Topology Builder can configure the required discretionary access control lists (DACLs)), or an account with equivalent user rights.</span></span>

2.  <span data-ttu-id="3f56d-112">Iniciar el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="3f56d-112">Start Topology Builder.</span></span> <span data-ttu-id="3f56d-113">Seleccione **Descargar topología de una implementación existente** o **abra topología desde un archivo local** si la ha guardado de forma local.</span><span class="sxs-lookup"><span data-stu-id="3f56d-113">Select **Download Topology from existing deployment**, or **Open Topology from a local file** if you saved it locally.</span></span>

3.  <span data-ttu-id="3f56d-114">En el árbol de consola, haga clic con el botón secundario en **Lync Server 2013** y, a continuación, haga clic en **publicar topología**.</span><span class="sxs-lookup"><span data-stu-id="3f56d-114">In the console tree, right-click **Lync Server 2013**, and then click **Publish Topology**.</span></span>

4.  <span data-ttu-id="3f56d-115">En la página **Publicar la topología**, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3f56d-115">On the **Publish the topology** page, click **Next**.</span></span>

5.  <span data-ttu-id="3f56d-116">En la página **Asistente para publicación completado**, compruebe que se ha publicado correctamente la topología y, luego, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="3f56d-116">On the **Publishing wizard complete** page, verify that the topology was successfully published, and then click **Finish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="3f56d-117">Después de publicar la topología, debe configurar la compatibilidad con el servidor de chat persistente antes de que se pueda archivar contenido.</span><span class="sxs-lookup"><span data-stu-id="3f56d-117">After publishing the topology, you must configure support for Persistent Chat Server before any content can be archived.</span></span>

    
    <span data-ttu-id="3f56d-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f56d-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

