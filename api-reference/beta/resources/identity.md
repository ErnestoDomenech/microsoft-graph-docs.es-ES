# <a name="identity-resource-type"></a>Tipo de recurso Identity

El recurso **Identity** representa una identidad de un _actor_. Por ejemplo, un actor puede ser un usuario, un dispositivo o una aplicación.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.identity"
}-->

```json
{
  "displayName": "string",
  "id": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad    | Tipo   | Descripción                                                                                                                                                                                                                                                                                                           |
|:------------|:-------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| displayName | String | El nombre para mostrar de la identidad. Tenga en cuenta que puede que no esté siempre disponible o actualizado. Por ejemplo, si un usuario cambia su nombre para mostrar, la API puede mostrar el nuevo valor en una respuesta futura, pero los elementos asociados con el usuario no estarán modificados al usar [delta](../api/item_delta.md).        |
| id          | String | Identificador único de la identidad.                                                                                                                                                                                                                                                                                   |

## <a name="remarks"></a>Comentarios

En algunas circunstancias, puede que el identificador único del actor no esté disponible. En este caso, se devuelve la propiedad **displayName** de la identidad, pero faltará la propiedad **id** del recurso.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "identity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
