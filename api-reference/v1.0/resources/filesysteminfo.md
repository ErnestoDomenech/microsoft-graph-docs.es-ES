---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: FileSystemInfo
ms.openlocfilehash: 9a5214f9c5e161de0be66ac634c7c5538b203772
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="filesysteminfo-facet"></a>Faceta FileSystemInfo

El recurso **FileSystemInfo** contiene propiedades que aparecen en el sistema de archivos local del dispositivo de la versión local de un elemento.
Esta faceta se puede usar para especificar la fecha de la última modificación o de creación del elemento tal y como estaba en el dispositivo local.

Está disponible en la propiedad fileSystemInfo de los recursos [driveItem][item-resource].

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "lastAccessedDateTime"
  ],
  "@odata.type": "microsoft.graph.fileSystemInfo"
}-->

```json
{
  "createdDateTime" : "datetime",
  "lastAccessedDateTime": "datetime",
  "lastModifiedDateTime" : "datetime"
}
```

## <a name="properties"></a>Propiedades

| Propiedad                 | Tipo           | Descripción                                                                                                          |
| :----------------------- | :------------- | :------------------------------------------------------------------------------------------------------------------- |
| **createdDateTime**      | DateTimeOffset | La fecha y la hora UTC de creación del archivo en un cliente.                                                              |
| **lastAccessedDateTime** | DateTimeOffset | La fecha y la hora UTC del último acceso al archivo. Solo disponible para la [lista de archivos recientes](../api/drive_recent.md). |
| **lastModifiedDateTime** | DateTimeOffset | La fecha y la hora UTC en que se ha modificado por última vez el archivo en un cliente.                                                        |

## <a name="notes"></a>Notas

Los valores de **createdDateTime** y **lastModifiedDateTime** varían de las mismas propiedades en el recurso [DriveItem](driveitem.md).
Los valores del recurso DriveItem son la fecha y hora de creación y modificación como se ve desde el servicio.
Los valores almacenados en el recurso **FileSystemInfo** los proporciona el cliente.

Por ejemplo, si un archivo se ha creado en el dispositivo el lunes, pero no se ha cargado al servicio hasta el martes, el cliente que carga el archivo debe escribir la faceta `fileSystemInfo` para incluir la fecha de creación del lunes. Cuando se recuperan los metadatos del elemento, la fecha de creación del elemento reflejará el martes, pero la faceta `fileSystemInfo` mostrará la fecha de creación original del lunes.

Estas propiedades son de lectura y escritura. Si está cargando un archivo y conoce los valores del cliente local de estos campos, debe incluirlos en la solicitud.

Si se actualiza el contenido del archivo y no se proporcionan estas propiedades, **lastModifiedDateTime** se restablece a la hora actual de forma automática.

## <a name="remarks"></a>Comentarios

* **lastAccessedDateTime** no está disponible para elementos en SharePoint Online u OneDrive para la Empresa.

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "The fileSystemInfo facet provides information about date created and modified by clients.",
  "keywords": "fileSystemInfo,client,system info,onedrive",
  "section": "documentation",
  "tocPath": "Facets/FileSystemInfo"
} -->
