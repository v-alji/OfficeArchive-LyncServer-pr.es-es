---
title: Configuración de la calidad de servicio en dispositivos Microsoft Lync Phone Edition
description: Configuración de la calidad de servicio en dispositivos Microsoft Lync Phone Edition.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Quality of Service on Microsoft Lync Phone Edition devices
ms:assetid: a6eb2620-a512-4ab6-bdfd-eb76be43bbfe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205137(v=OCS.15)
ms:contentKeyID: 48185004
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c0d1e4f10c6b4a550f5da25f8bd2e9fe97606255
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432705"
---
# <a name="configuring-quality-of-service-on-microsoft-lync-phone-edition-devices-in-lync-server-2013"></a><span data-ttu-id="8b99d-103">Configuración de la calidad de servicio en los dispositivos Microsoft Lync Phone Edition en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b99d-103">Configuring Quality of Service on Microsoft Lync Phone Edition devices in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b99d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b99d-104">

<span> </span></span></span>

<span data-ttu-id="8b99d-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="8b99d-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="8b99d-106">Aunque la calidad de servicio (QoS) no está habilitada de forma predeterminada en dispositivos como iPhone, QoS está habilitado de forma predeterminada para los dispositivos que ejecutan Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="8b99d-106">Although Quality of Service (QoS) is not enabled by default for devices such as iPhones, QoS is enabled by default for devices running Lync Phone Edition.</span></span> <span data-ttu-id="8b99d-107">(Estos dispositivos se conocen comúnmente como comunicaciones unificadas o comunicaciones unificadas). Para comprobarlo, ejecute el siguiente comando de Windows PowerShell desde el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="8b99d-107">(These devices are commonly referred to as UC or Unified Communication phones.) To verify this, run the following Windows PowerShell command from within the Lync Server Management Shell:</span></span>

    Get-CsUCPhoneConfiguration

<span data-ttu-id="8b99d-108">Si no ha realizado ningún cambio en la configuración de su teléfono de comunicaciones unificadas, recibirá la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="8b99d-108">If you have not made any changes to your UC phone configuration settings then you will get back information that looks like this:</span></span>

    Identity             : Global
    CalendarPollInterval : 00:03:00
    EnforcePhoneLock     : True
    PhoneLockTimeout     : 00:10:00
    MinPhonePinLength    : 6
    SIPSecurityMode      : High
    VoiceDiffServTag     : 40
    Voice8021p           : 0
    LoggingLevel         : Off

<span data-ttu-id="8b99d-109">Para fines de calidad de servicio, solo una de estas propiedades es de interés: VoiceDiffServTag.</span><span class="sxs-lookup"><span data-stu-id="8b99d-109">For Quality of Service purposes, only one of these properties is of interest: VoiceDiffServTag.</span></span> <span data-ttu-id="8b99d-110">El VoiceDiffServTag representa el valor de DSCP asignado al tráfico de voz que emana de un dispositivo de Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="8b99d-110">The VoiceDiffServTag represents the DSCP value assigned to voice traffic emanating from a Lync Phone Edition device.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="8b99d-111">El parámetro Voice8021p ya no es compatible con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8b99d-111">The Voice8021p parameter is no longer supported in Lync Server 2013.</span></span> <span data-ttu-id="8b99d-112">El parámetro sigue siendo válido para la compatibilidad con Microsoft Lync Server 2010; sin embargo, no tiene ningún efecto en los dispositivos que se usan con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8b99d-112">The parameter is still valid for backward compatibility with Microsoft Lync Server 2010; however, it has no effect on devices used with Lync Server 2013.</span></span>



</div>

<span data-ttu-id="8b99d-113">En la mayoría de las redes, marcar paquetes de Lync Phone Edition con un VoiceDiffServTag de 40 no debería causar problemas.</span><span class="sxs-lookup"><span data-stu-id="8b99d-113">In most networks, marking Lync Phone Edition packets with a VoiceDiffServTag of 40 should not cause any problems.</span></span> <span data-ttu-id="8b99d-114">Pero, 40 no es el valor usado normalmente para el tráfico de audio; en su lugar, el tráfico de audio se marca casi siempre con el código 46 de DSCP.</span><span class="sxs-lookup"><span data-stu-id="8b99d-114">However, 40 is not the value typically used for audio traffic; instead, audio traffic is almost always marked with the DSCP code 46.</span></span> <span data-ttu-id="8b99d-115">Para mantener la coherencia en toda la red, es posible que desee cambiar la propiedad VoiceDiffServTag de sus teléfonos de comunicaciones unificadas a 46.</span><span class="sxs-lookup"><span data-stu-id="8b99d-115">In order to maintain consistency throughout your network, you might want to change the VoiceDiffServTag property of your UC phones to 46.</span></span>

<span data-ttu-id="8b99d-116">Para ello, puede usar Windows PowerShell o el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8b99d-116">To do that, you can use either Windows PowerShell or the Lync Server Control Panel.</span></span> <span data-ttu-id="8b99d-117">Para modificar el valor de VoiceDiffServTag mediante Windows PowerShell, ejecute el siguiente comando desde el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="8b99d-117">To modify the VoiceDiffServTag value by using Windows PowerShell, run the following command from within the Lync Server Management Shell:</span></span>

    Set-CsUCPhoneConfiguration -VoiceDiffServTag 46

<span data-ttu-id="8b99d-118">El comando anterior modifica la colección global de las opciones de configuración del teléfono UC.</span><span class="sxs-lookup"><span data-stu-id="8b99d-118">The preceding command modifies the global collection of UC phone configuration settings.</span></span> <span data-ttu-id="8b99d-119">Sin embargo, ten en cuenta que la configuración del teléfono UC también se puede asignar al ámbito del sitio.</span><span class="sxs-lookup"><span data-stu-id="8b99d-119">Note, however, that UC phone settings can also be assigned to the site scope.</span></span> <span data-ttu-id="8b99d-120">Para modificar las opciones de configuración del teléfono UC en el ámbito del sitio, debe especificar la identidad del sitio.</span><span class="sxs-lookup"><span data-stu-id="8b99d-120">To modify UC phone configuration settings at the site scope, you must specify the site Identity.</span></span> <span data-ttu-id="8b99d-121">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8b99d-121">For example:</span></span>

    Set-CsUCPhoneConfiguration -Identity "site:Redmond" -VoiceDiffServTag 46

<span data-ttu-id="8b99d-122">También puede usar el siguiente comando para modificar de forma simultánea todas las opciones de configuración del teléfono UC:</span><span class="sxs-lookup"><span data-stu-id="8b99d-122">You can also use the following command to simultaneously modify all your UC phone configuration settings:</span></span>

    Get-CsUCPhoneConfiguration | Set-CsUCPhoneConfiguration -VoiceDiffServTag 46

<span data-ttu-id="8b99d-123">Si prefiere realizar este cambio mediante el panel de control de Lync Server, inicie el panel de control y, a continuación, realice el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="8b99d-123">If you prefer to make this change using Lync Server Control Panel, then start the Control Panel and then complete the following procedure:</span></span>

1.  <span data-ttu-id="8b99d-124">Haga clic en **clientes** y, después, en **configuración de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="8b99d-124">Click **Clients** and then click **Device Configuration**.</span></span>

2.  <span data-ttu-id="8b99d-125">En la pestaña **configuración de dispositivo** , haga doble clic en la colección de configuraciones que desea modificar (por ejemplo, **global**).</span><span class="sxs-lookup"><span data-stu-id="8b99d-125">On the **Device Configuration** tab, double-click the collection of settings you want to modify (for example, **Global**).</span></span>

3.  <span data-ttu-id="8b99d-126">En el cuadro de diálogo **Editar configuración del dispositivo** , establezca el valor de la casilla **calidad de servicio (QoS) de voz** en **46** y, a continuación, haga clic en **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="8b99d-126">In the **Edit Device Configuration** dialog box, set the value of the **Voice Quality of Service (QoS)** box to **46** and then click **Commit**.</span></span>

<span data-ttu-id="8b99d-127">Si tienes varias colecciones, deberás repetir este proceso para cada colección de opciones de teléfono de comunicaciones unificadas.</span><span class="sxs-lookup"><span data-stu-id="8b99d-127">If you have multiple collections you will need to repeat this process for each collection of UC phone settings.</span></span> <span data-ttu-id="8b99d-128">El panel de control de Lync Server no le permitirá modificar varias colecciones de configuración al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="8b99d-128">Lync Server Control Panel will not allow you to simultaneously modify multiple setting collections.</span></span>

<span data-ttu-id="8b99d-129">Si tiene dispositivos que no se basan en el sistema operativo Windows (como iPhones) de su organización, estos dispositivos no se verán afectados por el cambio de la configuración de VoiceDiffServTag.</span><span class="sxs-lookup"><span data-stu-id="8b99d-129">If you have devices that are not based on the Windows operating system (such as iPhones) in your organization these devices will not be affected by changing the VoiceDiffServTag setting.</span></span> <span data-ttu-id="8b99d-130">Si desea cambiar los valores de DSCP en esos dispositivos, tendrá que consultar el manual de administración de cada uno de los tipos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8b99d-130">If you want to change DSCP values on those devices you will need to refer to the administration manual for each of your device types.</span></span>

<span data-ttu-id="8b99d-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b99d-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

