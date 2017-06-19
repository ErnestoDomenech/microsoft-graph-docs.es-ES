# <a name="plannerassignment-resource-type"></a>Tipo de recurso plannerAssignment

El recurso **plannerAssignment** representa la asignación de una tarea a un usuario. Este tipo se usa en el tipo abierto [plannerAssignments](plannerassignments.md).


### <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|assignedBy|[identitySet](identityset.md)|La identidad del usuario que realiza la asignación de la tarea (el asignante).|
|assignedDateTime|DateTimeOffset|La hora a la que se asignó la tarea. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|orderHint|String|La sugerencia usada para ordenar las personas a las que se ha asignado una tarea. El formato se define tal como se describe [aquí](planner_order_hint_format.md).|

### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerAssignment"
}-->

```json
{
  "assignedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "assignedDateTime": "String (timestamp)",
  "orderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->