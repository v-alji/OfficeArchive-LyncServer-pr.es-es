---
title: 'Lync Server 2013: Implementar el almacenamiento de contactos unificado'
description: 'Lync Server 2013: implementación de almacenamiento de contactos unificado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying unified contact store
ms:assetid: 68959d58-ac8a-45de-afcd-b9de2c36799c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204963(v=OCS.15)
ms:contentKeyID: 48184373
ms.date: 06/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 056792d2e4ea66699b276d0d571e83c8a0256483
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398189"
---
# <a name="deploying-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="b32e4-103">Implementar el almacenamiento de contactos unificado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b32e4-103">Deploying unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b32e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b32e4-104">

<span> </span></span></span>

<span data-ttu-id="b32e4-105">_**Última modificación del tema:** 2016-06-06_</span><span class="sxs-lookup"><span data-stu-id="b32e4-105">_**Topic Last Modified:** 2016-06-06_</span></span>

<span data-ttu-id="b32e4-106">Habilitar el almacén de contactos unificado en Lync Server 2013 no requiere ninguna configuración de topología.</span><span class="sxs-lookup"><span data-stu-id="b32e4-106">Enabling unified contact store in Lync Server 2013 does not require any topology settings.</span></span> <span data-ttu-id="b32e4-107">Para habilitar el almacén de contactos unificado para los usuarios, necesita lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b32e4-107">Enabling unified contact store for users requires the following:</span></span>

  - <span data-ttu-id="b32e4-108">La directiva del almacén de contactos unificado está habilitada (que es el comportamiento predeterminado).</span><span class="sxs-lookup"><span data-stu-id="b32e4-108">Unified contact store policy is enabled (default is enabled).</span></span>

  - <span data-ttu-id="b32e4-109">Los usuarios inician sesión en Lync 2013 al menos una vez.</span><span class="sxs-lookup"><span data-stu-id="b32e4-109">Users log in with Lync 2013 at least once.</span></span>

<span data-ttu-id="b32e4-110">Después de migrar los contactos de un usuario, lo cual sucede automáticamente cuando un usuario inicia sesión con Lync 2013, el usuario puede tener acceso y administrar sus contactos de Lync desde Lync 2013, Outlook 2013 o Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="b32e4-110">After a user’s contacts have been migrated, which happens automatically when a user logs in with Lync 2013, the user can access and manage their Lync contacts from Lync 2013, Outlook 2013, or Outlook Web Access.</span></span> <span data-ttu-id="b32e4-111">El usuario no tiene que haber iniciado sesión en Lync para administrar sus contactos desde Outlook o Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="b32e4-111">The user does not have to be logged in to Lync to manage their contacts from Outlook or Outlook Web Access.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b32e4-112">Si un usuario inicia sesión desde Lync 2010 después de la migración, los contactos y grupos están disponibles y actualizados, pero el usuario no puede administrarlos (es decir, agregar, eliminar, mover, etiquetar, quitar o modificar) esos contactos.</span><span class="sxs-lookup"><span data-stu-id="b32e4-112">If a user logs in from Lync 2010 after migration, contacts and groups are available and up-to-date, but the user cannot manage (that is, add, delete, move, tag, untag, or modify) those contacts.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b32e4-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b32e4-113">In This Section</span></span>

  - [<span data-ttu-id="b32e4-114">Habilitar usuarios para el almacenamiento de contactos unificado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b32e4-114">Enable users for unified contact store in Lync Server 2013</span></span>](lync-server-2013-enable-users-for-unified-contact-store.md)

  - [<span data-ttu-id="b32e4-115">Realizar la migración de usuarios a almacén de contactos unificados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b32e4-115">Migrate users to unified contact store in Lync Server 2013</span></span>](lync-server-2013-migrate-users-to-unified-contact-store.md)

  - [<span data-ttu-id="b32e4-116">Revertir usuarios migrados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b32e4-116">Roll back migrated users in Lync Server 2013</span></span>](lync-server-2013-roll-back-migrated-users.md)

<span data-ttu-id="b32e4-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b32e4-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

