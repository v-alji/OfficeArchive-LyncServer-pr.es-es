---
title: 'Lync Server 2013: Configurar SQL Server'
description: 'Lync Server 2013: configurar SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure SQL Server
ms:assetid: 84504918-cb4f-4b2f-be17-a70770b69025
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398669(v=OCS.15)
ms:contentKeyID: 48184699
ms.date: 01/22/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2330dc4548e5157b7f29567551df4c89ee15998b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433720"
---
# <a name="configure-sql-server-in-lync-server-2013"></a><span data-ttu-id="d0ca6-103">Configurar SQL Server en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0ca6-103">Configure SQL Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d0ca6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d0ca6-104">

<span> </span></span></span>

<span data-ttu-id="d0ca6-105">_**Última modificación del tema:** 2015-01-22_</span><span class="sxs-lookup"><span data-stu-id="d0ca6-105">_**Topic Last Modified:** 2015-01-22_</span></span>

<span data-ttu-id="d0ca6-106">Para cada base de datos que implemente, puede usar una única instancia de SQL Server para todas las bases de datos de su implementación de Lync Server 2013, que se puede colocar en un servidor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="d0ca6-106">For each database that you deploy, you can use a single SQL Server instance for all databases for your Lync Server 2013 deployment that can be collocated on a database server.</span></span> <span data-ttu-id="d0ca6-107">Para obtener más información sobre collocation de base de datos, consulte [collocation de servidores compatibles en Lync server 2013](lync-server-2013-supported-server-collocation.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="d0ca6-107">For details about database collocation, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md) in the Supportability documentation.</span></span>

<span data-ttu-id="d0ca6-108">Además, cada instancia de SQL Server debe estar instalada y disponible antes de completar los pasos del generador de topología que configure las bases de datos o crear manualmente las bases de datos con los cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d0ca6-108">Additionally, each SQL Server instance must be installed and available prior to completing the steps in Topology Builder that set up the databases, or manually creating the databases with Windows PowerShell cmdlets.</span></span> <span data-ttu-id="d0ca6-109">Para obtener más información sobre la compatibilidad de SQL Server, consulte [configuración de hardware para Lync Server 2013](lync-server-2013-hardware-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d0ca6-109">For details about SQL Server supportability, see [Hardware setup for Lync Server 2013](lync-server-2013-hardware-setup.md).</span></span>

<div>

## <a name="to-install-microsoft-sql-server-2012"></a><span data-ttu-id="d0ca6-110">Para instalar Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0ca6-110">To install Microsoft SQL Server 2012</span></span>

  - <span data-ttu-id="d0ca6-111">Consulte la documentación de Microsoft SQL Server 2012 en: <https://technet.microsoft.com/library/bb500395(v=sql.110).aspx> .</span><span class="sxs-lookup"><span data-stu-id="d0ca6-111">See the Microsoft SQL Server 2012 documentation at: <https://technet.microsoft.com/library/bb500395(v=sql.110).aspx>.</span></span>

<span data-ttu-id="d0ca6-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d0ca6-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

