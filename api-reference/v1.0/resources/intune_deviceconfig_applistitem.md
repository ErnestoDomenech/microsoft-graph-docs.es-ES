# <a name="applistitem-resource-type"></a>Tipo de recurso appListItem

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa una aplicación en la lista de aplicaciones administradas
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|name|cadena|Nombre de la aplicación|
|publicador|cadena|Publicador de la aplicación|
|appStoreUrl|cadena|Dirección URL de la tienda de la aplicación|
|appId|cadena|El identificador de la aplicación o de la agrupación de la aplicación|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.appListItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.appListItem",
  "name": "String",
  "publisher": "String",
  "appStoreUrl": "String",
  "appId": "String"
}
```



