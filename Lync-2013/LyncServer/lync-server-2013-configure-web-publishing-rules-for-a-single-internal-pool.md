---
title: 'Lync Server 2013: Configurar las reglas de publicación web para un solo grupo de servidores interno'
description: 'Lync Server 2013: configurar reglas de publicación web para un único grupo interno.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure web publishing rules for a single internal pool
ms:assetid: 86ff4b2a-1ba9-46a2-a175-8b19e00a49dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429712(v=OCS.15)
ms:contentKeyID: 48184725
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45015c90fdac92fb488affc871f2cfaf9d7506a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433538"
---
# <a name="configure-web-publishing-rules-for-a-single-internal-pool-in-lync-server-2013"></a><span data-ttu-id="7187c-103">Configurar las reglas de publicación web para un solo grupo de servidores interno en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7187c-103">Configure web publishing rules for a single internal pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7187c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7187c-104">

<span> </span></span></span>

<span data-ttu-id="7187c-105">_**Última modificación del tema:** 2014-07-07_</span><span class="sxs-lookup"><span data-stu-id="7187c-105">_**Topic Last Modified:** 2014-07-07_</span></span>

<span data-ttu-id="7187c-106">Microsoft Forefront Threat Management Gateway 2010 y enrutamiento de solicitudes de aplicaciones de Internet Information Server (IIS ARR) usa reglas de publicación web para publicar recursos internos, como una dirección URL de una reunión, a usuarios de Internet.</span><span class="sxs-lookup"><span data-stu-id="7187c-106">Microsoft Forefront Threat Management Gateway 2010 and Internet Information Server Application Request Routing (IIS ARR) uses web publishing rules to publish internal resources, such as a meeting URL, to users on the Internet.</span></span>

<span data-ttu-id="7187c-107">Además de las direcciones URL de los servicios web para los directorios virtuales, también debe crear reglas de publicación para direcciones URL simples, la dirección URL de LyncDiscover y el servidor de Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="7187c-107">In addition to the Web Services URLs for the virtual directories, you must also create publishing rules for simple URLs, the LyncDiscover URL, and the Office Web Apps Server.</span></span> <span data-ttu-id="7187c-108">Para cada dirección URL simple, debe crear una regla individual en el proxy inverso que apunta a esa dirección URL simple.</span><span class="sxs-lookup"><span data-stu-id="7187c-108">For each simple URL, you must create an individual rule on the reverse proxy that points to that simple URL.</span></span>

<span data-ttu-id="7187c-109">Si implementa la movilidad y usa el descubrimiento automático, debe crear una regla de publicación para la dirección URL del servicio de detección automática externa.</span><span class="sxs-lookup"><span data-stu-id="7187c-109">If you are deploying mobility and using automatic discovery, you need to create a publishing rule for the external Autodiscover Service URL.</span></span> <span data-ttu-id="7187c-110">El descubrimiento automático también requiere reglas de publicación para la dirección URL de los servicios Web de Lync Server externo para el grupo de directores y el grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="7187c-110">Automatic discovery also requires publishing rules for the external Lync Server Web Services URL for your Director pool and Front End pool.</span></span> <span data-ttu-id="7187c-111">Para obtener información detallada sobre la creación de reglas de publicación web para el descubrimiento automático, consulte [configurar el proxy inverso para movilidad en Lync Server 2013](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="7187c-111">For details about creating the web publishing rules for automatic discovery, see [Configuring the reverse proxy for mobility in Lync Server 2013](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md).</span></span>

<span data-ttu-id="7187c-112">Use los procedimientos siguientes para crear reglas de publicación en Web.</span><span class="sxs-lookup"><span data-stu-id="7187c-112">Use the following procedures to create web publishing rules.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7187c-113">En estos procedimientos se supone que ha instalado la edición estándar de Forefront Threat Management Gateway (TMG) 2010 o que ha instalado y configurado Internet Information Server con la extensión de enrutamiento de solicitudes de aplicaciones (IIS ARR).</span><span class="sxs-lookup"><span data-stu-id="7187c-113">These procedures assume that you have installed the Standard Edition of Forefront Threat Management Gateway (TMG) 2010 or have installed and configured Internet Information Server with the Application request Routing (IIS ARR) extension.</span></span> <span data-ttu-id="7187c-114">Puede usar TMG o IIS ARR.</span><span class="sxs-lookup"><span data-stu-id="7187c-114">You use either TMG or IIS ARR.</span></span>



</div>

<div>

## <a name="to-create-a-web-server-publishing-rule-on-the-computer-running-tmg-2010"></a><span data-ttu-id="7187c-115">Para crear una regla de publicación de servidor Web en el equipo que ejecuta TMG 2010</span><span class="sxs-lookup"><span data-stu-id="7187c-115">To create a web server publishing rule on the computer running TMG 2010</span></span>

1.  <span data-ttu-id="7187c-116">Haga clic en **Inicio**, seleccione **programas**, **Microsoft Forefront TMG** y, a continuación, haga clic en **Administración de Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="7187c-116">Click **Start**, select **Programs**, select **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="7187c-117">En el panel izquierdo, expanda **ServerName**, haga clic con el botón secundario en **Directiva de Firewall**, seleccione **nuevo** y, después, haga clic en regla de **publicación de sitio web**.</span><span class="sxs-lookup"><span data-stu-id="7187c-117">In the left pane, expand **ServerName**, right-click **Firewall Policy**, select **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="7187c-118">En la página **Asistente para nueva regla de publicación de web** , escriba un nombre para mostrar para la regla de publicación (por ejemplo, LyncServerWebDownloadsRule).</span><span class="sxs-lookup"><span data-stu-id="7187c-118">On the **Welcome to the New Web Publishing Rule** page, type a display name for the publishing rule (for example, LyncServerWebDownloadsRule).</span></span>

4.  <span data-ttu-id="7187c-119">En la página **Seleccionar acción de regla** , seleccione **permitir**.</span><span class="sxs-lookup"><span data-stu-id="7187c-119">On the **Select Rule Action** page, select **Allow**.</span></span>

5.  <span data-ttu-id="7187c-120">En la página **tipo de publicación** , seleccione **publicar un único sitio web o un equilibrador de carga**.</span><span class="sxs-lookup"><span data-stu-id="7187c-120">On the **Publishing Type** page, select **Publish a single Web site or load balancer**.</span></span>

6.  <span data-ttu-id="7187c-121">En la página **seguridad de conexión de servidor** , seleccione **usar SSL para conectarse al servidor web o conjunto** de servidores publicado.</span><span class="sxs-lookup"><span data-stu-id="7187c-121">On the **Server Connection Security** page, select **Use SSL to connect to the published Web server or server farm**.</span></span>

7.  <span data-ttu-id="7187c-122">En la página **detalles internos de publicación** , escriba el nombre de dominio completo (FQDN) de la granja de servidores web interna que hospeda el contenido de la reunión y el contenido de la libreta de direcciones en el cuadro **nombre del sitio interno** .</span><span class="sxs-lookup"><span data-stu-id="7187c-122">On the **Internal Publishing Details** page, type the fully qualified domain name (FQDN) of the internal web farm that hosts your meeting content and Address Book content in the **Internal Site name** box.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7187c-123">Si su servidor interno es un servidor Standard Edition, este FQDN es el FQDN del servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="7187c-123">If your internal server is a Standard Edition server, this FQDN is the Standard Edition server FQDN.</span></span> <span data-ttu-id="7187c-124">Si su servidor interno es un grupo front-end, este FQDN es una IP virtual (VIP) de equilibrador de carga de hardware que equilibra la carga de los servidores internos de la granja de servidores Web.</span><span class="sxs-lookup"><span data-stu-id="7187c-124">If your internal server is a Front End pool, this FQDN is a hardware load balancer virtual IP (VIP) that load balances the internal web farm servers.</span></span> <span data-ttu-id="7187c-125">El servidor de TMG debe poder resolver el FQDN en la dirección IP del servidor Web interno.</span><span class="sxs-lookup"><span data-stu-id="7187c-125">The TMG server must be able to resolve the FQDN to the IP address of the internal web server.</span></span> <span data-ttu-id="7187c-126">Si el servidor de TMG no puede resolver el FQDN en la dirección IP correcta, puede seleccionar <STRONG>usar un nombre de equipo o una dirección IP para conectarse al servidor publicado</STRONG>y, a continuación, en el cuadro <STRONG>dirección IP</STRONG> <STRONG>o nombre del equipo</STRONG> , escriba la dirección IP del servidor Web interno.</span><span class="sxs-lookup"><span data-stu-id="7187c-126">If the TMG server is not able to resolve the FQDN to the proper IP address, you can select <STRONG>Use a computer name or IP address to connect to the published server</STRONG>, and then in the <STRONG>Computer name or</STRONG> <STRONG>IP address</STRONG> box, type the IP address of the internal web server.</span></span> <span data-ttu-id="7187c-127">Si lo hace, debe asegurarse de que el puerto 53 está abierto en el servidor de TMG y de que puede comunicarse con un servidor DNS que reside en la red perimetral.</span><span class="sxs-lookup"><span data-stu-id="7187c-127">If you do this, you must ensure that port 53 is open on the TMG server and that it can reach a DNS server that resides in the perimeter network.</span></span> <span data-ttu-id="7187c-128">También puede usar entradas en el archivo hosts local para proporcionar resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="7187c-128">You can also use entries in the local hosts file to provide name resolution.</span></span>

    
    </div>

8.  <span data-ttu-id="7187c-129">En la página **Internal Publishing details** , en la **ruta de acceso (opcional)** , escriba \* */\** _ como la ruta de acceso de la carpeta que se va a publicar.</span><span class="sxs-lookup"><span data-stu-id="7187c-129">On the **Internal Publishing Details** page, in the **Path (optional)** box, type \**/\** _ as the path of the folder to be published.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7187c-130">En el Asistente para la publicación de sitios web, solo puede especificar una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="7187c-130">In the website publishing wizard you can only specify one path.</span></span> <span data-ttu-id="7187c-131">Se pueden agregar rutas adicionales modificando las propiedades de la regla.</span><span class="sxs-lookup"><span data-stu-id="7187c-131">Additional paths can be added by modifying the properties of the rule.</span></span>

    
    </div>

9.  <span data-ttu-id="7187c-132">En la página _ \*detalles de nombre público\*\*, confirme que **este nombre de dominio** está seleccionado en **aceptar solicitudes de**, escriba el FQDN de servicios web externos en el cuadro **nombre público** .</span><span class="sxs-lookup"><span data-stu-id="7187c-132">On the _ *Public Name Details*\* page, confirm that **This domain name** is selected under **Accept Requests for**, type the external Web Services FQDN, in the **Public Name** box.</span></span>

10. <span data-ttu-id="7187c-133">En la página **seleccionar escucha de web** , haga clic en **nuevo** para abrir el Asistente para nueva definición de escucha de Web.</span><span class="sxs-lookup"><span data-stu-id="7187c-133">On **Select Web Listener** page, click **New** to open the New Web Listener Definition Wizard.</span></span>

11. <span data-ttu-id="7187c-134">En la página **Asistente para nueva escucha de web** , escriba un nombre para la escucha de Web en el cuadro Nombre de la **escucha de web** (por ejemplo, LyncServerWebServers).</span><span class="sxs-lookup"><span data-stu-id="7187c-134">On the **Welcome to the New Web Listener Wizard** page, type a name for the web listener in the **Web listener name** box (for example, LyncServerWebServers).</span></span>

12. <span data-ttu-id="7187c-135">En la página **seguridad de conexión de cliente** , seleccione **requerir conexiones seguras SSL con clientes**.</span><span class="sxs-lookup"><span data-stu-id="7187c-135">On the **Client Connection Security** page, select **Require SSL secured connections with clients**.</span></span>

13. <span data-ttu-id="7187c-136">En la página **dirección IP de escucha de web** , seleccione **externo** y, a continuación, haga clic en **seleccionar direcciones IP**.</span><span class="sxs-lookup"><span data-stu-id="7187c-136">On the **Web Listener IP Address** page, select **External**, and then click **Select IP Addresses**.</span></span>

14. <span data-ttu-id="7187c-137">En la página **selección de IP del agente de escucha externo** , seleccione **dirección IP especificada en el equipo Forefront TMG, en la red seleccionada**, seleccione la dirección IP adecuada y haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-137">On the **External Listener IP selection** page, select **Specified IP address on the Forefront TMG computer in the selected network**, select the appropriate IP address, click **Add**.</span></span>

15. <span data-ttu-id="7187c-138">En la página **certificados SSL de escucha** , seleccione **asignar un certificado para cada dirección IP**, seleccione la dirección IP asociada con el FQDN de la web externa y, a continuación, haga clic en **seleccionar certificado**.</span><span class="sxs-lookup"><span data-stu-id="7187c-138">On the **Listener SSL Certificates** page, select **Assign a certificate for each IP address**, select the IP address that is associated with the external web FQDN, and then click **Select Certificate**.</span></span>

16. <span data-ttu-id="7187c-139">En la página **seleccionar certificado** , seleccione el certificado que coincida con los nombres públicos especificados en el paso 9, haga clic en **seleccionar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-139">On the **Select Certificate** page, select the certificate that matches the public names specified in step 9, click **Select**.</span></span>

17. <span data-ttu-id="7187c-140">En la página **configuración de autenticación** , seleccione **sin autenticación**.</span><span class="sxs-lookup"><span data-stu-id="7187c-140">On the **Authentication Setting** page, select **No Authentication**.</span></span>

18. <span data-ttu-id="7187c-141">En la página de **configuración de inicio de sesión único** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="7187c-141">On the **Single Sign On Setting** page, click **Next**.</span></span>

19. <span data-ttu-id="7187c-142">En la página **finalización del Asistente para la escucha de web** , compruebe que la configuración de la **escucha de web** es correcta y, a continuación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-142">On the **Completing the Web Listener Wizard** page, verify that the **Web listener** settings are correct, and then click **Finish**.</span></span>

20. <span data-ttu-id="7187c-143">En la página **delegación de autenticación** , seleccione **sin delegación, pero el cliente puede autenticar directamente**.</span><span class="sxs-lookup"><span data-stu-id="7187c-143">On the **Authentication Delegation** page, select **No delegation, but client may authenticate directly**.</span></span>

21. <span data-ttu-id="7187c-144">En la página **conjunto de usuarios** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="7187c-144">On the **User Set** page, click **Next**.</span></span>

22. <span data-ttu-id="7187c-145">En la página **finalización del Asistente para nueva regla de publicación de web** , compruebe que la configuración de la regla de publicación de web es correcta y, a continuación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-145">On the **Completing the New Web Publishing Rule Wizard** page, verify that the web publishing rule settings are correct, and then click **Finish**.</span></span>

23. <span data-ttu-id="7187c-146">Haga clic en **aplicar** en el panel de detalles para guardar los cambios y actualizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="7187c-146">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

</div>

<div>

## <a name="to-create-a-web-server-publishing-rule-on-the-computer-running-iis-arr"></a><span data-ttu-id="7187c-147">Para crear una regla de publicación de servidor Web en el equipo que ejecuta IIS ARR</span><span class="sxs-lookup"><span data-stu-id="7187c-147">To create a web server publishing rule on the computer running IIS ARR</span></span>

1.  <span data-ttu-id="7187c-148">Enlace el certificado que usará para el proxy inverso al protocolo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7187c-148">Bind the certificate that you will use for the reverse proxy to the HTTPS protocol.</span></span> <span data-ttu-id="7187c-149">Haga clic en **Inicio**, seleccione **programas**, seleccione **herramientas administrativas** y, a continuación, haga clic en **Administrador de Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="7187c-149">Click **Start**, select **Programs**, select **Administrative Tools**, and then click **Internet Information Services (IIS) Manager**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7187c-150">Encontrará ayuda adicional, capturas de pantalla y orientación sobre la implementación y la configuración de IIS ARR en el artículo de NextHop <A href="https://go.microsoft.com/fwlink/?linkid=293391">que usa IIS ARR como proxy inverso para Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7187c-150">Additional help, screen shots and guidance on deploying and configuring IIS ARR can be found in the NextHop article <A href="https://go.microsoft.com/fwlink/?linkid=293391">Using IIS ARR as a Reverse Proxy for Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="7187c-151">Si aún no lo ha hecho, importe el certificado que usará para el proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="7187c-151">If you have not already done so, import the certificate that you will use for the reverse proxy.</span></span> <span data-ttu-id="7187c-152">En el **Administrador de Internet Information Services (IIS)**, haga clic en el nombre del servidor de proxy inverso en el tamaño del lado izquierdo de la consola.</span><span class="sxs-lookup"><span data-stu-id="7187c-152">In **Internet Information Services (IIS) Manager**, click the reverse proxy server name on the left-hand size of the console.</span></span> <span data-ttu-id="7187c-153">En medio de la consola, en **IIS** , busque **certificados de servidor**.</span><span class="sxs-lookup"><span data-stu-id="7187c-153">In the middle of the console under **IIS** locate **Server Certificates**.</span></span> <span data-ttu-id="7187c-154">Haga clic con el botón secundario en **certificados de servidor** y seleccione **abrir característica**.</span><span class="sxs-lookup"><span data-stu-id="7187c-154">Right-click **Server Certificates** and select **Open feature**.</span></span>

3.  <span data-ttu-id="7187c-155">En la parte derecha de la consola, haga clic en **Importar..**..</span><span class="sxs-lookup"><span data-stu-id="7187c-155">On the right hand side of the console, click **Import…**.</span></span> <span data-ttu-id="7187c-156">Escriba la ruta de acceso y el nombre de archivo del certificado con la extensión o haga clic en **...**</span><span class="sxs-lookup"><span data-stu-id="7187c-156">Type the path and filename of the certificate with the extension, or click **…**</span></span> <span data-ttu-id="7187c-157">para buscar el certificado.</span><span class="sxs-lookup"><span data-stu-id="7187c-157">to browse for the certificate.</span></span> <span data-ttu-id="7187c-158">Seleccione el certificado y haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="7187c-158">Select the certificate and click **Open**.</span></span> <span data-ttu-id="7187c-159">Proporcione la contraseña usada para proteger la clave privada (si ha asignado una contraseña al exportar el certificado y la clave privada).</span><span class="sxs-lookup"><span data-stu-id="7187c-159">Supply the password used to protect the private key (if you assigned a password when exporting the certificate and private key).</span></span> <span data-ttu-id="7187c-160">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-160">Click **OK**.</span></span> <span data-ttu-id="7187c-161">Si la importación del certificado se realizó correctamente, el certificado aparecerá como una entrada en medio de la consola como una entrada en **certificados de servidor**.</span><span class="sxs-lookup"><span data-stu-id="7187c-161">If the certificate import was successful, the certificate will appear as an entry in the middle of the console as an entry in **Server Certificates**.</span></span>

4.  <span data-ttu-id="7187c-162">Asignar el certificado para que lo use HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7187c-162">Assign the certificate for use by HTTPS.</span></span> <span data-ttu-id="7187c-163">En la parte izquierda de la consola, seleccione el **sitio web predeterminado** del servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="7187c-163">On the left-hand side of the console, select the **Default Web Site** of the IIS server.</span></span> <span data-ttu-id="7187c-164">En la parte derecha, haga clic en **enlaces...**.</span><span class="sxs-lookup"><span data-stu-id="7187c-164">On the right-hand side, click **Bindings…**.</span></span> <span data-ttu-id="7187c-165">En el cuadro de diálogo **enlaces del sitio** , haga clic en **Agregar...**.</span><span class="sxs-lookup"><span data-stu-id="7187c-165">In the **Site Bindings** dialog, click **Add…**.</span></span> <span data-ttu-id="7187c-166">En el cuadro de diálogo **Agregar enlace de sitio** , en **tipo:**, seleccione **https**.</span><span class="sxs-lookup"><span data-stu-id="7187c-166">On the **Add Site Binding** dialog under **Type:**, select **https**.</span></span> <span data-ttu-id="7187c-167">Si selecciona https, podrá seleccionar el certificado que se usará para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7187c-167">Selecting https will allow you to select the certificate to use for https.</span></span> <span data-ttu-id="7187c-168">En **certificado SSL:**, seleccione el certificado importado para el proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="7187c-168">Under **SSL certificate:**, select the certificate that you imported for the reverse proxy.</span></span> <span data-ttu-id="7187c-169">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-169">Click **OK**.</span></span> <span data-ttu-id="7187c-170">Después, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-170">Then, click **Close**.</span></span> <span data-ttu-id="7187c-171">El certificado se enlaza ahora al proxy inverso para la capa de sockets seguros (SSL) y la seguridad de la capa de transporte (TLS).</span><span class="sxs-lookup"><span data-stu-id="7187c-171">The certificate is now bound to the reverse proxy for secure socket layer (SSL) and transport layer security (TLS).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="7187c-172">Si recibe una advertencia al cerrar los cuadros de diálogo de enlaces que faltan certificados intermedios, debe buscar e importar el certificado de la entidad de certificación raíz de la entidad emisora y los certificados de la entidad de certificación intermedia.</span><span class="sxs-lookup"><span data-stu-id="7187c-172">If you receive a warning when closing the Bindings dialogs that intermediate certificates are missing, you need to locate and import the public CA root authority certificate and any intermediate CA certificates.</span></span> <span data-ttu-id="7187c-173">Consulte las instrucciones de la entidad emisora pública de la que ha solicitado el certificado y siga las instrucciones para solicitar e importar una cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="7187c-173">Consult the instructions at the public CA that you requested your certificate from and follow the instructions to request and import a certificate chain.</span></span> <span data-ttu-id="7187c-174">Si ha exportado el certificado desde el servidor perimetral, puede exportar el certificado de la entidad emisora raíz y los certificados de CA intermedios asociados con el servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="7187c-174">If you exported the certificate from your Edge Server, you can export the root CA certificate and any intermediate CA certificates associated with the Edge Server.</span></span> <span data-ttu-id="7187c-175">Importe el certificado de la entidad emisora raíz en el almacén de entidades emisoras de certificados raíz de confianza (no se debe confundir con el almacén de usuario) en el almacén de entidades de certificación intermedias del equipo.</span><span class="sxs-lookup"><span data-stu-id="7187c-175">Import the root CA certificate into the Computer’s (not to be confused with the User store) Trusted Root Certification Authorities store and intermediate certificates into the Computer’s Intermediate Certification Authorities store.</span></span>

    
    </div>

5.  <span data-ttu-id="7187c-176">En la parte izquierda de la consola, debajo del nombre del servidor IIS, haga clic con el botón secundario en **granjas de servidores** y haga clic en **crear granja de servidores...**.</span><span class="sxs-lookup"><span data-stu-id="7187c-176">On the left-hand side of the console below the IIS server name, right-click **Server Farms** then click **Create Server Farm…**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7187c-177">Si no ve el nodo de las <STRONG>granjas de servidores</STRONG> , tendrá que instalar el enrutamiento de solicitudes de aplicación.</span><span class="sxs-lookup"><span data-stu-id="7187c-177">If you do not see the <STRONG>Server Farms</STRONG> node, you need to install Application Request Routing.</span></span> <span data-ttu-id="7187c-178">Para obtener más información, consulte <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">configuración de servidores proxy inversos para Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7187c-178">For details, see <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Setting up reverse proxy servers for Lync Server 2013</A>.</span></span>

    
    </div>
    
    <span data-ttu-id="7187c-179">En el cuadro de diálogo **crear granja de servidores** del nombre de una **granja** de servidores, escriba un nombre (puede ser un nombre descriptivo para fines de identificación) para la primera dirección URL.</span><span class="sxs-lookup"><span data-stu-id="7187c-179">On the **Create Server Farm** dialog in **Server farm name**, type the a name (this can be a friendly name for identification purposes) for the first URL.</span></span> <span data-ttu-id="7187c-180">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="7187c-180">Click **Next**.</span></span>

6.  <span data-ttu-id="7187c-181">En el cuadro de diálogo **Agregar servidor** en **dirección de servidor**, escriba el nombre de dominio completo (FQDN) de los servicios web externos en el servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="7187c-181">On the **Add Server** dialog in **Server Address**, type the fully qualified domain name (FQDN) of the external web services on your Front End Server.</span></span> <span data-ttu-id="7187c-182">Los nombres que se usarán aquí para fines de ejemplo son los mismos que se usan en la sección de planificación del proxy inverso, [Resumen de certificados: proxy inverso en Lync Server 2013](lync-server-2013-certificate-summary-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="7187c-182">The names that will be used here for example purposes are the same that are used in the Planning section for the reverse proxy, [Certificate summary - Reverse proxy in Lync Server 2013](lync-server-2013-certificate-summary-reverse-proxy.md).</span></span> <span data-ttu-id="7187c-183">En referencia al planeamiento de proxy inverso, escribemos el nombre completo `webext.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="7187c-183">Referring to the reverse proxy planning, we type the FQDN `webext.contoso.com`.</span></span> <span data-ttu-id="7187c-184">Confirme que la casilla de verificación situada junto a **conectado** está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="7187c-184">Confirm that the checkbox next to **Online** is selected.</span></span> <span data-ttu-id="7187c-185">Haga clic en **Agregar** para agregar el servidor al grupo de servidores web para esta configuración.</span><span class="sxs-lookup"><span data-stu-id="7187c-185">Click **Add** to add the server to the pool of web servers for this configuration.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="7187c-186">Lync Server usa equilibradores de carga de hardware para el director de grupo y los servidores front-end para el tráfico HTTP y HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7187c-186">Lync Server uses hardware load balancers to pool Director and Front End Servers for HTTP and HTTPS traffic.</span></span> <span data-ttu-id="7187c-187">Solo deberá suministrar un FQDN al agregar un servidor a la granja de servidores de IIS ARR.</span><span class="sxs-lookup"><span data-stu-id="7187c-187">You will only supply one FQDN when adding a server to the IIS ARR Server Farm.</span></span> <span data-ttu-id="7187c-188">El FQDN será el servidor front-end o Director en las configuraciones de servidores no agrupados, o el FQDN del equilibrador de carga de hardware configurado para los grupos de servidores.</span><span class="sxs-lookup"><span data-stu-id="7187c-188">The FQDN will be the Front End Server or Director in non-pooled server configurations, or the FQDN of the configured hardware load balancer for server pools.</span></span> <span data-ttu-id="7187c-189">El único método admitido para equilibrar la carga de tráfico HTTP y HTTPS es mediante el uso de equilibradores de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="7187c-189">The only supported method to load balance HTTP and HTTPS traffic is by using hardware load balancers.</span></span>

    
    </div>

7.  <span data-ttu-id="7187c-190">En el cuadro de diálogo **Agregar servidor** , haga clic en **Configuración avanzada...**.</span><span class="sxs-lookup"><span data-stu-id="7187c-190">On the **Add Server** dialog, click **Advanced settings…**.</span></span> <span data-ttu-id="7187c-191">Se abrirá un cuadro de diálogo para definir el enrutamiento de solicitudes de aplicación de solicitudes al FQDN configurado.</span><span class="sxs-lookup"><span data-stu-id="7187c-191">This opens a dialog to define application request routing for requests to the configured FQDN.</span></span> <span data-ttu-id="7187c-192">El propósito es redefinir qué puerto se usa cuando IIS ARR procesa la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7187c-192">The purpose is to redefine what port is used when the request is processed by IIS ARR.</span></span>
    
    <span data-ttu-id="7187c-193">De forma predeterminada, el puerto HTTP de destino debe definirse como 8080.</span><span class="sxs-lookup"><span data-stu-id="7187c-193">By default, the destination HTTP port must be defined as 8080.</span></span> <span data-ttu-id="7187c-194">Haga clic en junto al **httpPort actual 80** y establezca el valor en **8080**.</span><span class="sxs-lookup"><span data-stu-id="7187c-194">Click next to the current **httpPort 80** and set the value to **8080**.</span></span> <span data-ttu-id="7187c-195">Haga clic en junto al **httpsPort actual 443** y establezca el valor en **4443**.</span><span class="sxs-lookup"><span data-stu-id="7187c-195">Click next to the current **httpsPort 443** and set the value to **4443**.</span></span> <span data-ttu-id="7187c-196">Deje el parámetro **Weight** en 100.</span><span class="sxs-lookup"><span data-stu-id="7187c-196">Leave the **weight** parameter at 100.</span></span> <span data-ttu-id="7187c-197">Si es necesario, puede redefinir los pesos para una regla determinada una vez que tiene las estadísticas de línea base.</span><span class="sxs-lookup"><span data-stu-id="7187c-197">If needed, you can redefine weights for a given rule once you have baseline statistics.</span></span> <span data-ttu-id="7187c-198">Haga clic en **Finalizar** para completar esta parte de la configuración de la regla.</span><span class="sxs-lookup"><span data-stu-id="7187c-198">Click **Finish** to complete this part of the rule configuration.</span></span>

8.  <span data-ttu-id="7187c-199">Es posible que vea un cuadro de diálogo de reescritura de reglas que le informa de que el administrador de IIS puede crear una regla de reescritura de dirección URL para enrutar todas las solicitudes entrantes al conjunto de servidores automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7187c-199">You may see a dialog Rewrite Rules that informs you that IIS Manager can create a URL rewrite rule to route all incoming requests to the server farm automatically.</span></span> <span data-ttu-id="7187c-200">Haga clic en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="7187c-200">Click **Yes**.</span></span> <span data-ttu-id="7187c-201">Ajuste las reglas manualmente, pero si selecciona Sí, se establece la configuración inicial..</span><span class="sxs-lookup"><span data-stu-id="7187c-201">You will adjust the rules manually, but selecting Yes sets the initial configuration..</span></span>

9.  <span data-ttu-id="7187c-202">Haga clic en el nombre del conjunto de servidores que acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="7187c-202">Click the name of the server farm that you have just created.</span></span> <span data-ttu-id="7187c-203">En la **granja de servidores** de la vista características del administrador de IIS, haga doble clic en **caché**.</span><span class="sxs-lookup"><span data-stu-id="7187c-203">Under **Server Farm** in IIS Manager Features View, you double-click **Caching**.</span></span> <span data-ttu-id="7187c-204">Anule la selección de **Habilitar caché de disco**.</span><span class="sxs-lookup"><span data-stu-id="7187c-204">Deselect **Enable disk cache**.</span></span> <span data-ttu-id="7187c-205">Haga clic en **aplicar** en el lado derecho.</span><span class="sxs-lookup"><span data-stu-id="7187c-205">Click **Apply** on the right-hand side.</span></span>

10. <span data-ttu-id="7187c-206">Haga clic en el nombre del conjunto de servidores.</span><span class="sxs-lookup"><span data-stu-id="7187c-206">Click the name of the server farm.</span></span> <span data-ttu-id="7187c-207">En la **granja de servidores** de la vista características del administrador de IIS, haga doble clic en **proxy**.</span><span class="sxs-lookup"><span data-stu-id="7187c-207">Under **Server Farm** in IIS Manager Features View, you double-click **Proxy**.</span></span> <span data-ttu-id="7187c-208">En la página Configuración de proxy, cambie el valor de **tiempo de espera (segundos)** a un valor adecuado para su implementación.</span><span class="sxs-lookup"><span data-stu-id="7187c-208">On the Proxy settings page change the value for **Time-out (seconds)** to a value appropriate for your deployment.</span></span> <span data-ttu-id="7187c-209">Haga clic en **aplicar** para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="7187c-209">Click **Apply** to save the change.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="7187c-210">El valor de tiempo de espera del proxy es un número que variará de una implementación a la de implementación.</span><span class="sxs-lookup"><span data-stu-id="7187c-210">The Proxy Time-out value is a number that will vary from deployment to deployment.</span></span> <span data-ttu-id="7187c-211">Debe supervisar la implementación y modificar el valor de la mejor experiencia para los clientes.</span><span class="sxs-lookup"><span data-stu-id="7187c-211">You should monitor your deployment and modify the value for the best experience for clients.</span></span> <span data-ttu-id="7187c-212">Es posible que pueda configurar el valor como mínimo como 200.</span><span class="sxs-lookup"><span data-stu-id="7187c-212">You may be able to set the value as low as 200.</span></span> <span data-ttu-id="7187c-213">Si admite clientes móviles de Lync en su entorno, debe establecer el valor en 960 para permitir el tiempo de espera de las notificaciones de inserción de Office 365 que tengan un valor de tiempo de espera de 900.</span><span class="sxs-lookup"><span data-stu-id="7187c-213">If you are supporting Lync mobile clients in your environment, you should set the value to 960 to allow for push notifications timeout from Office 365 which have a time-out value of 900.</span></span> <span data-ttu-id="7187c-214">Es muy probable que tenga que aumentar el valor de tiempo de espera para evitar desconexiones de cliente cuando el valor es demasiado bajo o disminuir el número si las conexiones a través del proxy no se desconectan y se devuelven mucho después de que el cliente se haya desconectado.</span><span class="sxs-lookup"><span data-stu-id="7187c-214">It is very likely that you will need to increase the time-out value to avoid client disconnects when the value is too low or decrease the number if connections through the proxy do not disconnect and clear long after the client has disconnected.</span></span> <span data-ttu-id="7187c-215">La supervisión y la alineación básica de lo que es normal para su entorno es la única forma precisa de determinar dónde se encuentra la configuración adecuada para este valor.</span><span class="sxs-lookup"><span data-stu-id="7187c-215">Monitoring and base-lining what is normal for your environment is the only accurate means to determine where the right setting is for this value.</span></span>

    
    </div>

11. <span data-ttu-id="7187c-216">Haga clic en el nombre del conjunto de servidores.</span><span class="sxs-lookup"><span data-stu-id="7187c-216">Click the name of the server farm.</span></span> <span data-ttu-id="7187c-217">En **granja de servidores** en la vista características del administrador de IIS, haga doble clic en **reglas de enrutamiento**.</span><span class="sxs-lookup"><span data-stu-id="7187c-217">Under **Server Farm** in IIS Manager Features View, you double-click **Routing Rules**.</span></span> <span data-ttu-id="7187c-218">En el cuadro de diálogo reglas de enrutamiento, en enrutamiento, desactive la casilla que se encuentra junto a habilitar descarga SSL.</span><span class="sxs-lookup"><span data-stu-id="7187c-218">On the Routing Rules dialog under Routing, clear the checkbox next to Enable SSL offloading.</span></span> <span data-ttu-id="7187c-219">Si la opción para borrar la casilla no está disponible, seleccione la casilla de verificación **usar URL de reescritura para inspeccionar las solicitudes entrantes**.</span><span class="sxs-lookup"><span data-stu-id="7187c-219">If the ability to clear the checkbox is not available, select the checkbox for **Use URL Rewrite to inspect incoming requests**.</span></span> <span data-ttu-id="7187c-220">Haga clic en **aplicar** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="7187c-220">Click **Apply** to save your changes.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="7187c-221">No se admite la descarga de SSL por parte del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="7187c-221">SSL Offloading by the reverse proxy is not supported.</span></span>

    
    </div>

12. <span data-ttu-id="7187c-222">Repita los pasos 5-11 para cada dirección URL que deba pasar a través del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="7187c-222">Repeat Steps 5-11 for each URL that must pass through the reverse proxy.</span></span> <span data-ttu-id="7187c-223">Una lista común sería la siguiente:</span><span class="sxs-lookup"><span data-stu-id="7187c-223">A common list would be the following:</span></span>
    
      - <span data-ttu-id="7187c-224">Servicios web del servidor front-end externo: webext.contoso.com (ya configurado por el paso inicial)</span><span class="sxs-lookup"><span data-stu-id="7187c-224">Front End Server Web services external: webext.contoso.com (already configured by initial walk through)</span></span>
    
      - <span data-ttu-id="7187c-225">Director de servicios Web externo para Director: webdirext.contoso.com (opcional si se implementa un director)</span><span class="sxs-lookup"><span data-stu-id="7187c-225">Director Web services external for Director: webdirext.contoso.com (Optional if a Director is deployed)</span></span>
    
      - <span data-ttu-id="7187c-226">Dirección URL simple: meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7187c-226">Simple URL meet: meet.contoso.com</span></span>
    
      - <span data-ttu-id="7187c-227">Marcado de dirección URL simple: dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7187c-227">Simple URL dialin: dialin.contoso.com</span></span>
    
      - <span data-ttu-id="7187c-228">Dirección URL de detección automática de Lync: lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7187c-228">Lync Autodiscover URL: lyncdiscover.contoso.com</span></span>
    
      - <span data-ttu-id="7187c-229">URL de Office Web Apps Server: officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7187c-229">Office Web Apps Server URL: officewebapps01.contoso.com</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="7187c-230">La dirección URL del servidor de Office Web Apps usará una dirección de httpsPort diferente.</span><span class="sxs-lookup"><span data-stu-id="7187c-230">The URL for the Office Web Apps Server will use a different httpsPort address.</span></span> <span data-ttu-id="7187c-231">En el paso 7, define <STRONG>httpsPort</STRONG> como <STRONG>443</STRONG> y <STRONG>httpPort</STRONG> como puerto <STRONG>80</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7187c-231">In step 7, you define the <STRONG>httpsPort</STRONG> as <STRONG>443</STRONG> and the <STRONG>httpPort</STRONG> as port <STRONG>80</STRONG>.</span></span> <span data-ttu-id="7187c-232">El resto de parámetros de configuración son iguales.</span><span class="sxs-lookup"><span data-stu-id="7187c-232">All other configuration settings are the same.</span></span>

        
        </div>

13. <span data-ttu-id="7187c-233">En la parte izquierda de la consola, haga clic en el nombre del servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="7187c-233">On the left-hand side of the console, click the IIS server name.</span></span> <span data-ttu-id="7187c-234">En el medio de la consola, busque **URL Rewrite** en **IIS**.</span><span class="sxs-lookup"><span data-stu-id="7187c-234">In the middle of the console, locate **URL Rewrite** under **IIS**.</span></span> <span data-ttu-id="7187c-235">Haga doble clic en la dirección URL de reescritura para abrir la configuración de la URL de reescritura de reglas.</span><span class="sxs-lookup"><span data-stu-id="7187c-235">Double-click URL Rewrite to open the URL Rewrite rules configuration.</span></span> <span data-ttu-id="7187c-236">Debería ver las reglas de cada granja de servidores que creó en los pasos anteriores.</span><span class="sxs-lookup"><span data-stu-id="7187c-236">You should see rules for each Server Farm that you created in the previous steps.</span></span> <span data-ttu-id="7187c-237">Si no lo hace, confirme que hizo clic en el nombre del **servidor IIS** inmediatamente debajo del nodo de la **Página de inicio** en la consola del administrador de Internet Information Server.</span><span class="sxs-lookup"><span data-stu-id="7187c-237">If you do not, confirm that you clicked on the **IIS Server** name immediately below the **Start Page** node in the Internet Information Server Manager console.</span></span>

14. <span data-ttu-id="7187c-238">En el cuadro de diálogo de **reescritura de direcciones URL** , con webext.contoso.com como ejemplo, el nombre completo de la regla tal como se muestra es **ARR \_ webext.contoso.com \_ loadbalance \_ SSL**.</span><span class="sxs-lookup"><span data-stu-id="7187c-238">In the **URL Rewrite** dialog, using webext.contoso.com as an example, the full name of the rule as displayed is **ARR\_webext.contoso.com\_loadbalance\_SSL**.</span></span>
    
      - <span data-ttu-id="7187c-239">Haga doble clic en la regla para abrir el cuadro de diálogo **Editar regla de entrada** .</span><span class="sxs-lookup"><span data-stu-id="7187c-239">Double-click the rule to open the **Edit Inbound Rule** dialog.</span></span>
    
      - <span data-ttu-id="7187c-240">Haga clic en **Agregar...**</span><span class="sxs-lookup"><span data-stu-id="7187c-240">Click **Add…**</span></span> <span data-ttu-id="7187c-241">en el cuadro de diálogo **condiciones** .</span><span class="sxs-lookup"><span data-stu-id="7187c-241">on the **Conditions** dialog.</span></span>
    
      - <span data-ttu-id="7187c-242">En la **entrada de condición** **Agregar condición** : escriba **{http \_ host}**.</span><span class="sxs-lookup"><span data-stu-id="7187c-242">On the **Add Condition** in **Condition input:** type **{HTTP\_HOST}**.</span></span> <span data-ttu-id="7187c-243">(Mientras escribe, aparece un cuadro de diálogo que le permitirá seleccionar la condición).</span><span class="sxs-lookup"><span data-stu-id="7187c-243">(As you type, a dialog appears that will let you select the condition).</span></span> <span data-ttu-id="7187c-244">en **comprobar si la cadena de entrada:** seleccione **coincide con el patrón**.</span><span class="sxs-lookup"><span data-stu-id="7187c-244">under **Check if input string:** select **Matches the Pattern**.</span></span> <span data-ttu-id="7187c-245">En el tipo de **entrada patrón** , debe seleccionarse la **\* *_. _* distinción entre mayúsculas y minúsculas** .</span><span class="sxs-lookup"><span data-stu-id="7187c-245">In the **Pattern input** type **\**_. _\* Ignore case*\* should be selected.</span></span> <span data-ttu-id="7187c-246">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-246">Click **OK**.</span></span>
    
      - <span data-ttu-id="7187c-247">Desplácese hacia abajo en el cuadro de diálogo **Editar regla de entrada** para ubicar el cuadro de diálogo de **acción** .</span><span class="sxs-lookup"><span data-stu-id="7187c-247">Scroll down in the **Edit Inbound Rule** dialog to locate the **Action** dialog.</span></span> <span data-ttu-id="7187c-248">**Tipo de acción:** debe establecerse en **enrutar a granja de servidores**, **esquema:** establecer en **https://**, **granja de servidores:** establezca la dirección URL a la que se aplica esta regla.</span><span class="sxs-lookup"><span data-stu-id="7187c-248">**Action Type:** should be set to **Route to Server Farm**, **Scheme:** set to **https://**, **Server farm:** set to the URL that this rule applies to.</span></span> <span data-ttu-id="7187c-249">Para este ejemplo, debe establecerse en **webext.contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="7187c-249">For this example, this should be set to **webext.contoso.com**.</span></span> <span data-ttu-id="7187c-250">**Path:** se establece en **/{R: 0}**</span><span class="sxs-lookup"><span data-stu-id="7187c-250">**Path:** is set to **/{R:0}**</span></span>
    
      - <span data-ttu-id="7187c-251">Haga clic en **aplicar** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="7187c-251">Click **Apply** to save your changes.</span></span> <span data-ttu-id="7187c-252">Haga clic en **volver a reglas** para volver a las reglas de reescritura de URL.</span><span class="sxs-lookup"><span data-stu-id="7187c-252">Click **Back to Rules** to return to the URL Rewrite rules.</span></span>

15. <span data-ttu-id="7187c-253">Repita el procedimiento definido en el paso 14 para cada una de las reglas de reescritura de SSL que haya definido, una por dirección URL de granja de servidores.</span><span class="sxs-lookup"><span data-stu-id="7187c-253">Repeat the procedure defined in Step 14 for each of the SSL rewrite rules that you have defined, one per Server Farm URL.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="7187c-254">De forma predeterminada, las reglas HTTP también se crean y se indican con nombres parecidos a las reglas de SSL.</span><span class="sxs-lookup"><span data-stu-id="7187c-254">By default, HTTP rules are created as well and are denoted by the similar naming to the SSL rules.</span></span> <span data-ttu-id="7187c-255">Para nuestro ejemplo actual, la regla HTTP se denomina <STRONG>ARR_webext. contoso. com _loadbalance</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7187c-255">For our current example, the HTTP rule would be named <STRONG>ARR_webext.contoso.com_loadbalance</STRONG>.</span></span> <span data-ttu-id="7187c-256">No se necesitan modificaciones en estas reglas y se pueden ignorar con seguridad.</span><span class="sxs-lookup"><span data-stu-id="7187c-256">No modifications are needed to these rules and they can be safely ignored.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-the-properties-of-the-web-publishing-rule-in-tmg-2010"></a><span data-ttu-id="7187c-257">Para modificar las propiedades de la regla de publicación web en TMG 2010</span><span class="sxs-lookup"><span data-stu-id="7187c-257">To modify the properties of the web publishing rule in TMG 2010</span></span>

1.  <span data-ttu-id="7187c-258">Haga clic en **Inicio**, seleccione **programas**, **Microsoft Forefront TMG** y, a continuación, haga clic en **Administración de Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="7187c-258">Click **Start**, point to **Programs**, select **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="7187c-259">En el panel izquierdo, expanda **ServerName** y, a continuación, haga clic en **Directiva de Firewall**.</span><span class="sxs-lookup"><span data-stu-id="7187c-259">In the left pane, expand **ServerName**, and then click **Firewall Policy**.</span></span>

3.  <span data-ttu-id="7187c-260">En el panel de detalles, haga clic con el botón secundario en la regla de publicación del servidor Web que creó en el procedimiento anterior (por ejemplo, LyncServerExternalRule) y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="7187c-260">In the details pane, right-click the web server publishing rule that you created in the previous procedure (for example, LyncServerExternalRule), and then click **Properties**.</span></span>

4.  <span data-ttu-id="7187c-261">En la página **propiedades** , en la pestaña **de** , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7187c-261">On the **Properties** page, on the **From** tab, do the following:</span></span>
    
      - <span data-ttu-id="7187c-262">En la lista **esta regla se aplica a tráfico de estas fuentes** , haga clic en **cualquier lugar** y luego haga clic en **quitar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-262">In the **This rule applies to traffic from these sources** list, click **Anywhere**, and then click **Remove**.</span></span>
    
      - <span data-ttu-id="7187c-263">Haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-263">Click **Add**.</span></span>
    
      - <span data-ttu-id="7187c-264">En **Agregar entidades de red**, expanda **redes**, haga clic en **externa**, haga clic en **Agregar** y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-264">In **Add Network Entities**, expand **Networks**, click **External**, click **Add**, and then click **Close**.</span></span>

5.  <span data-ttu-id="7187c-265">En la pestaña **para** , asegúrese de que la casilla **reenviar el encabezado de host original en lugar de la real** está activada.</span><span class="sxs-lookup"><span data-stu-id="7187c-265">On the **To** tab, ensure that the **Forward the original host header instead of the actual one** check box is selected.</span></span>

6.  <span data-ttu-id="7187c-266">En la pestaña **puente** , seleccione la casilla de verificación **redirigir la solicitud al puerto SSL** y, a continuación, especifique el puerto **4443**.</span><span class="sxs-lookup"><span data-stu-id="7187c-266">On the **Bridging** tab, select the **Redirect request to SSL port** check box, and then specify port **4443**.</span></span>

7.  <span data-ttu-id="7187c-267">En la pestaña **nombre público** , agregue las direcciones URL simples (por ejemplo, meet.contoso.com y Dialin.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7187c-267">On the **Public Name** tab, add the simple URLs (for example, meet.contoso.com and dialin.contoso.com).</span></span>

8.  <span data-ttu-id="7187c-268">Haga clic en **aplicar** para guardar los cambios y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7187c-268">Click **Apply** to save changes, and then click **OK**.</span></span>

9.  <span data-ttu-id="7187c-269">Haga clic en **aplicar** en el panel de detalles para guardar los cambios y actualizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="7187c-269">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

</div>

<div>

## <a name="to-modify-the-properties-of-the-web-publishing-rule-in-iis-arr"></a><span data-ttu-id="7187c-270">Para modificar las propiedades de la regla de publicación web en IIS ARR</span><span class="sxs-lookup"><span data-stu-id="7187c-270">To modify the properties of the web publishing rule in IIS ARR</span></span>

1.  <span data-ttu-id="7187c-271">Haga clic en **Inicio**, seleccione **programas**, seleccione **herramientas administrativas** y, a continuación, haga clic en **Administrador de Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="7187c-271">Click **Start**, select **Programs**, select **Administrative Tools**, and then click **Internet Information Services (IIS) Manager**.</span></span>

2.  <span data-ttu-id="7187c-272">En la parte izquierda de la consola, haga clic en el nombre del servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="7187c-272">On the left-hand side of the console, click the IIS server name.</span></span>

3.  <span data-ttu-id="7187c-273">En el medio de la consola, busque **URL Rewrite** en **IIS**.</span><span class="sxs-lookup"><span data-stu-id="7187c-273">In the middle of the console, locate **URL Rewrite** under **IIS**.</span></span> <span data-ttu-id="7187c-274">Haga doble clic en la dirección URL de reescritura para abrir la configuración de la URL de reescritura de reglas.</span><span class="sxs-lookup"><span data-stu-id="7187c-274">Double-click URL Rewrite to open the URL Rewrite rules configuration.</span></span>

4.  <span data-ttu-id="7187c-275">Haga doble clic en la regla que necesita modificar.</span><span class="sxs-lookup"><span data-stu-id="7187c-275">Double-click the rule that you need to modify.</span></span> <span data-ttu-id="7187c-276">Realice sus modificaciones, según sea necesario, en **coincidencia con la dirección URL**, **condiciones**, **variables de servidor** o **acción**.</span><span class="sxs-lookup"><span data-stu-id="7187c-276">Make your modifications, as needed, in **Match URL**, **Conditions**, **Server Variables** or **Action**.</span></span>

5.  <span data-ttu-id="7187c-277">Haga clic en **aplicar** para confirmar los cambios.</span><span class="sxs-lookup"><span data-stu-id="7187c-277">Click **Apply** to commit your changes.</span></span> <span data-ttu-id="7187c-278">Haga clic en **volver a reglas** para modificar otras reglas o cierre la consola del **Administrador de IIS** si ha terminado de realizar los cambios.</span><span class="sxs-lookup"><span data-stu-id="7187c-278">Click **Back to Rules** to modify other rules, or close the **IIS Manager** console if you are done with your changes.</span></span>

<span data-ttu-id="7187c-279"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7187c-279"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

