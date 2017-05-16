# Stream

## Get Message

> Success Response Example

```json
  {
      "auto_delete_after_read": "<null>",
      "auto_delete_at": "<null>",
      "created_at": "2017-05-03T07:32:11.000Z",
      "deleted": 0,
      "integration_id": "<null>",
      "message_id": "353203873430634497",
      "payload" :     
        {
          "key_id": "uoPxD3tXnKHi",
          "payload": "/JEKZ0Rhhpz5GMMXb8T6DxAJTRlRhDs1PvVtCLMuBSnRgBltaP1EJ/TSvlm/KNerDjvsepVaD5+8hsuLvSRSc/d3MSAqYrTfoGiN0zu0yAQeiejwI/I=",
          "sign": "wanpbkLh6T5MaXzdYMESXamq8G7mkXrzbT3Qj3JMt7FoUDUxNJAYjXx8tLadn7jR1wUkR9aYYfhEUxkZt3RX4mUmwB",
          "signer_pub_key": "W9JyHNLpYKPDM3Bwr87GQEjaar2n3LEDJ8PgdHZ9xgvHwkxq2stM",
        },
      "payload_format": "witcrypt",
      "private": false,
      "revision": "353203873430636545",
      "seen_by":     
        {
          "pupkin": "2017-05-03T07:32:11.283Z",
        },
      "sender": "pupkin",
      "sender_type": "USER",
      "thread_id": "<null>",
      "updated_at": "<null>",
      "updated_by": "<null>",
  }
```

### URL

    `TEAM.WORKSPACE.STREAM#MESSAGE.GET`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |
| workspace_id |  String |  yes      |
| message_id   |  String |  yes      |


## Messages List

> Success Response Example

```json
  {
    "messages": [
      {
        "auto_delete_after_read": "<null>",
        "auto_delete_at": "<null>",
        "created_at": "2017-05-03T07:32:11.000Z",
        "deleted": 0,
        "integration_id": "<null>",
        "message_id": "353203873430634497",
        "payload" :     
          {
            "key_id": "uoPxD3tXnKHi",
            "payload": "/JEKZ0Rhhpz5GMMXb8T6DxAJTRlRhDs1PvVtCLMuBSnRgBltaP1EJ/TSvlm/KNerDjvsepVaD5+8hsuLvSRSc/d3MSAqYrTfoGiN0zu0yAQeiejwI/I=",
            "sign": "wanpbkLh6T5MaXzdYMESXamq8G7mkXrzbT3Qj3JMt7FoUDUxNJAYjXx8tLadn7jR1wUkR9aYYfhEUxkZt3RX4mUmwB",
            "signer_pub_key": "W9JyHNLpYKPDM3Bwr87GQEjaar2n3LEDJ8PgdHZ9xgvHwkxq2stM",
          },
        "payload_format": "witcrypt",
        "private": false,
        "revision": "353203873430636545",
        "seen_by":     
          {
            "pupkin": "2017-05-03T07:32:11.283Z",
          },
        "sender": "pupkin",
        "sender_type": "USER",
        "thread_id": "<null>",
        "updated_at": "<null>",
        "updated_by": "<null>",
      },
    ],
    "revision": "353203873430636545",
  }
```

### URL

    `TEAM.WORKSPACE.STREAM#MESSAGE.LIST`

### URL Params

| Parameter        |  Type   |  Required |
|------------------|---------|-----------|
| team_id          |  String |  yes      |
| workspace_id     |  String |  yes      |
| thread_id        |  String |           |
| prior_message_id |  String |           |
| after_message_id |  String |           |
| limit_count      |  Int    |           |


## Send Message

> Success Response Example

```json
  {
    "message_id": "353203873430634497",
    "revision": "353203873430636545"
  }
```

### URL

    `TEAM.WORKSPACE.STREAM#MESSAGE.SEND`

### URL Params

| Parameter      |  Type                                                                    |  Required |
|----------------|--------------------------------------------------------------------------|-----------|
| team_id        |  String                                                                  |  yes      |
| workspace_id   |  String                                                                  |  yes      |
| sender         |  String                                                                  |  yes      |
| seen_by        |  Array[[SeenBy](#seenby)]                                                |  yes      |
| created_at     |  Date                                                                    |  yes      |
| payload_format |  [PayloadFormat](#payloadformat)                                         |  yes      |
| payload        |  [CryptoContainer](#cryptocontainer) OR Array[[Attachment](#attachment)] |  yes      |
| thread_id      |  String                                                                  |           |
| reply_to       |  String                                                                  |           |
| recipients     |  Array[String]                                                           |           |
| integration_id |  String                                                                  |           |
| auto_delete    |  Int                                                                     |           |


## Update Message

> Success Response Example

```json
  {
    "revision": "353203873430636545"
  }
```

### URL

    `TEAM.WORKSPACE.STREAM#MESSAGE.UPDATE`

### URL Params

| Parameter      |  Type                                                                    |  Required |
|----------------|--------------------------------------------------------------------------|-----------|
| team_id        |  String                                                                  |  yes      |
| workspace_id   |  String                                                                  |  yes      |
| message_id     |  String                                                                  |  yes      |
| payload_format |  [PayloadFormat](#payloadformat)                                         |  yes      |
| payload        |  [CryptoContainer](#cryptocontainer) OR Array[[Attachment](#attachment)] |  yes      |


## Delete Message

> Success Response Example

```json
  {
    "revision": "353203873430636545"
  }
```

### URL

    `TEAM.WORKSPACE.STREAM#MESSAGE.DELETE`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |
| workspace_id |  String |  yes      |
| message_id   |  String |  yes      |


## Mark Message Received

> Success Response Example

```json
  {
    "revision": "353203873430636545"
  }
```

### URL

    `TEAM.WORKSPACE.STREAM#MESSAGE.MARK.RECEIVED`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |
| workspace_id |  String |  yes      |
| message_id   |  String |  yes      |
