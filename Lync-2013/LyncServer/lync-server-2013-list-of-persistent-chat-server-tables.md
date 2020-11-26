---
title: 'Lync Server 2013: Lista de tablas de servidores de chat persistente'
description: 'Lync Server 2013: lista de tablas de servidores de chat persistentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of Persistent Chat Server tables
ms:assetid: 26c9e271-3516-4d90-b930-70fec4e359ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558628(v=OCS.15)
ms:contentKeyID: 48183659
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 838e6d8f83b137923075851b29df4c602a487391
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426588"
---
# <a name="list-of-persistent-chat-server-tables-in-lync-server-2013"></a><span data-ttu-id="f8996-103">Lista de tablas de servidores de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8996-103">List of Persistent Chat Server tables in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8996-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8996-104">

<span> </span></span></span>

<span data-ttu-id="f8996-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="f8996-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="f8996-106">El esquema de base de datos de chat persistente consta de las siguientes tablas.</span><span class="sxs-lookup"><span data-stu-id="f8996-106">The Persistent Chat database schema consists of the following tables.</span></span>

<div>

## <a name="active-directory-sync"></a><span data-ttu-id="f8996-107">Sincronización de Active Directory</span><span class="sxs-lookup"><span data-stu-id="f8996-107">Active Directory Sync</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8996-108">Tabla</span><span class="sxs-lookup"><span data-stu-id="f8996-108">Table</span></span></th>
<th><span data-ttu-id="f8996-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8996-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8996-110"><a href="lync-server-2013-tbladcookie.md">tblADCookie en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-110"><a href="lync-server-2013-tbladcookie.md">tblADCookie in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-111">Contiene las cookies de sincronización del Protocolo ligero de acceso a directorios (LDAP).</span><span class="sxs-lookup"><span data-stu-id="f8996-111">Contains the current Lightweight Directory Access Protocol (LDAP) Sync cookies.</span></span> <span data-ttu-id="f8996-112">Cada fila corresponde a un dominio de servicios de dominio de Active Directory en el que el servidor de chat persistente está supervisando activamente los cambios.</span><span class="sxs-lookup"><span data-stu-id="f8996-112">Each row corresponds to an Active Directory Domain Services domain that Persistent Chat Server is actively monitoring for changes.</span></span> <span data-ttu-id="f8996-113">(En esta tabla solo se representan los dominios de Active Directory pertinentes para el servidor de chat persistente).</span><span class="sxs-lookup"><span data-stu-id="f8996-113">(Only the Active Directory domains that are relevant for Persistent Chat Server are represented in this table.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-114"><a href="lync-server-2013-tblprincipalmemberdifference.md">tblPrincipalMemberDifference en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-114"><a href="lync-server-2013-tblprincipalmemberdifference.md">tblPrincipalMemberDifference in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-115">Contiene cambios en la pertenencia a grupos (miembros agregados y eliminados) que aún no han sido procesados por los pasos de sincronización de Active Directory más recientes y es una de las tablas temporales (junto con la tabla tblADUpdates) que se usa en el primer paso de la sincronización de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8996-115">Contains group membership changes (both added and removed members) that have not yet been processed by the later Active Directory Sync steps and is one of the temporary tables (along with tblADUpdates table) that is used in the first step of Active Directory Sync.</span></span></p>
<p><span data-ttu-id="f8996-116">Los cambios de pertenencia se almacenan, se procesan o ambos, solo para los grupos que se muestran en la tabla tblPrincipal o que ya tienen miembros.</span><span class="sxs-lookup"><span data-stu-id="f8996-116">Membership changes are stored, processed, or both, only for groups that are listed in the tblPrincipal table or that already have members listed there.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8996-117"><a href="lync-server-2013-tbladupdates.md">tblADUpdates en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-117"><a href="lync-server-2013-tbladupdates.md">tblADUpdates in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-118">Contiene cambios en los servicios de dominio de Active Directory que aún no han procesado los pasos de sincronización de Active Directory más recientes y es una de las tablas temporales (junto con la tabla tblPrincipalMemberDifference) que se usa en el primer paso de la sincronización de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8996-118">Contains changes to Active Directory Domain Services that have not yet been processed by the later Active Directory Sync steps and is one of the temporary tables (along with the tblPrincipalMemberDifference table) that is used in the first step of Active Directory Sync.</span></span></p>
<p><span data-ttu-id="f8996-119">Los cambios en Active Directory se almacenan, se procesan o ambos solo para los principales que ya aparecen en la tabla tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="f8996-119">Changes to Active Directory are stored, processed, or both only for principals that are already listed in the tblPrincipal table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-120"><a href="lync-server-2013-tblprincipalmembers.md">tblPrincipalMembers en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-120"><a href="lync-server-2013-tblprincipalmembers.md">tblPrincipalMembers in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-121">Contiene pertenencias principales.</span><span class="sxs-lookup"><span data-stu-id="f8996-121">Contains principal memberships.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8996-122"><a href="lync-server-2013-tblprincipalmeta.md">tblPrincipalMeta en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-122"><a href="lync-server-2013-tblprincipalmeta.md">tblPrincipalMeta in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-123">Contiene las entidades de identidad que deben actualizarse desde Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8996-123">Contains the principals that have to be refreshed from Active Directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-124"><a href="lync-server-2013-tblskippedaffiliations.md">tblSkippedAffiliations en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-124"><a href="lync-server-2013-tblskippedaffiliations.md">tblSkippedAffiliations in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-125">Contiene afiliaciones que no se pudieron actualizar por alguna razón, generalmente debido a errores de acceso a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8996-125">Contains affiliations that could not be refreshed for some reason, usually due to Active Directory access errors.</span></span></p>
<p><span data-ttu-id="f8996-126">Esta tabla es solo para fines informativos.</span><span class="sxs-lookup"><span data-stu-id="f8996-126">This table is for informational purposes only.</span></span> <span data-ttu-id="f8996-127">No se utiliza su contenido.</span><span class="sxs-lookup"><span data-stu-id="f8996-127">Its content is not used.</span></span></p>
<p><span data-ttu-id="f8996-128">Las principales de las afiliaciones que no se hayan actualizado correctamente se guardan en la tabla tblPrincipalMeta y se les da otra oportunidad para que se actualicen.</span><span class="sxs-lookup"><span data-stu-id="f8996-128">The principals with affiliations that could not be refreshed properly are kept in the tblPrincipalMeta table and are given another chance to be refreshed.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="principals-affiliations-nodes-scopes-and-roles"></a><span data-ttu-id="f8996-129">Principales, afiliaciones, nodos, ámbitos y roles</span><span class="sxs-lookup"><span data-stu-id="f8996-129">Principals, Affiliations, Nodes, Scopes, and Roles</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8996-130">Tabla</span><span class="sxs-lookup"><span data-stu-id="f8996-130">Table</span></span></th>
<th><span data-ttu-id="f8996-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8996-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8996-132"><a href="lync-server-2013-tblprincipaltype.md">tblPrincipalType en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-132"><a href="lync-server-2013-tblprincipaltype.md">tblPrincipalType in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-133">Contiene tipos de principal para categorizar lo que hay en la tabla tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="f8996-133">Contains principal types to categorize what is in the tblPrincipal table.</span></span> <span data-ttu-id="f8996-134">Esta tabla es estática.</span><span class="sxs-lookup"><span data-stu-id="f8996-134">This table is static.</span></span> <span data-ttu-id="f8996-135">Se configura durante la creación de la base de datos y no cambia.</span><span class="sxs-lookup"><span data-stu-id="f8996-135">It is set up during database creation and does not change.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-136"><a href="lync-server-2013-tblprincipal.md">tblPrincipal enn Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-136"><a href="lync-server-2013-tblprincipal.md">tblPrincipal in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-137">Contiene todos los principales (usuarios, carpetas, grupos, etc.).</span><span class="sxs-lookup"><span data-stu-id="f8996-137">Contains all principals (users, folders, groups, and so on).</span></span> <span data-ttu-id="f8996-138">El servidor de chat persistente gestiona esto como una lista heterogénea plana.</span><span class="sxs-lookup"><span data-stu-id="f8996-138">Persistent Chat Server handles this as a flat heterogeneous list.</span></span> <span data-ttu-id="f8996-139">Varias columnas se basan en el tipo de cada principal.</span><span class="sxs-lookup"><span data-stu-id="f8996-139">Various columns are based on the type of each principal.</span></span></p>
<p><span data-ttu-id="f8996-140">La mayoría de estos principios son copias almacenadas en caché de los objetos almacenados en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8996-140">Most of these principals are cached copies of objects stored in Active Directory.</span></span> <span data-ttu-id="f8996-141">La creación de la copia en caché en la tabla principal de estos objetos de Active Directory se denomina <em>suministro</em>.</span><span class="sxs-lookup"><span data-stu-id="f8996-141">Creating the cached copy in the Principal table of these Active Directory objects is referred as <em>provisioning</em>.</span></span></p>
<p><span data-ttu-id="f8996-142">Algunas entidades de identidad se crean de forma más agresiva que otras, y algunos objetos de Active Directory se pasan por alto.</span><span class="sxs-lookup"><span data-stu-id="f8996-142">Some principals are created more aggressively than others, and some Active Directory objects are ignored altogether.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8996-143"><a href="lync-server-2013-tblprincipalaffiliations.md">tblPrincipalAffiliations en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-143"><a href="lync-server-2013-tblprincipalaffiliations.md">tblPrincipalAffiliations in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-144">Contiene las afiliaciones principales que describen las pertenencias a grupos de seguridad de Active Directory, contenedores de Active Directory, etc.</span><span class="sxs-lookup"><span data-stu-id="f8996-144">Contains principal affiliations that describe memberships in Active Directory security groups, Active Directory containers, and so on.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-145"><a href="lync-server-2013-tblnode.md">tblNode en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-145"><a href="lync-server-2013-tblnode.md">tblNode in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-146">Contiene el nodo de categoría, administrado en el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f8996-146">Contains the category node, as managed in Lync Server Control Panel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8996-147"><a href="lync-server-2013-tblroletype.md">tblRoleType en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-147"><a href="lync-server-2013-tblroletype.md">tblRoleType in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-148">Contiene tipos de roles y sus conjuntos de permisos asociados.</span><span class="sxs-lookup"><span data-stu-id="f8996-148">Contains role types and their associated permission sets.</span></span> <span data-ttu-id="f8996-149">Esta tabla de búsqueda es estática.</span><span class="sxs-lookup"><span data-stu-id="f8996-149">This lookup table is static.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-150"><a href="lync-server-2013-tblscopeprincipal.md">tblScopePrincipal en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-150"><a href="lync-server-2013-tblscopeprincipal.md">tblScopePrincipal in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-151">Contiene ámbitos asignados a los nodos.</span><span class="sxs-lookup"><span data-stu-id="f8996-151">Contains scopes assigned to nodes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8996-152"><a href="lync-server-2013-tblprincipalrole.md">tblPrincipalRole en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-152"><a href="lync-server-2013-tblprincipalrole.md">tblPrincipalRole in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-153">Contiene roles asignados a nodos.</span><span class="sxs-lookup"><span data-stu-id="f8996-153">Contains roles assigned to nodes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-154"><a href="lync-server-2013-tblsiopwhitelist.md">tblSiopWhiteList en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-154"><a href="lync-server-2013-tblsiopwhitelist.md">tblSiopWhiteList in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-155">Contiene los complementos registrados que se pueden asociar con nodos.</span><span class="sxs-lookup"><span data-stu-id="f8996-155">Contains the registered Add-ins that can be associated with nodes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8996-156"><a href="lync-server-2013-tblenumattribute.md">tblEnumAttribute en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-156"><a href="lync-server-2013-tblenumattribute.md">tblEnumAttribute in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-157">Contiene solo los &quot; &quot; atributos de visibilidad y comportamiento codificados &quot; &quot; que se usan en la tabla tblNode.</span><span class="sxs-lookup"><span data-stu-id="f8996-157">Contains only the hardcoded &quot;Visibility&quot; and &quot;Behavior&quot; attributes that are used in the tblNode table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-158"><a href="lync-server-2013-tblenumvalue.md">tblEnumValue en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-158"><a href="lync-server-2013-tblenumvalue.md">tblEnumValue in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-159">Contiene los valores de los &quot; atributos de comportamiento de visibilidad "y" &quot; que se usan en la tabla tblNode.</span><span class="sxs-lookup"><span data-stu-id="f8996-159">Contains the values of the hardcoded &quot;Visibility” and “Behavior&quot; attributes that are used in the tblNode table.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="invites-chats-and-other-client-support"></a><span data-ttu-id="f8996-160">Invitaciones, chats y otros tipos de asistencia al cliente</span><span class="sxs-lookup"><span data-stu-id="f8996-160">Invites, Chats, and Other Client Support</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8996-161">Tabla</span><span class="sxs-lookup"><span data-stu-id="f8996-161">Table</span></span></th>
<th><span data-ttu-id="f8996-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8996-162">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8996-163"><a href="lync-server-2013-tblprincipalinvites.md">tblPrincipalInvites en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-163"><a href="lync-server-2013-tblprincipalinvites.md">tblPrincipalInvites in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-164">Contiene invitaciones para todos los usuarios aprovisionados del sistema en todos los nodos con la opción de invitación automática habilitada.</span><span class="sxs-lookup"><span data-stu-id="f8996-164">Contains invites for all provisioned users in the system for all nodes with Auto Invite enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-165"><a href="lync-server-2013-tblchat.md">tblChat en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-165"><a href="lync-server-2013-tblchat.md">tblChat in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-166">Contiene todos los mensajes instantáneos.</span><span class="sxs-lookup"><span data-stu-id="f8996-166">Contains all chat messages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8996-167"><a href="lync-server-2013-tbllastinviteid.md">tblLastInviteId en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-167"><a href="lync-server-2013-tbllastinviteid.md">tblLastInviteId in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-168">Contiene el identificador de la última invitación que se generó (y se usó en la tabla tblPrincipalInvites) para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="f8996-168">Contains the last invite ID that was generated (and used in the tblPrincipalInvites table) for each user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-169"><a href="lync-server-2013-tbllastchatid.md">tblLastChatId en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-169"><a href="lync-server-2013-tbllastchatid.md">tblLastChatId in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-170">Contiene el último identificador de chat generado (y usado en la tabla tblChat) para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="f8996-170">Contains the last chat ID that was generated (and used in the tblChat table) for each user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8996-171"><a href="lync-server-2013-tblpreference.md">tblPreference en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-171"><a href="lync-server-2013-tblpreference.md">tblPreference in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-172">Contiene preferencias de clientes de usuario (solo utilizadas por clientes heredados).</span><span class="sxs-lookup"><span data-stu-id="f8996-172">Contains user client preferences (used by legacy clients only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-173"><a href="lync-server-2013-tblfiletoken.md">tblFileToken en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-173"><a href="lync-server-2013-tblfiletoken.md">tblFileToken in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-174">Contiene tokens temporales para la transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="f8996-174">Contains temporary tokens for file transfer purposes.</span></span> <span data-ttu-id="f8996-175">Cada vez que se carga o descarga un archivo, el servicio de chat persistente genera un token que el cliente usa para acceder al almacén de archivos del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="f8996-175">Each time a file is uploaded or downloaded, the Persistent Chat service generates a token that the client uses to access the Web service file store.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="server-support"></a><span data-ttu-id="f8996-176">Compatibilidad con servidores</span><span class="sxs-lookup"><span data-stu-id="f8996-176">Server Support</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8996-177">Tabla</span><span class="sxs-lookup"><span data-stu-id="f8996-177">Table</span></span></th>
<th><span data-ttu-id="f8996-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8996-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8996-179"><a href="lync-server-2013-tblserveridentity.md">tblServerIdentity en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-179"><a href="lync-server-2013-tblserveridentity.md">tblServerIdentity in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-180">Contiene los servidores activos del grupo de servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="f8996-180">Contains the active servers in the Persistent Chat Server pool.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-181"><a href="lync-server-2013-tbladminlock.md">tblAdminLock en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-181"><a href="lync-server-2013-tbladminlock.md">tblAdminLock in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-182">Contiene el bloqueo de administrador para ejecutar algunos comandos de administrador.</span><span class="sxs-lookup"><span data-stu-id="f8996-182">Contains the administrator lock to run some administrator commands.</span></span> <span data-ttu-id="f8996-183">La entrada de revisión del sistema de la tabla tblSystemRevision se incrementa después de cada lanzamiento de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="f8996-183">The system revision entry in the tblSystemRevision table is incremented after each release of the lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8996-184"><a href="lync-server-2013-tblsystemrevision.md">tblSystemRevision en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-184"><a href="lync-server-2013-tblsystemrevision.md">tblSystemRevision in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-185">Contiene la entrada del número de revisión usado (junto con la tabla tblAdminLock) para lograr la coherencia entre varios servidores.</span><span class="sxs-lookup"><span data-stu-id="f8996-185">Contains the revision number entry used (along with the tblAdminLock table) for achieving consistency across multiple servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8996-186"><a href="lync-server-2013-tblactivepeers.md">tblActivePeers en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-186"><a href="lync-server-2013-tblactivepeers.md">tblActivePeers in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-187">Contiene conexiones de punto a punto actuales entre servicios de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="f8996-187">Contains current peer-to-peer connections between Persistent Chat services.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8996-188"><a href="lync-server-2013-tblconfig.md">tblConfig en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f8996-188"><a href="lync-server-2013-tblconfig.md">tblConfig in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="f8996-189">Contiene la configuración no compatible del servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="f8996-189">Contains the Persistent Chat Server unsupported configuration.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f8996-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8996-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

