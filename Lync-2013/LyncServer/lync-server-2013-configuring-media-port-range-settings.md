---
title: 'Lync Server 2013: configuración de intervalos de puertos de medios'
description: 'Lync Server 2013: configuración de intervalos de puertos de medios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring media port range settings
ms:assetid: 2c4b7c0b-0dce-48f4-a489-336d6e526f7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204770(v=OCS.15)
ms:contentKeyID: 48183723
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a7670284c593197068c366f43bbb3faaaad8f63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432916"
---
# <a name="configuring-media-port-range-settings-in-lync-server-2013"></a><span data-ttu-id="247e7-103">Configuración de la configuración de intervalo de puertos de medios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="247e7-103">Configuring media port range settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="247e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="247e7-104">

<span> </span></span></span>

<span data-ttu-id="247e7-105">_**Última modificación del tema:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="247e7-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="247e7-106">La configuración de intervalo de puertos de medios puede influir significativamente en el rendimiento del cliente y debe configurarse.</span><span class="sxs-lookup"><span data-stu-id="247e7-106">Media port range settings can significantly impact client performance and should be configured.</span></span> <span data-ttu-id="247e7-107">Puede configurar estas opciones con el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="247e7-107">You can configure these settings by using Lync Server Management Shell.</span></span>

### <a name="media-port-range-settings"></a><span data-ttu-id="247e7-108">Configuración de intervalo de puertos de medios</span><span class="sxs-lookup"><span data-stu-id="247e7-108">Media Port Range Settings</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="247e7-109">Setting</span><span class="sxs-lookup"><span data-stu-id="247e7-109">Setting</span></span></th>
<th><span data-ttu-id="247e7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="247e7-110">Description</span></span></th>
<th><span data-ttu-id="247e7-111">Cmdlet del shell de administración de Lync Server</span><span class="sxs-lookup"><span data-stu-id="247e7-111">Lync Server Management Shell cmdlet</span></span></th>
<th><span data-ttu-id="247e7-112">Parámetros del cmdlet</span><span class="sxs-lookup"><span data-stu-id="247e7-112">Cmdlet parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="247e7-113">Portrange\Enabled</span><span class="sxs-lookup"><span data-stu-id="247e7-113">Portrange\Enabled</span></span></p></td>
<td><p><span data-ttu-id="247e7-114">Especifica si el cliente debe usar los intervalos de puertos enviados por el servidor para multimedia y para la señalización.</span><span class="sxs-lookup"><span data-stu-id="247e7-114">Specifies whether the port ranges sent by the server should be used by the client for media and signaling.</span></span> <span data-ttu-id="247e7-115">Se usa junto con los subvalores MinMediaPort y MaxMediaPort.</span><span class="sxs-lookup"><span data-stu-id="247e7-115">Used in conjunction with the subvalues MinMediaPort and MaxMediaPort.</span></span></p></td>
<td><p><span data-ttu-id="247e7-116"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="247e7-116"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="247e7-117">ClientMediaPortRangeEnabled</span><span class="sxs-lookup"><span data-stu-id="247e7-117">ClientMediaPortRangeEnabled</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247e7-118">Portrange\MinMediaPort</span><span class="sxs-lookup"><span data-stu-id="247e7-118">Portrange\MinMediaPort</span></span></p></td>
<td><p><span data-ttu-id="247e7-119">Especifica el número de puerto de inicio que se va a usar para los medios.</span><span class="sxs-lookup"><span data-stu-id="247e7-119">Specifies the starting port number to use for media.</span></span> <span data-ttu-id="247e7-120">Se combina con MaxMediaPort para especificar el rango de puertos.</span><span class="sxs-lookup"><span data-stu-id="247e7-120">Combines with MaxMediaPort to specify the range of ports.</span></span> <span data-ttu-id="247e7-121">El intervalo mínimo recomendado es 40 puertos.</span><span class="sxs-lookup"><span data-stu-id="247e7-121">The recommended minimum range is 40 ports.</span></span></p></td>
<td><p><span data-ttu-id="247e7-122"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="247e7-122"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="247e7-123">ClientMediaPort (representa el número de puerto de inicio para usar en los medios del cliente)</span><span class="sxs-lookup"><span data-stu-id="247e7-123">ClientMediaPort (represents the starting port number to use for client media)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="247e7-124">Portrange\MaxMediaPort</span><span class="sxs-lookup"><span data-stu-id="247e7-124">Portrange\MaxMediaPort</span></span></p></td>
<td><p><span data-ttu-id="247e7-125">Especifica el número de puerto más alto que se debe usar para los medios.</span><span class="sxs-lookup"><span data-stu-id="247e7-125">Specifies the highest port number to use for media.</span></span> <span data-ttu-id="247e7-126">Se combina con MinMediaPort para especificar el rango de puertos.</span><span class="sxs-lookup"><span data-stu-id="247e7-126">Combines with MinMediaPort to specify the range of ports.</span></span> <span data-ttu-id="247e7-127">El intervalo mínimo recomendado es 40 puertos.</span><span class="sxs-lookup"><span data-stu-id="247e7-127">The recommended minimum range is 40 ports.</span></span></p></td>
<td><p><span data-ttu-id="247e7-128"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="247e7-128"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="247e7-129">ClientMediaPortRange (indica el número total de puertos disponibles para los medios de cliente; el valor predeterminado es 40)</span><span class="sxs-lookup"><span data-stu-id="247e7-129">ClientMediaPortRange (indicates the total number of ports available for client media; default is 40)</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-media-port-range-settings"></a><span data-ttu-id="247e7-130">Para configurar las opciones de intervalo de puertos de medios</span><span class="sxs-lookup"><span data-stu-id="247e7-130">To Configure Media Port Range Settings</span></span>

1.  <span data-ttu-id="247e7-131">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="247e7-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="247e7-132">Ejecute el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="247e7-132">Run the following cmdlet:</span></span>
    
        Get-CsConferencingConfiguration
    
    <span data-ttu-id="247e7-133">Este cmdlet devuelve la configuración de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="247e7-133">This cmdlet returns the conferencing configuration settings.</span></span>

3.  <span data-ttu-id="247e7-134">Ejecute el siguiente cmdlet con los parámetros y valores que desea cambiar (para obtener información detallada sobre los parámetros para este cmdlet, consulte la documentación del shell de administración de Lync Server):</span><span class="sxs-lookup"><span data-stu-id="247e7-134">Run the following cmdlet with the parameters and values you want to change (for details about the parameters for this cmdlet, see the Lync Server Management Shell documentation):</span></span>
    
        Set-CsConferencingConfiguration
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="247e7-135">Puede crear más conjuntos de parámetros de configuración de conferencias para sitios específicos.</span><span class="sxs-lookup"><span data-stu-id="247e7-135">You can create additional sets of conferencing configuration settings for specific sites.</span></span> <span data-ttu-id="247e7-136">Use el cmdlet <STRONG>New-CsConferencingConfiguration</STRONG> con una identidad de sitio.</span><span class="sxs-lookup"><span data-stu-id="247e7-136">Use the <STRONG>New- CsConferencingConfiguration</STRONG> cmdlet with a site identity.</span></span> <span data-ttu-id="247e7-137">Al crear nuevas opciones de configuración de conferencias para sitios, la configuración del sitio tiene prioridad sobre la configuración global.</span><span class="sxs-lookup"><span data-stu-id="247e7-137">When you create new conferencing configuration settings for sites, the site settings take precedence over the global settings.</span></span> <span data-ttu-id="247e7-138">Para obtener más información, consulte la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="247e7-138">For details, see the Lync Server Management Shell documentation.</span></span>

    
    <span data-ttu-id="247e7-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="247e7-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

