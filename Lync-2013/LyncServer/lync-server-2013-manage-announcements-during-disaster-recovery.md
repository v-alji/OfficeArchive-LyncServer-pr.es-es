---
title: 'Lync Server 2013: Administrar anuncios durante la recuperación ante desastres'
description: 'Lync Server 2013: administrar anuncios durante la recuperación de desastres.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage announcements during disaster recovery
ms:assetid: c33e51ea-421f-42d2-826b-b73968f6bd5b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721874(v=OCS.15)
ms:contentKeyID: 49733807
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d85dfcd15c9c3650bafafa6fa7702e19ac9c4f7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426126"
---
# <a name="manage-announcements-during-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="5e4e5-103">Administrar anuncios durante la recuperación ante desastres en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5e4e5-103">Manage announcements during disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5e4e5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5e4e5-104">

<span> </span></span></span>

<span data-ttu-id="5e4e5-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="5e4e5-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="5e4e5-106">Lync Server 2013 admite anuncios de llamadas a números no asignados durante las interrupciones.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-106">Lync Server 2013 supports announcements for calls to unassigned numbers during outages.</span></span> <span data-ttu-id="5e4e5-107">La función de restauración de la presentación durante una interrupción es opcional.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-107">Restoring announcement functionality during an outage is optional.</span></span> <span data-ttu-id="5e4e5-108">Si decide restaurar los anuncios durante una interrupción, tendrá que volver a crear la configuración del anuncio en el grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-108">If you choose to restore announcements during an outage, you need recreate your announcement configuration in the backup pool.</span></span> <span data-ttu-id="5e4e5-109">En esta sección se describe lo que debe hacer si elige restaurar los anuncios durante la recuperación de desastres.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-109">This section describes what you need to do if you choose to restore announcements during disaster recovery.</span></span>

<span data-ttu-id="5e4e5-110">Esta sección se aplica a los intervalos de números sin asignar que usan la aplicación de anuncios.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-110">This section applies to unassigned number ranges that use the Announcement application.</span></span> <span data-ttu-id="5e4e5-111">Esta sección no se aplica a los intervalos de números sin asignar que usan el operador automático de mensajería unificada (UM) de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-111">This section does not apply to unassigned number ranges that use Exchange Unified Messaging (UM) Auto Attendant.</span></span>

<div>

## <a name="before-an-outage"></a><span data-ttu-id="5e4e5-112">Antes de una interrupción</span><span class="sxs-lookup"><span data-stu-id="5e4e5-112">Before an Outage</span></span>

<span data-ttu-id="5e4e5-113">Independientemente de si opta por usar anuncios durante las interrupciones, debe realizar copias de seguridad separadas de los archivos de audio personalizados que haya configurado para la aplicación de anuncios.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-113">Regardless of whether you choose to use announcements during outages, you should take separate backups of any customized audio files that you configured for the Announcement application.</span></span> <span data-ttu-id="5e4e5-114">No se realiza una copia de seguridad de los anuncios personalizados como parte del proceso de recuperación de desastres de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-114">Customized announcements are not backed up as part of the Lync Server disaster recovery process.</span></span> <span data-ttu-id="5e4e5-115">Si no se realizan copias de seguridad separadas de los archivos y los archivos que ha cargado en el servidor o grupo de servidores están dañados, dañados o borrados, los archivos se perderán.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-115">If you do not take separate backups of the files and the files that you uploaded to the server or pool are damaged, corrupted, or erased, the files will be lost.</span></span>

<span data-ttu-id="5e4e5-116">Si no tiene copias de seguridad de archivos de audio personalizados y los archivos de audio originales ya no están disponibles, puede buscar los archivos de audio que ha configurado para una aplicación de anuncio en el almacén de archivos del servidor o grupo de servidores donde importó originalmente los archivos.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-116">If you do not have backup copies of customized audio files, and the original audio files are no longer available, you can find the audio files that you configured for an Announcement application by looking in the File Store for the server or pool where you originally imported the files.</span></span> <span data-ttu-id="5e4e5-117">Puede copiar todos los archivos de audio que haya configurado para la aplicación de anuncios desde el almacén de archivos.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-117">You can copy all the audio files that you configured for the Announcement application from the File Store.</span></span>

<span data-ttu-id="5e4e5-118">**Para copiar archivos de audio desde el almacén de archivos**</span><span class="sxs-lookup"><span data-stu-id="5e4e5-118">**To copy audio files from the file store**</span></span>

1.  <span data-ttu-id="5e4e5-119">En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="5e4e5-119">At the command line, run:</span></span>
    
        Xcopy <Source: Pool Announcement Service File Store path> <Destination>
    
    <span data-ttu-id="5e4e5-120">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5e4e5-120">For example:</span></span>
    
        Xcopy "<Pool File Store Path>\X-ApplicationServer-X\AppServerFiles\RGS\AS" "<Destination: Backup location>"
    
    <span data-ttu-id="5e4e5-121">Donde X-ApplicationServer-X se refiere al identificador de servicio del servidor de aplicaciones del grupo (por ejemplo, 1-ApplicationServer-1 ")</span><span class="sxs-lookup"><span data-stu-id="5e4e5-121">Where X-ApplicationServer-X refers to the service ID of the Application Server of the pool (for example, 1-ApplicationServer-1")</span></span>


</div>

<div>

## <a name="during-an-outage"></a><span data-ttu-id="5e4e5-122">Durante una interrupción</span><span class="sxs-lookup"><span data-stu-id="5e4e5-122">During an Outage</span></span>

<span data-ttu-id="5e4e5-123">Para usar la aplicación de anuncios durante una interrupción, debe volver a crear la configuración del anuncio en el grupo de copias de seguridad llevando a cabo las tareas descritas en esta sección.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-123">To use the Announcement application during an outage, you need to recreate the announcement configuration in the backup pool by performing the tasks described in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5e4e5-124">Le recomendamos que realice estas tareas después de la conmutación por error al grupo de copias de seguridad, ya que, tan pronto como realice el paso 2, el grupo de copia de seguridad tomará la propiedad de los intervalos de números sin asignar.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-124">We recommend that you perform these tasks after you fail over to the backup pool, because as soon as you perform step 2, the backup pool takes ownership of the unassigned number ranges.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="5e4e5-125">Estos pasos no son necesarios para los intervalos de números que usan un número de teléfono de operador automático de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-125">These steps are not required for number ranges that use an Exchange UM Auto Attendant phone number.</span></span>



</div>

<span data-ttu-id="5e4e5-126">**Para volver a crear la configuración del anuncio en el grupo de copias de seguridad**</span><span class="sxs-lookup"><span data-stu-id="5e4e5-126">**To recreate the announcement configuration in the backup pool**</span></span>

1.  <span data-ttu-id="5e4e5-127">Vuelva a crear los anuncios que ha implementado en el grupo principal del grupo de copias de seguridad de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5e4e5-127">Recreate the announcements that you deployed in the primary pool in the backup pool by doing the following:</span></span>
    
    1.  <span data-ttu-id="5e4e5-128">Importe los archivos de audio que se usan en el grupo primario al grupo de copia de seguridad usando el cmdlet **Import-CsAnnouncementFile** y especificando el grupo de copia de seguridad para el parámetro principal.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-128">Import any audio files used in the primary pool to the backup pool by using the **Import-CsAnnouncementFile** cmdlet and specifying the backup pool for the Parent parameter.</span></span>
    
    2.  <span data-ttu-id="5e4e5-129">Vuelva a crear cada anuncio con el cmdlet **New-CsAnnouncement** y especifique el grupo de copias de seguridad para el parámetro principal.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-129">Recreate each announcement by using the **New-CsAnnouncement** cmdlet and specifying the backup pool for the Parent parameter.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5e4e5-130">Para obtener detalles sobre el uso de estos parámetros para crear anuncios en el grupo de copia de seguridad, vea <A href="lync-server-2013-create-an-announcement.md">crear un anuncio en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-130">For details about using these parameters to create announcements in the backup pool, see <A href="lync-server-2013-create-an-announcement.md">Create an announcement in Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="5e4e5-131">Una vez que todos los anuncios se vuelvan a crear en el grupo de copia de seguridad, redirija todos los intervalos de números no asignados que usan anuncios en el grupo primario para los anuncios recreados en el grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-131">After all announcements are recreated in the backup pool, redirect all the unassigned number ranges that use announcements in the primary pool to the recreated announcements in the backup pool.</span></span>
    
    <span data-ttu-id="5e4e5-132">Para cada intervalo de números no asignado que usa un anuncio en el grupo primario, ejecute lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5e4e5-132">For each unassigned number range that uses an announcement in the primary pool, run the following:</span></span>
    
        Set-CsUnassignedNumber -Identity "<name of number range>" -AnnouncementService "<FQDN of backup pool>" -AnnouncementName "<announcement name in backup pool>"

</div>

<div>

## <a name="after-the-outage"></a><span data-ttu-id="5e4e5-133">Después de la interrupción</span><span class="sxs-lookup"><span data-stu-id="5e4e5-133">After the Outage</span></span>

<span data-ttu-id="5e4e5-134">Cuando el grupo principal esté disponible, tendrá que redirigir los intervalos de números no asignados que ha cambiado para la interrupción en el repositorio principal.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-134">When the primary pool becomes available, you need to redirect the unassigned number ranges that you changed for the outage back to the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5e4e5-135">Estos pasos no son necesarios para los intervalos de números que usan un número de teléfono de operador automático de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-135">These steps are not required for number ranges that use an Exchange UM Auto Attendant phone number.</span></span>



</div>

<span data-ttu-id="5e4e5-136">**Para restaurar anuncios en el grupo primario**</span><span class="sxs-lookup"><span data-stu-id="5e4e5-136">**To restore announcements in the primary pool**</span></span>

1.  <span data-ttu-id="5e4e5-137">Si tiene que reconstruir el grupo primario durante la recuperación, tendrá que volver a crear los anuncios en el grupo primario importando los archivos de audio y creando anuncios, del mismo modo que lo hizo en el grupo de copias de seguridad, excepto que especifique el grupo primario para el parámetro principal.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-137">If you had to rebuild the primary pool during the recovery, you need to recreate the announcements in the primary pool by importing the audio files and creating announcements, just as you did in the backup pool, except that you specify the primary pool for the Parent parameter.</span></span> <span data-ttu-id="5e4e5-138">Para obtener más información, vea "durante una interrupción" anteriormente en este tema.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-138">For details, see "During an Outage" earlier in this topic.</span></span>

2.  <span data-ttu-id="5e4e5-139">Para cada intervalo de números no asignado que haya cambiado para la interrupción, ejecute lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5e4e5-139">For each unassigned number range that you changed for the outage, run the following:</span></span>
    
        Set-CsUnassignedNumber [-Identity "<name of number range>"] -AnnouncementService "<FQDN of primary pool>" -AnnouncementName "<announcement name in primary pool>"

3.  <span data-ttu-id="5e4e5-140">De manera opcional, quite los anuncios que ha recreado en el grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-140">Optionally, remove the announcements that you recreated in the backup pool.</span></span> <span data-ttu-id="5e4e5-141">Obtenga una lista de anuncios para la aplicación de anuncios del grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-141">Get a list of announcements for the backup pool Announcement application.</span></span> <span data-ttu-id="5e4e5-142">En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="5e4e5-142">At the command line, run:</span></span>
    
        Get-CsAnnouncement -Identity "<Service:service ID>"
    
    <span data-ttu-id="5e4e5-143">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5e4e5-143">For example:</span></span>
    
        Get-CsAnnouncement -Identity "ApplicationServer:redmond.contoso.com
    
    <span data-ttu-id="5e4e5-144">En la lista resultante, busque los anuncios que desea quitar y copie los GUIDs.</span><span class="sxs-lookup"><span data-stu-id="5e4e5-144">In the resulting list, locate the announcements you want to remove and copy the GUIDs.</span></span> <span data-ttu-id="5e4e5-145">Para cada anuncio que desee quitar, ejecute:</span><span class="sxs-lookup"><span data-stu-id="5e4e5-145">For each announcement you want to remove, run:</span></span>
    
        Remove-CsAnnouncement -Identity "<Service:service ID/guid>"
    
    <span data-ttu-id="5e4e5-146">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5e4e5-146">For example:</span></span>
    
        Remove-CsAnnouncement -Identity "ApplicationServer:redmond.contoso.com/1951f734-c80f-4fb2-965d-51807c792b90"


<span data-ttu-id="5e4e5-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5e4e5-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

