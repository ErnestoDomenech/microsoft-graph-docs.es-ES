# <a name="schemaextension-resource-type-schema-extensions"></a>Tipo de recurso schemaExtension (extensiones de esquema)

Las extensiones de esquema permiten definir un esquema para extender y agregar datos personalizados fuertemente tipados a un tipo de recurso. Los datos personalizados aparecen como un tipo complejo en el recurso extendido. 

Las extensiones de esquema son compatibles con los siguientes tipos de recursos:

 - [contact](contact.md)
 - [device](device.md)
 - [evento](event.md) en un usuario o un calendario de grupo de Office 365
 - [post](post.md) de un grupo de Office 365
 - [group](group.md)
 - [message](message.md) 
 - [organization](organization.md)
 - [user](user.md)

Consulte el [ejemplo de extensión de esquema](../../../concepts/extensibility_schema_groups.md) para obtener información sobre cómo agregar datos personalizados a los grupos.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Create](../api/schemaextension_post_schemaextensions.md) | schemaExtension |Crea una definición de extensión de esquema.|
|[List](../api/schemaextension_list.md) | schemaExtension |Enumera las definiciones schemaExtension disponibles y sus propiedades.|
|[Get](../api/schemaextension_get.md) | schemaExtension |Lee las propiedades de una definición schemaExtension específica.|
|[Update](../api/schemaextension_update.md) | schemaExtension   |Actualiza una definición schemaExtension. |
|[Delete](../api/schemaextension_delete.md) | Ninguno |Elimina una definición schemaExtension. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|description|String|Descripción de la extensión de esquema.|
|id|Cadena|Identificador único para la definición de la extensión de esquema. <br>Puede asignar un valor de dos maneras: <ul><li>Concatenar el nombre de uno de los dominios comprobados con un nombre para la extensión del esquema con el fin de formar una cadena única en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}. Por ejemplo, `contoso_mySchema`. </li><li>Proporcionar un nombre de esquema y permitir a Microsoft Graph utilizar ese nombre de esquema para completar la asignación del **id.** en este formato: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Un ejemplo sería `extkvbmkofy_mySchema`.</li></ul>Una vez creada, esta propiedad no se puede modificar. |
|owner|String|El `appId` de la aplicación que es el propietario de la extensión del esquema. Esta propiedad se puede proporcionar en la creación, para establecer el propietario.  Si no se proporciona, entonces la aplicación de llamada `appId` se establecerá como la propietaria. En cualquier caso, el usuario que inició sesión debe ser el propietario de la aplicación. Una vez establecida, esta propiedad es de solo lectura y no se puede cambiar.| 
|properties|Colección [extensionSchemaProperty](extensionschemaproperty.md)|La colección de nombres de propiedad y tipos que conforman la definición de la extensión de esquema.|
|status|Cadena|El estado del ciclo de vida de la extensión de esquema. Los estados posibles son **InDevelopment** (En desarrollo), **Available** (Disponible) y **Deprecated** (En desuso). En el momento de la creación se establece automáticamente en **InDevelopment**. Las [extensiones de esquema](../../../concepts/extensibility_overview.md#schema-extensions) proporcionan más información sobre los comportamientos y las transiciones de estado posibles.|
|targetTypes|String collection|Conjunto de tipos de Microsoft Graph (compatibles con extensiones) a los que se puede aplicar la extensión de esquema. Seleccione **contact**, **device**, **event**, **group**, **message**, **organization**, **post** o **user**.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.schemaExtension"
}-->

```json
{
  "description": "String",
  "id": "String (identifier)",
  "owner": "String",
  "properties": [{"@odata.type": "microsoft.graph.extensionSchemaProperty"}],
  "status": "String",
  "targetTypes": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "schemaExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->