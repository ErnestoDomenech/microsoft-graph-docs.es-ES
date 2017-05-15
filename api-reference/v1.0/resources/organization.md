# <a name="organization-resource-type"></a>Tipo de recurso organization

Representa un inquilino de Azure Active Directory. Solo se admiten las operaciones de lectura y actualización en los inquilinos; la creación y eliminación no son compatibles. Se hereda de [directoryObject](directoryobject.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener organización](../api/organization_get.md) | [organization](organization.md) |Lea las propiedades y las relaciones del objeto organization.|
|[Actualizar](../api/organization_update.md) | [organization](organization.md)  |Actualice el objeto organization. (Solo se pueden actualizar las propiedades **marketingNotificationMails** y **technicalNotificationMails**). |

## <a name="properties"></a>Propiedades

| Propiedad                             | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                          |
|:-------------------------------------|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| assignedPlans                        | Colección [assignedPlan](assignedplan.md)                        | La colección de planes de servicio asociados con el inquilino. No admite valores NULL.                                                                                                                                                                                                            |
| ciudad                                 | String                                                            |                                                                                                                                                                                                                                                                                      |
| companyLastDirSyncTime               | DateTimeOffset                                                    | La fecha y hora en que se ha sincronizado por última vez el inquilino con el directorio local. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'` |
| country                              | String                                                            |                                                                                                                                                                                                                                                                                      |
| countryLetterCode                    | String                                                            |                                                                                                                                                                                                                                                                                      |
| deletionTimestamp                    | DateTimeOffset                                                    | El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`                                                                                     |
| dirSyncEnabled                       | Boolean                                                           | **true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado).                        |
| displayName                          | String                                                            | El nombre para mostrar del inquilino.                                                                                                                                                                                                                                                     |
| id                                   | String                                                            | El identificador único del inquilino. Hereda de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura.                                                                                                                                                            |
| marketingNotificationEmails          | Colección String                                                 | No admite valores NULL.                                                                                                                                                                                                                                                                        |
| objectType                           | String                                                            | Una cadena que identifica el tipo de objeto. Para los inquilinos, el valor es siempre "Company".                                                                                                                                                                                                 |
| postalCode                           | String                                                            |                                                                                                                                                                                                                                                                                      |
| preferredLanguage                    | String                                                            |                                                                                                                                                                                                                                                                                      |
| provisionedPlans                     | Colección [ProvisionedPlan](provisionedplan.md)                  | No admite valores NULL.                                                                                                                                                                                                                                                                        |
| provisioningErrors                   | Colección ProvisioningError | No admite valores NULL.                                                                                                                                                                                                                                                                        |
| securityComplianceNotificationMails  | Colección String                                                 |                                                                                                                                                                                                                                                                                      |
| securityComplianceNotificationPhones | Colección String                                                 |                                                                                                                                                                                                                                                                                      |
| state                                | String                                                            |                                                                                                                                                                                                                                                                                      |
| street                               | String                                                            |                                                                                                                                                                                                                                                                                      |
| technicalNotificationMails           | Colección String                                                 | No admite valores NULL.                                                                                                                                                                                                                                                                        |
| telephoneNumber                      | String                                                            |                                                                                                                                                                                                                                                                                      |
| verifiedDomains                      | Colección [VerifiedDomain](verifieddomain.md)                    | La colección de dominios asociados a este inquilino. No admite valores NULL.                                                                                                                                                                                                                 |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.organization"
}-->

```json
{
  "assignedPlans": [{"@odata.type": "microsoft.graph.assignedPlan"}],
  "businessPhones": ["string"],
  "city": "string",
  "country": "string",
  "countryLetterCode": "string",
  "displayName": "string",
  "id": "string (identifier)",
  "marketingNotificationEmails": ["string"],
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesSyncEnabled": true,
  "postalCode": "string",
  "preferredLanguage": "string",
  "provisionedPlans": [{"@odata.type": "microsoft.graph.provisionedPlan"}],
  "securityComplianceNotificationMails": ["string"],
  "securityComplianceNotificationPhones": ["string"],
  "state": "string",
  "street": "string",
  "technicalNotificationMails": ["string"],
  "verifiedDomains": [{"@odata.type": "microsoft.graph.verifiedDomain"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "organization resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->