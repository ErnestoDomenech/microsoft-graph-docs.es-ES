# <a name="group-resource-type"></a>tipo de recurso de grupo

Representa un grupo de Active Directory de Azure que puede ser un grupo de Office 365, un grupo dinámico o un grupo de seguridad. Se hereda de [directoryObject](directoryobject.md).


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Crear grupo](../api/group_post_groups.md) | [grupo](group.md) |Crea un grupo nuevo. Puede ser un grupo, un grupo dinámico o un grupo de seguridad de Office 365.|
|[Obtener grupo](../api/group_get.md) | [grupo](group.md) |Lee las propiedades de un objeto de grupo.|
|[Enumerar grupos](../api/group_list.md) |Colección [group](group.md) |Enumera los objetos de grupo y sus propiedades.|
|[Actualizar grupo](../api/group_update.md) | [grupo](group.md) |Actualiza las propiedades de un objeto de grupo. |
|[Eliminar grupo](../api/group_delete.md) | Ninguno |Eliminar objeto de grupo. |
|[Agregar miembro](../api/group_post_members.md) |Ninguno| Agrega un usuario o grupo a este grupo publicándolo en la propiedad de navegación **members** (compatible solo con grupos de seguridad y grupos de seguridad habilitados para correo).|
|[Enumerar miembros](../api/group_list_members.md) |Colección [directoryObject](directoryobject.md)| Obtiene los usuarios y grupos que son miembros directos de este grupo desde la propiedad de navegación **members**.|
|[Eliminar miembro](../api/group_delete_members.md) | Ninguno |Elimina a un miembro de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede eliminar usuarios u otros grupos. |
|[Enumerar memberOf](../api/group_list_memberof.md) |Colección [directoryObject](directoryobject.md)| Obtiene los grupos de los que este grupo es miembro directo desde la propiedad de navegación **memberOf**.|
|[Agregar propietario](../api/group_post_owners.md) |Ninguno| Agrega un nuevo propietario al grupo publicándolo en la propiedad de navegación **owners** (compatible solo con grupos de seguridad y grupos de seguridad habilitados para correo).|
|[Enumerar propietarios](../api/group_list_owners.md) |Colección [directoryObject](directoryobject.md)| Obtiene los propietarios del grupo desde la propiedad de navegación **owners**.|
|[Eliminar propietario](../api/group_delete_owners.md) | Ninguno |Elimina a un propietario de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **owners**.|
|[checkMemberGroups](../api/group_checkmembergroups.md)|Colección string|Comprueba la pertenencia de este grupo a una lista de grupos. La función es transitiva.|
|[getMemberGroups](../api/group_getmembergroups.md)|Colección string|Devuelve todos los grupos de los que el grupo es miembro. La función es transitiva.|
|[getMemberObjects](../api/group_getmemberobjects.md)|Colección string|Devuelve todos los grupos de los que el grupo es miembro. La función es transitiva. |
|[Crear evento](../api/group_post_events.md) |[Evento](event.md)| Crea un nuevo evento publicándolo en la colección de eventos.|
|[Enumerar eventos](../api/group_list_events.md) |Colección [event](event.md)| Obtiene una colección de objetos de evento.|
|[Enumerar calendarView](../api/group_list_calendarview.md) |Colección [event](event.md)| Obtiene una colección de eventos en un margen de tiempo especificado.|
|[Crear conversación](../api/group_post_conversations.md) |[Conversación](conversation.md)| Crea una nueva conversación publicándola en la colección de conversaciones.|
|[Enumerar conversaciones](../api/group_list_conversations.md) |Colección [conversation](conversation.md)| Obtiene una colección de objetos de conversación.|
|[Enumerar hilos](../api/group_list_threads.md) |Colección [conversationThread](conversationthread.md)| Obtiene todos los hilos de un grupo.|
|[Enumerar acceptedSenders](../api/group_list_acceptedsenders.md) |Colección [directoryObject](directoryobject.md)| Obtiene una lista de usuarios o grupos que se encuentran en la lista de acceptedSenders de este grupo.|
|[Agregar acceptedSenders](../api/group_post_acceptedsenders.md) |[directoryObject](directoryobject.md)| Agrega un usuario o grupo a la colección acceptSenders.|
|[Eliminar acceptedSender](../api/group_delete_acceptedsenders.md) |[directoryObject](directoryobject.md)| Elimina a un usuario o grupo de la colección acceptedSenders.|
|[Agregar rejectedSender](../api/group_post_rejectedsenders.md) |[directoryObject](directoryobject.md)| Agrega a un nuevo usuario o grupo a la colección rejectedSenders.|
|[Enumerar rejectedSenders](../api/group_list_rejectedsenders.md) |Colección [directoryObject](directoryobject.md)| Obtiene una lista de usuarios o grupos que se encuentran en la lista de rejectedSenders de este grupo.|
|[Eliminar rejectedSender](../api/group_delete_rejectedsenders.md) |[directoryObject](directoryobject.md)| Elimina a un nuevo usuario o grupo de la colección rejectedSenders.|
|[addFavorite](../api/group_addfavorite.md)|Ninguno|Agrega el grupo a la lista de grupos favoritos del usuario actual. Compatible solo con grupos de Office 365.|
|[removeFavorite](../api/group_removefavorite.md)|Ninguno|Elimina el grupo de la lista de grupos favoritos del usuario actual. Compatible solo con grupos de Office 365.|
|[subscribeByMail](../api/group_subscribebymail.md)|Ninguno|Establece la propiedad isSubscribedByMail como **true**. Permite que el usuario actual pueda recibir conversaciones de correo electrónico. Compatible solo con grupos de Office 365.|
|[unsubscribeByMail](../api/group_unsubscribebymail.md)|Ninguno|Establece la propiedad isSubscribedByMail como **false**. Impide que el usuario actual pueda recibir conversaciones de correo electrónico. Compatible solo con grupos de Office 365.|
|[resetUnseenCount](../api/group_resetunseencount.md)|Ninguno|Restablece a 0 la unseenCount de todas las publicaciones que el usuario actual no ha visto desde su última visita. Compatible solo con grupos de Office 365.|


## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|allowExternalSenders|Boolean|El valor predeterminado es **false**. Indica si los usuarios externos a la organización pueden enviar mensajes al grupo.|
|autoSubscribeNewMembers|Booleano|El valor predeterminado es **false**. Indica si los miembros agregados al grupo se suscribirán de forma automática para recibir notificaciones por correo electrónico. Puede establecer esta propiedad en una solicitud PATCH del grupo; no la establezca en la solicitud POST inicial que crea el grupo.|
|descripción|Cadena|Una descripción opcional del grupo. |
|displayName|String|El nombre para mostrar del grupo. Esta propiedad es necesaria cuando se crea un grupo y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.|
|groupTypes|Colección string| Especifica el tipo de grupo que se va a crear. Los valores posibles son **Unified** para crear un grupo de Office 365 o **DynamicMembership** para grupos dinámicos.  Para los demás tipos de grupos, como los grupos con seguridad habilitada y los grupos de seguridad habilitados para correo electrónico, no establezca esta propiedad. Es compatible con $filter.|
|id|String|El identificador único del grupo. Heredado de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura.|
|isSubscribedByMail|Booleano|El valor predeterminado es **true**. Indica si el usuario actual está suscrito para recibir conversaciones de correo electrónico.|
|Correo|String|La dirección SMTP del grupo, por ejemplo: "serviceadmins@contoso.onmicrosoft.com". Solo lectura. Es compatible con $filter.|
|mailEnabled|Booleano|Especifica si el grupo está habilitado para correo. Si la propiedad **securityEnabled** también es **true**, el grupo es un grupo de seguridad habilitado para correo electrónico; en caso contrario, el grupo es un grupo de distribución de Microsoft Exchange.|
|mailNickname|String|El alias de correo del grupo. Esta propiedad debe especificarse al crear un grupo. Es compatible con $filter.|
|onPremisesLastSyncDateTime|DateTimeOffset|Indica la última vez que el grupo se ha sincronizado con el directorio local. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura. Es compatible con $filter.|
|onPremisesSecurityIdentifier|String|Contiene el identificador de seguridad local (SID) del grupo que se sincroniza desde un recurso local a la nube. Solo lectura. |
|onPremisesSyncEnabled|Boolean|**true** si este grupo está sincronizado desde un directorio local; **false** si este grupo se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este grupo no se ha sincronizado nunca desde un directorio local (valor predeterminado). Solo lectura. Es compatible con $filter.|
|proxyAddresses|Colección string| El operador **any** es necesario para las expresiones de filtro en las propiedades de varios valores. Solo lectura. No admite valores NULL. Es compatible con $filter. |
|securityEnabled|Boolean|Especifica si el grupo es un grupo de seguridad. Si la propiedad **mailEnabled** también es true, el grupo es un grupo de seguridad habilitado para correo electrónico; de lo contrario, es un grupo de seguridad. Debe ser **false** para grupos de Office 365. Es compatible con $filter.|
|unseenCount|Int32|Número de mensajes que el usuario actual no ha visto desde su última visita.|
|visibility|String| Especifica la visibilidad de un grupo de Office 365. Los valores posibles son: **Private**, **Public** o vacío (que se interpreta como **Public**).|

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|acceptedSenders|Colección [directoryObject](directoryobject.md)|La lista de usuarios o grupos que tienen permiso para crear publicaciones o eventos de calendario en este grupo. Si esta lista no está vacía, solo pueden publicar los usuarios o grupos enumerados en ella.|
|calendario|[calendario](calendar.md)|El calendario del grupo. Solo lectura.|
|calendarView|Colección [event](event.md)|La vista Calendario del calendario. Solo lectura.|
|conversations|Colección [conversation](conversation.md)|Las conversaciones del grupo.|
|createdOnBehalfOf|[directoryObject](directoryobject.md)| El usuario (o la aplicación) que creó el grupo. NOTA: No se establece si el usuario es un administrador. Solo lectura.|
|Unidad|[drive](drive.md)|La unidad del grupo. Solo lectura.|
|events|Colección [event](event.md)|Los eventos de calendario del grupo.|
|memberOf|Colección [directoryObject](directoryobject.md)|Grupos a los que pertenece este grupo. Métodos HTTP: GET (compatible con todos los grupos). Solo lectura. Admite valores NULL.|
|members|Colección [directoryObject](directoryobject.md)| Los usuarios y los grupos que son miembros de este grupo. Métodos HTTP: GET (compatible con todos los grupos), POST (compatible con grupos de Office 365, grupos de seguridad y los grupos de seguridad habilitados para correo), DELETE (compatible con grupos de Office 365 y grupos de seguridad). Admite valores NULL.|
|owners|Colección [directoryObject](directoryobject.md)|Los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar este objeto. Limitado a 10 propietarios. Métodos HTTP: GET (compatible con todos los grupos), POST (compatible con grupos de Office 365, grupos de seguridad y los grupos de seguridad habilitados para correo), DELETE (compatible con grupos de Office 365 y grupos de seguridad). Admite valores NULL.|
|Foto|[profilePhoto](profilephoto.md)| La foto de perfil del grupo. |
|rejectedSenders|Colección [directoryObject](directoryobject.md)|La lista de usuarios o grupos que no tienen permiso para crear publicaciones o eventos de calendario en este grupo. Admite valores NULL|
|threads|Colección [conversationThread](conversationthread.md)| Los hilos de conversación del grupo. Admite valores NULL.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "acceptedSenders",
    "appRoleAssignments",
    "calendar",
    "calendarView",
    "conversations",
    "createdOnBehalfOf",
    "drive",
    "events",
    "memberOf",
    "members",
    "owners",
    "photo",
    "rejectedSenders",
    "threads"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.group"
}-->

```json
{
  "allowExternalSenders": false,
  "autoSubscribeNewMembers": true,
  "description": "string",
  "displayName": "string",
  "groupTypes": ["string"],
  "id": "string (identifier)",
  "isSubscribedByMail": true,
  "mail": "string",
  "mailEnabled": true,
  "mailNickname": "string",
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesSecurityIdentifier": "string",
  "onPremisesSyncEnabled": true,
  "proxyAddresses": ["string"],
  "securityEnabled": true,
  "unseenCount": 1024,
  "visibility": "string",
  "acceptedSenders": [ { "@odata.type": "microsoft.graph.directoryObject"} ],
  "calendar": { "@odata.type": "microsoft.graph.calendar" },
  "calendarView": [{ "@odata.type": "microsoft.graph.event" }],
  "conversations": [ { "@odata.type": "microsoft.graph.conversation" }],
  "createdOnBehalfOf": { "@odata.type": "microsoft.graph.directoryObject" },
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "events": [ { "@odata.type": "microsoft.graph.event" }],
  "memberOf": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "members": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "owners": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "photo": { "@odata.type": "microsoft.graph.profilePhoto" },
  "rejectedSenders": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "threads": [ { "@odata.type": "microsoft.graph.conversationThread" }]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->