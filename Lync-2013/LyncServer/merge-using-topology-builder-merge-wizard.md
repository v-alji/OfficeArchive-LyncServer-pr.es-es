---
title: Combinar mediante el Asistente para combinar generador de topología
description: Combinar mediante el Asistente para combinar generador de topología.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Merge using Topology Builder Merge wizard
ms:assetid: c3f3c425-dab6-4dcd-bf0e-d7fde05f2ebf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205243(v=OCS.15)
ms:contentKeyID: 48185343
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d71a63eef95e3e36802dedfa9fbc1a173d283b65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446958"
---
# <a name="merge-using-topology-builder-merge-wizard"></a><span data-ttu-id="a6185-103">Combinar mediante el Asistente para combinar generador de topología</span><span class="sxs-lookup"><span data-stu-id="a6185-103">Merge using Topology Builder Merge wizard</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6185-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6185-104">

<span> </span></span></span>

<span data-ttu-id="a6185-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="a6185-105">_**Topic Last Modified:** 2012-10-02_</span></span>

1.  <span data-ttu-id="a6185-106">Descargue la implementación existente con el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="a6185-106">Download the existing deployment using Topology Builder.</span></span>

2.  <span data-ttu-id="a6185-107">En el menú **acción** , seleccione **combinar Office Communications Server 2007 R2**.</span><span class="sxs-lookup"><span data-stu-id="a6185-107">From the **Action** menu, select **Merge Office Communications Server 2007 R2**.</span></span>

3.  <span data-ttu-id="a6185-108">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a6185-108">Click **Next**.</span></span>

4.  <span data-ttu-id="a6185-109">En **especificar configuración perimetral**, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="a6185-109">In **Specify Edge Setup**, click **Add**.</span></span>
    
    <span data-ttu-id="a6185-110">![Asistente para combinar topología, especificar página de configuración de Edge](images/JJ205243.cdca609d-d4d5-47d9-9ff8-8b1daa4106e1(OCS.15).jpg "Asistente para combinar topología, especificar página de configuración de Edge")</span><span class="sxs-lookup"><span data-stu-id="a6185-110">![Merge Topology Wizard, Specify Edge Setup page](images/JJ205243.cdca609d-d4d5-47d9-9ff8-8b1daa4106e1(OCS.15).jpg "Merge Topology Wizard, Specify Edge Setup page")</span></span>  

5.  <span data-ttu-id="a6185-111">En **especificar tipo de borde**, escriba el tipo de configuración del servidor perimetral y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a6185-111">In **Specify Edge Type**, enter the type of Edge Server configuration, and then click **Next**.</span></span> <span data-ttu-id="a6185-112">En este ejemplo se usa la opción de **servidor de borde único** .</span><span class="sxs-lookup"><span data-stu-id="a6185-112">This example uses the **Single Edge Server** option.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="a6185-113">La <STRONG>implementación de bordes expandida</STRONG> no es una configuración admitida.</span><span class="sxs-lookup"><span data-stu-id="a6185-113"><STRONG>Expanded Edge deployment</STRONG> is not a supported configuration.</span></span> <span data-ttu-id="a6185-114">Un <STRONG>servidor perimetral expandido</STRONG> debe convertirse primero en un <STRONG>único servidor perimetral</STRONG> o en un servidor <STRONG>perimetral consolidado de carga equilibrada</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="a6185-114">An <STRONG>Expanded Edge Server</STRONG> must first be converted to a <STRONG>Single Edge Server</STRONG> or a <STRONG>Load-balanced consolidated Edge</STRONG> Server.</span></span>

    
    </div>

6.  <span data-ttu-id="a6185-115">En **especificar la configuración de borde interno** , escriba la información relevante para el FQDN y los puertos internos del grupo de límites según sea necesario y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a6185-115">In **Specify Internal Edge Settings** , enter the relevant information for your Edge pool’s internal FQDN and ports as needed, and then click **Next**.</span></span>
    
    <span data-ttu-id="a6185-116">![Especificar el cuadro de diálogo Configuración de borde interno](images/JJ205243.dd664761-839c-4ac8-bd1a-5525589dfbb0(OCS.15).jpg "Especificar el cuadro de diálogo Configuración de borde interno")</span><span class="sxs-lookup"><span data-stu-id="a6185-116">![Specify Internal Edge Settings dialog](images/JJ205243.dd664761-839c-4ac8-bd1a-5525589dfbb0(OCS.15).jpg "Specify Internal Edge Settings dialog")</span></span>  

7.  <span data-ttu-id="a6185-117">En **especificar borde externo**, escriba la información de FQDN de conferencias web para su servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="a6185-117">In **Specify External Edge**, enter the web conferencing FQDN information for your Edge Server.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="a6185-118">Antes de hacer clic en <STRONG>siguiente</STRONG>, siga el paso siguiente de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="a6185-118">Before you click <STRONG>Next</STRONG>, do the next step in this procedure.</span></span> <span data-ttu-id="a6185-119">Es muy importante que no pierdas este paso.</span><span class="sxs-lookup"><span data-stu-id="a6185-119">It is very important that you do not miss this step.</span></span>

    
    </div>

8.  <span data-ttu-id="a6185-120">Active la casilla **este grupo de bordes se usa para la Federación y conectividad de mensajería instantánea pública** si planea usar el servidor perimetral de Office Communications Server 2007 R2 heredado para la Federación.</span><span class="sxs-lookup"><span data-stu-id="a6185-120">Check the **This Edge pool is used for federation and public IM connectivity** check box if you plan to use the legacy Office Communications Server 2007 R2 Edge Server for federation.</span></span> <span data-ttu-id="a6185-121">Si tiene varios servidores perimetrales implementados, solo uno de ellos estará habilitado para la Federación.</span><span class="sxs-lookup"><span data-stu-id="a6185-121">If you have multiple Edge Servers deployed, only one of them will be enabled for federation.</span></span> <span data-ttu-id="a6185-122">Si no activa esta casilla y decide más tarde que desea habilitar la Federación, debe ejecutar el Asistente para la combinación del generador de topología y volver a publicar su topología.</span><span class="sxs-lookup"><span data-stu-id="a6185-122">If you do not check this box and you decide later that you want to enable federation, you must run the Topology Builder Merge wizard and publish your topology again.</span></span>
    
    <span data-ttu-id="a6185-123">![Cuadro de diálogo servidor perimetral, especificar página de borde externo](images/JJ205243.32e97ce5-92f0-477e-8125-5d2ece237b13(OCS.15).jpg "Cuadro de diálogo servidor perimetral, especificar página de borde externo")</span><span class="sxs-lookup"><span data-stu-id="a6185-123">![Edge Server dialog, Specify External Edge page](images/JJ205243.32e97ce5-92f0-477e-8125-5d2ece237b13(OCS.15).jpg "Edge Server dialog, Specify External Edge page")</span></span>  

9.  <span data-ttu-id="a6185-124">En **especificar el siguiente salto**, escriba el nombre de dominio completo (FQDN) de la ubicación del próximo salto en su entorno.</span><span class="sxs-lookup"><span data-stu-id="a6185-124">In **Specify Next Hop**, enter the fully qualified domain name (FQDN) of the next hop location in your environment.</span></span> <span data-ttu-id="a6185-125">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="a6185-125">Click **Finish**.</span></span>
    
    <span data-ttu-id="a6185-126">![Cuadro de diálogo servidor perimetral, especificar página de próximo salto](images/JJ205243.e734ee0d-f91c-4f3f-8ae6-248ecabcf678(OCS.15).jpg "Cuadro de diálogo servidor perimetral, especificar página de próximo salto")</span><span class="sxs-lookup"><span data-stu-id="a6185-126">![Edge Server dialog, Specify Next Hop page](images/JJ205243.e734ee0d-f91c-4f3f-8ae6-248ecabcf678(OCS.15).jpg "Edge Server dialog, Specify Next Hop page")</span></span>  

10. <span data-ttu-id="a6185-127">En **especificar la configuración perimetral**, si se han agregado todos los servidores perimetrales de Office Communications Server 2007 R2, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a6185-127">In **Specify Edge Setup**, if all your Office Communications Server 2007 R2 Edge Servers have been added, click **Next**.</span></span> <span data-ttu-id="a6185-128">Si tiene más servidores perimetrales de Office Communications Server 2007 R2 para agregar, repita este procedimiento a partir del paso 4.</span><span class="sxs-lookup"><span data-stu-id="a6185-128">If you have more Office Communications Server 2007 R2 Edge Servers to add, repeat this procedure starting at step 4.</span></span>

11. <span data-ttu-id="a6185-129">En **especificar puerto SIP interno** , seleccione la configuración predeterminada (es decir, si no modificó el puerto SIP predeterminado).</span><span class="sxs-lookup"><span data-stu-id="a6185-129">In **Specify Internal SIP port** , select the default setting (that is, if you did not modify the default SIP port).</span></span> <span data-ttu-id="a6185-130">Cambie según corresponda si no usa un puerto predeterminado de 5061 y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a6185-130">Change as appropriate if you are not using a default port of 5061, and then click **Next**.</span></span>

12. <span data-ttu-id="a6185-131">En **Resumen**, haga clic en **siguiente** para empezar a combinar las topologías.</span><span class="sxs-lookup"><span data-stu-id="a6185-131">In **Summary**, click **Next** to begin merging the topologies.</span></span>

13. <span data-ttu-id="a6185-132">La página del asistente verifica que la combinación de las topologías se haya realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6185-132">The wizard page verifies that the merging of the topologies was successful.</span></span>

14. <span data-ttu-id="a6185-133">En la columna **Estado** , compruebe que el valor es **correcto** y, a continuación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="a6185-133">In the **Status** column, verify that the value is **Success**, and then click **Finish**.</span></span>

15. <span data-ttu-id="a6185-134">En el panel izquierdo del generador de topología, ahora debe ver el **BackCompatSite**, que indica que el entorno de Office Communications Server 2007 R2 se ha fusionado con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a6185-134">In the left pane of Topology Builder, you should now see the **BackCompatSite**, which indicates that your Office Communications Server 2007 R2 environment has been merged with Lync Server 2013.</span></span>
    
    <span data-ttu-id="a6185-135">![Generador de topología que muestra una topología combinada](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Generador de topología que muestra una topología combinada")</span><span class="sxs-lookup"><span data-stu-id="a6185-135">![Topology Builder showing a merged topology](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Topology Builder showing a merged topology")</span></span>  

16. <span data-ttu-id="a6185-136">En el menú **acción** , haga clic en **publicar topología** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a6185-136">From the **Action** menu, click **Publish Topology**, and then click **Next**.</span></span>

17. <span data-ttu-id="a6185-137">Cuando finalice el **Asistente para la publicación** , haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="a6185-137">When the **Publishing wizard** completes, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a6185-138">Es importante que complete el tema siguiente, <A href="import-policies-and-settings.md">importar directivas y configuración</A>, para asegurarse de que la configuración de directiva heredada se importa a Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a6185-138">It’s important that you complete the next topic, <A href="import-policies-and-settings.md">Import policies and settings</A>, to ensure that the legacy policy settings are imported into Lync Server 2013.</span></span>

    
    <span data-ttu-id="a6185-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6185-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

