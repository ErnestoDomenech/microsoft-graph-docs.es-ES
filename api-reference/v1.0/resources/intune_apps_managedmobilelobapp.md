# <a name="managedmobilelobapp-resource-type"></a>Tipo de recurso managedMobileLobApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase base abstracta que contiene las propiedades de todas las aplicaciones de línea de negocio móviles administradas.

Hereda de [managedApp](../resources/intune_apps_managedapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedMobileLobApps](../api/intune_apps_managedmobilelobapp_list.md)|Colección [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)|Enumere las propiedades y las relaciones de los objetos [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).|
|[Obtener managedMobileLobApp](../api/intune_apps_managedmobilelobapp_get.md)|[managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)|Lea las propiedades y las relaciones del objeto [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|displayName|Cadena|El título de la aplicación importado o proporcionado por el administrador. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|descripción|Cadena|La descripción de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|publicador|Cadena|El publicador de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|largeIcon|[mimeContent](../resources/intune_apps_mimecontent.md)|El icono grande, se muestra en los detalles de la aplicación y se usa para cargar el icono. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|isFeatured|Booleano|El valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|privacyInformationUrl|Cadena|La dirección URL de la declaración de privacidad. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|informationUrl|Cadena|La dirección URL para obtener más información. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|propietario|Cadena|Propietario de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|desarrollador|Cadena|El desarrollador de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|notas|Cadena|Notas de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|publishingState|Cadena|El estado de publicación de la aplicación. La aplicación no puede asignarse a menos que se publique. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.|
|appAvailability|Cadena|La disponibilidad de la aplicación. Heredado de [managedApp](../resources/intune_apps_managedapp.md). Los valores posibles son: `global` y `lineOfBusiness`.|
|versión|Cadena|La versión de la aplicación. Heredado de [managedApp](../resources/intune_apps_managedapp.md)|
|committedContentVersion|Cadena|La versión interna confirmada del contenido.|
|fileName|Cadena|El nombre del archivo de la aplicación de LOB principal.|
|tamaño|Int64|El tamaño total, incluidos todos los archivos cargados.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|La lista de categorías para esta aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|asignaciones|Colección [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|contentVersions|Colección [mobileAppContent](../resources/intune_apps_mobileappcontent.md)|La lista de versiones de contenido de esta aplicación.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedMobileLobApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedMobileLobApp",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "isFeatured": true,
  "privacyInformationUrl": "String",
  "informationUrl": "String",
  "owner": "String",
  "developer": "String",
  "notes": "String",
  "publishingState": "String",
  "appAvailability": "String",
  "version": "String",
  "committedContentVersion": "String",
  "fileName": "String",
  "size": 1024
}
```



