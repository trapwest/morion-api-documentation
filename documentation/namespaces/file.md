# 📂 file

### append

`file.append(path: string, data: string)`

| Name     | Type         | Description |
| -------- | ------------ | ----------- |
| **path** | **`string`** | path        |
| **data** | **`string`** | data        |

Replaces contents of the specified file

### write

`file.write(path: string, data: string)`

| Name     | Type         | Description |
| -------- | ------------ | ----------- |
| **path** | **`string`** | path        |
| **data** | **`string`** | data        |

Replaces contents of the specified file

### read

`file.read(path: string):` <mark style="color:purple;">`string`</mark>

| Name     | Type         | Description |
| -------- | ------------ | ----------- |
| **path** | **`string`** | path        |

Returns contents of the specified file.

### exists

`file.exists(path: string):` <mark style="color:purple;">`boolean`</mark>

| Name     | Type         | Description |
| -------- | ------------ | ----------- |
| **path** | **`string`** | path        |

Returns <mark style="color:green;">`true`</mark>, if the file exists.

### create\_dir

`file.create_dir(path: string)`

| Name     | Type         | Description |
| -------- | ------------ | ----------- |
| **path** | **`string`** | path        |

Creates a directory on a specific path.

### get\_directory\_files

`file.get_directory_files(path: string):` <mark style="color:purple;">`table`</mark>

| Name     | Type         | Description |
| -------- | ------------ | ----------- |
| **path** | **`string`** | path        |

Returns a table with all files on a specific path.
