---
title: Publicación de Office Web Apps Server con un servidor proxy inverso
description: Publicar Office Web Apps Server con un servidor proxy inverso.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publishing Office Web Apps Server using a reverse proxy server
ms:assetid: 0babe39f-c4b9-46f0-995a-33dc99c2be03
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204665(v=OCS.15)
ms:contentKeyID: 48183384
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 888399e315d90624ba41e23e173fa33813a92b43
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399041"
---
# <a name="publishing-office-web-apps-server-in-lync-server-2013-using-a-reverse-proxy-server"></a><span data-ttu-id="9d9d6-103">Publicación de Office Web Apps Server en Lync Server 2013 con un servidor proxy inverso</span><span class="sxs-lookup"><span data-stu-id="9d9d6-103">Publishing Office Web Apps Server in Lync Server 2013 using a reverse proxy server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d9d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d9d6-104">

<span> </span></span></span>

<span data-ttu-id="9d9d6-105">_**Última modificación del tema:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="9d9d6-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="9d9d6-106">Si quiere que los usuarios externos (es decir, los usuarios que inician sesión desde fuera del firewall de su organización) tengan acceso a las presentaciones de PowerPoint de Office Web Apps Server, tendrá que usar Office Web Apps Server y un servidor proxy inverso, como Microsoft Forefront Threat Management Gateway.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-106">If you want external users (that is, users logging on from outside your organization’s firewall) to have access to Office Web Apps Server PowerPoint presentations then you will need to use Office Web Apps Server and a reverse proxy server such as Microsoft Forefront Threat Management Gateway.</span></span> <span data-ttu-id="9d9d6-107">Eso también significa que necesitará crear y configurar una regla de publicación de sitios web; esa regla le ayudará a garantizar que los usuarios puedan conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-107">That also means that you will need to create and configure a website publishing rule; that rule will help ensure that users are able to connect to the server.</span></span> <span data-ttu-id="9d9d6-108">Si no necesita proporcionar acceso a usuarios externos, no necesita configurar una regla de publicación de sitios Web.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-108">If you do not need to provide access to external users then you do not need to configure a website publishing rule.</span></span>

<span data-ttu-id="9d9d6-109">Para configurar una regla de publicación de sitios web en Forefront Threat Management Gateway, complete el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="9d9d6-109">To configure a website publishing rule in Forefront Threat Management Gateway complete the following procedure:</span></span>

1.  <span data-ttu-id="9d9d6-110">Haga clic en **Inicio**, haga clic en **todos los programas**, **Microsoft Forefront TMG** y, a continuación, haga clic en **Administración de Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-110">Click **Start**, click **All Programs**, click **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="9d9d6-111">En Forefront TMG, haga clic con el botón derecho en **Directiva de Firewall**, seleccione **nuevo** y, a continuación, haga clic en regla de **publicación de sitio web**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-111">In Forefront TMG, right-click **Firewall Policy**, point to **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="9d9d6-112">En el Asistente para nueva regla de publicación de Web, en la página asistente **para nueva regla de publicación de web** , escriba un nombre para la nueva regla en el cuadro Nombre de la **regla de publicación de web** (por ejemplo, regla de **Office Web Apps Server**) y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-112">In the New Web Publishing Rule Wizard, on the **Welcome to the New Web Publishing Rule Wizard** page, type a name for your new rule in the **Web publishing rule name** box (for example, **Office Web Apps Server Rule**) and then click **Next**.</span></span>

4.  <span data-ttu-id="9d9d6-113">En la página **especificar acción de regla** , seleccione **permitir** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-113">On the **Specify Rule Action** page, select **Allow** and then click **Next**.</span></span>

5.  <span data-ttu-id="9d9d6-114">En la página **tipo de publicación** , seleccione **publicar un único sitio web o equilibrador de carga** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-114">On the **Publishing Type** page, select **Publish a single Web site or load balancer** and then click **Next**.</span></span>

6.  <span data-ttu-id="9d9d6-115">En la página **seguridad de conexión de servidor** , seleccione **usar SSL para conectarse al servidor web o conjunto** de servidores publicado y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-115">On the **Server Connection Security** page, select **Use SSL to connect to the published Web server or server farm** and then click **Next**.</span></span>

7.  <span data-ttu-id="9d9d6-116">En la página **Internal Publishing details** , escriba el FQDN de su servidor de Office Web Apps (por ejemplo, **officewebapps01.contoso.com**) en el cuadro **nombre de sitio interno** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-116">On the **Internal Publishing Details** page, type the FQDN of your Office Web Apps server (for example, **officewebapps01.contoso.com**) in the **Internal site name** box and then click **Next**.</span></span> <span data-ttu-id="9d9d6-117">El nombre introducido en el cuadro **nombre de sitio interno** debe aparecer en el campo de asunto o en el campo de nombre alternativo de asunto del certificado que haya asignado a Office Web Apps Server.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-117">The name entered in the **Internal site name** box must appear in the Subject field or the Subject Alternative Name field of the certificate you have assigned to Office Web Apps Server.</span></span>

8.  <span data-ttu-id="9d9d6-118">En la página **Internal Publishing details** , escriba **/ \* *_ en el cuadro _* Path (optional)** y, a continuación, haga clic en **Next**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-118">On the **Internal Publishing Details** page, type **/\**_ in the _\* Path (optional)*\* box and then click **Next**.</span></span> <span data-ttu-id="9d9d6-119">La \* Sintaxis/ayuda a garantizar que todas las carpetas y subcarpetas del sitio estén publicadas.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-119">The /\* syntax will help ensure that all the folders and subfolders for the site are published.</span></span>

9.  <span data-ttu-id="9d9d6-120">En la página **detalles de nombre público** , seleccione **este nombre de dominio (escriba a continuación)** en la lista desplegable **aceptar solicitudes de** y, a continuación, escriba el nombre completo de su servidor de Office Web Apps en el cuadro Nombre público.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-120">On the **Public Name Details** page, select **This domain name (type below)** from the **Accept requests for** drop-down list and then type the fully qualified for your Office Web Apps Server in the Public name box.</span></span> <span data-ttu-id="9d9d6-121">Este nombre debe ser el nombre usado para acceder a su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-121">This name should be the name used to access your website.</span></span> <span data-ttu-id="9d9d6-122">Por ejemplo, si se obtiene acceso a su sitio con la dirección URL http://officewebapps01.contoso.com , debe escribir **officewebapps01.contoso.com** en el cuadro **nombre público** .</span><span class="sxs-lookup"><span data-stu-id="9d9d6-122">For example, if your site is accessed using the URL http://officewebapps01.contoso.com then you should enter **officewebapps01.contoso.com** in the **Public name** box.</span></span>

10. <span data-ttu-id="9d9d6-123">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-123">Click **Next**.</span></span>

11. <span data-ttu-id="9d9d6-124">En la página **seleccionar escucha de web** , haga clic en **nuevo**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-124">On the **Select Web Listener** page, click **New**.</span></span>

12. <span data-ttu-id="9d9d6-125">En el Asistente para nueva definición de escucha de Web, escriba un nombre para la nueva escucha de Web (por ejemplo, **SSL**) en el cuadro Nombre de la **escucha de web** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-125">In the New Web Listener Definition Wizard, type a name for the new Web listener (for example, **SSL**) in the **Web listener name** box and then click **Next**.</span></span>

13. <span data-ttu-id="9d9d6-126">En la página **seguridad de conexión de cliente** , seleccione **requerir conexiones seguras SSL con los clientes** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-126">On the **Client Connection Security** page, select **Require SSL secured connections with clients** and then click **Next**.</span></span>

14. <span data-ttu-id="9d9d6-127">En la página **direcciones IP de escucha de web** , seleccione **externo**, seleccione **interno** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-127">On the **Web Listener IP Addresses** page, select **External**, select **Internal**, and then click **Next**.</span></span>

15. <span data-ttu-id="9d9d6-128">En la página **certificados SSL de escucha** , seleccione **usar un único certificado para esta escucha de web** y, a continuación, haga clic en **seleccionar certificado**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-128">On the **Listener SSL Certificates** page, select **Use a single certificate for this Web Listener** and then click **Select Certificate**.</span></span>

16. <span data-ttu-id="9d9d6-129">En el cuadro de diálogo **seleccionar certificado** , seleccione el certificado que se usará para esta escucha de web y, a continuación, haga clic en **seleccionar**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-129">In the **Select Certificate** dialog box, select the certificate to be used for this Web Listener and then click **Select**.</span></span>

17. <span data-ttu-id="9d9d6-130">En la página **certificados SSL de escucha** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-130">On the **Listener SSL Certificates** page, click **Next**.</span></span>

18. <span data-ttu-id="9d9d6-131">En la **página Configuración de autenticación** , seleccione **sin autenticación** en la lista desplegable **Seleccione cómo los clientes proporcionarán las credenciales a Forefront TMG** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-131">On the **Authentication Settings** page, select **No Authentication** from the **Select how clients will provide credentials to Forefront TMG** drop-down list, and then click **Next**.</span></span>

19. <span data-ttu-id="9d9d6-132">En la página **configuración de inicio de sesión único** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-132">On the **Single Sign On Settings** page, click **Next**.</span></span>

20. <span data-ttu-id="9d9d6-133">En la página **finalización del Asistente para nueva escucha de web** , revise el Resumen de las opciones de configuración que ha realizado.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-133">On the **Completing the New Web Listener Wizard** page, review the summary of the configuration choices you have made.</span></span> <span data-ttu-id="9d9d6-134">Cuando esté listo, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-134">When ready, click **Finish**.</span></span>

21. <span data-ttu-id="9d9d6-135">En la página **seleccionar escucha de web** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-135">On the **Select Web Listener** page, click **Next**.</span></span>

22. <span data-ttu-id="9d9d6-136">En la página **delegación de autenticación** , seleccione **sin delegación, pero el cliente puede autenticar directamente** desde el **Seleccione el método usado por Forefront TMG para autenticarse en la lista desplegable servidor Web publicado** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-136">On the **Authentication Delegation** page, select **No delegation, but client may authenticate directly** from the **Select the method used by Forefront TMG to authenticate to the published Web server** drop-down list and then click **Next**.</span></span>

23. <span data-ttu-id="9d9d6-137">En la página **conjuntos de usuarios** , confirme que aparecen los conjuntos de usuarios adecuados.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-137">On the **User Sets** page, confirm that the appropriate user sets are listed.</span></span> <span data-ttu-id="9d9d6-138">De forma predeterminada, este es el conjunto de usuarios de **todos los usuarios** .</span><span class="sxs-lookup"><span data-stu-id="9d9d6-138">By default, this is the **All Users** user set.</span></span> <span data-ttu-id="9d9d6-139">Haga clic en **Agregar** para agregar otros conjuntos de usuarios que haya definido.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-139">Click **Add** to add other user sets you may have defined.</span></span> <span data-ttu-id="9d9d6-140">Cuando haya terminado, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-140">When complete, click **Next**.</span></span>

24. <span data-ttu-id="9d9d6-141">En la página **finalización del Asistente para nueva regla de publicación de web** , haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-141">On the **Completing the New Web Publishing Rule Wizard** page, click **Finish**.</span></span>

<span data-ttu-id="9d9d6-142">Tenga en cuenta que hacer clic en **Finalizar** no significa que haya completado el proceso; es decir, esto no aplica automáticamente y habilita la nueva regla.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-142">Note that clicking **Finish** does not mean that you completed the process; that is, this does not automatically apply and enable the new rule.</span></span> <span data-ttu-id="9d9d6-143">En su lugar, tendrá que hacer clic en el botón **aplicar** que aparecerá en la interfaz de usuario de Forefront TMG.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-143">Instead, you will need to click the **Apply** button that will appear in the Forefront TMG user interface.</span></span> <span data-ttu-id="9d9d6-144">Al hacer clic en **aplicar** el cuadro de diálogo **Descripción de cambio de configuración** aparecerá.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-144">When you click **Apply** the **Configuration Change Description** dialog box will appear.</span></span> <span data-ttu-id="9d9d6-145">Haga clic en **aplicar** en ese cuadro de diálogo para habilitar la nueva regla de publicación.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-145">Click **Apply** in that dialog box to enable the new publishing rule.</span></span>

<span data-ttu-id="9d9d6-146">Una vez que se haya aplicado la nueva regla, tendrá que realizar algunas modificaciones menores en la regla para asegurarse de que los usuarios pueden usar las nuevas capacidades de presentación de PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-146">After your new rule has been applied, you will then need to make some minor modifications to the rule to make sure that users can use the new PowerPoint presentation capabilities.</span></span> <span data-ttu-id="9d9d6-147">Para ello, realice el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="9d9d6-147">To do that, complete the following procedure:</span></span>

1.  <span data-ttu-id="9d9d6-148">En Forefront TMG, haga clic con el botón secundario en el nombre de la nueva regla de publicación y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-148">In Forefront TMG, right-click the name of the new publishing rule and then click **Properties**.</span></span>

2.  <span data-ttu-id="9d9d6-149">En el cuadro de diálogo **propiedades** , en la pestaña **para** , seleccione la opción **reenviar el encabezado de host original en lugar del real**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-149">In the **Properties** dialog box, on the **To** tab, select the option **Forward the original host header instead of the actual one**.</span></span>

3.  <span data-ttu-id="9d9d6-150">En la pestaña **tráfico** , haga clic en **filtrado** y, a continuación, haga clic en **configurar http**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-150">On the **Traffic** tab, click **Filtering** and then click **Configure HTTP**.</span></span>

4.  <span data-ttu-id="9d9d6-151">En el cuadro de diálogo **configurar directiva http para la regla** , desactive la casilla **comprobar normalización** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-151">In the **Configuring HTTP policy for rule** dialog box, clear the **Verify normalization** check box and then click **OK**.</span></span>

5.  <span data-ttu-id="9d9d6-152">En el cuadro de diálogo **propiedades** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-152">In the **Properties** dialog box, click **OK**.</span></span>

6.  <span data-ttu-id="9d9d6-153">En Forefront TMG, haga clic en **aplicar** para habilitar los cambios.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-153">In Forefront TMG, click **Apply** to enable the changes.</span></span> <span data-ttu-id="9d9d6-154">Cuando aparezca el cuadro de diálogo **Descripción de cambio de configuración** , haga clic en **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="9d9d6-154">When the **Configuration Change Description** dialog box appears, click **Apply**.</span></span>

<span data-ttu-id="9d9d6-155">Después de completar la instalación, puede probar su servidor de Office Web Apps con los procedimientos del tema [validar la configuración de Office Web Apps Server en Lync server 2013](lync-server-2013-validating-the-configuration-of-office-web-apps-server.md).</span><span class="sxs-lookup"><span data-stu-id="9d9d6-155">After completing the installation you can test your Office Web Apps Server using the procedures in the topic [Validating the configuration of Office Web Apps Server in Lync Server 2013](lync-server-2013-validating-the-configuration-of-office-web-apps-server.md).</span></span>

<span data-ttu-id="9d9d6-156"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d9d6-156"></div>

<span> </span>

</div>

</div>

</span></span></div>

