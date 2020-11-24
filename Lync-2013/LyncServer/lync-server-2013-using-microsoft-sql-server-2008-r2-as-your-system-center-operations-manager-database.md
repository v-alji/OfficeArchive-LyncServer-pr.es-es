---
title: 'Lync Server 2013: uso de Microsoft SQL Server 2008 R2 como base de datos de System Center Operations Manager'
description: 'Lync Server 2013: usar Microsoft SQL Server 2008 R2 como base de datos de System Center Operations Manager.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database
ms:assetid: 0efe76da-8854-499e-bdc7-3623244a8e85
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687969(v=OCS.15)
ms:contentKeyID: 49733555
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 870c079e7e5e871fc62358e9bdd21653193fad7c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399431"
---
# <a name="using-microsoft-sql-server-2008-r2-as-your-system-center-operations-manager-database-for-lync-server-2013"></a><span data-ttu-id="3967c-103">Uso de Microsoft SQL Server 2008 R2 como base de datos de System Center Operations Manager para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3967c-103">Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3967c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3967c-104">

<span> </span></span></span>

<span data-ttu-id="3967c-105">_**Última modificación del tema:** 2013-07-29_</span><span class="sxs-lookup"><span data-stu-id="3967c-105">_**Topic Last Modified:** 2013-07-29_</span></span>

<span data-ttu-id="3967c-106">Para usar SQL Server 2008 R2 como base de datos back-end, complete los pasos que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="3967c-106">To use SQL Server 2008 R2 as your back-end database, complete the steps detailed in this topic.</span></span>

<div>

## <a name="configuring-sql-server-2008-r2-and-sql-server-reporting-services"></a><span data-ttu-id="3967c-107">Configuración de SQL Server 2008 R2 y SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="3967c-107">Configuring SQL Server 2008 R2 and SQL Server Reporting Services</span></span>

<span data-ttu-id="3967c-108">Antes de empezar a instalar System Center Operations Manager, debe realizar dos cambios en su SQL Server 2008 R2 y en la configuración de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="3967c-108">Before you begin installing System Center Operations Manager you must make two changes to your SQL Server 2008 R2 and your SQL Server Reporting Services configuration.</span></span> <span data-ttu-id="3967c-109">(Estos cambios solo son necesarios si usa SQL Server 2008 R2 como la base de datos de Operations Manager). En primer lugar, haga lo siguiente en el equipo que hospedará la base de datos de Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="3967c-109">(These changes are required only if you are using SQL Server 2008 R2 as your Operations Manager database.) First, do the following on the computer that will host your Operations Manager database:</span></span>

1.  <span data-ttu-id="3967c-110">Haga clic en **Inicio** y, después, en **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="3967c-110">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="3967c-111">En el cuadro de diálogo **Ejecutar** , escriba **C: \\ archivos de programa \\ Microsoft SQL Server \\ MSRS10 \_ 50. ARCHINST \\ Reporting Services \\ ReportServer** y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="3967c-111">In the **Run** dialog box, type **C:\\Program Files\\Microsoft SQL Server\\ MSRS10\_50.ARCHINST\\Reporting Services\\ReportServer** and then press ENTER.</span></span>

3.  <span data-ttu-id="3967c-112">En la carpeta **ReportServer** , abra el archivo **rsreportserver.config** en el Bloc de notas o en cualquier otro editor de texto.</span><span class="sxs-lookup"><span data-stu-id="3967c-112">In the **ReportServer** folder, open the file **rsreportserver.config** in Notepad or any other text editor.</span></span>

4.  <span data-ttu-id="3967c-113">Cerca del principio del archivo, verá una serie de nodos "agregar clave".</span><span class="sxs-lookup"><span data-stu-id="3967c-113">Near the beginning of the file you will see a series of "Add Key" nodes.</span></span> <span data-ttu-id="3967c-114">Busque la entrada que comienza **\< Add key = "SecureConnectionLevel"** y establezca el valor en **0**:</span><span class="sxs-lookup"><span data-stu-id="3967c-114">Find the entry that begins **\<Add Key="SecureConnectionLevel"** and set the value to **0**:</span></span>
    
        <Add Key="SecureConnectionLevel" Value="0"/>

5.  <span data-ttu-id="3967c-115">Guarde el archivo **rsreportserver.config** y, a continuación, cierre el editor de texto.</span><span class="sxs-lookup"><span data-stu-id="3967c-115">Save the file **rsreportserver.config** and then close your text editor.</span></span>

<span data-ttu-id="3967c-116">Después de actualizar el archivo de configuración del servidor de informes, debe asignar el certificado correcto a SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="3967c-116">After updating the Report Server configuration file you must then assign the correct certificate to SQL Server Reporting Services.</span></span> <span data-ttu-id="3967c-117">Siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="3967c-117">To do that:</span></span>

1.  <span data-ttu-id="3967c-118">Haga clic en **Inicio**, en **todos los programas**, en **Microsoft SQL Server 2008 R2**, en **herramientas de configuración** y, por último, en Administrador de **configuración de Reporting Services**.</span><span class="sxs-lookup"><span data-stu-id="3967c-118">Click **Start**, click **All Programs**, click **Microsoft SQL Server 2008 R2**, click **Configuration Tools**, and then click **Reporting Services Configuration Manager**.</span></span>

2.  <span data-ttu-id="3967c-119">En el cuadro de diálogo **conexión de configuración de Reporting Services** , asegúrese de que el nombre del servidor aparece en el cuadro **nombre del servidor** .</span><span class="sxs-lookup"><span data-stu-id="3967c-119">In the **Reporting Services Configuration Connection** dialog box, make sure that the name of your server appears in the **Server Name** box.</span></span> <span data-ttu-id="3967c-120">Seleccione la instancia de SQL Server que hospedará la base de datos de Operations Manager (por ejemplo, **ARCHINST**) en la lista desplegable **instancia del servidor de informes** y, a continuación, haga clic en **conectar**.</span><span class="sxs-lookup"><span data-stu-id="3967c-120">Select the SQL Server instance that will host your Operations Manager database (for example, **ARCHINST**) from the **Report Server Instance** drop-down list and then click **Connect**.</span></span>

3.  <span data-ttu-id="3967c-121">En el administrador de configuración de Reporting Services, haga clic en **URL de servicio Web**.</span><span class="sxs-lookup"><span data-stu-id="3967c-121">In Reporting Services Configuration Manager, click **Web Service URL**.</span></span>

4.  <span data-ttu-id="3967c-122">En la página **dirección URL de servicio Web** , seleccione el certificado que se usará para su Reporting Services en la lista desplegable **certificado SSL** y, a continuación, haga clic en **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="3967c-122">On the **Web Service URL** page, select the certificate to be used for your Reporting Services from the **SSL Certificate** dropdown list and then click **Apply**.</span></span> <span data-ttu-id="3967c-123">Después de unos segundos, verá un par de direcciones URL en el **servicio Web del servidor de informes**.</span><span class="sxs-lookup"><span data-stu-id="3967c-123">After a few seconds, you will see a pair of URLs listed under **Report Server Web Service URLs**.</span></span>

5.  <span data-ttu-id="3967c-124">Haga clic en ambas direcciones URL para comprobar que puede obtener acceso a SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="3967c-124">Click both of the URLs to verify that you can access SQL Server Reporting Services.</span></span>

6.  <span data-ttu-id="3967c-125">Cierre el administrador de configuración de Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="3967c-125">Close Reporting Services Configuration Manager.</span></span>

</div>

<div>

## <a name="creating-a-system-center-operations-manager-database-for-use-with-sql-server-2008-r2"></a><span data-ttu-id="3967c-126">Crear una base de datos de System Center Operations Manager para usarla con SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3967c-126">Creating a System Center Operations Manager database for use with SQL Server 2008 R2</span></span>

<span data-ttu-id="3967c-127">Si desea configurar System Center Operations Manager para usar una base de datos de SQL Server 2008 R2, tendrá que crear manualmente la base de datos de Operations Manager en el equipo que ejecuta SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="3967c-127">If you want to configure System Center Operations Manager to use a SQL Server 2008 R2 database, you will need to "manually" create the Operations Manager database on the computer running SQL Server 2008 R2.</span></span> <span data-ttu-id="3967c-128">(Una vez más, estos pasos no son necesarios si usa SQL Server 2005 o SQL Server 2008 como base de datos back-end).</span><span class="sxs-lookup"><span data-stu-id="3967c-128">(Again, these steps are not required if you are using SQL Server 2005 or SQL Server 2008 as your back-end database.)</span></span>

<span data-ttu-id="3967c-129">Para crear manualmente una base de datos de Operations Manager, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3967c-129">To manually create an Operations Manager database do the following:</span></span>

1.  <span data-ttu-id="3967c-130">En el medio de instalación de System Center Operations Manager 2007 R2, en la \\ carpeta SupportTools AMD64, haga doble clic en **DBCreateWizard.exe**.</span><span class="sxs-lookup"><span data-stu-id="3967c-130">On the System Center Operations Manager 2007 R2 setup media, in the SupportTools\\AMD64 folder, double-click **DBCreateWizard.exe**.</span></span>

2.  <span data-ttu-id="3967c-131">En el Asistente para configuración de base de datos, en la página asistente **para configuración de base de datos** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-131">In the Database Configuration Wizard, on the **Welcome to the Database Configuration Wizard** page, click **Next**.</span></span>

3.  <span data-ttu-id="3967c-132">En la página información de la **base** de datos, mantenga toda la configuración tal cual y haga clic en **siguiente** .</span><span class="sxs-lookup"><span data-stu-id="3967c-132">On the **Database Information** page leave all the settings as-is and then click **Next**</span></span>

4.  <span data-ttu-id="3967c-133">En la **página Configuración del grupo de administración** , escriba un nombre para el grupo de administración (por ejemplo, supervisión de **Lync Server**) en el cuadro **nombre del grupo de administración** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-133">On the **Management Group Configuration** page type a name for your Management Group (for example, **Lync Server Monitoring**) in the **Management Group name** box and then click **Next**.</span></span>

5.  <span data-ttu-id="3967c-134">En la página **informes de errores de Operations Manager** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-134">On the **Operations Manager Error Reports** page click **Next**.</span></span>

6.  <span data-ttu-id="3967c-135">En la página **Resumen** , haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="3967c-135">On the **Summary** page click **Finish**.</span></span>

</div>

<div>

## <a name="creating-a-system-center-operations-manager-data-warehouse-for-use-with-sql-server-2008-r2"></a><span data-ttu-id="3967c-136">Crear un almacén de datos de System Center Operations Manager para su uso con SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3967c-136">Creating a System Center Operations Manager data warehouse for use with SQL Server 2008 R2</span></span>

<span data-ttu-id="3967c-137">Microsoft Lync Server 2013 viene con tres nuevos informes de System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="3967c-137">Microsoft Lync Server 2013 ships with three new System Center Operations Manager reports:</span></span>

  - <span data-ttu-id="3967c-138">**Informe de disponibilidad de escenario de principio a fin**   Este informe detalla la disponibilidad y el tiempo de actividad de los servicios clave de Lync Server, como el registro o la presencia.</span><span class="sxs-lookup"><span data-stu-id="3967c-138">**End to End Scenario Availability Report**   This report details the availability/uptime for key Lync Server services such as registration or presence.</span></span>

  - <span data-ttu-id="3967c-139">**Informe de capacidad**   Con la información de contador de rendimiento, este informe muestra tendencias de componentes del sistema, como la disponibilidad de memoria y el uso del procesador.</span><span class="sxs-lookup"><span data-stu-id="3967c-139">**Capacity Report**   Using performance counter information, this report shows trends for system components such as memory availability and processor usage.</span></span>

  - <span data-ttu-id="3967c-140">**Informe de componente**   Este informe muestra los principales generadores de alertas agrupados por el componente Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3967c-140">**Component Report**   This report lists the top alert generators grouped by Lync Server component.</span></span>

<span data-ttu-id="3967c-141">Para poder usar estos nuevos informes, debe instalar un almacén de datos de System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="3967c-141">In order to use these new reports you must install a System Center Operations Manager data warehouse.</span></span> <span data-ttu-id="3967c-142">(Un almacén de datos proporciona almacenamiento a largo plazo de datos de operaciones). Para usar un almacén de datos con SQL Server 2008 R2, debe llevar a cabo los siguientes pasos en el equipo que hospeda la base de datos de SQL Server:</span><span class="sxs-lookup"><span data-stu-id="3967c-142">(A data warehouse provides for long-term storage of operations data.) To use a data warehouse with SQL Server 2008 R2 you must carry out the following steps on the computer that hosts your SQL Server database:</span></span>

1.  <span data-ttu-id="3967c-143">En el medio de instalación de System Center Operations Manager, en la \\ carpeta SETUP SupportTools \\ AMD64, haga doble clic en **DBCreateWizard.exe**.</span><span class="sxs-lookup"><span data-stu-id="3967c-143">On the System Center Operations Manager setup media, in the Setup\\SupportTools\\AMD64 folder, double-click **DBCreateWizard.exe**.</span></span>

2.  <span data-ttu-id="3967c-144">En el Asistente para configuración de base de datos, en la página asistente **para configuración de base de datos** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-144">In the Database Configuration Wizard, on the **Welcome to the Database Configuration Wizard** page, click **Next**.</span></span>

3.  <span data-ttu-id="3967c-145">En la página **información** de la base de datos, seleccione base de datos del almacén de **datos de Operations Manager** de la lista desplegable **tipo de base** de datos y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-145">On the **Database Information** page, select **Operations Manager Data Warehouse Database** from the **Database Type** dropdown list and then click **Next**.</span></span>

4.  <span data-ttu-id="3967c-146">En la página **Resumen** , haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="3967c-146">On the **Summary** page click **Finish**.</span></span>

</div>

<div>

## <a name="installing-the-system-center-operations-manager-console"></a><span data-ttu-id="3967c-147">Instalar la consola de System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="3967c-147">Installing the System Center Operations Manager console</span></span>

<span data-ttu-id="3967c-148">La consola de Operations Manager es la principal herramienta que se usa para administrar System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="3967c-148">The Operations Manager console is the primary tool used to manage System Center Operations Manager.</span></span> <span data-ttu-id="3967c-149">Antes de instalar la consola de Operations Manager, asegúrese de que ha instalado una versión compatible de SQL Server junto con SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="3967c-149">Before you install the Operations Manager console, make sure that you have installed a supported version of SQL Server along with the SQL Server Reporting Service.</span></span> <span data-ttu-id="3967c-150">También se recomienda que ejecute el administrador de configuración de Reporting Services de SQL Server para comprobar que el servicio de informes se ha instalado y configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3967c-150">It is also recommended that you run SQL Server's Reporting Services Configuration Manager to verify that the Reporting Service has been correctly installed and configured.</span></span>

<span data-ttu-id="3967c-151">Para instalar la consola de System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="3967c-151">To install the System Center Operations Manager console:</span></span>

1.  <span data-ttu-id="3967c-152">En el medio de instalación de System Center Operations Manager, haga doble clic en **SetupOM.exe**.</span><span class="sxs-lookup"><span data-stu-id="3967c-152">On the System Center Operations Manager setup media, double-click **SetupOM.exe**.</span></span>

2.  <span data-ttu-id="3967c-153">En System Center Operations Manager 2007 R2 Setup, haga clic en **check Prerequisites**.</span><span class="sxs-lookup"><span data-stu-id="3967c-153">In System Center Operations Manager 2007 R2 Setup, click **Check Prerequisites**.</span></span>

3.  <span data-ttu-id="3967c-154">En el visor de requisitos previos de System Center Operations Manager, seleccione los componentes de System Center que se instalarán: (**servidor**; **Consola**; y **PowerShell**) y, a continuación, haga clic en **comprobar**.</span><span class="sxs-lookup"><span data-stu-id="3967c-154">In the System Center Operations Manager Prerequisite Viewer, select the System Center components to be installed: (**Server**; **Console**; and **PowerShell**) and then click **Check**.</span></span> <span data-ttu-id="3967c-155">Compruebe que no se han notificado problemas de bloqueo y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="3967c-155">Verify that no blocking issues have been reported and then click **Close**.</span></span> <span data-ttu-id="3967c-156">Si se ha notificado un problema de bloqueo, corrija el problema y, a continuación, haga clic en **comprobar** para volver a ejecutar las pruebas de requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="3967c-156">If a blocking issue has been reported, correct the problem and then click **Check** to re-run the prerequisite testing.</span></span>

4.  <span data-ttu-id="3967c-157">En el programa de instalación de System Center Operations Manager, haga clic en **instalar Operations Manager**.</span><span class="sxs-lookup"><span data-stu-id="3967c-157">In System Center Operations Manager Setup, click **Install Operations Manager**.</span></span>

5.  <span data-ttu-id="3967c-158">En el Asistente de configuración de System Center Operations Manager, en la página **Asistente de configuración de System Center Operations Manager** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-158">In the System Center Operations Manager Setup wizard, on the **Welcome to the System Center Operations Manager Setup Wizard** page, click **Next**.</span></span>

6.  <span data-ttu-id="3967c-159">En la página **contrato de licencia para el usuario final** , seleccione Acepto **los términos del contrato de licencia** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-159">On the **End-User License Agreement** page, select **I accept the terms in the license agreement** and then click **Next**.</span></span>

7.  <span data-ttu-id="3967c-160">En la página **registro del producto** , escriba su nombre en el cuadro Nombre de **usuario** y nombre de la organización en el cuadro **organización** .</span><span class="sxs-lookup"><span data-stu-id="3967c-160">On the **Product Registration** page, type your name in the **User Name** box and name of your organization in the **Organization** box.</span></span> <span data-ttu-id="3967c-161">Escriba la clave de producto de System Center Operations Manager en el cuadro **Escriba la clave de CD de 25 dígitos** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-161">Type your System Center Operations Manager product key in the **Enter your 25 digit CD Key** box and then click **Next**.</span></span>

8.  <span data-ttu-id="3967c-162">En la página **instalación personalizada** , seleccione las opciones de System Center que se instalarán y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-162">On the **Custom Setup** page select the System Center options to be installed and then click **Next**.</span></span> <span data-ttu-id="3967c-163">Debe seleccionar **servidor de administración**, **interfaces de usuario** y **consola web** para su instalación.</span><span class="sxs-lookup"><span data-stu-id="3967c-163">You should select **Management Server**, **User Interfaces**, and **Web Console** to be installed.</span></span> <span data-ttu-id="3967c-164">La **base de datos** no se debe seleccionar y no debe instalarse.</span><span class="sxs-lookup"><span data-stu-id="3967c-164">**Database** should not be selected and should not be installed.</span></span>

9.  <span data-ttu-id="3967c-165">En la página **instancia del servidor de base de datos SC** , compruebe que el nombre del equipo en el que están instaladas las bases de datos de Operations Manager aparece en el cuadro **System Center Database Server** .</span><span class="sxs-lookup"><span data-stu-id="3967c-165">On the **SC Database Server Instance** page, verify that the name of the computer where the Operations Manager databases are installed appears in the **System Center Database Server** box.</span></span> <span data-ttu-id="3967c-166">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-166">Click **Next**.</span></span>

10. <span data-ttu-id="3967c-167">En la página de la **cuenta de acción del servidor de administración** , seleccione **dominio o cuenta de equipo local** y, a continuación, escriba los valores correspondientes en los cuadros **cuenta de usuario**, **contraseña** y **dominio o equipo local** .</span><span class="sxs-lookup"><span data-stu-id="3967c-167">On the **Management Server Action Account** page, select **Domain or Local Computer Account** and then enter the appropriate values in the **User Account**, **Password**, and **Domain or local computer** boxes.</span></span> <span data-ttu-id="3967c-168">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-168">Click **Next**.</span></span>

11. <span data-ttu-id="3967c-169">En la página de la **cuenta de servicio de configuración y SDK** , seleccione **dominio o cuenta de equipo local** y, a continuación, escriba los valores apropiados en los cuadros **cuenta de usuario**, **contraseña** y **dominio o equipo local** .</span><span class="sxs-lookup"><span data-stu-id="3967c-169">On the **SDK and Config Service Account** page, select **Domain or Local Computer Account** and then enter the appropriate values in the **User Account**, **Password**, and **Domain or local computer** boxes.</span></span> <span data-ttu-id="3967c-170">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-170">Click **Next**.</span></span>

12. <span data-ttu-id="3967c-171">En la página **informes de errores de Operations Manager** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-171">On the **Operations Manager Error Reports** page click **Next**.</span></span>

13. <span data-ttu-id="3967c-172">En la página del programa de mejora de la **experiencia del cliente** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-172">On the **Customer Experience Improvement Program** page click **Next**.</span></span>

14. <span data-ttu-id="3967c-173">En la página **listo para instalar el programa** , haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="3967c-173">On the **Ready to Install the Program** page, click **Install**.</span></span>

15. <span data-ttu-id="3967c-174">En la página **finalización del programa de instalación de System Center Operations Manager** , desactive la casilla de verificación **clave de cifrado de copia de seguridad** e **inicie la consola** y haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="3967c-174">On the **Completing the System Center Operations Manager Setup** page, clear the **Backup Encryption Key** and **Start the console checkboxes** and then click **Finish**.</span></span>

16. <span data-ttu-id="3967c-175">En el programa de instalación de System Center Operations Manager, haga clic en **salir**.</span><span class="sxs-lookup"><span data-stu-id="3967c-175">In System Center Operations Manager Setup click **Exit**.</span></span>

</div>

<div>

## <a name="installing-system-center-reporting-services"></a><span data-ttu-id="3967c-176">Instalar System Center Reporting Services</span><span class="sxs-lookup"><span data-stu-id="3967c-176">Installing System Center Reporting Services</span></span>

<span data-ttu-id="3967c-177">Después de instalar y configurar la consola de System Center Operations Manager, debe instalar System Center Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="3967c-177">After installing and configuring the System Center Operations Manager console you must then install System Center Reporting Services.</span></span> <span data-ttu-id="3967c-178">Si usa SQL Server 2008 R2 como la base de datos back-end de Operations Manager, significa que primero debe realizar un cambio temporal en el grupo de seguridad asociado con SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="3967c-178">If you are using SQL Server 2008 R2 as your Operations Manager back-end database, that means that you must first make a temporary change to the security group associated with SQL Server Reporting Services.</span></span> <span data-ttu-id="3967c-179">Si usa SQL Server 2008 R2, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3967c-179">If you are using SQL Server 2008 R2, you must do the following:</span></span>

1.  <span data-ttu-id="3967c-180">Haga clic en **Inicio**, seleccione **herramientas administrativas** y, a continuación, haga clic en **Administrador del servidor**.</span><span class="sxs-lookup"><span data-stu-id="3967c-180">Click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span>

2.  <span data-ttu-id="3967c-181">En Administrador del servidor, expanda **configuración**, expanda **usuarios locales y grupos** y, a continuación, haga clic en **grupos**.</span><span class="sxs-lookup"><span data-stu-id="3967c-181">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="3967c-182">Busque el grupo siguiente, donde ATL-SC-001 representa el nombre de su equipo y ARCHINST representa la instancia de SQL Server para la base de datos de System Center: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10 \_ 50. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="3967c-182">Locate the following group, where atl-sc-001 represents the name of your computer and ARCHINST represents the SQL Server instance for the System Center database: **SQLServerReportServerUser$atl-sc-001$MSRS10\_50.ARCHINST**.</span></span>

4.  <span data-ttu-id="3967c-183">Haga clic con el botón secundario en el grupo y haga clic en **cambiar nombre**.</span><span class="sxs-lookup"><span data-stu-id="3967c-183">Right-click the group and then click **Rename**.</span></span> <span data-ttu-id="3967c-184">Cambie el nombre del grupo eliminando **\_ 50** del nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="3967c-184">Rename the group by deleting **\_50** from the group name.</span></span> <span data-ttu-id="3967c-185">Por ejemplo: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="3967c-185">For example: **SQLServerReportServerUser$atl-sc-001$MSRS10.ARCHINST**.</span></span>

5.  <span data-ttu-id="3967c-186">Cierre el administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="3967c-186">Close Server Manager.</span></span>

<span data-ttu-id="3967c-187">En este momento, está listo para instalar System Center Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="3967c-187">At this point you are ready to install System Center Reporting Services.</span></span> <span data-ttu-id="3967c-188">Para ello, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3967c-188">To do this:</span></span>

1.  <span data-ttu-id="3967c-189">En el medio de instalación de System Center Operations Manager 2007 R2, haga doble clic en **SetupOM.exe**.</span><span class="sxs-lookup"><span data-stu-id="3967c-189">On the System Center Operations Manager 2007 R2 Setup media, double-click **SetupOM.exe**.</span></span>

2.  <span data-ttu-id="3967c-190">En el programa de instalación de System Center Operations Manager 2007 R2, haga clic en **instalar informes de Operations Manager**.</span><span class="sxs-lookup"><span data-stu-id="3967c-190">In System Center Operations Manager 2007 R2 Setup, click **Install Operations Manager Reporting**.</span></span>

3.  <span data-ttu-id="3967c-191">En el Asistente de configuración de informes de System Center Operations Manager 2007 R2, en la página de configuración de informes de la **bienvenida a Operations Manager** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-191">In the System Center Operations Manager 2007 R2 Reporting Setup wizard, on the **Welcome to Operations Manager Reporting Setup** page, click **Next**.</span></span>

4.  <span data-ttu-id="3967c-192">En la página contrato de licencia para el **usuario final** , seleccione Acepto **las condiciones del contrato de licencia** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-192">On the **End-user License Agreement** page select **I accept the terms of the license agreement** and then click **Next**.</span></span>

5.  <span data-ttu-id="3967c-193">En la página **registro del producto** , asegúrese de que su nombre y el nombre de su organización aparecen en los cuadros nombre de **usuario** y **organización** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-193">On the **Product Registration** page, ensure that your name and the name of your organization appear in the **User Name** and **Organization** boxes and then click **Next**.</span></span>

6.  <span data-ttu-id="3967c-194">En la página **Configuración personalizada** , haga clic en **servidor de informes** y seleccione **este componente y todos los componentes dependientes se instalarán en la unidad de disco local**.</span><span class="sxs-lookup"><span data-stu-id="3967c-194">On the **Custom Setup** page, click **Reporting Server** and select **This component, and all dependent components, will be installed on local disk drive**.</span></span> <span data-ttu-id="3967c-195">Haga clic en **almacén de datos** y seleccione **este componente no estará disponible** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-195">Click **Data Warehouse** and select **This component will not be available**, and then click **Next**.</span></span>

7.  <span data-ttu-id="3967c-196">En la página **conectar con el servidor de administración raíz** , escriba el nombre del servidor de administración de raíz de Operations Manager en el cuadro **servidor de administración raíz** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-196">On the **Connect to the Root Management Server** page, type the name of your Operations Manager root management server in the **Root Management Server** box and then click **Next**.</span></span>

8.  <span data-ttu-id="3967c-197">En la página **conectar con el almacén de datos de Operations Manager** , escriba la instancia de SQL Server donde se encuentra el almacén de datos en el cuadro **instancia de SQL Server** .</span><span class="sxs-lookup"><span data-stu-id="3967c-197">On the **Connect to the Operations Manager Data Warehouse** page, type the SQL Server instance where your data warehouse is located in the **SQL Server Instance** box.</span></span> <span data-ttu-id="3967c-198">(Si el almacén de datos se encuentra en la instancia predeterminada, simplemente escriba el nombre del servidor; por ejemplo: ATL-SQL-001.) Compruebe que el nombre de la base de datos **OperationsManagerDW** aparece en el cuadro **nombre** y que el puerto **1433** aparece en el cuadro **Puerto de SQL Server** .</span><span class="sxs-lookup"><span data-stu-id="3967c-198">(If your data warehouse is located in the Default instance then simply type the server name; for example: atl-sql-001.) Verify that the database name **OperationsManagerDW** appears in the **Name** box, and that port **1433** appears in the **SQL Server port** box.</span></span> <span data-ttu-id="3967c-199">Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-199">Click **Next**.</span></span>

9.  <span data-ttu-id="3967c-200">En la página **instancia de SQL Server Reporting** , seleccione su SQL Server Reporting Server en la lista desplegable **entrar en el servidor de SQL Server Reporting Services** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-200">On the **SQL Server Reporting Instance** page, select your SQL Server reporting server from the **Enter the SQL Server Reporting Services Server** dropdown list and then click **Next**.</span></span>

10. <span data-ttu-id="3967c-201">En la página de escritura de la **cuenta de almacenamiento de datos** , escriba el nombre y la contraseña del usuario al que se asignará inicialmente permisos de escritura para el almacén de datos en los cuadros cuenta de **usuario** y **contraseña** .</span><span class="sxs-lookup"><span data-stu-id="3967c-201">On the **Data Warehouse Write Account** page, enter the name and password of the user to be initially assigned write permissions to the data warehouse in the **User Account** and **Password** boxes.</span></span> <span data-ttu-id="3967c-202">Seleccione el dominio del usuario de la lista desplegable **dominio** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-202">Select the user's domain from the **Domain** dropdown list and then click **Next**.</span></span>

11. <span data-ttu-id="3967c-203">En la página **cuenta de lector de datos** , escriba el nombre y la contraseña de la cuenta de usuario que se usará cuando SQL Reporting Services consulte el almacén de datos en los cuadros cuenta de **usuario** y **contraseña** .</span><span class="sxs-lookup"><span data-stu-id="3967c-203">On the **Data Reader Account** page, enter the name and password of the user account to be used when SQL Reporting Services queries the data warehouse in the **User Account** and **Password** boxes.</span></span> <span data-ttu-id="3967c-204">Seleccione el dominio de la cuenta en la lista desplegable **dominio** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-204">Select the account domain from the **Domain** dropdown list and then click **Next**.</span></span>

12. <span data-ttu-id="3967c-205">En la página **informes de datos operativos** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-205">On the **Operational Data Reports** page, click **Next**.</span></span>

13. <span data-ttu-id="3967c-206">En la página **Microsoft Update** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3967c-206">On the **Microsoft Update** page, click **Next**.</span></span>

14. <span data-ttu-id="3967c-207">En la página **listo para instalar el programa** , haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="3967c-207">On the **Ready to Install the Program** page, click **Install**.</span></span>

15. <span data-ttu-id="3967c-208">En la página **finalización del Asistente para la instalación de los componentes de informes de Operations Manager** , haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="3967c-208">On the **Completing the Operations Manager Reporting Components Setup Wizard** page, click **Finish**.</span></span>

16. <span data-ttu-id="3967c-209">En System Center Operations Manager 2007 R2 Setup, haga clic en **Exit**.</span><span class="sxs-lookup"><span data-stu-id="3967c-209">In System Center Operations Manager 2007 R2 Setup, click **Exit**.</span></span>

<span data-ttu-id="3967c-210">Después de haber instalado System Center reporting, use el siguiente procedimiento para restablecer el nombre del grupo de seguridad asociado a los informes de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3967c-210">After System Center reporting has been installed you then use the following procedure to reset the name of the security group associated with SQL Server reporting.</span></span> <span data-ttu-id="3967c-211">De nuevo, este procedimiento solo es necesario si usas SQL Server:</span><span class="sxs-lookup"><span data-stu-id="3967c-211">Again, this procedure is only required if you are using SQL Server:</span></span>

1.  <span data-ttu-id="3967c-212">Haga clic en **Inicio**, seleccione **herramientas administrativas** y, a continuación, haga clic en **Administrador del servidor**.</span><span class="sxs-lookup"><span data-stu-id="3967c-212">Click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span>

2.  <span data-ttu-id="3967c-213">En Administrador del servidor, expanda **configuración**, expanda **usuarios locales y grupos** y, a continuación, haga clic en **grupos**.</span><span class="sxs-lookup"><span data-stu-id="3967c-213">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="3967c-214">Busque el grupo siguiente, donde ATL-SC-001 representa el nombre de su equipo y ARCHINST representa la instancia de SQL Server para las bases de datos de archivado y supervisión: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="3967c-214">Locate the following group, where atl-sc-001 represents the name of your computer and ARCHINST represents the SQL Server instance for the archiving and monitoring databases: **SQLServerReportServerUser$atl-sc-001$MSRS10.ARCHINST**.</span></span>

4.  <span data-ttu-id="3967c-215">Haga clic con el botón secundario en el grupo y haga clic en **cambiar nombre**.</span><span class="sxs-lookup"><span data-stu-id="3967c-215">Right-click the group and then click **Rename**.</span></span> <span data-ttu-id="3967c-216">Cambie el nombre del grupo agregando **\_ 50** al final del nombre del grupo, justo antes del nombre de la instancia de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3967c-216">Rename the group by adding **\_50** to the end of the group name, right before the SQL Server instance name.</span></span> <span data-ttu-id="3967c-217">Por ejemplo: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10 \_ 50. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="3967c-217">For example: **SQLServerReportServerUser$atl-sc-001$MSRS10\_50.ARCHINST**.</span></span>

5.  <span data-ttu-id="3967c-218">Cierre el administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="3967c-218">Close Server Manager.</span></span>

<span data-ttu-id="3967c-219">Si la consola de Operations System Center está abierta, tendrá que cerrar la aplicación y, a continuación, reiniciarla. Si no lo hace, la ficha **informes** no aparecerá en la interfaz de usuario de la consola de operaciones.</span><span class="sxs-lookup"><span data-stu-id="3967c-219">If the System Center Operations Console is open you will need to close the application and then restart it; if you do not do this the **Reporting** tab will not appear in the Operations Console user interface.</span></span> <span data-ttu-id="3967c-220">Tenga en cuenta que, después de reiniciar la consola de operaciones por primera vez, puede demorar varios minutos en aparecer todos los informes de supervisión en la pestaña **informes** .</span><span class="sxs-lookup"><span data-stu-id="3967c-220">Note that, after restarting the Operations Console the first time, it could take several minutes before all the Monitoring Reports appear on the **Reporting** tab.</span></span>

<span data-ttu-id="3967c-221"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3967c-221"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

