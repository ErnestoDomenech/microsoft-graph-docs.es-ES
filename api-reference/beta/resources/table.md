# <a name="table-resource-type"></a>Tipo de recurso Table

Representa una tabla de Excel.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get Table](../api/table_get.md) | [Table](table.md) |Lee las propiedades y relaciones del objeto table.|
|[Create TableColumn](../api/table_post_columns.md) |[TableColumn](tablecolumn.md)| Crea un TableColumn publicándolo en la colección columns.|
|[List columns](../api/table_list_columns.md) |Colección [TableColumn](tablecolumn.md)| Obtiene una colección de objetos TableColumn.|
|[Create TableRow](../api/table_post_rows.md) |[TableRow](tablerow.md)| Crea un TableRow publicándolo en la colección rows.|
|[List rows](../api/table_list_rows.md) |Colección [TableRow](tablerow.md)| Obtiene una colección de objetos TableRow.|
|[Update](../api/table_update.md) | [Table](table.md)    |Actualiza el objeto Table. |
|[Databodyrange](../api/table_databodyrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado al cuerpo de datos de la tabla.|
|[Headerrowrange](../api/table_headerrowrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado a la fila de encabezado de la tabla.|
|[Range](../api/table_range.md)|[Range](range.md)|Obtiene el objeto de rango asociado a toda la tabla.|
|[Totalrowrange](../api/table_totalrowrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado a la fila de totales de la tabla.|
|[Clearfilters](../api/table_clearfilters.md)|None|Borra todos los filtros aplicados actualmente en la tabla.|
|[Converttorange](../api/table_converttorange.md)|[Range](range.md)|Convierte la tabla en un rango de celdas normal. Se conservan todos los datos.|
|[Delete](../api/table_delete.md)|None|Elimina la tabla.|
|[Reapplyfilters](../api/table_reapplyfilters.md)|None|Vuelve a aplicar todos los filtros aplicados actualmente en la tabla.|
|[List](../api/table_list.md) | Colección [Table](table.md) |Obtener la colección de objetos table. |
|[Add](../api/tablecollection_add.md)|[Table](table.md)|Crea una tabla nueva. La dirección de origen del rango determina la hoja de cálculo en la que se agregará la tabla. Si no se puede agregar la tabla (por ejemplo, porque la dirección no es válida o porque la tabla se superpondría con otra tabla), se producirá un error.|



## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|id|int|Devuelve un valor que identifica de forma única la tabla de un libro determinado. El valor del identificador permanece igual, incluso cuando se cambia el nombre de la tabla. Solo lectura.|
|name|string|Nombre de la tabla.|
|showHeaders|boolean|Indica si la fila de encabezado está visible o no. Este valor puede establecerse para que muestre o quite la fila de encabezado.|
|showTotals|boolean|Indica si la fila de totales está visible o no. Este valor puede establecerse para que muestre o quite la fila de totales.|
|style|string|Valor constante que representa el estilo de tabla. Los valores posibles son: TableStyleLight1 thru TableStyleLight21, TableStyleMedium1 thru TableStyleMedium28, TableStyleStyleDark1 thru TableStyleStyleDark11. También puede especificarse un estilo personalizado definido por el usuario presente en el libro.|
|highlightFirstColumn|Booleano|Indica si la primera columna contiene un formato especial.    |
|highlightLastColumn|Booleano|Indica si la última columna contiene un formato especial.    |
|showBandedColumns|Booleano|Indica si las columnas muestran un formato con bandas en el que las columnas impares están resaltadas de manera diferente que las pares para facilitar la lectura de la tabla.    |
|showBandedRows|Booleano|Indica si las filas muestran un formato con bandas en el que las filas impares están resaltadas de manera diferente que las pares para facilitar la lectura de la tabla.    |
|showFilterButton|Booleano|Indica si los botones de filtro son visibles en la parte superior de cada encabezado de columna. Esta configuración solo se permite si la tabla contiene una fila de encabezado.    |

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|columns|Colección [TableColumn](tablecolumn.md)|Representa una colección de todas las columnas de la tabla. Solo lectura.|
|rows|Colección [TableRow](tablerow.md)|Representa una colección de todas las filas de la tabla. Solo lectura.|
|sort|[TableSort](tablesort.md)|Representa la ordenación de la tabla. Solo lectura.|
|worksheet|[Worksheet](worksheet.md)|Hoja de cálculo que contiene la tabla actual. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.table"
}-->

```json
{
  "highlightFirstColumn": true,
  "highlightLastColumn": true,
  "id": "String (identifier)",
  "name": "String",
  "showBandedColumns": true,
  "showBandedRows": true,
  "showFilterButton": true,
  "showHeaders": true,
  "showTotals": true,
  "style": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Table resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
