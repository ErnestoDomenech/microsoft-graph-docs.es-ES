# <a name="chartlegend-resource-type"></a>Tipo de recurso ChartLegend

Representa la leyenda de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartLegend](../api/chartlegend_get.md) | [ChartLegend](chartlegend.md) |Lee las propiedades y relaciones del objeto chartLegend.|
|[Update](../api/chartlegend_update.md) | [ChartLegend](chartlegend.md)    |Actualiza el objeto ChartLegend. |

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|overlay|boolean|Valor booleano que indica si la leyenda del gráfico debe superponerse al cuerpo principal del gráfico.|
|position|string|Representa la posición de la leyenda del gráfico. Valores posibles: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.|
|visible|boolean|Valor booleano que representa la visibilidad de un objeto ChartLegend.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|format|[ChartLegendFormat](chartlegendformat.md)|Representa el formato de una leyenda del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartLegend"
}-->

```json
{
  "overlay": true,
  "position": "string",
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartLegend resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->