---
title: 'Lync Server 2013: Configuración de IIS'
description: 'Lync Server 2013: configuración de IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IIS configuration
ms:assetid: b458babf-bf64-43f0-8a8e-612f5096b63c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412871(v=OCS.15)
ms:contentKeyID: 48185169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 901aca7bf5ff8824b54e93754569a6ef5defc10e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427435"
---
# <a name="iis-configuration-in-lync-server-2013"></a><span data-ttu-id="c0be8-103">Configuración de IIS en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0be8-103">IIS configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0be8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0be8-104">

<span> </span></span></span>

<span data-ttu-id="c0be8-105">_**Última modificación del tema:** 2014-02-17_</span><span class="sxs-lookup"><span data-stu-id="c0be8-105">_**Topic Last Modified:** 2014-02-17_</span></span>

<span data-ttu-id="c0be8-106">Para completar correctamente este procedimiento, debe haber iniciado sesión en el servidor como mínimo como administrador local y como usuario del dominio.</span><span class="sxs-lookup"><span data-stu-id="c0be8-106">To successfully complete this procedure, you should be logged on to the server minimally as a local administrator and a domain user.</span></span>

<span data-ttu-id="c0be8-107">Antes de configurar e instalar el servidor front-end para Lync Server 2013, Standard Edition o el primer servidor front-end de un grupo, instale y configure el rol de servidor y los servicios web para servicios de Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="c0be8-107">Before you configure and install the Front End Server for Lync Server 2013, Standard Edition or the first Front End Server in a pool, you install and configure the server role and Web Services for Internet Information Services (IIS).</span></span>

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="c0be8-108">Si su organización requiere que encuentre IIS y todos los servicios web en una unidad distinta de la del sistema, puede cambiar la ruta de acceso de la ubicación de instalación para los archivos de Lync Server 2013 en el cuadro de diálogo de configuración cuando instale inicialmente las herramientas administrativas de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c0be8-108">If your organization requires that you locate IIS and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server 2013 files in the Setup dialog box when you initially install the Lync Server 2013 Administrative tools.</span></span> <span data-ttu-id="c0be8-109">Instale las herramientas administrativas antes de instalar IIS.</span><span class="sxs-lookup"><span data-stu-id="c0be8-109">You install the Administrative tools before installing IIS.</span></span> <span data-ttu-id="c0be8-110">Si instala los archivos de instalación en esta ruta de acceso, incluidos OCSCore.msi, el resto de los archivos de Lync Server 2013 se implementarán también en esta unidad.</span><span class="sxs-lookup"><span data-stu-id="c0be8-110">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive as well.</span></span> <span data-ttu-id="c0be8-111">Para Dtails, consulte <A href="lync-server-2013-install-lync-server-administrative-tools.md">instalar las herramientas administrativas 2013 de Lync Server</A>.</span><span class="sxs-lookup"><span data-stu-id="c0be8-111">For dtails, see <A href="lync-server-2013-install-lync-server-administrative-tools.md">Install Lync Server 2013 administrative tools</A>.</span></span> <span data-ttu-id="c0be8-112">Para más información sobre cómo cambiar la ubicación de INETPUB implementada por el administrador de Windows Server al instalar IIS, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A> .</span><span class="sxs-lookup"><span data-stu-id="c0be8-112">For details about how to relocate the INETPUB deployed by Windows Server Manager when installing IIS, see <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A>.</span></span>



</div>

<span data-ttu-id="c0be8-113">En la tabla siguiente se indican los servicios de rol IIS 7,5 requeridos.</span><span class="sxs-lookup"><span data-stu-id="c0be8-113">The following table indicates the required IIS 7.5 role services.</span></span>

### <a name="iis-75-role-services"></a><span data-ttu-id="c0be8-114">Servicios de rol IIS 7,5</span><span class="sxs-lookup"><span data-stu-id="c0be8-114">IIS 7.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0be8-115">Encabezado de rol</span><span class="sxs-lookup"><span data-stu-id="c0be8-115">Role Heading</span></span></th>
<th><span data-ttu-id="c0be8-116">Servicio de rol</span><span class="sxs-lookup"><span data-stu-id="c0be8-116">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-117">Características HTTP comunes instaladas</span><span class="sxs-lookup"><span data-stu-id="c0be8-117">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="c0be8-118">Contenido estático</span><span class="sxs-lookup"><span data-stu-id="c0be8-118">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-119">Características HTTP comunes instaladas</span><span class="sxs-lookup"><span data-stu-id="c0be8-119">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="c0be8-120">Documento predeterminado</span><span class="sxs-lookup"><span data-stu-id="c0be8-120">Default document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-121">Características HTTP comunes instaladas</span><span class="sxs-lookup"><span data-stu-id="c0be8-121">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="c0be8-122">Errores HTTP</span><span class="sxs-lookup"><span data-stu-id="c0be8-122">HTTP errors</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-123">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0be8-123">Application development</span></span></p></td>
<td><p><span data-ttu-id="c0be8-124">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="c0be8-124">ASP.NET</span></span></p>
<p><span data-ttu-id="c0be8-125">Windows Server 2012 también requiere ASP. NET 4.5</span><span class="sxs-lookup"><span data-stu-id="c0be8-125">Windows Server 2012 also requires ASP.NET4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-126">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0be8-126">Application development</span></span></p></td>
<td><p><span data-ttu-id="c0be8-127">Extensibilidad de .NET</span><span class="sxs-lookup"><span data-stu-id="c0be8-127">.NET extensibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-128">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0be8-128">Application development</span></span></p></td>
<td><p><span data-ttu-id="c0be8-129">Extensiones de API de servidor de Internet (ISAPI)</span><span class="sxs-lookup"><span data-stu-id="c0be8-129">Internet Server API (ISAPI) extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-130">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0be8-130">Application development</span></span></p></td>
<td><p><span data-ttu-id="c0be8-131">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="c0be8-131">ISAPI filters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-132">Estado y diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c0be8-132">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="c0be8-133">Registro HTTP</span><span class="sxs-lookup"><span data-stu-id="c0be8-133">HTTP logging</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-134">Estado y diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c0be8-134">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="c0be8-135">Herramientas de registro</span><span class="sxs-lookup"><span data-stu-id="c0be8-135">Logging tools</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-136">Estado y diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c0be8-136">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="c0be8-137">Seguimiento</span><span class="sxs-lookup"><span data-stu-id="c0be8-137">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-138">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c0be8-138">Security</span></span></p></td>
<td><p><span data-ttu-id="c0be8-139">Autenticación anónima (instalado y habilitado de forma predeterminada)</span><span class="sxs-lookup"><span data-stu-id="c0be8-139">Anonymous authentication (installed and enabled by default)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-140">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c0be8-140">Security</span></span></p></td>
<td><p><span data-ttu-id="c0be8-141">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="c0be8-141">Windows authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-142">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c0be8-142">Security</span></span></p></td>
<td><p><span data-ttu-id="c0be8-143">Autenticación de asignación de certificado de cliente</span><span class="sxs-lookup"><span data-stu-id="c0be8-143">Client Certificate Mapping authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-144">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c0be8-144">Security</span></span></p></td>
<td><p><span data-ttu-id="c0be8-145">Filtrado de solicitudes</span><span class="sxs-lookup"><span data-stu-id="c0be8-145">Request filtering</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-146">Rendimiento</span><span class="sxs-lookup"><span data-stu-id="c0be8-146">Performance</span></span></p></td>
<td><p><span data-ttu-id="c0be8-147">Compresión de contenido estático</span><span class="sxs-lookup"><span data-stu-id="c0be8-147">Static content compression</span></span></p>
<p><span data-ttu-id="c0be8-148">Compresión de contenido dinámico</span><span class="sxs-lookup"><span data-stu-id="c0be8-148">Dynamic content compression</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-149">Herramientas de administración</span><span class="sxs-lookup"><span data-stu-id="c0be8-149">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="c0be8-150">Consola de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="c0be8-150">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-151">Herramientas de administración</span><span class="sxs-lookup"><span data-stu-id="c0be8-151">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="c0be8-152">Scripts y herramientas de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="c0be8-152">IIS Management Scripts and Tools</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c0be8-153">En el sistema operativo Windows Server 2008 R2 SP1 x64, puede usar Windows PowerShell 2,0.</span><span class="sxs-lookup"><span data-stu-id="c0be8-153">On the Windows Server 2008 R2 SP1 x64 operating system, you can use Windows PowerShell 2.0.</span></span> <span data-ttu-id="c0be8-154">Primero debe importar el módulo de ServerManager y, a continuación, instalar el rol y los servicios de rol de IIS 7,5.</span><span class="sxs-lookup"><span data-stu-id="c0be8-154">You must first import the ServerManager module, and then install the IIS 7.5 role and role services.</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Scripting-Tools, Web-Windows-Auth, Web-Asp-Net, Web-Log-Libraries, Web-Http-Tracing, Web-Stat-Compression, Web-Dyn-Compression, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Errors, Web-Http-Logging, Web-Net-Ext, Web-Client-Auth, Web-Filtering, Web-Mgmt-Console
   ```

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="c0be8-155">La autenticación anónima se instala de forma predeterminada con la función de servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="c0be8-155">Anonymous authentication is installed by default with the IIS server role.</span></span> <span data-ttu-id="c0be8-156">Puede administrar la autenticación anónima después de la instalación de IIS.</span><span class="sxs-lookup"><span data-stu-id="c0be8-156">You can manage anonymous authentication after the installation of IIS.</span></span> <span data-ttu-id="c0be8-157">Para obtener más información, vea "habilitar la autenticación anónima (IIS 7)" en <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A> .</span><span class="sxs-lookup"><span data-stu-id="c0be8-157">For details, see “Enable Anonymous Authentication (IIS 7)” at <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A>.</span></span>



</div>

<span data-ttu-id="c0be8-158">La tabla siguiente indica los servicios de rol IIS 8,0 e IIS 8,5 requeridos para Windows Server 2012 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c0be8-158">The following table indicates the required IIS 8.0 and IIS 8.5 role services for Windows Server 2012 and Windows Server 2012 R2.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="c0be8-159">Para Windows Server 2012 y Windows Server 2012 R2, el cmdlet Add-WindowsFeature ha sido reemplazado por el cmdlet Install-WindowsFeature.</span><span class="sxs-lookup"><span data-stu-id="c0be8-159">For Windows Server 2012 and Windows Server 2012 R2, the Add-WindowsFeature cmdlet has been replaced by the Install-WindowsFeature cmdlet.</span></span> <span data-ttu-id="c0be8-160">Para obtener información detallada, vea <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">install-WindowsFeature</A>.</span><span class="sxs-lookup"><span data-stu-id="c0be8-160">For details, see <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">Install-WindowsFeature</A>.</span></span>



</div>

### <a name="iis-80-and-iis-85-role-services"></a><span data-ttu-id="c0be8-161">Servicios de rol IIS 8,0 e IIS 8,5</span><span class="sxs-lookup"><span data-stu-id="c0be8-161">IIS 8.0 and IIS 8.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0be8-162">Encabezado de rol</span><span class="sxs-lookup"><span data-stu-id="c0be8-162">Role Heading</span></span></th>
<th><span data-ttu-id="c0be8-163">Servicio de rol</span><span class="sxs-lookup"><span data-stu-id="c0be8-163">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-164">Servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="c0be8-164">Web Server (IIS)</span></span></p></td>
<td><p><span data-ttu-id="c0be8-165">Servidor Web</span><span class="sxs-lookup"><span data-stu-id="c0be8-165">Web Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-166">Características HTTP comunes</span><span class="sxs-lookup"><span data-stu-id="c0be8-166">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="c0be8-167">Documento predeterminado</span><span class="sxs-lookup"><span data-stu-id="c0be8-167">Default Document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-168">Características HTTP comunes</span><span class="sxs-lookup"><span data-stu-id="c0be8-168">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="c0be8-169">Examen de directorios</span><span class="sxs-lookup"><span data-stu-id="c0be8-169">Directory Browsing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-170">Características HTTP comunes</span><span class="sxs-lookup"><span data-stu-id="c0be8-170">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="c0be8-171">Errores HTTP</span><span class="sxs-lookup"><span data-stu-id="c0be8-171">HTTP Errors</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-172">Características HTTP comunes</span><span class="sxs-lookup"><span data-stu-id="c0be8-172">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="c0be8-173">Contenido estático</span><span class="sxs-lookup"><span data-stu-id="c0be8-173">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-174">Características HTTP comunes</span><span class="sxs-lookup"><span data-stu-id="c0be8-174">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="c0be8-175">Redireccionamiento HTTP</span><span class="sxs-lookup"><span data-stu-id="c0be8-175">HTTP Redirection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-176">Estado y diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c0be8-176">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="c0be8-177">Registro HTTP</span><span class="sxs-lookup"><span data-stu-id="c0be8-177">HTTP Logging</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-178">Estado y diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c0be8-178">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="c0be8-179">Herramientas de registro</span><span class="sxs-lookup"><span data-stu-id="c0be8-179">Logging Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-180">Estado y diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c0be8-180">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="c0be8-181">Solicitar monitor</span><span class="sxs-lookup"><span data-stu-id="c0be8-181">Request Monitor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-182">Estado y diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c0be8-182">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="c0be8-183">Seguimiento</span><span class="sxs-lookup"><span data-stu-id="c0be8-183">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-184">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c0be8-184">Security</span></span></p></td>
<td><p><span data-ttu-id="c0be8-185">Filtro de solicitudes</span><span class="sxs-lookup"><span data-stu-id="c0be8-185">Request Filtering</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-186">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c0be8-186">Security</span></span></p></td>
<td><p><span data-ttu-id="c0be8-187">Autenticación básica</span><span class="sxs-lookup"><span data-stu-id="c0be8-187">Basic Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-188">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c0be8-188">Security</span></span></p></td>
<td><p><span data-ttu-id="c0be8-189">Autenticación por asignación de certificados de clientes</span><span class="sxs-lookup"><span data-stu-id="c0be8-189">Client Certificate Mapping Authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-190">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c0be8-190">Security</span></span></p></td>
<td><p><span data-ttu-id="c0be8-191">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="c0be8-191">Windows Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-192">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0be8-192">Application Development</span></span></p></td>
<td><p><span data-ttu-id="c0be8-193">Extensibilidad de .net 3,5</span><span class="sxs-lookup"><span data-stu-id="c0be8-193">.Net Extensibility 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-194">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0be8-194">Application Development</span></span></p></td>
<td><p><span data-ttu-id="c0be8-195">Extensibilidad de .net 4,5</span><span class="sxs-lookup"><span data-stu-id="c0be8-195">.Net Extensibility 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-196">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0be8-196">Application Development</span></span></p></td>
<td><p><span data-ttu-id="c0be8-197">ASP.Net 3,5</span><span class="sxs-lookup"><span data-stu-id="c0be8-197">ASP.Net 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-198">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0be8-198">Application Development</span></span></p></td>
<td><p><span data-ttu-id="c0be8-199">ASP.Net 4,5</span><span class="sxs-lookup"><span data-stu-id="c0be8-199">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-200">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0be8-200">Application Development</span></span></p></td>
<td><p><span data-ttu-id="c0be8-201">Extensiones ISAPI</span><span class="sxs-lookup"><span data-stu-id="c0be8-201">ISAPI Extensions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-202">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0be8-202">Application Development</span></span></p></td>
<td><p><span data-ttu-id="c0be8-203">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="c0be8-203">ISAPI Filters</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-204">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0be8-204">Application Development</span></span></p></td>
<td><p><span data-ttu-id="c0be8-205">Inclusiones del servidor</span><span class="sxs-lookup"><span data-stu-id="c0be8-205">Server Side Includes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-206">Herramientas de administración</span><span class="sxs-lookup"><span data-stu-id="c0be8-206">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="c0be8-207">Consola de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="c0be8-207">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-208">Herramientas de administración</span><span class="sxs-lookup"><span data-stu-id="c0be8-208">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="c0be8-209">Compatibilidad de metabase de IIS 6</span><span class="sxs-lookup"><span data-stu-id="c0be8-209">IIS 6 Metabase compatibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-210">Herramientas de administración</span><span class="sxs-lookup"><span data-stu-id="c0be8-210">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="c0be8-211">Scripts y herramientas de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="c0be8-211">IIS Management Scripts and Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-212">Características de .net 3,5 Framework</span><span class="sxs-lookup"><span data-stu-id="c0be8-212">.Net 3.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="c0be8-213">.Net 3,5 Framework</span><span class="sxs-lookup"><span data-stu-id="c0be8-213">.Net 3.5 Framework</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-214">Características de .net 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="c0be8-214">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="c0be8-215">4,5 de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="c0be8-215">.Net Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-216">Características de .net 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="c0be8-216">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="c0be8-217">ASP.Net 4,5</span><span class="sxs-lookup"><span data-stu-id="c0be8-217">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-218">Características de .net 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="c0be8-218">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="c0be8-219">Activación HTTP</span><span class="sxs-lookup"><span data-stu-id="c0be8-219">HTTP Activation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-220">Características de .net 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="c0be8-220">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="c0be8-221">Uso compartido de puertos TCP</span><span class="sxs-lookup"><span data-stu-id="c0be8-221">TCP Port Sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-222">Servicio de transferencia inteligente en segundo plano</span><span class="sxs-lookup"><span data-stu-id="c0be8-222">Background Intelligent Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="c0be8-223">Extensiones de servidor IIS</span><span class="sxs-lookup"><span data-stu-id="c0be8-223">IIS Server Extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-224">Servicios de tinta y escritura a mano</span><span class="sxs-lookup"><span data-stu-id="c0be8-224">Ink and Handwriting Services</span></span></p></td>
<td><p><span data-ttu-id="c0be8-225">Servicios de tinta y escritura a mano</span><span class="sxs-lookup"><span data-stu-id="c0be8-225">Ink and Handwriting Services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-226">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0be8-226">Media Foundation</span></span></p></td>
<td><p><span data-ttu-id="c0be8-227">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0be8-227">Media Foundation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-228">Infraestructura y interfaces de usuario</span><span class="sxs-lookup"><span data-stu-id="c0be8-228">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="c0be8-229">Herramientas de administración gráfica e infraestructura</span><span class="sxs-lookup"><span data-stu-id="c0be8-229">Graphical Management Tools and Infrastructure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-230">Infraestructura y interfaces de usuario</span><span class="sxs-lookup"><span data-stu-id="c0be8-230">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="c0be8-231">Experiencia de escritorio</span><span class="sxs-lookup"><span data-stu-id="c0be8-231">Desktop Experience</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-232">Infraestructura y interfaces de usuario</span><span class="sxs-lookup"><span data-stu-id="c0be8-232">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="c0be8-233">Shell gráfico de servidor</span><span class="sxs-lookup"><span data-stu-id="c0be8-233">Server Graphical Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-234">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="c0be8-234">Windows Identity Foundation 3.5</span></span></p></td>
<td><p><span data-ttu-id="c0be8-235">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="c0be8-235">Windows Identity Foundation 3.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0be8-236">Servicio de activación de procesos de Windows</span><span class="sxs-lookup"><span data-stu-id="c0be8-236">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="c0be8-237">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="c0be8-237">Process Model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0be8-238">Servicio de activación de procesos de Windows</span><span class="sxs-lookup"><span data-stu-id="c0be8-238">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="c0be8-239">API de configuración</span><span class="sxs-lookup"><span data-stu-id="c0be8-239">Configuration APIs</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c0be8-240">En Windows Server 2012 y Windows Server 2012 R2, puede usar Windows PowerShell 3,0 para instalar los requisitos de IIS.</span><span class="sxs-lookup"><span data-stu-id="c0be8-240">In Windows Server 2012 and Windows Server 2012 R2, you can use Windows PowerShell 3.0 to install the IIS Requirements.</span></span> <span data-ttu-id="c0be8-241">Usar el módulo ServerManager en Windows PowerShell 3,0, escriba:</span><span class="sxs-lookup"><span data-stu-id="c0be8-241">Using the ServerManager module in Windows PowerShell 3.0, type:</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Http-Errors, Web-Asp-Net, Web-Net-Ext, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Logging, Web-Log-Libraries, Web-Request-Monitor, Web-Http-Tracing, Web-Basic-Auth, Web-Windows-Auth, Web-Client-Auth, Web-Filtering, Web-Stat-Compression, Web-Dyn-Compression, NET-Framework-45-Core, NET-WCF-HTTP-Activation45, Web-Asp-Net45, Web-Mgmt-Tools, Web-Scripting-Tools, Web-Mgmt-Console, Web-Mgmt-Compat, Windows-Identity-Foundation, Server-Media-Foundation, BITS -Source D:\sources\sxs
   ```

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="c0be8-242">Novedades de Windows Server 2012 es el parámetro – Source que define dónde se pueden encontrar los medios de origen de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c0be8-242">New with Windows Server 2012 is the –Source parameter that defines where the Windows Server 2012 source media can be found.</span></span> <span data-ttu-id="c0be8-243">El medio se puede definir como una unidad de DVD (por ejemplo, D:\Sources\Sxs) o como un recurso compartido de red en el que se han copiado los archivos multimedia (por ejemplo, \\ fileserver\windows2012\sources\Sxs).</span><span class="sxs-lookup"><span data-stu-id="c0be8-243">The media can be defined as a DVD drive (for example, D:\Sources\Sxs), or to a network share that the media files have been copied (for example, \\fileserver\windows2012\sources\Sxs).</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c0be8-244">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0be8-244">See Also</span></span>


[<span data-ttu-id="c0be8-245">Requisitos de IIS para grupos de servidores front-end y servidores Standard Edition en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0be8-245">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-iis-requirements-for-front-end-pools-and-standard-edition-servers.md)  
  

<span data-ttu-id="c0be8-246"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0be8-246"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

