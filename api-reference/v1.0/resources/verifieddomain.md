# <a name="verifieddomain-resource-type"></a>Tipo de recurso verifiedDomain

Especifica un dominio para un inquilino. La propiedad **verifiedDomains** de la entidad [organization](organization.md) es una colección de **VerifiedDomain**.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|capabilities|String|Por ejemplo, "Email", "OfficeCommunicationsOnline".|
|isDefault|Boolean|                **true** si se trata del dominio predeterminado asociado al inquilino; de lo contrario, **false**.            |
|isInitial|Boolean|**true** si se trata del dominio inicial asociado al inquilino; de lo contrario, **false**.|
|name|String|Nombre del dominio; por ejemplo, "contoso.onmicrosoft.com".|
|type|String|Por ejemplo, "Administrado".|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.verifieddomain"
}-->

```json
{
  "capabilities": "string",
  "isDefault": true,
  "isInitial": true,
  "name": "string",
  "type": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "verifiedDomain resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
