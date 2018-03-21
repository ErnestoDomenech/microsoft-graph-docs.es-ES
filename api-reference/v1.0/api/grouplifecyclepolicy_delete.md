# <a name="delete-grouplifecyclepolicy"></a><span data-ttu-id="15479-101">Eliminar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="15479-101">Delete groupLifecyclePolicy</span></span>

<span data-ttu-id="15479-102">Elimina un objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md)</span><span class="sxs-lookup"><span data-stu-id="15479-102">Deletes a [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="15479-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="15479-103">Permissions</span></span>

<span data-ttu-id="15479-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="15479-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="15479-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="15479-106">Permission type</span></span>      | <span data-ttu-id="15479-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="15479-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="15479-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="15479-108">Delegated (work or school account)</span></span> | <span data-ttu-id="15479-109">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="15479-109">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="15479-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="15479-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="15479-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15479-111">Not supported.</span></span>    |
|<span data-ttu-id="15479-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="15479-112">Application</span></span> | <span data-ttu-id="15479-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="15479-113">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="15479-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="15479-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groupLifecyclePolicies/{id}

```

## <a name="request-headers"></a><span data-ttu-id="15479-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="15479-115">Request headers</span></span>

| <span data-ttu-id="15479-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="15479-116">Name</span></span> | <span data-ttu-id="15479-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="15479-117">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="15479-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="15479-118">Authorization</span></span> | <span data-ttu-id="15479-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="15479-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="15479-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="15479-121">Content-Type</span></span>  | <span data-ttu-id="15479-122">application/json</span><span class="sxs-lookup"><span data-stu-id="15479-122">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="15479-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="15479-123">Request body</span></span>
<span data-ttu-id="15479-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="15479-124">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="15479-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15479-125">Response</span></span>

<span data-ttu-id="15479-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15479-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="15479-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="15479-128">Example</span></span>

##### <a name="request"></a><span data-ttu-id="15479-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="15479-129">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_grouplifecyclepolicy"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groupLifecyclePolicies/{id}
```
##### <a name="response"></a><span data-ttu-id="15479-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15479-130">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete groupLifecyclePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->