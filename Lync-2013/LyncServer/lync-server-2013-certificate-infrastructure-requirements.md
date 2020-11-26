---
title: 'Lync Server 2013: Requisitos de la infraestructura de certificados'
description: Requisitos de la infraestructura de certificados de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate infrastructure requirements
ms:assetid: 0051aa23-0bbe-4e72-9f29-e01c6bcc6190
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398066(v=OCS.15)
ms:contentKeyID: 48183219
ms.date: 06/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02c7e69f272c29f0ba9386f403db326b4d39bbff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435414"
---
# <a name="certificate-infrastructure-requirements-for-lync-server-2013"></a><span data-ttu-id="ae907-103">Requisitos de la infraestructura de certificados para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae907-103">Certificate infrastructure requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae907-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae907-104">

<span> </span></span></span>

<span data-ttu-id="ae907-105">_**Última modificación del tema:** 2016-06-23_</span><span class="sxs-lookup"><span data-stu-id="ae907-105">_**Topic Last Modified:** 2016-06-23_</span></span>

<span data-ttu-id="ae907-106">Lync Server 2013 requiere una infraestructura de clave pública (PKI) para que sea compatible con las conexiones TLS y Mutual TLS (MTLS).</span><span class="sxs-lookup"><span data-stu-id="ae907-106">Lync Server 2013 requires a public key infrastructure (PKI) to support TLS and mutual TLS (MTLS) connections.</span></span>

<span data-ttu-id="ae907-107">Lync Server usa certificados para los siguientes fines:</span><span class="sxs-lookup"><span data-stu-id="ae907-107">Lync Server uses certificates for the following purposes:</span></span>

  - <span data-ttu-id="ae907-108">Conexiones TLS entre el cliente y el servidor</span><span class="sxs-lookup"><span data-stu-id="ae907-108">TLS connections between client and server</span></span>

  - <span data-ttu-id="ae907-109">Conexiones MTLS entre servidores</span><span class="sxs-lookup"><span data-stu-id="ae907-109">MTLS connections between servers</span></span>

  - <span data-ttu-id="ae907-110">Federación mediante la detección automática de asociados de DNS</span><span class="sxs-lookup"><span data-stu-id="ae907-110">Federation using automatic DNS discovery of partners</span></span>

  - <span data-ttu-id="ae907-111">Acceso de usuarios remotos a la mensajería instantánea (MI)</span><span class="sxs-lookup"><span data-stu-id="ae907-111">Remote user access for instant messaging (IM)</span></span>

  - <span data-ttu-id="ae907-112">Acceso de usuarios externos a sesiones de audio/vídeo (A/V), uso compartido de aplicaciones y conferencias</span><span class="sxs-lookup"><span data-stu-id="ae907-112">External user access to audio/video (A/V) sessions, application sharing, and conferencing</span></span>

  - <span data-ttu-id="ae907-113">Solicitudes de teléfono móvil con el descubrimiento automático de servicios Web</span><span class="sxs-lookup"><span data-stu-id="ae907-113">Mobile requests using automatic discovery of Web Services</span></span>

<span data-ttu-id="ae907-114">Para Lync Server, se aplican los siguientes requisitos comunes:</span><span class="sxs-lookup"><span data-stu-id="ae907-114">For Lync Server, the following common requirements apply:</span></span>

  - <span data-ttu-id="ae907-115">Todos los certificados de servidor deben admitir la autorización de servidor (EKU de servidor).</span><span class="sxs-lookup"><span data-stu-id="ae907-115">All server certificates must support server authorization (Server EKU).</span></span>

  - <span data-ttu-id="ae907-116">Todos los certificados de servidor deben contener un punto de distribución CRL (CDP).</span><span class="sxs-lookup"><span data-stu-id="ae907-116">All server certificates must contain a CRL Distribution Point (CDP).</span></span>

  - <span data-ttu-id="ae907-117">Todos los certificados deben estar firmados mediante un algoritmo de firma compatible con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ae907-117">All certificates must be signed using a signing algorithm supported by the operating system.</span></span> <span data-ttu-id="ae907-118">Lync Server 2013 admite el conjunto de tamaños de compendio SHA-1 y SHA-2 (224, 256, 384 y 512 bits), y cumple o supera los requisitos del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ae907-118">Lync Server 2013 supports the SHA-1 and SHA-2 suite of digest sizes (224, 256, 384 and 512-bit), and meets or exceeds the operating system requirements.</span></span> <span data-ttu-id="ae907-119">Para obtener asistencia sobre el sistema operativo, consulte [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002) .</span><span class="sxs-lookup"><span data-stu-id="ae907-119">For operating system support, see [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ae907-120">No está permitido usar el algoritmo de firma RSASSA-PSS, ya que podría dar lugar a errores en problemas relacionados con el inicio de sesión y el desvío de llamadas, entre otros. </span><span class="sxs-lookup"><span data-stu-id="ae907-120">Using the RSASSA-PSS signature algorithm is unsupported, and may lead to errors on login and call forwarding issues, among other problems.</span></span>

    
    </div>

  - <span data-ttu-id="ae907-121">La inscripción automática es compatible con los servidores internos que ejecutan Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ae907-121">Auto-enrollment is supported for internal servers running Lync Server.</span></span>

  - <span data-ttu-id="ae907-122">La inscripción automática no es compatible con los servidores perimetrales de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ae907-122">Auto-enrollment is not supported for Lync Server Edge Servers.</span></span>

  - <span data-ttu-id="ae907-123">Al enviar una solicitud de certificado basada en Web a una CA de Windows Server 2003, debe enviarla desde un equipo con Windows Server 2003 con SP2 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ae907-123">When you submit a web-based certificate request to a Windows Server 2003 CA, you must submit it from a computer running either Windows Server 2003 with SP2 or Windows XP.</span></span>
    
    <span data-ttu-id="ae907-124">Tenga en cuenta que, aunque KB922706 ofrece compatibilidad para resolver problemas con la inscripción de certificados Web en una inscripción Web de servicios de Certificate Server de Windows Server 2003, no permite usar Windows Server 2008, Windows Vista o Windows 7 para solicitar un certificado a una CA de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ae907-124">Note that although KB922706 provides support for resolving issues with enrolling web certificates against a Windows Server 2003 Certificate Services web enrollment, it does not make it possible to use Windows Server 2008, Windows Vista, or Windows 7 to request a certificate from a Windows Server 2003 CA.</span></span>

  - <span data-ttu-id="ae907-125">Se admiten longitudes de clave de cifrado de 1024, 2048 y 4096.</span><span class="sxs-lookup"><span data-stu-id="ae907-125">Encryption key lengths of 1024, 2048, and 4096 are supported.</span></span> <span data-ttu-id="ae907-126">Se recomienda usar longitudes de clave de 2048 y superiores.</span><span class="sxs-lookup"><span data-stu-id="ae907-126">Key lengths of 2048 and greater are recommended.</span></span>

  - <span data-ttu-id="ae907-127">El algoritmo de firma hash o implícito predeterminado es RSA.</span><span class="sxs-lookup"><span data-stu-id="ae907-127">The default digest, or hash signing, algorithm is RSA.</span></span> <span data-ttu-id="ae907-128">\_ \_ \_ También se admiten los algoritmos P256, ECDH P384 y P521 ECDH.</span><span class="sxs-lookup"><span data-stu-id="ae907-128">The ECDH\_P256, ECDH\_P384, and ECDH\_P521 algorithms are also supported.</span></span> 

<div>

## <a name="in-this-section"></a><span data-ttu-id="ae907-129">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ae907-129">In This Section</span></span>

  - [<span data-ttu-id="ae907-130">Requisitos de certificado para Servidores internos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae907-130">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="ae907-131">Requisitos de certificado para el acceso de usuarios externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae907-131">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="ae907-132">Requisitos de certificados para el servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae907-132">Certificate requirements for Persistent Chat server in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="ae907-133">Requisitos de certificado para movilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae907-133">Certificate requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-mobility.md)

<span data-ttu-id="ae907-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae907-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

