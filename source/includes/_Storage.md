# Storage

## Get File

> Success Response Example

```json
  {
    "metadata": {
      "key_id": "uoPxD3tXnKHi",
      "payload": "/JGZepkwzJY++DdTd3OWNQS43lp3Y1mLyFp0ynslFHUgWF3JB0j7mo3cSbQPyK06caAf5Vn1ptmvE8G5iExH/8AUhFyDoJU85njh8yhHbTTnKX7jRkYJuuqAiqkcTLiD3/L7UhPqGhG9KLzxF9076yi93qPv/neesLA4cw1OBocGJwfgnlQ=",
      "sign": "wabBLU5yKMGN3bQETrDnsQxyc9wh6VGGyTh4nzHxN7YQcpJ6acyzwkSZ1HfgHYAxj1v5wtJhnFL5NLvYiydm1sYcrH",
      "signer_pub_key": W9JyHNLpYKPDM3Bwr87GQEjaar2n3LEDJ8PgdHZ9xgvHwkxq2stM,
    },  
    "file_id": "349447611987525633",
    "updated_at": "2017-04-12T14:32:23.000Z",
    "deleted": false,
    "thumbnail": {
        "location": "https://s.elk.co/team/workspace/file/349445385447538689/349445385978118145/352839465051357185/352839465051357185.thumbnail",
        "mime_type": "image/jpeg",
        "size": 162168,
      },
    "uploaded_chunks": [
      {
        "index": 0,
        "offset": 0,
        "size": 500000,
      },
      {
        "index": 1,
        "offset": 500000,
        "size": 500000,
      },
    ],
    "last_modified": "2017-04-12T13:59:58.000Z",
    "size": 4228777,
    "metadata_format": "crypto-container",
    "crypto_key_id": "uoPxD3tXnKHi",
    "mime_type": "image/jpeg",
    "canceled": 0,
    "revision": "349451673657147393",
    "updated_by": "pupkin",
    "location": "https://s.elk.co/team/workspace/file/349445385447538689/349445385978118145/352839465051357185/352839465051357185.file",
    "created_by": "pupkin",
    "preview": {
        "location": "https://s.elk.co/team/workspace/file/349445385447538689/349445385978118145/352839465051357185/352839465051357185.preview",
        "mime_type": "image/jpeg",
        "size": 278160,
      },
    "uploaded_size": 1751369,
    "created_at": "2017-04-12T14:00:06.000Z",
    "stream_thread_id": "349447612081897473"
  }
```

### URL

    `TEAM.WORKSPACE.STORAGE#FILE.GET`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |
| workspace_id |  String |  yes      |
| file_id      |  String |  yes      |


## Files List

> Success Response Example

```json
    {
      "files": [
        {
          "metadata": {
            "key_id": "uoPxD3tXnKHi",
            "payload": "/JGZepkwzJY++DdTd3OWNQS43lp3Y1mLyFp0ynslFHUgWF3JB0j7mo3cSbQPyK06caAf5Vn1ptmvE8G5iExH/8AUhFyDoJU85njh8yhHbTTnKX7jRkYJuuqAiqkcTLiD3/L7UhPqGhG9KLzxF9076yi93qPv/neesLA4cw1OBocGJwfgnlQ=",
            "sign": "wabBLU5yKMGN3bQETrDnsQxyc9wh6VGGyTh4nzHxN7YQcpJ6acyzwkSZ1HfgHYAxj1v5wtJhnFL5NLvYiydm1sYcrH",
            "signer_pub_key": W9JyHNLpYKPDM3Bwr87GQEjaar2n3LEDJ8PgdHZ9xgvHwkxq2stM,
          },  
          "file_id": "349447611987525633",
          "updated_at": "2017-04-12T14:32:23.000Z",
          "deleted": false,
          "thumbnail": {
              "location": "https://s.elk.co/team/workspace/file/349445385447538689/349445385978118145/352839465051357185/352839465051357185.thumbnail",
              "mime_type": "image/jpeg",
              "size": 162168,
            },
          "uploaded_chunks": [
            {
              "index": 0,
              "offset": 0,
              "size": 500000,
            },
            {
              "index": 1,
              "offset": 500000,
              "size": 500000,
            },
          ],
          "last_modified": "2017-04-12T13:59:58.000Z",
          "size": 4228777,
          "metadata_format": "crypto-container",
          "crypto_key_id": "uoPxD3tXnKHi",
          "mime_type": "image/jpeg",
          "canceled": 0,
          "revision": "349451673657147393",
          "updated_by": "pupkin",
          "location": "https://s.elk.co/team/workspace/file/349445385447538689/349445385978118145/352839465051357185/352839465051357185.file",
          "created_by": "pupkin",
          "preview": {
              "location": "https://s.elk.co/team/workspace/file/349445385447538689/349445385978118145/352839465051357185/352839465051357185.preview",
              "mime_type": "image/jpeg",
              "size": 278160,
            },
          "uploaded_size": 1751369,
          "created_at": "2017-04-12T14:00:06.000Z",
          "stream_thread_id": "349447612081897473"
        },
      ],
      "revision": "349451673657147393"
    }
```

### URL

    `TEAM.WORKSPACE.STORAGE#FILE.LIST`

### URL Params

| Parameter     |  Type   |  Required |
|---------------|---------|-----------|
| team_id       |  String |  yes      |
| workspace_id  |  String |  yes      |
| prior_file_id |  String |           |
| after_file_id |  String |           |
| limit_count   |  Int    |           |


## Get File Upload URL

> Success Response Example

```json
  {
    "url": "https://s.elk.co/team/workspace/file/349445385447538689/349445385978118145/352839465051357185/352839465051357185.file"
  }
```

### URL

    `TEAM.WORKSPACE.STORAGE#FILE.UPLOADER.GET`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |
| workspace_id |  String |  yes      |


## Delete File

> Success Response Example

```json
  {
    "revision": "349451673657147393"
  }
```

### URL

    `TEAM.WORKSPACE.STORAGE#FILE.DELETE`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |
| workspace_id |  String |  yes      |
| file_id      |  String |  yes      |
