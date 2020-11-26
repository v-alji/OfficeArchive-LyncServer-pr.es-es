---
title: 'Lync Server 2013: Configurar los nombres de dominio completos (FQDN) de la granja de servidores web'
description: 'Lync Server 2013: configurar FQDN de granja de servidores Web.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure web farm FQDNs
ms:assetid: cb25dbbd-dcea-4997-8e14-e5007dd7d3ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429722(v=OCS.15)
ms:contentKeyID: 48185481
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8a07faac4d4809ffe10e7ca3699e7441e6dbcb7b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433552"
---
# <a name="configure-web-farm-fqdns-for-lync-server-2013"></a><span data-ttu-id="2e07a-103">Configurar los nombres de dominio completos (FQDN) de la granja de servidores web para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e07a-103">Configure web farm FQDNs for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2e07a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2e07a-104">

<span> </span></span></span>

<span data-ttu-id="2e07a-105">_**Última modificación del tema:** 2013-03-29_</span><span class="sxs-lookup"><span data-stu-id="2e07a-105">_**Topic Last Modified:** 2013-03-29_</span></span>

<span data-ttu-id="2e07a-106">Al definir la configuración del servidor Standard Edition, el grupo de servidores front-end, el director o el grupo de directores en el generador de topología, se configura un nombre de dominio completo (FQDN) de servicios web externos.</span><span class="sxs-lookup"><span data-stu-id="2e07a-106">When you defined the configuration of the Standard Edition server, Front End pool, Director or Director pool in Topology Builder, you configure an external web services fully qualified domain name (FQDN).</span></span> <span data-ttu-id="2e07a-107">Durante el proceso de inicio de sesión de un cliente alojado en el servidor Standard Edition o en el grupo front-end, los FQDN de los servicios web configurados se envían por medio de aprovisionamiento en banda.</span><span class="sxs-lookup"><span data-stu-id="2e07a-107">During the log on process of a client homed in the Standard Edition server or Front End pool, the configured web services FQDNs are sent by way of in-band provisioning.</span></span> <span data-ttu-id="2e07a-108">Si necesita agregar o cambiar la dirección URL de los servicios web externos, use el generador de topología para configurar o volver a configurar la configuración de los servicios Web mediante el procedimiento de este tema.</span><span class="sxs-lookup"><span data-stu-id="2e07a-108">If you need to add or change the external web services URL, you use Topology Builder to configure or reconfigure the web services configuration using the procedure in this topic.</span></span>

<div>

## <a name="to-configure-an-external-pool-fqdn-for-web-services"></a><span data-ttu-id="2e07a-109">Para configurar un FQDN de grupo externo para servicios Web</span><span class="sxs-lookup"><span data-stu-id="2e07a-109">To configure an external pool FQDN for web services</span></span>

1.  <span data-ttu-id="2e07a-110">Iniciar generador de topología: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **generador de topología de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="2e07a-110">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="2e07a-111">En el generador de topología, en el árbol de consola, en **front ends Standard Edition**, **servidores front-end Enterprise Edition**, y **directores**, haga clic con el botón secundario en el nombre del grupo que necesita editar y, a continuación, haga clic en **Editar propiedades**.</span><span class="sxs-lookup"><span data-stu-id="2e07a-111">In Topology Builder, in the console tree under **Standard Edition Front Ends**, **Enterprise Edition Front Ends**, and **Directors**, right-click the pool name that you need to edit, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="2e07a-112">En la sección **servicios web** , agregue o edite el **FQDN de servicios web externos**.</span><span class="sxs-lookup"><span data-stu-id="2e07a-112">In the **Web services** section, add or edit the **External web services FQDN**.</span></span>

4.  <span data-ttu-id="2e07a-113">Revise y ajuste los **puertos de escucha** para http y https.</span><span class="sxs-lookup"><span data-stu-id="2e07a-113">Review and adjust the **Listening ports** for both HTTP and HTTPS.</span></span> <span data-ttu-id="2e07a-114">Los valores predeterminados son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2e07a-114">The defaults will be:</span></span>
    
      - <span data-ttu-id="2e07a-115">**Puertos de escucha:** HTTP 8080, HTTPS 4443</span><span class="sxs-lookup"><span data-stu-id="2e07a-115">**Listening ports:** HTTP 8080, HTTPS 4443</span></span>
    
      - <span data-ttu-id="2e07a-116">**Puertos publicados:** HTTP 80, HTTPS 443</span><span class="sxs-lookup"><span data-stu-id="2e07a-116">**Published ports:** HTTP 80, HTTPS 443</span></span>
    
    <span data-ttu-id="2e07a-117">Donde los **puertos de escucha** son el puerto en el que los servicios web externos se configurarán para recibir solicitudes del proxy inverso, y los **puertos publicados** son los puertos publicados externamente por el proxy inverso y se comunican a los clientes durante el aprovisionamiento en banda.</span><span class="sxs-lookup"><span data-stu-id="2e07a-117">Where the **Listening ports** is the port that the external web services will be configured to receive requests from the reverse proxy, and the **Published ports** is the ports that are published externally by the reverse proxy and is communicated to clients during in-band provisioning.</span></span>

5.  <span data-ttu-id="2e07a-118">Cuando haya completado las adiciones y actualizaciones, haga clic en **Aceptar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="2e07a-118">When you have completed your additions and updates, click **OK** to continue.</span></span>

6.  <span data-ttu-id="2e07a-119">Haga clic con el botón secundario en **Lync Server 2013** y, a continuación, haga clic en **publicar**.</span><span class="sxs-lookup"><span data-stu-id="2e07a-119">Right-click **Lync Server 2013**, and then click **Publish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="2e07a-120">Después de la publicación, se puede presentar un vínculo que le informará de que hay pasos adicionales que es necesario realizar.</span><span class="sxs-lookup"><span data-stu-id="2e07a-120">After publishing successfully completes, a link may be presented that informs you that there are additional steps that need to be taken.</span></span> <span data-ttu-id="2e07a-121">Si se hace clic en el vínculo, se abre una lista de servidores afectados por los cambios realizados en el generador de topología que requerirán volver a ejecutar el Asistente para la implementación de Lync Server en cada servidor de la lista para actualizar la configuración de los componentes agregados, eliminados o modificados.</span><span class="sxs-lookup"><span data-stu-id="2e07a-121">The link, if clicked, opens a list of servers affected by the changes made in Topology Builder that will require you to re-run the Lync Server Deployment Wizard on each listed server to update the configuration for added, removed, or changed components.</span></span>

    
    </div>

7.  <span data-ttu-id="2e07a-122">Repita estos pasos para cada servidor Standard Edition, grupo de servidores front-end, director o grupo de directores de la organización.</span><span class="sxs-lookup"><span data-stu-id="2e07a-122">Repeat these steps for each Standard Edition server, Front End pool, Director or Director pool in the organization.</span></span>

<span data-ttu-id="2e07a-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2e07a-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

