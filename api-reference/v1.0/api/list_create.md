---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Crear una lista de SharePoint
ms.openlocfilehash: 7ba657bda38c25ef8f1e5fdda2f7438794e04d2a
ms.sourcegitcommit: 339070a20730bc4d363da7eb346d5f3c1e1d6c3e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="create-a-new-list"></a><span data-ttu-id="1fc8c-102">Crear una lista</span><span class="sxs-lookup"><span data-stu-id="1fc8c-102">Create a new list</span></span>

<span data-ttu-id="1fc8c-103">Cree una [lista][] en un [sitio][].</span><span class="sxs-lookup"><span data-stu-id="1fc8c-103">Create a new [list][] in a [site][].</span></span>

## <a name="permissions"></a><span data-ttu-id="1fc8c-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="1fc8c-104">Permissions</span></span>

<span data-ttu-id="1fc8c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1fc8c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|            <span data-ttu-id="1fc8c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1fc8c-107">Permission type</span></span>             | <span data-ttu-id="1fc8c-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1fc8c-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="1fc8c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1fc8c-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="1fc8c-110">Sites.Manage.All</span><span class="sxs-lookup"><span data-stu-id="1fc8c-110">Sites.Manage.All</span></span>                            |
| <span data-ttu-id="1fc8c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1fc8c-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1fc8c-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1fc8c-112">Not supported.</span></span>                              |
| <span data-ttu-id="1fc8c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1fc8c-113">Application</span></span>                            | <span data-ttu-id="1fc8c-114">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1fc8c-114">Sites.ReadWrite.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="1fc8c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1fc8c-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST https://graph.microsoft.com/v1.0/sites/{site-id}/lists
```

## <a name="request-body"></a><span data-ttu-id="1fc8c-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="1fc8c-116">Request body</span></span>

<span data-ttu-id="1fc8c-117">En el cuerpo de la solicitud, proporcione una representación JSON del recurso [list][] que quiere crear.</span><span class="sxs-lookup"><span data-stu-id="1fc8c-117">In the request body, supply a JSON representation of the [list][] resource to create.</span></span>

## <a name="example"></a><span data-ttu-id="1fc8c-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fc8c-118">Example</span></span>

<span data-ttu-id="1fc8c-119">Aquí se muestra un ejemplo de cómo crear una lista genérica.</span><span class="sxs-lookup"><span data-stu-id="1fc8c-119">Here is an example of how to create a new generic list.</span></span>

<!-- { "blockType": "request", "name": "create-list", "scopes": "sites.readwrite.all" } -->

```http
POST /sites/{site-id}/lists
Content-Type: application/json

{
  "name": "Books",
  "columns": [
    {
      "name": "Author",
      "text": { }
    },
    {
      "name": "PageCount",
      "number": { }
    }
  ],
  "list": {
    "template": "genericList"
  }
}
```

<span data-ttu-id="1fc8c-120">**Nota**: Las columnas personalizadas son opcionales.</span><span class="sxs-lookup"><span data-stu-id="1fc8c-120">**Note:** Custom columns are optional.</span></span>

<span data-ttu-id="1fc8c-121">Además de las columnas especificadas aquí, se crean listas con columnas definidas en la **plantilla** de referencia.</span><span class="sxs-lookup"><span data-stu-id="1fc8c-121">In addition to any columns specified here, new lists are created with columns defined in the referenced **template**.</span></span>
<span data-ttu-id="1fc8c-122">Si la faceta **list** o la **plantilla** están sin especificar, el valor predeterminado de la lista es la plantilla `genericList`, que incluye una columna _Título_.</span><span class="sxs-lookup"><span data-stu-id="1fc8c-122">If the **list** facet or **template** is unspecified, the list defaults to the `genericList` template, which includes a _Title_ column.</span></span>

## <a name="response"></a><span data-ttu-id="1fc8c-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1fc8c-123">Response</span></span>

<span data-ttu-id="1fc8c-124">Si se realiza correctamente, este método devuelve un valor [list][] en el cuerpo de la respuesta de la lista creada.</span><span class="sxs-lookup"><span data-stu-id="1fc8c-124">If successful, this method returns a [list][] in the response body for the created list.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.list", "truncated": true } -->

```json
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "22e03ef3-6ef4-424d-a1d3-92a337807c30",
  "createdDateTime": "2017-04-30T01:21:00Z",
  "createdBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "8606e4d5-d582-4f5f-aeba-7d7c18b20cfd"
    }
  },
  "lastModifiedDateTime": "2016-08-30T08:26:00Z",
  "lastModifiedBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "8606e4d5-d582-4f5f-aeba-7d7c18b20cfd"
    }
  }
}
```

<span data-ttu-id="1fc8c-125">**Nota:** El objeto Response se trunca para obtener una mayor claridad.</span><span class="sxs-lookup"><span data-stu-id="1fc8c-125">**Note:** The response object is truncated for clarity.</span></span>
<span data-ttu-id="1fc8c-126">Se devolverán las propiedades predeterminadas de la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="1fc8c-126">Default properties will be returned from the actual call.</span></span>

[list]: ../resources/list.md
[site]: ../resources/site.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a new SharePoint list.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "List/Create"
} -->