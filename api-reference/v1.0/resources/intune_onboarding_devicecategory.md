# <a name="devicecategory-resource-type"></a><span data-ttu-id="61602-101">Tipo de recurso deviceCategory</span><span class="sxs-lookup"><span data-stu-id="61602-101">deviceCategory resource type</span></span>

> <span data-ttu-id="61602-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="61602-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="61602-103">Las categorías de dispositivo proporcionan una forma de organizar sus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="61602-103">Device categories provides a way to organize your devices.</span></span> <span data-ttu-id="61602-104">Al usar categorías de dispositivos, los administradores de la compañía pueden definir las categorías de forma pertinente para su empresa.</span><span class="sxs-lookup"><span data-stu-id="61602-104">Using device categories, company administrators can define their own categories that make sense to their company.</span></span> <span data-ttu-id="61602-105">A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="61602-105">These categories can then be applied to a device in the Intune Azure console or selected by a user during device enrollment.</span></span> <span data-ttu-id="61602-106">Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="61602-106">You can filter reports and create dynamic Azure Active Directory device groups based on device categories.</span></span>
## <a name="methods"></a><span data-ttu-id="61602-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="61602-107">Methods</span></span>
|<span data-ttu-id="61602-108">Método</span><span class="sxs-lookup"><span data-stu-id="61602-108">Method</span></span>|<span data-ttu-id="61602-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61602-109">Return Type</span></span>|<span data-ttu-id="61602-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="61602-110">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="61602-111">Enumerar deviceCategories</span><span class="sxs-lookup"><span data-stu-id="61602-111">List deviceCategories</span></span>](../api/intune_onboarding_devicecategory_list.md)|<span data-ttu-id="61602-112">Colección [deviceCategory](../resources/intune_onboarding_devicecategory.md)</span><span class="sxs-lookup"><span data-stu-id="61602-112">[deviceCategory](../resources/intune_onboarding_devicecategory.md) collection</span></span>|<span data-ttu-id="61602-113">Enumere las propiedades y las relaciones de los objetos [deviceCategory](../resources/intune_onboarding_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="61602-113">List properties and relationships of the [deviceCategory](../resources/intune_onboarding_devicecategory.md) objects.</span></span>|
|[<span data-ttu-id="61602-114">Obtener deviceCategory</span><span class="sxs-lookup"><span data-stu-id="61602-114">Get deviceCategory</span></span>](../api/intune_onboarding_devicecategory_get.md)|[<span data-ttu-id="61602-115">deviceCategory</span><span class="sxs-lookup"><span data-stu-id="61602-115">deviceCategory</span></span>](../resources/intune_onboarding_devicecategory.md)|<span data-ttu-id="61602-116">Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune_onboarding_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="61602-116">Read properties and relationships of [plannerPlanDetails](../resources/intune_onboarding_devicecategory.md) object.</span></span>|
|[<span data-ttu-id="61602-117">Crear deviceCategory</span><span class="sxs-lookup"><span data-stu-id="61602-117">Create deviceCategory</span></span>](../api/intune_onboarding_devicecategory_create.md)|[<span data-ttu-id="61602-118">deviceCategory</span><span class="sxs-lookup"><span data-stu-id="61602-118">deviceCategory</span></span>](../resources/intune_onboarding_devicecategory.md)|<span data-ttu-id="61602-119">Cree un objeto [deviceCategory](../resources/intune_onboarding_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="61602-119">Create a new [plannerBucket](../resources/intune_onboarding_devicecategory.md) object.</span></span>|
|[<span data-ttu-id="61602-120">Eliminar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="61602-120">Delete deviceCategory</span></span>](../api/intune_onboarding_devicecategory_delete.md)|<span data-ttu-id="61602-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="61602-121">None</span></span>|<span data-ttu-id="61602-122">Elimina un [deviceCategory](../resources/intune_onboarding_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="61602-122">Deletes a [deviceCategory](../resources/intune_onboarding_devicecategory.md).</span></span>|
|[<span data-ttu-id="61602-123">Actualizar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="61602-123">Update deviceCategory</span></span>](../api/intune_onboarding_devicecategory_update.md)|[<span data-ttu-id="61602-124">deviceCategory</span><span class="sxs-lookup"><span data-stu-id="61602-124">deviceCategory</span></span>](../resources/intune_onboarding_devicecategory.md)|<span data-ttu-id="61602-125">Actualice las propiedades de un objeto [deviceCategory](../resources/intune_onboarding_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="61602-125">Update the properties of a [calendar](../resources/intune_onboarding_devicecategory.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="61602-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61602-126">Properties</span></span>
|<span data-ttu-id="61602-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="61602-127">Property</span></span>|<span data-ttu-id="61602-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="61602-128">Type</span></span>|<span data-ttu-id="61602-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="61602-129">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="61602-130">id</span><span class="sxs-lookup"><span data-stu-id="61602-130">id</span></span>|<span data-ttu-id="61602-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="61602-131">String</span></span>|<span data-ttu-id="61602-132">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61602-132">Unique identifier for the device category.</span></span> <span data-ttu-id="61602-133">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="61602-133">Read-only.</span></span>|
|<span data-ttu-id="61602-134">displayName</span><span class="sxs-lookup"><span data-stu-id="61602-134">displayName</span></span>|<span data-ttu-id="61602-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="61602-135">String</span></span>|<span data-ttu-id="61602-136">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61602-136">Display name for the device category.</span></span>|
|<span data-ttu-id="61602-137">descripción</span><span class="sxs-lookup"><span data-stu-id="61602-137">description</span></span>|<span data-ttu-id="61602-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="61602-138">String</span></span>|<span data-ttu-id="61602-139">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61602-139">Optional description for the device category.</span></span>|

## <a name="relationships"></a><span data-ttu-id="61602-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="61602-140">Relationships</span></span>
<span data-ttu-id="61602-141">Ninguna</span><span class="sxs-lookup"><span data-stu-id="61602-141">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="61602-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="61602-142">JSON Representation</span></span>
<span data-ttu-id="61602-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="61602-143">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String"
}
```


