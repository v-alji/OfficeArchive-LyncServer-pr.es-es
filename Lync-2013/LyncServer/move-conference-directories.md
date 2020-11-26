---
title: Mover directorios de conferencia
description: Mueva los directorios de las conferencias.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move conference directories
ms:assetid: 71a28308-1f3b-4717-b535-2f4bfe3499a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204994(v=OCS.15)
ms:contentKeyID: 48184463
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a91c30c0bedc84c684a096f5ea482fa911dc798
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438547"
---
# <a name="move-conference-directories"></a><span data-ttu-id="12248-103">Mover directorios de conferencia</span><span class="sxs-lookup"><span data-stu-id="12248-103">Move conference directories</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="12248-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="12248-104">

<span> </span></span></span>

<span data-ttu-id="12248-105">_**Última modificación del tema:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="12248-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="12248-106">Antes de dar de baja un grupo, debe realizar el siguiente procedimiento para cada directorio de conferencia del grupo de Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="12248-106">Before decommissioning a pool, you need to perform the following procedure for each conference directory in your Office Communications Server 2007 R2 pool.</span></span>

<div>

## <a name="to-move-a-conference-directory-to-lync-server-2013"></a><span data-ttu-id="12248-107">Para mover un directorio de conferencia a Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="12248-107">To move a conference directory to Lync Server 2013</span></span>

1.  <span data-ttu-id="12248-108">Abra el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="12248-108">Open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="12248-109">Para obtener la identidad de los directorios de conferencia de su organización, ejecute los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="12248-109">To obtain the identity of the conference directories in your organization, run the following commands:</span></span>
    
        Get-CsConferenceDirectory
    
    <span data-ttu-id="12248-110">Dado que este cmdlet devuelve todos los directorios de conferencia de su organización, es posible que desee limitar los resultados solo a la agrupación que desea retirar.</span><span class="sxs-lookup"><span data-stu-id="12248-110">Because this cmdlet returns all the conference directories in your organization, you may want to limit the results to only the pool you want to decommission.</span></span> <span data-ttu-id="12248-111">Por ejemplo, si desea retirar un grupo con el nombre de dominio completo (FQDN) pool01.contoso.net:</span><span class="sxs-lookup"><span data-stu-id="12248-111">For example, if you want to decommission a pool with the fully qualified domain name (FQDN) pool01.contoso.net:</span></span>
    
        Get-CsConferenceDirectory | Where-Object {$_.ServiceID -match "pool01.contoso.net"}
    
    <span data-ttu-id="12248-112">Este cmdlet devuelve todos los directorios de conferencia en los que el identificador de servicio contiene el FQDN pool01.contoso.net.</span><span class="sxs-lookup"><span data-stu-id="12248-112">This cmdlet returns all the conference directories where service ID contains the FQDN pool01.contoso.net.</span></span>

3.  <span data-ttu-id="12248-113">Para mover los directorios de una conferencia, ejecute lo siguiente para cada directorio de conferencia del Grupo:</span><span class="sxs-lookup"><span data-stu-id="12248-113">To move conference directories, run the following for each conference directory in the pool:</span></span>
    
        Move-CsConferenceDirectory -Identity <Numeric identity of conference directory> -TargetPool <FQDN of pool where ownership is to be transitioned>
    
    <span data-ttu-id="12248-114">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="12248-114">For example:</span></span>
    
        Move-CsConferenceDirectory -Identity 3 -TargetPool pool02.contoso.net

<div>


> [!NOTE]  
> <span data-ttu-id="12248-115">Puede experimentar un error, que se muestra a continuación, provocado por el shell de administración de Lync Server que requiere un conjunto actualizado de permisos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="12248-115">You may experience an error, shown below, that is caused by the Lync Server Management Shell requiring an updated set of permissions from Active Directory.</span></span> <span data-ttu-id="12248-116">Para resolver el error, cierre la ventana actual y abra un nuevo shell de administración de Lync Server y vuelva a ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="12248-116">To resolve the error, closed the current window and open a new Lync Server Management Shell and run the command again.</span></span>



</div>

<span data-ttu-id="12248-117">![Salida de error de movimiento-CsConferenceDirectory](images/JJ204994.4748b9e8-9651-4527-afe1-cbdc6d5ce4a8(OCS.15).jpg "Salida de error de Move-CsConferenceDirectory")</span><span class="sxs-lookup"><span data-stu-id="12248-117">![Move-CsConferenceDirectory error output](images/JJ204994.4748b9e8-9651-4527-afe1-cbdc6d5ce4a8(OCS.15).jpg "Move-CsConferenceDirectory error output")</span></span>

<span data-ttu-id="12248-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="12248-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

