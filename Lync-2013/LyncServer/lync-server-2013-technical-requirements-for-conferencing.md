---
title: 'Lync Server 2013: Requisitos técnicos para conferencias'
description: Requisitos técnicos de Lync Server 2013 para conferencias.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for conferencing
ms:assetid: 3c0d89e1-53e6-46d7-bf8c-491260b292ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425889(v=OCS.15)
ms:contentKeyID: 48183923
ms.date: 06/26/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b3b787d84288d789cd0d824081439004f19327e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399227"
---
# <a name="technical-requirements-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="fe38b-103">Requisitos técnicos para conferencias en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fe38b-103">Technical requirements for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fe38b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fe38b-104">

<span> </span></span></span>

<span data-ttu-id="fe38b-105">_**Última modificación del tema:** 2014-06-25_</span><span class="sxs-lookup"><span data-stu-id="fe38b-105">_**Topic Last Modified:** 2014-06-25_</span></span>

<span data-ttu-id="fe38b-106">Para Lync Server 2013, las conferencias de acceso telefónico local, las conferencias A/V, las conferencias de mensajería instantánea (mi) y las capacidades de conferencia web siempre se ejecutan en servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="fe38b-106">For Lync Server 2013, dial-in conferencing, A/V conferencing, instant messaging (IM) conferencing and web conferencing capabilities always run on Front End Servers.</span></span>

<span data-ttu-id="fe38b-107">En esta sección se detallan los requisitos de hardware y software de estos servidores, junto con el collocation compatible.</span><span class="sxs-lookup"><span data-stu-id="fe38b-107">This section details the hardware and software requirements for these servers, along with the supported collocation.</span></span>

<span data-ttu-id="fe38b-108">Las conferencias de acceso telefónico local son una característica que incluye una variedad de componentes.</span><span class="sxs-lookup"><span data-stu-id="fe38b-108">Dial-in conferencing is a feature that includes a variety of components.</span></span> <span data-ttu-id="fe38b-109">Algunos de los componentes son específicos de las conferencias de acceso telefónico local y otros son componentes de telefonía empresarial.</span><span class="sxs-lookup"><span data-stu-id="fe38b-109">Some of the components are specific to dial-in conferencing and some are Enterprise Voice components.</span></span> <span data-ttu-id="fe38b-110">En esta sección se describen los requisitos para los componentes específicos de las conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="fe38b-110">This section describes the requirements for the components that are specific to dial-in conferencing.</span></span> <span data-ttu-id="fe38b-111">Para obtener más información sobre los requisitos de la puerta de enlace de red telefónica conmutada (RTC) y el servidor de mediación, consulte [componente servidor de mediación en Lync server 2013](lync-server-2013-mediation-server-component.md) , así como [componentes y topologías de servidor de mediación en Lync Server 2013](lync-server-2013-components-and-topologies-for-mediation-server.md) en la documentación de planificación.</span><span class="sxs-lookup"><span data-stu-id="fe38b-111">For details about Mediation Server and public switched telephone network (PSTN) gateway requirements, see [Mediation Server component in Lync Server 2013](lync-server-2013-mediation-server-component.md) and [Components and topologies for Mediation Server in Lync Server 2013](lync-server-2013-components-and-topologies-for-mediation-server.md) in the Planning documentation.</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="fe38b-112">Requisitos de hardware</span><span class="sxs-lookup"><span data-stu-id="fe38b-112">Hardware Requirements</span></span>

<span data-ttu-id="fe38b-113">Debido a que las conferencias web y A/V se colocan con el servidor front-end, los requisitos de hardware del servidor son los mismos que los servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="fe38b-113">Because web conferencing and A/V conferencing are collocated with the Front End Server, the server hardware requirements are the same as for the Front End Servers.</span></span> <span data-ttu-id="fe38b-114">Para obtener más información sobre los requisitos de hardware, vea [plataformas de hardware de servidor para Lync Server 2013](lync-server-2013-server-hardware-platforms.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="fe38b-114">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span> <span data-ttu-id="fe38b-115">Los siguientes componentes necesarios para las conferencias de acceso telefónico local también tienen los mismos requisitos de hardware que los servidores front-end:</span><span class="sxs-lookup"><span data-stu-id="fe38b-115">The following components required for dial-in conferencing also have the same hardware requirements as Front End Servers:</span></span>

  - <span data-ttu-id="fe38b-116">Servicio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fe38b-116">Application service</span></span>

  - <span data-ttu-id="fe38b-117">Aplicación Operador de conferencia</span><span class="sxs-lookup"><span data-stu-id="fe38b-117">Conferencing Attendant application</span></span>

  - <span data-ttu-id="fe38b-118">Aplicación de anuncio de conferencia</span><span class="sxs-lookup"><span data-stu-id="fe38b-118">Conferencing Announcement application</span></span>

<span data-ttu-id="fe38b-119">Los requisitos de hardware para el servidor front-end son los mismos que para otros muchos roles de servidor de Lync Server 2013 se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fe38b-119">The hardware requirements for Front End Server are the same as for many other server roles in Lync Server 2013 are outlined in the following table.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="fe38b-120">Requisitos de software</span><span class="sxs-lookup"><span data-stu-id="fe38b-120">Software Requirements</span></span>

<span data-ttu-id="fe38b-121">Debido a que las conferencias web y A/V se colocan con el servidor front-end, los requisitos de software del servidor son los mismos que los servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="fe38b-121">Because web conferencing and A/V conferencing are collocated with the Front End Server, the server software requirements are the same as for the Front End Servers.</span></span> <span data-ttu-id="fe38b-122">Para obtener más información sobre los requisitos de software, vea [compatibilidad del sistema operativo servidor y herramientas en Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="fe38b-122">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="fe38b-123">Para las conferencias web, Lync Server 2013 también requiere Office Web Apps y Office Web Apps Server (anteriormente conocido como servidor WAC) para controlar presentaciones de PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="fe38b-123">For web conferencing, Lync Server 2013 also requires Office Web Apps and the Office Web Apps Server (formerly known as WAC Server) to handle PowerPoint presentations.</span></span> <span data-ttu-id="fe38b-124">Para obtener más información, vea [configurar la integración con Office Web Apps Server y Lync server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="fe38b-124">For details, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="fe38b-125">Para las conferencias de acceso telefónico local, servicio de aplicaciones, operador de conferencias y aplicación de anuncio de Conferencia tienen los mismos requisitos del sistema operativo que los servidores de aplicaciones para el usuario.</span><span class="sxs-lookup"><span data-stu-id="fe38b-125">For dial-in conferencing, Application service, Conferencing Attendant application, and Conferencing Announcement application have the same operating system requirements as Front End Servers.</span></span> <span data-ttu-id="fe38b-126">Para obtener más información sobre los requisitos de software, vea [compatibilidad del sistema operativo servidor y herramientas en Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="fe38b-126">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="fe38b-127">El Asistente de conferencia y la aplicación de anuncio de conferencia requieren que Windows Media Format Runtime esté instalado en los servidores frontales.</span><span class="sxs-lookup"><span data-stu-id="fe38b-127">Conferencing Attendant application and Conferencing Announcement application require that Windows Media Format Runtime is installed on Front End Servers.</span></span> <span data-ttu-id="fe38b-128">El tiempo de ejecución de Windows Media Format es necesario para reproducir archivos de audio de Windows Media (WMA) que se usan para música en espera, nombres grabados y avisos.</span><span class="sxs-lookup"><span data-stu-id="fe38b-128">The Windows Media Format Runtime is required to play Windows Media audio (WMA) files that are used for music on hold, recorded names, and prompts.</span></span> <span data-ttu-id="fe38b-129">Excepto en el caso de Windows Server 2012 y Windows Server 2012 R2, el tiempo de ejecución de Windows Media Format se instala automáticamente como parte de la experiencia de escritorio de Windows al ejecutar el programa de instalación, pero es posible que tenga que reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="fe38b-129">Except for Windows Server 2012 and Windows Server 2012 R2, the Windows Media Format Runtime is installed automatically as part of the Windows Desktop Experience when you run Setup, but you might need to restart the computer.</span></span> <span data-ttu-id="fe38b-130">Por lo tanto, le recomendamos que instale como parte de la experiencia de escritorio de Windows, que incluye el Windows Media Format Runtime antes de ejecutar el programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="fe38b-130">Therefore, we recommend that you install as part of the Windows Desktop Experience, which includes Windows Media Format Runtime before you run Setup.</span></span> <span data-ttu-id="fe38b-131">Windows Server 2012 y Windows Server 2012 R2 requieren Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="fe38b-131">Windows Server 2012 and Windows Server 2012 R2 requires Microsoft Media Foundation.</span></span>

</div>

<div>

## <a name="port-requirements-for-dial-in-conferencing"></a><span data-ttu-id="fe38b-132">Requisitos de puerto para las conferencias de acceso telefónico local</span><span class="sxs-lookup"><span data-stu-id="fe38b-132">Port Requirements for dial-in conferencing</span></span>

<span data-ttu-id="fe38b-133">En la siguiente tabla se describen los puertos que usan las conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="fe38b-133">The following table describes the ports that are used by dial-in conferencing.</span></span> <span data-ttu-id="fe38b-134">Si usa un equilibrador de carga, asegúrese de que el equilibrador de carga está configurado para los puertos usados por todas las aplicaciones que se ejecutarán en el grupo.</span><span class="sxs-lookup"><span data-stu-id="fe38b-134">If you use a load balancer, ensure that the load balancer is configured for the ports used by any applications that will run in the pool.</span></span>

<span data-ttu-id="fe38b-135">Estos puertos son configuraciones predeterminadas que se pueden cambiar con el cmdlet **Set-CsApplicationServer**.</span><span class="sxs-lookup"><span data-stu-id="fe38b-135">These ports are default settings that you can change by using the **Set-CsApplicationServer** cmdlet.</span></span> <span data-ttu-id="fe38b-136">Para obtener más información sobre este cmdlet, consulte la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe38b-136">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fe38b-137">Todas las instancias de la misma aplicación de un grupo usan el mismo puerto de escucha de SIP.</span><span class="sxs-lookup"><span data-stu-id="fe38b-137">All instances of the same application in a pool use the same SIP listening port.</span></span>



</div>

### <a name="ports-used-by-dial-in-conferencing"></a><span data-ttu-id="fe38b-138">Puertos usados por las conferencias de acceso telefónico local</span><span class="sxs-lookup"><span data-stu-id="fe38b-138">Ports used by dial-in conferencing</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe38b-139">Número de puerto</span><span class="sxs-lookup"><span data-stu-id="fe38b-139">Port number</span></span></th>
<th><span data-ttu-id="fe38b-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe38b-140">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe38b-141">5072</span><span class="sxs-lookup"><span data-stu-id="fe38b-141">5072</span></span></p></td>
<td><p><span data-ttu-id="fe38b-142">Usado por la aplicación de operador de conferencia para solicitudes de escucha de SIP</span><span class="sxs-lookup"><span data-stu-id="fe38b-142">Used by Conferencing Attendant application for SIP listening requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe38b-143">5073</span><span class="sxs-lookup"><span data-stu-id="fe38b-143">5073</span></span></p></td>
<td><p><span data-ttu-id="fe38b-144">Usado por la aplicación de anuncios de conferencias para solicitudes de escucha de SIP</span><span class="sxs-lookup"><span data-stu-id="fe38b-144">Used by Conferencing Announcement application for SIP listening requests</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients-for-dial-in-conferencing"></a><span data-ttu-id="fe38b-145">Clientes compatibles con conferencias de acceso telefónico local</span><span class="sxs-lookup"><span data-stu-id="fe38b-145">Supported Clients for Dial-In Conferencing</span></span>

<span data-ttu-id="fe38b-146">Puede usar el siguiente cliente para programar conferencias locales que admitan el acceso telefónico:</span><span class="sxs-lookup"><span data-stu-id="fe38b-146">You can use the following client to schedule on-premises conferences that support dial-in access:</span></span>

  - <span data-ttu-id="fe38b-147">Complemento de reunión en línea para Lync 2013 (se instala automáticamente al instalar Lync 2013 o asistente)</span><span class="sxs-lookup"><span data-stu-id="fe38b-147">Online Meeting Add-in for Lync 2013 (installed automatically when you install Lync 2013 or Attendee)</span></span>

</div>

<div>

## <a name="dial-in-conferencing-settings-page-requirements"></a><span data-ttu-id="fe38b-148">Requisitos de la página de configuración de la Conferencia de acceso telefónico local</span><span class="sxs-lookup"><span data-stu-id="fe38b-148">Dial-in Conferencing Settings page Requirements</span></span>

<span data-ttu-id="fe38b-149">La página de configuración de la Conferencia de acceso telefónico local admite las combinaciones de sistemas operativos y exploradores Web que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fe38b-149">The Dial-in Conferencing Settings page supports the combinations of operating systems and web browsers described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fe38b-150">se admiten las versiones de 32 y 64 bits de los sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="fe38b-150">32-bit and 64-bit versions of the operating systems are supported.</span></span>



</div>

### <a name="supported-operating-systems-and-web-browsers"></a><span data-ttu-id="fe38b-151">Sistemas operativos y exploradores web compatibles</span><span class="sxs-lookup"><span data-stu-id="fe38b-151">Supported Operating Systems and Web Browsers</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe38b-152">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="fe38b-152">Operating system</span></span></th>
<th><span data-ttu-id="fe38b-153">Explorador web</span><span class="sxs-lookup"><span data-stu-id="fe38b-153">Web browser</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe38b-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fe38b-154">Windows 7</span></span></p></td>
<td><p><span data-ttu-id="fe38b-155">Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="fe38b-155">Internet Explorer 9</span></span></p>
<p><span data-ttu-id="fe38b-156">Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="fe38b-156">Internet Explorer 8</span></span></p>
<p><span data-ttu-id="fe38b-157">Firefox</span><span class="sxs-lookup"><span data-stu-id="fe38b-157">Firefox</span></span></p></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe38b-158">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fe38b-158">Windows Server 2008 R2</span></span></p></td>
<td><p><span data-ttu-id="fe38b-159">Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="fe38b-159">Internet Explorer 9</span></span></p>
<p><span data-ttu-id="fe38b-160">Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="fe38b-160">Internet Explorer 8</span></span></p>
<p><span data-ttu-id="fe38b-161">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="fe38b-161">Internet Explorer 7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe38b-162">Mac OS</span><span class="sxs-lookup"><span data-stu-id="fe38b-162">Mac OS</span></span></p></td>
<td><p><span data-ttu-id="fe38b-163">Firefox</span><span class="sxs-lookup"><span data-stu-id="fe38b-163">Firefox</span></span></p>
<p><span data-ttu-id="fe38b-164">Safari</span><span class="sxs-lookup"><span data-stu-id="fe38b-164">Safari</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="audio-file-requirements-for-dial-in-conferencing"></a><span data-ttu-id="fe38b-165">Requisitos de los archivos de audio para las conferencias de acceso telefónico local</span><span class="sxs-lookup"><span data-stu-id="fe38b-165">Audio File Requirements for dial-in conferencing</span></span>

<span data-ttu-id="fe38b-166">Lync Server 2013 no admite la personalización de mensajes de voz y de música para conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="fe38b-166">Lync Server 2013 does not support customization of voice prompts and music for dial-in conferencing.</span></span> <span data-ttu-id="fe38b-167">Sin embargo, si tiene una gran necesidad comercial que le exija cambiar los archivos de audio predeterminados, consulte el artículo 961177 de Microsoft Knowledge base, [Cómo personalizar las solicitudes de voz o los archivos de música para conferencias de audio de acceso telefónico local en Microsoft Office Communications Server 2007 R2](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=961177).</span><span class="sxs-lookup"><span data-stu-id="fe38b-167">However, if you have a strong business need that requires you to change the default audio files, see Microsoft Knowledge Base article 961177, [How to customize voice prompts or music files for dial-in audio conferencing in Microsoft Office Communications Server 2007 R2](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=961177).</span></span>

<span data-ttu-id="fe38b-168">También puede usar la herramienta de administración de [solicitudes de voz personalizadas del operador de conferencias de Microsoft Lync Server](https://go.microsoft.com/fwlink/p/?linkid=396880) , que permite a los administradores reemplazar los avisos de voz predeterminados que se usan cuando una llamada de teléfono se une a una reunión de Lync con peticiones personalizadas para proporcionar otra experiencia de entrada de reunión.</span><span class="sxs-lookup"><span data-stu-id="fe38b-168">You can also use the [Microsoft Lync Server Conferencing Attendant Custom Voice Prompts](https://go.microsoft.com/fwlink/p/?linkid=396880) management utility, which enables administrators to replace the default voice prompts used when a phone caller joins a Lync meeting with custom prompts to provide a different meeting entry experience.</span></span> <span data-ttu-id="fe38b-169">Las solicitudes de voz personalizadas se pueden instalar en un servidor que ejecute Lync Server 2010 o Lync Server 2013, Enterprise o Standard.</span><span class="sxs-lookup"><span data-stu-id="fe38b-169">The custom voice prompts can be installed on a server that is running Lync Server 2010 or Lync Server 2013, either Enterprise or Standard Edition.</span></span>

<span data-ttu-id="fe38b-170">El operador de conferencia y la aplicación de anuncio de Conferencia tienen los siguientes requisitos de música en espera, nombre grabado y archivos de solicitud de audio:</span><span class="sxs-lookup"><span data-stu-id="fe38b-170">Conferencing Attendant application and Conferencing Announcement application have the following requirements for music on hold, recorded name, and audio prompt files:</span></span>

  - <span data-ttu-id="fe38b-171">Formato de archivo de audio de Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="fe38b-171">Windows Media Audio (WMA) file format</span></span>

  - <span data-ttu-id="fe38b-172">Mono de 16 bits</span><span class="sxs-lookup"><span data-stu-id="fe38b-172">16-bit mono</span></span>

  - <span data-ttu-id="fe38b-173">48 kbps CBR 2 pasos (velocidad de bits constante)</span><span class="sxs-lookup"><span data-stu-id="fe38b-173">48 kbps 2-pass CBR (constant bit rate)</span></span>

  - <span data-ttu-id="fe38b-174">Nivel de voz a -24DB</span><span class="sxs-lookup"><span data-stu-id="fe38b-174">Speech level at -24DB</span></span>

</div>

<div>

## <a name="user-requirements-for-dial-in-conferencing"></a><span data-ttu-id="fe38b-175">Requisitos de usuario para las conferencias de acceso telefónico local</span><span class="sxs-lookup"><span data-stu-id="fe38b-175">User Requirements for Dial-In Conferencing</span></span>

<span data-ttu-id="fe38b-176">Los usuarios de conferencias de acceso telefónico local necesitan tener un número de teléfono único o una extensión asignada a su cuenta.</span><span class="sxs-lookup"><span data-stu-id="fe38b-176">Dial-in conferencing users must have a unique phone number or extension assigned to their account.</span></span> <span data-ttu-id="fe38b-177">Este requisito admite la autenticación durante las conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="fe38b-177">This requirement supports authentication during dial-in conferencing.</span></span> <span data-ttu-id="fe38b-178">Los usuarios empresariales (es decir, los usuarios que tienen credenciales de servicios de dominio de Active Directory y cuentas de Lync Server dentro de la organización) escriben su número de teléfono (o extensión) y un número de identificación personal (PIN) para llamar a conferencias como un usuario autenticado.</span><span class="sxs-lookup"><span data-stu-id="fe38b-178">Enterprise users (that is, users who have Active Directory Domain Services credentials and Lync Server accounts within your organization) enter their phone number (or extension) and a personal identification number (PIN) to dial in to conferences as an authenticated user.</span></span>

<span data-ttu-id="fe38b-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fe38b-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

