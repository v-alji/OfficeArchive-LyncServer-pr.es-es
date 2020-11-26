---
title: 'Lync Server 2013: tblComplianceState'
description: 'Lync Server 2013: tblComplianceState'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceState
ms:assetid: ea82e56c-3cca-4d89-b4e6-6bcaeb1f2830
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615045(v=OCS.15)
ms:contentKeyID: 48185937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6eaf35eee8b4e24ec4d04e607fa77fd91b91e4e8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423515"
---
# <a name="tblcompliancestate-in-lync-server-2013"></a><span data-ttu-id="5fa59-103">tblComplianceState en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5fa59-103">tblComplianceState in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5fa59-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5fa59-104">

<span> </span></span></span>

<span data-ttu-id="5fa59-105">_**Última modificación del tema:** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="5fa59-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="5fa59-106">tblComplianceState contiene información de estado de cumplimiento para todo el grupo.</span><span class="sxs-lookup"><span data-stu-id="5fa59-106">tblComplianceState contains pool-wide compliance state information.</span></span>

### <a name="columns"></a><span data-ttu-id="5fa59-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="5fa59-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5fa59-108">Columna</span><span class="sxs-lookup"><span data-stu-id="5fa59-108">Column</span></span></th>
<th><span data-ttu-id="5fa59-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fa59-109">Type</span></span></th>
<th><span data-ttu-id="5fa59-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fa59-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fa59-111">lastProcessedEntryID</span><span class="sxs-lookup"><span data-stu-id="5fa59-111">lastProcessedEntryID</span></span></p></td>
<td><p><span data-ttu-id="5fa59-112">BIGINT, not null</span><span class="sxs-lookup"><span data-stu-id="5fa59-112">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="5fa59-113">IDENTIFICADOR del último evento de cumplimiento procesado.</span><span class="sxs-lookup"><span data-stu-id="5fa59-113">ID of the latest processed compliance event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fa59-114">activeServerID</span><span class="sxs-lookup"><span data-stu-id="5fa59-114">activeServerID</span></span></p></td>
<td><p><span data-ttu-id="5fa59-115">int, not null</span><span class="sxs-lookup"><span data-stu-id="5fa59-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="5fa59-116">IDENTIFICADOR del servidor de cumplimiento que contiene el bloqueo exclusivo de la base de datos, o bien-1 si no hay ninguno.</span><span class="sxs-lookup"><span data-stu-id="5fa59-116">ID of the Compliance server holding the exclusive lock on the database, or -1 if none.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fa59-117">lockExpirationTime</span><span class="sxs-lookup"><span data-stu-id="5fa59-117">lockExpirationTime</span></span></p></td>
<td><p><span data-ttu-id="5fa59-118">datetime2, not null</span><span class="sxs-lookup"><span data-stu-id="5fa59-118">datetime2, not null</span></span></p></td>
<td><p><span data-ttu-id="5fa59-119">Fecha de expiración de bloqueo (si activeServerID no es-1).</span><span class="sxs-lookup"><span data-stu-id="5fa59-119">Lock expiration time (if activeServerID is not -1).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5fa59-120">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5fa59-120">


</div>

<span> </span>

</div>

</div>

</span></span></div>

