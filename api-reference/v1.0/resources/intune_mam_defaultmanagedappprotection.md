# <a name="defaultmanagedappprotection-resource-type"></a>Tipo de recurso defaultManagedAppProtection

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directiva usada para configurar las opciones de administración detallada de un conjunto de aplicaciones específico para todos los usuarios a los que no se destina una directiva TargetedManagedAppProtection

Hereda de [managedAppProtection](../resources/intune_mam_managedappprotection.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar defaultManagedAppProtections](../api/intune_mam_defaultmanagedappprotection_list.md)|Colección [defaultManagedAppProtection](../resources/intune_mam_defaultmanagedappprotection.md)|Enumere las propiedades y las relaciones de los objetos [defaultManagedAppProtection](../resources/intune_mam_defaultmanagedappprotection.md).|
|[Obtener defaultManagedAppProtection](../api/intune_mam_defaultmanagedappprotection_get.md)|[defaultManagedAppProtection](../resources/intune_mam_defaultmanagedappprotection.md)|Lea las propiedades y las relaciones del objeto [defaultManagedAppProtection](../resources/intune_mam_defaultmanagedappprotection.md).|
|[Crear defaultManagedAppProtection](../api/intune_mam_defaultmanagedappprotection_create.md)|[defaultManagedAppProtection](../resources/intune_mam_defaultmanagedappprotection.md)|Cree un objeto [defaultManagedAppProtection](../resources/intune_mam_defaultmanagedappprotection.md).|
|[Eliminar defaultManagedAppProtection](../api/intune_mam_defaultmanagedappprotection_delete.md)|Ninguno|Elimina un [defaultManagedAppProtection](../resources/intune_mam_defaultmanagedappprotection.md).|
|[Actualizar defaultManagedAppProtection](../api/intune_mam_defaultmanagedappprotection_update.md)|[defaultManagedAppProtection](../resources/intune_mam_defaultmanagedappprotection.md)|Actualice las propiedades de un objeto [defaultManagedAppProtection](../resources/intune_mam_defaultmanagedappprotection.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|Cadena|Nombre para mostrar de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|description|Cadena|La descripción de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|id|Cadena|Clave de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|versión|Cadena|Versión de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|periodOfflineBeforeAccessCheck|Duración|El período tras el cual se comprueba el acceso cuando el dispositivo no está conectado a Internet. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|periodOnlineBeforeAccessCheck|Duración|El período tras el cual se comprueba el acceso cuando el dispositivo está conectado a Internet. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|allowedInboundDataTransferSources|Cadena|Orígenes desde los que permite la transferencia de datos. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `allApps`, `managedApps` y `none`.|
|allowedOutboundDataTransferDestinations|Cadena|Destinos a los que permite la transferencia de datos. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `allApps`, `managedApps` y `none`.|
|organizationalCredentialsRequired|Booleano|Indica si son necesarias las credenciales de la organización para usar la aplicación. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|allowedOutboundClipboardSharingLevel|Cadena|El nivel al que puede compartirse el Portapapeles entre aplicaciones en el dispositivo administrado. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `allApps`, `managedAppsWithPasteIn`, `managedApps` y `blocked`.|
|dataBackupBlocked|Booleano|Indica si se bloquea la copia de seguridad de los datos de la aplicación administrada. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|deviceComplianceRequired|Booleano|Indica si se requiere el cumplimiento del dispositivo. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|managedBrowserToOpenLinksRequired|Booleano|Indica si se deberían abrir los vínculos de Internet en la aplicación del explorador administrado. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|saveAsBlocked|Booleano|Indica si los usuarios pueden usar el elemento de menú "Guardar como" para guardar una copia de los archivos protegidos. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|periodOfflineBeforeWipeIsEnforced|Duración|La cantidad de tiempo que una aplicación puede estar desconectada de Internet antes de que se borren los datos administrados. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|pinRequired|Booleano|Indica si se requiere un PIN de nivel de aplicación. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|maximumPinRetries|Int32|Número máximo de intentos de reintento de PIN incorrecto antes de que se borre la aplicación administrada. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|simplePinBlocked|Booleano|Indica si simplePin está bloqueado. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|minimumPinLength|Int32|Longitud mínima de PIN necesaria para un PIN de nivel de aplicación si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|pinCharacterSet|Cadena|Conjunto de caracteres que se puede usar para un PIN de nivel de aplicación si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md). Los valores posibles son: `numeric` y `alphanumericAndSymbol`.|
|periodBeforePinReset|Duración|TimePeriod antes de que se deba restablecer el PIN de todos los niveles si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|allowedDataStorageLocations|Colección de cadenas|Ubicaciones de almacenamiento de datos en las que un usuario puede almacenar datos administrados. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|contactSyncBlocked|Booleano|Indica si se pueden sincronizar los contactos en el dispositivo del usuario. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|printBlocked|Booleano|Indica si se puede imprimir desde las aplicaciones administradas. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|fingerprintBlocked|Booleano|Indica si se permite el uso del lector de huella digital en lugar de un PIN si PinRequired se establece en True. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|disableAppPinIfDevicePinIsSet|Booleano|Indica si es necesario el uso del PIN de la aplicación si se establece el PIN del dispositivo. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|minimumRequiredOsVersion|Cadena|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|minimumWarningOsVersion|Cadena|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada que intenta obtener acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|minimumRequiredAppVersion|Cadena|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|minimumWarningAppVersion|Cadena|Las versiones anteriores a la versión especificada provocarán un mensaje de advertencia en la aplicación administrada. Heredado de [managedAppProtection](../resources/intune_mam_managedappprotection.md)|
|appDataEncryptionType|Cadena|Tipo de cifrado que debería usarse para los datos en una aplicación administrada. (Solo para iOS) Los valores posibles son: `useDeviceSettings`, `afterDeviceRestart`, `whenDeviceLockedExceptOpenFiles` y `whenDeviceLocked`.|
|screenCaptureBlocked|Booleano|Indica si se bloquea la captura de pantalla.|
|encryptAppData|Booleano|Indica si se deben cifrar los datos de la aplicación administrada. Solo para Android|
|disableAppEncryptionIfDeviceEncryptionIsEnabled|Booleano|Cuando se habilita esta configuración, el cifrado de nivel de aplicación está deshabilitado si el cifrado de nivel de dispositivo está activado|
|minimumRequiredSdkVersion|Cadena|Las versiones anteriores a la versión especificada impedirán que la aplicación administrada obtenga acceso a los datos de la compañía.|
|customSettings|Colección [keyValuePair](../resources/intune_mam_keyvaluepair.md)|Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a los usuarios afectados, sin modificar por este servicio|
|deployedAppCount|Int32|Número de aplicaciones en las que se implementará la directiva actual.|
|minimumRequiredPatchVersion|Cadena|Definir el nivel más antiguo de revisión de seguridad de Android necesario para que un usuario pueda tener acceso seguro a la aplicación.|
|minimumWarningPatchVersion|Cadena|Definir el nivel más antiguo de revisión de seguridad de Android recomendado para que un usuario pueda tener acceso seguro a la aplicación.|
|faceIdBlocked|Booleano|Indica si se permite el uso de FaceID en lugar de un PIN si PinRequired se establece en True.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|aplicaciones|Colección [managedMobileApp](../resources/intune_mam_managedmobileapp.md)|Lista de aplicaciones en las que se implementará la directiva.|
|deploymentSummary|[managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md)|Propiedad de navegación para el resumen de implementación de la configuración.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.defaultManagedAppProtection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.defaultManagedAppProtection",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String",
  "periodOfflineBeforeAccessCheck": "String (duration)",
  "periodOnlineBeforeAccessCheck": "String (duration)",
  "allowedInboundDataTransferSources": "String",
  "allowedOutboundDataTransferDestinations": "String",
  "organizationalCredentialsRequired": true,
  "allowedOutboundClipboardSharingLevel": "String",
  "dataBackupBlocked": true,
  "deviceComplianceRequired": true,
  "managedBrowserToOpenLinksRequired": true,
  "saveAsBlocked": true,
  "periodOfflineBeforeWipeIsEnforced": "String (duration)",
  "pinRequired": true,
  "maximumPinRetries": 1024,
  "simplePinBlocked": true,
  "minimumPinLength": 1024,
  "pinCharacterSet": "String",
  "periodBeforePinReset": "String (duration)",
  "allowedDataStorageLocations": [
    "String"
  ],
  "contactSyncBlocked": true,
  "printBlocked": true,
  "fingerprintBlocked": true,
  "disableAppPinIfDevicePinIsSet": true,
  "minimumRequiredOsVersion": "String",
  "minimumWarningOsVersion": "String",
  "minimumRequiredAppVersion": "String",
  "minimumWarningAppVersion": "String",
  "appDataEncryptionType": "String",
  "screenCaptureBlocked": true,
  "encryptAppData": true,
  "disableAppEncryptionIfDeviceEncryptionIsEnabled": true,
  "minimumRequiredSdkVersion": "String",
  "customSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "String",
      "value": "String"
    }
  ],
  "deployedAppCount": 1024,
  "minimumRequiredPatchVersion": "String",
  "minimumWarningPatchVersion": "String",
  "faceIdBlocked": true
}
```



