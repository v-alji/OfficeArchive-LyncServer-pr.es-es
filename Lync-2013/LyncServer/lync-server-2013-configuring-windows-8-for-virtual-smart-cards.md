---
title: 'Lync Server 2013: configuración de Windows 8 para tarjetas inteligentes virtuales'
description: 'Lync Server 2013: configuración de Windows 8 para tarjetas inteligentes virtuales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Windows 8 for Virtual Smart Cards
ms:assetid: 4916c167-4ee3-4f3e-b65c-33e588595112
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308564(v=OCS.15)
ms:contentKeyID: 54973684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 112047f91a20dd552c628fb33eba7bb9ad3d0f01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432320"
---
# <a name="configuring-windows-8-for-using-virtual-smart-cards-with-lync-server-2013"></a><span data-ttu-id="215b4-103">Configuración de Windows 8 para el uso de tarjetas inteligentes virtuales con Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="215b4-103">Configuring Windows 8 for using Virtual Smart Cards with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="215b4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="215b4-104">

<span> </span></span></span>

<span data-ttu-id="215b4-105">_**Última modificación del tema:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="215b4-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="215b4-106">Un factor que se necesita considerar al implementar la autenticación en dos fases y la tecnología de tarjetas inteligentes es el costo de la implementación.</span><span class="sxs-lookup"><span data-stu-id="215b4-106">One factor to consider when deploying two-factor authentication and smart card technology is the cost of implementation.</span></span> <span data-ttu-id="215b4-107">Windows 8 proporciona una serie de nuevas capacidades de seguridad y una de las características nuevas más interesantes es la compatibilidad con las tarjetas inteligentes virtuales.</span><span class="sxs-lookup"><span data-stu-id="215b4-107">Windows 8 provides a number of new security capabilities, and one of the most interesting new features is support for virtual smart cards.</span></span>

<span data-ttu-id="215b4-108">Para los equipos que vienen con el chip del Módulo de plataforma segura (TPM) que cumple la especificación versión 1.2, las organizaciones ahora pueden obtener beneficios del inicio de sesión con tarjeta inteligente sin hacer inversiones adicionales en hardware.</span><span class="sxs-lookup"><span data-stu-id="215b4-108">For computers equipped with a Trusted Platform Module (TPM) chip that meets specification version 1.2, organizations can now get the benefits of smart card logon without making any additional investments in hardware.</span></span> <span data-ttu-id="215b4-109">Para obtener más información, consulte uso de tarjetas inteligentes virtuales con Windows 8 en [https://go.microsoft.com/fwlink/p/?LinkId=313365](https://go.microsoft.com/fwlink/p/?linkid=313365) .</span><span class="sxs-lookup"><span data-stu-id="215b4-109">For more information, see Using Virtual Smart Cards with Windows 8 at [https://go.microsoft.com/fwlink/p/?LinkId=313365](https://go.microsoft.com/fwlink/p/?linkid=313365).</span></span>

<div>

## <a name="to-configure-windows-8-for-virtual-smart-cards"></a><span data-ttu-id="215b4-110">Para configurar Windows 8 para las tarjetas inteligentes virtuales</span><span class="sxs-lookup"><span data-stu-id="215b4-110">To Configure Windows 8 for Virtual Smart Cards</span></span>

1.  <span data-ttu-id="215b4-111">Inicie sesión en el equipo con Windows 8 con las credenciales de un usuario habilitado para Lync.</span><span class="sxs-lookup"><span data-stu-id="215b4-111">Log in to the Windows 8 computer using the credentials of a Lync-enabled user.</span></span>

2.  <span data-ttu-id="215b4-112">En la pantalla de inicio de Windows 8, mueva el cursor a la esquina inferior derecha de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="215b4-112">At the Windows 8 Start screen, move your cursor to the bottom right corner of the screen.</span></span>

3.  <span data-ttu-id="215b4-113">Seleccione la opción **Buscar** y, luego, busque **Command Prompt**.</span><span class="sxs-lookup"><span data-stu-id="215b4-113">Select the **Search** option, and then search for **Command Prompt**.</span></span>

4.  <span data-ttu-id="215b4-114">Haga clic con el botón derecho en **Símbolo del sistema** y, luego, seleccione **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="215b4-114">Right click on **Command Prompt**, and then select **Run as Administrator**.</span></span>

5.  <span data-ttu-id="215b4-115">Abra la consola de administración del Módulo de plataforma segura (TPM) ejecutando el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="215b4-115">Open the Trusted Platform Module (TPM) Management console by running the following command:</span></span>
    
        Tpm.msc

6.  <span data-ttu-id="215b4-116">Desde la consola de administración de TPM, compruebe que la versión de la especificación de TPM sea al menos 1.2</span><span class="sxs-lookup"><span data-stu-id="215b4-116">From the TPM management console, verify that your TPM specification version is at least 1.2</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="215b4-117">Si recibe un diálogo que indique que no se encuentra un Módulo de plataforma segura (TPM) compatible, compruebe que el equipo tenga un módulo TPM compatible y que esté habilitado en el sistema BIOS.</span><span class="sxs-lookup"><span data-stu-id="215b4-117">If you receive a dialog stating that a Compatible Trust Platform Module (TPM) cannot be found, verify that the computer has a compatible TPM module and that it is enabled in the system BIOS.</span></span>

    
    </div>

7.  <span data-ttu-id="215b4-118">Cierre la consola de administración de TPM</span><span class="sxs-lookup"><span data-stu-id="215b4-118">Close the TPM management console</span></span>

8.  <span data-ttu-id="215b4-119">Desde el símbolo del sistema, cree una tarjeta inteligente virtual por medio del siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="215b4-119">From the command prompt, create a new virtual smart card using the following command:</span></span>
    
        TpmVscMgr create /name MyVSC /pin default /adminkey random /generate
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="215b4-120">Para proporcionar un valor PIN personalizado al crear la tarjeta inteligente virtual, use en su lugar la solicitud de PIN.</span><span class="sxs-lookup"><span data-stu-id="215b4-120">To provide a custom PIN value when creating the virtual smart card, use /pin prompt instead.</span></span>

    
    </div>

9.  <span data-ttu-id="215b4-121">Desde el símbolo del sistema, abra la consola de administración del equipo ejecutando el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="215b4-121">From the command prompt, open the Computer Management console by running the following command:</span></span>
    
        CompMgmt.msc

10. <span data-ttu-id="215b4-122">En la consola de administración del equipo, seleccione **Administración de dispositivos**.</span><span class="sxs-lookup"><span data-stu-id="215b4-122">In the Computer Management console, select **Device Management**.</span></span>

11. <span data-ttu-id="215b4-123">Expanda **Lectores de tarjetas inteligentes**.</span><span class="sxs-lookup"><span data-stu-id="215b4-123">Expand **Smart card readers**.</span></span>

12. <span data-ttu-id="215b4-124">Compruebe que el nuevo lector de tarjetas inteligentes virtuales se haya creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="215b4-124">Verify that the new virtual smart card reader has been created successfully.</span></span>

<span data-ttu-id="215b4-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="215b4-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

