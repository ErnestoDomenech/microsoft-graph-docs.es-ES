# <a name="androidminimumoperatingsystem-resource-type"></a>Tipo de recurso androidMinimumOperatingSystem

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del sistema operativo mínimo necesario para una aplicación móvil de Android.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|v4_0|Booleano|Versión 4.0 o posterior.|
|v4_0_3|Booleano|Versión 4.0.3 o posterior.|
|v4_1|Booleano|Versión 4.1 o posterior.|
|v4_2|Booleano|Versión 4.2 o posterior.|
|v4_3|Booleano|Versión 4.3 o posterior.|
|v4_4|Booleano|Versión 4.4 o posterior.|
|v5_0|Booleano|Versión 5.0 o posterior.|
|v5_1|Booleano|Versión 5.1 o posterior.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidMinimumOperatingSystem",
  "v4_0": true,
  "v4_0_3": true,
  "v4_1": true,
  "v4_2": true,
  "v4_3": true,
  "v4_4": true,
  "v5_0": true,
  "v5_1": true
}
```



