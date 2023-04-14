# 🔗 web

### get

`web.get(url: string):` <mark style="color:purple;">`string`</mark>

| Name    | Type         | Description |
| ------- | ------------ | ----------- |
| **url** | **`string`** | url         |

Sends a GET request to the URL.

### post

`web.post(url: string, params: string, type: number)`

| Name       | Type         | Description |
| ---------- | ------------ | ----------- |
| **url**    | **`string`** | url         |
| **params** | **`string`** | params      |
| **type**   | **`number`** | type        |

Sends a POST request to the URL.

### put

`web.put(url: string, header: string, params: string)`

| Name       | Type         | Description |
| ---------- | ------------ | ----------- |
| **url**    | **`string`** | url         |
| **header** | **`string`** | header      |
| **params**   | **`string`** | params        |

Sends a PUT request to the URL.

### delete

`web.delete(url: string, params: string)`

| Name       | Type         | Description |
| ---------- | ------------ | ----------- |
| **url**    | **`string`** | url         |
| **params** | **`string`** | params      |

Sends a DELETE request to the URL.
