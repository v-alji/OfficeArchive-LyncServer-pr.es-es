---
title: 'Lync Server 2013: integración con Microsoft Exchange Server 2013'
description: 'Lync Server 2013: integración con Microsoft Exchange Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Integrating Lync Server 2013 and Exchange Server 2013
ms:assetid: 795dc1c6-524f-4012-8b66-103b55198044
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688098(v=OCS.15)
ms:contentKeyID: 49733697
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54ab4a81e5455bc0a44677b1509876f39ff4d985
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426882"
---
# <a name="integrating-microsoft-lync-server-2013-and-microsoft-exchange-server-2013"></a><span data-ttu-id="31f36-103">Integración de Microsoft Lync Server 2013 y Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f36-103">Integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31f36-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31f36-104">

<span> </span></span></span>

<span data-ttu-id="31f36-105">_**Última modificación del tema:** 2014-07-09_</span><span class="sxs-lookup"><span data-stu-id="31f36-105">_**Topic Last Modified:** 2014-07-09_</span></span>

<span data-ttu-id="31f36-106">Exchange y Lync Server tienen un largo historial de integración y compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="31f36-106">Exchange and Lync Server have a long history of integration and compatibility.</span></span> <span data-ttu-id="31f36-107">Esta integración es más apreciable dentro de la aplicación cliente correspondiente.</span><span class="sxs-lookup"><span data-stu-id="31f36-107">This integration is most noticeable within their respective client application.</span></span> <span data-ttu-id="31f36-108">Por ejemplo, se puede informar de la información de presencia de Lync en Microsoft Outlook. también puede usar el calendario de Outlook para actualizar automáticamente la información de presencia.</span><span class="sxs-lookup"><span data-stu-id="31f36-108">For example, Lync presence information can be reported in Microsoft Outlook; likewise, Lync can use Outlook calendar to automatically update that presence information.</span></span> <span data-ttu-id="31f36-109">(Por ejemplo, Lync puede cambiar su estado a ocupado siempre que su calendario muestre que tiene una reunión programada). Aunque no es necesario ejecutar Exchange para ejecutar Lync Server (o viceversa), hay pocas dudas acerca de que usar los dos productos juntos epitomizes la definición del término "mejor juntos".</span><span class="sxs-lookup"><span data-stu-id="31f36-109">(For example, Lync can change your status to Busy any time your calendar shows that you have a meeting scheduled.) Although you do not have to run Exchange in order to run Lync Server (or vice-versa) there's little doubt that using the two products together epitomizes the very definition of the term "better together."</span></span>

<span data-ttu-id="31f36-110">Esto se aplica especialmente a la publicación de Microsoft Lync Server 2013 y Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="31f36-110">This is especially true with the release of Microsoft Lync Server 2013 and Microsoft Exchange Server 2013.</span></span> <span data-ttu-id="31f36-111">Además de las características, como mensajería unificada y mensajería instantánea y presencia, que se encuentran en Microsoft Exchange Server 2010 y Microsoft Lync Server 2010, las versiones 2013 de los productos de servidor incluyen varias capacidades nuevas.</span><span class="sxs-lookup"><span data-stu-id="31f36-111">In addition to features, such as unified messaging and IM and presence, that are found in Microsoft Exchange Server 2010 and Microsoft Lync Server 2010, the 2013 releases of the server products include a number of new capabilities.</span></span> <span data-ttu-id="31f36-112">Estas funciones incluyen elementos como los siguientes:</span><span class="sxs-lookup"><span data-stu-id="31f36-112">These capabilities include such things as:</span></span>

  - <span data-ttu-id="31f36-113">**Integración de archivado de Lync**.</span><span class="sxs-lookup"><span data-stu-id="31f36-113">**Lync Archiving Integration**.</span></span> <span data-ttu-id="31f36-114">En Lync Server 2013, los administradores siguen teniendo la opción de archivar la mensajería instantánea y las transcripciones de conferencias por Internet en SQL Server (de la misma manera que estas transcripciones se archivaron en Lync Server 2010).</span><span class="sxs-lookup"><span data-stu-id="31f36-114">In Lync Server 2013 administrators still have the option of having instant messaging and Web conferencing transcripts archived to SQL Server (the same way these transcripts were archived in Lync Server 2010).</span></span> <span data-ttu-id="31f36-115">Sin embargo, de forma alternativa, los administradores pueden optar por archivar transcripciones en Exchange 2013, almacenar dichas transcripciones en los buzones de los usuarios individuales de la misma forma en que Exchange archiva las comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="31f36-115">Alternatively, however, administrators can choose to have transcripts archived to Exchange 2013, storing those transcripts in the individual user mailboxes in the same way in which Exchange archives communications.</span></span> <span data-ttu-id="31f36-116">Eso significa que un único repositorio para todas sus comunicaciones electrónicas (tanto de Exchange como de Lync Server), lo que facilita la búsqueda y la recuperación de esas comunicaciones archivadas en caso de que surja la necesidad.</span><span class="sxs-lookup"><span data-stu-id="31f36-116">That means a single repository for all your electronic communications (from both Exchange and Lync Server), which makes it much easier to search for and retrieve those archived communications should the need arise.</span></span>

  - <span data-ttu-id="31f36-117">**Almacén de contactos unificado**.</span><span class="sxs-lookup"><span data-stu-id="31f36-117">**Unified Contact Store**.</span></span> <span data-ttu-id="31f36-118">En Lync Server 2010, los usuarios tenían que mantener listas de contactos independientes en Outlook y Lync; de hecho, para asegurarse de que tenía los mismos contactos disponibles en los dos productos, tenía que mantener listas de contactos duplicadas, una para Outlook y otra para Lync.</span><span class="sxs-lookup"><span data-stu-id="31f36-118">In Lync Server 2010, users had to maintain separate contact lists in Outlook and Lync; in fact, to ensure that you had the same contacts available in both products you had to maintain duplicate contact lists, one for Outlook and one for Lync.</span></span> <span data-ttu-id="31f36-119">Sin embargo, con Lync Server 2013, los contactos de usuario se pueden almacenar en Exchange 2013 y en el almacenamiento de contactos unificado.</span><span class="sxs-lookup"><span data-stu-id="31f36-119">With Lync Server 2013, however, user contacts can be stored in Exchange 2013 and the unified contact store.</span></span> <span data-ttu-id="31f36-120">Usar un único almacén de contactos permite a los usuarios mantener un solo conjunto de contactos, con el mismo conjunto de contactos disponibles en Lync 2013, Outlook 2013 y Outlook Web Access 2013.</span><span class="sxs-lookup"><span data-stu-id="31f36-120">Using a single contact store enables users to maintain just one set of contacts, with that same set of contacts being available in Lync 2013, Outlook 2013, and Outlook Web Access 2013.</span></span>

  - <span data-ttu-id="31f36-121">**Programación de reuniones de Lync desde OWA**.</span><span class="sxs-lookup"><span data-stu-id="31f36-121">**Lync Meeting Scheduling from OWA**.</span></span> <span data-ttu-id="31f36-122">Con la integración de Lync Server 2013 y Exchange 2013, los usuarios pueden programar reuniones de Lync desde Outlook Web Access 2013.</span><span class="sxs-lookup"><span data-stu-id="31f36-122">With Lync Server 2013 and Exchange 2013 integration, users can schedule Lync meetings from Outlook Web Access 2013.</span></span>

  - <span data-ttu-id="31f36-123">**Fotos de alta resolución**.</span><span class="sxs-lookup"><span data-stu-id="31f36-123">**High resolution photos**.</span></span> <span data-ttu-id="31f36-124">Lync 2010 solo podría mostrar fotos pequeñas de sus contactos; Esto se debe a que esas fotos se almacenaron en Active Directory y Active Directory impone un píxel de 48 por 48 de tamaño de píxel en las fotos almacenadas.</span><span class="sxs-lookup"><span data-stu-id="31f36-124">Lync 2010 could only display small photos of your contacts; that's because those photos were stored in Active Directory, and Active Directory imposes a 48 pixel by 48 pixel size limitation on stored photos.</span></span> <span data-ttu-id="31f36-125">Sin embargo, con Lync Server 2013, las fotos se pueden almacenar en Microsoft Exchange. Esto permite que las fotos de alta resolución sean tan grandes como 648 píxeles por 648 píxeles.</span><span class="sxs-lookup"><span data-stu-id="31f36-125">With Lync Server 2013, however, photos can be stored in Microsoft Exchange; that allows for high-resolution photos as large as 648 pixels by 648 pixels.</span></span> <span data-ttu-id="31f36-126">Como cabría esperar, Lync 2013 se ha actualizado para permitir la visualización de estas fotografías de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="31f36-126">As you might expect, Lync 2013 has been upgraded to allow for the display of these high-resolution photographs.</span></span>

<span data-ttu-id="31f36-127">Tenga en cuenta que estas nuevas características requieren el uso de Lync Server 2013 y Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="31f36-127">Keep in mind that these new features require the use of both Lync Server 2013 and Exchange 2013.</span></span> <span data-ttu-id="31f36-128">Además de eso, los usuarios que esperan sacar el máximo provecho de estas nuevas capacidades deben tener cuentas en Lync Server 2013 y en Exchange 2013, y deben usar las versiones más recientes del software cliente (por ejemplo, Lync 2013).</span><span class="sxs-lookup"><span data-stu-id="31f36-128">In addition to that, users who hope to take full advantage of these new capabilities must have accounts on Lync Server 2013 and Exchange 2013, and must be using the latest versions of the client software (e.g., Lync 2013).</span></span> <span data-ttu-id="31f36-129">Por ejemplo, el almacén de contactos unificado no está disponible para los usuarios que se han alojado en Lync Server 2010; del mismo modo, las fotos de alta resolución no se pueden mostrar en Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="31f36-129">For example, the unified contact store is not available to users who have been homed on Lync Server 2010; likewise, high-resolution photos cannot be displayed in Lync 2010.</span></span>

<span data-ttu-id="31f36-130">Esta documentación proporciona información acerca de la integración de Lync Server 2013 y de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="31f36-130">This documentation provides information on integrating Lync Server 2013 and Exchange 2013.</span></span> <span data-ttu-id="31f36-131">incluye información paso a paso sobre cómo habilitar nuevas características, como la integración de archivado y el almacenamiento de contactos unificado.</span><span class="sxs-lookup"><span data-stu-id="31f36-131">including step-by-step information on enabling new features such archiving Integration and the unified contact store.</span></span> <span data-ttu-id="31f36-132">Lo que no hace esta documentación es comentar la configuración inicial y la configuración de estos dos productos.</span><span class="sxs-lookup"><span data-stu-id="31f36-132">What this documentation does not do is discuss the initial setup and configuration of these two products.</span></span> <span data-ttu-id="31f36-133">Para obtener detalles sobre la implementación de Lync Server 2013, visite el centro tecnológico de Lync Server 2013 en [https://go.microsoft.com/fwlink/p/?LinkId=246127](https://go.microsoft.com/fwlink/p/?linkid=246127) .</span><span class="sxs-lookup"><span data-stu-id="31f36-133">For details about deploying Lync Server 2013 see the Lync Server 2013 Tech Center at [https://go.microsoft.com/fwlink/p/?LinkId=246127](https://go.microsoft.com/fwlink/p/?linkid=246127).</span></span> <span data-ttu-id="31f36-134">Para obtener más información sobre la implementación de Exchange 2013, visite el Exchange 2013 Tech Center en [https://go.microsoft.com/fwlink/p/?LinkId=268528](https://go.microsoft.com/fwlink/p/?linkid=268528) .</span><span class="sxs-lookup"><span data-stu-id="31f36-134">For details about deploying Exchange 2013 see the Exchange 2013 Tech Center at [https://go.microsoft.com/fwlink/p/?LinkId=268528](https://go.microsoft.com/fwlink/p/?linkid=268528).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="31f36-135">En esta sección</span><span class="sxs-lookup"><span data-stu-id="31f36-135">In This Section</span></span>

[<span data-ttu-id="31f36-136">Requisitos previos para integrar Microsoft Lync Server 2013 y Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f36-136">Prerequisites for integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>](lync-server-2013-prerequisites-for-integrating-with-exchange-server-2013.md)

[<span data-ttu-id="31f36-137">Configurar aplicaciones de socio en Microsoft Lync Server 2013 y Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f36-137">Configuring partner applications in Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>](lync-server-2013-configuring-partner-applications-in-lync-server-2013-and-exchange-server-2013.md)

[<span data-ttu-id="31f36-138">Configuración de Microsoft Lync Server 2013 para usar el archivado de Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f36-138">Configuring Microsoft Lync Server 2013 to use Microsoft Exchange Server 2013 archiving</span></span>](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md)

[<span data-ttu-id="31f36-139">Configuración de Microsoft SharePoint Server 2013 para buscar datos archivados de Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f36-139">Configuring Microsoft SharePoint Server 2013 to search for archived Microsoft Lync Server 2013 data</span></span>](lync-server-2013-configuring-microsoft-sharepoint-server-2013-to-search-for-archived-lync-server-2013-data.md)

[<span data-ttu-id="31f36-140">Configuración de Microsoft Lync Server 2013 para usar el almacenamiento de contactos unificado</span><span class="sxs-lookup"><span data-stu-id="31f36-140">Configuring Microsoft Lync Server 2013 to use the unified contact store</span></span>](lync-server-2013-configuring-lync-server-to-use-the-unified-contact-store.md)

[<span data-ttu-id="31f36-141">Configurar el uso de fotos de alta resolución en Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f36-141">Configuring the use of high-resolution photos in Microsoft Lync Server 2013</span></span>](lync-server-2013-configuring-the-use-of-high-resolution-photos.md)

[<span data-ttu-id="31f36-142">Configuración de la mensajería unificada de Microsoft Exchange Server 2013 para el correo de voz de Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31f36-142">Configuring Microsoft Exchange Server 2013 Unified Messaging for Microsoft Lync Server 2013 voice mail</span></span>](lync-server-2013-configuring-microsoft-exchange-server-2013-unified-messaging-for-lync-server-2013-voice-mail.md)

[<span data-ttu-id="31f36-143">Integración de Microsoft Lync Server 2013 y Microsoft Outlook Web App 2013</span><span class="sxs-lookup"><span data-stu-id="31f36-143">Integrating Microsoft Lync Server 2013 and Microsoft Outlook Web App 2013</span></span>](lync-server-2013-integrating-lync-server-and-outlook-web-app-2013.md)

<span data-ttu-id="31f36-144"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31f36-144"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

