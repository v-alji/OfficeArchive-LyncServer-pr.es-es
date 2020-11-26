---
title: 'Lync Server 2013: administración del servicio de libreta de direcciones'
description: 'Lync Server 2013: administración del servicio de libreta de direcciones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering the Address Book Service
ms:assetid: 801e4243-9670-4477-aa2f-88b61ecf5351
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429711(v=OCS.15)
ms:contentKeyID: 48184649
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 86d549b06b5c6ac1c450edf9e7edb0b902ef9adf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440699"
---
# <a name="administering-the-address-book-service-in-lync-server-2013"></a><span data-ttu-id="d5aec-103">Administrar el servicio de libreta de direcciones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5aec-103">Administering the Address Book Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5aec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5aec-104">

<span> </span></span></span>

<span data-ttu-id="d5aec-105">_**Última modificación del tema:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="d5aec-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="d5aec-106">Como parte de la implementación de Lync Server, Enterprise Edition o Standard Edition Server, el servicio de libreta de direcciones se instala de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d5aec-106">As a part of the deployment of Lync Server, Enterprise Edition or Standard Edition server, the Address Book Service is installed by default.</span></span> <span data-ttu-id="d5aec-107">La base de datos que usa el servicio de libreta de direcciones, RTCab, se crea en el servidor SQL (para Enterprise Edition, que es el servidor SQL Server de servicios de fondo; en el servidor Standard Edition, el servidor SQL Server en el que se proviene).</span><span class="sxs-lookup"><span data-stu-id="d5aec-107">The database used by the Address Book Service – RTCab – is created on the SQL Server (for Enterprise Edition, this is the back-end SQL Server; for Standard Edition server, the collocated SQL Server).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d5aec-108">Para obtener información sobre el uso de <STRONG>ADSI Edit</STRONG> para editar atributos de objetos de Active Directory Domain Services, consulte <A href="https://go.microsoft.com/fwlink/?linkid=330427">ADSI Edit</A>.</span><span class="sxs-lookup"><span data-stu-id="d5aec-108">For information about using <STRONG>ADSI Edit</STRONG> to edit Active Directory Domain Services object attributes, see <A href="https://go.microsoft.com/fwlink/?linkid=330427">ADSI Edit</A>.</span></span> <span data-ttu-id="d5aec-109">Para obtener información sobre una herramienta del kit de recursos específicamente para el servicio de libreta de direcciones, consulte <A href="https://go.microsoft.com/fwlink/?linkid=330429">herramientas del kit de recursos de Microsoft Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d5aec-109">For information about a tool in the Resource Kit specifically for the Address Book service, see <A href="https://go.microsoft.com/fwlink/?linkid=330429">Microsoft Lync Server 2013 Resource Kit Tools</A>.</span></span>



</div>

<div>

## <a name="address-book-server-phone-number-normalization"></a><span data-ttu-id="d5aec-110">Normalización del número de teléfono del servidor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="d5aec-110">Address Book Server Phone Number Normalization</span></span>

<span data-ttu-id="d5aec-111">Lync Server requiere el estándar RFC 3966/E. 164 números de teléfono.</span><span class="sxs-lookup"><span data-stu-id="d5aec-111">Lync Server requires standardized RFC 3966/E.164 phone numbers.</span></span> <span data-ttu-id="d5aec-112">Para usar números de teléfono que no se hayan estructurado o que tengan un formato incoherente, Lync Server depende del servidor de la libreta de direcciones para preprocesar los números de teléfono antes de que se entreguen a las reglas de normalización.</span><span class="sxs-lookup"><span data-stu-id="d5aec-112">To use phone numbers that are unstructured or inconsistently formatted, Lync Server relies on the Address Book Server to preprocess phone numbers before they are handed off to the normalization rules.</span></span> <span data-ttu-id="d5aec-113">Cuando se usa un número de teléfono de la libreta de direcciones y se aplica la regla de normalización, los clientes, como Lync Phone Edition y Lync Mobile, pueden usar estos números normalizados.</span><span class="sxs-lookup"><span data-stu-id="d5aec-113">When a phone number is used from the address book and the normalization rule is applied, clients, such as Lync Phone Edition and Lync Mobile, can use these normalized numbers.</span></span>

<span data-ttu-id="d5aec-114">Es posible que las reglas de normalización que se usaron en versiones anteriores no funcionen correctamente sin algunos ajustes.</span><span class="sxs-lookup"><span data-stu-id="d5aec-114">The normalization rules that were used in previous versions may not work properly without some adjustments.</span></span> <span data-ttu-id="d5aec-115">Dado que los espacios en blanco y los caracteres no obligatorios se quitan antes de las reglas de normalización, si la expresión de Regex está buscando específicamente un guión u otro carácter que se ha quitado, es posible que la regla de normalización no se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="d5aec-115">Because the white space and non-mandatory characters are removed prior to the normalization rules, if your regex expression is specifically looking for a dash or other character that was removed, your normalization rule might fail.</span></span> <span data-ttu-id="d5aec-116">Debe revisar las reglas de normalización para asegurarse de que no busquen estos caracteres no obligatorios o de que la regla puede dar error y continuar en el caso de que el carácter no se presente donde la regla se anticipe.</span><span class="sxs-lookup"><span data-stu-id="d5aec-116">You should review your normalization rules to ensure that either they are not looking for these non-mandatory characters, or that the rule can fail gracefully and continue in the event that the character is not present where the rule anticipates it will be.</span></span>

</div>

<div>

## <a name="user-replicator-and-address-book-server"></a><span data-ttu-id="d5aec-117">Duplicador de usuarios y servidor de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="d5aec-117">User Replicator and Address Book Server</span></span>

<span data-ttu-id="d5aec-118">El servidor de la libreta de direcciones utiliza los datos proporcionados por el replicador de usuarios para actualizar la información que obtiene inicialmente de la lista global de direcciones (GAL).</span><span class="sxs-lookup"><span data-stu-id="d5aec-118">The Address Book Server uses data provided by User Replicator to update the information that it initially obtains from the global address list (GAL).</span></span> <span data-ttu-id="d5aec-119">El replicador de usuarios escribe los atributos de los servicios de dominio de Active Directory para cada usuario, contacto y grupo en la tabla AbUserEntry de la base de datos y el servidor de la libreta de direcciones sincroniza los datos de usuario de la base de datos en los archivos del almacén de archivos del servidor de la libreta de direcciones y en la base de datos de la libreta de direcciones RTCab</span><span class="sxs-lookup"><span data-stu-id="d5aec-119">User Replicator writes the Active Directory Domain Services attributes for each user, contact, and group into the AbUserEntry table in the database and the Address Book Server syncs the user data from the database into files in the Address Book Server file store and into the Address Book database RTCab.</span></span> <span data-ttu-id="d5aec-120">El esquema de la tabla AbUserEntry usa dos columnas: **UserGuid** y **UserData**.</span><span class="sxs-lookup"><span data-stu-id="d5aec-120">The schema for the AbUserEntry table uses two columns, **UserGuid** and **UserData**.</span></span> <span data-ttu-id="d5aec-121">**UserGuid** es la columna de índice y contiene el GUID de 16 bytes del objeto de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d5aec-121">**UserGuid** is the index column and contains the 16-byte GUID of the Active Directory object.</span></span> <span data-ttu-id="d5aec-122">**UserData** es una columna de imagen que contiene todos los atributos de servicios de dominio de Active Directory mencionados anteriormente para ese contacto.</span><span class="sxs-lookup"><span data-stu-id="d5aec-122">**UserData** is an image column which contains all of the previously mentioned Active Directory Domain Services attributes for that contact.</span></span>

<span data-ttu-id="d5aec-123">El replicador de usuarios determina qué atributos de Active Directory se escribirán leyendo una tabla de configuración que se encuentra en la misma instancia basada en SQL Server que la tabla AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="d5aec-123">User Replicator determines which Active Directory attributes to write by reading a configuration table located in the same SQL Server-based instance as the AbUserEntry table.</span></span> <span data-ttu-id="d5aec-124">La tabla ABAttribute contiene tres columnas: **ID**, **Name**, **Flags** y **enable**.</span><span class="sxs-lookup"><span data-stu-id="d5aec-124">The AbAttribute table contains three columns, **ID**, **Name**, **Flags**, and **Enable**.</span></span> <span data-ttu-id="d5aec-125">La tabla se crea durante la configuración de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d5aec-125">The table is created during database setup.</span></span> <span data-ttu-id="d5aec-126">Si la tabla ABAttribute está vacía, User Replicator omite su lógica de procesamiento de la tabla AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="d5aec-126">If the AbAttribute table is empty, User Replicator skips its AbUserEntry table processing logic.</span></span> <span data-ttu-id="d5aec-127">Los atributos del servidor de la libreta de direcciones son dinámicos y se recuperan de la tabla ABAttribute, que inicialmente escribe el servidor de la libreta de direcciones cuando se activa el servidor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d5aec-127">Address Book Server attributes are dynamic and are retrieved from the AbAttribute table, which is initially written by the Address Book Server when the Address Book Server is activated.</span></span>

<span data-ttu-id="d5aec-128">La activación del servidor de la libreta de direcciones rellena la tabla abattributes con los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d5aec-128">Address Book Server activation populates the AbAttribute table with the values shown in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5aec-129">ID</span><span class="sxs-lookup"><span data-stu-id="d5aec-129">ID</span></span></th>
<th><span data-ttu-id="d5aec-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="d5aec-130">Name</span></span></th>
<th><span data-ttu-id="d5aec-131">Marcas</span><span class="sxs-lookup"><span data-stu-id="d5aec-131">Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-132">1</span><span class="sxs-lookup"><span data-stu-id="d5aec-132">1</span></span></p></td>
<td><p><span data-ttu-id="d5aec-133">givenName</span><span class="sxs-lookup"><span data-stu-id="d5aec-133">givenName</span></span></p></td>
<td><p><span data-ttu-id="d5aec-134">0x01400000</span><span class="sxs-lookup"><span data-stu-id="d5aec-134">0x01400000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-135">2</span><span class="sxs-lookup"><span data-stu-id="d5aec-135">2</span></span></p></td>
<td><p><span data-ttu-id="d5aec-136">Utilidad</span><span class="sxs-lookup"><span data-stu-id="d5aec-136">Sn</span></span></p></td>
<td><p><span data-ttu-id="d5aec-137">0x02400000</span><span class="sxs-lookup"><span data-stu-id="d5aec-137">0x02400000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-138">3</span><span class="sxs-lookup"><span data-stu-id="d5aec-138">3</span></span></p></td>
<td><p><span data-ttu-id="d5aec-139">Nunca</span><span class="sxs-lookup"><span data-stu-id="d5aec-139">displayName</span></span></p></td>
<td><p><span data-ttu-id="d5aec-140">0x03420000</span><span class="sxs-lookup"><span data-stu-id="d5aec-140">0x03420000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-141">4</span><span class="sxs-lookup"><span data-stu-id="d5aec-141">4</span></span></p></td>
<td><p><span data-ttu-id="d5aec-142">Título</span><span class="sxs-lookup"><span data-stu-id="d5aec-142">Title</span></span></p></td>
<td><p><span data-ttu-id="d5aec-143">0x04000000</span><span class="sxs-lookup"><span data-stu-id="d5aec-143">0x04000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-144">5</span><span class="sxs-lookup"><span data-stu-id="d5aec-144">5</span></span></p></td>
<td><p><span data-ttu-id="d5aec-145">mailNickname</span><span class="sxs-lookup"><span data-stu-id="d5aec-145">mailNickname</span></span></p></td>
<td><p><span data-ttu-id="d5aec-146">0x05400000</span><span class="sxs-lookup"><span data-stu-id="d5aec-146">0x05400000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-147">6</span><span class="sxs-lookup"><span data-stu-id="d5aec-147">6</span></span></p></td>
<td><p><span data-ttu-id="d5aec-148">Compañía</span><span class="sxs-lookup"><span data-stu-id="d5aec-148">Company</span></span></p></td>
<td><p><span data-ttu-id="d5aec-149">0x06000000</span><span class="sxs-lookup"><span data-stu-id="d5aec-149">0x06000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-150">7</span><span class="sxs-lookup"><span data-stu-id="d5aec-150">7</span></span></p></td>
<td><p><span data-ttu-id="d5aec-151">physicalDeliveryOfficeName</span><span class="sxs-lookup"><span data-stu-id="d5aec-151">physicalDeliveryOfficeName</span></span></p></td>
<td><p><span data-ttu-id="d5aec-152">0x07000000</span><span class="sxs-lookup"><span data-stu-id="d5aec-152">0x07000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-153">4,8</span><span class="sxs-lookup"><span data-stu-id="d5aec-153">8</span></span></p></td>
<td><p><span data-ttu-id="d5aec-154">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="d5aec-154">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="d5aec-155">0x08520C00</span><span class="sxs-lookup"><span data-stu-id="d5aec-155">0x08520C00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-156">99,999</span><span class="sxs-lookup"><span data-stu-id="d5aec-156">9</span></span></p></td>
<td><p><span data-ttu-id="d5aec-157">NúmeroDeTeléfono</span><span class="sxs-lookup"><span data-stu-id="d5aec-157">telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="d5aec-158">0x09022800</span><span class="sxs-lookup"><span data-stu-id="d5aec-158">0x09022800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-159">base10</span><span class="sxs-lookup"><span data-stu-id="d5aec-159">10</span></span></p></td>
<td><p><span data-ttu-id="d5aec-160">Teléfono particular</span><span class="sxs-lookup"><span data-stu-id="d5aec-160">homePhone</span></span></p></td>
<td><p><span data-ttu-id="d5aec-161">0x0A302800</span><span class="sxs-lookup"><span data-stu-id="d5aec-161">0x0A302800</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-162">once</span><span class="sxs-lookup"><span data-stu-id="d5aec-162">11</span></span></p></td>
<td><p><span data-ttu-id="d5aec-163">Móvil</span><span class="sxs-lookup"><span data-stu-id="d5aec-163">Mobile</span></span></p></td>
<td><p><span data-ttu-id="d5aec-164">0x0B622800</span><span class="sxs-lookup"><span data-stu-id="d5aec-164">0x0B622800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-165">2007</span><span class="sxs-lookup"><span data-stu-id="d5aec-165">12</span></span></p></td>
<td><p><span data-ttu-id="d5aec-166">otherTelephone</span><span class="sxs-lookup"><span data-stu-id="d5aec-166">otherTelephone</span></span></p></td>
<td><p><span data-ttu-id="d5aec-167">0x0C302000</span><span class="sxs-lookup"><span data-stu-id="d5aec-167">0x0C302000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-168">13</span><span class="sxs-lookup"><span data-stu-id="d5aec-168">13</span></span></p></td>
<td><p><span data-ttu-id="d5aec-169">ipPhone</span><span class="sxs-lookup"><span data-stu-id="d5aec-169">ipPhone</span></span></p></td>
<td><p><span data-ttu-id="d5aec-170">0x0D302000</span><span class="sxs-lookup"><span data-stu-id="d5aec-170">0x0D302000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-171">14</span><span class="sxs-lookup"><span data-stu-id="d5aec-171">14</span></span></p></td>
<td><p><span data-ttu-id="d5aec-172">Tales</span><span class="sxs-lookup"><span data-stu-id="d5aec-172">Mail</span></span></p></td>
<td><p><span data-ttu-id="d5aec-173">0x0E500000</span><span class="sxs-lookup"><span data-stu-id="d5aec-173">0x0E500000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-174">4,5</span><span class="sxs-lookup"><span data-stu-id="d5aec-174">15</span></span></p></td>
<td><p><span data-ttu-id="d5aec-175">groupType</span><span class="sxs-lookup"><span data-stu-id="d5aec-175">groupType</span></span></p></td>
<td><p><span data-ttu-id="d5aec-176">0x0F010800</span><span class="sxs-lookup"><span data-stu-id="d5aec-176">0x0F010800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-177">apartado</span><span class="sxs-lookup"><span data-stu-id="d5aec-177">16</span></span></p></td>
<td><p><span data-ttu-id="d5aec-178">Grandes</span><span class="sxs-lookup"><span data-stu-id="d5aec-178">Department</span></span></p></td>
<td><p><span data-ttu-id="d5aec-179">0x10000000</span><span class="sxs-lookup"><span data-stu-id="d5aec-179">0x10000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-180">apartado</span><span class="sxs-lookup"><span data-stu-id="d5aec-180">17</span></span></p></td>
<td><p><span data-ttu-id="d5aec-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5aec-181">Description</span></span></p></td>
<td><p><span data-ttu-id="d5aec-182">0x11000100</span><span class="sxs-lookup"><span data-stu-id="d5aec-182">0x11000100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-183">18</span><span class="sxs-lookup"><span data-stu-id="d5aec-183">18</span></span></p></td>
<td><p><span data-ttu-id="d5aec-184">Administrador</span><span class="sxs-lookup"><span data-stu-id="d5aec-184">Manager</span></span></p></td>
<td><p><span data-ttu-id="d5aec-185">0x12040001</span><span class="sxs-lookup"><span data-stu-id="d5aec-185">0x12040001</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-186">19</span><span class="sxs-lookup"><span data-stu-id="d5aec-186">19</span></span></p></td>
<td><p><span data-ttu-id="d5aec-187">proxyAddress</span><span class="sxs-lookup"><span data-stu-id="d5aec-187">proxyAddress</span></span></p></td>
<td><p><span data-ttu-id="d5aec-188">0x00500105</span><span class="sxs-lookup"><span data-stu-id="d5aec-188">0x00500105</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-189">veinte</span><span class="sxs-lookup"><span data-stu-id="d5aec-189">20</span></span></p></td>
<td><p><span data-ttu-id="d5aec-190">msExchHideFromAddressLists</span><span class="sxs-lookup"><span data-stu-id="d5aec-190">msExchHideFromAddressLists</span></span></p></td>
<td><p><span data-ttu-id="d5aec-191">0xFF000003</span><span class="sxs-lookup"><span data-stu-id="d5aec-191">0xFF000003</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-192">99</span><span class="sxs-lookup"><span data-stu-id="d5aec-192">99</span></span></p></td>
<td><p><span data-ttu-id="d5aec-193">entryID</span><span class="sxs-lookup"><span data-stu-id="d5aec-193">entryID</span></span></p></td>
<td><p><span data-ttu-id="d5aec-194">0x99000000</span><span class="sxs-lookup"><span data-stu-id="d5aec-194">0x99000000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d5aec-195">Los números de la columna **identificador** deben ser únicos y nunca se deben volver a usar.</span><span class="sxs-lookup"><span data-stu-id="d5aec-195">The numbers in the **ID** column must be unique and should never be reused.</span></span> <span data-ttu-id="d5aec-196">Además, mantener los valores de identificador en 256 ahorra espacio en los archivos de salida escritos por el servidor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d5aec-196">Also, keeping the ID values under 256 saves space in the output files written by the Address Book Server.</span></span> <span data-ttu-id="d5aec-197">Sin embargo, el valor del identificador máximo es 65535.</span><span class="sxs-lookup"><span data-stu-id="d5aec-197">However, the maximum ID value is 65535.</span></span> <span data-ttu-id="d5aec-198">La columna **nombre** corresponde al nombre del atributo de Active Directory que el replicador de usuarios debe incluir en la tabla AbUserEntry por cada contacto.</span><span class="sxs-lookup"><span data-stu-id="d5aec-198">The **Name** column corresponds to the Active Directory attribute name that User Replicator should put in the AbUserEntry table for each contact.</span></span> <span data-ttu-id="d5aec-199">El valor de la columna **Flags** se usa para definir el tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="d5aec-199">The value in the **Flags** column is used to define the type of attribute.</span></span> <span data-ttu-id="d5aec-200">Los siguientes tipos de atributos del servidor de la libreta de direcciones son reconocidos por el replicador de usuarios, indicado por el byte bajo del valor de la columna **marcas** .</span><span class="sxs-lookup"><span data-stu-id="d5aec-200">The following types of Address Book Server attributes are recognized by User Replicator, indicated by the low byte of the value in the **Flags** column.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5aec-201">Atributo</span><span class="sxs-lookup"><span data-stu-id="d5aec-201">Attribute</span></span></th>
<th><span data-ttu-id="d5aec-202">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5aec-202">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-203">0X0</span><span class="sxs-lookup"><span data-stu-id="d5aec-203">0x0</span></span></p></td>
<td><p><span data-ttu-id="d5aec-204">Un atributo de cadena.</span><span class="sxs-lookup"><span data-stu-id="d5aec-204">A string attribute.</span></span> <span data-ttu-id="d5aec-205">El replicador de usuarios convierte este tipo en UTF-8 antes de almacenarlo en la tabla AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="d5aec-205">User Replicator converts this type to UTF-8 before storing it in the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-206">0x1</span><span class="sxs-lookup"><span data-stu-id="d5aec-206">0x1</span></span></p></td>
<td><p><span data-ttu-id="d5aec-207">Un atributo binario.</span><span class="sxs-lookup"><span data-stu-id="d5aec-207">A binary attribute.</span></span> <span data-ttu-id="d5aec-208">El replicador de usuarios almacena este objeto en el BLOB sin ninguna conversión.</span><span class="sxs-lookup"><span data-stu-id="d5aec-208">User Replicator stores this in the blob without any conversion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-209">0X2</span><span class="sxs-lookup"><span data-stu-id="d5aec-209">0x2</span></span></p></td>
<td><p><span data-ttu-id="d5aec-210">Un atributo de cadena, pero se incluye solo si el valor del atributo comienza por &quot; Tel: &quot; .</span><span class="sxs-lookup"><span data-stu-id="d5aec-210">A string attribute, but is included only if the attribute value begins with &quot;tel:&quot;.</span></span> <span data-ttu-id="d5aec-211">Esto se redestina principalmente a los atributos de cadena de valor múltiple, en concreto <strong>proxyAddresses</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5aec-211">This is primarily for multi-valued string attributes, specifically <strong>proxyAddresses</strong>.</span></span> <span data-ttu-id="d5aec-212">En este caso, el servidor de la libreta de direcciones solo está interesado en las entradas de <strong>proxyAddresses</strong> que comienzan con &quot; Tel: &quot; .</span><span class="sxs-lookup"><span data-stu-id="d5aec-212">In this case, Address Book Server is interested only in <strong>proxyAddresses</strong> entries that begin with &quot;tel:&quot;.</span></span> <span data-ttu-id="d5aec-213">Por lo tanto, en interés de ahorrar espacio, User Replicator almacena solo las entradas que comienzan con &quot; Tel: &quot; .</span><span class="sxs-lookup"><span data-stu-id="d5aec-213">Therefore, in the interest of saving space, User Replicator stores only the entries that begin with &quot;tel:&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-214">0X3</span><span class="sxs-lookup"><span data-stu-id="d5aec-214">0x3</span></span></p></td>
<td><p><span data-ttu-id="d5aec-215">Un atributo de cadena booleana, que si es verdadero hace que el replicador de usuarios no incluya este contacto en la tabla AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="d5aec-215">A Boolean string attribute, which if TRUE causes User Replicator to not include this contact in the AbUserEntry table.</span></span> <span data-ttu-id="d5aec-216">Si es falso, hace que el replicador de usuarios incluya los atributos de este contacto en la tabla AbUserEntry, pero no en el atributo concreto con este indicador.</span><span class="sxs-lookup"><span data-stu-id="d5aec-216">If FALSE, it causes User Replicator to include the attributes for this contact in the AbUserEntry table, but not the particular attribute with this flag.</span></span> <span data-ttu-id="d5aec-217">Este es otro tipo especial de caso que es principalmente para el atributo <strong>msExchHideFromAddressLists</strong> .</span><span class="sxs-lookup"><span data-stu-id="d5aec-217">This is another special case type that is primarily for the <strong>msExchHideFromAddressLists</strong> attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-218">0x4</span><span class="sxs-lookup"><span data-stu-id="d5aec-218">0x4</span></span></p></td>
<td><p><span data-ttu-id="d5aec-219">Un atributo de cadena, pero se incluye solo si el valor del atributo comienza por &quot; SMTP: &quot; e incluye el &quot; @ &quot; símbolo.</span><span class="sxs-lookup"><span data-stu-id="d5aec-219">A string attribute, but is included only if the attribute value begins with &quot;smtp:&quot; and includes the &quot;@&quot; symbol.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-220">0X5</span><span class="sxs-lookup"><span data-stu-id="d5aec-220">0x5</span></span></p></td>
<td><p><span data-ttu-id="d5aec-221">Un atributo de cadena, pero se incluye solo si el valor del atributo comienza por &quot; Tel: &quot; o &quot; SMTP: &quot; e incluye el &quot; @ &quot; símbolo.</span><span class="sxs-lookup"><span data-stu-id="d5aec-221">A string attribute, but is included only if the attribute value begins with either &quot;tel:&quot; or &quot;smtp:&quot; and includes the &quot;@&quot; symbol.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-222">0x100</span><span class="sxs-lookup"><span data-stu-id="d5aec-222">0x100</span></span></p></td>
<td><p><span data-ttu-id="d5aec-223">Si se establece, se trata de un atributo de valor múltiple que puede aparecer más de una vez para cada contacto.</span><span class="sxs-lookup"><span data-stu-id="d5aec-223">If set, this is a multi-valued attribute that can appear more than once for each contact.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-224">0x400</span><span class="sxs-lookup"><span data-stu-id="d5aec-224">0x400</span></span></p></td>
<td><p><span data-ttu-id="d5aec-225">Si se establece, se identifica el atributo de nombre de cuenta de usuario de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="d5aec-225">If set, this identifies the email user account name attribute for a contact.</span></span> <span data-ttu-id="d5aec-226">El servidor de la libreta de direcciones usa esta marca para identificar qué valor de atributo se muestra en la entrada del registro de eventos de normalización del teléfono.</span><span class="sxs-lookup"><span data-stu-id="d5aec-226">Address Book Server uses this flag to identify which attribute value to show in the phone normalization event log entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-227">0x800</span><span class="sxs-lookup"><span data-stu-id="d5aec-227">0x800</span></span></p></td>
<td><p><span data-ttu-id="d5aec-228">Si se establece, identifica un atributo obligatorio para un contacto.</span><span class="sxs-lookup"><span data-stu-id="d5aec-228">If set, this identifies a required attribute for a contact.</span></span> <span data-ttu-id="d5aec-229">El servidor de la libreta de direcciones incluye un usuario en la tabla AbUserEntry solo si hay un valor para este atributo en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d5aec-229">Address Book Server includes a user in the AbUserEntry table only if there is a value for this attribute in Active Directory.</span></span> <span data-ttu-id="d5aec-230">Si hay más de un atributo obligatorio, solo uno de ellos necesita tener un valor para incluir al usuario en la tabla AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="d5aec-230">If there is more than one required attribute, only one of them is required to have a value to include the user in the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-231">ó</span><span class="sxs-lookup"><span data-stu-id="d5aec-231">0x1000</span></span></p></td>
<td><p><span data-ttu-id="d5aec-232">Si se establece, el servidor de la libreta de direcciones siempre normaliza el valor de este atributo.</span><span class="sxs-lookup"><span data-stu-id="d5aec-232">If set, Address Book Server always normalizes the value of this attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-233">0x2000</span><span class="sxs-lookup"><span data-stu-id="d5aec-233">0x2000</span></span></p></td>
<td><p><span data-ttu-id="d5aec-234">Si se establece, el servidor de la libreta de direcciones usa el número normalizado de <strong>proxyAddresses</strong>, si la configuración de <strong>USENORMALIZATIONRULES</strong> CMS es falsa. de lo contrario, se comporta igual que cuando el bit de la marca es 0x1000.</span><span class="sxs-lookup"><span data-stu-id="d5aec-234">If set, Address Book Server uses the normalized number from <strong>proxyAddresses</strong>, if the <strong>UseNormalizationRules</strong> CMS setting is FALSE; otherwise it behaves the same as when the flag bit is 0x1000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-235">0x4000</span><span class="sxs-lookup"><span data-stu-id="d5aec-235">0x4000</span></span></p></td>
<td><p><span data-ttu-id="d5aec-236">Si se establece, el servidor de la libreta de direcciones no incluye los objetos de la tabla AbUserEntry que tienen este valor para el atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="d5aec-236">If set, Address Book Server does not include objects in the AbUserEntry table that have this value for the specified attribute.</span></span> <span data-ttu-id="d5aec-237">Por ejemplo, si el atributo <strong>msRTCSIP-PrimaryUserAddress</strong> tiene este bit de marca establecido, los contactos que tienen este atributo no se escriben en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d5aec-237">For example, if the <strong>msRTCSIP-PrimaryUserAddress</strong> attribute has this flag bit set, then contacts that have this attribute are not written to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-238">0x8000</span><span class="sxs-lookup"><span data-stu-id="d5aec-238">0x8000</span></span></p></td>
<td><p><span data-ttu-id="d5aec-239">Si se establece, el servidor de la libreta de direcciones no incluye los objetos de la tabla AbUserEntry que no tienen este valor para el atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="d5aec-239">If set, Address Book Server does not include objects in the AbUserEntry table that do not have this value for the specified attribute.</span></span> <span data-ttu-id="d5aec-240">Si se establecen los bits de indicador 0x4000 y 0x8000 en un objeto, el atributo con el valor de bit de indicador establecido en 0x4000 tiene prioridad y el objeto se excluye de la tabla AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="d5aec-240">If both the 0x4000 and 0x8000 flag bits are set on an object, the attribute with the flag bit value set to 0x4000 takes precedence, and the object is excluded from the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-241">0x10000</span><span class="sxs-lookup"><span data-stu-id="d5aec-241">0x10000</span></span></p></td>
<td><p><span data-ttu-id="d5aec-242">Si se establece, representa un objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="d5aec-242">If set, this represents a group object.</span></span> <span data-ttu-id="d5aec-243">Replicador de usuarios usa este bit de marca para incluir contactos con el atributo <strong>GroupType</strong> cuya presencia indica un grupo (por ejemplo, una lista de distribución o un grupo de seguridad).</span><span class="sxs-lookup"><span data-stu-id="d5aec-243">User Replicator uses this flag bit to include contacts with the <strong>groupType</strong> attribute whose presence indicates a group (for example, a distribution list or security group).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-244">0x20000</span><span class="sxs-lookup"><span data-stu-id="d5aec-244">0x20000</span></span></p></td>
<td><p><span data-ttu-id="d5aec-245">Si se establece, User Replicator usa este bit de marca para incluir este atributo en los archivos del servidor de la libreta de direcciones específicos del dispositivo (es decir, los archivos con la extensión. DABS).</span><span class="sxs-lookup"><span data-stu-id="d5aec-245">If set, User Replicator uses this flag bit to include this attribute in device-specific Address Book Server files (that is, files with a .dabs extension).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d5aec-246">En versiones anteriores de Lync Server, al aplicar un cambio en Active Directory, el administrador tendría que ejecutar **Update-CSUserDatabase** y **Update – CSAddressBook** cmdlets de Windows PowerShell para conservar el cambio en la base de datos de usuario de Lync Server y RTCab de inmediato.</span><span class="sxs-lookup"><span data-stu-id="d5aec-246">In previous versions of Lync Server, when applying a change to Active Directory, the administrator would be required to run **Update -CSUserDatabase** and **Update –CSAddressBook** Windows PowerShell cmdlets to persist the change to the Lync Server user database and RTCab database immediately.</span></span> <span data-ttu-id="d5aec-247">En Lync Server 2013, el replicador de usuarios de Lync Server atenderá los cambios de Active Directory y actualizará la base de datos de usuarios de Lync Server en función de un intervalo configurado.</span><span class="sxs-lookup"><span data-stu-id="d5aec-247">In Lync Server 2013, Lync Server User Replicator will pick up the changes from Active Directory and update the Lync Server user database based on a configured interval.</span></span> <span data-ttu-id="d5aec-248">El replicador de usuarios de Lync Server también propagará los cambios a la base de datos de RTCab rápidamente sin que el Administrador tenga que ejecutar Update-CSAddressBook.</span><span class="sxs-lookup"><span data-stu-id="d5aec-248">Lync Server User Replicator will also propagate the changes to the RTCab database quickly without the administrator having to run Update-CSAddressBook.</span></span> <span data-ttu-id="d5aec-249">Si la consulta Web de libreta de direcciones está habilitada, los cambios se reflejarán en los resultados de búsqueda de los clientes de Lync.</span><span class="sxs-lookup"><span data-stu-id="d5aec-249">If Address Book Web query is enabled, then the changes will be reflected in search results by Lync clients.</span></span> <span data-ttu-id="d5aec-250">Los administradores solo tendrán que ejecutar Update-CSAddressBook si está habilitada la descarga del archivo de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d5aec-250">Administrators will only need to run Update -CSAddressBook if the Address Book file download is enabled.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d5aec-251">De forma predeterminada, el replicador de usuarios de Lync Server se ejecuta automáticamente cada 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="d5aec-251">By default Lync Server User Replicator runs automatically every 5 minutes.</span></span> <span data-ttu-id="d5aec-252">Puede configurar este intervalo mediante Set-CSUserReplicatorConfiguration-ReplicationCycleInterval &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="d5aec-252">You can configure this interval by using Set -CSUserReplicatorConfiguration -ReplicationCycleInterval &lt;&gt;.</span></span>



</div>

</div>

<div>

## <a name="filtering-the-address-book"></a><span data-ttu-id="d5aec-253">Filtrar la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="d5aec-253">Filtering the Address Book</span></span>

<span data-ttu-id="d5aec-254">Los usuarios rellenados en los archivos del servidor de la libreta de direcciones se pueden controlar en función de determinados atributos de servicios de dominio de Active Directory enumerados en la tabla ABAttribute.</span><span class="sxs-lookup"><span data-stu-id="d5aec-254">The users populated in the Address Book Server files can be controlled based on certain Active Directory Domain Services attributes listed in the AbAttribute table.</span></span> <span data-ttu-id="d5aec-255">Un atributo de este tipo utilizado para filtrar es el atributo **msExchangeHideFromAddressBook** .</span><span class="sxs-lookup"><span data-stu-id="d5aec-255">One such attribute used for filtering is the **msExchangeHideFromAddressBook** attribute.</span></span> <span data-ttu-id="d5aec-256">Este es un atributo de usuario agregado por el esquema de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5aec-256">This is a user attribute added by the Exchange schema.</span></span> <span data-ttu-id="d5aec-257">Si el valor de este atributo es verdadero, Exchange Server usa este atributo para ocultar el contacto de la lista global de direcciones (GAL) de Outlook.</span><span class="sxs-lookup"><span data-stu-id="d5aec-257">If the value of this attribute is TRUE, Exchange Server uses this attribute to hide the contact from the Outlook Global Address List (GAL).</span></span> <span data-ttu-id="d5aec-258">De forma similar, si el valor de este atributo es TRUE, User Replicator no incluye a ese usuario en la tabla AbUserEntry y este usuario no estará en los archivos del servidor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d5aec-258">Similarly, if the value of this attribute is TRUE, User Replicator does not include that user in the AbUserEntry table and this user will not be in the Address Book Server files.</span></span>

<span data-ttu-id="d5aec-259">Puede usar algunos bits de la bandera para definir un filtro que se usará en los atributos del servidor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d5aec-259">You can use some flag bits to define a filter to use on Address Book Server attributes.</span></span> <span data-ttu-id="d5aec-260">Por ejemplo, la presencia de ciertos bits de indicador puede identificar un atributo como un atributo Include o un atributo exclude.</span><span class="sxs-lookup"><span data-stu-id="d5aec-260">For example, the presence of certain flag bits can identify an attribute as an include attribute or an exclude attribute.</span></span> <span data-ttu-id="d5aec-261">El duplicador de usuarios filtra los contactos que contienen un atributo de exclusión y filtra los contiene que no contienen un atributo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="d5aec-261">User Replicator filters out contacts that contain an exclude attribute and filters out contains that do not contain an include attribute.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="d5aec-262">Para obtener más información sobre cómo filtrar la libreta de direcciones, consulte <A href="https://technet.microsoft.com/library/gg415643(v=ocs.15)">cmdlets del servidor de la libreta de direcciones en Lync Server 2013</A>y <A href="https://go.microsoft.com/fwlink/?linkid=330430">filtrar la libreta de direcciones de Lync 2013</A></span><span class="sxs-lookup"><span data-stu-id="d5aec-262">For more information about filtering the Address Book, see <A href="https://technet.microsoft.com/library/gg415643(v=ocs.15)">Address Book Server cmdlets in Lync Server 2013</A>, and <A href="https://go.microsoft.com/fwlink/?linkid=330430">Filter Lync 2013 address book</A></span></span>



</div>

<span data-ttu-id="d5aec-263">Actualmente, hay tres filtros diferentes.</span><span class="sxs-lookup"><span data-stu-id="d5aec-263">Currently, there are three different filters.</span></span> <span data-ttu-id="d5aec-264">En la tabla siguiente se enumeran estos filtros.</span><span class="sxs-lookup"><span data-stu-id="d5aec-264">The following table lists these filters.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5aec-265">Atributo</span><span class="sxs-lookup"><span data-stu-id="d5aec-265">Attribute</span></span></th>
<th><span data-ttu-id="d5aec-266">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5aec-266">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-267">0x800</span><span class="sxs-lookup"><span data-stu-id="d5aec-267">0x800</span></span></p></td>
<td><p><span data-ttu-id="d5aec-268">Si se establece, identifica un atributo obligatorio para un contacto.</span><span class="sxs-lookup"><span data-stu-id="d5aec-268">If set, this identifies a required attribute for a contact.</span></span> <span data-ttu-id="d5aec-269">Replicador de usuarios usa este bit de marca para filtrar los contactos que no contienen al menos un atributo requerido.</span><span class="sxs-lookup"><span data-stu-id="d5aec-269">User Replicator uses this flag bit to filter out contacts that do not contain at least one required attribute.</span></span> <span data-ttu-id="d5aec-270">El OuPathId es un atributo obligatorio, que siempre se establece.</span><span class="sxs-lookup"><span data-stu-id="d5aec-270">The OuPathId is a required attribute, which is always set.</span></span> <span data-ttu-id="d5aec-271">Por lo tanto, se debe establecer al menos uno de los atributos obligatorios.</span><span class="sxs-lookup"><span data-stu-id="d5aec-271">So at least one of other required attributes should be set.</span></span> <span data-ttu-id="d5aec-272">De lo contrario, el valor de Contact (es decir, con el valor de atributo requerido OuPathId) aún no se escribirá en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d5aec-272">Otherwise, contact (that is, with value of required attribute OuPathId) will still not be written to database.</span></span> <span data-ttu-id="d5aec-273">Por ejemplo, si <strong>telephoneNumber</strong> y <strong>teléfono particular</strong> se definen como atributos necesarios, solo los contactos que tengan al menos uno de estos atributos se escribirán en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d5aec-273">For example, if <strong>telephoneNumber</strong> and <strong>homePhone</strong> are defined as required attributes, only the contacts that have at least one of these attributes are written to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5aec-274">0x4000</span><span class="sxs-lookup"><span data-stu-id="d5aec-274">0x4000</span></span></p></td>
<td><p><span data-ttu-id="d5aec-275">Si se establece, esto identifica un atributo exclude.</span><span class="sxs-lookup"><span data-stu-id="d5aec-275">If set, this identifies an exclude attribute.</span></span> <span data-ttu-id="d5aec-276">Replicador de usuarios usa este bit de marca para filtrar los contactos que contienen este atributo.</span><span class="sxs-lookup"><span data-stu-id="d5aec-276">User Replicator uses this flag bit to filter out contacts that contain this attribute.</span></span> <span data-ttu-id="d5aec-277">Por ejemplo, si <strong>msRTCSIP-PrimaryUserAddress</strong> se define como un atributo Exclude, los contactos que tienen este atributo no se escriben en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d5aec-277">For example, if <strong>msRTCSIP-PrimaryUserAddress</strong> is defined as an exclude attribute, contacts that have this attribute are not written to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5aec-278">0x8000</span><span class="sxs-lookup"><span data-stu-id="d5aec-278">0x8000</span></span></p></td>
<td><p><span data-ttu-id="d5aec-279">Si se establece, esto identifica un atributo Include.</span><span class="sxs-lookup"><span data-stu-id="d5aec-279">If set, this identifies an include attribute.</span></span> <span data-ttu-id="d5aec-280">Replicador de usuarios usa este bit de marca para filtrar los contactos que no contienen este atributo.</span><span class="sxs-lookup"><span data-stu-id="d5aec-280">User Replicator uses this flag bit to filter out contacts that do not contain this attribute.</span></span> <span data-ttu-id="d5aec-281">Por ejemplo, si <strong>msRTCSIP-PrimaryUserAddress</strong> se define como un atributo Include, solo los contactos que tienen este atributo se escriben en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d5aec-281">For example, if <strong>msRTCSIP-PrimaryUserAddress</strong> is defined as an include attribute, only the contacts that have this attribute are written to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="d5aec-282">Si se establecen los bits de indicador 0x4000 (atributo Exclude) y 0x8000 (include Attribute), el bit 0x4000 reemplaza el valor de 0x8000 bit y se excluye el contacto.</span><span class="sxs-lookup"><span data-stu-id="d5aec-282">If both the 0x4000 (exclude attribute) and 0x8000 (include attribute) flag bits are set, the 0x4000 bit overrides the 0x8000 bit and the contact is excluded.</span></span>



</div>

<span data-ttu-id="d5aec-283">Aunque puede filtrar la libreta de direcciones para incluir solo algunos usuarios, la limitación de las entradas no limita la capacidad de otros usuarios de ponerse en contacto con los usuarios filtrados ni de ver su estado de presencia.</span><span class="sxs-lookup"><span data-stu-id="d5aec-283">Although you can filter the Address Book to include only certain users, limiting entries does not limit other users' ability to contact the filtered users or to see their presence status.</span></span> <span data-ttu-id="d5aec-284">Los usuarios siempre pueden encontrarse, enviar mensajes instantáneos manualmente o iniciar llamadas manualmente a usuarios que no estén en la libreta de direcciones escribiendo el nombre de inicio de sesión completo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="d5aec-284">Users can always find, manually send instant messages, or manually initiate calls to users not in the Address Book by entering a user's complete sign-in name.</span></span> <span data-ttu-id="d5aec-285">Además, la información de contacto de un usuario también podría encontrarse en Outlook.</span><span class="sxs-lookup"><span data-stu-id="d5aec-285">Also, contact information for a user could also be found in Outlook.</span></span>

<span data-ttu-id="d5aec-286">Aunque la opción de registros de contactos completos en los archivos de la libreta de direcciones permite usar Lync Server para iniciar el correo electrónico, el teléfono o las llamadas de telefonía empresariales (es decir, si la telefonía IP empresarial está habilitada en el servidor) con usuarios que no están configurados para el protocolo de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="d5aec-286">While having full contact records in the Address Book files enables you to use Lync Server to initiate email, telephone, or Enterprise Voice calls (that is, if Enterprise Voice is enabled on the server) with users that are not configured for Session Initiation Protocol (SIP), some organizations prefer to include only SIP-enabled users in their Address Book Server entries.</span></span> <span data-ttu-id="d5aec-287">Puede filtrar la libreta de direcciones para incluir solo usuarios habilitados para SIP si desactiva la bit de 0x800 en la columna **Flags** de los siguientes atributos obligatorios: **mailNickname**, **telephoneNumber**, **teléfono particular** y **Mobile**.</span><span class="sxs-lookup"><span data-stu-id="d5aec-287">You can filter the Address Book to include only SIP-enabled users by clearing the 0x800 bit in the **Flags** column of the following required attributes: **mailNickname**, **telephoneNumber**, **homePhone**, and **mobile**.</span></span> <span data-ttu-id="d5aec-288">También puede filtrar la libreta de direcciones para incluir solo los usuarios habilitados para SIP mediante la configuración de 0x8000 (include Attribute) en la columna **Flags** del atributo **msRTCSIP-PrimaryUserAddress** .</span><span class="sxs-lookup"><span data-stu-id="d5aec-288">You can also filter the Address Book to include only SIP-enabled users by setting the 0x8000 (include attribute) in the **Flags** column of the **msRTCSIP-PrimaryUserAddress** attribute.</span></span> <span data-ttu-id="d5aec-289">Esto también ayuda a excluir cuentas de servicio de los archivos de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d5aec-289">This also helps to exclude service accounts from the Address Book files.</span></span>

<span data-ttu-id="d5aec-290">Después de modificar la tabla ABAttribute, puede actualizar los datos de la tabla AbUserEntry ejecutando el cmdlet **Update-CsUserDatabase** comando.</span><span class="sxs-lookup"><span data-stu-id="d5aec-290">After you modify the AbAttribute table, you can refresh the data in the AbUserEntry table by running the cmdlet **Update-CsUserDatabase** command.</span></span> <span data-ttu-id="d5aec-291">Después de que se complete la replicación de UR, puede actualizar el archivo en el almacén de archivos del servidor de la libreta de direcciones ejecutando manualmente el cmdlet **UpdateCsAddressBook** .</span><span class="sxs-lookup"><span data-stu-id="d5aec-291">After UR replication completes, you can update the file in the Address Book Server file store by manually running the cmdlet **UpdateCsAddressBook** command.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d5aec-292">El servidor front-end en el que se encuentra el servidor de la libreta de direcciones no se puede configurar de forma administrativa.</span><span class="sxs-lookup"><span data-stu-id="d5aec-292">The Front End Server that the Address Book Server is placed is not administratively configurable.</span></span> <span data-ttu-id="d5aec-293">Uno se elige durante la implementación (normalmente, el primer servidor front-end implementado).</span><span class="sxs-lookup"><span data-stu-id="d5aec-293">One is chosen during deployment—typically, the first Front End Server deployed.</span></span> <span data-ttu-id="d5aec-294">En el caso de que se produzca un error, el servicio de libreta de direcciones se moverá a otro servidor front-end y no requiere ninguna atención administrativa.</span><span class="sxs-lookup"><span data-stu-id="d5aec-294">In the event of failure, the Address Book Service will move to another Front End Server, and requires no administrative attention.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d5aec-295">Si ha consolidado o modificado de otra manera su infraestructura desde una implementación de varios bosques o de una implementación de principal/secundario (como consolidar su infraestructura antes de migrar a Lync Server), es posible que se produzcan errores en la descarga del servicio de libreta de direcciones y la consulta Web de la libreta de direcciones para algunos usuarios.</span><span class="sxs-lookup"><span data-stu-id="d5aec-295">If you have consolidated or otherwise modified your infrastructure from a multi-forest deployment or a parent/child deployment (such as consolidating your infrastructure before moving to Lync Server), you may find that the Address Book service download and the Address Book Web Query fails for some users.</span></span> <span data-ttu-id="d5aec-296">Cuando se encuentra en una implementación que tiene varios dominios o bosques, el atributo <STRONG>MsRTCSIP-OriginatorSid</STRONG> se rellena en los objetos de usuario que presentan el problema.</span><span class="sxs-lookup"><span data-stu-id="d5aec-296">When in a deployment that had multiple domains or forests, the attribute <STRONG>MsRTCSIP-OriginatorSid</STRONG> is populated on the user objects that are exhibiting the issue.</span></span> <span data-ttu-id="d5aec-297">El atributo <STRONG>MsRTCSIP-OriginatorSid</STRONG> debe establecerse en null en estos objetos para resolver el problema.</span><span class="sxs-lookup"><span data-stu-id="d5aec-297">The <STRONG>MsRTCSIP-OriginatorSid</STRONG> attribute must be set to NULL on these objects to resolve the issue.</span></span>



<span data-ttu-id="d5aec-298"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5aec-298"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

