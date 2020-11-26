---
title: 'Lync Server 2013: Configurar certificados para la interfaz perimetral interna'
description: 'Lync Server 2013: configurar certificados para la interfaz de borde interno.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up certificates for the internal edge interface
ms:assetid: a1963cc9-87c5-4935-86c0-6bedc6afd0ac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412750(v=OCS.15)
ms:contentKeyID: 48184949
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 52473069735d4f48c247367194139c479e71293f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424005"
---
# <a name="set-up-certificates-for-the-internal-edge-interface-in-lync-server-2013"></a><span data-ttu-id="5534e-103">Configurar certificados para la interfaz perimetral interna en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5534e-103">Set up certificates for the internal edge interface in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5534e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5534e-104">

<span> </span></span></span>

<span data-ttu-id="5534e-105">_**Última modificación del tema:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="5534e-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="5534e-106">Cuando ejecute el Asistente para certificados, asegúrese de haber iniciado sesión con una cuenta que sea miembro de un grupo al que se le hayan asignado los permisos adecuados para el tipo de plantilla de certificado que va a usar.</span><span class="sxs-lookup"><span data-stu-id="5534e-106">When you run the Certificate Wizard, ensure that you are logged in using an account that is a member of a group that has been assigned the appropriate permissions for the type of certificate template you will use.</span></span> <span data-ttu-id="5534e-107">De forma predeterminada, una solicitud de certificado de Lync Server 2013 usará la plantilla de certificado de servidor Web.</span><span class="sxs-lookup"><span data-stu-id="5534e-107">By default, a Lync Server 2013 certificate request will use the Web Server certificate template.</span></span> <span data-ttu-id="5534e-108">Si usa una cuenta que sea miembro del grupo RTCUniversalServerAdmins para solicitar un certificado con esta plantilla, compruebe que el grupo tiene asignados los permisos de inscripción necesarios para usar esa plantilla.</span><span class="sxs-lookup"><span data-stu-id="5534e-108">If you use an account that is a member of the RTCUniversalServerAdmins group to request a certificate using this template, verify that the group has been assigned the Enroll permissions required to use that template.</span></span>



</div>

<span data-ttu-id="5534e-109">Se necesita un único certificado en la interfaz interna de cada servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-109">A single certificate is required on the internal interface of each Edge Server.</span></span> <span data-ttu-id="5534e-110">Los certificados de la interfaz interna pueden ser emitidos por una entidad de certificación (CA) interna o una CA pública.</span><span class="sxs-lookup"><span data-stu-id="5534e-110">Certificates for the internal interface can be issued by an internal enterprise certification authority (CA) or a public CA.</span></span> <span data-ttu-id="5534e-111">Si su organización tiene una CA interna implementada, puede ahorrar en el gasto de usar certificados públicos mediante la entidad de certificación interna para emitir el certificado de la interfaz interna.</span><span class="sxs-lookup"><span data-stu-id="5534e-111">If your organization has an internal CA deployed you can save on the expense of using public certificates by using the internal CA to issue the certificate for the internal interface.</span></span> <span data-ttu-id="5534e-112">Puede usar una CA interna de Windows Server 2008 o una CA de Windows Server 2008 R2 para crear estos certificados.</span><span class="sxs-lookup"><span data-stu-id="5534e-112">You can use an internal Windows Server 2008 CA or Windows Server 2008 R2 CA to create these certificates.</span></span>

<span data-ttu-id="5534e-113">Para obtener más información sobre este y otros requisitos de certificado, consulte [requisitos de certificados para el acceso de usuarios externos en Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="5534e-113">For details about this and other certificate requirements, see [Certificate requirements for external user access in Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span></span>

<span data-ttu-id="5534e-114">Para configurar certificados en la interfaz de borde interno en un sitio, siga los procedimientos de esta sección para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5534e-114">To set up certificates on the internal edge interface at a site, use the procedures in this section to do the following:</span></span>

1.  <span data-ttu-id="5534e-115">Descarga la cadena de certificación de la entidad emisora para la interfaz interna de cada servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-115">Download the CA certification chain for the internal interface to each Edge Server.</span></span>

2.  <span data-ttu-id="5534e-116">Importe la cadena de certificación de la entidad de certificación de la interfaz interna en cada servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-116">Import the CA certification chain for the internal interface, on each Edge Server.</span></span>

3.  <span data-ttu-id="5534e-117">Cree la solicitud de certificado para la interfaz interna, en un servidor perimetral, denominado el primer servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-117">Create the certificate request for the internal interface, on one Edge Server, called the first Edge Server.</span></span>

4.  <span data-ttu-id="5534e-118">Importe el certificado de la interfaz interna en el primer servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-118">Import the certificate for the internal interface on the first Edge Server.</span></span>

5.  <span data-ttu-id="5534e-119">Importe el certificado en los otros servidores perimetrales de este sitio (o implementado detrás de este equilibrador de carga).</span><span class="sxs-lookup"><span data-stu-id="5534e-119">Import the certificate on the other Edge Servers at this site (or deployed behind this load balancer).</span></span>

6.  <span data-ttu-id="5534e-120">Asigne el certificado de la interfaz interna de cada servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-120">Assign the certificate for the internal interface of every Edge Server.</span></span>

<span data-ttu-id="5534e-121">Si tiene más de un sitio con servidores perimetrales (es decir, una topología perimetral de varios sitios) o conjuntos independientes de servidores perimetrales implementados con distintos equilibradores de carga, debe seguir estos pasos para cada sitio que tenga servidores perimetrales y para cada conjunto de servidores perimetrales implementados detrás de un equilibrador de carga diferente.</span><span class="sxs-lookup"><span data-stu-id="5534e-121">If you have more than one site with Edge Servers (that is, a multiple-site edge topology), or separate sets of Edge Servers deployed behind different load balancers, you need to follow these steps for each site that has Edge Servers, and for each set of Edge Servers deployed behind a different load balancer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5534e-122">Los pasos de esta sección se basan en el uso de una CA de Windows Server &nbsp; 2008, Windows server &nbsp; 2008 &nbsp; R2 CA, Windows Server 2012 CA o Windows Server 2012 R2 CA para crear un certificado para cada servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-122">The steps for procedures in this section are based on using a Windows Server&nbsp;2008 CA, Windows Server&nbsp;2008&nbsp;R2 CA, Windows Server 2012 CA, or Windows Server 2012 R2 CA to create a certificate for each Edge Server.</span></span> <span data-ttu-id="5534e-123">Para obtener instrucciones paso a paso para cualquier otra CA, consulte la documentación de esa CA.</span><span class="sxs-lookup"><span data-stu-id="5534e-123">For step-by-step guidance for any other CA, consult the documentation for that CA.</span></span> <span data-ttu-id="5534e-124">De forma predeterminada, todos los usuarios autenticados tienen los derechos de usuario adecuados para solicitar certificados.</span><span class="sxs-lookup"><span data-stu-id="5534e-124">By default, all authenticated users have the appropriate user rights to request certificates.</span></span><BR><span data-ttu-id="5534e-125">Los procedimientos de esta sección se basan en la creación de solicitudes de certificado en el servidor perimetral como parte del proceso de implementación del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-125">The procedures in this section are based on creating certificate requests on the Edge Server as part of the Edge Server deployment process.</span></span> <span data-ttu-id="5534e-126">Es posible crear solicitudes de certificados con el servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="5534e-126">It is possible to create certificate requests using the Front End Server.</span></span> <span data-ttu-id="5534e-127">Puede hacerlo para completar la solicitud de certificado al principio del proceso de planeación e implementación, antes de iniciar la implementación de los servidores perimetrales.</span><span class="sxs-lookup"><span data-stu-id="5534e-127">You can do this to complete the certificate request early in the planning and deployment process, before you start deployment of the Edge Servers.</span></span> <span data-ttu-id="5534e-128">Para ello, debe asegurarse de que el certificado solicitado se haya definido con una clave privada exportable.</span><span class="sxs-lookup"><span data-stu-id="5534e-128">To do this, you must ensure that the certificate you request is defined with an exportable private key.</span></span><BR><span data-ttu-id="5534e-129">Los procedimientos de esta sección describen el uso de un archivo. cer y un archivo. p7b para el certificado.</span><span class="sxs-lookup"><span data-stu-id="5534e-129">The procedures in this section describe using a .cer and a .p7b file for the certificate.</span></span> <span data-ttu-id="5534e-130">Si usa un tipo de archivo diferente, modifique estos procedimientos según corresponda.</span><span class="sxs-lookup"><span data-stu-id="5534e-130">If you use a different type of file, modify these procedures as appropriate.</span></span>



</div>

<div>

## <a name="to-download-the-ca-certification-chain-for-the-internal-interface-using-certsrv-web-site"></a><span data-ttu-id="5534e-131">Para descargar la cadena de certificación de CA para la interfaz interna mediante el sitio web certsrv</span><span class="sxs-lookup"><span data-stu-id="5534e-131">To download the CA certification chain for the internal interface using certsrv Web site</span></span>

1.  <span data-ttu-id="5534e-132">Inicie sesión en un servidor de Lync Server 2013 de la red interna (es decir, no en el servidor perimetral) como miembro del grupo **administradores** .</span><span class="sxs-lookup"><span data-stu-id="5534e-132">Log on to an Lync Server 2013 server in the internal network (that is, not the Edge Server) as a member of the **Administrators** group.</span></span>

2.  <span data-ttu-id="5534e-133">Ejecute el comando siguiente en un símbolo del sistema haciendo clic en **Inicio**, haga clic en **Ejecutar** y, a continuación, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5534e-133">Run the following command at a command prompt by clicking **Start**, clicking **Run**, and then typing the following:</span></span>
    
        https://<name of your Issuing CA Server>/certsrv
    
    <span data-ttu-id="5534e-134">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5534e-134">For example:</span></span>
    
        https://ca01.contoso.net/certsrv
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5534e-135">Si está usando Windows Server 2008 o Windows Server 2008 R2 Enterprise CA, debe usar https, no http.</span><span class="sxs-lookup"><span data-stu-id="5534e-135">If you are using a Windows Server 2008 or Windows Server 2008 R2 enterprise CA, you must use https, not http.</span></span>

    
    </div>

3.  <span data-ttu-id="5534e-136">En la página web certsrv de la CA que emite el certificado, en **Seleccione una tarea**, haga clic en **Descargar certificado de CA, cadena de certificados o CRL**.</span><span class="sxs-lookup"><span data-stu-id="5534e-136">On the issuing CA’s certsrv web page, under **Select a task**, click **Download a CA certificate, certificate chain, or CRL**.</span></span>

4.  <span data-ttu-id="5534e-137">En **descargar un certificado de CA, una cadena de certificados o una CRL**, haga clic en **Descargar cadena de certificados de la entidad emisora**.</span><span class="sxs-lookup"><span data-stu-id="5534e-137">Under **Download a CA Certificate, Certificate Chain, or CRL**, click **Download CA certificate chain**.</span></span>

5.  <span data-ttu-id="5534e-138">En el cuadro de diálogo **descarga de archivos** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-138">In the **File Download** dialog box, click **Save**.</span></span>

6.  <span data-ttu-id="5534e-139">Guarde el archivo. p7b en la unidad de disco duro del servidor y, a continuación, cópielo en una carpeta de cada servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-139">Save the .p7b file to the hard disk drive on the server, and then copy it to a folder on each Edge Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5534e-140">El archivo. p7b contiene todos los certificados que se encuentran en la ruta de certificación.</span><span class="sxs-lookup"><span data-stu-id="5534e-140">The .p7b file contains all of the certificates that are in the certification path.</span></span> <span data-ttu-id="5534e-141">Para ver la ruta de certificación, abra el certificado de servidor y haga clic en la ruta de certificación.</span><span class="sxs-lookup"><span data-stu-id="5534e-141">To view the certification path, open the server certificate and click the certification path.</span></span>

    
    </div>

</div>

<div>

## <a name="to-export-the-ca-certification-chain-for-the-internal-interface-using-mmc"></a><span data-ttu-id="5534e-142">Para exportar la cadena de certificación de la CA para la interfaz interna con MMC</span><span class="sxs-lookup"><span data-stu-id="5534e-142">To export the CA certification chain for the internal interface using MMC</span></span>

1.  <span data-ttu-id="5534e-143">Puede exportar el certificado raíz de la entidad emisora desde cualquier equipo unido a un dominio mediante la consola de administración de Microsoft (MMC).</span><span class="sxs-lookup"><span data-stu-id="5534e-143">You can export the CA root certificate from any domain joined machine using the Microsoft Management Console (MMC).</span></span> <span data-ttu-id="5534e-144">Haga clic en **Inicio**, haga clic en **Ejecutar** y escriba **MMC**.</span><span class="sxs-lookup"><span data-stu-id="5534e-144">Click **Start**, click **Run**, and then type **MMC**.</span></span>

2.  <span data-ttu-id="5534e-145">En la consola MMC, haga clic en **archivo** y en **Agregar o quitar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-145">In the MMC console, click **File**, click **Add/Remove**.</span></span>

3.  <span data-ttu-id="5534e-146">En la lista de cuadros de diálogo **Agregar o quitar complementos** , seleccione **certificados** y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-146">From the **Add or Remove Snap-ins** dialog list, select **Certificates**, then click **Add**.</span></span> <span data-ttu-id="5534e-147">Cuando se le solicite, seleccione **cuenta de equipo**.</span><span class="sxs-lookup"><span data-stu-id="5534e-147">When prompted, select **Computer Account**.</span></span> <span data-ttu-id="5534e-148">En el diálogo **Seleccionar equipo**, seleccione **Equipo local**.</span><span class="sxs-lookup"><span data-stu-id="5534e-148">On the **Select Computer** dialog, select **Local Computer**.</span></span> <span data-ttu-id="5534e-149">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-149">Click **Finish**.</span></span> <span data-ttu-id="5534e-150">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-150">Click **OK**.</span></span>

4.  <span data-ttu-id="5534e-151">Expanda **certificados (equipo local)**.</span><span class="sxs-lookup"><span data-stu-id="5534e-151">Expand **Certificates (Local Computer)**.</span></span> <span data-ttu-id="5534e-152">Expanda **entidades de certificación raíz de confianza**, seleccione **certificados**.</span><span class="sxs-lookup"><span data-stu-id="5534e-152">Expand **Trusted Root Certification Authorities**, select **Certificates**.</span></span>

5.  <span data-ttu-id="5534e-153">Haga clic en el certificado raíz emitido por su CA.</span><span class="sxs-lookup"><span data-stu-id="5534e-153">Click the root certificate issued by your CA.</span></span> <span data-ttu-id="5534e-154">Haga clic con el botón secundario en el certificado, seleccione **todas las tareas** y **exportar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-154">Right click the certificate, select **All Tasks**, select **Export**.</span></span> <span data-ttu-id="5534e-155">Se abrirá el **Asistente para exportación de certificados** .</span><span class="sxs-lookup"><span data-stu-id="5534e-155">The **Certificate Export Wizard** will open.</span></span>

6.  <span data-ttu-id="5534e-156">En el **Asistente para exportación de certificados**, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-156">In the **Certificate Export Wizard**, click **Next**.</span></span>

7.  <span data-ttu-id="5534e-157">En el cuadro de diálogo **exportar formato de archivo** , seleccione un formato para exportar.</span><span class="sxs-lookup"><span data-stu-id="5534e-157">On the **Export File Format** dialog, select a format to export to.</span></span> <span data-ttu-id="5534e-158">Recomendamos el **estándar de sintaxis de mensajes criptográficos: \# certificados PKCS 7 (. P7B)**.</span><span class="sxs-lookup"><span data-stu-id="5534e-158">We recommend the **Cryptographic Message Syntax Standard – PKCS \#7 Certificates (.P7B)**.</span></span> <span data-ttu-id="5534e-159">Si selecciona la **Sintaxis de mensajes criptográficos estándar: \# certificados PKCS 7 (. P7B)**, seleccione la casilla **incluir todos los certificados en la ruta de certificación si es posible** para exportar la cadena de certificados, incluido el certificado de CA raíz y los certificados de CA intermedias.</span><span class="sxs-lookup"><span data-stu-id="5534e-159">If you select the **Cryptographic Message Syntax Standard – PKCS \#7 Certificates (.P7B)**, select the **Include all certificates in the certification path if possible** checkbox to export the certificate chain, including the root CA certificate and any Intermediate CA certificates.</span></span> <span data-ttu-id="5534e-160">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-160">Click **Next**.</span></span>

8.  <span data-ttu-id="5534e-161">En el cuadro de diálogo **archivo para exportar** , en la entrada nombre de archivo, escriba una ruta de acceso y un nombre de archivo (la extensión predeterminada es. p7b) para el certificado exportado.</span><span class="sxs-lookup"><span data-stu-id="5534e-161">On the **File to Export** dialog in the file name entry, type a path and file name (default extension is .p7b) for the exported certificate.</span></span> <span data-ttu-id="5534e-162">De manera opcional, haga clic en **examinar**, busque un directorio en el que ubicar el certificado exportado y proporcione un nombre para el certificado exportado.</span><span class="sxs-lookup"><span data-stu-id="5534e-162">Optionally, click **Browse**, locate a directory to place the exported certificate in and provide a name for the exported certificate.</span></span> <span data-ttu-id="5534e-163">Haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-163">Click **Save**.</span></span> <span data-ttu-id="5534e-164">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-164">Click **Next**.</span></span>

9.  <span data-ttu-id="5534e-165">Revise el Resumen de acciones y haga clic en **Finalizar** para completar la exportación del certificado.</span><span class="sxs-lookup"><span data-stu-id="5534e-165">Review the summary of actions, and click **Finish** to complete the export of the certificate.</span></span> <span data-ttu-id="5534e-166">Haga clic en **Aceptar** para confirmar si la exportación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5534e-166">Click **OK** to confirm the successful export.</span></span>

</div>

<div>

## <a name="to-import-the-ca-certification-chain-for-the-internal-interface"></a><span data-ttu-id="5534e-167">Para importar la cadena de certificación de CA de la interfaz interna</span><span class="sxs-lookup"><span data-stu-id="5534e-167">To import the CA certification chain for the internal interface</span></span>

1.  <span data-ttu-id="5534e-168">En cada servidor perimetral, abra Microsoft Management Console (MMC) haciendo clic en **Inicio**, haga clic en **Ejecutar**, escriba **MMC** en el cuadro **abrir** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-168">On each Edge Server, open the Microsoft Management Console (MMC) by clicking **Start**, clicking **Run**, typing **mmc** in the **Open** box, and then clicking **OK**.</span></span>

2.  <span data-ttu-id="5534e-169">En el menú **archivo** , haga clic en **Agregar o quitar complemento** y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-169">On the **File** menu, click **Add/Remove Snap-in**, and then click **Add**.</span></span>

3.  <span data-ttu-id="5534e-170">En el cuadro **Agregar complementos independientes** , haga clic en **certificados** y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-170">In the **Add Standalone Snap-ins** box, click **Certificates**, and then click **Add**.</span></span>

4.  <span data-ttu-id="5534e-171">En el cuadro de diálogo **Complemento de certificados**, haga clic en **Cuenta de equipo** y luego haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-171">In the **Certificate snap-in** dialog box, click **Computer account**, and then click **Next**.</span></span>

5.  <span data-ttu-id="5534e-172">En el cuadro de diálogo **seleccionar equipo** , asegúrese de que la casilla **equipo local: (el equipo en el que se está ejecutando esta consola)** está activada y, a continuación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-172">In the **Select Computer** dialog box, ensure that the **Local computer: (the computer this console is running on)** check box is selected, and then click **Finish**.</span></span>

6.  <span data-ttu-id="5534e-173">Haga clic en **cerrar** y, a continuación, en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-173">Click **Close**, and then click **OK**.</span></span>

7.  <span data-ttu-id="5534e-174">En el árbol de consola, expanda **certificados (equipo local)**, haga clic con el botón secundario en **entidades emisoras raíz de confianza**, seleccione **todas las tareas** y haga clic en **importar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-174">In the console tree, expand **Certificates (Local Computer)**, right-click **Trusted Root Certification Authorities**, point to **All Tasks**, and then click **Import**.</span></span>

8.  <span data-ttu-id="5534e-175">En el asistente, en **archivo para importar**, especifique el nombre de archivo del certificado (es decir, el nombre que especificó al descargar la cadena de certificación de la entidad emisora para la interfaz interna en el procedimiento anterior).</span><span class="sxs-lookup"><span data-stu-id="5534e-175">In the wizard, in **File to Import**, specify the file name of the certificate (that is, the name of that you specified when you downloaded the CA certification chain for the internal interface in the previous procedure).</span></span>

9.  <span data-ttu-id="5534e-176">Repita este procedimiento en cada servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-176">Repeat this procedure on each Edge Server.</span></span>

</div>

<div>

## <a name="to-create-the-certificate-request-for-the-internal-interface"></a><span data-ttu-id="5534e-177">Para crear la solicitud de certificado para la interfaz interna</span><span class="sxs-lookup"><span data-stu-id="5534e-177">To create the certificate request for the internal interface</span></span>

1.  <span data-ttu-id="5534e-178">En uno de los servidores perimetrales, inicie el Asistente para la implementación y, junto al **paso 3: solicitar, instalar o asignar certificados**, haga clic en **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-178">On one of the Edge Servers, start the Deployment Wizard, and next to **Step 3: Request, Install, or Assign Certificates**, click **Run**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5534e-179">Si tiene varios servidores perimetrales en una ubicación de un grupo, puede ejecutar el Asistente para certificados en cualquiera de los servidores perimetrales.</span><span class="sxs-lookup"><span data-stu-id="5534e-179">If you have multiple Edge Servers in one location in a pool, you can run the Certificate Wizard on any one of the Edge Servers.</span></span><BR><span data-ttu-id="5534e-180">Después de ejecutar el paso 3 por primera vez, el botón cambiará a <STRONG>ejecutarse</STRONG>y una marca de verificación verde que indica que la tarea se completó correctamente no se mostrará hasta que se hayan solicitado, instalado y asignado todos los certificados necesarios.</span><span class="sxs-lookup"><span data-stu-id="5534e-180">After you run Step 3 the first time, the button changes to <STRONG>Run again</STRONG>, and a green check mark that indicates successful completion of the task is not displayed until all require certificates have been requested, installed, and assigned.</span></span>

    
    </div>

2.  <span data-ttu-id="5534e-181">En la página **Tareas de certificado disponibles**, haga clic en **Crear una nueva solicitud de certificado**.</span><span class="sxs-lookup"><span data-stu-id="5534e-181">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

3.  <span data-ttu-id="5534e-182">En la página **solicitud de certificado** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-182">On the **Certificate Request** page, click **Next**.</span></span>

4.  <span data-ttu-id="5534e-183">En la página **Solicitudes retrasadas o inmediatas**, haga clic en **Prepare ahora la solicitud, pero envíela más tarde**.</span><span class="sxs-lookup"><span data-stu-id="5534e-183">On the **Delayed or Immediate Requests** page, click **Prepare the request now, but send it later**.</span></span>

5.  <span data-ttu-id="5534e-184">En la página **archivo de solicitud de certificado** , escriba la ruta de acceso completa y el nombre de archivo en el que se va a guardar la solicitud (por ejemplo, **c: \\ CERT \_ Internal \_ Edge. cer**).</span><span class="sxs-lookup"><span data-stu-id="5534e-184">On the **Certificate Request File** page, type the full path and file name to which the request is to be saved (for example, **c:\\cert\_internal\_edge.cer**).</span></span>

6.  <span data-ttu-id="5534e-185">En la página **especificar plantilla de certificado alternativa** , para usar una plantilla distinta de la plantilla predeterminada de WebServer, seleccione la casilla **Usar plantilla de certificado alternativa para la entidad emisora de certificados seleccionada** .</span><span class="sxs-lookup"><span data-stu-id="5534e-185">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected Certificate Authority** check box.</span></span>

7.  <span data-ttu-id="5534e-186">En la página **nombre y configuración de seguridad** , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5534e-186">On the **Name and Security Settings** page, do the following:</span></span>
    
      - <span data-ttu-id="5534e-187">En **nombre descriptivo**, escriba un nombre para mostrar para el certificado (por ejemplo, contorno interno).</span><span class="sxs-lookup"><span data-stu-id="5534e-187">In **Friendly name**, type a display name for the certificate (for example, Internal Edge).</span></span>
    
      - <span data-ttu-id="5534e-188">En **longitud bit**, especifique la longitud en bits (normalmente, el valor predeterminado de **2048**).</span><span class="sxs-lookup"><span data-stu-id="5534e-188">In **Bit length**, specify the bit length (typically, the default of **2048**).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="5534e-189">Las longitudes de bits más altas ofrecen más seguridad pero tienen un impacto negativo en la velocidad.</span><span class="sxs-lookup"><span data-stu-id="5534e-189">Higher bit lengths offer more security, but they have a negative impact on speed.</span></span>

        
        </div>
    
      - <span data-ttu-id="5534e-190">Si es necesario exportar el certificado, active la casilla **marcar clave privada de certificado como exportable** .</span><span class="sxs-lookup"><span data-stu-id="5534e-190">If the certificate needs to be exportable, select the **Mark certificate private key as exportable** check box.</span></span>

8.  <span data-ttu-id="5534e-191">En la página información de la **organización** , escriba el nombre de la organización y la unidad organizativa (OU) (por ejemplo, una división o un departamento).</span><span class="sxs-lookup"><span data-stu-id="5534e-191">On the **Organization Information** page, type the name for the organization and the organizational unit (OU) (for example, a division or department).</span></span>

9.  <span data-ttu-id="5534e-192">En la página **información geográfica** , especifique la información de ubicación.</span><span class="sxs-lookup"><span data-stu-id="5534e-192">On the **Geographical Information** page, specify the location information.</span></span>

10. <span data-ttu-id="5534e-193">En la página **nombre de sujeto/nombres alternativos de asunto** , se muestra la información que el asistente rellenará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5534e-193">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span>

11. <span data-ttu-id="5534e-194">En la página **configurar otros nombres alternativos de asunto** , especifique los nombres alternativos adicionales que sean obligatorios.</span><span class="sxs-lookup"><span data-stu-id="5534e-194">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>

12. <span data-ttu-id="5534e-195">En la página Resumen de la **solicitud** , revise la información del certificado que se va a usar para generar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5534e-195">On the **Request Summary** page, review the certificate information that is going to be used to generate the request.</span></span>

13. <span data-ttu-id="5534e-196">Una vez completados los comandos, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5534e-196">After the commands complete, do the following:</span></span>
    
      - <span data-ttu-id="5534e-197">Para ver el registro de la solicitud de certificado, haga clic en **Ver registro**.</span><span class="sxs-lookup"><span data-stu-id="5534e-197">To view the log for the certificate request, click **View Log**.</span></span>
    
      - <span data-ttu-id="5534e-198">Para completar la solicitud de certificado, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-198">To complete the certificate request, click **Next**.</span></span>

14. <span data-ttu-id="5534e-199">En la página **archivo de solicitud de certificado** , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5534e-199">On the **Certificate Request File** page, do the following:</span></span>
    
      - <span data-ttu-id="5534e-200">Para ver el archivo de solicitud de firma de certificado generado (CSR), haga clic en **Ver**.</span><span class="sxs-lookup"><span data-stu-id="5534e-200">To view the generated certificate signing request (CSR) file, click **View**.</span></span>
    
      - <span data-ttu-id="5534e-201">Para cerrar el asistente, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-201">To close the wizard, click **Finish**.</span></span>

15. <span data-ttu-id="5534e-202">Envíe este archivo a la entidad emisora (por correo electrónico u otro método admitido por su organización para la entidad emisora de certificados de empresa) y, cuando reciba el archivo de respuesta, copie el nuevo certificado en este equipo para que esté disponible para la importación.</span><span class="sxs-lookup"><span data-stu-id="5534e-202">Submit this file to your CA (by email or other method supported by your organization for your enterprise CA) and, when you receive the response file, copy the new certificate to this computer so that it is available for import.</span></span>

</div>

<div>

## <a name="to-import-the-certificate-for-the-internal-interface"></a><span data-ttu-id="5534e-203">Para importar el certificado de la interfaz interna</span><span class="sxs-lookup"><span data-stu-id="5534e-203">To import the certificate for the internal interface</span></span>

1.  <span data-ttu-id="5534e-204">Inicie sesión en el servidor perimetral en el que creó la solicitud de certificado como miembro del grupo de administradores local.</span><span class="sxs-lookup"><span data-stu-id="5534e-204">Log on to the Edge Server on which you created the certificate request as a member of the local Administrators group.</span></span>

2.  <span data-ttu-id="5534e-205">En el Asistente para la implementación, junto al **paso 3: solicitar, instalar o asignar certificados**, haga clic en **Ejecutar de nuevo**.</span><span class="sxs-lookup"><span data-stu-id="5534e-205">In the Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <span data-ttu-id="5534e-206">Después de ejecutar el paso 3 por primera vez, el botón cambia a **ejecutarse**, pero no se muestra una marca de verificación verde (que indica que la tarea se ha completado correctamente) hasta que se hayan solicitado, instalado y asignado todos los certificados necesarios.</span><span class="sxs-lookup"><span data-stu-id="5534e-206">After you run Step 3 the first time, the button changes to **Run again**, but a green check mark (indicating successful completion of the task) is not displayed until all require certificates have been requested, installed, and assigned.</span></span>

3.  <span data-ttu-id="5534e-207">En la página **tareas de certificados disponibles** , haga clic en **importar un certificado desde un. Archivo P7b,. pfx o. cer**.</span><span class="sxs-lookup"><span data-stu-id="5534e-207">On the **Available Certificate Tasks** page, click **Import a certificate from a .P7b, .pfx or .cer file**.</span></span>

4.  <span data-ttu-id="5534e-208">En la página **importar certificado** , escriba la ruta de acceso completa y el nombre de archivo del certificado que solicitó y recibió para la interfaz interna de este servidor perimetral (o bien, haga clic en **examinar** para buscar y seleccionar el archivo).</span><span class="sxs-lookup"><span data-stu-id="5534e-208">On the **Import Certificate** page, type the full path and file name of the certificate that you requested and received for the internal interface of this Edge Server (or, click **Browse** to locate and select the file).</span></span>

5.  <span data-ttu-id="5534e-209">Si va a importar certificados de otros miembros del grupo, un certificado que contenga una clave privada, seleccione la casilla el **archivo de certificado contiene la clave privada del certificado** y especifique la contraseña.</span><span class="sxs-lookup"><span data-stu-id="5534e-209">If you are importing certificates for other members of the pool a certificate containing a private key, select the **Certificate file contains certifcate’s private key** check box and specify the password.</span></span>

</div>

<div>

## <a name="to-export-the-certificate-with-the-private-key-for-edge-servers-in-a-pool"></a><span data-ttu-id="5534e-210">Para exportar el certificado con la clave privada para servidores perimetrales en un grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="5534e-210">To export the certificate with the private key for Edge Servers in a pool</span></span>

1.  <span data-ttu-id="5534e-211">Inicie sesión como miembro del grupo administradores en el mismo servidor perimetral en el que importó el certificado.</span><span class="sxs-lookup"><span data-stu-id="5534e-211">Log on as a member of the Administrators group to the same Edge Server on which you imported the certificate.</span></span>

2.  <span data-ttu-id="5534e-212">Haga clic en **Inicio**, haga clic en **Ejecutar** y escriba **MMC**.</span><span class="sxs-lookup"><span data-stu-id="5534e-212">Click **Start**, click **Run**, and type **MMC**.</span></span>

3.  <span data-ttu-id="5534e-213">Desde la consola MMC, haga clic en **archivo** y en **Agregar o quitar complemento**.</span><span class="sxs-lookup"><span data-stu-id="5534e-213">From the MMC console, click **File**, click **Add/Remove Snap-in**.</span></span>

4.  <span data-ttu-id="5534e-214">En la página Agregar o quitar complementos, haga clic en **certificados** y, después, en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-214">From Add or Remove Snap-ins page, click **Certificates**, click **Add**.</span></span>

5.  <span data-ttu-id="5534e-215">En el cuadro de diálogo del complemento certificados, seleccione **cuenta de equipo**.</span><span class="sxs-lookup"><span data-stu-id="5534e-215">In the Certificates snap-in dialog, select **Computer account**.</span></span> <span data-ttu-id="5534e-216">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-216">Click **Next**.</span></span> <span data-ttu-id="5534e-217">En seleccionar equipo, seleccione **equipo local: (el equipo en el que se está ejecutando esta consola)**.</span><span class="sxs-lookup"><span data-stu-id="5534e-217">In Select Computer, select **Local computer: (the computer this console is running on)**.</span></span> <span data-ttu-id="5534e-218">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-218">Click **Finish**.</span></span> <span data-ttu-id="5534e-219">Haga clic en **Aceptar** para completar la configuración de la consola MMC.</span><span class="sxs-lookup"><span data-stu-id="5534e-219">Click **OK** to complete configuration of the MMC console.</span></span>

6.  <span data-ttu-id="5534e-220">Haga doble clic en **Certificados (equipo local)** para expandir los almacenes de certificados.</span><span class="sxs-lookup"><span data-stu-id="5534e-220">Double-click **Certificates (Local Computer)** to expand the certificate stores.</span></span> <span data-ttu-id="5534e-221">Haga doble clic en **personal** y, a continuación, haga doble clic en **certificados**.</span><span class="sxs-lookup"><span data-stu-id="5534e-221">Double-click **Personal**, then double-click **Certificates**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5534e-222">Si no hay certificados en el almacén personal de certificados para el equipo local, no hay ninguna clave privada asociada al certificado que se importó.</span><span class="sxs-lookup"><span data-stu-id="5534e-222">If there are no certificates in the Certificates Personal store for the local computer, there is no private key associated with the certificate that was imported.</span></span> <span data-ttu-id="5534e-223">Revise los pasos de la solicitud e importar.</span><span class="sxs-lookup"><span data-stu-id="5534e-223">Review the request and import steps.</span></span> <span data-ttu-id="5534e-224">Si el problema persiste, póngase en contacto con el administrador o el proveedor de su entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="5534e-224">If the problem persists, contact your certification authority administrator or provider.</span></span>

    
    </div>

7.  <span data-ttu-id="5534e-225">En el almacén personal de certificados del equipo local, haga clic con el botón secundario en el certificado que va a exportar.</span><span class="sxs-lookup"><span data-stu-id="5534e-225">In the Certificates Personal store for the local computer, right-click the certificate that you are exporting.</span></span> <span data-ttu-id="5534e-226">Haga clic en **todas las tareas**, en **exportar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-226">Click **All Tasks**, click **Export**.</span></span>

8.  <span data-ttu-id="5534e-227">En el Asistente para exportación de certificados, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-227">In the Certificate Export Wizard, click **Next**.</span></span> <span data-ttu-id="5534e-228">Seleccione **sí, exportar la clave privada**.</span><span class="sxs-lookup"><span data-stu-id="5534e-228">Select **Yes, export the private key**.</span></span> <span data-ttu-id="5534e-229">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-229">Click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5534e-230">Si la selección <STRONG>sí, exportar la clave privada</STRONG> no está disponible, la clave privada asociada a este certificado no se marcó para exportar.</span><span class="sxs-lookup"><span data-stu-id="5534e-230">If the selection <STRONG>Yes, export the private key</STRONG> is not available, the private key associated with this certificate was not marked for export.</span></span> <span data-ttu-id="5534e-231">Tendrá que volver a solicitar el certificado, lo que garantiza que el certificado estará marcado para permitir la exportación de la clave privada antes de poder continuar con la exportación.</span><span class="sxs-lookup"><span data-stu-id="5534e-231">You will need to request the certificate again, ensuring that the certificate is marked to allow for the export of the private key before you can continue with the export.</span></span> <span data-ttu-id="5534e-232">Póngase en contacto con el administrador o proveedor de su entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="5534e-232">Contact your certification authority administrator or provider.</span></span>

    
    </div>

9.  <span data-ttu-id="5534e-233">En el cuadro de diálogo Exportar formatos de archivo, seleccione **intercambio de información personal – PKCS \# 12 (. PFX)** y, a continuación, seleccione lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5534e-233">On the Export File Formats dialog, select **Personal Information Exchange – PKCS\#12 (.PFX)** and then select the following:</span></span>
    
      - <span data-ttu-id="5534e-234">Incluir todos los certificados en la ruta de certificación si es posible</span><span class="sxs-lookup"><span data-stu-id="5534e-234">Include all certificates in the certification path if possible</span></span>
    
      - <span data-ttu-id="5534e-235">Exportar todas las propiedades extendidas</span><span class="sxs-lookup"><span data-stu-id="5534e-235">Export all extended properties</span></span>
        
        <div>
        

        > [!WARNING]  
        > <span data-ttu-id="5534e-236">Al exportar el certificado desde un servidor perimetral, no seleccione <STRONG>eliminar la clave privada si la exportación es correcta</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5534e-236">When exporting the certificate from an Edge server, do not select <STRONG>Delete the private key if the export is successful</STRONG>.</span></span> <span data-ttu-id="5534e-237">Si selecciona esta opción, necesitará importar el certificado y la clave privada a este servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-237">Selecting this option will require that you import the certificate and the private key to this Edge server.</span></span>

        
        </div>
    
    <span data-ttu-id="5534e-238">Haga clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="5534e-238">Click **Next** to continue.</span></span>

10. <span data-ttu-id="5534e-239">Si desea asignar una contraseña para proteger la clave privada, escriba una contraseña para la clave privada.</span><span class="sxs-lookup"><span data-stu-id="5534e-239">If you want to assign password to protect the private key, type a password for the private key.</span></span> <span data-ttu-id="5534e-240">Vuelva a escribir la contraseña para confirmarla.</span><span class="sxs-lookup"><span data-stu-id="5534e-240">Re-enter the password to confirm.</span></span> <span data-ttu-id="5534e-241">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-241">Click **Next**.</span></span>

11. <span data-ttu-id="5534e-242">Escriba la ruta y el nombre de archivo del certificado exportado, con la extensión de archivo .pfx.</span><span class="sxs-lookup"><span data-stu-id="5534e-242">Type a path and file name for the exported certificate, using a file extension of .pfx.</span></span> <span data-ttu-id="5534e-243">La ruta de acceso debe ser accesible para todos los demás servidores perimetrales del grupo o disponible para el transporte por medio de medios extraíbles, por ejemplo, una unidad flash USB.</span><span class="sxs-lookup"><span data-stu-id="5534e-243">The path must either be accessible to all other Edge servers in the pool or available to transport by means of removable media - for example, a USB flash drive.</span></span> <span data-ttu-id="5534e-244">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-244">Click **Next**.</span></span>

12. <span data-ttu-id="5534e-245">Revise el resumen en el cuadro de diálogo completando el Asistente para exportación de certificados.</span><span class="sxs-lookup"><span data-stu-id="5534e-245">Review the summary on the Completing the Certificate Export Wizard dialog.</span></span> <span data-ttu-id="5534e-246">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-246">Click **Finish**.</span></span>

13. <span data-ttu-id="5534e-247">Haga clic en **Aceptar** en el cuadro de diálogo de exportación correcta.</span><span class="sxs-lookup"><span data-stu-id="5534e-247">Click **OK** in the successful export dialog.</span></span>

14. <span data-ttu-id="5534e-248">Importe el archivo de certificado exportado a los otros servidores perimetrales siguiendo los pasos descritos en los procedimientos de [configuración de certificados para la interfaz de borde externo de Lync Server 2013](lync-server-2013-set-up-certificates-for-the-external-edge-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="5534e-248">Import the exported certificate file to the other Edge servers following the steps outlined in the [Set up certificates for the external edge interface for Lync Server 2013](lync-server-2013-set-up-certificates-for-the-external-edge-interface.md) procedures.</span></span>

</div>

<div>

## <a name="to-assign-the-internal-certificate-on-the-edge-servers"></a><span data-ttu-id="5534e-249">Para asignar el certificado interno en los servidores perimetrales</span><span class="sxs-lookup"><span data-stu-id="5534e-249">To assign the internal certificate on the Edge Servers</span></span>

1.  <span data-ttu-id="5534e-250">En cada servidor perimetral, en el Asistente para la implementación, junto al **paso 3: solicitar, instalar o asignar certificados**, haga clic en **Ejecutar de nuevo**.</span><span class="sxs-lookup"><span data-stu-id="5534e-250">On each Edge Server, in the Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>

2.  <span data-ttu-id="5534e-251">En la página **tareas de certificados disponibles** , haga clic en **asignar un certificado existente**.</span><span class="sxs-lookup"><span data-stu-id="5534e-251">On the **Available Certificate Tasks** page, click **Assign an existing certificate**.</span></span>

3.  <span data-ttu-id="5534e-252">En la página **Asignación del certificado**, seleccione **Interfaz perimetral interna** en la lista.</span><span class="sxs-lookup"><span data-stu-id="5534e-252">On the **Certificate Assignment** page, select **Edge Internal** in the list.</span></span>

4.  <span data-ttu-id="5534e-253">En la página **almacén de certificados** , seleccione el certificado importado para el contorno interno (desde el procedimiento anterior).</span><span class="sxs-lookup"><span data-stu-id="5534e-253">On the **Certificate Store** page, select the certificate that you imported for the internal edge (from the previous procedure).</span></span>

5.  <span data-ttu-id="5534e-254">En la página **Resumen de asignación de certificado** , revise la configuración y, a continuación, haga clic en **siguiente** para asignar los certificados.</span><span class="sxs-lookup"><span data-stu-id="5534e-254">On the **Certificate Assignment Summary** page, review your settings, and then click **Next** to assign the certificates.</span></span>

6.  <span data-ttu-id="5534e-255">En la página de finalización del asistente, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="5534e-255">On the wizard completion page, click **Finish**.</span></span>

7.  <span data-ttu-id="5534e-256">Después de usar este procedimiento para asignar el certificado de contorno interno, abra el complemento certificado en cada servidor, expanda **certificados (equipo local)**, expanda **personal**, haga clic en **certificados** y, a continuación, compruebe en el panel de detalles que aparece el certificado de contorno interno.</span><span class="sxs-lookup"><span data-stu-id="5534e-256">After using this procedure to assign the internal edge certificate, open the Certificate snap-in on each server, expand **Certificates (Local computer)**, expand **Personal**, click **Certificates**, and then verify in the details pane that the internal edge certificate is listed.</span></span>

8.  <span data-ttu-id="5534e-257">Si su implementación incluye varios servidores perimetrales, repita este procedimiento para cada servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5534e-257">If your deployment includes multiple Edge Servers, repeat this procedure for each Edge Server.</span></span>

<span data-ttu-id="5534e-258"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5534e-258"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

