# <a name="educationclass-resource-type"></a><span data-ttu-id="eea4d-101">Tipo de recurso educationClass</span><span class="sxs-lookup"><span data-stu-id="eea4d-101">educationClass resource type</span></span>

<span data-ttu-id="eea4d-102">Representa una clase en un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="eea4d-102">Represents a class within a school.</span></span> <span data-ttu-id="eea4d-103">El recurso **educationClass** corresponde al grupo de Office 365 y comparte el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="eea4d-103">The **educationClass** resource corresponds to the Office 365 group and shares the same ID.</span></span> <span data-ttu-id="eea4d-104">Los alumnos son miembros normales de la clase y los profesores son propietarios y tienen los derechos adecuados.</span><span class="sxs-lookup"><span data-stu-id="eea4d-104">Students are regular members of the class, and teachers are owners and have appropriate rights.</span></span> <span data-ttu-id="eea4d-105">Para que las experiencias de Office funcionen correctamente, los profesores deben ser miembros de las colecciones de profesores y de miembros.</span><span class="sxs-lookup"><span data-stu-id="eea4d-105">For Office experiences to work correctly, teachers must be members of both the teachers and members collections.</span></span>  


## <a name="methods"></a><span data-ttu-id="eea4d-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="eea4d-106">Methods</span></span>

| <span data-ttu-id="eea4d-107">Método</span><span class="sxs-lookup"><span data-stu-id="eea4d-107">Method</span></span>           | <span data-ttu-id="eea4d-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eea4d-108">Return Type</span></span>    |<span data-ttu-id="eea4d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="eea4d-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="eea4d-110">Obtener educationClass</span><span class="sxs-lookup"><span data-stu-id="eea4d-110">Get educationClass</span></span>](../api/educationclass_get.md) | [<span data-ttu-id="eea4d-111">educationClass</span><span class="sxs-lookup"><span data-stu-id="eea4d-111">educationClass</span></span>](educationclass.md) |<span data-ttu-id="eea4d-112">Lea las propiedades y relaciones de un objeto **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="eea4d-112">Read properties and relationships of **plannerTaskDetails** object.</span></span>|
|[<span data-ttu-id="eea4d-113">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="eea4d-113">Add member</span></span>](../api/educationclass_post_members.md) |[<span data-ttu-id="eea4d-114">educationUser</span><span class="sxs-lookup"><span data-stu-id="eea4d-114">educationUser</span></span>](educationuser.md)| <span data-ttu-id="eea4d-115">Agregue un nuevo **educationUser** en la clase publicando en la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="eea4d-115">Add a new **educationUser** for the class by posting to the members navigation property.</span></span>|
|[<span data-ttu-id="eea4d-116">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="eea4d-116">List members</span></span>](../api/educationclass_list_members.md) |<span data-ttu-id="eea4d-117">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="eea4d-117">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="eea4d-118">Obtenga una colección de objetos **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="eea4d-118">Get an **educationUser** object collection.</span></span>|
|[<span data-ttu-id="eea4d-119">Quitar alumnos</span><span class="sxs-lookup"><span data-stu-id="eea4d-119">Remove student</span></span>](../api/educationclass_delete_members.md) |[<span data-ttu-id="eea4d-120">educationUser</span><span class="sxs-lookup"><span data-stu-id="eea4d-120">educationUser</span></span>](educationuser.md)| <span data-ttu-id="eea4d-121">Quite un **educationUser** de la clase mediante la propiedad de navegación de miembros.</span><span class="sxs-lookup"><span data-stu-id="eea4d-121">Remove an **educationUser** from the class through the members navigation property.</span></span>|
|[<span data-ttu-id="eea4d-122">Enumerar centros educativos</span><span class="sxs-lookup"><span data-stu-id="eea4d-122">List schools</span></span>](../api/educationclass_list_schools.md) |<span data-ttu-id="eea4d-123">Colección [educationSchool](educationschool.md)</span><span class="sxs-lookup"><span data-stu-id="eea4d-123">[educationSchool](educationschool.md) collection</span></span>| <span data-ttu-id="eea4d-124">Obtenga una colección de objetos **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="eea4d-124">Get an **educationSchool** object collection.</span></span>|
|[<span data-ttu-id="eea4d-125">Agregar profesor</span><span class="sxs-lookup"><span data-stu-id="eea4d-125">Add teacher</span></span>](../api/educationclass_post_teachers.md) |[<span data-ttu-id="eea4d-126">educationUser</span><span class="sxs-lookup"><span data-stu-id="eea4d-126">educationUser</span></span>](educationuser.md)| <span data-ttu-id="eea4d-127">Agregue un nuevo **educationUser** en la clase publicando en la propiedad de navegación de profesores.</span><span class="sxs-lookup"><span data-stu-id="eea4d-127">Add a new **educationUser** for the class by posting to the teachers navigation property.</span></span>|
|[<span data-ttu-id="eea4d-128">Enumerar profesores</span><span class="sxs-lookup"><span data-stu-id="eea4d-128">List teachers</span></span>](../api/educationclass_list_teachers.md) |<span data-ttu-id="eea4d-129">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="eea4d-129">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="eea4d-130">Obtenga una lista de los profesores de la clase.</span><span class="sxs-lookup"><span data-stu-id="eea4d-130">Get a list of teachers for the class.</span></span>|
|[<span data-ttu-id="eea4d-131">Quitar profesor</span><span class="sxs-lookup"><span data-stu-id="eea4d-131">Remove teacher</span></span>](../api/educationclass_delete_teachers.md) |[<span data-ttu-id="eea4d-132">educationUser</span><span class="sxs-lookup"><span data-stu-id="eea4d-132">educationUser</span></span>](educationuser.md)| <span data-ttu-id="eea4d-133">Quite un **educationUser** de la clase mediante la propiedad de navegación de profesores.</span><span class="sxs-lookup"><span data-stu-id="eea4d-133">Remove an **educationUser** from the class through the teachers navigation property.</span></span>|
|[<span data-ttu-id="eea4d-134">Obtener grupo</span><span class="sxs-lookup"><span data-stu-id="eea4d-134">Get group</span></span>](../api/educationclass_get_group.md) |[<span data-ttu-id="eea4d-135">group</span><span class="sxs-lookup"><span data-stu-id="eea4d-135">group</span></span>](group.md)| <span data-ttu-id="eea4d-136">Obtenga el **group** de Office 365 correspondiente a este objeto **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="eea4d-136">Get the Office 365 **group** that corresponds to this **educationClass**.</span></span>|
|[<span data-ttu-id="eea4d-137">Actualizar</span><span class="sxs-lookup"><span data-stu-id="eea4d-137">Update</span></span>](../api/educationclass_update.md) | [<span data-ttu-id="eea4d-138">educationClass</span><span class="sxs-lookup"><span data-stu-id="eea4d-138">educationClass</span></span>](educationclass.md)    |<span data-ttu-id="eea4d-139">Actualice un objeto **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="eea4d-139">Update **educationClass** object.</span></span> |
|[<span data-ttu-id="eea4d-140">Eliminar</span><span class="sxs-lookup"><span data-stu-id="eea4d-140">Delete</span></span>](../api/educationclass_delete.md) | <span data-ttu-id="eea4d-141">Ninguno</span><span class="sxs-lookup"><span data-stu-id="eea4d-141">None</span></span> |<span data-ttu-id="eea4d-142">Elimine un objeto **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="eea4d-142">Delete **educationClass** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="eea4d-143">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eea4d-143">Properties</span></span>
| <span data-ttu-id="eea4d-144">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eea4d-144">Property</span></span>     | <span data-ttu-id="eea4d-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="eea4d-145">Type</span></span>   |<span data-ttu-id="eea4d-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="eea4d-146">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="eea4d-147">id</span><span class="sxs-lookup"><span data-stu-id="eea4d-147">id</span></span>| <span data-ttu-id="eea4d-148">String</span><span class="sxs-lookup"><span data-stu-id="eea4d-148">String</span></span>| <span data-ttu-id="eea4d-149">Identificador único de la clase</span><span class="sxs-lookup"><span data-stu-id="eea4d-149">Unique identifier for the identity.</span></span>|
|<span data-ttu-id="eea4d-150">description</span><span class="sxs-lookup"><span data-stu-id="eea4d-150">description</span></span>|<span data-ttu-id="eea4d-151">String</span><span class="sxs-lookup"><span data-stu-id="eea4d-151">String</span></span>| <span data-ttu-id="eea4d-152">Descripción de la clase</span><span class="sxs-lookup"><span data-stu-id="eea4d-152">Description of the template.</span></span>|
|<span data-ttu-id="eea4d-153">displayName</span><span class="sxs-lookup"><span data-stu-id="eea4d-153">displayName</span></span>|<span data-ttu-id="eea4d-154">String</span><span class="sxs-lookup"><span data-stu-id="eea4d-154">String</span></span>| <span data-ttu-id="eea4d-155">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="eea4d-155">Name of the class.</span></span>|
|<span data-ttu-id="eea4d-156">mailNickname</span><span class="sxs-lookup"><span data-stu-id="eea4d-156">mailNickname</span></span>|<span data-ttu-id="eea4d-157">String</span><span class="sxs-lookup"><span data-stu-id="eea4d-157">String</span></span>| <span data-ttu-id="eea4d-158">Nombre de correo para enviar correo electrónico a todos los miembros, si esta opción está habilitada.</span><span class="sxs-lookup"><span data-stu-id="eea4d-158">Mail name for sending email to all members, if this is enabled.</span></span> |
|<span data-ttu-id="eea4d-159">createdBy</span><span class="sxs-lookup"><span data-stu-id="eea4d-159">createdBy</span></span>|[<span data-ttu-id="eea4d-160">identitySet</span><span class="sxs-lookup"><span data-stu-id="eea4d-160">identitySet</span></span>](identityset.md)| <span data-ttu-id="eea4d-161">Entidad que ha creado la clase.</span><span class="sxs-lookup"><span data-stu-id="eea4d-161">Entity who created the class</span></span> |
|<span data-ttu-id="eea4d-162">classCode</span><span class="sxs-lookup"><span data-stu-id="eea4d-162">classCode</span></span>|<span data-ttu-id="eea4d-163">String</span><span class="sxs-lookup"><span data-stu-id="eea4d-163">String</span></span>| <span data-ttu-id="eea4d-164">Código de clase que usa el centro educativo para identificar la clase.</span><span class="sxs-lookup"><span data-stu-id="eea4d-164">Class code used by the school to identify the class.</span></span>|
|<span data-ttu-id="eea4d-165">externalId</span><span class="sxs-lookup"><span data-stu-id="eea4d-165">externalId</span></span>|<span data-ttu-id="eea4d-166">String</span><span class="sxs-lookup"><span data-stu-id="eea4d-166">String</span></span>| <span data-ttu-id="eea4d-167">Identificador de la clase en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="eea4d-167">ID of the class from the syncing system.</span></span> |
|<span data-ttu-id="eea4d-168">externalName</span><span class="sxs-lookup"><span data-stu-id="eea4d-168">externalName</span></span>|<span data-ttu-id="eea4d-169">String</span><span class="sxs-lookup"><span data-stu-id="eea4d-169">String</span></span>|<span data-ttu-id="eea4d-170">Nombre de la clase en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="eea4d-170">Name of the class in the syncing system.</span></span>|
|<span data-ttu-id="eea4d-171">externalSource</span><span class="sxs-lookup"><span data-stu-id="eea4d-171">externalSource</span></span>|<span data-ttu-id="eea4d-172">string</span><span class="sxs-lookup"><span data-stu-id="eea4d-172">string</span></span>| <span data-ttu-id="eea4d-173">Forma en que se ha creado la clase.</span><span class="sxs-lookup"><span data-stu-id="eea4d-173">How this class was created.</span></span> <span data-ttu-id="eea4d-174">Los valores posibles son: `sis`, `manual` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="eea4d-174">Possible values are: `sis`, `manual`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="eea4d-175">term</span><span class="sxs-lookup"><span data-stu-id="eea4d-175">Term.</span></span>|[<span data-ttu-id="eea4d-176">educationTerm</span><span class="sxs-lookup"><span data-stu-id="eea4d-176">educationTerm</span></span>](educationterm.md)|<span data-ttu-id="eea4d-177">Período de la clase.</span><span class="sxs-lookup"><span data-stu-id="eea4d-177">Term for this class.</span></span>|


## <a name="relationships"></a><span data-ttu-id="eea4d-178">Relaciones</span><span class="sxs-lookup"><span data-stu-id="eea4d-178">Relationships</span></span>
| <span data-ttu-id="eea4d-179">Relación</span><span class="sxs-lookup"><span data-stu-id="eea4d-179">Relationship</span></span> | <span data-ttu-id="eea4d-180">Tipo</span><span class="sxs-lookup"><span data-stu-id="eea4d-180">Type</span></span>   |<span data-ttu-id="eea4d-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="eea4d-181">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="eea4d-182">members</span><span class="sxs-lookup"><span data-stu-id="eea4d-182">members</span></span>|<span data-ttu-id="eea4d-183">Colección [educationUser](../resources/educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="eea4d-183">[educationUser](../resources/educationuser.md) collection</span></span>| <span data-ttu-id="eea4d-184">Todos los usuarios de la clase.</span><span class="sxs-lookup"><span data-stu-id="eea4d-184">All users in the class.</span></span> <span data-ttu-id="eea4d-185">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="eea4d-185">Nullable.</span></span>|
|<span data-ttu-id="eea4d-186">schools</span><span class="sxs-lookup"><span data-stu-id="eea4d-186">schools</span></span>|<span data-ttu-id="eea4d-187">Colección [educationSchool](../resources/educationschool.md)</span><span class="sxs-lookup"><span data-stu-id="eea4d-187">[educationSchool](../resources/educationschool.md) collection</span></span>| <span data-ttu-id="eea4d-188">Todos los centros educativos a los que está asociada la clase.</span><span class="sxs-lookup"><span data-stu-id="eea4d-188">All schools that this class is associated with.</span></span> <span data-ttu-id="eea4d-189">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="eea4d-189">Nullable.</span></span>|
|<span data-ttu-id="eea4d-190">teachers</span><span class="sxs-lookup"><span data-stu-id="eea4d-190">teachers</span></span>|<span data-ttu-id="eea4d-191">Colección [educationUser](../resources/educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="eea4d-191">[educationUser](../resources/educationuser.md) collection</span></span>|  <span data-ttu-id="eea4d-192">Todos los profesores de la clase.</span><span class="sxs-lookup"><span data-stu-id="eea4d-192">All teachers in the class.</span></span> <span data-ttu-id="eea4d-193">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="eea4d-193">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="eea4d-194">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="eea4d-194">JSON representation</span></span>

<span data-ttu-id="eea4d-195">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="eea4d-195">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationClass"
}-->

```json
{
  "id": "String",
  "description": "String",
  "classCode": "String",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "displayName": "String",
  "externalId": "String",
  "externalName": "String",
  "externalSource": "string",
  "mailNickname": "String",
  "term": {"@odata.type": "microsoft.graph.education.term"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationClass resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->