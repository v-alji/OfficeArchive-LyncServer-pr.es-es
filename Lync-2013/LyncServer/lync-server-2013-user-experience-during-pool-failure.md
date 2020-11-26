---
title: Experiencia de usuario de Lync Server 2013 durante un error de grupo
description: Experiencia de usuario de Lync Server 2013 durante un error de grupo.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User experience during pool failure
ms:assetid: b224b0d0-87e3-4cac-ae87-f45f54fabb49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205184(v=OCS.15)
ms:contentKeyID: 48185166
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a0483a01b643d8195e7f8f6259c11ab6fc3561f2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440783"
---
# <a name="user-experience-during-pool-failure-in-lync-server-2013"></a><span data-ttu-id="96916-103">Experiencia de usuario durante un error de grupo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96916-103">User experience during pool failure in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96916-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96916-104">

<span> </span></span></span>

<span data-ttu-id="96916-105">_**Última modificación del tema:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="96916-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="96916-106">Si se conmuta por error un grupo, todos los usuarios del grupo afectado estarán obligados a cerrar sesión y, a continuación, iniciar sesión en el grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="96916-106">If a pool is failed over, all users of the affected pool are forced to sign out and then sign into the backup pool.</span></span> <span data-ttu-id="96916-107">Durante un período breve los usuarios que inicien sesión en el grupo de copia de seguridad pueden encontrarse en modo de resistencia.</span><span class="sxs-lookup"><span data-stu-id="96916-107">For a brief period users who sign into the backup pool may be in resiliency mode.</span></span> <span data-ttu-id="96916-108">En el modo de resistencia, los usuarios no pueden realizar tareas que provocarían un cambio continuo en Lync Server, como agregar un contacto.</span><span class="sxs-lookup"><span data-stu-id="96916-108">In Resiliency mode, users are unable to perform tasks that would cause a persistent change on Lync Server, such as adding a contact.</span></span> <span data-ttu-id="96916-109">Una vez finalizada la conmutación por error, todos los usuarios pueden utilizar todos los servicios del grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="96916-109">After the failover is complete, all users can get all services from the backup pool.</span></span>

<span data-ttu-id="96916-110">Todas las sesiones que tiene un usuario cuando se produce un error en el grupo, y el usuario debe volver a establecer esas sesiones después de la conmutación por error para continuar.</span><span class="sxs-lookup"><span data-stu-id="96916-110">Any sessions a user has when the pool fails are disrupted, and the user must re-establish those sessions after failover to continue.</span></span>

<span data-ttu-id="96916-111">No se vuelven a ubicar los usuarios durante la conmutación por error o la conmutación por recuperación.</span><span class="sxs-lookup"><span data-stu-id="96916-111">Users are not rehomed during failover or failback.</span></span> <span data-ttu-id="96916-112">Los usuarios que están hospedados en un grupo donde se produce un error se hospedarán temporalmente en el grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="96916-112">Users who are homed on a pool that fails will be temporarily serviced by the backup pool.</span></span> <span data-ttu-id="96916-113">Cuando se restaura el grupo de inicio, el administrador puede migrar por error a estos usuarios para que sean atendidas por su grupo original.</span><span class="sxs-lookup"><span data-stu-id="96916-113">When the home pool is restored, the administrator can fail back these users to be serviced by their original home pool.</span></span>

<span data-ttu-id="96916-114">Nota en Lync 2013, la base de datos de la información de ubicación no se replica en el grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="96916-114">Note in Lync 2013, the Location Information Server database is not replicated to the backup pool.</span></span> <span data-ttu-id="96916-115">Como procedimiento recomendado, el administrador tiene que realizar una copia de seguridad de la base de datos LIS periódicamente y usar la última versión de dicha copia para restaurar la base de datos LIS en el grupo de copia de seguridad tras la conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="96916-115">For best practice, the administrator should regularly back up the LIS database and use the latest backup copy to restore the LIS database in the backup pool after the failover.</span></span>

<div>

## <a name="user-experience-during-failover"></a><span data-ttu-id="96916-116">Experiencia del usuario durante la conmutación por error</span><span class="sxs-lookup"><span data-stu-id="96916-116">User Experience During Failover</span></span>

<span data-ttu-id="96916-117">Cuando un usuario se encuentra en un grupo que falla, el usuario ha cerrado sesión. Todas las sesiones de punto a punto en las que participó el usuario están terminadas, al igual que las conferencias organizadas por dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="96916-117">When a user is in a pool that fails, the user is logged out. Any peer-to-peer session the user was participating in is terminated, as are conferences organized by that user.</span></span> <span data-ttu-id="96916-118">El usuario no puede volver a iniciar sesión hasta que caduque el temporizador de resistencia del registrador o el administrador inicie los procedimientos de conmutación por error, lo que ocurra primero.</span><span class="sxs-lookup"><span data-stu-id="96916-118">The user cannot log back in until either the registrar resiliency timer expires or the administrator initiates failover procedures, whichever comes first.</span></span> <span data-ttu-id="96916-119">Cuando el usuario reinicia sesión, iniciará la sesión en el grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="96916-119">When the user logs back in, they will log in to the backup pool.</span></span> <span data-ttu-id="96916-120">Si inicia sesión antes de que finalice la conmutación por error, estará en modo de resistencia hasta que finalice la conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="96916-120">If they log in before the failover has completed, they will be in Resiliency mode until failover is complete.</span></span> <span data-ttu-id="96916-121">Solo entonces el usuario puede establecer sesiones nuevas o volver a establecer sesiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="96916-121">Only then the user is able to establish new sessions or re-establish previous sessions.</span></span>

</div>

<div>

## <a name="user-experience-during-failback"></a><span data-ttu-id="96916-122">Experiencia de usuario durante la conmutación por recuperación</span><span class="sxs-lookup"><span data-stu-id="96916-122">User Experience During Failback</span></span>

<span data-ttu-id="96916-123">La conmutación por recuperación de un grupo puede ocurrir cuando un usuario afectado ha iniciado sesión en el grupo de copia de seguridad y el usuario permanece conectado y sigue trabajando durante la conmutación por recuperación.</span><span class="sxs-lookup"><span data-stu-id="96916-123">Pool failback can happen while an affected user is logged on to the backup pool, and the user remains logged on and working during the failback.</span></span> <span data-ttu-id="96916-124">Tenga en cuenta que el proceso de recuperación tras error tarda varios minutos en completarse.</span><span class="sxs-lookup"><span data-stu-id="96916-124">Note that the failback process takes several minute to complete.</span></span>  <span data-ttu-id="96916-125">Como referencia, se espera que tarde 60 minutos como máximo para un grupo de 20 000 usuarios.</span><span class="sxs-lookup"><span data-stu-id="96916-125">For reference, it is expected to take up to 60 minutes for a pool of 20,000 users.</span></span>

<span data-ttu-id="96916-126">En las tablas siguientes se muestran más detalles sobre cómo un usuario con un cliente de Lync 2013 o de Microsoft Lync 2010 se ve afectado durante y después de la conmutación por recuperación, y también cómo los usuarios de otros grupos ven e interactúan con un usuario de un grupo que se vuelve a enviar.</span><span class="sxs-lookup"><span data-stu-id="96916-126">The following tables show more details about how a user with a Lync 2013 client or a Microsoft Lync 2010 client is affected during and after failback, and also how users in other pools see and interact with a user in a pool who is being failed back.</span></span> <span data-ttu-id="96916-127">Los usuarios con clientes de Microsoft Office Communicator 2007 R2 no pueden iniciar sesión hasta que el grupo de servidores front-end no se haya realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="96916-127">Users with Microsoft Office Communicator 2007 R2 clients cannot sign in until the Front End pool is completely failed back.)</span></span>

<span data-ttu-id="96916-128">El término *usuario afectado* hace referencia a cualquier usuario que sufrió una conmutación por error en el grupo principal y está hospedado ahora en el grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="96916-128">The term *affected user* refers to any user who was failed over from the home pool and is being serviced by the backup pool.</span></span> <span data-ttu-id="96916-129">Por definición, cualquier usuario que haya alojado originalmente en el grupo de copias de seguridad no es un usuario afectado.</span><span class="sxs-lookup"><span data-stu-id="96916-129">By definition, any user originally homed on the backup pool is not an affected user.</span></span>

### <a name="user-experience-for-an-affected-user-in-a-pool-in-failback"></a><span data-ttu-id="96916-130">Experiencia de un usuario afectado en un grupo de conmutación por recuperación</span><span class="sxs-lookup"><span data-stu-id="96916-130">User Experience for an Affected User in a Pool in Failback</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96916-131">Tarea o estado del usuario</span><span class="sxs-lookup"><span data-stu-id="96916-131">User state or task</span></span></th>
<th><span data-ttu-id="96916-132">Durante la conmutación por recuperación</span><span class="sxs-lookup"><span data-stu-id="96916-132">During failback</span></span></th>
<th><span data-ttu-id="96916-133">Una vez finalizada la conmutación por recuperación</span><span class="sxs-lookup"><span data-stu-id="96916-133">After failback completion</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96916-134">Estado del usuario que ya ha iniciado sesión</span><span class="sxs-lookup"><span data-stu-id="96916-134">User state of user already logged in</span></span></p></td>
<td><p><span data-ttu-id="96916-p108">El usuario permanece en su sesión y sigue conectado al grupo de copia de seguridad. En algún momento, se cerrará la sesión del usuario y volverá a la sesión en el grupo principal original, en el modo de resistencia.</span><span class="sxs-lookup"><span data-stu-id="96916-p108">User stays signed in and connected to backup pool. At some point user will be signed out and sign back in to the original home pool, in Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="96916-137">El usuario continúa en su sesión y se coloca en modo normal.</span><span class="sxs-lookup"><span data-stu-id="96916-137">User remains signed in and goes into regular mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96916-138">Inicio de sesión de un nuevo usuario</span><span class="sxs-lookup"><span data-stu-id="96916-138">New user logging in</span></span></p></td>
<td><p><span data-ttu-id="96916-139">El usuario puede iniciar sesión en el grupo principal en el modo de resistencia.</span><span class="sxs-lookup"><span data-stu-id="96916-139">User can sign in to the home pool in Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="96916-140">El usuario puede iniciar sesión en el grupo principal original en modo normal.</span><span class="sxs-lookup"><span data-stu-id="96916-140">User can sign in to the original home pool in regular mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96916-141">Conferencias en curso organizadas por un usuario afectado</span><span class="sxs-lookup"><span data-stu-id="96916-141">Ongoing conferences organized by affected user</span></span></p></td>
<td><p><span data-ttu-id="96916-p109">Se terminan todas las modalidades de conferencia. Se mostrará el botón Unirse de nuevo, pero ningún usuario puede volver a unirse mientras el usuario afectado está en modo de resistencia.</span><span class="sxs-lookup"><span data-stu-id="96916-p109">All modalities of conference are terminated. Rejoin button will appear, but no users can rejoin while the affected user is in Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="96916-p110">Ahora funcionan todas las modalidades. Cada participante tiene que hacer clic para volver a unirse a la conferencia.</span><span class="sxs-lookup"><span data-stu-id="96916-p110">All modalities now work. Every participant needs to click to rejoin the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96916-146">Conferencias en curso organizadas por un usuario no afectado</span><span class="sxs-lookup"><span data-stu-id="96916-146">Ongoing conferences organized by unaffected user</span></span></p></td>
<td><p><span data-ttu-id="96916-p111">La conferencia continúa y el usuario afectado puede permanecer en la conferencia. El usuario afectado está limitado a lo que se puede hacer en el modo de resistencia.</span><span class="sxs-lookup"><span data-stu-id="96916-p111">Conference continues and affected user can stay in the conference. Affected user is restricted to what he/she can do in Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="96916-149">La conferencia continúa y el usuario afectado puede permanecer en la conferencia y todas las modalidades funcionan después de que el usuario sale del modo de resistencia.</span><span class="sxs-lookup"><span data-stu-id="96916-149">Conference continues, and affected user can stay in the conference and all modalities work after user exits Resiliency mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96916-150">Programación o modificación de las reuniones programadas, creación de conferencias ad-hoc</span><span class="sxs-lookup"><span data-stu-id="96916-150">Scheduling or modifying scheduled meetings, creating ad-hoc conferences</span></span></p></td>
<td><p><span data-ttu-id="96916-151">No son posibles mientras el usuario está en modo de resistencia.</span><span class="sxs-lookup"><span data-stu-id="96916-151">Not possible while user is in Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="96916-152">Disponibles para todas las modalidades.</span><span class="sxs-lookup"><span data-stu-id="96916-152">Available for all modalities.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96916-153">Presencia según otros usuarios en el mismo grupo</span><span class="sxs-lookup"><span data-stu-id="96916-153">Presence as seen by other users in the same pool</span></span></p></td>
<td><p><span data-ttu-id="96916-154">Presencia desconocida mientras el usuario está conectado al grupo de copia de seguridad durante el modo de resistencia.</span><span class="sxs-lookup"><span data-stu-id="96916-154">Presence unknown while user is signed into backup pool during Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="96916-155">Muestra el último estado de presencia establecido por el usuario, y los cambios de presencia ahora se reflejarán.</span><span class="sxs-lookup"><span data-stu-id="96916-155">Shows the last presence state set by the user, and presence changes will now be reflected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96916-156">Disponibilidad del servicio de la libreta de direcciones y la lista de contactos</span><span class="sxs-lookup"><span data-stu-id="96916-156">Contacts list and Address Book Service availability</span></span></p></td>
<td><p><span data-ttu-id="96916-157">No disponible</span><span class="sxs-lookup"><span data-stu-id="96916-157">Not available</span></span></p></td>
<td><p><span data-ttu-id="96916-158">Disponible</span><span class="sxs-lookup"><span data-stu-id="96916-158">Available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96916-159">Todas las sesiones punto a punto y las modalidades</span><span class="sxs-lookup"><span data-stu-id="96916-159">All peer-to-peer sessions and modalities</span></span></p></td>
<td><p><span data-ttu-id="96916-160">Disponible</span><span class="sxs-lookup"><span data-stu-id="96916-160">Available</span></span></p></td>
<td><p><span data-ttu-id="96916-161">Disponible</span><span class="sxs-lookup"><span data-stu-id="96916-161">Available</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="user-experience-for-a-user-homed-in-an-unaffected-pool-during-failback-of-another-pool"></a><span data-ttu-id="96916-162">Experiencia de un usuario hospedado en un grupo de servidores no afectado durante la conmutación por recuperación de otro grupo</span><span class="sxs-lookup"><span data-stu-id="96916-162">User Experience for a User Homed in an Unaffected Pool During Failback of Another Pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96916-163">Tarea de usuario</span><span class="sxs-lookup"><span data-stu-id="96916-163">User task</span></span></th>
<th><span data-ttu-id="96916-164">Durante la conmutación por recuperación</span><span class="sxs-lookup"><span data-stu-id="96916-164">During failback</span></span></th>
<th><span data-ttu-id="96916-165">Una vez finalizada la conmutación por recuperación</span><span class="sxs-lookup"><span data-stu-id="96916-165">After failback completion</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96916-166">Visualización de la presencia del usuario afectado</span><span class="sxs-lookup"><span data-stu-id="96916-166">Viewing presence of affected user</span></span></p></td>
<td><p><span data-ttu-id="96916-167">Muestra el último estado de presencia establecido por el usuario afectado.</span><span class="sxs-lookup"><span data-stu-id="96916-167">Shows the last presence state set by the affected user.</span></span></p></td>
<td><p><span data-ttu-id="96916-p112">En funcionamiento. Los usuarios no afectados verán las actualizaciones realizadas por los usuarios afectados.</span><span class="sxs-lookup"><span data-stu-id="96916-p112">Working. Unaffected users see updates made by affected users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96916-170">Conferencias en curso organizadas por un usuario afectado</span><span class="sxs-lookup"><span data-stu-id="96916-170">Ongoing conferences organized by affected user</span></span></p></td>
<td><p><span data-ttu-id="96916-171">Se terminan todas las modalidades de conferencia.</span><span class="sxs-lookup"><span data-stu-id="96916-171">All modalities of conference are terminated.</span></span></p></td>
<td><p><span data-ttu-id="96916-p113">Ahora funcionan todas las modalidades. Cada participante tiene que hacer clic para volver a unirse a la conferencia.</span><span class="sxs-lookup"><span data-stu-id="96916-p113">All modalities now work. Every participant needs to click to rejoin the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96916-174">Conferencias en curso organizadas por un usuario no afectado</span><span class="sxs-lookup"><span data-stu-id="96916-174">Ongoing conferences organized by unaffected user</span></span></p></td>
<td><p><span data-ttu-id="96916-175">La conferencia continúa, el usuario afectado puede permanecer en la conferencia y funcionan todas las modalidades.</span><span class="sxs-lookup"><span data-stu-id="96916-175">Conference continues, and affected user can stay in the conference and all modalities work.</span></span></p></td>
<td><p><span data-ttu-id="96916-176">La conferencia continúa, el usuario afectado puede permanecer en la conferencia y funcionan todas las modalidades.</span><span class="sxs-lookup"><span data-stu-id="96916-176">Conference continues, and affected user can stay in the conference and all modalities work.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96916-177">Todas las sesiones punto a punto y las modalidades</span><span class="sxs-lookup"><span data-stu-id="96916-177">All peer-to-peer sessions and modalities</span></span></p></td>
<td><p><span data-ttu-id="96916-178">Disponible</span><span class="sxs-lookup"><span data-stu-id="96916-178">Available</span></span></p></td>
<td><p><span data-ttu-id="96916-179">Disponible</span><span class="sxs-lookup"><span data-stu-id="96916-179">Available</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="96916-180">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96916-180">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

