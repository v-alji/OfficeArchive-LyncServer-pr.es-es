---
title: 'Lync Server 2013: Implementar tipos de dirección IP en un servidor perimetral'
description: 'Lync Server 2013: implementar tipos de direcciones IP en un servidor perimetral.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy IP address types on an Edge Server
ms:assetid: 6e2fe7e8-6e90-4d1a-8fc5-e3be92c46571
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204984(v=OCS.15)
ms:contentKeyID: 48184435
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7798ca2f7b38865a2b4ea373546dd4e7203f5b8e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430205"
---
# <a name="deploy-ip-address-types-on-an-edge-server-for-lync-server-2013"></a><span data-ttu-id="753f1-103">Implementar tipos de dirección IP en un servidor perimetral para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="753f1-103">Deploy IP address types on an Edge Server for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="753f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="753f1-104">

<span> </span></span></span>

<span data-ttu-id="753f1-105">_**Última modificación del tema:** 2012-06-14_</span><span class="sxs-lookup"><span data-stu-id="753f1-105">_**Topic Last Modified:** 2012-06-14_</span></span>

<span data-ttu-id="753f1-106">Con el generador de topologías, siga los pasos que se indican en el siguiente procedimiento para implementar tipos de direcciones IP en un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="753f1-106">Using Topology Builder, perform the steps in the following procedure to deploy IP address types on an Edge Server.</span></span>

<div>

## <a name="to-deploy-ip-address-types-on-an-edge-server"></a><span data-ttu-id="753f1-107">Para implementar tipos de direcciones IP en un servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="753f1-107">To deploy IP address types on an Edge Server</span></span>

1.  <span data-ttu-id="753f1-108">En el generador de topologías, en **grupos de límites**, haga clic con el botón secundario en el servidor dentro de un grupo y seleccione **Editar propiedades**.</span><span class="sxs-lookup"><span data-stu-id="753f1-108">In Topology Builder, under **Edge pools**, right-click the server within a pool, and then select **Edit Properties**.</span></span> <span data-ttu-id="753f1-109">(También puede seleccionar el servidor y, a continuación, hacer clic en **Editar propiedades** en el menú **acción** ).</span><span class="sxs-lookup"><span data-stu-id="753f1-109">(Alternatively, select the server, and then click **Edit Properties** from the **Action** menu.)</span></span>

2.  <span data-ttu-id="753f1-p102">En la ventana **Editar propiedades**, seleccione la configuración de dirección IP que quiera admitir. En las siguientes figuras se muestra una configuración de pila dual para la interfaz interna y la interfaz externa.</span><span class="sxs-lookup"><span data-stu-id="753f1-p102">In the **Edit Properties** window, select the IP address configuration that you want to support. The following figures show a dual stack configuration for the internal interface and the external interface.</span></span>
    
    <span data-ttu-id="753f1-112">**Interfaz interna del servidor perimetral de pila dual**</span><span class="sxs-lookup"><span data-stu-id="753f1-112">**Dual stacked Edge Server internal interface**</span></span>
    
    <span data-ttu-id="753f1-113">![Página de propiedades generales de Lync Server](images/JJ204984.5b0883ee-b9f2-4a21-91a9-3286d0beb63b(OCS.15).png "Página de propiedades generales de Lync Server")</span><span class="sxs-lookup"><span data-stu-id="753f1-113">![Lync Server general properties page](images/JJ204984.5b0883ee-b9f2-4a21-91a9-3286d0beb63b(OCS.15).png "Lync Server general properties page")</span></span>
    
    <span data-ttu-id="753f1-114">**Interfaz externa del servidor perimetral de pila dual**</span><span class="sxs-lookup"><span data-stu-id="753f1-114">**Dual stacked Edge Server external interface**</span></span>
    
    <span data-ttu-id="753f1-115">![Página de siguiente salto/configuración externa de Lync Server](images/JJ204984.2aa00ce2-ba50-40aa-bbf1-78636016daf9(OCS.15).png "Página de siguiente salto/configuración externa de Lync Server")</span><span class="sxs-lookup"><span data-stu-id="753f1-115">![Lync Server next hop/external configuration page](images/JJ204984.2aa00ce2-ba50-40aa-bbf1-78636016daf9(OCS.15).png "Lync Server next hop/external configuration page")</span></span>

3.  <span data-ttu-id="753f1-116">Es preciso proporcionar las direcciones internas y externas apropiadas para cada tipo de dirección que seleccione.</span><span class="sxs-lookup"><span data-stu-id="753f1-116">For each address type that you select, you must supply appropriate internal and external addresses.</span></span>

<span data-ttu-id="753f1-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="753f1-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

