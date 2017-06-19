# <a name="notebook-resource-type"></a>Tipo de recurso notebook

Bloc de notas de OneNote.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "sectionGroups",
    "sections"
  ],
  "@odata.type": "microsoft.graph.notebook"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "isDefault": true,
  "isShared": true,
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "links": {"@odata.type": "microsoft.graph.notebookLinks"},
  "displayName": "string",
  "sectionGroupsUrl": "string",
  "sectionsUrl": "string",
  "self": "string",
  "userRole": "String"
}

```
## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|createdBy|[identitySet](identityset.md)|Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.|
|createdDateTime|DateTimeOffset|La fecha y la hora en que se creó el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|id|String|El identificador único del bloc de notas. Solo lectura.|
|isDefault|Booleano|Indica si se trata del bloc de notas predeterminado del usuario. Solo lectura.|
|isShared|Booleano|Indica si se comparte el bloc de notas. Si es true, además del propietario, otros usuarios pueden ver el contenido del bloc de notas. Solo lectura.|
|lastModifiedBy|[identitySet](identityset.md)|Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora en que se modificó por última vez el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|links|[NotebookLinks](notebooklinks.md)|Vínculos para abrir el bloc de notas. El vínculo `oneNoteClientURL` abre el bloc de notas en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebURL` abre el bloc de notas en OneNote Online.|
|displayName|String|El nombre del bloc de notas.|
|sectionGroupsUrl|String|La dirección URL de la propiedad de navegación `sectionGroups`, que devuelve todos los grupos de secciones del bloc de notas. Solo lectura.|
|sectionsUrl|String|La dirección URL de la propiedad de navegación `sections`, que devuelve todas las secciones del bloc de notas. Solo lectura.|
|self|String|El punto de conexión donde puede obtener información detallada sobre el bloc de notas. Solo lectura.|
|userRole|String|Los valores posibles son `Owner`, `Contributor`, `Reader` y `None`. Owner representa el acceso de nivel de propietario al bloc de notas. Contributor representa el acceso de lectura/escritura al bloc de notas. Reader representa el acceso de solo lectura al bloc de notas. Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|sectionGroups|Colección [SectionGroup](sectiongroup.md)|Los grupos de secciones del bloc de notas. Solo lectura. Admite valores NULL.|
|sections|Colección [Section](section.md)|Secciones del bloc de notas. Solo lectura. Admite valores NULL.|

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener bloc de notas](../api/notebook_get.md) | [Notebook](notebook.md) |Leer las propiedades y las relaciones del bloc de notas.|
|[Crear grupo de secciones](../api/notebook_post_sectiongroups.md) |[SectionGroup](sectiongroup.md)| Crear un grupo de secciones publicándolo en el bloc de notas especificado de la colección sectionGroups.|
|[Enumerar grupos de secciones](../api/notebook_list_sectiongroups.md) |Colección [SectionGroup](sectiongroup.md)| Obtener una colección de grupos de secciones en el bloc de notas especificado.|
|[Crear sección](../api/notebook_post_sections.md) |[Section](section.md)| Crear una sección publicándola en el bloc de notas especificado de la colección de secciones.|
|[Enumerar secciones](../api/notebook_list_sections.md) |Colección [Section](section.md)| Obtener una colección de secciones en el bloc de notas especificado.|
|[copyNotebook](../api/notebook_copynotebook.md)| Ninguno | Copia un bloc de notas.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notebook resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->