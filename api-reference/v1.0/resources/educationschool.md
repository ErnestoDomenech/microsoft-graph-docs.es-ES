# <a name="educationschool-resource-type"></a><span data-ttu-id="c9a0a-101">Tipo de recurso educationSchool</span><span class="sxs-lookup"><span data-stu-id="c9a0a-101">educationSchool resource type</span></span>

<span data-ttu-id="c9a0a-102">Centro educativo.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-102">A school.</span></span> <span data-ttu-id="c9a0a-103">El recurso **educationSchool** actualmente corresponde a un recurso [administrativeUnit](../../beta/resources/administrativeunit.md) y comparte el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-103">The **educationSchool** resource currently corresponds to an [administrativeUnit](../../beta/resources/administrativeunit.md) resource and shares the same ID.</span></span>  

><span data-ttu-id="c9a0a-104">**Nota:** Los recursos la **administrativeUnit** y **educationOrganization** se encuentran actualmente en versión beta.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-104">**Note:**  The **administrativeUnit** and **educationOrganization** resources are currently in beta.</span></span> <span data-ttu-id="c9a0a-105">Si usa estos recursos, asegúrese de revisar el [registro de cambios](../../../concepts/changelog.md) periódicamente.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-105">If you're using these resources, be sure to review the [Changelog](../../../concepts/changelog.md) periodically.</span></span> <span data-ttu-id="c9a0a-106">Al publicar recursos de la API de Microsoft Graph en el punto de conexión /v1.0, se indica la versión en el registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-106">When Microsoft Graph API resources are released to the v1.0  endpoint, we'll note this in the Changelog.</span></span> <span data-ttu-id="c9a0a-107">Si la aplicación usa los recursos **administrativeUnit** o **educationOrganization**, habrá que declarar las direcciones URL de la solicitud base, tal y como se muestra en el siguiente bloque de código:</span><span class="sxs-lookup"><span data-stu-id="c9a0a-107">If your app consumes the **administrativeUnit** or **educationOrganization** resources, you will need to declare base request URLs as shown in the the following code block.</span></span>  
  ```JavaScript
  var v1BaseUrl = “https://graph.microsoft.com/v1.0/education”;
  var betaBaseUrl = “https://graph.microsoft.com/beta/education”;  // for administrativeUnit and educationOrganization
  ```

<span data-ttu-id="c9a0a-108">Este recurso es un subtipo de [educationOrganization](../../beta/resources/educationorganization.md).</span><span class="sxs-lookup"><span data-stu-id="c9a0a-108">This resource is a subtype of [educationOrganization](../../beta/resources/educationorganization.md).</span></span>


## <a name="methods"></a><span data-ttu-id="c9a0a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c9a0a-109">Methods</span></span>

| <span data-ttu-id="c9a0a-110">Método</span><span class="sxs-lookup"><span data-stu-id="c9a0a-110">Method</span></span>           | <span data-ttu-id="c9a0a-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9a0a-111">Return Type</span></span>    |<span data-ttu-id="c9a0a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9a0a-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c9a0a-113">Get</span><span class="sxs-lookup"><span data-stu-id="c9a0a-113">Get</span></span>](../api/educationschool_get.md) | [<span data-ttu-id="c9a0a-114">educationSchool</span><span class="sxs-lookup"><span data-stu-id="c9a0a-114">educationSchool</span></span>](educationschool.md) |<span data-ttu-id="c9a0a-115">Lea las propiedades y relaciones de un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-115">Read properties and relationships of **plannerTaskDetails** object.</span></span>|
|[<span data-ttu-id="c9a0a-116">Agregar clase</span><span class="sxs-lookup"><span data-stu-id="c9a0a-116">Add class</span></span>](../api/educationschool_post_classes.md) |[<span data-ttu-id="c9a0a-117">educationClass</span><span class="sxs-lookup"><span data-stu-id="c9a0a-117">educationClass</span></span>](educationclass.md)| <span data-ttu-id="c9a0a-118">Agregue un nuevo **educationClass** en el centro educativo publicando en la propiedad de navegación de clases.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-118">Add a new **educationClass** for the school by posting to the classes navigation property.</span></span>|
|[<span data-ttu-id="c9a0a-119">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="c9a0a-119">List classes</span></span>](../api/educationschool_list_classes.md) |<span data-ttu-id="c9a0a-120">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="c9a0a-120">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="c9a0a-121">Obtenga la colección de objetos **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-121">Get the **educationClass** object collection.</span></span>|
|[<span data-ttu-id="c9a0a-122">Quitar clase</span><span class="sxs-lookup"><span data-stu-id="c9a0a-122">Remove class</span></span>](../api/educationschool_delete_classes.md) |[<span data-ttu-id="c9a0a-123">educationClass</span><span class="sxs-lookup"><span data-stu-id="c9a0a-123">educationClass</span></span>](educationclass.md)| <span data-ttu-id="c9a0a-124">Quite un **educationClass** del centro educativo mediante la propiedad de navegación de clases.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-124">Remove an **educationClass** from the school through the classes navigation property.</span></span>|
|[<span data-ttu-id="c9a0a-125">Agregar usuario</span><span class="sxs-lookup"><span data-stu-id="c9a0a-125">Add user</span></span>](../api/educationschool_post_users.md) |[<span data-ttu-id="c9a0a-126">educationUser</span><span class="sxs-lookup"><span data-stu-id="c9a0a-126">educationUser</span></span>](educationuser.md)| <span data-ttu-id="c9a0a-127">Agregue un nuevo **educationUser** en el centro educativo publicando en la propiedad de navegación **users**.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-127">Add a new **educationUser** for the school by posting to the **users** navigation property.</span></span>|
|[<span data-ttu-id="c9a0a-128">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="c9a0a-128">List users</span></span>](../api/educationschool_list_users.md) |<span data-ttu-id="c9a0a-129">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="c9a0a-129">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="c9a0a-130">Obtenga la colección de objetos **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-130">Get the **educationUser** object collection.</span></span>|
|[<span data-ttu-id="c9a0a-131">Quitar usuario</span><span class="sxs-lookup"><span data-stu-id="c9a0a-131">Remove user</span></span>](../api/educationschool_delete_users.md) |[<span data-ttu-id="c9a0a-132">educationUser</span><span class="sxs-lookup"><span data-stu-id="c9a0a-132">educationUser</span></span>](educationuser.md)| <span data-ttu-id="c9a0a-133">Quite un **educationUser** del centro educativo mediante la propiedad de navegación **users**.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-133">Remove an **educationUser** from the school through the **users** navigation property.</span></span>|
|[<span data-ttu-id="c9a0a-134">Obtener administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="c9a0a-134">Get administrativeUnit</span></span>](../api/educationschool_get_administrativeunit.md) |[<span data-ttu-id="c9a0a-135">administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="c9a0a-135">administrativeUnit</span></span>](../../beta/resources/administrativeunit.md)| <span data-ttu-id="c9a0a-136">Obtenga el directorio simple **administrativeUnit** correspondiente a este objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-136">Get the **administrativeUnit** that corresponds to this **educationSchool**.</span></span>|
|[<span data-ttu-id="c9a0a-137">Actualizar</span><span class="sxs-lookup"><span data-stu-id="c9a0a-137">Update</span></span>](../api/educationschool_update.md) | [<span data-ttu-id="c9a0a-138">educationSchool</span><span class="sxs-lookup"><span data-stu-id="c9a0a-138">educationSchool</span></span>](educationschool.md) |<span data-ttu-id="c9a0a-139">Actualice un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-139">Update an **event** object.</span></span> |
|[<span data-ttu-id="c9a0a-140">Eliminar</span><span class="sxs-lookup"><span data-stu-id="c9a0a-140">Delete</span></span>](../api/educationschool_delete.md) | <span data-ttu-id="c9a0a-141">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c9a0a-141">None</span></span> |<span data-ttu-id="c9a0a-142">Elimine un objeto **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-142">Delete an **event** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="c9a0a-143">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9a0a-143">Properties</span></span>
| <span data-ttu-id="c9a0a-144">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c9a0a-144">Property</span></span>     | <span data-ttu-id="c9a0a-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9a0a-145">Type</span></span>   |<span data-ttu-id="c9a0a-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9a0a-146">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c9a0a-147">id</span><span class="sxs-lookup"><span data-stu-id="c9a0a-147">id</span></span>|<span data-ttu-id="c9a0a-148">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-148">String</span></span>|<span data-ttu-id="c9a0a-149">GUID de este centro educativo.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-149">GUID of this school.</span></span>|
|<span data-ttu-id="c9a0a-150">displayName</span><span class="sxs-lookup"><span data-stu-id="c9a0a-150">displayName</span></span>| <span data-ttu-id="c9a0a-151">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-151">String</span></span>| <span data-ttu-id="c9a0a-152">Nombre para mostrar del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-152">Display name of the template.</span></span>| 
|<span data-ttu-id="c9a0a-153">description</span><span class="sxs-lookup"><span data-stu-id="c9a0a-153">description</span></span>| <span data-ttu-id="c9a0a-154">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-154">String</span></span> | <span data-ttu-id="c9a0a-155">Descripción del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-155">Description of the template.</span></span>| 
|<span data-ttu-id="c9a0a-156">status</span><span class="sxs-lookup"><span data-stu-id="c9a0a-156">status</span></span>| <span data-ttu-id="c9a0a-157">string</span><span class="sxs-lookup"><span data-stu-id="c9a0a-157">string</span></span>| <span data-ttu-id="c9a0a-158">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-158">Read-only.</span></span> <span data-ttu-id="c9a0a-159">Los valores posibles son: `inactive`, `active`, `expired` y `deleteable`.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-159">Possible values are: `inactive`, `active`, `expired`, `deleteable`.</span></span>|
|<span data-ttu-id="c9a0a-160">externalSource</span><span class="sxs-lookup"><span data-stu-id="c9a0a-160">externalSource</span></span>| <span data-ttu-id="c9a0a-161">string</span><span class="sxs-lookup"><span data-stu-id="c9a0a-161">string</span></span>| <span data-ttu-id="c9a0a-162">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-162">Read-only.</span></span>  <span data-ttu-id="c9a0a-163">Los valores posibles son: `sis`, `manual` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-163">Possible values are: `sis`, `manual`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="c9a0a-164">principalEmail</span><span class="sxs-lookup"><span data-stu-id="c9a0a-164">principalEmail</span></span>| <span data-ttu-id="c9a0a-165">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-165">String</span></span>| <span data-ttu-id="c9a0a-166">Dirección de correo electrónico del director.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-166">Email address of the principal.</span></span>|
|<span data-ttu-id="c9a0a-167">principalName</span><span class="sxs-lookup"><span data-stu-id="c9a0a-167">principalName</span></span>| <span data-ttu-id="c9a0a-168">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-168">String</span></span> | <span data-ttu-id="c9a0a-169">Nombre del director.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-169">Name of the principal.</span></span>|
|<span data-ttu-id="c9a0a-170">externalPrincipalId</span><span class="sxs-lookup"><span data-stu-id="c9a0a-170">externalPrincipalId</span></span>| <span data-ttu-id="c9a0a-171">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-171">String</span></span> | <span data-ttu-id="c9a0a-172">Identificador del director en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-172">ID of principal in syncing system.</span></span> |
|<span data-ttu-id="c9a0a-173">highestGrade</span><span class="sxs-lookup"><span data-stu-id="c9a0a-173">highestGrade</span></span>|<span data-ttu-id="c9a0a-174">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-174">String</span></span>| <span data-ttu-id="c9a0a-175">Curso más alto que se imparte.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-175">Highest grade taught.</span></span> |
|<span data-ttu-id="c9a0a-176">lowestGrade</span><span class="sxs-lookup"><span data-stu-id="c9a0a-176">lowestGrade</span></span>|<span data-ttu-id="c9a0a-177">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-177">String</span></span>| <span data-ttu-id="c9a0a-178">Curso más bajo que se imparte.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-178">Lowest grade taught.</span></span> |
|<span data-ttu-id="c9a0a-179">schoolNumber</span><span class="sxs-lookup"><span data-stu-id="c9a0a-179">schoolNumber</span></span>|<span data-ttu-id="c9a0a-180">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-180">String</span></span>| <span data-ttu-id="c9a0a-181">Número del centro educativo</span><span class="sxs-lookup"><span data-stu-id="c9a0a-181">School Number.</span></span>|
|<span data-ttu-id="c9a0a-182">externalId</span><span class="sxs-lookup"><span data-stu-id="c9a0a-182">externalId</span></span>|<span data-ttu-id="c9a0a-183">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-183">String</span></span>| <span data-ttu-id="c9a0a-184">Identificador del centro educativo en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-184">ID of school in syncing system.</span></span> |
|<span data-ttu-id="c9a0a-185">phone</span><span class="sxs-lookup"><span data-stu-id="c9a0a-185">Phone</span></span>|<span data-ttu-id="c9a0a-186">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-186">String</span></span>| <span data-ttu-id="c9a0a-187">Número de teléfono del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-187">Phone number of school.</span></span> |
|<span data-ttu-id="c9a0a-188">fax</span><span class="sxs-lookup"><span data-stu-id="c9a0a-188">fax</span></span>|<span data-ttu-id="c9a0a-189">String</span><span class="sxs-lookup"><span data-stu-id="c9a0a-189">String</span></span>| <span data-ttu-id="c9a0a-190">Número de fax del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-190">Fax number of school.</span></span> |
|<span data-ttu-id="c9a0a-191">address</span><span class="sxs-lookup"><span data-stu-id="c9a0a-191">address</span></span>|[<span data-ttu-id="c9a0a-192">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="c9a0a-192">physicalAddress</span></span>](physicaladdress.md)| <span data-ttu-id="c9a0a-193">Dirección del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-193">Address of the school.</span></span>|
|<span data-ttu-id="c9a0a-194">createdBy</span><span class="sxs-lookup"><span data-stu-id="c9a0a-194">createdBy</span></span>|[<span data-ttu-id="c9a0a-195">identitySet</span><span class="sxs-lookup"><span data-stu-id="c9a0a-195">identitySet</span></span>](identityset.md)|<span data-ttu-id="c9a0a-196">Entidad que ha creado el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-196">Entity who created the school.</span></span>|


## <a name="relationships"></a><span data-ttu-id="c9a0a-197">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c9a0a-197">Relationships</span></span>
| <span data-ttu-id="c9a0a-198">Relación</span><span class="sxs-lookup"><span data-stu-id="c9a0a-198">Relationship</span></span> | <span data-ttu-id="c9a0a-199">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9a0a-199">Type</span></span>   |<span data-ttu-id="c9a0a-200">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9a0a-200">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c9a0a-201">classes</span><span class="sxs-lookup"><span data-stu-id="c9a0a-201">Classes</span></span>|<span data-ttu-id="c9a0a-202">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="c9a0a-202">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="c9a0a-203">Clases impartidas en el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-203">Classes taught at the school.</span></span> <span data-ttu-id="c9a0a-204">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-204">Nullable.</span></span>|
|<span data-ttu-id="c9a0a-205">users</span><span class="sxs-lookup"><span data-stu-id="c9a0a-205">users</span></span>|<span data-ttu-id="c9a0a-206">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="c9a0a-206">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="c9a0a-207">Usuarios del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-207">Users in the school.</span></span> <span data-ttu-id="c9a0a-208">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-208">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c9a0a-209">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c9a0a-209">JSON representation</span></span>

<span data-ttu-id="c9a0a-210">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="c9a0a-210">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationSchool"
}-->

```json
{
  "id": "String",
  "displayName": "String",
  "description": "String",
  "status": "String",
  "externalSource": "String",
  "principalEmail": "String",
  "principalName": "String",
  "externalPrincipalId": "String",
  "highestGrade": "String",
  "lowestGrade": "String",
  "schoolNumber": "String",
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "externalId": "String",
  "fax": "String",
  "phone": "String",
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationSchool resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->