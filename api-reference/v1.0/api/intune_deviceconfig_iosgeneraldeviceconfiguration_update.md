# <a name="update-iosgeneraldeviceconfiguration"></a>Actualizar iosGeneralDeviceConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [iosGeneralDeviceConfiguration](../resources/intune_deviceconfig_iosgeneraldeviceconfiguration.md).
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
En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosGeneralDeviceConfiguration](../resources/intune_deviceconfig_iosgeneraldeviceconfiguration.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosGeneralDeviceConfiguration](../resources/intune_deviceconfig_iosgeneraldeviceconfiguration.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|description|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|accountBlockModification|Boolean|Indica si se va a permitir la modificación de cuentas cuando el dispositivo está en modo supervisado.|
|activationLockAllowWhenSupervised|Boolean|Indica si se va a permitir el bloqueo de activación cuando el dispositivo está en modo supervisado.|
|airDropBlocked|Boolean|Indica si se va a permitir AirDrop cuando el dispositivo está en modo supervisado.|
|airDropForceUnmanagedDropTarget|Boolean|Indica si se va a hacer que AirDrop se considere un destino de colocación no administrado (iOS 9.0 y versiones posteriores).|
|airPlayForcePairingPasswordForOutgoingRequests|Boolean|Indica si se va a forzar que todos los dispositivos que reciban solicitudes de AirPlay de este dispositivo usen una contraseña de emparejamiento.|
|appleWatchBlockPairing|Boolean|Indica si se va a permitir el emparejamiento con Apple Watch cuando el dispositivo está en modo supervisado (iOS 9.0 y versiones posteriores).|
|appleWatchForceWristDetection|Boolean|Indica si se va a forzar que un Apple Watch emparejado use la detección de muñeca (iOS 8.2 y versiones posteriores).|
|appleNewsBlocked|Boolean|Indica si se va a impedir que el usuario utilice Noticias cuando el dispositivo está en modo supervisado (iOS 9.0 y versiones posteriores).|
|appsSingleAppModeList|Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)|Obtiene o establece la lista de aplicaciones de iOS que pueden entrar de forma autónoma en el Modo de aplicación única. Solo bajo supervisión. iOS 7.0 y versiones posteriores. Esta colección puede contener un máximo de 500 elementos.|
|appsVisibilityList|Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)|Lista de aplicaciones en la lista de visibilidad (sea la lista de aplicaciones visibles o que se pueden iniciar o la lista de aplicaciones ocultas o que no se pueden iniciar, controlada por AppsVisibilityListType) (iOS 9.3 y versiones posteriores). Esta colección puede contener un máximo de 10 000 elementos.|
|appsVisibilityListType|String|Tipo de lista que se encuentra en la AppsVisibilityList. Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.|
|appStoreBlockAutomaticDownloads|Boolean|Indica si se va a impedir la descarga automática de aplicaciones compradas en otros dispositivos cuando el dispositivo está en modo supervisado (iOS 9.0 y versiones posteriores).|
|appStoreBlocked|Boolean|Indica si se va a impedir que el usuario utilice la aplicación App Store.|
|appStoreBlockInAppPurchases|Boolean|Indica si se va a impedir que el usuario haga compras en la aplicación.|
|appStoreBlockUIAppInstallation|Boolean|Indica si se va a bloquear la aplicación App Store, sin restringir la instalación mediante aplicaciones host. Se aplica solo al modo supervisado (iOS 9.0 o posterior).|
|appStoreRequirePassword|Boolean|Indica si se va a requerir una contraseña cuando se use la tienda de aplicaciones.|
|bluetoothBlockModification|Boolean|Indica si se va a permitir la modificación de la configuración Bluetooth cuando el dispositivo está en modo supervisado (iOS 10.0 y versiones posteriores).|
|cameraBlocked|Boolean|Indica si se va a impedir que el usuario tenga acceso a la cámara del dispositivo.|
|cellularBlockDataRoaming|Boolean|Indica si se va a bloquear la itinerancia de datos.|
|cellularBlockGlobalBackgroundFetchWhileRoaming|Boolean|Indica si se va a bloquear la captura de fondo global mientras se está en itinerancia.|
|cellularBlockPerAppDataModification|Boolean|Indica si se van a permitir los cambios en la configuración de uso de datos de aplicaciones de telefonía móvil cuando el dispositivo está en modo supervisado.|
|cellularBlockPersonalHotspot|Boolean|Indica si se va a bloquear el punto de acceso personal.|
|cellularBlockVoiceRoaming|Boolean|Indica si se va a bloquear la itinerancia de voz.|
|certificatesBlockUntrustedTlsCertificates|Boolean|Indica si se van a bloquear los certificados TLS que no son de confianza.|
|classroomAppBlockRemoteScreenObservation|Boolean|Indica si se va a permitir la observación de pantalla remota de la aplicación Classroom cuando el dispositivo está en modo supervisado (iOS 9.3 y versiones posteriores).|
|classroomAppForceUnpromptedScreenObservation|Boolean|Indica si se va a autorizar de forma automática al profesor de un curso administrado en la aplicación Classroom para que vea la pantalla de un alumno sin preguntarle cuando el dispositivo está en modo supervisado.|
|compliantAppsList|Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)|Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType). Esta colección puede contener un máximo de 10 000 elementos.|
|compliantAppListType|String|Lista que se encuentra en la AppComplianceList. Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.|
|configurationProfileBlockChanges|Boolean|Indica si se va a impedir que el usuario instale perfiles de configuración y certificados de forma interactiva cuando el dispositivo está en modo supervisado.|
|definitionLookupBlocked|Boolean|Indica si se va a bloquear la búsqueda de definiciones cuando el dispositivo está en modo supervisado (iOS 8.1.3 y versiones posteriores).|
|deviceBlockEnableRestrictions|Boolean|Indica si se va a permitir que el usuario active las restricciones en los ajustes del dispositivo cuando el dispositivo está en modo supervisado.|
|deviceBlockEraseContentAndSettings|Boolean|Indica si se va a permitir el uso de la opción "Borrar todo el contenido y la configuración" en el dispositivo cuando está en modo supervisado.|
|deviceBlockNameModification|Boolean|Indica si se va a permitir la modificación del nombre del dispositivo cuando el dispositivo está en modo supervisado (iOS 9.0 y versiones posteriores).|
|diagnosticDataBlockSubmission|Boolean|Indica si se va a bloquear el envío de datos de diagnóstico.|
|diagnosticDataBlockSubmissionModification|Boolean|Indica si se va a permitir la modificación de los ajustes del envío de diagnósticos cuando el dispositivo está en modo supervisado (iOS 9.3.2 y versiones posteriores).|
|documentsBlockManagedDocumentsInUnmanagedApps|Boolean|Indica si se va a impedir que el usuario visualice documentos administrados en las aplicaciones no administradas.|
|documentsBlockUnmanagedDocumentsInManagedApps|Boolean|Indica si se va a impedir que el usuario visualice documentos no administrados en las aplicaciones administradas.|
|emailInDomainSuffixes|Colección String|Una dirección de correo electrónico que carezca de un sufijo que coincida con cualquiera de estas cadenas se considerará fuera de dominio.|
|enterpriseAppBlockTrust|Boolean|Indica si se va a impedir que el usuario confíe en una aplicación empresarial.|
|enterpriseAppBlockTrustModification|Boolean|Indica si se va a impedir que el usuario modifique la configuración de confianza de una aplicación empresarial.|
|faceTimeBlocked|Boolean|Indica si se va a impedir que el usuario utilice FaceTime.|
|findMyFriendsBlocked|Boolean|Indica si se va a bloquear la aplicación Buscar a mis amigos cuando el dispositivo está en modo supervisado.|
|gamingBlockGameCenterFriends|Boolean|Indica si se va a impedir que el usuario tenga amigos en Game Center.|
|gamingBlockMultiplayer|Boolean|Indica si se va a impedir que el usuario utilice los juegos multijugador.|
|gameCenterBlocked|Boolean|Indica si se va a impedir que el usuario utilice Game Center cuando el dispositivo está en modo supervisado.|
|hostPairingBlocked|Boolean|Indica si se va a permitir el emparejamiento de host para controlar los dispositivos con los que se puede emparejar un dispositivo iOS cuando está en modo supervisado.|
|iBooksStoreBlocked|Boolean|Indica si se va a impedir que el usuario utilice iBooks Store cuando el dispositivo está en modo supervisado.|
|iBooksStoreBlockErotica|Boolean|Indica si se va a impedir que el usuario descargue archivos multimedia que se han etiquetado como eróticos desde iBookstore.|
|iCloudBlockActivityContinuation|Boolean|Indica si se va a impedir que el usuario continúe con el trabajo que empezó en el dispositivo iOS en otro dispositivo macOS o iOS.|
|iCloudBlockBackup|Boolean|Indica si se va a bloquear la copia de seguridad de iCloud.|
|iCloudBlockDocumentSync|Boolean|Indica si se va a bloquear la sincronización de documentos de iCloud.|
|iCloudBlockManagedAppsSync|Boolean|Indica si se va a bloquear la sincronización en la nube de aplicaciones administradas.|
|iCloudBlockPhotoLibrary|Boolean|Indica si se va a bloquear la Fototeca de iCloud.|
|iCloudBlockPhotoStreamSync|Boolean|Indica si se va a bloquear la sincronización de fotos en streaming de iCloud.|
|iCloudBlockSharedPhotoStream|Boolean|Indica si se va a bloquear la sincronización de fotos en streaming compartidas.|
|iCloudRequireEncryptedBackup|Boolean|Indica si se va a requerir que las copias de seguridad de iCloud estén cifradas.|
|iTunesBlockExplicitContent|Boolean|Indica si se va a impedir que el usuario tenga acceso a contenido explícito en iTunes y la aplicación App Store.|
|iTunesBlockMusicService|Boolean|Indica si se va a bloquear el servicio Música y revertir la aplicación Música al modo clásico cuando el dispositivo está en modo supervisado (iOS 9.3 y versiones posteriores, y macOS 10.12 y versiones posteriores).|
|iTunesBlockRadio|Boolean|Indica si se va a impedir que el usuario utilice iTunes Radio cuando el dispositivo está en modo supervisado (iOS 9.3 y versiones posteriores).|
|keyboardBlockAutoCorrect|Boolean|Indica si se va a bloquear el autocorrector cuando el dispositivo está en modo supervisado (iOS 8.1.3 y versiones posteriores).|
|keyboardBlockDictation|Boolean|Indica si se va a impedir que el usuario utilice la entrada por dictado cuando el dispositivo está en modo supervisado.|
|keyboardBlockPredictive|Boolean|Indica si se van a bloquear los teclados predictivos cuando el dispositivo está en modo supervisado (iOS 8.1.3 y versiones posteriores).|
|keyboardBlockShortcuts|Boolean|Indica si se van a bloquear los métodos abreviados de teclado cuando el dispositivo está en modo supervisado (iOS 9.0 y versiones posteriores).|
|keyboardBlockSpellCheck|Boolean|Indica si se va a bloquear la revisión ortográfica cuando el dispositivo está en modo supervisado (iOS 8.1.3 y versiones posteriores).|
|kioskModeAllowAssistiveSpeak|Boolean|Indica si se va a permitir la lectura de asistencia en el modo de pantalla completa.|
|kioskModeAllowAssistiveTouchSettings|Boolean|Indica si se va a permitir el acceso a los ajustes de AssistiveTouch en el modo de pantalla completa.|
|kioskModeAllowAutoLock|Boolean|Indica si se va a permitir el bloqueo automático del dispositivo en el modo de pantalla completa.|
|kioskModeAllowColorInversionSettings|Boolean|Indica si se va a permitir el acceso a la configuración de inversión del color en el modo de pantalla completa.|
|kioskModeAllowRingerSwitch|Boolean|Indica si se va a permitir el uso del cambio de tono en el modo de pantalla completa.|
|kioskModeAllowScreenRotation|Boolean|Indica si se va a permitir la rotación de pantalla en el modo de pantalla completa.|
|kioskModeAllowSleepButton|Boolean|Indica si se va a permitir el uso del botón de suspensión en el modo de pantalla completa.|
|kioskModeAllowTouchscreen|Boolean|Indica si se va a permitir el uso de la pantalla táctil en el modo de pantalla completa.|
|kioskModeAllowVoiceOverSettings|Boolean|Indica si se va a permitir el acceso a la configuración de voz en off en el modo de pantalla completa.|
|kioskModeAllowVolumeButtons|Boolean|Indica si se va a permitir el uso de los botones de volumen en el modo de pantalla completa.|
|kioskModeAllowZoomSettings|Boolean|Indica si se va a permitir el acceso a la configuración de zoom en el modo de pantalla completa.|
|kioskModeAppStoreUrl|String|Dirección URL en la tienda de aplicaciones a la aplicación que se usará para el modo de pantalla completa. Úsela si se desconoce KioskModeManagedAppId.|
|kioskModeRequireAssistiveTouch|Boolean|Indica si se va a requerir AssistiveTouch en el modo de pantalla completa.|
|kioskModeRequireColorInversion|Boolean|Indica si se va a requerir la inversión de color en el modo de pantalla completa.|
|kioskModeRequireMonoAudio|Boolean|Indica si se va a requerir el audio mono en el modo de pantalla completa.|
|kioskModeRequireVoiceOver|Boolean|Indica si se va a requerir la voz en off en el modo de pantalla completa.|
|kioskModeRequireZoom|Boolean|Indica si se va a requerir el zoom en el modo de pantalla completa.|
|kioskModeManagedAppId|String|Identificador de la aplicación administrada que se usará para el modo de pantalla completa. Si se especifica KioskModeManagedAppId, se omitirá KioskModeAppStoreUrl.|
|lockScreenBlockControlCenter|Boolean|Indica si se va a impedir que el usuario utilice el centro de control en la pantalla de bloqueo.|
|lockScreenBlockNotificationView|Boolean|Indica si se va a impedir que el usuario utilice la visualización de notificaciones en la pantalla de bloqueo.|
|lockScreenBlockPassbook|Boolean|Indica si se va a impedir que el usuario utilice Passbook cuando el dispositivo está bloqueado.|
|lockScreenBlockTodayView|Boolean|Indica si se va a impedir que el usuario utilice la vista de hoy en la pantalla de bloqueo.|
|mediaContentRatingAustralia|[mediaContentRatingAustralia](../resources/intune_deviceconfig_mediacontentratingaustralia.md)|Opciones de clasificación de contenido multimedia para Australia.|
|mediaContentRatingCanada|[mediaContentRatingCanada](../resources/intune_deviceconfig_mediacontentratingcanada.md)|Opciones de clasificación de contenido multimedia para Canadá.|
|mediaContentRatingFrance|[mediaContentRatingFrance](../resources/intune_deviceconfig_mediacontentratingfrance.md)|Opciones de clasificación de contenido multimedia para Francia.|
|mediaContentRatingGermany|[mediaContentRatingGermany](../resources/intune_deviceconfig_mediacontentratinggermany.md)|Opciones de clasificación de contenido multimedia para Alemania.|
|mediaContentRatingIreland|[mediaContentRatingIreland](../resources/intune_deviceconfig_mediacontentratingireland.md)|Opciones de clasificación de contenido multimedia para Irlanda.|
|mediaContentRatingJapan|[mediaContentRatingJapan](../resources/intune_deviceconfig_mediacontentratingjapan.md)|Opciones de clasificación de contenido multimedia para Japón.|
|mediaContentRatingNewZealand|[mediaContentRatingNewZealand](../resources/intune_deviceconfig_mediacontentratingnewzealand.md)|Opciones de clasificación de contenido multimedia para Nueva Zelanda.|
|mediaContentRatingUnitedKingdom|[mediaContentRatingUnitedKingdom](../resources/intune_deviceconfig_mediacontentratingunitedkingdom.md)|Opciones de clasificación de contenido multimedia para el Reino Unido.|
|mediaContentRatingUnitedStates|[mediaContentRatingUnitedStates](../resources/intune_deviceconfig_mediacontentratingunitedstates.md)|Opciones de clasificación de contenido multimedia para Estados Unidos.|
|networkUsageRules|Colección [iosNetworkUsageRule](../resources/intune_deviceconfig_iosnetworkusagerule.md)|Lista de aplicaciones administradas y las reglas de red que se les aplican. Esta colección puede contener un máximo de 1000 elementos.|
|mediaContentRatingApps|String|Configuración de clasificación de contenido multimedia para aplicaciones. Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove4`, `agesAbove9`, `agesAbove12` y `agesAbove17`.|
|messagesBlocked|Boolean|Indica si se va a impedir que el usuario utilice la aplicación Mensajes en el dispositivo supervisado.|
|notificationsBlockSettingsModification|Boolean|Indica si se va a permitir la modificación de la configuración de notificaciones (iOS 9.3 y versiones posteriores).|
|passcodeBlockFingerprintUnlock|Boolean|Indica si se va a impedir el desbloqueo por huella digital.|
|passcodeBlockFingerprintModification|Boolean|Bloquear la modificación de huellas digitales registradas de Touch ID en el modo supervisado.|
|passcodeBlockModification|Boolean|Indica si se va a permitir la modificación de los códigos de acceso en el dispositivo supervisado (iOS 9.0 y versiones posteriores).|
|passcodeBlockSimple|Boolean|Indica si se van a bloquear los códigos de acceso simples.|
|passcodeExpirationDays|Int32|Número de días antes de que expire el código de acceso. Valores válidos de 1 a 65 535.|
|passcodeMinimumLength|Int32|Longitud mínima del código de acceso. Valores válidos de 4 a 14.|
|passcodeMinutesOfInactivityBeforeLock|Int32|Minutos de inactividad antes de que sea necesario un código de acceso.|
|passcodeMinutesOfInactivityBeforeScreenTimeout|Int32|Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.|
|passcodeMinimumCharacterSetCount|Int32|Número de juegos de caracteres que debe contener un código de acceso. Valores válidos de 0 a 4.|
|passcodePreviousPasscodeBlockCount|Int32|Número de códigos de acceso anteriores que bloquear. Valores válidos de 1 a 24.|
|passcodeSignInFailureCountBeforeWipe|Int32|Número de errores de inicio de sesión permitidos antes de borrar los datos del dispositivo. Valores válidos de 4 a 11.|
|passcodeRequiredType|String|Tipo de código de acceso necesario. Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.|
|passcodeRequired|Boolean|Indica si se va a requerir un código de acceso.|
|podcastsBlocked|Boolean|Indica si se va a impedir que el usuario utilice Podcasts en el dispositivo supervisado (iOS 8.0 y versiones posteriores).|
|safariBlockAutofill|Boolean|Indica si se va a impedir que el usuario utilice la opción de autorrellenado en Safari.|
|safariBlockJavaScript|Boolean|Indica si se va a bloquear JavaScript en Safari.|
|safariBlockPopups|Boolean|Indica si se van a bloquear los elementos emergentes en Safari.|
|safariBlocked|Boolean|Indica si se va a impedir que el usuario utilice Safari.|
|safariCookieSettings|String|Configuración de cookies para Safari. Los valores posibles son: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited` y `allowAlways`.|
|safariManagedDomains|Colección String|Las direcciones URL que coinciden con los patrones mostrados aquí se considerarán administradas.|
|safariPasswordAutoFillDomains|Colección String|Los usuarios solo pueden guardar las contraseñas en Safari de las direcciones URL que coinciden con los patrones mostrados aquí. Se aplica a dispositivos en modo supervisado (iOS 9.3 o posterior).|
|safariRequireFraudWarning|Boolean|Indica si se va a requerir una advertencia de fraude en Safari.|
|screenCaptureBlocked|Boolean|Indica si se va a impedir que el usuario tome capturas de pantalla.|
|siriBlocked|Boolean|Indica si se va a impedir que el usuario utilice Siri.|
|siriBlockedWhenLocked|Boolean|Indica si se va a impedir que el usuario utilice Siri cuando está bloqueado.|
|siriBlockUserGeneratedContent|Boolean|Indica si se va a impedir que Siri haga consultas de contenido generado por el usuario cuando se utiliza en un dispositivo supervisado.|
|siriRequireProfanityFilter|Boolean|Indica si se va a impedir que Siri dicte o hable con lenguaje irreverente en un dispositivo supervisado.|
|spotlightBlockInternetResults|Boolean|Indica si se va a impedir que la búsqueda Spotlight devuelva resultados de Internet en un dispositivo supervisado.|
|voiceDialingBlocked|Boolean|Indica si se va a bloquear la marcación por voz.|
|wallpaperBlockModification|Boolean|Indica si se va permitir la modificación del fondo de pantalla en un dispositivo supervisado (iOS 9.0 y versiones posteriores).|
|wiFiConnectOnlyToConfiguredNetworks|Boolean|Indica si se va a forzar al dispositivo para que use solo redes Wi-Fi de perfiles de configuración cuando el dispositivo está en modo supervisado.|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosGeneralDeviceConfiguration](../resources/intune_deviceconfig_iosgeneraldeviceconfiguration.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 7773

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountBlockModification": true,
  "activationLockAllowWhenSupervised": true,
  "airDropBlocked": true,
  "airDropForceUnmanagedDropTarget": true,
  "airPlayForcePairingPasswordForOutgoingRequests": true,
  "appleWatchBlockPairing": true,
  "appleWatchForceWristDetection": true,
  "appleNewsBlocked": true,
  "appsSingleAppModeList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityListType": "appsInListCompliant",
  "appStoreBlockAutomaticDownloads": true,
  "appStoreBlocked": true,
  "appStoreBlockInAppPurchases": true,
  "appStoreBlockUIAppInstallation": true,
  "appStoreRequirePassword": true,
  "bluetoothBlockModification": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockGlobalBackgroundFetchWhileRoaming": true,
  "cellularBlockPerAppDataModification": true,
  "cellularBlockPersonalHotspot": true,
  "cellularBlockVoiceRoaming": true,
  "certificatesBlockUntrustedTlsCertificates": true,
  "classroomAppBlockRemoteScreenObservation": true,
  "classroomAppForceUnpromptedScreenObservation": true,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "configurationProfileBlockChanges": true,
  "definitionLookupBlocked": true,
  "deviceBlockEnableRestrictions": true,
  "deviceBlockEraseContentAndSettings": true,
  "deviceBlockNameModification": true,
  "diagnosticDataBlockSubmission": true,
  "diagnosticDataBlockSubmissionModification": true,
  "documentsBlockManagedDocumentsInUnmanagedApps": true,
  "documentsBlockUnmanagedDocumentsInManagedApps": true,
  "emailInDomainSuffixes": [
    "Email In Domain Suffixes value"
  ],
  "enterpriseAppBlockTrust": true,
  "enterpriseAppBlockTrustModification": true,
  "faceTimeBlocked": true,
  "findMyFriendsBlocked": true,
  "gamingBlockGameCenterFriends": true,
  "gamingBlockMultiplayer": true,
  "gameCenterBlocked": true,
  "hostPairingBlocked": true,
  "iBooksStoreBlocked": true,
  "iBooksStoreBlockErotica": true,
  "iCloudBlockActivityContinuation": true,
  "iCloudBlockBackup": true,
  "iCloudBlockDocumentSync": true,
  "iCloudBlockManagedAppsSync": true,
  "iCloudBlockPhotoLibrary": true,
  "iCloudBlockPhotoStreamSync": true,
  "iCloudBlockSharedPhotoStream": true,
  "iCloudRequireEncryptedBackup": true,
  "iTunesBlockExplicitContent": true,
  "iTunesBlockMusicService": true,
  "iTunesBlockRadio": true,
  "keyboardBlockAutoCorrect": true,
  "keyboardBlockDictation": true,
  "keyboardBlockPredictive": true,
  "keyboardBlockShortcuts": true,
  "keyboardBlockSpellCheck": true,
  "kioskModeAllowAssistiveSpeak": true,
  "kioskModeAllowAssistiveTouchSettings": true,
  "kioskModeAllowAutoLock": true,
  "kioskModeAllowColorInversionSettings": true,
  "kioskModeAllowRingerSwitch": true,
  "kioskModeAllowScreenRotation": true,
  "kioskModeAllowSleepButton": true,
  "kioskModeAllowTouchscreen": true,
  "kioskModeAllowVoiceOverSettings": true,
  "kioskModeAllowVolumeButtons": true,
  "kioskModeAllowZoomSettings": true,
  "kioskModeAppStoreUrl": "https://example.com/kioskModeAppStoreUrl/",
  "kioskModeRequireAssistiveTouch": true,
  "kioskModeRequireColorInversion": true,
  "kioskModeRequireMonoAudio": true,
  "kioskModeRequireVoiceOver": true,
  "kioskModeRequireZoom": true,
  "kioskModeManagedAppId": "Kiosk Mode Managed App Id value",
  "lockScreenBlockControlCenter": true,
  "lockScreenBlockNotificationView": true,
  "lockScreenBlockPassbook": true,
  "lockScreenBlockTodayView": true,
  "mediaContentRatingAustralia": {
    "@odata.type": "microsoft.graph.mediaContentRatingAustralia",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingCanada": {
    "@odata.type": "microsoft.graph.mediaContentRatingCanada",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingFrance": {
    "@odata.type": "microsoft.graph.mediaContentRatingFrance",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingGermany": {
    "@odata.type": "microsoft.graph.mediaContentRatingGermany",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingIreland": {
    "@odata.type": "microsoft.graph.mediaContentRatingIreland",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingJapan": {
    "@odata.type": "microsoft.graph.mediaContentRatingJapan",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingNewZealand": {
    "@odata.type": "microsoft.graph.mediaContentRatingNewZealand",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedKingdom": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedStates": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "networkUsageRules": [
    {
      "@odata.type": "microsoft.graph.iosNetworkUsageRule",
      "managedApps": [
        {
          "@odata.type": "microsoft.graph.appListItem",
          "name": "Name value",
          "publisher": "Publisher value",
          "appStoreUrl": "https://example.com/appStoreUrl/",
          "appId": "App Id value"
        }
      ],
      "cellularDataBlockWhenRoaming": true,
      "cellularDataBlocked": true
    }
  ],
  "mediaContentRatingApps": "allBlocked",
  "messagesBlocked": true,
  "notificationsBlockSettingsModification": true,
  "passcodeBlockFingerprintUnlock": true,
  "passcodeBlockFingerprintModification": true,
  "passcodeBlockModification": true,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 6,
  "passcodeMinimumLength": 5,
  "passcodeMinutesOfInactivityBeforeLock": 5,
  "passcodeMinutesOfInactivityBeforeScreenTimeout": 14,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeSignInFailureCountBeforeWipe": 4,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "podcastsBlocked": true,
  "safariBlockAutofill": true,
  "safariBlockJavaScript": true,
  "safariBlockPopups": true,
  "safariBlocked": true,
  "safariCookieSettings": "blockAlways",
  "safariManagedDomains": [
    "Safari Managed Domains value"
  ],
  "safariPasswordAutoFillDomains": [
    "Safari Password Auto Fill Domains value"
  ],
  "safariRequireFraudWarning": true,
  "screenCaptureBlocked": true,
  "siriBlocked": true,
  "siriBlockedWhenLocked": true,
  "siriBlockUserGeneratedContent": true,
  "siriRequireProfanityFilter": true,
  "spotlightBlockInternetResults": true,
  "voiceDialingBlocked": true,
  "wallpaperBlockModification": true,
  "wiFiConnectOnlyToConfiguredNetworks": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 7949

{
  "@odata.type": "#microsoft.graph.iosGeneralDeviceConfiguration",
  "id": "ebba5202-5202-ebba-0252-baeb0252baeb",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountBlockModification": true,
  "activationLockAllowWhenSupervised": true,
  "airDropBlocked": true,
  "airDropForceUnmanagedDropTarget": true,
  "airPlayForcePairingPasswordForOutgoingRequests": true,
  "appleWatchBlockPairing": true,
  "appleWatchForceWristDetection": true,
  "appleNewsBlocked": true,
  "appsSingleAppModeList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityListType": "appsInListCompliant",
  "appStoreBlockAutomaticDownloads": true,
  "appStoreBlocked": true,
  "appStoreBlockInAppPurchases": true,
  "appStoreBlockUIAppInstallation": true,
  "appStoreRequirePassword": true,
  "bluetoothBlockModification": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockGlobalBackgroundFetchWhileRoaming": true,
  "cellularBlockPerAppDataModification": true,
  "cellularBlockPersonalHotspot": true,
  "cellularBlockVoiceRoaming": true,
  "certificatesBlockUntrustedTlsCertificates": true,
  "classroomAppBlockRemoteScreenObservation": true,
  "classroomAppForceUnpromptedScreenObservation": true,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "configurationProfileBlockChanges": true,
  "definitionLookupBlocked": true,
  "deviceBlockEnableRestrictions": true,
  "deviceBlockEraseContentAndSettings": true,
  "deviceBlockNameModification": true,
  "diagnosticDataBlockSubmission": true,
  "diagnosticDataBlockSubmissionModification": true,
  "documentsBlockManagedDocumentsInUnmanagedApps": true,
  "documentsBlockUnmanagedDocumentsInManagedApps": true,
  "emailInDomainSuffixes": [
    "Email In Domain Suffixes value"
  ],
  "enterpriseAppBlockTrust": true,
  "enterpriseAppBlockTrustModification": true,
  "faceTimeBlocked": true,
  "findMyFriendsBlocked": true,
  "gamingBlockGameCenterFriends": true,
  "gamingBlockMultiplayer": true,
  "gameCenterBlocked": true,
  "hostPairingBlocked": true,
  "iBooksStoreBlocked": true,
  "iBooksStoreBlockErotica": true,
  "iCloudBlockActivityContinuation": true,
  "iCloudBlockBackup": true,
  "iCloudBlockDocumentSync": true,
  "iCloudBlockManagedAppsSync": true,
  "iCloudBlockPhotoLibrary": true,
  "iCloudBlockPhotoStreamSync": true,
  "iCloudBlockSharedPhotoStream": true,
  "iCloudRequireEncryptedBackup": true,
  "iTunesBlockExplicitContent": true,
  "iTunesBlockMusicService": true,
  "iTunesBlockRadio": true,
  "keyboardBlockAutoCorrect": true,
  "keyboardBlockDictation": true,
  "keyboardBlockPredictive": true,
  "keyboardBlockShortcuts": true,
  "keyboardBlockSpellCheck": true,
  "kioskModeAllowAssistiveSpeak": true,
  "kioskModeAllowAssistiveTouchSettings": true,
  "kioskModeAllowAutoLock": true,
  "kioskModeAllowColorInversionSettings": true,
  "kioskModeAllowRingerSwitch": true,
  "kioskModeAllowScreenRotation": true,
  "kioskModeAllowSleepButton": true,
  "kioskModeAllowTouchscreen": true,
  "kioskModeAllowVoiceOverSettings": true,
  "kioskModeAllowVolumeButtons": true,
  "kioskModeAllowZoomSettings": true,
  "kioskModeAppStoreUrl": "https://example.com/kioskModeAppStoreUrl/",
  "kioskModeRequireAssistiveTouch": true,
  "kioskModeRequireColorInversion": true,
  "kioskModeRequireMonoAudio": true,
  "kioskModeRequireVoiceOver": true,
  "kioskModeRequireZoom": true,
  "kioskModeManagedAppId": "Kiosk Mode Managed App Id value",
  "lockScreenBlockControlCenter": true,
  "lockScreenBlockNotificationView": true,
  "lockScreenBlockPassbook": true,
  "lockScreenBlockTodayView": true,
  "mediaContentRatingAustralia": {
    "@odata.type": "microsoft.graph.mediaContentRatingAustralia",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingCanada": {
    "@odata.type": "microsoft.graph.mediaContentRatingCanada",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingFrance": {
    "@odata.type": "microsoft.graph.mediaContentRatingFrance",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingGermany": {
    "@odata.type": "microsoft.graph.mediaContentRatingGermany",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingIreland": {
    "@odata.type": "microsoft.graph.mediaContentRatingIreland",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingJapan": {
    "@odata.type": "microsoft.graph.mediaContentRatingJapan",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingNewZealand": {
    "@odata.type": "microsoft.graph.mediaContentRatingNewZealand",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedKingdom": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedStates": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "networkUsageRules": [
    {
      "@odata.type": "microsoft.graph.iosNetworkUsageRule",
      "managedApps": [
        {
          "@odata.type": "microsoft.graph.appListItem",
          "name": "Name value",
          "publisher": "Publisher value",
          "appStoreUrl": "https://example.com/appStoreUrl/",
          "appId": "App Id value"
        }
      ],
      "cellularDataBlockWhenRoaming": true,
      "cellularDataBlocked": true
    }
  ],
  "mediaContentRatingApps": "allBlocked",
  "messagesBlocked": true,
  "notificationsBlockSettingsModification": true,
  "passcodeBlockFingerprintUnlock": true,
  "passcodeBlockFingerprintModification": true,
  "passcodeBlockModification": true,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 6,
  "passcodeMinimumLength": 5,
  "passcodeMinutesOfInactivityBeforeLock": 5,
  "passcodeMinutesOfInactivityBeforeScreenTimeout": 14,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeSignInFailureCountBeforeWipe": 4,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "podcastsBlocked": true,
  "safariBlockAutofill": true,
  "safariBlockJavaScript": true,
  "safariBlockPopups": true,
  "safariBlocked": true,
  "safariCookieSettings": "blockAlways",
  "safariManagedDomains": [
    "Safari Managed Domains value"
  ],
  "safariPasswordAutoFillDomains": [
    "Safari Password Auto Fill Domains value"
  ],
  "safariRequireFraudWarning": true,
  "screenCaptureBlocked": true,
  "siriBlocked": true,
  "siriBlockedWhenLocked": true,
  "siriBlockUserGeneratedContent": true,
  "siriRequireProfanityFilter": true,
  "spotlightBlockInternetResults": true,
  "voiceDialingBlocked": true,
  "wallpaperBlockModification": true,
  "wiFiConnectOnlyToConfiguredNetworks": true
}
```



