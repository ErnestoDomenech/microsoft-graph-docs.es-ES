<a id="domaindnscnamerecord-resource-type" class="xliff"></a>
# Tipo de recurso domainDnsCnameRecord

Representa un registro CNAME agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).


<a id="methods" class="xliff"></a>
## Métodos
No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.

<a id="properties" class="xliff"></a>
## Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|canonicalName|String| Nombre canónico del registro CNAME. Se usa para configurar el registro CNAME en el host DNS. |
|id|String| Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.|
|isOptional|Boolean| Si es false, el cliente debe configurar el registro CNAME en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio. No admite valores NULL |
|etiqueta|Cadena| Valor que se usa al configurar el *alias/host/name* del registro CNAME en el host DNS. |
|recordType|Cadena| Tipo de registro DNS. El valor es siempre *CName*. Clave|
|supportedService|Cadena| Servicio o función de Microsoft Online que tiene una dependencia en el registro CNAME.</br></br>Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*|
|ttl|Int32| Valor que se debe usar al configurar la propiedad de período de vida (ttl) del registro CNAME en el host DNS. No admite valores NULL |

<a id="relationships" class="xliff"></a>
## Relaciones
Ninguno


<a id="json-representation" class="xliff"></a>
## Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsCnameRecord"
}-->

```json
{
  "canonicalName": "String",
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "recordType": "String",
  "supportedService": "String",
  "ttl": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsCnameRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->