---
title: 'Lync Server 2013: asociar informes de supervisión a una base de datos reflejada'
description: 'Lync Server 2013: asociar informes de supervisión a una base de datos reflejada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Associating Monitoring Reports with a mirror database
ms:assetid: 42b797c6-8db8-4ad7-886e-8ddf8deb06f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945624(v=OCS.15)
ms:contentKeyID: 51541467
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d64b37901e7939b5e904dec73caac2d3483e2d71
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438263"
---
# <a name="associating-monitoring-reports-with-a-mirror-database-in-lync-server-2013"></a><span data-ttu-id="2914b-103">Asociar informes de supervisión a una base de datos reflejada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2914b-103">Associating Monitoring Reports with a mirror database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2914b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2914b-104">

<span> </span></span></span>

<span data-ttu-id="2914b-105">_**Última modificación del tema:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="2914b-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="2914b-106">Si configura una base de datos reflejada para supervisar su base de datos, la reflejada asumirá el puesto de la base de datos principal cuando se produzca una conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="2914b-106">If you configure a mirror for your monitoring database, that mirror database will take over as the primary database if a failover occurs.</span></span> <span data-ttu-id="2914b-107">Sin embargo, si usa los informes de supervisión de Lync Server y se produce un error, es posible que los informes de supervisión no se conecten a la base de datos reflejada.</span><span class="sxs-lookup"><span data-stu-id="2914b-107">However, if you use Lync Server Monitoring Reports and a failover occurs, you might find that your Monitoring Reports are not connecting to the mirror database.</span></span> <span data-ttu-id="2914b-108">Esto se debe a que, al instalar los informes de supervisión, solo se ha especificado la ubicación de la base de datos principal y no la de la base de datos reflejada.</span><span class="sxs-lookup"><span data-stu-id="2914b-108">This is because, when you install Monitoring Reports, you specify only the location of the primary database; you do not specify the location of the mirror database.</span></span>

<span data-ttu-id="2914b-p102">Para que los informes de supervisión pasen automáticamente a la base datos reflejada en caso de conmutación por error, necesita agregar la base de datos reflejada como "socio de conmutación por error" a las dos bases de datos que utilizan informes de supervisión (una base datos para los datos del registro detallado de llamadas y otra para los datos de Calidad de la experiencia). Tenga presente que este paso se ha de realizar después de haber instalado los informes de supervisión. Puede agregar información de socio de conmutación por error manualmente editando los valores de la cadena de conexión que utilizan las dos bases de datos. Para ello, realice el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="2914b-p102">To get Monitoring Reports to automatically failover to the mirror database, you must add the mirror database as a "failover partner" to the two databases that are used by Monitoring Reports (one database for Call Detail Record data, and the other for Quality of Experience (QoE) data). (Note that this step should be performed after you have installed Monitoring Reports.) You can add the failover partner information by manually editing the connection string values used by these two databases. To do that, complete the following procedure:</span></span>

1.  <span data-ttu-id="2914b-p103">Use Internet Explorer para abrir la página de inicio de **SQL Server Reporting Services**. La dirección URL de la página de inicio de Reporting Services está formada por:</span><span class="sxs-lookup"><span data-stu-id="2914b-p103">Use Internet Explorer to open the **SQL Server Reporting Services** home page. The Reporting Services home page URL includes:</span></span>
    
      - <span data-ttu-id="2914b-114">El prefijo **http:**.</span><span class="sxs-lookup"><span data-stu-id="2914b-114">The **http:** prefix.</span></span>
    
      - <span data-ttu-id="2914b-115">El nombre de dominio completo (FQDN) del equipo en el que se ha instalado Reporting Services (por ejemplo, **atl-sql-001.litwareinc.com**).</span><span class="sxs-lookup"><span data-stu-id="2914b-115">The fully qualified domain name (FQDN) of the computer where the Reporting Services are installed (for example, **atl-sql-001.litwareinc.com**).</span></span>
    
      - <span data-ttu-id="2914b-116">La cadena de **caracteres \_ /Reports**.</span><span class="sxs-lookup"><span data-stu-id="2914b-116">The character string **/Reports\_**.</span></span>
    
      - <span data-ttu-id="2914b-117">El nombre de la instancia de la base de datos en la que están instalados los informes de supervisión (por ejemplo, **archinst**).</span><span class="sxs-lookup"><span data-stu-id="2914b-117">The name of the database instance where the Monitoring Reports are installed (for example, **archinst**).</span></span>
    
    <span data-ttu-id="2914b-118">Por ejemplo, si se ha instalado SQL Server Reporting Services en el equipo atl-sql-001.litwareinc.com y los informes de supervisión utilizan la instancia de base de datos archinst, la dirección URL de la página de inicio será:</span><span class="sxs-lookup"><span data-stu-id="2914b-118">For example, if SQL Server Reporting Services was installed on the computer atl-sql-001.litwareinc.com and the Monitoring Reports use the database instance archinst, the home page URL would look like this:</span></span>
    
    **http://atl-sql-001.litwareinc.com/Reports\_archinst**

2.  <span data-ttu-id="2914b-119">Una vez que haya tenido acceso a la Página principal de Reporting Services, haga clic **LyncServerReports** y luego en **\_ contenido de informes**.</span><span class="sxs-lookup"><span data-stu-id="2914b-119">After you have accessed the Reporting Services home page, click **LyncServerReports**, and then click **Reports\_Content**.</span></span> <span data-ttu-id="2914b-120">Esto le llevará a la página **de \_ contenido informes** de los informes de supervisión de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2914b-120">That will take you to the **Reports\_Content** page for the Lync Server Monitoring Reports.</span></span>

3.  <span data-ttu-id="2914b-121">En la página de **\_ contenido informes** , haga clic en el origen de datos **CDRDB** .</span><span class="sxs-lookup"><span data-stu-id="2914b-121">On the **Reports\_Content** page, click the **CDRDB** data source.</span></span>

4.  <span data-ttu-id="2914b-p105">En la página **CDRDB**, en la ficha **Propiedades**, busque el cuadro de texto titulado **Cadena de conexión**. La cadena de conexión actual será similar a:</span><span class="sxs-lookup"><span data-stu-id="2914b-p105">On the **CDRDB** page, on the **Properties** tab, look for the text box labeled **Connection string**. The current connection string will look similar to this:</span></span>
    
    <span data-ttu-id="2914b-124">**Origen de datos = (local) \\ archinst; catálogo inicial = LcsCDR**</span><span class="sxs-lookup"><span data-stu-id="2914b-124">**Data source=(local)\\archinst;initial catalog=LcsCDR**</span></span>

5.  <span data-ttu-id="2914b-p106">Modifique la cadena de conexión para incluir el nombre del servidor y la instancia de base de datos de la base de datos reflejada. Por ejemplo, si el servidor se llama atl-mirror-001 y la base de datos reflejada se encuentra en la instancia archinst, tendrá que agregar para especificar la base de datos reflejada esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="2914b-p106">Edit the connection string to include the server name and database instance for the mirror database. For example, if the server is named atl-mirror-001 and the mirror database is in the archinst instance, you will need to add to specify the mirror database using this syntax:</span></span>
    
    <span data-ttu-id="2914b-127">**Asociado de conmutación por error = ATL-Mirror-001 \\ archinst**</span><span class="sxs-lookup"><span data-stu-id="2914b-127">**Failover Partner=atl-mirror-001\\archinst**</span></span>
    
    <span data-ttu-id="2914b-128">La cadena de conexión resultante necesitará ser:</span><span class="sxs-lookup"><span data-stu-id="2914b-128">Your edited connection string will look like this:</span></span>
    
    <span data-ttu-id="2914b-129">**Origen de datos = (local) \\ archinst; Asociado de conmutación por error = ATL-Mirror-001 \\ archinst; Initial Catalog = LcsCDR**</span><span class="sxs-lookup"><span data-stu-id="2914b-129">**Data source=(local)\\archinst;Failover Partner=atl-mirror-001\\archinst;initial catalog=LcsCDR**</span></span>

6.  <span data-ttu-id="2914b-130">Cuando haya actualizado la cadena de conexión, haga clic en **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="2914b-130">After updating the connection string, click **Apply**.</span></span>

7.  <span data-ttu-id="2914b-131">En la página **CDRDB** , haga clic en el vínculo de **\_ contenido informes** .</span><span class="sxs-lookup"><span data-stu-id="2914b-131">On the **CDRDB** page, click the **Reports\_Content** link.</span></span> <span data-ttu-id="2914b-132">Haga clic en el origen de datos **QMSDB** y, luego, modifique la cadena de conexión de la base de datos QoE.</span><span class="sxs-lookup"><span data-stu-id="2914b-132">Click the **QMSDB** data source, and then edit the connection string for the QoE database.</span></span> <span data-ttu-id="2914b-133">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2914b-133">For example:</span></span>
    
    <span data-ttu-id="2914b-134">**Origen de datos = (local) \\ archinst; Asociado de conmutación por error = ATL-Mirror-001 \\ archinst; Initial Catalog = QoEMetrics**</span><span class="sxs-lookup"><span data-stu-id="2914b-134">**Data source=(local)\\archinst;Failover Partner=atl-mirror-001\\archinst;initial catalog=QoEMetrics**</span></span>

8.  <span data-ttu-id="2914b-135">Haga clic en **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="2914b-135">Click **Apply**.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="2914b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2914b-136">See Also</span></span>


[<span data-ttu-id="2914b-137">Instalar los informes de supervisión de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2914b-137">Installing Lync Server 2013 Monitoring Reports</span></span>](lync-server-2013-installing-lync-server-2013-monitoring-reports.md)  
[<span data-ttu-id="2914b-138">Usar informes de supervisión en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2914b-138">Using Monitoring Reports in Lync Server 2013</span></span>](lync-server-2013-using-monitoring-reports.md)  
  

<span data-ttu-id="2914b-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2914b-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

