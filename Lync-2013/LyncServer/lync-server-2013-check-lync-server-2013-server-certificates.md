---
title: 'Lync Server 2013: comprobar certificados de servidor de Lync Server 2013'
description: 'Lync Server 2013: Compruebe los certificados de servidor de Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Check server certificates
ms:assetid: 7b0474e8-0efe-47f0-84eb-a1ba575dabfd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725210(v=OCS.15)
ms:contentKeyID: 63969620
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 641651cb425b4fe8bd820bcebfa277084233bb1d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435022"
---
# <a name="check-lync-server-2013-server-certificates"></a><span data-ttu-id="2b3fa-103">Comprobar certificados de servidor de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b3fa-103">Check Lync Server 2013 server certificates</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b3fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b3fa-104">

<span> </span></span></span>

<span data-ttu-id="2b3fa-105">_**Última modificación del tema:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="2b3fa-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b3fa-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="2b3fa-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="2b3fa-107">Cada mes</span><span class="sxs-lookup"><span data-stu-id="2b3fa-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b3fa-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="2b3fa-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="2b3fa-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b3fa-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b3fa-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="2b3fa-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="2b3fa-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="2b3fa-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Get-CsCertificate.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Get-CsCertificate cmdlet.</span></span> <span data-ttu-id="2b3fa-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="2b3fa-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Get-CsCertificate&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="2b3fa-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b3fa-114">Description</span></span>

<span data-ttu-id="2b3fa-115">El cmdlet Get-CsCertificate le permite recuperar información acerca de cada uno de los certificados de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-115">The Get-CsCertificate cmdlet enables you to retrieve information about each of your Lync Server certificates.</span></span> <span data-ttu-id="2b3fa-116">Esto es especialmente importante porque los certificados tienen una fecha de expiración integrada.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-116">That’s especially important because certificates have a built-in expiration date.</span></span> <span data-ttu-id="2b3fa-117">Por ejemplo, los certificados emitidos de forma privada normalmente vencen después de 12 meses.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-117">For example,, privately-issued certificates typically expire after 12 months.</span></span> <span data-ttu-id="2b3fa-118">Si alguno de los certificados de Lync Server vence, perderá la funcionalidad correspondiente hasta que se renueve o se reemplace el certificado.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-118">If any of your Lync Server certificates expire then you'll lose the accompanying functionality until that certificate is renewed or replaced.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="2b3fa-119">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="2b3fa-119">Running the test</span></span>

<span data-ttu-id="2b3fa-120">Para obtener información sobre cada uno de los certificados de Lync Server, simplemente ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="2b3fa-120">To return information about each of your Lync Server certificates just run the following command:</span></span>

`Get-CsCertificate`

<span data-ttu-id="2b3fa-121">O bien, puede filtrar la información del certificado devuelto según la fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-121">Or, you can filter the return certificate information based on expiration date.</span></span> <span data-ttu-id="2b3fa-122">Por ejemplo, este comando limita los datos devueltos a certificados que vencen (no se pueden usar después) 1 de junio de 2014:</span><span class="sxs-lookup"><span data-stu-id="2b3fa-122">For example, this command limits the returned data to certificates that expire (cannot be used after) June 1, 2014:</span></span>

`Get-CsCertificate | Where-Object {$_.NotAfter -lt "6/1/2014"}`

<span data-ttu-id="2b3fa-123">Para obtener más información, consulte la documentación de ayuda del cmdlet Get-CsCertificate.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-123">For more information, see the Help documentation for the Get-CsCertificate cmdlet.</span></span>

<span data-ttu-id="2b3fa-124">Tenga en cuenta que, aunque exista el cmdlet Test-CsCertificateConfiguration, no es muy útil para los administradores.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-124">Note that, although the Test-CsCertificateConfiguration cmdlet exists, it is not very useful to administrators.</span></span> <span data-ttu-id="2b3fa-125">(En su lugar, el Asistente de certificados usa principalmente ese cmdlet). Aunque el cmdlet funcione, la información que devuelve es de un valor mínimo, tal y como se muestra en el siguiente ejemplo de salida:</span><span class="sxs-lookup"><span data-stu-id="2b3fa-125">(Instead, that cmdlet is primarily used by the Certificate wizard.) Although the cmdlet works, the information that it returns is of minimal value as shown in the following output example:</span></span>

<span data-ttu-id="2b3fa-126">Uso de la huella digital</span><span class="sxs-lookup"><span data-stu-id="2b3fa-126">Thumbprint Use</span></span>

<span data-ttu-id="2b3fa-127">\---------- ---</span><span class="sxs-lookup"><span data-stu-id="2b3fa-127">\---------- ---</span></span>

<span data-ttu-id="2b3fa-128">A9D51A2911C74FABFF7F2A8A994B20857D399107 predeterminado</span><span class="sxs-lookup"><span data-stu-id="2b3fa-128">A9D51A2911C74FABFF7F2A8A994B20857D399107 Default</span></span>

</div>

<div>

## <a name="reviewing-the-output"></a><span data-ttu-id="2b3fa-129">Revisar la salida</span><span class="sxs-lookup"><span data-stu-id="2b3fa-129">Reviewing the output</span></span>

<span data-ttu-id="2b3fa-130">El cmdlet Get-CsCertificate devuelve información similar a la siguiente para cada uno de los certificados de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="2b3fa-130">The Get-CsCertificate cmdlet returns information similar to the following for each of your Lync Server certificates:</span></span>

<span data-ttu-id="2b3fa-131">Emisor: CN = FabrikamCA</span><span class="sxs-lookup"><span data-stu-id="2b3fa-131">Issuer : CN=FabrikamCA</span></span>

<span data-ttu-id="2b3fa-132">Nopérezer: 12/28/2015 3:35:41 PM</span><span class="sxs-lookup"><span data-stu-id="2b3fa-132">NotAfter : 12/28/2015 3:35:41 PM</span></span>

<span data-ttu-id="2b3fa-133">NotBefore: 1/2/2014 12:49:37 PM</span><span class="sxs-lookup"><span data-stu-id="2b3fa-133">NotBefore : 1/2/2014 12:49:37 PM</span></span>

<span data-ttu-id="2b3fa-134">SerialNumber: 611BB01200000000000C</span><span class="sxs-lookup"><span data-stu-id="2b3fa-134">SerialNumber : 611BB01200000000000C</span></span>

<span data-ttu-id="2b3fa-135">Asunto: CN = LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="2b3fa-135">Subject : CN=LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="2b3fa-136">AlternativeNames: {sip.fabrikam.com, LYNC-SE.fabrikam.com,</span><span class="sxs-lookup"><span data-stu-id="2b3fa-136">AlternativeNames : {sip.fabrikam.com, LYNC-SE.fabrikam.com,</span></span>

<span data-ttu-id="2b3fa-137">meet.fabrikam.com, admin.fabrikam.com...}</span><span class="sxs-lookup"><span data-stu-id="2b3fa-137">meet.fabrikam.com, admin.fabrikam.com...}</span></span>

<span data-ttu-id="2b3fa-138">Huella digital: A9D51A2911C74FABFF7F2A8A994B20857D399107</span><span class="sxs-lookup"><span data-stu-id="2b3fa-138">Thumbprint : A9D51A2911C74FABFF7F2A8A994B20857D399107</span></span>

<span data-ttu-id="2b3fa-139">Uso: predeterminado</span><span class="sxs-lookup"><span data-stu-id="2b3fa-139">Use : Default</span></span>

<span data-ttu-id="2b3fa-140">Como regla general, los principales problemas relacionados con los certificados de Lync Server incluyen fechas y horas, como cuando los certificados surten efecto (NotBefore) o cuando vencen (novalente).</span><span class="sxs-lookup"><span data-stu-id="2b3fa-140">As a rule, the top issues involving Lync Server certificates involve dates and times, such as when certificates take effect (NotBefore) or when they expire (NotAfter).</span></span> <span data-ttu-id="2b3fa-141">Como estas fechas y horas son tan importantes, es posible que desee limitar los datos devueltos a información como el uso de certificados, el número de serie del certificado y la fecha de expiración del certificado; después, puede revisar rápidamente todos los certificados y cuándo vencerán.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-141">Because these dates and times are so important, you might want to limit the returned data to information such as the certificate use, the certificate serial number, and the certificate expiration date; then you can quickly review all the certificates and when they will expire.</span></span> <span data-ttu-id="2b3fa-142">Para obtener solo esa información, use el comando junto con las opciones que se muestran:</span><span class="sxs-lookup"><span data-stu-id="2b3fa-142">To return just that information, use the command together with the options as shown:</span></span>

`Get-CsCertificate | Select-Object Use, SerialNumber, NotAfter | Sort-Object NotAfter`

<span data-ttu-id="2b3fa-143">Ese comando devuelve datos similares a los siguientes, con los certificados ordenados por su fecha de expiración:</span><span class="sxs-lookup"><span data-stu-id="2b3fa-143">That command returns data similar to the following, with the certificates sorted in order of their expiration date:</span></span>

<span data-ttu-id="2b3fa-144">Usar SerialNumber alpérezer</span><span class="sxs-lookup"><span data-stu-id="2b3fa-144">Use SerialNumber NotAfter</span></span>

<span data-ttu-id="2b3fa-145">\--- ------------ --------</span><span class="sxs-lookup"><span data-stu-id="2b3fa-145">\--- ------------ --------</span></span>

<span data-ttu-id="2b3fa-146">611BB01200000000000C predeterminados 12/28/2015 3:35:41 P.M.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-146">Default 611BB01200000000000C 12/28/2015 3:35:41 PM</span></span>

<span data-ttu-id="2b3fa-147">WebServicesInteral 32980AA20BBB20000191 02/15/2016 2:16:12 PM</span><span class="sxs-lookup"><span data-stu-id="2b3fa-147">WebServicesInteral 32980AA20BBB20000191 02/15/2016 2:16:12 PM</span></span>

<span data-ttu-id="2b3fa-148">WebServicesExternal 0451B012003872651A0C 02/20/2016 7:11:58 AM</span><span class="sxs-lookup"><span data-stu-id="2b3fa-148">WebServicesExternal 0451B012003872651A0C 02/20/2016 7:11:58 AM</span></span>

<span data-ttu-id="2b3fa-149">Si tiene problemas con el certificado, es posible que desee revisar el AlternativeNames configurado para un certificado.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-149">If you have certificate problems, you might want to review the AlternativeNames configured for a certificate.</span></span> <span data-ttu-id="2b3fa-150">A primera vista, parece ser un problema.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-150">At first glance, that seems to be a problem.</span></span> <span data-ttu-id="2b3fa-151">De forma predeterminada, y según el tamaño de la ventana de la consola, Get-CsCertificate posible que no pueda mostrar todos los nombres:</span><span class="sxs-lookup"><span data-stu-id="2b3fa-151">By default, and depending on the size of your console window, Get-CsCertificate might not be able to display all the names:</span></span>

<span data-ttu-id="2b3fa-152">AlternativeNames: {sip.fabrikam.com, LYNC.fabrikam.com,</span><span class="sxs-lookup"><span data-stu-id="2b3fa-152">AlternativeNames : {sip.fabrikam.com, LYNC.fabrikam.com,</span></span>

<span data-ttu-id="2b3fa-153">meet.fabrikam.com, admin. Fabrika...}</span><span class="sxs-lookup"><span data-stu-id="2b3fa-153">meet.fabrikam.com, admin.fabrika...}</span></span>

<span data-ttu-id="2b3fa-154">Para ver todos los nombres alternativos asignados a un certificado, use un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="2b3fa-154">To see all the alternative names assigned to a certificate use a command similar to this one:</span></span>

`Get-CsCertificate | Where-Object {$_.SerialNumber -eq "611BB01200000000000C"} | Select-Object -ExpandProperty AlternativeNames`

<span data-ttu-id="2b3fa-155">Que le mostrarán todos los nombres alternativos en el certificado:</span><span class="sxs-lookup"><span data-stu-id="2b3fa-155">That should show you all of the alternative names on the certificate:</span></span>

<span data-ttu-id="2b3fa-156">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="2b3fa-156">sip.fabrikam.com</span></span>

<span data-ttu-id="2b3fa-157">LYNC.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="2b3fa-157">LYNC.fabrikam.com</span></span>

<span data-ttu-id="2b3fa-158">meet.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="2b3fa-158">meet.fabrikam.com</span></span>

<span data-ttu-id="2b3fa-159">admin.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="2b3fa-159">admin.fabrikam.com</span></span>

<span data-ttu-id="2b3fa-160">LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="2b3fa-160">LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="2b3fa-161">Dialin.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="2b3fa-161">Dialin.fabrikam.com</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2b3fa-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b3fa-162">See Also</span></span>


[<span data-ttu-id="2b3fa-163">Get-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="2b3fa-163">Get-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCertificate)  
  

<span data-ttu-id="2b3fa-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b3fa-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

