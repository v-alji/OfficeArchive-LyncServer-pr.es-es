---
title: 'Lync Server 2013: Configurar certificados para el proxy inverso'
description: 'Lync Server 2013: configurar certificados para el proxy inverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up certificates for the reverse proxy
ms:assetid: c03a08ec-a67b-4f11-b0d7-6677461beaaa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412938(v=OCS.15)
ms:contentKeyID: 48185291
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4b84241775bb3594840b68551048c01ff5faba2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441749"
---
# <a name="set-up-certificates-for-the-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="ae3a4-103">Configurar certificados para el proxy inverso en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae3a4-103">Set up certificates for the reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae3a4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae3a4-104">

<span> </span></span></span>

<span data-ttu-id="ae3a4-105">_**Última modificación del tema:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="ae3a4-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="ae3a4-106">Cada servidor proxy inverso requiere un certificado de servidor web para que lo use el servicio de escucha.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-106">Each reverse proxy server requires a web server certificate for use by the listening service.</span></span> <span data-ttu-id="ae3a4-107">El certificado de servidor Web debe ser emitido por una entidad de certificación (CA) pública.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-107">The web server certificate must be issued by a public certification authority (CA).</span></span>

<span data-ttu-id="ae3a4-108">Para obtener más información sobre este y otros requisitos de certificado, consulte [requisitos de certificados para el acceso de usuarios externos en Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="ae3a4-108">For details about this and other certificate requirements, see [Certificate requirements for external user access in Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span></span>

<div>

## <a name="to-set-up-a-web-services-certificate-for-the-reverse-proxy"></a><span data-ttu-id="ae3a4-109">Para configurar un certificado de servicios web para el proxy inverso</span><span class="sxs-lookup"><span data-stu-id="ae3a4-109">To set up a Web Services certificate for the reverse proxy</span></span>

  - <span data-ttu-id="ae3a4-110">Ya debe haber configurado su proxy inverso, incluyendo la configuración del certificado de servicios Web.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-110">You should have already set up your reverse proxy, including setting up the Web Services certificate.</span></span> <span data-ttu-id="ae3a4-111">Si no lo hizo antes de empezar la implementación de los servidores perimetrales, use los procedimientos de [configuración de los servidores proxy inversos para Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) para crear solicitudes e instalar el certificado de servicios web y, después, cree cada regla de publicación web y configúrela para usar el certificado.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-111">If you did not do so before starting your deployment of your Edge Servers, use the procedures in [Setting up reverse proxy servers for Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) to create request and install the Web Services certificate, and then create each web publishing rule and configure it to use the certificate.</span></span>

<span data-ttu-id="ae3a4-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae3a4-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

