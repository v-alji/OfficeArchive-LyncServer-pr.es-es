---
title: Procedimientos recomendados para el servidor de chat persistente
description: Procedimientos recomendados para el servidor de chat persistente.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server best practices
ms:assetid: dc18e7f7-599b-4d32-abf7-cd9e691426a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398970(v=OCS.15)
ms:contentKeyID: 48185612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c575c0afa0366e88748eadfcf4c04fccb20b375
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438788"
---
# <a name="persistent-chat-server-best-practices"></a><span data-ttu-id="56fdc-103">Procedimientos recomendados para el servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="56fdc-103">Persistent Chat Server best practices</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="56fdc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="56fdc-104">

<span> </span></span></span>

<span data-ttu-id="56fdc-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="56fdc-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="56fdc-106">A medida que crea las categorías y los salones de chat persistentes, y diseña su alcance y pertenencia, las siguientes sugerencias pueden ayudar a su planeamiento:</span><span class="sxs-lookup"><span data-stu-id="56fdc-106">As you create your categories and Persistent Chat rooms and design your scoping and membership, the following tips can help your planning:</span></span>

  - <span data-ttu-id="56fdc-107">Si su empresa no requiere una pared ética, no limite el ámbito del árbol de categorías.</span><span class="sxs-lookup"><span data-stu-id="56fdc-107">If your company does not require an ethical wall, do not narrow the scope in your category tree.</span></span> <span data-ttu-id="56fdc-108">Coloca a todos los usuarios en el ámbito de una categoría y crea todos los salones de chat en esa categoría.</span><span class="sxs-lookup"><span data-stu-id="56fdc-108">Put all your users in the scope of one category, and create all chat rooms in that category.</span></span> <span data-ttu-id="56fdc-109">Posteriormente, use solo listas de pertenencia para conceder o restringir el acceso a cada salón de chat.</span><span class="sxs-lookup"><span data-stu-id="56fdc-109">Subsequently, use only membership lists to grant or restrict access to each chat room.</span></span>

  - <span data-ttu-id="56fdc-110">En la mayoría de los casos, debe permitir que los usuarios creen nuevos salones de chat para que las discusiones sobre los nuevos temas se puedan iniciar en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="56fdc-110">In most cases, you should enable users to create new chat rooms so that discussions about new topics can be started any time.</span></span> <span data-ttu-id="56fdc-111">Para ello, la lista de **creadores** es la misma que la lista de **AllowedMembers** .</span><span class="sxs-lookup"><span data-stu-id="56fdc-111">Do this by making the **Creators** list the same as the **AllowedMembers** list.</span></span> <span data-ttu-id="56fdc-112">Sin embargo, si desea permitir que solo un equipo de soporte técnico central o usuarios designados creen salas, convierta la lista de **creadores** en el subconjunto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="56fdc-112">However, if you want to allow only a central support team or designated users to create rooms, then make the **Creators** list as the appropriate subset.</span></span>

  - <span data-ttu-id="56fdc-113">Asigne a cada salón de chat un nombre completo y un resumen de descripción que describa Dónde encaja en la organización.</span><span class="sxs-lookup"><span data-stu-id="56fdc-113">Give each chat room a complete name and description summary that describes where it fits in with your organization.</span></span> <span data-ttu-id="56fdc-114">Como los usuarios no pueden ver el nombre de la categoría cuando usan el salón de chat, no puede confiar en el nombre de la categoría para ayudar a los usuarios a determinar el foro de discusión previsto para el salón de chat.</span><span class="sxs-lookup"><span data-stu-id="56fdc-114">Because users cannot see the category name when they use the chat room, you cannot rely on the category name to help users determine the intended discussion forum for the chat room.</span></span>

  - <span data-ttu-id="56fdc-115">Es posible que desee tener un flujo de trabajo de creación de salas personalizada si tiene determinadas convenciones de nomenclatura u otros controles de acceso o validaciones para implementar.</span><span class="sxs-lookup"><span data-stu-id="56fdc-115">You may want to have a custom room creation workflow if you have certain naming conventions or other access controls or validations to implement.</span></span> <span data-ttu-id="56fdc-116">La configuración de chat persistente le permite personalizar el **RoomManagementUrl** a algo que hospede.</span><span class="sxs-lookup"><span data-stu-id="56fdc-116">The Persistent Chat configuration enables you to customize the **RoomManagementUrl** to something that you host.</span></span> <span data-ttu-id="56fdc-117">Por ejemplo, cuando los usuarios hacen clic en **crear una sala** en su cliente de Lync, pueden redirigirse a la solución personalizada.</span><span class="sxs-lookup"><span data-stu-id="56fdc-117">For example, when users click **Create a room** in their Lync client, they can be redirected to your custom solution.</span></span>

  - <span data-ttu-id="56fdc-118">Cree una variedad de complementos que le ayuden a mejorar la experiencia de los salones de chat aportando otros datos empresariales a salones de chat.</span><span class="sxs-lookup"><span data-stu-id="56fdc-118">Create a variety of add-ins that help to enhance the experience of chat rooms by bringing in other business data into chat rooms.</span></span> <span data-ttu-id="56fdc-119">Los administradores deben registrar los complementos que desean permitir en el sistema.</span><span class="sxs-lookup"><span data-stu-id="56fdc-119">Administrators must register the add-ins that they want to allow in the system.</span></span> <span data-ttu-id="56fdc-120">Los administradores de salones de chat y los creadores pueden elegir en la lista de complementos permitidos para los más importantes para sus respectivos salones.</span><span class="sxs-lookup"><span data-stu-id="56fdc-120">Chat room managers and creators can choose from the list of allowed add-ins for the ones most relevant to their respective rooms.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="56fdc-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="56fdc-121">See Also</span></span>


[<span data-ttu-id="56fdc-122">Administrar categorías, salones de chat y complementos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="56fdc-122">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>](lync-server-2013-managing-categories-rooms-and-add-ins.md)  
  

<span data-ttu-id="56fdc-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="56fdc-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

