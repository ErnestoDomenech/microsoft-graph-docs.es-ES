# <a name="deviceexchangeaccessstatesummary-resource-type"></a><span data-ttu-id="a17e6-101">Tipo de recurso deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="a17e6-101">deviceExchangeAccessStateSummary resource type</span></span>

> <span data-ttu-id="a17e6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a17e6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a17e6-103">Resumen del estado de acceso del dispositivo a Exchange</span><span class="sxs-lookup"><span data-stu-id="a17e6-103">Device Exchange Access State summary</span></span>
## <a name="properties"></a><span data-ttu-id="a17e6-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a17e6-104">Properties</span></span>
|<span data-ttu-id="a17e6-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a17e6-105">Property</span></span>|<span data-ttu-id="a17e6-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a17e6-106">Type</span></span>|<span data-ttu-id="a17e6-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a17e6-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a17e6-108">allowedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a17e6-108">allowedDeviceCount</span></span>|<span data-ttu-id="a17e6-109">Int32</span><span class="sxs-lookup"><span data-stu-id="a17e6-109">Int32</span></span>|<span data-ttu-id="a17e6-110">Número total de dispositivos con el estado de acceso de Exchange: Permitido.</span><span class="sxs-lookup"><span data-stu-id="a17e6-110">Total count of devices with Exchange Access State: Allowed.</span></span>|
|<span data-ttu-id="a17e6-111">blockedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a17e6-111">blockedDeviceCount</span></span>|<span data-ttu-id="a17e6-112">Int32</span><span class="sxs-lookup"><span data-stu-id="a17e6-112">Int32</span></span>|<span data-ttu-id="a17e6-113">Número total de dispositivos con el estado de acceso de Exchange: Bloqueado.</span><span class="sxs-lookup"><span data-stu-id="a17e6-113">Total count of devices with Exchange Access State: Blocked.</span></span>|
|<span data-ttu-id="a17e6-114">quarantinedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a17e6-114">quarantinedDeviceCount</span></span>|<span data-ttu-id="a17e6-115">Int32</span><span class="sxs-lookup"><span data-stu-id="a17e6-115">Int32</span></span>|<span data-ttu-id="a17e6-116">Número total de dispositivos con el estado de acceso de Exchange: En cuarentena.</span><span class="sxs-lookup"><span data-stu-id="a17e6-116">Total count of devices with Exchange Access State: Quarantined.</span></span>|
|<span data-ttu-id="a17e6-117">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a17e6-117">unknownDeviceCount</span></span>|<span data-ttu-id="a17e6-118">Int32</span><span class="sxs-lookup"><span data-stu-id="a17e6-118">Int32</span></span>|<span data-ttu-id="a17e6-119">Número total de dispositivos con el estado de acceso de Exchange: Desconocido.</span><span class="sxs-lookup"><span data-stu-id="a17e6-119">Total count of devices with Exchange Access State: Unknown.</span></span>|
|<span data-ttu-id="a17e6-120">unavailableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a17e6-120">unavailableDeviceCount</span></span>|<span data-ttu-id="a17e6-121">Int32</span><span class="sxs-lookup"><span data-stu-id="a17e6-121">Int32</span></span>|<span data-ttu-id="a17e6-122">Número total de dispositivos para los que no se puede encontrar el estado de acceso de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a17e6-122">Total count of devices for which no Exchange Access State could be found.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a17e6-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a17e6-123">Relationships</span></span>
<span data-ttu-id="a17e6-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a17e6-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a17e6-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a17e6-125">JSON Representation</span></span>
<span data-ttu-id="a17e6-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a17e6-126">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceExchangeAccessStateSummary",
  "allowedDeviceCount": 1024,
  "blockedDeviceCount": 1024,
  "quarantinedDeviceCount": 1024,
  "unknownDeviceCount": 1024,
  "unavailableDeviceCount": 1024
}
```


