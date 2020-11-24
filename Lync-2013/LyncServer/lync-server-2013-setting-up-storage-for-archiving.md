---
title: 'Lync Server 2013: configuración del almacenamiento para archivar'
description: 'Lync Server 2013: configuración del almacenamiento para archivar.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up storage for Archiving
ms:assetid: f751245c-743e-454f-8325-968ae5e3de71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205392(v=OCS.15)
ms:contentKeyID: 48185858
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7ee431b17b31c49ace7fae1f90d79ec6de2ada4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398135"
---
# <a name="setting-up-storage-for-archiving-in-lync-server-2013"></a>Configurar almacenamiento para archivar en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-12-17_

El almacenamiento de archivado para Lync Server 2013 incluye lo siguiente:

  - **Almacenamiento de datos**   El almacenamiento de datos es necesario para almacenar el contenido de mensajes instantáneos.

  - **Almacenamiento de archivos**   El almacenamiento de archivos es necesario para almacenar conferencias (reunión) contenido de datos y almacenamiento de archivos.

<div>

## <a name="setting-up-data-storage"></a>Configurar el almacenamiento de datos

Los requisitos para configurar el almacenamiento de datos para archivar en Lync Server 2013 dependen de cómo quiera almacenar los datos de archivado:

  - Integre el archivado de Lync Server 2013 con su implementación de Exchange para almacenar datos de archivado con el almacenamiento de Exchange.

  - Configure servidores de base de datos de SQL Server independientes para almacenar los datos de archivado.

<div>

## <a name="setting-up-exchange-storage-for-archiving-data"></a>Configurar el almacenamiento de Exchange para archivar datos

La configuración de Exchange para el almacenamiento de datos de archivado requiere que su implementación de Exchange ejecute Exchange 2013. Además, los buzones de usuario deben estar alojados en el servidor de Exchange 2013 y sus buzones deben ponerse en espera de In-Place. Para obtener más información sobre cómo configurar 2013 de Exchange, consulte la documentación del producto de Exchange.

</div>

<div>

## <a name="setting-up-sql-server-database-servers-for-storage-of-archiving-data"></a>Configurar servidores de base de datos de SQL Server para el almacenamiento de datos de archivado

El archivado en Lync Server 2013 requiere que el software de base de datos de SQL Server almacene los datos archivados, a menos que integre su implementación con Exchange.

Para bases de datos de archivado de SQL Server, debe instalar SQL Server en el equipo que hospedará la base de datos de archivado. Puede usar la misma instancia de SQL que usa para la base de datos back-end de un grupo de servidores front-end. Para obtener un rendimiento óptimo, debe implementar la base de datos de archivado en un equipo que sea independiente del almacén de administración central. Para obtener más información sobre los componentes de collocating Lync Server 2013, consulte [collocation de servidor compatibles en Lync server 2013](lync-server-2013-supported-server-collocation.md) en la documentación de soporte técnico.

Cada servidor de base de datos debe estar ejecutando una versión compatible de SQL Server. Para obtener más información sobre las versiones compatibles, consulte [requisitos técnicos para archivar en Lync Server 2013](lync-server-2013-technical-requirements-for-archiving.md) en la documentación de planeación.

Debe configurar las plataformas de SQL Server antes de implementar y habilitar el archivado. Si la cuenta que se usará para publicar la topología tiene los derechos y permisos de administrador apropiados, puede crear la base de datos de archivado (LcsLog) al publicar la topología. También puede crear la base de datos más adelante, incluyendo como parte del procedimiento de instalación. Para obtener más información sobre SQL Server, consulte SQL Server TechCenter en [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045) .

<div>


> [!NOTE]  
> Asegúrese de que el tipo de inicio del servicio Agente SQL Server sea automático y de que el servicio Agente SQL Server se esté ejecutando para la instancia de SQL que contiene la base de datos de archivado, de modo que el trabajo de mantenimiento de SQL Server predeterminado pueda ejecutarse de acuerdo con el control del servicio Agente SQL Server.



</div>

</div>

</div>

<div>

## <a name="setting-up-file-storage"></a>Configurar el almacenamiento de archivos

El archivado usa el recurso compartido de archivos 2013 de Lync Server que especificó al configurar el grupo de servidores front-end o el servidor Standard Edition. No puede cambiar el recurso compartido de archivos que se usa para el archivado. Para obtener detalles sobre los sistemas de almacenamiento de archivos admitidos, vea [compatibilidad de almacenamiento de archivos en Lync Server 2013](lync-server-2013-file-storage-support.md) en la documentación de soporte técnico.

</div>

</div>

<span> </span>

</div>

</div>

</div>

