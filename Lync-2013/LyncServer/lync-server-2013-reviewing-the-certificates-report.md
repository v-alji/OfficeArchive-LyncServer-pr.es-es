---
title: 'Lync Server 2013: revisar el informe certificados'
description: 'Lync Server 2013: revisar el informe certificados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reviewing the Certificates Report
ms:assetid: 549cfc9b-3cc5-4483-a93c-fc0738c7f622
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558651(v=OCS.15)
ms:contentKeyID: 51541477
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2133e2f70c78217788d84251c2035a9115bc3283
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442460"
---
# <a name="reviewing-the-certificates-report-in-lync-server-2013"></a><span data-ttu-id="9bb10-103">Revisar el informe de certificados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9bb10-103">Reviewing the Certificates Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9bb10-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9bb10-104">

<span> </span></span></span>

<span data-ttu-id="9bb10-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="9bb10-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="9bb10-106">El informe certificados contiene todos los certificados necesarios en la implementación recomendada de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9bb10-106">The Certificates Report contains all certificates that are required in the recommended Lync Server 2013 deployment.</span></span> <span data-ttu-id="9bb10-107">La herramienta de planeación cuenta con los nombres de asunto y los nombres alternativos de asunto que se escriben.</span><span class="sxs-lookup"><span data-stu-id="9bb10-107">The Planning Tool accounts for the subject names and subject alternative names that are entered.</span></span> <span data-ttu-id="9bb10-108">El texto predeterminado que se deja sin editar puede representar un posible desafío para el equipo responsable de solicitar y emitir los certificados.</span><span class="sxs-lookup"><span data-stu-id="9bb10-108">Default text that is left unedited may represent a potential challenge for the team responsible for requesting and issuing the certificates.</span></span> <span data-ttu-id="9bb10-109">La información del certificado también contiene datos sobre el origen desde el cual puede emitirse normalmente el certificado.</span><span class="sxs-lookup"><span data-stu-id="9bb10-109">Certificate information also contains information about where the certificate can typically be issued from.</span></span> <span data-ttu-id="9bb10-110">Si la infraestructura no dispone de una infraestructura de clave pública (PKI) interna, todos los certificados se pueden solicitar a través de un proveedor de certificados público.</span><span class="sxs-lookup"><span data-stu-id="9bb10-110">If the infrastructure does not have an internal public key infrastructure (PKI) in place, all certificates can be requested through a public certificate provider.</span></span> <span data-ttu-id="9bb10-111">Los campos “Uso mejorado de clave (EKU)” y “Asignar a” del informe son muy útiles para comprender el objetivo y la ubicación de cada certificado.</span><span class="sxs-lookup"><span data-stu-id="9bb10-111">Extended key usages (EKU) and Assign To fields in the report are very helpful in understanding what the purpose and location for each certificate should be.</span></span>

<span data-ttu-id="9bb10-112">![Informe de administración de certificados](images/Gg558651.63a29335-d9e4-41ae-97ec-3c9d9fd30d8a(OCS.15).jpg "Informe de administración de certificados")</span><span class="sxs-lookup"><span data-stu-id="9bb10-112">![Certificates Admin Report](images/Gg558651.63a29335-d9e4-41ae-97ec-3c9d9fd30d8a(OCS.15).jpg "Certificates Admin Report")</span></span>

<span data-ttu-id="9bb10-113">Revise con atención y comprenda completamente el uso y el propósito de cada certificado de la implementación.</span><span class="sxs-lookup"><span data-stu-id="9bb10-113">Carefully review, and be sure to understand, the use and purpose of each certificate in the deployment.</span></span> <span data-ttu-id="9bb10-114">Si tiene alguna pregunta acerca de la función de un certificado, determine los elementos con los que se comunica un servidor o servicio.</span><span class="sxs-lookup"><span data-stu-id="9bb10-114">If there is a question about what a certificate does, determine which server or service is talking to what.</span></span> <span data-ttu-id="9bb10-115">Los certificados de Lync Server 2013 se usan para dos propósitos principales:</span><span class="sxs-lookup"><span data-stu-id="9bb10-115">Certificates in Lync Server 2013 are used for two primary purposes:</span></span>

  - <span data-ttu-id="9bb10-p103">Seguridad de la capa de transporte mutua (MTLS): los equipos que participan en la comunicación presentan un certificado que prueba su identidad al otro equipo; esto se conoce como autenticación del servidor. La comunicación no puede comenzar hasta que ambos equipos confíen mutuamente en la identidad del otro.</span><span class="sxs-lookup"><span data-stu-id="9bb10-p103">Mutual Transport Layer Security (MTLS) – The computers involved in the communication each present a certificate that proves their identity to another computer. This is known as server authentication. Communication cannot begin until each computer trusts the other computer’s identity.</span></span>

  - <span data-ttu-id="9bb10-119">Cifrado: el cifrado (Capa de sockets seguros, o SSL, y Seguridad de la capa de transporte, o TLS) es un medio fundamental para proteger las comunicaciones y la privacidad, así como para crear comunicaciones de confianza y un sistema de colaboración.</span><span class="sxs-lookup"><span data-stu-id="9bb10-119">Encryption – Encryption (Secure Sockets Layer, or SSL, and Transport Layer Security, or TLS) is a critical means to help secure communications, help ensure privacy, and to create a trusted communications and collaboration system.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="9bb10-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bb10-120">See Also</span></span>


[<span data-ttu-id="9bb10-121">Revisión de los informes del administrador en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9bb10-121">Reviewing the Administrator Reports in Lync Server 2013</span></span>](lync-server-2013-reviewing-the-administrator-reports.md)  
  

<span data-ttu-id="9bb10-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9bb10-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

