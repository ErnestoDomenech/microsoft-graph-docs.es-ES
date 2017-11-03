---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Recuperar miniaturas de un archivo o una carpeta
ms.openlocfilehash: 864765898955d0a690ab85dc0be9761a7a9d1856
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="list-thumbnails-for-a-driveitem"></a><span data-ttu-id="b987b-102">Enumerar miniaturas de un DriveItem</span><span class="sxs-lookup"><span data-stu-id="b987b-102">List thumbnails for a DriveItem</span></span>

<span data-ttu-id="b987b-103">Recupere una colección de recursos de [ThumbnailSet](../resources/thumbnailset.md) de un recurso de [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="b987b-103">Retrieve a collection of [ThumbnailSet](../resources/thumbnailset.md) resources for a [DriveItem](../resources/driveitem.md) resource.</span></span>

<span data-ttu-id="b987b-p101">Un DriveItem puede estar representado por cero o más recursos [ThumbnailSet](../resources/thumbnailset.md). Cada **thumbnailSet** puede tener uno o varios objetos en [**miniatura**](../resources/thumbnail.md), que son imágenes que representan el elemento. Por ejemplo, un **thumbnailSet** puede incluir objetos en **miniatura**, los más comunes son `small`, `medium` o `large`.</span><span class="sxs-lookup"><span data-stu-id="b987b-p101">A DriveItem can be represented by zero or more [ThumbnailSet](../resources/thumbnailset.md) resources. Each **thumbnailSet** can have one or more [**thumbnail**](../resources/thumbnail.md) objects, which are images that represent the item. For example, a **thumbnailSet** may include **thumbnail** objects, such as common ones including `small`, `medium`, or `large`.</span></span>

<span data-ttu-id="b987b-p102">Hay muchas maneras de trabajar con miniaturas en OneDrive. Aquí tiene las más comunes:</span><span class="sxs-lookup"><span data-stu-id="b987b-p102">There are many ways to work with thumbnails on OneDrive. Here are the most common ones:</span></span>

* <span data-ttu-id="b987b-109">Enumerar las miniaturas disponibles para un elemento</span><span class="sxs-lookup"><span data-stu-id="b987b-109">Enumerate available thumbnails for an item</span></span>
* <span data-ttu-id="b987b-110">Recuperar una sola miniatura para un elemento</span><span class="sxs-lookup"><span data-stu-id="b987b-110">Retrieve a single thumbnail for an item</span></span>
* <span data-ttu-id="b987b-111">Recuperar el contenido de miniaturas</span><span class="sxs-lookup"><span data-stu-id="b987b-111">Retrieve thumbnail content</span></span>
* <span data-ttu-id="b987b-112">Recuperar miniaturas para varios elementos en una sola solicitud</span><span class="sxs-lookup"><span data-stu-id="b987b-112">Retrieve thumbnails for multiple items in a single request</span></span>
* <span data-ttu-id="b987b-113">Recuperar los tamaños personalizados de miniaturas</span><span class="sxs-lookup"><span data-stu-id="b987b-113">Retrieve custom thumbnail sizes</span></span>
* <span data-ttu-id="b987b-114">Cargar una miniatura personalizada para un elemento </span><span class="sxs-lookup"><span data-stu-id="b987b-114">Upload a custom thumbnail for an item</span></span>
* <span data-ttu-id="b987b-115">Determinar si existe una miniatura cargada personalizada</span><span class="sxs-lookup"><span data-stu-id="b987b-115">Determine if a custom uploaded thumbnail exists</span></span>

## <a name="permissions"></a><span data-ttu-id="b987b-116">Permisos</span><span class="sxs-lookup"><span data-stu-id="b987b-116">Permissions</span></span>

<span data-ttu-id="b987b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b987b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b987b-119">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b987b-119">Permission type</span></span>      | <span data-ttu-id="b987b-120">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b987b-120">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b987b-121">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b987b-121">Delegated (work or school account)</span></span> | <span data-ttu-id="b987b-122">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b987b-122">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="b987b-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b987b-123">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b987b-124">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b987b-124">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="b987b-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b987b-125">Application</span></span> | <span data-ttu-id="b987b-126">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b987b-126">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b987b-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b987b-127">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/thumbnails
GET /groups/{group-id}/drive/items/{item-id}/thumbnails
GET /me/drive/items/{item-id}/thumbnails
GET /sites/{site-id}/drive/items/{item-id}/thumbnails
GET /users/{user-id}/drive/items/{item-id}/thumbnails
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b987b-128">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b987b-128">Optional query parameters</span></span>

<span data-ttu-id="b987b-129">Este método admite el [parámetro de consulta OData](../../../concepts/query_parameters.md) `$select` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b987b-129">This method supports the `$select` [OData puery parameter](../../../concepts/query_parameters.md) to customize the response.</span></span>

## <a name="response"></a><span data-ttu-id="b987b-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b987b-130">Response</span></span>

<span data-ttu-id="b987b-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ThumbnailSet](../resources/thumbnailset.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b987b-131">If successful, this method returns a `200 OK` response code and collection of [ThumbnailSet](../resources/thumbnailset.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b987b-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b987b-132">Example</span></span>

<span data-ttu-id="b987b-133">Aquí tiene un ejemplo de la solicitud que recupera las miniaturas disponibles de un elemento en el OneDrive del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="b987b-133">Here is an example of the request which retrieves available thumbnails for an item in the current user's OneDrive.</span></span>

<!-- { "blockType": "request", "name": "enum-item-thumbnails", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails
```

<span data-ttu-id="b987b-134">Esta devuelve una matriz de **thumbnailSets** disponibles para el elemento.</span><span class="sxs-lookup"><span data-stu-id="b987b-134">This returns an array of available **thumbnailSets** for the item.</span></span> <span data-ttu-id="b987b-135">Cualquier elemento de una unidad puede tener cero o más miniaturas.</span><span class="sxs-lookup"><span data-stu-id="b987b-135">Any item in OneDrive can have zero or more thumbnails.</span></span>

<span data-ttu-id="b987b-136">**Nota**: Puede usar el parámetro de cadena de consulta _select_ para controlar qué tamaños de miniatura se devuelven en **ThumbnailSet**.</span><span class="sxs-lookup"><span data-stu-id="b987b-136">**Note:** You can use the _select_ query string parameter to control which thumbnail sizes are returned in the **ThumbnailSet**.</span></span>
<span data-ttu-id="b987b-137">Por ejemplo, `/thumbnails?select=medium` recupera solo las miniaturas medianas.</span><span class="sxs-lookup"><span data-stu-id="b987b-137">For example, `/thumbnails?select=medium` retrieves only the medium sized thumbnails.</span></span>


### <a name="response"></a><span data-ttu-id="b987b-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b987b-138">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.thumbnailSet)" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "0",
      "small": { "height": 64, "width": 96, "url": "https://sn3302files..."},
      "medium": { "height": 117, "width": 176, "url": "https://sn3302files..."},
      "large": { "height": 533, "width": 800, "url": "https://sn3302files..."}
    }
  ]
}
```

## <a name="get-a-single-thumbnail"></a><span data-ttu-id="b987b-139">Obtener una única miniatura</span><span class="sxs-lookup"><span data-stu-id="b987b-139">Retrieve a single thumbnail</span></span>

<span data-ttu-id="b987b-140">Recupere los metadatos de una sola miniatura y un tamaño solicitándolo directamente en una solicitud.</span><span class="sxs-lookup"><span data-stu-id="b987b-140">Retrieve the metadata for a single thumbnail and size by addressing it directly in a request.</span></span>

### <a name="http-request"></a><span data-ttu-id="b987b-141">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b987b-141">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-one-thumbnail", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}
```

### <a name="path-parameters"></a><span data-ttu-id="b987b-142">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="b987b-142">Path parameters</span></span>

| <span data-ttu-id="b987b-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="b987b-143">Name</span></span>         | <span data-ttu-id="b987b-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="b987b-144">Type</span></span>   | <span data-ttu-id="b987b-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="b987b-145">Description</span></span>                                                                              |
|:-------------|:-------|:-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b987b-146">**item-id**</span><span class="sxs-lookup"><span data-stu-id="b987b-146">**item-id**</span></span>  | <span data-ttu-id="b987b-147">string</span><span class="sxs-lookup"><span data-stu-id="b987b-147">string</span></span> | <span data-ttu-id="b987b-148">El identificador único para el elemento al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="b987b-148">The unique identifier for the item referenced.</span></span>                                           |
| <span data-ttu-id="b987b-149">**thumb-id**</span><span class="sxs-lookup"><span data-stu-id="b987b-149">**thumb-id**</span></span> | <span data-ttu-id="b987b-150">número</span><span class="sxs-lookup"><span data-stu-id="b987b-150">number</span></span> | <span data-ttu-id="b987b-151">El índice de la miniatura, normalmente de 0-4.</span><span class="sxs-lookup"><span data-stu-id="b987b-151">The index of the thumbnail, usually 0-4.</span></span> <span data-ttu-id="b987b-152">Si existe una miniatura personalizada, su índice es 0.</span><span class="sxs-lookup"><span data-stu-id="b987b-152">If there is a custom thumbnail, its index is 0.</span></span> |
| <span data-ttu-id="b987b-153">**size**</span><span class="sxs-lookup"><span data-stu-id="b987b-153">**size**</span></span>     | <span data-ttu-id="b987b-154">cadena</span><span class="sxs-lookup"><span data-stu-id="b987b-154">string</span></span> | <span data-ttu-id="b987b-155">El tamaño de la miniatura solicitada.</span><span class="sxs-lookup"><span data-stu-id="b987b-155">The size of the thumbnail requested.</span></span> <span data-ttu-id="b987b-156">Puede ser uno de los tamaños estándares enumerados a continuación o uno personalizado.</span><span class="sxs-lookup"><span data-stu-id="b987b-156">This can be one of the standard sizes listed below or a custom size.</span></span> |

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.thumbnail" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "width": 100,
  "height": 100,
  "url": "http://onedrive.com/asd123a/asdjlkasjdkasdjlk.jpg"
}
```

## <a name="retrieve-thumbnail-binary-content"></a><span data-ttu-id="b987b-157">Recuperar el contenido binario de miniaturas</span><span class="sxs-lookup"><span data-stu-id="b987b-157">Retrieve thumbnail content</span></span>

<span data-ttu-id="b987b-158">Puede recuperar directamente el contenido de la miniatura solicitando la propiedad **content** de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="b987b-158">You can directly retrieve the content of the thumbnail by requesting the **content** property of the thumbnail.</span></span>

### <a name="http-request"></a><span data-ttu-id="b987b-159">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b987b-159">HTTP request</span></span>

<!-- { "blockType": "request", "name":"get-thumbnail-content", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}/content
```

### <a name="response"></a><span data-ttu-id="b987b-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b987b-160">Response</span></span>

<span data-ttu-id="b987b-161">El servicio responde con un redireccionamiento a la dirección URL de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="b987b-161">The service responds with a redirect to the thumbnail URL.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

<span data-ttu-id="b987b-162">Las direcciones URL de la miniatura son seguras en caché.</span><span class="sxs-lookup"><span data-stu-id="b987b-162">Thumbnail URLs are cache-safe.</span></span> <span data-ttu-id="b987b-163">La dirección URL cambiará, si el elemento cambia de manera que necesite una nueva miniatura para generarse.</span><span class="sxs-lookup"><span data-stu-id="b987b-163">The URL will change, if the item changes in a way that requires a new thumbnail to be generated.</span></span>


## <a name="getting-thumbnails-while-listing-driveitems"></a><span data-ttu-id="b987b-164">Obtención de miniaturas al enumerar recursos DriveItem</span><span class="sxs-lookup"><span data-stu-id="b987b-164">Getting thumbnails while listing DriveItems</span></span>

<span data-ttu-id="b987b-165">Si está recuperando una lista de recursos DriveItem para mostrar, puede usar el parámetro de cadena de consulta _$expand_ para que también incluya las miniaturas de esos recursos.</span><span class="sxs-lookup"><span data-stu-id="b987b-165">If you are retrieving a list of DriveItem resources to display, you can use the _$expand_ query string parameter to also include the thumbnails for those resources.</span></span>
<span data-ttu-id="b987b-166">Esto permite que su aplicación recupere miniaturas y elementos en una única solicitud, en lugar de emitir varias solicitudes.</span><span class="sxs-lookup"><span data-stu-id="b987b-166">This enables your app to retrieve thumbnails and items in a single request, instead of issuing many requests.</span></span>

### <a name="http-request"></a><span data-ttu-id="b987b-167">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b987b-167">HTTP request</span></span>

<!-- { "blockType": "request", "name":"get-thumbnail-while-listing", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/children?$expand=thumbnails
```

### <a name="response"></a><span data-ttu-id="b987b-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b987b-168">Response</span></span>

<span data-ttu-id="b987b-169">Las respuestas del servicio con la lista de recursos DriveItem y sus miniaturas.</span><span class="sxs-lookup"><span data-stu-id="b987b-169">The service responses with the list of DriveItems and their thumbnails.</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItem)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "182331E8-2788-4932-B52A-A6550577043F",
      "name": "my photo.jpg",
      "thumbnails": [
        {
          "small": { "width": 96,
                     "height": 96,
                     "url": "https://sn3302files..."
                   }
        }
      ]
    },
    {
      "id": "2D223953-A56B-4D9B-ADF3-13E7820673A2",
      "name": "presentation.pptx",
      "thumbnails": [
        {
          "small": { "width": 96,
                     "height": 96,
                     "url": "https://sn3302files..."
                   }
        }
      ]
    }
  ]
}
```

## <a name="size-values"></a><span data-ttu-id="b987b-170">Valores de tamaño</span><span class="sxs-lookup"><span data-stu-id="b987b-170">Size values</span></span>

<span data-ttu-id="b987b-p110">Esta tabla define los tamaños posibles de las miniaturas. Puede solicitar cualquier tamaño de miniatura arbitrario, pero es probable que existan valores definidos y que se devuelva un valor rápidamente:</span><span class="sxs-lookup"><span data-stu-id="b987b-p110">This table defines the possible thumbnail sizes. While you can request any arbitrary thumbnail size, the defined values are likely to exist and return a value quickly:</span></span>

| <span data-ttu-id="b987b-173">Nombre</span><span class="sxs-lookup"><span data-stu-id="b987b-173">Name</span></span>           | <span data-ttu-id="b987b-174">Resolución</span><span class="sxs-lookup"><span data-stu-id="b987b-174">Resolution</span></span>  | <span data-ttu-id="b987b-175">Relación de aspecto</span><span class="sxs-lookup"><span data-stu-id="b987b-175">Aspect Ratio</span></span> | <span data-ttu-id="b987b-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="b987b-176">Description</span></span>                                                          |
|:---------------|:------------|:-------------|:---------------------------------------------------------------------|
| `small`        | <span data-ttu-id="b987b-177">borde más largo 96</span><span class="sxs-lookup"><span data-stu-id="b987b-177">96 longest</span></span>  | <span data-ttu-id="b987b-178">Original</span><span class="sxs-lookup"><span data-stu-id="b987b-178">Original</span></span>     | <span data-ttu-id="b987b-179">Miniatura pequeña y muy comprimida recortada en una relación de aspecto cuadrada.</span><span class="sxs-lookup"><span data-stu-id="b987b-179">Small, highly compressed thumbnail cropped to a square aspect ratio.</span></span> |
| `medium`       | <span data-ttu-id="b987b-180">borde más largo 176</span><span class="sxs-lookup"><span data-stu-id="b987b-180">176 longest</span></span> | <span data-ttu-id="b987b-181">Original</span><span class="sxs-lookup"><span data-stu-id="b987b-181">Original</span></span>     | <span data-ttu-id="b987b-182">Miniatura recortada al tamaño estándar del elemento para la vista web de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="b987b-182">Cropped to the standard item size for the OneDrive web view.</span></span>         |
| `large`        | <span data-ttu-id="b987b-183">borde más largo 800</span><span class="sxs-lookup"><span data-stu-id="b987b-183">800 longest</span></span> | <span data-ttu-id="b987b-184">Original</span><span class="sxs-lookup"><span data-stu-id="b987b-184">Original</span></span>     | <span data-ttu-id="b987b-185">Miniatura con el borde más largo cambiado a un tamaño de 800 píxeles.</span><span class="sxs-lookup"><span data-stu-id="b987b-185">Thumbnail with the longest edge resized to 800 pixels.</span></span>               |
| `smallSquare`  | <span data-ttu-id="b987b-186">96x96</span><span class="sxs-lookup"><span data-stu-id="b987b-186">96x96</span></span>       | <span data-ttu-id="b987b-187">Recorte cuadrado</span><span class="sxs-lookup"><span data-stu-id="b987b-187">Square Crop</span></span>  | <span data-ttu-id="b987b-188">Miniatura de cuadrado pequeño</span><span class="sxs-lookup"><span data-stu-id="b987b-188">Small square thumbnail</span></span>                                               |
| `mediumSquare` | <span data-ttu-id="b987b-189">176x176</span><span class="sxs-lookup"><span data-stu-id="b987b-189">176x176</span></span>     | <span data-ttu-id="b987b-190">Recorte cuadrado</span><span class="sxs-lookup"><span data-stu-id="b987b-190">Square Crop</span></span>  | <span data-ttu-id="b987b-191">Miniatura de cuadrado pequeño</span><span class="sxs-lookup"><span data-stu-id="b987b-191">Small square thumbnail</span></span>                                               |
| `largeSquare`  | <span data-ttu-id="b987b-192">800x800</span><span class="sxs-lookup"><span data-stu-id="b987b-192">800x800</span></span>     | <span data-ttu-id="b987b-193">Recorte cuadrado</span><span class="sxs-lookup"><span data-stu-id="b987b-193">Square Crop</span></span>  | <span data-ttu-id="b987b-194">Miniatura de cuadrado grande</span><span class="sxs-lookup"><span data-stu-id="b987b-194">Large square thumbnail</span></span>                                               |

## <a name="requesting-custom-thumbnail-sizes"></a><span data-ttu-id="b987b-195">Solicitar tamaños personalizados de miniaturas</span><span class="sxs-lookup"><span data-stu-id="b987b-195">Retrieve custom thumbnail sizes</span></span>

<span data-ttu-id="b987b-196">Además de los tamaños definidos, la aplicación puede solicitar un tamaño de miniatura personalizado especificando las dimensiones de la miniatura prefijada con `c`.</span><span class="sxs-lookup"><span data-stu-id="b987b-196">In addition to the defined sizes, your app can request a custom thumbnail size by specifying the dimensions of the thumbnail prefixed with `c`.</span></span>
<span data-ttu-id="b987b-197">Por ejemplo, si su aplicación necesita miniaturas de tamaño 300x400, puede solicitar ese tamaño de esta forma:</span><span class="sxs-lookup"><span data-stu-id="b987b-197">For example if you need thumbnails that are 300x400, you can request that size like this:</span></span>

<!-- { "name": "get-thumbnail-custom-size", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails?select=c300x400_Crop
```

<span data-ttu-id="b987b-198">Que responde solo con el tamaño de miniatura personalizado seleccionado:</span><span class="sxs-lookup"><span data-stu-id="b987b-198">Which responds with just the custom thumbnail size selected:</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.thumbnailSet)" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "0",
      "c300x400_Crop": { "height": 300, "width": 400, "url": "https://sn3302files.onedrive.com/123"},
    }
  ]
}
```

<span data-ttu-id="b987b-199">Puede especificar las siguientes opciones después del tamaño de la miniatura solicitado:</span><span class="sxs-lookup"><span data-stu-id="b987b-199">You can specify the following options after the size of the thumbnail requested:</span></span>

### <a name="examples-of-custom-identifiers"></a><span data-ttu-id="b987b-200">Ejemplos de identificadores personalizados</span><span class="sxs-lookup"><span data-stu-id="b987b-200">Examples of custom identifiers</span></span>

| <span data-ttu-id="b987b-201">Identificador de miniatura</span><span class="sxs-lookup"><span data-stu-id="b987b-201">Thumbnail identifier</span></span> | <span data-ttu-id="b987b-202">Resolución</span><span class="sxs-lookup"><span data-stu-id="b987b-202">Resolution</span></span>             | <span data-ttu-id="b987b-203">Relación de aspecto</span><span class="sxs-lookup"><span data-stu-id="b987b-203">Aspect ratio</span></span> | <span data-ttu-id="b987b-204">Descripción</span><span class="sxs-lookup"><span data-stu-id="b987b-204">Description</span></span>                                                                                                                                         |
|:---------------------|:-----------------------|:-------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b987b-205">c300x400</span><span class="sxs-lookup"><span data-stu-id="b987b-205">c300x400</span></span>             | <span data-ttu-id="b987b-206">Limitado por un cuadro de 300x400</span><span class="sxs-lookup"><span data-stu-id="b987b-206">Bounded by 300x400 box</span></span> | <span data-ttu-id="b987b-207">Original</span><span class="sxs-lookup"><span data-stu-id="b987b-207">Original</span></span>     | <span data-ttu-id="b987b-208">Genera una miniatura que se adapta dentro de un cuadro de 300x400 píxeles, manteniendo la relación de aspecto</span><span class="sxs-lookup"><span data-stu-id="b987b-208">Generate a thumbnail that fits inside a 300x400 pixel box, maintaining aspect ratio</span></span>                                                                 |
| <span data-ttu-id="b987b-209">c300x400_Crop</span><span class="sxs-lookup"><span data-stu-id="b987b-209">c300x400_Crop</span></span>        | <span data-ttu-id="b987b-210">300x400</span><span class="sxs-lookup"><span data-stu-id="b987b-210">300x400</span></span>                | <span data-ttu-id="b987b-211">Recortado</span><span class="sxs-lookup"><span data-stu-id="b987b-211">Cropped</span></span>      | <span data-ttu-id="b987b-212">Genera una miniatura que tiene 300x400 píxeles.</span><span class="sxs-lookup"><span data-stu-id="b987b-212">Generate a thumbnail that is 300x400 pixels.</span></span> <span data-ttu-id="b987b-213">Esto funciona cambiando el tamaño de la imagen para rellenar el cuadro de 300x400 y recortando lo que sobresalga de este.</span><span class="sxs-lookup"><span data-stu-id="b987b-213">This works by resizing the image to fill the 300x400 box and cropping whatever spills outside the box.</span></span> |

<span data-ttu-id="b987b-214">**Nota**: La miniatura devuelta puede no coincidir exactamente con las dimensiones en píxeles que se solicitaron, pero coincidirá con la relación de aspecto.</span><span class="sxs-lookup"><span data-stu-id="b987b-214">**Note:** The thumbnail returned may not exactly match the pixel dimensions that was requested, but will match the aspect ratio.</span></span>
<span data-ttu-id="b987b-215">En algunos casos, puede devolverse una miniatura más grande que la que se ha solicitado si la miniatura ya existe y se puede escalar fácilmente para ajustarse a la resolución solicitada.</span><span class="sxs-lookup"><span data-stu-id="b987b-215">In some cases, a larger thumbnail may be returned than was requested, if the thumbnail already exists and can easily be scaled to match the requested resolution.</span></span>

## <a name="remarks"></a><span data-ttu-id="b987b-216">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b987b-216">Remarks</span></span>

<span data-ttu-id="b987b-217">**Nota** En OneDrive para la Empresa y en SharePoint:</span><span class="sxs-lookup"><span data-stu-id="b987b-217">**Note** In OneDrive for Business and SharePoint:</span></span>

<span data-ttu-id="b987b-218">El uso de estas llamadas para expandir la colección de miniaturas no funcionará:</span><span class="sxs-lookup"><span data-stu-id="b987b-218">Using these calls to expand the thumbnails collection will not work:</span></span>

* `GET /drive/root:/{item-path}?expand=children(expand=thumbnails)`
* `GET /drive/items/{item-id}/children?expand=thumbnails`

<span data-ttu-id="b987b-219">Las miniaturas no se admiten en SharePoint Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b987b-219">Thumbnails are not supported on SharePoint Server 2016.</span></span>

### <a name="error-responses"></a><span data-ttu-id="b987b-220">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="b987b-220">Error responses</span></span>

<span data-ttu-id="b987b-221">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="b987b-221">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: ../../../concepts/errors.md

<!-- {
  "type": "#page.annotation",
  "description": "Get metadata and content for thumbnails of multiple sizes for OneDrive items.",
  "keywords": "thumbnail,content,download,sizes",
  "section": "documentation",
  "tocPath": "Items/Thumbnails"
} -->