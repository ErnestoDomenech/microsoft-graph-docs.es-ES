---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Audio
ms.openlocfilehash: 43b9999ecfb472a82e00a12ca820fdf8548eec64
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="audio-facet"></a>Faceta Audio

El recurso **Audio** agrupa las propiedades relacionadas con el audio en un elemento en una sola estructura.

Si un objeto [**DriveItem**](driveitem.md) tiene una faceta **audio** que no sea null, el elemento representa un archivo de audio.
Las propiedades del recurso **Audio** se rellenan al extraer metadatos del archivo. 

## <a name="json-representation"></a>Representación JSON

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.audio" } -->
```json
{
  "album": "string",
  "albumArtist": "string",
  "artist": "string",
  "bitrate": 128,
  "composers": "string",
  "copyright": "string",
  "disc": 0,
  "discCount": 0,
  "duration": 567,
  "genre": "string",
  "hasDrm": false,
  "isVariableBitrate": false,
  "title": "string",
  "track": 1,
  "trackCount": 16,
  "year": 2014
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad         | Tipo    | Descripción                                                          |
|:----------------------|:--------|:---------------------------------------------------------------------|
| **album**             | string  | El título del álbum de este archivo de audio.                          |
| **albumArtist**       | string  | El artista que se nombra en el álbum del archivo de audio.                    |
| **artist**            | string  | El intérprete del archivo de audio.                            |
| **bitrate**           | Int32   | Velocidad de bits expresada en kbps.                                           |
| **composers**         | string  | El nombre del compositor del archivo de audio.                          |
| **copyright**         | string  | Información de copyright del archivo de audio.                            |
| **disc**              | Int32   | El número del disco del que procede este archivo de audio.                    |
| **discCount**         | Int32   | El número total de discos de este álbum.                             |
| **duration**          | Int64   | Duración del archivo de audio, expresada en milisegundos                |
| **genre**             | string  | El género de este archivo de audio.                                        |
| **hasDrm**            | boolean | Indica si el archivo está protegido con administración de derechos digitales.   |
| **isVariableBitrate** | boolean | Indica si el archivo está codificado con una velocidad de bits variable.            |
| **title**             | string  | El título del archivo de audio.                                         |
| **track**             | Int32   | El número de la pista en el disco original de este archivo de audio.    |
| **trackCount**        | Int32   | El número total de pistas en el disco original de este archivo de audio. |
| **year**              | Int32   | El año en que se ha grabado el archivo de audio.                                |

[item-resource]: ../resources/driveitem.md

## <a name="remarks"></a>Comentarios

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The audio facet provides information about music or audio metadata.",
  "keywords": "music,audio,metadata,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Audio"
} -->
