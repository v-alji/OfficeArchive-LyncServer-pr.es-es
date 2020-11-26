---
title: Requisitos previos
description: Requisitos previos.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prerequisites
ms:assetid: 48016bea-be3b-4ba5-8df8-d8ad4d9243d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945592(v=OCS.15)
ms:contentKeyID: 51541417
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 936e52961539ed57fe1b610d42fb1c9cf35589b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446414"
---
# <a name="prerequisites"></a><span data-ttu-id="de53f-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="de53f-103">Prerequisites</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de53f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de53f-104">

<span> </span></span></span>

<span data-ttu-id="de53f-105">_**Última modificación del tema:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="de53f-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="de53f-106">Existen diversos requisitos de hardware, software y configuración del sistema que necesitará para ejecutar la herramienta Lync Server 2013 stress and performance.</span><span class="sxs-lookup"><span data-stu-id="de53f-106">There are various hardware, software, and system configuration requirements that you’ll need to run the Lync Server 2013 Stress and Performance Tool.</span></span>

<div>

## <a name="client-hardware-requirements"></a><span data-ttu-id="de53f-107">Requisitos de hardware del cliente</span><span class="sxs-lookup"><span data-stu-id="de53f-107">Client Hardware Requirements</span></span>

<span data-ttu-id="de53f-108">Para ejecutar la herramienta Lync Server 2013 de estrés y rendimiento en la implementación de Lync Server 2013, por cada 4.500 usuarios cuya carga desee simular, necesitará al menos un equipo dedicado que cumpla los siguientes requisitos mínimos de hardware:</span><span class="sxs-lookup"><span data-stu-id="de53f-108">To run the Lync Server 2013 Stress and Performance Tool on your Lync Server 2013 deployment, for every 4,500 users whose load you want to simulate, you’ll need at least one dedicated computer that meets the following minimum hardware requirements:</span></span>

  - <span data-ttu-id="de53f-109">Adaptador de red de 1 gigabit</span><span class="sxs-lookup"><span data-stu-id="de53f-109">1 gigabit network adapter</span></span>

  - <span data-ttu-id="de53f-110">8 GB de RAM</span><span class="sxs-lookup"><span data-stu-id="de53f-110">8-GB ram</span></span>

  - <span data-ttu-id="de53f-111">2 unidades de procesamiento central (CPU) de doble núcleo</span><span class="sxs-lookup"><span data-stu-id="de53f-111">2 dual-core central processing units (CPUs)</span></span>

</div>

<div>

## <a name="client-software-requirements"></a><span data-ttu-id="de53f-112">Requisitos de software de cliente</span><span class="sxs-lookup"><span data-stu-id="de53f-112">Client Software Requirements</span></span>

<span data-ttu-id="de53f-113">Para ejecutar la herramienta Lync Server 2013 stress and performance en la implementación de Lync Server 2013, los sistemas operativos compatibles son:</span><span class="sxs-lookup"><span data-stu-id="de53f-113">To run the Lync Server 2013 Stress and Performance Tool on your Lync Server 2013 deployment, the supported operating systems are:</span></span>

  - <span data-ttu-id="de53f-114">Sistema operativo Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de53f-114">Windows Server 2012 operating system</span></span>

  - <span data-ttu-id="de53f-115">Sistema operativo Windows Server 2008 (edición de 64 bits)</span><span class="sxs-lookup"><span data-stu-id="de53f-115">Windows Server 2008 operating system (64-bit edition)</span></span>

<span data-ttu-id="de53f-116">El equipo cliente debe cumplir con los siguientes requisitos de software:</span><span class="sxs-lookup"><span data-stu-id="de53f-116">Your client computer must meet the following software requirements:</span></span>

  - <span data-ttu-id="de53f-117">Debe tener instalado el motor en tiempo de ejecución de [Microsoft .NET Framework 4,5](https://go.microsoft.com/fwlink/?linkid=143212) .</span><span class="sxs-lookup"><span data-stu-id="de53f-117">You must have the [Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?linkid=143212) runtime installed.</span></span>

  - <span data-ttu-id="de53f-118">En Windows Server 2008/Windows Server 2012, la característica de experiencia de escritorio debe estar habilitada.</span><span class="sxs-lookup"><span data-stu-id="de53f-118">On Windows Server 2008/Windows Server 2012, the Desktop Experience feature must be enabled.</span></span>

  - <span data-ttu-id="de53f-119">Debe tener instalado el [paquete redistribuible de Microsoft Visual C++ 2012](https://go.microsoft.com/fwlink/?linkid=143216) (x64).</span><span class="sxs-lookup"><span data-stu-id="de53f-119">You must have the [Microsoft Visual C++ 2012 redistributable package](https://go.microsoft.com/fwlink/?linkid=143216) (x64) installed.</span></span>

  - <span data-ttu-id="de53f-120">Una implementación de Lync Server 2013 totalmente configurada.</span><span class="sxs-lookup"><span data-stu-id="de53f-120">A fully configured Lync Server 2013 deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="de53f-121">Las bibliotecas de la API administrada de comunicaciones unificadas de Microsoft (UCMA) 4,0 se incluyen en el paquete de instalación, de modo que UCMA no es necesario y no debe instalarse en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="de53f-121">Microsoft Unified Communications Managed API (UCMA) 4.0 libraries are included in the installation package, so UCMA is not required and should not be installed on client computers.</span></span>



</div>

</div>

<div>

## <a name="configuration-requirements"></a><span data-ttu-id="de53f-122">Requisitos de configuración</span><span class="sxs-lookup"><span data-stu-id="de53f-122">Configuration Requirements</span></span>

<span data-ttu-id="de53f-123">Los equipos que ejecutarán la herramienta de estrés y rendimiento de Lync Server 2013 deben estar configurados de acuerdo con los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="de53f-123">The computers that will run the Lync Server 2013 Stress and Performance Tool must be configured according to the following requirements:</span></span>

1.  <span data-ttu-id="de53f-124">Debe haber iniciado sesión como miembro del grupo de administradores locales o de dominio.</span><span class="sxs-lookup"><span data-stu-id="de53f-124">You must be logged on as a member of the Domain or Local Admins group.</span></span>

2.  <span data-ttu-id="de53f-125">La herramienta de estrés y rendimiento de Lync Server 2013 (LyncPerfTool.exe) no se puede ejecutar en un equipo que también ejecute componentes de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="de53f-125">Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe) cannot be run on a computer that is also running Lync Server 2013 components.</span></span>

3.  <span data-ttu-id="de53f-126">Debe ejecutar la herramienta de creación de usuarios de Lync Server 2013 (UserProvisioningTool.exe) en el servidor front-end o en el servidor Standard Edition donde residirán las cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="de53f-126">You must run the Lync Server 2013 User Creation tool (UserProvisioningTool.exe) on the Front End Server or on the Standard Edition server where the user accounts will reside.</span></span> <span data-ttu-id="de53f-127">Cuando la herramienta se ejecuta varias veces, cada usuario habilitado para las comunicaciones unificadas de Microsoft debe tener un número de teléfono único.</span><span class="sxs-lookup"><span data-stu-id="de53f-127">When the tool is run multiple times, each user who is enabled for Microsoft Unified Communications must have a unique phone number.</span></span>

4.  <span data-ttu-id="de53f-128">El tamaño del archivo de paginación debe ser administrado por el sistema o debe ser al menos 1,5 veces la cantidad de RAM del sistema.</span><span class="sxs-lookup"><span data-stu-id="de53f-128">The page file size should be system-managed, or should be at least 1.5 times the amount of RAM on the system.</span></span>

<span data-ttu-id="de53f-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de53f-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

