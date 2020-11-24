---
title: Configurar el cliente de Skype empresarial en Lync Server 2013
description: Configure el cliente de Skype empresarial en Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure the client experience
ms:assetid: 61e783f1-24f4-430b-ae52-c76a4d206dc7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn954919(v=OCS.15)
ms:contentKeyID: 65227958
ms.date: 09/18/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c7f75ae0fa61d9048991934a0ecce7a886079961
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398369"
---
# <a name="configure-the-client-experience-with-skype-for-business"></a><span data-ttu-id="bffad-103">Configure the client experience with Skype for Business</span><span class="sxs-lookup"><span data-stu-id="bffad-103">Configure the client experience with Skype for Business</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bffad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bffad-104">

<span> </span></span></span>

<span data-ttu-id="bffad-105">_**Última modificación del tema:** 2015-09-17_</span><span class="sxs-lookup"><span data-stu-id="bffad-105">_**Topic Last Modified:** 2015-09-17_</span></span>

<span data-ttu-id="bffad-106">**Resumen:** En este tema se describe cómo configurar la experiencia de cliente para los usuarios de clientes de Skype empresarial en un entorno de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bffad-106">**Summary:** This topic describes how to configure the client experience for Skype for Business client users in a Lync Server 2013 environment.</span></span> <span data-ttu-id="bffad-107">Puede configurar la experiencia de cliente solo si está ejecutando Lync Server 2013 con la actualización acumulativa de diciembre de 2014 (5.0.8308.857) o una versión posterior instalada.</span><span class="sxs-lookup"><span data-stu-id="bffad-107">You can configure the client experience only if you are running Lync Server 2013 with the December 2014 Cumulative Update (5.0.8308.857) or later installed.</span></span> <span data-ttu-id="bffad-108">Para obtener más información sobre cómo actualizar Lync Server 2013, vea [actualizaciones para Lync server 2013](https://go.microsoft.com/fwlink/p/?linkid=532651).</span><span class="sxs-lookup"><span data-stu-id="bffad-108">For information about updating Lync Server 2013, see [Updates for Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=532651).</span></span>

<span data-ttu-id="bffad-109">Skype empresarial ofrece una nueva experiencia de usuario que se basa en la experiencia de producto de consumo de Skype.</span><span class="sxs-lookup"><span data-stu-id="bffad-109">Skype for Business provides a new user experience that is based on the Skype consumer product experience.</span></span> <span data-ttu-id="bffad-110">Además de todas las características de Lync, Skype empresarial proporciona nuevas características con controles simplificados y iconos conocidos.</span><span class="sxs-lookup"><span data-stu-id="bffad-110">In addition to all the features of Lync, Skype for Business provides new features with simplified controls and familiar icons.</span></span> <span data-ttu-id="bffad-111">Para obtener información detallada sobre la nueva experiencia del cliente, vea [Lync ahora es Skype empresarial: vea](https://go.microsoft.com/fwlink/?linkid=529022)las novedades.</span><span class="sxs-lookup"><span data-stu-id="bffad-111">For detailed information about the new client experience, see [Lync is now Skype for Business -- see what's new](https://go.microsoft.com/fwlink/?linkid=529022).</span></span>

<span data-ttu-id="bffad-112">Lync Server 2013 admite la nueva experiencia de cliente de Skype empresarial, así como la experiencia del cliente de Lync.</span><span class="sxs-lookup"><span data-stu-id="bffad-112">Lync Server 2013 supports the new Skype for Business client experience as well as the Lync client experience.</span></span> <span data-ttu-id="bffad-113">Como administrador, puede elegir la experiencia de cliente preferida para sus usuarios.</span><span class="sxs-lookup"><span data-stu-id="bffad-113">As an administrator, you can choose the preferred client experience for your users.</span></span> <span data-ttu-id="bffad-114">Por ejemplo, es posible que desee implementar la experiencia del cliente de Lync hasta que los usuarios de su organización estén completamente capacitados en la nueva experiencia de Skype empresarial.</span><span class="sxs-lookup"><span data-stu-id="bffad-114">For example, you might want to deploy the Lync client experience until users in your organization are fully trained in the new Skype for Business experience.</span></span> <span data-ttu-id="bffad-115">O bien, si aún no ha actualizado todos los usuarios a Skype empresarial Server 2015, es posible que quiera que todos los usuarios tengan la misma experiencia de cliente hasta que se actualicen al nuevo servidor.</span><span class="sxs-lookup"><span data-stu-id="bffad-115">Or, if you have not yet upgraded all users to Skype for Business Server 2015, you might want all users to have the same client experience until all are upgraded to the new server.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="bffad-116">Si su organización tiene implementadas las versiones de Skype empresarial Server 2015 y de Lync Server 2013, la experiencia del cliente predeterminada variará según las versiones del servidor y la configuración de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="bffad-116">If your organization has both Skype for Business Server 2015 and Lync Server 2013 deployed, the default client experience will differ depending on server versions and UI settings.</span></span> <span data-ttu-id="bffad-117">Cuando los usuarios inicien Skype empresarial por primera vez, verán siempre la interfaz de usuario de Skype empresarial, aunque haya seleccionado la interfaz de usuario de Lync.</span><span class="sxs-lookup"><span data-stu-id="bffad-117">When users launch Skype for Business for the first time, they will always see the Skype for Business user interface--even if you have selected the Lync user interface.</span></span> <span data-ttu-id="bffad-118">Después de varios minutos, se pide a los usuarios que cambien al modo de Lync.</span><span class="sxs-lookup"><span data-stu-id="bffad-118">After several minutes, users are asked to switch to Lync mode.</span></span> <span data-ttu-id="bffad-119">Para más información, vea <STRONG>Comportamiento del cliente en el primer inicio</STRONG> más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="bffad-119">For more information, see <STRONG>First launch client behavior</STRONG> later in this topic.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="bffad-120">La experiencia de cliente de Lync 2013 no es una opción para las versiones de cliente de Skype empresarial 2016.</span><span class="sxs-lookup"><span data-stu-id="bffad-120">The Lync 2013 client experience is not an option for Skype for Business 2016 client versions.</span></span> <span data-ttu-id="bffad-121">Antes de que intente configurar su entorno de cliente para usar el cliente de Lync 2013, compruebe la versión y asegúrese de que no empieza con el número 16; por ejemplo: 16.x.x.x.</span><span class="sxs-lookup"><span data-stu-id="bffad-121">Before you attempt to configure your client environment to use the Lync 2013 client, please check the client version to ensure it does not start with the number 16; for example: 16.x.x.x.</span></span>



</div>

<div>

## <a name="configure-the-client-experience"></a><span data-ttu-id="bffad-122">Configure the client experience</span><span class="sxs-lookup"><span data-stu-id="bffad-122">Configure the client experience</span></span>

<span data-ttu-id="bffad-123">Puede especificar la experiencia del cliente que verán los usuarios de su organización mediante el cmdlet **set-ClientPolicy** con el parámetro EnableSkypeUI.</span><span class="sxs-lookup"><span data-stu-id="bffad-123">You can specify the client experience the users in your organization will see by using the **Set-CSClientPolicy** cmdlet with the EnableSkypeUI parameter.</span></span> <span data-ttu-id="bffad-124">El siguiente comando selecciona la experiencia del cliente de Skype empresarial para todos los usuarios de su organización afectados por la directiva global (Recuerde que las directivas específicas del sitio o del usuario invalidan la directiva global):</span><span class="sxs-lookup"><span data-stu-id="bffad-124">The following command selects the Skype for Business client experience for all users in your organization affected by the Global policy (remember, site or user-specific policies override the Global policy):</span></span>

    Set-CsClientPolicy -Identity Global -EnableSkypeUI $true

<span data-ttu-id="bffad-125">El siguiente comando selecciona la experiencia del cliente de Lync para todos los usuarios de su organización afectados por la directiva global:</span><span class="sxs-lookup"><span data-stu-id="bffad-125">The next command selects the Lync client experience for all users in your organization affected by the Global policy:</span></span>

    Set-CsClientPolicy -Identity Global -EnableSkypeUI $false

<span data-ttu-id="bffad-126">El siguiente comando selecciona la experiencia del cliente de Skype empresarial para todos los usuarios del sitio de Redmond:</span><span class="sxs-lookup"><span data-stu-id="bffad-126">The next command selects the Skype for Business client experience for all users within the Redmond site:</span></span>

    Set-CsClientPolicy -Identity site:Redmond -EnableSkypeUI $true

<span data-ttu-id="bffad-127">Si desea configurar la experiencia de cliente para usuarios específicos de su organización, puede crear una nueva Directiva de usuario con el cmdlet **New-ClientPolicy** y, después, asignar la Directiva a usuarios específicos mediante el cmdlet **Grant-ClientPolicy** .</span><span class="sxs-lookup"><span data-stu-id="bffad-127">If you want to configure the client experience for specific users within your organization, you can create a new user policy by using the **New-CsClientPolicy** cmdlet, and then assign the policy to specific users by using the **Grant-CsClientPolicy** cmdlet.</span></span>

<span data-ttu-id="bffad-128">Por ejemplo, el siguiente comando crea una nueva Directiva de cliente, SalesClientUI, que selecciona la experiencia de cliente de Skype empresarial:</span><span class="sxs-lookup"><span data-stu-id="bffad-128">For example, the following command creates a new client policy, SalesClientUI, that selects the Skype for Business client experience:</span></span>

    New-CsClientPolicy -Identity SalesClientUI -EnableSkypeUI $true

<span data-ttu-id="bffad-129">El siguiente comando asigna la directiva SalesClientUI a todos los miembros del departamento de Ventas:</span><span class="sxs-lookup"><span data-stu-id="bffad-129">The next command assigns the policy, SalesClientUI, to all members of the Sales department:</span></span>

    Get-CsUser -LDAPFilter "Department=Sales" | Grant-CsClientPolicy -PolicyName SalesClientUI

</div>

<div>

## <a name="first-launch-client-behaviors"></a><span data-ttu-id="bffad-130">Comportamientos del cliente en el primer inicio</span><span class="sxs-lookup"><span data-stu-id="bffad-130">First launch client behaviors</span></span>

<span data-ttu-id="bffad-131">De forma predeterminada, cuando los usuarios inician Skype empresarial por primera vez, siempre verán la interfaz de usuario de Skype empresarial, aunque haya seleccionado la experiencia del cliente de Lync al establecer el valor del parámetro EnableSkypeUI en $False tal como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="bffad-131">By default, when users launch Skype for Business for the first time, they will always see the Skype for Business user interface--even if you have selected the Lync client experience by setting the value of the EnableSkypeUI parameter to $False as described previously.</span></span> <span data-ttu-id="bffad-132">Después de varios minutos, se les solicitará a los usuarios que cambien al modo Lync.</span><span class="sxs-lookup"><span data-stu-id="bffad-132">After several minutes, users will then be asked to switch to Lync mode.</span></span>

<span data-ttu-id="bffad-133">Si desea mostrar la interfaz de usuario de Lync cuando los usuarios inician el cliente Skype Empresarial por primera vez, siga estos pasos antes de que el cliente se inicie por primera vez después de la actualización:</span><span class="sxs-lookup"><span data-stu-id="bffad-133">If you want to display the Lync user interface when users launch the Skype for Business client for the first time, follow these steps before the client is started for the first time after being updated:</span></span>

1.  <span data-ttu-id="bffad-134">Confirme que el valor de `EnableSkypeUI` se establece en $false de la Directiva que está usando como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="bffad-134">Confirm that the value of `EnableSkypeUI` is set to $False in the policy you are using as described previously.</span></span>

2.  <span data-ttu-id="bffad-p108">Actualice el registro del sistema en el equipo del usuario. Hágalo una sola vez antes de que los usuarios inicien el cliente Skype Empresarial por primera vez. Para obtener información sobre cómo crear un objeto de directiva de grupo para actualizar el registro en un equipo unido a un dominio, consulte la sección correspondiente en este mismo tema.</span><span class="sxs-lookup"><span data-stu-id="bffad-p108">Update the system registry on the user's computer. You should do this before the first time users launch the Skype for Business client, and you should do this only once. For information about how to create a Group Policy Object to update the registry on a domain joined computer, see the section later in the topic.</span></span>
    
    <span data-ttu-id="bffad-138">En la clave del **\[ \_ software HKEY current \_ User \\ software de \\ Microsoft \\ Office \\ Lync \]** , cree un nuevo valor **binario** .</span><span class="sxs-lookup"><span data-stu-id="bffad-138">In the **\[HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\Lync\]** key, create a new **Binary** value.</span></span>
    
    <span data-ttu-id="bffad-139">El **Nombre del valor** debe ser **EnableSkypeUI** y los **Datos del valor** deben configurarse como **00 00 00 00**.</span><span class="sxs-lookup"><span data-stu-id="bffad-139">The **Value name** must be **EnableSkypeUI**, and the **Value data** must be set to **00 00 00 00**.</span></span>
    
    <span data-ttu-id="bffad-140">La clave debería ser similar a esta:</span><span class="sxs-lookup"><span data-stu-id="bffad-140">The key should look like the following:</span></span>
    
        [HKEY_CURRENT_USER\Software\Microsoft\Office\Lync]
        "CanSharePptInCollab"=dword:00000001
        "CanShareOneNoteInCollab"=dword:00000001
        "CanAppShareInCollab"=dword:00000001
        "EnableSkypeUI"=hex:00,00,00,00

<span data-ttu-id="bffad-141">La interfaz de usuario de Lync se mostrará ahora cuando los usuarios inicien el cliente Skype Empresarial por primera vez.</span><span class="sxs-lookup"><span data-stu-id="bffad-141">The Lync user interface will now be displayed when users launch the Skype for Business client for the first time.</span></span>

<div>

## <a name="control-the-display-of-the-welcome-screen-tutorial"></a><span data-ttu-id="bffad-142">Tutorial sobre controlar cómo se muestra la pantalla de bienvenida</span><span class="sxs-lookup"><span data-stu-id="bffad-142">Control the display of the Welcome screen tutorial</span></span>

<span data-ttu-id="bffad-143">Cuando los usuarios abren el cliente de Skype empresarial, el comportamiento predeterminado es mostrar una pantalla de bienvenida que incluye *7 consejos rápidos que la mayoría de las personas solicitan*.</span><span class="sxs-lookup"><span data-stu-id="bffad-143">When users open the Skype for Business client, the default behavior is to display a Welcome screen that includes *7 Quick tips most people ask for*.</span></span> <span data-ttu-id="bffad-144">Puede desactivar la visualización de la pantalla de inicio de sesión, pero puede permitir que los usuarios sigan teniendo acceso al tutorial agregando el siguiente valor de registro en el equipo del cliente:</span><span class="sxs-lookup"><span data-stu-id="bffad-144">You can turn off the display of the Welcome screen but still allow users to access the tutorial by adding the following Registry value on the client computer:</span></span>

<span data-ttu-id="bffad-145">En la clave del **\[ \_ software HKEY current \_ User \\ software de \\ Microsoft \\ Office \\ 15,0 \\ Lync \]** , cree un nuevo valor de **DWORD (32 bits)**.</span><span class="sxs-lookup"><span data-stu-id="bffad-145">In the **\[HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync\]** key, create a new **DWORD (32-bit) Value**.</span></span> <span data-ttu-id="bffad-146">El **Nombre del valor** debe ser **IsBasicTutorialSeenByUser** y los **Datos del valor** deben configurarse como **1**.</span><span class="sxs-lookup"><span data-stu-id="bffad-146">The **Value name** must be **IsBasicTutorialSeenByUser**, and the **Value data** must be set to **1**.</span></span>

<span data-ttu-id="bffad-147">La clave debería ser similar a esta:</span><span class="sxs-lookup"><span data-stu-id="bffad-147">The key should look like the following:</span></span>

    "IsBasicTutorialSeenByUser"=dword:00000001

</div>

<div>

## <a name="turn-off-the-client-tutorial"></a><span data-ttu-id="bffad-148">Desactivar el tutorial del cliente</span><span class="sxs-lookup"><span data-stu-id="bffad-148">Turn off the client tutorial</span></span>

<span data-ttu-id="bffad-149">Si no desea que los usuarios puedan tener acceso al tutorial, puede desactivar el tutorial del cliente con el siguiente valor de registro:</span><span class="sxs-lookup"><span data-stu-id="bffad-149">If you do not want your users to be able to access the tutorial, you can turn off the client tutorial with the following Registry value:</span></span>

<span data-ttu-id="bffad-150">En la clave del **\[ \_ software HKEY current \_ User \\ software de \\ Microsoft \\ Office \\ 15,0 \\ Lync \]** , cree un nuevo valor de **DWORD (32 bits)**.</span><span class="sxs-lookup"><span data-stu-id="bffad-150">In the **\[HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync\]** key, create a new **DWORD (32-bit) Value**.</span></span> <span data-ttu-id="bffad-151">El **Nombre del valor** debe ser **TutorialFeatureEnabled** y los **Datos del valor** deben configurarse como **0**.</span><span class="sxs-lookup"><span data-stu-id="bffad-151">The **Value name** must be **TutorialFeatureEnabled**, and the **Value data** must be set to **0**.</span></span>

    "TutorialFeatureEnabled"=dword:00000000

<span data-ttu-id="bffad-152">Puede volver a activar el tutorial configurando los **Datos del valor** como **1**.</span><span class="sxs-lookup"><span data-stu-id="bffad-152">You can turn the tutorial back on by setting the **Value data** to **1**.</span></span>

</div>

</div>

<div>

## <a name="default-client-experiences"></a><span data-ttu-id="bffad-153">Experiencias de cliente predeterminadas</span><span class="sxs-lookup"><span data-stu-id="bffad-153">Default client experiences</span></span>

<span data-ttu-id="bffad-154">Si su organización tiene instalados tanto Skype empresarial Server 2015 como Lync Server, la experiencia del cliente será diferente según las versiones del servidor y la configuración de la interfaz de usuario de Skype.</span><span class="sxs-lookup"><span data-stu-id="bffad-154">If your organization has both Skype for Business Server 2015 and Lync Server deployed, the client experience will differ depending on server versions and the Skype UI setting.</span></span> <span data-ttu-id="bffad-155">La tabla siguiente muestra la experiencia de cliente inicial en función de la versión del servidor y la configuración de la interfaz de usuario:</span><span class="sxs-lookup"><span data-stu-id="bffad-155">The following table shows the initial client experience based on server version and the UI setting:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bffad-156">Versión del servidor</span><span class="sxs-lookup"><span data-stu-id="bffad-156">Server version</span></span></p></th>
<th><p><span data-ttu-id="bffad-157">Configuración de EnableSkypeUI</span><span class="sxs-lookup"><span data-stu-id="bffad-157">EnableSkypeUI setting</span></span></p></th>
<th><p><span data-ttu-id="bffad-158">Experiencia del cliente</span><span class="sxs-lookup"><span data-stu-id="bffad-158">Client experience</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bffad-159">Skype Empresarial Server 2015</span><span class="sxs-lookup"><span data-stu-id="bffad-159">Skype for Business Server 2015</span></span></p></td>
<td><p><span data-ttu-id="bffad-160">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="bffad-160">Default</span></span></p></td>
<td><p><span data-ttu-id="bffad-161">Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="bffad-161">Skype for Business</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bffad-162">Skype Empresarial Server 2015</span><span class="sxs-lookup"><span data-stu-id="bffad-162">Skype for Business Server 2015</span></span></p></td>
<td><p><span data-ttu-id="bffad-163">Verdadero</span><span class="sxs-lookup"><span data-stu-id="bffad-163">True</span></span></p></td>
<td><p><span data-ttu-id="bffad-164">Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="bffad-164">Skype for Business</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bffad-165">Skype Empresarial Server 2015</span><span class="sxs-lookup"><span data-stu-id="bffad-165">Skype for Business Server 2015</span></span></p></td>
<td><p><span data-ttu-id="bffad-166">Falso</span><span class="sxs-lookup"><span data-stu-id="bffad-166">False</span></span></p></td>
<td><p><span data-ttu-id="bffad-167">El usuario solicitó cambiar al modo de Lync (el usuario puede cambiar a Skype empresarial más adelante si cambia la configuración de la interfaz de usuario a $true)</span><span class="sxs-lookup"><span data-stu-id="bffad-167">User asked to switch to Lync mode (user can switch to Skype for Business later if you change the UI setting to $true)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bffad-168">Lync Server 2010 o Lync Server 2013 (con las revisiones correctas)</span><span class="sxs-lookup"><span data-stu-id="bffad-168">Lync Server 2010 or Lync Server 2013 (with correct patches)</span></span></p></td>
<td><p><span data-ttu-id="bffad-169">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="bffad-169">Default</span></span></p></td>
<td><p><span data-ttu-id="bffad-170">El usuario solicitó cambiar al modo de Lync (el usuario puede cambiar a Skype empresarial más adelante si cambia la configuración de la interfaz de usuario a $true)</span><span class="sxs-lookup"><span data-stu-id="bffad-170">User asked to switch to Lync mode (user can switch to Skype for Business later if you change the UI setting to $true)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bffad-171">Lync Server 2010 o Lync Server 2013 (con las revisiones correctas)</span><span class="sxs-lookup"><span data-stu-id="bffad-171">Lync Server 2010 or Lync Server 2013 (with correct patches)</span></span></p></td>
<td><p><span data-ttu-id="bffad-172">Verdadero</span><span class="sxs-lookup"><span data-stu-id="bffad-172">True</span></span></p></td>
<td><p><span data-ttu-id="bffad-173">Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="bffad-173">Skype for Business</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bffad-174">Lync Server 2010 o Lync Server 2013 (con las revisiones correctas)</span><span class="sxs-lookup"><span data-stu-id="bffad-174">Lync Server 2010 or Lync Server 2013 (with correct patches)</span></span></p></td>
<td><p><span data-ttu-id="bffad-175">Falso</span><span class="sxs-lookup"><span data-stu-id="bffad-175">False</span></span></p></td>
<td><p><span data-ttu-id="bffad-176">El usuario solicitó cambiar al modo de Lync (el usuario puede cambiar a Skype empresarial más adelante si cambia la configuración de la interfaz de usuario a $true)</span><span class="sxs-lookup"><span data-stu-id="bffad-176">User asked to switch to Lync mode (user can switch to Skype for Business later if you change the UI setting to $true)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bffad-177">Lync Server 2010 o Lync Server 2013 (sin revisiones)</span><span class="sxs-lookup"><span data-stu-id="bffad-177">Lync Server 2010 or Lync Server 2013 (without patches)</span></span></p></td>
<td><p><span data-ttu-id="bffad-178">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="bffad-178">Default</span></span></p></td>
<td><p><span data-ttu-id="bffad-179">El usuario solicitó cambiar a la experiencia del cliente de Lync (el usuario no puede cambiar a Skype empresarial más tarde)</span><span class="sxs-lookup"><span data-stu-id="bffad-179">User asked to switch to Lync client experience (user cannot switch to Skype for Business later)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bffad-180">La siguiente tabla muestra la experiencia del cliente cuando el administrador cambia la configuración inicial para la experiencia de la interfaz de usuario de Skype:</span><span class="sxs-lookup"><span data-stu-id="bffad-180">The next table shows the client experience when the administrator changes the initial setting for the Skype UI experience:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bffad-181">Versión del servidor</span><span class="sxs-lookup"><span data-stu-id="bffad-181">Server version</span></span></p></th>
<th><p><span data-ttu-id="bffad-182">Configuración de la interfaz de usuario de Skype</span><span class="sxs-lookup"><span data-stu-id="bffad-182">Skype UI setting</span></span></p></th>
<th><p><span data-ttu-id="bffad-183">Interfaz de usuario de cliente = Lync</span><span class="sxs-lookup"><span data-stu-id="bffad-183">Client UI = Lync</span></span></p></th>
<th><p><span data-ttu-id="bffad-184">IU del cliente = Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="bffad-184">Client UI = Skype for Business</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bffad-185">Skype Empresarial Server 2015</span><span class="sxs-lookup"><span data-stu-id="bffad-185">Skype for Business Server 2015</span></span></p></td>
<td><p><span data-ttu-id="bffad-186">Verdadero</span><span class="sxs-lookup"><span data-stu-id="bffad-186">True</span></span></p></td>
<td><p><span data-ttu-id="bffad-187">El usuario solicitó cambiar a Skype empresarial</span><span class="sxs-lookup"><span data-stu-id="bffad-187">User asked to switch to Skype for Business</span></span></p></td>
<td><p><span data-ttu-id="bffad-188">Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="bffad-188">Skype for Business</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bffad-189">Skype Empresarial Server 2015</span><span class="sxs-lookup"><span data-stu-id="bffad-189">Skype for Business Server 2015</span></span></p></td>
<td><p><span data-ttu-id="bffad-190">Falso</span><span class="sxs-lookup"><span data-stu-id="bffad-190">False</span></span></p></td>
<td><p><span data-ttu-id="bffad-191">IU de Lync</span><span class="sxs-lookup"><span data-stu-id="bffad-191">Lync UI</span></span></p></td>
<td><p><span data-ttu-id="bffad-192">El usuario solicitó cambiar a la interfaz de usuario de Lync</span><span class="sxs-lookup"><span data-stu-id="bffad-192">User asked to switch to Lync UI</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bffad-193">Lync Server 2010 o Lync Server 2013 (con las revisiones correctas)</span><span class="sxs-lookup"><span data-stu-id="bffad-193">Lync Server 2010 or Lync Server 2013 (with correct patches)</span></span></p></td>
<td><p><span data-ttu-id="bffad-194">Verdadero</span><span class="sxs-lookup"><span data-stu-id="bffad-194">True</span></span></p></td>
<td><p><span data-ttu-id="bffad-195">El usuario solicitó cambiar a Skype empresarial</span><span class="sxs-lookup"><span data-stu-id="bffad-195">User asked to switch to Skype for Business</span></span></p></td>
<td><p><span data-ttu-id="bffad-196">Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="bffad-196">Skype for Business</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bffad-197">Lync Server 2010 o Lync Server 2013 (con las revisiones correctas)</span><span class="sxs-lookup"><span data-stu-id="bffad-197">Lync Server 2010 or Lync Server 2013 (with correct patches)</span></span></p></td>
<td><p><span data-ttu-id="bffad-198">Falso</span><span class="sxs-lookup"><span data-stu-id="bffad-198">False</span></span></p></td>
<td><p><span data-ttu-id="bffad-199">IU de Lync</span><span class="sxs-lookup"><span data-stu-id="bffad-199">Lync UI</span></span></p></td>
<td><p><span data-ttu-id="bffad-200">El usuario solicitó cambiar a la interfaz de usuario de Lync</span><span class="sxs-lookup"><span data-stu-id="bffad-200">User asked to switch to Lync UI</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bffad-201">Lync Server 2010 o Lync Server 2013 (sin revisiones)</span><span class="sxs-lookup"><span data-stu-id="bffad-201">Lync Server 2010 or Lync Server 2013 (without patches)</span></span></p></td>
<td><p><span data-ttu-id="bffad-202">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="bffad-202">Default</span></span></p></td>
<td><p><span data-ttu-id="bffad-203">Modo de Lync (no se puede cambiar a Skype empresarial)</span><span class="sxs-lookup"><span data-stu-id="bffad-203">Lync mode (cannot switch to Skype for Business)</span></span></p></td>
<td><p><span data-ttu-id="bffad-204">Interfaz de usuario de Lync (no se puede cambiar a Skype empresarial)</span><span class="sxs-lookup"><span data-stu-id="bffad-204">Lync UI (cannot switch to Skype for Business)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bffad-205">Las versiones de parche necesarias para administrar la configuración del cliente de Skype empresarial son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="bffad-205">The patch versions required to manage the configuration of the Skype for Business client are:</span></span>

  - <span data-ttu-id="bffad-206">Lync Server 2010: actualización acumulativa de febrero de 2015 (4.0.7577.710) para Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="bffad-206">Lync Server 2010 - February 2015 Cumulative Update (4.0.7577.710) for Lync Server 2010.</span></span> <span data-ttu-id="bffad-207">Para obtener más información, consulte [actualizaciones para Lync Server 2010](https://go.microsoft.com/fwlink/p/?linkid=532771)</span><span class="sxs-lookup"><span data-stu-id="bffad-207">For information, see [Updates for Lync Server 2010](https://go.microsoft.com/fwlink/p/?linkid=532771)</span></span>

  - <span data-ttu-id="bffad-208">Lync Server 2013-diciembre 2014 actualización acumulativa (5.0.8308.857) para Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bffad-208">Lync Server 2013 - December 2014 Cumulative Update (5.0.8308.857) for Lync Server 2013.</span></span> <span data-ttu-id="bffad-209">Para obtener más información, consulte [actualizaciones para Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=532772).</span><span class="sxs-lookup"><span data-stu-id="bffad-209">For information, see [Updates for Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=532772).</span></span>

</div>

<div>

## <a name="create-a-group-policy-object-to-modify-the-registry-on-a-domain-joined-computer"></a><span data-ttu-id="bffad-210">Crear un objeto de directiva de grupo para modificar el registro en un equipo unido a un dominio</span><span class="sxs-lookup"><span data-stu-id="bffad-210">Create a Group Policy Object to modify the registry on a domain joined computer</span></span>

<span data-ttu-id="bffad-p115">La actualización del registro para visualizar la experiencia de cliente Lync la primera vez que el usuario inicia el cliente Skype Empresarial debe realizarse solo una vez. Si utiliza un objeto de directiva de grupo (GPO) para actualizar el registro, es necesario que defina el objeto para crear un nuevo valor en lugar de actualizar los datos de valor. Cuando se aplica el GPO, si el nuevo valor no existe, el GPO lo creará y establecerá los datos del valor en 0.</span><span class="sxs-lookup"><span data-stu-id="bffad-p115">The registry update to display the Lync client experience the first time a user launches the Skype for Business client should be done only once. If you use a Group Policy Object (GPO) to update the registry, you need to define the object to create a new value rather than update the Value data. When the GPO is applied, if the new value does not exist, the GPO will create it and set the Value data to 0.</span></span>

<span data-ttu-id="bffad-p116">El procedimiento siguiente describe cómo modificar el registro de manera que la experiencia de cliente Lync se muestre la primera vez que el usuario inicie Skype Empresarial. También puede utilizar este procedimiento para actualizar el registro para desactivar el tutorial de la pantalla de inicio de sesión como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="bffad-p116">The following procedure describes how to modify the registry so that the Lync client experience is displayed the first time a user launches the Skype for Business. You can also use this procedure to update the registry to disable the Welcome screen tutorial as described earlier.</span></span>

<span data-ttu-id="bffad-216">**Para crear el GPO**</span><span class="sxs-lookup"><span data-stu-id="bffad-216">**To create the GPO**</span></span>

1.  <span data-ttu-id="bffad-217">Inicie la **Consola de administración de directivas de grupo**.</span><span class="sxs-lookup"><span data-stu-id="bffad-217">Start the **Group Policy Management console**.</span></span>
    
    <span data-ttu-id="bffad-218">Para obtener información acerca de cómo usar la consola de administración de directivas de grupo, consulte [Consola de administración de directivas de grupo](https://go.microsoft.com/fwlink/?linkid=532759).</span><span class="sxs-lookup"><span data-stu-id="bffad-218">For information about how to use the Group Policy Management Console, see [Group Policy Management Console](https://go.microsoft.com/fwlink/?linkid=532759).</span></span>

2.  <span data-ttu-id="bffad-219">Haga clic con el botón derecho en el nodo **Objetos de directiva de grupo** y seleccione **Nuevo** en el menú.</span><span class="sxs-lookup"><span data-stu-id="bffad-219">Right-click the **Group Policy Objects** node and select **New** on the menu.</span></span>

3.  <span data-ttu-id="bffad-220">En el diálogo **Nuevo GPO**, escriba un nombre para el GPO, por ejemplo, **MakeLyncDefaultUI** y, luego, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="bffad-220">In the **New GPO** dialog, enter a name for the GPO, for example, **MakeLyncDefaultUI**, and then click **OK**.</span></span>

4.  <span data-ttu-id="bffad-221">Haga clic con el botón secundario en el nuevo GPO que acaba de crear y, luego en el menú, seleccione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="bffad-221">Right-click on the new GPO you just created and then select **Edit** from the menu.</span></span>

5.  <span data-ttu-id="bffad-222">En el **Editor de administración de directivas de grupo**, expanda **Configuración de usuario**, expanda **Preferencias**, expanda **Configuración de Windows** y seleccione el nodo **Registro**.</span><span class="sxs-lookup"><span data-stu-id="bffad-222">In the **Group Policy Management Editor**, expand **User Configuration**, expand **Preferences**, expand **Windows Settings**, and then select the **Registry** node.</span></span>

6.  <span data-ttu-id="bffad-223">Haga clic con el botón derecho en el nodo **registro** y, después, seleccione **nuevo** \> **elemento del registro**.</span><span class="sxs-lookup"><span data-stu-id="bffad-223">Right-click on the **Registry** node, and then select **New** \> **Registry Item**.</span></span>

7.  <span data-ttu-id="bffad-224">En el diálogo **Nuevas propiedades de Registro**, actualice lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bffad-224">On the **New Registry Properties** dialog, update the following:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="bffad-225">Campo</span><span class="sxs-lookup"><span data-stu-id="bffad-225">Field</span></span></th>
    <th><span data-ttu-id="bffad-226">Valor para seleccionar o escribir</span><span class="sxs-lookup"><span data-stu-id="bffad-226">Value to select or enter</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="bffad-227"><strong>Acción</strong></span><span class="sxs-lookup"><span data-stu-id="bffad-227"><strong>Action</strong></span></span></p></td>
    <td><p><span data-ttu-id="bffad-228"><strong>Creación</strong></span><span class="sxs-lookup"><span data-stu-id="bffad-228"><strong>Create</strong></span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="bffad-229"><strong>Subárbol</strong></span><span class="sxs-lookup"><span data-stu-id="bffad-229"><strong>Hive</strong></span></span></p></td>
    <td><p><span data-ttu-id="bffad-230">HKEY_CURRENT_USER</span><span class="sxs-lookup"><span data-stu-id="bffad-230">HKEY_CURRENT_USER</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="bffad-231"><strong>Ruta de acceso a la clave</strong></span><span class="sxs-lookup"><span data-stu-id="bffad-231"><strong>Key Path</strong></span></span></p></td>
    <td><p><span data-ttu-id="bffad-232">Software\Microsoft\Office\Lync</span><span class="sxs-lookup"><span data-stu-id="bffad-232">Software\Microsoft\Office\Lync</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="bffad-233"><strong>Nombre del valor</strong></span><span class="sxs-lookup"><span data-stu-id="bffad-233"><strong>Value name</strong></span></span></p></td>
    <td><p><span data-ttu-id="bffad-234">EnableSkypeUI</span><span class="sxs-lookup"><span data-stu-id="bffad-234">EnableSkypeUI</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="bffad-235"><strong>Tipo de valor</strong></span><span class="sxs-lookup"><span data-stu-id="bffad-235"><strong>Value type</strong></span></span></p></td>
    <td><p><span data-ttu-id="bffad-236">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bffad-236">REG_BINARY</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="bffad-237"><strong>Datos del valor</strong></span><span class="sxs-lookup"><span data-stu-id="bffad-237"><strong>Value data</strong></span></span></p></td>
    <td><p><span data-ttu-id="bffad-238">00000000</span><span class="sxs-lookup"><span data-stu-id="bffad-238">00000000</span></span></p></td>
    </tr>
    </tbody>
    </table>


8.  <span data-ttu-id="bffad-239">Haga clic en **Aceptar** para guardar los cambios y cierre el GPO.</span><span class="sxs-lookup"><span data-stu-id="bffad-239">Click **OK** to save your changes, and then close the GPO.</span></span>

<span data-ttu-id="bffad-240">A continuación, tendrá que vincular el GPO que ha creado al grupo de usuarios al que desea asignar la política, como una UO.</span><span class="sxs-lookup"><span data-stu-id="bffad-240">Next, you'll need to link the GPO you created to the group of users that you want to assign the policy to, such as an OU.</span></span>

<span data-ttu-id="bffad-241">**Para usar el GPO para asignar la Directiva**</span><span class="sxs-lookup"><span data-stu-id="bffad-241">**To use the GPO to assign the policy**</span></span>

1.  <span data-ttu-id="bffad-242">En la consola de administración de directivas de grupo, haga clic con el botón derecho en la UO a la que desea asignar la directiva y seleccione **Vincular a un GPO existente**.</span><span class="sxs-lookup"><span data-stu-id="bffad-242">In the Group Policy Management Console, right-click on the OU you want to assign the policy to, and then select **Link to an existing GPO**.</span></span>

2.  <span data-ttu-id="bffad-243">En el diálogo **Seleccionar GPO**, seleccione el GPO que ha creado y seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="bffad-243">On the **Select GPO** dialog, select the GPO you created, and then select **OK**.</span></span>

3.  <span data-ttu-id="bffad-244">En el equipo del usuario de destino, abra un símbolo del sistema y escriba el comando siguiente:</span><span class="sxs-lookup"><span data-stu-id="bffad-244">On the target user's computer, open a command prompt and type the following command:</span></span>
    
    <span data-ttu-id="bffad-245">**gpupdate /target:usuario**</span><span class="sxs-lookup"><span data-stu-id="bffad-245">**gpupdate /target:user**</span></span>
    
    <span data-ttu-id="bffad-p117">El mensaje "Actualizando directiva..." se muestra mientras se aplica el GPO. Cuando se ha completado, aparece el mensaje "La actualización de la directiva de usuario ha concluido satisfactoriamente".</span><span class="sxs-lookup"><span data-stu-id="bffad-p117">The message "Updating policy..." is displayed while the GPO is applied. When it is completed, the message "User Policy update has completed successfully" is displayed.</span></span>

4.  <span data-ttu-id="bffad-248">En el símbolo del sistema, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="bffad-248">At the command prompt, type the following command:</span></span>
    
    <span data-ttu-id="bffad-249">**gpresult /r**</span><span class="sxs-lookup"><span data-stu-id="bffad-249">**gpresult /r**</span></span>
    
    <span data-ttu-id="bffad-250">Debería ver "Objetos de directiva de grupo asignados" con el nombre del GPO que creó mostrado a continuación.</span><span class="sxs-lookup"><span data-stu-id="bffad-250">You should see "Assigned Group Policy Objects" with the name of the GPO you created displayed below.</span></span>

<span data-ttu-id="bffad-251">También puede comprobar que el GPO ha actualizado correctamente el registro en el equipo del usuario al examinar el registro.</span><span class="sxs-lookup"><span data-stu-id="bffad-251">You can also verify that the GPO has successfully updated the registry on a user's computer by examining the registry.</span></span> <span data-ttu-id="bffad-252">Abra el editor del registro y vaya a la clave del **\[ \_ software HKEY current \_ User de \\ \\ Microsoft \\ Office \\ Lync \]** .</span><span class="sxs-lookup"><span data-stu-id="bffad-252">Open Registry Editor and navigate to the **\[HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\Lync\]** key.</span></span> <span data-ttu-id="bffad-253">Si el GPO ha actualizado correctamente el registro, verá un valor denominado EnableSkypeUI con un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="bffad-253">If the GPO successfully updated the registry you will see a value named EnableSkypeUI with a value of 0.</span></span>

<span data-ttu-id="bffad-254"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bffad-254"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

