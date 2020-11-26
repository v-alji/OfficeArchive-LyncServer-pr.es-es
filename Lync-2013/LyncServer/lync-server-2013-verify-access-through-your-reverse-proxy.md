---
title: 'Lync Server 2013: Comprobar el acceso a través del proxy inverso'
description: 'Lync Server 2013: comprobar el acceso a través del proxy inverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify access through your reverse proxy
ms:assetid: 3076a786-e022-4d41-91ec-1bf252b2a468
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429697(v=OCS.15)
ms:contentKeyID: 48183753
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 593aac5574f0dcf683351f12a6392f6116480ac5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443478"
---
# <a name="verify-access-through-your-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="3083a-103">Comprobar el acceso a través del proxy inverso en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3083a-103">Verify access through your reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3083a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3083a-104">

<span> </span></span></span>

<span data-ttu-id="3083a-105">_**Última modificación del tema:** 2013-03-29_</span><span class="sxs-lookup"><span data-stu-id="3083a-105">_**Topic Last Modified:** 2013-03-29_</span></span>

<span data-ttu-id="3083a-106">Use el procedimiento siguiente para comprobar que los usuarios pueden obtener acceso a la información del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="3083a-106">Use the following procedure to verify that your users can access information on the reverse proxy.</span></span> <span data-ttu-id="3083a-107">Es posible que tenga que completar la configuración del firewall y del sistema de nombres de dominio (DNS) antes de que Access funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="3083a-107">You might need to complete the firewall configuration and Domain Name System (DNS) configuration before access will work correctly.</span></span>

<div>

## <a name="to-verify-that-you-can-access-the-website-through-the-internet"></a><span data-ttu-id="3083a-108">Para comprobar que puede obtener acceso al sitio web a través de Internet</span><span class="sxs-lookup"><span data-stu-id="3083a-108">To verify that you can access the website through the Internet</span></span>

  - <span data-ttu-id="3083a-109">Abra un explorador Web, escriba las direcciones URL en la barra de **direcciones** que los clientes usan para acceder a los archivos de la libreta de direcciones y el sitio web para las conferencias de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3083a-109">Open a web browser, type the URLs in the **Address** bar that clients use to access the Address Book files and the website for conferencing as follows:</span></span>
    
      - <span data-ttu-id="3083a-110">En servidor de la libreta de direcciones, escriba una dirección URL similar a la siguiente: **https://externalwebfarmFQDN/abs** donde externalwebfarmFQDN es el FQDN externo de los servicios web externos que hospedan los servicios de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3083a-110">For Address Book Server, type a URL similar to the following: **https://externalwebfarmFQDN/abs** where externalwebfarmFQDN is the external FQDN of the external web services that hosts Address Book services.</span></span> <span data-ttu-id="3083a-111">El usuario debe recibir un desafío HTTP, ya que la seguridad de directorios de la carpeta del servidor de la libreta de direcciones está configurada de forma predeterminada en la autenticación de Windows.</span><span class="sxs-lookup"><span data-stu-id="3083a-111">The user should receive an HTTP challenge, because directory security on the Address Book Server folder is configured to Windows authentication by default.</span></span>
    
      - <span data-ttu-id="3083a-112">Para conferencias, escriba una dirección URL similar a la siguiente: **https://externalwebfarmFQDN/meet** donde externalwebfarmFQDN es el FQDN externo de la granja de servidores web que hospeda el contenido de la reunión.</span><span class="sxs-lookup"><span data-stu-id="3083a-112">For conferencing, type a URL similar to the following: **https://externalwebfarmFQDN/meet** where externalwebfarmFQDN is the external FQDN of the web farm that hosts meeting content.</span></span> <span data-ttu-id="3083a-113">Esta dirección URL debe mostrar la página de solución de problemas para conferencias.</span><span class="sxs-lookup"><span data-stu-id="3083a-113">This URL should display the troubleshooting page for conferencing.</span></span> <span data-ttu-id="3083a-114">También puede confirmar que su dirección URL simple para conferencias funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="3083a-114">Alternatively, confirm that your Simple URL for conferencing functions correctly.</span></span> <span data-ttu-id="3083a-115">Una dirección URL sencilla de ejemplo para la combinación de conferencia puede ser https://meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3083a-115">An example Simple URL for the conference join might be https://meet.contoso.com</span></span>
    
      - <span data-ttu-id="3083a-116">En expansión de grupos de distribución, escriba una dirección URL similar a la siguiente: **https://externalwebfarmFQDN/GroupExpansion/service.svc** .</span><span class="sxs-lookup"><span data-stu-id="3083a-116">For distribution group expansion, type a URL similar to the following: **https://externalwebfarmFQDN/GroupExpansion/service.svc**.</span></span> <span data-ttu-id="3083a-117">El usuario debe recibir un desafío HTTP, porque la seguridad de directorio en el servicio de expansión del grupo de distribución está configurada de forma predeterminada en la autenticación de Windows.</span><span class="sxs-lookup"><span data-stu-id="3083a-117">The user should receive an HTTP challenge, because directory security on the distribution group expansion service is configured to Windows authentication by default.</span></span>
    
      - <span data-ttu-id="3083a-118">Para el acceso telefónico, escriba la dirección URL sencilla similar a la siguiente, **https://externalwebfarmFQDN/dialin** donde externalwebfarmFQDN es el nombre completo externo del conjunto de servidores web que hospeda la página de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="3083a-118">For dial-in, type the simple URL similar to the following **https://externalwebfarmFQDN/dialin** where externalwebfarmFQDN is the external FQDN of the web farm that hosts the dial-in page for dial-in conferencing.</span></span> <span data-ttu-id="3083a-119">El usuario debe dirigirse a la página de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="3083a-119">The user should be directed to the dial-in page.</span></span> <span data-ttu-id="3083a-120">También puede confirmar que su dirección de acceso telefónico simple funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="3083a-120">Alternatively, confirm that your Simple URL dial-in functions correctly.</span></span> <span data-ttu-id="3083a-121">Un ejemplo de una dirección URL simple para el acceso telefónico es https://dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3083a-121">An example Simple URL for dial-in might be https://dialin.contoso.com</span></span>
    
      - <span data-ttu-id="3083a-122">Para confirmar que la dirección URL de detección automática funciona, escriba https://lyncdiscover .</span><span class="sxs-lookup"><span data-stu-id="3083a-122">To confirm that the autodiscover URL is working, type https://lyncdiscover.</span></span> <span data-ttu-id="3083a-123">externaldomainFQDN.</span><span class="sxs-lookup"><span data-stu-id="3083a-123">externaldomainFQDN.</span></span> <span data-ttu-id="3083a-124">El explorador debe pedirle que abra un archivo.</span><span class="sxs-lookup"><span data-stu-id="3083a-124">The browser should prompt you to open a file.</span></span> <span data-ttu-id="3083a-125">Seleccione Bloc de notas para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="3083a-125">Select Notepad to open it.</span></span> <span data-ttu-id="3083a-126">Una respuesta típica sería similar a:</span><span class="sxs-lookup"><span data-stu-id="3083a-126">A typical response would be similar to:</span></span>
        
            {"AccessLocation":"External","Root":{"Links":[{"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/domain","token":"Domain"},
            {"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/user","token":"User"},
            {"href":"https:\/\/lyncweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/oauth\/user","token":"OAuth"}]}}

<span data-ttu-id="3083a-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3083a-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

