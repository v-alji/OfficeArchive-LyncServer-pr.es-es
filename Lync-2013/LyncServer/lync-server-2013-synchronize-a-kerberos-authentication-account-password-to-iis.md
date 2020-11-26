---
title: Sincronizar una contraseña de cuenta de autenticación Kerberos con IIS
description: Sincronizar una contraseña de una cuenta de autenticación Kerberos con IIS.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Synchronize a Kerberos authentication account password to IIS
ms:assetid: 05925a66-2684-4c1b-adfa-69bd0da1bf38
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398107(v=OCS.15)
ms:contentKeyID: 48183296
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59555fc25088d0d932105f77051f959b4bcebb46
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444591"
---
# <a name="synchronize-a-kerberos-authentication-account-password-to-iis-in-lync-server-2013"></a><span data-ttu-id="ff4ca-103">Sincronizar una contraseña de cuenta de autenticación Kerberos con IIS en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff4ca-103">Synchronize a Kerberos authentication account password to IIS in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ff4ca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ff4ca-104">

<span> </span></span></span>

<span data-ttu-id="ff4ca-105">_**Última modificación del tema:** 2010-11-08_</span><span class="sxs-lookup"><span data-stu-id="ff4ca-105">_**Topic Last Modified:** 2010-11-08_</span></span>

<span data-ttu-id="ff4ca-106">Para completar correctamente este procedimiento, debe haber iniciado sesión como un usuario que sea miembro del grupo RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="ff4ca-107">En un sitio, los servidores front-end, los servidores Standard Edition y los directores pueden usar una cuenta de autenticación Kerberos para autenticar solicitudes en el servicio de servicios Web.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-107">In a site, Front End Servers, Standard Edition servers, and Directors can use a Kerberos authentication account for purposes of authenticating requests to the Web Services service.</span></span> <span data-ttu-id="ff4ca-108">En este procedimiento se busca cada servidor que ejecuta servicios web en un sitio al que se le ha asignado una cuenta de Kerberos y se actualizan los valores de configuración de servicios de Internet Information Server (IIS) para usar la cuenta de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-108">This procedure locates each server running Web Services in a site that has been assigned a Kerberos account and updates the Internet Information Services (IIS) configuration settings to use the Kerberos account.</span></span> <span data-ttu-id="ff4ca-109">Para obtener más información, vea [establecer una contraseña de cuenta de autenticación Kerberos en un servidor de Lync server 2013](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md).</span><span class="sxs-lookup"><span data-stu-id="ff4ca-109">For details, see [Set a Kerberos authentication account password on a server in Lync Server 2013](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md).</span></span>

<div>

## <a name="to-set-and-configure-a-kerberos-authentication-account-password"></a><span data-ttu-id="ff4ca-110">Para establecer y configurar una contraseña de cuenta de autenticación Kerberos</span><span class="sxs-lookup"><span data-stu-id="ff4ca-110">To set and configure a Kerberos authentication account password</span></span>

1.  <span data-ttu-id="ff4ca-111">Inicie sesión en un equipo de origen (como fe01.contoso.com) como miembro del grupo RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-111">Log on to a source computer (such as fe01.contoso.com) as a member of RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="ff4ca-112">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ff4ca-113">Desde la línea de comandos del shell de administración de Lync Server, ejecute los dos comandos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ff4ca-113">From the Lync Server Management Shell command line, run the following two commands:</span></span>
    
        Set-CsKerberosAccountPassword -FromComputer SourceComputer -ToComputer DestinationComputer
    
    <span data-ttu-id="ff4ca-114">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ff4ca-114">For example:</span></span>
    
        Set-CsKerberosAccountPassword -FromComputer fe01.contoso.com -ToComputer dir01.contoso.com
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="ff4ca-115">El nombre del equipo de origen y del equipo de destino debe ser un nombre de dominio completo (FQDN) del servidor.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-115">The name of the source computer and destination computer must be a fully qualified domain (FQDN) name of the server.</span></span> <span data-ttu-id="ff4ca-116">No puede usar el FQDN del grupo de servidores a menos que el nombre de la sección sea el mismo que el nombre del equipo que está usando como equipo de origen o equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-116">You cannot use the pool FQDN unless the pool name is the same as the name of the computer that you are using as a source computer or destination computer.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="ff4ca-117">Después de realizar cambios en la autenticación Kerberos, como agregar una cuenta o quitar una cuenta, debe ejecutar <STRONG>enable-CsTopology</STRONG> desde el símbolo del sistema del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-117">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="ff4ca-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ff4ca-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

