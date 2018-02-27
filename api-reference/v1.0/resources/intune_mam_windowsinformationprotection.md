# <a name="windowsinformationprotection-resource-type"></a><span data-ttu-id="3a553-101">Tipo de recurso windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="3a553-101">windowsInformationProtection resource type</span></span>

> <span data-ttu-id="3a553-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3a553-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3a553-103">Directiva de Windows Information Protection para configurar las opciones de administración detalladas</span><span class="sxs-lookup"><span data-stu-id="3a553-103">Policy for Windows information protection to configure detailed management settings</span></span>

<span data-ttu-id="3a553-104">Hereda de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-104">Inherits from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>

## <a name="methods"></a><span data-ttu-id="3a553-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a553-105">Methods</span></span>
|<span data-ttu-id="3a553-106">Método</span><span class="sxs-lookup"><span data-stu-id="3a553-106">Method</span></span>|<span data-ttu-id="3a553-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a553-107">Return Type</span></span>|<span data-ttu-id="3a553-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a553-108">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="3a553-109">Enumerar windowsInformationProtections</span><span class="sxs-lookup"><span data-stu-id="3a553-109">List windowsInformationProtections</span></span>](../api/intune_mam_windowsinformationprotection_list.md)|<span data-ttu-id="3a553-110">Colección [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-110">[windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) collection</span></span>|<span data-ttu-id="3a553-111">Enumere las propiedades y las relaciones de los objetos [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="3a553-111">List properties and relationships of the [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) objects.</span></span>|
|[<span data-ttu-id="3a553-112">Obtener windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="3a553-112">Get windowsInformationProtection</span></span>](../api/intune_mam_windowsinformationprotection_get.md)|[<span data-ttu-id="3a553-113">windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="3a553-113">windowsInformationProtection</span></span>](../resources/intune_mam_windowsinformationprotection.md)|<span data-ttu-id="3a553-114">Lea las propiedades y las relaciones del objeto [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="3a553-114">Read properties and relationships of [plannerPlanDetails](../resources/intune_mam_windowsinformationprotection.md) object.</span></span>|
|[<span data-ttu-id="3a553-115">Acción assign</span><span class="sxs-lookup"><span data-stu-id="3a553-115">assign action</span></span>](../api/intune_mam_windowsinformationprotection_assign.md)|<span data-ttu-id="3a553-116">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3a553-116">None</span></span>|<span data-ttu-id="3a553-117">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3a553-117">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="3a553-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a553-118">Properties</span></span>
|<span data-ttu-id="3a553-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a553-119">Property</span></span>|<span data-ttu-id="3a553-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a553-120">Type</span></span>|<span data-ttu-id="3a553-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a553-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3a553-122">displayName</span><span class="sxs-lookup"><span data-stu-id="3a553-122">displayName</span></span>|<span data-ttu-id="3a553-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="3a553-123">String</span></span>|<span data-ttu-id="3a553-124">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="3a553-124">Policy display name.</span></span> <span data-ttu-id="3a553-125">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-125">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="3a553-126">description</span><span class="sxs-lookup"><span data-stu-id="3a553-126">description</span></span>|<span data-ttu-id="3a553-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="3a553-127">String</span></span>|<span data-ttu-id="3a553-128">La descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="3a553-128">The policy's description.</span></span> <span data-ttu-id="3a553-129">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-129">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="3a553-130">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="3a553-130">createdDateTime</span></span>|<span data-ttu-id="3a553-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3a553-131">DateTimeOffset</span></span>|<span data-ttu-id="3a553-132">La fecha y la hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="3a553-132">The date and time when the page was created.</span></span> <span data-ttu-id="3a553-133">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-133">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="3a553-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="3a553-134">lastModifiedDateTime</span></span>|<span data-ttu-id="3a553-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3a553-135">DateTimeOffset</span></span>|<span data-ttu-id="3a553-136">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="3a553-136">Last time the policy was modified.</span></span> <span data-ttu-id="3a553-137">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-137">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="3a553-138">id</span><span class="sxs-lookup"><span data-stu-id="3a553-138">id</span></span>|<span data-ttu-id="3a553-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="3a553-139">String</span></span>|<span data-ttu-id="3a553-140">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3a553-140">Key of the setting.</span></span> <span data-ttu-id="3a553-141">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-141">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="3a553-142">versión</span><span class="sxs-lookup"><span data-stu-id="3a553-142">version</span></span>|<span data-ttu-id="3a553-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="3a553-143">String</span></span>|<span data-ttu-id="3a553-144">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3a553-144">Version of the entity.</span></span> <span data-ttu-id="3a553-145">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-145">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="3a553-146">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="3a553-146">enforcementLevel</span></span>|<span data-ttu-id="3a553-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="3a553-147">String</span></span>|<span data-ttu-id="3a553-148">Nivel de obligatoriedad del trabajo en curso. Consulte la definición de enumeración para los valores compatibles. Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="3a553-148">WIP enforcement level.See the Enum definition for supported values Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="3a553-149">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="3a553-149">enterpriseDomain</span></span>|<span data-ttu-id="3a553-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="3a553-150">String</span></span>|<span data-ttu-id="3a553-151">Dominio empresarial principal</span><span class="sxs-lookup"><span data-stu-id="3a553-151">Primary enterprise domain</span></span>|
|<span data-ttu-id="3a553-152">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="3a553-152">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="3a553-153">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-153">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="3a553-154">Lista de dominios empresariales que quiere proteger</span><span class="sxs-lookup"><span data-stu-id="3a553-154">List of enterprise domains to be protected</span></span>|
|<span data-ttu-id="3a553-155">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="3a553-155">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="3a553-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a553-156">Boolean</span></span>|<span data-ttu-id="3a553-157">Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN)</span><span class="sxs-lookup"><span data-stu-id="3a553-157">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured</span></span>|
|<span data-ttu-id="3a553-158">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="3a553-158">dataRecoveryCertificate</span></span>|[<span data-ttu-id="3a553-159">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="3a553-159">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune_mam_windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="3a553-160">Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="3a553-160">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="3a553-161">Esto es lo mismo que el certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS)</span><span class="sxs-lookup"><span data-stu-id="3a553-161">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS)</span></span>|
|<span data-ttu-id="3a553-162">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="3a553-162">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="3a553-163">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a553-163">Boolean</span></span>|<span data-ttu-id="3a553-164">Esta directiva controla si quiere revocar las claves de trabajo en curso cuando un dispositivo anule la inscripción del servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="3a553-164">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="3a553-165">Si se establece en 1 (No revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción.</span><span class="sxs-lookup"><span data-stu-id="3a553-165">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="3a553-166">Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="3a553-166">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span>|
|<span data-ttu-id="3a553-167">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="3a553-167">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="3a553-168">Guid</span><span class="sxs-lookup"><span data-stu-id="3a553-168">Guid</span></span>|<span data-ttu-id="3a553-169">GUID de TemplateID que se va a usar para el cifrado RMS.</span><span class="sxs-lookup"><span data-stu-id="3a553-169">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="3a553-170">La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo tienen acceso</span><span class="sxs-lookup"><span data-stu-id="3a553-170">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access</span></span>|
|<span data-ttu-id="3a553-171">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="3a553-171">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="3a553-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a553-172">Boolean</span></span>|<span data-ttu-id="3a553-173">Especifica si se permite el cifrado de Azure RMS para WIP.</span><span class="sxs-lookup"><span data-stu-id="3a553-173">Specifies whether to allow Azure RMS encryption for WIP</span></span>|
|<span data-ttu-id="3a553-174">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="3a553-174">iconsVisible</span></span>|<span data-ttu-id="3a553-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a553-175">Boolean</span></span>|<span data-ttu-id="3a553-176">Determina si se agregan las superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3a553-176">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="3a553-177">A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP</span><span class="sxs-lookup"><span data-stu-id="3a553-177">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app</span></span>|
|<span data-ttu-id="3a553-178">protectedApps</span><span class="sxs-lookup"><span data-stu-id="3a553-178">protectedApps</span></span>|<span data-ttu-id="3a553-179">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-179">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="3a553-180">Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado</span><span class="sxs-lookup"><span data-stu-id="3a553-180">Protected applications can access enterprise data and the data handled by those applications are protected with encryption</span></span>|
|<span data-ttu-id="3a553-181">exemptApps</span><span class="sxs-lookup"><span data-stu-id="3a553-181">exemptApps</span></span>|<span data-ttu-id="3a553-182">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-182">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="3a553-183">Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos.</span><span class="sxs-lookup"><span data-stu-id="3a553-183">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="3a553-184">Esto ocurre porque algunas aplicaciones empresariales críticas podrían tener problemas de compatibilidad con los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="3a553-184">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span>|
|<span data-ttu-id="3a553-185">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="3a553-185">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="3a553-186">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-186">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="3a553-187">Esta es la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="3a553-187">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="3a553-188">Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales</span><span class="sxs-lookup"><span data-stu-id="3a553-188">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to</span></span>|
|<span data-ttu-id="3a553-189">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="3a553-189">enterpriseProxiedDomains</span></span>|<span data-ttu-id="3a553-190">Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-190">[windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="3a553-191">Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección.</span><span class="sxs-lookup"><span data-stu-id="3a553-191">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="3a553-192">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="3a553-192">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="3a553-193">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="3a553-193">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="3a553-194">Un servidor proxy que se use para este propósito también debe configurarse mediante la directiva EnterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="3a553-194">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy</span></span>|
|<span data-ttu-id="3a553-195">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="3a553-195">enterpriseIPRanges</span></span>|<span data-ttu-id="3a553-196">Colección [windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-196">[windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="3a553-197">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="3a553-197">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="3a553-198">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="3a553-198">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="3a553-199">Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales</span><span class="sxs-lookup"><span data-stu-id="3a553-199">These locations will be considered a safe destination for enterprise data to be shared to</span></span>|
|<span data-ttu-id="3a553-200">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="3a553-200">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="3a553-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a553-201">Boolean</span></span>|<span data-ttu-id="3a553-202">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="3a553-202">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="3a553-203">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="3a553-203">Default is false</span></span>|
|<span data-ttu-id="3a553-204">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="3a553-204">enterpriseProxyServers</span></span>|<span data-ttu-id="3a553-205">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-205">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="3a553-206">Esta es una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="3a553-206">This is a list of proxy servers.</span></span> <span data-ttu-id="3a553-207">Cualquier servidor que no esté en esta lista se considera no empresarial</span><span class="sxs-lookup"><span data-stu-id="3a553-207">Any server not on this list is considered non-enterprise</span></span>|
|<span data-ttu-id="3a553-208">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="3a553-208">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="3a553-209">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-209">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="3a553-210">Esta es la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="3a553-210">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="3a553-211">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="3a553-211">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="3a553-212">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="3a553-212">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="3a553-213">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="3a553-213">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="3a553-214">Los servidores proxy solo se usan para configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy</span><span class="sxs-lookup"><span data-stu-id="3a553-214">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies</span></span>|
|<span data-ttu-id="3a553-215">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="3a553-215">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="3a553-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a553-216">Boolean</span></span>|<span data-ttu-id="3a553-217">Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="3a553-217">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="3a553-218">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="3a553-218">Default is false</span></span>|
|<span data-ttu-id="3a553-219">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="3a553-219">neutralDomainResources</span></span>|<span data-ttu-id="3a553-220">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-220">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="3a553-221">Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal</span><span class="sxs-lookup"><span data-stu-id="3a553-221">List of domain names that can used for work or personal resource</span></span>|
|<span data-ttu-id="3a553-222">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="3a553-222">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="3a553-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a553-223">Boolean</span></span>|<span data-ttu-id="3a553-224">Esta opción es para que el indexador de Windows Search permita o impida la indexación de los elementos</span><span class="sxs-lookup"><span data-stu-id="3a553-224">This switch is for the Windows Search Indexer, to allow or disallow indexing of items</span></span>|
|<span data-ttu-id="3a553-225">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="3a553-225">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="3a553-226">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-226">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="3a553-227">Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa</span><span class="sxs-lookup"><span data-stu-id="3a553-227">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary</span></span>|
|<span data-ttu-id="3a553-228">isAssigned</span><span class="sxs-lookup"><span data-stu-id="3a553-228">isAssigned</span></span>|<span data-ttu-id="3a553-229">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a553-229">Boolean</span></span>|<span data-ttu-id="3a553-230">Indica si la directiva se implementará en los grupos de inclusión o no.</span><span class="sxs-lookup"><span data-stu-id="3a553-230">Indicates if the policy is deployed to any inclusion groups or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3a553-231">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3a553-231">Relationships</span></span>
|<span data-ttu-id="3a553-232">Relación</span><span class="sxs-lookup"><span data-stu-id="3a553-232">Relationship</span></span>|<span data-ttu-id="3a553-233">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a553-233">Type</span></span>|<span data-ttu-id="3a553-234">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a553-234">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3a553-235">protectedAppLockerFiles</span><span class="sxs-lookup"><span data-stu-id="3a553-235">protectedAppLockerFiles</span></span>|<span data-ttu-id="3a553-236">Colección [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-236">[windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md) collection</span></span>|<span data-ttu-id="3a553-237">Otra forma de introducir aplicaciones protegidas mediante archivos XML</span><span class="sxs-lookup"><span data-stu-id="3a553-237">Another way to input protected apps through xml files</span></span>|
|<span data-ttu-id="3a553-238">exemptAppLockerFiles</span><span class="sxs-lookup"><span data-stu-id="3a553-238">exemptAppLockerFiles</span></span>|<span data-ttu-id="3a553-239">Colección [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-239">[windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md) collection</span></span>|<span data-ttu-id="3a553-240">Otra forma de introducir aplicaciones exentas mediante archivos XML</span><span class="sxs-lookup"><span data-stu-id="3a553-240">Another way to input exempt apps through xml files</span></span>|
|<span data-ttu-id="3a553-241">asignaciones</span><span class="sxs-lookup"><span data-stu-id="3a553-241">assignments</span></span>|<span data-ttu-id="3a553-242">Colección [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="3a553-242">[targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md) collection</span></span>|<span data-ttu-id="3a553-243">Propiedad de navegación a la lista de grupos de seguridad destinados a la directiva.</span><span class="sxs-lookup"><span data-stu-id="3a553-243">Navigation property to list of security groups targeted for policy.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3a553-244">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3a553-244">JSON Representation</span></span>
<span data-ttu-id="3a553-245">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3a553-245">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsInformationProtection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtection",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String",
  "enforcementLevel": "String",
  "enterpriseDomain": "String",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "String",
    "description": "String",
    "expirationDateTime": "String (timestamp)",
    "certificate": "binary"
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "<Unknown Primitive Type Edm.Guid>",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "String",
      "description": "String",
      "publisherName": "String",
      "productName": "String",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "String",
      "description": "String",
      "publisherName": "String",
      "productName": "String",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "String",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "String",
          "proxy": "String"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "String",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "String",
          "upperAddress": "String"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "isAssigned": true
}
```


