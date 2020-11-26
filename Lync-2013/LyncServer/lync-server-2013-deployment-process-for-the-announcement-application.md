---
title: 'Lync Server 2013: proceso de implementación para la aplicación de anuncios'
description: 'Lync Server 2013: proceso de implementación para la aplicación de anuncios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for the Announcement application
ms:assetid: 72c66249-c4ce-48ce-b1b9-90ebf77d7805
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398545(v=OCS.15)
ms:contentKeyID: 48184500
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 559977c32f63fae312164b5b0c36698fa13afb09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429646"
---
# <a name="deployment-process-for-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="b9c72-103">Proceso de implementación para la aplicación de anuncios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b9c72-103">Deployment process for the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b9c72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b9c72-104">

<span> </span></span></span>

<span data-ttu-id="b9c72-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="b9c72-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="b9c72-106">Esta sección proporciona una descripción general de los pasos necesarios para implementar la aplicación de anuncios.</span><span class="sxs-lookup"><span data-stu-id="b9c72-106">This section provides an overview of the steps involved in deploying the Announcement application.</span></span> <span data-ttu-id="b9c72-107">Debe implementar la telefonía IP empresarial antes de configurar los anuncios.</span><span class="sxs-lookup"><span data-stu-id="b9c72-107">You must deploy Enterprise Voice before you configure announcements.</span></span> <span data-ttu-id="b9c72-108">Los componentes requeridos por la aplicación de anuncios se instalan y se habilitan al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="b9c72-108">The components required by the Announcement application are installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="announcement-deployment-process"></a><span data-ttu-id="b9c72-109">Proceso de implementación de anuncios</span><span class="sxs-lookup"><span data-stu-id="b9c72-109">Announcement Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9c72-110">Fase</span><span class="sxs-lookup"><span data-stu-id="b9c72-110">Phase</span></span></th>
<th><span data-ttu-id="b9c72-111">Pasos</span><span class="sxs-lookup"><span data-stu-id="b9c72-111">Steps</span></span></th>
<th><span data-ttu-id="b9c72-112">Roles</span><span class="sxs-lookup"><span data-stu-id="b9c72-112">Roles</span></span></th>
<th><span data-ttu-id="b9c72-113">Documentación de implementación</span><span class="sxs-lookup"><span data-stu-id="b9c72-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9c72-114">Configurar opciones de anuncio</span><span class="sxs-lookup"><span data-stu-id="b9c72-114">Configure Announcement settings</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="b9c72-115">Cree el anuncio grabando y cargando archivos de audio, o bien usando texto a voz (TTS).</span><span class="sxs-lookup"><span data-stu-id="b9c72-115">Create the announcement by recording and uploading audio files or by using text-to-speech (TTS).</span></span></p></li>
<li><p><span data-ttu-id="b9c72-116">Configure los intervalos de números no asignados de la tabla de números no asignados y asócielos al anuncio correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b9c72-116">Configure the unassigned number ranges in the unassigned number table and associate them with the appropriate announcement.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b9c72-117">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="b9c72-117">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="b9c72-118">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="b9c72-118">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="b9c72-119">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="b9c72-119">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="b9c72-120">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="b9c72-120">CsAdministrator</span></span></p>
<p><span data-ttu-id="b9c72-121">CsViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="b9c72-121">CsViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="b9c72-122"><a href="lync-server-2013-create-an-announcement.md">Crear un anuncio en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b9c72-122"><a href="lync-server-2013-create-an-announcement.md">Create an announcement in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="b9c72-123"><a href="lync-server-2013-configure-the-unassigned-number-table.md">Configurar la tabla de números sin asignar en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b9c72-123"><a href="lync-server-2013-configure-the-unassigned-number-table.md">Configure the unassigned number table in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9c72-124">Comprobar la implementación de anuncios</span><span class="sxs-lookup"><span data-stu-id="b9c72-124">Verify your Announcement deployment</span></span></p></td>
<td><p><span data-ttu-id="b9c72-125">Escuche los anuncios para comprobar que la configuración funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b9c72-125">Test by listening to announcements to verify that your configuration works as expected.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="b9c72-126"><a href="lync-server-2013-optional-verify-announcement-deployment.md">Faculta Comprobar la implementación de la presentación en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b9c72-126"><a href="lync-server-2013-optional-verify-announcement-deployment.md">(Optional) Verify Announcement deployment in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b9c72-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b9c72-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

