---
title: Instalar el paquete de compatibilidad con versiones anteriores de WMI
description: Instalar el paquete de compatibilidad con versiones anteriores de WMI.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Install WMI Backward Compatibility package
ms:assetid: 38797fbd-06a0-4008-b099-158e7b5d7703
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204816(v=OCS.15)
ms:contentKeyID: 48183893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9062e209981fd180b8772801960bd94d2256513a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439585"
---
# <a name="install-wmi-backward-compatibility-package"></a><span data-ttu-id="ddd9f-103">Instalar el paquete de compatibilidad con versiones anteriores de WMI</span><span class="sxs-lookup"><span data-stu-id="ddd9f-103">Install WMI Backward Compatibility package</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ddd9f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ddd9f-104">

<span> </span></span></span>

<span data-ttu-id="ddd9f-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="ddd9f-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="ddd9f-106">Si intenta ejecutar el Asistente para la combinación del generador de topología sin instalar el paquete de compatibilidad con versiones anteriores de WMI, verá el siguiente error:</span><span class="sxs-lookup"><span data-stu-id="ddd9f-106">If you attempt to run the Topology Builder Merge wizard without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="ddd9f-107">![Mensaje de error de WMI](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "Mensaje de error de WMI")</span><span class="sxs-lookup"><span data-stu-id="ddd9f-107">![WMI error message](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "WMI error message")</span></span>

<span data-ttu-id="ddd9f-108">Si intenta ejecutar el cmdlet **Merge-CsLegacytopology** sin instalar el paquete de compatibilidad con versiones anteriores de WMI, verá el siguiente error:</span><span class="sxs-lookup"><span data-stu-id="ddd9f-108">If you attempt to run the **Merge-CsLegacytopology** cmdlet without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="ddd9f-109">![Error del proveedor WMI de Windows PowerShell](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Error del proveedor WMI de Windows PowerShell")</span><span class="sxs-lookup"><span data-stu-id="ddd9f-109">![Windows PowerShell WMI Provider Error](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Windows PowerShell WMI Provider Error")</span></span>

<span data-ttu-id="ddd9f-110">Para instalar el paquete de compatibilidad con versiones anteriores de WMI</span><span class="sxs-lookup"><span data-stu-id="ddd9f-110">To install the WMI Backward Compatibility Package</span></span>

1.  <span data-ttu-id="ddd9f-111">Desde los medios de instalación, vaya a configuración de instalación de \\ \\ AMD64 \\ \\OCSWMIBC.MSI.</span><span class="sxs-lookup"><span data-stu-id="ddd9f-111">From your installation media, navigate to \\SETUP\\AMD64\\SETUP\\OCSWMIBC.MSI.</span></span>

2.  <span data-ttu-id="ddd9f-112">Instalar OCSWMIBC.MSI.</span><span class="sxs-lookup"><span data-stu-id="ddd9f-112">Install OCSWMIBC.MSI.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="ddd9f-113">OCSWMIBC.msi debe instalarse en el equipo en el que se ejecuta el Asistente para la combinación del generador de topología.</span><span class="sxs-lookup"><span data-stu-id="ddd9f-113">OCSWMIBC.msi must be installed on the computer where the Topology Builder Merge wizard is run.</span></span> <span data-ttu-id="ddd9f-114">Sin embargo, le recomendamos que instale OCSWMIBC.msi en todos los servidores front-end de su topología.</span><span class="sxs-lookup"><span data-stu-id="ddd9f-114">However, we recommend installing OCSWMIBC.msi on all Front End servers in your topology.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="ddd9f-115">OCSWMIBC.msi se puede instalar en cualquier equipo del dominio que tenga instalados los componentes principales de Lync Server 2013 y el shell de administración de Lync Server 2013, y tiene acceso a la topología de Office Communications Server 2007 R2 (proveedor WMI a servicios de dominio de Active Directory (AD DS) y a SQL Server).</span><span class="sxs-lookup"><span data-stu-id="ddd9f-115">OCSWMIBC.msi can be installed on any computer in the domain that has the Lync Server 2013 Core Components and the Lync Server 2013 Management Shell installed, and has access to the Office Communications Server 2007 R2 topology (WMI provider to Active Directory Domain Services (AD DS) and SQL Server).</span></span>

    
    <span data-ttu-id="ddd9f-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ddd9f-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

