---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Sitio
ms.openlocfilehash: db465f93f336a51d862daf6e05b1d6bc422247ea
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="site-resource"></a>Recurso site

El recurso **site** proporciona metadatos y relaciones para un sitio de SharePoint.

## <a name="tasks"></a>Tareas

Todos los ejemplos siguientes son relativos a `https://graph.microsoft.com/v1.0`.

| Nombre de tarea                | Solicitud de ejemplo
|:-------------------------|:--------------------------------------------------
| [Obtener sitio raíz][]        | GET /sites/root
| [Obtener sitio][]             | GET /sites/{site-id}
| [Obtener sitio por su ruta de acceso][]     | GET /sites/{hostname}:/{site-path}
| [Obtener sitio para un grupo][] | GET /groups/{group-id}/sites/root
| [Buscar sitios][]     | GET /sites?search={query}

[Obtener sitio]: ../api/site_get.md
[Obtener sitio raíz]: ../api/site_get.md
[Obtener sitio por su ruta de acceso]: ../api/site_getbypath.md
[Obtener sitio para un grupo]: ../api/site_get.md
[Buscar sitios]: ../api/site_search.md

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **site**.

El recurso **driveItem** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.

<!-- { "blockType": "resource",
       "@odata.type": "microsoft.graph.site",
       "keyProperty": "id",
       "optionalProperties": [ "root", "sharepointIds", "siteCollection", "drive", "drives", "sites" ] } -->

```json
{
  "id": "string",
  "root": { "@odata.type": "microsoft.graph.root" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "siteCollection": {"@odata.type": "microsoft.graph.siteCollection"},
  "displayName": "string",

  /* relationships */
  "contentTypes": [ { "@odata.type": "microsoft.graph.contentType" }],
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "drives": [ { "@odata.type": "microsoft.graph.drive" }],
  "items": [ { "@odata.type": "microsoft.graph.baseItem" }],
  "lists": [ { "@odata.type": "microsoft.graph.list" }],
  "sites": [ { "@odata.type": "microsoft.graph.site"} ],
  "columns": [ { "@odata.type": "microsoft.graph.columnDefinition" }],
  "onenote": [ { "@odata.type": "microsoft.graph.onenote"} ],

  /* inherited from baseItem */
  "name": "string",
  "createdDateTime": "datetime",
  "description": "string",
  "eTag": "string",
  "lastModifiedDateTime": "datetime",
  "webUrl": "url"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad            | Tipo                                | Descripción                                                                                    |
| :----------------------- | :---------------------------------- | :--------------------------------------------------------------------------------------------- |
| **id**                   | string                              | El identificador único del elemento. Solo lectura.                                                  |
| **createdDateTime**      | DateTimeOffset                      | La fecha y la hora de creación del elemento. Solo lectura.                                             |
| **description**          | string                              | Texto descriptivo del sitio.                                                             |
| **displayName**          | string                              | El título completo del sitio. Solo lectura.                                                        |
| **lastModifiedDateTime** | DateTimeOffset                      | Fecha y hora de la última modificación del elemento. Solo lectura.                                       |
| **name**                 | string                              | Nombre o título del elemento.                                                                  |
| **root**                 | [root](root.md)                     | Si está presente, indica que se trata del sitio raíz de la colección de sitios. Solo lectura.            |
| **sharepointIds**        | [sharepointIds](sharepointids.md)   | Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.                       |
| **siteCollection**       | [siteCollection](sitecollection.md) | Proporciona detalles sobre la colección de sitios del sitio. Solo disponible en el sitio raíz. Solo lectura. |
| **webUrl**               | string (url)                        | Dirección URL que muestra el elemento en el explorador. Solo lectura.                                          |

## <a name="relationships"></a>Relaciones

| Nombre de la relación | Tipo                             | Descripción
|:------------------|:---------------------------------|:----------------------
| **columns**       | Collection([columnDefinition][]) | La colección de definiciones de columna reutilizables en listas en este sitio.
| **contentTypes**  | Collection([contentType][])      | La colección de tipos de contenido definidos para este sitio.
| **drive**         | [drive][]                        | La unidad predeterminada (biblioteca de documentos) para este sitio.
| **drives**        | Collection([drive][])            | La colección de unidades (bibliotecas de documentos) de este sitio.
| **items**         | Collection([baseItem][])         | Se utiliza para resolver cualquier elemento contenido en este sitio. Esta colección no se puede enumerar.
| **lists**         | Collection([list][])             | La colección de listas en este sitio.
| **sites**         | Collection([site][])             | La colección de subsitios de este sitio.
| **onenote**       | [onenote][]                      | Realiza una llamada al servicio de OneNote para operaciones relacionadas con blocs de notas.

[columnDefinition]: columndefinition.md
[baseItem]: baseitem.md
[contentType]: contentType.md
[drive]: drive.md
[identitySet]: identityset.md
[list]: list.md
[site]: site.md
[onenote]: onenote.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Sites",
  "tocBookmarks": { "Resources/Site": "#" }
} -->
