---
title: 'Lync Server 2013: Quitar la autenticación Kerberos de un sitio'
description: 'Lync Server 2013: quitar la autenticación Kerberos de un sitio.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove Kerberos authentication from a site
ms:assetid: 93171b02-bb36-42dc-943d-86d9dde45b59
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398749(v=OCS.15)
ms:contentKeyID: 48184806
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a3d9100d07d37e98800cfce106bc75fcfaeaa59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436387"
---
# <a name="in-lync-server-2013-remove-kerberos-authentication-from-a-site"></a><span data-ttu-id="719b1-103">Quitar la autenticación Kerberos de un sitio en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="719b1-103">In Lync Server 2013 remove Kerberos authentication from a site</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="719b1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="719b1-104">

<span> </span></span></span>

<span data-ttu-id="719b1-105">_**Última modificación del tema:** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="719b1-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="719b1-106">Para completar correctamente este procedimiento, debe haber iniciado sesión como un usuario que sea miembro del grupo RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="719b1-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="719b1-107">Si necesita quitar la autenticación Kerberos de un sitio o retirar un sitio, debe quitar la asignación de cuenta de autenticación Kerberos del sitio mediante el cmdlet **Remove-CsKerberosAccountAssignment** .</span><span class="sxs-lookup"><span data-stu-id="719b1-107">If you need to remove Kerberos authentication from a site or retire a site, you must remove the Kerberos authentication account assignment from the site by using the **Remove-CsKerberosAccountAssignment** cmdlet.</span></span> <span data-ttu-id="719b1-108">Use el siguiente procedimiento para quitar la asignación de cuenta de autenticación Kerberos, que quita la asignación de todos los equipos del sitio.</span><span class="sxs-lookup"><span data-stu-id="719b1-108">Use the following procedure to remove the Kerberos authentication account assignment, which removes the assignment from all computers in the site.</span></span>

<div class=" ">


> [!WARNING]  
> <span data-ttu-id="719b1-109">Si va a retirar permanentemente la cuenta habilitada para Kerberos, debe usar usuarios y equipos de Active Directory para eliminarla de los servicios de dominio de Active Directory después de quitar la asignación.</span><span class="sxs-lookup"><span data-stu-id="719b1-109">If you are permanently retiring the Kerberos-enabled account, you should use Active Directory Users and Computers to delete it from Active Directory Domain Services after you have removed the assignment.</span></span> <span data-ttu-id="719b1-110">Si tiene previsto usar el objeto en el futuro, es posible que desee mantener el objeto de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="719b1-110">If you plan to use the object in the future, you might want to keep the Active Directory object.</span></span>



</div>

<div>

## <a name="to-remove-kerberos-authentication-from-a-site"></a><span data-ttu-id="719b1-111">Para quitar la autenticación Kerberos de un sitio</span><span class="sxs-lookup"><span data-stu-id="719b1-111">To remove Kerberos authentication from a site</span></span>

1.  <span data-ttu-id="719b1-112">Como miembro del grupo RTCUniversalServerAdmins, inicie sesión en un equipo del dominio que ejecute Lync Server 2013 o en un equipo en el que estén instaladas las herramientas administrativas.</span><span class="sxs-lookup"><span data-stu-id="719b1-112">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="719b1-113">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="719b1-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="719b1-114">En la línea de comandos, ejecute los dos comandos siguientes:</span><span class="sxs-lookup"><span data-stu-id="719b1-114">From the command line, run the following two commands:</span></span>
    
       ```PowerShell
        Remove-CsKerberosAccountAssignment -Identity "site:SiteName"
       ```
    
       ```PowerShell
        Enable-CsTopology
       ```
    
    <span data-ttu-id="719b1-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="719b1-115">For example:</span></span>
    
       ```PowerShell
        Remove-CsKerberosAccountAssignment -Identity "site:Redmond"
       ```
    
       ```PowerShell
        Enable-CsTopology
       ```
    
    <div class=" ">
    

    > [!IMPORTANT]  
    > <span data-ttu-id="719b1-116">Después de realizar cambios en la autenticación Kerberos, como agregar una cuenta o quitar una cuenta, debe ejecutar <STRONG>enable-CsTopology</STRONG> desde el símbolo del sistema del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="719b1-116">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="719b1-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="719b1-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

