# <a name="how-to-protect-your-company-app-data-with-microsoft-intune"></a><span data-ttu-id="726a3-101">Cómo proteger los datos empresariales de aplicaciones con Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="726a3-101">How to protect your company app data with Microsoft Intune</span></span>

> <span data-ttu-id="726a3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/es-ES/cloud-platform/microsoft-intune-pricing) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="726a3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://www.microsoft.com/es-ES/cloud-platform/microsoft-intune-pricing) by the customer.</span></span>

<span data-ttu-id="726a3-103">Las directivas de protección de aplicaciones de Microsoft Intune ayudan a proteger los datos empresariales y evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="726a3-103">Microsoft Intune app protection policies help protect your company data and prevent data loss.</span></span>

<span data-ttu-id="726a3-104">Puede usar las directivas de protección de aplicaciones de Intune para ayudar a proteger los datos de su empresa.</span><span class="sxs-lookup"><span data-stu-id="726a3-104">You can use Intune app protection policies to help protect your company’s data.</span></span> <span data-ttu-id="726a3-105">Debido a que las directivas de protección de aplicaciones de Intune se pueden usar de forma independiente de cualquier solución de administración de dispositivos móviles (MDM), protege los datos de su empresa con o sin inscribir los dispositivos en una solución de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="726a3-105">Because Intune app protection policies can be used independent of any mobile-device management (MDM) solution, you protect your company’s data with or without enrolling devices in a device management solution.</span></span> <span data-ttu-id="726a3-106">Mediante la implementación de directivas de nivel de aplicación, puede restringir el acceso a los recursos de la empresa y mantener los datos dentro del ámbito del departamento de TI.</span><span class="sxs-lookup"><span data-stu-id="726a3-106">By implementing app-level policies, you can restrict access to company resources and keep data within the purview of your IT department.</span></span>

<span data-ttu-id="726a3-107">Los siguientes recursos de Graph están disponibles para administrar las directivas de protección de aplicaciones en Intune:</span><span class="sxs-lookup"><span data-stu-id="726a3-107">The following Graph resources are available to manage app protection polices in Intune:</span></span>

- [<span data-ttu-id="726a3-108">Destino de asignación de todos los dispositivos</span><span class="sxs-lookup"><span data-stu-id="726a3-108">All devices assignment target</span></span>](intune_mam_alldevicesassignmenttarget.md)
- [<span data-ttu-id="726a3-109">Destino de asignación de todos los usuarios con licencia</span><span class="sxs-lookup"><span data-stu-id="726a3-109">All licensed users assignment target</span></span>](intune_mam_alllicensedusersassignmenttarget.md)
- [<span data-ttu-id="726a3-110">Protección de aplicaciones administradas de Android</span><span class="sxs-lookup"><span data-stu-id="726a3-110">Android managed app protection</span></span>](intune_mam_androidmanagedappprotection.md)
- [<span data-ttu-id="726a3-111">Registro de aplicaciones administradas de Android</span><span class="sxs-lookup"><span data-stu-id="726a3-111">Android managed app registration</span></span>](intune_mam_androidmanagedappregistration.md)
- [<span data-ttu-id="726a3-112">Identificador de aplicaciones para móviles de Android</span><span class="sxs-lookup"><span data-stu-id="726a3-112">Android mobile app identifier</span></span>](intune_mam_androidmobileappidentifier.md)
- [<span data-ttu-id="726a3-113">Protección predeterminada de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="726a3-113">Default managed app protection</span></span>](intune_mam_defaultmanagedappprotection.md)
- [<span data-ttu-id="726a3-114">Destino de asignación de administración de dispositivos y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="726a3-114">Device and app management assignment target</span></span>](intune_mam_deviceandappmanagementassignmenttarget.md)
- [<span data-ttu-id="726a3-115">Administración de aplicaciones de dispositivo</span><span class="sxs-lookup"><span data-stu-id="726a3-115">Device app management</span></span>](intune_mam_deviceappmanagement.md)
- [<span data-ttu-id="726a3-116">Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="726a3-116">Device management</span></span>](intune_wip_devicemanagement.md)
- [<span data-ttu-id="726a3-117">Destino de asignación de grupo de exclusión</span><span class="sxs-lookup"><span data-stu-id="726a3-117">Exclusion group assignment target</span></span>](intune_mam_exclusiongroupassignmenttarget.md)
- [<span data-ttu-id="726a3-118">Destino de asignación de grupo</span><span class="sxs-lookup"><span data-stu-id="726a3-118">Group assignment target</span></span>](intune_mam_groupassignmenttarget.md)
- [<span data-ttu-id="726a3-119">Protección de aplicaciones administradas de iOS</span><span class="sxs-lookup"><span data-stu-id="726a3-119">iOS managed app protection</span></span>](intune_mam_iosmanagedappprotection.md)
- [<span data-ttu-id="726a3-120">Registro de aplicaciones administradas de iOS</span><span class="sxs-lookup"><span data-stu-id="726a3-120">iOS managed app registration</span></span>](intune_mam_iosmanagedappregistration.md)
- [<span data-ttu-id="726a3-121">Identificador de aplicaciones para móviles de iOS</span><span class="sxs-lookup"><span data-stu-id="726a3-121">iOS mobile app identifier</span></span>](intune_mam_iosmobileappidentifier.md)
- [<span data-ttu-id="726a3-122">Intervalo IP</span><span class="sxs-lookup"><span data-stu-id="726a3-122">IP range</span></span>](intune_mam_iprange.md)
- [<span data-ttu-id="726a3-123">Intervalo IPv4</span><span class="sxs-lookup"><span data-stu-id="726a3-123">IPv4 range</span></span>](intune_mam_ipv4range.md)
- [<span data-ttu-id="726a3-124">Intervalo IPv6</span><span class="sxs-lookup"><span data-stu-id="726a3-124">IPv6 range</span></span>](intune_mam_ipv6range.md)
- [<span data-ttu-id="726a3-125">JSON</span><span class="sxs-lookup"><span data-stu-id="726a3-125">json</span></span>](intune_mam_json.md)
- [<span data-ttu-id="726a3-126">Par clave-valor</span><span class="sxs-lookup"><span data-stu-id="726a3-126">Key/value pair</span></span>](intune_mam_keyvaluepair.md)
- [<span data-ttu-id="726a3-127">Configuración de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="726a3-127">Managed app configuration</span></span>](intune_mam_managedappconfiguration.md)
- [<span data-ttu-id="726a3-128">Estado de diagnóstico de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="726a3-128">Managed app diagnostic status</span></span>](intune_mam_managedappdiagnosticstatus.md)
- [<span data-ttu-id="726a3-129">Operación de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="726a3-129">Managed app operation</span></span>](intune_mam_managedappoperation.md)
- [<span data-ttu-id="726a3-130">Resumen de implementación de directivas de aplicaciones administradas por aplicación</span><span class="sxs-lookup"><span data-stu-id="726a3-130">Managed app policy deployment summary per app</span></span>](intune_mam_managedapppolicydeploymentsummaryperapp.md)
- [<span data-ttu-id="726a3-131">Resumen de implementación de directivas de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="726a3-131">Managed app policy deployment summary</span></span>](intune_mam_managedapppolicydeploymentsummary.md)
- [<span data-ttu-id="726a3-132">Directiva de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="726a3-132">Managed app policy</span></span>](intune_mam_managedapppolicy.md)
- [<span data-ttu-id="726a3-133">Protección de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="726a3-133">Managed app protection</span></span>](intune_mam_managedappprotection.md)
- [<span data-ttu-id="726a3-134">Registro de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="726a3-134">Managed app registration</span></span>](intune_mam_managedappregistration.md)
- [<span data-ttu-id="726a3-135">Estado de las aplicaciones administradas sin procesar</span><span class="sxs-lookup"><span data-stu-id="726a3-135">Managed app status raw</span></span>](intune_mam_managedappstatusraw.md)
- [<span data-ttu-id="726a3-136">Estado de las aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="726a3-136">Managed app status</span></span>](intune_mam_managedappstatus.md)
- [<span data-ttu-id="726a3-137">Aplicación móvil administrada</span><span class="sxs-lookup"><span data-stu-id="726a3-137">Managed mobile app</span></span>](intune_mam_managedmobileapp.md)
- [<span data-ttu-id="726a3-138">Directiva de Windows Information Protection de MDM</span><span class="sxs-lookup"><span data-stu-id="726a3-138">MDM windows information protection policy</span></span>](intune_mam_mdmwindowsinformationprotectionpolicy.md)
- [<span data-ttu-id="726a3-139">Identificador de aplicaciones para móviles</span><span class="sxs-lookup"><span data-stu-id="726a3-139">Mobile app identifier</span></span>](intune_mam_mobileappidentifier.md)
- [<span data-ttu-id="726a3-140">Dominio con proxy</span><span class="sxs-lookup"><span data-stu-id="726a3-140">Proxied domain</span></span>](intune_mam_proxieddomain.md)
- [<span data-ttu-id="726a3-141">Configuración de aplicaciones administradas dirigidas</span><span class="sxs-lookup"><span data-stu-id="726a3-141">Targeted managed app configuration</span></span>](intune_mam_targetedmanagedappconfiguration.md)
- [<span data-ttu-id="726a3-142">Asignación de directiva de administración de aplicaciones objetivo</span><span class="sxs-lookup"><span data-stu-id="726a3-142">Targeted managed app policy assignment</span></span>](intune_mam_targetedmanagedapppolicyassignment.md)
- [<span data-ttu-id="726a3-143">Protección de aplicaciones administradas de objetivo</span><span class="sxs-lookup"><span data-stu-id="726a3-143">Targeted managed app protection</span></span>](intune_mam_targetedmanagedappprotection.md)
- [<span data-ttu-id="726a3-144">User</span><span class="sxs-lookup"><span data-stu-id="726a3-144">User</span></span>](intune_mam_user.md)
- [<span data-ttu-id="726a3-145">Resumen de aprendizaje sobre las aplicaciones de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-145">Windows information protection app learning summary</span></span>](intune_wip_windowsinformationprotectionapplearningsummary.md)
- [<span data-ttu-id="726a3-146">Archivo de bloqueo de aplicaciones de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-146">Windows information protection app locker file</span></span>](intune_mam_windowsinformationprotectionapplockerfile.md)
- [<span data-ttu-id="726a3-147">Aplicación de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-147">Windows information protection app</span></span>](intune_mam_windowsinformationprotectionapp.md)
- [<span data-ttu-id="726a3-148">Certificado de recuperación de datos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-148">Windows information protection data recovery certificate</span></span>](intune_mam_windowsinformationprotectiondatarecoverycertificate.md)
- [<span data-ttu-id="726a3-149">Aplicación de escritorio de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-149">Windows information protection desktop app</span></span>](intune_mam_windowsinformationprotectiondesktopapp.md)
- [<span data-ttu-id="726a3-150">Colección de intervalos IP de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-150">Windows information protection IP range collection</span></span>](intune_mam_windowsinformationprotectioniprangecollection.md)
- [<span data-ttu-id="726a3-151">Resumen de aprendizaje sobre la red de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-151">Windows information protection network learning summary</span></span>](intune_wip_windowsinformationprotectionnetworklearningsummary.md)
- [<span data-ttu-id="726a3-152">Directiva de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-152">Windows information protection policy</span></span>](intune_mam_windowsinformationprotectionpolicy.md)
- [<span data-ttu-id="726a3-153">Colección de dominios con proxy de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-153">Windows information protection proxied domain collection</span></span>](intune_mam_windowsinformationprotectionproxieddomaincollection.md)
- [<span data-ttu-id="726a3-154">Colección de recursos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-154">Windows information protection resource collection</span></span>](intune_mam_windowsinformationprotectionresourcecollection.md)
- [<span data-ttu-id="726a3-155">Aplicación de la tienda de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-155">Windows information protection store app</span></span>](intune_mam_windowsinformationprotectionstoreapp.md)
- [<span data-ttu-id="726a3-156">Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="726a3-156">Windows information protection</span></span>](intune_mam_windowsinformationprotection.md)