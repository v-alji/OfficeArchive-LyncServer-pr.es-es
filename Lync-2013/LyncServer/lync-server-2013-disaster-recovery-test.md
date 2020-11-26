---
title: 'Lync Server 2013: prueba de recuperación ante desastres'
description: 'Lync Server 2013: prueba de recuperación ante desastres.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disaster recovery test
ms:assetid: 04f5e747-d837-4350-9fc0-8605dbf025a7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747887(v=OCS.15)
ms:contentKeyID: 63969571
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa22abd37f656134c54381d63f29d3160ff85257
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437836"
---
# <a name="disaster-recovery-test-in-lync-server-2013"></a><span data-ttu-id="3f947-103">Prueba de recuperación ante desastres en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f947-103">Disaster recovery test in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f947-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f947-104">

<span> </span></span></span>

<span data-ttu-id="3f947-105">_**Última modificación del tema:** 2015-01-26_</span><span class="sxs-lookup"><span data-stu-id="3f947-105">_**Topic Last Modified:** 2015-01-26_</span></span>

<span data-ttu-id="3f947-106">Realice una recuperación del sistema de un servidor de grupo 2013 de Lync Server para probar el proceso de recuperación ante desastres documentado.</span><span class="sxs-lookup"><span data-stu-id="3f947-106">Perform a system recovery for a Lync Server 2013 pool server to test your documented disaster recovery process.</span></span> <span data-ttu-id="3f947-107">Esta prueba simulará un error completo de hardware en un servidor y ayudará a garantizar que los recursos, planes y datos estén disponibles para su recuperación.</span><span class="sxs-lookup"><span data-stu-id="3f947-107">This test will simulate a complete hardware failure for one server, and will help guarantee that the resources, plans, and data is available for recovery.</span></span> <span data-ttu-id="3f947-108">Trate de variar cada mes el objeto de esta simulación, de modo que su organización vaya poniendo a prueba distintos servidores u otros elementos.</span><span class="sxs-lookup"><span data-stu-id="3f947-108">Try to rotate the focus of the test each month so that your organization tests the failure of a different server or other piece of equipment every time.</span></span>

<span data-ttu-id="3f947-p102">Tenga en cuenta que el programa mediante el cual las organizaciones realizan pruebas de recuperación ante desastres puede variar. Es muy importante no ignorar o descuidar estas pruebas.</span><span class="sxs-lookup"><span data-stu-id="3f947-p102">Note that the schedule by which organizations perform Disaster Recovery testing will vary. It is very important that disaster recovery testing is not ignored or neglected.</span></span>

<div>


<span data-ttu-id="3f947-111">Exporte su topología, directivas y configuración de configuración de Lync Server 2013 a un archivo.</span><span class="sxs-lookup"><span data-stu-id="3f947-111">Export your Lync Server 2013 topology, policies, and configuration settings to a file.</span></span> <span data-ttu-id="3f947-112">Entre otras cosas, este archivo podrá usarse para restaurar esta información en el Almacén de administración central después de una actualización, un error de hardware o cualquier otro problema que resulte en la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="3f947-112">Among other things, this file can then be used to restore this information to the Central Management store after an upgrade, a hardware failure, or some other issue has resulted in data loss.</span></span>

<span data-ttu-id="3f947-113">Importe la topología, las directivas y las opciones de configuración de Lync Server 2013 en el almacén de administración central o en el equipo local, tal y como se muestra en los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="3f947-113">Import your Lync Server 2013 topology, policies, and configuration settings to either the Central Management store or to the local computer as shown in the following commands:</span></span>

`Import-CsConfiguration -ByteInput <Byte[]> [-Force <SwitchParameter>] [-LocalStore <SwitchParameter>]`

`Import-CsConfiguration -FileName <String> [-Force <SwitchParameter>] [-LocalStore <SwitchParameter>]`

<span data-ttu-id="3f947-114">Para hacer una copia de seguridad de los datos de producción de Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="3f947-114">To back up production Lync Server 2013 data:</span></span>

  - <span data-ttu-id="3f947-115">Haga una copia de seguridad de las bases de datos RTC y LCSLog con el proceso de copia de seguridad estándar de SQL Server para volcar la base de datos en un dispositivo de volcado de archivo o cinta.</span><span class="sxs-lookup"><span data-stu-id="3f947-115">Back up the RTC and LCSLog databases by using the standard SQL Server backup process to dump the database to a file or tape dump device.</span></span>

  - <span data-ttu-id="3f947-116">Use una aplicación de terceros para realizar en un archivo o cinta una copia de seguridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="3f947-116">Use third-party backup application to back up the data to file or to tape.</span></span>

  - <span data-ttu-id="3f947-117">Use el cmdlet Export-CsUserData para crear una exportación XML de toda la base de datos RTC.</span><span class="sxs-lookup"><span data-stu-id="3f947-117">Use the Export-CsUserData cmdlet to create an XML export of the whole RTC database.</span></span>

  - <span data-ttu-id="3f947-118">Use la copia de seguridad del sistema de archivos o una aplicación de terceros para realizar una copia de seguridad del contenido de las reuniones y los registros de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="3f947-118">Use the file system backup or third-party to back up meeting content and compliance logs.</span></span>

  - <span data-ttu-id="3f947-119">Use la herramienta de línea de comandos Export-CsConfiguration para realizar copias de seguridad de la configuración de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3f947-119">Use the Export-CsConfiguration command-line tool to back up Lync Server 2013 settings.</span></span>

<span data-ttu-id="3f947-120">El primer paso en el procedimiento de conmutación por error incluye el traslado forzoso de los usuarios desde el grupo de producción al grupo de recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="3f947-120">The first step in the failover procedure includes a forced move of users from the production pool to the Disaster Recovery pool.</span></span>

<span data-ttu-id="3f947-121">Se trata de un traslado forzoso porque el grupo de producción no estará disponible para aceptar la reubicación de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="3f947-121">This will be a forced move because the production pool won't be available to accept the user relocation.</span></span>

<span data-ttu-id="3f947-122">El proceso de desplazar usuarios de Lync Server 2013 es realmente un cambio en un atributo del objeto de cuenta de usuario, además de una actualización de registro en la base de datos de SQL de RTC.</span><span class="sxs-lookup"><span data-stu-id="3f947-122">The Lync Server 2013 move user process is effectively a change to an attribute on the user account object in addition to a record update on the RTC SQL database.</span></span>

<span data-ttu-id="3f947-123">Estos datos pueden restaurarse mediante los dos siguientes procesos:</span><span class="sxs-lookup"><span data-stu-id="3f947-123">This data can be restored through the following two processes:</span></span>

  - <span data-ttu-id="3f947-124">La base de datos RTC puede restaurarse desde el dispositivo de volcado de copia de seguridad original desde el servidor SQL de producción mediante el proceso de restauración estándar de SQL Server o mediante una herramienta de copia de seguridad y restauración de terceros.</span><span class="sxs-lookup"><span data-stu-id="3f947-124">RTC database can be restored from the original backup dump device from the production SQL Server using the standard SQL Server restore process, or using a third-party backup/restore utility.</span></span>

  - <span data-ttu-id="3f947-125">Los datos de contacto de usuarios pueden restaurarse con la utilidad DBIMPEXP.exe, utilizando el archivo XML creado por la exportación del SQL Server de producción.</span><span class="sxs-lookup"><span data-stu-id="3f947-125">User contact data can be restored with the DBIMPEXP.exe utility using the XML file that was created from the production SQL Server export.</span></span>

<span data-ttu-id="3f947-126">Una vez que se hayan restaurado estos datos, los usuarios podrán conectarse eficazmente al grupo de recuperación ante desastres de Lync Server 2013 y funcionar como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="3f947-126">After this data is restored, users can effectively connect to the Disaster Recovery Lync Server 2013 pool, and operate as usual.</span></span>

<span data-ttu-id="3f947-127">Para permitir que los usuarios se conecten al grupo de recuperación ante desastres de Lync Server 2013, será necesario un cambio de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="3f947-127">To enable users to connect to the Disaster Recovery Lync Server 2013 pool, a DNS record change will be required.</span></span>

<span data-ttu-id="3f947-128">Los clientes hará referencia al grupo de producción de Lync Server 2013 con la configuración automática y los registros SRV de DNS de:</span><span class="sxs-lookup"><span data-stu-id="3f947-128">The production Lync Server 2013 pool will be referenced by clients using the auto-configuration and DNS SRV records of:</span></span>

  - <span data-ttu-id="3f947-129">SRV: \_ SIP. \_ TSL.\<domain\></span><span class="sxs-lookup"><span data-stu-id="3f947-129">SRV: \_sip.\_tls.\<domain\></span></span> <span data-ttu-id="3f947-130">/CNAME: SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="3f947-130">/CNAME: SIP.\<domain\></span></span>

  - <span data-ttu-id="3f947-131">CNAME: SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="3f947-131">CNAME: SIP.\<domain\></span></span> <span data-ttu-id="3f947-132">/cvc-pool-1.\<domain\></span><span class="sxs-lookup"><span data-stu-id="3f947-132">/cvc-pool-1.\<domain\></span></span>

<span data-ttu-id="3f947-133">Para facilitar la conmutación por error, este registro CNAME debe actualizarse para que haga referencia al FQDN DROCSPool:</span><span class="sxs-lookup"><span data-stu-id="3f947-133">To facilitate the failover, this CNAME record must be updated to reference the DROCSPool FQDN:</span></span>

  - <span data-ttu-id="3f947-134">CNAME: SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="3f947-134">CNAME: SIP.\<domain\></span></span> <span data-ttu-id="3f947-135">/DROCSPool.\<domain\></span><span class="sxs-lookup"><span data-stu-id="3f947-135">/DROCSPool.\<domain\></span></span>

  - <span data-ttu-id="3f947-136">SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="3f947-136">Sip.\<domain\></span></span>

  - <span data-ttu-id="3f947-137">Dichos.\<domain\></span><span class="sxs-lookup"><span data-stu-id="3f947-137">AV.\<domain\></span></span>

  - <span data-ttu-id="3f947-138">WebConf.\<domain\></span><span class="sxs-lookup"><span data-stu-id="3f947-138">webconf.\<domain\></span></span>

  - <span data-ttu-id="3f947-139">OCSServices.\<domain\></span><span class="sxs-lookup"><span data-stu-id="3f947-139">OCSServices.\<domain\></span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3f947-140">Para obtener información detallada sobre la administración y los procedimientos de administración, consulte <A href="lync-server-2013-backing-up-and-restoring-lync-server.md">copia de seguridad y restauración de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3f947-140">For detailed administration and management procedures, see <A href="lync-server-2013-backing-up-and-restoring-lync-server.md">Backing up and restoring Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3f947-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f947-141">See Also</span></span>


[<span data-ttu-id="3f947-142">Planeación de alta disponibilidad y recuperación ante desastres en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f947-142">Planning for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
[<span data-ttu-id="3f947-143">Cmdlets de copia de seguridad y alta disponibilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f947-143">Backup and high availability cmdlets in Lync Server 2013</span></span>](https://docs.microsoft.com/powershell/module/skype/?view=skype-ps)  


[<span data-ttu-id="3f947-144">Importar-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f947-144">Import-CsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsConfiguration)  
[<span data-ttu-id="3f947-145">Copia de seguridad y restauración de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f947-145">Backing up and restoring Lync Server 2013</span></span>](lync-server-2013-backing-up-and-restoring-lync-server.md)  
[<span data-ttu-id="3f947-146">Administrar la recuperación ante desastres, la alta disponibilidad y el servicio de copia de seguridad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f947-146">Managing Lync Server 2013 disaster recovery, high availability, and Backup Service</span></span>](lync-server-2013-managing-lync-server-disaster-recovery-high-availability-and-backup-service.md)  
  

<span data-ttu-id="3f947-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f947-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

