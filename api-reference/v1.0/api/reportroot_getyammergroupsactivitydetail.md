# <a name="reportroot-getyammergroupsactivitydetail"></a>reportRoot: getYammerGroupsActivityDetail

Obtiene información sobre la actividad de grupos de Yammer por grupo.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de grupos de Yammer](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

| Tipo de permiso                        | Permisos (de menos a más privilegiados) |
| :------------------------------------- | :--------------------------------------- |
| Delegado (cuenta profesional o educativa)     | No admitida.                           |
| Delegado (cuenta personal de Microsoft) | No admitida.                           |
| Aplicación                            | Reports.Read.All                         |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerGroupsActivityDetail(period='{period_value}')
GET /reports/getYammerGroupsActivityDetail(date={date_value})
```

## <a name="request-parameters"></a>Parámetros de la solicitud

En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.

| Parámetro | Tipo   | Descripción                              |
| :-------- | :----- | :--------------------------------------- |
| period    | cadena | Especifica la duración de tiempo durante la que se agrega el informe. Los valores admitidos para {period_value} son: D7, D30, D90 y D180. Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe. |
| date      | Fecha   | Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad. {date_value} necesita tener el formato de AAAA-MM-DD. Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo. |

> **Nota:** Necesita establecer un período o una fecha en la URL.

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre          | Descripción               |
| :------------ | :------------------------ |
| Authorization | {token} de portador. Obligatorio. |
| If-None-Match | Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`. Opcional. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe. La URL se encuentra en el encabezado `Location` de la respuesta.

Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.

El archivo CSV tiene los siguientes encabezados de columna.

- Fecha de actualización del informe
- Nombre para mostrar del grupo
- Eliminado
- Nombre principal de propietario
- Fecha de la última actividad
- Tipo de grupo
- Office 365 conectado
- Número de miembros
- Número de publicaciones
- Número de lecturas
- Número de etiquetados como “Me gusta”
- Período del informe

## <a name="example"></a>Ejemplo

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammergroupsactivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerGroupsActivityDetail(period='D7')
```

#### <a name="response"></a>Respuesta

Este es un ejemplo de la respuesta.

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Group Display Name,Is Deleted,Owner Principal Name,Last Activity Date,Group Type,Office 365 Connected,Member Count,Posted Count,Read Count,Liked Count,Report Period
```
