# <a name="create-group"></a>Crear grupo

Use esta API para crear un grupo como se especifica en el cuerpo de la solicitud. Puede crear uno de 3 tipos de grupos:

* Grupo de Office 365 (también conocido como grupo unificado)
* Grupo dinámico
* Grupo de seguridad


## <a name="prerequisites"></a>Requisitos previos
Se requiere el siguiente **ámbito** para ejecutar esta API: _Group.ReadWrite.All_ 
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /groups
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | cadena  | Portador de <token>. Necesario. |

## <a name="request-body"></a>Cuerpo de la solicitud
La tabla siguiente muestra las propiedades del recurso [grupo](../resources/group.md) que debe especificar al mínimo al crear un grupo. 

| Propiedad | Tipo | Descripción|
|:---------------|:--------|:----------|
| displayName | string | El nombre para mostrar en la libreta de direcciones del grupo. |
| mailEnabled | boolean | Establézcalo en **true** para grupos habilitados para correo. Establézcalo en **true** si está creando un grupo de Office 365. Establézcalo en **false** si está creando un grupo dinámico o de seguridad.|
| mailNickname | string | El alias de correo del grupo. |
| securityEnabled | boolean | Establézcalo en **true** para grupos con seguridad habilitada. Establézcalo en **true** si está creando un grupo dinámico o de seguridad. Establézcalo en **false** si está creando un grupo de Office 365. |

Especificar la propiedad **groupTypes** si está creando un grupo de Office 365 o dinámico, como se indica a continuación.

| Tipo de grupo | Propiedad **groupTypes** |
|:--------------|:------------------------|
| Office 365 (también conocido como grupo unificado)| "Unificado" | 
| Dinámico | "DynamicMembership" | 
| Seguridad | Sin establecer. | 

Especifique otras propiedades modificables según sea necesario para su grupo. Para más información, vea las propiedades del recurso [grupo](../resources/group.md).

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Este es un ejemplo de una solicitud que crea un grupo de Office 365.
<!-- {
  "blockType": "request",
  "name": "create_group_from_groups"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups
Content-type: application/json
Content-length: 244

{
  "description": "Self help community for library",
  "displayName": "Library Assist",
  "groupTypes": [
    "Unified"
  ],
  "mailEnabled": true,
  "mailNickname": "library",
  "securityEnabled": false
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán más propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 244

{
  "description": "Self help community for library",
  "displayName": "Library Assist",
  "groupTypes": [
    "Unified"
  ],
  "mail": "library@contoso.onmicrosoft.com",
  "mailEnabled": true,
  "mailNickname": "library",
  "securityEnabled": false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->