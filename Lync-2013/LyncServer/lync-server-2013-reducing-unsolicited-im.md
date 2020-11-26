---
title: 'Lync Server 2013: Reducir la mensajería instantánea no solicitada'
description: 'Lync Server 2013: reducir la mensajería instantánea no solicitada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reducing unsolicited IM for Lync Server 2013
ms:assetid: d2998708-e699-4465-a918-e1d9ea4c49c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518335(v=OCS.15)
ms:contentKeyID: 62625493
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 294c53a6b82b4dc345fbb9afcf9983d5bd35893a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436674"
---
# <a name="reducing-unsolicited-im-for-lync-server-2013"></a><span data-ttu-id="1a262-103">Reducir la mensajería instantánea no solicitada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a262-103">Reducing unsolicited IM for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1a262-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1a262-104">

<span> </span></span></span>

<span data-ttu-id="1a262-105">_**Última modificación del tema:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="1a262-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="1a262-106">La aplicación inteligente de filtro de mensajes instantáneos ayuda a proteger la implementación de Microsoft Lync Server 2013 contra los virus más comunes con una degradación mínima para la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="1a262-106">The Intelligent IM Filter application helps protect your Microsoft Lync Server 2013 deployment against the most common viruses with minimal degradation to the user experience.</span></span> <span data-ttu-id="1a262-107">El filtro inteligente de mensajes instantáneos proporciona lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1a262-107">The Intelligent IM Filter provides the following:</span></span>

  - <span data-ttu-id="1a262-108">Filtrado de URL mejorado</span><span class="sxs-lookup"><span data-stu-id="1a262-108">Enhanced URL filtering</span></span>

  - <span data-ttu-id="1a262-109">Filtrado mejorado de transferencia de archivos</span><span class="sxs-lookup"><span data-stu-id="1a262-109">Enhanced file transfer filtering</span></span>

<span data-ttu-id="1a262-110">Use el filtro inteligente de mi para configurar filtros para bloquear mensajes instantáneos no solicitados o potencialmente dañinos de puntos de conexión desconocidos fuera del firewall de la empresa.</span><span class="sxs-lookup"><span data-stu-id="1a262-110">Use Intelligent IM Filter to configure filters to block unsolicited or potentially harmful instant messages from unknown endpoints outside the corporate firewall.</span></span> <span data-ttu-id="1a262-111">Para configurar filtros, especifique los criterios que se van a usar para determinar qué se debe bloquear, por ejemplo, los mensajes instantáneos que contengan hipervínculos y archivos con extensiones específicas.</span><span class="sxs-lookup"><span data-stu-id="1a262-111">You configure filters by specifying the criteria to be used to determine what should be blocked, such as instant messages containing hyperlinks and files with specific extensions.</span></span>

<span data-ttu-id="1a262-112">Antes de implementar la aplicación inteligente de filtro de mensajes de mensajería instantánea, debe comprender cómo se aplican las opciones de filtrado cuando los mensajes se enrutan desde un servidor de Lync Server 2013 a otro.</span><span class="sxs-lookup"><span data-stu-id="1a262-112">Before you deploy the Intelligent IM Message Filter application, you should understand how filtering options are applied when messages are routed from one Lync Server 2013 server to another.</span></span> <span data-ttu-id="1a262-113">La manera en que se aplican estas opciones de filtrado es coherente, independientemente de si los servidores se encuentran en una sola organización o en los límites de la organización.</span><span class="sxs-lookup"><span data-stu-id="1a262-113">The way these filtering options are applied is consistent, regardless of whether the servers are located in a single organization or across organizational boundaries.</span></span> <span data-ttu-id="1a262-114">Esta coherencia se aplica a la forma en que el aviso personalizado y los mensajes de advertencia se insertan en mensajes y se envían por servidores.</span><span class="sxs-lookup"><span data-stu-id="1a262-114">This consistency applies to the way that the customized notice, and warning texts are inserted into messages and sent across servers.</span></span>

<span data-ttu-id="1a262-115">La opción de filtrado recomendada es permitir la mensajería instantánea con hipervínculos pero requerir el filtro inteligente de mensajes instantáneos para deshabilitar el vínculo al insertar un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="1a262-115">The recommended filtering option is to allow instant messages with hyperlinks but require the Intelligent IM Filter to disable the link by inserting an underscore before it.</span></span> <span data-ttu-id="1a262-116">Si elige esta opción, tendrá la opción adicional de redactar un aviso para los usuarios que aparece al principio de cada mensaje instantáneo que contiene un hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="1a262-116">If you choose this option, you have the additional option of composing a notice to users that appears at the beginning of each instant message that contains a hyperlink.</span></span>

<span data-ttu-id="1a262-117">Una segunda opción de filtrado es permitir los mensajes instantáneos con hipervínculos no modificados.</span><span class="sxs-lookup"><span data-stu-id="1a262-117">A second filtering option is to allow instant messages with unmodified hyperlinks.</span></span> <span data-ttu-id="1a262-118">Si elige esta opción, tiene la opción adicional (recomendado) de redactar una advertencia para los usuarios que se insertan en cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="1a262-118">If you choose this option, you have the additional option (recommended) of composing a warning to users that is inserted in each message.</span></span>

<span data-ttu-id="1a262-119">Una tercera opción es bloquear todos los mensajes instantáneos que contienen hipervínculos.</span><span class="sxs-lookup"><span data-stu-id="1a262-119">A third option is to block all instant messages that contain hyperlinks.</span></span> <span data-ttu-id="1a262-120">Si elige esta opción, el servidor envía una advertencia al usuario.</span><span class="sxs-lookup"><span data-stu-id="1a262-120">If you choose this option, the server sends a warning to the user.</span></span> <span data-ttu-id="1a262-121">Debes escribir esta advertencia.</span><span class="sxs-lookup"><span data-stu-id="1a262-121">You must write this warning.</span></span>

<span data-ttu-id="1a262-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1a262-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

