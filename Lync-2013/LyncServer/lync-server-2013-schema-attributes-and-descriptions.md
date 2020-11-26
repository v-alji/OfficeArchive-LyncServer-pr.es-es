---
title: 'Lync Server 2013: descripciones y atributos de esquema'
description: 'Lync Server 2013: descripciones y atributos de esquema.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema attributes and descriptions
ms:assetid: b009df76-9c22-471d-b57a-bda009a98261
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412841(v=OCS.15)
ms:contentKeyID: 48185083
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18888d20a772b3e84970e7d874bd6b6964affc75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444962"
---
# <a name="schema-attributes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="b7451-103">Atributos y descripciones de esquema en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7451-103">Schema attributes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7451-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7451-104">

<span> </span></span></span>

<span data-ttu-id="b7451-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="b7451-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="b7451-106">En esta sección se describen todos los atributos de esquema usados por Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b7451-106">This section describes all the schema attributes used by Lync Server 2013.</span></span> <span data-ttu-id="b7451-107">Para las clases asociadas a los atributos, consulte [atributos de esquema por clase en Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span><span class="sxs-lookup"><span data-stu-id="b7451-107">For the classes associated with attributes, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span> <span data-ttu-id="b7451-108">Para obtener una lista de las clases y atributos que son nuevos en Lync Server 2013, consulte [cambios en el esquema de Lync server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="b7451-108">For a list of classes and attributes that are new in Lync Server 2013, see [Schema changes in Lync Server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span></span>

<span data-ttu-id="b7451-109">Los atributos que están vinculados se especifican como vínculos hacia adelante o vínculos hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="b7451-109">Attributes that are linked pairs are specified as forward links or back links.</span></span> <span data-ttu-id="b7451-110">Un atributo que hace referencia a otro objeto es un vínculo hacia adelante; el atributo del otro objeto que hace referencia al primer objeto es un vínculo hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="b7451-110">An attribute that refers to another object is a forward link; the attribute of the other object that refers back to the first object is a back link.</span></span> <span data-ttu-id="b7451-111">Los vínculos de reenvío son actualizables, mientras que los vínculos posteriores son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b7451-111">Forward links are updatable, while back links are read-only.</span></span>

<span data-ttu-id="b7451-112">Algunos atributos tienen un valor de máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="b7451-112">Some attributes have a bit-mask value.</span></span> <span data-ttu-id="b7451-113">Para estos atributos, cada configuración está representada por un bit y el valor decimal que se muestra representa la posición del bit.</span><span class="sxs-lookup"><span data-stu-id="b7451-113">For these attributes, each setting is represented by a bit, and the displayed decimal value represents the bit position.</span></span> <span data-ttu-id="b7451-114">Las posiciones de bits comienzan con el bit 0.</span><span class="sxs-lookup"><span data-stu-id="b7451-114">Bit positions start with bit 0.</span></span> <span data-ttu-id="b7451-115">Por ejemplo, 1 (binario) es el bit 0 establecido y 10000 (binario) es el bit 4 establecido.</span><span class="sxs-lookup"><span data-stu-id="b7451-115">For example, 1 (binary) is bit 0 set and 10000 (binary) is bit 4 set.</span></span> <span data-ttu-id="b7451-116">Cada bit representa una propiedad.</span><span class="sxs-lookup"><span data-stu-id="b7451-116">Each bit represents a property.</span></span> <span data-ttu-id="b7451-117">A continuación se muestran algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="b7451-117">The following are some examples:</span></span>

  - <span data-ttu-id="b7451-118">10000 (binario) tiene un valor decimal de 16 (es decir, el bit 4 está establecido).</span><span class="sxs-lookup"><span data-stu-id="b7451-118">10000 (binary) has a decimal value of 16 (that is, bit 4 is set).</span></span>

  - <span data-ttu-id="b7451-119">100 millones (binario) tiene un valor decimal de 256 (es decir, el bit 8 está establecido).</span><span class="sxs-lookup"><span data-stu-id="b7451-119">100000000 (binary) has a decimal value of 256 (that is, bit 8 is set).</span></span>

  - <span data-ttu-id="b7451-120">1100 (binario) tiene un valor decimal de 12 (es decir, los bits 2 y 3 están establecidos; las propiedades representadas por los dos bits están habilitadas).</span><span class="sxs-lookup"><span data-stu-id="b7451-120">1100 (binary) has a decimal value of 12 (that is, bits 2 and 3 are set; properties represented by both bits are enabled).</span></span>

  - <span data-ttu-id="b7451-121">1111000001 (binario) tiene un valor decimal de 961 (es decir, están establecidos los bits 0, 6, 7, 8 y 9; las propiedades de cada uno de estos bits están habilitadas).</span><span class="sxs-lookup"><span data-stu-id="b7451-121">1111000001 (binary) has a decimal value of 961 (that is, bits 0, 6, 7, 8, and 9 are set; properties for each of these bits are enabled).</span></span>

<div id="sectionSection0" class="section">

### <a name="schema-attributes-for-lync-server-2013"></a><span data-ttu-id="b7451-122">Atributos de esquema para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7451-122">Schema Attributes for Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7451-123">Atributo</span><span class="sxs-lookup"><span data-stu-id="b7451-123">Attribute</span></span></th>
<th><span data-ttu-id="b7451-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7451-124">Description</span></span></th>
<th><span data-ttu-id="b7451-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7451-125">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7451-126">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b7451-126">dnsHostName</span></span></p></td>
<td><p><span data-ttu-id="b7451-127">Un atributo existente en servicios de dominio de Active Directory que está ahora asociado a las clases <strong>msRTCSIP-Pool</strong> y <strong>msRTCSIP-MonitoringServer</strong> .</span><span class="sxs-lookup"><span data-stu-id="b7451-127">An existing attribute in Active Directory Domain Services that is now associated with the <strong>msRTCSIP-Pool</strong> and <strong>msRTCSIP-MonitoringServer</strong> classes.</span></span> <span data-ttu-id="b7451-128">Este atributo especifica el nombre de dominio completo (FQDN) de un grupo o servidor de supervisión.</span><span class="sxs-lookup"><span data-stu-id="b7451-128">This attribute specifies the fully qualified domain name (FQDN) of a pool or Monitoring Server.</span></span></p>
<p><span data-ttu-id="b7451-129">Un valor válido para cada segmento es de 63 caracteres; un valor válido para todo el FQDN es 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b7451-129">A valid value for each segment is 63 characters; a valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="b7451-130">Novedades de Microsoft Office Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-130">New in Microsoft Office Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-131">msDS-SourceObjectDN</span><span class="sxs-lookup"><span data-stu-id="b7451-131">msDS-SourceObjectDN</span></span></p></td>
<td><p><span data-ttu-id="b7451-132">Este atributo contiene la representación de cadena del nombre distintivo (DN) del objeto de otro bosque que corresponde a este objeto.</span><span class="sxs-lookup"><span data-stu-id="b7451-132">This attribute contains the string representation of the distinguished name (DN) of the object in another forest that corresponds to this object.</span></span> <span data-ttu-id="b7451-133">Este atributo se usa para la expansión del grupo de distribución y la asistencia automática.</span><span class="sxs-lookup"><span data-stu-id="b7451-133">This attribute is used for distribution group expansion and auto attendance.</span></span> <span data-ttu-id="b7451-134">Este atributo se define en el esquema predeterminado de Active Directory para Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-134">This attribute is defined in the default Active Directory schema for Windows Server 2003 R2.</span></span></p>
<p><span data-ttu-id="b7451-135">Para evitar tener que actualizar AD DS a Windows Server 2003 R2, la preparación del esquema de Active Directory extiende el esquema de Windows Server 2003 con esta definición de atributo.</span><span class="sxs-lookup"><span data-stu-id="b7451-135">To avoid requiring an upgrade of AD DS to Windows Server 2003 R2, Active Directory schema preparation extends the Windows Server 2003 schema with this attribute definition.</span></span></p></td>
<td><p><span data-ttu-id="b7451-136">Novedades de Microsoft Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-136">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-137">msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="b7451-137">msExchUCVoiceMailSettings</span></span></p></td>
<td><p><span data-ttu-id="b7451-138">Este atributo de valor múltiple contiene la configuración del correo de voz.</span><span class="sxs-lookup"><span data-stu-id="b7451-138">This multi-valued attribute holds voice mail settings.</span></span> <span data-ttu-id="b7451-139">Este atributo se comparte con la mensajería unificada de Exchange (UM).</span><span class="sxs-lookup"><span data-stu-id="b7451-139">This attribute is shared with Exchange Unified Messaging (UM).</span></span></p></td>
<td><p><span data-ttu-id="b7451-140">Novedades de Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-140">New in Microsoft Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-141">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="b7451-141">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="b7451-142">Este atributo de valor múltiple contiene los identificadores para las directivas de retención que se aplican al usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-142">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="b7451-143">Las directivas de retención mantienen los elementos del buzón de correo para el usuario durante el período de espera.</span><span class="sxs-lookup"><span data-stu-id="b7451-143">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="b7451-144">Este atributo se comparte con Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="b7451-144">This attribute is shared with Exchange 2013.</span></span></p></td>
<td><p><span data-ttu-id="b7451-145">Novedades de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b7451-145">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-146">msRTCSIP-AcpInfo</span><span class="sxs-lookup"><span data-stu-id="b7451-146">msRTCSIP-AcpInfo</span></span></p></td>
<td><p><span data-ttu-id="b7451-147">Este atributo almacena información del proveedor de servicios de audioconferencia para un usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-147">This attribute stores audio conferencing provider information for a user.</span></span></p></td>
<td><p><span data-ttu-id="b7451-148">Novedades de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-148">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-149">msRTCSIP-ApplicationDestination</span><span class="sxs-lookup"><span data-stu-id="b7451-149">msRTCSIP-ApplicationDestination</span></span></p></td>
<td><p><span data-ttu-id="b7451-150">Este atributo señala a la entrada de servicio de confianza del contacto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-150">This attribute points to the trusted service entry for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="b7451-151">Novedades de Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-151">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-152">msRTCSIP-ApplicationList</span><span class="sxs-lookup"><span data-stu-id="b7451-152">msRTCSIP-ApplicationList</span></span></p></td>
<td><p><span data-ttu-id="b7451-153">Este atributo contiene una lista de aplicaciones hospedadas en el servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b7451-153">This attribute contains a list of hosted applications on the application server.</span></span></p></td>
<td><p><span data-ttu-id="b7451-154">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-154">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-155">msRTCSIP-ApplicationOptions</span><span class="sxs-lookup"><span data-stu-id="b7451-155">msRTCSIP-ApplicationOptions</span></span></p></td>
<td><p><span data-ttu-id="b7451-156">Este atributo especifica las opciones para el contacto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-156">This attribute specifies the options for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="b7451-157">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-157">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-158">msRTCSIP-ApplicationPrimaryLanguage</span><span class="sxs-lookup"><span data-stu-id="b7451-158">msRTCSIP-ApplicationPrimaryLanguage</span></span></p></td>
<td><p><span data-ttu-id="b7451-159">Este atributo contiene el idioma principal del contacto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-159">This attribute contains the primary language for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="b7451-160">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-160">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-161">msRTCSIP-ApplicationSecondaryLanguages</span><span class="sxs-lookup"><span data-stu-id="b7451-161">msRTCSIP-ApplicationSecondaryLanguages</span></span></p></td>
<td><p><span data-ttu-id="b7451-162">Este atributo de valor múltiple contiene los idiomas secundarios para el contacto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-162">This multiple value attribute contains the secondary languages for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="b7451-163">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-163">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-164">msRTCSIP-ApplicationServerBL</span><span class="sxs-lookup"><span data-stu-id="b7451-164">msRTCSIP-ApplicationServerBL</span></span></p></td>
<td><p><span data-ttu-id="b7451-165">Este atributo contiene una lista de servidores de aplicaciones que pertenecen a este grupo.</span><span class="sxs-lookup"><span data-stu-id="b7451-165">This attribute contains a list of application servers that belong to this pool.</span></span> <span data-ttu-id="b7451-166">El vínculo de reenvío correspondiente a este atributo de vínculo de retroceso es <strong>msRTCSIP-ApplicationServerPoolLink</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-166">The corresponding forward link to this back link attribute is <strong>msRTCSIP-ApplicationServerPoolLink</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-167">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-167">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-168">msRTCSIP-ApplicationServerPoolLink</span><span class="sxs-lookup"><span data-stu-id="b7451-168">msRTCSIP-ApplicationServerPoolLink</span></span></p></td>
<td><p><span data-ttu-id="b7451-169">Este atributo señala al grupo al que pertenece este servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b7451-169">This attribute points to the pool to which this application server belongs.</span></span> <span data-ttu-id="b7451-170">Este es el vínculo hacia adelante.</span><span class="sxs-lookup"><span data-stu-id="b7451-170">This is the forward link.</span></span> <span data-ttu-id="b7451-171">El correspondiente vínculo de retroceso es <strong>msRTCSIP-ApplicationServerBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-171">The corresponding backward link is <strong>msRTCSIP-ApplicationServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-172">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-172">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-173">msRTCSIP-ArchiveDefault (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-173">msRTCSIP-ArchiveDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="b7451-174">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-174">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="b7451-175">Obsoleto en Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-175">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-176">msRTCSIP-ArchiveDefaultFlags (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-176">msRTCSIP-ArchiveDefaultFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-177">Este atributo especifica el valor predeterminado global dentro del límite del bosque para archivar todas las comunicaciones de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="b7451-177">This attribute specifies the global default within the forest boundary for archiving all user communications.</span></span> <span data-ttu-id="b7451-178">Esto lo aplica la capa del agente de archivado.</span><span class="sxs-lookup"><span data-stu-id="b7451-178">This is enforced by the archiving agent layer.</span></span> <span data-ttu-id="b7451-179">El intervalo de valores para este atributo es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="b7451-179">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-180"><strong>True</strong>: archivar todos los usuarios</span><span class="sxs-lookup"><span data-stu-id="b7451-180"><strong>TRUE</strong>: Archive all users</span></span></p></li>
<li><p><span data-ttu-id="b7451-181"><strong>False</strong>: no archivar todos los usuarios</span><span class="sxs-lookup"><span data-stu-id="b7451-181"><strong>FALSE</strong>: Do not archive all users</span></span></p></li>
</ul>
<p><span data-ttu-id="b7451-182">Este atributo controla globalmente, dentro del límite del bosque, cómo se archivan las comunicaciones de los usuarios dentro de una red interna.</span><span class="sxs-lookup"><span data-stu-id="b7451-182">This attribute globally controls, within the forest boundary, how user communications within an internal network are archived.</span></span></p>
<p><span data-ttu-id="b7451-183"><strong>Comportamiento de Live Communications Server 2005 (ahora retirado)</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-183"><strong>Live Communications Server 2005 behavior (now retired)</strong></span></span></p>
<p><span data-ttu-id="b7451-184">El intervalo de valores para este atributo es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="b7451-184">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-185">0: archivar el cuerpo del mensaje [bit 0]</span><span class="sxs-lookup"><span data-stu-id="b7451-185">0: Archive the message body [bit 0]</span></span></p></li>
<li><p><span data-ttu-id="b7451-186">1: no archivar el cuerpo del mensaje [bit 0]</span><span class="sxs-lookup"><span data-stu-id="b7451-186">1: Do not archive the message body [bit 0]</span></span></p></li>
</ul>
<p><span data-ttu-id="b7451-187"><strong>Comportamiento de Office Communications Server 2007</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-187"><strong>Office Communications Server 2007 behavior</strong></span></span></p>
<p><span data-ttu-id="b7451-188">El intervalo de valores para este atributo es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="b7451-188">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-189">0: ArchiveFederationDefaultWithoutBody (retirado)</span><span class="sxs-lookup"><span data-stu-id="b7451-189">0: ArchiveFederationDefaultWithoutBody (retired)</span></span></p></li>
<li><p><span data-ttu-id="b7451-190">1-2: ArchiveInternalCommunications</span><span class="sxs-lookup"><span data-stu-id="b7451-190">1-2: ArchiveInternalCommunications</span></span></p></li>
<li><p><span data-ttu-id="b7451-191">3-4: ArchiveFederatedCommunications</span><span class="sxs-lookup"><span data-stu-id="b7451-191">3-4: ArchiveFederatedCommunications</span></span></p></li>
<li><p><span data-ttu-id="b7451-192">5: RecordPresenceRegistrations</span><span class="sxs-lookup"><span data-stu-id="b7451-192">5: RecordPresenceRegistrations</span></span></p></li>
<li><p><span data-ttu-id="b7451-193">6: RecordIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="b7451-193">6: RecordIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="b7451-194">7: RecordGroupIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="b7451-194">7: RecordGroupIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="b7451-195">8: RecordFileTransferInstances</span><span class="sxs-lookup"><span data-stu-id="b7451-195">8: RecordFileTransferInstances</span></span></p></li>
<li><p><span data-ttu-id="b7451-196">9: RecordAudioCallDetails</span><span class="sxs-lookup"><span data-stu-id="b7451-196">9: RecordAudioCallDetails</span></span></p></li>
<li><p><span data-ttu-id="b7451-197">10: RecordVideoCallDetails</span><span class="sxs-lookup"><span data-stu-id="b7451-197">10: RecordVideoCallDetails</span></span></p></li>
<li><p><span data-ttu-id="b7451-198">11: RecordRemoteAssistanceCallDetails</span><span class="sxs-lookup"><span data-stu-id="b7451-198">11: RecordRemoteAssistanceCallDetails</span></span></p></li>
<li><p><span data-ttu-id="b7451-199">12: RecordApplicationSharingDetails</span><span class="sxs-lookup"><span data-stu-id="b7451-199">12: RecordApplicationSharingDetails</span></span></p></li>
<li><p><span data-ttu-id="b7451-200">13: RecordMeetingInstantiations</span><span class="sxs-lookup"><span data-stu-id="b7451-200">13: RecordMeetingInstantiations</span></span></p></li>
<li><p><span data-ttu-id="b7451-201">14: RecordMeetingJoins</span><span class="sxs-lookup"><span data-stu-id="b7451-201">14: RecordMeetingJoins</span></span></p></li>
<li><p><span data-ttu-id="b7451-202">15: RecordDataJoins</span><span class="sxs-lookup"><span data-stu-id="b7451-202">15: RecordDataJoins</span></span></p></li>
<li><p><span data-ttu-id="b7451-203">16: RecordAVJoins</span><span class="sxs-lookup"><span data-stu-id="b7451-203">16: RecordAVJoins</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-204">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-204">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="b7451-205">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-205">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-206">msRTCSIP-ArchiveFederationDefault (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-206">msRTCSIP-ArchiveFederationDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="b7451-207">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-207">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="b7451-208">Obsoleto en Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-208">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-209">msRTCSIP-ArchiveFederationDefaultFlags (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-209">msRTCSIP-ArchiveFederationDefaultFlags (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="b7451-210">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-210">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="b7451-211">Obsoleto en Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-211">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-212">msRTCSIP-ArchivingEnabled</span><span class="sxs-lookup"><span data-stu-id="b7451-212">msRTCSIP-ArchivingEnabled</span></span></p></td>
<td><p><span data-ttu-id="b7451-213">Este atributo es un entero usado como campo de bits para controlar si se van a archivar las comunicaciones de un solo usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-213">This attribute is an integer used as a bit field to control whether a single user’s communications are to be archived.</span></span> <span data-ttu-id="b7451-214">Este control lo aplica la capa del agente de archivado.</span><span class="sxs-lookup"><span data-stu-id="b7451-214">This control is enforced by the archiving agent layer.</span></span> <span data-ttu-id="b7451-215">Se marca para la replicación del catálogo global.</span><span class="sxs-lookup"><span data-stu-id="b7451-215">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="b7451-216">El ámbito de este atributo es específico de un solo usuario o contacto.</span><span class="sxs-lookup"><span data-stu-id="b7451-216">The scope of this attribute is specific to a single user or contact.</span></span> <span data-ttu-id="b7451-217">Los valores válidos (y las posiciones de bits asociadas) en Lync Server son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-217">The valid values (and associated bit positions) in Lync Server are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-218">0: no archivar (sin bit establecido)</span><span class="sxs-lookup"><span data-stu-id="b7451-218">0: Do not archive (no bit set)</span></span></p></li>
<li><p><span data-ttu-id="b7451-219">1: retirado (posición de bit 0)</span><span class="sxs-lookup"><span data-stu-id="b7451-219">1: Retired (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="b7451-220">2: retirado (posición de bit 1)</span><span class="sxs-lookup"><span data-stu-id="b7451-220">2: Retired (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="b7451-221">4: comunicaciones internas de archivo (posición de bit 2)</span><span class="sxs-lookup"><span data-stu-id="b7451-221">4: Archive internal communications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="b7451-222">8: archivar comunicaciones federadas (posición de bit 3)</span><span class="sxs-lookup"><span data-stu-id="b7451-222">8: Archive federated communications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="b7451-223">Los valores anteriores válidos en Live Communications Server 2005 son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-223">Previously valid values in Live Communications Server 2005 are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-224">0: Use el valor predeterminado definido por <strong>msRTCSIP-ArchiveDefault</strong> y <strong>msRTCSIP-ArchiveFederation</strong> en este orden de prioridad:</span><span class="sxs-lookup"><span data-stu-id="b7451-224">0:Use the default value defined by <strong>msRTCSIP-ArchiveDefault</strong> and <strong>msRTCSIP-ArchiveFederation</strong> in this order of precedence:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-225">1: archivo</span><span class="sxs-lookup"><span data-stu-id="b7451-225">1: Archive</span></span></p></li>
<li><p><span data-ttu-id="b7451-226">2: no archivar</span><span class="sxs-lookup"><span data-stu-id="b7451-226">2: Do not archive</span></span></p></li>
<li><p><span data-ttu-id="b7451-227">3: archivar sin el cuerpo del mensaje</span><span class="sxs-lookup"><span data-stu-id="b7451-227">3: Archive without the message body</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="b7451-228">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-228">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-229">msRTCSIP-ArchivingServerData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-229">msRTCSIP-ArchivingServerData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-230">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-230">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-231">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-231">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-232">msRTCSIP-ArchivingServerVersion (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-232">msRTCSIP-ArchivingServerVersion (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-233">Este atributo define la versión del servicio de archivado.</span><span class="sxs-lookup"><span data-stu-id="b7451-233">This attribute defines the version of the Archiving service.</span></span> <span data-ttu-id="b7451-234">Este atributo es un tipo entero monotonously que se incrementa con cada lanzamiento oficial de producto.</span><span class="sxs-lookup"><span data-stu-id="b7451-234">This attribute is a monotonously increasing integer type that increments with each official product release.</span></span> <span data-ttu-id="b7451-235">Los valores válidos posibles son:</span><span class="sxs-lookup"><span data-stu-id="b7451-235">The possible valid values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-236">Undefined: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7451-236">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="b7451-237">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="b7451-237">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="b7451-238">Live Communications Server 2005 con SP1</span><span class="sxs-lookup"><span data-stu-id="b7451-238">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="b7451-239">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="b7451-239">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="b7451-240">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="b7451-240">4: Office Communications Server 2007 R2</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-241">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-241">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-242">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-243">msRTCSIP-BackEndServer</span><span class="sxs-lookup"><span data-stu-id="b7451-243">msRTCSIP-BackEndServer</span></span></p></td>
<td><p><span data-ttu-id="b7451-244">Este atributo especifica el nombre de dominio completo (FQDN) del servidor back-end de la agrupación.</span><span class="sxs-lookup"><span data-stu-id="b7451-244">This attribute specifies the FQDN of the Back End Server of the pool.</span></span> <span data-ttu-id="b7451-245">Puesto que solo puede haber un único servidor de servicios de fondo por grupo, se trata de un atributo de valor único.</span><span class="sxs-lookup"><span data-stu-id="b7451-245">Because there can only be a single Back End Server per pool, this is a single-valued attribute.</span></span></p>
<p><span data-ttu-id="b7451-246">El valor válido para cada segmento es de 63 caracteres; el valor válido para todo el FQDN es 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b7451-246">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="b7451-247">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-247">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-248">msRTCSIP-ConferenceDirectoryHomePool</span><span class="sxs-lookup"><span data-stu-id="b7451-248">msRTCSIP-ConferenceDirectoryHomePool</span></span></p></td>
<td><p><span data-ttu-id="b7451-249">Este atributo contiene el identificador del grupo de servidores que hospeda el directorio de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="b7451-249">This attribute contains the identifier of the pool that hosts the conference directory.</span></span></p></td>
<td><p><span data-ttu-id="b7451-250">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-250">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-251">msRTCSIP-ConferenceDirectoryId</span><span class="sxs-lookup"><span data-stu-id="b7451-251">msRTCSIP-ConferenceDirectoryId</span></span></p></td>
<td><p><span data-ttu-id="b7451-252">Este atributo contiene el identificador de un directorio de conferencia.</span><span class="sxs-lookup"><span data-stu-id="b7451-252">This attribute contains the identifier of a conference directory.</span></span></p></td>
<td><p><span data-ttu-id="b7451-253">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-253">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-254">msRTCSIP-ConferenceDirectoryTargetPool</span><span class="sxs-lookup"><span data-stu-id="b7451-254">msRTCSIP-ConferenceDirectoryTargetPool</span></span></p></td>
<td><p><span data-ttu-id="b7451-255">Este atributo contiene el identificador de la agrupación a la que se mueve el directorio de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="b7451-255">This attribute contains the identifier of the pool to which the conference directory is being moved.</span></span></p></td>
<td><p><span data-ttu-id="b7451-256">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-256">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-257">msRTCSIP-default</span><span class="sxs-lookup"><span data-stu-id="b7451-257">msRTCSIP-Default</span></span></p></td>
<td><p><span data-ttu-id="b7451-258">Este atributo booleano define si el uso del teléfono es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b7451-258">This Boolean attribute defines whether the phone usage is a default usage.</span></span> <span data-ttu-id="b7451-259">Si este atributo se establece en <strong>true</strong>, el uso del teléfono es un uso predeterminado y el administrador no puede eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="b7451-259">If this attribute is set to <strong>TRUE</strong>, the phone usage is a default usage and cannot be deleted by the administrator.</span></span> <span data-ttu-id="b7451-260">Si este atributo se establece en <strong>false</strong>, el uso se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="b7451-260">If this attribute is set to <strong>FALSE</strong>, the usage can be deleted.</span></span></p></td>
<td><p><span data-ttu-id="b7451-261">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-261">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-262">msRTCSIP-DefaultCWAExternalURL</span><span class="sxs-lookup"><span data-stu-id="b7451-262">msRTCSIP-DefaultCWAExternalURL</span></span></p></td>
<td><p><span data-ttu-id="b7451-263">Este atributo identifica la dirección URL de Communicator Web Access para los usuarios que están fuera de la organización.</span><span class="sxs-lookup"><span data-stu-id="b7451-263">This attribute identifies the Communicator Web Access URL for users who are outside the organization.</span></span></p></td>
<td><p><span data-ttu-id="b7451-264">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-264">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-265">msRTCSIP-DefaultCWAInternalURL</span><span class="sxs-lookup"><span data-stu-id="b7451-265">msRTCSIP-DefaultCWAInternalURL</span></span></p></td>
<td><p><span data-ttu-id="b7451-266">Este atributo identifica la dirección URL de Communicator Web Access para los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="b7451-266">This attribute identifies the Communicator Web Access URL for users who are inside the organization.</span></span></p></td>
<td><p><span data-ttu-id="b7451-267">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-267">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-268">msRTCSIP-DefaultLocationProfileLink (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-268">msRTCSIP-DefaultLocationProfileLink (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-269">Este atributo de valor único contiene el nombre distintivo (DN) de un objeto de clase de Perfil de ubicación asignado a él.</span><span class="sxs-lookup"><span data-stu-id="b7451-269">This single-valued attribute contains the distinguished name (DN) of a location profile class object assigned to it.</span></span></p>
<p><span data-ttu-id="b7451-270">Vínculo hacia adelante: <strong>identificador de vínculo 11036</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-270">Forward link: <strong>Link ID 11036</strong></span></span></p>
<p><span data-ttu-id="b7451-271">El correspondiente vínculo de retroceso es <strong>msRTCSIP-ServerReferenceBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-271">The corresponding backward link is <strong>msRTCSIP-ServerReferenceBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-272">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-272">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-273">msRTCSIP-DefaultPolicy (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-273">msRTCSIP-DefaultPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-274">Este atributo Boolean especifica si la Directiva es una directiva predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b7451-274">This Boolean attribute specifies whether the policy is a default policy.</span></span> <span data-ttu-id="b7451-275">La Directiva es una directiva predeterminada cuando se establece en <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-275">The policy is a default policy when set to <strong>TRUE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-276">Novedades de Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="b7451-276">New in Office Communications Server 2007</span></span></p>
<p><span data-ttu-id="b7451-277">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-277">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-278">msRTCSIP-DefaultRouteToEdgeProxy (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-278">msRTCSIP-DefaultRouteToEdgeProxy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-279">Este atributo especifica el FQDN del servidor perimetral que está ejecutando el servicio perimetral de acceso, si se puede obtener acceso a él directamente, o del equilibrador de carga de hardware para un grupo de servidores que ejecutan el servicio perimetral de acceso.</span><span class="sxs-lookup"><span data-stu-id="b7451-279">This attribute specifies the FQDN of either the Edge Server running the Access Edge service, if it can be accessed directly, or of the hardware load balancer for a pool of servers running Access Edge service.</span></span> <span data-ttu-id="b7451-280">Si solo se puede acceder a los servidores que ejecutan Access Edge a través de uno o más directores, este atributo especifica el FQDN y, opcionalmente, el número de puerto del director o del equilibrador de carga de hardware que atiende un grupo de directores.</span><span class="sxs-lookup"><span data-stu-id="b7451-280">If the servers running Access Edge service can be accessed only through one or more Directors, this attribute specifies the FQDN and, optionally, the port number of the Director or of the hardware load balancer serving a Director pool.</span></span></p>
<p><span data-ttu-id="b7451-281">El valor válido para cada segmento es de 63 caracteres; el valor válido para todo el FQDN es 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b7451-281">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="b7451-282">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-282">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="b7451-283">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-283">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-284">msRTCSIP-DefaultRouteToEdgeProxyPort (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-284">msRTCSIP-DefaultRouteToEdgeProxyPort (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-285">Este atributo representa el número de puerto que debe usarse para conectarse al servidor que ejecuta el servicio perimetral de acceso.</span><span class="sxs-lookup"><span data-stu-id="b7451-285">This attribute represents the port number that should be used to connect to the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="b7451-286">El valor válido es un valor entero que especifica el puerto que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b7451-286">The valid value is an integer value specifying the port to be used.</span></span> <span data-ttu-id="b7451-287">El valor predeterminado es 5061.</span><span class="sxs-lookup"><span data-stu-id="b7451-287">The default value is 5061.</span></span></p></td>
<td><p><span data-ttu-id="b7451-288">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-288">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="b7451-289">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-289">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-290">msRTCSIP-DefPresenceSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-290">msRTCSIP-DefPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-291">Este atributo representa el período de tiempo de espera predeterminado de la suscripción de presencia.</span><span class="sxs-lookup"><span data-stu-id="b7451-291">This attribute represents the default presence subscription time-out period.</span></span></p></td>
<td><p><span data-ttu-id="b7451-292">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-292">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-293">msRTCSIP-DefRegistrationTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-293">msRTCSIP-DefRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-294">Este atributo representa la ventana de tiempo de espera de registro predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b7451-294">This attribute represents the default registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="b7451-295">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-295">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-297">Este atributo representa la ventana de tiempo de espera predeterminada de la suscripción de datos de itinerancia.</span><span class="sxs-lookup"><span data-stu-id="b7451-297">This attribute represents the default roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="b7451-298">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-298">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-299">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="b7451-299">msRTCSIP-DeploymentLocator</span></span></p></td>
<td><p><span data-ttu-id="b7451-300">Este atributo se usa en una topología de dominio dividida y contiene un nombre de dominio completo (FQDN).</span><span class="sxs-lookup"><span data-stu-id="b7451-300">This attribute is used in a split domain topology and contains a fully qualified domain name (FQDN).</span></span></p></td>
<td><p><span data-ttu-id="b7451-301">Novedades de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-301">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-302">msRTCSIP-Description (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-302">msRTCSIP-Description (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-303">Este atributo de cadena Unicode de valor único contiene una descripción detallada de esta ruta de teléfono o regla de normalización.</span><span class="sxs-lookup"><span data-stu-id="b7451-303">This single-valued UNICODE string attribute contains a friendly description of this phone route or normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="b7451-304">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-304">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-305">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-305">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-306">msRTCSIP-DomainData</span><span class="sxs-lookup"><span data-stu-id="b7451-306">msRTCSIP-DomainData</span></span></p></td>
<td><p><span data-ttu-id="b7451-307">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-307">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-308">msRTCSIP-DomainName</span><span class="sxs-lookup"><span data-stu-id="b7451-308">msRTCSIP-DomainName</span></span></p></td>
<td><p><span data-ttu-id="b7451-309">Este atributo representa un dominio configurado para el registrador.</span><span class="sxs-lookup"><span data-stu-id="b7451-309">This attribute represents a domain configured for the Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-310">msRTCSIP-EdgeProxyData</span><span class="sxs-lookup"><span data-stu-id="b7451-310">msRTCSIP-EdgeProxyData</span></span></p></td>
<td><p><span data-ttu-id="b7451-311">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-311">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-312">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-312">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-313">msRTCSIP-EdgeProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="b7451-313">msRTCSIP-EdgeProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="b7451-314">Este atributo especifica el FQDN del servidor que ejecuta el servicio perimetral de acceso.</span><span class="sxs-lookup"><span data-stu-id="b7451-314">This attribute specifies the FQDN of the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="b7451-315">El valor válido para cada segmento es de 63 caracteres; el valor válido para todo el FQDN es 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b7451-315">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="b7451-316">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-316">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-317">msRTCSIP-EnableBestEffortNotify (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-317">msRTCSIP-EnableBestEffortNotify (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-318">Este atributo controla si un servidor genera una solicitud de notificación de mejor esfuerzo (BENOTIFY), en lugar de una solicitud NOTIFY, en respuesta a una solicitud SUBSCRIBE de un cliente.</span><span class="sxs-lookup"><span data-stu-id="b7451-318">This attribute controls whether a server generates a Best Effort NOTIFY (BENOTIFY) request, instead of a NOTIFY request, in response to a SUBSCRIBE request from a client.</span></span> <span data-ttu-id="b7451-319">BENOTIFY es una extensión que mejora el rendimiento del Protocolo de enlace para notificaciones en el que el servidor genera solicitudes BENOTIFY, en lugar de solicitudes de notificación ordinarias.</span><span class="sxs-lookup"><span data-stu-id="b7451-319">BENOTIFY is a performance-enhancing extension to the subscribe notification handshake where the server generates BENOTIFY requests, instead of regular NOTIFY requests.</span></span> <span data-ttu-id="b7451-320">La ventaja de rendimiento es que una solicitud BENOTIFY no requiere una respuesta 200 del cliente, ya que la solicitud NOTIFY sí.</span><span class="sxs-lookup"><span data-stu-id="b7451-320">The performance benefit is that a BENOTIFY request does not require a 200 OK response from the client as the NOTIFY request does.</span></span></p>
<p><span data-ttu-id="b7451-321">Los valores válidos son <strong>true</strong> o <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-321">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="b7451-322">Live Communications Server 2003 no admite solicitudes BENOTIFY.</span><span class="sxs-lookup"><span data-stu-id="b7451-322">Live Communications Server 2003 does not support BENOTIFY requests.</span></span> <span data-ttu-id="b7451-323">Para interactuar con aplicaciones de servidor escritas con la API de servidor de Live Communications Server 2003 que se ejecuta en Live Communications Server 2005 y en servidores de terceros, las solicitudes BENOTIFY pueden deshabilitarse estableciendo su valor en <STRONG>false</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b7451-323">To interoperate with server applications written with the Live Communications Server 2003 server API running on Live Communications Server 2005 and third-party servers, BENOTIFY requests can be disabled by setting its value to <STRONG>FALSE</STRONG>.</span></span> <span data-ttu-id="b7451-324">BENOTIFY no forma parte del proceso de estandarización de SIP (el equipo de tareas de ingeniería de Internet) IETF.</span><span class="sxs-lookup"><span data-stu-id="b7451-324">BENOTIFY is not currently part of the IETF (Internet Engineering Task Force) SIP standardization process.</span></span>


</div></td>
<td><p><span data-ttu-id="b7451-325">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-325">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="b7451-326">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-326">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-327">msRTCSIP-EnableFederation (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-327">msRTCSIP-EnableFederation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-328">Este atributo es un modificador global que los administradores de ti usan para configurar si los usuarios pueden comunicarse con usuarios de otras organizaciones.</span><span class="sxs-lookup"><span data-stu-id="b7451-328">This attribute is a global switch that IT administrators use to configure whether users are allowed to communicate with users from other organizations.</span></span> <span data-ttu-id="b7451-329">Permite a un administrador sobrescribir el atributo <strong>FederationEnabled</strong> de un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="b7451-329">It enables an administrator to overwrite an individual user’s <strong>FederationEnabled</strong> attribute.</span></span> <span data-ttu-id="b7451-330">Este atributo puede ser útil para ayudar a proteger la red interna de ataques de Internet que pueden estar causados por gusanos, virus o ataques dirigidos a la compañía.</span><span class="sxs-lookup"><span data-stu-id="b7451-330">This attribute can be useful to help protect the internal network from Internet attacks that may be caused by worms, viruses, or targeted attacks on the company.</span></span></p>
<p><span data-ttu-id="b7451-331">Los valores válidos (y las posiciones de bits asociadas) son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-331">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-332">1: habilitado para conectividad de mensajería instantánea pública (posición de bit 0)</span><span class="sxs-lookup"><span data-stu-id="b7451-332">1: Enabled for public IM connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="b7451-333">2: reservado (posición de bit 1)</span><span class="sxs-lookup"><span data-stu-id="b7451-333">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="b7451-334">4: reservado (posición de bit 2)</span><span class="sxs-lookup"><span data-stu-id="b7451-334">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="b7451-335">8: reservado (posición de bit 3)</span><span class="sxs-lookup"><span data-stu-id="b7451-335">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="b7451-336">16: control remoto de llamadas habilitado [telefonía] (posición de bit 4)</span><span class="sxs-lookup"><span data-stu-id="b7451-336">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="b7451-337">64: AllowOrganizeMeetingWithAnonymousParticipants (permitir a los usuarios invitar a usuarios anónimos a reuniones (bit 6)</span><span class="sxs-lookup"><span data-stu-id="b7451-337">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="b7451-338">128: UCEnabled (habilitar usuarios para comunicaciones unificadas) (posición de bit 7)</span><span class="sxs-lookup"><span data-stu-id="b7451-338">128: UCEnabled (enable users for unified communications) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="b7451-339">256: EnabledForEnhancedPresence (habilitar usuario para conectividad de mensajería instantánea pública) (posición de bit 8)</span><span class="sxs-lookup"><span data-stu-id="b7451-339">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="b7451-340">512: RemoteCallControlDualMode (posición de bit 9)</span><span class="sxs-lookup"><span data-stu-id="b7451-340">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-341">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-341">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="b7451-342">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-342">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-343">msRTCSIP-EnterpriseServices</span><span class="sxs-lookup"><span data-stu-id="b7451-343">msRTCSIP-EnterpriseServices</span></span></p></td>
<td><p><span data-ttu-id="b7451-344">Este atributo indica si los servicios empresariales se cargan en el servidor dado.</span><span class="sxs-lookup"><span data-stu-id="b7451-344">This attribute indicates whether the Enterprise Services are loaded on the given server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-345">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="b7451-345">msRTCSIP-ExtensionData</span></span></p></td>
<td><p><span data-ttu-id="b7451-346">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-346">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-347">msRTCSIP-ExternalAccessCode</span><span class="sxs-lookup"><span data-stu-id="b7451-347">msRTCSIP-ExternalAccessCode</span></span></p></td>
<td><p><span data-ttu-id="b7451-348">Este atributo contiene el código de marcado para acceso externo.</span><span class="sxs-lookup"><span data-stu-id="b7451-348">This attribute contains the dial code for external access.</span></span></p></td>
<td><p><span data-ttu-id="b7451-349">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-349">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-350">msRTCSIP-FederationEnabled</span><span class="sxs-lookup"><span data-stu-id="b7451-350">msRTCSIP-FederationEnabled</span></span></p></td>
<td><p><span data-ttu-id="b7451-351">Este atributo controla si un solo usuario está habilitado para la Federación.</span><span class="sxs-lookup"><span data-stu-id="b7451-351">This attribute controls whether a single user is enabled for federation.</span></span> <span data-ttu-id="b7451-352">La capa de servicios empresariales la aplica.</span><span class="sxs-lookup"><span data-stu-id="b7451-352">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="b7451-353">Se marca para la replicación del catálogo global.</span><span class="sxs-lookup"><span data-stu-id="b7451-353">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="b7451-354">Los valores válidos son <strong>true</strong> o <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-354">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-355">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-355">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-356">msRTCSIP-FrontEndServers</span><span class="sxs-lookup"><span data-stu-id="b7451-356">msRTCSIP-FrontEndServers</span></span></p></td>
<td><p><span data-ttu-id="b7451-357">Este atributo es una lista con varios valores de los nombres de dominio de todos los servidores Enterprise Edition asociados a un grupo.</span><span class="sxs-lookup"><span data-stu-id="b7451-357">This attribute is a multi-valued list of the domain names of all Enterprise Edition servers associated with a pool.</span></span></p>
<p><span data-ttu-id="b7451-358">Vínculo anterior: <strong>identificador de vínculo 11023</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-358">Back link: <strong>Link ID 11023</strong></span></span></p>
<p><span data-ttu-id="b7451-359">El vínculo de reenvío correspondiente a este vínculo anterior es <strong>msRTCSIP-PoolAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-359">The corresponding forward link to this back link is <strong>msRTCSIP-PoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-360">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-360">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-361">msRTCSIP-gateways (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-361">msRTCSIP-Gateways (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-362">Este atributo de cadena de valor múltiple contiene una lista de puertas de enlace y puertos (por puerta de enlace).</span><span class="sxs-lookup"><span data-stu-id="b7451-362">This multi-valued string attribute contains a list of gateways and ports (per gateway).</span></span></p></td>
<td><p><span data-ttu-id="b7451-363">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-363">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-364">msRTCSIP-GlobalSettingsData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-364">msRTCSIP-GlobalSettingsData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-365">Este atributo almacena pares de nombre: valor.</span><span class="sxs-lookup"><span data-stu-id="b7451-365">This attribute stores name:value pairs.</span></span> <span data-ttu-id="b7451-366">El par nombre: valor ya definido es para permitir el <strong>sondeo de la configuración de presencia</strong> .</span><span class="sxs-lookup"><span data-stu-id="b7451-366">The already-defined name:value pair is for the <strong>allow polling for presence</strong> setting.</span></span></p></td>
<td><p><span data-ttu-id="b7451-367">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-367">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-368">msRTCSIP-GroupingID</span><span class="sxs-lookup"><span data-stu-id="b7451-368">msRTCSIP-GroupingID</span></span></p></td>
<td><p><span data-ttu-id="b7451-369">Este atributo es un identificador único de un grupo que se usa para agrupar las entradas de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="b7451-369">This attribute is a unique identifier of a group that is used to group address book entries.</span></span></p></td>
<td><p><span data-ttu-id="b7451-370">Novedades de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-370">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-371">msRTCSIP-HomeServer (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-371">msRTCSIP-HomeServer (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="b7451-372">Novedades de Live Communications Server 2003 (no usado).</span><span class="sxs-lookup"><span data-stu-id="b7451-372">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="b7451-373">Obsoleto en Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-373">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-374">msRTCSIP-HomeServerString (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-374">msRTCSIP-HomeServerString (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="b7451-375">Novedades de Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b7451-375">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="b7451-376">Obsoleto en Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-376">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-377">msRTCSIP-HomeUsers (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-377">msRTCSIP-HomeUsers (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="b7451-378">Novedades de Live Communications Server 2003 (no usado).</span><span class="sxs-lookup"><span data-stu-id="b7451-378">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="b7451-379">Obsoleto en Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-379">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-380">msRTCSIP-InternetAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="b7451-380">msRTCSIP-InternetAccessEnabled</span></span></p></td>
<td><p><span data-ttu-id="b7451-381">Este atributo controla si un solo usuario está habilitado para el acceso de usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="b7451-381">This attribute controls whether a single user is enabled for outside user access.</span></span> <span data-ttu-id="b7451-382">La capa de servicios empresariales la aplica.</span><span class="sxs-lookup"><span data-stu-id="b7451-382">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="b7451-383">Se marca para la replicación del catálogo global.</span><span class="sxs-lookup"><span data-stu-id="b7451-383">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="b7451-384">Los valores válidos son <strong>true</strong> o <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-384">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-385">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-385">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-386">msRTCSIP-IsMaster (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-386">msRTCSIP-IsMaster (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="b7451-387">Novedades de Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7451-387">New in Live Communications Server 2003</span></span></p>
<p><span data-ttu-id="b7451-388">Obsoleto en Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-388">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-389">msRTCSIP-line</span><span class="sxs-lookup"><span data-stu-id="b7451-389">msRTCSIP-Line</span></span></p></td>
<td><p><span data-ttu-id="b7451-390">Este atributo de valor único contiene el identificador de dispositivo (el URI de SIP o el URI de TEL? del teléfono que usa Lync para telefonía).</span><span class="sxs-lookup"><span data-stu-id="b7451-390">This single-valued attribute contains the device ID (either the SIP URI or the TEL URI of the phone the user controls) used by Lync for telephony.</span></span> <span data-ttu-id="b7451-391">Este atributo está marcado para la replicación del catálogo global y está indizado.</span><span class="sxs-lookup"><span data-stu-id="b7451-391">This attribute is marked for Global Catalog replication and is indexed.</span></span> <span data-ttu-id="b7451-392">Si un usuario está habilitado para Enterprise Voice, este atributo almacena la versión normalizada E. 164 del número de teléfono del usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-392">If a user is enabled for Enterprise Voice, this attribute stores the E.164 normalized version of the user’s phone number.</span></span></p></td>
<td><p><span data-ttu-id="b7451-393">Novedades de Microsoft Office Live Communications Server 2005 con SP1</span><span class="sxs-lookup"><span data-stu-id="b7451-393">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-394">msRTCSIP-LineServer</span><span class="sxs-lookup"><span data-stu-id="b7451-394">msRTCSIP-LineServer</span></span></p></td>
<td><p><span data-ttu-id="b7451-395">Este atributo de valor único contiene el URI SIP del servidor de puerta de enlace CSTA-SIP.</span><span class="sxs-lookup"><span data-stu-id="b7451-395">This single-valued attribute contains the SIP URI of the CSTA-SIP gateway server.</span></span> <span data-ttu-id="b7451-396">Este atributo está marcado para la replicación del catálogo global, pero no está indizado.</span><span class="sxs-lookup"><span data-stu-id="b7451-396">This attribute is marked for Global Catalog replication but is not indexed.</span></span></p></td>
<td><p><span data-ttu-id="b7451-397">Novedades de Microsoft Office Live Communications Server 2005 con SP1</span><span class="sxs-lookup"><span data-stu-id="b7451-397">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-398">msRTCSIP-LocalNormalizationData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-398">msRTCSIP-LocalNormalizationData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-399">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-399">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-400">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-400">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-401">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-401">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-402">msRTCSIP-LocalNormalizationLinks (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-402">msRTCSIP-LocalNormalizationLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-403">Este atributo de valor múltiple contiene una lista de nombres completos de normalización (DN) de normalización asociados con este perfil de ubicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-403">This multi-valued attribute contains a list of local normalization distinguished names (DN) associated with this location profile.</span></span> <span data-ttu-id="b7451-404">El tipo de este atributo es un binario DN.</span><span class="sxs-lookup"><span data-stu-id="b7451-404">The type of this attribute is a DN binary.</span></span> <span data-ttu-id="b7451-405">Existe una relación de uno a varios entre el perfil de ubicación y las reglas de normalización locales.</span><span class="sxs-lookup"><span data-stu-id="b7451-405">There is a one-to-many relationship between location profile and local normalization rules.</span></span> <span data-ttu-id="b7451-406">El orden de la lista de DNs de normalización local debe mantenerse en el orden especificado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="b7451-406">The ordering of the list of local normalization DNs must be maintained in the order specified by the administrator.</span></span> <span data-ttu-id="b7451-407">La conservación del pedido se mantiene mediante la parte binaria del código binario DN, que especifica el índice del pedido.</span><span class="sxs-lookup"><span data-stu-id="b7451-407">The preservation of order is maintained by the binary portion of the DN binary, which specifies the order index.</span></span></p>
<p><span data-ttu-id="b7451-408">Vínculo hacia adelante: <strong>identificador de vínculo 11034</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-408">Forward link: <strong>Link ID 11034</strong></span></span></p>
<p><span data-ttu-id="b7451-409">El vínculo atrás correspondiente a este atributo de vínculo hacia adelante es <strong>msRTCSIP-LocationProfileBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-409">The corresponding back link to this forward link attribute is <strong>msRTCSIP-LocationProfileBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-410">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-410">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-411">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-411">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-412">msRTCSIP-LocalNormalizationOptions</span><span class="sxs-lookup"><span data-stu-id="b7451-412">msRTCSIP-LocalNormalizationOptions</span></span></p></td>
<td><p><span data-ttu-id="b7451-413">Este atributo contiene una lista de opciones para la regla de normalización.</span><span class="sxs-lookup"><span data-stu-id="b7451-413">This attribute contains a list of options for the normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="b7451-414">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-414">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-415">msRTCSIP-LocationName (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-415">msRTCSIP-LocationName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-416">Este atributo de valor único contiene un nombre descriptivo para el perfil de ubicación que indica la ubicación que representa este perfil.</span><span class="sxs-lookup"><span data-stu-id="b7451-416">This single-valued attribute contains a friendly name for the location profile that indicates which location this profile represents.</span></span> <span data-ttu-id="b7451-417">Dado que puede haber varios perfiles de ubicación, el administrador necesita una forma de distinguir los distintos perfiles.</span><span class="sxs-lookup"><span data-stu-id="b7451-417">Because there can be multiple location profiles, the administrator needs a way to distinguish between different profiles.</span></span></p></td>
<td><p><span data-ttu-id="b7451-418">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-418">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-419">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-419">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-420">msRTCSIP-locationProfileBL (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-420">msRTCSIP-locationProfileBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-421">Este atributo de valor múltiple contiene una lista de nombres distintivos del perfil de ubicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-421">This multi-valued attribute contains a list of location profile distinguished names.</span></span> <span data-ttu-id="b7451-422">Este atributo especifica el vínculo de retroceso a uno o más perfiles de ubicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-422">This attribute specifies the back link to one or more location profiles.</span></span></p>
<p><span data-ttu-id="b7451-423">Vínculo anterior: <strong>identificador de vínculo 11035</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-423">Back link: <strong>Link ID 11035</strong></span></span></p>
<p><span data-ttu-id="b7451-424">Este atributo corresponde al vínculo de reenvío <strong>msRTCSIP-LocalNormalizationLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-424">This attribute corresponds to the forward link <strong>msRTCSIP-LocalNormalizationLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-425">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-425">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-426">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-426">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-427">msRTCSIP-LocationProfileData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-427">msRTCSIP-LocationProfileData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-428">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-428">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-429">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-429">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-430">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-430">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-431">msRTCSIP-LocationProfileOptions</span><span class="sxs-lookup"><span data-stu-id="b7451-431">msRTCSIP-LocationProfileOptions</span></span></p></td>
<td><p><span data-ttu-id="b7451-432">Este atributo contiene las opciones para el perfil de ubicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-432">This attribute contains the options for the location profile.</span></span></p></td>
<td><p><span data-ttu-id="b7451-433">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-433">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-434">msRTCSIP-MappingContact</span><span class="sxs-lookup"><span data-stu-id="b7451-434">msRTCSIP-MappingContact</span></span></p></td>
<td><p><span data-ttu-id="b7451-435">Este atributo de valor múltiple contiene una lista de contactos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-435">This multiple-value attribute holds a list of application contacts.</span></span></p></td>
<td><p><span data-ttu-id="b7451-436">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-436">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-437">msRTCSIP-MappingLocation</span><span class="sxs-lookup"><span data-stu-id="b7451-437">msRTCSIP-MappingLocation</span></span></p></td>
<td><p><span data-ttu-id="b7451-438">Este atributo de valor múltiple contiene una lista de perfiles de ubicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-438">This multiple-value attribute holds a list of location profiles.</span></span></p></td>
<td><p><span data-ttu-id="b7451-439">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-439">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-440">msRTCSIP-MaxNumOutstandingSearchPerServer (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-440">msRTCSIP-MaxNumOutstandingSearchPerServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-441">Este atributo representa el número máximo de solicitudes de búsqueda pendientes por servidor.</span><span class="sxs-lookup"><span data-stu-id="b7451-441">This attribute represents the maximum number of outstanding search requests per server.</span></span></p></td>
<td><p><span data-ttu-id="b7451-442">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-442">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-443">msRTCSIP-MaxNumSubscriptionsPerUser (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-443">msRTCSIP-MaxNumSubscriptionsPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-444">El atributo representa el número máximo de suscripciones por usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-444">The attribute represents the maximum number of subscriptions per user.</span></span></p></td>
<td><p><span data-ttu-id="b7451-445">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-445">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-446">msRTCSIP-MaxPresenceSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-446">msRTCSIP-MaxPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-447">Este atributo representa la ventana máximo de tiempo de espera de suscripción.</span><span class="sxs-lookup"><span data-stu-id="b7451-447">This attribute represents the maximum subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="b7451-448">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-448">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-449">msRTCSIP-MaxRegistrationsTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-449">msRTCSIP-MaxRegistrationsTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-450">Este atributo representa el límite máximo de registros de la ventana de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="b7451-450">This attribute represents the maximum registrations time-out window.</span></span></p></td>
<td><p><span data-ttu-id="b7451-451">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-451">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-453">Este atributo representa la ventana de tiempo de espera máxima de suscripciones de datos de movilidad.</span><span class="sxs-lookup"><span data-stu-id="b7451-453">This attribute represents the maximum roaming data subscriptions time-out window.</span></span></p></td>
<td><p><span data-ttu-id="b7451-454">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-454">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-455">msRTCSIP-MCUData</span><span class="sxs-lookup"><span data-stu-id="b7451-455">msRTCSIP-MCUData</span></span></p></td>
<td><p><span data-ttu-id="b7451-456">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-456">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-457">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-457">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-458">msRTCSIP-MCUFactoryAddress</span><span class="sxs-lookup"><span data-stu-id="b7451-458">msRTCSIP-MCUFactoryAddress</span></span></p></td>
<td><p><span data-ttu-id="b7451-459">Este atributo es un atributo del punto de control de servicio en la clase de equipo que especifica un vínculo a la fábrica de la unidad de control multipunto (MCU) a la que pertenece.</span><span class="sxs-lookup"><span data-stu-id="b7451-459">This attribute is a service control point attribute under the computer class that specifies a link back to the multipoint control unit (MCU) Factory to which it belongs.</span></span> <span data-ttu-id="b7451-460">Este punto de control de servicio y atributo se crea para cada MCU de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7451-460">This service control point and attribute is created for every Microsoft MCU.</span></span> <span data-ttu-id="b7451-461">Cada MCU de Microsoft debe encontrar el servidor back-end del grupo al que pertenece, a fin de recuperar la configuración de nivel de grupo.</span><span class="sxs-lookup"><span data-stu-id="b7451-461">Each Microsoft MCU must find the Back End Server of the pool to which it belongs, in order to retrieve pool-level settings from it.</span></span></p>
<p><span data-ttu-id="b7451-462">El valor de este atributo es el nombre distintivo (DN) del generador MCU.</span><span class="sxs-lookup"><span data-stu-id="b7451-462">The value of this attribute is the distinguished name (DN) of the MCU Factory.</span></span> <span data-ttu-id="b7451-463">Este es un atributo de valor único y está marcado para replicación de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="b7451-463">This is a single-valued attribute and marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="b7451-464">Vínculo hacia adelante: <strong>identificador de vínculo 11026</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-464">Forward link: <strong>Link ID 11026</strong></span></span></p>
<p><span data-ttu-id="b7451-465">El vínculo atrás correspondiente a este atributo de vínculo hacia adelante es <strong>msRTCSIP-MCUServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-465">The corresponding back link to this forward link attribute is <strong>msRTCSIP-MCUServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-466">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-466">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-467">msRTCSIP-MCUFactoryData</span><span class="sxs-lookup"><span data-stu-id="b7451-467">msRTCSIP-MCUFactoryData</span></span></p></td>
<td><p><span data-ttu-id="b7451-468">Este es un atributo reservado de cadena múltiple.</span><span class="sxs-lookup"><span data-stu-id="b7451-468">This is a multi-string reserved attribute.</span></span> <span data-ttu-id="b7451-469">La configuración almacenada en este atributo se representa como un par nombre = valor.</span><span class="sxs-lookup"><span data-stu-id="b7451-469">Settings stored in this attribute are represented as name=value pairs.</span></span> <span data-ttu-id="b7451-470">Los pares de nombre definido actualmente = valor son:</span><span class="sxs-lookup"><span data-stu-id="b7451-470">Currently defined name=value pairs are:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-471">FactoryURL = &lt; URL&gt;</span><span class="sxs-lookup"><span data-stu-id="b7451-471">FactoryURL = &lt;URL&gt;</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-472">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-472">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-473">msRTCSIP-MCUFactoryPath</span><span class="sxs-lookup"><span data-stu-id="b7451-473">msRTCSIP-MCUFactoryPath</span></span></p></td>
<td><p><span data-ttu-id="b7451-474">Este es un atributo de valor único que contiene el nombre distintivo (DN) de un solo generador MCU asociado con un grupo.</span><span class="sxs-lookup"><span data-stu-id="b7451-474">This is a single-valued attribute that contains the distinguished name (DN) of a single MCU factory associated with a pool.</span></span></p>
<p><span data-ttu-id="b7451-475">Vínculo hacia adelante: <strong>identificador de vínculo 11024</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-475">Forward link: <strong>Link ID 11024</strong></span></span></p>
<p><span data-ttu-id="b7451-476">El vínculo atrás correspondiente a este atributo de vínculo hacia adelante es <strong>msRTCSIP-PoolAddresses</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-476">The corresponding back link to this forward link attribute is <strong>msRTCSIP-PoolAddresses</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-477">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-477">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-478">msRTCSIP-MCUFactoryProviderID</span><span class="sxs-lookup"><span data-stu-id="b7451-478">msRTCSIP-MCUFactoryProviderID</span></span></p></td>
<td><p><span data-ttu-id="b7451-479">Este atributo es una cadena de valor único que especifica el GUID del proveedor de factoría MCU.</span><span class="sxs-lookup"><span data-stu-id="b7451-479">This attribute is a single-valued string that specifies the GUID of the MCU factory provider.</span></span> <span data-ttu-id="b7451-480">Según el valor de GUID, el proceso de fábrica de MCU determina si se debe atender a este tipo de MCU.</span><span class="sxs-lookup"><span data-stu-id="b7451-480">Based on the GUID value, the MCU factory process determines whether to service this MCU type.</span></span> <span data-ttu-id="b7451-481">Si el valor de GUID es <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>, el proceso de fábrica de MCU (disponible de forma predeterminada en Lync Server) lo procesará.</span><span class="sxs-lookup"><span data-stu-id="b7451-481">If the GUID value is <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>, then the MCU factory process (available by default in Lync Server) will process it.</span></span> <span data-ttu-id="b7451-482">Para cualquier otro valor de GUID, el proceso de fábrica de MCU no procesará el tipo de MCU.</span><span class="sxs-lookup"><span data-stu-id="b7451-482">For any other GUID value, the MCU factory process will not service the MCU type.</span></span></p></td>
<td><p><span data-ttu-id="b7451-483">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-483">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-484">msRTCSIP-MCUServers</span><span class="sxs-lookup"><span data-stu-id="b7451-484">msRTCSIP-MCUServers</span></span></p></td>
<td><p><span data-ttu-id="b7451-485">Este atributo es una lista con varios valores de nombres completos (DN).</span><span class="sxs-lookup"><span data-stu-id="b7451-485">This attribute is a multi-valued list of distinguished names (DN).</span></span> <span data-ttu-id="b7451-486">Este atributo contiene una lista de todos los servidores MCU del mismo tipo y proveedor asociados a este generador MCU.</span><span class="sxs-lookup"><span data-stu-id="b7451-486">This attribute contains a list of all MCU servers of the same type and vendor associated with this MCU factory.</span></span> <span data-ttu-id="b7451-487">El valor válido para cada segmento es de 63 caracteres; el valor válido para todo el FQDN es 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b7451-487">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p>
<p><span data-ttu-id="b7451-488">Vínculo anterior: identificador de vínculo 11027</span><span class="sxs-lookup"><span data-stu-id="b7451-488">Back link: Link ID 11027</span></span></p>
<p><span data-ttu-id="b7451-489">El vínculo de reenvío correspondiente a este vínculo anterior es <strong>msRTCSIP-MCUFactoryAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-489">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-490">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-490">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-491">msRTCSIP-MCUType</span><span class="sxs-lookup"><span data-stu-id="b7451-491">msRTCSIP-MCUType</span></span></p></td>
<td><p><span data-ttu-id="b7451-492">Este atributo es una cadena de valor único que especifica el medio que el MCU puede controlar.</span><span class="sxs-lookup"><span data-stu-id="b7451-492">This attribute is a single-valued string that specifies the medium the MCU can handle.</span></span></p>
<p><span data-ttu-id="b7451-493">Los tipos válidos compatibles son:</span><span class="sxs-lookup"><span data-stu-id="b7451-493">Supported valid types are:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-494">satisfacción</span><span class="sxs-lookup"><span data-stu-id="b7451-494">meeting</span></span></p></li>
<li><p><span data-ttu-id="b7451-495">audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="b7451-495">audio-video</span></span></p></li>
<li><p><span data-ttu-id="b7451-496">Chatea</span><span class="sxs-lookup"><span data-stu-id="b7451-496">chat</span></span></p></li>
<li><p><span data-ttu-id="b7451-497">conf. teléfono</span><span class="sxs-lookup"><span data-stu-id="b7451-497">phone-conf</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-498">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-498">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-499">msRTCSIP-MCUVendor</span><span class="sxs-lookup"><span data-stu-id="b7451-499">msRTCSIP-MCUVendor</span></span></p></td>
<td><p><span data-ttu-id="b7451-500">Este atributo es una cadena de valor único que especifica el nombre de un proveedor de la MCU.</span><span class="sxs-lookup"><span data-stu-id="b7451-500">This attribute is a single-valued string that specifies an MCU vendor’s name.</span></span> <span data-ttu-id="b7451-501">Todos los MCU de Microsoft especificarán que este atributo sea <strong>Microsoft Corporation</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-501">All Microsoft MCUs will specify this attribute to be <strong>Microsoft Corporation</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-502">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-502">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-503">msRTCSIP-MeetingFlags (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-503">msRTCSIP-MeetingFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-504">Este atributo define diferentes opciones de reunión que se habilitan globalmente para todos los usuarios o los objetos de contacto.</span><span class="sxs-lookup"><span data-stu-id="b7451-504">This attribute defines different meeting options that are enabled globally for all users or contact objects.</span></span> <span data-ttu-id="b7451-505">Este atributo es un valor de máscara de bits de tipo entero.</span><span class="sxs-lookup"><span data-stu-id="b7451-505">This attribute is a bit-mask value of integer type.</span></span></p>
<p><span data-ttu-id="b7451-506">Los valores válidos (y las posiciones de bits asociadas) son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-506">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-507">0: AllowOrganizeMeetingWithAnonymousParticipants es None (no permite que los usuarios inviten a usuarios anónimos a reuniones) (sin ningún bit)</span><span class="sxs-lookup"><span data-stu-id="b7451-507">0: AllowOrganizeMeetingWithAnonymousParticipants is None (do not allow users to invite anonymous users to meetings) (no bits set)</span></span></p></li>
<li><p><span data-ttu-id="b7451-508">4: AllowOrganizeMeetingWithAnonymousParticipants es todos (permitir que todos los usuarios inviten a usuarios anónimos a reuniones) (posición de bit 2)</span><span class="sxs-lookup"><span data-stu-id="b7451-508">4: AllowOrganizeMeetingWithAnonymousParticipants is Everyone (allow all users to invite anonymous users to meetings) (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="b7451-509">8: AllowOrganizeMeetingWithAnonymousParticipants es UsePerUserSetting (permitir a los usuarios invitar a usuarios anónimos a reuniones según la configuración por usuario) (posición de bit 3)</span><span class="sxs-lookup"><span data-stu-id="b7451-509">8: AllowOrganizeMeetingWithAnonymousParticipants is UsePerUserSetting (allow users to invite anonymous users to meetings based on per user setting) (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="b7451-510">16: UserPerUserMeetingPolicy (se define la Directiva de reunión por usuario) (posición de bit 4)</span><span class="sxs-lookup"><span data-stu-id="b7451-510">16: UserPerUserMeetingPolicy (meeting policy is defined per user) (bit position 4)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-511">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-511">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-512">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-512">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-513">msRTCSIP-MeetingPolicy (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-513">msRTCSIP-MeetingPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-514">Este atributo especifica el nombre completo (DN) de la Directiva que el administrador ha asignado a este usuario como un atributo de valor único.</span><span class="sxs-lookup"><span data-stu-id="b7451-514">This attribute specifies the distinguished name (DN) of the policy the administrator has assigned for this user as a single-valued attribute.</span></span></p></td>
<td><p><span data-ttu-id="b7451-515">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-515">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-516">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-516">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-517">msRTCSIP-MinPresenceSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-517">msRTCSIP-MinPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-518">Este atributo representa la ventana de tiempo de espera de suscripción de presencia mínima.</span><span class="sxs-lookup"><span data-stu-id="b7451-518">This attribute represents the minimum presence subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="b7451-519">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-519">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-520">msRTCSIP-MinRegistrationTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-520">msRTCSIP-MinRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-521">Este atributo representa la ventana de tiempo de espera de registro mínimo.</span><span class="sxs-lookup"><span data-stu-id="b7451-521">This attribute represents the minimum registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="b7451-522">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-522">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-523">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-523">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-525">Este atributo representa la ventana de tiempo de espera de la suscripción de datos de itinerancia mínima.</span><span class="sxs-lookup"><span data-stu-id="b7451-525">This attribute represents the minimum roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="b7451-526">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-526">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-527">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-527">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-528">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="b7451-528">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="b7451-529">Este atributo se usa para almacenar el back-end de SQL Server reflejado usado por el grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="b7451-529">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
<td><p><span data-ttu-id="b7451-530">Novedades de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b7451-530">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-531">msRTCSIP-MobilityFlags</span><span class="sxs-lookup"><span data-stu-id="b7451-531">msRTCSIP-MobilityFlags</span></span></p></td>
<td><p><span data-ttu-id="b7451-532">Este atributo contiene opciones e indicadores que definen la configuración de movilidad.</span><span class="sxs-lookup"><span data-stu-id="b7451-532">This attribute contains options and flags that define mobility settings.</span></span></p></td>
<td><p><span data-ttu-id="b7451-533">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-533">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-534">msRTCSIP-MobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b7451-534">msRTCSIP-MobilityPolicy</span></span></p></td>
<td><p><span data-ttu-id="b7451-535">Este atributo contiene el DN de un objeto de directiva de movilidad.</span><span class="sxs-lookup"><span data-stu-id="b7451-535">This attribute contains the DN for a mobility policy object.</span></span></p></td>
<td><p><span data-ttu-id="b7451-536">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-536">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-537">msRTCSIP-NumDevicesPerUser (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-537">msRTCSIP-NumDevicesPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-538">Este atributo representa la cantidad permitida de dispositivos en los que un usuario puede registrarse para comunicaciones SIP y suscribirse a la presencia.</span><span class="sxs-lookup"><span data-stu-id="b7451-538">This attribute represents the allowed number of devices on which a user can register for SIP communications and subscribe to presence.</span></span></p></td>
<td><p><span data-ttu-id="b7451-539">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-539">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-540">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-540">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-541">msRTCSIP-OptionFlags</span><span class="sxs-lookup"><span data-stu-id="b7451-541">msRTCSIP-OptionFlags</span></span></p></td>
<td><p><span data-ttu-id="b7451-542">Este atributo especifica las opciones que están habilitadas para el objeto de usuario o contacto.</span><span class="sxs-lookup"><span data-stu-id="b7451-542">This attribute specifies the options that are enabled for the user or contact object.</span></span> <span data-ttu-id="b7451-543">Este atributo es un valor de máscara de bits de tipo entero.</span><span class="sxs-lookup"><span data-stu-id="b7451-543">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="b7451-544">Cada opción está representada por un bit.</span><span class="sxs-lookup"><span data-stu-id="b7451-544">Each option is represented by a bit.</span></span> <span data-ttu-id="b7451-545">Este atributo se marca para la replicación del catálogo global.</span><span class="sxs-lookup"><span data-stu-id="b7451-545">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="b7451-546">Los valores válidos (y las posiciones de bits asociadas) son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-546">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-547">1: habilitado para conectividad de mensajería instantánea (mi) pública (posición de bit 0)</span><span class="sxs-lookup"><span data-stu-id="b7451-547">1: Enabled for public instant messaging (IM) connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="b7451-548">2: reservado (posición de bit 1)</span><span class="sxs-lookup"><span data-stu-id="b7451-548">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="b7451-549">4: reservado (posición de bit 2)</span><span class="sxs-lookup"><span data-stu-id="b7451-549">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="b7451-550">8: reservado (posición de bit 3)</span><span class="sxs-lookup"><span data-stu-id="b7451-550">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="b7451-551">16: control remoto de llamadas habilitado [telefonía] (posición de bit 4)</span><span class="sxs-lookup"><span data-stu-id="b7451-551">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="b7451-552">64: AllowOrganizeMeetingWithAnonymousParticipants (permitir a los usuarios invitar a usuarios anónimos a reuniones (bit 6)</span><span class="sxs-lookup"><span data-stu-id="b7451-552">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="b7451-553">128: UCEnabled (habilitar usuarios para UC) (posición de bit 7)</span><span class="sxs-lookup"><span data-stu-id="b7451-553">128: UCEnabled (enable users for UC) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="b7451-554">256: EnabledForEnhancedPresence (habilitar usuario para conectividad de mensajería instantánea pública) (posición de bit 8)</span><span class="sxs-lookup"><span data-stu-id="b7451-554">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="b7451-555">512: RemoteCallControlDualMode (posición de bit 9)</span><span class="sxs-lookup"><span data-stu-id="b7451-555">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-556">Novedades de Live Communications Server 2005 con SP1.</span><span class="sxs-lookup"><span data-stu-id="b7451-556">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-557">msRTCSIP-OriginatorSID</span><span class="sxs-lookup"><span data-stu-id="b7451-557">msRTCSIP-OriginatorSID</span></span></p></td>
<td><p><span data-ttu-id="b7451-558">Este atributo se usa en las topologías de bosque de recursos y central para habilitar el inicio de sesión único cuando el ObjectSID de un usuario de la cuenta principal de Windows NT Server se copia en este atributo del objeto de usuario o contacto correspondiente del recurso o del bosque central.</span><span class="sxs-lookup"><span data-stu-id="b7451-558">This attribute is used in resource and central forest topologies to enable single sign-on when a user’s ObjectSID from the Windows NT Server principal account is copied into this attribute of the corresponding user or contact object in the resource or central forest.</span></span> <span data-ttu-id="b7451-559">Communicator Web Access busca un usuario en AD DS con este atributo o el ObjectSID del usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-559">Communicator Web Access searches for a user in AD DS using this attribute or the user’s ObjectSID.</span></span> <span data-ttu-id="b7451-560">Este atributo se marca para la replicación del catálogo global.</span><span class="sxs-lookup"><span data-stu-id="b7451-560">This attribute is marked for global catalog replication.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-561">msRTCSIP-OwnerUrn</span><span class="sxs-lookup"><span data-stu-id="b7451-561">msRTCSIP-OwnerUrn</span></span></p></td>
<td><p><span data-ttu-id="b7451-562">Este atributo es el nombre de recursos uniforme (URN) del propietario de un contacto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-562">This attribute is the Uniform Resource Name (URN) of the owner for an application contact.</span></span></p></td>
<td><p><span data-ttu-id="b7451-563">Novedades de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-563">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-564">msRTCSIP-Pattern (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-564">msRTCSIP-Pattern (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-565">Este atributo de cadena de valor único contiene un patrón usado para hacer coincidir números de marcado con el formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="b7451-565">This single-valued string attribute contains a pattern used for matching dial numbers into E.164 format.</span></span> <span data-ttu-id="b7451-566">Si el número de marcado coincide con este patrón, la traducción se aplica al número marcado.</span><span class="sxs-lookup"><span data-stu-id="b7451-566">If the dial number matches this pattern, the translation is applied to the dialed number.</span></span></p></td>
<td><p><span data-ttu-id="b7451-567">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-567">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-568">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-568">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-569">msRTCSIP-PhoneRouteBL (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-569">msRTCSIP-PhoneRouteBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-570">Este atributo de valor múltiple contiene una lista de nombres distintivos de rutas de teléfono (DN).</span><span class="sxs-lookup"><span data-stu-id="b7451-570">This multi-valued attribute contains a list of phone route distinguished names (DN).</span></span> <span data-ttu-id="b7451-571">Este atributo especifica el vínculo de retroceso a una o más rutas de teléfono.</span><span class="sxs-lookup"><span data-stu-id="b7451-571">This attribute specifies the back link to one or more phone routes.</span></span></p>
<p><span data-ttu-id="b7451-572">Vínculo anterior: <strong>identificador de vínculo 11033</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-572">Back link: <strong>Link ID 11033</strong></span></span></p>
<p><span data-ttu-id="b7451-573">Este atributo corresponde al vínculo de reenvío <strong>msRTCSIP-RouteUsageLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-573">This attribute corresponds to the forward link <strong>msRTCSIP-RouteUsageLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-574">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-574">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-575">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-575">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-576">msRTCSIP-PhoneRouteData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-576">msRTCSIP-PhoneRouteData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-577">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-577">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-578">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-578">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-579">msRTCSIP-PhoneRouteName (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-579">msRTCSIP-PhoneRouteName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-580">Este atributo de cadena Unicode de valor único especifica el nombre descriptivo de la ruta telefónica, de modo que el administrador puede hacer referencia a ella fácilmente.</span><span class="sxs-lookup"><span data-stu-id="b7451-580">This single valued UNICODE string attribute specifies the friendly name of the phone route, so it can easily be referenced by the administrator.</span></span></p></td>
<td><p><span data-ttu-id="b7451-581">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-581">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-582">msRTCSIP-PhoneUsageData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-582">msRTCSIP-PhoneUsageData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-583">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-583">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-584">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-584">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-585">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-585">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-586">msRTCSIP-PolicyContent (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-586">msRTCSIP-PolicyContent (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-587">Este atributo es una cadena Unicode de valor único.</span><span class="sxs-lookup"><span data-stu-id="b7451-587">This attribute is a single-valued Unicode string.</span></span> <span data-ttu-id="b7451-588">Este atributo de cadena contiene la definición de directiva en formato XML.</span><span class="sxs-lookup"><span data-stu-id="b7451-588">This string attribute contains the policy definition in XML format.</span></span> <span data-ttu-id="b7451-589">La definición del esquema XML es común en los distintos tipos de Directiva, solo la configuración es distinta para cada tipo de directiva.</span><span class="sxs-lookup"><span data-stu-id="b7451-589">The XML schema definition is common across different policy types, only the settings are different for each policy type.</span></span></p>
<p><span data-ttu-id="b7451-590">La definición de esquema XML (XSD) se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b7451-590">The XML schema definition (XSD) is defined as follows:</span></span></p>
<pre><code>&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
&lt;xs:schema id=&quot;instance&quot; xmlns=&quot;&quot; xmlns:xs=&quot;http://www.w3.org/2001/XMLSchema&quot; xmlns:msdata=&quot;urn:schemas-microsoft-com:xml-msdata&quot;&gt;
  &lt;xs:element name=&quot;instance&quot; msdata:IsDataSet=&quot;true&quot;&gt;
    &lt;xs:complexType&gt;
      &lt;xs:choice maxOccurs=&quot;unbounded&quot;&gt;
        &lt;xs:element name=&quot;property&quot; nillable=&quot;true&quot;&gt;
          &lt;xs:complexType&gt;
            &lt;xs:simpleContent msdata:ColumnName=&quot;property_Text&quot; msdata:Ordinal=&quot;1&quot;&gt;
              &lt;xs:extension base=&quot;xs:string&quot;&gt;
                &lt;xs:attribute name=&quot;name&quot; type=&quot;xs:string&quot; /&gt;
              &lt;/xs:extension&gt;
            &lt;/xs:simpleContent&gt;
          &lt;/xs:complexType&gt;
        &lt;/xs:element&gt;
      &lt;/xs:choice&gt;
    &lt;/xs:complexType&gt;
  &lt;/xs:element&gt;
&lt;/xs:schema&gt;</code></pre></td>
<td><p><span data-ttu-id="b7451-591">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-591">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-592">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-592">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-593">msRTCSIP-PolicyData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-593">msRTCSIP-PolicyData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-594">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-594">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-595">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-595">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-596">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-596">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-597">msRTCSIP-PolicyType (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-597">msRTCSIP-PolicyType (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-598">Este atributo de cadena Unicode de valor único contiene el tipo de directiva.</span><span class="sxs-lookup"><span data-stu-id="b7451-598">This single-valued Unicode string attribute contains the policy type.</span></span> <span data-ttu-id="b7451-599">Los tipos de directiva válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-599">Valid policy types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-600">satisfacción</span><span class="sxs-lookup"><span data-stu-id="b7451-600">meeting</span></span></p></li>
<li><p><span data-ttu-id="b7451-601">telefonía</span><span class="sxs-lookup"><span data-stu-id="b7451-601">telephony</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-602">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-602">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-603">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-603">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-604">msRTCSIP-PoolAddress</span><span class="sxs-lookup"><span data-stu-id="b7451-604">msRTCSIP-PoolAddress</span></span></p></td>
<td><p><span data-ttu-id="b7451-605">Este atributo especifica un vínculo al grupo al que pertenece el equipo.</span><span class="sxs-lookup"><span data-stu-id="b7451-605">This attribute specifies a link back to the pool to which a computer belongs.</span></span> <span data-ttu-id="b7451-606">Este atributo se establece independientemente de si el equipo está ejecutando la versión Standard Edition o la versión Enterprise de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b7451-606">This attribute is set regardless of whether the computer is running the Standard Edition or the Enterprise Edition of Lync Server.</span></span> <span data-ttu-id="b7451-607">Este atributo se marca para la replicación del catálogo global.</span><span class="sxs-lookup"><span data-stu-id="b7451-607">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="b7451-608">El valor válido es el nombre de dominio del grupo.</span><span class="sxs-lookup"><span data-stu-id="b7451-608">The valid value is the domain name of the pool.</span></span></p>
<p><span data-ttu-id="b7451-609">Vínculo hacia adelante: <strong>identificador de vínculo 11022</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-609">Forward link: <strong>Link ID 11022</strong></span></span></p>
<p><span data-ttu-id="b7451-610">El vínculo atrás correspondiente a este atributo de vínculo hacia adelante es <strong>msRTCSIP-FrontEndServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-610">The corresponding back link to this forward link attribute is <strong>msRTCSIP-FrontEndServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-611">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-611">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-612">msRTCSIP-PoolAddresses</span><span class="sxs-lookup"><span data-stu-id="b7451-612">msRTCSIP-PoolAddresses</span></span></p></td>
<td><p><span data-ttu-id="b7451-613">Se trata de un atributo de valor múltiple que contiene una lista de los nombres completos (DN) de los grupos a los que está asociada la fábrica del MCU.</span><span class="sxs-lookup"><span data-stu-id="b7451-613">This is a multi-valued attribute that contains a list of the distinguished names (DN) of pools with which the MCU factory is associated.</span></span></p>
<p><span data-ttu-id="b7451-614">Vínculo anterior: <strong>identificador de vínculo 11025</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-614">Back link: <strong>Link ID 11025</strong></span></span></p>
<p><span data-ttu-id="b7451-615">El vínculo de reenvío correspondiente a este vínculo anterior es <strong>msRTCSIP-MCUFactoryPath</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-615">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryPath</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-616">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-616">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-617">msRTCSIP-PoolData</span><span class="sxs-lookup"><span data-stu-id="b7451-617">msRTCSIP-PoolData</span></span></p></td>
<td><p><span data-ttu-id="b7451-618">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-618">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-619">Novedades de Live Communications Server 2005 con SP1.</span><span class="sxs-lookup"><span data-stu-id="b7451-619">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-620">msRTCSIP-PoolDisplayName</span><span class="sxs-lookup"><span data-stu-id="b7451-620">msRTCSIP-PoolDisplayName</span></span></p></td>
<td><p><span data-ttu-id="b7451-621">Este atributo especifica un nombre arbitrario para un grupo que se muestra en la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="b7451-621">This attribute specifies an arbitrary name for a pool that is displayed by the management console.</span></span> <span data-ttu-id="b7451-622">El administrador puede cambiar este nombre.</span><span class="sxs-lookup"><span data-stu-id="b7451-622">This name can be changed by the administrator.</span></span></p>
<p><span data-ttu-id="b7451-623">El valor válido es una cadena que representa el nombre de un grupo.</span><span class="sxs-lookup"><span data-stu-id="b7451-623">The valid value is a string representing the name of a pool.</span></span></p></td>
<td><p><span data-ttu-id="b7451-624">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-624">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-625">msRTCSIP-PoolDomainFQDN</span><span class="sxs-lookup"><span data-stu-id="b7451-625">msRTCSIP-PoolDomainFQDN</span></span></p></td>
<td><p><span data-ttu-id="b7451-626">Este atributo es un valor de cadena de valor único.</span><span class="sxs-lookup"><span data-stu-id="b7451-626">This attribute is a single-valued string value.</span></span> <span data-ttu-id="b7451-627">El valor de este atributo, cuando está presente, representa el FQDN de dominio de la agrupación si el administrador desea crear un grupo front-end con un FQDN que no se ajuste a la estructura de dominios de Active Directory en la que se crea el grupo front-end (por ejemplo, un espacio de nombres SIP separado del espacio de nombres del sistema de nombres de dominio (DNS)).</span><span class="sxs-lookup"><span data-stu-id="b7451-627">The value of this attribute, when present, represents the pool’s domain FQDN if the administrator wants to create a Front End pool with an FQDN that does not conform to the Active Directory domain structure in which the Front End pool is created (for example, a SIP namespace disjoined from Domain Name System (DNS) namespace).</span></span></p>
<p><span data-ttu-id="b7451-628">Le recomendamos que asigne el FQDN del dominio del grupo de servidores front-end a la parte de nombre de dominio como el dominio de Active Directory en el que se encuentra el grupo.</span><span class="sxs-lookup"><span data-stu-id="b7451-628">We recommend that you map the Front End pool domain FQDN to the domain name portion as the Active Directory domain in which the pool resides.</span></span> <span data-ttu-id="b7451-629">Por lo tanto, cuando no hay ningún valor en este atributo, el FQDN del grupo de servidores front-end se establece de forma predeterminada en la estructura de nombres de dominio de Active Directory, como indica el atributo <strong>DnsHostName</strong> .</span><span class="sxs-lookup"><span data-stu-id="b7451-629">Therefore, when no value is present in this attribute, the Front End pool FQDN will default to the Active Directory domain name structure, as denoted by the <strong>dnsHostName</strong> attribute.</span></span></p></td>
<td><p><span data-ttu-id="b7451-630">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-630">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-631">msRTCSIP-PoolFunctionality</span><span class="sxs-lookup"><span data-stu-id="b7451-631">msRTCSIP-PoolFunctionality</span></span></p></td>
<td><p><span data-ttu-id="b7451-632">Lista con varios valores de los nombres de dominio de todos los servidores de Lync Server, Enterprise Edition asociados a un grupo.</span><span class="sxs-lookup"><span data-stu-id="b7451-632">A multi-valued list of the domain names of all Lync Server, Enterprise Edition servers associated with a pool.</span></span> <span data-ttu-id="b7451-633">Este atributo de tipo entero define si el grupo es capaz de la mensajería instantánea (mi), la presencia y las reuniones.</span><span class="sxs-lookup"><span data-stu-id="b7451-633">This attribute of type integer defines whether the pool is capable of instant messaging (IM) and presence, and meetings.</span></span></p>
<p><span data-ttu-id="b7451-634">Los posibles tipos de valor válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-634">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-635">Undefined: mensajería instantánea y servicio de presencia (Live Communications Server 2005 y 2003)</span><span class="sxs-lookup"><span data-stu-id="b7451-635">Undefined: IM and Presence Service (Live Communications Server 2005 and 2003)</span></span></p></li>
<li><p><span data-ttu-id="b7451-636">1: mensajería instantánea y servicio de presencia (Lync Server)</span><span class="sxs-lookup"><span data-stu-id="b7451-636">1: IM and Presence Service (Lync Server)</span></span></p></li>
<li><p><span data-ttu-id="b7451-637">2: mensajería instantánea y presencia y servicio de reuniones (Lync Server)</span><span class="sxs-lookup"><span data-stu-id="b7451-637">2: IM and Presence and Meeting Service (Lync Server)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-638">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-638">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-639">msRTCSIP-PoolType</span><span class="sxs-lookup"><span data-stu-id="b7451-639">msRTCSIP-PoolType</span></span></p></td>
<td><p><span data-ttu-id="b7451-640">Este atributo especifica si un grupo de servidores ejecuta un servidor Standard Edition o Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="b7451-640">This attribute specifies whether a server pool is running Standard Edition server or Enterprise Edition server.</span></span> <span data-ttu-id="b7451-641">Este atributo es un valor de máscara de bits de tipo entero.</span><span class="sxs-lookup"><span data-stu-id="b7451-641">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="b7451-642">Cada opción está representada por un bit.</span><span class="sxs-lookup"><span data-stu-id="b7451-642">Each option is represented by a bit.</span></span></p>
<p><span data-ttu-id="b7451-643">Los valores válidos (y las posiciones de bits asociadas) son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-643">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-644">1: servidor Standard Edition, usuarios de hosts (posición de bit 0)</span><span class="sxs-lookup"><span data-stu-id="b7451-644">1: Standard Edition server, hosts users (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="b7451-645">2: servidor Enterprise Edition, usuarios de hosts (posición de bit 1)</span><span class="sxs-lookup"><span data-stu-id="b7451-645">2: Enterprise Edition server, hosts users (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="b7451-646">4: servidor Standard Edition, aplicaciones de hosts (posición de bit 2)</span><span class="sxs-lookup"><span data-stu-id="b7451-646">4: Standard Edition server, hosts applications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="b7451-647">8: servidor Enterprise Edition, aplicaciones para hosts (posición de bit 3)</span><span class="sxs-lookup"><span data-stu-id="b7451-647">8: Enterprise Edition server, hosts applications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="b7451-648">Puesto que Lync Server no es compatible con los grupos que hospedan solo aplicaciones, los únicos valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-648">Because Lync Server does not support pools that host only applications, the only valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-649">5: servidor Standard Edition, hospeda usuarios y aplicaciones (posiciones de bits 0 y 2)</span><span class="sxs-lookup"><span data-stu-id="b7451-649">5: Standard Edition server, hosts users and applications (bit positions 0 and 2)</span></span></p></li>
<li><p><span data-ttu-id="b7451-650">10: servidor Enterprise Edition, hospeda usuarios y aplicaciones (posiciones de bits 1 y 3)</span><span class="sxs-lookup"><span data-stu-id="b7451-650">10: Enterprise Edition server, hosts users and applications (bit positions 1 and 3)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-651">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-651">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-652">msRTCSIP-PoolVersion</span><span class="sxs-lookup"><span data-stu-id="b7451-652">msRTCSIP-PoolVersion</span></span></p></td>
<td><p><span data-ttu-id="b7451-653">Este atributo define la versión del grupo.</span><span class="sxs-lookup"><span data-stu-id="b7451-653">This attribute defines the pool version.</span></span> <span data-ttu-id="b7451-654">Es un tipo entero que se incrementa con cada lanzamiento de producto principal.</span><span class="sxs-lookup"><span data-stu-id="b7451-654">It is an integer type that is incremented with each major product release.</span></span></p>
<p><span data-ttu-id="b7451-655">Los posibles tipos de valor válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-655">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-656">0: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7451-656">0: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="b7451-657">1: Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="b7451-657">1: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="b7451-658">2: Live Communications Server 2005 con SP1</span><span class="sxs-lookup"><span data-stu-id="b7451-658">2: Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="b7451-659">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="b7451-659">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="b7451-660">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="b7451-660">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="b7451-661">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="b7451-661">5: Lync Server 2010</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-662">Live Communications Server 2005 con SP1.</span><span class="sxs-lookup"><span data-stu-id="b7451-662">Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-663">msRTCSIP-PresenceFlags</span><span class="sxs-lookup"><span data-stu-id="b7451-663">msRTCSIP-PresenceFlags</span></span></p></td>
<td><p><span data-ttu-id="b7451-664">Este atributo contiene opciones e indicadores que definen la configuración de presencia.</span><span class="sxs-lookup"><span data-stu-id="b7451-664">This attribute contains options and flags that define presence settings.</span></span></p></td>
<td><p><span data-ttu-id="b7451-665">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-665">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-666">msRTCSIP-PresencePolicy</span><span class="sxs-lookup"><span data-stu-id="b7451-666">msRTCSIP-PresencePolicy</span></span></p></td>
<td><p><span data-ttu-id="b7451-667">Este atributo contiene el DN de un objeto de directiva de presencia.</span><span class="sxs-lookup"><span data-stu-id="b7451-667">This attribute contains the DN for a presence policy object.</span></span></p></td>
<td><p><span data-ttu-id="b7451-668">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-668">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-669">msRTCSIP-PrimaryHomeServer</span><span class="sxs-lookup"><span data-stu-id="b7451-669">msRTCSIP-PrimaryHomeServer</span></span></p></td>
<td><p><span data-ttu-id="b7451-670">Este atributo habilita a un usuario o contacto para mensajería SIP.</span><span class="sxs-lookup"><span data-stu-id="b7451-670">This attribute enables a user or contact for SIP messaging.</span></span> <span data-ttu-id="b7451-671">Se agrega a la clase de contacto porque en la topología del bosque central, los objetos de contacto, no los objetos de usuario, están habilitados para SIP.</span><span class="sxs-lookup"><span data-stu-id="b7451-671">It is added to the contact class because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="b7451-672">El valor válido es el nombre completo del servidor Standard Edition o del grupo front-end de Enterprise Edition en el que se aloja un usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-672">The valid value is the DN of the Standard Edition server or Enterprise Edition Front End pool where a user is homed.</span></span></p></td>
<td><p><span data-ttu-id="b7451-673">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-673">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-674">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="b7451-674">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="b7451-675">Este atributo contiene la dirección SIP de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="b7451-675">This attribute contains the SIP address of a given user.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-676">msRTCSIP-PrivateLine</span><span class="sxs-lookup"><span data-stu-id="b7451-676">msRTCSIP-PrivateLine</span></span></p></td>
<td><p><span data-ttu-id="b7451-677">Este atributo contiene el identificador del dispositivo de línea privada.</span><span class="sxs-lookup"><span data-stu-id="b7451-677">This attribute contains the device ID of the private line device.</span></span></p></td>
<td><p><span data-ttu-id="b7451-678">Novedades de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-678">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-679">msRTCSIP-enrutable</span><span class="sxs-lookup"><span data-stu-id="b7451-679">msRTCSIP-Routable</span></span></p></td>
<td><p><span data-ttu-id="b7451-680">Este atributo es un atributo booleano que se usa para determinar si Lync Server está autorizado a enrutar a este servicio mediante su dirección GRUU.</span><span class="sxs-lookup"><span data-stu-id="b7451-680">This attribute is a Boolean attribute used to determine whether Lync Server is authorized to route to this service using its GRUU address.</span></span> <span data-ttu-id="b7451-681">Si este valor se establece en <strong>true</strong>, Lync Server está autorizado para enrutar a este servicio.</span><span class="sxs-lookup"><span data-stu-id="b7451-681">If this value is set to <strong>TRUE</strong>, Lync Server is authorized to route to this service.</span></span> <span data-ttu-id="b7451-682">Si este valor se establece en <strong>false</strong>, Lync Server no está autorizado a enrutar a este servicio.</span><span class="sxs-lookup"><span data-stu-id="b7451-682">If this value is set to <strong>FALSE</strong>, Lync Server is not authorized to route to this service.</span></span></p></td>
<td><p><span data-ttu-id="b7451-683">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-683">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-684">msRTCSIP-RouteUsageAttribute (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-684">msRTCSIP-RouteUsageAttribute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-685">Este atributo de cadena Unicode de valor único define un atributo que califica el uso de una ruta de teléfono.</span><span class="sxs-lookup"><span data-stu-id="b7451-685">This single-valued UNICODE string attribute defines an attribute that qualifies the usage for a phone route.</span></span> <span data-ttu-id="b7451-686">La selección de una ruta telefónica se determina en función de dos elementos: el atributo de uso asignado a la ruta telefónica y los atributos de uso de directivas permitidos por la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b7451-686">Selection of a phone route is determined based on two elements: the usage attribute assigned to the phone route and the caller’s allowed policy usage attributes.</span></span> <span data-ttu-id="b7451-687">Se selecciona la primera ruta del teléfono con un atributo de uso que coincida con el uso permitido de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b7451-687">The first phone route with a usage attribute that matches the caller’s allowed usage is selected.</span></span></p></td>
<td><p><span data-ttu-id="b7451-688">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-688">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-689">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-689">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-690">msRTCSIP-RouteUsageLinks (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-690">msRTCSIP-RouteUsageLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-691">Este atributo de nombre distintivo (DN) multivalor contiene una lista de nombres completos de uso de ruta.</span><span class="sxs-lookup"><span data-stu-id="b7451-691">This multi-valued distinguished name (DN) attribute contains a list of route usage distinguished names.</span></span></p>
<p><span data-ttu-id="b7451-692">Vínculo hacia adelante: <strong>identificador de vínculo 11032</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-692">Forward link: <strong>Link ID 11032</strong></span></span></p>
<p><span data-ttu-id="b7451-693">Este atributo es un vínculo hacia adelante al vínculo atrás correspondiente <strong>msRTCSIP-PhoneRouteBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-693">This attribute is a forward link to the corresponding back link <strong>msRTCSIP-PhoneRouteBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-694">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-694">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-695">msRTCSIP-RoutingPoolDN</span><span class="sxs-lookup"><span data-stu-id="b7451-695">msRTCSIP-RoutingPoolDN</span></span></p></td>
<td><p><span data-ttu-id="b7451-696">Este atributo contiene el DN que apunta al grupo al que debe pasar todo el tráfico SIP dirigido a este servicio MCU o de confianza.</span><span class="sxs-lookup"><span data-stu-id="b7451-696">This attribute contains the DN that points to the pool that all SIP traffic addressed to this MCU or Trusted Service must go through.</span></span></p></td>
<td><p><span data-ttu-id="b7451-697">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-697">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-698">msRTCSIP-RuleName (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-698">msRTCSIP-RuleName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-699">Este atributo de cadena Unicode de valor único especifica el nombre descriptivo de la regla de normalización, de modo que un administrador puede hacer referencia a ella fácilmente.</span><span class="sxs-lookup"><span data-stu-id="b7451-699">This single-valued UNICODE string attribute specifies the friendly name of the normalization rule, so it can easily be referenced by an administrator.</span></span></p></td>
<td><p><span data-ttu-id="b7451-700">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-700">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-701">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-701">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-702">msRTCSIP-SchemaVersion</span><span class="sxs-lookup"><span data-stu-id="b7451-702">msRTCSIP-SchemaVersion</span></span></p></td>
<td><p><span data-ttu-id="b7451-703">Este atributo representa la versión del esquema implementada actualmente en la organización.</span><span class="sxs-lookup"><span data-stu-id="b7451-703">This attribute represents the schema version currently deployed in the organization.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-704">msRTCSIP-SearchMaxRequests (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-704">msRTCSIP-SearchMaxRequests (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-705">Este atributo limita el número de resultados de búsqueda que se devolverán desde una búsqueda de directorio cuando un usuario busca un contacto con Communicator.</span><span class="sxs-lookup"><span data-stu-id="b7451-705">This attribute limits the number of search results to be returned from a directory search when a user searches for a contact using Communicator.</span></span> <span data-ttu-id="b7451-706">Este atributo invalidará el valor proporcionado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="b7451-706">This attribute will override the value provided by the client.</span></span></p></td>
<td><p><span data-ttu-id="b7451-707">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-707">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-708">msRTCSIP-SearchMaxResults (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-708">msRTCSIP-SearchMaxResults (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-709">Este atributo limita el número de solicitudes de búsqueda devuelto.</span><span class="sxs-lookup"><span data-stu-id="b7451-709">This attribute limits the number of search requests returned.</span></span></p></td>
<td><p><span data-ttu-id="b7451-710">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-710">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-711">msRTCSIP-ServerBL</span><span class="sxs-lookup"><span data-stu-id="b7451-711">msRTCSIP-ServerBL</span></span></p></td>
<td><p><span data-ttu-id="b7451-712">Este atributo de valor múltiple es un vínculo hacia atrás que contiene una lista de nombres completos (DN).</span><span class="sxs-lookup"><span data-stu-id="b7451-712">This multi-valued attribute is a back link that contains a list of distinguished names (DN).</span></span> <span data-ttu-id="b7451-713">Este DNs apunta a un grupo o a un objeto <strong>TrustedService</strong> .</span><span class="sxs-lookup"><span data-stu-id="b7451-713">These DNs point to a pool or <strong>TrustedService</strong> object.</span></span></p>
<p><span data-ttu-id="b7451-714">Este atributo corresponde al vínculo de reenvío <strong>msRTCSIP-TrustedServiceLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-714">This attribute corresponds to the forward link <strong>msRTCSIP-TrustedServiceLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-715">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-715">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-716">msRTCSIP-ServerData</span><span class="sxs-lookup"><span data-stu-id="b7451-716">msRTCSIP-ServerData</span></span></p></td>
<td><p><span data-ttu-id="b7451-717">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-717">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-718">msRTCSIP-ServerReferenceBL (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-718">msRTCSIP-ServerReferenceBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-719">Este atributo de valor múltiple contiene una lista de nombres completos.</span><span class="sxs-lookup"><span data-stu-id="b7451-719">This multi-valued attribute contains a list of distinguished names.</span></span> <span data-ttu-id="b7451-720">Estos nombres completos devuelven vínculos que hacen referencia a otros objetos de servidor a los que se puede asignar un perfil de ubicación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b7451-720">These distinguished names are back links that reference other server objects that can be assigned a default location profile.</span></span></p>
<p><span data-ttu-id="b7451-721">Vínculo anterior: <strong>identificador de vínculo 11037</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-721">Back link: <strong>Link ID 11037</strong></span></span></p>
<p><span data-ttu-id="b7451-722">El vínculo de reenvío correspondiente a este vínculo anterior es <strong>msRTCSIP-DefaultLocationProfileLink</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-722">The corresponding forward link to this back link is <strong>msRTCSIP-DefaultLocationProfileLink</strong>.</span></span></p>
<p><span data-ttu-id="b7451-723">Este atributo de vínculo de retroceso solo hace referencia a los grupos y servidores de mediación.</span><span class="sxs-lookup"><span data-stu-id="b7451-723">This back link attribute references pools and Mediation Servers only.</span></span></p></td>
<td><p><span data-ttu-id="b7451-724">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-724">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-725">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-725">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-726">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7451-726">msRTCSIP-ServerVersion</span></span></p></td>
<td><p><span data-ttu-id="b7451-727">Este atributo define la información de versión del servidor.</span><span class="sxs-lookup"><span data-stu-id="b7451-727">This attribute defines the version information of the server.</span></span> <span data-ttu-id="b7451-728">Este número de versión se aplica a todos los roles de servidor.</span><span class="sxs-lookup"><span data-stu-id="b7451-728">This version number applies to all server roles.</span></span> <span data-ttu-id="b7451-729">Es un monotonously que aumenta con cada versión oficial del producto.</span><span class="sxs-lookup"><span data-stu-id="b7451-729">It is a monotonously increasing integer that increments with each official product release.</span></span></p>
<p><span data-ttu-id="b7451-730">Los posibles valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-730">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-731">Undefined: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7451-731">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="b7451-732">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="b7451-732">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="b7451-733">Live Communications Server 2005 con SP1</span><span class="sxs-lookup"><span data-stu-id="b7451-733">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="b7451-734">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="b7451-734">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="b7451-735">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="b7451-735">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="b7451-736">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="b7451-736">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="b7451-737">6: Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7451-737">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-738">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-738">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-739">msRTCSIP-SourceObjectType</span><span class="sxs-lookup"><span data-stu-id="b7451-739">msRTCSIP-SourceObjectType</span></span></p></td>
<td><p><span data-ttu-id="b7451-740">Este atributo de valor único de tipo entero especifica el tipo de objeto al que apunta <strong>MSDS-SourceObjectDN</strong> , de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b7451-740">This single-valued attribute of integer type specifies the type of object the <strong>msDS-SourceObjectDN</strong> points to, as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-741">null | 0x00000001: representa un objeto de usuario principal de Windows NT Server de un bosque diferente</span><span class="sxs-lookup"><span data-stu-id="b7451-741">null | 0x00000001: Represents a Windows NT Server principal user object from a different forest</span></span></p></li>
<li><p><span data-ttu-id="b7451-742">Los siguientes atributos representan un tipo de grupo de un bosque diferente para la expansión de grupos de distribución:</span><span class="sxs-lookup"><span data-stu-id="b7451-742">The following attributes represent a group type from a different forest for distribution group expansion:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="b7451-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="b7451-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="b7451-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="b7451-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="b7451-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="b7451-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="b7451-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="b7451-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span><span class="sxs-lookup"><span data-stu-id="b7451-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span></span></p></li>
<li><p><span data-ttu-id="b7451-748">0x90000000: representa un objeto de acceso de operador automático o de suscriptor del mismo bosque o de un bosque diferente</span><span class="sxs-lookup"><span data-stu-id="b7451-748">0x90000000: Represents an Auto-Attendant or subscriber access object from the same forest or a different forest</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="b7451-749">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-749">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-750">msRTCSIP-SubscriptionAuthRequired (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-750">msRTCSIP-SubscriptionAuthRequired (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="b7451-751">Novedades de Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b7451-751">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="b7451-752">Obsoleto en Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-752">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-753">msRTCSIP-TargetHomeServer</span><span class="sxs-lookup"><span data-stu-id="b7451-753">msRTCSIP-TargetHomeServer</span></span></p></td>
<td><p><span data-ttu-id="b7451-754">Este atributo le permite mover un usuario o un objeto de contacto de un grupo de servidores de Lync a otro.</span><span class="sxs-lookup"><span data-stu-id="b7451-754">This attribute enables you to move a user or contact object from one Lync Server pool to another.</span></span> <span data-ttu-id="b7451-755">Este atributo se agrega a la clase de contacto, porque en la topología del bosque central, los objetos de contacto, no los objetos de usuario, están habilitados para SIP.</span><span class="sxs-lookup"><span data-stu-id="b7451-755">This attribute is added to the contact class, because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="b7451-756">El valor válido es el nombre completo del servidor Standard Edition o del grupo de servidores front end al que se va a mover un usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-756">The valid value is the DN of the destination Standard Edition server or Front End pool to which a user is to be moved.</span></span></p></td>
<td><p><span data-ttu-id="b7451-757">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-757">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-758">msRTCSIP-TargetPhoneNumber (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-758">msRTCSIP-TargetPhoneNumber (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-759">Este atributo de cadena de valor único contiene un intervalo o un patrón de números de teléfono para enrutar a las puertas de enlace especificadas definidas en <strong>msRTCSIP-gateways</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-759">This single-valued string attribute contains a phone number pattern or range to route to the specified gateways defined in <strong>msRTCSIP-Gateways</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-760">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-760">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-761">msRTCSIP-TargetUserPolicies</span><span class="sxs-lookup"><span data-stu-id="b7451-761">msRTCSIP-TargetUserPolicies</span></span></p></td>
<td><p><span data-ttu-id="b7451-762">Este atributo almacena pares de nombre y valor para las directivas de destino de los usuarios de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b7451-762">This attribute stores name-value pairs for target policies for Lync Server users.</span></span></p></td>
<td><p><span data-ttu-id="b7451-763">Novedades de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-763">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-764">msRTCSIP-TenantId</span><span class="sxs-lookup"><span data-stu-id="b7451-764">msRTCSIP-TenantId</span></span></p></td>
<td><p><span data-ttu-id="b7451-765">Este atributo almacena el identificador único para un inquilino.</span><span class="sxs-lookup"><span data-stu-id="b7451-765">This attribute stores the unique identifier for a tenant.</span></span></p></td>
<td><p><span data-ttu-id="b7451-766">Novedades de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-766">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-767">msRTCSIP-Translation (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-767">msRTCSIP-Translation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-768">Este atributo es utilizado por la característica de voz de Lync Server y contiene la cadena de traducción para aplicar en el número marcado, si se encuentra una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="b7451-768">This attribute is used by the voice feature of Lync Server and contains the translation string to apply on the dialed number, if a match is found.</span></span></p></td>
<td><p><span data-ttu-id="b7451-769">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-769">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="b7451-770">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-770">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-771">msRTCSIP-TrustedMCUData</span><span class="sxs-lookup"><span data-stu-id="b7451-771">msRTCSIP-TrustedMCUData</span></span></p></td>
<td><p><span data-ttu-id="b7451-772">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-772">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-773">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-773">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-774">msRTCSIP-TrustedMCUFQDN</span><span class="sxs-lookup"><span data-stu-id="b7451-774">msRTCSIP-TrustedMCUFQDN</span></span></p></td>
<td><p><span data-ttu-id="b7451-775">Este atributo es un valor de cadena que contiene el FQDN del MCU.</span><span class="sxs-lookup"><span data-stu-id="b7451-775">This attribute is a string value that contains the FQDN of the MCU.</span></span> <span data-ttu-id="b7451-776">Este es un atributo de valor único.</span><span class="sxs-lookup"><span data-stu-id="b7451-776">This is a single-valued attribute.</span></span> <span data-ttu-id="b7451-777">El valor válido para cada segmento es de 63 caracteres; el valor válido para todo el FQDN es 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b7451-777">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="b7451-778">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-778">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-779">msRTCSIP-TrustedProxyData</span><span class="sxs-lookup"><span data-stu-id="b7451-779">msRTCSIP-TrustedProxyData</span></span></p></td>
<td><p><span data-ttu-id="b7451-780">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-780">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-781">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-781">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-782">msRTCSIP-TrustedProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="b7451-782">msRTCSIP-TrustedProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="b7451-783">Este atributo es un valor de cadena que contiene el nombre completo del servidor que ejecuta Proxy Server.</span><span class="sxs-lookup"><span data-stu-id="b7451-783">This attribute is a string value that contains the FQDN of the server running Proxy Server.</span></span> <span data-ttu-id="b7451-784">Este atributo tiene un único valor.</span><span class="sxs-lookup"><span data-stu-id="b7451-784">This attribute is single-valued.</span></span> <span data-ttu-id="b7451-785">El valor válido para cada segmento es de 63 caracteres; el valor válido para todo el FQDN es 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b7451-785">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="b7451-786">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-786">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-787">msRTCSIP-TrustedServerData</span><span class="sxs-lookup"><span data-stu-id="b7451-787">msRTCSIP-TrustedServerData</span></span></p></td>
<td><p><span data-ttu-id="b7451-788">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-788">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-789">msRTCSIP-TrustedServerFQDN</span><span class="sxs-lookup"><span data-stu-id="b7451-789">msRTCSIP-TrustedServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="b7451-790">Este atributo es un atributo de valor único que representa el FQDN de un servidor de confianza.</span><span class="sxs-lookup"><span data-stu-id="b7451-790">This attribute is a single-valued attribute that represents the FQDN of a trusted server.</span></span></p></td>
<td><p><span data-ttu-id="b7451-791">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-791">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-792">msRTCSIP-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="b7451-792">msRTCSIP-TrustedServerVersion</span></span></p></td>
<td><p><span data-ttu-id="b7451-793">Este atributo especifica el número de versión de un servidor en la lista de servidores de confianza.</span><span class="sxs-lookup"><span data-stu-id="b7451-793">This attribute specifies the version number of a server in the trusted server list.</span></span></p>
<p><span data-ttu-id="b7451-794">Los posibles valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-794">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-795">NULL: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7451-795">NULL: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="b7451-796">2: Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="b7451-796">2: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="b7451-797">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="b7451-797">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="b7451-798">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="b7451-798">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="b7451-799">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="b7451-799">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="b7451-800">6: Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7451-800">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-801">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-801">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-802">msRTCSIP-TrustedServiceFlags</span><span class="sxs-lookup"><span data-stu-id="b7451-802">msRTCSIP-TrustedServiceFlags</span></span></p></td>
<td><p><span data-ttu-id="b7451-803">Este atributo define las opciones que están habilitadas para el servicio de confianza.</span><span class="sxs-lookup"><span data-stu-id="b7451-803">This attribute defines the options that are enabled for the trusted service.</span></span></p></td>
<td><p><span data-ttu-id="b7451-804">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-804">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-805">msRTCSIP-TrustedServiceLinks</span><span class="sxs-lookup"><span data-stu-id="b7451-805">msRTCSIP-TrustedServiceLinks</span></span></p></td>
<td><p><span data-ttu-id="b7451-806">Este atributo de valor múltiple contiene una lista de nombres completos (DN) que hacen referencia a un objeto de servicio de confianza, como un servicio de autenticación de retransmisión multimedia.</span><span class="sxs-lookup"><span data-stu-id="b7451-806">This multi-valued attribute contains a list of distinguished names (DN) that reference a trusted service object, such as a Media Relay Authentication Service.</span></span> <span data-ttu-id="b7451-807">Un servicio de autenticación de retransmisión multimedia (que se encuentra físicamente en el servidor perimetral que ejecuta el servicio de conferencia A/V) debe estar asociado a un grupo para admitir escenarios de audio para usuarios remotos.</span><span class="sxs-lookup"><span data-stu-id="b7451-807">A Media Relay Authentication Service (physically collocated on the Edge Server running the A/V Conferencing service) must be associated with a pool to support audio scenarios for remote users.</span></span></p>
<p><span data-ttu-id="b7451-808">El vínculo atrás correspondiente a este atributo de vínculo hacia adelante es <strong>msRTCSIP-ServerBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-808">The corresponding back link to this forward link attribute is <strong>msRTCSIP-ServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-809">UC</span><span class="sxs-lookup"><span data-stu-id="b7451-809">UC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-810">msRTCSIP-TrustedServicePort</span><span class="sxs-lookup"><span data-stu-id="b7451-810">msRTCSIP-TrustedServicePort</span></span></p></td>
<td><p><span data-ttu-id="b7451-811">Este atributo es un entero que define el número de puerto que se usa para conectarse a este servicio de GRUU.</span><span class="sxs-lookup"><span data-stu-id="b7451-811">This attribute is an integer that defines the port number used to connect to this GRUU service.</span></span></p></td>
<td><p><span data-ttu-id="b7451-812">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-812">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-813">msRTCSIP-TrustedServiceType</span><span class="sxs-lookup"><span data-stu-id="b7451-813">msRTCSIP-TrustedServiceType</span></span></p></td>
<td><p><span data-ttu-id="b7451-814">Este atributo es un valor de cadena que define el tipo de servicio GRUU que representa.</span><span class="sxs-lookup"><span data-stu-id="b7451-814">This attribute is a string value that defines the type of GRUU service it represents.</span></span></p>
<p><span data-ttu-id="b7451-815">Los tipos de servicio GRUU válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-815">The valid GRUU service types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-816">MediationServer</span><span class="sxs-lookup"><span data-stu-id="b7451-816">MediationServer</span></span></p></li>
<li><p><span data-ttu-id="b7451-817">Puerta</span><span class="sxs-lookup"><span data-stu-id="b7451-817">Gateway</span></span></p></li>
<li><p><span data-ttu-id="b7451-818">Servicio de autenticación de retransmisión de multimedia (MRAS)</span><span class="sxs-lookup"><span data-stu-id="b7451-818">Media Relay Authentication Service (MRAS)</span></span></p></li>
<li><p><span data-ttu-id="b7451-819">QoSM</span><span class="sxs-lookup"><span data-stu-id="b7451-819">QoSM</span></span></p></li>
<li><p><span data-ttu-id="b7451-820">msRTCSIP-UserExtension CWA</span><span class="sxs-lookup"><span data-stu-id="b7451-820">msRTCSIP-UserExtension CWA</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-821">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-821">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-822">msRTCSIP-TrustedWebComponentsServerData</span><span class="sxs-lookup"><span data-stu-id="b7451-822">msRTCSIP-TrustedWebComponentsServerData</span></span></p></td>
<td><p><span data-ttu-id="b7451-823">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-823">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-824">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-824">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-825">msRTCSIP-TrustedWebComponentsServerFQDN</span><span class="sxs-lookup"><span data-stu-id="b7451-825">msRTCSIP-TrustedWebComponentsServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="b7451-826">Este atributo es un valor de cadena que contiene el FQDN de los servicios Web de Lync Server de IIS.</span><span class="sxs-lookup"><span data-stu-id="b7451-826">This attribute is a string value that contains the FQDN of the IIS running Lync Server Web Services.</span></span> <span data-ttu-id="b7451-827">Este es un atributo de valor único.</span><span class="sxs-lookup"><span data-stu-id="b7451-827">This is a single-valued attribute.</span></span> <span data-ttu-id="b7451-828">El valor válido para cada segmento es de 63 caracteres; el valor válido para todo el FQDN es 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b7451-828">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="b7451-829">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-829">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-830">msRTCSIP-UCFlags (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-830">msRTCSIP-UCFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-831">Este atributo define diferentes opciones de UC que se habilitan globalmente para todos los objetos de usuario o contacto.</span><span class="sxs-lookup"><span data-stu-id="b7451-831">This attribute defines different UC options that are enabled globally to all user or contact objects.</span></span> <span data-ttu-id="b7451-832">Este atributo es un valor de máscara de bits de tipo entero.</span><span class="sxs-lookup"><span data-stu-id="b7451-832">This attribute is a bit-mask value of integer type.</span></span> <span data-ttu-id="b7451-833">Cada opción está representada por la presencia de un bit.</span><span class="sxs-lookup"><span data-stu-id="b7451-833">Each option is represented by the presence of a bit.</span></span></p>
<p><span data-ttu-id="b7451-834">El posible valor válido (y la posición de bits asociada) son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-834">The possible valid value (and associated bit position) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-835">4: UsePerUserUCPolicy (posición de bit 2)</span><span class="sxs-lookup"><span data-stu-id="b7451-835">4: UsePerUserUCPolicy (bit position 2)</span></span></p></li>
</ul>
<p><span data-ttu-id="b7451-836">Cuando se establece este bit, se define la Directiva de UC por usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-836">When this bit is set, the UC policy is defined per user.</span></span></p></td>
<td><p><span data-ttu-id="b7451-837">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-837">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-838">msRTCSIP-UCPolicy (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-838">msRTCSIP-UCPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-839">Este atributo de valor único contiene el nombre completo (DN) de la Directiva UC que el administrador ha asignado para este usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-839">This single-valued attribute contains the distinguished name (DN) of the UC policy that the administrator has assigned for this user.</span></span></p></td>
<td><p><span data-ttu-id="b7451-840">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-840">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-841">msRTCSIP-UserDomainList (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-841">msRTCSIP-UserDomainList (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b7451-842">Este atributo proporciona una lista de todos los dominios de un bosque que hospedan usuarios habilitados para SIP.</span><span class="sxs-lookup"><span data-stu-id="b7451-842">This attribute provides a list of all the domains in a forest that host SIP-enabled users.</span></span> <span data-ttu-id="b7451-843">El valor predeterminado es una lista vacía, que indica que todos los dominios del bosque están habilitados para SIP.</span><span class="sxs-lookup"><span data-stu-id="b7451-843">The default is an empty list, indicating that all domains in the forest are SIP-enabled.</span></span></p>
<p><span data-ttu-id="b7451-844">Los valores válidos son varias cadenas que representan los nombres de dominio de los dominios individuales.</span><span class="sxs-lookup"><span data-stu-id="b7451-844">Valid values are multiple strings representing the domain names of individual domains.</span></span></p></td>
<td><p><span data-ttu-id="b7451-845">Novedades de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-845">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="b7451-846">Obsoleto en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-846">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-847">msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="b7451-847">msRTCSIP-UserEnabled</span></span></p></td>
<td><p><span data-ttu-id="b7451-848">Este atributo determina si el usuario está actualmente habilitado para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b7451-848">This attribute determines whether the user is currently enabled for Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-849">msRTCSIP-UserExtension</span><span class="sxs-lookup"><span data-stu-id="b7451-849">msRTCSIP-UserExtension</span></span></p></td>
<td><p><span data-ttu-id="b7451-850">Este atributo de valor múltiple contiene una lista de pares de nombre y valor en el formato de &quot; name = value. &quot; Este atributo se marca para la replicación del catálogo global.</span><span class="sxs-lookup"><span data-stu-id="b7451-850">This multi-valued attribute contains a list of name-value pairs in the format of &quot;name=value.&quot; This attribute is marked for global catalog replication.</span></span></p></td>
<td><p><span data-ttu-id="b7451-851">Novedades de Live Communications Server 2005 con SP1.</span><span class="sxs-lookup"><span data-stu-id="b7451-851">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-852">msRTCSIP-UserLocationProfile</span><span class="sxs-lookup"><span data-stu-id="b7451-852">msRTCSIP-UserLocationProfile</span></span></p></td>
<td><p><span data-ttu-id="b7451-853">Este atributo contiene el nombre distintivo (DN) que apunta a un objeto de Perfil de ubicación.</span><span class="sxs-lookup"><span data-stu-id="b7451-853">This attribute contains the distinguished name (DN) that points to a location profile object.</span></span></p></td>
<td><p><span data-ttu-id="b7451-854">Novedades de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b7451-854">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-855">msRTCSIP-UserPolicies</span><span class="sxs-lookup"><span data-stu-id="b7451-855">msRTCSIP-UserPolicies</span></span></p></td>
<td><p><span data-ttu-id="b7451-856">Este atributo almacena pares de nombre y valor para directivas de usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-856">This attribute stores name-value pairs for user policies.</span></span></p></td>
<td><p><span data-ttu-id="b7451-857">Novedades de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b7451-857">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-858">msRTCSIP-UserPolicy</span><span class="sxs-lookup"><span data-stu-id="b7451-858">msRTCSIP-UserPolicy</span></span></p></td>
<td><p><span data-ttu-id="b7451-859">Este es un atributo de valor múltiple que contiene una lista de nombres completos con binario (DN_WITH_BINARY) que apunta a directivas de usuario globales de diferentes tipos.</span><span class="sxs-lookup"><span data-stu-id="b7451-859">This is a multi-valued attribute containing a list of distinguished names with binary (DN_WITH_BINARY) pointing to global user policies of different types.</span></span> <span data-ttu-id="b7451-860">El elemento binario indica el tipo de directiva a la que apunta la parte DN.</span><span class="sxs-lookup"><span data-stu-id="b7451-860">The binary part indicates the type of policy to which the DN portion points.</span></span></p>
<p><span data-ttu-id="b7451-861">Los valores binarios válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7451-861">The valid binary values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-862">0x00000001: política de reuniones</span><span class="sxs-lookup"><span data-stu-id="b7451-862">0x00000001: Meeting policy</span></span></p></li>
<li><p><span data-ttu-id="b7451-863">0x00000002: Directiva UC</span><span class="sxs-lookup"><span data-stu-id="b7451-863">0x00000002: UC policy</span></span></p></li>
<li><p><span data-ttu-id="b7451-864">0x00000005: Directiva de presencia</span><span class="sxs-lookup"><span data-stu-id="b7451-864">0x00000005: Presence policy</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-865">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-865">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-866">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="b7451-866">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="b7451-867">Este es el identificador de grupo de enrutamiento SIP.</span><span class="sxs-lookup"><span data-stu-id="b7451-867">This is the SIP routing group ID.</span></span> <span data-ttu-id="b7451-868">Los usuarios del mismo grupo se registrarán en el mismo servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="b7451-868">Users in the same group will register to the same Front End Server.</span></span></p></td>
<td><p><span data-ttu-id="b7451-869">Novedades de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b7451-869">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-870">msRTCSIP-WebComponentsData</span><span class="sxs-lookup"><span data-stu-id="b7451-870">msRTCSIP-WebComponentsData</span></span></p></td>
<td><p><span data-ttu-id="b7451-871">Este es un atributo de valor múltiple.</span><span class="sxs-lookup"><span data-stu-id="b7451-871">This is a multi-valued attribute.</span></span> <span data-ttu-id="b7451-872">Este atributo se reserva para usarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b7451-872">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="b7451-873">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-873">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-874">msRTCSIP-WebComponentsPoolAddress</span><span class="sxs-lookup"><span data-stu-id="b7451-874">msRTCSIP-WebComponentsPoolAddress</span></span></p></td>
<td><p><span data-ttu-id="b7451-875">Este atributo de valor único apunta al grupo de servidores o al servidor Standard Edition al que pertenecen los componentes Web.</span><span class="sxs-lookup"><span data-stu-id="b7451-875">This single-valued attribute points to the pool or Standard Edition server to which the web components belong.</span></span></p>
<p><span data-ttu-id="b7451-876">Vínculo hacia adelante: <strong>identificador de vínculo 11028</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-876">Forward link: <strong>Link ID 11028</strong></span></span></p>
<p><span data-ttu-id="b7451-877">El vínculo atrás correspondiente a este atributo de vínculo hacia adelante es <strong>msRTCSIP-WebComponentsServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-877">The corresponding back link to this forward link attribute is <strong>msRTCSIP-WebComponentsServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-878">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-878">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-879">msRTCSIP-WebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="b7451-879">msRTCSIP-WebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="b7451-880">Este atributo es una lista con varios valores de nombres completos.</span><span class="sxs-lookup"><span data-stu-id="b7451-880">This attribute is a multi-valued list of distinguished names.</span></span> <span data-ttu-id="b7451-881">Este atributo contiene una lista de todos los servidores web asociados con este grupo.</span><span class="sxs-lookup"><span data-stu-id="b7451-881">This attribute contains a list of all Web servers associated with this pool.</span></span></p>
<p><span data-ttu-id="b7451-882">Vínculo anterior: <strong>identificador de vínculo 11029</strong></span><span class="sxs-lookup"><span data-stu-id="b7451-882">Back link: <strong>Link ID 11029</strong></span></span></p>
<p><span data-ttu-id="b7451-883">El vínculo de reenvío correspondiente a este vínculo anterior es <strong>msRTCSIP-WebComponentsPoolAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7451-883">The corresponding forward link to this back link is <strong>msRTCSIP-WebComponentsPoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="b7451-884">Novedades de Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="b7451-884">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-885">msRTCSIP-WMIInstanceId (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="b7451-885">msRTCSIP-WMIInstanceId (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="b7451-886">Novedades de Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b7451-886">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="b7451-887">Obsoleto en Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="b7451-887">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-888">OtherIPPhone</span><span class="sxs-lookup"><span data-stu-id="b7451-888">OtherIPPhone</span></span></p></td>
<td><p><span data-ttu-id="b7451-889">Este atributo de Active Directory existente es utilizado por telefonía para especificar la lista de direcciones TCP/IP alternativas para un teléfono.</span><span class="sxs-lookup"><span data-stu-id="b7451-889">This existing Active Directory attribute is used by telephony to specify the list of alternate TCP/IP addresses for a phone.</span></span></p></td>
<td><p><span data-ttu-id="b7451-890">Nuevo en el sistema operativo Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b7451-890">New in Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-891">PhoneOfficeOther</span><span class="sxs-lookup"><span data-stu-id="b7451-891">PhoneOfficeOther</span></span></p></td>
<td><p><span data-ttu-id="b7451-892">Los componentes de voz de Lync Server usan este atributo de Active Directory existente, solo para objetos de contacto, con el fin de enrutar llamadas a los números de acceso de los suscriptores y el operador automático de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="b7451-892">This existing Active Directory attribute is used by the voice components in Lync Server, for contact objects only, for the purpose of routing calls to the unified messaging auto-attendant and subscriber access numbers.</span></span> <span data-ttu-id="b7451-893">La dirección de desvío de llamadas incondicionales se almacena en este atributo de valor múltiple.</span><span class="sxs-lookup"><span data-stu-id="b7451-893">The unconditional call forwarding address is stored in this multi-valued attribute.</span></span> <span data-ttu-id="b7451-894">Esta cuenta se crea para el propósito específico del acceso de operador automático y suscriptor.</span><span class="sxs-lookup"><span data-stu-id="b7451-894">This account is created for the specific purpose of auto-attendant and subscriber access.</span></span> <span data-ttu-id="b7451-895">Los administradores no deben modificar los atributos de esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="b7451-895">This account’s attributes should not be modified by administrators.</span></span></p></td>
<td><p><span data-ttu-id="b7451-896">Nuevo en el sistema operativo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b7451-896">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7451-897">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="b7451-897">ProxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="b7451-898">Este atributo de valor múltiple de Active Directory existente forma parte del esquema de Active Directory base introducido en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b7451-898">This existing Active Directory multi-valued attribute is part of the base Active Directory schema introduced in Windows 2000.</span></span> <span data-ttu-id="b7451-899">Este atributo contiene las distintas direcciones de X400, X500 y SMTP del correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-899">This attribute contains the various X400, X500, and SMTP addresses of the user’s email.</span></span> <span data-ttu-id="b7451-900">En Live Communications Server 2003 y versiones posteriores, el URI del SIP del usuario se agrega a la lista con la &quot; etiqueta SIP: &quot; .</span><span class="sxs-lookup"><span data-stu-id="b7451-900">In Live Communications Server 2003 and later, the user’s SIP URI is added to this list, using the &quot;sip:&quot; tag.</span></span></p>
<p><span data-ttu-id="b7451-901">Las siguientes aplicaciones buscan el URI SIP del usuario desde este atributo:</span><span class="sxs-lookup"><span data-stu-id="b7451-901">The following applications search the user’s SIP URI from this attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="b7451-902">Cliente de mensajería y colaboración 2003 de Microsoft Office Outlook</span><span class="sxs-lookup"><span data-stu-id="b7451-902">Microsoft Office Outlook 2003 messaging and collaboration client</span></span></p></li>
<li><p><span data-ttu-id="b7451-903">Microsoft Office SharePoint Server 2007</span><span class="sxs-lookup"><span data-stu-id="b7451-903">Microsoft Office SharePoint Server 2007</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b7451-904">Nuevo en el sistema operativo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b7451-904">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7451-905">NúmeroDeTeléfono</span><span class="sxs-lookup"><span data-stu-id="b7451-905">TelephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="b7451-906">Este atributo de Active Directory existente contiene el número de teléfono para el usuario.</span><span class="sxs-lookup"><span data-stu-id="b7451-906">This existing Active Directory attribute contains the telephone number for the user.</span></span></p></td>
<td><p><span data-ttu-id="b7451-907">Nuevo en el sistema operativo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b7451-907">New in Windows 2000 operating system.</span></span></p></td>
</tr><span data-ttu-id="b7451-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7451-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

