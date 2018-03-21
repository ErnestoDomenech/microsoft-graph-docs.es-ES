# <a name="get-auditevent"></a><span data-ttu-id="822b0-101">Obtener auditEvent</span><span class="sxs-lookup"><span data-stu-id="822b0-101">Get auditEvent</span></span>

> <span data-ttu-id="822b0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="822b0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="822b0-103">Lea las propiedades y las relaciones del objeto [auditEvent](../resources/intune_auditing_auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="822b0-103">Read properties and relationships of [plannerTaskDetails](../resources/intune_auditing_auditevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="822b0-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="822b0-104">Prerequisites</span></span>
<span data-ttu-id="822b0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="822b0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="822b0-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="822b0-107">Permission type</span></span>|<span data-ttu-id="822b0-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="822b0-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="822b0-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="822b0-109">Delegated (work or school account)</span></span>|<span data-ttu-id="822b0-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="822b0-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="822b0-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="822b0-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="822b0-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="822b0-112">Not supported.</span></span>|
|<span data-ttu-id="822b0-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="822b0-113">Application</span></span>|<span data-ttu-id="822b0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="822b0-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="822b0-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="822b0-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/auditEvents/{auditEventId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="822b0-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="822b0-116">Optional query parameters</span></span>
<span data-ttu-id="822b0-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="822b0-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="822b0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="822b0-118">Request headers</span></span>
|<span data-ttu-id="822b0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="822b0-119">Header</span></span>|<span data-ttu-id="822b0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="822b0-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="822b0-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="822b0-121">Authorization</span></span>|<span data-ttu-id="822b0-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="822b0-122">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="822b0-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="822b0-123">Accept</span></span>|<span data-ttu-id="822b0-124">application/json</span><span class="sxs-lookup"><span data-stu-id="822b0-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="822b0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="822b0-125">Request body</span></span>
<span data-ttu-id="822b0-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="822b0-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="822b0-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="822b0-127">Response</span></span>
<span data-ttu-id="822b0-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de [auditEvent](../resources/intune_auditing_auditevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="822b0-128">If successful, this method returns a `200 OK` response code and a [DriveItemVersion](../resources/intune_auditing_auditevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="822b0-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="822b0-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="822b0-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="822b0-130">Request</span></span>
<span data-ttu-id="822b0-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="822b0-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/auditEvents/{auditEventId}
```

### <a name="response"></a><span data-ttu-id="822b0-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="822b0-132">Response</span></span>
<span data-ttu-id="822b0-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="822b0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1598

{
  "value": {
    "@odata.type": "#microsoft.graph.auditEvent",
    "id": "59653ce8-3ce8-5965-e83c-6559e83c6559",
    "displayName": "Display Name value",
    "componentName": "Component Name value",
    "actor": {
      "@odata.type": "microsoft.graph.auditActor",
      "type": "Type value",
      "permissions": [
        "Permissions value"
      ],
      "userPermissions": [
        "User Permissions value"
      ],
      "applicationId": "Application Id value",
      "applicationDisplayName": "Application Display Name value",
      "userPrincipalName": "User Principal Name value",
      "servicePrincipalName": "Service Principal Name value",
      "ipAddress": "Ip Address value",
      "userId": "User Id value"
    },
    "activity": "Activity value",
    "activityDateTime": "2016-12-31T23:59:51.6363086-08:00",
    "activityType": "Activity Type value",
    "activityOperationType": "Activity Operation Type value",
    "activityResult": "Activity Result value",
    "correlationId": "<Unknown Primitive Type Edm.Guid>",
    "resources": [
      {
        "@odata.type": "microsoft.graph.auditResource",
        "displayName": "Display Name value",
        "modifiedProperties": [
          {
            "@odata.type": "microsoft.graph.auditProperty",
            "displayName": "Display Name value",
            "oldValue": "Old Value value",
            "newValue": "New Value value"
          }
        ],
        "type": "Type value",
        "resourceId": "Resource Id value"
      }
    ],
    "category": "Category value"
  }
}
```


