---
title: 'Lync Server 2013: personalizar la música de estacionamiento de llamadas en espera'
description: 'Lync Server 2013: personalizar la música de estacionamiento de llamadas en espera.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Customize Call Park music on hold
ms:assetid: 3d78e6f9-a4ae-49f4-a89f-4515acb49dac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688031(v=OCS.15)
ms:contentKeyID: 49733621
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 19219e4a77d4be4a18a43255e142339a4af6f463
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431382"
---
# <a name="customize-call-park-music-on-hold-in-lync-server-2013"></a><span data-ttu-id="f40ea-103">Personalizar la música de estacionamiento de llamadas en espera en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f40ea-103">Customize Call Park music on hold in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f40ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f40ea-104">

<span> </span></span></span>

<span data-ttu-id="f40ea-105">_**Última modificación del tema:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="f40ea-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="f40ea-106">Puede especificar su propio archivo de música para que use la música en espera, en lugar del archivo de música predeterminado que se incluye con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f40ea-106">You can specify your own music file to use for music on hold, instead of the default music file that ships with Lync Server 2013.</span></span> <span data-ttu-id="f40ea-107">Para personalizar la música en espera, utilice el cmdlet **Set-CsCallParkServiceMusicOnHoldFile**.</span><span class="sxs-lookup"><span data-stu-id="f40ea-107">To customize music on hold, use the **Set-CsCallParkServiceMusicOnHoldFile** cmdlet.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f40ea-108">Si personaliza la música en espera y quiere la misma música para varios sitios, debe configurar el archivo de música para cada sitio que ejecute la aplicación estacionamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="f40ea-108">If you customize music on hold and want the same music for multiple sites, you must configure the music file for each site that runs the Call Park application.</span></span>



</div>

<div>

## <a name="to-customize-the-music-file"></a><span data-ttu-id="f40ea-109">Para personalizar el archivo de música</span><span class="sxs-lookup"><span data-stu-id="f40ea-109">To customize the music file</span></span>

1.  <span data-ttu-id="f40ea-110">Inicie sesión en el equipo donde está instalado el shell de administración de Lync Server como miembro del grupo RTCUniversalServerAdmins o con los derechos de usuario necesarios, tal y como se describe en [permisos de configuración de delegado en Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="f40ea-110">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="f40ea-111">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="f40ea-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f40ea-112">Ejecute:</span><span class="sxs-lookup"><span data-stu-id="f40ea-112">Run:</span></span>
    
        Set-CsCallParkServiceMusicOnHoldFile -Service <ServiceID where the Call Park application resides> -Content <Byte[]>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="f40ea-113">Use el cmdlet <STRONG>Get-CsService</STRONG> para identificar el servicio.</span><span class="sxs-lookup"><span data-stu-id="f40ea-113">Use the <STRONG>Get-CsService</STRONG> cmdlet to identify the service.</span></span> <span data-ttu-id="f40ea-114">Para obtener más información, vea <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsService">Get-CsService</A>.</span><span class="sxs-lookup"><span data-stu-id="f40ea-114">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsService">Get-CsService</A>.</span></span>

    
    </div>
    
    <span data-ttu-id="f40ea-115">En el ejemplo siguiente se muestra cómo obtener el contenido de un archivo, soothingmusic.wma, como matriz de bytes y asignarlo a una variable.</span><span class="sxs-lookup"><span data-stu-id="f40ea-115">The following example shows how to obtain the contents of a file, soothingmusic.wma, as a byte array and assign it to a variable.</span></span> <span data-ttu-id="f40ea-116">A continuación, el archivo de audio se asigna como el archivo de música en espera en Estacionamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="f40ea-116">Then the audio file is assigned as the music-on-hold file for Call Park.</span></span> <span data-ttu-id="f40ea-117">Para obtener más información, consulte [set-CsCallParkServiceMusicOnHoldFile](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkServiceMusicOnHoldFile).</span><span class="sxs-lookup"><span data-stu-id="f40ea-117">For details, see [Set-CsCallParkServiceMusicOnHoldFile](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkServiceMusicOnHoldFile).</span></span>
    
        $a = Get-Content -ReadCount 0 -Encoding byte "C:\MoHFiles\soothingmusic.wma"
        Set-CsCallParkServiceMusicOnHoldFile -Service Redmond1-applicationserver-1 -Content $a

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f40ea-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f40ea-118">See Also</span></span>


[<span data-ttu-id="f40ea-119">Set-CsCallParkServiceMusicOnHoldFile</span><span class="sxs-lookup"><span data-stu-id="f40ea-119">Set-CsCallParkServiceMusicOnHoldFile</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkServiceMusicOnHoldFile)  
[<span data-ttu-id="f40ea-120">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="f40ea-120">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
  

<span data-ttu-id="f40ea-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f40ea-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

