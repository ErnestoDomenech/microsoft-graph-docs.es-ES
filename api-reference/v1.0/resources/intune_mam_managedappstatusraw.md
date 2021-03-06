# <a name="managedappstatusraw-resource-type"></a>Tipo de recurso managedAppStatusRaw

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa un informe de estado sin tipo sobre la configuración y la protección de la aplicación de las organizaciones.

Hereda de [managedAppStatus](../resources/intune_mam_managedappstatus.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedAppStatusRaws](../api/intune_mam_managedappstatusraw_list.md)|Colección [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md)|Enumere las propiedades y las relaciones de los objetos [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md).|
|[Obtener managedAppStatusRaw](../api/intune_mam_managedappstatusraw_get.md)|[managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md)|Lea las propiedades y las relaciones del objeto [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md).|
|[Crear managedAppStatusRaw](../api/intune_mam_managedappstatusraw_create.md)|[managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md)|Cree un objeto [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md).|
|[Eliminar managedAppStatusRaw](../api/intune_mam_managedappstatusraw_delete.md)|Ninguna|Elimina un [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md).|
|[Actualizar managedAppStatusRaw](../api/intune_mam_managedappstatusraw_update.md)|[managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md)|Actualice las propiedades de un objeto [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre descriptivo del informe de estado. Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)|
|id|cadena|Clave de la entidad. Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)|
|versión|cadena|Versión de la entidad. Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)|
|contenido|[Json](../resources/intune_mam_json.md)|Contenido del informe de estado.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppStatusRaw"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppStatusRaw",
  "displayName": "String",
  "id": "String (identifier)",
  "version": "String",
  "content": {
    "@odata.type": "microsoft.graph.Json"
  }
}
```



