#### Posts

| Method | Endpoint | Description |
| :----: | ---- | --------------- |
| **GET** | [/posts](#get-posts-list) | Get posts list. |
| **GET** | /posts/:post_id | Get post details. |
| **POST** | /posts/:post_id | Create post. |
| **DELETE** | /posts/:post_id | Delete post. |

====

#### Get Post List
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
