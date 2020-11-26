---
title: 'Lync Server 2013: crear una directiva de archivado para habilitar o deshabilitar el archivado de las comunicaciones internas o externas de determinados sitios o usuarios'
description: 'Lync Server 2013: crear una directiva de archivado para habilitar o deshabilitar el archivado de las comunicaciones internas o externas de determinados sitios o usuarios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431991"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a>Crear una directiva de archivado en Lync Server 2013 para habilitar o deshabilitar el archivado de las comunicaciones internas o externas para usuarios o sitios específicos

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-02-23_

En Lync Server 2013, se usan directivas para habilitar y deshabilitar el archivado de comunicaciones internas y comunicaciones externas para usuarios alojados en Lync Server 2013. Esto incluye las siguientes directivas de archivado:

  - Una directiva global que se crea de forma predeterminada al implementar Lync Server 2013.

  - Directivas opcionales a nivel de sitio y de usuario que puede crear y usar para especificar cómo se implementa el archivado para usuarios o sitios específicos.

Inicialmente, debe configurar las directivas de archivado al implementar el archivado, pero puede cambiar, agregar y eliminar directivas después de la implementación. En el panel de control de Lync Server 2013, puede usar la página **Directiva de archivado** del grupo **archivado y supervisión** para administrar directivas a nivel global, nivel de sitio y nivel de usuario. Si integra el almacenamiento de Lync Server con el almacenamiento de Exchange 2013, las directivas de usuario de Exchange tienen prioridad sobre las directivas de archivado de Lync Server 2013.

Para obtener más información sobre cómo se implementan las directivas, incluida la jerarquía de directivas, consulte [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, la documentación de implementación o la documentación de operaciones.

<div>


> [!NOTE]
> Para controlar la implementación de archivado, debe especificar las opciones para archivar las configuraciones, por ejemplo, si desea archivar la mensajería instantánea o la Conferencia, el uso del modo crítico y las opciones de depuración. De forma predeterminada, no se habilita ninguna opción en la configuración global de archivado ni en ninguna configuración de archivado de sitios o grupos. Debe especificar todas las opciones apropiadas en las configuraciones de archivado antes de habilitar el archivado de las comunicaciones internas o externas en las directivas de archivado. Para obtener más información, vea <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">administrar las opciones de configuración de archivado en Lync Server 2013 para su organización, sitios y grupos</A> en la documentación de operaciones.<BR>Si habilitó la integración de Microsoft Exchange para su implementación, las directivas de Exchange controlan si el archivado está habilitado para los usuarios que están alojados en Exchange 2013 y si sus buzones se ponen en espera In-Place. Para obtener más información, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configurar directivas para archivar en Lync Server 2013 al usar la integración de Exchange Server</A> en la documentación de implementación.



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a>Para crear una directiva de archivado para un sitio o usuarios

1.  Desde una cuenta de usuario que se asigne al rol CsArchivingAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.

2.  Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server. Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).

3.  En la barra de navegación izquierda, haga clic en **Supervisión y archivado** y, después, en **Directiva de archivado**.

4.  Haga clic en **Nuevo** y, luego, siga uno de estos procedimientos:
    
      - Para crear una directiva de archivado de nivel de sitio, haga clic en **Directiva del sitio** y, a continuación, en **seleccionar un sitio**, haga clic en el sitio al que se va a aplicar la Directiva.
    
      - Para crear una directiva de archivado de usuario, haga clic en **Directiva de usuario**.

5.  En **Directiva de archivado nueva**, haga lo siguiente:
    
      - En **Nombre**, especifique un nombre para la nueva directiva (por ejemplo, externalContoso).
    
      - En **Descripción**, proporcione información detallada sobre la función de la directiva (por ejemplo, directiva de archivado de usuarios externos para Contoso).
    
      - Para controlar el archivado de comunicaciones con usuarios internos, active o desactive la casilla **Archivar comunicaciones internas**.
    
      - Para controlar el archivado de comunicaciones externas, active o desactive la casilla **Archivar comunicaciones externas**.

6.  Haga clic en **Confirmar**.
    
    <div>
    

    > [!IMPORTANT]
    > La configuración de una directiva de usuario únicamente se aplica a los usuarios y grupos de usuarios específicos a los que aplica la directiva. Para obtener más información, consulte <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">aplicar una directiva de archivado a los usuarios en Lync Server 2013</A>

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a>Creación de una directiva de archivado mediante cmdlets de Windows PowerShell

Las directivas de archivado se pueden crear con Windows PowerShell y el cmdlet **Remove-CsArchivingPolicy** . Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell. Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a>Para crear una nueva Directiva de archivado en el ámbito del sitio

  - Este comando crea una directiva de archivado para el sitio Redmond:
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a>Para crear una nueva Directiva de archivado en el ámbito de cada usuario

  - Para crear una nueva Directiva de archivado en el ámbito de cada usuario, simplemente especifique una identidad única al crear la Directiva:
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a>Para crear una directiva de archivado que permita el archivado de sesiones de comunicaciones internas

  - Ya que no se especifican parámetros (excepto el parámetro obligatorio Identity) en los comandos anteriores, las nuevas directivas usarán los valores predeterminados para todas sus propiedades. Para crear directivas que usen otros valores de propiedades, basta con incluir el parámetro y el valor de parámetro correspondiente. Por ejemplo, para crear una directiva de archivado que permita el archivado de sesiones de mensajería instantánea interna, use un comando como este:
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a>Para crear una directiva de archivado que permita el archivado de sesiones de comunicaciones tanto internas como externas

  - Con la inclusión de varios parámetros se pueden cambiar varios valores de propiedad. Por ejemplo, este comando configura la nueva Directiva para archivar las sesiones de mensajería instantánea internas y externas:
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

Para obtener más información, vea el tema de ayuda sobre el cmdlet [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) .

</div>

<div>

## <a name="see-also"></a>Vea también


[Administrar el archivado de comunicaciones internas y externas en Lync Server 2013](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

