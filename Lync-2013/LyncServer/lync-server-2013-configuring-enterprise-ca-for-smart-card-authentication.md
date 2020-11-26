---
title: 'Lync Server 2013: configuración de la CA de empresa para la autenticación de tarjetas inteligentes'
description: 'Lync Server 2013: configuración de la CA de empresa para la autenticación de tarjetas inteligentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise CA for smart card authentication
ms:assetid: c24e0891-e108-4cb6-9902-c6a4c8e68455
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308571(v=OCS.15)
ms:contentKeyID: 54973692
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98044c96dd04d02fd87609918f309cf65227b133
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433153"
---
# <a name="configuring-enterprise-ca-for-smart-card-authentication-in-lync-server-2013"></a><span data-ttu-id="7b4ae-103">Configuración de CA de empresa para la autenticación de tarjetas inteligentes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b4ae-103">Configuring Enterprise CA for smart card authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7b4ae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7b4ae-104">

<span> </span></span></span>

<span data-ttu-id="7b4ae-105">_**Última modificación del tema:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="7b4ae-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="7b4ae-106">En la sección siguiente se describe cómo configurar una entidad de certificación (CA) raíz de empresa para admitir la autenticación de tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-106">The following section describes how to configure an Enterprise Root Certification Authority (CA) to support smart card authentication.</span></span> <span data-ttu-id="7b4ae-107">Para obtener información sobre cómo instalar una entidad emisora de certificados raíz de empresa, vea instalar una entidad de certificación raíz de empresa en [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364) .</span><span class="sxs-lookup"><span data-stu-id="7b4ae-107">For information on how to install an Enterprise Root CA, see Install an Enterprise Root Certification Authority at [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364).</span></span>

<div>

## <a name="configuring-an-enterprise-root-certificate-authority-to-support-smart-card-authentication"></a><span data-ttu-id="7b4ae-108">Configurar una entidad emisora de certificados raíz de empresa para admitir la autenticación de tarjetas inteligentes</span><span class="sxs-lookup"><span data-stu-id="7b4ae-108">Configuring an Enterprise Root Certificate Authority to Support Smart Card Authentication</span></span>

<span data-ttu-id="7b4ae-109">En los siguientes pasos, se describe cómo configurar una CA raíz empresarial para admitir la autenticación de tarjeta inteligente:</span><span class="sxs-lookup"><span data-stu-id="7b4ae-109">The following steps describe how to configure an Enterprise Root CA to support Smart Card Authentication:</span></span>

1.  <span data-ttu-id="7b4ae-110">Inicie sesión en el equipo de la CA empresarial usando una cuenta de administrador de dominio.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-110">Log in to the Enterprise CA computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="7b4ae-111">Inicie el Administrador del sistema y compruebe que está instalado el rol Inscripción web de entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-111">Launch System Manager, and verify that the Certificate Authority Web Enrollment role is installed.</span></span>

3.  <span data-ttu-id="7b4ae-112">En el menú **Herramientas administrativas**, abra la consola de administración de **Entidad de certificación**.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-112">From the **Administrative Tools** menu, open the **Certification Authority** management console.</span></span>

4.  <span data-ttu-id="7b4ae-113">En el panel de navegación, expanda **Entidad de certificación**.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-113">In the Navigation pane, expand **Certification Authority**.</span></span>

5.  <span data-ttu-id="7b4ae-114">Haga clic con el botón derecho en **Plantillas de certificado**, elija **Nueva** y, luego, elija **Plantilla de certificado que se va a emitir**.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-114">Right click on **Certificate Templates**, select **New**, then select **Certificate Template to Issue**.</span></span>

6.  <span data-ttu-id="7b4ae-115">Elija **Enrollment Agent**, **Usuario de tarjeta inteligente** e **Inicio de sesión de Tarjeta inteligente**.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-115">Select **Enrollment Agent**, **Smartcard User**, and **Smartcard Logon**.</span></span>

7.  <span data-ttu-id="7b4ae-116">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-116">Click **OK**.</span></span>

8.  <span data-ttu-id="7b4ae-117">Haga clic con el botón derecho en **Plantillas de certificado**.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-117">Right click on **Certificate Templates**.</span></span>

9.  <span data-ttu-id="7b4ae-118">Elija **Administrar**.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-118">Select **Manage**.</span></span>

10. <span data-ttu-id="7b4ae-119">Abra las propiedades de la plantilla Usuario de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-119">Open the properties of the Smartcard User template.</span></span>

11. <span data-ttu-id="7b4ae-120">Haga clic en la pestaña **Seguridad**.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-120">Click on the **Security** tab.</span></span>

12. <span data-ttu-id="7b4ae-121">Cambie los permisos como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="7b4ae-121">Change the permissions as follows:</span></span>
    
      - <span data-ttu-id="7b4ae-122">Agregue cuentas de usuario individuales de AD con los permisos Leer/Inscribir (permitir), o</span><span class="sxs-lookup"><span data-stu-id="7b4ae-122">Add individual user AD accounts with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="7b4ae-123">Agregue un grupo de seguridad que contenga los usuarios de tarjeta inteligente con permisos Leer/Inscribir (permitir), o</span><span class="sxs-lookup"><span data-stu-id="7b4ae-123">Add a security group containing smart card users with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="7b4ae-124">Agregue el grupo Usuarios del dominio con los permisos Leer/Inscribir (permitir)</span><span class="sxs-lookup"><span data-stu-id="7b4ae-124">Add the Domain Users group with Read/Enroll (Allow) permissions</span></span>

<span data-ttu-id="7b4ae-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7b4ae-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

