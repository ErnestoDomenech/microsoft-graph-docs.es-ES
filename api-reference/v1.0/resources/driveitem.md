# <a name="driveitem-resource-type"></a>Tipo de recurso DriveItem

El recurso **DriveItem** representa un elemento de una unidad. Todos los objetos de sistema de archivo de nivel superior en OneDrive se devuelven como recursos de elemento. 

Se puede acceder a los **DriveItems** a través de su **identificador**, mediante la sintaxis `/items/{item-id}`, o a través de su ruta de acceso al sistema de archivos, mediante la sintaxis `/drive/root:/path/to/file`. 

Los elementos tienen facetas modeladas como propiedades que proporcionan datos sobre las identidades y las capacidades del elemento. Las carpetas tienen una [**faceta folder**](folder.md) y los archivos tienen una [**faceta file**](file.md). Las imágenes tienen una [**faceta image**](image.md) además de la faceta file. Las imágenes tomadas con una cámara (fotos) tienen una [**faceta photo**](photo.md) que identifica el elemento como una foto y proporciona las propiedades de cuándo se tomó la foto y con qué dispositivo.

Los elementos con una faceta **folder** actúan como contenedores de elementos y tienen una referencia `children` que indica una colección de elementos dentro de la carpeta.


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "children", "createdByUser", "lastModifiedByUser", "permissions", "thumbnails"],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.driveItem"
}-->

```json
{
  "audio": {"@odata.type": "microsoft.graph.audio"},
  "cTag": "string",
  "content": "stream",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "deleted": {"@odata.type": "microsoft.graph.deleted"},
  "eTag": "string",
  "file": {"@odata.type": "microsoft.graph.file"},
  "fileSystemInfo": {"@odata.type": "microsoft.graph.fileSystemInfo"},
  "folder": {"@odata.type": "microsoft.graph.folder"},
  "id": "string (identifier)",
  "image": {"@odata.type": "microsoft.graph.image"},
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "location": {"@odata.type": "microsoft.graph.geoCoordinates"},
  "name": "string",
  "package": {"@odata.type": "microsoft.graph.package"},
  "parentReference": {"@odata.type": "microsoft.graph.itemReference"},
  "photo": {"@odata.type": "microsoft.graph.photo"},
  "remoteItem": {"@odata.type": "microsoft.graph.remoteItem"},
  "searchResult": {"@odata.type": "microsoft.graph.searchResult"},
  "shared": {"@odata.type": "microsoft.graph.shared"},
  "size": 1024,
  "specialFolder": {"@odata.type": "microsoft.graph.specialFolder"},
  "video": {"@odata.type": "microsoft.graph.video"},
  "webDavUrl": "string",
  "webUrl": "string",

  "createdByUser": { "@odata.type": "microsoft.graph.user" },
  "lastModifiedByUser": { "@odata.type": "microsoft.graph.user" },
  "children": [ { "@odata.type": "microsoft.graph.driveItem" }],
  "thumbnails": [ {"@odata.type": "microsoft.graph.thumbnailSet"}],
  "permissions": [ {"@odata.type": "microsoft.graph.permission"} ]
}

```

## <a name="properties"></a>Propiedades

| Propiedad             | Tipo                                | Descripción                                                                                                                                                               |
|:---------------------|:------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| audio                | [audio](audio.md)                   | Metadatos de audio, si el elemento es un archivo de audio. Solo lectura.                                                                                                                  |
| contenido              | Secuencia                              | La secuencia de contenido, si el elemento representa un archivo.                                                                                                                        |
| createdBy            | [identitySet](identityset.md)       | Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.                                                                                          |
| createdDateTime      | DateTimeOffset                      | Fecha y hora de creación del elemento. Solo lectura.                                                                                                                                |
| cTag                 | String                              | Un eTag del contenido del elemento. No se cambia este eTag si solo se modifican los metadatos. **Nota** Esta propiedad no se devuelve si el elemento es una carpeta. Solo lectura. |
| deleted              | [deleted](deleted.md)               | Información sobre el estado del elemento eliminado. Solo lectura.                                                                                                               |
| eTag                 | String                              | ETag de todo el elemento (metadatos + contenido). Solo lectura.                                                                                                                 |
| archivo                 | [file](file.md)                     | Metadatos de archivo, si el elemento es un archivo. Solo lectura.                                                                                                                          |
| fileSystemInfo       | [fileSystemInfo](filesysteminfo.md) | Información del sistema de archivos del cliente. Lectura y escritura.                                                                                                                            |
| folder               | [folder](folder.md)                 | Metadatos de carpeta, si el elemento es una carpeta. Solo lectura.                                                                                                                      |
| id                   | String                              | El identificador único del elemento dentro del Drive. Solo lectura.                                                                                                            |
| imagen                | [image](image.md)                   | Metadatos de imagen, si el elemento es una imagen. Solo lectura.                                                                                                                       |
| lastModifiedBy       | [identitySet](identityset.md)       | Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.                                                                                    |
| lastModifiedDateTime | DateTimeOffset                      | Fecha y hora de la última modificación del elemento. Solo lectura.                                                                                                                      |
| location             | [geoCoordinates](geoCoordinates.md) | Metadatos de ubicación, si el elemento tiene datos de ubicación. Solo lectura.                                                                                                              |
| name                 | String                              | El nombre del elemento (nombre de archivo y extensión). Lectura y escritura.                                                                                                                |
| paquete              | [package](package.md)               | Si está presente, indica que este elemento es un paquete en lugar de una carpeta o archivo. Los paquetes se tratan como archivos en algunos contextos y como carpetas en otros. Solo lectura.         |
| parentReference      | [itemReference](itemreference.md)   | Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.                                                                                                                 |
| Foto                | [photo](photo.md)                   | Metadatos de foto, si el elemento es una foto. Solo lectura.                                                                                                                        |
| remoteItem           | [remoteItem](remoteitem.md)         | Datos de elemento remoto, si el elemento se comparte desde una unidad distinta a la de acceso. Solo lectura.                                                                        |
| searchResult         | [searchResult](searchresult.md)     | Metadatos de búsqueda, si el elemento es un resultado de búsqueda. Solo lectura.                                                                                                          |
| compartido               | [shared](shared.md)                 | Indica que el elemento se ha compartido con otros usuarios y proporciona información sobre el estado del elemento compartido. Solo lectura.                                               |
| size                 | Int64                               | Tamaño del elemento en bytes. Solo lectura.                                                                                                                                     |
| specialFolder        | [specialFolder](specialfolder.md)   | Si el elemento actual también está disponible como una carpeta especial, se devuelve esta faceta. Solo lectura.                                                                             |
| video                | [video](video.md)                   | Metadatos de vídeo, si el elemento es un vídeo. Solo lectura.                                                                                                                        |
| webUrl               | String                              | Dirección URL que muestra el recurso en el explorador. Solo lectura.                                                                                                                 |

**Nota:** Las propiedades eTag y cTag funcionan de forma diferente en los contenedores (carpetas). El valor de cTag se modifica cuando se cambia el contenido o los metadatos de cualquier descendiente de la carpeta. El valor de eTag solo se modifica cuando se cambian las propiedades de la carpeta, excepto las propiedades que derivan de descendientes (como **childCount** o **lastModifiedDateTime**).

## <a name="instance-attributes"></a>Atributos de instancia

Los atributos de instancia son propiedades con comportamientos especiales. Estas propiedades son temporales y o bien a) definen el comportamiento que debería tener el servicio o b) proporcionan valores de propiedad a corto plazo, como una dirección URL de descarga de un elemento que expira.

| Nombre de propiedad                     | Tipo   | Descripción                                                                                                                                                         |
|:----------------------------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| @microsoft.graph.conflictBehavior | string | El comportamiento de resolución de conflictos para las acciones que crean un nuevo elemento. Puede utilizar los valores de *fail*, *replace*, o *rename*. El valor predeterminado de PUT es *replace*. Nunca se devuelve un elemento con esta anotación. Solo escritura.                               |
| @microsoft.graph.downloadUrl      | string | Una dirección URL que puede utilizarse para descargar el contenido de este archivo. No es necesaria la autenticación con esta dirección URL. Solo lectura.                                                    |
| @microsoft.graph.sourceUrl        | string | Al emitir una solicitud PUT, esta anotación de instancia puede utilizarse para indicar al servicio que descargue el contenido de la dirección URL y lo guarde como el archivo. Solo escritura. |

**Nota:** El valor @microsoft.graph.downloadUrl es una dirección URL de corta duración y no puede almacenarse en caché. La dirección URL solo estará disponible durante un breve período de tiempo antes de ser invalidada.

## <a name="relationships"></a>Relaciones

| Relación       | Tipo                                       | Descripción                                                                                                                                                                       |
|:-------------------|:-------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| children           | Colección [driveitem](driveitem.md)       | Colección que contiene objetos de elemento de los elementos secundarios inmediatos. Solo los elementos que representan carpetas tienen elementos secundarios. Solo lectura. Admite valores NULL.                                        |
| createdByUser      | [user](user.md)                            | Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.                                                                                                  |
| lastModifiedByUser | [user](user.md)                            | Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.                                                                                            |
| permisos        | Colección [permission](permission.md)     | El conjunto de permisos del elemento. Solo lectura. Admite valores NULL.                                                                                                                         |
| miniaturas         | Colección [thumbnailSet](thumbnailset.md) | Colección que contiene objetos [ThumbnailSet](thumbnailSet.md) asociados al elemento. Para obtener más información, consulte [obtener miniaturas](../api/thumbnailset_get.md). Solo lectura. Admite valores NULL. |


## <a name="methods"></a>Métodos

| Método                                                 | Ruta de acceso a REST                                |
|:-------------------------------------------------------|:-----------------------------------------|
| [Obtener elemento](../api/item_get.md)                         | `GET /drive/items/{item-id}`             |
| [Enumerar elementos secundarios](../api/item_list_children.md)          | `GET /drive/items/{item-id}/children`    |
| [Crear elemento](../api/item_post_children.md)            | `POST /drive/items/{item-id}/children`   |
| [Actualizar elemento](../api/item_update.md)                   | `PATCH /drive/items/{item-id}`           |
| [Cargar contenido](../api/item_uploadcontent.md)         | `PUT /drive/items/{item-id}/content`     |
| [Descargar contenido](../api/item_downloadcontent.md)     | `GET /drive/items/{item-id}/content`      |
| [Eliminar elemento](../api/item_delete.md)                   | `DELETE /drive/items/{item-id}`          |
| [Mover elemento](../api/item_move.md)                       | `PATCH /drive/items/{item-id}`           |
| [Copiar elemento](../api/item_copy.md)                       | `POST /drive/items/{item-id}/copy`       |
| [Buscar elementos](../api/item_search.md)                  | `GET /drive/items/{item-id}/search(q='text')`  |
| [Buscar cambios](../api/item_delta.md)                   | `GET /drive/root/delta`                  |
| [Enumerar miniaturas](../api/item_list_thumbnails.md)      | `GET /drive/items/{item-id}/thumbnails`  |
| [Crear vínculo para compartir](../api/item_createlink.md)       | `POST /drive/items/{item-id}/createLink` |
| [Agregar permisos](../api/item_invite.md)               | `POST /drive/items/{item-id}/invite`     |
| [Enumerar permisos](../api/item_list_permissions.md)    | `GET /drive/items/{item-id}/permissions` |
| [Eliminar permiso](../api/permission_delete.md)       | `DELETE /drive/items/{item-id}/permissions/{perm-id}` |


## <a name="remarks"></a>Comentarios

En las bibliotecas de documentos de OneDrive para la Empresa o SharePoint, la propiedad **cTag** no se devuelve si el elemento es una [carpeta](folder.md).

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "item resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->