# <a name="update-iosdevicefeaturesconfiguration"></a>Actualizar iosDeviceFeaturesConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementConfiguration.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No compatible.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|description|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|assetTagTemplate|String|Información de la etiqueta de activo del dispositivo, se muestra en la ventana de inicio de sesión y en la pantalla de bloqueo.|
|lockScreenFootnote|String|Nota al pie que se muestra en la ventana de inicio de sesión y la pantalla de bloqueo. Disponible en iOS 9.3.1 y versiones posteriores.|
|homeScreenDockIcons|Colección [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)|Lista de las aplicaciones y carpetas que aparecen en el Dock de la pantalla de inicio. Esta colección puede contener un máximo de 500 elementos.|
|homeScreenPages|Colección [iosHomeScreenPage](../resources/intune_deviceconfig_ioshomescreenpage.md)|Lista de páginas en la pantalla de inicio. Esta colección puede contener un máximo de 500 elementos.|
|notificationSettings|Colección [iosNotificationSettings](../resources/intune_deviceconfig_iosnotificationsettings.md)|Configuración de notificaciones de cada identificador de agrupación. Solo se aplica a los dispositivos en modo supervisado (iOS 9.3 y versiones posteriores). Esta colección puede contener un máximo de 500 elementos.|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1983

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "assetTagTemplate": "Asset Tag Template value",
  "lockScreenFootnote": "Lock Screen Footnote value",
  "homeScreenDockIcons": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenFolder",
      "displayName": "Display Name value",
      "pages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
          "displayName": "Display Name value",
          "apps": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenApp",
              "displayName": "Display Name value",
              "bundleID": "Bundle ID value"
            }
          ]
        }
      ]
    }
  ],
  "homeScreenPages": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenPage",
      "displayName": "Display Name value",
      "icons": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolder",
          "displayName": "Display Name value",
          "pages": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
              "displayName": "Display Name value",
              "apps": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenApp",
                  "displayName": "Display Name value",
                  "bundleID": "Bundle ID value"
                }
              ]
            }
          ]
        }
      ]
    }
  ],
  "notificationSettings": [
    {
      "@odata.type": "microsoft.graph.iosNotificationSettings",
      "bundleID": "Bundle ID value",
      "appName": "App Name value",
      "publisher": "Publisher value",
      "enabled": true,
      "showInNotificationCenter": true,
      "showOnLockScreen": true,
      "alertType": "banner",
      "badgesEnabled": true,
      "soundsEnabled": true
    }
  ]
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2160

{
  "@odata.type": "#microsoft.graph.iosDeviceFeaturesConfiguration",
  "id": "651e0ab3-0ab3-651e-b30a-1e65b30a1e65",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "assetTagTemplate": "Asset Tag Template value",
  "lockScreenFootnote": "Lock Screen Footnote value",
  "homeScreenDockIcons": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenFolder",
      "displayName": "Display Name value",
      "pages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
          "displayName": "Display Name value",
          "apps": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenApp",
              "displayName": "Display Name value",
              "bundleID": "Bundle ID value"
            }
          ]
        }
      ]
    }
  ],
  "homeScreenPages": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenPage",
      "displayName": "Display Name value",
      "icons": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolder",
          "displayName": "Display Name value",
          "pages": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
              "displayName": "Display Name value",
              "apps": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenApp",
                  "displayName": "Display Name value",
                  "bundleID": "Bundle ID value"
                }
              ]
            }
          ]
        }
      ]
    }
  ],
  "notificationSettings": [
    {
      "@odata.type": "microsoft.graph.iosNotificationSettings",
      "bundleID": "Bundle ID value",
      "appName": "App Name value",
      "publisher": "Publisher value",
      "enabled": true,
      "showInNotificationCenter": true,
      "showOnLockScreen": true,
      "alertType": "banner",
      "badgesEnabled": true,
      "soundsEnabled": true
    }
  ]
}
```



