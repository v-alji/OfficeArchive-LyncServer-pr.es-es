---
title: 'Lync Server 2013: uso de Config.xml para realizar tareas de instalación'
description: 'Lync Server 2013: usar Config.xml para realizar tareas de instalación.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Config.xml to perform installation tasks
ms:assetid: 0813184a-ab40-417c-b3a3-c2090766b831
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204651(v=OCS.15)
ms:contentKeyID: 48183332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22fff14e21a120c3a0ee2cd6432fd1eba2bbee5f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438956"
---
# <a name="using-configxml-to-perform-installation-tasks-in-lync-server-2013"></a><span data-ttu-id="74209-103">Usar Config.xml para realizar tareas de instalación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74209-103">Using Config.xml to perform installation tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="74209-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="74209-104">

<span> </span></span></span>

<span data-ttu-id="74209-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="74209-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="74209-p101">Aunque la Herramienta de personalización de Office (OCT) es la principal herramienta de instalación personalizada, los administradores pueden usar el archivo Config.xml para especificar instrucciones de instalación adicionales que no estén disponibles en la OCT. Las personalizaciones que se describen a continuación solo se pueden llevar a cabo mediante el archivo Config.xml:</span><span class="sxs-lookup"><span data-stu-id="74209-p101">Although the Office Customization Tool (OCT) is the primary tool for customization installation, administrators can use the Config.xml file to specify additional installation instructions that are not available in the OCT. The following customizations can only be made by using the Config.xml file:</span></span>

  - <span data-ttu-id="74209-108">Especifique la ruta de acceso del punto de instalación de red.</span><span class="sxs-lookup"><span data-stu-id="74209-108">Specify the path of the network installation point.</span></span>

  - <span data-ttu-id="74209-109">Seleccione los productos que desea instalar.</span><span class="sxs-lookup"><span data-stu-id="74209-109">Select the products to install.</span></span>

  - <span data-ttu-id="74209-110">Configure el registro y la ubicación del archivo de personalización de la instalación y las actualizaciones de software.</span><span class="sxs-lookup"><span data-stu-id="74209-110">Configure logging and the location of the Setup customization file and software updates.</span></span>

  - <span data-ttu-id="74209-111">Especifique las opciones de instalación como, por ejemplo, el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="74209-111">Specify installation options, such as user name.</span></span>

  - <span data-ttu-id="74209-112">Copie el origen de instalación local (LIS) en el equipo del usuario sin instalar Office.</span><span class="sxs-lookup"><span data-stu-id="74209-112">Copy the local installation source (LIS) to the user's computer without installing Office.</span></span>

  - <span data-ttu-id="74209-113">Agregue o quite idiomas de la instalación.</span><span class="sxs-lookup"><span data-stu-id="74209-113">Add or remove languages from the installation.</span></span>

<span data-ttu-id="74209-114">Le recomendamos que use el archivo Config.xml para configurar la instalación silenciosa de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="74209-114">We recommend that you use the Config.xml file to configure Lync 2013 silent installation.</span></span>

<span data-ttu-id="74209-115">De forma predeterminada, el archivo de Config.xml que se almacena en la carpeta del producto principal (por ejemplo, \\ producto. WW) indica al programa de instalación que instale ese producto.</span><span class="sxs-lookup"><span data-stu-id="74209-115">By default, the Config.xml file that is stored in the core product folder (for example, \\product.WW) directs Setup to install that product.</span></span> <span data-ttu-id="74209-116">Por ejemplo, el archivo Config.xml de la siguiente carpeta instala Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="74209-116">For example, the Config.xml file in the following folder installs Lync 2013:</span></span>

  - <span data-ttu-id="74209-117">\\\\\\compartir servidor \\ Lync15 \\ Lync. WW \\Config.xml</span><span class="sxs-lookup"><span data-stu-id="74209-117">\\\\server\\share\\Lync15\\Lync.WW \\Config.xml</span></span>

<span data-ttu-id="74209-118">En la tabla siguiente se enumeran los elementos Config.xml más usados en la instalación de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="74209-118">The Config.xml elements most commonly used for Lync 2013 installation are listed in the following table.</span></span>

### <a name="configxml-elements"></a><span data-ttu-id="74209-119">Elementos de Config.xml</span><span class="sxs-lookup"><span data-stu-id="74209-119">Config.xml elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74209-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="74209-120">Element</span></span></th>
<th><span data-ttu-id="74209-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="74209-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74209-122">Configuración</span><span class="sxs-lookup"><span data-stu-id="74209-122">Configuration</span></span></p></td>
<td><p><span data-ttu-id="74209-123">Elemento de nivel superior (obligatorio).</span><span class="sxs-lookup"><span data-stu-id="74209-123">Top-level element (required).</span></span> <span data-ttu-id="74209-124">Contiene el atributo product, por ejemplo: producto = Lync</span><span class="sxs-lookup"><span data-stu-id="74209-124">Contains the Product attribute, for example: Product=Lync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74209-125">OptionState</span><span class="sxs-lookup"><span data-stu-id="74209-125">OptionState</span></span></p></td>
<td><p><span data-ttu-id="74209-126">Especifica cómo se controlan las características específicas del producto durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="74209-126">Specifies how specific product features are handled during installation.</span></span> <span data-ttu-id="74209-127">Use los siguientes atributos para impedir la instalación de los servicios de conectividad empresarial, que incluyen componentes compartidos que interfieren con Outlook 2010:</span><span class="sxs-lookup"><span data-stu-id="74209-127">Use the following attributes to prevent installation of Business Connectivity Services, which includes shared components that interfere with Outlook 2010:</span></span></p>
<ul>
<li><p><span data-ttu-id="74209-128">ID = &quot; LOBiMain&quot;</span><span class="sxs-lookup"><span data-stu-id="74209-128">Id=&quot;LOBiMain&quot;</span></span></p></li>
<li><p><span data-ttu-id="74209-129">Estado = &quot; ausente&quot;</span><span class="sxs-lookup"><span data-stu-id="74209-129">State=&quot;Absent&quot;</span></span></p></li>
<li><p><span data-ttu-id="74209-130">Children = &quot; Force&quot;</span><span class="sxs-lookup"><span data-stu-id="74209-130">Children=&quot;Force&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74209-131">Pantalla</span><span class="sxs-lookup"><span data-stu-id="74209-131">Display</span></span></p></td>
<td><p><span data-ttu-id="74209-p105">El nivel de interfaz de usuario que el programa de instalación muestra al usuario. Los atributos típicos incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="74209-p105">The level of UI that Setup displays to the user. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="74209-134">CompletionNotice = &quot; yes &quot;  |  &quot; no &quot; (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="74209-134">CompletionNotice=&quot;Yes&quot; | &quot;No&quot;(default)</span></span></p></li>
<li><p><span data-ttu-id="74209-135">AcceptEula = &quot; yes &quot;  |  &quot; no &quot; (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="74209-135">AcceptEula=&quot;Yes&quot; | &quot;No&quot;(default)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74209-136">Registro</span><span class="sxs-lookup"><span data-stu-id="74209-136">Logging</span></span></p></td>
<td><p><span data-ttu-id="74209-p106">Opciones para el tipo de registro que realiza el programa de instalación. Los atributos típicos incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="74209-p106">Options for the kind of logging that Setup performs. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="74209-139">Type = &quot; OFF &quot;  |  &quot; Standard &quot; (valor predeterminado) | &quot; Detallado&quot;</span><span class="sxs-lookup"><span data-stu-id="74209-139">Type =&quot;Off&quot; | &quot;Standard&quot;(default) | &quot;Verbose&quot;</span></span></p></li>
<li><p><span data-ttu-id="74209-140">Template=”filename.txt” (el nombre del archivo de registro)</span><span class="sxs-lookup"><span data-stu-id="74209-140">Template=”filename.txt” (the name of the log file)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74209-141">Configuración</span><span class="sxs-lookup"><span data-stu-id="74209-141">Setting</span></span></p></td>
<td><p><span data-ttu-id="74209-p107">Especifica los valores de propiedades de Windows Installer. Los atributos típicos incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="74209-p107">Specifies values for Windows Installer properties. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="74209-144">Setting ID = &quot; name &quot; (el nombre de la propiedad de Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="74209-144">Setting Id=&quot;name&quot; (the name of the Windows Installer property)</span></span></p></li>
<li><p><span data-ttu-id="74209-145">Value = &quot; Value &quot; (el valor que se asignará a la propiedad)</span><span class="sxs-lookup"><span data-stu-id="74209-145">Value=&quot;value&quot; (the value to assign to the property)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74209-146">DistributionPoint</span><span class="sxs-lookup"><span data-stu-id="74209-146">DistributionPoint</span></span></p></td>
<td><p><span data-ttu-id="74209-p108">La ruta de acceso completa del punto de instalación de red desde la que se ejecuta la instalación. Incluye el atributo de ubicación:</span><span class="sxs-lookup"><span data-stu-id="74209-p108">The fully qualified path of the network installation point from which the installation is to run. Includes the Location attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="74209-149">Location=”path”</span><span class="sxs-lookup"><span data-stu-id="74209-149">Location=”path”</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74209-150">En el ejemplo siguiente se muestra un archivo Config.xml para una instalación silenciosa de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="74209-150">The following example shows a Config.xml file for a typical silent installation of Lync 2013.</span></span>

    <Configuration Product="Lync">
      <OptionState Id="LOBiMain" State="Absent" Children="Force" />
      <Display Level="None" CompletionNotice="No" AcceptEula="Yes" />
      <Logging Type="verbose" Path="%temp%" Template="LyncSetupVerbose(*).log" />
      <Setting Id="SETUP_REBOOT" Value="Never" />
      <DistributionPoint Location="\\server\share\Lync15" />
    </Configuration>

<span data-ttu-id="74209-151">Encontrará información detallada sobre cómo usar el archivo de Config.xml para realizar tareas de instalación y mantenimiento de Office en <https://go.microsoft.com/fwlink/p/?linkid=267514> .</span><span class="sxs-lookup"><span data-stu-id="74209-151">Detailed information about using the Config.xml file to perform Office installation and maintenance tasks is available at <https://go.microsoft.com/fwlink/p/?linkid=267514>.</span></span>

<div>

## <a name="to-customize-the-configxml-file"></a><span data-ttu-id="74209-152">Para personalizar el archivo Config.xml</span><span class="sxs-lookup"><span data-stu-id="74209-152">To customize the Config.xml file</span></span>

1.  <span data-ttu-id="74209-153">Abra el archivo Config.xml usando una herramienta de edición de texto como el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="74209-153">Open the Config.xml file by using a text editor tool, such as Notepad.</span></span>

2.  <span data-ttu-id="74209-154">Localice las líneas que contienen los elementos que desee cambiar.</span><span class="sxs-lookup"><span data-stu-id="74209-154">Locate the lines that contain the elements you want to change.</span></span>

3.  <span data-ttu-id="74209-155">Modifique la entrada de elemento con las opciones silenciosas que desea usar.</span><span class="sxs-lookup"><span data-stu-id="74209-155">Modify the element entry with the silent options that you want to use.</span></span> <span data-ttu-id="74209-156">Asegúrese de quitar los delimitadores de comentarios, " \<\!--" and "--\> ".</span><span class="sxs-lookup"><span data-stu-id="74209-156">Make sure that you remove the comment delimiters, "\<\!--" and "--\>".</span></span> <span data-ttu-id="74209-157">Por ejemplo, utilice la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="74209-157">For example, use the following syntax:</span></span>
    
        < DistributionPoint Location="\\server\share\Lync15" />

4.  <span data-ttu-id="74209-158">Guarde el archivo Config.xml.</span><span class="sxs-lookup"><span data-stu-id="74209-158">Save the Config.xml file.</span></span>

<span data-ttu-id="74209-159"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="74209-159"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

