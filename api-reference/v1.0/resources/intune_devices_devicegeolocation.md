# <a name="devicegeolocation-resource-type"></a><span data-ttu-id="2b148-101">Tipo de recurso deviceGeoLocation</span><span class="sxs-lookup"><span data-stu-id="2b148-101">deviceGeoLocation resource type</span></span>

> <span data-ttu-id="2b148-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2b148-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2b148-103">Ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="2b148-103">Device location</span></span>
## <a name="properties"></a><span data-ttu-id="2b148-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b148-104">Properties</span></span>
|<span data-ttu-id="2b148-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b148-105">Property</span></span>|<span data-ttu-id="2b148-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b148-106">Type</span></span>|<span data-ttu-id="2b148-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b148-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2b148-108">lastCollectedDateTime</span><span class="sxs-lookup"><span data-stu-id="2b148-108">lastCollectedDateTime</span></span>|<span data-ttu-id="2b148-109">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2b148-109">DateTimeOffset</span></span>|<span data-ttu-id="2b148-110">Hora en la que se registró la ubicación, con respecto a UTC</span><span class="sxs-lookup"><span data-stu-id="2b148-110">Time at which location was recorded, relative to UTC</span></span>|
|<span data-ttu-id="2b148-111">longitude</span><span class="sxs-lookup"><span data-stu-id="2b148-111">longitude</span></span>|<span data-ttu-id="2b148-112">Doble</span><span class="sxs-lookup"><span data-stu-id="2b148-112">Double</span></span>|<span data-ttu-id="2b148-113">Coordenadas de longitud de la ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="2b148-113">Longitude coordinate of the device's location</span></span>|
|<span data-ttu-id="2b148-114">latitude</span><span class="sxs-lookup"><span data-stu-id="2b148-114">latitude</span></span>|<span data-ttu-id="2b148-115">Doble</span><span class="sxs-lookup"><span data-stu-id="2b148-115">Double</span></span>|<span data-ttu-id="2b148-116">Coordenadas de latitud de la ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="2b148-116">Latitude coordinate of the device's location</span></span>|
|<span data-ttu-id="2b148-117">altitude</span><span class="sxs-lookup"><span data-stu-id="2b148-117">altitude</span></span>|<span data-ttu-id="2b148-118">Doble</span><span class="sxs-lookup"><span data-stu-id="2b148-118">Double</span></span>|<span data-ttu-id="2b148-119">Altitud, en metros por encima del nivel del mar</span><span class="sxs-lookup"><span data-stu-id="2b148-119">Altitude, given in meters above sea level</span></span>|
|<span data-ttu-id="2b148-120">horizontalAccuracy</span><span class="sxs-lookup"><span data-stu-id="2b148-120">horizontalAccuracy</span></span>|<span data-ttu-id="2b148-121">Doble</span><span class="sxs-lookup"><span data-stu-id="2b148-121">Double</span></span>|<span data-ttu-id="2b148-122">Precisión de longitud y latitud en metros</span><span class="sxs-lookup"><span data-stu-id="2b148-122">Accuracy of longitude and latitude in meters</span></span>|
|<span data-ttu-id="2b148-123">verticalAccuracy</span><span class="sxs-lookup"><span data-stu-id="2b148-123">verticalAccuracy</span></span>|<span data-ttu-id="2b148-124">Doble</span><span class="sxs-lookup"><span data-stu-id="2b148-124">Double</span></span>|<span data-ttu-id="2b148-125">Precisión de altitud en metros</span><span class="sxs-lookup"><span data-stu-id="2b148-125">Accuracy of altitude in meters</span></span>|
|<span data-ttu-id="2b148-126">rumbo</span><span class="sxs-lookup"><span data-stu-id="2b148-126">heading</span></span>|<span data-ttu-id="2b148-127">Doble</span><span class="sxs-lookup"><span data-stu-id="2b148-127">Double</span></span>|<span data-ttu-id="2b148-128">Rumbo en grados desde el norte geográfico</span><span class="sxs-lookup"><span data-stu-id="2b148-128">Heading in degrees from true north</span></span>|
|<span data-ttu-id="2b148-129">velocidad</span><span class="sxs-lookup"><span data-stu-id="2b148-129">speed</span></span>|<span data-ttu-id="2b148-130">Doble</span><span class="sxs-lookup"><span data-stu-id="2b148-130">Double</span></span>|<span data-ttu-id="2b148-131">La velocidad a la que se desplaza el dispositivo en metros por segundo</span><span class="sxs-lookup"><span data-stu-id="2b148-131">Speed the device is traveling in meters per second</span></span>|

## <a name="relationships"></a><span data-ttu-id="2b148-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2b148-132">Relationships</span></span>
<span data-ttu-id="2b148-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2b148-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2b148-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2b148-134">JSON Representation</span></span>
<span data-ttu-id="2b148-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2b148-135">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceGeoLocation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceGeoLocation",
  "lastCollectedDateTime": "String (timestamp)",
  "longitude": "<Unknown Primitive Type Edm.Double>",
  "latitude": "<Unknown Primitive Type Edm.Double>",
  "altitude": "<Unknown Primitive Type Edm.Double>",
  "horizontalAccuracy": "<Unknown Primitive Type Edm.Double>",
  "verticalAccuracy": "<Unknown Primitive Type Edm.Double>",
  "heading": "<Unknown Primitive Type Edm.Double>",
  "speed": "<Unknown Primitive Type Edm.Double>"
}
```


