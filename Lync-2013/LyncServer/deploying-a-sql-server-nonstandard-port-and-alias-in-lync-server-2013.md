---
title: Implementación de un alias y un puerto no estándar de SQL Server en Lync Server 2013
description: Implementar un puerto y alias no estándar de SQL Server en Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a SQL Server nonstandard port and alias in Lync Server 2013
ms:assetid: 2da92c1f-250e-407a-8651-fb2aec76aeb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn776290(v=OCS.15)
ms:contentKeyID: 62634609
ms.date: 09/17/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da76db2b946a47e13fe3549d7184b0b12894a83a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398262"
---
# <a name="deploying-a-sql-server-nonstandard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="b16da-103">Implementación de un alias y un puerto no estándar de SQL Server en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b16da-103">Deploying a SQL Server nonstandard port and alias in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b16da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b16da-104">

<span> </span></span></span>

<span data-ttu-id="b16da-105">_**Última modificación del tema:** 2015-09-16_</span><span class="sxs-lookup"><span data-stu-id="b16da-105">_**Topic Last Modified:** 2015-09-16_</span></span>

<span data-ttu-id="b16da-106">Microsoft Lync Server 2013 admite el uso de un puerto y un alias no estándar en SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b16da-106">Microsoft Lync Server 2013 supports using a non-standard port and alias in SQL Server.</span></span> <span data-ttu-id="b16da-107">El uso de un puerto no estándar de SQL Server y un alias aumenta la seguridad y crea un entorno más flexible para la implementación de Lync.</span><span class="sxs-lookup"><span data-stu-id="b16da-107">Using a SQL Server non-standard port and an alias increases security and creates a more flexible environment for the Lync deployment.</span></span> <span data-ttu-id="b16da-108">Estos pasos son solo un paso para proteger correctamente el entorno de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b16da-108">These steps are only a single step in properly securing your Lync Server 2013 environment.</span></span> <span data-ttu-id="b16da-109">Hay que seguir pasos adicionales para reducir la superficie de ataque de una implementación de 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b16da-109">Additional steps should be taken to reduce the attack surface of a Lync Server 2013 implementation.</span></span>

<span data-ttu-id="b16da-110">En el siguiente artículo se describen los pasos necesarios para configurar un puerto no estándar y un alias de SQL Server en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b16da-110">The following article describes the steps required to setup a SQL Server non-standard port and alias in Lync Server 2013.</span></span>

<div>

## <a name="deploying-a-sql-server-non-standard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="b16da-111">Implementar un puerto y alias no estándar de SQL Server en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b16da-111">Deploying a SQL Server Non-Standard Port and Alias in Lync Server 2013</span></span>

<span data-ttu-id="b16da-112">El generador de topología de Lync Server 2013 admite el uso de un alias de SQL Server como nombre de dominio completo (FQDN) en lugar del FQDN real de SQL Server al configurar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b16da-112">Lync Server 2013 Topology Builder supports using a SQL Server alias as the Fully Qualified Domain Name (FQDN) instead of the actual SQL Server FQDN when configuring Lync Server 2013.</span></span> <span data-ttu-id="b16da-113">Esto permite que el FQDN real de SQL Server esté oculto para cualquier atacante malintencionado.</span><span class="sxs-lookup"><span data-stu-id="b16da-113">This allows the actual SQL Server FQDN to be hidden from any malicious attacker.</span></span> <span data-ttu-id="b16da-114">Además, el uso de un puerto no estándar oculta el puerto real de cualquier atacante que pudiera intentar atacar la base de datos en el puerto estándar 1433, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-114">In addition, using a non-standard port obscures the actual port from any would be attacker attempting to attack the database on the standard port 1433, as shown in the following figure.</span></span>

<span data-ttu-id="b16da-115">![Los atacantes no saben el número de puerto al que atacar.](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "Los atacantes no saben el número de puerto al que atacar.")</span><span class="sxs-lookup"><span data-stu-id="b16da-115">![A hacker doesn't know the port number to attack.](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "A hacker doesn't know the port number to attack.")</span></span>

<span data-ttu-id="b16da-116">Para tener éxito al determinar el puerto que usa Lync Server 2013 para comunicarse con SQL Server, el atacante necesita examinar todos los puertos para obtener la información del puerto.</span><span class="sxs-lookup"><span data-stu-id="b16da-116">In order to be successful in determining the port Lync Server 2013 is using to communicate with SQL Server, the attacker would need to scan all ports to obtain the port information.</span></span> <span data-ttu-id="b16da-117">Una exploración de puertos por parte de un atacante aumenta las probabilidades de que la seguridad pueda detectar y detener la instrucción.</span><span class="sxs-lookup"><span data-stu-id="b16da-117">A port scan by an attacker increases the chances that security can detect and stop the instruction.</span></span> <span data-ttu-id="b16da-118">Además de agregar mayor seguridad con un puerto no estándar, también puede usar un alias de SQL Server para proporcionar flexibilidad a la implementación.</span><span class="sxs-lookup"><span data-stu-id="b16da-118">In addition to adding increased security with a non-standard port, you can also use a SQL Server alias to provide flexibility for the deployment.</span></span> <span data-ttu-id="b16da-119">Esto es útil para reducir los cambios de configuración en situaciones en las que se requiere un cambio de nombre de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b16da-119">This is valuable in order to reduce configuration changes in situations where a SQL Server name change is required.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b16da-120">SQL Server proporciona dos métodos de tolerancia a errores (clústeres de conmutación por error y reflejos).</span><span class="sxs-lookup"><span data-stu-id="b16da-120">SQL Server provides two fault tolerance methods (Failover Clustering and Mirroring).</span></span> <span data-ttu-id="b16da-121">Los métodos de tolerancia a errores de SQL Server se admiten con un puerto no estándar y un alias de SQL Server con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b16da-121">Both SQL Server fault tolerance methods are supported using a SQL Server non-standard port and alias with Lync Server 2013.</span></span> <span data-ttu-id="b16da-122">Si el back-end de SQL Server utilizado por el grupo está en una configuración duplicada, el servicio explorador SQL de los servidores back-end de SQL Server debe estar ejecutándose para que los servidores de aplicaciones para el usuario se conecten a la base de datos reflejada cuando las bases de datos se conmutan por error al servidor SQL reflejado.</span><span class="sxs-lookup"><span data-stu-id="b16da-122">If the SQL Server backend used by the pool is in a mirrored configuration, then the SQL browser service on the SQL Server backend servers should be running for Front End servers to connect to the mirrored database when the databases are failed over to the mirrored SQL Server.</span></span>



</div>

<span data-ttu-id="b16da-123">Al configurar la conectividad de base de datos de SQL Server desde el generador de topología, o al utilizar el cmdlet Install-CsDatabase, no es posible definir de forma explícita un número de puerto no estándar de SQL Server y asociarlo a una instancia de SQL.</span><span class="sxs-lookup"><span data-stu-id="b16da-123">When configuring SQL Server database connectivity from within Topology Builder, or when using the Install-CsDatabase cmdlet, it’s not possible to explicitly define a SQL Server non-standard port number and associate it with a SQL instance.</span></span> <span data-ttu-id="b16da-124">Para establecer un puerto no estándar, tendrá que usar las utilidades de SQL Server y de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="b16da-124">To set a non-standard port, you’ll need to use SQL Server and Windows Server utilities.</span></span>

<span data-ttu-id="b16da-125">Para configurar un puerto y un alias no estándar de SQL Server para usar con Lync Server 2013, tendrá que completar tres pasos principales.</span><span class="sxs-lookup"><span data-stu-id="b16da-125">To set up a SQL Server non-standard port and alias for use with Lync Server 2013, you will need to complete three primary steps.</span></span> <span data-ttu-id="b16da-126">Estos pasos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b16da-126">These steps are:</span></span>

  - <span data-ttu-id="b16da-127">Confirme que Lync Server 2013 tiene las actualizaciones más recientes aplicadas.</span><span class="sxs-lookup"><span data-stu-id="b16da-127">Confirm that Lync Server 2013 has the Latest Updates Applied.</span></span>

  - <span data-ttu-id="b16da-128">Configure el puerto y el alias no estándar de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b16da-128">Setup the SQL Server Non-Standard Port and Alias.</span></span>

  - <span data-ttu-id="b16da-129">Configure Lync Server 2013 con el alias de SQL Server con el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="b16da-129">Configure Lync Server 2013 with the SQL Server alias using Topology Builder.</span></span>

  - <span data-ttu-id="b16da-130">Publique la topología y Compruebe la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b16da-130">Publish the Topology, and Verify the Database.</span></span>

<div>

## <a name="confirm-that-lync-server-2013-has-the-latest-updates-applied"></a><span data-ttu-id="b16da-131">Confirmar que Lync Server 2013 tiene las actualizaciones más recientes aplicadas</span><span class="sxs-lookup"><span data-stu-id="b16da-131">Confirm that Lync Server 2013 has the Latest Updates Applied</span></span>

<span data-ttu-id="b16da-132">Es importante mantener Lync Server 2013 actualizado.</span><span class="sxs-lookup"><span data-stu-id="b16da-132">It is important to keep Lync Server 2013 up to date.</span></span> <span data-ttu-id="b16da-133">Para consultar las actualizaciones más recientes e información sobre cómo aplicarlas, consulte [actualizaciones para Lync Server 2013](https://support.microsoft.com/kb/2809243).</span><span class="sxs-lookup"><span data-stu-id="b16da-133">To check for the most recent updates and information on how to apply them, see [Updates for Lync Server 2013](https://support.microsoft.com/kb/2809243).</span></span>

</div>

<div>

## <a name="setup-the-sql-server-non-standard-port-and-alias"></a><span data-ttu-id="b16da-134">Configurar el puerto y el alias no estándar de SQL Server</span><span class="sxs-lookup"><span data-stu-id="b16da-134">Setup the SQL Server Non-Standard Port and Alias</span></span>

<span data-ttu-id="b16da-135">El puerto y el alias no estándar de SQL Server se deben configurar en la instancia de la base de datos para que se pueda hacer referencia a ellos desde el generador de topología de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b16da-135">The SQL Server non-standard port and alias must be set up on the database instance before it can be referenced from Lync Server 2013 Topology Builder.</span></span> <span data-ttu-id="b16da-136">Para configurar un puerto y un alias no estándar de SQL Server, tendrá que completar tres pasos principales.</span><span class="sxs-lookup"><span data-stu-id="b16da-136">To set up a SQL Server non-standard port and alias, you will have to complete three primary steps.</span></span> <span data-ttu-id="b16da-137">Estos pasos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b16da-137">These steps are as follows:</span></span>

  - <span data-ttu-id="b16da-138">Cambie los valores predeterminados de los protocolos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b16da-138">Change the Default TCP/IP Protocol Values.</span></span>

  - <span data-ttu-id="b16da-139">Crear y configurar un alias de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b16da-139">Create and Configure a SQL Server Alias.</span></span>

  - <span data-ttu-id="b16da-140">Crear un registro de recursos de nombre canónico (CNAME) del sistema de nombres de dominio (DNS).</span><span class="sxs-lookup"><span data-stu-id="b16da-140">Create a Domain Name System (DNS) Canonical Name (CNAME) Resource Record.</span></span>

<span data-ttu-id="b16da-141">**Modificar los valores predeterminados de los protocolos TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="b16da-141">**Modify the Default TCP/IP Protocol Values**</span></span>

1.  <span data-ttu-id="b16da-142">Seleccione **Inicio** y elija **Administrador de configuración de SQL Server**, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-142">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-143">![Icono de SQL Server Management Studio](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "Icono de SQL Server Management Studio")</span><span class="sxs-lookup"><span data-stu-id="b16da-143">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="b16da-144">En el panel de navegación, elija expandir la **instancia de SQL Server**, expanda la **configuración de red de SQL Server** y elija **protocolos para \<instance name\>**, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-144">In the navigation pane, choose to expand the **SQL Server instance**, choose to expand **SQL Server Network Configuration**, and choose **Protocols for \<instance name\>**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-145">![Propiedades de Navegar a TCP/IP](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "Propiedades de Navegar a TCP/IP")</span><span class="sxs-lookup"><span data-stu-id="b16da-145">![Navigate to TCP/IP Properties](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "Navigate to TCP/IP Properties")</span></span>

3.  <span data-ttu-id="b16da-146">En el panel derecho, haga clic con el botón derecho en **TCP/IP** y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="b16da-146">In the right pane, right-click **TCP/IP**, and select **Properties**.</span></span> <span data-ttu-id="b16da-147">Se muestra el cuadro de diálogo Propiedades de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b16da-147">The TCP/IP Properties dialog box is displayed.</span></span>

4.  <span data-ttu-id="b16da-148">Seleccione la ficha **direcciones IP** . La ficha direcciones IP muestra todas las direcciones IP activas en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b16da-148">Select the **IP Addresses** tab. The IP Addresses tab shows all of the active IP addresses on the server.</span></span> <span data-ttu-id="b16da-149">Están en el formato IP1, IP2, hasta IPAll, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-149">These are in the format IP1, IP2, up to IPAll, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-150">![Propiedades de Abrir TCP/IP.](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "Propiedades de Abrir TCP/IP.")</span><span class="sxs-lookup"><span data-stu-id="b16da-150">![Open TCP/IP properties.](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "Open TCP/IP properties.")</span></span>

5.  <span data-ttu-id="b16da-151">Borre el campo **puertos dinámicos TCP** para todas las direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="b16da-151">Clear the **TCP Dynamic Ports** field for all IP addresses.</span></span> <span data-ttu-id="b16da-152">Si el campo contiene un carácter cero, significa que SQL Server está escuchando en puertos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="b16da-152">If the field contains a zero character, then it means SQL Server is listening on dynamic ports.</span></span> <span data-ttu-id="b16da-153">Asegúrese de que estos campos están desactivados y no contienen un cero.</span><span class="sxs-lookup"><span data-stu-id="b16da-153">Make sure these fields are cleared and do not contain a zero.</span></span>

6.  <span data-ttu-id="b16da-154">En la dirección IP que usará Lync Server para conectarse a la base de datos, asegúrese de que la **opción habilitada** está establecida en **sí**, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-154">For the IP address that Lync Server will be using to connect to the database, make sure that **Enabled** is set to **Yes**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-155">![Establece habilitado en Sí para la IP correcta.](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "Establece habilitado en Sí para la IP correcta.")</span><span class="sxs-lookup"><span data-stu-id="b16da-155">![Set enabled as Yes for the correct IP.](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "Set enabled as Yes for the correct IP.")</span></span>

7.  <span data-ttu-id="b16da-156">En la sección **IPAll** de la parte inferior del cuadro de diálogo, escriba el puerto deseado en el campo **puerto TCP** , como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-156">In the **IPAll** section at the bottom of the dialog, enter the desired port in the **TCP Port** field, as shown in the following figure.</span></span> <span data-ttu-id="b16da-157">En este ejemplo, usamos el puerto 50062, pero puede usar cualquier puerto entre 49152 y 65535.</span><span class="sxs-lookup"><span data-stu-id="b16da-157">In this example, we use port 50062, but you can use any port between 49152 and 65535.</span></span> <span data-ttu-id="b16da-158">Estos son los puertos asignados a uso dinámico y privado, y esto garantiza que no entrará en conflicto con otros puertos que se usan en la implementación de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b16da-158">These are the ports assigned to dynamic and private use, and this ensures you won’t conflict with other ports being used in the Lync Server 2013 deployment.</span></span>
    
    <span data-ttu-id="b16da-159">![Establece el puerto en la sección IPAII.](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "Establece el puerto en la sección IPAII.")</span><span class="sxs-lookup"><span data-stu-id="b16da-159">![Set port in IPAll section.](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "Set port in IPAll section.")</span></span>

8.  <span data-ttu-id="b16da-160">Elija **Aceptar** para salir del cuadro de diálogo Propiedades de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b16da-160">Choose **OK** to exit the TCP/IP Properties dialog.</span></span>

9.  <span data-ttu-id="b16da-161">Para reiniciar la instancia de SQL Server, seleccione **servicios de SQL** Server en el panel izquierdo del administrador de configuración de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b16da-161">Restart the SQL Server instance by selecting **SQL Server Services** in the left pane of SQL Server Configuration Manager.</span></span> <span data-ttu-id="b16da-162">A continuación, haga clic con el botón secundario en **SQL Server \<instance name\>** en el panel derecho y seleccione **reiniciar**, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-162">Then right-click **SQL Server \<instance name\>** in the right pane, and select **Restart**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-163">![Restablecer el servicio de SQL Server para la instancia.](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "Restablecer el servicio de SQL Server para la instancia.")</span><span class="sxs-lookup"><span data-stu-id="b16da-163">![Reset the SQL Server service for instance.](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "Reset the SQL Server service for instance.")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b16da-164">Asegúrate de actualizar la configuración del firewall para que quepa en el nuevo puerto de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b16da-164">Make sure you update your firewall settings to accommodate the new SQL Server port.</span></span>



</div>

<span data-ttu-id="b16da-165">**Crear y configurar un alias de SQL Server**</span><span class="sxs-lookup"><span data-stu-id="b16da-165">**Create and Configure a SQL Server Alias**</span></span>

1.  <span data-ttu-id="b16da-166">Seleccione **Inicio** y elija **Administrador de configuración de SQL Server**, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-166">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-167">![Icono de SQL Server Management Studio](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "Icono de SQL Server Management Studio")</span><span class="sxs-lookup"><span data-stu-id="b16da-167">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="b16da-168">En el panel izquierdo, elija expandir la **instancia de SQL Server**, elija expandir la **\<version\> configuración de SQL Native Client** y, a continuación, elija **alias**, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-168">In the left pane, choose to expand **SQL Server instance**, choose to expand **SQL Native Client \<version\> Configuration**, and then choose **Aliases**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-169">![Alias en el administrador de configuración de SQL Server.](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "Alias en el administrador de configuración de SQL Server.")</span><span class="sxs-lookup"><span data-stu-id="b16da-169">![Aliases in SQL Server Configuration Manager.](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "Aliases in SQL Server Configuration Manager.")</span></span>

3.  <span data-ttu-id="b16da-170">Haga clic con el botón derecho en **alias** y seleccione **nuevo alias...**.</span><span class="sxs-lookup"><span data-stu-id="b16da-170">Right-click **Aliases**, and select **New Alias…**.</span></span>

4.  <span data-ttu-id="b16da-171">Escriba el **nombre de alias**, el **número de Puerto**, el **Protocolo** y el **servidor**, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-171">Enter the **Alias Name**, **Port Number**, **Protocol**, and **Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-172">![Crear un nuevo alias](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "Crear un nuevo alias")</span><span class="sxs-lookup"><span data-stu-id="b16da-172">![Creating a new alias](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "Creating a new alias")</span></span>
    
    <div>
    

    > [!CAUTION]  
    > <span data-ttu-id="b16da-173">Asegúrese de introducir el mismo puerto no estándar que usó en el paso anterior, ya que es el puerto en el que se escuchará SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b16da-173">Make sure to enter the same non-standard port you used in the previous step since that is the port SQL Server will be listening on.</span></span> <span data-ttu-id="b16da-174">Si un alias configurado se está conectando a un FQDN o instancia incorrecto de SQL Server, deshabilite y vuelva a habilitar el protocolo de red asociado.</span><span class="sxs-lookup"><span data-stu-id="b16da-174">If a configured alias is connecting to the wrong SQL Server FQDN or Instance, disable and then re-enable the associated network protocol.</span></span> <span data-ttu-id="b16da-175">De este modo, se borrará la información de conexión almacenada en la memoria caché y el cliente se conectará correctamente.</span><span class="sxs-lookup"><span data-stu-id="b16da-175">Doing this clears any cached connection information and allows the client to connect correctly.</span></span>

    
    </div>

<span data-ttu-id="b16da-176">**Crear un registro de recursos CNAME de DNS**</span><span class="sxs-lookup"><span data-stu-id="b16da-176">**Create a DNS CNAME Resource Record**</span></span>

1.  <span data-ttu-id="b16da-177">Inicie sesión en el equipo que administra DNS.</span><span class="sxs-lookup"><span data-stu-id="b16da-177">Sign into the computer managing DNS.</span></span>

2.  <span data-ttu-id="b16da-178">Seleccione **Inicio** y elija **Administrador del servidor**, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-178">Select **Start**, and choose **Server Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-179">![Abrir el administrador del servidor](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "Abrir el administrador del servidor")</span><span class="sxs-lookup"><span data-stu-id="b16da-179">![Opening Server Manager](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "Opening Server Manager")</span></span>

3.  <span data-ttu-id="b16da-180">Seleccione el menú desplegable **herramientas** y, a continuación, seleccione **DNS**, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-180">Choose the **Tools** drop-down, and select **DNS**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-181">![Abrir DNS desde el administrador del servidor.](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "Abrir DNS desde el administrador del servidor.")</span><span class="sxs-lookup"><span data-stu-id="b16da-181">![Opening DNS from Server Manager.](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "Opening DNS from Server Manager.")</span></span>

4.  <span data-ttu-id="b16da-182">En el panel de la izquierda, expanda el nodo nombre del servidor, expanda el nodo zonas de búsqueda directa y elija el dominio correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b16da-182">In the left pane, expand the server name node, expand the Forward Lookup Zones node, and choose the relevant domain.</span></span>

5.  <span data-ttu-id="b16da-183">Haga clic con el botón derecho en el dominio y seleccione **nuevo alias (CNAME)...**, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-183">Right-click the domain, and select **New Alias (CNAME)…**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-184">![Selección de la opción para crear un nuevo alias CNAME](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "Selección de la opción para crear un nuevo alias CNAME")</span><span class="sxs-lookup"><span data-stu-id="b16da-184">![Selecting option to create a new alias CNAME](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "Selecting option to create a new alias CNAME")</span></span>

6.  <span data-ttu-id="b16da-185">Escriba el **nombre de alias** y el **FQDN de SQL Server**, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-185">Enter the **Alias Name** and the **FQDN for SQL Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-186">![Rellenando el cuadro de diálogo nuevo alias CNAME.](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "Rellenando el cuadro de diálogo nuevo alias CNAME.")</span><span class="sxs-lookup"><span data-stu-id="b16da-186">![Filling in the new alias CNAME dialog.](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "Filling in the new alias CNAME dialog.")</span></span>

7.  <span data-ttu-id="b16da-187">Elija **Aceptar** para guardar el CNAME y verlo en el administrador de DNS.</span><span class="sxs-lookup"><span data-stu-id="b16da-187">Choose **OK** to save the CNAME and view it in DNS Manager.</span></span>

</div>

<div>

## <a name="validate-database-connectivity"></a><span data-ttu-id="b16da-188">Validar la conectividad de la base de datos</span><span class="sxs-lookup"><span data-stu-id="b16da-188">Validate Database Connectivity</span></span>

<span data-ttu-id="b16da-189">Hay varias formas diferentes de asegurarse de que funciona.</span><span class="sxs-lookup"><span data-stu-id="b16da-189">There are many different ways to make sure it is working.</span></span> <span data-ttu-id="b16da-190">Desea asegurarse de que la base de datos de SQL Server está escuchando en el puerto especificado usando el alias.</span><span class="sxs-lookup"><span data-stu-id="b16da-190">You want to make sure that the SQL Server database is listening on the specified port using the alias.</span></span> <span data-ttu-id="b16da-191">Una comprobación rápida se puede completar con los comandos **netstat** y **telnet** .</span><span class="sxs-lookup"><span data-stu-id="b16da-191">A quick check can be completed using the **netstat** and **telnet** commands.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b16da-192">El cliente Telnet es una característica que se incluye con Windows Server, pero que debe instalarse.</span><span class="sxs-lookup"><span data-stu-id="b16da-192">Telnet Client is a Feature that comes with Windows Server but that must be installed.</span></span> <span data-ttu-id="b16da-193">Para instalar una característica de Windows Server, abra el administrador del servidor y seleccione Agregar roles y características en el menú administrar.</span><span class="sxs-lookup"><span data-stu-id="b16da-193">A Windows Server Feature can be installed by opening Server Manager and selecting Add Roles and Features from the Manage menu.</span></span>



</div>

<span data-ttu-id="b16da-194">**Usar netstat y Telnet para comprobar la conectividad de la base de datos**</span><span class="sxs-lookup"><span data-stu-id="b16da-194">**Use netstat and telnet to verify database connectivity**</span></span>

1.  <span data-ttu-id="b16da-195">Seleccione **Inicio** y escriba **cmd** para abrir un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="b16da-195">Select **Start**, and type **cmd** to open a command prompt.</span></span>

2.  <span data-ttu-id="b16da-196">Escriba **netstat-a-f** y confirme que SQL Server se está ejecutando con el puerto correcto, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b16da-196">Type **netstat -a -f**, and confirm that SQL Server is running with the correct port, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b16da-197">![Uso de netstat para comprobar el puerto.](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "Uso de netstat para comprobar el puerto.")</span><span class="sxs-lookup"><span data-stu-id="b16da-197">![Using netstat to verify port.](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "Using netstat to verify port.")</span></span>

3.  <span data-ttu-id="b16da-198">Escriba **telnet \<alias name\> \<port \#\>** para confirmar la conexión a la instancia de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b16da-198">Type **telnet \<alias name\> \<port \#\>** to confirm the connection to the SQL Server instance.</span></span> <span data-ttu-id="b16da-199">Si la conexión se realiza correctamente, Telnet se conectará y no se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="b16da-199">If the connection is successful, telnet will connect and you shouldn’t see an error.</span></span> <span data-ttu-id="b16da-200">Esto muestra que la instancia de SQL Server está escuchando en el puerto correcto con el alias correcto.</span><span class="sxs-lookup"><span data-stu-id="b16da-200">This shows that the SQL Server instance is listening on the correct port with the correct alias.</span></span> <span data-ttu-id="b16da-201">Si hay un problema al conectarse a la base de datos de SQL Server, entonces Telnet muestra un error que indica que no se puede establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="b16da-201">If there’s a problem connecting to the SQL Server database, then telnet shows an error that the connection cannot be made.</span></span> <span data-ttu-id="b16da-202">Ahora que ha verificado la conectividad de la base de datos en el servidor de base de datos, puede hacer lo mismo desde Lync Server (a través de la red) y asegurarse de que no haya firewalls bloqueando el acceso durante el proceso.</span><span class="sxs-lookup"><span data-stu-id="b16da-202">Now that you have checked database connectivity on the database server, you can do the same thing from Lync Server (over the network) and make sure there aren’t any firewalls blocking access along the way.</span></span>

</div>

<div>

## <a name="conclusion"></a><span data-ttu-id="b16da-203">Conclusión</span><span class="sxs-lookup"><span data-stu-id="b16da-203">Conclusion</span></span>

<span data-ttu-id="b16da-204">Una vez que el alias de SQL Server se ha configurado, puede usarlo para crear una topología de Lync Server 2013 en la herramienta Generador de topología.</span><span class="sxs-lookup"><span data-stu-id="b16da-204">Once the SQL Server alias has been configured, you can use it to create a Lync Server 2013 topology in the Topology Builder tool.</span></span> <span data-ttu-id="b16da-205">Para obtener más información acerca de las topologías, consulte [definir y configurar la topología en Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="b16da-205">For more information about topologies, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b16da-206">Vea también</span><span class="sxs-lookup"><span data-stu-id="b16da-206">See Also</span></span>


<span data-ttu-id="b16da-207">[Microsoft Lync Server 2013](microsoft-lync-server-2013.md)  
 [Planificación de la seguridad en Lync Server 2013](lync-server-2013-planning-for-security.md)</span><span class="sxs-lookup"><span data-stu-id="b16da-207">[Microsoft Lync Server 2013](microsoft-lync-server-2013.md) 
[Planning for security in Lync Server 2013](lync-server-2013-planning-for-security.md)</span></span>  
[<span data-ttu-id="b16da-208">Definición y configuración de la topología en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b16da-208">Defining and configuring the topology in Lync Server 2013</span></span>](lync-server-2013-defining-and-configuring-the-topology.md)  
[<span data-ttu-id="b16da-209">Implementar Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b16da-209">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="b16da-210"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b16da-210"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

