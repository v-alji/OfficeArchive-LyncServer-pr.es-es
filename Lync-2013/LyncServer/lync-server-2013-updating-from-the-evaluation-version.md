---
title: 'Lync Server 2013: actualización desde la versión de evaluación'
description: 'Lync Server 2013: actualización desde la versión de evaluación.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Updating from the evaluation version of Lync Server 2013
ms:assetid: 62a88180-4289-4a2a-9cb9-1b9899344a63
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521005(v=OCS.15)
ms:contentKeyID: 48184294
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 340badf9f5d2506c50cf8c03faa82223eabbd5af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399474"
---
# <a name="updating-from-the-evaluation-version-of-lync-server-2013"></a><span data-ttu-id="8c4f2-103">Actualización de la versión de evaluación de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c4f2-103">Updating from the evaluation version of Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c4f2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c4f2-104">

<span> </span></span></span>

<span data-ttu-id="8c4f2-105">_**Última modificación del tema:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="8c4f2-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="8c4f2-106">Si ha instalado la versión de evaluación de Microsoft Lync Server 2013, tendrá que actualizar esa instalación en una copia con licencia del software; Esto se debe a que la versión de evaluación vence el 180 días después de su instalación.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-106">If you have installed the Evaluation version of Microsoft Lync Server 2013, you will eventually need to update that installation a licensed copy of the software; that's because the evaluation version expires 180 days after it was installed.</span></span> <span data-ttu-id="8c4f2-107">Sin embargo, no tendrá que desinstalar completamente la versión de evaluación y, a continuación, instalar la versión con licencia.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-107">However, you will not need to completely uninstall the evaluation version and then install the licensed version.</span></span> <span data-ttu-id="8c4f2-108">En su lugar, después de haber obtenido una clave de licencia válida, puede actualizar la versión de evaluación de Lync Server 2013 llevando a cabo el siguiente procedimiento en cada equipo que actúe como servidor perimetral, director o servidor de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-108">Instead, after you have obtained a valid licensing key, you can update the evaluation version of Lync Server 2013 by carrying out the following procedure on each computer acting as a Lync Server Front End Server, Director, or Edge Server.</span></span> <span data-ttu-id="8c4f2-109">Tenga en cuenta que no es necesario actualizar equipos que lleven a cabo otras funciones de servidor, como un servidor de supervisión o un servidor de archivado.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-109">Note that you do not have to update computers carrying out other server roles, such as a Monitoring Server or Archiving Server.</span></span>

<div>

## <a name="updating-from-the-evaluation-version-of-microsoft-lync-server-2013"></a><span data-ttu-id="8c4f2-110">Actualización desde la versión de evaluación de Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c4f2-110">Updating from the Evaluation Version of Microsoft Lync Server 2013</span></span>

<span data-ttu-id="8c4f2-111">Para actualizar un equipo desde la versión de evaluación de Lync Server 2013 a la versión con licencia del software:</span><span class="sxs-lookup"><span data-stu-id="8c4f2-111">To update a computer from the evaluation version of Lync Server 2013 to the licensed version of the software:</span></span>

<span data-ttu-id="8c4f2-112">**Actualización desde la versión de evaluación de Microsoft Lync Server 2013**</span><span class="sxs-lookup"><span data-stu-id="8c4f2-112">**Updating from the Evaluation Version of Microsoft Lync Server 2013**</span></span>

1.  <span data-ttu-id="8c4f2-113">Inicie sesión en el equipo como administrador local.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-113">Log on to the computer as a local administrator.</span></span>

2.  <span data-ttu-id="8c4f2-114">Haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-114">Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="8c4f2-115">En el shell de administración de Lync Server, escriba el siguiente comando y, a continuación, presione ENTRAR:</span><span class="sxs-lookup"><span data-stu-id="8c4f2-115">In the Lync Server Management Shell, type the following command and then press ENTER:</span></span>
    
        msiexec.exe /fvomus server.msi EVALTOFULL=1 /qb
    
    <span data-ttu-id="8c4f2-116">Tenga en cuenta que es posible que tenga que especificar la ruta de acceso completa del archivo server.msi.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-116">Note that you might need to specify the full path to the file server.msi.</span></span> <span data-ttu-id="8c4f2-117">Este archivo puede encontrarse en la carpeta Setup de los archivos de instalación de medios de volumen de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-117">This file can be found in the Setup folder of the Lync Server Volume media installation files.</span></span>

4.  <span data-ttu-id="8c4f2-118">Cuando finalice la instalación, escriba lo siguiente en el símbolo del sistema y, a continuación, presione ENTRAR:</span><span class="sxs-lookup"><span data-stu-id="8c4f2-118">After Setup finishes running, type the following from the command prompt and then press ENTER:</span></span>
    
        Enable-CsComputer

5.  <span data-ttu-id="8c4f2-119">Repita este procedimiento en cualquier otro servidor front-end, director o servidor perimetral que ejecute una copia de evaluación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-119">Repeat this procedure on any other Front End Server, Director, or Edge Server running an evaluation copy of Lync Server.</span></span> <span data-ttu-id="8c4f2-120">Este procedimiento también se debe realizar en los servidores de sucursal que se hayan implementado con los archivos de instalación de Lync Server media.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-120">This procedure should also be performed on any Branch Office Servers that were deployed by using the Lync Server media installation files.</span></span>

<span data-ttu-id="8c4f2-121">Si no está seguro de si la versión de evaluación de Lync Server se está ejecutando en un equipo determinado, puede comprobar si ejecuta el siguiente comando desde el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="8c4f2-121">If you are not sure if the evaluation version of Lync Server is running on a given computer you can verify that by running the following command from within the Lync Server Management Shell:</span></span>

    Get-CsServerVersion

<span data-ttu-id="8c4f2-122">El cmdlet [Get-CsServerVersion](https://docs.microsoft.com/powershell/module/skype/Get-CsServerVersion) analizará el equipo local y devolverá una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="8c4f2-122">The [Get-CsServerVersion](https://docs.microsoft.com/powershell/module/skype/Get-CsServerVersion) cmdlet will analyze the local computer and report back one of the following:</span></span>

  - <span data-ttu-id="8c4f2-123">La clave de licencia por volumen de Lync Server se ha instalado en el equipo, lo que significa que no es necesaria ninguna actualización.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-123">That the Lync Server volume license key has been installed on the computer, meaning that no updating is necessary.</span></span>

  - <span data-ttu-id="8c4f2-124">La clave de licencia de evaluación de Lync Server se ha instalado, lo que significa que debe actualizarse el equipo.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-124">That the Lync Server evaluation license key has been installed, meaning that the computer must be updated.</span></span>

  - <span data-ttu-id="8c4f2-125">Que no se requiere ninguna clave de licencia por volumen en el equipo.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-125">That no volume license key is required on the computer.</span></span> <span data-ttu-id="8c4f2-126">La actualización de la versión de evaluación a la versión con licencia solo es necesaria en servidores front-end, directores y servidores perimetrales.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-126">Updating from the evaluation version to the licensed version is only required on Front End Servers, Directors, and Edge Servers.</span></span>

<span data-ttu-id="8c4f2-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c4f2-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

