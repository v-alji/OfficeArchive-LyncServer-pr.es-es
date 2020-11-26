---
title: 'Lync Server 2013: requisitos de la aplicación de la tienda Windows de Lync'
description: 'Lync Server 2013: requisitos de la aplicación de la tienda Windows de Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Windows Store app requirements
ms:assetid: 5f2e0a40-8450-4f61-b6f6-913fc1906020
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ823129(v=OCS.15)
ms:contentKeyID: 50120200
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17e8705a55625bcf0ad099ead1000a82c994d867
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426171"
---
# <a name="lync-windows-store-app-requirements-for-lync-server-2013"></a><span data-ttu-id="2cf9d-103">Requisitos de la aplicación de la tienda Windows de Lync para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2cf9d-103">Lync Windows Store app requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2cf9d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2cf9d-104">

<span> </span></span></span>

<span data-ttu-id="2cf9d-105">_**Última modificación del tema:** 2013-12-03_</span><span class="sxs-lookup"><span data-stu-id="2cf9d-105">_**Topic Last Modified:** 2013-12-03_</span></span>

<span data-ttu-id="2cf9d-106">Las organizaciones con una implementación local de Lync Server deben cumplir los siguientes requisitos para admitir la aplicación de la tienda Windows de Lync.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-106">Organizations with an on-premises deployment of Lync Server must meet the following requirements to support Lync Windows Store app.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2cf9d-107">Para Lync Server 2010, ejecute la actualización acumulativa para Lync Server 2010: febrero de 2012 (disponible en <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2670352"> https://go.microsoft.com/fwlink/?linkid=3052&amp ; kbid = 2670352</A>) o posterior en todos los servidores.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-107">For Lync Server 2010, run the cumulative update for Lync Server 2010: February 2012 (available at <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2670352">https://go.microsoft.com/fwlink/?linkid=3052&amp;kbid=2670352</A>) or later on all servers.</span></span> <span data-ttu-id="2cf9d-108">Para permitir que los usuarios se unan a reuniones, ejecute la actualización acumulativa para Lync Server 2010:2012 de octubre (disponible en <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2737915"> https://go.microsoft.com/fwlink/?linkid=3052&amp ; kbid = 2737915</A>) en los servidores.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-108">To enable users to join meetings, run the cumulative update for Lync Server 2010: October 2012 (available at <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2737915">https://go.microsoft.com/fwlink/?linkid=3052&amp;kbid=2737915</A>) on the servers.</span></span>



</div>

  - <span data-ttu-id="2cf9d-109">Habilite la detección automática, Lync Web App y los servicios de vale Web en el servidor.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-109">Enable the Autodiscover, Lync Web App, and Web Ticket services on the server.</span></span>

  - <span data-ttu-id="2cf9d-110">Habilitar la autenticación de certificados en el servidor front-end o en el grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-110">Enable certificate authentication on the Front End Server or Front End pool.</span></span> <span data-ttu-id="2cf9d-111">(El proceso de registro del usuario en el servidor front-end o en el grupo de servidores front-end se suele denominar registrar). Para obtener más información, consulte [crear opciones de configuración de registrar en Lync Server 2013](lync-server-2013-create-registrar-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="2cf9d-111">(The user registration process on the Front End Server or Front End pool is often referred to as the registrar.) For details, see [Create Registrar configuration settings in Lync Server 2013](lync-server-2013-create-registrar-configuration-settings.md).</span></span>

  - <span data-ttu-id="2cf9d-112">Publique los registros de recursos de alias DNS (CNAME) del servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-112">Publish the DNS alias (CNAME) resource records for the Autodiscover service.</span></span>

  - <span data-ttu-id="2cf9d-113">Ya no es necesario asegurarse de que el punto de distribución (CDP) de la lista de revocación de certificados (CRL) para los certificados emitidos para Lync Server apunta a un recurso HTTP en lugar de a un recurso LDAP.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-113">It is no longer a requirement to make sure the Certificate Revocation List (CRL) Distribution Point (CDP) for the certificates issued to Lync server points to an HTTP resource instead of an LDAP resource.</span></span> <span data-ttu-id="2cf9d-114">Sin embargo, asegúrese de que los equipos cliente tienen instaladas las actualizaciones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-114">However, make sure that client computers have the latest Windows updates installed.</span></span>

  - <span data-ttu-id="2cf9d-115">Configure servidores proxy HTTP en la empresa para permitir el tráfico HTTP relacionado con Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-115">Configure HTTP proxies in the enterprise to allow Lync server related HTTP traffic.</span></span>  <span data-ttu-id="2cf9d-116">Agregue excepciones para la detección automática, Lync Web App y servicios webticket, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-116">Add exceptions for the Autodiscover, Lync Web App, and WebTicket services, if necessary.</span></span>

  - <span data-ttu-id="2cf9d-117">En los clientes, instale Windows 8,1 y la última versión de la aplicación de la tienda Windows de Lync para corregir un problema de inicio de sesión que generalmente se produce al usar varios dominios (por ejemplo, cuando el URI SIP está **Usera@domainZ.com** , pero el servidor perimetral es **SIP.domainX.com**).</span><span class="sxs-lookup"><span data-stu-id="2cf9d-117">On clients, install Windows 8.1 and the latest version of Lync Windows Store app to fix a sign-in issue that generally occurs when using multiple domains (for example, when the SIP URI is **userA@domainZ.com** but the Edge Server is **sip.domainX.com**).</span></span>

<span data-ttu-id="2cf9d-118">Si su organización se suscribe a Lync Online o a Microsoft 365 y está usando su propio nombre de dominio, debe realizar algunos pasos adicionales para configurar la red para el descubrimiento automático de los servidores de Lync.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-118">If your organization subscribes to Lync Online or Microsoft 365 and you are using your own domain name, you must take some extra steps to set up your network for autodiscovery of the Lync servers.</span></span> <span data-ttu-id="2cf9d-119">Los requisitos de configuración de red son los mismos para la aplicación de la tienda Windows de Lync y Lync en dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-119">The network configuration requirements are the same for Lync Windows Store app and Lync on mobile devices.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="2cf9d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cf9d-120">See Also</span></span>


[<span data-ttu-id="2cf9d-121">Implementación de la aplicación de la tienda Windows de Lync en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2cf9d-121">Deploying Lync Windows Store app in Lync Server 2013</span></span>](lync-server-2013-deploying-lync-windows-store-app.md)  
  

<span data-ttu-id="2cf9d-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2cf9d-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
