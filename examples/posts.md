#### Posts

| Method | Endpoint | Description |
| :----: | ---- | --------------- |
| **GET** | [/posts](#get-posts-list) | Get posts list. |
| **GET** | /posts/:post_id | Get post details. |
| **PUT** | /posts/:post_id | Update post details. |
| **POST** | /posts/:post_id | Create post. |
| **DELETE** | /posts/:post_id | Delete post. |

====

#### List posts
```
GET /posts
```

##### Response
```
Status: 200 OK
```

```json
{
    "id": 1,
    "name": "Test post 1"
},
{
    "id": 2,
    "name": "Test post 2"
}
```

====

#### Get Post
```
GET /posts/:post_id
```

##### Response

```
Status: 200 OK
```

```json
{
    "id": 1,
    "title": "Hello world!",
    "body": "This is a blog post!"
}
```

====


#### Create Post
```
POST /posts
```

##### Parameters

| Name | Type | Description |
| :----: | :----: | :---------------: |
| `title` | `string` | **Required.** Post title. |

```json
{
    "name": "Hello World."
}
```

##### Response

```
Status: 201 Created
```

```json
{
    "message": "Post Created.",
    "id": 1
}
```

====


#### Update Post
```
PUT /posts/:post_id
```

##### Parameters

| Name | Type | Description |
| :----: | :----: | :---------------: |
| `title` | `string` | **Required.** Post title. |
| `body` | `string` | **Required.** Post body. |

```json
{
    "name": "Hello World.",
    "body": "Hello, this is a blog post!"
}
```

##### Response

```
Status: 200 OK
```

```json
{
    "message": "Post Updated.",
    "id": 1
}
```

====


#### Update Post
```
DELETE /posts/:post_id
```

##### Response

```
Status: 204 No Content
```

```json
{
    "message": "Post Deleted.",
    "id": 1
}
```
