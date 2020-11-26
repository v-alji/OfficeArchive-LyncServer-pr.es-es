---
title: (Recomendado) Crear directorios de conferencia
description: Práctica Crear directorios de conferencia.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: (Recommended) Create Conference Directories
ms:assetid: 787f4c94-1c96-468a-a74d-e06b7bd4b8a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn832056(v=OCS.15)
ms:contentKeyID: 63146389
ms.date: 10/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b14982893fbc14a87818875a787d0f776da84ae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443268"
---
# <a name="recommended-create-conference-directories"></a><span data-ttu-id="03cbd-103">(Recomendado) Crear directorios de conferencia</span><span class="sxs-lookup"><span data-stu-id="03cbd-103">(Recommended) Create Conference Directories</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="03cbd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="03cbd-104">

<span> </span></span></span>

<span data-ttu-id="03cbd-105">_**Última modificación del tema:** 2014-10-03_</span><span class="sxs-lookup"><span data-stu-id="03cbd-105">_**Topic Last Modified:** 2014-10-03_</span></span>

<span data-ttu-id="03cbd-106">Los directorios de conferencia mantienen una asignación entre el identificador de reunión alfanumérico que un participante usa para unirse a una conferencia al usar Lync 2013 y el identificador de conferencia de acceso telefónico local que usa un participante de conferencia de acceso telefónico local para unirse a la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="03cbd-106">Conference directories maintain a mapping between the alphanumeric meeting ID that a participant uses to join a conference when using Lync 2013, and the numeric-only conference ID that a dial-in conferencing participant uses to join the conference.</span></span> <span data-ttu-id="03cbd-107">El formato del identificador de conferencia es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="03cbd-107">The format of the conference ID is as follows:</span></span>

    <housekeeping digit (1 digit)><conference directory (usually 1-2 digits)><conference number (variable number of digits><check digit (1 digit)>

<span data-ttu-id="03cbd-108">Si crea varios directorios de conferencia, se asegurará de que los Id. de conferencia se mantienen cortos hasta que se haya creado un número significativo de conferencias.</span><span class="sxs-lookup"><span data-stu-id="03cbd-108">Creating multiple conference directories will ensure that conference IDs will stay short until a significant amount of conferences have been created.</span></span> <span data-ttu-id="03cbd-109">En una organización con un número establecido de conferencias por usuario, se recomienda crear un directorio de conferencia por cada 999 usuarios en el grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="03cbd-109">In an organization with a typical number of conferences per user, we recommend that you create one conference directory for every 999 users in the pool.</span></span> <span data-ttu-id="03cbd-110">Con esta pauta, los identificadores de conferencia generalmente se mantienen reducidos.</span><span class="sxs-lookup"><span data-stu-id="03cbd-110">Using this guideline the conference IDs can generally be kept small.</span></span> <span data-ttu-id="03cbd-111">Sin embargo, cuando el número de directorios de conferencia (en los grupos) exceda de 9, la longitud del id. de conferencia aumentará para dar soporte a otras conferencias.</span><span class="sxs-lookup"><span data-stu-id="03cbd-111">However, once the number of conference directories (across the pools) exceed 9, the Conference ID length will grow to support additional conferences.</span></span>

<div>

## <a name="creating-a-conference-directory"></a><span data-ttu-id="03cbd-112">Crear un directorio de conferencia</span><span class="sxs-lookup"><span data-stu-id="03cbd-112">Creating a conference directory</span></span>

1.  <span data-ttu-id="03cbd-113">En el shell de administración de Lync Server, escriba el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="03cbd-113">In Lync Server Management Shell, type the following cmdlet:</span></span>
    
        New-CsConferenceDirectory -Identity <XdsGlobalRelativeIdentity> -HomePool <String> [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
    
    <span data-ttu-id="03cbd-114">Por ejemplo, el siguiente ejemplo crea un directorio de conferencia con la identidad 42, hospedada en el grupo atl-cs-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="03cbd-114">For example, the following creates a conference directory with the identity 42, hosted on the pool atl-cs-001.litwareinc.com:</span></span>
    
        New-CsConferenceDirectory -Identity 42 -HomePool "atl-cs-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="03cbd-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="03cbd-115">See Also</span></span>


[<span data-ttu-id="03cbd-116">Requisitos de las conferencias de acceso telefónico local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="03cbd-116">Dial-in conferencing requirements in Lync Server 2013</span></span>](lync-server-2013-dial-in-conferencing-requirements.md)  


[<span data-ttu-id="03cbd-117">New-CsConferenceDirectory</span><span class="sxs-lookup"><span data-stu-id="03cbd-117">New-CsConferenceDirectory</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsConferenceDirectory)  
  

<span data-ttu-id="03cbd-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="03cbd-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

