# <a name="user-getmembergroups"></a>usuario: getMemberGroups
Devuelva todos los grupos de los que el usuario es miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación [memberOf](../api/user_list_memberof.md), que devuelve solo los grupos de los que el usuario es miembro directo.

Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. El número máximo de grupos que puede devolver cada solicitud es de 2046. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

>**Nota:** En este momento, esta API requiere el permiso Directory.Read.All o superior. El uso del permiso Group.Read.All, bien sea de forma independiente o junto con el permiso User devolverá un error. Se trata de un problema conocido.

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | *User.Read y Group.Read.All*, *User.ReadBasic.All y Group.Read.All*, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | *Group.Read.All*, Directory.Read.All, Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/getMemberGroups
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|securityEnabledOnly|Boolean|**true** para especificar que solo se deben devolver los grupos de seguridad de los que el usuario es miembro; **false** para especificar que se deben devolver todos los grupos de los que el usuario es miembro. Nota: Establecer este parámetro en **verdadero** solo es posible al llamar este método en un usuario.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el usuario sea miembro.

## <a name="example"></a>Ejemplo
Aquí tiene un ejemplo de cómo llamar a esta API.
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "user_getmembergroups"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/getMemberGroups
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "value": [
    "string-value"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: getMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
