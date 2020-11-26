---
title: 'Lync Server 2013: Servicio web de actualización de dispositivos'
description: 'Lync Server 2013: servicio Web de actualización de dispositivos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Update Web service
ms:assetid: 036f473d-a131-431f-8051-76ccadc5cfba
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994015(v=OCS.15)
ms:contentKeyID: 51803921
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45511d34ab99f295481472f2a3c14bf21da32ff6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429370"
---
# <a name="device-update-web-service-in-lync-server-2013"></a><span data-ttu-id="2fd44-103">Servicio web de actualización de dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd44-103">Device Update Web service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2fd44-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2fd44-104">

<span> </span></span></span>

<span data-ttu-id="2fd44-105">_**Última modificación del tema:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="2fd44-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="2fd44-106">Lync Server incluye el servicio Web de actualización de dispositivos, que se instala automáticamente como parte del rol de servicios Web.</span><span class="sxs-lookup"><span data-stu-id="2fd44-106">Lync Server includes the Device Update Web service, which is automatically installed as part of the Web Services role.</span></span> <span data-ttu-id="2fd44-107">Este servicio le permite descargar actualizaciones de Microsoft, probarlas y, a continuación, implementarlas en los teléfonos IP de su organización.</span><span class="sxs-lookup"><span data-stu-id="2fd44-107">This service lets you download updates from Microsoft, test them, and then deploy the updates to IP phones in your organization.</span></span> <span data-ttu-id="2fd44-108">También puede usar el servicio Web de actualización de dispositivos para revertir dispositivos a versiones de software anteriores.</span><span class="sxs-lookup"><span data-stu-id="2fd44-108">You can also use Device Update Web service to roll back devices to previous software versions.</span></span>

<span data-ttu-id="2fd44-109">En esta sección se proporcionan detalles sobre cómo administrar el servicio Web de actualización de dispositivos y cómo se implementan las actualizaciones mediante registros de actualización de dispositivos, reglas (Lync Phone Edition usa *reglas* para asociar actualizaciones de versión de firmware con dispositivos de hardware) y valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="2fd44-109">This section provides details about how to manage the Device Update Web service and deployed updates by using device update logs, rules (Lync Phone Edition uses *rules* to associate firmware version updates with hardware devices), and configuration settings.</span></span>

<span data-ttu-id="2fd44-110">Para obtener más información sobre el proceso y las características del servicio Web de actualización de dispositivos, consulte [actualización de dispositivos](https://technet.microsoft.com/library/gg412864\(v=ocs.14\).aspx) en la biblioteca de TechNet de 2010 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2fd44-110">For details about the Device Update Web service process and features, see [Updating Devices](https://technet.microsoft.com/library/gg412864\(v=ocs.14\).aspx) in the Lync Server 2010 TechNet Library.</span></span> <span data-ttu-id="2fd44-111">(Tenga en cuenta que el servicio Web de actualización de dispositivos, como todos los componentes de Lync Phone Edition, funciona de la misma manera con Lync Server 2013 como lo hace con Lync Server 2010).</span><span class="sxs-lookup"><span data-stu-id="2fd44-111">(Note that the Device Update Web service, like all Lync Phone Edition components, works the same way with Lync Server 2013 as it does with Lync Server 2010.)</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2fd44-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2fd44-112">In This Section</span></span>

  - [<span data-ttu-id="2fd44-113">Registros y archivos de actualización de dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd44-113">Device Update logs and files in Lync Server 2013</span></span>](lync-server-2013-device-update-logs-and-files.md)

  - [<span data-ttu-id="2fd44-114">Reglas de actualización de dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd44-114">Device Update rules in Lync Server 2013</span></span>](lync-server-2013-device-update-rules.md)

  - [<span data-ttu-id="2fd44-115">Configuración de actualización de dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd44-115">Device Update configuration settings in Lync Server 2013</span></span>](lync-server-2013-device-update-configuration-settings.md)

  - [<span data-ttu-id="2fd44-116">Ver actualizaciones de software para dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd44-116">View software updates for devices in Lync Server 2013</span></span>](lync-server-2013-view-software-updates-for-devices-in-your-organization.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2fd44-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fd44-117">See Also</span></span>


<span data-ttu-id="2fd44-118">[Herramientas y servicios para administrar y solucionar problemas de dispositivos](https://technet.microsoft.com/library/gg425800\(v=ocs.14\).aspx)</span><span class="sxs-lookup"><span data-stu-id="2fd44-118">[Tools and Services for Managing and Troubleshooting Devices](https://technet.microsoft.com/library/gg425800\(v=ocs.14\).aspx)</span></span>  
  

<span data-ttu-id="2fd44-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2fd44-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

