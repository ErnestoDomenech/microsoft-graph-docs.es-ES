# <a name="add-educationuser-to-an-educationschool"></a><span data-ttu-id="ec71e-101">Agregar educationUser a un educationSchool</span><span class="sxs-lookup"><span data-stu-id="ec71e-101">Add educationUser to an educationSchool</span></span>

<span data-ttu-id="ec71e-102">Agregue un usuario a un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="ec71e-102">Add a user to a role</span></span>

## <a name="permissions"></a><span data-ttu-id="ec71e-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="ec71e-103">Permissions</span></span>
<span data-ttu-id="ec71e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ec71e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ec71e-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ec71e-106">Permission type</span></span>      | <span data-ttu-id="ec71e-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ec71e-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ec71e-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ec71e-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="ec71e-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ec71e-109">Not supported.</span></span>  |
|<span data-ttu-id="ec71e-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ec71e-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="ec71e-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ec71e-111">Not supported.</span></span>  |
|<span data-ttu-id="ec71e-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ec71e-112">Application</span></span> | <span data-ttu-id="ec71e-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ec71e-113">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ec71e-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ec71e-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/schools/{id}/users/$ref
```
## <a name="request-headers"></a><span data-ttu-id="ec71e-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ec71e-115">Request headers</span></span>
| <span data-ttu-id="ec71e-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec71e-116">Header</span></span>       | <span data-ttu-id="ec71e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ec71e-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ec71e-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="ec71e-118">Authorization</span></span>  | <span data-ttu-id="ec71e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ec71e-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ec71e-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ec71e-121">Content-Type</span></span>  | <span data-ttu-id="ec71e-122">application/json</span><span class="sxs-lookup"><span data-stu-id="ec71e-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ec71e-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ec71e-123">Request body</span></span>
<span data-ttu-id="ec71e-124">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="ec71e-124">In the request body, supply a JSON representation of an [invitation](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="ec71e-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec71e-125">Response</span></span>
<span data-ttu-id="ec71e-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec71e-126">If successful, this method returns a `204 No Content` response code and an [event](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ec71e-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec71e-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ec71e-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ec71e-128">Request</span></span>
<span data-ttu-id="ec71e-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ec71e-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationuser_from_educationschool"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/schools/<id>/users/$ref
Content-type: application/json
Content-length: 56

{
  "@odata.id":"https://graph.microsoft.com/v1.0/education/users/14008"
}
```

##### <a name="response"></a><span data-ttu-id="ec71e-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec71e-130">Response</span></span>
<span data-ttu-id="ec71e-131">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec71e-131">The following is an example of the response.</span></span> 

<!-- Add the educationClass resource to the response. -->

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->