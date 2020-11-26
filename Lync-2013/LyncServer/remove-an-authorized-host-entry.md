---
title: Quitar una entrada de host autorizado
description: Quitar una entrada de host autorizado.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove an authorized host entry
ms:assetid: 56a04140-347e-4eef-bede-0e858534f71e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204902(v=OCS.15)
ms:contentKeyID: 48184177
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95aa8df1745ad3108654fcb9b441b5919d42ec40
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443261"
---
# <a name="remove-an-authorized-host-entry"></a><span data-ttu-id="54bfa-103">Quitar una entrada de host autorizado</span><span class="sxs-lookup"><span data-stu-id="54bfa-103">Remove an authorized host entry</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="54bfa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="54bfa-104">

<span> </span></span></span>

<span data-ttu-id="54bfa-105">_**Última modificación del tema:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="54bfa-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="54bfa-106">En este tema se describe cómo quitar una entrada de host autorizado heredado (conocida como *entrada de aplicación de confianza* en Lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="54bfa-106">This topic describes how to remove a legacy authorized host entry (known as a *trusted application entry* in Lync Server 2013).</span></span> <span data-ttu-id="54bfa-107">Debe quitar las entradas de host autorizado existentes para las puertas de enlace SIP/CSTA de su implementación de Office Communications Server 2007 R2 al migrar el control de llamadas remotas a una implementación de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="54bfa-107">You must remove existing authorized host entries for any SIP/CSTA gateways in your Office Communications Server 2007 R2 deployment when you migrate remote call control to a Lync Server 2013 deployment.</span></span> <span data-ttu-id="54bfa-108">Debe usar las herramientas administrativas incluidas en Office Communications Server 2007 R2 para quitar las entradas de host autorizadas existentes.</span><span class="sxs-lookup"><span data-stu-id="54bfa-108">You must use the administrative tools included with Office Communications Server 2007 R2 to remove the existing authorized host entries.</span></span>

<div>

## <a name="to-remove-an-authorized-host-entry-in-an-office-communications-server-2007-r2-deployment"></a><span data-ttu-id="54bfa-109">Para quitar una entrada de host autorizado en una implementación de Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="54bfa-109">To remove an authorized host entry in an Office Communications Server 2007 R2 deployment</span></span>

1.  <span data-ttu-id="54bfa-110">Abra la consola administrativa de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="54bfa-110">Open the Office Communications Server 2007 R2 administrative console.</span></span>

2.  <span data-ttu-id="54bfa-111">Expanda el árbol y haga clic con el botón secundario en el grupo en el que se creó el host autorizado.</span><span class="sxs-lookup"><span data-stu-id="54bfa-111">Expand the tree and right-click the pool where the authorized host was created.</span></span>

3.  <span data-ttu-id="54bfa-112">Haga clic en **propiedades** y, a continuación, en **propiedades de front-end**.</span><span class="sxs-lookup"><span data-stu-id="54bfa-112">Click **Properties**, and then click **Front End Properties**.</span></span>

4.  <span data-ttu-id="54bfa-113">Haga clic en la pestaña **autorización del host** .</span><span class="sxs-lookup"><span data-stu-id="54bfa-113">Click the **Host Authorization** tab.</span></span>

5.  <span data-ttu-id="54bfa-114">Seleccione un servidor y haga clic en **quitar**.</span><span class="sxs-lookup"><span data-stu-id="54bfa-114">Select a server, and then click **Remove**.</span></span>

6.  <span data-ttu-id="54bfa-115">En **propiedades**, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="54bfa-115">In **Properties**, click **OK**.</span></span>

<span data-ttu-id="54bfa-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="54bfa-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

