# Channel

## Subscribe Channel

> Success Response Example

```json
  {
    "synced": true,
    "revision": "349451673657147393"
  }
```

### URL

    `CHANNEL#SUBSCRIBE`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| channel   |  String |  yes      |
| revision  |  String |  yes      |


## Unsubscribe Channel

> Empty Response

### URL

    `CHANNEL#UNSUBSCRIBE`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| channel   |  String |  yes      |
