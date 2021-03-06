# <a name="get-user-mailbox-settings"></a>Obtener configuración del buzón del usuario

Obtener el objeto [mailboxSettings](../resources/mailboxsettings.md) del usuario. Esto incluye la configuración de las respuestas automáticas (avisar a los usuarios de forma automática tras la recepción de su correo electrónico), configuración regional (idioma y país o región) y zona horaria.

Puede ver toda la configuración del buzón u obtener una configuración específica.

La zona horaria es una de las opciones preferidas que puede configurar un usuario para su buzón. Los formatos de zona horaria válidos son el formato Windows y la [zona horaria de la autoridad de asignación de números de Internet (IANA)](http://www.iana.org/time-zones), también conocida como “zona horaria Olson”. El formato Windows es el predeterminado. 

Cuando se obtiene la zona horaria preferida de un usuario, esta se devuelve en el formato en el que se configuró. Si quiere que esa zona horaria se muestre en un formato específico (Windows o IANA), puede [actualizar primero la zona horaria preferida en ese formato como opción de configuración del buzón](user_update_mailboxsettings.md). Posteriormente, podrá obtener la zona horaria en ese formato. Como alternativa, puede administrar la conversión de formato por separado en la aplicación.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | MailboxSettings.Read, MailboxSettings.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | MailboxSettings.Read, MailboxSettings.ReadWrite    |
|Aplicación | MailboxSettings.Read, MailboxSettings.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
Para obtener toda la configuración del buzón, que incluye la configuración de las respuestas automáticas:
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailboxSettings
GET /users/{id|userPrincipalName}/mailboxSettings
```

Para obtener una configuración específica (por ejemplo, solo la configuración de las respuestas automáticas, la configuración regional o la zona horaria):
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailboxSettings/automaticRepliesSetting
GET /users/{id|userPrincipalName}/mailboxSettings/automaticRepliesSetting

GET /me/mailboxSettings/language
GET /users/{id|userPrincipalName}/mailboxSettings/language

GET /me/mailboxSettings/timeZone
GET /users/{id|userPrincipalName}/mailboxSettings/timeZone
```
## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y uno de los siguientes objetos solicitados en el cuerpo de la respuesta:

- Objeto [mailboxSettings](../resources/mailboxsettings.md)
- Objeto [automaticRepliesSetting](../resources/automaticRepliesSetting.md)
- Objeto [localeInfo](../resources/localeinfo.md)
- string (para **timeZone**)

## <a name="example"></a>Ejemplo
##### <a name="request-1"></a>Solicitud 1
El primer ejemplo obtiene toda la configuración del buzón del usuario que ha iniciado sesión, que incluye la configuración de idioma, la zona horaria y la configuración de las respuestas automáticas.
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_1"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailboxSettings
```
##### <a name="response-1"></a>Respuesta 1
La respuesta incluye toda la configuración del buzón. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailboxSettings"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/mailboxSettings",
    "automaticRepliesSetting": {
        "status": "Scheduled",
        "externalAudience": "All",
        "scheduledStartDateTime": {
            "dateTime": "2016-03-14T07:00:00.0000000",
            "timeZone": "UTC"
        },
        "scheduledEndDateTime": {
            "dateTime": "2016-03-28T07:00:00.0000000",
            "timeZone": "UTC"
        },
        "internalReplyMessage": "<html>\n<body>\n<p>I'm at our company's worldwide reunion and will respond to your message as soon as I return.<br>\n</p></body>\n</html>\n",
        "externalReplyMessage": "<html>\n<body>\n<p>I'm at the Contoso worldwide reunion and will respond to your message as soon as I return.<br>\n</p></body>\n</html>\n"
    },
    "timeZone":"UTC",
    "language":{
      "locale":"en-US",
      "displayName":"English (United States)"
    }
}
```

##### <a name="request-2"></a>Solicitud 2
El segundo ejemplo obtiene específicamente la configuración de las respuestas automáticas del buzón del usuario que ha iniciado sesión.
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_2"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailboxSettings/automaticRepliesSetting
```
##### <a name="response-2"></a>Respuesta 2
La respuesta incluye solo la configuración de las respuestas automáticas. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.automaticRepliesSetting"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/api/v1.0/$metadata#Me/mailboxSettings/automaticRepliesSetting",
    "status": "alwaysEnabled",
    "externalAudience": "None",
    "scheduledStartDateTime": {
        "dateTime": "2016-03-19T02:00:00.0000000",
        "timeZone": "UTC"
    },
    "scheduledEndDateTime": {
        "dateTime": "2016-03-20T02:00:00.0000000",
        "timeZone": "UTC"
    },
    "internalReplyMessage": "<html>\n<body>\n<p>I'm at our company's worldwide reunion and will respond to your message as soon as I return.<br>\n</p></body>\n</html>\n",
    "externalReplyMessage": "<html>\n<body>\n<p>I'm at the Contoso worldwide reunion and will respond to your message as soon as I return.<br>\n</p></body>\n</html>\n"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get mailbox settings",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->