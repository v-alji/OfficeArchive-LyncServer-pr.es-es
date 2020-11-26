---
title: 'Lync Server 2013: Requisitos técnicos para la aplicación Anuncio'
description: 'Lync Server 2013: requisitos técnicos para la aplicación de anuncios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for the Announcement application
ms:assetid: fbd8c204-3765-4b22-a0c9-a781b5126366
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205413(v=OCS.15)
ms:contentKeyID: 48185944
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: adc5019408b79301bbcda3993ceb7d96ee4d9b7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444311"
---
# <a name="technical-requirements-for-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="f8173-103">Requisitos técnicos para la aplicación Anuncio en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8173-103">Technical requirements for the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8173-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8173-104">

<span> </span></span></span>

<span data-ttu-id="f8173-105">_**Última modificación del tema:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="f8173-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="f8173-106">En esta sección se describen los siguientes requisitos técnicos para la aplicación de anuncios:</span><span class="sxs-lookup"><span data-stu-id="f8173-106">This section describes the following technical requirements for the Announcement application:</span></span>

  - <span data-ttu-id="f8173-107">Requisitos de hardware</span><span class="sxs-lookup"><span data-stu-id="f8173-107">Hardware requirements</span></span>

  - <span data-ttu-id="f8173-108">Requisitos de software</span><span class="sxs-lookup"><span data-stu-id="f8173-108">Software requirements</span></span>

  - <span data-ttu-id="f8173-109">Requisitos de los puertos</span><span class="sxs-lookup"><span data-stu-id="f8173-109">Port requirements</span></span>

  - <span data-ttu-id="f8173-110">Requisitos de los archivos de audio</span><span class="sxs-lookup"><span data-stu-id="f8173-110">Audio file requirements</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="f8173-111">Requisitos de hardware</span><span class="sxs-lookup"><span data-stu-id="f8173-111">Hardware Requirements</span></span>

<span data-ttu-id="f8173-112">La aplicación de anuncios tiene los mismos requisitos de hardware que los servidores de aplicaciones para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f8173-112">The Announcement application has the same hardware requirements as Front End Servers.</span></span> <span data-ttu-id="f8173-113">Para obtener más información sobre los requisitos de hardware, vea [plataformas de hardware de servidor para Lync Server 2013](lync-server-2013-server-hardware-platforms.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="f8173-113">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="f8173-114">Requisitos de software</span><span class="sxs-lookup"><span data-stu-id="f8173-114">Software Requirements</span></span>

<span data-ttu-id="f8173-115">La aplicación de anuncios tiene los mismos requisitos del sistema operativo y requisitos previos de software que los servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="f8173-115">The Announcement application has the same operating system requirements and software prerequisites as Front End Servers.</span></span> <span data-ttu-id="f8173-116">Para obtener más información sobre los requisitos de software, vea [compatibilidad del sistema operativo servidor y herramientas en Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) en la documentación de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="f8173-116">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="f8173-117">Todos los servidores front-end o los servidores Standard Edition que ejecuten la aplicación de anuncio deben tener instalado el Windows Media Format Runtime para servidores que ejecuten Windows Server 2008 R2 o Microsoft Media Foundation para servidores que ejecuten Windows Server 2012 o Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="f8173-117">All Front End Servers or Standard Edition servers that run the Announcement application must have the Windows Media Format Runtime installed for servers running Windows Server 2008 R2, or Microsoft Media Foundation for servers running Windows Server 2012 or Windows Server 2012 R2.</span></span> <span data-ttu-id="f8173-118">En Windows Server 2008 R2, Windows Media Format Runtime se instala como parte de la experiencia de escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="f8173-118">For Windows Server 2008 R2, the Windows Media Format Runtime is installed as part of Windows Desktop Experience.</span></span> <span data-ttu-id="f8173-119">Se necesita Windows Media Format Runtime o Microsoft Media Foundation para los archivos de audio de Windows Media (. WMA) que la aplicación del anuncio reproduce para los anuncios y la música.</span><span class="sxs-lookup"><span data-stu-id="f8173-119">Windows Media Format Runtime or Microsoft Media Foundation is required for Windows Media Audio (.wma) files that the Announcement application plays for announcements and music.</span></span>

</div>

<div>

## <a name="port-requirements"></a><span data-ttu-id="f8173-120">Requisitos de los puertos</span><span class="sxs-lookup"><span data-stu-id="f8173-120">Port Requirements</span></span>

<span data-ttu-id="f8173-121">La aplicación de anuncios usa el siguiente puerto:</span><span class="sxs-lookup"><span data-stu-id="f8173-121">The Announcement application uses the following port:</span></span>

  - <span data-ttu-id="f8173-122">**Puerto 5071** Se utiliza para solicitudes de escucha SIP</span><span class="sxs-lookup"><span data-stu-id="f8173-122">**Port 5071**   Used for SIP listening requests</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f8173-123">Este puerto es el predeterminado, pero puedes cambiarlo utilizando el cmdlet <STRONG>Set-CsApplicationServer</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f8173-123">This port is the default setting, which you can change by using the <STRONG>Set-CsApplicationServer</STRONG> cmdlet.</span></span> <span data-ttu-id="f8173-124">Para obtener más información sobre este cmdlet, consulte la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f8173-124">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>



</div>

</div>

<div>

## <a name="audio-file-requirements"></a><span data-ttu-id="f8173-125">Requisitos de archivos de audio</span><span class="sxs-lookup"><span data-stu-id="f8173-125">Audio File Requirements</span></span>

<span data-ttu-id="f8173-126">La aplicación de anuncios admite el formato de archivo de onda (. wav) y el formato de archivo de audio de Windows Media (. WMA) para música y anuncios.</span><span class="sxs-lookup"><span data-stu-id="f8173-126">The Announcement application supports Wave (.wav) file format and Windows Media audio (.wma) file format for music and announcements.</span></span> <span data-ttu-id="f8173-127">Los requisitos de los archivos de audio para la aplicación de anuncios son los mismos que los de la aplicación de grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8173-127">Audio file requirements for the Announcement application are the same as for the Response Group application.</span></span> <span data-ttu-id="f8173-128">Para obtener más información, consulte [requisitos técnicos para el grupo de respuesta en Lync Server 2013](lync-server-2013-technical-requirements-for-response-group.md).</span><span class="sxs-lookup"><span data-stu-id="f8173-128">For details, see [Technical requirements for Response Group in Lync Server 2013](lync-server-2013-technical-requirements-for-response-group.md).</span></span>

<span data-ttu-id="f8173-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8173-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

