# <a name="helpers-examples-that-arent-included-in-the-docs"></a>Aplicaciones auxiliares (ejemplos que no se incluyen en los documentos)

Se trata de elementos que tuve que agregar en los documentos para asegurarme de que la herramienta Markdown-Scanner podía controlar adecuadamente los documentos de gráfico.


## <a name="define-the-me-as-singleton"></a>Definir la /me como singleton

<!-- {"blockType": "request", "name": "get_current_user" } -->
```http
GET https://graph.microsoft.com/v1.0/me
```

<!-- {"blockType": "response", "@odata.type": "microsoft.graph.user", truncated: true } -->
```http
HTTP/1.1 200 OK

{
}
```


## <a name="define-drives-as-an-queryable-entityset"></a>Definir unidades como entityset consultable
<!-- {"blockType": "request", "name": "get_drive_from_id" } -->
```http
GET https://graph.microsoft.com/v1.0/drives/{drive-id}
```

<!-- {"blockType": "response", "@odata.type": "microsoft.graph.drive", truncated: true } -->
```http
HTTP/1.1 200 OK

{
}
```


## <a name="define-users-as-an-queryable-entityset"></a>Definir usuarios como entityset consultable

<!-- {"blockType": "request", "name": "get_users" } -->
```http
GET https://graph.microsoft.com/v1.0/users/{user-id}
```

<!-- {"blockType": "response", "@odata.type": "microsoft.graph.user", truncated: true } -->
```http
HTTP/1.1 200 OK

{
}
```
