---
title: 'Lync Server 2013: Configurar una conferencia de acceso telefónico local'
description: 'Lync Server 2013: configuración de conferencias de acceso telefónico local.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring dial-in conferencing
ms:assetid: 79a98c5d-a0a8-4729-828d-b9166842432c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398600(v=OCS.15)
ms:contentKeyID: 48184587
ms.date: 10/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9c3353caa1344b717b0f64c271149f078f194e5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433209"
---
# <a name="configuring-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="328ac-103">Configurar una conferencia de acceso telefónico local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-103">Configuring dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="328ac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="328ac-104">

<span> </span></span></span>

<span data-ttu-id="328ac-105">_**Última modificación del tema:** 2014-10-03_</span><span class="sxs-lookup"><span data-stu-id="328ac-105">_**Topic Last Modified:** 2014-10-03_</span></span>

<span data-ttu-id="328ac-106">Esta sección le guiará a través de la configuración de las conferencias de acceso telefónico local de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="328ac-106">This section guides you through the configuration of Lync Server 2013 dial-in conferencing.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="328ac-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="328ac-107">In This Section</span></span>

  - [<span data-ttu-id="328ac-108">Requisitos previos y permisos de configuración para conferencias de acceso telefónico en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-108">Dial-in conferencing configuration prerequisites and permissions in Lync Server 2013</span></span>](lync-server-2013-dial-in-conferencing-configuration-prerequisites-and-permissions.md)

  - [<span data-ttu-id="328ac-109">Lista de comprobación para la implementación de las conferencias de acceso telefónico local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-109">Deployment checklist for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-dial-in-conferencing.md)

  - [<span data-ttu-id="328ac-110">Configurar planes de marcado para las conferencias de acceso telefónico local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-110">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md)

  - [<span data-ttu-id="328ac-111">Asegúrese de que los planes de marcado de Lync Server 2013 tienen regiones asignadas</span><span class="sxs-lookup"><span data-stu-id="328ac-111">Make sure dial plans Lync Server 2013 have assigned regions</span></span>](lync-server-2013-make-sure-dial-plans-have-assigned-regions.md)

  - [<span data-ttu-id="328ac-112">(Opcional) Comprobar la configuración de la directiva de PIN en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-112">(Optional) Verify PIN policy settings in Lync Server 2013</span></span>](lync-server-2013-optional-verify-pin-policy-settings.md)

  - [<span data-ttu-id="328ac-113">Configurar la directiva de conferencias para el acceso telefónico local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-113">Configure conferencing policy for dial-in in Lync Server 2013</span></span>](lync-server-2013-configure-conferencing-policy-for-dial-in.md)

  - [<span data-ttu-id="328ac-114">Configurar números de conferencia de acceso telefónico en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-114">Configure dial-in conferencing access numbers in Lync Server 2013</span></span>](lync-server-2013-configure-dial-in-conferencing-access-numbers.md)

  - [<span data-ttu-id="328ac-115">(Opcional) Comprobar la configuración de conferencia de acceso telefónico local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-115">(Optional) Verify dial-in conferencing settings in Lync Server 2013</span></span>](lync-server-2013-optional-verify-dial-in-conferencing-settings.md)

  - [<span data-ttu-id="328ac-116">(Opcional) Modificar la asignación de teclas para comandos DTMF en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-116">(Optional) Modify key mapping for DTMF commands in Lync Server 2013</span></span>](lync-server-2013-optional-modify-key-mapping-for-dtmf-commands.md)

  - [<span data-ttu-id="328ac-117">(Opcional) Habilitar y deshabilitar los anuncios de participación y abandono de conferencias en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-117">(Optional) Enable and disable conference join and leave announcements in Lync Server 2013</span></span>](lync-server-2013-optional-enable-and-disable-conference-join-and-leave-announcements.md)

  - [<span data-ttu-id="328ac-118">(Opcional) Comprobar la conferencia de acceso telefónico local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-118">(Optional) Verify dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-optional-verify-dial-in-conferencing.md)

  - [<span data-ttu-id="328ac-119">Implementar el complemento de conferencia en línea para Lync 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-119">Deploy the Online Meeting Add-in for Lync 2013</span></span>](lync-server-2013-deploy-the-online-meeting-add-in-for-lync-2013.md)

  - [<span data-ttu-id="328ac-120">Configurar la cuenta de usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-120">Configure user account settings in Lync Server 2013</span></span>](lync-server-2013-configure-user-account-settings.md)

  - [<span data-ttu-id="328ac-121">(Recommended) Create Conference Directories</span><span class="sxs-lookup"><span data-stu-id="328ac-121">(Recommended) Create Conference Directories</span></span>](recommended-create-conference-directories.md)

  - [<span data-ttu-id="328ac-122">(Opcional) Dar la bienvenida a los usuarios de la conferencia de acceso telefónico local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-122">(Optional) Welcome users to dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-optional-welcome-users-to-dial-in-conferencing.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="328ac-123">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="328ac-123">Related Sections</span></span>

[<span data-ttu-id="328ac-124">Implementar Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="328ac-124">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)

<span data-ttu-id="328ac-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="328ac-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

