---
title: Probar la configuración de la cuenta Kerberos asignada a un sitio
description: Probando la configuración de la cuenta Kerberos asignada a un sitio.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing configuration of the Kerberos account assigned to a site
ms:assetid: a087d77e-c59e-44f5-9caa-ccfd41be7276
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743837(v=OCS.15)
ms:contentKeyID: 63969637
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0eab1618474a19753a4c6064d59aa4f8a856fceb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441070"
---
# <a name="testing-configuration-of-the-kerberos-account-assigned-to-a-site-in-lync-server-2013"></a><span data-ttu-id="46515-103">Prueba de la configuración de la cuenta Kerberos asignada a un sitio en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46515-103">Testing configuration of the Kerberos account assigned to a site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="46515-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="46515-104">

<span> </span></span></span>

<span data-ttu-id="46515-105">_**Última modificación del tema:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="46515-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46515-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="46515-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="46515-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="46515-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46515-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="46515-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="46515-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="46515-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46515-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="46515-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="46515-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="46515-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="46515-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsKerberosAccountAssignment.</span><span class="sxs-lookup"><span data-stu-id="46515-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsKerberosAccountAssignment cmdlet.</span></span> <span data-ttu-id="46515-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="46515-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsKerberosAccountAssignment&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="46515-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="46515-114">Description</span></span>

<span data-ttu-id="46515-115">El cmdlet Test-CsKerberosAccountAssignment le permite comprobar que una cuenta Kerberos está asociada con un sitio determinado, que esta cuenta está configurada correctamente y que la cuenta funciona como se espera.</span><span class="sxs-lookup"><span data-stu-id="46515-115">The Test-CsKerberosAccountAssignment cmdlet enables you to verify that a Kerberos account is associated with a given site, that this account is configured correctly, and that the account is working as expected.</span></span> <span data-ttu-id="46515-116">Las cuentas de Kerberos son cuentas de equipo que pueden servir como entidad principal de autenticación para todos los equipos de un sitio que ejecutan Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="46515-116">Kerberos accounts are computer accounts that can serve as the authentication principal for all the computers in a site that are running Internet Information Server (IIS).</span></span> <span data-ttu-id="46515-117">Debido a que estas cuentas usan el protocolo de autenticación Kerberos, las cuentas se conocen como cuentas Kerberos y el nuevo proceso de autenticación se conoce como autenticación Web Kerberos.</span><span class="sxs-lookup"><span data-stu-id="46515-117">Because these accounts use the Kerberos authentication protocol, the accounts are known as Kerberos accounts, and the new authentication process is known as Kerberos web authentication.</span></span> <span data-ttu-id="46515-118">Esto le permite administrar todos los servidores IIS mediante una sola cuenta.</span><span class="sxs-lookup"><span data-stu-id="46515-118">This enables you to manage all IIS servers by using a single account.</span></span>

<span data-ttu-id="46515-119">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="46515-119">For more information, see the Help documentation for the [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="46515-120">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="46515-120">Running the Test</span></span>

<span data-ttu-id="46515-121">De forma predeterminada, Test-CsKerberosAccountAssignment muestra muy pocos resultados en pantalla.</span><span class="sxs-lookup"><span data-stu-id="46515-121">By default, Test-CsKerberosAccountAssignment displays very little output on-screen.</span></span> <span data-ttu-id="46515-122">En su lugar, la información devuelta por el cmdlet se escribe en un archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="46515-122">Instead, information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="46515-123">Por eso, le recomendamos que incluya el parámetro verbose y el parámetro de informe en cualquier momento que ejecute test-CsKerberosAccountAssignment.</span><span class="sxs-lookup"><span data-stu-id="46515-123">Because of that, we recommend that you include the Verbose parameter and the Report parameter any time that you run Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="46515-124">El parámetro verbose proporcionará una salida ligeramente más detallada en pantalla mientras se ejecuta el cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46515-124">The Verbose parameter will provide slightly more detailed output on-screen while the cmdlet runs.</span></span> <span data-ttu-id="46515-125">El parámetro de informe le permite especificar una ruta de acceso y un nombre de archivo para el archivo HTML generado por test-CsKerberosAccountAssignment.</span><span class="sxs-lookup"><span data-stu-id="46515-125">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="46515-126">Si no incluye el parámetro de informe, el archivo HTML se guardará automáticamente en la carpeta usuarios y recibirá un nombre parecido a este: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span><span class="sxs-lookup"><span data-stu-id="46515-126">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="46515-127">También debe especificar una identidad de sitio al ejecutar test-CsKerberosAccountAssignment.</span><span class="sxs-lookup"><span data-stu-id="46515-127">You must also specify a site Identity when you run Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="46515-128">Las cuentas de Kerberos se asignan en el ámbito del sitio.</span><span class="sxs-lookup"><span data-stu-id="46515-128">Kerberos accounts are assigned at the site scope.</span></span>

<span data-ttu-id="46515-129">El siguiente comando se ejecuta Test-CsKerberosAccountAssignment y guarda el resultado en un archivo denominado C: \\ Logs \\KerberosTest.html:</span><span class="sxs-lookup"><span data-stu-id="46515-129">The following command runs Test-CsKerberosAccountAssignment and saves the output to a file that is named C:\\Logs\\KerberosTest.html:</span></span>

    Test-CsKerberosAccountAssignment -Identity "site:Redmond" -Report "C:\Logs\KerberosTest.html" -Verbose

<span data-ttu-id="46515-130">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="46515-130">For more information, see the Help documentation for the [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="46515-131">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="46515-131">Determining Success or Failure</span></span>

<span data-ttu-id="46515-132">El cmdlet Test-CsKerberosAccountAssignment no devuelve una indicación simple de éxito o error.</span><span class="sxs-lookup"><span data-stu-id="46515-132">The Test-CsKerberosAccountAssignment cmdlet does not return a simple indication of success or failure.</span></span> <span data-ttu-id="46515-133">En su lugar, debe ver el archivo HTML generado usando Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="46515-133">Instead, you must view the generated HTML file by using Internet Explorer.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="46515-134">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="46515-134">Reasons Why the Test Might Have Failed</span></span>

<span data-ttu-id="46515-135">Estas son algunas de las razones comunes por las que Test-CsKerberosAccountAssignment puede dar error:</span><span class="sxs-lookup"><span data-stu-id="46515-135">Here are some common reasons why Test-CsKerberosAccountAssignment might fail:</span></span>

  - <span data-ttu-id="46515-136">Es posible que haya especificado una identidad de sitio incorrecta.</span><span class="sxs-lookup"><span data-stu-id="46515-136">You might have specified an incorrect site Identity.</span></span> <span data-ttu-id="46515-137">Para devolver una lista de identidades de sitio válidas, use este comando:</span><span class="sxs-lookup"><span data-stu-id="46515-137">To return a list of valid site Identity, use this command:</span></span>
    
        Get-CsSite | Select-Identity Identity
    
    <span data-ttu-id="46515-138">Una identidad de sitio suele tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="46515-138">A site Identity typically looks as follows:</span></span>
    
    <span data-ttu-id="46515-139">sitio: Redmond</span><span class="sxs-lookup"><span data-stu-id="46515-139">site:Redmond</span></span>

  - <span data-ttu-id="46515-140">Es posible que el sitio especificado no tenga una cuenta de Kerberos asignada.</span><span class="sxs-lookup"><span data-stu-id="46515-140">The specified site might not have a Kerberos account assigned to it.</span></span> <span data-ttu-id="46515-141">Puede determinar si se asigna o no una cuenta Kerberos a un sitio ejecutando un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="46515-141">You can determine whether or not a Kerberos account is assigned to a site by running a command similar to this:</span></span>
    
        Get-CsKerberosAccountAssignment -Identity "site:Redmond"

  - <span data-ttu-id="46515-142">Es posible que su cuenta de Kerberos tenga una contraseña que no es válida.</span><span class="sxs-lookup"><span data-stu-id="46515-142">Your Kerberos account might have a password that isn't valid.</span></span> <span data-ttu-id="46515-143">Si recibe el siguiente mensaje de error en el informe, es probable que tenga que restablecer la contraseña de la cuenta Kerberos:</span><span class="sxs-lookup"><span data-stu-id="46515-143">If you receive the following error message in report, you'll probably have to reset the Kerberos account password:</span></span>
    
    <span data-ttu-id="46515-144">InvalidKerberosConfiguration: la configuración de Kerberos no es válida.</span><span class="sxs-lookup"><span data-stu-id="46515-144">InvalidKerberosConfiguration: The Kerberos configuration is invalid.</span></span>
    
    <span data-ttu-id="46515-145">InvalidKerberosConfiguration: la configuración de Kerberos en atl-cs001.litwareinc.com no es válida.</span><span class="sxs-lookup"><span data-stu-id="46515-145">InvalidKerberosConfiguration: The Kerberos configuration on atl-cs001.litwareinc.com is invalid.</span></span> <span data-ttu-id="46515-146">La cuenta asignada esperada es litwareinc \\ kerberostest.</span><span class="sxs-lookup"><span data-stu-id="46515-146">The expected assigned account is litwareinc\\kerberostest.</span></span> <span data-ttu-id="46515-147">Asegúrese de que la cuenta no haya expirado y de que la contraseña configurada en el equipo coincida con la contraseña de Active Directory de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="46515-147">Ensure that the account has not expired, and the configured password on the machine matches the Active Directory password of the account.</span></span>
    
    <span data-ttu-id="46515-148">Puede establecer la contraseña con el cmdlet [set-CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="46515-148">You can set the password using the [Set-CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="46515-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="46515-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

