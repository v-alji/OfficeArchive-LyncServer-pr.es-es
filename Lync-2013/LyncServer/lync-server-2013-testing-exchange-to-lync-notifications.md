---
title: 'Lync Server 2013: pruebas de notificaciones de Exchange a Lync'
description: 'Lync Server 2013: pruebas de las notificaciones de Exchange a Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Exchange to Lync notifications
ms:assetid: ed2d6325-3cf5-4450-9951-03092bcb0a7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727315(v=OCS.15)
ms:contentKeyID: 63969665
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bdf453bfdaab7e7b6bdaae8b67ac7759c0d55af4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398970"
---
# <a name="testing-exchange-to-lync-notifications-in-lync-server-2013"></a><span data-ttu-id="5b831-103">Prueba de las notificaciones de Exchange para Lync en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b831-103">Testing Exchange to Lync notifications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b831-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b831-104">

<span> </span></span></span>

<span data-ttu-id="5b831-105">_**Última modificación del tema:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="5b831-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b831-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="5b831-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="5b831-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="5b831-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b831-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="5b831-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="5b831-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b831-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b831-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="5b831-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="5b831-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="5b831-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="5b831-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe asignar un rol de RBAC que tenga permiso para ejecutar el cmdlet <strong>Test-CsExStorageNotification</strong> .</span><span class="sxs-lookup"><span data-stu-id="5b831-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsExStorageNotification</strong> cmdlet.</span></span> <span data-ttu-id="5b831-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5b831-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsExStorageNotification&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="5b831-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b831-114">Description</span></span>

<span data-ttu-id="5b831-115">El cmdlet **Test-CsExStorageNotification** se usa para comprobar que el servicio de notificación de Microsoft Exchange Server 2013 puede notificar a Lync Server 2013 en cualquier momento en que se realicen actualizaciones en la lista de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="5b831-115">The **Test-CsExStorageNotification** cmdlet is used to verify that the Microsoft Exchange Server 2013 notification service can notify Lync Server 2013 any time updates are made to a user's Contact List.</span></span> <span data-ttu-id="5b831-116">Este cmdlet solo es válido si usa el almacén de contactos unificado.</span><span class="sxs-lookup"><span data-stu-id="5b831-116">This cmdlet is valid only if you are using the unified contact store.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="5b831-117">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="5b831-117">Running the test</span></span>

<span data-ttu-id="5b831-118">El comando que se muestra en el ejemplo 1 prueba si el servicio de almacenamiento de Lync Server puede conectarse al servicio de notificación de buzón de Microsoft Exchange Server para el usuario sip:kenmyer@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="5b831-118">The command shown in Example 1 tests to see whether the Lync Server Storage Service can connect to the Microsoft Exchange Server mailbox notification service for the user sip:kenmyer@litwareinc.com.</span></span> <span data-ttu-id="5b831-119">En este ejemplo, NetNamedPipe se usa como enlace de WCF.</span><span class="sxs-lookup"><span data-stu-id="5b831-119">In this example, NetNamedPipe is used as the WCF binding.</span></span>

    Test-CsExStorageNotification -SipUri "sip:kenmyer@litwareinc.com" -Binding "NetNamedPipe"

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="5b831-120">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="5b831-120">Determining success or failure</span></span>

<span data-ttu-id="5b831-121">Si la integración de Exchange está configurada correctamente, recibirá un resultado similar a este, con la propiedad result marcada como **correcta**:</span><span class="sxs-lookup"><span data-stu-id="5b831-121">If Exchange integration is configured correctly , you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="5b831-122">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="5b831-122">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="5b831-123">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="5b831-123">Result : Success</span></span>

<span data-ttu-id="5b831-124">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5b831-124">Latency : 00:00:00</span></span>

<span data-ttu-id="5b831-125">Mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="5b831-125">Error Message :</span></span>

<span data-ttu-id="5b831-126">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="5b831-126">Diagnosis :</span></span>

<span data-ttu-id="5b831-127">Si el usuario especificado no puede recibir notificaciones, el resultado se mostrará como error y la información adicional se registrará en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="5b831-127">If the specified user can't receive notifications, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="5b831-128">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="5b831-128">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="5b831-129">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="5b831-129">Result : Failure</span></span>

<span data-ttu-id="5b831-130">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5b831-130">Latency : 00:00:00</span></span>

<span data-ttu-id="5b831-131">Mensaje de error: 10060, error al intentar la conexión porque la persona conectada</span><span class="sxs-lookup"><span data-stu-id="5b831-131">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="5b831-132">no respondió correctamente después de un período de tiempo, o</span><span class="sxs-lookup"><span data-stu-id="5b831-132">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="5b831-133">error en la conexión establecida porque el host conectado tiene</span><span class="sxs-lookup"><span data-stu-id="5b831-133">established connection failed because connected host has</span></span>

<span data-ttu-id="5b831-134">Error al responder 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="5b831-134">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="5b831-135">Excepción interna: error en el intento de conexión porque el</span><span class="sxs-lookup"><span data-stu-id="5b831-135">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="5b831-136">la parte conectada no respondió correctamente después de un período de</span><span class="sxs-lookup"><span data-stu-id="5b831-136">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="5b831-137">hora o error de conexión establecida porque el host conectado</span><span class="sxs-lookup"><span data-stu-id="5b831-137">time, or established connection failed because connected host</span></span>

<span data-ttu-id="5b831-138">Error al responder 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="5b831-138">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="5b831-139">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="5b831-139">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="5b831-140">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="5b831-140">Reasons why the test might have failed</span></span>

<span data-ttu-id="5b831-141">Estas son algunas de las razones comunes por las que **Test-CsExStorageNotification** podría fallar:</span><span class="sxs-lookup"><span data-stu-id="5b831-141">Here are some common reasons why **Test-CsExStorageNotification** might fail:</span></span>

  - <span data-ttu-id="5b831-142">Se proporcionó un valor de parámetro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="5b831-142">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="5b831-143">Si se usa, los parámetros opcionales deben estar configurados correctamente o se producirá un error en la prueba.</span><span class="sxs-lookup"><span data-stu-id="5b831-143">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="5b831-144">Vuelva a ejecutar el comando sin los parámetros opcionales y vea si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="5b831-144">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="5b831-145">Este comando fallará si Microsoft Exchange Server está mal configurado o aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="5b831-145">This command will fail if the Microsoft Exchange Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5b831-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b831-146">See Also</span></span>


[<span data-ttu-id="5b831-147">Test-CsExStorageConnectivity</span><span class="sxs-lookup"><span data-stu-id="5b831-147">Test-CsExStorageConnectivity</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsExStorageConnectivity)  
  

<span data-ttu-id="5b831-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b831-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

