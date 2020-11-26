---
title: 'Lync Server 2013: configuración de Estados de presencia personalizados'
description: 'Lync Server 2013: configuración de Estados de presencia personalizados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring custom presence states
ms:assetid: e17364a8-8b93-45fc-a614-c80e45435d42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398997(v=OCS.15)
ms:contentKeyID: 48185534
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28b277f096ff17ffa63615468ac9b4f21dead68e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433223"
---
# <a name="configuring-custom-presence-states-in-lync-server-2013"></a><span data-ttu-id="abb0c-103">Configuración de Estados de presencia personalizada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abb0c-103">Configuring custom presence states in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abb0c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abb0c-104">

<span> </span></span></span>

<span data-ttu-id="abb0c-105">_**Última modificación del tema:** 2013-01-10_</span><span class="sxs-lookup"><span data-stu-id="abb0c-105">_**Topic Last Modified:** 2013-01-10_</span></span>

<span data-ttu-id="abb0c-106">Para definir Estados de presencia personalizado en Lync 2013, cree un archivo de configuración de presencia personalizado XML y, a continuación, especifique su ubicación mediante los cmdlets del shell de administración de Lync Server **New-ClientPolicy** o **set-ClientPolicy** con el parámetro CustomStateURL.</span><span class="sxs-lookup"><span data-stu-id="abb0c-106">To define custom presence states in Lync 2013, create an XML custom presence configuration file, and then specify its location by using the Lync Server Management Shell cmdlets **New-CSClientPolicy** or **Set-CSClientPolicy** with the parameter CustomStateURL.</span></span>

<span data-ttu-id="abb0c-107">Los archivos de configuración tienen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="abb0c-107">Configuration files have the following properties:</span></span>

  - <span data-ttu-id="abb0c-108">Los Estados de presencia personalizada se pueden configurar con los indicadores de presencia disponibles, ocupado y no molestar.</span><span class="sxs-lookup"><span data-stu-id="abb0c-108">Custom presence states can be configured with the Available, Busy, and Do Not Disturb presence indicators.</span></span>

  - <span data-ttu-id="abb0c-109">El atributo Availability determina qué indicador de presencia está asociado al texto de estado del estado personalizado.</span><span class="sxs-lookup"><span data-stu-id="abb0c-109">The availability attribute determines which presence indicator is associated with the status text of the custom state.</span></span> <span data-ttu-id="abb0c-110">En el ejemplo que se muestra más adelante en este tema, se muestra el texto de estado trabajo desde casa, a la derecha del indicador de presencia verde (disponible).</span><span class="sxs-lookup"><span data-stu-id="abb0c-110">In the example later in this topic, the status text Working from Home is displayed to the right of the green (Available) presence indicator.</span></span>

  - <span data-ttu-id="abb0c-111">La longitud máxima del texto de estado es de 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="abb0c-111">The maximum length of the status text is 64 characters.</span></span>

  - <span data-ttu-id="abb0c-112">Se pueden agregar un máximo de cuatro Estados de presencia personalizados.</span><span class="sxs-lookup"><span data-stu-id="abb0c-112">A maximum of four custom presence states can be added.</span></span>

  - <span data-ttu-id="abb0c-113">El parámetro CustomStateURL especifica la ubicación del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="abb0c-113">The CustomStateURL parameter specifies the location of the configuration file.</span></span> <span data-ttu-id="abb0c-114">En Lync 2013, el modo de alta seguridad de SIP está habilitado de forma predeterminada, por lo que tendrá que almacenar el archivo de configuración de presencia personalizado en un servidor Web que tenga habilitado HTTPS.</span><span class="sxs-lookup"><span data-stu-id="abb0c-114">In Lync 2013, SIP high security mode is enabled by default, so you will need to store the custom presence configuration file on a web server that has HTTPS enabled.</span></span> <span data-ttu-id="abb0c-115">De lo contrario, los clientes de Lync 2013 no podrán conectarse a él.</span><span class="sxs-lookup"><span data-stu-id="abb0c-115">Otherwise, Lync 2013 clients will be unable to connect to it.</span></span> <span data-ttu-id="abb0c-116">Por ejemplo, una dirección válida sería `https://lspool.corp.contoso.com/ClientConfigFolder/CustomPresence.xml` .</span><span class="sxs-lookup"><span data-stu-id="abb0c-116">For example, a valid address would be `https://lspool.corp.contoso.com/ClientConfigFolder/CustomPresence.xml`.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="abb0c-117">Aunque no se recomienda en un entorno de producción, puede probar un archivo de configuración que se encuentre en un recurso compartido de archivos no HTTPS mediante la configuración del registro EnableSIPHighSecurityMode para deshabilitar el modo de alta seguridad SIP en el cliente.</span><span class="sxs-lookup"><span data-stu-id="abb0c-117">Although it is not recommended in a production environment, you can test a configuration file that is located on a non-HTTPS file share by using the EnableSIPHighSecurityMode registry setting to disable SIP high security mode on the client.</span></span> <span data-ttu-id="abb0c-118">A continuación, puede usar la configuración del registro CustomStateURL para especificar una ubicación que no sea HTTPS para el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="abb0c-118">Then you can use the CustomStateURL registry setting to specify a non-HTTPS location for the configuration file.</span></span> <span data-ttu-id="abb0c-119">Observe que Lync 2013 acepta la configuración del registro de Lync 2010, pero se ha actualizado el subárbol del registro.</span><span class="sxs-lookup"><span data-stu-id="abb0c-119">Note that Lync 2013 honors Lync 2010 registry settings, but the registry hive has been updated.</span></span> <span data-ttu-id="abb0c-120">Crearía la configuración del registro de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="abb0c-120">You would create the registry settings as follows:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="abb0c-121">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync\EnableSIPHighSecurityMode</span><span class="sxs-lookup"><span data-stu-id="abb0c-121">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync\EnableSIPHighSecurityMode</span></span></P>
> <P><span data-ttu-id="abb0c-122">Tipo: DWORD</span><span class="sxs-lookup"><span data-stu-id="abb0c-122">Type: DWORD</span></span></P>
> <P><span data-ttu-id="abb0c-123">Datos del valor: 0</span><span class="sxs-lookup"><span data-stu-id="abb0c-123">Value data: 0</span></span></P>
> <LI>
> <P><span data-ttu-id="abb0c-124">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync\CustomStateURL</span><span class="sxs-lookup"><span data-stu-id="abb0c-124">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync\CustomStateURL</span></span></P>
> <P><span data-ttu-id="abb0c-125">Tipo: String (REG_SZ)</span><span class="sxs-lookup"><span data-stu-id="abb0c-125">Type: String (REG_SZ)</span></span></P>
> <P><span data-ttu-id="abb0c-126">Datos de valor (ejemplos): file:// \\lspool.corp.contoso.com\LSFileShare\ClientConfigFolder\Presence.xml o file:///c:/LSFileShare/ClientConfigFolder/Group_1_Pres.xml</span><span class="sxs-lookup"><span data-stu-id="abb0c-126">Value data (examples): file://\\lspool.corp.contoso.com\LSFileShare\ClientConfigFolder\Presence.xml or file:///c:/LSFileShare/ClientConfigFolder/Group_1_Pres.xml</span></span></P></LI></UL>



</div>

<span data-ttu-id="abb0c-127">Adaptar el estado de presencia personalizado especificando uno o más esquemas de identificador de configuración regional (LCID) en el archivo de configuración XML.</span><span class="sxs-lookup"><span data-stu-id="abb0c-127">Localize your custom presence state by specifying one or more locale ID (LCID) schema in the XML configuration file.</span></span> <span data-ttu-id="abb0c-128">En el ejemplo que aparece más adelante en este tema se muestra la traducción a Inglés-Estados Unidos (1033), Noruego-Bokmål (1044), Francés-Francia (1036) y Turco (1055).</span><span class="sxs-lookup"><span data-stu-id="abb0c-128">The example later in this topic shows localization into English - United States (1033), Norwegian - Bokmål (1044), French - France (1036), and Turkish (1055).</span></span> <span data-ttu-id="abb0c-129">Para obtener una lista de LCID, consulte IDs de configuración regional asignadas por Microsoft en <https://go.microsoft.com/fwlink/p/?linkid=157331> .</span><span class="sxs-lookup"><span data-stu-id="abb0c-129">For a list of LCIDs, see Locale IDs Assigned by Microsoft at <https://go.microsoft.com/fwlink/p/?linkid=157331>.</span></span>

<div>

## <a name="to-add-custom-presence-states-to-lync-2013"></a><span data-ttu-id="abb0c-130">Para agregar Estados de presencia personalizado a Lync 2013</span><span class="sxs-lookup"><span data-stu-id="abb0c-130">To add custom presence states to Lync 2013</span></span>

1.  <span data-ttu-id="abb0c-131">Cree un archivo de configuración XML que use el formato del ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="abb0c-131">Create an XML configuration file that uses the format of the following example:</span></span>
    
        <?xml version="1.0"?>
        <customStates xmlns="http://schemas.microsoft.com/09/2009/communicator/customStates">
          <customState ID="1" availability="online">
            <activity LCID="1033">Working from Home</activity>
            <activity LCID="1044">activity 2 for 1044</activity>
            <activity LCID="1055">activity 3 for 1055</activity>
          </customState>
          <customState ID="2" availability="busy">
            <activity LCID="1033">In a Live Meeting</activity>
            <activity LCID="1036">Equivalent French String for - In a Live Meeting </activity>
          </customState>
          <customState ID="3" availability="busy">
            <activity LCID="1033">Meeting with Customer</activity>
            <activity LCID="1055">meeting with client</activity>
            <activity LCID="1036">Equivalent French String for - Meeting with Customer</activity>
          </customState>
          <customState ID="4" availability="do-not-disturb">
            <activity LCID="1033">Interviewing</activity>
          </customState>
        </customStates>

2.  <span data-ttu-id="abb0c-132">Guarde el archivo de configuración XML en un servidor Web con HTTPS habilitado.</span><span class="sxs-lookup"><span data-stu-id="abb0c-132">Save the XML configuration file to a web server with HTTPS enabled.</span></span> <span data-ttu-id="abb0c-133">En este ejemplo, el archivo se denomina Presence.xml y se guarda en la ubicación https://lspool.corp.contoso.com/ClientConfigFolder/CustomPresence.xml .</span><span class="sxs-lookup"><span data-stu-id="abb0c-133">In this example, the file is named Presence.xml and saved to the location https://lspool.corp.contoso.com/ClientConfigFolder/CustomPresence.xml.</span></span>

3.  <span data-ttu-id="abb0c-134">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="abb0c-134">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="abb0c-135">En el shell de administración de Lync Server, defina la ubicación del archivo de configuración XML con un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="abb0c-135">In the Lync Server Management Shell, define the location of your XML configuration file by using a command similar to the following:</span></span>
    
        New-CsClientPolicy -Identity ContosoCustomStates 
        -CustomStateURL "https://lspool.corp.contoso.com/ClientConfigFolder/CustomPresence.xml"

5.  <span data-ttu-id="abb0c-136">Use el cmdlet **Grant-ClientPolicy** para asignar esta nueva Directiva a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="abb0c-136">Use the **Grant-CSClientPolicy** cmdlet to assign this new policy to users.</span></span>

<span data-ttu-id="abb0c-137">Para obtener más información, vea [New-ClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) y [Grant-ClientPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsClientPolicy) en la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="abb0c-137">For details, see [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) and [Grant-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsClientPolicy) in the Lync Server Management Shell documentation.</span></span>

<div>


> [!NOTE]  
> <UL>
> <LI>
> <P><span data-ttu-id="abb0c-138">De forma predeterminada, Lync Server 2013 &nbsp; actualiza las directivas y la configuración del cliente cada tres horas.</span><span class="sxs-lookup"><span data-stu-id="abb0c-138">By default, Lync Server 2013&nbsp;updates client policies and settings every three hours.</span></span></P>
> <LI>
> <P><span data-ttu-id="abb0c-139">Si desea seguir usando la configuración de la Directiva de grupo de versiones anteriores, como CustomStateURL, Lync 2013 reconocerá la configuración si se encuentra en el subárbol del registro de la nueva Directiva (HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync).</span><span class="sxs-lookup"><span data-stu-id="abb0c-139">If you want to continue using Group Policy settings from previous releases, such as CustomStateURL, Lync 2013 will recognize the settings if they are located in the new policy registry hive (HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Office\15.0\Lync).</span></span> <span data-ttu-id="abb0c-140">Sin embargo, las directivas de cliente basadas en servidor tienen prioridad.</span><span class="sxs-lookup"><span data-stu-id="abb0c-140">However, server-based client policies take precedence.</span></span></P></LI></UL><span data-ttu-id="abb0c-141">



</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abb0c-141">



</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

