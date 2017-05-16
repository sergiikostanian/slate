---
title: API Reference

language_tabs:
  - JSON

toc_footers:
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - Session
  - User
  - Password
  - Team
  - TeamCrypto
  - TeamMember
  - Workspace
  - Participant
  - Stream
  - Storage
  - Crypto
  - Notification
  - Channel
  - BaseTypes
  - errors

search: true
---

# Introduction

Welcome to the StrongBox API! Here you will see awesome introduction soon...
We have examples in JSON, you can view it in the dark area on the right.

# Request

> Request Example

```json  
    {
      "id": "2561B039-1E94-49B9-9A63-6F364E8C7A8E",
      "req": "USER.SESSION#CREATE",
      "args": {
        "login": "pupkin",
        "password": "qwert",
        "ttl": 0,
      }
    }
```

### Request Structure

| Parameter |  Type     |             Description |
|------|---------|----------------------------------|
| id   |  String |  Request UUID                    |
| req  |  String |  Request URL                     |
| args |  JSON   |  Request Parameters, can be empty |


# Response

> Success Response Example

```json
    {
      "rep": "2561B039-1E94-49B9-9A63-6F364E8C7A8E",
      "data": {
          "pin_code": "Lgi7TtJn5Jo1f5aWf66vMQ",
          "salt": "y1H3gF0ZraklErj683dbpA",
          "session_id": "SAvsVn1WoKtucoR188GOug",
          "user_id": "pupkin",
          "ttl": 0,
      },
      "err": null
    }
```

> Error Response Example

```json
    {
      "rep": "787357F1-E3F4-4BFB-90B4-8978FE87C9EE",
      "err": {
        "code": "ERR:INVALID_CREDENTIALS",
        "msg": "Error",
      }
    }
```

### Response Structure

| Parameter |  Type     |             Description |
|------|---------|----------------------------------|
| rep  |  String |  Request UUID for this response  |
| data |  JSON   |  Response data, can be empty     |
| err  |  JSON   |  Error data, can be empty        |
