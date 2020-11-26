---
title: Lista de comprobación de implementación de Lync Server 2013 para conferencias web
description: Lista de comprobación de implementación de Lync Server 2013 para conferencias web.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for web conferencing
ms:assetid: 9908ebe0-e5d3-4920-b9b1-85021f7e69e9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205104(v=OCS.15)
ms:contentKeyID: 48184878
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6194cb71af268a45dc5c142c1814d8c1ef15c09e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429709"
---
# <a name="deployment-checklist-for-web-conferencing-in-lync-server-2013"></a><span data-ttu-id="29dbf-103">Lista de comprobación de implementación para conferencias web en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29dbf-103">Deployment checklist for web conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="29dbf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="29dbf-104">

<span> </span></span></span>

<span data-ttu-id="29dbf-105">_**Última modificación del tema:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="29dbf-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="29dbf-106">Al igual que con la implementación de otros componentes de Lync Server 2013, la implementación de conferencias web requiere que use el generador de topología para crear y publicar una topología que incorpore conferencias.</span><span class="sxs-lookup"><span data-stu-id="29dbf-106">As with deployment of your other Lync Server 2013 components, deployment of web conferencing requires that you use Topology Builder to create and publish a topology that incorporates conferencing.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="29dbf-107">Secuencia de implementación</span><span class="sxs-lookup"><span data-stu-id="29dbf-107">Deployment Sequence</span></span>

<span data-ttu-id="29dbf-108">Puede implementar conferencias al mismo tiempo que implementa su Topología inicial o después de haber implementado al menos un grupo de servidores front-end o un servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="29dbf-108">You can deploy conferencing at the same time that you deploy your initial topology or after you have deployed at least one Front End pool or Standard Edition server.</span></span>

</div>

<div>

## <a name="conferencing-deployment-process"></a><span data-ttu-id="29dbf-109">Proceso de implementación de conferencia</span><span class="sxs-lookup"><span data-stu-id="29dbf-109">Conferencing Deployment Process</span></span>

<span data-ttu-id="29dbf-110">En la tabla siguiente se proporciona una descripción general de los pasos necesarios para implementar las conferencias en una topología existente.</span><span class="sxs-lookup"><span data-stu-id="29dbf-110">The following table provides an overview of the steps required to deploy conferencing into an existing topology.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29dbf-111">Fase</span><span class="sxs-lookup"><span data-stu-id="29dbf-111">Phase</span></span></th>
<th><span data-ttu-id="29dbf-112">Pasos</span><span class="sxs-lookup"><span data-stu-id="29dbf-112">Steps</span></span></th>
<th><span data-ttu-id="29dbf-113">Roles y pertenencias a grupos</span><span class="sxs-lookup"><span data-stu-id="29dbf-113">Roles and group memberships</span></span></th>
<th><span data-ttu-id="29dbf-114">Documentación</span><span class="sxs-lookup"><span data-stu-id="29dbf-114">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29dbf-115"><strong>Instalar los requisitos previos de hardware y software</strong></span><span class="sxs-lookup"><span data-stu-id="29dbf-115"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="29dbf-116">La Conferencia se ejecuta en servidores frontales en un grupo de servidores front-end y servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="29dbf-116">Conferencing runs on Front End Servers in a Front End pool and Standard Edition servers.</span></span> <span data-ttu-id="29dbf-117">No hay ningún requisito adicional de hardware o de software aparte de los necesarios para instalar dichos servidores.</span><span class="sxs-lookup"><span data-stu-id="29dbf-117">It has no additional hardware or software requirements beyond what is required to install those servers.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="29dbf-118">Lync Server 2013 usa Office Web Apps y Office Web Apps Server para controlar el uso compartido y el procesamiento de presentaciones de PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="29dbf-118">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="29dbf-119">Para obtener información sobre cómo instalar y configurar el servidor de Office Web Apps, vea <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">configurar la integración con Office Web Apps Server y Lync server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="29dbf-119">For information about installing and configuring the Office Web Apps Server, see <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configuring integration with Office Web Apps Server and Lync Server 2013</A>.</span></span>


</div></td>
<td><p><span data-ttu-id="29dbf-120">Usuario de dominio miembro del grupo Administradores locales</span><span class="sxs-lookup"><span data-stu-id="29dbf-120">Domain user who is a member of the local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="29dbf-121"><a href="lync-server-2013-supported-hardware.md">Hardware compatible con Lync Server 2013</a> en la documentación de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="29dbf-121"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="29dbf-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Compatibilidad con el software de servidor y la infraestructura en Lync Server 2013</a> en la documentación de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="29dbf-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="29dbf-123"><a href="lync-server-2013-determining-your-system-requirements.md">Determinar los requisitos del sistema para Lync Server 2013</a> en la documentación de planificación.</span><span class="sxs-lookup"><span data-stu-id="29dbf-123"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="29dbf-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Requisitos técnicos para archivar en Lync Server 2013</a> en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="29dbf-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technical requirements for Archiving in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29dbf-125"><strong>Crear la topología interna adecuada para admitir la conferencia</strong></span><span class="sxs-lookup"><span data-stu-id="29dbf-125"><strong>Create the appropriate internal topology to support conferencing</strong></span></span></p></td>
<td><p><span data-ttu-id="29dbf-126">Ejecute el generador de topología para agregar conferencias a la topología y, a continuación, publique la topología.</span><span class="sxs-lookup"><span data-stu-id="29dbf-126">Run Topology Builder to add conferencing to the topology, and then publish the topology.</span></span></p></td>
<td><p><span data-ttu-id="29dbf-127">Para definir una topología, una cuenta que sea miembro del grupo Usuarios locales</span><span class="sxs-lookup"><span data-stu-id="29dbf-127">To define a topology, an account that is a member of the local Users group</span></span></p>
<p><span data-ttu-id="29dbf-128">Para publicar la topología, una cuenta que sea miembro del grupo administradores del dominio y del grupo RTCUniversalServerAdmins, y que tenga permisos de control total (lectura/escritura/modificación) en el recurso compartido de archivos para el almacén de archivos de Lync Server 2013 (para que topología pueda configurar las DACL obligatorias)</span><span class="sxs-lookup"><span data-stu-id="29dbf-128">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and that has full control permissions (read/write/modify) on the file share to be used for the Lync Server 2013 file store (so that Topology Builder can configure the required DACLs)</span></span></p></td>
<td><p><span data-ttu-id="29dbf-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Defina y configure una topología en el generador de topologías para Lync Server 2013</a> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="29dbf-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Define and configure a topology in Topology Builder for Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29dbf-130"><strong>Configurar directivas de conferencia y soporte técnico</strong></span><span class="sxs-lookup"><span data-stu-id="29dbf-130"><strong>Configure conferencing policies and support</strong></span></span></p></td>
<td><p><span data-ttu-id="29dbf-131">Use el panel de control de Lync Server 2013 o el shell de administración de Lync Server para configurar las opciones de conferencia.</span><span class="sxs-lookup"><span data-stu-id="29dbf-131">Use the Lync Server 2013 Control Panel or Lync Server Management Shell to configure conferencing settings.</span></span></p></td>
<td><p><span data-ttu-id="29dbf-132">Grupo RTCUniversalServerAdmins (solo Windows PowerShell) o asignar usuarios al rol [] o CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="29dbf-132">RTCUniversalServerAdmins group ( Windows PowerShell only) or assign users to the [] or CSAdministrator role</span></span></p></td>
<td><p><span data-ttu-id="29dbf-133"><a href="lync-server-2013-conferencing-policies.md">Directivas de conferencia en Lync Server 2013</a> en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="29dbf-133"><a href="lync-server-2013-conferencing-policies.md">Conferencing policies in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="29dbf-134">Lync Server 2013 ahora incluye la configuración **MaxUploadFileSizeMb** , que limita el tamaño de los archivos que se pueden cargar durante una reunión.</span><span class="sxs-lookup"><span data-stu-id="29dbf-134">Lync Server 2013 now includes the **MaxUploadFileSizeMb** setting, which limits the size of files that can be uploaded during a meeting.</span></span> <span data-ttu-id="29dbf-135">El valor predeterminado de esta configuración es 500 MB.</span><span class="sxs-lookup"><span data-stu-id="29dbf-135">The default value for this setting is 500 MB.</span></span> <span data-ttu-id="29dbf-136">Puede ajustar **MaxUploadFileSizeMb** con el cmdlet **set-CsConferencingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="29dbf-136">You can adjust **MaxUploadFileSizeMb** using the **Set-CsConferencingConfiguration** cmdlet.</span></span>

<span data-ttu-id="29dbf-137">**MaxUploadFileSizeMb** no limita la configuración de carga de archivos de Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="29dbf-137">**MaxUploadFileSizeMb** does not limit the file upload setting for Lync Web App.</span></span> <span data-ttu-id="29dbf-138">El límite de carga de tamaño de archivo para Lync Web App se establece en aproximadamente 30 MB y está controlado por el archivo web.config de IIS:/DataCollabWeb/Int \[ ext \] /handler/web.config. Para configurar el límite de carga del tamaño de archivo de Lync Web App, actualice `maxRequestLength` y `maxAllowedContentLength` en el web.config archivo, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="29dbf-138">The file size upload limit for Lync Web App is set to approximately 30MB and is controlled by the IIS web.config file: /DataCollabWeb/Int\[Ext\]/Handler/web.config. To configure the file size upload limit for Lync Web App, update `maxRequestLength` and `maxAllowedContentLength` in the web.config file as shown below.</span></span>

    <system.web>
        <!-- 
            Since this handler is used to upload files to DMCU the request size (in kilobytes) 
            has to fit max allowed file size uploaded by LWA client.
            The timeout has to reflect the min client bandwidth. Timeout of 600 secs 
            and 512 Kbits of *client* bandwidth would result into aproximately 30 Mbytes 
            for LWA upload size limit.
        -->
          <httpRuntime maxRequestLength="500000" executionTimeout="600" />
    
    
    
                    <security>
                    <requestFiltering>
                               <requestLimits maxAllowedContentLength="524288000" />
                    </requestFiltering>
                    </security>

<span data-ttu-id="29dbf-139">Debe actualizar el archivo de web.config para cada servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="29dbf-139">You must update the web.config file for each Front End Server.</span></span>

<span data-ttu-id="29dbf-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="29dbf-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

