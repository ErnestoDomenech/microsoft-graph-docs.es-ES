# <a name="message-resource-type"></a>tipo de recurso de mensaje

Un mensaje en un mailFolder.

Este recurso le permite agregar sus propios datos a las propiedades personalizadas mediante [extensiones](../../../concepts/extensibility_overview.md).


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Enumerar mensajes](../api/user_list_messages.md) |Colección [message](message.md) | Obtiene todos los mensajes del buzón del usuario que ha iniciado sesión (incluidas las carpetas Elementos eliminados y Otros correos). |
|[Crear mensaje](../api/user_post_messages.md) | [mensaje](message.md) | [Crea](../api/user_post_messages.md#request-1) un borrador de un mensaje nuevo. |
|[Obtener mensaje](../api/message_get.md) | [mensaje](message.md) |Lee las propiedades y las relaciones del objeto de mensaje.|
|[Actualizar](../api/message_update.md) | [mensaje](message.md) |Actualiza el objeto de mensaje.|
|[Eliminar](../api/message_delete.md) | Ninguno |Elimina el objeto de mensaje. |
|[copy](../api/message_copy.md)|[Mensaje](message.md)|Copia un mensaje a una carpeta.|
|[createForward](../api/message_createforward.md)|[Mensaje](message.md)|Crea un borrador del mensaje que de reenvío. Después puede [actualizar](../api/message_update.md) o [enviar](../api/message_send.md) el borrador.|
|[createReply](../api/message_createreply.md)|[Mensaje](message.md)|Crea un borrador del mensaje de respuesta. Después puede [actualizar](../api/message_update.md) o [enviar](../api/message_send.md) el borrador.|
|[createReplyAll](../api/message_createreplyall.md)|[Mensaje](message.md)|Crea un borrador del mensaje de respuesta a todos. Después puede [actualizar](../api/message_update.md) o [enviar](../api/message_send.md) el borrador.|
|[forward](../api/message_forward.md)|Ninguno|Reenvía un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[move](../api/message_move.md)|[Mensaje](message.md)|Mueve un mensaje a una carpeta. Se crea una nueva copia del mensaje en la carpeta de destino.|
|[reply](../api/message_reply.md)|Ninguno|Responde al remitente de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[replyAll](../api/message_replyall.md)|Ninguno|Responde a todos los remitentes de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[send](../api/message_send.md)|Ninguno|Envía un borrador de mensaje creado anteriormente. El mensaje se guarda en la carpeta Elementos enviados.|
|**Datos adjuntos**| | |
|[Enumerar datos adjuntos](../api/message_list_attachments.md) |Colección [attachment](attachment.md)| Obtiene todos los datos adjuntos en un mensaje.|
|[Agregar datos adjuntos](../api/message_post_attachments.md) |[Dato adjunto](attachment.md)| Agrega un dato adjunto nuevo a un mensaje publicándolo en la colección de datos adjuntos.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension_post_opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.|
|[Obtener extensión abierta](../api/opentypeextension_get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene un objeto u objetos de extensión abierta identificados por nombre o por nombre completo.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[mensaje](message.md)  |Crea una o más propiedades extendidas de valor único en un mensaje nuevo o existente.   |
|[Obtener mensaje con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_get.md)  | [mensaje](message.md) | Obtiene mensajes que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [mensaje](message.md) | Crea una o más propiedades extendidas de varios valores en un mensaje nuevo o existente.  |
|[Obtener mensaje con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_get.md)  | [mensaje](message.md) | Obtiene un mensaje que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |


## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|bccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cco: del mensaje.|
|body|[itemBody](itembody.md)|El cuerpo del mensaje. Puede mostrarse en formato de texto o HTML.|
|bodyPreview|Cadena|Los primeros 255 caracteres del cuerpo del mensaje. Se muestran en formato de texto.|
|categories|Colección string|Las categorías asociadas al mensaje.|
|ccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cc: del mensaje.|
|changeKey|Cadena|La versión del mensaje.|
|conversationId|Cadena|El identificador de la conversación a la que pertenece el correo electrónico.|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación del mensaje.|
|from|[recipient](recipient.md)|El propietario del buzón y el remitente del mensaje.|
|hasAttachments|Booleano|Indica si el mensaje tiene datos adjuntos.|
|id|Cadena|Identificador único del mensaje (tenga en cuenta que este valor puede cambiar si se mueve o se altera un mensaje)|
|importance|Cadena| La importancia del mensaje: `Low`, `Normal` y `High`.|
|inferenceClassification | String | La clasificación del mensaje para el usuario, según relevancia inferida, importancia o según una invalidación explícita. Los valores posibles son: `focused` o `other`. |
|internetMessageId |Cadena |El identificador del mensaje en el formato especificado por [RFC2822](http://www.ietf.org/rfc/rfc2822.txt). |
|isDeliveryReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|isDraft|Boolean|Indica si el mensaje es un borrador. Un mensaje es un borrador si no se ha enviado todavía.|
|isRead|Booleano|Indica si se ha leído el mensaje.|
|isReadReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora de la última modificación del mensaje.|
|parentFolderId|Cadena|El identificador único para el mailFolder principal del mensaje.|
|receivedDateTime|DateTimeOffset|La fecha y la hora en las que se recibió el mensaje.|
|replyTo|Colección [recipient](recipient.md)|Las direcciones de correo electrónico que se utilizan al responder.|
|sender|[recipient](recipient.md)|La cuenta que se utiliza realmente para generar el mensaje.|
|sentDateTime|DateTimeOffset|La fecha y la hora de envío del mensaje.|
|subject|Cadena|El asunto del mensaje.|
|toRecipients|Colección [recipient](recipient.md)|Los destinatarios Para: del mensaje.|
|uniqueBody|[itemBody](itembody.md)|La parte del cuerpo del mensaje que es única del mensaje actual. El elemento **uniqueBody** no se devuelve de manera predeterminada, pero puede recuperarse para cualquier mensaje con la consulta `?$select=uniqueBody`. Puede mostrarse en formato de texto o HTML.|
|webLink|Cadena|La dirección URL para abrir el mensaje en Outlook Web App.<br><br>Puede anexar un argumento ispopout al final de la dirección URL para cambiar cómo se muestra el mensaje. Si ispopout no está presente o se establece en 1, se muestra el mensaje en una ventana emergente. Si ispopout se establece en 0, el navegador mostrará el mensaje en el panel de revisión de Outlook Web App.<br><br>El mensaje se abrirá en el navegador si está conectado a su buzón mediante Outlook Web App. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.<br><br>Se puede obtener acceso a esta dirección URL desde un iFrame.|

**Quitar un script de la propiedad body**

El cuerpo del mensaje puede mostrarse en formato de texto o HTML. Si el cuerpo se muestra en HTML, de forma predeterminada, cualquier código HTML potencialmente peligroso (por ejemplo, JavaScript) insertado en la propiedad **body** se quitará antes de que el contenido del cuerpo se devuelva en una respuesta REST. Para obtener todo el contenido HTML original, incluya el siguiente encabezado de solicitud HTTP:
```
Prefer: outlook.allow-unsafe-html
```

**Configuración de las propiedades from y sender**

Cuando se redacta un mensaje, en la mayoría de los casos, las propiedades From y Sender representan al mismo usuario que inició sesión, a menos que alguno esté actualizado como se describe en los siguientes escenarios:

- La propiedad **from** se puede cambiar si el administrador de Exchange ha asignado los derechos **sendAs** del buzón a otros usuarios. El administrador puede realizar esta acción si selecciona **Permisos del buzón** del propietario del buzón en el Portal de administración de Azure o si usa el Centro de administración de Exchange o un cmdlet Add-ADPermission de Windows PowerShell. A continuación, puede configurar mediante programación la propiedad **from** para uno de los usuarios que tiene derechos **sendAs** de ese buzón.
- La propiedad **sender** se puede cambiar si el propietario del buzón ha delegado uno o más usuarios para que puedan enviar mensajes desde ese buzón. El propietario del buzón puede delegar en Outlook. Cuando un delegado envía un mensaje en nombre del propietario del buzón, la propiedad **sender** está establecida en la cuenta del delegado y la propiedad **from** sigue siendo el propietario del buzón. Mediante programación, puede configurar la propiedad **sender** para un usuario que tiene derechos de delegado en ese buzón.

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|attachments|Colección [attachment](attachment.md)|Los datos adjuntos [fileAttachment](fileattachment.md) y [itemAttachment](itemattachment.md) del mensaje.|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para el mensaje. Solo lectura. Admite valores NULL.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el mensaje. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el mensaje. Solo lectura. Admite valores NULL.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "attachments",
    "extensions",
    "singleValueExtendedProperties",
    "multiValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.message"
}-->

```json
{
  "bccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "body": {"@odata.type": "microsoft.graph.itemBody"},
  "bodyPreview": "string",
  "categories": ["string"],
  "ccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "changeKey": "string",
  "conversationId": "string",
  "createdDateTime": "String (timestamp)",
  "from": {"@odata.type": "microsoft.graph.recipient"},
  "hasAttachments": true,
  "id": "string (identifier)",
  "importance": "String",
  "inferenceClassification": "String",
  "internetMessageId": "String",
  "isDeliveryReceiptRequested": true,
  "isDraft": true,
  "isRead": true,
  "isReadReceiptRequested": true,
  "lastModifiedDateTime": "String (timestamp)",
  "parentFolderId": "string",
  "receivedDateTime": "String (timestamp)",
  "replyTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "sender": {"@odata.type": "microsoft.graph.recipient"},
  "sentDateTime": "String (timestamp)",
  "subject": "string",
  "toRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "uniqueBody": {"@odata.type": "microsoft.graph.itemBody"},
  "webLink": "string"
}

```

## <a name="see-also"></a>Vea también

- [Obtener configuración del buzón](../api/user_get_mailboxsettings.md) 
- [Actualizar configuración del buzón](../api/user_update_mailboxsettings.md)
- [Agregar datos personalizados a los recursos mediante extensiones](../../../concepts/extensibility_overview.md)
- [Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)](../../../concepts/extensibility_open_users.md)
- [Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)](../../../concepts/extensibility_schema_groups.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->