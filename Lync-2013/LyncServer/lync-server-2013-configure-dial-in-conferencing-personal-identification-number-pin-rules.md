---
title: Configurar las reglas de número de identificación personal (PIN) de las conferencias de acceso telefónico local
description: Configurar las reglas de número de identificación personal (PIN) de las conferencias de acceso telefónico local.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial-in conferencing personal identification number (PIN) rules
ms:assetid: 27b79fb1-e2dc-4f71-bc82-b6eb61be2b16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520967(v=OCS.15)
ms:contentKeyID: 48183668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 799092ba57e9a85cd196840fc81c1f46b96e9900
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399912"
---
# <a name="configure-dial-in-conferencing-personal-identification-number-pin-rules-in-lync-server-2013"></a><span data-ttu-id="a0d33-103">Configurar las reglas de número de identificación personal (PIN) de conferencias de acceso telefónico local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0d33-103">Configure dial-in conferencing personal identification number (PIN) rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0d33-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0d33-104">

<span> </span></span></span>

<span data-ttu-id="a0d33-105">_**Última modificación del tema:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="a0d33-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="a0d33-106">Los usuarios de Lync Server 2013 que tienen credenciales de servicios de dominio de Active Directory (AD DS) en su organización pueden unirse a conferencias de acceso telefónico local como usuarios autenticados mediante un número de identificación personal (PIN).</span><span class="sxs-lookup"><span data-stu-id="a0d33-106">Lync Server 2013 users who have Active Directory Domain Services (AD DS) credentials in your organization can join dial-in conferences as authenticated users by using a personal identification number (PIN).</span></span> <span data-ttu-id="a0d33-107">La directiva de PIN define las reglas de funcionamiento de los PIN de conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="a0d33-107">PIN policy defines the rules for how dial-in conferencing PINs work.</span></span>

<span data-ttu-id="a0d33-108">Puede crear una nueva directiva de PIN si desea aplicar una directiva específica a un sitio a un grupo de usuarios determinado.</span><span class="sxs-lookup"><span data-stu-id="a0d33-108">You can create a new PIN policy if you want a specific policy to apply to a site or to a certain group of users.</span></span> <span data-ttu-id="a0d33-109">Si desea usar la misma directiva de PIN para toda la organización, puede usar la directiva de PIN global y modificarla según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a0d33-109">If you want to use the same PIN policy for your entire organization, you can use the global PIN policy and modify it as needed.</span></span> <span data-ttu-id="a0d33-110">Las directivas de PIN se aplican a usuarios que van del ámbito más limitado al ámbito más extenso.</span><span class="sxs-lookup"><span data-stu-id="a0d33-110">PIN policies apply to users from the narrowest scope to the widest scope.</span></span> <span data-ttu-id="a0d33-111">Si asigna una directiva de PIN de usuario a un usuario, esa configuración tendrá preferencia.</span><span class="sxs-lookup"><span data-stu-id="a0d33-111">If you assign a user-level PIN policy to a user, those settings take precedence.</span></span> <span data-ttu-id="a0d33-112">Si no asigna una directiva de usuario, se aplica la directiva de PIN de sitio, si existe.</span><span class="sxs-lookup"><span data-stu-id="a0d33-112">If you do not assign a user policy, the site-level PIN policy applies, if it exists.</span></span> <span data-ttu-id="a0d33-113">Si no se aplica ni la directiva de usuario ni la de sitio, la directiva de PIN global proporcionará la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a0d33-113">If no user or site policies apply, global PIN policy provides the default settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a0d33-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a0d33-114">In This Section</span></span>

  - [<span data-ttu-id="a0d33-115">Modificar la configuración del PIN de la conferencia de acceso telefónico local predeterminada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0d33-115">Modify the default dial-in conferencing PIN settings in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-dial-in-conferencing-pin-settings.md)

  - [<span data-ttu-id="a0d33-116">Crear o modificar la configuración de PIN de conferencia de acceso telefónico local para un sitio o grupo de usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0d33-116">Create or modify dial-in conferencing PIN settings in Lync Server 2013 for a site or group of users</span></span>](lync-server-2013-create-or-modify-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users.md)

  - [<span data-ttu-id="a0d33-117">Eliminar la configuración del PIN de conferencias de acceso telefónico local para un sitio o grupo de usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0d33-117">Delete dial-in conferencing PIN settings for a site or group of users in Lync Server 2013</span></span>](lync-server-2013-delete-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users.md)

<span data-ttu-id="a0d33-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0d33-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

