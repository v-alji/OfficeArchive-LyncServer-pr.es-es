---
title: 'Lync Server 2013: marco de seguridad para Lync Server'
description: 'Lync Server 2013: marco de seguridad de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Security framework for Lync Server 2013
ms:assetid: 01131e28-b38e-40d9-8524-06725b9c6608
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481316(v=OCS.15)
ms:contentKeyID: 59893866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d30c26929ddedbf653abd1fc353b6873ad8f36f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441903"
---
# <a name="security-framework-for-lync-server-2013"></a><span data-ttu-id="af8f0-103">Marco de seguridad para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af8f0-103">Security framework for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af8f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af8f0-104">

<span> </span></span></span>

<span data-ttu-id="af8f0-105">_**Última modificación del tema:** 2013-11-08_</span><span class="sxs-lookup"><span data-stu-id="af8f0-105">_**Topic Last Modified:** 2013-11-08_</span></span>

<span data-ttu-id="af8f0-106">Esta sección proporciona una descripción general de los elementos fundamentales que forman el marco de seguridad de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="af8f0-106">This section provides an overview of the fundamental elements that form the security framework for Microsoft Lync Server 2013.</span></span> <span data-ttu-id="af8f0-107">Comprender el funcionamiento conjunto de estos elementos es esencial para tomar decisiones fundamentadas sobre la seguridad de su implementación particular de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="af8f0-107">Understanding how these elements work together is essential to making informed decisions about securing your particular Lync Server 2013 deployment.</span></span>

<span data-ttu-id="af8f0-108">Dichos elementos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="af8f0-108">These elements are as follows:</span></span>

  - <span data-ttu-id="af8f0-109">Los servicios de dominio de Active Directory (AD DS) proporcionan un único repositorio de back-end de confianza para cuentas de usuario y recursos de red.</span><span class="sxs-lookup"><span data-stu-id="af8f0-109">Active Directory Domain Services (AD DS) provides a single trusted back-end repository for user accounts and network resources.</span></span>

  - <span data-ttu-id="af8f0-110">El control de acceso basado en roles (RBAC) le permite delegar tareas administrativas y mantener, al mismo tiempo, altos estándares de seguridad.</span><span class="sxs-lookup"><span data-stu-id="af8f0-110">Role-Based Access Control (RBAC) enables you to delegate administrative tasks while maintaining high standards for security.</span></span>

  - <span data-ttu-id="af8f0-111">La infraestructura de clave pública (PKI) utiliza certificados emitidos por entidades de certificación (CA) de confianza para autenticar los servidores y garantizar la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="af8f0-111">Public Key Infrastructure (PKI) uses certificates issued by trusted certification authorities (CAs) to authenticate servers and ensure data integrity.</span></span>

  - <span data-ttu-id="af8f0-p102">La Seguridad de la capa de transporte (TLS), HTTPS sobre SSL (HTTPS) y Mutual TLS (MTLS) permiten la autenticación de los extremos y el cifrado de la mensajería instantánea. Las secuencias de audio, vídeo y uso compartido de aplicaciones punto a punto se cifran con el protocolo de transporte seguro en tiempo real (SRTP).</span><span class="sxs-lookup"><span data-stu-id="af8f0-p102">Transport Layer Security (TLS), HTTPS over SSL (HTTPS), and mutual TLS (MTLS) enable endpoint authentication and IM encryption. Point-to-point audio, video, and application sharing streams are encrypted using Secure Real-Time Transport Protocol (SRTP).</span></span>

  - <span data-ttu-id="af8f0-114">Para la autenticación del usuario se usan los protocolos estándar de la industria, siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="af8f0-114">Industry-standard protocols for user authentication, where possible.</span></span>

  - <span data-ttu-id="af8f0-115">Windows PowerShell ofrece características de seguridad que están habilitadas de forma predeterminada para que los usuarios no puedan ejecutar scripts con facilidad o sin problemas.</span><span class="sxs-lookup"><span data-stu-id="af8f0-115">Windows PowerShell provides security features that are enabled by default so that users cannot easily or unknowingly run scripts.</span></span>

<span data-ttu-id="af8f0-116">Estos elementos de seguridad fundamentales funcionan conjuntamente para definir usuarios, servidores, conexiones y operaciones de confianza para ayudar a garantizar una base segura para Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="af8f0-116">These fundamental security elements work together to define trusted users, servers, connections, and operations to help ensure a secure foundation for Lync Server 2013.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="af8f0-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="af8f0-117">In This Section</span></span>

<span data-ttu-id="af8f0-118">Los temas de esta sección describen cómo funciona cada uno de estos elementos fundamentales para mejorar la seguridad de su infraestructura de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="af8f0-118">The topics in this section describe how each of these fundamental elements works to enhance the security of your Lync Server infrastructure.</span></span>

  - [<span data-ttu-id="af8f0-119">Servicios de dominio de Active Directory para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af8f0-119">Active Directory Domain Services for Lync Server 2013</span></span>](lync-server-2013-active-directory-domain-services-for-lync-server.md)

  - [<span data-ttu-id="af8f0-120">Control de acceso basado en roles (RBAC) para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af8f0-120">Role-based access control (RBAC) for Lync Server 2013</span></span>](lync-server-2013-role-based-access-control-rbac.md)

  - [<span data-ttu-id="af8f0-121">Infraestructura de clave pública para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af8f0-121">Public Key Infrastructure for Lync Server 2013</span></span>](lync-server-2013-public-key-infrastructure.md)

  - [<span data-ttu-id="af8f0-122">TLS y MTLS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af8f0-122">TLS and MTLS for Lync Server 2013</span></span>](lync-server-2013-tls-and-mtls.md)

  - [<span data-ttu-id="af8f0-123">Cifrado para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af8f0-123">Encryption for Lync Server 2013</span></span>](lync-server-2013-encryption.md)

  - [<span data-ttu-id="af8f0-124">Autenticación de usuarios y clientes para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af8f0-124">User and client authentication for Lync Server 2013</span></span>](lync-server-2013-user-and-client-authentication.md)

  - [<span data-ttu-id="af8f0-125">Herramientas de administración de Windows PowerShell y Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af8f0-125">Windows PowerShell and Lync Server 2013 management tools</span></span>](lync-server-2013-windows-powershell-and-lync-server-management-tools.md)

<span data-ttu-id="af8f0-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af8f0-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

