# <a name="create-androidforworkenrollmentprofile"></a><span data-ttu-id="5ba5a-101">Crear androidForWorkEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="5ba5a-101">Create androidForWorkEnrollmentProfile</span></span>

> <span data-ttu-id="5ba5a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5ba5a-103">Cree un objeto [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="5ba5a-103">Create a new [plannerBucket](../resources/intune_androidforwork_androidforworkenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5ba5a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5ba5a-104">Prerequisites</span></span>
<span data-ttu-id="5ba5a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5ba5a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5ba5a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5ba5a-107">Permission type</span></span>|<span data-ttu-id="5ba5a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5ba5a-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5ba5a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5ba5a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5ba5a-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5ba5a-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5ba5a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5ba5a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5ba5a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-112">Not supported.</span></span>|
|<span data-ttu-id="5ba5a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5ba5a-113">Application</span></span>|<span data-ttu-id="5ba5a-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5ba5a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5ba5a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/androidForWorkEnrollmentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="5ba5a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5ba5a-116">Request headers</span></span>
|<span data-ttu-id="5ba5a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ba5a-117">Header</span></span>|<span data-ttu-id="5ba5a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5ba5a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5ba5a-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="5ba5a-119">Authorization</span></span>|<span data-ttu-id="5ba5a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="5ba5a-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5ba5a-121">Accept</span></span>|<span data-ttu-id="5ba5a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5ba5a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5ba5a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5ba5a-123">Request body</span></span>
<span data-ttu-id="5ba5a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidForWorkEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="5ba5a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidForWorkEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="5ba5a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5ba5a-126">Property</span></span>|<span data-ttu-id="5ba5a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ba5a-127">Type</span></span>|<span data-ttu-id="5ba5a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ba5a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5ba5a-129">accountId</span><span class="sxs-lookup"><span data-stu-id="5ba5a-129">accountId</span></span>|<span data-ttu-id="5ba5a-130">String</span><span class="sxs-lookup"><span data-stu-id="5ba5a-130">String</span></span>|<span data-ttu-id="5ba5a-131">GUID del espacio empresarial al que pertenece el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-131">Tenant GUID the enrollment profile belongs to.</span></span>|
|<span data-ttu-id="5ba5a-132">id</span><span class="sxs-lookup"><span data-stu-id="5ba5a-132">id</span></span>|<span data-ttu-id="5ba5a-133">String</span><span class="sxs-lookup"><span data-stu-id="5ba5a-133">String</span></span>|<span data-ttu-id="5ba5a-134">GUID único del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-134">Unique GUID for the enrollment profile.</span></span>|
|<span data-ttu-id="5ba5a-135">name</span><span class="sxs-lookup"><span data-stu-id="5ba5a-135">name</span></span>|<span data-ttu-id="5ba5a-136">String</span><span class="sxs-lookup"><span data-stu-id="5ba5a-136">String</span></span>|<span data-ttu-id="5ba5a-137">(En desuso) Nombre para mostrar del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-137">(Deprecated) Display name for the enrollment profile.</span></span>|
|<span data-ttu-id="5ba5a-138">displayName</span><span class="sxs-lookup"><span data-stu-id="5ba5a-138">displayName</span></span>|<span data-ttu-id="5ba5a-139">String</span><span class="sxs-lookup"><span data-stu-id="5ba5a-139">String</span></span>|<span data-ttu-id="5ba5a-140">Nombre para mostrar del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-140">Display name for the enrollment profile.</span></span>|
|<span data-ttu-id="5ba5a-141">description</span><span class="sxs-lookup"><span data-stu-id="5ba5a-141">description</span></span>|<span data-ttu-id="5ba5a-142">String</span><span class="sxs-lookup"><span data-stu-id="5ba5a-142">String</span></span>|<span data-ttu-id="5ba5a-143">Descripción del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-143">Description for the enrollment profile.</span></span>|
|<span data-ttu-id="5ba5a-144">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5ba5a-144">createdDateTime</span></span>|<span data-ttu-id="5ba5a-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ba5a-145">DateTimeOffset</span></span>|<span data-ttu-id="5ba5a-146">Fecha y hora en que se creó el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-146">Date time the enrollment profile was created.</span></span>|
|<span data-ttu-id="5ba5a-147">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5ba5a-147">modifiedDateTime</span></span>|<span data-ttu-id="5ba5a-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ba5a-148">DateTimeOffset</span></span>|<span data-ttu-id="5ba5a-149">(En desuso) Fecha y hora en que se modificó el perfil de inscripción por última vez.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-149">(Deprecated) Date time the enrollment profile was last modified.</span></span>|
|<span data-ttu-id="5ba5a-150">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5ba5a-150">lastModifiedDateTime</span></span>|<span data-ttu-id="5ba5a-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ba5a-151">DateTimeOffset</span></span>|<span data-ttu-id="5ba5a-152">Fecha y hora en que se modificó el perfil de inscripción por última vez.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-152">Date time the enrollment profile was last modified.</span></span>|
|<span data-ttu-id="5ba5a-153">tokenValue</span><span class="sxs-lookup"><span data-stu-id="5ba5a-153">tokenValue</span></span>|<span data-ttu-id="5ba5a-154">String</span><span class="sxs-lookup"><span data-stu-id="5ba5a-154">String</span></span>|<span data-ttu-id="5ba5a-155">Valor del token creado más recientemente para este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-155">Value of the most recently created token for this enrollment profile.</span></span>|
|<span data-ttu-id="5ba5a-156">tokenExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="5ba5a-156">tokenExpirationDateTime</span></span>|<span data-ttu-id="5ba5a-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ba5a-157">DateTimeOffset</span></span>|<span data-ttu-id="5ba5a-158">Fecha y hora en que expirará el token creado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-158">Date time the most recently created token will expire.</span></span>|
|<span data-ttu-id="5ba5a-159">totalEnrollmentCount</span><span class="sxs-lookup"><span data-stu-id="5ba5a-159">totalEnrollmentCount</span></span>|<span data-ttu-id="5ba5a-160">Int32</span><span class="sxs-lookup"><span data-stu-id="5ba5a-160">Int32</span></span>|<span data-ttu-id="5ba5a-161">(En desuso) Número total de dispositivos Android que se han inscrito con este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-161">(Deprecated) Total number of Android devices that have enrolled using this enrollment profile.</span></span>|
|<span data-ttu-id="5ba5a-162">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="5ba5a-162">enrolledDeviceCount</span></span>|<span data-ttu-id="5ba5a-163">Int32</span><span class="sxs-lookup"><span data-stu-id="5ba5a-163">Int32</span></span>|<span data-ttu-id="5ba5a-164">Número total de dispositivos Android que se han inscrito con este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-164">Total number of Android devices that have enrolled using this enrollment profile.</span></span>|
|<span data-ttu-id="5ba5a-165">qrCode</span><span class="sxs-lookup"><span data-stu-id="5ba5a-165">qrCode</span></span>|<span data-ttu-id="5ba5a-166">String</span><span class="sxs-lookup"><span data-stu-id="5ba5a-166">String</span></span>|<span data-ttu-id="5ba5a-167">(En desuso) Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-167">(Deprecated) String used to generate a QR code for the token.</span></span>|
|<span data-ttu-id="5ba5a-168">qrCodeContent</span><span class="sxs-lookup"><span data-stu-id="5ba5a-168">qrCodeContent</span></span>|<span data-ttu-id="5ba5a-169">String</span><span class="sxs-lookup"><span data-stu-id="5ba5a-169">String</span></span>|<span data-ttu-id="5ba5a-170">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-170">String used to generate a QR code for the token.</span></span>|
|<span data-ttu-id="5ba5a-171">qrCodeImage</span><span class="sxs-lookup"><span data-stu-id="5ba5a-171">qrCodeImage</span></span>|[<span data-ttu-id="5ba5a-172">mimeContent</span><span class="sxs-lookup"><span data-stu-id="5ba5a-172">mimeContent</span></span>](../resources/intune_androidforwork_mimecontent.md)|<span data-ttu-id="5ba5a-173">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-173">String used to generate a QR code for the token.</span></span>|



## <a name="response"></a><span data-ttu-id="5ba5a-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ba5a-174">Response</span></span>
<span data-ttu-id="5ba5a-175">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-175">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_androidforwork_androidforworkenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5ba5a-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5ba5a-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="5ba5a-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5ba5a-177">Request</span></span>
<span data-ttu-id="5ba5a-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-178">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/androidForWorkEnrollmentProfiles
Content-type: application/json
Content-length: 645

{
  "@odata.type": "#microsoft.graph.androidForWorkEnrollmentProfile",
  "accountId": "Account Id value",
  "name": "Name value",
  "displayName": "Display Name value",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "tokenValue": "Token Value value",
  "tokenExpirationDateTime": "2016-12-31T23:59:54.0590989-08:00",
  "totalEnrollmentCount": 4,
  "enrolledDeviceCount": 3,
  "qrCode": "Qr Code value",
  "qrCodeContent": "Qr Code Content value",
  "qrCodeImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  }
}
```

### <a name="response"></a><span data-ttu-id="5ba5a-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ba5a-179">Response</span></span>
<span data-ttu-id="5ba5a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5ba5a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 813

{
  "@odata.type": "#microsoft.graph.androidForWorkEnrollmentProfile",
  "accountId": "Account Id value",
  "id": "e6742553-2553-e674-5325-74e6532574e6",
  "name": "Name value",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "tokenValue": "Token Value value",
  "tokenExpirationDateTime": "2016-12-31T23:59:54.0590989-08:00",
  "totalEnrollmentCount": 4,
  "enrolledDeviceCount": 3,
  "qrCode": "Qr Code value",
  "qrCodeContent": "Qr Code Content value",
  "qrCodeImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  }
}
```


