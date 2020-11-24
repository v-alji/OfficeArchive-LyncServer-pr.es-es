---
title: Resumen de certificado - Grupo de director escalado, equilibrador de carga de hardware
description: 'Resumen de certificado: Grupo de directores de la carga del hardware.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Scaled Director pool, hardware load balancer
ms:assetid: 45940add-8027-418d-b79a-9033b494762f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204846(v=OCS.15)
ms:contentKeyID: 48183992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 08abc37940cd41a29d6620cfc0a2a801de4a8e38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399413"
---
# <a name="certificate-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a>Resumen de certificado - Grupo de director escalado, equilibrador de carga de hardware en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2012-10-20_

Los requisitos de certificado para un director con un equilibrador de carga de hardware usarán un certificado predeterminado que tiene un nombre de sujeto y nombres alternativos de asunto para los servicios que el grupo de directores puede recibir. Se solicita un certificado para cada director del grupo. Además, hay un certificado de token de OAuth para la autenticación de servidor a servidor que se instala en cada servidor.

### <a name="certificates-for-a-scaled-director-using-a-hardware-load-balancer"></a>Certificados para un director con escala usando un equilibrador de carga de hardware

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Nombre de sujeto</th>
<th>Nombres alternativos de asunto (SAN)</th>
<th>Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Predeterminado</p></td>
<td><p>dirpool01.contoso.net</p></td>
<td><p>dirpool01.contoso.net</p>
<p>dir01.contoso.net</p>
<p>dialin.contoso.com</p>
<p>meet.contoso.com</p>
<p>lyncdiscoverinternal.contoso.com</p>
<p>lyncdiscover.contoso.com</p>
<p>(Opcional) *. contoso.com</p></td>
<td><p>Los certificados de director se pueden solicitar desde una entidad de certificación (CA) administrada internamente o desde una CA pública.</p>
<p>El Director responde a las solicitudes del proxy inverso en el perímetro o del servidor perimetral.</p>
<p>O bien, una entrada comodín para las direcciones URL simples</p></td>
</tr>
<tr class="even">
<td><p>OAuthTokenIssuer</p></td>
<td><p>dir01.contoso.net</p></td>
<td><p>Ninguna entrada</p></td>
<td>


> [!IMPORTANT]
> Tenga en cuenta que la longitud de clave mínima es 1024, pero es posible que reciba una advertencia que indica que la longitud de clave mínima recomendada es de 2048 bits.


<p>El certificado OAuthTokenIssuer es un certificado de un único propósito para el propósito de autenticar servidores en un entorno de gran escala y se puede solicitar desde una entidad de certificación interna o desde una CA pública. El certificado es obligatorio.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

