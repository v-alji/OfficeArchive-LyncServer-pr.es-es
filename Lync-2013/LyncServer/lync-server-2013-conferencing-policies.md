---
title: 'Lync Server 2013: directivas de conferencia'
description: 'Lync Server 2013: directivas de conferencia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing policies
ms:assetid: 8f92eb7c-ee66-4df6-a726-4bff93b122cb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688133(v=OCS.15)
ms:contentKeyID: 49733732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6f117cfb077fc24c3e728e208d8bef78cd3284ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434315"
---
# <a name="conferencing-policies-in-lync-server-2013"></a><span data-ttu-id="169d3-103">Directivas de conferencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="169d3-103">Conferencing policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="169d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="169d3-104">

<span> </span></span></span>

<span data-ttu-id="169d3-105">_**Última modificación del tema:** 2012-09-18_</span><span class="sxs-lookup"><span data-stu-id="169d3-105">_**Topic Last Modified:** 2012-09-18_</span></span>

<span data-ttu-id="169d3-106">La Directiva de conferencia define las características y capacidades que los usuarios tienen disponibles durante una conferencia (también conocido como reunión).</span><span class="sxs-lookup"><span data-stu-id="169d3-106">Conferencing policy defines the features and capabilities that users have available during a conference (also known as a meeting).</span></span> <span data-ttu-id="169d3-107">La configuración de directivas de conferencia contiene una amplia variedad de opciones de programación y participación, que van desde si una reunión puede incluir audio y vídeo IP hasta la cantidad máxima de personas que pueden asistir.</span><span class="sxs-lookup"><span data-stu-id="169d3-107">Conferencing policy settings encompass a wide variety of scheduling and participation options, ranging from whether a meeting can include IP audio and video to the maximum number of people who can attend.</span></span> <span data-ttu-id="169d3-108">Los administradores pueden usar la Directiva de conferencia para administrar la seguridad, el ancho de banda y los aspectos legales de las reuniones.</span><span class="sxs-lookup"><span data-stu-id="169d3-108">Administrators can use conferencing policy to manage security, bandwidth, and legal aspects of meetings.</span></span>

<span data-ttu-id="169d3-109">Puede definir la directiva de conferencias en tres niveles: ámbito global, ámbito de sitio y ámbito de usuario.</span><span class="sxs-lookup"><span data-stu-id="169d3-109">You can define conferencing policy on three levels: global scope, site scope, and user scope.</span></span> <span data-ttu-id="169d3-110">La configuración se aplica a un usuario específico del ámbito más limitado al ámbito más extenso.</span><span class="sxs-lookup"><span data-stu-id="169d3-110">Settings apply to a specific user from the narrowest scope to the widest scope.</span></span> <span data-ttu-id="169d3-111">Si asigna una directiva de usuario a un usuario, la configuración tendrá prioridad.</span><span class="sxs-lookup"><span data-stu-id="169d3-111">If you assign a user policy to a user, those settings take precedence.</span></span> <span data-ttu-id="169d3-112">Si no asigna una directiva de usuario, se aplicará la configuración de sitio.</span><span class="sxs-lookup"><span data-stu-id="169d3-112">If you do not assign a user policy, site settings apply.</span></span> <span data-ttu-id="169d3-113">Si no se aplica ni la directiva de usuario ni la de sitio, la directiva global proporcionará la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="169d3-113">If no user or site policies apply, global policy provides the default settings.</span></span>

<span data-ttu-id="169d3-114">Existe una directiva global predeterminada, de modo que no puede crear una nueva directiva global.</span><span class="sxs-lookup"><span data-stu-id="169d3-114">A global policy exists by default, so you cannot create a new global policy.</span></span> <span data-ttu-id="169d3-115">Tampoco puede eliminar la directiva global existente, pero puede cambiar la directiva global para personalizar la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="169d3-115">You also cannot delete the existing global policy, but you can change the existing global policy to customize your default settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="169d3-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="169d3-116">In This Section</span></span>

  - [<span data-ttu-id="169d3-117">Ver información de directiva de conferencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="169d3-117">View conferencing policy information in Lync Server 2013</span></span>](lync-server-2013-view-conferencing-policy-information.md)

  - [<span data-ttu-id="169d3-118">Crear o modificar una directiva de conferencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="169d3-118">Create or modify a conferencing policy in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-conferencing-policy.md)

  - [<span data-ttu-id="169d3-119">Eliminar una directiva de conferencia existente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="169d3-119">Delete an existing conferencing policy in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-conferencing-policy.md)

  - [<span data-ttu-id="169d3-120">Referencia de configuración de directiva de conferencia para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="169d3-120">Conferencing policy settings reference for Lync Server 2013</span></span>](lync-server-2013-conferencing-policy-settings-reference.md)

<span data-ttu-id="169d3-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="169d3-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

