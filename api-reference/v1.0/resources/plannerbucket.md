# Tipo de recurso plannerBucket
<a id="plannerbucket-resource-type" class="xliff"></a>

El recurso **plannerBucket** representa un depósito (o "columna personalizada") para las tareas de un plan de Office 365. Se encuentra en un [plannerPlan](plannerPlan.md) y puede tener una colección de [plannerTasks](plannerTask.md).



## Métodos
<a id="methods" class="xliff"></a>

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerBucket](../api/plannerbucket_get.md) | [plannerBucket](plannerbucket.md) |Leer las propiedades y las relaciones del objeto **plannerBucket**.|
|[Enumerar plannerTasks](../api/plannerbucket_list_tasks.md) |Colección [plannerTask](plannertask.md)| Obtenga una colección de objetos **plannerTask**.|
|[Create](../api/planner_post_buckets.md) | [plannerBucket](plannerbucket.md)   | Crear un nuevo objeto **plannerBucket**. |
|[Update](../api/plannerbucket_update.md) | [plannerBucket](plannerbucket.md)   |Actualizar el objeto **plannerBucket**. |
|[Delete](../api/plannerbucket_delete.md) | Ninguno |Eliminar el objeto **plannerBucket**. |

## Propiedades
<a id="properties" class="xliff"></a>
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Solo lectura. Id. del depósito. Tiene 28 caracteres y distingue entre mayúsculas y minúsculas. La [validación del formato](planner_identifiers_disclaimer.md) se efectúa en el servicio.|
|nombre|Cadena|Nombre del depósito.|
|orderHint|Cadena|Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](planner_order_hint_format.md).|
|planId|Cadena|Id. de plan al que pertenece el depósito.|

## Relaciones
<a id="relationships" class="xliff"></a>
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|tasks|Colección [plannerTask](plannertask.md)| Solo lectura. Admite valores NULL. Colección de tareas del depósito.|

## Representación JSON
<a id="json-representation" class="xliff"></a>
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerBucket"
}-->

```json
{
  "id": "String (identifier)",
  "name": "String",
  "orderHint": "String",
  "planId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerBucket resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->