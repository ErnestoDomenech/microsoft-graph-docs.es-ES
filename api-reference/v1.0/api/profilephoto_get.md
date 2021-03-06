# <a name="get-photo"></a>Obtener foto

Obtenga el objeto [profilePhoto](../resources/profilephoto.md) especificado o sus metadatos (propiedades profilePhoto).

> **Nota** Esta operación en la versión 1.0 admite solo un buzón profesional o educativo del usuario y no uno personal.

Los tamaños de fotos HD admitidos en Office 365 son los siguientes: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504' y '648x648'. Las fotos pueden ser de cualquier dimensión si se almacenan en Azure Active Directory.

Puede obtener los metadatos de la foto más grande disponible, o bien especifique un tamaño para obtener los metadatos de ese tamaño de foto.
Si el tamaño solicitado no está disponible, puede obtener un tamaño menor que el usuario haya cargado y facilitado.
Por ejemplo, si el usuario carga una foto de 504 x 504 píxeles, todos los tamaños de la foto salvo el de 648 x 648 estarán disponible para su descarga.
Si el tamaño especificado no está disponible en el buzón del usuario o en Azure Active Directory, se devolverá el tamaño de "1 x 1" con el resto de los metadatos.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Tipo de recurso del **usuario**:<br/>User.Read, User.ReadBasic.All, User.Read.All, User.ReadWrite, User.ReadWrite.All<br /><br />Para el recurso de **grupo**:<br />Group.Read.All, Group.ReadWrite.All<br /><br />Para el recurso de **contacto**:<br />Contacts.Read, Contacts.ReadWrite |
|Delegado (cuenta personal de Microsoft) | No admitido |
|Aplicación                        | Tipo de recurso del **usuario**:<br/>User.Read.All, User.ReadWrite.All<br /><br />Para el recurso de **grupo**:<br />Group.Read.All, Group.ReadWrite.All<br /><br />Para el recurso de **contacto**:<br />Contacts.Read, Contacts.ReadWrite |


## <a name="http-request-to-get-the-photo"></a>Solicitud HTTP para obtener la foto
<!-- { "blockType": "ignored" } -->
```http
GET /me/photo/$value
GET /users/{id | userPrincipalName}/photo/$value
GET /groups/{id}/photo/$value
GET /me/contacts/{id}/photo/$value
GET /users/{id | userPrincipalName}/contacts/{id}/photo/$value
GET /me/contactfolders/{contactFolderId}/contacts/{id}/photo/$value
GET /users/{id | userPrincipalName}/contactfolders/{contactFolderId}/contacts/{id}/photo/$value
```
## <a name="http-request-to-get-the-metadata-of-the-photo"></a>Solicitud HTTP para obtener los metadatos de la foto
<!-- { "blockType": "ignored" } -->
```http
GET /me/photo
GET /users/{id | userPrincipalName}/photo
GET /groups/{id}/photo
GET /me/contacts/{id}/photo
GET /users/{id | userPrincipalName}/contacts/{id}/photo
GET /me/contactfolders/{contactFolderId}/contacts/{id}/photo
GET /users/{id | userPrincipalName}/contactfolders/{contactFolderId}/contacts/{id}/photo
```

## <a name="parameters"></a>Parámetros

|**Parámetro**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|_Parámetros de dirección URL_|
|size  |String  | Un tamaño de foto. Los tamaños de fotos HD admitidos en Office 365 son los siguientes: '48x48', '64x64', '96x96', '120x120', '240x240', 
'360x360','432x432', '504x504' y '648x648'. Las fotos pueden ser de cualquier dimensión si se almacenan en Azure Active Directory. |

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.
## <a name="response-for-getting-the-photo"></a>Respuesta para obtener la foto
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y los datos binarios de la foto solicitada.  Si no hay ninguna foto, la operación devuelve `404 Not Found`.
## <a name="response-for-getting-the-metadata-of-the-photo"></a>Respuesta para obtener los metadatos de la foto
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [profilePhoto](../resources/profilePhoto.md) en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request-1"></a>Solicitud 1
Esta solicitud obtiene la foto del usuario que ha iniciado sesión, en el tamaño más grande disponible.
<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/photo/$value
```

##### <a name="response-1"></a>Respuesta 1
Contiene los datos binarios de la foto solicitada. El código de respuesta HTTP es 200.

##### <a name="request-2"></a>Solicitud 2
Esta solicitud recibe la foto de 48x48 para el usuario que inició sesión.

<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/photos/48x48/$value
Content-Type: image/jpg
```

##### <a name="response-2"></a>Respuesta 2
Contiene los datos binarios de la foto de 48x48 solicitada. El código de respuesta HTTP es 200.

##### <a name="request-3"></a>Solicitud 3
Esta solicitud obtiene los metadatos de la foto del usuario que ha iniciado sesión.
<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/photo
```

##### <a name="response-3"></a>Respuesta 3

Los siguientes datos de respuesta muestran los metadatos de la foto. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar.
<!-- {
  "blockType": "ignored"
}-->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/photo/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-7d04-b48b-20075df800e5@1717622f-1d94-c0d4-9d74-f907ad6677b4')/photo",
    "@odata.mediaContentType": "image/jpeg",
    "@odata.mediaEtag": "\"BA09D118\"",
    "id": "240X240",
    "width": 240,
    "height": 240
}
```

Los datos de respuesta siguientes muestran el contenido de una respuesta cuando aún no se ha cargado ninguna foto para el usuario. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar.

<!-- {
  "blockType": "ignored"
}-->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/photo/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-7d04-b48b-20075df800e5@1717622f-1d94-c0d4-9d74-f907ad6677b4')/photo",
    "@odata.mediaContentType": "image/gif",
    "@odata.mediaEtag": "",
    "id": "1X1",
    "width": 1,
    "height": 1
}
```
## <a name="using-the-binary-data-of-the-requested-photo"></a>Usar los datos binarios de la foto solicitada

Cuando use el punto de conexión `/photo/$value` para obtener los datos binarios de una foto de perfil, tendrá que convertir los datos en una cadena en base 64 para agregarlos como datos adjuntos de correo electrónico. Este es un ejemplo de JavaScript de cómo crear una matriz que se puede pasar como valor del parámetro `Attachments` de un [mensaje de Outlook](user_post_messages.md).

      const attachments = [{
        '@odata.type': '#microsoft.graph.fileAttachment',
        ContentBytes: file.toString('base64'),
        Name: 'mypic.jpg'
      }];

Vea el [Ejemplo de conexión a Microsoft Graph de Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample) para obtener una implementación de este ejemplo.

Si quiere que la imagen aparezca en una página web, cree un objeto en memoria de la imagen y conviértalo en el origen de un elemento Image. Este es un ejemplo de JavaScript de esta operación.

    const url = window.URL || window.webkitURL;
    const blobUrl = url.createObjectURL(image.data);
    document.getElementById(imageElement).setAttribute("src", blobUrl);

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
