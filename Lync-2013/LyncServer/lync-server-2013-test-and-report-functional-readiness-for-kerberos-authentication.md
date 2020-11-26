---
title: Comprobar y crear informes de disponibilidad funcional para la autenticación Kerberos
description: Probar e informar de la preparación funcional de la autenticación Kerberos.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test and report functional readiness for Kerberos authentication
ms:assetid: d52c39e5-747d-4f29-88aa-30fd6f26b99c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398925(v=OCS.15)
ms:contentKeyID: 48185519
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5d32591a8cced7dce2e0bb78cc26189dce1900a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444304"
---
# <a name="test-and-report-functional-readiness-for-kerberos-authentication-in-lync-server-2013"></a><span data-ttu-id="3251e-103">Comprobar y crear informes de disponibilidad funcional para la autenticación Kerberos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3251e-103">Test and report functional readiness for Kerberos authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3251e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3251e-104">

<span> </span></span></span>

<span data-ttu-id="3251e-105">_**Última modificación del tema:** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="3251e-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="3251e-106">Para completar correctamente este procedimiento, debe haber iniciado sesión como un usuario que sea miembro del grupo RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="3251e-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="3251e-107">Puede usar el cmdlet **Test-CsKerberosAccountAssignment** de Windows PowerShell para probar y notificar la preparación funcional de una asignación de sitio para la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="3251e-107">You can use the **Test-CsKerberosAccountAssignment** Windows PowerShell cmdlet to test and report the functional readiness of a site assignment for Kerberos authentication.</span></span> <span data-ttu-id="3251e-108">Este comando consulta el sitio especificado en el parámetro Identity requerido.</span><span class="sxs-lookup"><span data-stu-id="3251e-108">This command queries the site specified in the required Identity parameter.</span></span> <span data-ttu-id="3251e-109">El parámetro de informe opcional hace que el cmdlet escriba un informe HTML en C: \\ logs en el equipo en el que se ejecuta el comando.</span><span class="sxs-lookup"><span data-stu-id="3251e-109">The optional Report parameter causes the cmdlet to write an HTML report to C:\\Logs on the computer on which the command is run.</span></span> <span data-ttu-id="3251e-110">El parámetro detallado opcional informa de la información de actividad en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="3251e-110">The optional Verbose parameter reports activity information to the screen.</span></span>

<div>

## <a name="to-test-and-report-functional-readiness-for-kerberos-authentication-for-a-site"></a><span data-ttu-id="3251e-111">Para probar e informar sobre la preparación funcional de la autenticación Kerberos para un sitio</span><span class="sxs-lookup"><span data-stu-id="3251e-111">To test and report functional readiness for Kerberos authentication for a site</span></span>

1.  <span data-ttu-id="3251e-112">Como miembro del grupo RTCUniversalServerAdmins, inicie sesión en un equipo del dominio que ejecute Lync Server 2013 o en el equipo en el que estén instaladas las herramientas administrativas.</span><span class="sxs-lookup"><span data-stu-id="3251e-112">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to the computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="3251e-113">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="3251e-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="3251e-114">En la línea de comandos, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="3251e-114">From the command line, run the following command:</span></span>
    
        Test-CsKerberosAccountAssignment -Identity "site:SiteName" -Report "c:\logs\FileName.htm" -Verbose
    
    <span data-ttu-id="3251e-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3251e-115">For example:</span></span>
    
        Test-CsKerberosAccountAssignment -Identity "site:Redmond" -Report "c:\logs\KerberosReport.htm" -Verbose

<span data-ttu-id="3251e-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3251e-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

