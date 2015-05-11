
#### Comments

Blog comment's comments resource.

| Method | Endpoint | Description |
| :----: | ---- | --------------- |
| **GET** | [/comments](#list-comments) | Get comments list. |
| **GET** | [/comments/:comment_id](#get-comment) | Get comment details. |
| **POST** | [/comments/:comment_id](#create-comment) | Create comment. |
| **PUT** | [/comments/:comment_id](#update-comment) | Update comment details. |
| **DELETE** | [/comments/:comment_id](#delete-comment) | Delete comment. |

====

#### List comments
```
GET /comments
```

##### Response
```
Status: 200 OK
```

```json
{
    "id": 1,
    "author": "Alf",
    "body": "Hello! Great post!"
},
{
    "id": 2,
    "author": "Alf",
    "body": "Awesome article!"
}
```

====

#### Get comment
```
GET /comments/:comment_id
```

##### Response

```
Status: 200 OK
```

```json
{
    "id": 1,
    "author": "Alf",
    "name": "Hello! Great post!"
}
```

====


#### Create comment
```
POST /comments
```

##### Parameters

| Name | Type | Description |
| :----: | :----: | :---------------: |
| `body` | `string` | **Required.** Comment body. |

```json
{
    "body": "Hello! Great post!"
}
```

##### Response

```
Status: 201 Created
```

```json
{
    "message": "Comment Created.",
    "id": 1
}
```

====


#### Update comment
```
PUT /comments/:comment_id
```

##### Parameters

| Name | Type | Description |
| :----: | :----: | :---------------: |
| `body` | `string` | **Required.** comment body. |

```json
{
    "body": "Hello! Great post!"
}
```

##### Response

```
Status: 200 OK
```

```json
{
    "message": "Comment Updated.",
    "id": 1
}
```

====


#### Delete comment
```
DELETE /comments/:comment_id
```

##### Response

```
Status: 204 No Content
```

```json
{
    "message": "comment Deleted.",
    "id": 1
}
```
