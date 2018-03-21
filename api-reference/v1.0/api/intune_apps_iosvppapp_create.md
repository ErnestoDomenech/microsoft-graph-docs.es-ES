# <a name="create-iosvppapp"></a><span data-ttu-id="c48fe-101">Crear iosVppApp</span><span class="sxs-lookup"><span data-stu-id="c48fe-101">Create iosVppApp</span></span>

> <span data-ttu-id="c48fe-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c48fe-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c48fe-103">Cree un objeto [iosVppApp](../resources/intune_apps_iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="c48fe-103">Create a new [plannerBucket](../resources/intune_apps_iosvppapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c48fe-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c48fe-104">Prerequisites</span></span>
<span data-ttu-id="c48fe-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c48fe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c48fe-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c48fe-107">Permission type</span></span>|<span data-ttu-id="c48fe-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c48fe-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c48fe-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c48fe-109">Delegated (work or school account)</span></span>|<span data-ttu-id="c48fe-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c48fe-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="c48fe-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c48fe-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c48fe-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c48fe-112">Not supported.</span></span>|
|<span data-ttu-id="c48fe-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c48fe-113">Application</span></span>|<span data-ttu-id="c48fe-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="c48fe-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c48fe-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c48fe-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="c48fe-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c48fe-116">Request headers</span></span>
|<span data-ttu-id="c48fe-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c48fe-117">Header</span></span>|<span data-ttu-id="c48fe-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c48fe-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c48fe-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="c48fe-119">Authorization</span></span>|<span data-ttu-id="c48fe-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c48fe-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="c48fe-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c48fe-121">Accept</span></span>|<span data-ttu-id="c48fe-122">application/json</span><span class="sxs-lookup"><span data-stu-id="c48fe-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c48fe-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c48fe-123">Request body</span></span>
<span data-ttu-id="c48fe-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosVppApp.</span><span class="sxs-lookup"><span data-stu-id="c48fe-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="c48fe-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosVppApp.</span><span class="sxs-lookup"><span data-stu-id="c48fe-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="c48fe-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c48fe-126">Property</span></span>|<span data-ttu-id="c48fe-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="c48fe-127">Type</span></span>|<span data-ttu-id="c48fe-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c48fe-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c48fe-129">id</span><span class="sxs-lookup"><span data-stu-id="c48fe-129">id</span></span>|<span data-ttu-id="c48fe-130">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-130">String</span></span>|<span data-ttu-id="c48fe-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c48fe-131">Key of the setting.</span></span> <span data-ttu-id="c48fe-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-133">displayName</span><span class="sxs-lookup"><span data-stu-id="c48fe-133">displayName</span></span>|<span data-ttu-id="c48fe-134">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-134">String</span></span>|<span data-ttu-id="c48fe-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="c48fe-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="c48fe-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-137">description</span><span class="sxs-lookup"><span data-stu-id="c48fe-137">description</span></span>|<span data-ttu-id="c48fe-138">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-138">String</span></span>|<span data-ttu-id="c48fe-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c48fe-139">The description of the app.</span></span> <span data-ttu-id="c48fe-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-141">publisher</span><span class="sxs-lookup"><span data-stu-id="c48fe-141">Publisher</span></span>|<span data-ttu-id="c48fe-142">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-142">String</span></span>|<span data-ttu-id="c48fe-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c48fe-143">The name of the app.</span></span> <span data-ttu-id="c48fe-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="c48fe-145">largeIcon</span></span>|[<span data-ttu-id="c48fe-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="c48fe-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="c48fe-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="c48fe-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="c48fe-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c48fe-149">createdDateTime</span></span>|<span data-ttu-id="c48fe-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c48fe-150">DateTimeOffset</span></span>|<span data-ttu-id="c48fe-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c48fe-151">The date and time when the page was created.</span></span> <span data-ttu-id="c48fe-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c48fe-153">lastModifiedDateTime</span></span>|<span data-ttu-id="c48fe-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c48fe-154">DateTimeOffset</span></span>|<span data-ttu-id="c48fe-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c48fe-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="c48fe-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="c48fe-157">isFeatured</span></span>|<span data-ttu-id="c48fe-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="c48fe-158">Boolean</span></span>|<span data-ttu-id="c48fe-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="c48fe-160">privacyInformationUrl</span></span>|<span data-ttu-id="c48fe-161">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-161">String</span></span>|<span data-ttu-id="c48fe-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="c48fe-162">The privacy statement Url.</span></span> <span data-ttu-id="c48fe-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="c48fe-164">informationUrl</span></span>|<span data-ttu-id="c48fe-165">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-165">String</span></span>|<span data-ttu-id="c48fe-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c48fe-166">The more information Url.</span></span> <span data-ttu-id="c48fe-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-168">owner</span><span class="sxs-lookup"><span data-stu-id="c48fe-168">owner</span></span>|<span data-ttu-id="c48fe-169">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-169">String</span></span>|<span data-ttu-id="c48fe-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c48fe-170">The owner of the timesheet.</span></span> <span data-ttu-id="c48fe-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-172">developer</span><span class="sxs-lookup"><span data-stu-id="c48fe-172">developer</span></span>|<span data-ttu-id="c48fe-173">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-173">String</span></span>|<span data-ttu-id="c48fe-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c48fe-174">The name of the app.</span></span> <span data-ttu-id="c48fe-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-176">notes</span><span class="sxs-lookup"><span data-stu-id="c48fe-176">Notes</span></span>|<span data-ttu-id="c48fe-177">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-177">String</span></span>|<span data-ttu-id="c48fe-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c48fe-178">Notes for the app.</span></span> <span data-ttu-id="c48fe-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="c48fe-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c48fe-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="c48fe-180">publishingState</span></span>|<span data-ttu-id="c48fe-181">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-181">String</span></span>|<span data-ttu-id="c48fe-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c48fe-182">The publishing state for the app.</span></span> <span data-ttu-id="c48fe-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="c48fe-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="c48fe-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="c48fe-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="c48fe-185">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="c48fe-185">usedLicenseCount</span></span>|<span data-ttu-id="c48fe-186">Int32</span><span class="sxs-lookup"><span data-stu-id="c48fe-186">Int32</span></span>|<span data-ttu-id="c48fe-187">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="c48fe-187">The number of VPP licenses in use.</span></span>|
|<span data-ttu-id="c48fe-188">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="c48fe-188">totalLicenseCount</span></span>|<span data-ttu-id="c48fe-189">Int32</span><span class="sxs-lookup"><span data-stu-id="c48fe-189">Int32</span></span>|<span data-ttu-id="c48fe-190">Número total de licencias VPP.</span><span class="sxs-lookup"><span data-stu-id="c48fe-190">The total number of VPP licenses.</span></span>|
|<span data-ttu-id="c48fe-191">releaseDateTime</span><span class="sxs-lookup"><span data-stu-id="c48fe-191">releaseDateTime</span></span>|<span data-ttu-id="c48fe-192">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c48fe-192">DateTimeOffset</span></span>|<span data-ttu-id="c48fe-193">Fecha y hora de publicación de la aplicación de VPP.</span><span class="sxs-lookup"><span data-stu-id="c48fe-193">The VPP application release date and time.</span></span>|
|<span data-ttu-id="c48fe-194">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="c48fe-194">appStoreUrl</span></span>|<span data-ttu-id="c48fe-195">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-195">String</span></span>|<span data-ttu-id="c48fe-196">Dirección URL de la tienda.</span><span class="sxs-lookup"><span data-stu-id="c48fe-196">The store URL.</span></span>|
|<span data-ttu-id="c48fe-197">licensingType</span><span class="sxs-lookup"><span data-stu-id="c48fe-197">licensingType</span></span>|[<span data-ttu-id="c48fe-198">vppLicensingType</span><span class="sxs-lookup"><span data-stu-id="c48fe-198">vppLicensingType</span></span>](../resources/intune_apps_vpplicensingtype.md)|<span data-ttu-id="c48fe-199">Tipo de licencia compatible.</span><span class="sxs-lookup"><span data-stu-id="c48fe-199">The supported License Type.</span></span>|
|<span data-ttu-id="c48fe-200">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="c48fe-200">applicableDeviceType</span></span>|[<span data-ttu-id="c48fe-201">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="c48fe-201">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="c48fe-202">Tipo de dispositivo iOS aplicable.</span><span class="sxs-lookup"><span data-stu-id="c48fe-202">The applicable iOS Device Type.</span></span>|
|<span data-ttu-id="c48fe-203">vppTokenOrganizationName</span><span class="sxs-lookup"><span data-stu-id="c48fe-203">vppTokenOrganizationName</span></span>|<span data-ttu-id="c48fe-204">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-204">String</span></span>|<span data-ttu-id="c48fe-205">Organización asociada al token del Programa de Compras por Volumen de Apple</span><span class="sxs-lookup"><span data-stu-id="c48fe-205">The organization associated with the Apple Volume Purchase Program Token</span></span>|
|<span data-ttu-id="c48fe-206">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="c48fe-206">vppTokenAccountType</span></span>|<span data-ttu-id="c48fe-207">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-207">String</span></span>|<span data-ttu-id="c48fe-208">Tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="c48fe-208">The type of volume purchase program which the given Apple Volume Purchase Program Token is associated with.</span></span> <span data-ttu-id="c48fe-209">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="c48fe-209">Possible values are: `business`, `education`.</span></span> <span data-ttu-id="c48fe-210">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="c48fe-210">Possible values are: `business`, `education`.</span></span>|
|<span data-ttu-id="c48fe-211">vppTokenAppleId</span><span class="sxs-lookup"><span data-stu-id="c48fe-211">vppTokenAppleId</span></span>|<span data-ttu-id="c48fe-212">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-212">String</span></span>|<span data-ttu-id="c48fe-213">Identificador de Apple asociado al token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="c48fe-213">The Apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="c48fe-214">bundleId</span><span class="sxs-lookup"><span data-stu-id="c48fe-214">bundleId</span></span>|<span data-ttu-id="c48fe-215">String</span><span class="sxs-lookup"><span data-stu-id="c48fe-215">String</span></span>|<span data-ttu-id="c48fe-216">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="c48fe-216">The Identity Name.</span></span>|



## <a name="response"></a><span data-ttu-id="c48fe-217">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c48fe-217">Response</span></span>
<span data-ttu-id="c48fe-218">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosVppApp](../resources/intune_apps_iosvppapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c48fe-218">If successful, this method returns a `201 Created` response code and a [ListItemVersion](../resources/intune_apps_iosvppapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c48fe-219">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c48fe-219">Example</span></span>
### <a name="request"></a><span data-ttu-id="c48fe-220">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c48fe-220">Request</span></span>
<span data-ttu-id="c48fe-221">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c48fe-221">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1286

{
  "@odata.type": "#microsoft.graph.iosVppApp",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing",
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "releaseDateTime": "2017-01-01T00:01:34.7470482-08:00",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "licensingType": {
    "@odata.type": "microsoft.graph.vppLicensingType",
    "supportsUserLicensing": true,
    "supportsDeviceLicensing": true
  },
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "vppTokenOrganizationName": "Vpp Token Organization Name value",
  "vppTokenAccountType": "education",
  "vppTokenAppleId": "Vpp Token Apple Id value",
  "bundleId": "Bundle Id value"
}
```

### <a name="response"></a><span data-ttu-id="c48fe-222">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c48fe-222">Response</span></span>
<span data-ttu-id="c48fe-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c48fe-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1394

{
  "@odata.type": "#microsoft.graph.iosVppApp",
  "id": "a0ac9b6f-9b6f-a0ac-6f9b-aca06f9baca0",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing",
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "releaseDateTime": "2017-01-01T00:01:34.7470482-08:00",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "licensingType": {
    "@odata.type": "microsoft.graph.vppLicensingType",
    "supportsUserLicensing": true,
    "supportsDeviceLicensing": true
  },
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "vppTokenOrganizationName": "Vpp Token Organization Name value",
  "vppTokenAccountType": "education",
  "vppTokenAppleId": "Vpp Token Apple Id value",
  "bundleId": "Bundle Id value"
}
```


