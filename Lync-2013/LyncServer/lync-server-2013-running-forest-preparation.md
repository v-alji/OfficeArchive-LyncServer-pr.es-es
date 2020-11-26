---
title: 'Lync Server 2013: Ejecutar la preparación del bosque'
description: 'Lync Server 2013: ejecución de la preparación del bosque.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running forest preparation
ms:assetid: 9d62f7be-bcfe-421d-8d8a-225567102a35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412732(v=OCS.15)
ms:contentKeyID: 48184991
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad3ef2d7583d541701d6606946ca1df1bbd8cf23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442218"
---
# <a name="running-forest-preparation-for-lync-server-2013"></a><span data-ttu-id="052f3-103">Ejecutar la preparación del bosque para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="052f3-103">Running forest preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="052f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="052f3-104">

<span> </span></span></span>

<span data-ttu-id="052f3-105">_**Última modificación del tema:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="052f3-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="052f3-106">Puede usar el programa de instalación o los cmdlets del shell de administración de Lync Server para preparar el bosque.</span><span class="sxs-lookup"><span data-stu-id="052f3-106">You can use Setup or Lync Server Management Shell cmdlets to prepare the forest.</span></span> <span data-ttu-id="052f3-107">El cmdlet que prepara el bosque es **enable-CsAdForest**.</span><span class="sxs-lookup"><span data-stu-id="052f3-107">The cmdlet that prepares the forest is **Enable-CsAdForest**.</span></span>

<span data-ttu-id="052f3-108">Después de preparar el bosque, debe comprobar que la configuración global se ha replicado antes de ejecutar la preparación del dominio.</span><span class="sxs-lookup"><span data-stu-id="052f3-108">After you prepare the forest, you must verify that global settings have been replicated before running domain preparation.</span></span>

<div>

## <a name="to-use-setup-to-prepare-the-forest"></a><span data-ttu-id="052f3-109">Para usar el programa de instalación para preparar el bosque</span><span class="sxs-lookup"><span data-stu-id="052f3-109">To use Setup to prepare the forest</span></span>

1.  <span data-ttu-id="052f3-110">Inicie sesión en un equipo unido a un dominio como miembro del grupo administradores de empresa del dominio raíz del bosque.</span><span class="sxs-lookup"><span data-stu-id="052f3-110">Log on to a computer that is joined to a domain as a member of the Enterprise Admins group for the forest root domain.</span></span>

2.  <span data-ttu-id="052f3-111">Desde la carpeta o los medios de instalación de Lync Server 2013, ejecute Setup.exe para iniciar el Asistente para la implementación.</span><span class="sxs-lookup"><span data-stu-id="052f3-111">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Deployment Wizard.</span></span>

3.  <span data-ttu-id="052f3-112">Haga clic en **Preparar Active Directory** y espere hasta que se determine el estado de implementación.</span><span class="sxs-lookup"><span data-stu-id="052f3-112">Click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

4.  <span data-ttu-id="052f3-113">En el **paso 3: preparar el bosque actual**, haga clic en **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="052f3-113">At **Step 3: Prepare Current Forest**, click **Run**.</span></span>

5.  <span data-ttu-id="052f3-114">En la página **preparar el bosque** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="052f3-114">On the **Prepare Forest** page, click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="052f3-115">La preparación del bosque le permite elegir dónde ubicar los grupos universales para Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="052f3-115">Forest Preparation allows you to choose where to place the Universal Groups for Lync Server 2013.</span></span> <span data-ttu-id="052f3-116">Elija una ubicación que respete los requisitos de su organización.</span><span class="sxs-lookup"><span data-stu-id="052f3-116">Choose a location that is consistent with the requirements of your organization.</span></span>

    
    </div>

6.  <span data-ttu-id="052f3-117">En la página **Ejecución de comandos**, busque **Estado de tarea: Completado** y haga clic en **Ver registro**.</span><span class="sxs-lookup"><span data-stu-id="052f3-117">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

7.  <span data-ttu-id="052f3-118">En la columna **acción** , expanda **preparar bosque**, busque un **\<Success\>** resultado de ejecución al final de cada tarea para comprobar que la preparación del bosque se completó correctamente, cierre el registro y, a continuación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="052f3-118">Under the **Action** column, expand **Forest Prep**, look for a **\<Success\>** Execution Result at the end of each task to verify that forest preparation completed successfully, close the log, and then click **Finish**.</span></span>

8.  <span data-ttu-id="052f3-119">Espere a que se complete la replicación de Active Directory, o fuerce la replicación en todos los controladores de dominio que aparecen en el complemento **sitios y servicios de Active** Directory para el controlador de dominio raíz del bosque, antes de ejecutar la preparación del dominio.</span><span class="sxs-lookup"><span data-stu-id="052f3-119">Wait for Active Directory replication to complete, or force replication to all domain controllers listed in the **Active Directory Sites and Services** snap-in for the forest root domain controller, before running domain preparation.</span></span> <span data-ttu-id="052f3-120">Fuerce la replicación entre los controladores de dominio de todos los sitios de Active Directory para que la replicación dentro de los sitios se produzca en minutos.</span><span class="sxs-lookup"><span data-stu-id="052f3-120">Force replication between the domain controllers in all Active Directory sites to cause replication within the sites to occur within minutes.</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-forest"></a><span data-ttu-id="052f3-121">Para usar cmdlets para preparar el bosque</span><span class="sxs-lookup"><span data-stu-id="052f3-121">To use cmdlets to prepare the forest</span></span>

1.  <span data-ttu-id="052f3-122">Inicie sesión en un equipo unido a un dominio como miembro del grupo administradores del dominio en el dominio raíz del bosque.</span><span class="sxs-lookup"><span data-stu-id="052f3-122">Log on to a computer that is joined to a domain as a member of the Domain Admins group in the forest root domain.</span></span>

2.  <span data-ttu-id="052f3-123">Instale los componentes básicos de Lync Server de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="052f3-123">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="052f3-124">Desde la carpeta o los elementos multimedia de la instalación de Lync Server 2013, ejecute Setup.exe para iniciar el Asistente para la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="052f3-124">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="052f3-125">Si se le pide que instale el redistribuible de Microsoft Visual C++, haga clic en **sí**.</span><span class="sxs-lookup"><span data-stu-id="052f3-125">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="052f3-126">En el cuadro de diálogo instalación de Lync Server 2013 se le pide una ubicación para instalar los archivos de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="052f3-126">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="052f3-127">Elija la ubicación predeterminada o **Desplácese** hasta la ubicación que desee y, a continuación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="052f3-127">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="052f3-128">En la página contrato de licencia, seleccione **acepto los términos del contrato de licencia** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="052f3-128">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="052f3-129">El instalador instala los componentes principales de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="052f3-129">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="052f3-130">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="052f3-130">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="052f3-131">Ejecute:</span><span class="sxs-lookup"><span data-stu-id="052f3-131">Run:</span></span>
    
        Enable-CsAdForest [-GroupDomain <FQDN of the domain in which to create the universal groups>]
    
    <span data-ttu-id="052f3-132">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="052f3-132">For example:</span></span>
    
        Enable-CsAdForest -GroupDomain domain1.contoso.com 
    
    <span data-ttu-id="052f3-133">Si no especifica el parámetro GroupDomain, el valor predeterminado es el dominio local.</span><span class="sxs-lookup"><span data-stu-id="052f3-133">If you do not specify the GroupDomain parameter, the default value is the local domain.</span></span> <span data-ttu-id="052f3-134">Si se han creado grupos universales en un dominio que no es el dominio predeterminado, debe especificar el parámetro GroupDomain de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="052f3-134">If universal groups were created previously in a domain that is not the default domain, you must specify the GroupDomain parameter explicitly.</span></span>

5.  <span data-ttu-id="052f3-135">Espere a que se complete la replicación de Active Directory, o fuerce la replicación en todos los controladores de dominio que aparecen en el complemento **sitios y servicios de Active** Directory para el controlador de dominio raíz del bosque, antes de ejecutar la preparación del dominio.</span><span class="sxs-lookup"><span data-stu-id="052f3-135">Wait for Active Directory replication to complete, or force replication to all domain controllers listed in the **Active Directory Sites and Services** snap-in for the forest root domain controller, before running domain preparation.</span></span>

6.  <span data-ttu-id="052f3-136">Verifique que la preparación del bosque se haya realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="052f3-136">Verify that forest preparation was successful.</span></span> <span data-ttu-id="052f3-137">Ejecute:</span><span class="sxs-lookup"><span data-stu-id="052f3-137">Run:</span></span>
    
        Get-CsAdForest 
    
    <span data-ttu-id="052f3-138">Este cmdlet devuelve un valor de **LC \_ FORESTSETTINGS \_ estado \_ listo** si la preparación del bosque se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="052f3-138">This cmdlet returns a value of **LC\_FORESTSETTINGS\_STATE\_READY** if forest preparation was successful.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="052f3-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="052f3-139">See Also</span></span>


[<span data-ttu-id="052f3-140">Usar cmdlets para invertir la preparación del bosque para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="052f3-140">Using cmdlets to reverse forest preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-forest-preparation.md)  


[<span data-ttu-id="052f3-141">Preparación del bosque para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="052f3-141">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
  

<span data-ttu-id="052f3-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="052f3-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

