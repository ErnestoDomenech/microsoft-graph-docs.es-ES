# <a name="get-windows10endpointprotectionconfiguration"></a><span data-ttu-id="be1f7-101">Obtener windows10EndpointProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="be1f7-101">Get windows10EndpointProtectionConfiguration</span></span>

> <span data-ttu-id="be1f7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="be1f7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="be1f7-103">Lea las propiedades y las relaciones del objeto [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="be1f7-103">Read properties and relationships of [plannerBucketTaskBoardTaskFormat](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="be1f7-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="be1f7-104">Prerequisites</span></span>
<span data-ttu-id="be1f7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="be1f7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="be1f7-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="be1f7-107">Permission type</span></span>|<span data-ttu-id="be1f7-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="be1f7-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="be1f7-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="be1f7-109">Delegated (work or school account)</span></span>|<span data-ttu-id="be1f7-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="be1f7-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="be1f7-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="be1f7-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="be1f7-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="be1f7-112">Not supported.</span></span>|
|<span data-ttu-id="be1f7-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="be1f7-113">Application</span></span>|<span data-ttu-id="be1f7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="be1f7-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="be1f7-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="be1f7-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="be1f7-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="be1f7-116">Optional query parameters</span></span>
<span data-ttu-id="be1f7-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be1f7-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="be1f7-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="be1f7-118">Request headers</span></span>
|<span data-ttu-id="be1f7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be1f7-119">Header</span></span>|<span data-ttu-id="be1f7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="be1f7-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="be1f7-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="be1f7-121">Authorization</span></span>|<span data-ttu-id="be1f7-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="be1f7-122">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="be1f7-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="be1f7-123">Accept</span></span>|<span data-ttu-id="be1f7-124">application/json</span><span class="sxs-lookup"><span data-stu-id="be1f7-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="be1f7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="be1f7-125">Request body</span></span>
<span data-ttu-id="be1f7-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="be1f7-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="be1f7-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be1f7-127">Response</span></span>
<span data-ttu-id="be1f7-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be1f7-128">If successful, this method returns a `200 OK` response code and a [section](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="be1f7-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be1f7-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="be1f7-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="be1f7-130">Request</span></span>
<span data-ttu-id="be1f7-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="be1f7-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="be1f7-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be1f7-132">Response</span></span>
<span data-ttu-id="be1f7-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="be1f7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4628

{
  "value": {
    "@odata.type": "#microsoft.graph.windows10EndpointProtectionConfiguration",
    "id": "09709403-9403-0970-0394-700903947009",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "firewallBlockStatefulFTP": true,
    "firewallIdleTimeoutForSecurityAssociationInSeconds": 2,
    "firewallPreSharedKeyEncodingMethod": "none",
    "firewallIPSecExemptionsAllowNeighborDiscovery": true,
    "firewallIPSecExemptionsAllowICMP": true,
    "firewallIPSecExemptionsAllowRouterDiscovery": true,
    "firewallIPSecExemptionsAllowDHCP": true,
    "firewallCertificateRevocationListCheckMethod": "none",
    "firewallMergeKeyingModuleSettings": true,
    "firewallPacketQueueingMethod": "disabled",
    "firewallProfileDomain": {
      "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
      "firewallEnabled": "blocked",
      "stealthModeBlocked": true,
      "incomingTrafficBlocked": true,
      "unicastResponsesToMulticastBroadcastsBlocked": true,
      "inboundNotificationsBlocked": true,
      "authorizedApplicationRulesFromGroupPolicyMerged": true,
      "globalPortRulesFromGroupPolicyMerged": true,
      "connectionSecurityRulesFromGroupPolicyMerged": true,
      "outboundConnectionsBlocked": true,
      "inboundConnectionsBlocked": true,
      "securedPacketExemptionAllowed": true,
      "policyRulesFromGroupPolicyMerged": true
    },
    "firewallProfilePublic": {
      "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
      "firewallEnabled": "blocked",
      "stealthModeBlocked": true,
      "incomingTrafficBlocked": true,
      "unicastResponsesToMulticastBroadcastsBlocked": true,
      "inboundNotificationsBlocked": true,
      "authorizedApplicationRulesFromGroupPolicyMerged": true,
      "globalPortRulesFromGroupPolicyMerged": true,
      "connectionSecurityRulesFromGroupPolicyMerged": true,
      "outboundConnectionsBlocked": true,
      "inboundConnectionsBlocked": true,
      "securedPacketExemptionAllowed": true,
      "policyRulesFromGroupPolicyMerged": true
    },
    "firewallProfilePrivate": {
      "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
      "firewallEnabled": "blocked",
      "stealthModeBlocked": true,
      "incomingTrafficBlocked": true,
      "unicastResponsesToMulticastBroadcastsBlocked": true,
      "inboundNotificationsBlocked": true,
      "authorizedApplicationRulesFromGroupPolicyMerged": true,
      "globalPortRulesFromGroupPolicyMerged": true,
      "connectionSecurityRulesFromGroupPolicyMerged": true,
      "outboundConnectionsBlocked": true,
      "inboundConnectionsBlocked": true,
      "securedPacketExemptionAllowed": true,
      "policyRulesFromGroupPolicyMerged": true
    },
    "defenderAttackSurfaceReductionExcludedPaths": [
      "Defender Attack Surface Reduction Excluded Paths value"
    ],
    "defenderGuardedFoldersAllowedAppPaths": [
      "Defender Guarded Folders Allowed App Paths value"
    ],
    "defenderAdditionalGuardedFolders": [
      "Defender Additional Guarded Folders value"
    ],
    "defenderExploitProtectionXml": "ZGVmZW5kZXJFeHBsb2l0UHJvdGVjdGlvblhtbA==",
    "defenderExploitProtectionXmlFileName": "Defender Exploit Protection Xml File Name value",
    "defenderSecurityCenterBlockExploitProtectionOverride": true,
    "appLockerApplicationControl": "enforceComponentsAndStoreApps",
    "smartScreenEnableInShell": true,
    "smartScreenBlockOverrideForFiles": true,
    "applicationGuardEnabled": true,
    "applicationGuardBlockFileTransfer": "blockImageAndTextFile",
    "applicationGuardBlockNonEnterpriseContent": true,
    "applicationGuardAllowPersistence": true,
    "applicationGuardForceAuditing": true,
    "applicationGuardBlockClipboardSharing": "blockBoth",
    "applicationGuardAllowPrintToPDF": true,
    "applicationGuardAllowPrintToXPS": true,
    "applicationGuardAllowPrintToLocalPrinters": true,
    "applicationGuardAllowPrintToNetworkPrinters": true,
    "bitLockerDisableWarningForOtherDiskEncryption": true,
    "bitLockerEnableStorageCardEncryptionOnMobile": true,
    "bitLockerEncryptDevice": true,
    "bitLockerRemovableDrivePolicy": {
      "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy",
      "encryptionMethod": "aesCbc256",
      "requireEncryptionForWriteAccess": true,
      "blockCrossOrganizationWriteAccess": true
    }
  }
}
```


