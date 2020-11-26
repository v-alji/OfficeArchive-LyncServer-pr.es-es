---
title: 'Lync Server 2013: Iniciar sesión y utilizar Lync 2013 en la máquina virtual'
description: 'Lync Server 2013: iniciar sesión y usar Lync 2013 en la máquina virtual.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Signing in and using Lync 2013 on the virtual machine
ms:assetid: 6140fc19-5bef-4b58-9b0f-19112b5ecd00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204948(v=OCS.15)
ms:contentKeyID: 48184318
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad9a92d450fb9d60aed70617089d95280528892f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444700"
---
# <a name="signing-in-and-using-lync-2013-on-the-virtual-machine"></a><span data-ttu-id="450af-103">Iniciar sesión y utilizar Lync 2013 en la máquina virtual</span><span class="sxs-lookup"><span data-stu-id="450af-103">Signing in and using Lync 2013 on the virtual machine</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="450af-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="450af-104">

<span> </span></span></span>

<span data-ttu-id="450af-105">_**Última modificación del tema:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="450af-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="450af-106">Después de habilitar el complemento VDI, se realizan los pasos siguientes cuando el usuario inicia sesión en Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="450af-106">After the VDI plug-in is enabled, the following steps occur when the user signs in to Lync 2013.</span></span>

1.  <span data-ttu-id="450af-107">El usuario escribe sus credenciales en el cliente de Lync 2013 que se ejecuta en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="450af-107">The user types his or her credentials in to the Lync 2013 client running on the virtual machine.</span></span>

2.  <span data-ttu-id="450af-108">Una vez que Lync detecta la disponibilidad del complemento VDI, Lync le pide al usuario que vuelva a escribir sus credenciales.</span><span class="sxs-lookup"><span data-stu-id="450af-108">After Lync detects the availability of the VDI plug-in, Lync prompts the user to re-enter his or her credentials.</span></span> <span data-ttu-id="450af-109">En este cuadro de diálogo, conviene seleccionar la casilla **Guardar mi contraseña** para no tener que escribir las credenciales en inicios de sesión posteriores.</span><span class="sxs-lookup"><span data-stu-id="450af-109">In this dialog box, we recommend that the user select the **Save my password** check box so that he or she will not be required to enter credentials during subsequent sign in.</span></span>

3.  <span data-ttu-id="450af-110">Lync comienza a emparejarse con el complemento VDI.</span><span class="sxs-lookup"><span data-stu-id="450af-110">Lync begins pairing with the VDI plug-in.</span></span> <span data-ttu-id="450af-111">Antes de completar el emparejamiento, el cliente muestra dos iconos en la barra de estado de Lync.</span><span class="sxs-lookup"><span data-stu-id="450af-111">Before pairing is complete, the client displays two icons in the Lync status bar.</span></span> <span data-ttu-id="450af-112">El icono de la esquina inferior izquierda indica que no hay dispositivos de audio disponibles, y el icono parpadeante en la esquina inferior derecha indica que el emparejamiento de VDI está en curso, tal y como se muestra:</span><span class="sxs-lookup"><span data-stu-id="450af-112">The icon in the lower left indicates that no audio devices are available, and the blinking icon in the lower right indicates that the VDI pairing is in progress, as shown:</span></span>
    
    <span data-ttu-id="450af-113">![Icono de VDI de Lync que muestra el emparejamiento correcto](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Icono de VDI de Lync que muestra el emparejamiento correcto")</span><span class="sxs-lookup"><span data-stu-id="450af-113">![Lync VDI icon showing successful pairing](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Lync VDI icon showing successful pairing")</span></span>  

4.  <span data-ttu-id="450af-114">Una vez realizado el emparejamiento de VDI, los iconos cambian para indicar el dispositivo de audio que se utilizará para las llamadas y el emparejamiento de VDI:</span><span class="sxs-lookup"><span data-stu-id="450af-114">After VDI pairing is successful, the icons change to indicate the audio device that will be used for calls and the VDI pairing success:</span></span>
    
    <span data-ttu-id="450af-115">![Icono de emparejamiento de VDI de Lync que muestra el éxito](images/JJ204948.57be3387-a3e5-4949-831e-f5ff9fcc5598(OCS.15).png "Icono de emparejamiento de VDI de Lync que muestra el éxito")</span><span class="sxs-lookup"><span data-stu-id="450af-115">![Lync VDI pairing icon showing success](images/JJ204948.57be3387-a3e5-4949-831e-f5ff9fcc5598(OCS.15).png "Lync VDI pairing icon showing success")</span></span>  

5.  <span data-ttu-id="450af-116">Después de que Lync emparejado con el complemento VDI, el usuario puede ver su presencia en dispositivos compatibles con Lync que están conectados al equipo local.</span><span class="sxs-lookup"><span data-stu-id="450af-116">After Lync pairs with the VDI plug-in, the user can see his or her presence on Lync compatible devices that are connected to the local computer.</span></span> <span data-ttu-id="450af-117">Ahora, el usuario puede colocar y contestar llamadas como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="450af-117">The user can now place and answer calls as usual.</span></span>

<span data-ttu-id="450af-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="450af-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

