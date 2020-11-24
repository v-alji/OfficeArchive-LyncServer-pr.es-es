---
title: 'Lync Server 2013: Pasos para preparar e implementar el entorno híbrido de Lync Server'
description: 'Lync Server 2013: pasos para preparar e implementar el entorno híbrido de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Steps to prepare and deploy Lync Server 2013 hybrid environment
ms:assetid: a50d4f7b-63f4-4663-af63-56ca87e4e3e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205157(v=OCS.15)
ms:contentKeyID: 48185060
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ffb791a8a45b2220d8987c8d688f346447747c00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398129"
---
# <a name="steps-to-prepare-and-deploy-lync-server-2013-hybrid-environment"></a><span data-ttu-id="fa4e6-103">Pasos para preparar e implementar el entorno híbrido de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa4e6-103">Steps to prepare and deploy Lync Server 2013 hybrid environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fa4e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fa4e6-104">

<span> </span></span></span>

<span data-ttu-id="fa4e6-105">_**Última modificación del tema:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="fa4e6-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="fa4e6-106">En la tabla siguiente se enumeran los pasos necesarios para preparar el entorno para una implementación híbrida con Skype empresarial online y Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-106">The following table lists the steps required to prepare your environment for a hybrid deployment with Skype for Business Online and Microsoft Office 365.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa4e6-107">¿Completado?</span><span class="sxs-lookup"><span data-stu-id="fa4e6-107">Completed?</span></span></th>
<th><span data-ttu-id="fa4e6-108">Paso</span><span class="sxs-lookup"><span data-stu-id="fa4e6-108">Step</span></span></th>
<th><span data-ttu-id="fa4e6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa4e6-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="fa4e6-110">Crear una cuenta de inquilino para Office 365 y habilitar Lync Online</span><span class="sxs-lookup"><span data-stu-id="fa4e6-110">Create a tenant account for Office 365 and enable Lync Online</span></span></p></td>
<td><p><span data-ttu-id="fa4e6-111">Obtenga más información sobre Office 365 y Lync Online en <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-111">Learn about Office 365 and Lync Online at <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">Office 365</a>.</span></span></p>
<p><span data-ttu-id="fa4e6-112">Para asegurarse de que su entorno está listo para Office 365, consulte los <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">requisitos del sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-112">To make sure that your environment is ready for Office 365, see the <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">System Requirements</a>.</span></span></p>
<p><span data-ttu-id="fa4e6-113">Para obtener detalles sobre la configuración de Office 365, consulte <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">Introducción a office 365</a> y <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">configurar Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-113">For details about setting up Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">Getting Started with Office 365</a> and <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">Set Up Office 365</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="fa4e6-114">Agregue su dominio y compruebe la propiedad</span><span class="sxs-lookup"><span data-stu-id="fa4e6-114">Add your domain and verify ownership</span></span></p></td>
<td><p><span data-ttu-id="fa4e6-115">Su dominio se denomina también a veces <em>dominio personal</em>.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-115">Your domain is sometimes also referred to as your <em>vanity domain</em>.</span></span> <span data-ttu-id="fa4e6-116">Debe agregar su dominio a su organización de Office 365 y, a continuación, seguir los pasos para validar el dominio con Office 365.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-116">You must add your domain to your Office 365 organization, and then follow the steps to validate the domain with Office 365.</span></span> <span data-ttu-id="fa4e6-117">Esto se hace para confirmar que usted es el propietario del dominio.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-117">This is to confirm that you are the owner of the domain.</span></span></p>
<p><span data-ttu-id="fa4e6-118">Para agregar su dominio a su organización de Office 365, siga los pasos que se describen en <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">Agregar su dominio a office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-118">To add your domain to your Office 365 organization, follow the steps described at <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">Add your domain to Office 365</a>.</span></span></p>
<p><span data-ttu-id="fa4e6-119">Complete todos los pasos de cada sección del tema, incluida la &quot; edición de registros DNS para los servicios de Office 365.&quot;</span><span class="sxs-lookup"><span data-stu-id="fa4e6-119">Complete all of the steps in each section in the topic, including &quot;Edit DNS records for your Office 365 services.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="fa4e6-120">Comprobar la preparación del entorno</span><span class="sxs-lookup"><span data-stu-id="fa4e6-120">Verify environment readiness</span></span></p></td>
<td><p><span data-ttu-id="fa4e6-121">Puede usar el Asistente de configuración de Office 365 para ayudarle a implementar Office 365.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-121">You can use the Office 365 Setup Assistant to help you deploy Office 365.</span></span> <span data-ttu-id="fa4e6-122">Para obtener más información, vea <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">usar el Asistente de configuración para determinar la preparación de Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-122">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">Use Setup Assistant to determine Office 365 readiness</a>.</span></span></p>
<p><span data-ttu-id="fa4e6-123">Para obtener más información sobre cómo usar la herramienta e implementar Office 365, consulte la <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">Guía de implementación de office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-123">For details about using the tool and deploying Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">Office 365 deployment guide</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="fa4e6-124">Prepararse para la sincronización de Active Directory</span><span class="sxs-lookup"><span data-stu-id="fa4e6-124">Prepare for Active Directory synchronization</span></span></p></td>
<td><p><span data-ttu-id="fa4e6-125">La sincronización de Active Directory mantiene su Active Directory local sincronizado continuamente con Office 365.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-125">Active Directory synchronization keeps your on-premises Active Directory continuously synchronized with Office 365.</span></span> <span data-ttu-id="fa4e6-126">Esto le permite no solo crear versiones sincronizadas de cada grupo y cuenta de usuario, sino que también le permite la sincronización de la lista global de direcciones (GAL) desde su entorno de Microsoft Exchange Server local con Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-126">This lets you create synchronized versions of each user account and group, and also enables global address list (GAL) synchronization from your local Microsoft Exchange Server environment to Microsoft Exchange Online.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="fa4e6-127">Debe sincronizar las cuentas de AD de todos los usuarios de Lync de su organización entre las implementaciones de Lync locales y en línea, incluso si los usuarios no se mueven a Lync Online.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-127">You need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="fa4e6-128">Si no sincroniza todos los usuarios, puede ser que la comunicación entre los usuarios locales y en línea de su organización no funcione como se podría esperar.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-128">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>


</div>
<p><span data-ttu-id="fa4e6-129">Para preparar el entorno para la sincronización de Active Directory, siga los pasos que se describen en <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">Guía básica de sincronización de directorios</a>, incluida la configuración del inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-129">To prepare your environment for Active Directory synchronization, follow the steps described in <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">Directory synchronization Roadmap</a>, including setting up single sign-on.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="fa4e6-130">Crear certificados para servicios de Federación de Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="fa4e6-130">Create certificates for Active Directory Federation Services (AD FS)</span></span></p></td>
<td><p><span data-ttu-id="fa4e6-131">Tendrá que crear los certificados que se usan para la Federación de identidades con Office 365.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-131">You will need to create the certificates that are used for identity federation with Office 365.</span></span> <span data-ttu-id="fa4e6-132">Para obtener más información, consulte la sección "certificados de servidor de Federación" de los temas planear e implementar AD FS para su uso con el inicio de sesión único en la <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">lista de comprobación: Use AD FS para implementar y administrar el inicio de sesión único</a>.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-132">For more information, see the “Federation server certificates” section of the Plan for and deploy AD FS for use with single sign-on topic at <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">Checklist: Use AD FS to implement and manage single sign-on</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="fa4e6-133">Asignar certificados para AD FS</span><span class="sxs-lookup"><span data-stu-id="fa4e6-133">Assign certificates for AD FS</span></span></p></td>
<td><p><span data-ttu-id="fa4e6-134">Después de crear los certificados que se usan para la Federación de identidades con Office 365, debe instalarlos y asignarlos.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-134">After you create the certificates that are used for identity federation with Office 365, you must install and assign them.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="fa4e6-135">Mover los usuarios piloto a Skype empresarial online</span><span class="sxs-lookup"><span data-stu-id="fa4e6-135">Move pilot users to Skype for Business Online</span></span></p></td>
<td><p><span data-ttu-id="fa4e6-136">Una vez completados los pasos para preparar y configurar su entorno para Skype empresarial online, puede empezar a mover los usuarios piloto a Lync Online.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-136">After you have completed the steps to prepare and configure your environment for Skype for Business Online, you can start moving pilot users to Lync Online.</span></span></p>
<p><span data-ttu-id="fa4e6-137">Consulte <a href="lync-server-2013-move-users-to-lync-online.md">mover usuarios a Lync Online en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-137">See <a href="lync-server-2013-move-users-to-lync-online.md">Move users to Lync Online in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="fa4e6-138">Administrar usuarios en una implementación híbrida</span><span class="sxs-lookup"><span data-stu-id="fa4e6-138">Administering users in a hybrid deployment</span></span></p></td>
<td><p><span data-ttu-id="fa4e6-139">Para obtener detalles sobre cómo administrar usuarios en una implementación híbrida, consulte <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">administrar usuarios en una implementación híbrida de Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="fa4e6-139">For details about how to administer users in a hybrid deployment, see <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Administering users in a hybrid Lync Server 2013 deployment</a>.</span></span></p></td>
</tr><span data-ttu-id="fa4e6-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fa4e6-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

