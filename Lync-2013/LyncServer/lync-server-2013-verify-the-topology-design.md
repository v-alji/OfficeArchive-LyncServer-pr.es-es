---
title: 'Lync Server 2013: Comprobar el diseño de la topología'
description: 'Lync Server 2013: comprobar el diseño de la topología.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify the topology design
ms:assetid: c1b61814-239e-4101-aab0-de3db1d8793c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412951(v=OCS.15)
ms:contentKeyID: 48185311
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cb1e65343aacddbc11d3b909dfdff715503cab93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438914"
---
# <a name="verify-the-topology-design-in-lync-server-2013"></a><span data-ttu-id="8ee39-103">Comprobar el diseño de la topología en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ee39-103">Verify the topology design in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ee39-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ee39-104">

<span> </span></span></span>

<span data-ttu-id="8ee39-105">_**Última modificación del tema:** 2012-01-02_</span><span class="sxs-lookup"><span data-stu-id="8ee39-105">_**Topic Last Modified:** 2012-01-02_</span></span>

<span data-ttu-id="8ee39-106">El generador de topología verifica automáticamente la topología.</span><span class="sxs-lookup"><span data-stu-id="8ee39-106">Topology Builder automatically verifies the topology.</span></span> <span data-ttu-id="8ee39-107">Cualquier error de topología se identifica como un error de validación, indicado por el icono de error de validación junto al rol de servidor.</span><span class="sxs-lookup"><span data-stu-id="8ee39-107">Any topology error is identified as a validation error, indicated by the validation error icon next to the server role.</span></span> <span data-ttu-id="8ee39-108">También es importante comprobar que la topología representa correctamente la topología de la implementación.</span><span class="sxs-lookup"><span data-stu-id="8ee39-108">It is important to also verify that the topology correctly represents the topology for your deployment.</span></span>

<div>

## <a name="to-verify-the-topology-prior-to-publication"></a><span data-ttu-id="8ee39-109">Para comprobar la topología antes de la publicación</span><span class="sxs-lookup"><span data-stu-id="8ee39-109">To verify the topology prior to publication</span></span>

1.  <span data-ttu-id="8ee39-110">Compruebe que todas las URL sencillas están configuradas correctamente.</span><span class="sxs-lookup"><span data-stu-id="8ee39-110">Check that all simple URLs are configured correctly.</span></span>

2.  <span data-ttu-id="8ee39-111">Confirme que el servidor basado en SQL Server está en línea y disponible para el equipo donde el Generador de topologías está instalado, incluidas todas las reglas de firewall necesarias.</span><span class="sxs-lookup"><span data-stu-id="8ee39-111">Confirm that the SQL Server-based server is online and available to the computer where Topology Builder is installed, including any necessary firewall rules.</span></span>

3.  <span data-ttu-id="8ee39-112">Confirme que el recurso compartido de archivos está disponible y que tiene los permisos definidos correctamente.</span><span class="sxs-lookup"><span data-stu-id="8ee39-112">Confirm that the file share is available and has the proper permissions defined.</span></span>

4.  <span data-ttu-id="8ee39-113">Confirme que se han definido en la topología los roles de servidor correctos que cumplen los requisitos de la implementación.</span><span class="sxs-lookup"><span data-stu-id="8ee39-113">Confirm that the correct server roles that meet the deployment requirements are defined in the topology.</span></span>

5.  <span data-ttu-id="8ee39-114">Compruebe que los servidores existen en los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8ee39-114">Verify that the servers exist in Active Directory Domain Services.</span></span> <span data-ttu-id="8ee39-115">Esto ocurrirá automáticamente si ha unido los servidores al dominio.</span><span class="sxs-lookup"><span data-stu-id="8ee39-115">This will happen automatically if you have joined the servers to the domain.</span></span>

<span data-ttu-id="8ee39-116">Tras comprobar la topología y constatar que no hay errores de validación, estará listo para publicar la topología.</span><span class="sxs-lookup"><span data-stu-id="8ee39-116">When you have verified the topology and there are no validation errors, you should be ready to publish the topology.</span></span> <span data-ttu-id="8ee39-117">Si hay errores de validación, debe corregirlos antes de poder publicar la topología.</span><span class="sxs-lookup"><span data-stu-id="8ee39-117">If there are validation errors, you must correct these before you can publish the topology.</span></span> <span data-ttu-id="8ee39-118">Para obtener más información sobre cómo publicar su topología, vea [publicar la topología en Lync Server 2013](lync-server-2013-publish-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="8ee39-118">For details about publishing your topology, see [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md).</span></span>

<span data-ttu-id="8ee39-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ee39-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

