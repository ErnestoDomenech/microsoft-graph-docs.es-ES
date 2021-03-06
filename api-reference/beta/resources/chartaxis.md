# <a name="chartaxis-resource-type"></a>Tipo de recurso ChartAxis

Representa un solo eje de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartAxis](../api/chartaxis_get.md) | [ChartAxis](chartaxis.md) |Lee las propiedades y relaciones del objeto chartAxis.|
|[Update](../api/chartaxis_update.md) | [ChartAxis](chartaxis.md)    |Actualiza el objeto ChartAxis. |

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|majorUnit|object|Representa el intervalo entre dos marcas de graduación principales. Puede establecerse en un valor numérico o en una cadena vacía.  El valor devuelto siempre es un número.|
|maximum|object|Representa el valor máximo del eje de valores.  Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos).  El valor devuelto siempre es un número.|
|minimum|object|Representa el valor mínimo del eje de valores. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.|
|minorUnit|object|Representa el rango entre dos marcas de graduación secundarias. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|format|[ChartAxisFormat](chartaxisformat.md)|Representa el formato de un objeto de gráfico, que incluye el formato de línea y de fuente. Solo lectura.|
|majorGridlines|[ChartGridlines](chartgridlines.md)|Devuelve un objeto de línea de cuadrícula que representa las líneas de cuadrícula principales del eje especificado. Solo lectura.|
|minorGridlines|[ChartGridlines](chartgridlines.md)|Devuelve un objeto de línea de cuadrícula que representa las líneas de cuadrícula secundarias del eje especificado. Solo lectura.|
|title|[ChartAxisTitle](chartaxistitle.md)|Representa el título del eje. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartaxis"
}-->

```json
{
  "majorUnit": "string",
  "maximum": "string",
  "minimum": "string",
  "minorUnit": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxis resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->