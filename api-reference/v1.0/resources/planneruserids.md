# Tipo de recurso plannerUserIds
<a id="planneruserids-resource-type" class="xliff"></a>

El recurso **plannerUserIds** representa la lista de identificadores de usuario con los que se comparte un [plan](plannerplan.md). Este es un tipo abierto. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos para compartir el plan del [grupo](group.md). También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo.


## Propiedades
<a id="properties" class="xliff"></a>
El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar los id. de usuario como propiedades y sus valores deben ser el booleano `true`. Si los id. de usuario ya no se comparten, las propiedades se quitarán automáticamente estableciendo sus valores en el booleano `false`.


## Representación JSON
<a id="json-representation" class="xliff"></a>

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerUserIds"
}-->

```json
{
  "String-value": true
}
```

// Ejemplo
```json
{
  "400723e1-102b-43aa-aba9-f35524827084": true, // property name is user id
  "f117339e-c914-4a9c-9b66-1c062b027556": true,
  "e886d105-23b9-47e2-bde1-757e75ee4a28": true
}

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerUserIds resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->