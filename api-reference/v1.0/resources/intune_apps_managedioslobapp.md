# <a name="managedioslobapp-resource-type"></a>Tipo de recurso managedIOSLobApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades y las propiedades heredadas de las aplicaciones administradas de línea de negocio de iOS.

Hereda de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedIOSLobApps](../api/intune_apps_managedioslobapp_list.md)|Colección [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md)|Enumere las propiedades y las relaciones de los objetos [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).|
|[Obtener managedIOSLobApp](../api/intune_apps_managedioslobapp_get.md)|[managedIOSLobApp](../resources/intune_apps_managedioslobapp.md)|Lea las propiedades y las relaciones del objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).|
|[Crear managedIOSLobApp](../api/intune_apps_managedioslobapp_create.md)|[managedIOSLobApp](../resources/intune_apps_managedioslobapp.md)|Cree un objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).|
|[Eliminar managedIOSLobApp](../api/intune_apps_managedioslobapp_delete.md)|Ninguna|Elimina un [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).|
|[Actualizar managedIOSLobApp](../api/intune_apps_managedioslobapp_update.md)|[managedIOSLobApp](../resources/intune_apps_managedioslobapp.md)|Actualice las propiedades de un objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).|

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
|committedContentVersion|Cadena|La versión interna confirmada del contenido. Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)|
|fileName|Cadena|El nombre del archivo de la aplicación de LOB principal. Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)|
|tamaño|Int64|El tamaño total, incluidos todos los archivos cargados. Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)|
|bundleId|Cadena|El nombre de la identidad.|
|applicableDeviceType|[iosDeviceType](../resources/intune_apps_iosdevicetype.md)|La arquitectura de iOS en la cual se puede ejecutar esta aplicación.|
|minimumSupportedOperatingSystem|[iosMinimumOperatingSystem](../resources/intune_apps_iosminimumoperatingsystem.md)|El valor para el sistema operativo mínimo aplicable.|
|expirationDateTime|DateTimeOffset|La fecha de expiración.|
|versionNumber|Cadena|El número de la versión de la aplicación administrada de línea de negocio (LoB) de iOS.|
|buildNumber|Cadena|El número de compilación de la aplicación administrada de línea de negocio (LoB) de iOS.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|La lista de categorías para esta aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|asignaciones|Colección [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|contentVersions|Colección [mobileAppContent](../resources/intune_apps_mobileappcontent.md)|La lista de versiones de contenido de esta aplicación. Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedIOSLobApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedIOSLobApp",
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
  "size": 1024,
  "bundleId": "String",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true
  },
  "expirationDateTime": "String (timestamp)",
  "versionNumber": "String",
  "buildNumber": "String"
}
```



