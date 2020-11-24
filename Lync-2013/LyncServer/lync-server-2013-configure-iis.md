---
title: 'Lync Server 2013: Configurar IIS'
description: 'Lync Server 2013: configuración de IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure IIS
ms:assetid: bc4ae8cc-ec0c-42f1-9034-058930e530d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412918(v=OCS.15)
ms:contentKeyID: 48185248
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cdd08e47d05f2e32f14178eaaa3a100f8c445dda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399366"
---
# <a name="configure-iis-for-lync-server-2013"></a><span data-ttu-id="a5a17-103">Configurar IIS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a5a17-103">Configure IIS for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a5a17-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a5a17-104">

<span> </span></span></span>

<span data-ttu-id="a5a17-105">_**Última modificación del tema:** 2011-12-16_</span><span class="sxs-lookup"><span data-stu-id="a5a17-105">_**Topic Last Modified:** 2011-12-16_</span></span>

<span data-ttu-id="a5a17-106">La configuración de servicios de Internet Information Server (IIS) para Lync Server 2013 implica la instalación de los componentes correctos para admitir los servicios web que necesita Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a5a17-106">Configuring Internet Information Services (IIS) for Lync Server 2013 involves installing the correct components to support the Web Services needed by Lync Server 2013.</span></span> <span data-ttu-id="a5a17-107">Para obtener más información sobre la instalación de IIS, consulte [configuración de IIS en Lync Server 2013](lync-server-2013-iis-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="a5a17-107">For details about installing IIS, see [IIS configuration in Lync Server 2013](lync-server-2013-iis-configuration.md).</span></span> <span data-ttu-id="a5a17-108">Si dispone de una directiva para ejecutar el Asistente para configuración de seguridad en los servidores antes de ponerlos en servicio o como una parte típica de su mantenimiento, consulte [reactivar el servidor después de que el Asistente para configuración de seguridad cierra los puertos en IIS](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md) para obtener información sobre un efecto secundario de la ejecución del asistente que cerrará los puertos en una configuración de IIS de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a5a17-108">If you have a policy to run the Security Configuration Wizard on servers before putting them into service or as a typical part of your maintenance, see [Re-activate server after Security Configuration Wizard closes ports in IIS](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md) for information about a side effect of running the wizard that will close ports on a Lync Server 2013 IIS configuration.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a5a17-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a5a17-109">In This Section</span></span>

  - [<span data-ttu-id="a5a17-110">Configuración de IIS en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a5a17-110">IIS configuration in Lync Server 2013</span></span>](lync-server-2013-iis-configuration.md)

  - [<span data-ttu-id="a5a17-111">Volver a activar el servidor después de que el Asistente para la configuración de la seguridad cierre los puertos en IIS</span><span class="sxs-lookup"><span data-stu-id="a5a17-111">Re-activate server after Security Configuration Wizard closes ports in IIS</span></span>](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md)

<span data-ttu-id="a5a17-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a5a17-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

