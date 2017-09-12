# <a name="workbookrange-columnsbefore"></a><span data-ttu-id="08fdb-101">workbookRange: columnsBefore</span><span class="sxs-lookup"><span data-stu-id="08fdb-101">workbookRange: columnsBefore</span></span>

<span data-ttu-id="08fdb-102">Obtiene un número determinado de columnas a la izquierda del rango especificado.</span><span class="sxs-lookup"><span data-stu-id="08fdb-102">Gets a certain number of columns to the left of the given range.</span></span>

## <a name="permissions"></a><span data-ttu-id="08fdb-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="08fdb-103">Permissions</span></span>
<span data-ttu-id="08fdb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="08fdb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="08fdb-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="08fdb-106">Permission type</span></span>      | <span data-ttu-id="08fdb-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="08fdb-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="08fdb-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="08fdb-108">Delegated (work or school account)</span></span> | <span data-ttu-id="08fdb-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="08fdb-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="08fdb-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="08fdb-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="08fdb-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08fdb-111">Not supported.</span></span>    |
|<span data-ttu-id="08fdb-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="08fdb-112">Application</span></span> | <span data-ttu-id="08fdb-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08fdb-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="08fdb-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="08fdb-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/columnsBefore(count=n)

```
## <a name="request-headers"></a><span data-ttu-id="08fdb-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="08fdb-115">Request headers</span></span>
| <span data-ttu-id="08fdb-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="08fdb-116">Name</span></span>       | <span data-ttu-id="08fdb-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="08fdb-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="08fdb-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="08fdb-118">Authorization</span></span>  | <span data-ttu-id="08fdb-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="08fdb-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="08fdb-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="08fdb-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="08fdb-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="08fdb-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="parameters"></a><span data-ttu-id="08fdb-124">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08fdb-124">Parameters</span></span>

| <span data-ttu-id="08fdb-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="08fdb-125">Parameter</span></span>    | <span data-ttu-id="08fdb-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="08fdb-126">Type</span></span>   |<span data-ttu-id="08fdb-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="08fdb-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="08fdb-128">count</span><span class="sxs-lookup"><span data-stu-id="08fdb-128">count</span></span>|<span data-ttu-id="08fdb-129">Int32</span><span class="sxs-lookup"><span data-stu-id="08fdb-129">Int32</span></span>|<span data-ttu-id="08fdb-p104">El número de columnas que se va a incluir en el intervalo resultante. En general, use un número positivo para crear un intervalo fuera del intervalo actual. También puede usar un número negativo para crear un intervalo dentro del intervalo actual. El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="08fdb-p104">The number of columns to include in the resulting range. In general, use a positive number to create a range outside the current range. You can also use a negative number to create a range within the current range. The default value is 1</span></span>|

## <a name="request-body"></a><span data-ttu-id="08fdb-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="08fdb-134">Request body</span></span>

### <a name="response"></a><span data-ttu-id="08fdb-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08fdb-135">Response</span></span>
<span data-ttu-id="08fdb-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08fdb-136">If successful, this method returns `200, OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="08fdb-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08fdb-137">Example</span></span>
<span data-ttu-id="08fdb-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="08fdb-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="08fdb-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="08fdb-139">Request</span></span>
<span data-ttu-id="08fdb-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08fdb-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrange_columnsbefore"
}-->
```http
POST https://graph.microsoft.com/v1.0/drive/root/workbook/worksheets/{id}/range/columnsBefore(count=2)
```

##### <a name="response"></a><span data-ttu-id="08fdb-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08fdb-141">Response</span></span>
<span data-ttu-id="08fdb-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="08fdb-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 157

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnHidden": true,
  "columnIndex": 99
}
```