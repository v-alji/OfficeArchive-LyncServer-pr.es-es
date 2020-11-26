---
title: 'Lync Server 2013: Exportar casos de prueba de enrutamiento de voz'
description: 'Lync Server 2013: exporte los casos de prueba de enrutamiento de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export voice routing test cases
ms:assetid: 489ac472-1a35-4755-b390-48f7cdf31e94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425957(v=OCS.15)
ms:contentKeyID: 48184050
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 934bd183a17c46cf82fe5bc04faaa55a9bbe4731
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428352"
---
# <a name="export-voice-routing-test-cases-in-lync-server-2013"></a><span data-ttu-id="8dffb-103">Exportar casos de prueba de enrutamiento de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8dffb-103">Export voice routing test cases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8dffb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8dffb-104">

<span> </span></span></span>

<span data-ttu-id="8dffb-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="8dffb-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="8dffb-106">Los casos de prueba proporcionan una manera de probar las rutas de voz de su organización: defina elementos como el número que se marcará y el plan de marcado y la Directiva de voz que se utilizará, y Lync Server puede comprobar que, dadas las condiciones, el número proporcionado se pueda enrutar correctamente a la red PSTN.</span><span class="sxs-lookup"><span data-stu-id="8dffb-106">Test cases provide a way for you to test voice routes in your organization: you define such things as the number to be dialed and the dial plan and voice policy to be employed, and Lync Server can then verify that, given those conditions, the supplied number can successfully be routed to the PSTN network.</span></span>

<span data-ttu-id="8dffb-107">Los casos de prueba, que se pueden crear con el panel de control de Lync Server, normalmente solo se guardan en el servidor en el que se creó y ejecutó originalmente el caso.</span><span class="sxs-lookup"><span data-stu-id="8dffb-107">Test cases, which can be created by using Lync Server Control Panel, are typically saved only on the server where the case was originally created and run.</span></span> <span data-ttu-id="8dffb-108">Sin embargo, estos casos de prueba se pueden exportar como archivos XML (con la extensión. vtest) y, a continuación, importarse en otros servidores.</span><span class="sxs-lookup"><span data-stu-id="8dffb-108">However, these test cases can be exported as XML files (with the .vtest extension) and then imported on other servers.</span></span> <span data-ttu-id="8dffb-109">Esto le permite ejecutar las mismas pruebas en diferentes equipos que se encuentran en diferentes puntos de su topología.</span><span class="sxs-lookup"><span data-stu-id="8dffb-109">This enables you to run the same tests on different computers located at different points in your topology.</span></span>

<div>

## <a name="to-export-a-voice-routing-test-case"></a><span data-ttu-id="8dffb-110">Para exportar un caso de prueba de enrutamiento de voz</span><span class="sxs-lookup"><span data-stu-id="8dffb-110">To export a voice routing test case</span></span>

1.  <span data-ttu-id="8dffb-111">En el panel de control de Lync Server, haga clic en **enrutamiento de voz** y en **probar enrutamiento de voz**.</span><span class="sxs-lookup"><span data-stu-id="8dffb-111">In Lync Server Control Panel, click **Voice Routing** and then click **Test Voice Routing**.</span></span>

2.  <span data-ttu-id="8dffb-112">En la pestaña **probar el enrutamiento de voz** , seleccione el caso de prueba (o casos de prueba) que se va a exportar.</span><span class="sxs-lookup"><span data-stu-id="8dffb-112">On the **Test Voice Routing** tab, select the test case (or test cases) to be exported.</span></span> <span data-ttu-id="8dffb-113">Para seleccionar varios casos de prueba, haga clic en el primer caso que se va a exportar y, a continuación, mantenga presionada la tecla Ctrl y seleccione los casos adicionales que se van a exportar.</span><span class="sxs-lookup"><span data-stu-id="8dffb-113">To select multiple test cases, click the first case to be exported, then hold down the Ctrl key and select the additional cases to be exported.</span></span>

3.  <span data-ttu-id="8dffb-114">Haga clic en **acción** y, a continuación, en **exportar casos de prueba**.</span><span class="sxs-lookup"><span data-stu-id="8dffb-114">Click **Action**, then click **Export test cases**.</span></span>

4.  <span data-ttu-id="8dffb-115">En el cuadro de diálogo **Guardar como** , seleccione una carpeta para almacenar los casos de prueba exportados y escriba un nombre para el archivo XML resultante en el cuadro **nombre de archivo** .</span><span class="sxs-lookup"><span data-stu-id="8dffb-115">In the **Save As** dialog box, select a folder to store the exported test cases and type a name for the resulting XML file in the **File name** box.</span></span> <span data-ttu-id="8dffb-116">Tenga en cuenta que si va a exportar varias pruebas, todos estos casos de prueba se guardarán en un único archivo XML.</span><span class="sxs-lookup"><span data-stu-id="8dffb-116">Note that if you are exporting multiple tests cases all of these test cases will be saved to a single XML file.</span></span>

5.  <span data-ttu-id="8dffb-117">Para guardar los casos de prueba, haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="8dffb-117">To save the test cases, click **Save**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8dffb-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="8dffb-118">See Also</span></span>


[<span data-ttu-id="8dffb-119">Importar casos de prueba de enrutamiento de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8dffb-119">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)  
  

<span data-ttu-id="8dffb-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8dffb-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

