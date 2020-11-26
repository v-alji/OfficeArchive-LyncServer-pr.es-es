---
title: 'Lync Server 2013: Configurar las contraseñas de cuenta de autenticación Kerberos'
description: 'Lync Server 2013: configuración de contraseñas de cuentas de autenticación Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Kerberos authentication account passwords
ms:assetid: b435f88e-4a77-4be7-b7e5-c17484303b74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412870(v=OCS.15)
ms:contentKeyID: 48185167
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614b1411f9454c39843f4e69cabbfc3b02986e51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423977"
---
# <a name="setting-up-kerberos-authentication-account-passwords-in-lync-server-2013"></a><span data-ttu-id="c268e-103">Configurar las contraseñas de cuenta de autenticación Kerberos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c268e-103">Setting up Kerberos authentication account passwords in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c268e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c268e-104">

<span> </span></span></span>

<span data-ttu-id="c268e-105">_**Última modificación del tema:** 2010-11-03_</span><span class="sxs-lookup"><span data-stu-id="c268e-105">_**Topic Last Modified:** 2010-11-03_</span></span>

<span data-ttu-id="c268e-106">Después de crear el objeto de equipo para la cuenta de autenticación Kerberos, puede configurar la contraseña de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c268e-106">After you create the computer object for the Kerberos authentication account, you can set up the password for the account.</span></span> <span data-ttu-id="c268e-107">Ejecute el cmdlet de Windows PowerShell para establecer la contraseña de la cuenta Kerberos en un servidor.</span><span class="sxs-lookup"><span data-stu-id="c268e-107">You run the Windows PowerShell cmdlet for setting the Kerberos account password on one server.</span></span> <span data-ttu-id="c268e-108">Puede establecer la contraseña en el objeto que ha creado para la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c268e-108">You can set the password on the object that you created for the Kerberos authentication.</span></span> <span data-ttu-id="c268e-109">La contraseña puede establecerse en un valor conocido pero, de forma predeterminada, es una contraseña aleatoria.</span><span class="sxs-lookup"><span data-stu-id="c268e-109">The password can be set to a known value, but by default is a random password.</span></span> <span data-ttu-id="c268e-110">La contraseña está disponible para todos los orígenes de autenticación Kerberos que usan la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c268e-110">The password is available to all Kerberos authentication sources that use the account.</span></span> <span data-ttu-id="c268e-111">Use los cmdlets de Windows PowerShell para configurar y administrar las contraseñas de las cuentas de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c268e-111">You use Windows PowerShell cmdlets to set up and manage Kerberos account passwords.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c268e-112">El objeto de cuenta Kerberos es un objeto de equipo, pero usa el parámetro Cuentadeusuario para las operaciones de los cmdlets de Windows PowerShell a los que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="c268e-112">The Kerberos account object is a computer object, but uses the UserAccount parameter for operations in the Windows PowerShell cmdlets that are referenced.</span></span> <span data-ttu-id="c268e-113">Tenga en cuenta que no se trata de un error, pero el comportamiento previsto para el cmdlet cuando se usa con la creación y el mantenimiento de la cuenta de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c268e-113">Note that this is not a mistake, but the intended behavior of the cmdlet when used with the Kerberos account creation and maintenance.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c268e-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c268e-114">In This Section</span></span>

  - [<span data-ttu-id="c268e-115">Establecer una contraseña de cuenta de autenticación Kerberos en un servidor en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c268e-115">Set a Kerberos authentication account password on a server in Lync Server 2013</span></span>](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md)

  - [<span data-ttu-id="c268e-116">Sincronizar una contraseña de cuenta de autenticación Kerberos con IIS en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c268e-116">Synchronize a Kerberos authentication account password to IIS in Lync Server 2013</span></span>](lync-server-2013-synchronize-a-kerberos-authentication-account-password-to-iis.md)

<span data-ttu-id="c268e-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c268e-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

