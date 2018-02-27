# <a name="add-a-student"></a><span data-ttu-id="69b83-101">Agregar un alumno</span><span class="sxs-lookup"><span data-stu-id="69b83-101">Add a student</span></span>

<span data-ttu-id="69b83-102">Agregue un miembro a una clase.</span><span class="sxs-lookup"><span data-stu-id="69b83-102">Add a member to a class.</span></span>

## <a name="permissions"></a><span data-ttu-id="69b83-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="69b83-103">Permissions</span></span>
<span data-ttu-id="69b83-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="69b83-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="69b83-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="69b83-106">Permission type</span></span>      | <span data-ttu-id="69b83-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="69b83-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="69b83-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="69b83-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="69b83-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69b83-109">Not supported.</span></span>  |
|<span data-ttu-id="69b83-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="69b83-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="69b83-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69b83-111">Not supported.</span></span>  |
|<span data-ttu-id="69b83-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="69b83-112">Application</span></span> | <span data-ttu-id="69b83-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="69b83-113">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="69b83-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="69b83-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/members/$ref
```
## <a name="request-headers"></a><span data-ttu-id="69b83-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="69b83-115">Request headers</span></span>
| <span data-ttu-id="69b83-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69b83-116">Header</span></span>       | <span data-ttu-id="69b83-117">Valor</span><span class="sxs-lookup"><span data-stu-id="69b83-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="69b83-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="69b83-118">Authorization</span></span>  | <span data-ttu-id="69b83-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="69b83-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="69b83-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="69b83-121">Content-Type</span></span>  | <span data-ttu-id="69b83-122">application/json</span><span class="sxs-lookup"><span data-stu-id="69b83-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="69b83-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="69b83-123">Request body</span></span>
<span data-ttu-id="69b83-124">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="69b83-124">In the request body, supply a JSON representation of an [invitation](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="69b83-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69b83-125">Response</span></span>
<span data-ttu-id="69b83-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69b83-126">If successful, this method returns a `204 No Content` response code and an [event](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="69b83-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="69b83-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="69b83-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="69b83-128">Request</span></span>
<span data-ttu-id="69b83-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="69b83-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationuser_from_educationclass"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/classes/11011/members/$ref
Content-type: application/json
Content-length: 56

{
  "@odata.id":"https://graph.microsoft.com/v1.0/education/users/13015"
}
```

##### <a name="response"></a><span data-ttu-id="69b83-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69b83-130">Response</span></span>
<span data-ttu-id="69b83-131">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69b83-131">The following is an example of the response.</span></span> 


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