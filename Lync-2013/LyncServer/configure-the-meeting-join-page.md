---
title: Configurar la página para unirse a la reunión
description: Configurar la página de la combinación de reuniones.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure the meeting join page
ms:assetid: 036c9d03-ad95-4d63-a3d8-6cae1a8ad530
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204635(v=OCS.15)
ms:contentKeyID: 48183260
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af49a57a6844c59bf6f6631d996d8efe12152c52
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398862"
---
# <a name="configure-the-meeting-join-page"></a><span data-ttu-id="5accf-103">Configurar la página para unirse a la reunión</span><span class="sxs-lookup"><span data-stu-id="5accf-103">Configure the meeting join page</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5accf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5accf-104">

<span> </span></span></span>

<span data-ttu-id="5accf-105">_**Última modificación del tema:** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="5accf-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="5accf-106">Cuando un usuario hace clic en un vínculo de reunión en una convocatoria de reunión, la página de la reunión detecta si un cliente de Lync 2013 ya está instalado en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="5accf-106">When a user clicks a meeting link in a meeting request, the meeting join page detects whether a Lync 2013 client is already installed on the user’s computer.</span></span> <span data-ttu-id="5accf-107">Si un cliente ya está instalado, ese cliente se abre y se une a la reunión.</span><span class="sxs-lookup"><span data-stu-id="5accf-107">If a client is already installed, that client opens and joins the meeting.</span></span> <span data-ttu-id="5accf-108">Si un cliente no está instalado, de forma predeterminada se abre la versión 2013 de Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="5accf-108">If a client is not installed, by default the 2013 version of Lync Web App opens.</span></span>

<span data-ttu-id="5accf-109">Puede modificar el comportamiento de la página de la combinación de reuniones si desea permitir que los usuarios se unan a reuniones con Office Communicator 2007 R2 o el operador de Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="5accf-109">You can modify the behavior of the meeting join page if you want to allow users to join meetings with Office Communicator 2007 R2 or Lync 2010 Attendant.</span></span> <span data-ttu-id="5accf-110">Estas opciones de configuración se han eliminado del panel de control de Lync Server 2013, pero se configuran mediante el cmdlet CsWebServiceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5accf-110">These configuration options have been removed from the Lync Server 2013 Control Panel, but you configure them by using the CsWebServiceConfiguration cmdlet.</span></span>

### <a name="meeting-join-page-cswebserviceconfiguration-parameters"></a><span data-ttu-id="5accf-111">Página de combinación de reuniones CsWebServiceConfiguration parámetros</span><span class="sxs-lookup"><span data-stu-id="5accf-111">Meeting Join Page CsWebServiceConfiguration Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5accf-112">Parámetro CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5accf-112">CsWebServiceConfiguration Parameter</span></span></th>
<th><span data-ttu-id="5accf-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="5accf-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5accf-114">ShowJoinUsingLegacyClientLink</span><span class="sxs-lookup"><span data-stu-id="5accf-114">ShowJoinUsingLegacyClientLink</span></span></p></td>
<td><p><span data-ttu-id="5accf-115">Si se establece en true, los usuarios que se unan a una reunión mediante una aplicación cliente que no sea Lync tendrán la oportunidad de unirse a la reunión mediante Office Communicator 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="5accf-115">If set to True, users joining a meeting by using a client application other than Lync will be given the opportunity to join the meeting by using Office Communicator 2007 R2.</span></span> <span data-ttu-id="5accf-116">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="5accf-116">The default value is False.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5accf-117">ShowAlternateJoinOptionsExpanded</span><span class="sxs-lookup"><span data-stu-id="5accf-117">ShowAlternateJoinOptionsExpanded</span></span></p></td>
<td><p><span data-ttu-id="5accf-118">Si se establece en true, las opciones alternativas para unirse a una conferencia en línea (como Office Communicator 2007 R2) se expandirán y mostrarán automáticamente a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="5accf-118">When set to True then alternate options for joining an online conference (such as Office Communicator 2007 R2) will automatically be expanded and shown to users.</span></span> <span data-ttu-id="5accf-119">Cuando se establece en false (valor predeterminado), estas opciones estarán disponibles, pero el usuario tendrá que mostrar la lista de opciones por sí mismos.</span><span class="sxs-lookup"><span data-stu-id="5accf-119">When set to False (the default value) these options will be available, but the user will have to display the list of options for themselves.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-the-meeting-join-page-by-using-lync-server-2013-management-shell"></a><span data-ttu-id="5accf-120">Para configurar la página de la combinación de reuniones con el shell de administración de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5accf-120">To configure the meeting join page by using Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="5accf-121">Inicie el shell de administración de Lync Server 2013: haga clic en **Inicio**, haga clic en **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="5accf-121">Start the Lync Server 2013 Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="5accf-122">Ejecute el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5accf-122">Run the following cmdlet:</span></span>
    
        Get-CsWebServiceConfiguration
    
    <span data-ttu-id="5accf-123">Este cmdlet devuelve los parámetros de configuración del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="5accf-123">This cmdlet returns the web service configuration settings.</span></span>

3.  <span data-ttu-id="5accf-124">Ejecute el siguiente comando, con los parámetros establecidos en true o false, en función de su preferencia (para obtener información detallada sobre los parámetros para este cmdlet, consulte la documentación del shell de administración de Lync Server 2013):</span><span class="sxs-lookup"><span data-stu-id="5accf-124">Run the following command, with the parameters set to True or False, depending on your preference (for details about the parameters for this cmdlet, see the Lync Server 2013 Management Shell documentation):</span></span>
    
        Set-CsWebServiceConfiguration -Identity global -ShowJoinUsingLegacyClientLink $True

<span data-ttu-id="5accf-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5accf-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

