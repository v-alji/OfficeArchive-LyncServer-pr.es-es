---
title: 'Lync Server 2013: configuración nueva y modificada para Lync 2013'
description: 'Lync Server 2013: configuración nueva y modificada para Lync 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New and changed settings for Lync 2013
ms:assetid: bb13789c-7eda-461c-a387-02ea8ca4dabe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205204(v=OCS.15)
ms:contentKeyID: 48185241
ms.date: 12/08/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1bf744e1bae774904733390ec624be523ad32bc1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445487"
---
# <a name="new-and-changed-settings-for-lync-2013"></a><span data-ttu-id="93961-103">Configuración nueva y modificada para Lync 2013</span><span class="sxs-lookup"><span data-stu-id="93961-103">New and changed settings for Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93961-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93961-104">

<span> </span></span></span>

<span data-ttu-id="93961-105">_**Última modificación del tema:** 2014-12-05_</span><span class="sxs-lookup"><span data-stu-id="93961-105">_**Topic Last Modified:** 2014-12-05_</span></span>

<span data-ttu-id="93961-106">En este tema se tratan los cambios en los cmdlets del shell de administración de Lync Server que se relacionan directamente con la administración de clientes.</span><span class="sxs-lookup"><span data-stu-id="93961-106">This topic discusses changes to Lync Server Management Shell cmdlets that relate directly to client management.</span></span> <span data-ttu-id="93961-107">Lync Server 2013 introduce varios parámetros nuevos y deja obsoletos los parámetros de las características que se pueden configurar por otros medios.</span><span class="sxs-lookup"><span data-stu-id="93961-107">Lync Server 2013 introduces several new parameters, and deprecates parameters for features that can be configured through other means.</span></span>

<div>

## <a name="new-client-management-parameters"></a><span data-ttu-id="93961-108">Nuevos parámetros de administración de clientes</span><span class="sxs-lookup"><span data-stu-id="93961-108">New Client Management Parameters</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93961-109">Nuevo</span><span class="sxs-lookup"><span data-stu-id="93961-109">New</span></span></th>
<th><span data-ttu-id="93961-110">Cmdlet del shell de administración de Lync Server</span><span class="sxs-lookup"><span data-stu-id="93961-110">Lync Server Management Shell Cmdlet</span></span></th>
<th><span data-ttu-id="93961-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="93961-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93961-112">TracingLevel</span><span class="sxs-lookup"><span data-stu-id="93961-112">TracingLevel</span></span></p></td>
<td><p><span data-ttu-id="93961-113">ClientPolicy</span><span class="sxs-lookup"><span data-stu-id="93961-113">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="93961-114">Cuando se establece en true, el seguimiento de software se habilita en Lync; Cuando se establece en false, el seguimiento de software se deshabilitará.</span><span class="sxs-lookup"><span data-stu-id="93961-114">When set to True, software tracing will be enabled in Lync; when set to False, software tracing will be disabled.</span></span> <span data-ttu-id="93961-115">El seguimiento de software implica mantener un registro detallado de todo lo que hace un programa (incluido el seguimiento de llamadas API).</span><span class="sxs-lookup"><span data-stu-id="93961-115">Software tracing involves keeping a detailed record of everything that a program does (including tracking API calls).</span></span> <span data-ttu-id="93961-116">El seguimiento es principalmente útil para los programadores y el personal de soporte técnico de aplicaciones. Esta configuración es equivalente a la configuración de directiva de grupo de Communications Server 2007 R2 para &quot; activar el seguimiento de Communicator. &quot; La configuración es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="93961-116">Tracing is mostly useful to developers and to application support personnel.This setting is equivalent to the Communications Server 2007 R2 Group Policy setting &quot;Turn on tracing for Communicator.&quot; The settings are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="93961-117">OFF = el seguimiento está deshabilitado y el usuario no puede cambiar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="93961-117">Off = Tracing is disabled and the user cannot change this setting.</span></span></p></li>
<li><p><span data-ttu-id="93961-118">Light = se realiza un seguimiento mínimo y el usuario no puede cambiar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="93961-118">Light = Minimal tracing is performed, and the user cannot change this setting.</span></span></p></li>
<li><p><span data-ttu-id="93961-119">On = se realiza el seguimiento detallado y el usuario no puede cambiar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="93961-119">On = Verbose tracing is performed, and the user cannot change this setting.</span></span></p></li>
</ul>
<p><span data-ttu-id="93961-120">De forma predeterminada TracingLevel se establece en un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="93961-120">By default TracingLevel is set to a null value.</span></span> <span data-ttu-id="93961-121">Eso significa que se realiza un seguimiento mínimo, pero el usuario puede habilitar o deshabilitar este seguimiento mínimo.</span><span class="sxs-lookup"><span data-stu-id="93961-121">That means that minimal tracing is performed, but the user can enable or disable this minimal tracing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93961-122">EnableMediaRedirection</span><span class="sxs-lookup"><span data-stu-id="93961-122">EnableMediaRedirection</span></span></p></td>
<td><p><span data-ttu-id="93961-123">ClientPolicy</span><span class="sxs-lookup"><span data-stu-id="93961-123">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="93961-124">Cuando se establece en true ($True) permite que las secuencias de audio y vídeo se separen de otro tráfico de red, a su vez, esto permite que los dispositivos cliente realicen la codificación y la descodificación de audio y vídeo de forma local.</span><span class="sxs-lookup"><span data-stu-id="93961-124">When set to True ($True) allows audio and video streams to be separated from other network traffic, In turn, this allows client devices to do encoding and decoding of audio and video locally.</span></span> <span data-ttu-id="93961-125">Normalmente, el redireccionamiento de medios tiene un uso de ancho de banda menor, una mayor escalabilidad del servidor y una experiencia de usuario más óptima en comparación con técnicas similares, como el acceso remoto del dispositivo o la compresión de códec.</span><span class="sxs-lookup"><span data-stu-id="93961-125">Media redirection typically results in lower bandwidth usage, higher server scalability, and a more-optimal user experience compared to similar techniques such as device remoting or codec compression.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93961-126">AllowLargeMeetings</span><span class="sxs-lookup"><span data-stu-id="93961-126">AllowLargeMeetings</span></span></p></td>
<td><p><span data-ttu-id="93961-127">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="93961-127">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="93961-128">Cuando se establece en true, todas las reuniones de Lync se tratan como &quot; reuniones grandes. &quot; En una reunión grande, se colocan restricciones en el número de notificaciones que se envían a los participantes, además del tamaño de la lista de la reunión que se transmite de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="93961-128">When set to True, all Lync Meetings are treated as &quot;large meetings.&quot; With a large meeting, restrictions are placed on the number of notifications that are sent to participants, in addition to the size of the meeting roster that is transmitted by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93961-129">DisablePowerPointAnnotations</span><span class="sxs-lookup"><span data-stu-id="93961-129">DisablePowerPointAnnotations</span></span></p></td>
<td><p><span data-ttu-id="93961-130">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="93961-130">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="93961-131">Cuando se establece en true ($True), los usuarios no podrán agregar anotaciones a las diapositivas de PowerPoint usadas en una conferencia.</span><span class="sxs-lookup"><span data-stu-id="93961-131">When set to True ($True) users won’t be able to add annotations to PowerPoint slides used in a conference.</span></span> <span data-ttu-id="93961-132">Sin embargo (según el valor de la propiedad AllowAnnotations), los usuarios seguirán teniendo acceso a otras características de pizarra.</span><span class="sxs-lookup"><span data-stu-id="93961-132">However (depending on the value of the AllowAnnotations property), users will still have access to other whiteboarding features.</span></span> <span data-ttu-id="93961-133">El valor predeterminado es false, lo que significa que se permiten las anotaciones de PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="93961-133">The default value is False, meaning that PowerPoint annotations are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93961-134">AllowSharedNotes</span><span class="sxs-lookup"><span data-stu-id="93961-134">AllowSharedNotes</span></span></p></td>
<td><p><span data-ttu-id="93961-135">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="93961-135">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="93961-136">Cuando se establece en true (valor predeterminado), cualquier Bloc de notas de OneNote abierto vinculado a la Conferencia se actualizará automáticamente con información como los participantes de la Conferencia, así como detalles sobre el contenido compartido durante la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="93961-136">When set to True (the default value) any open OneNote notebooks linked to the conference will automatically be updated with information such as conference participants and details about content shared during the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93961-137">EnableInviteCustomization</span><span class="sxs-lookup"><span data-stu-id="93961-137">EnableInviteCustomization</span></span></p></td>
<td><p><span data-ttu-id="93961-138">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="93961-138">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="93961-139">Se usa junto con los otros parámetros de CsMeetingConfiguration para personalizar las invitaciones a reuniones generadas por el complemento de reunión en línea para Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="93961-139">Used along with the other new CsMeetingConfiguration parameters to customize the meeting invitations generated by the Online Meeting Add-in for Lync 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93961-140">LogoURL</span><span class="sxs-lookup"><span data-stu-id="93961-140">LogoURL</span></span></p></td>
<td><p><span data-ttu-id="93961-141">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="93961-141">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="93961-142">Agrega el logotipo de su organización a todas las invitaciones generadas por el complemento de reuniones en línea para Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="93961-142">Adds your organization’s logo to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="93961-143">Especifique la dirección URL de una imagen GIF o JPG.</span><span class="sxs-lookup"><span data-stu-id="93961-143">You specify the URL of a GIF or JPG image.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93961-144">HelpURL</span><span class="sxs-lookup"><span data-stu-id="93961-144">HelpURL</span></span></p></td>
<td><p><span data-ttu-id="93961-145">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="93961-145">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="93961-146">Agrega la dirección URL de ayuda o soporte técnico de la organización a todas las invitaciones generadas por el complemento de reuniones en línea para Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="93961-146">Adds your organization’s help or support URL to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93961-147">LegalURL</span><span class="sxs-lookup"><span data-stu-id="93961-147">LegalURL</span></span></p></td>
<td><p><span data-ttu-id="93961-148">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="93961-148">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="93961-149">Agrega texto legal o texto de renuncia a todas las invitaciones generadas por el complemento de reuniones en línea para Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="93961-149">Adds legal text or disclaimer text to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="93961-150">Especifique la dirección URL de la ubicación del texto.</span><span class="sxs-lookup"><span data-stu-id="93961-150">You specify the URL for the location of the text.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93961-151">CustomFooterText</span><span class="sxs-lookup"><span data-stu-id="93961-151">CustomFooterText</span></span></p></td>
<td><p><span data-ttu-id="93961-152">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="93961-152">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="93961-153">Agrega un pie de página personalizado a todas las invitaciones generadas por el complemento de reuniones en línea para Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="93961-153">Adds a custom footer to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="93961-154">Especifique la dirección URL de la ubicación del texto del pie de página personalizado.</span><span class="sxs-lookup"><span data-stu-id="93961-154">You specify the URL for the location of the custom footer text.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="deprecated-client-management-parameters"></a><span data-ttu-id="93961-155">Parámetros de administración de clientes desusados</span><span class="sxs-lookup"><span data-stu-id="93961-155">Deprecated Client Management Parameters</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93961-156">Parámetro</span><span class="sxs-lookup"><span data-stu-id="93961-156">Parameter</span></span></th>
<th><span data-ttu-id="93961-157">Cmdlet del shell de administración de Lync Server</span><span class="sxs-lookup"><span data-stu-id="93961-157">Lync Server Management Shell Cmdlet</span></span></th>
<th><span data-ttu-id="93961-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="93961-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93961-159">CustomizedHelpUrl</span><span class="sxs-lookup"><span data-stu-id="93961-159">CustomizedHelpUrl</span></span></p></td>
<td><p><span data-ttu-id="93961-160">ClientPolicy</span><span class="sxs-lookup"><span data-stu-id="93961-160">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="93961-161">Este parámetro ha quedado obsoleto para usarse con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93961-161">This parameter has been deprecated for use with Lync Server 2013.</span></span> <span data-ttu-id="93961-162">Cuando se usa conjuntamente con EnableEnterpriseCustomizedHelp, este parámetro permitió a una organización especificar una dirección URL para que cuando los usuarios hagan clic en el menú ayuda en Lync, se muestre una ayuda personalizada.</span><span class="sxs-lookup"><span data-stu-id="93961-162">When used in conjunction with EnableEnterpriseCustomizedHelp, this parameter enabled an organization to specify a URL so that when users clicked the Help menu in Lync, customized help would display.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93961-163">EnableEnterpriseCustomizedHelp</span><span class="sxs-lookup"><span data-stu-id="93961-163">EnableEnterpriseCustomizedHelp</span></span></p></td>
<td><p><span data-ttu-id="93961-164">ClientPolicy</span><span class="sxs-lookup"><span data-stu-id="93961-164">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="93961-165">Este parámetro ha quedado obsoleto para usarse con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93961-165">This parameter has been deprecated for use with Lync Server 2013.</span></span> <span data-ttu-id="93961-166">Cuando se usa conjuntamente con CustomizedHelpUrl, este parámetro permitió que las organizaciones mostraran ayuda personalizada.</span><span class="sxs-lookup"><span data-stu-id="93961-166">When used in conjunction with CustomizedHelpUrl, this parameter enabled organizations to display customized help.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93961-167">EnableSQMData</span><span class="sxs-lookup"><span data-stu-id="93961-167">EnableSQMData</span></span></p></td>
<td><p><span data-ttu-id="93961-168">ClientPolicy</span><span class="sxs-lookup"><span data-stu-id="93961-168">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="93961-169">El parámetro EnableSQMData del cmdlet Set-CSClientPolicy se ha eliminado en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93961-169">The EnableSQMData parameter of the Set-CSClientPolicy cmdlet has been removed in Lync Server 2013.</span></span> <span data-ttu-id="93961-170">En su lugar, puede usar la configuración de directiva de grupo compartida para datos de administración de calidad de software (SQM) para determinar la interfaz de usuario para la opción de mejora de la experiencia del cliente en la página Opciones generales del cliente de Lync:</span><span class="sxs-lookup"><span data-stu-id="93961-170">Instead, you can use the shared Group Policy setting for Software Quality Management (SQM) data to determine the user interface for the Customer Experience Improvement option in the Lync client General options page:</span></span></p>
<p><span data-ttu-id="93961-171">HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Common\QMEnable</span><span class="sxs-lookup"><span data-stu-id="93961-171">HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Common\QMEnable</span></span></p>
<p><span data-ttu-id="93961-172">Los</span><span class="sxs-lookup"><span data-stu-id="93961-172">Values:</span></span></p>
<p><span data-ttu-id="93961-173">1 = Mostrar y seleccionar la casilla (el usuario puede desactivar la casilla de verificación)</span><span class="sxs-lookup"><span data-stu-id="93961-173">1 = Display and select the check box (the user can clear the check box)</span></span></p>
<p><span data-ttu-id="93961-174">0 = desactivar y deshabilitar la casilla (el usuario no puede reemplazar)</span><span class="sxs-lookup"><span data-stu-id="93961-174">0 = Turn off and disable the check box (user can't override)</span></span></p>
<p><span data-ttu-id="93961-175">Null = el valor está determinado por el programa de instalación de Office y se muestra la casilla de verificación para que los usuarios establezcan lo que elijan.</span><span class="sxs-lookup"><span data-stu-id="93961-175">Null = The value is determined by Office setup, and the check box is displayed for users to set as they choose</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93961-176">AllowExchangeContactStore</span><span class="sxs-lookup"><span data-stu-id="93961-176">AllowExchangeContactStore</span></span></p></td>
<td><p><span data-ttu-id="93961-177">ClientPolicy</span><span class="sxs-lookup"><span data-stu-id="93961-177">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="93961-178">Este parámetro se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="93961-178">This parameter has been removed.</span></span> <span data-ttu-id="93961-179">En su lugar, al implementar Lync Server 2013 y publicar la topología, el almacén de contactos unificado está habilitado para todos los usuarios de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="93961-179">Instead, when you deploy Lync Server 2013 and publish the topology, unified contact store is enabled for all users by default.</span></span> <span data-ttu-id="93961-180">Esto significa que todos los contactos de un usuario se guardan en Exchange y que están disponibles en Lync, Outlook y Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="93961-180">This means that all a user’s contacts are kept in Exchange and are available in Lync, Outlook, and Outlook Web Access.</span></span> <span data-ttu-id="93961-181">Puede usar el cmdlet Set-CsUserServicesPolicy para personalizar los usuarios que tienen disponible el almacén de contactos unificado.</span><span class="sxs-lookup"><span data-stu-id="93961-181">You can use the Set-CsUserServicesPolicy cmdlet to customize which users have unified contact store available.</span></span> <span data-ttu-id="93961-182">Puede habilitar usuarios de forma global, por sitio, por inquilino o por individuos o grupos de personas.</span><span class="sxs-lookup"><span data-stu-id="93961-182">You can enable users globally, by site, by tenant, or by individuals or groups of individuals.</span></span> <span data-ttu-id="93961-183">Para obtener más información, vea <a href="lync-server-2013-enable-users-for-unified-contact-store.md">Habilitar usuarios para el almacenamiento de contactos unificado en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="93961-183">For details, see <a href="lync-server-2013-enable-users-for-unified-contact-store.md">Enable users for unified contact store in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93961-184">MAPIPollInterval</span><span class="sxs-lookup"><span data-stu-id="93961-184">MAPIPollInterval</span></span></p></td>
<td><p><span data-ttu-id="93961-185">ClientPolicy</span><span class="sxs-lookup"><span data-stu-id="93961-185">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="93961-186">Este parámetro no se usa en Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="93961-186">This parameter is not used by Lync 2013.</span></span> <span data-ttu-id="93961-187">En versiones anteriores, este parámetro especificaba la frecuencia con la que el cliente recuperó datos MAPI de las carpetas públicas de Exchange.</span><span class="sxs-lookup"><span data-stu-id="93961-187">In previous releases, this parameter specified how often the client retrieved MAPI data from Exchange public folders</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93961-188">DisableICE</span><span class="sxs-lookup"><span data-stu-id="93961-188">DisableICE</span></span></p></td>
<td><p><span data-ttu-id="93961-189">ClientPolicy</span><span class="sxs-lookup"><span data-stu-id="93961-189">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="93961-190">Este parámetro quedó obsoleto en Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="93961-190">This parameter was deprecated in Lync 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="93961-191">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93961-191">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

