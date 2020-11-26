---
title: 'Lync Server 2013: crear el diseño de topología inicial'
description: 'Lync Server 2013: crear el diseño de la topología inicial.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create the initial design
ms:assetid: f3131153-de14-41be-b1e6-7d4bb0191af1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615047(v=OCS.15)
ms:contentKeyID: 51541530
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c91bfe68a1de4a1f9862948edd708b8efa6a5c6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431585"
---
# <a name="create-the-initial-topology-design-for-lync-server-2013"></a><span data-ttu-id="52dee-103">Crear el diseño de topología inicial para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52dee-103">Create the initial topology design for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="52dee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="52dee-104">

<span> </span></span></span>

<span data-ttu-id="52dee-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="52dee-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="52dee-106">Una vez que haya terminado de instalar Lync Server 2013, la herramienta de planeación, estará listo para iniciar la herramienta de planeación y empezar a diseñar la infraestructura de Lync Server 2013 propuesta.</span><span class="sxs-lookup"><span data-stu-id="52dee-106">After you have finished installing the Lync Server 2013, Planning Tool, you are ready to start the Planning Tool and begin designing the proposed Lync Server 2013 infrastructure.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="52dee-107">La herramienta de planeación es una herramienta guiada por un asistente con guías detalladas para informar sobre el proceso de toma de decisiones en el diseño de sitios y topología.</span><span class="sxs-lookup"><span data-stu-id="52dee-107">The Planning Tool is a wizard-driven tool with detailed guides to inform your decision-making process in designing your sites and topology.</span></span> <span data-ttu-id="52dee-108">Este tema está pensado no es una guía exhaustiva, pero simplemente para ayudarle a empezar a usar la herramienta de planificación en sus sesiones de diseño.</span><span class="sxs-lookup"><span data-stu-id="52dee-108">This topic is intended not as an exhaustive guide, but simply to help get you started using the Planning Tool in your design sessions.</span></span>



</div>

<div>

## <a name="to-get-started-using-the-planning-tool-and-create-the-initial-design"></a><span data-ttu-id="52dee-109">Para empezar a usar la herramienta de planificación y crear el diseño inicial</span><span class="sxs-lookup"><span data-stu-id="52dee-109">To get started using the Planning Tool and create the initial design</span></span>

1.  <span data-ttu-id="52dee-110">Inicie Lync Server 2013, herramienta de planeación: haga clic en **Inicio**, haga clic en **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **herramienta de planeación**.</span><span class="sxs-lookup"><span data-stu-id="52dee-110">Start the Lync Server 2013, Planning Tool: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Planning Tool**.</span></span>

2.  <span data-ttu-id="52dee-111">Después de iniciar la herramienta de planeación, aparece la página **de bienvenida a la herramienta de planeación de Microsoft Lync Server 2013** .</span><span class="sxs-lookup"><span data-stu-id="52dee-111">After the Planning Tool has started, the **Welcome to the Planning Tool for Microsoft Lync Server 2013** page appears.</span></span> <span data-ttu-id="52dee-112">Para empezar el diseño, elija una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="52dee-112">Choose one of the following options to begin your design:</span></span>
    
      - <span data-ttu-id="52dee-113">**Opción 1: Introducción**   Haga clic en **comenzar** proporciona una serie específica de preguntas de la entrevista con las selecciones pertinentes para definir los criterios.</span><span class="sxs-lookup"><span data-stu-id="52dee-113">**Option 1: Get Started**   Clicking **Get Started** provides a specific series of interview questions with relevant selections to define the criteria.</span></span> <span data-ttu-id="52dee-114">Una vez completada la sección de entrevistas de **Introducción**, se pasa a la fase **Diseñar sitios** para definir la arquitectura del sitio.</span><span class="sxs-lookup"><span data-stu-id="52dee-114">After you have finished the initial **Get Started** interview section, you proceed into **Design Sites** to define your site architecture.</span></span> <span data-ttu-id="52dee-115">Para completar esta opción, vaya al paso 3.</span><span class="sxs-lookup"><span data-stu-id="52dee-115">To complete this option, proceed to step 3.</span></span>
    
      - <span data-ttu-id="52dee-116">**Opción 2: diseñar sitios**   Al hacer clic en **diseñar sitios** en la página de bienvenida, se omiten las preguntas de entrevistas presentadas en **la sección introducción** .</span><span class="sxs-lookup"><span data-stu-id="52dee-116">**Option 2: Design Sites**   Clicking **Design Sites** at the Welcome page bypasses the interview questions presented in the **Get Started** section.</span></span> <span data-ttu-id="52dee-117">Los datos que el usuario facilita al responder a las preguntas de la entrevista de **Introducción** se definen como sus valores predeterminados con esta opción.</span><span class="sxs-lookup"><span data-stu-id="52dee-117">The information that would have been gathered by responding to the interview questions in **Get Started** section is set to default values with this option.</span></span> <span data-ttu-id="52dee-118">Al hacer clic en **Diseñar sitios**, los diseñadores avanzados pueden prescindir de la entrevista inicial y modificar los valores predeterminados a su conveniencia en la página de inicio de **Sitios centrales**.</span><span class="sxs-lookup"><span data-stu-id="52dee-118">By clicking **Design Sites**, the experienced designer can bypass the initial interview and change the default values, as needed, on the **Central Sites** start page.</span></span> <span data-ttu-id="52dee-119">Para completar esta opción, omita los pasos del 3 al 5 y comience en el paso 6.</span><span class="sxs-lookup"><span data-stu-id="52dee-119">To complete this option, skip over steps 3-5 and start at step 6.</span></span>
    
      - <span data-ttu-id="52dee-120">**Opción 3: Mostrar la topología guardada**   Si ya ha completado y guardado una topología a través del uso anterior de la herramienta de planeación, puede omitir la mayoría de estos pasos y empezar abriendo y mostrando la topología.</span><span class="sxs-lookup"><span data-stu-id="52dee-120">**Option 3: Display Your Saved Topology**   If you have already completed and saved a topology through previous use of the Planning Tool, you can skip over most of these steps and start by opening and displaying the topology.</span></span> <span data-ttu-id="52dee-121">Además, puede cambiar y actualizar la topología, volverla a guardar y exportarla a Microsoft Excel o Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="52dee-121">You can also make changes and updates to the topology, resave it, and then export it to Microsoft Excel or Microsoft Visio.</span></span> <span data-ttu-id="52dee-122">Para completar esta opción, omita los pasos del 3 al 12 y comience en el paso 13.</span><span class="sxs-lookup"><span data-stu-id="52dee-122">To complete this option, skip over steps 3-12 and start at step 13.</span></span>

3.  <span data-ttu-id="52dee-123">Haga **clic en introducción para** empezar a diseñar su topología de 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="52dee-123">Click **Get Started** to begin designing your Lync Server 2013 topology.</span></span>

4.  <span data-ttu-id="52dee-p106">Responda a cada pregunta seleccionando el criterio correcto para el diseño; después, haga clic en **Siguiente** para pasar a la página siguiente del Asistente. Haga clic en **Atrás** para hacer cambios en páginas anteriores.</span><span class="sxs-lookup"><span data-stu-id="52dee-p106">Answer each section by selecting the appropriate criteria for your design, and then click **Next** to proceed to the next Wizard page. Click **Back** to make changes on previous pages.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="52dee-126">Cada página presenta una descripción de los criterios de selección, así como recomendaciones basadas en los procedimientos preferidos y el planeamiento de capacidad.</span><span class="sxs-lookup"><span data-stu-id="52dee-126">Each page has a description of the selection criteria, and recommendations based on preferred practices and capacity planning.</span></span> <span data-ttu-id="52dee-127">Si necesita más información, haga clic en <STRONG>más</STRONG> información para obtener información detallada de la documentación de planeación de Lync Server 2013 en el sitio web de Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="52dee-127">If you require additional details, click <STRONG>Learn more</STRONG> to read detailed information from the Lync Server 2013 Planning documentation on the Microsoft TechNet website.</span></span> <span data-ttu-id="52dee-128">Para tener acceso al sitio web de Microsoft TechNet, debe disponerse de conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="52dee-128">You must have Internet connectivity to access the Microsoft TechNet website.</span></span>

    
    </div>

5.  <span data-ttu-id="52dee-129">Seleccione las opciones pertinentes para el diseño.</span><span class="sxs-lookup"><span data-stu-id="52dee-129">Select the appropriate options for your design.</span></span> <span data-ttu-id="52dee-130">Tras haber definido los criterios iniciales, se mostrará una página para confirmar que se ha completado la información general sobre las características.</span><span class="sxs-lookup"><span data-stu-id="52dee-130">After the initial criteria are defined, a page will confirm that your Features Overview is complete.</span></span>

6.  <span data-ttu-id="52dee-131">Haga clic en **diseñar sitios** para definir el sitio central.</span><span class="sxs-lookup"><span data-stu-id="52dee-131">Click **Design Sites** to define your central site.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="52dee-132">Cada topología de Lync Server 2013 tendrá al menos un sitio central.</span><span class="sxs-lookup"><span data-stu-id="52dee-132">Each Lync Server 2013 topology will have at least one central site.</span></span> <span data-ttu-id="52dee-133">Su diseño puede tener un único sitio central, un sitio central con un número de sitios de sucursales, una serie de sitios centrales o varios sitios centrales con sitios de sucursales asociados con cada sitio central.</span><span class="sxs-lookup"><span data-stu-id="52dee-133">Your design may have a single central site, a central site with a number of branch sites, a number of central sites, or a number of central sites with branch sites associated with each central site.</span></span>

    
    </div>

7.  <span data-ttu-id="52dee-134">En **nombre del sitio**, escriba el nombre que identificará a este sitio central.</span><span class="sxs-lookup"><span data-stu-id="52dee-134">In **Site Name**, type the name that will identify this central site.</span></span>

8.  <span data-ttu-id="52dee-135">En **usuarios alojados del sitio**, escriba el número esperado de usuarios simultáneos locales que estarán alojados en este sitio central.</span><span class="sxs-lookup"><span data-stu-id="52dee-135">In **Site Homed Users**, type the expected number of on-premises concurrent users who will be homed in this central site.</span></span>

9.  <span data-ttu-id="52dee-136">En **usuarios domésticos en la nube**, escriba el número esperado de usuarios simultáneos en línea que estarán alojados en este sitio central.</span><span class="sxs-lookup"><span data-stu-id="52dee-136">In **Cloud Homed Users**, type the expected number of online concurrent users who will be homed in this central site.</span></span>

10. <span data-ttu-id="52dee-137">Modifique las opciones de Colaboración en línea, Usuarios, Voz, Opciones de implementación adicionales o Aplicaciones de servidor según se necesite.</span><span class="sxs-lookup"><span data-stu-id="52dee-137">Modify the selections for Online Collaboration, Users, Voice, Additional Deployment Options, or Server Applications, as needed.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="52dee-138">En esta fase del diseño, solamente puede activar o desactivar opciones de implementación.</span><span class="sxs-lookup"><span data-stu-id="52dee-138">At this point in the design, you can only select or clear options for your deployment.</span></span> <span data-ttu-id="52dee-139">Sin embargo, puede configurar más opciones en una fase posterior de la herramienta de planificación.</span><span class="sxs-lookup"><span data-stu-id="52dee-139">However, you can configure more options in a later phase of the Planning Tool.</span></span> <span data-ttu-id="52dee-140">También hay opciones no disponibles y que no se pueden desactivar.</span><span class="sxs-lookup"><span data-stu-id="52dee-140">There are also options that are unavailable and cannot be cleared.</span></span> <span data-ttu-id="52dee-141">Además, es posible que deba desactivar una opción para poder desactivar otra.</span><span class="sxs-lookup"><span data-stu-id="52dee-141">In addition, you may have to clear one option in order to clear another.</span></span> <span data-ttu-id="52dee-142">Por ejemplo, si desactiva la opción <STRONG>Telefonía IP empresarial</STRONG> debajo de Voz, las opciones <STRONG>Grupo de respuesta</STRONG>, <STRONG>Anuncio</STRONG> y <STRONG>Estacionamiento de llamadas</STRONG> debajo de Aplicaciones de servidor (todas ellas características de Telefonía IP empresarial) también se desactivan.</span><span class="sxs-lookup"><span data-stu-id="52dee-142">For example, if you clear the <STRONG>Enterprise Voice</STRONG> option under Voice, then the <STRONG>Response Group</STRONG>, <STRONG>Announcement</STRONG>, and <STRONG>Call Park</STRONG> options under Server Applications (all of which are features of Enterprise Voice) are also cleared.</span></span>

    
    </div>

11. <span data-ttu-id="52dee-143">Después de haber definido un nombre de sitio y la cantidad de usuarios, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="52dee-143">After defining a site name and number of users, click **Next**.</span></span>

12. <span data-ttu-id="52dee-144">Las siguientes páginas solicitan información sobre los dominios SIP, la configuración de la Conferencia, la configuración de voz y la infraestructura, la mensajería unificada de Exchange, el acceso de usuarios externos, la configuración de chat persistente, la configuración de cliente, las opciones de collocation y los sitios de sucursales</span><span class="sxs-lookup"><span data-stu-id="52dee-144">The following pages ask for information about SIP domains, conference settings, voice settings and infrastructure, Exchange UM, external user access, Persistent Chat settings, client settings, collocation options, and branch sites.</span></span> <span data-ttu-id="52dee-145">Responda a estas preguntas según considere adecuado.</span><span class="sxs-lookup"><span data-stu-id="52dee-145">Answer these questions as appropriate.</span></span>

13. <span data-ttu-id="52dee-146">La pregunta final pregunta si desea crear otro sitio central.</span><span class="sxs-lookup"><span data-stu-id="52dee-146">The final question asks if you want to create another central site.</span></span> <span data-ttu-id="52dee-147">Si selecciona **sí**, la herramienta de planeación vuelve a la página sitios centrales.</span><span class="sxs-lookup"><span data-stu-id="52dee-147">If you select **Yes**, then the Planning Tool returns to the Central Sites page.</span></span> <span data-ttu-id="52dee-148">Si selecciona **No**, haga clic en **Siguiente** y después en **Dibujar** para mostrar la vista Topología global de nivel alto.</span><span class="sxs-lookup"><span data-stu-id="52dee-148">If you select **No**, click **Next**, and then click **Draw** to display the high-level Global Topology view.</span></span>

14. <span data-ttu-id="52dee-149">Para ver una topología que ya existe, haga clic en **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="52dee-149">To view an existing topology, click **Display**.</span></span>

15. <span data-ttu-id="52dee-150">Haga clic en el archivo .xml que representa la topología guardada anteriormente; a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="52dee-150">Click the .xml file that represents the previously saved topology, and then click **Open**.</span></span>

16. <span data-ttu-id="52dee-151">La herramienta de planeación muestra la página de topología global.</span><span class="sxs-lookup"><span data-stu-id="52dee-151">The Planning Tool displays the Global Topology page.</span></span> <span data-ttu-id="52dee-152">Ahora puede empezar a editar, actualizar o cambiar la topología mediante las herramientas disponibles en la herramienta de planificación.</span><span class="sxs-lookup"><span data-stu-id="52dee-152">You can now begin editing, updating, or changing the topology by using the tools available in the Planning Tool.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="52dee-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="52dee-153">See Also</span></span>


[<span data-ttu-id="52dee-154">Edición del diseño en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52dee-154">Editing the design in Lync Server 2013</span></span>](lync-server-2013-editing-the-design.md)  
  

<span data-ttu-id="52dee-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="52dee-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

