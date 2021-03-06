# <a name="intunebrand-resource-type"></a>Tipo de recurso intuneBrand

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

intuneBrand contiene datos que se usan para personalizar las aplicaciones del Portal de empresa, así como el portal web del usuario final.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|Cadena|Nombre de la compañía u organización que se muestra a los usuarios finales.|
|contactITName|Cadena|Nombre de la persona u organización responsable del soporte técnico de TI.|
|contactITPhoneNumber|Cadena|Número de teléfono de la persona u organización responsable del soporte técnico de TI.|
|contactITEmailAddress|Cadena|Dirección de correo electrónico de la persona u organización responsable del soporte técnico de TI.|
|contactITNotes|Cadena|Comentarios de texto con respecto a la persona u organización responsable del soporte técnico de TI.|
|privacyUrl|Cadena|Dirección URL de la directiva de privacidad de la empresa u organización.|
|onlineSupportSiteUrl|Cadena|Dirección URL del sitio del departamento de soporte técnico de la empresa u organización.|
|onlineSupportSiteName|Cadena|Nombre para mostrar del sitio del departamento de soporte técnico de la empresa u organización.|
|themeColor|[rgbColor](../resources/intune_onboarding_rgbcolor.md)|Color de tema principal utilizado en el portal web y las aplicaciones del Portal de empresa.|
|showLogo|Booleano|Booleano que indica si se muestran o no las imágenes de logotipo proporcionadas por el administrador.|
|lightBackgroundLogo|[mimeContent](../resources/intune_onboarding_mimecontent.md)|Imagen de logotipo que se muestra en las aplicaciones del Portal de empresa con un fondo claro detrás del logotipo.|
|darkBackgroundLogo|[mimeContent](../resources/intune_onboarding_mimecontent.md)|Imagen de logotipo que se muestra en las aplicaciones del Portal de empresa con un fondo oscuro detrás del logotipo.|
|showNameNextToLogo|Booleano|Booleano que indica si se muestra o no el nombre para mostrar proporcionado por el administrador.|
|showDisplayNameNextToLogo|Booleano|Booleano que indica si se muestra o no el nombre para mostrar proporcionado por el administrador.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.intuneBrand"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.intuneBrand",
  "displayName": "String",
  "contactITName": "String",
  "contactITPhoneNumber": "String",
  "contactITEmailAddress": "String",
  "contactITNotes": "String",
  "privacyUrl": "String",
  "onlineSupportSiteUrl": "String",
  "onlineSupportSiteName": "String",
  "themeColor": {
    "@odata.type": "microsoft.graph.rgbColor",
    "r": 1024,
    "g": 1024,
    "b": 1024
  },
  "showLogo": true,
  "lightBackgroundLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "darkBackgroundLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "showNameNextToLogo": true,
  "showDisplayNameNextToLogo": true
}
```



