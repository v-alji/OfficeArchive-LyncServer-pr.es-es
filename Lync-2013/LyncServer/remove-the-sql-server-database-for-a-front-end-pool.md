---
title: Quitar la base de datos de SQL Server para un grupo de servidores front-end
description: Quitar la base de datos de SQL Server de un grupo de servidores front-end.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the SQL Server database for a Front End pool
ms:assetid: 6bb932df-3ed7-49b6-ae17-61e4c6a5fe82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688084(v=OCS.15)
ms:contentKeyID: 49733681
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c5d47e4c52197c5792fa3b7770da7bbd1b26cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400074"
---
# <a name="remove-the-sql-server-database-for-a-front-end-pool"></a><span data-ttu-id="f38cc-103">Quitar la base de datos de SQL Server para un grupo de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="f38cc-103">Remove the SQL Server database for a Front End pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f38cc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f38cc-104">

<span> </span></span></span>

<span data-ttu-id="f38cc-105">_**Última modificación del tema:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="f38cc-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="f38cc-106">Después de quitar un grupo front-end de Microsoft Lync Server 2010 o volver a configurar el grupo para que use una base de datos diferente, puede quitar las bases de datos de SQL Server que hospedaron los datos del grupo.</span><span class="sxs-lookup"><span data-stu-id="f38cc-106">After you remove a Microsoft Lync Server 2010 Front End pool or reconfigure the pool to use a different database, you can remove the SQL Server databases that hosted the pool data.</span></span> <span data-ttu-id="f38cc-107">Use los procedimientos siguientes para quitar las definiciones del generador de topología y, a continuación, quite los archivos de base de datos y de registro del servidor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="f38cc-107">Use the following procedures to remove the definitions from Topology Builder, and then remove the database and log files from the database server.</span></span>

<div>

## <a name="to-remove-the-sql-server-database-using-topology-builder"></a><span data-ttu-id="f38cc-108">Para quitar la base de datos de SQL Server con el generador de topologías</span><span class="sxs-lookup"><span data-stu-id="f38cc-108">To remove the SQL Server database using Topology Builder</span></span>

1.  <span data-ttu-id="f38cc-109">Desde el servidor front-end de Lync Server 2013, abra Topology Builder y descargue la topología existente.</span><span class="sxs-lookup"><span data-stu-id="f38cc-109">From the Lync Server 2013 Front End Server, open Topology Builder and download the existing topology.</span></span>

2.  <span data-ttu-id="f38cc-110">En el generador de topología, vaya a **componentes compartidos** y, a continuación, a **almacenes de SQL Server**, haga clic con el botón secundario en la instancia de SQL Server asociada al grupo front-end eliminado o reconfigurado y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="f38cc-110">In Topology Builder, navigate to **Shared Components** and then **SQL Server Stores**, right-click the SQL Server instance associated with the removed or reconfigured Front End pool, and then click **Delete**.</span></span>

3.  <span data-ttu-id="f38cc-111">Publique la topología y, a continuación, compruebe el estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="f38cc-111">Publish the topology, and then check the replication status.</span></span>

</div>

<div>

## <a name="to-remove-user-and-application-databases-from-the-sql-server"></a><span data-ttu-id="f38cc-112">Para quitar bases de datos de usuario y de aplicación de SQL Server</span><span class="sxs-lookup"><span data-stu-id="f38cc-112">To remove user and application databases from the SQL Server</span></span>

1.  <span data-ttu-id="f38cc-113">Para quitar las bases de datos de SQL Server, debe ser miembro del grupo de administradores de bases de datos de SQL Server para el servidor SQL donde va a quitar los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="f38cc-113">To remove the databases on the SQL Server, you must be a member of the SQL Server sysadmins group for the SQL Server where you are removing the database files.</span></span>

2.  <span data-ttu-id="f38cc-114">Abrir el shell de administración de Lync Server</span><span class="sxs-lookup"><span data-stu-id="f38cc-114">Open Lync Server Management Shell</span></span>

3.  <span data-ttu-id="f38cc-115">Para quitar la base de datos para el almacén de usuario del grupo, escriba:</span><span class="sxs-lookup"><span data-stu-id="f38cc-115">To remove the database for the pool user store, type:</span></span>
    
        Uninstall-CsDataBase -DatabaseType User -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    <span data-ttu-id="f38cc-116">Donde \<FQDN\> es el nombre de dominio completo (FQDN) del servidor de la base de datos y \<instance\> es la instancia de la base de datos con nombre (es decir, si se definió una).</span><span class="sxs-lookup"><span data-stu-id="f38cc-116">Where \<FQDN\> is the fully qualified domain name (FQDN) of the database server, and \<instance\> is the named database instance (that is, if one was defined).</span></span>

4.  <span data-ttu-id="f38cc-117">Para quitar la base de datos para el almacén de aplicaciones del grupo, escriba:</span><span class="sxs-lookup"><span data-stu-id="f38cc-117">To remove the database for the pool application store, type:</span></span>
    
        Uninstall-CsDataBase -DatabaseType Application -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    <span data-ttu-id="f38cc-118">Donde \<FQDN\> es el nombre completo del servidor de la base de datos y \<instance\> es la instancia de la base de datos con nombre (es decir, si se definió una).</span><span class="sxs-lookup"><span data-stu-id="f38cc-118">Where \<FQDN\> is the FQDN of the database server, and \<instance\> is the named database instance (that is, if one was defined).</span></span>

5.  <span data-ttu-id="f38cc-119">Cuando el cmdlet **Uninstall-CsDataBase** le pida que confirme las acciones, lea la información y, a continuación, presione **s** (o presione Entrar) para continuar, o presione **N** y después entrar si quiere detener el cmdlet (es decir, en caso de que se produzcan errores).</span><span class="sxs-lookup"><span data-stu-id="f38cc-119">When the **Uninstall-CsDataBase** cmdlet prompts you to confirm actions, read the information, and then press **Y** (or press Enter) to proceed, or press **N** and then Enter if you want to stop the cmdlet (that is, in case there errors).</span></span>

<span data-ttu-id="f38cc-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f38cc-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

