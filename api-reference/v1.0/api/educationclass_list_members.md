# <a name="list-members"></a><span data-ttu-id="4fa82-101">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="4fa82-101">List members</span></span>

<span data-ttu-id="4fa82-102">Recupera los profesores y alumnos de una clase.</span><span class="sxs-lookup"><span data-stu-id="4fa82-102">Retrieves the teachers and students for a class.</span></span> <span data-ttu-id="4fa82-103">Tenga en cuenta que si se usa el token delegado, los miembros solo pueden ser vistos por otros miembros de la clase.</span><span class="sxs-lookup"><span data-stu-id="4fa82-103">Note that if the delegated token is used, members can only be seen by other members of the class.</span></span>

## <a name="permissions"></a><span data-ttu-id="4fa82-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="4fa82-104">Permissions</span></span>
<span data-ttu-id="4fa82-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4fa82-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4fa82-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4fa82-107">Permission type</span></span>      | <span data-ttu-id="4fa82-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4fa82-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4fa82-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4fa82-109">Delegated (work or school account)</span></span> |  <span data-ttu-id="4fa82-110">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="4fa82-110">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="4fa82-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4fa82-111">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="4fa82-112">No admitido</span><span class="sxs-lookup"><span data-stu-id="4fa82-112">Not supported</span></span>  |
|<span data-ttu-id="4fa82-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4fa82-113">Application</span></span> | <span data-ttu-id="4fa82-114">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4fa82-114">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="4fa82-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4fa82-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/members
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4fa82-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4fa82-116">Optional query parameters</span></span>
<span data-ttu-id="4fa82-117">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4fa82-117">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4fa82-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4fa82-118">Request headers</span></span>
| <span data-ttu-id="4fa82-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fa82-119">Header</span></span>       | <span data-ttu-id="4fa82-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4fa82-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4fa82-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="4fa82-121">Authorization</span></span>  | <span data-ttu-id="4fa82-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4fa82-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4fa82-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4fa82-124">Request body</span></span>
<span data-ttu-id="4fa82-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4fa82-125">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="4fa82-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4fa82-126">Response</span></span>
<span data-ttu-id="4fa82-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4fa82-127">If successful, this method returns a `200 OK` response code and collection of [groupSettingTemplate](../resources/educationuser.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4fa82-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4fa82-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4fa82-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4fa82-129">Request</span></span>
<span data-ttu-id="4fa82-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4fa82-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_members"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/classes/11016/members
```
##### <a name="response"></a><span data-ttu-id="4fa82-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4fa82-131">Response</span></span>
<span data-ttu-id="4fa82-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4fa82-132">The following is an example of the response.</span></span> 

><span data-ttu-id="4fa82-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4fa82-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 593

{
  "value": [
    {
      "id": "13013",
      "displayName": "Ora Klein",
      "givenName": "Ora",
      "middleName": " ",
      "surname": "Klein",
      "mail": "OraK@contoso.com",
      "mobilePhone": "+1 (253) 555-0101",
      "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
      },
      "externalSource": "School of Fine Art",
      "mailingAddress": {
        "city": "Buffalo",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "NY",
        "street": "12345 Main St."
      },
      "primaryRole": "teacher",
      "externalId": "13013",
      "teacherNumber": "8802",
      "residenceAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
    },
    {
      "id": "13005",
      "displayName": "Erna Parker",
      "givenName": "Erna",
      "middleName": " ",
      "surname": "Parker",
      "mail": "ernap@contoso.com",
      "mobilePhone": "+1 (253) 555-0104",
      "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
      },
      "externalSource": "School of Fine Art",
      "mailingAddress": {
        "city": "Buffalo",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "NY",
        "street": "12345 Main St."
      },
      "primaryRole": "student",
      "externalId": "13005",
      "birthDate": "2001-01-01T00:00:00Z",
      "gender": "female",
      "grade": "9",
      "graduationYear": "2019",
      "studentNumber": "13005",
      "residenceAddress": {
        "city": "Long Beach",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Maple St."
      },
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List members",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->