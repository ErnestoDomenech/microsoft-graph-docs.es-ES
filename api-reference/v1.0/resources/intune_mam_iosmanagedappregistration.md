# <a name="iosmanagedappregistration-resource-type"></a>Tipo de recurso iosManagedAppRegistration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa los detalles de sincronización de una aplicación para iOS, con capacidades de administración, para un usuario específico.
El recurso ManagedAppRegistration representa los detalles de una aplicación, con capacidad de administración, usado por un miembro de la organización.

Hereda de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosManagedAppRegistrations](../api/intune_mam_iosmanagedappregistration_list.md)|Colección [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md)|Enumere las propiedades y las relaciones de los objetos [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md).|
|[Obtener iosManagedAppRegistration](../api/intune_mam_iosmanagedappregistration_get.md)|[iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md)|Lea las propiedades y las relaciones del objeto [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md).|
|[Crear iosManagedAppRegistration](../api/intune_mam_iosmanagedappregistration_create.md)|[iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md)|Cree un objeto [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md).|
|[Eliminar iosManagedAppRegistration](../api/intune_mam_iosmanagedappregistration_delete.md)|Ninguna|Elimina un [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md).|
|[Actualizar iosManagedAppRegistration](../api/intune_mam_iosmanagedappregistration_update.md)|[iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md)|Actualice las propiedades de un objeto [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|createdDateTime|DateTimeOffset|Fecha y hora de creación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|lastSyncDateTime|DateTimeOffset|Fecha y hora de la última sincronización de la aplicación con el servicio de administración. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|applicationVersion|Cadena|Versión de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|managementSdkVersion|Cadena|Versión del SDK de administración de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|platformVersion|Cadena|Versión del sistema operativo. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|deviceType|Cadena|Tipo de dispositivo de host. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|deviceTag|Cadena|La etiqueta generada del SDK de administración de la aplicación, que le ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo. No garantiza que las aplicaciones se relacionen en todas las condiciones. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|deviceName|Cadena|Nombre del dispositivo de host. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|flaggedReasons|Colección string|Cero o más razones por las que se ha marcado el registro de una aplicación. Por ejemplo, una aplicación que se ejecuta en un dispositivo liberado. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|userId|Cadena|El identificador de usuario al que pertenece este registro de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|appIdentifier|[mobileAppIdentifier](../resources/intune_mam_mobileappidentifier.md)|El identificador del paquete de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|id|Cadena|Clave de la entidad. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|versión|Cadena|Versión de la entidad. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|appliedPolicies|Colección [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|Ya se habían aplicado cero o más directivas en la aplicación registrada cuando se sincronizó por última vez con el servicio de administración. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|intendedPolicies|Colección [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|El administrador esperaba cero o más directivas hasta el momento. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|operaciones|Colección [managedAppOperation](../resources/intune_mam_managedappoperation.md)|Se activaron cero o más operaciones de larga duración en el registro de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosManagedAppRegistration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosManagedAppRegistration",
  "createdDateTime": "String (timestamp)",
  "lastSyncDateTime": "String (timestamp)",
  "applicationVersion": "String",
  "managementSdkVersion": "String",
  "platformVersion": "String",
  "deviceType": "String",
  "deviceTag": "String",
  "deviceName": "String",
  "flaggedReasons": [
    "String"
  ],
  "userId": "String",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.iosMobileAppIdentifier",
    "bundleId": "String"
  },
  "id": "String (identifier)",
  "version": "String"
}
```



