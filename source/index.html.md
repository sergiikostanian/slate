---
title: API Reference

language_tabs:
  - JSON

toc_footers:
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - Session
  - TeamMember
  - errors

search: true
---

# Introduction

Welcome to the Kittn API! You can use our API to access Kittn API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

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
