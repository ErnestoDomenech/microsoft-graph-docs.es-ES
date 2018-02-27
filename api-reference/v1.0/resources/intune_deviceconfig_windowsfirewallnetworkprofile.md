# <a name="windowsfirewallnetworkprofile-resource-type"></a><span data-ttu-id="4be60-101">Tipo de recurso windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4be60-101">windowsFirewallNetworkProfile resource type</span></span>

> <span data-ttu-id="4be60-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4be60-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4be60-103">Directivas de perfiles de firewall de Windows.</span><span class="sxs-lookup"><span data-stu-id="4be60-103">Windows Firewall Profile Policies.</span></span>
## <a name="properties"></a><span data-ttu-id="4be60-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4be60-104">Properties</span></span>
|<span data-ttu-id="4be60-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4be60-105">Property</span></span>|<span data-ttu-id="4be60-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4be60-106">Type</span></span>|<span data-ttu-id="4be60-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4be60-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4be60-108">firewallEnabled</span><span class="sxs-lookup"><span data-stu-id="4be60-108">firewallEnabled</span></span>|<span data-ttu-id="4be60-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="4be60-109">String</span></span>|<span data-ttu-id="4be60-110">Activa el firewall y el cumplimiento de seguridad avanzada. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.</span><span class="sxs-lookup"><span data-stu-id="4be60-110">Turn on the firewall and advanced security enforcement Possible values are: `notConfigured`, `blocked`, `allowed`.</span></span>|
|<span data-ttu-id="4be60-111">stealthModeBlocked</span><span class="sxs-lookup"><span data-stu-id="4be60-111">stealthModeBlocked</span></span>|<span data-ttu-id="4be60-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="4be60-112">Boolean</span></span>|<span data-ttu-id="4be60-113">Evita que el servidor funcione en modo silencioso</span><span class="sxs-lookup"><span data-stu-id="4be60-113">Prevent the server from operating in stealth mode</span></span>|
|<span data-ttu-id="4be60-114">incomingTrafficBlocked</span><span class="sxs-lookup"><span data-stu-id="4be60-114">incomingTrafficBlocked</span></span>|<span data-ttu-id="4be60-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="4be60-115">Boolean</span></span>|<span data-ttu-id="4be60-116">Configura el firewall para bloquear todo el tráfico entrante independientemente de otras opciones de configuración de directiva</span><span class="sxs-lookup"><span data-stu-id="4be60-116">Configures the firewall to block all incoming traffic regardless of other policy settings</span></span>|
|<span data-ttu-id="4be60-117">unicastResponsesToMulticastBroadcastsBlocked</span><span class="sxs-lookup"><span data-stu-id="4be60-117">unicastResponsesToMulticastBroadcastsBlocked</span></span>|<span data-ttu-id="4be60-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="4be60-118">Boolean</span></span>|<span data-ttu-id="4be60-119">Configura el firewall para bloquear las respuestas de unidifusión al tráfico de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="4be60-119">Configures the firewall to block unicast responses to multicast broadcast traffic</span></span>|
|<span data-ttu-id="4be60-120">inboundNotificationsBlocked</span><span class="sxs-lookup"><span data-stu-id="4be60-120">inboundNotificationsBlocked</span></span>|<span data-ttu-id="4be60-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="4be60-121">Boolean</span></span>|<span data-ttu-id="4be60-122">Impide que el firewall muestre notificaciones cuando se impide que una aplicación escuche en un puerto</span><span class="sxs-lookup"><span data-stu-id="4be60-122">Prevents the firewall from displaying notifications when an application is blocked from listening on a port</span></span>|
|<span data-ttu-id="4be60-123">authorizedApplicationRulesFromGroupPolicyMerged</span><span class="sxs-lookup"><span data-stu-id="4be60-123">authorizedApplicationRulesFromGroupPolicyMerged</span></span>|<span data-ttu-id="4be60-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="4be60-124">Boolean</span></span>|<span data-ttu-id="4be60-125">Configura el firewall para combinar reglas de aplicaciones autorizadas de directiva de grupo con las de almacén local en lugar de omitir las reglas del almacén local</span><span class="sxs-lookup"><span data-stu-id="4be60-125">Configures the firewall to merge authorized application rules from group policy with those from local store instead of ignoring the local store rules</span></span>|
|<span data-ttu-id="4be60-126">globalPortRulesFromGroupPolicyMerged</span><span class="sxs-lookup"><span data-stu-id="4be60-126">globalPortRulesFromGroupPolicyMerged</span></span>|<span data-ttu-id="4be60-127">Booleano</span><span class="sxs-lookup"><span data-stu-id="4be60-127">Boolean</span></span>|<span data-ttu-id="4be60-128">Configura el firewall para combinar reglas de puerto global de directiva de grupo con las de almacén local en lugar de omitir las reglas del almacén local</span><span class="sxs-lookup"><span data-stu-id="4be60-128">Configures the firewall to merge global port rules from group policy with those from local store instead of ignoring the local store rules</span></span>|
|<span data-ttu-id="4be60-129">connectionSecurityRulesFromGroupPolicyMerged</span><span class="sxs-lookup"><span data-stu-id="4be60-129">connectionSecurityRulesFromGroupPolicyMerged</span></span>|<span data-ttu-id="4be60-130">Booleano</span><span class="sxs-lookup"><span data-stu-id="4be60-130">Boolean</span></span>|<span data-ttu-id="4be60-131">Configura el firewall para combinar reglas de seguridad de la conexión de directiva de grupo con las de almacén local en lugar de omitir las reglas del almacén local</span><span class="sxs-lookup"><span data-stu-id="4be60-131">Configures the firewall to merge connection security rules from group policy with those from local store instead of ignoring the local store rules</span></span>|
|<span data-ttu-id="4be60-132">outboundConnectionsBlocked</span><span class="sxs-lookup"><span data-stu-id="4be60-132">outboundConnectionsBlocked</span></span>|<span data-ttu-id="4be60-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="4be60-133">Boolean</span></span>|<span data-ttu-id="4be60-134">Configura el firewall para que bloquee todas las conexiones salientes de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="4be60-134">Configures the firewall to block all outgoing connections by default</span></span>|
|<span data-ttu-id="4be60-135">inboundConnectionsBlocked</span><span class="sxs-lookup"><span data-stu-id="4be60-135">inboundConnectionsBlocked</span></span>|<span data-ttu-id="4be60-136">Booleano</span><span class="sxs-lookup"><span data-stu-id="4be60-136">Boolean</span></span>|<span data-ttu-id="4be60-137">Configura el firewall para que bloquee todas las conexiones entrantes de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="4be60-137">Configures the firewall to block all incoming connections by default</span></span>|
|<span data-ttu-id="4be60-138">securedPacketExemptionAllowed</span><span class="sxs-lookup"><span data-stu-id="4be60-138">securedPacketExemptionAllowed</span></span>|<span data-ttu-id="4be60-139">Booleano</span><span class="sxs-lookup"><span data-stu-id="4be60-139">Boolean</span></span>|<span data-ttu-id="4be60-140">Configura el firewall para permitir que el equipo host responda al tráfico de red no solicitado si ese tráfico se protege con IPSec, incluso cuando stealthModeBlocked se establece en true</span><span class="sxs-lookup"><span data-stu-id="4be60-140">Configures the firewall to allow the host computer to respond to unsolicited network traffic of that traffic is secured by IPSec even when stealthModeBlocked is set to true</span></span>|
|<span data-ttu-id="4be60-141">policyRulesFromGroupPolicyMerged</span><span class="sxs-lookup"><span data-stu-id="4be60-141">policyRulesFromGroupPolicyMerged</span></span>|<span data-ttu-id="4be60-142">Booleano</span><span class="sxs-lookup"><span data-stu-id="4be60-142">Boolean</span></span>|<span data-ttu-id="4be60-143">Configura el firewall para combinar directivas de regla de firewall de directiva de grupo con las de almacén local en lugar de omitir las reglas del almacén local</span><span class="sxs-lookup"><span data-stu-id="4be60-143">Configures the firewall to merge Firewall Rule policies from group policy with those from local store instead of ignoring the local store rules</span></span>|

## <a name="relationships"></a><span data-ttu-id="4be60-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4be60-144">Relationships</span></span>
<span data-ttu-id="4be60-145">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4be60-145">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4be60-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4be60-146">JSON Representation</span></span>
<span data-ttu-id="4be60-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4be60-147">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsFirewallNetworkProfile",
  "firewallEnabled": "String",
  "stealthModeBlocked": true,
  "incomingTrafficBlocked": true,
  "unicastResponsesToMulticastBroadcastsBlocked": true,
  "inboundNotificationsBlocked": true,
  "authorizedApplicationRulesFromGroupPolicyMerged": true,
  "globalPortRulesFromGroupPolicyMerged": true,
  "connectionSecurityRulesFromGroupPolicyMerged": true,
  "outboundConnectionsBlocked": true,
  "inboundConnectionsBlocked": true,
  "securedPacketExemptionAllowed": true,
  "policyRulesFromGroupPolicyMerged": true
}
```


