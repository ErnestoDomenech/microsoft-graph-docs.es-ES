# <a name="get-photo"></a>Obtener foto

Obtenga el objeto [profilePhoto](../resources/profilephoto.md) especificado o sus metadatos (propiedades profilePhoto).

Una operación GET busca la foto especificada en el buzón del usuario de Exchange Online.

> **Nota** Esta operación en la versión 1.0 admite solo un buzón de usuario de trabajo o escuela y no uno personal.

## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:

*    Foto de perfil de cualquier usuario del inquilino, incluido el usuario que ha iniciado sesión: *User.ReadBasic.All; User.Read.All; User.ReadWrite.All*
*    Foto de perfil específicamente del usuario que ha iniciado sesión: *User.Read, User.ReadWrite; User.ReadBasic.All; User.Read.All; User.ReadWrite.All*
* Foto de perfil de un **grupo** - *Group.Read.All; Group.ReadWrite.All*
* Foto de un **contacto** - *Contacts.Read; Contacts.ReadWrite*

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

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Authorization  | string  | \<Token\> de portador. Necesario. |

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
Esta solicitud obtiene los metadatos de la foto del usuario que ha iniciado sesión.
<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/photo
```

##### <a name="response-2"></a>Respuesta 2

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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->