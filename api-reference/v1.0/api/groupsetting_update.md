# <a name="update-a-group-setting"></a>Actualizar una configuración de grupo

Actualiza las propiedades de un objeto de configuración de grupo específico.

## <a name="prerequisites"></a>Requisitos previos

Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*

> Nota: Solo los administradores de inquilinos tienen permiso para realizar operaciones de creación, actualización y eliminación.

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->

Actualiza una configuración para todo el inquilino o para un grupo específico.

```http
PATCH /groupSettings/{id}
PATCH /groups/{id}/settings/{id}
```
## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales
| Nombre | Descripción |
|:-----------|:-----------|
| Authorization  | {token} de portador. Obligatorio. |
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. 

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
| values | settingValue | Conjunto actualizado de valores.  NOTA: Debe proporcionar el conjunto de toda la colección. No puede actualizar un único conjunto de valores. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `204 OK` y el objeto [groupSetting](../resources/groupsetting.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "update_groupsetting"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groupSettings/{id}
Content-type: application/json
Content-length: 173

{
  "displayName": "displayName-value",
  "templateId": "templateId-value",
  "values": [
    {
      "name": "name-value",
      "value": "value-value"
    }
  ]
}
```
##### <a name="response"></a>Respuesta

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupSetting"
} -->
```http
HTTP/1.1 204 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update groupSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->