# <a name="subscribedsku-resource-type"></a>Tipo de recurso subscribedSku

Contiene información acerca de una SKU de servicio a la que la empresa está suscrita.

Solo se admite la operación de lectura con las SKU suscritas; no se admiten las operaciones de creación, actualización y eliminación. No se admiten expresiones de filtro de consulta. Se hereda de [DirectoryObject](directoryobject.md).

## <a name="methods"></a>Métodos
| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get subscribedSku](../api/subscribedsku_get.md) | [subscribedSku](subscribedsku.md) |Lea las propiedades y relaciones del objeto subscribedSku.|
|[Enumerar subscribedsku](../api/subscribedsku_list.md) | Colección [subscribedSku](subscribedsku.md) |Recupere la lista de suscripciones comerciales que ha adquirido una organización.|

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|appliesTo|String| Por ejemplo, "usuario" o "empresa". |
|capabilityStatus|String| Por ejemplo, "habilitado". |
|consumedUnits|Int32| El número de licencias asignadas. |
|id|String| El identificador único del recurso del objeto sku suscrito. Clave, no admite valores NULL. |
|prepaidUnits|[licenseUnitsDetail](licenseunitsdetail.md)| Información sobre el número y el estado de las licencias prepagadas. |
|servicePlans|Colección [servicePlanInfo](serviceplaninfo.md)| Información acerca de los planes de servicio que están disponibles con el SKU. No admite valores NULL |
|skuId|Guid| El identificador único (GUID) para el SKU de servicio. |
|skuPartNumber|String| La parte numérica del SKU, por ejemplo: "AAD_PREMIUM" o "RMSBASIC". |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.subscribedSku"
}-->

```json
{
  "appliesTo": "string",
  "capabilityStatus": "string",
  "consumedUnits": 1024,
  "id": "string (identifier)",
  "prepaidUnits": {"@odata.type": "microsoft.graph.licenseUnitsDetail"},
  "servicePlans": [{"@odata.type": "microsoft.graph.servicePlanInfo"}],
  "skuId": "guid",
  "skuPartNumber": "string"
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscribedSku resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
