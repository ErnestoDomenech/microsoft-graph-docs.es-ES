# <a name="range-lastrow"></a>Range: LastRow

Obtiene la última fila del intervalo. Por ejemplo, la última fila de "B2:D5" es "B5:D5".
## <a name="prerequisites"></a>Requisitos previos
Se requieren los siguientes **ámbitos** para ejecutar esta API: 
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/LastRow
POST /workbook/worksheets(<id|name>)/range(<address>)/LastRow
POST /workbook/tables(<id|name>)/columns(<id|name>)/range/LastRow

```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | Portador<code>|


## <a name="request-body"></a>Cuerpo de la solicitud

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
Aquí tiene un ejemplo de cómo llamar a esta API.
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "range_lastrow"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/LastRow
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: LastRow",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->