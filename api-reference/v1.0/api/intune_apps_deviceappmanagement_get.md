# <a name="get-deviceappmanagement"></a><span data-ttu-id="3da36-101">Obtener deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="3da36-101">Get deviceAppManagement</span></span>

> <span data-ttu-id="3da36-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3da36-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3da36-103">Lea las propiedades y las relaciones del objeto [deviceAppManagement](../resources/intune_apps_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="3da36-103">Read properties and relationships of [plannerTaskDetails](../resources/intune_apps_deviceappmanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3da36-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3da36-104">Prerequisites</span></span>
<span data-ttu-id="3da36-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3da36-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3da36-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3da36-107">Permission type</span></span>|<span data-ttu-id="3da36-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3da36-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3da36-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3da36-109">Delegated (work or school account)</span></span>|<span data-ttu-id="3da36-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="3da36-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="3da36-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3da36-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3da36-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3da36-112">Not supported.</span></span>|
|<span data-ttu-id="3da36-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3da36-113">Application</span></span>|<span data-ttu-id="3da36-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3da36-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3da36-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3da36-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement
```

## <a name="optional-query-parameters"></a><span data-ttu-id="3da36-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3da36-116">Optional query parameters</span></span>
<span data-ttu-id="3da36-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3da36-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3da36-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3da36-118">Request headers</span></span>
|<span data-ttu-id="3da36-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3da36-119">Header</span></span>|<span data-ttu-id="3da36-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3da36-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3da36-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="3da36-121">Authorization</span></span>|<span data-ttu-id="3da36-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3da36-122">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="3da36-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3da36-123">Accept</span></span>|<span data-ttu-id="3da36-124">application/json</span><span class="sxs-lookup"><span data-stu-id="3da36-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3da36-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3da36-125">Request body</span></span>
<span data-ttu-id="3da36-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3da36-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3da36-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3da36-127">Response</span></span>
<span data-ttu-id="3da36-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAppManagement](../resources/intune_apps_deviceappmanagement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3da36-128">If successful, this method returns a `200 OK` response code and a [ListItemVersion](../resources/intune_apps_deviceappmanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3da36-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3da36-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="3da36-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3da36-130">Request</span></span>
<span data-ttu-id="3da36-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3da36-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement
```

### <a name="response"></a><span data-ttu-id="3da36-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3da36-132">Response</span></span>
<span data-ttu-id="3da36-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3da36-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 133

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceAppManagement",
    "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb"
  }
}
```


