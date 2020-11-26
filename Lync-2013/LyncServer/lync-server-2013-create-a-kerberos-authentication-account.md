---
title: 'Lync Server 2013: Crear una cuenta de autenticación Kerberos'
description: 'Lync Server 2013: crear una cuenta de autenticación Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a Kerberos authentication account
ms:assetid: 63f0cef6-562a-4209-ae25-71f8dc7c7295
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398449(v=OCS.15)
ms:contentKeyID: 48184348
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f8e87a8ffcc95af4a44e516ac4e1f4d635d737
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432180"
---
# <a name="create-a-kerberos-authentication-account-in-lync-server-2013"></a><span data-ttu-id="c2b1b-103">Crear una cuenta de autenticación Kerberos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2b1b-103">Create a Kerberos authentication account in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c2b1b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c2b1b-104">

<span> </span></span></span>

<span data-ttu-id="c2b1b-105">_**Última modificación del tema:** 2012-01-02_</span><span class="sxs-lookup"><span data-stu-id="c2b1b-105">_**Topic Last Modified:** 2012-01-02_</span></span>

<span data-ttu-id="c2b1b-106">Para completar correctamente este procedimiento, debe haber iniciado sesión en el servidor o dominio como miembro del grupo administradores de dominio.</span><span class="sxs-lookup"><span data-stu-id="c2b1b-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group.</span></span>

<span data-ttu-id="c2b1b-107">Puede crear cuentas de autenticación Kerberos para cada sitio o puede crear una sola cuenta de autenticación Kerberos y usarla para todos los sitios.</span><span class="sxs-lookup"><span data-stu-id="c2b1b-107">You can create Kerberos authentication accounts for each site or you can create a single Kerberos authentication account and use it for all sites.</span></span> <span data-ttu-id="c2b1b-108">Use los cmdlets de Windows PowerShell para crear y administrar las cuentas, incluida la identificación de las cuentas asignadas a cada sitio.</span><span class="sxs-lookup"><span data-stu-id="c2b1b-108">You use Windows PowerShell cmdlets to create and manage the accounts, including identifying the accounts assigned to each site.</span></span> <span data-ttu-id="c2b1b-109">El generador de topología y el panel de control de Lync Server 2013 no muestran cuentas de autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c2b1b-109">Topology Builder and the Lync Server 2013 Control Panel do not display Kerberos authentication accounts.</span></span> <span data-ttu-id="c2b1b-110">Use el procedimiento siguiente para crear una o más cuentas de usuario para usarlas en la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c2b1b-110">Use the following procedure to create one or more user accounts to be used for Kerberos authentication.</span></span>

<div>

## <a name="to-create-a-kerberos-account"></a><span data-ttu-id="c2b1b-111">Para crear una cuenta de Kerberos</span><span class="sxs-lookup"><span data-stu-id="c2b1b-111">To create a Kerberos account</span></span>

1.  <span data-ttu-id="c2b1b-112">Como miembro del grupo administradores de dominio, inicie sesión en un equipo del dominio que ejecute Lync Server 2013 o en un equipo en el que estén instaladas las herramientas administrativas.</span><span class="sxs-lookup"><span data-stu-id="c2b1b-112">As a member of the Domain Admins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="c2b1b-113">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="c2b1b-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="c2b1b-114">En la línea de comandos, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="c2b1b-114">From the command line, run the following command:</span></span>
    
        New-CsKerberosAccount -UserAccount "Domain\UserAccount" -ContainerDN "CN=Users,DC=DomainName,DC=DomainExtension"
    
    <span data-ttu-id="c2b1b-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c2b1b-115">For example:</span></span>
    
        New-CsKerberosAccount -UserAccount "Contoso\KerbAuth" -ContainerDN "CN=Users,DC=contoso,DC=com"

4.  <span data-ttu-id="c2b1b-116">Confirme que el objeto de equipo se creó al abrir usuarios y equipos de Active Directory, expanda el contenedor **usuarios** y, a continuación, confirme que el objeto de equipo de la cuenta de usuario se encuentra en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="c2b1b-116">Confirm that the Computer object was created by opening Active Directory User and Computers, expand the **Users** container, and then confirm that the Computer object for the user account is in the container.</span></span>

<span data-ttu-id="c2b1b-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c2b1b-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

