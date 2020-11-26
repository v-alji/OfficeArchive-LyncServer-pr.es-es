---
title: 'Lync Server 2013: crear o modificar una cola'
description: 'Lync Server 2013: crear o modificar una cola.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a queue
ms:assetid: b9d6366a-839f-4651-a01d-9254546cadeb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205207(v=OCS.15)
ms:contentKeyID: 48185247
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cbd8d6d00df8d6a09ef5861d876bd1363db09e3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431760"
---
# <a name="create-or-modify-a-queue-in-lync-server-2013"></a><span data-ttu-id="246cf-103">Crear o modificar una cola en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="246cf-103">Create or modify a queue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="246cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="246cf-104">

<span> </span></span></span>

<span data-ttu-id="246cf-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="246cf-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="246cf-106">Use uno de los procedimientos siguientes para crear o modificar una cola.</span><span class="sxs-lookup"><span data-stu-id="246cf-106">Use one of the following procedures to create or modify a queue.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-create-or-modify-a-queue"></a><span data-ttu-id="246cf-107">Para usar el panel de control de Lync Server para crear o modificar una cola</span><span class="sxs-lookup"><span data-stu-id="246cf-107">To use Lync Server Control Panel to create or modify a queue</span></span>

1.  <span data-ttu-id="246cf-108">Inicie sesión como miembro del grupo RTCUniversalServerAdmins o como miembro de uno de los roles administrativos predefinidos que admiten el Grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="246cf-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="246cf-109">Si es uno de los administradores delegados del grupo de respuesta de un flujo de trabajo administrado, puede crear o modificar colas de grupo de respuesta y asignarlas a los flujos de trabajo que administre.</span><span class="sxs-lookup"><span data-stu-id="246cf-109">If you are one of the delegated Response Group Managers for a managed workflow, you can create or modify response group queues and assign them to the workflows that you manage.</span></span>

    
    </div>

2.  <span data-ttu-id="246cf-110">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="246cf-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="246cf-111">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="246cf-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="246cf-112">En la barra de navegación izquierda, haga clic en **Grupos de respuesta** y luego en **Cola**.</span><span class="sxs-lookup"><span data-stu-id="246cf-112">In the left navigation bar, click **Response Groups**, and then click **Queue**.</span></span>

4.  <span data-ttu-id="246cf-113">En la página **Cola**, lleve a cabo alguna de estas acciones:</span><span class="sxs-lookup"><span data-stu-id="246cf-113">On the **Queue** page, do one of the following:</span></span>
    
      - <span data-ttu-id="246cf-114">Para crear una cola nueva, haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="246cf-114">To create a new queue, click **New**.</span></span> <span data-ttu-id="246cf-115">En **Seleccionar un servicio**, escriba total o parcialmente el nombre del servicio **ApplicationServer** en cuyo campo de búsqueda desea agregar la cola.</span><span class="sxs-lookup"><span data-stu-id="246cf-115">In **Select a Service**, type part or all of the name of the **ApplicationServer** service where you want to add the queue in the search field.</span></span> <span data-ttu-id="246cf-116">En la lista de servicios que aparezca, haga clic en el servicio que desea y en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="246cf-116">In the resulting list of services, click the service that you want, and then click **OK**.</span></span>
    
      - <span data-ttu-id="246cf-p103">Para modificar una cola actual, escriba total o parcialmente el nombre de la cola en el campo de búsqueda. En la lista de colas que aparezca, haga clic sucesivamente en la cola que desea, **Editar** y **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="246cf-p103">To modify an existing queue, type all or part of the queue name in the search field. In the resulting list of queues, click the queue that you want, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="246cf-119">En **Nombre**, escriba un nombre de identificación para la cola.</span><span class="sxs-lookup"><span data-stu-id="246cf-119">In **Name**, type an identifying name for the queue.</span></span>

6.  <span data-ttu-id="246cf-120">En **Descripción**, escriba la descripción de la cola.</span><span class="sxs-lookup"><span data-stu-id="246cf-120">In **Description**, type a description for the queue.</span></span>

7.  <span data-ttu-id="246cf-p104">En **Grupos**, especifique los grupos que desea asignar a la cola. Lleve a cabo una de estas acciones:</span><span class="sxs-lookup"><span data-stu-id="246cf-p104">In **Groups**, specify the groups you want to assign to the queue. Do one of the following:</span></span>
    
      - <span data-ttu-id="246cf-p105">Para agregar un grupo a la cola, haga clic en **Seleccionar**. En el campo de búsqueda **Seleccionar grupos**, escriba total o parcialmente el nombre del grupo de agentes que desea asignar a la cola. A continuación, haga clic en el grupo de agentes que desea y en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="246cf-p105">To add a group to the queue, click **Select**. In the **Select Groups** search field, type all or part of the name of the agent group that you want to assign to the queue, click the agent group that you want, and then click **OK**.</span></span>
    
      - <span data-ttu-id="246cf-125">Para quitar un grupo de la cola, en la lista de grupos de agentes, haga clic en el grupo que desea quitar y en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="246cf-125">To remove a group from the queue, in the list of agent groups, click the group that you want to remove, and then click **Remove**.</span></span>
    
      - <span data-ttu-id="246cf-126">Para cambiar el orden en el que se buscan los agentes, en la lista de grupos de agentes, haga clic en un grupo y en la flecha arriba o abajo.</span><span class="sxs-lookup"><span data-stu-id="246cf-126">To change the order in which agents are searched, in the list of agent groups, click a group, and then click the up arrow or down arrow.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="246cf-p106">Cuando el servidor busca un agente disponible en la cola, usa el orden de grupo. Es decir, busca primero en el primer grupo de la lista, después en el segundo grupo y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="246cf-p106">When the server searches for an available agent for the queue, it uses group order. That is, the first group in the list is searched first, followed by the second group in the list, and so on.</span></span>

        
        </div>

8.  <span data-ttu-id="246cf-129">Para especificar un período máximo de tiempo de espera para el autor de una llamada antes de que un agente responda, active la casilla **Habilitar tiempo de espera de cola** y haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="246cf-129">To specify a maximum period of time for a caller to wait on hold before an agent answers the call, select the **Enable queue time-out** check box, and then do the following:</span></span>
    
    1.  <span data-ttu-id="246cf-130">En **Período de tiempo de espera (segundos)**, especifique el número máximo de segundos que el autor de una llamada debe esperar hasta que un agente responda.</span><span class="sxs-lookup"><span data-stu-id="246cf-130">In **Time-out period (seconds)**, specify the maximum number of seconds a caller waits for an agent to answer the call.</span></span>
    
    2.  <span data-ttu-id="246cf-131">En **Acción de llamada**, seleccione la acción que debe producirse cuando se agote el tiempo de espera de una llamada:</span><span class="sxs-lookup"><span data-stu-id="246cf-131">In **Call Action**, select the action that occurs when a call times out as follows:</span></span>
    
    <!-- end list -->
    
      - <span data-ttu-id="246cf-132">Para desconectar la llamada una vez transcurrido el tiempo de espera, haga clic en **Desconectar**.</span><span class="sxs-lookup"><span data-stu-id="246cf-132">To disconnect the call after the timeout, click **Disconnect**.</span></span>
    
      - <span data-ttu-id="246cf-133">Para desviar la llamada al correo de voz, haga clic en **reenviar al correo de voz** y, a continuación, en el campo **dirección SIP** , escriba una dirección de correo de voz con el formato SIP: \<username\> @ \<domainname\> (por ejemplo, SIP:Bob@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="246cf-133">To forward the call to voice mail, click **Forward to voice mail**, and then in the **SIP address** field, type a voice mail address in the format sip:\<username\>@\<domainname\> (for example, sip:bob@contoso.com).</span></span>
    
      - <span data-ttu-id="246cf-134">Para desviar la llamada a otro número de teléfono, haga clic en **reenviar a número de teléfono** y, a continuación, en el campo **dirección SIP** , escriba el número de teléfono en el formato SIP: \<number\> @ \<domainname\> (por ejemplo, SIP:+14255550121@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="246cf-134">To forward the call to another telephone number, click **Forward to telephone number**, and then in the **SIP address** field, type the telephone number in the format sip:\<number\>@\<domainname\> (for example, sip:+14255550121@contoso.com).</span></span>
    
      - <span data-ttu-id="246cf-135">Para desviar la llamada a otro usuario, haga clic en **reenviar a dirección SIP** y, a continuación, en el campo **dirección SIP** , escriba el URI para el usuario con el formato SIP: \<username\> @ \<domainname\> .</span><span class="sxs-lookup"><span data-stu-id="246cf-135">To forward the call to another user, click **Forward to SIP address**, and then in the **SIP address** field, type the URI for the user in the format sip:\<username\>@\<domainname\>.</span></span>
    
      - <span data-ttu-id="246cf-136">Para reenviar la llamada a otra cola, haga clic en **Desviar a otra cola** y busque la cola que desea usar.</span><span class="sxs-lookup"><span data-stu-id="246cf-136">To forward the call to another queue, click **Forward to another queue**, and then browse to the queue that you want to use.</span></span>

9.  <span data-ttu-id="246cf-137">Para especificar el número máximo de llamadas que se pueden incluir en una cola, active la casilla **Habilitar desbordamiento de cola** y haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="246cf-137">To specify a maximum number of calls that the queue can hold, select the **Enable queue overflow** check box, and then do the following:</span></span>
    
    1.  <span data-ttu-id="246cf-138">En **Número máximo de llamadas**, seleccione el número máximo de llamadas que desea incluir en la cola.</span><span class="sxs-lookup"><span data-stu-id="246cf-138">In **Maximum number of calls**, select the maximum number of calls that you want the queue to hold.</span></span>
    
    2.  <span data-ttu-id="246cf-139">En **Desviar la llamada**, seleccione la llamada que desea reenviar cuando la cola está completa: **Llamada más reciente** o **Llamada más antigua**.</span><span class="sxs-lookup"><span data-stu-id="246cf-139">In **Forward the call**, select which call is to be forwarded when the queue is full: **Newest Call** or **Oldest Call**.</span></span>
    
    3.  <span data-ttu-id="246cf-140">En **Acción de llamada**, seleccione la acción que debe producirse cuando se alcance el umbral de desbordamiento conforme a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="246cf-140">In **Call action**, select the action that occurs when the overflow threshold is met as follows:</span></span>
    
    <!-- end list -->
    
      - <span data-ttu-id="246cf-141">Para desconectar la llamada una vez transcurrido el tiempo de espera, haga clic en **Desconectar**.</span><span class="sxs-lookup"><span data-stu-id="246cf-141">To disconnect the call after the timeout, click **Disconnect**.</span></span>
    
      - <span data-ttu-id="246cf-142">Para desviar la llamada al correo de voz, haga clic en **reenviar al correo de voz** y, a continuación, en el campo **dirección SIP** , escriba una dirección de correo de voz con el formato SIP: \<username\> @ \<domainname\> (por ejemplo, SIP:Bob@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="246cf-142">To forward the call to voice mail, click **Forward to voice mail**, and then in the **SIP address** field, type a voice mail address in the format sip:\<username\>@\<domainname\> (for example, sip:bob@contoso.com).</span></span>
    
      - <span data-ttu-id="246cf-143">Para desviar la llamada a otro número de teléfono, haga clic en **reenviar a número de teléfono** y, a continuación, en el campo **dirección SIP** , escriba el número de teléfono en el formato SIP: \<number\> @ \<domainname\> (por ejemplo, SIP:+14255550121@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="246cf-143">To forward the call to another telephone number, click **Forward to telephone number**, and then in the **SIP address** field, type the telephone number in the format sip:\<number\>@\<domainname\> (for example, sip:+14255550121@contoso.com).</span></span>
    
      - <span data-ttu-id="246cf-144">Para desviar la llamada a otro usuario, haga clic en **reenviar a dirección SIP** y, a continuación, en el campo **dirección SIP** , escriba el URI para el usuario con el formato SIP: \<username\> @ \<domainname\> .</span><span class="sxs-lookup"><span data-stu-id="246cf-144">To forward the call to another user, click **Forward to SIP address**, and then in the **SIP address** field, type the URI for the user in the format sip:\<username\>@\<domainname\>.</span></span>
    
      - <span data-ttu-id="246cf-145">Para reenviar la llamada a otra cola, haga clic en **Desviar a otra cola** y busque la cola que desea usar.</span><span class="sxs-lookup"><span data-stu-id="246cf-145">To forward the call to another queue, click **Forward to another queue**, and then browse to the queue that you want to use.</span></span>

10. <span data-ttu-id="246cf-146">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="246cf-146">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-create-or-modify-a-queue"></a><span data-ttu-id="246cf-147">Para usar Windows PowerShell para crear o modificar una cola</span><span class="sxs-lookup"><span data-stu-id="246cf-147">To use Windows PowerShell to create or modify a queue</span></span>

1.  <span data-ttu-id="246cf-148">Inicie sesión como miembro del grupo RTCUniversalServerAdmins o como miembro de uno de los roles administrativos predefinidos que admiten el Grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="246cf-148">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="246cf-149">Si es uno de los administradores delegados del grupo de respuesta de un flujo de trabajo administrado, puede crear colas y grupos de agentes, y asignar estos grupos a las colas.</span><span class="sxs-lookup"><span data-stu-id="246cf-149">If you are one of the delegated Response Group Managers for a managed workflow, you will be able to create agent groups and queues, and assign agent groups to queues.</span></span>

    
    </div>

2.  <span data-ttu-id="246cf-150">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="246cf-150">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="246cf-p107">Cree el aviso que debe reproducirse cuando se alcance el umbral de tiempo de espera de la cola y guárdelo en una variable. En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="246cf-p107">Create the prompt to be played when the queue timeout threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $promptTO = New-CsRgsPrompt -TextToSpeechPrompt "<text for TTS prompt>"
    
    <span data-ttu-id="246cf-153">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="246cf-153">For example:</span></span>
    
        "All agents are currently busy. Please call back later."
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="246cf-154">Para usar un archivo de audio para el mensaje, ejecute el cmdlet <STRONG>Import-CsRgsAudioFile</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="246cf-154">To use an audio file for the prompt, use the <STRONG>Import-CsRgsAudioFile</STRONG> cmdlet.</span></span> <span data-ttu-id="246cf-155">Para obtener más información, consulte <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span><span class="sxs-lookup"><span data-stu-id="246cf-155">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="246cf-p109">Defina la acción que debe realizarse cuando se alcance el umbral de tiempo de espera de la cola y guárdela en una variable. En la línea de comandos ejecute:</span><span class="sxs-lookup"><span data-stu-id="246cf-p109">Define the action to be taken when the queue timeout threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $actionTO = New-CsRgsCallAction -Prompt <saved prompt from previous step> -Action <action to be taken>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="246cf-158">Para obtener detalles sobre las posibles acciones y su sintaxis, vea <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">New-CsRgsCallAction</A>.</span><span class="sxs-lookup"><span data-stu-id="246cf-158">For details about possible actions and their syntax, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">New-CsRgsCallAction</A>.</span></span>

    
    </div>
    
    <span data-ttu-id="246cf-159">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="246cf-159">For example:</span></span>
    
        $action = New-CsRgsCallAction -Prompt $promptTO -Action Terminate

5.  <span data-ttu-id="246cf-p110">Cree el aviso que debe reproducirse cuando se alcance el umbral de desbordamiento de la cola y guárdelo en una variable. En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="246cf-p110">Create the prompt to be played when the queue overflow threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $promptOV = New-CsRgsPrompt -TextToSpeechPrompt "<text for TTS prompt>"
    
    <span data-ttu-id="246cf-162">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="246cf-162">For example:</span></span>
    
        $promptOV = New-CsRgsPrompt -TextToSpeechPrompt "Too many calls are waiting. Please call back later."
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="246cf-163">Para usar un archivo de audio para el mensaje, ejecute el cmdlet <STRONG>Import-CsRgsAudioFile</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="246cf-163">To use an audio file for the prompt, use the <STRONG>Import-CsRgsAudioFile</STRONG> cmdlet.</span></span> <span data-ttu-id="246cf-164">Para obtener más información, consulte <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span><span class="sxs-lookup"><span data-stu-id="246cf-164">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span></span>

    
    </div>

6.  <span data-ttu-id="246cf-p112">Defina la acción que debe realizarse cuando se alcance el umbral de desbordamiento de la cola y guárdela en una variable. En la línea de comandos ejecute:</span><span class="sxs-lookup"><span data-stu-id="246cf-p112">Define the action to be taken when the queue overflow threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $actionOV = New-CsRgsCallAction -Prompt <saved prompt from previous step> -Action <action to be taken>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="246cf-167">Para obtener detalles sobre las posibles acciones y su sintaxis, vea <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">New-CsRgsCallAction</A>.</span><span class="sxs-lookup"><span data-stu-id="246cf-167">For details about possible actions and their syntax, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">New-CsRgsCallAction</A>.</span></span>

    
    </div>
    
    <span data-ttu-id="246cf-168">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="246cf-168">For example:</span></span>
    
        $action = New-CsRgsCallAction -Prompt $promptOV -Action Terminate

7.  <span data-ttu-id="246cf-p113">Recupere el nombre de servicio del servicio Grupo de respuestas y asígnelo a una variable. En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="246cf-p113">Retrieve the service name for the Response Group service and assign it to a variable. At the command line, run:</span></span>
    
        $serviceId="service:"+(Get-CSService | ?{$_.Applications -Like "*RGS*"}).ServiceId;

8.  <span data-ttu-id="246cf-p114">Obtenga la identidad del grupo de agentes que debe asignarse a la cola. En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="246cf-p114">Get the identity of the agent group to be assigned to the queue. At the command line, run:</span></span>
    
        $agid = (Get-CsRgsAgentGroup -Name "Help Desk").Identity;
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="246cf-173">Para obtener más información sobre cómo crear el grupo agente, consulte <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsAgentGroup">New-CsRgsAgentGroup</A></span><span class="sxs-lookup"><span data-stu-id="246cf-173">For details about creating the agent group, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsAgentGroup">New-CsRgsAgentGroup</A></span></span>

    
    </div>

9.  <span data-ttu-id="246cf-p115">Cree la cola. En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="246cf-p115">Create the queue. At the command line, run:</span></span>
    
        $q = New-CsRgsQueue -Parent <saved service ID from previous step> -Name "<name of queue>" [-Description "<description for queue>"] [-TimeoutThreshold <# seconds before call times out>] [-TimeoutAction <saved timeout action>] [-OverflowThreshold <# calls queue can hold>] [-OverflowCandidate <call to be acted on when overflow threshold met>] [-OverflowAction <saved overflow action>] [-AgentGroupIDList(<agent group identity>)];
    
    <span data-ttu-id="246cf-176">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="246cf-176">For example:</span></span>
    
        $q = New-CsRgsQueue -Parent $serviceId -Name "Help Desk" -Description "Contoso Help Desk" -TimeoutThreshold 300 -TimeoutAction $actionTO -OverflowThreshold 10 -OverflowCandidate NewestCall -OverflowAction $actionOV -AgentGroupIDList($agid.Identity;

10. <span data-ttu-id="246cf-p116">Confirme que la cola se ha creado. Ejecute:</span><span class="sxs-lookup"><span data-stu-id="246cf-p116">Confirm that the queue is created. Run:</span></span>
    
        Get-CsRgsQueue -Name "Help Desk"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="246cf-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="246cf-179">See Also</span></span>


[<span data-ttu-id="246cf-180">Nuevo: CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="246cf-180">New-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsQueue)  
[<span data-ttu-id="246cf-181">Set-CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="246cf-181">Set-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsRgsQueue)  
[<span data-ttu-id="246cf-182">New-CsRgsPrompt</span><span class="sxs-lookup"><span data-stu-id="246cf-182">New-CsRgsPrompt</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt)  
[<span data-ttu-id="246cf-183">Nuevo: CsRgsCallAction</span><span class="sxs-lookup"><span data-stu-id="246cf-183">New-CsRgsCallAction</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction)  
[<span data-ttu-id="246cf-184">Get-CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="246cf-184">Get-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsQueue)  
[<span data-ttu-id="246cf-185">Importar-CsRgsAudioFile</span><span class="sxs-lookup"><span data-stu-id="246cf-185">Import-CsRgsAudioFile</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile)  
[<span data-ttu-id="246cf-186">Remove-CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="246cf-186">Remove-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsRgsQueue)  
  

<span data-ttu-id="246cf-187"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="246cf-187"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

