---
title: 'Lync Server 2013: crear la configuración de la calidad de la experiencia'
description: 'Lync Server 2013: crear una configuración de la calidad de la experiencia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create Quality of Experience configuration settings
ms:assetid: 64f05569-07c7-4f76-a96b-ea4125a510d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521006(v=OCS.15)
ms:contentKeyID: 48184357
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 279265f396fc8fcbfba80d195fc587924a2979f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431613"
---
# <a name="create-quality-of-experience-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="7baf8-103">Crear la configuración de la calidad de la experiencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7baf8-103">Create Quality of Experience configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7baf8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7baf8-104">

<span> </span></span></span>

<span data-ttu-id="7baf8-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="7baf8-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="7baf8-p101">Las métricas de calidad de la experiencia (QoE) realizan un seguimiento de la calidad de las llamadas de audio y vídeo que se han efectuado en la organización, incluido la cantidad de paquetes de red perdidos, el ruido de fondo y la cantidad de "vibración" (diferencias en el retraso de paquetes). Esta información se almacena en una base de datos independiente de otras estadísticas, como los registros de detalles de llamadas, lo que permite activar y desactivar las métricas QoE de manera independiente de otros datos registrados.</span><span class="sxs-lookup"><span data-stu-id="7baf8-p101">Quality of Experience (QoE) metrics track the quality of audio and video calls made in your organization, including such things as the number of network packets lost, background noise, and the amount of "jitter" (differences in packet delay). These metrics are stored in a database apart from other data (such as call detail records), which allows you to enable and disable QoE independent of other data recording.</span></span>

<span data-ttu-id="7baf8-108">Al instalar Microsoft Lync Server 2013, se crea una única colección global de parámetros de configuración de QoE.</span><span class="sxs-lookup"><span data-stu-id="7baf8-108">When you install Microsoft Lync Server 2013, a single, global collection of QoE configuration settings is created for you.</span></span> <span data-ttu-id="7baf8-109">Los administradores también tienen la posibilidad de crear opciones personalizadas en el ámbito del sitio.</span><span class="sxs-lookup"><span data-stu-id="7baf8-109">Administrators also have the option of creating custom settings at the site scope.</span></span> <span data-ttu-id="7baf8-110">Cuando estas opciones de ámbito de sitio se usan, tienen prioridad frente a la configuración global.</span><span class="sxs-lookup"><span data-stu-id="7baf8-110">Whenever these site-scoped settings are used, they take precedence over the global settings.</span></span> <span data-ttu-id="7baf8-111">Así, por ejemplo, si crea opciones de ámbito de sitio para el sitio de Redmond, serán las opciones que se usen (y no la configuración global) para administrar la calidad de la experiencia en Redmond.</span><span class="sxs-lookup"><span data-stu-id="7baf8-111">For example, if you create site-scoped settings for the Redmond site then those settings (rather than the global settings) will be used to manage QoE in Redmond.</span></span>

<span data-ttu-id="7baf8-112">Las opciones de configuración de QoE se pueden crear con el panel de control de Lync Server o el cmdlet [New-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsQoEConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="7baf8-112">QoE configuration settings can be created by using either Lync Server Control Panel or the [New-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsQoEConfiguration) cmdlet.</span></span> <span data-ttu-id="7baf8-113">Si está usando el panel de control de Lync Server para crear una nueva configuración, las siguientes opciones estarán disponibles:</span><span class="sxs-lookup"><span data-stu-id="7baf8-113">If you are using Lync Server Control Panel to create new settings the following options will be available to you:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7baf8-114">Valor de IU</span><span class="sxs-lookup"><span data-stu-id="7baf8-114">UI Setting</span></span></th>
<th><span data-ttu-id="7baf8-115">Parámetro de PowerShell</span><span class="sxs-lookup"><span data-stu-id="7baf8-115">PowerShell Parameter</span></span></th>
<th><span data-ttu-id="7baf8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="7baf8-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7baf8-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="7baf8-117">Name</span></span></p></td>
<td><p><span data-ttu-id="7baf8-118">Identidad</span><span class="sxs-lookup"><span data-stu-id="7baf8-118">Identity</span></span></p></td>
<td><p><span data-ttu-id="7baf8-p104">Identificador único de la opción que se va a crear. La opción de configuración de QoE solo se puede crear en el ámbito del sitio.</span><span class="sxs-lookup"><span data-stu-id="7baf8-p104">Unique identifier for the settings to be created. QoE configuration settings can only be created at the site scope.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7baf8-121">Habilitar supervisión de datos de calidad de la experiencia (QoE)</span><span class="sxs-lookup"><span data-stu-id="7baf8-121">Enable monitoring of QoE data</span></span></p></td>
<td><p><span data-ttu-id="7baf8-122">EnableQoE</span><span class="sxs-lookup"><span data-stu-id="7baf8-122">EnableQoE</span></span></p></td>
<td><p><span data-ttu-id="7baf8-123">Especifica si los registros QoE se recopilarán y guardarán en la base de datos de supervisión.</span><span class="sxs-lookup"><span data-stu-id="7baf8-123">Specifies whether QoE records will be collected and saved to the monitoring database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7baf8-124">Habilitar purgado de datos de calidad de la experiencia (QoE)</span><span class="sxs-lookup"><span data-stu-id="7baf8-124">Enable purging of QoE data</span></span></p></td>
<td><p><span data-ttu-id="7baf8-125">EnablePurging</span><span class="sxs-lookup"><span data-stu-id="7baf8-125">EnablePurging</span></span></p></td>
<td><p><span data-ttu-id="7baf8-126">Especifica si los registros se van a purgar una vez transcurrida la duración definida en la propiedad <strong>Conservar datos de QoE durante el período de duración máximo (días)</strong>.</span><span class="sxs-lookup"><span data-stu-id="7baf8-126">Specifies whether records will be purged after the duration defined in the <strong>Keep QoE data for a maximum duration (days)</strong> property has elapsed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7baf8-127">Conservar datos de calidad de la experiencia (QoE) durante un máximo de (días)</span><span class="sxs-lookup"><span data-stu-id="7baf8-127">Keep QoE data for maximum duration (days)</span></span></p></td>
<td><p><span data-ttu-id="7baf8-128">KeepQoEDataForDays</span><span class="sxs-lookup"><span data-stu-id="7baf8-128">KeepQoEDataForDays</span></span></p></td>
<td><p><span data-ttu-id="7baf8-p105">Cantidad de días en que los datos de QoE se almacenarán antes de que se purguen de la base de datos. Este valor se ignora si el purgado está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7baf8-p105">Number of days QoE data will be stored before being purged from the database. This value is ignored if purging is disabled.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="7baf8-131">El cmdlet New-CsQoEConfiguration incluye opciones adicionales que no están disponibles en el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7baf8-131">The New-CsQoEConfiguration cmdlet includes additional options not available in Lync Server Control Panel.</span></span> <span data-ttu-id="7baf8-132">Para obtener más información, vea el tema <A href="https://docs.microsoft.com/powershell/module/skype/New-CsQoEConfiguration">de ayuda nuevo-CsQoEConfiguration</A> .</span><span class="sxs-lookup"><span data-stu-id="7baf8-132">For more information, see the <A href="https://docs.microsoft.com/powershell/module/skype/New-CsQoEConfiguration">New-CsQoEConfiguration</A> help topic.</span></span>



</div>

<div>

## <a name="to-create-qoe-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="7baf8-133">Para crear la configuración de la calidad de la aplicación con el panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="7baf8-133">To create QoE configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="7baf8-134">Inicie sesión en el equipo como miembro del grupo RTCUniversalServerAdmins o como miembro del rol CsVoiceAdministrator, CsServerAdministrator o CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="7baf8-134">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="7baf8-135">Para obtener más información, consulte [permisos de configuración de delegación en Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="7baf8-135">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="7baf8-136">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7baf8-136">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7baf8-137">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7baf8-137">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7baf8-138">En la barra de navegación izquierda, haga clic en **Configuración y archivado** y, luego, en **Datos sobre la calidad de la experiencia**.</span><span class="sxs-lookup"><span data-stu-id="7baf8-138">In the left navigation bar, click **Monitoring and Archiving**, and then click **Quality of Experience Data**.</span></span>

4.  <span data-ttu-id="7baf8-139">En la página **Datos de calidad de la experiencia**, haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="7baf8-139">On the **Quality of Experience Data** page, click **New**.</span></span>

5.  <span data-ttu-id="7baf8-140">En **Seleccionar un sitio**, haga clic en el sitio al que va a aplicar la directiva y, luego, en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7baf8-140">In **Select a Site**, click the site to which the policy is to be applied, and click **OK**.</span></span>

6.  <span data-ttu-id="7baf8-141">En **Nueva configuración de calidad de la experiencia**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7baf8-141">In **New Quality of Experience Setting**, do the following:</span></span>
    
      - <span data-ttu-id="7baf8-142">Seleccione **Habilitar supervisión de datos de calidad de la experiencia (QoE)** para activar la supervisión.</span><span class="sxs-lookup"><span data-stu-id="7baf8-142">Select **Enable monitoring of QoE data** to turn on monitoring.</span></span>
    
      - <span data-ttu-id="7baf8-143">Seleccione **Habilitar purgado de datos de calidad de la experiencia (QoE)** para activar el purgado.</span><span class="sxs-lookup"><span data-stu-id="7baf8-143">Select **Enable purging of QoE data** to turn on purging.</span></span>
    
      - <span data-ttu-id="7baf8-144">En **Conservar datos de calidad de la experiencia (QoE) durante un máximo de (días)**, seleccione la cantidad máxima de días durante la que se tienen que conservar los registros de QoE.</span><span class="sxs-lookup"><span data-stu-id="7baf8-144">In **Keep QoE for maximum duration (days)**, select the maximum number of days that QoE records should be retained.</span></span>

7.  <span data-ttu-id="7baf8-145">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="7baf8-145">Click **Commit**.</span></span>

</div>

<div>

## <a name="creating-qoe-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="7baf8-146">Creación de parámetros de configuración de QoE con cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7baf8-146">Creating QoE Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="7baf8-147">Puede crear parámetros de configuración de QoE mediante Windows PowerShell y el cmdlet New-CsQoEConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7baf8-147">You can create QoE configuration settings by using Windows PowerShell and the New-CsQoEConfiguration cmdlet.</span></span> <span data-ttu-id="7baf8-148">Puede ejecutar este cmdlet desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7baf8-148">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="7baf8-149">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="7baf8-149">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-collection-of-qoe-configuration-settings"></a><span data-ttu-id="7baf8-150">Para crear una colección de opciones de configuración de QoE</span><span class="sxs-lookup"><span data-stu-id="7baf8-150">To create a new collection of QoE configuration settings</span></span>

  - <span data-ttu-id="7baf8-151">Con este comando se crea una colección de opciones de configuración de QoE para usarla en el sitio de Redmond:</span><span class="sxs-lookup"><span data-stu-id="7baf8-151">This command creates a new collection of QoE configuration settings applied to the Redmond site:</span></span>
    
        New-CsQoEConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-collection-of-qoe-configuration-settings-where-qoe-monitoring-is-disabled"></a><span data-ttu-id="7baf8-152">Para crear una colección de opciones de configuración de QoE cuando la supervisión de QoE está deshabilitada</span><span class="sxs-lookup"><span data-stu-id="7baf8-152">To create a new collection of QoE configuration settings where QoE monitoring is disabled</span></span>

  - <span data-ttu-id="7baf8-p110">Dado que en el comando anterior no se ha especificado ningún parámetro (aparte del obligado Identity), la nueva colección de opciones de configuración usará los valores predeterminados en todas sus propiedades. Para crear opciones que usen otros valores de propiedad, bastará con incluir el parámetro y los valores que sean adecuados. Por ejemplo, use un comando como el siguiente para crear una colección de opciones de configuración de calidad de la experiencia que permita deshabilitar el registro de QoE de forma predeterminada:</span><span class="sxs-lookup"><span data-stu-id="7baf8-p110">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding command, the new collection of configuration settings will use the default values for all its properties. To create settings that use different property values, simply include the appropriate parameter and parameter value. For example, to create a collection of Quality of Experience configuration settings that, by default, allow disable QoE recording use a command like this:</span></span>
    
        New-CsQoEConfiguration -Identity "site:Redmond" -EnableQoE $False

</div>

<div>

## <a name="to-specify-multiple-property-values-when-creating-a-new-collection-of-qoe-configuration-settings"></a><span data-ttu-id="7baf8-156">Para especificar varios valores de propiedad al crear una colección de opciones de configuración de QoE</span><span class="sxs-lookup"><span data-stu-id="7baf8-156">To specify multiple property values when creating a new collection of QoE configuration settings</span></span>

  - <span data-ttu-id="7baf8-p111">Si desea especificar varios valores de propiedad, es preciso incluir varios parámetros. Por ejemplo, con este comando se configuran nuevas opciones que permiten conservar los datos de QoE durante 30 días y purgar los datos antiguos a las 3:00 AM:</span><span class="sxs-lookup"><span data-stu-id="7baf8-p111">You can multiple property values by including multiple parameters. For example, this command configures the new settings to keep QoE data for 30 days and to purge old data at 3:00 AM:</span></span>
    
        New-CsQoEConfiguration -Identity "site:Redmond" -KeepQoEDataForDays 30 -PurgeHourOfDay 3

</div>

<span data-ttu-id="7baf8-159">Para obtener más información, vea el tema de ayuda sobre el cmdlet [New-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsQoEConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="7baf8-159">For more information, see the help topic for the [New-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsQoEConfiguration) cmdlet.</span></span>

<span data-ttu-id="7baf8-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7baf8-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

