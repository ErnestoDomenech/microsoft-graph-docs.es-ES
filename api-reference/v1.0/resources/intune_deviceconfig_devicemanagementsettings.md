# <a name="devicemanagementsettings-resource-type"></a><span data-ttu-id="0fac7-101">Tipo de recurso deviceManagementSettings</span><span class="sxs-lookup"><span data-stu-id="0fac7-101">deviceManagementSettings resource type</span></span>

> <span data-ttu-id="0fac7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0fac7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0fac7-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0fac7-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="0fac7-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0fac7-104">Properties</span></span>
|<span data-ttu-id="0fac7-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0fac7-105">Property</span></span>|<span data-ttu-id="0fac7-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="0fac7-106">Type</span></span>|<span data-ttu-id="0fac7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fac7-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0fac7-108">deviceComplianceCheckinThresholdDays</span><span class="sxs-lookup"><span data-stu-id="0fac7-108">deviceComplianceCheckinThresholdDays</span></span>|<span data-ttu-id="0fac7-109">Int32</span><span class="sxs-lookup"><span data-stu-id="0fac7-109">Int32</span></span>|<span data-ttu-id="0fac7-110">El número de días que se permite a un dispositivo continuar sin registrarse para seguir siendo compatible.</span><span class="sxs-lookup"><span data-stu-id="0fac7-110">The number of days a device is allowed to go without checking in to remain compliant.</span></span> <span data-ttu-id="0fac7-111">Valores válidos de 0 a 120</span><span class="sxs-lookup"><span data-stu-id="0fac7-111">Valid values 0 to 120</span></span>|
|<span data-ttu-id="0fac7-112">isScheduledActionEnabled</span><span class="sxs-lookup"><span data-stu-id="0fac7-112">isScheduledActionEnabled</span></span>|<span data-ttu-id="0fac7-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="0fac7-113">Boolean</span></span>|<span data-ttu-id="0fac7-114">Es la característica que está o no habilitada para la acción programada para la regla.</span><span class="sxs-lookup"><span data-stu-id="0fac7-114">Is feature enabled or not for scheduled action for rule.</span></span>|
|<span data-ttu-id="0fac7-115">secureByDefault</span><span class="sxs-lookup"><span data-stu-id="0fac7-115">secureByDefault</span></span>|<span data-ttu-id="0fac7-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="0fac7-116">Boolean</span></span>|<span data-ttu-id="0fac7-117">Cuando es true, el dispositivo debe ser no compatible cuando no hay ninguna directiva de cumplimiento dirigida</span><span class="sxs-lookup"><span data-stu-id="0fac7-117">Device should be noncompliant when there is no compliance policy targeted when this is true</span></span>|

## <a name="relationships"></a><span data-ttu-id="0fac7-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0fac7-118">Relationships</span></span>
<span data-ttu-id="0fac7-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0fac7-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0fac7-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0fac7-120">JSON Representation</span></span>
<span data-ttu-id="0fac7-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0fac7-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementSettings",
  "deviceComplianceCheckinThresholdDays": 1024,
  "isScheduledActionEnabled": true,
  "secureByDefault": true
}
```


