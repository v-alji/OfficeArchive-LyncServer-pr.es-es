---
title: 'Lync Server 2013: tblADCookie'
description: 'Lync Server 2013: tblADCookie'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADCookie
ms:assetid: 0a9102c4-47aa-40ea-8a0d-20e72ab09848
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558610(v=OCS.15)
ms:contentKeyID: 48183366
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 41c3dde3730ede07b204a473c7fe0a5ab68054d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398729"
---
# <a name="tbladcookie-in-lync-server-2013"></a><span data-ttu-id="a752f-103">tblADCookie en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a752f-103">tblADCookie in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a752f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a752f-104">

<span> </span></span></span>

<span data-ttu-id="a752f-105">_**Última modificación del tema:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="a752f-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="a752f-106">tblADCookie contiene las cookies de sincronización LDAP (Protocolo ligero de acceso a directorios) actuales.</span><span class="sxs-lookup"><span data-stu-id="a752f-106">tblADCookie contains the current Lightweight Directory Access Protocol (LDAP) Sync cookies.</span></span>

### <a name="columns"></a><span data-ttu-id="a752f-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="a752f-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a752f-108">Columna</span><span class="sxs-lookup"><span data-stu-id="a752f-108">Column</span></span></th>
<th><span data-ttu-id="a752f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a752f-109">Type</span></span></th>
<th><span data-ttu-id="a752f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a752f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a752f-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="a752f-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="a752f-112">GUID, not null</span><span class="sxs-lookup"><span data-stu-id="a752f-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="a752f-113">GUID principal del dominio que se está supervisando.</span><span class="sxs-lookup"><span data-stu-id="a752f-113">Principal GUID of the domain being monitored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a752f-114">prinDCHost</span><span class="sxs-lookup"><span data-stu-id="a752f-114">prinDCHost</span></span></p></td>
<td><p><span data-ttu-id="a752f-115">nvarchar (255)</span><span class="sxs-lookup"><span data-stu-id="a752f-115">nvarchar (255)</span></span></p></td>
<td><p><span data-ttu-id="a752f-116">Nombre de dominio completo (FQDN) del controlador de dominio actual usado para la sincronización de servicios de dominio de Active Directory. Tiene valor informativo.</span><span class="sxs-lookup"><span data-stu-id="a752f-116">Fully qualified domain name (FQDN) of the current domain controller used for Active Directory Domain Services Sync. Has informational value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a752f-117">adcContent</span><span class="sxs-lookup"><span data-stu-id="a752f-117">adcContent</span></span></p></td>
<td><p><span data-ttu-id="a752f-118">imagen (binario)</span><span class="sxs-lookup"><span data-stu-id="a752f-118">image (binary)</span></span></p></td>
<td><p><span data-ttu-id="a752f-119">Cookie de sincronización de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a752f-119">Active Directory Sync cookie.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a752f-120">lastUpdated</span><span class="sxs-lookup"><span data-stu-id="a752f-120">lastUpdated</span></span></p></td>
<td><p><span data-ttu-id="a752f-121">datetime</span><span class="sxs-lookup"><span data-stu-id="a752f-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="a752f-122">Marca de tiempo con la hora de actualización de la fila.</span><span class="sxs-lookup"><span data-stu-id="a752f-122">Time stamp with the row update time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a752f-123">lockedUntil</span><span class="sxs-lookup"><span data-stu-id="a752f-123">lockedUntil</span></span></p></td>
<td><p><span data-ttu-id="a752f-124">datetime</span><span class="sxs-lookup"><span data-stu-id="a752f-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="a752f-125">Tiempo hasta que se bloquean los cambios en la fila.</span><span class="sxs-lookup"><span data-stu-id="a752f-125">Time until the row is locked for changes.</span></span> <span data-ttu-id="a752f-126">Esto forma parte de un mecanismo de interbloqueo de software que garantiza que solo uno de los servicios de chat realiza la sincronización de Active Directory a la vez.</span><span class="sxs-lookup"><span data-stu-id="a752f-126">This is part of a software interlock mechanism that ensures that only one of the chat services does the Active Directory Sync at a time.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="a752f-127">Sus</span><span class="sxs-lookup"><span data-stu-id="a752f-127">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a752f-128">Columna (s)</span><span class="sxs-lookup"><span data-stu-id="a752f-128">Column(s)</span></span></th>
<th><span data-ttu-id="a752f-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="a752f-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a752f-130">prinGuid</span><span class="sxs-lookup"><span data-stu-id="a752f-130">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="a752f-131">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="a752f-131">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a752f-132">prinGuid</span><span class="sxs-lookup"><span data-stu-id="a752f-132">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="a752f-133">Clave externa con la búsqueda en la tabla principal. prinGuid.</span><span class="sxs-lookup"><span data-stu-id="a752f-133">Foreign key with lookup in Principal.prinGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a752f-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a752f-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

