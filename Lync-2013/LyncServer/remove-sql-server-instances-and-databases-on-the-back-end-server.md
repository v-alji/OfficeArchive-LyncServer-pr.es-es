---
title: Quitar instancias de SQL Server y bases de datos en el servidor back-end
description: Quitar instancias y bases de datos de SQL Server en el servidor back-end.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove SQL Server instances and databases on the Back End Server
ms:assetid: 32457df9-7dd9-4fca-9362-ea4de26b0296
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688016(v=OCS.15)
ms:contentKeyID: 49733606
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c87426a3496e6def2ad65775f5dadb1a0141ae3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400097"
---
# <a name="remove-sql-server-instances-and-databases-on-the-back-end-server"></a><span data-ttu-id="3c74c-103">Quitar instancias de SQL Server y bases de datos en el servidor back-end</span><span class="sxs-lookup"><span data-stu-id="3c74c-103">Remove SQL Server instances and databases on the Back End Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3c74c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3c74c-104">

<span> </span></span></span>

<span data-ttu-id="3c74c-105">_**Última modificación del tema:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="3c74c-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="3c74c-106">Puede quitar las bases de datos y las instancias de Microsoft SQL Server después de quitar los servidores que ejecutan Lync Server 2010 que dependen de ellos o después de volver a configurar los servidores que ejecutan Lync Server 2010 para usar otra base de datos.</span><span class="sxs-lookup"><span data-stu-id="3c74c-106">You remove the Microsoft SQL Server databases and instances after you remove the servers running Lync Server 2010 that are dependent on them, or after you reconfigure the servers running Lync Server 2010 to use another database.</span></span> <span data-ttu-id="3c74c-107">Debe realizar el procedimiento de este tema cuando retire el servidor SQL Server actual o vuelva a configurar el servidor actual que ejecuta Lync Server 2010 de tal forma que represente las bases de datos obsoletas o no disponibles.</span><span class="sxs-lookup"><span data-stu-id="3c74c-107">You need to perform the procedure in this topic when you retire the current SQL Server or reconfigure the current server running Lync Server 2010 in such a way that it renders the databases obsolete or unavailable.</span></span>

<span data-ttu-id="3c74c-108">Para quitar las bases de datos o instancias del servidor de archivado o del servidor de supervisión, primero debe quitar el rol de servidor.</span><span class="sxs-lookup"><span data-stu-id="3c74c-108">To remove the databases or instances for the Archiving Server or Monitoring Server, you must first remove the server role.</span></span> <span data-ttu-id="3c74c-109">De forma similar, para quitar las instancias o bases de datos de un grupo de servidores front-end, primero debe quitar o volver a configurar la función de servidor dependiente.</span><span class="sxs-lookup"><span data-stu-id="3c74c-109">Similarly, to remove the instances or databases for Front End pool, you must first remove or reconfigure the dependent server role.</span></span> <span data-ttu-id="3c74c-110">Estos procedimientos no hacen distinción entre bases de datos colocadas o instancias independientes para servidores.</span><span class="sxs-lookup"><span data-stu-id="3c74c-110">These procedures make no distinction between collocated databases or separate instances for servers.</span></span> <span data-ttu-id="3c74c-111">Los procedimientos no se ven afectados por la collocation de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="3c74c-111">The procedures are unaffected by the collocation of databases.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3c74c-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3c74c-112">In This Section</span></span>

  - [<span data-ttu-id="3c74c-113">Quitar la base de datos de SQL Server para un grupo de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="3c74c-113">Remove the SQL Server database for a Front End pool</span></span>](remove-the-sql-server-database-for-a-front-end-pool.md)

  - [<span data-ttu-id="3c74c-114">Quitar la base de datos de SQL Server de un servidor de supervisión</span><span class="sxs-lookup"><span data-stu-id="3c74c-114">Remove the SQL Server database for a Monitoring server</span></span>](remove-the-sql-server-database-for-a-monitoring-server.md)

  - [<span data-ttu-id="3c74c-115">Quitar la base de datos de SQL Server de un servidor de archivado</span><span class="sxs-lookup"><span data-stu-id="3c74c-115">Remove the SQL Server database for an Archiving server</span></span>](remove-the-sql-server-database-for-an-archiving-server.md)

<span data-ttu-id="3c74c-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3c74c-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

