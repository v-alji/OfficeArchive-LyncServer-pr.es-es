---
title: Configuración XMPP de ejemplo - Federación XMPP con Google Talk
description: 'Ejemplo de configuración XMPP: Federación XMPP con Google Talk.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428456"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a><span data-ttu-id="86963-103">Configuración XMPP de ejemplo en Lync Server 2013 - Federación XMPP con Google Talk</span><span class="sxs-lookup"><span data-stu-id="86963-103">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="86963-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="86963-104">

<span> </span></span></span>

<span data-ttu-id="86963-105">_**Última modificación del tema:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="86963-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="86963-106">Un ejemplo de configuración para implementar el proxy XMPP define una federación con Google Talk.</span><span class="sxs-lookup"><span data-stu-id="86963-106">An example configuration for deploying the XMPP Proxy defines a federation with Google Talk.</span></span>

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a><span data-ttu-id="86963-107">Configuración XMPP de ejemplo - Federación XMPP con Google Talk</span><span class="sxs-lookup"><span data-stu-id="86963-107">Example XMPP configuration – XMPP federation with Google Talk</span></span>

1.  <span data-ttu-id="86963-108">En el servidor front-end, abra el Asistente para la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="86963-108">On the Front End Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="86963-109">Haga clic en **instalar** o **actualizar el sistema Lync Server** y, a continuación, haga clic en **configurar** o **quitar los componentes de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="86963-109">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="86963-110">**Vuelva a** hacer clic en ejecutar.</span><span class="sxs-lookup"><span data-stu-id="86963-110">Click **Run Again**.</span></span>

2.  <span data-ttu-id="86963-111">En **instalación de los componentes de Lync Server**, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="86963-111">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="86963-112">La pantalla resumen mostrará las acciones a medida que se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="86963-112">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="86963-113">Una vez completada la implementación, haga clic en **Ver registro** para ver los archivos de registro disponibles.</span><span class="sxs-lookup"><span data-stu-id="86963-113">After the deployment is complete, click **View Log** to view available log files.</span></span> <span data-ttu-id="86963-114">Haga clic en **Finalizar** para completar la implementación.</span><span class="sxs-lookup"><span data-stu-id="86963-114">Click **Finish** to complete the deployment.</span></span>

3.  <span data-ttu-id="86963-115">En el servidor perimetral, abra el Asistente para la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="86963-115">On the Edge Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="86963-116">Haga clic en **instalar** o **actualizar el sistema Lync Server** y, a continuación, haga clic en **configurar** o **quitar los componentes de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="86963-116">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="86963-117">**Vuelva a** hacer clic en ejecutar.</span><span class="sxs-lookup"><span data-stu-id="86963-117">Click **Run Again**.</span></span>

4.  <span data-ttu-id="86963-118">Agregue Google Talk como socio XMPP permitido.</span><span class="sxs-lookup"><span data-stu-id="86963-118">Add Google Talk as an XMPP allowed partner.</span></span> <span data-ttu-id="86963-119">Actualmente, Google Talk solo admite conexiones TCP sin cifrar para la Federación de XMPP de servidor a servidor y solo admite el Dialback de servidor para la verificación de identidad.</span><span class="sxs-lookup"><span data-stu-id="86963-119">Google Talk currently only supports unencrypted, TCP connections for server-to-server XMPP federation and only supports Server Dialback for identity verification.</span></span> <span data-ttu-id="86963-120">(Consulte <http://xmpp.org/extensions/xep-0220.html> ).</span><span class="sxs-lookup"><span data-stu-id="86963-120">(See <http://xmpp.org/extensions/xep-0220.html>).</span></span>
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  <span data-ttu-id="86963-121">Para habilitar la Federación perimetral, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="86963-121">To enable Edge Federation, type the following:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  <span data-ttu-id="86963-122">En **instalación de los componentes de Lync Server**, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="86963-122">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="86963-123">La pantalla resumen mostrará las acciones a medida que se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="86963-123">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="86963-124">Una vez completada la implementación, haga clic en **Ver registro** para ver los archivos de registro disponibles.</span><span class="sxs-lookup"><span data-stu-id="86963-124">After the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="86963-125">Haga clic en **Finalizar** para completar la implementación.</span><span class="sxs-lookup"><span data-stu-id="86963-125">Click **Finish** to complete the deployment.</span></span>

7.  <span data-ttu-id="86963-126">En el servidor perimetral, en el Asistente de implementación de Lync Server, junto al **paso 3: solicitar, instalar o asignar certificados**, haga clic en **Ejecutar de nuevo**.</span><span class="sxs-lookup"><span data-stu-id="86963-126">On the Edge Server, in the Lync Server Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="86963-127">Si está implementando el servidor perimetral por primera vez, verá ejecutar en lugar de volver a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="86963-127">If you are deploying the Edge Server for the first time, you will see Run instead of Run Again.</span></span>

    
    </div>

8.  <span data-ttu-id="86963-128">En la página **Tareas de certificado disponibles**, haga clic en **Crear una nueva solicitud de certificado**.</span><span class="sxs-lookup"><span data-stu-id="86963-128">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

9.  <span data-ttu-id="86963-129">En la página **solicitud de certificado** , haga clic en certificado de **borde externo**.</span><span class="sxs-lookup"><span data-stu-id="86963-129">On the **Certificate Request** page, click **External Edge Certificate**.</span></span>

10. <span data-ttu-id="86963-130">En la página **solicitud inmediata o demorada** , active la casilla **preparar la solicitud ahora pero enviarla más tarde** .</span><span class="sxs-lookup"><span data-stu-id="86963-130">On the **Delayed or Immediate Request** page, select the **Prepare the request now, but send it later** check box.</span></span>

11. <span data-ttu-id="86963-131">En la página **archivo de solicitud de certificado** , escriba la ruta de acceso completa y el nombre del archivo en el que se va a guardar la solicitud (por ejemplo, c: \\ CERT \_ la \_ Edge. cer).</span><span class="sxs-lookup"><span data-stu-id="86963-131">On the **Certificate Request File** page, type the full path and file name of the file to which the request is to be saved (for example, c:\\cert\_exernal\_edge.cer).</span></span>

12. <span data-ttu-id="86963-132">En la página **especificar plantilla de certificado alternativa** , para usar una plantilla distinta de la plantilla predeterminada de WebServer, seleccione la casilla **Usar plantilla de certificado alternativa para la entidad emisora de certificados seleccionada** .</span><span class="sxs-lookup"><span data-stu-id="86963-132">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected certification authority** check box.</span></span>

13. <span data-ttu-id="86963-133">En la página **nombre y configuración de seguridad** , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="86963-133">On the **Name and Security Settings** page, do the following:</span></span>
    
    1.  <span data-ttu-id="86963-134">En **nombre descriptivo**, escriba un nombre para mostrar para el certificado.</span><span class="sxs-lookup"><span data-stu-id="86963-134">In **Friendly name**, type a display name for the certificate</span></span>
    
    2.  <span data-ttu-id="86963-135">En **longitud bit**, especifique la longitud en bits (normalmente, el valor predeterminado de **2048**).</span><span class="sxs-lookup"><span data-stu-id="86963-135">In **Bit length**, specify the bit length (typically, the default of **2048**)</span></span>
    
    3.  <span data-ttu-id="86963-136">Compruebe que la casilla **marcar clave privada de certificado como exportable** está seleccionada</span><span class="sxs-lookup"><span data-stu-id="86963-136">Verify that the **Mark certificate private key as exportable** check box is selected</span></span>

14. <span data-ttu-id="86963-137">En la página información de la **organización** , escriba el nombre de la organización y la unidad organizativa (por ejemplo, una división o un departamento).</span><span class="sxs-lookup"><span data-stu-id="86963-137">On the **Organization Information** page, type the name for the organization and the organizational unit (for example, a division or department)</span></span>

15. <span data-ttu-id="86963-138">En la página **información geográfica** , especifique la información de ubicación</span><span class="sxs-lookup"><span data-stu-id="86963-138">On the **Geographical Information** page, specify the location information</span></span>

16. <span data-ttu-id="86963-139">En la página **nombre de sujeto/nombres alternativos de asunto** , se muestra la información que el asistente rellenará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="86963-139">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span> <span data-ttu-id="86963-140">Si se necesitan nombres alternativos de asunto adicionales, debe especificarlos en los dos pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="86963-140">If additional subject alternative names are needed, you specify them in the next two steps</span></span>

17. <span data-ttu-id="86963-141">En la página **configuración del dominio SIP en la página de nombres alternativos de asunto (San)** , seleccione la casilla dominio para agregar un SIP.</span><span class="sxs-lookup"><span data-stu-id="86963-141">On the **SIP Domain Setting on Subject Alternate Names (SANs)** page, select the domain check box to add a sip.</span></span> <span data-ttu-id="86963-142">\<sipdomain\> entrada a la lista de nombres alternativos de asunto.</span><span class="sxs-lookup"><span data-stu-id="86963-142">\<sipdomain\> entry to the subject alternative names list.</span></span>

18. <span data-ttu-id="86963-143">En la página **configurar otros nombres alternativos de asunto** , especifique los nombres alternativos adicionales que sean obligatorios.</span><span class="sxs-lookup"><span data-stu-id="86963-143">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="86963-144">Si el proxy XMPP está instalado, de forma predeterminada, el nombre de dominio (por ejemplo, contoso.com) se rellena en las entradas SAN.</span><span class="sxs-lookup"><span data-stu-id="86963-144">If the XMPP proxy is installed, by default the domain name (such as contoso.com) is populated in the SAN entries.</span></span> <span data-ttu-id="86963-145">Si necesita más entradas, agréguelos en este paso.</span><span class="sxs-lookup"><span data-stu-id="86963-145">If you require more entries, add them in this step.</span></span>

    
    </div>

19. <span data-ttu-id="86963-146">En la página **solicitar Resumen** , revise la información del certificado que se va a usar para generar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="86963-146">On the **Request Summary** page, review the certificate information to be used to generate the request.</span></span>

20. <span data-ttu-id="86963-147">Cuando termine de ejecutarse los comandos, puede **ver el registro** o hacer clic en **siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="86963-147">After the commands finish running, you can **View Log**, or click **Next** to continue.</span></span>

21. <span data-ttu-id="86963-148">En la página de **archivo de solicitud de certificado** , puede ver el archivo de solicitud de firma de certificado generado (CSR) haciendo clic en **Ver** o salir del asistente de certificados haciendo clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="86963-148">On the **Certificate Request File** page, you can view the generated certificate signing request (CSR) file by clicking **View** or exit the Certificate Wizard by clicking **Finish**.</span></span>

22. <span data-ttu-id="86963-149">Copie el archivo de solicitud y envíelo a la entidad emisora de certificados pública.</span><span class="sxs-lookup"><span data-stu-id="86963-149">Copy the request file and submit to your public certification authority.</span></span>

23. <span data-ttu-id="86963-150">Después de recibir, importar y asignar el certificado público, debe detener y reiniciar los servicios del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="86963-150">After receiving, importing and assigning the public certificate, you must stop and restart the Edge Server services.</span></span> <span data-ttu-id="86963-151">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="86963-151">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**..</span></span> <span data-ttu-id="86963-152">En el shell de administración de Lync Server, escriba:</span><span class="sxs-lookup"><span data-stu-id="86963-152">In the Lync Server Management Shell, type:</span></span>
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. <span data-ttu-id="86963-153">Para configurar DNS para la Federación XMPP, agregue el siguiente registro SRV a DNS externo: \_ XMPP-Server. \_ TCP.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="86963-153">To configure DNS for XMPP federation, you add the following SRV record to external DNS:\_xmpp-server.\_tcp.\<domain name\></span></span> <span data-ttu-id="86963-154">El registro SRV se resolverá en el FQDN perimetral de acceso del servidor perimetral, con un valor de puerto de 5269</span><span class="sxs-lookup"><span data-stu-id="86963-154">The SRV record will resolve to the access edge FQDN of the Edge server, with a port value of 5269</span></span>

25. <span data-ttu-id="86963-155">Configure una nueva Directiva de acceso externo para habilitar todos los usuarios abriendo el shell de administración de Lync Server en un servidor front-end y escribiendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="86963-155">Configure a new External Access Policy to enable all users by opening the Lync Server Management Shell on a Front End Server and typing:</span></span>
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

<span data-ttu-id="86963-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="86963-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

