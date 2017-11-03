---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtenga carpetas especiales.
ms.openlocfilehash: 894c0dc2c41441ab8006f58dcf5ccbc9d0043b0a
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="get-a-special-folder-by-name"></a><span data-ttu-id="c3da1-102">Obtener una carpeta especial por su nombre</span><span class="sxs-lookup"><span data-stu-id="c3da1-102">Get a special folder by name</span></span>

<span data-ttu-id="c3da1-103">Use la colección especial para acceder a una carpeta especial por su nombre.</span><span class="sxs-lookup"><span data-stu-id="c3da1-103">Use the special collection to access a special folder by name.</span></span>

<span data-ttu-id="c3da1-p101">Las carpetas especiales proporcionan alias simples para acceder a carpetas conocidas en OneDrive sin necesidad de buscar la carpeta por su ruta (que requeriría localización) o hacer referencia a la carpeta con un identificador. Si una carpeta especial cambia de nombre o se mueve a otra ubicación de la unidad, esta sintaxis seguirá encontrando esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="c3da1-p101">Special folders provide simple aliases to access well-known folders in OneDrive without the need to look up the folder by path (which would require localization), or reference the folder with an ID. If a special folder is renamed or moved to another location within the drive, this syntax will continue to find that folder.</span></span>

<span data-ttu-id="c3da1-p102">Las carpetas especiales se crean de forma automática la primera vez que una aplicación intenta escribir en una, si aún no existe. Si un usuario elimina una, se vuelve a crear al volver a escribir en ella.</span><span class="sxs-lookup"><span data-stu-id="c3da1-p102">Special folders are automatically created the first time an application attempts to write to one, if it doesn't already exist. If a user deletes one, it is recreated when written to again.</span></span>

> <span data-ttu-id="c3da1-108">**Nota:**  Si tiene permisos de solo lectura y solicita una carpeta especial que no existe, recibirá un error `403 Forbidden`.</span><span class="sxs-lookup"><span data-stu-id="c3da1-108">**Note:**  If you have read-only permissions and request a special folder that doesn't exist, you'll receive a `403 Forbidden` error.</span></span>

## <a name="permissions"></a><span data-ttu-id="c3da1-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="c3da1-109">Permissions</span></span>

<span data-ttu-id="c3da1-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c3da1-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|            <span data-ttu-id="c3da1-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c3da1-112">Permission type</span></span>             |                                           <span data-ttu-id="c3da1-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c3da1-113">Permissions (from least to most privileged)</span></span>                                            |
| :------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="c3da1-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c3da1-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="c3da1-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3da1-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>                            |
| <span data-ttu-id="c3da1-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c3da1-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c3da1-117">Files.ReadWrite.AppFolder, Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3da1-117">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |
| <span data-ttu-id="c3da1-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c3da1-118">Application</span></span>                            | <span data-ttu-id="c3da1-119">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3da1-119">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>                                                         |

## <a name="http-request"></a><span data-ttu-id="c3da1-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c3da1-120">HTTP Request</span></span>

<!-- { "blockType": "request", "name": "get-special-folder", "scopes": "files.read" } -->

```http
GET /me/drive/special/{name}
```

### <a name="special-folder-names"></a><span data-ttu-id="c3da1-121">Nombres de carpetas especiales</span><span class="sxs-lookup"><span data-stu-id="c3da1-121">Special folder names</span></span>

<span data-ttu-id="c3da1-122">Los siguientes nombres de carpetas especiales están disponibles en OneDrive y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="c3da1-122">The follow special folder names are available in OneDrive and OneDrive for Business.</span></span>

| <span data-ttu-id="c3da1-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="c3da1-123">Name</span></span>        | <span data-ttu-id="c3da1-124">Id. de carpeta</span><span class="sxs-lookup"><span data-stu-id="c3da1-124">Folder id</span></span>    | <span data-ttu-id="c3da1-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3da1-125">Description</span></span>                                                              |
|:------------|:-------------|:-------------------------------------------------------------------------|
| <span data-ttu-id="c3da1-126">Documentos</span><span class="sxs-lookup"><span data-stu-id="c3da1-126">Documents</span></span>   | `documents`  | <span data-ttu-id="c3da1-127">La carpeta Documentos.</span><span class="sxs-lookup"><span data-stu-id="c3da1-127">The Documents folder.</span></span>                                                    |
| <span data-ttu-id="c3da1-128">Fotos</span><span class="sxs-lookup"><span data-stu-id="c3da1-128">Photos</span></span>      | `photos`     | <span data-ttu-id="c3da1-129">La carpeta Fotos.</span><span class="sxs-lookup"><span data-stu-id="c3da1-129">The Photos folder.</span></span>                                                       |
| <span data-ttu-id="c3da1-130">Álbum de cámara</span><span class="sxs-lookup"><span data-stu-id="c3da1-130">Camera Roll</span></span> | `cameraroll` | <span data-ttu-id="c3da1-131">La carpeta de copia de seguridad del álbum de cámara.</span><span class="sxs-lookup"><span data-stu-id="c3da1-131">The Camera Roll Backup folder.</span></span>                                           |
| <span data-ttu-id="c3da1-132">Raíz de la aplicación</span><span class="sxs-lookup"><span data-stu-id="c3da1-132">App Root</span></span>    | `approot`    | <span data-ttu-id="c3da1-p104">La carpeta personal de la aplicación. Normalmente en `/Apps/{Application Name}`</span><span class="sxs-lookup"><span data-stu-id="c3da1-p104">The application's personal folder. Usually in `/Apps/{Application Name}`</span></span> |
| <span data-ttu-id="c3da1-135">Música</span><span class="sxs-lookup"><span data-stu-id="c3da1-135">Music</span></span>       | `music`      | <span data-ttu-id="c3da1-136">La carpeta Música.</span><span class="sxs-lookup"><span data-stu-id="c3da1-136">The Music folder.</span></span>                                                        |


### <a name="optional-query-parameters"></a><span data-ttu-id="c3da1-137">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c3da1-137">Optional query parameters</span></span>

<span data-ttu-id="c3da1-138">Este método admite los [parámetros de consulta OData](../../../concepts/query_parameters.md) `$expand` y `$select` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3da1-138">This method supports the `$expand` and `$select` [OData query parameters](../../../concepts/query_parameters.md) to customize the response.</span></span>

## <a name="http-response"></a><span data-ttu-id="c3da1-139">Respuesta HTTP</span><span class="sxs-lookup"><span data-stu-id="c3da1-139">HTTP Response</span></span>

<span data-ttu-id="c3da1-140">Este método devuelve un código de respuesta `200 OK` y un objeto [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3da1-140">If successful, this method returns a `200 OK` response code and a [driveItem](../resources/driveitem.md) object in the response body.</span></span>

<span data-ttu-id="c3da1-141">Puede usar este método de direccionamiento de una carpeta especial junto con llamadas adicionales a las propiedades o relaciones en el objeto driveItem.</span><span class="sxs-lookup"><span data-stu-id="c3da1-141">You can use this method of addressing a special folder inline with additional calls to properties or relationships on the driveItem.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "0123456789abc",
  "name": "Documents",
  "eTag": "012345819293.1",
  "specialFolder": {
    "name": "documents"
  }
}
```

## <a name="get-children-of-a-special-folder"></a><span data-ttu-id="c3da1-142">Obtener elementos secundarios de una carpeta especial</span><span class="sxs-lookup"><span data-stu-id="c3da1-142">Get children of a special folder</span></span>

<span data-ttu-id="c3da1-143">Para solicitar los elementos secundarios de una carpeta especial, puede solicitar la colección `children` o usar la opción [expand](../../../concepts/query_parameters.md) para expandir la colección de elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c3da1-143">To request the children of a special folder, you can request the `children` collection or use the [expand](../../../concepts/query_parameters.md) option to expand the children collection.</span></span>

### <a name="http-request"></a><span data-ttu-id="c3da1-144">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c3da1-144">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-special-children", "scopes": "files.read" } -->

```http
GET /me/drive/special/{name}/children
```

### <a name="http-response"></a><span data-ttu-id="c3da1-145">Respuesta HTTP</span><span class="sxs-lookup"><span data-stu-id="c3da1-145">HTTP response</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "isCollection": true, "truncated": true} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {"name": "myfile.jpg", "size": 2048 },
    {"name": "Documents", "folder": { "childCount": 4} },
    {"name": "Photos", "folder": { "childCount": 203} },
    {"name": "my sheet(1).xlsx", "size": 197 }
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="c3da1-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3da1-146">Remarks</span></span>

> <span data-ttu-id="c3da1-147">**Nota**: Los objetos DriveItems con la faceta `specialFolder` indican que el elemento es una carpeta especial y se puede obtener acceso a ella mediante la colección `special`.</span><span class="sxs-lookup"><span data-stu-id="c3da1-147">**Note:** DriveItems with the `specialFolder` facet indicate the item is a special folder and can be accessed via the `special` collection.</span></span>

<span data-ttu-id="c3da1-148">Si la aplicación tiene permisos de solo lectura, la solicitud para obtener una carpeta especial o los elementos secundarios de una carpeta especial puede producir un error `404 Not Found` o `403 Forbidden` si la carpeta especial todavía no existe.</span><span class="sxs-lookup"><span data-stu-id="c3da1-148">If your app has read-only permissions, the request to get a special folder or the children of a special folder may fail with a `404 Not Found` or a `403 Forbidden` error if the special folder does not already exist.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Access known folders in OneDrive through the special folder collection",
  "keywords": "known folders",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Special folders"
} -->