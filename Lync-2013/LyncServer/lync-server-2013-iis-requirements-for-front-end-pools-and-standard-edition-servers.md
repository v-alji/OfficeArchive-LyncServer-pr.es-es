---
title: Requisitos de IIS para grupos de servidores front-end y servidores Standard Edition
description: Requisitos de IIS para las agrupaciones front end y los servidores Standard Edition.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IIS requirements for Front End pools and Standard Edition servers
ms:assetid: e8a6c7ac-b6d5-4c7e-abe9-d8ea5eedbc62
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399038(v=OCS.15)
ms:contentKeyID: 48185888
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f56452c7e47352333ac3ac5a51d649b0828a0ff9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427428"
---
# <a name="iis-requirements-for-front-end-pools-and-standard-edition-servers-in-lync-server-2013"></a><span data-ttu-id="613b0-103">Requisitos de IIS para grupos de servidores front-end y servidores Standard Edition en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="613b0-103">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="613b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="613b0-104">

<span> </span></span></span>

<span data-ttu-id="613b0-105">_**Última modificación del tema:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="613b0-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="613b0-106">Para los servidores Standard Edition y los servidores front-end y directores, el instalador de Lync Server 2013 crea directorios virtuales en servicios de Internet Information Server (IIS) para los siguientes fines:</span><span class="sxs-lookup"><span data-stu-id="613b0-106">For Standard Edition servers and Front End Servers, and Directors, the Lync Server 2013 installer creates virtual directories in Internet Information Services (IIS) for the following purposes:</span></span>

  - <span data-ttu-id="613b0-107">Para permitir que los usuarios descarguen archivos desde el servicio de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="613b0-107">To enable users to download files from the Address Book Service</span></span>

  - <span data-ttu-id="613b0-108">Para permitir que los clientes obtengan actualizaciones</span><span class="sxs-lookup"><span data-stu-id="613b0-108">To enable clients to obtain updates</span></span>

  - <span data-ttu-id="613b0-109">Para habilitar la Conferencia</span><span class="sxs-lookup"><span data-stu-id="613b0-109">To enable conferencing</span></span>

  - <span data-ttu-id="613b0-110">Para permitir que los usuarios descarguen contenido de la reunión</span><span class="sxs-lookup"><span data-stu-id="613b0-110">To enable users to download meeting content</span></span>

  - <span data-ttu-id="613b0-111">Para permitir a los usuarios expandir grupos de distribución</span><span class="sxs-lookup"><span data-stu-id="613b0-111">To enable users to expand distribution groups</span></span>

  - <span data-ttu-id="613b0-112">Para habilitar las conferencias telefónicas</span><span class="sxs-lookup"><span data-stu-id="613b0-112">To enable phone conferencing</span></span>

  - <span data-ttu-id="613b0-113">Para habilitar las características de grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="613b0-113">To enable response group features</span></span>

<span data-ttu-id="613b0-114">Además, la actualización acumulativa para Lync Server 2010: el instalador de 2011 de noviembre crea directorios virtuales en IIS con los siguientes fines:</span><span class="sxs-lookup"><span data-stu-id="613b0-114">In addition, the cumulative update for Lync Server 2010: November 2011 installer creates virtual directories in IIS for the following purposes:</span></span>

  - <span data-ttu-id="613b0-115">En servidores front-end o servidores Standard Edition para admitir la funcionalidad de movilidad, como la mensajería instantánea (mi) y la presencia, en dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="613b0-115">On Front End Servers or Standard Edition servers to support mobility functionality, such as instant messaging (IM) and presence, on mobile devices</span></span>

  - <span data-ttu-id="613b0-116">En servidores front-end o servidores Standard Edition y en directores para permitir que los dispositivos móviles descubran automáticamente los recursos de movilidad</span><span class="sxs-lookup"><span data-stu-id="613b0-116">On Front End Servers or Standard Edition servers and on Directors to enable mobile devices to automatically discover mobility resources</span></span>



> [!NOTE]
> <span data-ttu-id="613b0-117">Si va a implementar la movilidad, le recomendamos que use IIS 7,5.</span><span class="sxs-lookup"><span data-stu-id="613b0-117">If you are deploying mobility, we recommend that you use IIS 7.5.</span></span> <span data-ttu-id="613b0-118">El instalador del servicio de movilidad de Lync Server establece algunas marcas ASP.NET para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="613b0-118">The Lync Server Mobility Service installer sets some ASP.NET flags to improve performance.</span></span> <span data-ttu-id="613b0-119">IIS 7,5 se instala de forma predeterminada en Windows Server 2008 R2 y el instalador del servicio de movilidad cambia automáticamente la configuración de ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="613b0-119">IIS 7.5 is installed by default on Windows Server 2008 R2, and the Mobility Service installer automatically changes the ASP.NET settings.</span></span> <span data-ttu-id="613b0-120">Si usa IIS 7,0 en Windows Server 2008, tendrá que cambiar manualmente esta configuración.</span><span class="sxs-lookup"><span data-stu-id="613b0-120">If you use IIS 7.0 on Windows Server 2008, you need to manually change these settings.</span></span>



<span data-ttu-id="613b0-121">Lync Server requiere que se instalen los siguientes módulos de IIS:</span><span class="sxs-lookup"><span data-stu-id="613b0-121">Lync Server requires the following IIS modules to be installed:</span></span>


> [!IMPORTANT]
> <span data-ttu-id="613b0-122">Si su organización requiere que encuentre IIS y todos los servicios web en una unidad distinta de la del sistema, puede cambiar la ruta de acceso de la ubicación de instalación para los archivos de Lync Server en el cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="613b0-122">If your organization requires that you locate IIS and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server files in the Setup dialog box.</span></span> <span data-ttu-id="613b0-123">Si instala los archivos de instalación en esta ruta de acceso, incluidos OCSCore.msi, el resto de los archivos de Lync Server también se implementarán en esta unidad.</span><span class="sxs-lookup"><span data-stu-id="613b0-123">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server files will be deployed to this drive as well.</span></span> <span data-ttu-id="613b0-124">Para más información sobre cómo cambiar la ubicación de INETPUB implementada por el administrador de Windows Server al instalar IIS, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A> .</span><span class="sxs-lookup"><span data-stu-id="613b0-124">For details about how to relocate the INETPUB deployed by Windows Server Manager when installing IIS, see <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A>.</span></span>


  - <span data-ttu-id="613b0-125">Contenido estático</span><span class="sxs-lookup"><span data-stu-id="613b0-125">Static Content</span></span>

  - <span data-ttu-id="613b0-126">Documento predeterminado</span><span class="sxs-lookup"><span data-stu-id="613b0-126">Default Document</span></span>

  - <span data-ttu-id="613b0-127">Errores HTTP</span><span class="sxs-lookup"><span data-stu-id="613b0-127">HTTP Errors</span></span>

  - <span data-ttu-id="613b0-128">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="613b0-128">ASP.NET</span></span>

  - <span data-ttu-id="613b0-129">Extensibilidad de .NET</span><span class="sxs-lookup"><span data-stu-id="613b0-129">.NET Extensibility</span></span>

  - <span data-ttu-id="613b0-130">Extensiones de API de servidor de Internet (ISAPI)</span><span class="sxs-lookup"><span data-stu-id="613b0-130">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="613b0-131">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="613b0-131">ISAPI Filters</span></span>

  - <span data-ttu-id="613b0-132">Registro HTTP</span><span class="sxs-lookup"><span data-stu-id="613b0-132">HTTP Logging</span></span>

  - <span data-ttu-id="613b0-133">Herramientas de registro</span><span class="sxs-lookup"><span data-stu-id="613b0-133">Logging Tools</span></span>

  - <span data-ttu-id="613b0-134">Seguimiento</span><span class="sxs-lookup"><span data-stu-id="613b0-134">Tracing</span></span>

  - <span data-ttu-id="613b0-135">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="613b0-135">Windows Authentication</span></span>

  - <span data-ttu-id="613b0-136">Filtro de solicitudes</span><span class="sxs-lookup"><span data-stu-id="613b0-136">Request Filtering</span></span>

  - <span data-ttu-id="613b0-137">Compresión de contenido estático</span><span class="sxs-lookup"><span data-stu-id="613b0-137">Static Content Compression</span></span>

  - <span data-ttu-id="613b0-138">Compresión de contenido dinámico</span><span class="sxs-lookup"><span data-stu-id="613b0-138">Dynamic Content Compression</span></span>

  - <span data-ttu-id="613b0-139">Consola de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="613b0-139">IIS Management Console</span></span>

  - <span data-ttu-id="613b0-140">Scripts y herramientas de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="613b0-140">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="613b0-141">Autenticación anónima (se instala de forma predeterminada cuando se instala IIS)</span><span class="sxs-lookup"><span data-stu-id="613b0-141">Anonymous Authentication (installed by default when IIS is installed)</span></span>

  - <span data-ttu-id="613b0-142">Autenticación por asignación de certificados de clientes</span><span class="sxs-lookup"><span data-stu-id="613b0-142">Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="613b0-143">En la tabla siguiente se enumeran los URI de los directorios virtuales de acceso interno y los recursos del sistema de archivos a los que hacen referencia.</span><span class="sxs-lookup"><span data-stu-id="613b0-143">The following table lists the URIs for the virtual directories for internal access and the file system resources to which they refer.</span></span>

### <a name="virtual-directories-for-internal-access"></a><span data-ttu-id="613b0-144">Directorios virtuales para acceso interno</span><span class="sxs-lookup"><span data-stu-id="613b0-144">Virtual Directories for Internal Access</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="613b0-145">Característica</span><span class="sxs-lookup"><span data-stu-id="613b0-145">Feature</span></span></th>
<th><span data-ttu-id="613b0-146">URI de directorio virtual</span><span class="sxs-lookup"><span data-stu-id="613b0-146">Virtual directory URI</span></span></th>
<th><span data-ttu-id="613b0-147">Se refiere a</span><span class="sxs-lookup"><span data-stu-id="613b0-147">Refers to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="613b0-148">Servidor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="613b0-148">Address Book Server</span></span></p></td>
<td><p><span data-ttu-id="613b0-149"> https:// &lt; FQDN interno de &gt; /ABS/int/handler</span><span class="sxs-lookup"><span data-stu-id="613b0-149">https://&lt;Internal FQDN&gt;/ABS/int/Handler</span></span></p></td>
<td><p><span data-ttu-id="613b0-150">Ubicación del servidor de libretas de direcciones descargar archivos para usuarios internos.</span><span class="sxs-lookup"><span data-stu-id="613b0-150">Location of Address Book Server download files for internal users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="613b0-151">Servicio Detección automática</span><span class="sxs-lookup"><span data-stu-id="613b0-151">Autodiscover Service</span></span></p></td>
<td><p><span data-ttu-id="613b0-152"> https:// &lt; FQDN interno de &gt; /Autodiscover</span><span class="sxs-lookup"><span data-stu-id="613b0-152">https://&lt;Internal FQDN&gt;/Autodiscover</span></span></p></td>
<td><p><span data-ttu-id="613b0-153">Ubicación del servicio Detección automática de Lync Server que busca recursos de movilidad para usuarios internos de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="613b0-153">Location of the Lync Server Autodiscover Service that locates mobility resources for internal mobile device users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="613b0-154">Actualizaciones del cliente</span><span class="sxs-lookup"><span data-stu-id="613b0-154">Client updates</span></span></p></td>
<td><p><span data-ttu-id="613b0-155"> http:// &lt; FQDN interno de &gt; /AutoUpdate/int</span><span class="sxs-lookup"><span data-stu-id="613b0-155">http://&lt;Internal FQDN&gt;/AutoUpdate/Int</span></span></p></td>
<td><p><span data-ttu-id="613b0-156">Ubicación de los archivos de actualización para clientes internos basados en equipos.</span><span class="sxs-lookup"><span data-stu-id="613b0-156">Location of update files for internal computer-based clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="613b0-157">Conferencia</span><span class="sxs-lookup"><span data-stu-id="613b0-157">Conf</span></span></p></td>
<td><p><span data-ttu-id="613b0-158"> http:// &lt; FQDN interno de &gt; /conf/int</span><span class="sxs-lookup"><span data-stu-id="613b0-158">http://&lt;Internal FQDN&gt;/Conf/Int</span></span></p></td>
<td><p><span data-ttu-id="613b0-159">Ubicación de los recursos de conferencia para usuarios internos.</span><span class="sxs-lookup"><span data-stu-id="613b0-159">Location of conferencing resources for internal users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="613b0-160">Actualizaciones de dispositivos</span><span class="sxs-lookup"><span data-stu-id="613b0-160">Device updates</span></span></p></td>
<td><p><span data-ttu-id="613b0-161">&lt;FQDN http:// &gt; /DeviceUpdateFiles_Int interno</span><span class="sxs-lookup"><span data-stu-id="613b0-161">http://&lt;Internal FQDN&gt;/DeviceUpdateFiles_Int</span></span></p></td>
<td><p><span data-ttu-id="613b0-162">Ubicación de los archivos de actualización de dispositivos de comunicaciones unificadas (UC) para dispositivos internos de UC.</span><span class="sxs-lookup"><span data-stu-id="613b0-162">Location of unified communications (UC) device update files for internal UC devices.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="613b0-163">Reunión</span><span class="sxs-lookup"><span data-stu-id="613b0-163">Meeting</span></span></p></td>
<td><p><span data-ttu-id="613b0-164"> http:// &lt; FQDN interno de &gt; /etc/Place/null</span><span class="sxs-lookup"><span data-stu-id="613b0-164">http://&lt;Internal FQDN&gt;/etc/place/null</span></span></p></td>
<td><p><span data-ttu-id="613b0-165">Ubicación del contenido de la reunión para usuarios internos.</span><span class="sxs-lookup"><span data-stu-id="613b0-165">Location of meeting content for internal users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="613b0-166">Servicio de movilidad</span><span class="sxs-lookup"><span data-stu-id="613b0-166">Mobility Service</span></span></p></td>
<td><p><span data-ttu-id="613b0-167"> https:// &lt; FQDN interno de &gt; /MCX</span><span class="sxs-lookup"><span data-stu-id="613b0-167">https://&lt;Internal FQDN&gt;/Mcx</span></span></p></td>
<td><p><span data-ttu-id="613b0-168">Ubicación de los recursos del servicio de movilidad para usuarios internos de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="613b0-168">Location of Mobility Service resources for internal mobile device users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="613b0-169">Servicio de consulta Web de expansión de grupo y libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="613b0-169">Group Expansion and Address Book Web Query service</span></span></p></td>
<td><p><span data-ttu-id="613b0-170"> http:// &lt; FQDN interno de &gt; /GroupExpansion/int/Service.asmx</span><span class="sxs-lookup"><span data-stu-id="613b0-170">http://&lt;Internal FQDN&gt;/GroupExpansion/int/service.asmx</span></span></p></td>
<td><p><span data-ttu-id="613b0-171">Ubicación del servicio Web que permite la expansión de grupos para usuarios internos.</span><span class="sxs-lookup"><span data-stu-id="613b0-171">Location of the Web service that enables group expansion for internal users.</span></span> <span data-ttu-id="613b0-172">Además, la ubicación del servicio de consultas Web de la libreta de direcciones que proporciona información de la lista global de direcciones a los clientes móviles internos de Lync Mobile Microsoft Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="613b0-172">Also, the location of the Address Book Web Query service that provides global address list information to internal Lync Mobile Microsoft Lync 2010 Mobile clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="613b0-173">Conferencias telefónicas</span><span class="sxs-lookup"><span data-stu-id="613b0-173">Phone Conferencing</span></span></p></td>
<td><p><span data-ttu-id="613b0-174"> http:// &lt; FQDN interno de &gt; /PhoneConferencing/int</span><span class="sxs-lookup"><span data-stu-id="613b0-174">http://&lt;Internal FQDN&gt;/PhoneConferencing/Int</span></span></p></td>
<td><p><span data-ttu-id="613b0-175">Ubicación de los datos de la conferencia telefónica para usuarios internos.</span><span class="sxs-lookup"><span data-stu-id="613b0-175">Location of phone conferencing data for internal users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="613b0-176">Actualizaciones de dispositivos</span><span class="sxs-lookup"><span data-stu-id="613b0-176">Device updates</span></span></p></td>
<td><p><span data-ttu-id="613b0-177"> http:// &lt; FQDN interno de &gt; /RequestHandler</span><span class="sxs-lookup"><span data-stu-id="613b0-177">http://&lt;Internal FQDN&gt;/RequestHandler</span></span></p></td>
<td><p><span data-ttu-id="613b0-178">Ubicación del controlador de solicitudes de servicio Web de actualización de dispositivos que permite a los dispositivos de UC internos cargar registros y comprobar si hay actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="613b0-178">Location of the Device Update Web service Request Handler that enables internal UC devices to upload logs and check for updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="613b0-179">Aplicación de grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="613b0-179">Response Group application</span></span></p></td>
<td><p><span data-ttu-id="613b0-180"> http:// &lt; FQDN interno de &gt; /RgsConfig</span><span class="sxs-lookup"><span data-stu-id="613b0-180">http://&lt;Internal FQDN&gt;/RgsConfig</span></span></p>
<p><span data-ttu-id="613b0-181"> http:// &lt; FQDN interno de &gt; /RgsClients</span><span class="sxs-lookup"><span data-stu-id="613b0-181">http://&lt;Internal FQDN&gt;/RgsClients</span></span></p></td>
<td><p><span data-ttu-id="613b0-182">Ubicación de la herramienta de configuración de grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="613b0-182">Location of Response Group Configuration Tool.</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="613b0-183">Para los grupos de servidores front-end en una configuración consolidada, debe implementar IIS antes de agregar servidores al grupo.</span><span class="sxs-lookup"><span data-stu-id="613b0-183">For Front End pools in a consolidated configuration, you must deploy IIS before you can add servers to the pool.</span></span>


<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="seguridad" alt="security" /><span data-ttu-id="613b0-185">Nota de seguridad:</span><span class="sxs-lookup"><span data-stu-id="613b0-185">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="613b0-186">Debe usar el complemento administrativo de IIS para asignar el certificado utilizado por el servidor de componentes Web de IIS.</span><span class="sxs-lookup"><span data-stu-id="613b0-186">You must use the IIS administrative snap-in to assign the certificate used by the IIS web component server.</span></span></td>
</tr>
</tbody>
</table><span data-ttu-id="613b0-187">



</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="613b0-187">



</div>

<span> </span>

</div>

</div>

</span></span></div>

