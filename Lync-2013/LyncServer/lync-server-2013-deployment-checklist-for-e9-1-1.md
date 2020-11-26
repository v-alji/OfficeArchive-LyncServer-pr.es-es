---
title: 'Lync Server 2013: lista de comprobación de implementación para E9-1-1'
description: 'Lync Server 2013: lista de comprobación de implementación para E9-1-1.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for E9-1-1
ms:assetid: cc6a656a-6043-4b9b-85c2-5708b9bb1c06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398864(v=OCS.15)
ms:contentKeyID: 48185655
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0c93762e2acef5e065249ced17bfa0eab2f159e4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429716"
---
# <a name="deployment-checklist-for-e9-1-1-in-lync-server-2013"></a><span data-ttu-id="fe6e6-103">Lista de comprobación de implementación para E9-1-1 en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fe6e6-103">Deployment checklist for E9-1-1 in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fe6e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fe6e6-104">

<span> </span></span></span>

<span data-ttu-id="fe6e6-105">_**Última modificación del tema:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="fe6e6-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="fe6e6-106">Para planificar de forma eficaz una 9-1-1 mejorada (E9-1-1), asegúrese de incluir los siguientes requisitos de implementación:</span><span class="sxs-lookup"><span data-stu-id="fe6e6-106">To plan effectively for Enhanced 9-1-1 (E9-1-1), be sure to include the following deployment requirements:</span></span>

  - <span data-ttu-id="fe6e6-107">Requisitos previos para implementar E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-107">Prerequisites for deploying E9-1-1.</span></span>

  - <span data-ttu-id="fe6e6-108">Pasos necesarios para implementar el E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-108">Steps that are required to deploy E9-1-1.</span></span>

<div>

## <a name="deployment-prerequisites-for-e9-1-1"></a><span data-ttu-id="fe6e6-109">Requisitos previos para implementar E9-1-1</span><span class="sxs-lookup"><span data-stu-id="fe6e6-109">Deployment Prerequisites for E9-1-1</span></span>

<span data-ttu-id="fe6e6-110">Antes de implementar E9-1-1, ya debe haber implementado los servidores internos de Lync Server, incluido un almacén de administración central, un grupo front-end o un servidor Standard Edition, uno o varios servidores de mediación o grupos de servidores de mediación y clientes de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-110">Before you deploy E9-1-1, you must already have deployed your Lync Server internal servers, including a Central Management store, a Front End pool or a Standard Edition server, one or more Mediation Servers or Mediation Server pools, and Lync Server clients.</span></span> <span data-ttu-id="fe6e6-111">Además, una implementación de E9-1-1 requiere un tronco SIP con un proveedor de servicios E9-1-1 certificado o una puerta de enlace de número de identificación de ubicación de emergencia (ELIN) a la red telefónica conmutada (RTC).</span><span class="sxs-lookup"><span data-stu-id="fe6e6-111">In addition, an E9-1-1 deployment requires a SIP trunk to a qualified E9-1-1 service provider or an Emergency Location Identification Number (ELIN) gateway to your public switched telephone network (PSTN).</span></span> <span data-ttu-id="fe6e6-112">Lync Server admite el uso de proveedores de servicios de E9-1-1 únicamente en los Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-112">Lync Server supports using E9-1-1 service providers only inside the United States.</span></span>

</div>

<div>

## <a name="deployment-process"></a><span data-ttu-id="fe6e6-113">Proceso de implementación</span><span class="sxs-lookup"><span data-stu-id="fe6e6-113">Deployment Process</span></span>

<span data-ttu-id="fe6e6-114">En la tabla siguiente se proporciona información general del proceso de implementación de E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-114">The following table provides an overview of the E9-1-1 deployment process.</span></span> <span data-ttu-id="fe6e6-115">Para obtener más información sobre los pasos de implementación, vea [configurar 9-1-1 mejorado en Lync Server 2013](lync-server-2013-configure-enhanced-9-1-1.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-115">For details about deployment steps, see [Configure Enhanced 9-1-1 in Lync Server 2013](lync-server-2013-configure-enhanced-9-1-1.md) in the Deployment documentation.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe6e6-116">Fase</span><span class="sxs-lookup"><span data-stu-id="fe6e6-116">Phase</span></span></th>
<th><span data-ttu-id="fe6e6-117">Pasos</span><span class="sxs-lookup"><span data-stu-id="fe6e6-117">Steps</span></span></th>
<th><span data-ttu-id="fe6e6-118">Roles</span><span class="sxs-lookup"><span data-stu-id="fe6e6-118">Roles</span></span></th>
<th><span data-ttu-id="fe6e6-119">Documentación de implementación</span><span class="sxs-lookup"><span data-stu-id="fe6e6-119">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe6e6-120">Realizar configuraciones de tronco, rutas y usos de voz</span><span class="sxs-lookup"><span data-stu-id="fe6e6-120">Configure voice usages, routes, and trunk configurations</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="fe6e6-p103">Cree un registro de uso de RTC. Se trata del mismo nombre que se ha usado para el parámetro <strong>Uso de RTC</strong> en la directiva de ubicación.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-p103">Create a new PSTN usage record. This is the same name that is used for the <strong>PSTN Usage</strong> setting in the location policy.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-123">Cree o asigne una ruta de voz con el registro de uso de RTC creado en el paso anterior y apunte el atributo de puerta de enlace al tronco SIP E9-1-1 o la puerta de enlace ELIN. </span><span class="sxs-lookup"><span data-stu-id="fe6e6-123">Create or assign a voice route to the PSTN usage record created in the previous step and then point the gateway attribute to the E9-1-1 SIP trunk or ELIN gateway.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-124">Para un proveedor de servicios E9-1-1 de tronco SIP, defina el tronco que va a gestionar las llamadas E9-1-1 sobre el SIP para transferir datos PIDF-LO con el cmdlet <strong>Set-CsTrunkConfiguration –EnablePIDFLOSupport</strong>.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-124">For a SIP trunk E9-1-1 service provider, set the trunk that will be handling E9-1-1 calls over the SIP to pass PIDF-LO data by using the <strong>Set-CsTrunkConfiguration –EnablePIDFLOSupport</strong> cmdlet.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-p104">Opcionalmente, para un proveedor de servicios E9-1-1 de tronco SIP, cree o asigne una ruta RTC local para llamadas no gestionadas por el tronco SIP del proveedor de servicios E9-1-1. Esta ruta se usará si la conexión al proveedor de servicios E9-1-1 no está disponible. Si lo admite el proveedor de servicios E9-1-1, asigne una regla de configuración de tronco a la puerta de enlace que convierte la cadena de marcado 911 en el número de llamada directa a la extensión (DID) del Centro de respuesta a llamadas de emergencia nacional y/o regional.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-p104">Optionally, for a SIP trunk E9-1-1 service provider, create or assign a local PSTN route for calls that are not handled by the E9-1-1 service provider’s SIP trunk. This route will be used if the connection to the E9-1-1 service provider is not available. If supported by your E9-1-1 service provider, assign a trunk configuration rule to the gateway that translates the 911 dial string into the direct inward dialing (DID) number of the national/regional Emergency Call Response Center (ECRC).</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="fe6e6-128">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="fe6e6-128">CSVoiceAdmin</span></span></p></td>
<td><p><span data-ttu-id="fe6e6-129"><a href="lync-server-2013-configure-an-e9-1-1-voice-route.md">Configurar una ruta de voz E9-1-1 en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fe6e6-129"><a href="lync-server-2013-configure-an-e9-1-1-voice-route.md">Configure an E9-1-1 voice route in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6e6-130">Crear directivas de ubicación y asignarlas a usuarios y subredes</span><span class="sxs-lookup"><span data-stu-id="fe6e6-130">Create location policies and assign them to users and subnets</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="fe6e6-131">Revise la directiva de ubicación global.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-131">Review the global location policy.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-132">Cree una directiva de ubicación con un ámbito en el nivel de usuario o, si la organización tiene más de un sitio con diferentes usos de emergencia, cree una directiva de ubicación con un ámbito de nivel de red.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-132">Create a location policy with a user-level scope; or, if the organization has more than one site with different emergency usages, create a location policy with a network-level scope.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-133">Asigne la directiva de ubicación a sitios de red.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-133">Assign the location policy to network sites.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-134">Agregue las subredes apropiadas al sitio de red.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-134">Add the appropriate subnets to the network site.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-135">Asigne la directiva de ubicación a directivas de usuario (opcional).</span><span class="sxs-lookup"><span data-stu-id="fe6e6-135">(Optional) Assign the location policy to user policies.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="fe6e6-136">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="fe6e6-136">CSVoiceAdmin</span></span></p>
<p><span data-ttu-id="fe6e6-137">CSLocationAdmin (excepto para crear directivas de ubicación)</span><span class="sxs-lookup"><span data-stu-id="fe6e6-137">CSLocationAdmin (except for creating Location Policies)</span></span></p></td>
<td><p><span data-ttu-id="fe6e6-138"><a href="lync-server-2013-create-location-policies.md">Crear directivas de ubicación en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fe6e6-138"><a href="lync-server-2013-create-location-policies.md">Create location policies in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="fe6e6-139"><a href="lync-server-2013-add-a-location-policy-to-a-network-site.md">Agregar una directiva de ubicación a un sitio de red en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fe6e6-139"><a href="lync-server-2013-add-a-location-policy-to-a-network-site.md">Add a location policy to a network site in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="fe6e6-140"><a href="lync-server-2013-associate-subnets-with-network-sites-for-e9-1-1.md">Asociar subredes con sitios de red para E9-1-1 en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fe6e6-140"><a href="lync-server-2013-associate-subnets-with-network-sites-for-e9-1-1.md">Associate subnets with network sites for E9-1-1 in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6e6-141">Configurar la base de datos de ubicaciones</span><span class="sxs-lookup"><span data-stu-id="fe6e6-141">Configure the location database</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="fe6e6-142">Rellene la base de datos con asignaciones de elementos de red a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-142">Populate the database with a mapping of network elements to locations.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-143">Para las puertas de enlace ELIN, agregue la ELINs a la &lt; &gt; columna NombreCompañía.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-143">For ELIN gateways, add the ELINs to the &lt;CompanyName&gt; column.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-144">Configure la conexión con el proveedor de servicios de E9-1-1 para validar las direcciones.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-144">Configure the connection to the E9-1-1 service provider for validating addresses.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-145">Valide las direcciones con el proveedor de servicios E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-145">Validate the addresses with the E9-1-1 service provider.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-146">Publique la base de datos actualizada.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-146">Publish the updated database.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-147">Para las puertas de enlace ELIN, cargue los ELIN en la base de datos de identificación automática de ubicaciones (ALI) del proveedor de RTC.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-147">For ELIN gateways, upload the ELINs to your PSTN carrier's Automatic Location Identification (ALI) database.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="fe6e6-148">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="fe6e6-148">CSVoiceAdmin</span></span></p>
<p><span data-ttu-id="fe6e6-149">CSLocationAdmin</span><span class="sxs-lookup"><span data-stu-id="fe6e6-149">CSLocationAdmin</span></span></p></td>
<td><p><span data-ttu-id="fe6e6-150"><a href="lync-server-2013-configure-the-location-database.md">Configure the location database in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fe6e6-150"><a href="lync-server-2013-configure-the-location-database.md">Configure the location database in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6e6-151">Configurar características avanzadas (opcional)</span><span class="sxs-lookup"><span data-stu-id="fe6e6-151">Configure Advanced Features (optional)</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="fe6e6-152">Configure la dirección URL de la aplicación SNMP.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-152">Configure the URL for the SNMP application.</span></span></p></li>
<li><p><span data-ttu-id="fe6e6-153">Configure la dirección URL para la ubicación del servicio de información de ubicación secundaria.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-153">Configure the URL for the location of the Secondary Location Information service.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="fe6e6-154">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="fe6e6-154">CSVoiceAdmin</span></span></p></td>
<td><p><span data-ttu-id="fe6e6-155"><a href="lync-server-2013-configure-an-snmp-application.md">Configurar una aplicación SNMP en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fe6e6-155"><a href="lync-server-2013-configure-an-snmp-application.md">Configure an SNMP application in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="fe6e6-156"><a href="lync-server-2013-configure-a-secondary-location-information-service.md">Configurar un servicio de información de ubicación secundaria en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="fe6e6-156"><a href="lync-server-2013-configure-a-secondary-location-information-service.md">Configure a secondary Location Information service in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fe6e6-157">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fe6e6-157">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

