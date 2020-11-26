---
title: 'Lync Server 2013: crear o modificar un flujo de trabajo de un grupo de captura'
description: 'Lync Server 2013: crear o modificar un flujo de trabajo de grupo de captura.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a hunt group workflow
ms:assetid: dcb9effb-5d12-4dee-80fc-ab9654222d5a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205321(v=OCS.15)
ms:contentKeyID: 48185596
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95f6374352c87d13b1e5c09bcef267059016eae0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431837"
---
# <a name="create-or-modify-a-hunt-group-workflow-in-lync-server-2013"></a><span data-ttu-id="2ede4-103">Crear o modificar un flujo de trabajo de grupo de captura en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ede4-103">Create or modify a hunt group workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2ede4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2ede4-104">

<span> </span></span></span>

<span data-ttu-id="2ede4-105">_**Última modificación del tema:** 2013-09-11_</span><span class="sxs-lookup"><span data-stu-id="2ede4-105">_**Topic Last Modified:** 2013-09-11_</span></span>

<span data-ttu-id="2ede4-106">Use uno de los procedimientos siguientes para crear o modificar un flujo de trabajo de grupo de captura.</span><span class="sxs-lookup"><span data-stu-id="2ede4-106">Use one of the following procedures to create or modify a hunt group workflow.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2ede4-107">Puede usar el shell de administración de Lync Server o la herramienta de configuración de grupos de respuesta para crear y modificar flujos de trabajo de grupos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2ede4-107">You can use Lync Server Management Shell or the Response Group Configuration Tool to create and modify hunt group workflows.</span></span> <span data-ttu-id="2ede4-108">Puede obtener acceso a la herramienta de configuración de grupos de respuesta desde el panel de control de Lync Server o abriendo la página web directamente desde un explorador web escribiendo la siguiente dirección URL: <STRONG>https://</STRONG> &lt; webPoolFqdn &gt; <STRONG>/RgsConfig</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-108">You can access the Response Group Configuration Tool from Lync Server Control Panel, or by opening the webpage directly from a web browser by typing the following URL: <STRONG>https://</STRONG>&lt;webPoolFqdn&gt;<STRONG>/RgsConfig</STRONG>.</span></span>



</div>

<div>

## <a name="to-use-response-group-configuration-tool-to-create-or-modify-a-hunt-group-workflow"></a><span data-ttu-id="2ede4-109">Para usar la herramienta de configuración de grupos de respuesta para crear o modificar un flujo de trabajo de Hunt Group</span><span class="sxs-lookup"><span data-stu-id="2ede4-109">To use Response Group Configuration Tool to create or modify a hunt group workflow</span></span>

1.  <span data-ttu-id="2ede4-110">Inicie sesión como miembro del grupo RTCUniversalServerAdmins o como miembro de uno de los roles administrativos predefinidos que admiten el Grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ede4-110">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="2ede4-111">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2ede4-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2ede4-112">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2ede4-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="2ede4-113">En la barra de navegación izquierda, haga clic en **Grupos de respuesta** y después en **Flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-113">In the left navigation bar, click **Response Groups**, and then click **Workflow**.</span></span>

4.  <span data-ttu-id="2ede4-114">En la página **Flujo de trabajo**, haga clic en **Crear o editar un flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-114">On the **Workflow** page, click **Create or edit a workflow**.</span></span>

5.  <span data-ttu-id="2ede4-115">En el campo de búsqueda **Seleccionar un servicio**, escriba la totalidad o parte del nombre del servicio **ApplicationServer** que hospeda el flujo de trabajo que desea crear o cambiar.</span><span class="sxs-lookup"><span data-stu-id="2ede4-115">In the **Select a Service** search field, type all or part of the name of the **ApplicationServer** service that hosts the workflow that you want to create or change.</span></span> <span data-ttu-id="2ede4-116">En la lista de servicios resultante, haga clic en el servicio que desee y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-116">In the resulting list of services, click the service that you want, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-117">Se abrirá la herramienta de configuración de grupos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ede4-117">The Response Group Configuration Tool opens.</span></span> <span data-ttu-id="2ede4-118">También puede abrir la herramienta de configuración de grupo de respuesta directamente desde un explorador web escribiendo la siguiente URL: <STRONG>https://</STRONG> &lt; webPoolFqdn &gt; <STRONG>/RgsConfig</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-118">You can also open the Response Group Configuration Tool directly from a web browser by typing the following URL: <STRONG>https://</STRONG>&lt;webPoolFqdn&gt;<STRONG>/RgsConfig</STRONG>.</span></span>

    
    </div>

6.  <span data-ttu-id="2ede4-119">Siga uno de estos pasos:</span><span class="sxs-lookup"><span data-stu-id="2ede4-119">Do one of the following:</span></span>
    
      - <span data-ttu-id="2ede4-120">Under **Create a New Workflow**, next to **Hunt Group, click Create**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-120">Under **Create a New Workflow**, next to **Hunt Group, click Create**.</span></span>
    
      - <span data-ttu-id="2ede4-121">En **Administrar un flujo de trabajo existente**, localice el flujo de trabajo que desea cambiar y, a continuación, en **Acción**, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-121">Under **Manage an Existing Workflow**, locate the workflow you want to change, and then under **Action**, click **Edit**.</span></span>

7.  <span data-ttu-id="2ede4-122">Si está listo para que los usuarios empiecen a llamar al flujo de trabajo, seleccione **Activar el flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-122">If you are ready for users to start calling the workflow, select **Activate the workflow**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-p105">Si está creando un flujo de trabajo administrado, seleccione <STRONG>Activar el flujo de trabajo</STRONG>. Después de guardar el flujo de trabajo administrado activo, puede modificarlo y desactivarlo.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p105">If you are to creating a managed workflow, you need to select <STRONG>Activate the workflow</STRONG>. After you save the active, managed workflow, you can then modify and deactivate it.</span></span>

    
    </div>

8.  <span data-ttu-id="2ede4-125">Para permitir que los usuarios federados puedan llamar al grupo, active la casilla **Habilitar para federación**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-125">To allow federated users to call the group, select the **Enable for federation** check box.</span></span> <span data-ttu-id="2ede4-126">También debe tener una directiva de acceso externo que se aplique a la aplicación de grupo de respuesta configurada para la Federación.</span><span class="sxs-lookup"><span data-stu-id="2ede4-126">You must also have an external access policy that applies to the Response Group application configured for federation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-127">La Directiva de acceso externo global se aplica a la aplicación de grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ede4-127">The global external access policy applies to the Response Group application.</span></span> <span data-ttu-id="2ede4-128">Puede configurar la directiva global para la Federación de grupos de respuesta mediante el panel de control de Lync Server o mediante el cmdlet <STRONG>set-CsExternalAccessPolicy</STRONG> para establecer el parámetro EnableOutsideAccess en true.</span><span class="sxs-lookup"><span data-stu-id="2ede4-128">You can configure the global policy for response group federation by using Lync Server Control Panel or by using the <STRONG>Set-CsExternalAccessPolicy</STRONG> cmdlet to set the EnableOutsideAccess parameter to True.</span></span> <span data-ttu-id="2ede4-129">Recuerde que la configuración de la directiva global se aplica a todos los usuarios, a menos que se les haya asignado una directiva de usuario o de sitio.</span><span class="sxs-lookup"><span data-stu-id="2ede4-129">Keep in mind that global policy settings apply to all users unless they are assigned a site or user policy.</span></span> <span data-ttu-id="2ede4-130">Por lo tanto, antes de cambiar la configuración de los grupos de respuesta, asegúrese de que la configuración de la federación cumpla los requisitos de la organización.</span><span class="sxs-lookup"><span data-stu-id="2ede4-130">Therefore, before changing this setting for response groups, make sure that the federation setting meets the requirements of your organization.</span></span> <span data-ttu-id="2ede4-131">Para obtener más información sobre cómo se aplican las directivas a los usuarios, vea <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">administrar la Directiva de acceso externo en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-131">For details about how policies apply to users, see <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">Manage external access policy in Lync Server 2013</A>.</span></span> <span data-ttu-id="2ede4-132">Para obtener más información sobre la configuración de Federación, consulte <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsExternalAccessPolicy">set-CsExternalAccessPolicy</A>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-132">For details about the federation setting, see <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsExternalAccessPolicy">Set-CsExternalAccessPolicy</A>.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-133">Los usuarios que se hospedan en Lync Online no pueden realizar llamadas a grupos de respuesta hospedados en una implementación local.</span><span class="sxs-lookup"><span data-stu-id="2ede4-133">Users who are hosted in Lync Online can’t place calls to response groups that are hosted in an on-premise deployment.</span></span> <span data-ttu-id="2ede4-134">Esto sucede en ambas implementaciones híbridas y en los casos en los que una implementación local se federa con una implementación de Lync Online.</span><span class="sxs-lookup"><span data-stu-id="2ede4-134">This is true in both hybrid deployments and in cases where an on-premise deployment is federated with a Lync Online deployment.</span></span>

    
    </div>

9.  <span data-ttu-id="2ede4-135">Para ocultar la identidad de los agentes durante las llamadas, active la casilla **Habilitar anonimato de agente**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-135">To hide the identity of agents during calls, select the **Enable agent anonymity** check box.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-p109">Las llamadas anónimas no pueden empezar con mensajería instantánea (MI) ni un vídeo, aunque el agente o la persona que llame pueda agregar MI o un vídeo después de establecer la llamada. Asimismo, un agente anónimo puede poner llamadas en espera, transferir llamadas (tanto transferencias a otras líneas como consultas), además de estacionar y recuperar llamadas. Las llamadas anónimas no admiten conferencias, uso compartido de aplicaciones ni de escritorio, transferencia de archivos, función de pizarra, colaboración de datos y grabación de llamadas. Los agentes que usen el complemento VDI de Lync pueden recibir llamadas entrantes anónimas, pero no realizar llamadas salientes anónimas.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p109">Anonymous calls cannot start with instant messaging (IM) or video, although the agent or the caller can add IM and video after the call is established. An anonymous agent can also put calls on hold, transfer calls (both blind and consultative transfers), and park and retrieve calls. Anonymous calls do not support conferencing, application sharing and desktop sharing, file transfer, whiteboarding and data collaboration, and call recording. Agents using the Lync VDI Plugin can receive incoming calls anonymously, but they cannot make outgoing calls anonymously.</span></span>

    
    </div>

10. <span data-ttu-id="2ede4-140">En **Especifique la dirección del grupo que recibirá las llamadas**, escriba la dirección del identificador uniforme de recursos (URI) del SIP primario del grupo que responderá las llamadas al flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2ede4-140">Under **Enter the address of the group that will receive the calls**, type the primary SIP uniform resource identifier (URI) address of the group that will answer calls to the workflow.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-141">El URI principal de un flujo de trabajo es la forma cómo se identifica y se denomina el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2ede4-141">The primary URI for a workflow is how the workflow is identified and referenced.</span></span> <span data-ttu-id="2ede4-142">El URI de SIP que especifique se creará como un objeto de contacto en los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2ede4-142">The SIP URI that you enter is created as a contact object in Active Directory Domain Services.</span></span> <span data-ttu-id="2ede4-143">Para crear el URI, el objeto debe ser único en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2ede4-143">To create the URI, the object must be unique in Active Directory.</span></span>

    
    </div>

11. <span data-ttu-id="2ede4-144">En **nombre para mostrar**, escriba el nombre que desea mostrar para el flujo de trabajo (por ejemplo, grupo de respuesta de ventas).</span><span class="sxs-lookup"><span data-stu-id="2ede4-144">In **Display name**, type the name that you want to display for the workflow (for example, Sales Response Group).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-145">No incluyas los &lt; caracteres "" o " &gt; " en el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="2ede4-145">Do not include the "&lt;" or "&gt;" characters in the display name.</span></span> <span data-ttu-id="2ede4-146">No use los siguientes nombres para mostrar porque están reservados: <STRONG>RGS Presence Watcher</STRONG> o <STRONG>Announcement Service</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-146">Do not use the following display names because they are reserved: <STRONG>RGS Presence Watcher</STRONG> or <STRONG>Announcement Service</STRONG>.</span></span>

    
    </div>

12. <span data-ttu-id="2ede4-147">En **Número de teléfono**, especifique el URI de línea para el grupo de respuesta (por ejemplo, +14255550165).</span><span class="sxs-lookup"><span data-stu-id="2ede4-147">Under **Telephone number**, type the line URI for the response group (for example, +14255550165).</span></span>

13. <span data-ttu-id="2ede4-148">En **Número para mostrar**, escriba el número tal como desea que aparezca para el grupo de respuesta (por ejemplo, +1 (425) 555-0165).</span><span class="sxs-lookup"><span data-stu-id="2ede4-148">In **Display number**, type the number as you want it to appear for the response group (for example, +1 (425) 555-0165).</span></span>

14. <span data-ttu-id="2ede4-149">Faculta En **Descripción**, escriba una descripción para el flujo de trabajo tal y como desea que aparezca en la tarjeta de contacto en el cliente de Lync.</span><span class="sxs-lookup"><span data-stu-id="2ede4-149">(Optional) In **Description**, type a description for the workflow as you want it to appear on the contact card in Lync client.</span></span>

15. <span data-ttu-id="2ede4-150">En **Tipo de flujo de trabajo**, seleccione **Administrado** si este flujo de trabajo va a ser administrado por un administrador de grupos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ede4-150">In **Workflow Type**, select **Managed** if this workflow will be managed by a Response Group Manager.</span></span> <span data-ttu-id="2ede4-151">Siga este procedimiento para asignar administradores de grupos de respuesta al flujo de trabajo:</span><span class="sxs-lookup"><span data-stu-id="2ede4-151">Do the following to assign Response Group Managers to the workflow:</span></span>
    
    1.  <span data-ttu-id="2ede4-152">Escriba el URI del SIP de un administrador para este flujo de trabajo y haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-152">Type the SIP URI of a manager for this workflow, and click **Add**.</span></span>
    
    2.  <span data-ttu-id="2ede4-153">Escriba el URI del SIP de otros administradores que desee agregar al flujo de trabajo y haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-153">Type the SIP URI of additional managers to add to the workflow, and click **Add**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="2ede4-p113">A todos los usuarios designados administradores de un grupo de respuestas se les asigna el rol CsResponseGroupManager. Los usuarios a los que no se haya asignado este rol no pueden administrar grupos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p113">Every user who is designated as a manager of a response group must be assigned the CsResponseGroupManager role. If users are not assigned this role, they cannot manage response groups.</span></span>

    
    </div>

16. <span data-ttu-id="2ede4-156">En **Paso 2 Seleccionar un idioma**, haga clic en el idioma que desea utilizar para reconocimiento de voz y conversión de texto a voz.</span><span class="sxs-lookup"><span data-stu-id="2ede4-156">Under **Step 2 Select a Language**, click the language that you want to use for speech recognition and text-to-speech.</span></span>

17. <span data-ttu-id="2ede4-157">Si desea definir un mensaje de bienvenida, en el **Paso 3 Configurar un mensaje de bienvenida**, active la casilla **Reproducir un mensaje de bienvenida** y luego lleve a cabo uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="2ede4-157">If you want to configure a welcome message, under **Step 3 Configure a Welcome Message**, select the **Play a welcome message** check box, and then do one of the following:</span></span>
    
      - <span data-ttu-id="2ede4-158">Para escribir el mensaje de bienvenida como texto que se convertirá en voz para el autor de la llamada, haga clic en **Usar texto a voz** y después escriba el mensaje de bienvenida en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2ede4-158">To enter the welcome message as text that is converted to speech for callers, click **Use text-to-speech**, and then type the welcome message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2ede4-p114">No incluya etiquetas HTML en el texto que especifique. Si incluye etiquetas HTML, recibirá un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p114">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="2ede4-p115">Para usar una grabación de un archivo de audio de Windows Media (.wma) o WAVE (.wav) para el mensaje de bienvenida, haga clic en **Seleccionar una grabación**. Si desea cargar un archivo de audio nuevo, haga clic en el vínculo **una grabación**. En la nueva ventana del explorador, haga clic en **Examinar**, seleccione el archivo de audio y luego haga clic en **Abrir**. Haga clic en **Cargar** para cargar el archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p115">To use a wave (.wav) or Windows Media audio (.wma) file recording for the welcome message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the audio file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2ede4-165">Todos los archivos de audio proporcionados por el usuario deben cumplir ciertos requisitos.</span><span class="sxs-lookup"><span data-stu-id="2ede4-165">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="2ede4-166">Para obtener detalles sobre los formatos de archivo admitidos, consulte <A href="lync-server-2013-technical-requirements-for-response-group.md">requisitos técnicos para el grupo de respuesta de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-166">For details about supported file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

18. <span data-ttu-id="2ede4-167">En **Paso 4 Especificar horario comercial**, en el cuadro **Su zona horaria**, haga clic en la zona horaria para el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2ede4-167">Under **Step 4 Specify Your Business Hours**, in **Your time zone**, click the time zone for the workflow.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-p117">La zona horaria es aquella donde residen los autores de las llamadas y los agentes del flujo de trabajo. Se usa para calcular las horas de apertura y de cierre. Por ejemplo, si el flujo de trabajo se configura para usar la zona horaria Hora oriental de América del Norte y el flujo de trabajo se programa para abrirse a las 7:00 horas y cerrarse a las 23:00 horas, se supone que las horas de apertura y de cierre son, respectivamente, 7:00 horas en horario oriental y 23:00 horas en horario oriental. (Debe escribir las horas en el formato de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="2ede4-p117">The time zone is the time zone where the callers and agents of the workflow reside. It is used to calculate the open and close hours. For example, if the workflow is configured to use the North American Eastern Time zone and the workflow is scheduled to open at 7:00 A.M. and close at 11:00 P.M., the open and close times are assumed to be 7:00 Eastern Time and 23:00 Eastern Time respectively. (You must enter the times in 24-hour time notation.)</span></span>

    
    </div>

19. <span data-ttu-id="2ede4-173">Para seleccionar el tipo de programación de horario comercial que quiere usar, siga uno de los procedimientos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2ede4-173">Select the type of business hours schedule you want to use by doing one of the following:</span></span>
    
      - <span data-ttu-id="2ede4-174">Para usar una programación predefinida de horario comercial, haga clic en **Usar una programación preestablecida** y después seleccione el horario que desea utilizar en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="2ede4-174">To use a predefined schedule of business hours, click **Use a preset schedule**, and then select the schedule you want to use from the drop-down list.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2ede4-175">Debe definir al menos una programación preestablecida previamente para poder seleccionar esta opción.</span><span class="sxs-lookup"><span data-stu-id="2ede4-175">You must have defined at least one preset schedule previously to be able to select this option.</span></span> <span data-ttu-id="2ede4-176">Puede definir programaciones preestablecidas con el cmdlet <STRONG>New-CSRgsHoursOfBusiness</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-176">You define preset schedules by using the <STRONG>New-CSRgsHoursOfBusiness</STRONG> cmdlet.</span></span> <span data-ttu-id="2ede4-177">Para obtener más información, consulte <A href="lync-server-2013-optional-define-response-group-business-hours.md">(opcional) definir las horas de trabajo del grupo de respuesta en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-177">For details, see <A href="lync-server-2013-optional-define-response-group-business-hours.md">(Optional) Define Response Group business hours in Lync Server 2013</A>.</span></span>

        
        </div>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2ede4-178">Cuando selecciona una programación preestablecida, <STRONG>Día</STRONG>, <STRONG>Abrir</STRONG> y <STRONG>Cerrar</STRONG> se rellenan automáticamente con los días y las horas en los que el grupo de respuesta se encuentra disponible.</span><span class="sxs-lookup"><span data-stu-id="2ede4-178">When you select a preset schedule, <STRONG>Day</STRONG>, <STRONG>Open</STRONG>, and <STRONG>Close</STRONG> are automatically filled with the days and hours that the response group is available.</span></span>

        
        </div>
    
      - <span data-ttu-id="2ede4-179">Para usar una programación personalizada que se aplique solo a este flujo de trabajo, haga clic en **Usar una programación personalizada**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-179">To use a custom schedule that applies only to this workflow, click **Use a custom schedule**.</span></span>

20. <span data-ttu-id="2ede4-180">Si está creando una programación personalizada para este flujo de trabajo, haga clic en las casillas correspondientes a los días de la semana durante los que se encuentra disponible el grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ede4-180">If you are creating a custom schedule for this workflow, click the check boxes for the days of the week that the response group is available.</span></span>

21. <span data-ttu-id="2ede4-181">Si está creando una programación personalizada, especifique las horas en **Abrir** y **Cerrar** para cada día de la semana en el que esté disponible el grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ede4-181">If you are creating a custom schedule, type the **Open** and **Close** hours for each day of the week that the response group available.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-p119">Las horas de <STRONG>Abrir</STRONG> y <STRONG>Cerrar</STRONG> deben mostrarse en formato de 24 horas. Por ejemplo, si en su oficina se trabaja de 9 a 5 y se cierra al mediodía para el almuerzo, el horario comercial se especificará de la siguiente manera: <STRONG>Abrir</STRONG> 9:00, <STRONG>Cerrar</STRONG> 12:00, <STRONG>Abrir</STRONG> 13:00 y <STRONG>Cerrar</STRONG> 17:00.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p119">The <STRONG>Open</STRONG> and <STRONG>Close</STRONG> hours must be in 24-hour time notation. For example, if your office works a 9-to-5 work day and closes at noon for lunch, the business hours are specified as <STRONG>Open</STRONG> 9:00, <STRONG>Close</STRONG> 12:00, <STRONG>Open</STRONG> 13:00, and <STRONG>Close</STRONG> 17:00.</span></span>

    
    </div>

22. <span data-ttu-id="2ede4-184">Si desea reproducir un mensaje cuando la oficina no esté abierta, active la casilla **Reproducir un mensaje cuando el grupo de respuesta esté fuera del horario comercial** y después especifique el mensaje que se va a reproducir siguiendo uno de los procedimientos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2ede4-184">If you want to play a message when the office is not open, select the **Play a message when the response group is outside of business hours** check box, and then specify the message to play by doing one of the following:</span></span>
    
      - <span data-ttu-id="2ede4-185">Para escribir el mensaje como texto que se convertirá en voz para el autor de la llamada, haga clic en **Usar texto a voz** y después escriba el mensaje de bienvenida en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2ede4-185">To enter the message as text that is converted to speech for the caller, click **Use text-to-speech**, and then type the message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2ede4-p120">No incluya etiquetas HTML en el texto que especifique. Si incluye etiquetas HTML, recibirá un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p120">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="2ede4-p121">Para usar una grabación en un archivo de audio para el mensaje, haga clic en **Seleccionar una grabación**. Si desea cargar un archivo de audio nuevo, haga clic en el vínculo **una grabación**. En la nueva ventana del explorador, haga clic en **Examinar**, seleccione el archivo que desea usar y después haga clic en **Abrir**. Haga clic en **Cargar** para cargar el archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p121">To use an audio file recording for the message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2ede4-192">Todos los archivos de audio proporcionados por el usuario deben cumplir ciertos requisitos.</span><span class="sxs-lookup"><span data-stu-id="2ede4-192">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="2ede4-193">Para obtener detalles sobre los formatos de archivo de audio admitidos, consulte <A href="lync-server-2013-technical-requirements-for-response-group.md">requisitos técnicos para el grupo de respuesta de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-193">For details about supported audio file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

23. <span data-ttu-id="2ede4-194">Especifique cómo abordar las llamadas tras la reproducción del mensaje (si se ha configurado uno):</span><span class="sxs-lookup"><span data-stu-id="2ede4-194">Specify how to handle calls after the message is played (if a message is configured):</span></span>
    
      - <span data-ttu-id="2ede4-195">Para desconectar la llamada, haga clic en **Desconectar llamada**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-195">To disconnect the call, click **Disconnect Call**.</span></span>
    
      - <span data-ttu-id="2ede4-196">Para desviar la llamada al correo de voz, haga clic en **Desviar a correo de voz** y escriba la dirección de correo de voz.</span><span class="sxs-lookup"><span data-stu-id="2ede4-196">To forward the call to voice mail, click **Forward to voice mail**, and then type the voice mail address.</span></span> <span data-ttu-id="2ede4-197">El formato de la dirección de correo de voz es \<username\> @ \<domainName\> (por ejemplo, Bob@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="2ede4-197">The format for the voice mail address is \<username\>@\<domainName\> (for example, bob@contoso.com).</span></span>
    
      - <span data-ttu-id="2ede4-198">Para desviar la llamada a otro usuario, haga clic en **Desviar a URI del SIP** y escriba la dirección de usuario.</span><span class="sxs-lookup"><span data-stu-id="2ede4-198">To forward the call to another user, click **Forward to SIP URI**, and then type a user address.</span></span> <span data-ttu-id="2ede4-199">El formato de la dirección de usuario es \<username\> @ \<domainName\> .</span><span class="sxs-lookup"><span data-stu-id="2ede4-199">The format for the user address is \<username\>@\<domainName\>.</span></span>
    
      - <span data-ttu-id="2ede4-200">Para desviar la llamada a otro número de teléfono, haga clic en **Desviar a número de teléfono** y escriba el número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="2ede4-200">To forward the call to another telephone number, click **Forward to telephone number**, and then type the telephone number.</span></span> <span data-ttu-id="2ede4-201">El formato del número de teléfono es \<number\> @ \<domainName\> (por ejemplo, + 14255550121@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="2ede4-201">The format for the telephone number is \<number\>@\<domainName\> (for example, +14255550121@contoso.com).</span></span> <span data-ttu-id="2ede4-202">El nombre de dominio se usa para redirigir al autor de la llamada al destino correcto.</span><span class="sxs-lookup"><span data-stu-id="2ede4-202">The domain name is used to route the caller to the correct destination.</span></span>

24. <span data-ttu-id="2ede4-203">En **Paso 5 Especificar vacaciones**, haga clic en las casillas para uno o más conjuntos de vacaciones que definan los días en los que el grupo de respuesta no esté laboralmente disponible.</span><span class="sxs-lookup"><span data-stu-id="2ede4-203">Under **Step 5 Specify Your Holidays**, click the check boxes for one or more sets of holidays that define the days when the response group is closed for business.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-204">Defina las vacaciones y los conjuntos de vacaciones antes de configurar el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2ede4-204">You need to define holidays and holiday sets before you configure the workflow.</span></span> <span data-ttu-id="2ede4-205">Para ello, use los cmdlets <STRONG>New-CsRgsHoliday</STRONG> y <STRONG>New-CsRgsHolidaySet</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-205">Use the <STRONG>New-CsRgsHoliday</STRONG> and <STRONG>New-CsRgsHolidaySet</STRONG> cmdlets to define holidays and holiday sets.</span></span> <span data-ttu-id="2ede4-206">Para obtener más información, consulte <A href="lync-server-2013-optional-define-response-group-holiday-sets.md">(opcional) definir conjuntos de días festivos de grupos de respuesta en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-206">For details, see <A href="lync-server-2013-optional-define-response-group-holiday-sets.md">(Optional) Define Response Group holiday sets in Lync Server 2013</A>.</span></span>

    
    </div>

25. <span data-ttu-id="2ede4-207">Si desea reproducir un mensaje durante las vacaciones, active la casilla **Reproducir un mensaje durante las vacaciones** y después especifique el mensaje que se va a reproducir con uno de los siguientes procedimientos:</span><span class="sxs-lookup"><span data-stu-id="2ede4-207">If you want to play a message on holidays, select the **Play a message during holidays** check box, and then specify the message to play by doing one of the following:</span></span>
    
      - <span data-ttu-id="2ede4-208">Para escribir el mensaje como texto que se convertirá en voz para el autor de la llamada, haga clic en **Usar texto a voz** y después escriba el mensaje de bienvenida en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2ede4-208">To enter the message as text that is converted to speech for the caller, click **Use text-to-speech**, and then type the message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2ede4-p127">No incluya etiquetas HTML en el texto que especifique. Si incluye etiquetas HTML, recibirá un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p127">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="2ede4-p128">Para usar una grabación en un archivo de audio para el mensaje, haga clic en **Seleccionar una grabación**. Si desea cargar un archivo de audio nuevo, haga clic en el vínculo **una grabación**. En la nueva ventana del explorador, haga clic en **Examinar**, seleccione el archivo que desea usar y después haga clic en **Abrir**. Haga clic en **Cargar** para cargar el archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p128">To use an audio file recording for the message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2ede4-215">Todos los archivos de audio proporcionados por el usuario deben cumplir ciertos requisitos.</span><span class="sxs-lookup"><span data-stu-id="2ede4-215">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="2ede4-216">Para obtener detalles sobre los formatos de archivo de audio admitidos, consulte <A href="lync-server-2013-technical-requirements-for-response-group.md">requisitos técnicos para el grupo de respuesta de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-216">For details about supported audio file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

26. <span data-ttu-id="2ede4-217">Especifique cómo abordar las llamadas tras la reproducción del mensaje (si se ha configurado uno):</span><span class="sxs-lookup"><span data-stu-id="2ede4-217">Specify how to handle calls after the message is played (if a message is configured):</span></span>
    
      - <span data-ttu-id="2ede4-218">Para desconectar la llamada, haga clic en **Desconectar llamada**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-218">To disconnect the call, click **Disconnect Call**.</span></span>
    
      - <span data-ttu-id="2ede4-219">Para desviar la llamada al correo de voz, haga clic en **Desviar a correo de voz** y escriba la dirección de correo de voz.</span><span class="sxs-lookup"><span data-stu-id="2ede4-219">To forward the call to voice mail, click **Forward to voice mail**, and then type the voice mail address.</span></span> <span data-ttu-id="2ede4-220">El formato de la dirección de correo de voz es \<username\> @ \<domainName\> (por ejemplo, Bob@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="2ede4-220">The format for the voice mail address is \<username\>@\<domainName\> (for example, bob@contoso.com).</span></span>
    
      - <span data-ttu-id="2ede4-221">Para desviar la llamada a otro usuario, haga clic en **Desviar a URI del SIP** y escriba la dirección de usuario.</span><span class="sxs-lookup"><span data-stu-id="2ede4-221">To forward the call to another user, click **Forward to SIP URI**, and then type a user address.</span></span> <span data-ttu-id="2ede4-222">El formato de la dirección de usuario es \<username\> @ \<domainName\> .</span><span class="sxs-lookup"><span data-stu-id="2ede4-222">The format for the user address is \<username\>@\<domainName\>.</span></span>
    
      - <span data-ttu-id="2ede4-223">Para desviar la llamada a otro número de teléfono, haga clic en **Desviar a número de teléfono** y escriba el número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="2ede4-223">To forward the call to another telephone number, click **Forward to telephone number**, and then type the telephone number.</span></span> <span data-ttu-id="2ede4-224">El formato del número de teléfono es \<number\> @ \<domainName\> (por ejemplo, + 14255550121@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="2ede4-224">The format for the telephone number is \<number\>@\<domainName\> (for example, +14255550121@contoso.com).</span></span> <span data-ttu-id="2ede4-225">El nombre de dominio se usa para redirigir al autor de la llamada al destino correcto.</span><span class="sxs-lookup"><span data-stu-id="2ede4-225">The domain name is used to route the caller to the correct destination.</span></span>

27. <span data-ttu-id="2ede4-226">En el **Paso 6 Configurar una cola**, en **Seleccione la cola que recibirá las llamadas**, seleccione la cola donde desea que los autores de las llamadas se mantengan en espera hasta que un agente esté disponible.</span><span class="sxs-lookup"><span data-stu-id="2ede4-226">Under **Step 6 Configure a Queue**, in **Select the queue that will receive the calls**, select the queue that you want to hold callers until an agent becomes available.</span></span>

28. <span data-ttu-id="2ede4-227">En el **Paso 7 Configurar música en espera**, elija la música que desea que escuchen los autores de las llamadas mientras esperan a un agente; para ello lleve a cabo uno de procedimientos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2ede4-227">Under **Step 7 Configure Music on Hold**, choose the music you want callers to listen to while waiting for an agent by doing one of the following:</span></span>
    
      - <span data-ttu-id="2ede4-228">Para usar la grabación habitual de música en espera, haga clic en **Usar predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-228">To use the default music-on-hold recording, click **Use default**.</span></span>
    
      - <span data-ttu-id="2ede4-p133">Para usar una grabación de un archivo de audio para la música en espera, haga clic en **Seleccionar un archivo de música**. Si desea cargar un archivo de audio nuevo, haga clic en el vínculo **un archivo de música**. En la nueva ventana del explorador, haga clic en **Examinar**, seleccione el archivo que desea usar y después haga clic en **Abrir**. Haga clic en **Cargar** para cargar el archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p133">To use an audio file recording for the music on hold, click **Select a music file**. If you want to upload a new audio file, click the **a music file** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2ede4-233">Todos los archivos de audio proporcionados por el usuario deben cumplir ciertos requisitos.</span><span class="sxs-lookup"><span data-stu-id="2ede4-233">All user provided audio files must meet certain requirements.</span></span> <span data-ttu-id="2ede4-234">Para obtener detalles sobre los formatos de archivo de audio admitidos, consulte <A href="lync-server-2013-technical-requirements-for-response-group.md">requisitos técnicos para el grupo de respuesta de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-234">For details about supported audio file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

29. <span data-ttu-id="2ede4-235">Haga clic en **Implementar**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-235">Click **Deploy**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-create-or-modify-a-hunt-group-workflow"></a><span data-ttu-id="2ede4-236">Para usar Windows PowerShell para crear o modificar un flujo de trabajo de grupo de captura</span><span class="sxs-lookup"><span data-stu-id="2ede4-236">To use Windows PowerShell to create or modify a hunt group workflow</span></span>

1.  <span data-ttu-id="2ede4-237">Inicie sesión como miembro del grupo RTCUniversalServerAdmins o como miembro de uno de los roles administrativos predefinidos que admiten el Grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ede4-237">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="2ede4-238">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-238">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="2ede4-p135">Cree el mensaje de bienvenida que se reproducirá y guárdelo en una variable. En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="2ede4-p135">Create the prompt to be played for the welcome message, and save it in a variable. At the command line, run:</span></span>
    
        $promptWM = New-CsRgsPrompt -TextToSpeechPrompt "<text for TTS prompt>"
    
    <span data-ttu-id="2ede4-241">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2ede4-241">For example:</span></span>
    
        $promptWM = New-CsRgsPrompt -TextToSpeechPrompt "Welcome to Contoso. Please wait for an available agent."
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-242">Para usar un archivo de audio para el mensaje, ejecute el cmdlet <STRONG>Import-CsRgsAudioFile</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-242">To use an audio file for the prompt, use the <STRONG>Import-CsRgsAudioFile</STRONG> cmdlet.</span></span> <span data-ttu-id="2ede4-243">Para obtener más información, consulte <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span><span class="sxs-lookup"><span data-stu-id="2ede4-243">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="2ede4-244">Obtenga la identidad de la cola o la pregunta a la que se dirigirán las llamadas.</span><span class="sxs-lookup"><span data-stu-id="2ede4-244">Get the identity of the queue or question where the calls will be directed.</span></span> <span data-ttu-id="2ede4-245">En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="2ede4-245">At the command line, run:</span></span>
    
        $qid = (Get-CsRgsQueue -Name "Help Desk").Identity
    
    <span data-ttu-id="2ede4-246">Para obtener detalles sobre la creación de la cola, vea [New-CsRgsQueue](https://docs.microsoft.com/powershell/module/skype/New-CsRgsQueue).</span><span class="sxs-lookup"><span data-stu-id="2ede4-246">For details about creating the queue, see [New-CsRgsQueue](https://docs.microsoft.com/powershell/module/skype/New-CsRgsQueue).</span></span>

5.  <span data-ttu-id="2ede4-p138">Defina la acción que se ejecutará cuando un flujo de trabajo se abra en horas de trabajo y guárdela en una variable. En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="2ede4-p138">Define the default action to be taken when a workflow is opened during business hours, and save it in a variable. At the command line, run:</span></span>
    
        $actionWM = New-CsRgsCallAction -Prompt <saved prompt from previous step> -Action <action to be taken> -QueueID $qid
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-p139">Para los flujos de trabajo de grupo de búsqueda, la acción habitual será dirigir la llamada a una cola. Este parámetro se usa para los flujos de trabajo activos. No se necesita para los flujos de trabajo inactivos.</span><span class="sxs-lookup"><span data-stu-id="2ede4-p139">For hunt group workflows, the default action must direct the call to a queue. This is parameter is required for active workflows. It is not required for inactive workflows.</span></span>

    
    </div>
    
    <span data-ttu-id="2ede4-252">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2ede4-252">For example:</span></span>
    
        $actionWM = New-CsRgsCallAction -Prompt $promptWM -Action TransferToQueue -QueueID $qid.Identity

6.  <span data-ttu-id="2ede4-253">Si desea definir horas laborables y vacaciones, debe crearlas antes de crear o modificar el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2ede4-253">If you want to define business hours and holidays, you need to create them before you create or modify the workflow.</span></span> <span data-ttu-id="2ede4-254">Para obtener más información, consulte [(opcional) definir las horas de trabajo del grupo de respuesta en Lync server 2013](lync-server-2013-optional-define-response-group-business-hours.md) y [(opcional) definir conjuntos de días festivos de grupos de respuesta en Lync Server 2013](lync-server-2013-optional-define-response-group-holiday-sets.md).</span><span class="sxs-lookup"><span data-stu-id="2ede4-254">For details, see [(Optional) Define Response Group business hours in Lync Server 2013](lync-server-2013-optional-define-response-group-business-hours.md) and [(Optional) Define Response Group holiday sets in Lync Server 2013](lync-server-2013-optional-define-response-group-holiday-sets.md).</span></span>

7.  <span data-ttu-id="2ede4-255">Si desea tener mensajes para las llamadas que se reciben en un horario no laborable o en época de vacaciones, use el cmdlet **New-CsRgsPrompt** para definir el mensaje y el cmdlet **New-CsRgsCallAction** para definir la acción que se ejecutará después del mensaje.</span><span class="sxs-lookup"><span data-stu-id="2ede4-255">If you want to have prompts for calls that are received out of business hours or on holidays, use the **New-CsRgsPrompt** cmdlet to define the prompt, and use the **New-CsRgsCallAction** to define the action to be taken after the prompt.</span></span> <span data-ttu-id="2ede4-256">Para obtener más información, vea [New-CsRgsPrompt](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt) y [New-CsRgsCallAction](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction).</span><span class="sxs-lookup"><span data-stu-id="2ede4-256">For details, see [New-CsRgsPrompt](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt) and [New-CsRgsCallAction](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction).</span></span>

8.  <span data-ttu-id="2ede4-257">Recupere el nombre del servicio del grupo de respuesta de Lync Server y asígnelo a una variable.</span><span class="sxs-lookup"><span data-stu-id="2ede4-257">Retrieve the service name for the Lync Server Response Group service and assign it to a variable.</span></span> <span data-ttu-id="2ede4-258">En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="2ede4-258">At the command, run:</span></span>
    
        $serviceId="service:"+(Get-CSService | ?{$_.Applications -like "*RGS*"}).ServiceId;

9.  <span data-ttu-id="2ede4-259">Cree o modifique el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2ede4-259">Create or modify the workflow.</span></span> <span data-ttu-id="2ede4-260">Para crear un flujo de trabajo, use **New-CsRgsWorkflow**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-260">To create a workflow, use **New-CsRgsWorkflow**.</span></span> <span data-ttu-id="2ede4-261">Para modificar un flujo de trabajo, use **Set-CsRgsWorkflow**.</span><span class="sxs-lookup"><span data-stu-id="2ede4-261">To modify a workflow, use **Set-CsRgsWorkflow**.</span></span> <span data-ttu-id="2ede4-262">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2ede4-262">At the command line, type:</span></span>
    
        $workflowHG = New-CsRgsWorkflow -Parent <service ID for the Response Group service> -Name "<hunt group name>" [-Description "<hunt group description>"] -PrimaryUri "<SIP address for the workflow>" [-LineUri "<Phone number for the workflow>"] [-DisplayNumber "<Phone number displayed in Lync>"] [-Active <$true | $false>] [-Anonymous <$true | $false>] [-DefaultAction <variable from preceding step>] [-EnabledForFederation <$true | $false>] [-Managed <$true | $false>] [-MangersByUri <SIP addresses for Response Group Managers who can manage the workflow>]
    
    <span data-ttu-id="2ede4-263">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2ede4-263">For example:</span></span>
    
        $workflowHG = New-CsRgsWorkflow -Parent $serviceID -Name "Human Resources" -Description "Human Resources workflow" -PrimaryUri "sip:humanresources@contoso.com" -LineUri "TEL:+14255551219" -DisplayNumber "555-1219" -Active $true -Anonymous $true -DefaultAction $actionWM -EnabledForFederation $false -Managed $true -ManagersByUri "sip:bob@contoso.com", "mindy@contoso.com"
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="2ede4-264">Todos los usuarios que hayan sido designados administradores de flujos de trabajo deben tener asignado el rol CsResponseGroupManager.</span><span class="sxs-lookup"><span data-stu-id="2ede4-264">All users who are designated managers for workflows must be assigned the CsResponseGroupManager role.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ede4-265">Para obtener detalles sobre parámetros opcionales adicionales, vea <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsWorkflow">New-CsRgsWorkflow</A> o <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsRgsWorkflow">set-CsRgsWorkflow</A></span><span class="sxs-lookup"><span data-stu-id="2ede4-265">For details about additional optional parameters, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsWorkflow">New-CsRgsWorkflow</A> or <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsRgsWorkflow">Set-CsRgsWorkflow</A></span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2ede4-266">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ede4-266">See Also</span></span>


[<span data-ttu-id="2ede4-267">Faculta Definir conjuntos de días festivos de grupos de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ede4-267">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)  


[<span data-ttu-id="2ede4-268">Faculta Definir las horas de trabajo del grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ede4-268">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)  


[<span data-ttu-id="2ede4-269">Nuevo: CsRgsWorkflow</span><span class="sxs-lookup"><span data-stu-id="2ede4-269">New-CsRgsWorkflow</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsWorkflow)  
[<span data-ttu-id="2ede4-270">Set-CsRgsWorkflow</span><span class="sxs-lookup"><span data-stu-id="2ede4-270">Set-CsRgsWorkflow</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsRgsWorkflow)  
[<span data-ttu-id="2ede4-271">New-CsRgsPrompt</span><span class="sxs-lookup"><span data-stu-id="2ede4-271">New-CsRgsPrompt</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt)  
[<span data-ttu-id="2ede4-272">Nuevo: CsRgsCallAction</span><span class="sxs-lookup"><span data-stu-id="2ede4-272">New-CsRgsCallAction</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction)  
  

<span data-ttu-id="2ede4-273"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2ede4-273"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

