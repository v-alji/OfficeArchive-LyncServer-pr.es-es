---
title: 'Lync Server 2013: mover usuarios a Lync Online'
description: 'Lync Server 2013: mover usuarios a Lync Online.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move users to Lync Online
ms:assetid: 6a523c86-2eac-4fa4-973a-4406872c9a7d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204969(v=OCS.15)
ms:contentKeyID: 48184392
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 501eda3a76cec3226831c0af3631317377cd82cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425279"
---
# <a name="move-users-to-lync-online-in-lync-server-2013"></a><span data-ttu-id="ab0d9-103">Mover usuarios a Lync Online en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab0d9-103">Move users to Lync Online in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab0d9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab0d9-104">

<span> </span></span></span>

<span data-ttu-id="ab0d9-105">_**Última modificación del tema:** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="ab0d9-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="ab0d9-106">Antes de empezar a migrar usuarios a Lync Online, debe realizar una copia de seguridad de los datos de usuario asociados a las cuentas que se van a mover.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-106">Before you start migrating users to Lync Online, you should backup the user data associated with the accounts to be moved.</span></span> <span data-ttu-id="ab0d9-107">No todos los datos de usuario se mueven con la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-107">Not all user data is moved with the user account.</span></span> <span data-ttu-id="ab0d9-108">Para obtener más información, vea [requisitos de copia de seguridad y restauración en Lync Server 2013: datos](lync-server-2013-backup-and-restoration-requirements-data.md).</span><span class="sxs-lookup"><span data-stu-id="ab0d9-108">For information, see [Backup and restoration requirements in Lync Server 2013: data](lync-server-2013-backup-and-restoration-requirements-data.md).</span></span>

<div>

## <a name="migrate-user-settings-to-lync-online"></a><span data-ttu-id="ab0d9-109">Migrar la configuración de usuario a Lync Online</span><span class="sxs-lookup"><span data-stu-id="ab0d9-109">Migrate User Settings to Lync Online</span></span>

<span data-ttu-id="ab0d9-110">La configuración de usuario se mueve con la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-110">User settings are moved with the user account.</span></span> <span data-ttu-id="ab0d9-111">Algunos valores de configuración locales no se mueven con la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-111">Some on-premises settings are not moved with the user account.</span></span>

</div>

<div>

## <a name="moving-pilot-users-to-lync-online"></a><span data-ttu-id="ab0d9-112">Mover los usuarios piloto a Lync Online</span><span class="sxs-lookup"><span data-stu-id="ab0d9-112">Moving Pilot Users to Lync Online</span></span>

<span data-ttu-id="ab0d9-113">Antes de empezar a mover usuarios a Lync Online, es posible que desee mover unos pocos usuarios piloto para confirmar que su entorno está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-113">Before you begin to move users to Lync Online, you may want to move a few pilot users to confirm that your environment is correctly configured.</span></span> <span data-ttu-id="ab0d9-114">Después, puede comprobar que las características y los servicios de Lync funcionan de la forma esperada antes de intentar mover usuarios adicionales.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-114">You can then verify that Lync features and services function as expected before attempting to move additional users.</span></span>

<span data-ttu-id="ab0d9-115">Para mover un usuario local a su inquilino de Lync Online, ejecute los siguientes cmdlets en el shell de administración de Lync Server, con las credenciales de administrador de su organización de Microsoft 365 u Office 365.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-115">To move an on-premises user to your Lync Online tenant, run the following cmdlets in the Lync Server Management Shell, using the administrator credentials for your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="ab0d9-116">Sustituya “username@contoso.com” por la información del usuario que quiera mover.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-116">Replace "username@contoso.com" with the information for the user that you want to move.</span></span>

   ```PowerShell
    $creds=Get-Credential
   ```

   ```PowerShell
    Move-CsUser -Identity username@contoso.com -Target sipfed.online.lync.com -Credential $creds -HostedMigrationOverrideUrl <URL>
   ```

<span data-ttu-id="ab0d9-117">El formato de la dirección URL especificada para el parámetro **HostedMigrationOverrideUrl** debe ser la dirección URL del grupo en el que se está ejecutando el servicio de migración hospedada, en el siguiente formato: https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.SVC.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-117">The format of the URL specified for the **HostedMigrationOverrideUrl** parameter must be the URL to the pool where the Hosted Migration service is running, in the following format: Https://\<Pool FQDN\>/HostedMigration/hostedmigrationService.svc.</span></span>

<span data-ttu-id="ab0d9-118">Para determinar la dirección URL del servicio de migración hospedada, consulte la URL del panel de control de Lync Online de la cuenta de la organización de Microsoft 365 u Office 365.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-118">You can determine the URL to the Hosted Migration Service by viewing the URL for the Lync Online Control Panel for your Microsoft 365 or Office 365 organization account.</span></span>

<span data-ttu-id="ab0d9-119">**Para determinar la dirección URL del servicio de migración hospedada de su organización**</span><span class="sxs-lookup"><span data-stu-id="ab0d9-119">**To determine the Hosted Migration Service URL for your organization**</span></span>

1.  <span data-ttu-id="ab0d9-120">Inicie sesión en su organización de Microsoft 365 u Office 365 como administrador.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-120">Login to your Microsoft 365 or Office 365 organization as an administrator.</span></span>

2.  <span data-ttu-id="ab0d9-121">Abra el **centro de administración de Lync**.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-121">Open the **Lync admin center**.</span></span>

3.  <span data-ttu-id="ab0d9-122">Con el **centro de administración de Lync** mostrado, seleccione y copie la dirección URL en la barra de direcciones hasta **Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-122">With the **Lync admin center** displayed, select and copy the URL in the address bar up to **lync.com**.</span></span> <span data-ttu-id="ab0d9-123">Una dirección URL de ejemplo es muy similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ab0d9-123">An example URL looks similar to the following:</span></span>
    
    `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`

4.  <span data-ttu-id="ab0d9-124">Sustituya **webdir** en la dirección URL por **admin**. Quedará como a continuación:</span><span class="sxs-lookup"><span data-stu-id="ab0d9-124">Replace **webdir** in the URL with **admin**, resulting in the following:</span></span>
    
    `https://admin0a.online.lync.com`

5.  <span data-ttu-id="ab0d9-125">Anexe la cadena siguiente a la URL: **/MigraciónHospedada/ServicioDeMigraciónHospedada.svc**.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-125">Append the following string to the URL: **/HostedMigration/hostedmigrationservice.svc**.</span></span>
    
    <span data-ttu-id="ab0d9-126">La dirección URL resultante, que es el valor de **HostedMigrationOverrideUrl**, necesita ser como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ab0d9-126">The resulting URL, which is the value of the **HostedMigrationOverrideUrl**, should look like the following:</span></span>
    
    `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`

</div>

<div>

## <a name="moving-users-to-lync-online"></a><span data-ttu-id="ab0d9-127">Mover usuarios a Lync Online</span><span class="sxs-lookup"><span data-stu-id="ab0d9-127">Moving Users to Lync Online</span></span>

<span data-ttu-id="ab0d9-128">Puede mover varios usuarios mediante el cmdlet [Get-CsUser](https://docs.microsoft.com/powershell/module/skype/Get-CsUser) con el parámetro – filter para seleccionar los usuarios con una propiedad específica asignada a las cuentas de usuario, como RegistrarPool.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-128">You can move multiple users by using the [Get-CsUser](https://docs.microsoft.com/powershell/module/skype/Get-CsUser) cmdlet with the –Filter parameter to select the users with a specific property assigned to the user accounts, such as RegistrarPool.</span></span> <span data-ttu-id="ab0d9-129">Después, puede canalizar los usuarios devueltos al cmdlet [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) , tal y como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-129">You can then pipe the returned users to the [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) cmdlet, as shown in the following example.</span></span>

    Get-CsUser -Filter {UserProperty -eq "UserPropertyValue"} | Move-CsUser -Target sipfed.online.lync.com -Credential $creds -HostedMigrationOverrideUrl <URL>

<span data-ttu-id="ab0d9-130">También puede usar el parámetro –OU para recuperar todos los usuarios del OU especificado, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-130">You can also use the –OU parameter to retrieve all users in the specified OU, as shown in the following example.</span></span>

    Get-CsUser -OU "cn=hybridusers,cn=contoso.." | Move-CsUser -Target sipfed.online.lync.com -Credentials $creds -HostedMigrationOverrideUrl <URL>

</div>

<div>

## <a name="verify-lync-online-user-settings-and-features"></a><span data-ttu-id="ab0d9-131">Comprobar las características y la configuración de usuario de Lync Online</span><span class="sxs-lookup"><span data-stu-id="ab0d9-131">Verify Lync Online User Settings and Features</span></span>

<span data-ttu-id="ab0d9-132">Puede comprobar que el usuario se ha movido correctamente de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="ab0d9-132">You can verify that the user was moved successfully in the following ways:</span></span>

  - <span data-ttu-id="ab0d9-133">Vea el estado del usuario en el panel de control de Lync Online.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-133">View the status of the user in the Lync Online Control Panel.</span></span> <span data-ttu-id="ab0d9-134">El indicador visual de los usuarios locales y los usuarios en línea es diferente.</span><span class="sxs-lookup"><span data-stu-id="ab0d9-134">The visual indicator for on-premises users and online users is different.</span></span>

  - <span data-ttu-id="ab0d9-135">Ejecute el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ab0d9-135">Run the following cmdlet:</span></span>
    
        Get-CsUser -Identity

<span data-ttu-id="ab0d9-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab0d9-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

